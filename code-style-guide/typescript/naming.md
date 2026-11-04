# Naming — TS/JS review instructions

Adapted from Google's [TS/JS Style Guide](https://google.github.io/styleguide/tsguide.html#naming), source blob `89c4630754647df4b2dc3ebabef33276f6eeece1`. Google and contributors; [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/). This adaptation adds application checks, removes presentation wrappers and expands internal links. No Google endorsement is implied.

Read [scope and precedence](README.md) and the [React/Vite applicability profile](react-vite-profile.md) first. The profile's explicit exceptions override the corresponding source rules. Other applicable source rules below retain their original strength. Source examples are illustrative, not additional requirements.

## Application checks

- **TS5.1:** Name domain concepts, states and units rather than implementation trivia.
- **TS5.2:** Use PascalCase for components/types, lowerCamelCase for ordinary variables/functions and CONSTANT_CASE for intended module-level constants.
- **TS5.3:** Do not uppercase every const or invent interface prefixes.
- **TS5.4:** Keep short names only when their small scope makes the meaning obvious; qualify ambiguous state names such as index or length.
- **TS5.5:** Respect external API names, framework requirements and the source's unused-parameter exceptions.

## Detailed baseline, including source subsections

The retained source text below supplies the detailed rules, rationale and exceptions. Consult it for the specific pattern under review; do not infer missing constraints from the short checks above.

## Naming

<a id="identifiers"></a>

### Identifiers

Identifiers *must* use only ASCII letters, digits, underscores (for constants
and structured test method names), and (rarely) the '$' sign.

<a id="naming-style"></a>

#### Naming style

TypeScript expresses information in types, so names *should not* be decorated
with information that is included in the type. (See also
[Testing Blog](https://testing.googleblog.com/2017/10/code-health-identifiernamingpostforworl.html)
for more about what not to include.)

Some concrete examples of this rule:

*   Do not use trailing or leading underscores for private properties or
    methods.
*   Do not use the `opt_` prefix for optional parameters.
    *   For accessors, see [accessor rules](https://google.github.io/styleguide/tsguide.html#classes-getters-and-setters) below.
*   Do not mark interfaces specially (~~`IMyInterface`~~ or
    ~~`MyFooInterface`~~) unless it's idiomatic in its environment. When
    introducing an interface for a class, give it a name that expresses why the
    interface exists in the first place (e.g. `class TodoItem` and
    `interface TodoItemStorage` if the interface expresses the format used for
    storage/serialization in JSON).
*   Suffixing `Observable`s with `$` is a common external convention and can
    help resolve confusion regarding observable values vs concrete values.
    Judgement on whether this is a useful convention is left up to individual
    teams, but *should* be consistent within projects.

<a id="identifiers-abbreviations"></a>

<a id="descriptive-names"></a>

#### Descriptive names

Names *must* be descriptive and clear to a new reader. Do not use abbreviations
that are ambiguous or unfamiliar to readers outside your project, and do not
abbreviate by deleting letters within a word.

*   **Exception:** Variables that are in scope for 10 lines or fewer, including
    arguments that are *not* part of an exported API, *may* use short (e.g.
    single letter) variable names.

```ts
// Good identifiers:
errorCount          // No abbreviation.
dnsConnectionIndex  // Most people know what "DNS" stands for.
referrerUrl         // Ditto for "URL".
customerId          // "Id" is both ubiquitous and unlikely to be misunderstood.
```

```ts
// Disallowed identifiers:
n                   // Meaningless.
nErr                // Ambiguous abbreviation.
nCompConns          // Ambiguous abbreviation.
wgcConnections      // Only your group knows what this stands for.
pcReader            // Lots of things can be abbreviated "pc".
cstmrId             // Deletes internal letters.
kSecondsPerDay      // Do not use Hungarian notation.
customerID          // Incorrect camelcase of "ID".
```

<a id="naming-camel-case-defined"></a>

<a id="camel-case"></a>

#### Camel case

Treat abbreviations like acronyms in names as whole words, i.e. use
`loadHttpUrl`, not ~~`loadHTTPURL`~~, unless required by a platform name (e.g.
`XMLHttpRequest`).

<a id="identifiers-dollar-sign"></a>

#### Dollar sign

Identifiers *should not* generally use `$`, except when required by naming
conventions for third party frameworks. [See above](https://google.github.io/styleguide/tsguide.html#naming-style) for more on
using `$` with `Observable` values.

<a id="naming-class-names"></a>
<a id="naming-method-names"></a>
<a id="naming-enum-names"></a>
<a id="naming-constant-names"></a>
<a id="naming-local-variable-names"></a>
<a id="naming-non-constant-field-names"></a>
<a id="naming-parameter-names"></a>

<a id="naming-rules-by-identifier-type"></a>

### Rules by identifier type

Most identifier names should follow the casing in the table below, based on the
identifier's type.



| Style            | Category |
| ---------------- | -------- |
| `UpperCamelCase` | class / interface / type / enum / decorator / type parameters / component functions in TSX / JSXElement type parameter |
| `lowerCamelCase` | variable / parameter / function / method / property / module alias |
| `CONSTANT_CASE`  | global constant values, including enum values. See [Constants](https://google.github.io/styleguide/tsguide.html#identifiers-constants) below. |
| `#ident`         | private identifiers are never used. |



<a id="naming-template-parameter-names"></a>

<a id="identifiers-type-parameters"></a>

#### Type parameters

Type parameters, like in `Array<T>`, *may* use a single upper case character
(`T`) or `UpperCamelCase`.

<a id="identifiers-test-names"></a>

#### Test names

Test method names inxUnit-style test frameworks *may* be structured with `_`
separators, e.g. `testX_whenY_doesZ()`.

<a id="identifiers-underscore-prefix-suffix"></a>

#### Underscore (`_`) prefix/suffix

An underscore prefix indicates a syntactically-required identifier will not be
used. It is encouraged to provide a meaningful name after the underscore, but a
standalone `_` is allowed.

```ts
(_projectId, api) => of(!params.disabledApis.includes(api));

[].filter((_, i) => i % 2 === 0);

for await (const _item of getAllTheThings()) {
  count++;
}

using _cleanupFoo = foo();
```

Do not use this style for trailing unused parameters, those should be omitted.

Trailing unused parameters are allowed on methods that are specifically intended
to be overridden.

```ts
[].filter((element, _index) => !element.hasSomeProperty());
```

```ts
[].filter(element => !element.hasSomeProperty());
```

Identifiers must not use `_` as a suffix.

> Tip: If you only need some of the elements from an array (or TypeScript
> tuple), you can insert extra commas in a destructuring statement to ignore
> in-between elements:
>
> ```ts
> const [a, , b] = [1, 5, 10];  // a <- 1, b <- 10
> ```

<a id="identifiers-imports"></a>

#### Imports

Module namespace imports are `lowerCamelCase` while files are `snake_case`,
which means that imports correctly will not match in casing style, such as

```ts
import * as fooBar from './foo_bar';
```

Some libraries might commonly use a namespace import prefix that violates this
naming scheme, but overbearingly common open source use makes the violating
style more readable. The only libraries that currently fall under this exception
are:

*   [jquery](https://jquery.com/), using the `$` prefix
*   [threejs](https://threejs.org/), using the `THREE` prefix

<a id="identifiers-constants"></a>

#### Constants

**Immutable**: `CONSTANT_CASE` indicates that a value is *intended* to not be
changed, and *may* be used for values that can technically be modified (i.e.
values that are not deeply frozen) to indicate to users that they must not be
modified.

```ts
const UNIT_SUFFIXES = {
  'milliseconds': 'ms',
  'seconds': 's',
};
// Even though per the rules of JavaScript UNIT_SUFFIXES is
// mutable, the uppercase shows users to not modify it.
```

A constant can also be a `static readonly` property of a class.

```ts
class Foo {
  private static readonly MY_SPECIAL_NUMBER = 5;

  bar() {
    return 2 * Foo.MY_SPECIAL_NUMBER;
  }
}
```

**Global**: Only symbols declared on the module level, static fields of module
level classes, and values of module level enums, *may* use `CONST_CASE`. If a
value can be instantiated more than once over the lifetime of the program (e.g.
a local variable declared within a function, or a static field on a class nested
in a function) then it *must* use `lowerCamelCase`.
[Local-scope aliases](https://google.github.io/styleguide/tsguide.html#aliases) are excepted and should use the format of the
existing identifier.

If a value is an arrow function that implements an interface, then it *may* be
declared `lowerCamelCase`.

<a id="naming-local-aliases"></a>

<a id="aliases"></a>

#### Aliases

When creating a local-scope alias of an existing symbol, use the format of the
existing identifier. The local alias *must* match the existing naming and format
of the source. For variables use `const` for your local aliases, and for class
fields use the `readonly` attribute.

> Note: If you're creating an alias just to expose it to a template in your
> framework of choice, remember to also apply the proper
> [access modifiers](https://google.github.io/styleguide/tsguide.html#properties-used-outside-of-class-lexical-scope).

```ts
const {BrewStateEnum} = SomeType;
const CAPACITY = 5;

class Teapot {
  readonly BrewStateEnum = BrewStateEnum;
  readonly CAPACITY = CAPACITY;
}
```

<a id="type-system"></a>
