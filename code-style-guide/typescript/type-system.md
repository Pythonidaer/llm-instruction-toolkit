# Type system — TS/JS review instructions

Adapted from Google's [TS/JS Style Guide](https://google.github.io/styleguide/tsguide.html#type-system), source blob `89c4630754647df4b2dc3ebabef33276f6eeece1`. Google and contributors; [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/). This adaptation adds application checks, removes presentation wrappers and expands internal links. No Google endorsement is implied.

Read [scope and precedence](README.md) and the [React/Vite applicability profile](react-vite-profile.md) first. The profile's explicit exceptions override the corresponding source rules. Other applicable source rules below retain their original strength. Source examples are illustrative, not additional requirements.

## Application checks

- **TS6.1:** Rely on obvious inference; add annotations where a contract or complex expression becomes clearer.
- **TS6.2:** Prefer interfaces for ordinary object contracts under this profile; use aliases for unions/tuples and other appropriate expressions.
- **TS6.3:** Represent absence explicitly at the use site, and narrow near the boundary.
- **TS6.4:** Prefer unknown to unchecked any; validate external values before using them.
- **TS6.5:** Use simple arrays and types rather than elaborate generic machinery. Use meaningful dictionary key names.
- **TS6.6:** Do not manufacture advanced TypeScript abstractions just to demonstrate TypeScript knowledge.

## Detailed baseline, including source subsections

The retained source text below supplies the detailed rules, rationale and exceptions. Consult it for the specific pattern under review; do not infer missing constraints from the short checks above.

## Type system

<a id="type-inference"></a>

### Type inference

Code *may* rely on type inference as implemented by the TypeScript compiler for
all type expressions (variables, fields, return types, etc).

```ts
const x = 15;  // Type inferred.
```

Leave out type annotations when types are trivially inferred: unexported
variables or parameters initialized to a `string`, `number`, or `boolean`
literal. Type annotations are not considered trivial on exported symbols where
required to be compatible with `isolatedDeclarations`.

```ts
let count: number = 0;  // Bad: type annotation here is redundant

// Bad: Exported interpolation fails isolatedDeclarations.
export const PATH = `/users/${id}`;
```

```ts
let count = 0;

// Good: Explicit type for isolatedDeclarations.
export const PATH: string = `/users/${id}`;
```

Also leave out explicit generic types where they are redundant with the type
annotation.

```ts
// Bad: Specifying '<string>' twice is unnecessary.
const x: Set<string> = new Set<string>();
```

```ts
const x = new Set<string>();             // Preferred when local
export const y: Set<string> = new Set(); // Annotation required for exports
```

For more complex expressions, type annotations can help with readability of the
program:

```ts
// Hard to reason about the type of 'value' without an annotation.
const value = await rpc.getSomeValue().transform();
```

```ts
// Can tell the type of 'value' at a glance.
const value: string[] = await rpc.getSomeValue().transform();
```

Whether an annotation is required is decided by the code reviewer.

<a id="return-types"></a>

#### Return types

Whether to include return type annotations for functions and methods is up to
the code author. Reviewers *may* ask for annotations to clarify complex return
types that are hard to understand. Projects *may* have a local policy to always
require return types, but this is not a general TypeScript style requirement.

There are two benefits to explicitly typing out the implicit return values of
functions and methods:

-   More precise documentation to benefit readers of the code.
-   Surface potential type errors faster in the future if there are code changes
    that change the return type of the function.

<a id="null-vs-undefined"></a>

<a id="undefined-and-null"></a>

### Undefined and null

TypeScript supports `undefined` and `null` types. Nullable types can be
constructed as a union type (`string|null`); similarly with `undefined`. There
is no special syntax for unions of `undefined` and `null`.

TypeScript code can use either `undefined` or `null` to denote absence of a
value, there is no general guidance to prefer one over the other. Many
JavaScript APIs use `undefined` (e.g. `Map.get`), while many DOM and Google APIs
use `null` (e.g. `Element.getAttribute`), so the appropriate absent value
depends on the context.

<a id="nullableundefined-type-aliases"></a>

#### Nullable/undefined type aliases

Type aliases *must not* include `|null` or `|undefined` in a union type.
Nullable aliases typically indicate that null values are being passed around
through too many layers of an application, and this clouds the source of the
original issue that resulted in `null`. They also make it unclear when specific
values on a class or interface might be absent.

Instead, code *must* only add `|null` or `|undefined` when the alias is actually
used. Code *should* deal with null values close to where they arise, using the
below techniques.

```ts
// Bad
type CoffeeResponse = Latte|Americano|undefined;

class CoffeeService {
  getLatte(): CoffeeResponse { ... };
}
```

```ts
// Better
type CoffeeResponse = Latte|Americano;

class CoffeeService {
  getLatte(): CoffeeResponse|undefined { ... };
}
```

<a id="structural-types-vs-nominal-types"></a>

<a id="use-structural-types"></a>

### Use structural types

TypeScript's type system is structural, not nominal. That is, a value matches a
type if it has at least all the properties the type requires and the properties'
types match, recursively.

When providing a structural-based implementation, explicitly include the type at
the declaration of the symbol (this allows more precise type checking and error
reporting).

```ts
const foo: Foo = {
  a: 123,
  b: 'abc',
}
```

```ts
const badFoo = {
  a: 123,
  b: 'abc',
}
```

Use interfaces to define structural types, not classes

```ts
interface Foo {
  a: number;
  b: string;
}

const foo: Foo = {
  a: 123,
  b: 'abc',
}
```

```ts
class Foo {
  readonly a: number;
  readonly b: number;
}

const foo: Foo = {
  a: 123,
  b: 'abc',
}
```

Why?

The "badFoo" object above relies on type inference. Additional fields could be
added to "badFoo" and the type is inferred based on the object itself.

When passing a "badFoo" to a function that takes a "Foo", the error will be at
the function call site, rather than at the object declaration site. This is also
useful when changing the surface of an interface across broad codebases.

```ts
interface Animal {
  sound: string;
  name: string;
}

function makeSound(animal: Animal) {}

/**
 * 'cat' has an inferred type of '{sound: string}'
 */
const cat = {
  sound: 'meow',
};

/**
 * 'cat' does not meet the type contract required for the function, so the
 * TypeScript compiler errors here, which may be very far from where 'cat' is
 * defined.
 */
makeSound(cat);

/**
 * Horse has a structural type and the type error shows here rather than the
 * function call.  'horse' does not meet the type contract of 'Animal'.
 */
const horse: Animal = {
  sound: 'niegh',
};

const dog: Animal = {
  sound: 'bark',
  name: 'MrPickles',
};

makeSound(dog);
makeSound(horse);
```

<a id="interfaces-vs-type-aliases"></a>

<a id="prefer-interfaces"></a>

### Prefer interfaces over type literal aliases

TypeScript supports
[type aliases](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#type-aliases)
for naming a type expression. This can be used to name primitives, unions,
tuples, and any other types.

However, when declaring types for objects, use interfaces instead of a type
alias for the object literal expression.

```ts
interface User {
  firstName: string;
  lastName: string;
}
```

```ts
type User = {
  firstName: string,
  lastName: string,
}
```

Why?

These forms are nearly equivalent, so under the principle of just choosing one
out of two forms to prevent variation, we should choose one. Additionally, there
are also
[interesting technical reasons to prefer interface](https://ncjamieson.com/prefer-interfaces/).
That page quotes the TypeScript team lead: "Honestly, my take is that it should
really just be interfaces for anything that they can model. There is no benefit
to type aliases when there are so many issues around display/perf."

<a id="arrayt-type"></a>

### `Array<T>` Type

For simple types (containing just alphanumeric characters and dot), use the
syntax sugar for arrays, `T[]` or `readonly T[]`, rather than the longer form
`Array<T>` or `ReadonlyArray<T>`.

For multi-dimensional non-`readonly` arrays of simple types, use the syntax
sugar form (`T[][]`, `T[][][]`, and so on) rather than the longer form.

For anything more complex, use the longer form `Array<T>`.

These rules apply at each level of nesting, i.e. a simple `T[]` nested in a more
complex type would still be spelled as `T[]`, using the syntax sugar.

```ts
let a: string[];
let b: readonly string[];
let c: ns.MyObj[];
let d: string[][];
let e: Array<{n: number, s: string}>;
let f: Array<string|number>;
let g: ReadonlyArray<string|number>;
let h: InjectionToken<string[]>;  // Use syntax sugar for nested types.
let i: ReadonlyArray<string[]>;
let j: Array<readonly string[]>;
```

```ts
let a: Array<string>;  // The syntax sugar is shorter.
let b: ReadonlyArray<string>;
let c: Array<ns.MyObj>;
let d: Array<string[]>;
let e: {n: number, s: string}[];  // The braces make it harder to read.
let f: (string|number)[];         // Likewise with parens.
let g: readonly (string | number)[];
let h: InjectionToken<Array<string>>;
let i: readonly string[][];
let j: (readonly string[])[];
```

<a id="indexable-key-string-type"></a>

### Indexable types / index signatures (`{[key: string]: T}`)

In JavaScript, it's common to use an object as an associative array (aka "map",
"hash", or "dict"). Such objects can be typed using an
[index signature](https://www.typescriptlang.org/docs/handbook/2/objects.html#index-signatures)
(`[k: string]: T`) in TypeScript:

```ts
const fileSizes: {[fileName: string]: number} = {};
fileSizes['readme.txt'] = 541;
```

In TypeScript, provide a meaningful label for the key. (The label only exists
for documentation; it's unused otherwise.)

```ts
const users: {[key: string]: number} = ...;
```

```ts
const users: {[userName: string]: number} = ...;
```

> Rather than using one of these, consider using the ES6 `Map` and `Set` types
> instead. JavaScript objects have
> [surprising undesirable behaviors](http://2ality.com/2012/01/objects-as-maps.html)
> and the ES6 types more explicitly convey your intent. Also, `Map`s can be
> keyed by—and `Set`s can contain—types other than `string`.

TypeScript's built-in `Record<Keys, ValueType>` type allows constructing types
with a defined set of keys. This is distinct from associative arrays in that the
keys are statically known. See advice on that
[below](https://google.github.io/styleguide/tsguide.html#mapped-conditional-types).

<a id="mapped-conditional-types"></a>

### Mapped and conditional types

TypeScript's
[mapped types](https://www.typescriptlang.org/docs/handbook/2/mapped-types.html)
and
[conditional types](https://www.typescriptlang.org/docs/handbook/2/conditional-types.html)
allow specifying new types based on other types. TypeScript's standard library
includes several type operators based on these (`Record`, `Partial`, `Readonly`
etc).

These type system features allow succinctly specifying types and constructing
powerful yet type safe abstractions. They come with a number of drawbacks
though:

*   Compared to explicitly specifying properties and type relations (e.g. using
    interfaces and extension, see below for an example), type operators require
    the reader to mentally evaluate the type expression. This can make programs
    substantially harder to read, in particular combined with type inference and
    expressions crossing file boundaries.
*   Mapped & conditional types' evaluation model, in particular when combined
    with type inference, is underspecified, not always well understood, and
    often subject to change in TypeScript compiler versions. Code can
    "accidentally" compile or seem to give the right results. This increases
    future support cost of code using type operators.
*   Mapped & conditional types are most powerful when deriving types from
    complex and/or inferred types. On the flip side, this is also when they are
    most prone to create hard to understand and maintain programs.
*   Some language tooling does not work well with these type system features.
    E.g. your IDE's find references (and thus rename property refactoring) will
    not find properties in a `Pick<T, Keys>` type, and Code Search won't
    hyperlink them. *

The style recommendation is:

*   Always use the simplest type construct that can possibly express your code.
*   A little bit of repetition or verbosity is often much cheaper than the long
    term cost of complex type expressions.
*   Mapped & conditional types may be used, subject to these considerations.

For example, TypeScript's built-in `Pick<T, Keys>` type allows creating a new
type by subsetting another type `T`, but simple interface extension can often be
easier to understand.

```ts
interface User {
  shoeSize: number;
  favoriteIcecream: string;
  favoriteChocolate: string;
}

// FoodPreferences has favoriteIcecream and favoriteChocolate, but not shoeSize.
type FoodPreferences = Pick<User, 'favoriteIcecream'|'favoriteChocolate'>;
```

This is equivalent to spelling out the properties on `FoodPreferences`:

```ts
interface FoodPreferences {
  favoriteIcecream: string;
  favoriteChocolate: string;
}
```

To reduce duplication, `User` could extend `FoodPreferences`, or (possibly
better) nest a field for food preferences:

```ts
interface FoodPreferences { /* as above */ }
interface User extends FoodPreferences {
  shoeSize: number;
  // also includes the preferences.
}
```

Using interfaces here makes the grouping of properties explicit, improves IDE
support, allows better optimization, and arguably makes the code easier to
understand.

<a id="any"></a>

### `any` Type

TypeScript's `any` type is a super and subtype of all other types, and allows
dereferencing all properties. As such, `any` is dangerous - it can mask severe
programming errors, and its use undermines the value of having static types in
the first place.

**Consider *not* to use `any`.** In circumstances where you want to use `any`,
consider one of:

-   [Provide a more specific type](https://google.github.io/styleguide/tsguide.html#any-specific)
-   [Use `unknown`](https://google.github.io/styleguide/tsguide.html#any-unknown)
-   [Suppress the lint warning and document why](https://google.github.io/styleguide/tsguide.html#any-suppress)

<a id="any-specific"></a>

#### Providing a more specific type

Use interfaces , an inline object type, or a type alias:

```ts
// Use declared interfaces to represent server-side JSON.
declare interface MyUserJson {
  name: string;
  email: string;
}

// Use type aliases for types that are repetitive to write.
type MyType = number|string;

// Or use inline object types for complex returns.
function getTwoThings(): {something: number, other: string} {
  // ...
  return {something, other};
}

// Use a generic type, where otherwise a library would say `any` to represent
// they don't care what type the user is operating on (but note "Return type
// only generics" below).
function nicestElement<T>(items: T[]): T {
  // Find the nicest element in items.
  // Code can also put constraints on T, e.g. <T extends HTMLElement>.
}
```

<a id="any-unknown"></a>

#### Using `unknown` over `any`

The `any` type allows assignment into any other type and dereferencing any
property off it. Often this behaviour is not necessary or desirable, and code
just needs to express that a type is unknown. Use the built-in type `unknown` in
that situation — it expresses the concept and is much safer as it does not allow
dereferencing arbitrary properties.

```ts
// Can assign any value (including null or undefined) into this but cannot
// use it without narrowing the type or casting.
const val: unknown = value;
```

```ts
const danger: any = value /* result of an arbitrary expression */;
danger.whoops();  // This access is completely unchecked!
```

To safely use `unknown` values, narrow the type using a
[type guard](https://www.typescriptlang.org/docs/handbook/advanced-types.html#type-guards-and-differentiating-types)

<a id="any-suppress"></a>

#### Suppressing `any` lint warnings

Sometimes using `any` is legitimate, for example in tests to construct a mock
object. In such cases, add a comment that suppresses the lint warning, and
document why it is legitimate.

```ts
// This test only needs a partial implementation of BookService, and if
// we overlooked something the test will fail in an obvious way.
// This is an intentionally unsafe partial mock
// tslint:disable-next-line:no-any
const mockBookService = ({get() { return mockBook; }} as any) as BookService;
// Shopping cart is not used in this test
// tslint:disable-next-line:no-any
const component = new MyComponent(mockBookService, /* unused ShoppingCart */ null as any);
```

<a id="empty-interface-type"></a>

### `{}` Type

The `{}` type, also known as an *empty interface* type, represents an interface
with no properties. An empty interface type has no specified properties and
therefore any non-nullish value is assignable to it.

```ts
let player: {};

player = {
  health: 50,
}; // Allowed.

console.log(player.health) // Property 'health' does not exist on type '{}'.
```

```ts
function takeAnything(obj:{}) {

}

takeAnything({});
takeAnything({ a: 1, b: 2 });
```

Google3 code **should not** use `{}` for most use cases. `{}` represents any
non-nullish primitive or object type, which is rarely appropriate. Prefer one of
the following more-descriptive types:

*   `unknown` can hold any value, including `null` or `undefined`, and is
    generally more appropriate for opaque values.
*   `Record<string, T>` is better for dictionary-like objects, and provides
    better type safety by being explicit about the type `T` of contained values
    (which may itself be `unknown`).
*   `object` excludes primitives as well, leaving only non-nullish functions and
    objects, but without any other assumptions about what properties may be
    available.

<a id="tuple-types"></a>

### Tuple types

If you are tempted to create a Pair type, instead use a tuple type:

```ts
interface Pair {
  first: string;
  second: string;
}
function splitInHalf(input: string): Pair {
  ...
  return {first: x, second: y};
}
```

```ts
function splitInHalf(input: string): [string, string] {
  ...
  return [x, y];
}

// Use it like:
const [leftHalf, rightHalf] = splitInHalf('my string');
```

However, often it's clearer to provide meaningful names for the properties.

If declaring an `interface` is too heavyweight, you can use an inline object
literal type:

```ts
function splitHostPort(address: string): {host: string, port: number} {
  ...
}

// Use it like:
const address = splitHostPort(userAddress);
use(address.port);

// You can also get tuple-like behavior using destructuring:
const {host, port} = splitHostPort(userAddress);
```

<a id="wrapper-types"></a>

### Wrapper types

There are a few types related to JavaScript primitives that *should not* ever be
used:

-   `String`, `Boolean`, and `Number` have slightly different meaning from the
    corresponding primitive types `string`, `boolean`, and `number`. Always use
    the lowercase version.
-   `Object` has similarities to both `{}` and `object`, but is slightly looser.
    Use `{}` for a type that include everything except `null` and `undefined`,
    or lowercase `object` to further exclude the other primitive types (the
    three mentioned above, plus `symbol` and `bigint`).

Further, never invoke the wrapper types as constructors (with `new`).

<a id="return-type-only-generics"></a>

### Return type only generics

Avoid creating APIs that have return type only generics. When working with
existing APIs that have return type only generics always explicitly specify the
generics.

<a id="appendices-style-related-tools"></a>

<a id="toolchain-requirements"></a>
