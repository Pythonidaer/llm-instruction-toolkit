# Sources, license and coverage

## Source identity

Google and contributors, **TS/JS Style Guide**.
Published: https://google.github.io/styleguide/tsguide.html
Immutable source bytes: https://api.github.com/repos/google/styleguide/git/blobs/89c4630754647df4b2dc3ebabef33276f6eeece1
Source blob SHA: 89c4630754647df4b2dc3ebabef33276f6eeece1

The blob SHA identifies file content rather than a commit. The [maintained Markdown source](https://github.com/google/styleguide/blob/gh-pages/tsguide.md) may change; use the Git blob API above to retrieve the reviewed version.

License: [Creative Commons Attribution 3.0 Unported](https://creativecommons.org/licenses/by/3.0/), as provided in [google/styleguide LICENSE](https://github.com/google/styleguide/blob/gh-pages/LICENSE). The original license text is retained at [LICENSE.google.txt](LICENSE.google.txt). Attribution and original notices are retained. No endorsement is implied.

## Adaptation decisions

The original document was split along its nine top-level sections. Each file retains detailed source rules and examples and adds stable-ID application checks. Presentation-only HTML wrappers/comments were removed, and local source links were expanded to the published guide. Named anchors, subsection prose, examples and qualifications remain. The opening applicability warning is reflected in the topic README and React/Vite profile.

The React/Vite profile is separately labelled toolkit guidance and records exceptions for framework exports, filenames, formatting, runtime privacy/optimizer assumptions and external error boundaries. It adds general React/JSX review guidance. It does not claim Google authored React architecture guidance. Google's source can contain historical tooling references; do not install deprecated tools or adopt compiler explanations without checking the consuming project's actual toolchain.

## Coverage map

Every heading (including nested fifth-level headings) from the retained source sections maps below. This is a coverage inventory, not a claim that every rule has been tested in a consuming project. Read the applicable subsection in full before enforcing it.

| Source heading | Destination |
| --- | --- |
| Introduction | [introduction](introduction.md) |
| Terminology notes | [introduction](introduction.md) |
| Guide notes | [introduction](introduction.md) |
| Source file basics | [source-file-basics](source-file-basics.md) |
| File encoding: UTF-8 | [source-file-basics](source-file-basics.md) |
| Whitespace characters | [source-file-basics](source-file-basics.md) |
| Special escape sequences | [source-file-basics](source-file-basics.md) |
| Non-ASCII characters | [source-file-basics](source-file-basics.md) |
| Source file structure | [source-file-structure](source-file-structure.md) |
| Copyright information | [source-file-structure](source-file-structure.md) |
| `@fileoverview` JSDoc | [source-file-structure](source-file-structure.md) |
| Imports | [source-file-structure](source-file-structure.md) |
| Import paths | [source-file-structure](source-file-structure.md) |
| Namespace versus named imports | [source-file-structure](source-file-structure.md) |
| Special case: Apps JSPB protos | [source-file-structure](source-file-structure.md) |
| Renaming imports | [source-file-structure](source-file-structure.md) |
| Exports | [source-file-structure](source-file-structure.md) |
| Export visibility | [source-file-structure](source-file-structure.md) |
| Mutable exports | [source-file-structure](source-file-structure.md) |
| Container classes | [source-file-structure](source-file-structure.md) |
| Import and export type | [source-file-structure](source-file-structure.md) |
| Import type | [source-file-structure](source-file-structure.md) |
| Export type | [source-file-structure](source-file-structure.md) |
| Dynamic `import()` type | [source-file-structure](source-file-structure.md) |
| Use modules not namespaces | [source-file-structure](source-file-structure.md) |
| Language features | [language-features](language-features.md) |
| Local variable declarations | [language-features](language-features.md) |
| Use const and let | [language-features](language-features.md) |
| One variable per declaration | [language-features](language-features.md) |
| Array literals | [language-features](language-features.md) |
| Do not use the `Array` constructor | [language-features](language-features.md) |
| Do not define properties on arrays | [language-features](language-features.md) |
| Array destructuring | [language-features](language-features.md) |
| Object literals | [language-features](language-features.md) |
| Do not use the `Object` constructor | [language-features](language-features.md) |
| Iterating objects | [language-features](language-features.md) |
| Using spread syntax | [language-features](language-features.md) |
| Computed property names | [language-features](language-features.md) |
| Object destructuring | [language-features](language-features.md) |
| Classes | [language-features](language-features.md) |
| Class declarations | [language-features](language-features.md) |
| Don't create member variables only used in constructors | [language-features](language-features.md) |
| Class method declarations | [language-features](language-features.md) |
| Overriding toString | [language-features](language-features.md) |
| Static methods | [language-features](language-features.md) |
| Avoid private static methods | [language-features](language-features.md) |
| Do not rely on dynamic dispatch | [language-features](language-features.md) |
| Avoid static `this` references | [language-features](language-features.md) |
| Constructors | [language-features](language-features.md) |
| Class members | [language-features](language-features.md) |
| No #private fields | [language-features](language-features.md) |
| Use readonly | [language-features](language-features.md) |
| Parameter properties | [language-features](language-features.md) |
| Field initializers | [language-features](language-features.md) |
| Properties used outside of class lexical scope | [language-features](language-features.md) |
| Getters and setters | [language-features](language-features.md) |
| Computed properties | [language-features](language-features.md) |
| Visibility | [language-features](language-features.md) |
| Disallowed class patterns | [language-features](language-features.md) |
| Do not manipulate `prototype`s directly | [language-features](language-features.md) |
| Functions | [language-features](language-features.md) |
| Terminology | [language-features](language-features.md) |
| Prefer function declarations for named functions | [language-features](language-features.md) |
| Nested functions | [language-features](language-features.md) |
| Do not use function expressions | [language-features](language-features.md) |
| Arrow function bodies | [language-features](language-features.md) |
| Rebinding `this` | [language-features](language-features.md) |
| Prefer passing arrow functions as callbacks | [language-features](language-features.md) |
| Arrow functions as properties | [language-features](language-features.md) |
| Event handlers | [language-features](language-features.md) |
| Parameter initializers | [language-features](language-features.md) |
| Prefer rest and spread when appropriate | [language-features](language-features.md) |
| Formatting functions | [language-features](language-features.md) |
| Function Length | [language-features](language-features.md) |
| this | [language-features](language-features.md) |
| Primitive literals | [language-features](language-features.md) |
| String literals | [language-features](language-features.md) |
| Use single quotes | [language-features](language-features.md) |
| No line continuations | [language-features](language-features.md) |
| Template literals | [language-features](language-features.md) |
| Number literals | [language-features](language-features.md) |
| Type coercion | [language-features](language-features.md) |
| Coercing to numbers | [language-features](language-features.md) |
| Implicit coercion | [language-features](language-features.md) |
| Control structures | [language-features](language-features.md) |
| Control flow statements and blocks | [language-features](language-features.md) |
| Assignment in control statements | [language-features](language-features.md) |
| Iterating containers | [language-features](language-features.md) |
| Grouping parentheses | [language-features](language-features.md) |
| Exception handling | [language-features](language-features.md) |
| Instantiate errors using `new` | [language-features](language-features.md) |
| Only throw errors | [language-features](language-features.md) |
| Catching and rethrowing | [language-features](language-features.md) |
| Empty catch blocks | [language-features](language-features.md) |
| ErrorOptions cause must be an Error object | [language-features](language-features.md) |
| Switch statements | [language-features](language-features.md) |
| Equality checks | [language-features](language-features.md) |
| Type and non-nullability assertions | [language-features](language-features.md) |
| Type assertion syntax | [language-features](language-features.md) |
| Double assertions | [language-features](language-features.md) |
| Type assertions and object literals | [language-features](language-features.md) |
| Keep try blocks focused | [language-features](language-features.md) |
| Decorators | [language-features](language-features.md) |
| Disallowed features | [language-features](language-features.md) |
| Wrapper objects for primitive types | [language-features](language-features.md) |
| Automatic Semicolon Insertion | [language-features](language-features.md) |
| Const enums | [language-features](language-features.md) |
| Debugger statements | [language-features](language-features.md) |
| `with` | [language-features](language-features.md) |
| Dynamic code evaluation | [language-features](language-features.md) |
| Non-standard features | [language-features](language-features.md) |
| Modifying built-in objects | [language-features](language-features.md) |
| Naming | [naming](naming.md) |
| Identifiers | [naming](naming.md) |
| Naming style | [naming](naming.md) |
| Descriptive names | [naming](naming.md) |
| Camel case | [naming](naming.md) |
| Dollar sign | [naming](naming.md) |
| Rules by identifier type | [naming](naming.md) |
| Type parameters | [naming](naming.md) |
| Test names | [naming](naming.md) |
| Underscore (`_`) prefix/suffix | [naming](naming.md) |
| Imports | [naming](naming.md) |
| Constants | [naming](naming.md) |
| Aliases | [naming](naming.md) |
| Type system | [type-system](type-system.md) |
| Type inference | [type-system](type-system.md) |
| Return types | [type-system](type-system.md) |
| Undefined and null | [type-system](type-system.md) |
| Nullable/undefined type aliases | [type-system](type-system.md) |
| Use structural types | [type-system](type-system.md) |
| Prefer interfaces over type literal aliases | [type-system](type-system.md) |
| `Array<T>` Type | [type-system](type-system.md) |
| Indexable types / index signatures (`{[key: string]: T}`) | [type-system](type-system.md) |
| Mapped and conditional types | [type-system](type-system.md) |
| `any` Type | [type-system](type-system.md) |
| Providing a more specific type | [type-system](type-system.md) |
| Using `unknown` over `any` | [type-system](type-system.md) |
| Suppressing `any` lint warnings | [type-system](type-system.md) |
| `{}` Type | [type-system](type-system.md) |
| Tuple types | [type-system](type-system.md) |
| Wrapper types | [type-system](type-system.md) |
| Return type only generics | [type-system](type-system.md) |
| Toolchain requirements | [toolchain](toolchain.md) |
| TypeScript compiler | [toolchain](toolchain.md) |
| @ts-ignore | [toolchain](toolchain.md) |
| Conformance | [toolchain](toolchain.md) |
| Comments and documentation | [comments-and-documentation](comments-and-documentation.md) |
| JSDoc versus comments | [comments-and-documentation](comments-and-documentation.md) |
| Multi-line comments | [comments-and-documentation](comments-and-documentation.md) |
| JSDoc general form | [comments-and-documentation](comments-and-documentation.md) |
| Markdown | [comments-and-documentation](comments-and-documentation.md) |
| JSDoc tags | [comments-and-documentation](comments-and-documentation.md) |
| Line wrapping | [comments-and-documentation](comments-and-documentation.md) |
| Document all top-level exports of modules | [comments-and-documentation](comments-and-documentation.md) |
| Class comments | [comments-and-documentation](comments-and-documentation.md) |
| Method and function comments | [comments-and-documentation](comments-and-documentation.md) |
| Parameter property comments | [comments-and-documentation](comments-and-documentation.md) |
| JSDoc type annotations | [comments-and-documentation](comments-and-documentation.md) |
| Make comments that actually add information | [comments-and-documentation](comments-and-documentation.md) |
| Comments when calling a function | [comments-and-documentation](comments-and-documentation.md) |
| Place documentation prior to decorators | [comments-and-documentation](comments-and-documentation.md) |
| Policies | [policies](policies.md) |
| Consistency | [policies](policies.md) |
| Reformatting existing code | [policies](policies.md) |
| Deprecation | [policies](policies.md) |
| Generated code: mostly exempt | [policies](policies.md) |
| Style guide goals | [policies](policies.md) |
