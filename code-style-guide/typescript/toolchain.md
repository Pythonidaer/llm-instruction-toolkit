# Toolchain requirements — TS/JS review instructions

Adapted from Google's [TS/JS Style Guide](https://google.github.io/styleguide/tsguide.html#toolchain-requirements), source blob `89c4630754647df4b2dc3ebabef33276f6eeece1`. Google and contributors; [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/). This adaptation adds application checks, removes presentation wrappers and expands internal links. No Google endorsement is implied.

Read [scope and precedence](README.md) and the [React/Vite applicability profile](react-vite-profile.md) first. The profile's explicit exceptions override the corresponding source rules. Other applicable source rules below retain their original strength. Source examples are illustrative, not additional requirements.

## Application checks

- **TS7.1:** Run the consuming project's actual type-check/build commands; a transpiler-only build is not sufficient type verification.
- **TS7.2:** Do not silence errors with broad suppression directives.
- **TS7.3:** Treat named Google conformance tools as source context, not dependencies to install automatically.
- **TS7.4:** Use the existing formatter/linter configuration first; add project tooling only in a separately authorized implementation pass.

## Detailed baseline, including source subsections

The retained source text below supplies the detailed rules, rationale and exceptions. Consult it for the specific pattern under review; do not infer missing constraints from the short checks above.

## Toolchain requirements

Google style requires using a number of tools in specific ways, outlined here.

<a id="google-format"></a>
<a id="use-the-google3-formatter"></a>
<a id="source-code-formatting"></a>
<a id="appendices-clang-format"></a>
<a id="formatting"></a>
<a id="formatting-array-literals"></a>
<a id="formatting-block-indentation"></a>
<a id="formatting-column-limit"></a>
<a id="formatting-empty-blocks"></a>
<a id="formatting-function-expressions"></a>
<a id="formatting-nonempty-blocks"></a>
<a id="formatting-object-literals"></a>
<a id="formatting-one-statement-perline"></a>
<a id="formatting-statements"></a>
<a id="formatting-switch-statements"></a>
<a id="formatting-vertical-whitespace"></a>
<a id="formatting-whitespace"></a>

<a id="typescript-compiler"></a>

### TypeScript compiler

All TypeScript files must pass type checking using the standard tool chain.

<a id="ts-ignore"></a>

#### @ts-ignore

Do not use `@ts-ignore` nor the variants `@ts-expect-error` or `@ts-nocheck`.

Why?

They superficially seem to be an easy way to "fix" a compiler error, but in
practice, a specific compiler error is often caused by a larger problem that can
be fixed more directly.

For example, if you are using `@ts-ignore` to suppress a type error, then it's
hard to predict what types the surrounding code will end up seeing. For many
type errors, the advice in [how to best use `any`](https://google.github.io/styleguide/tsguide.html#any) is useful.

You may use `@ts-expect-error` in unit tests, though you generally *should not*.
`@ts-expect-error` suppresses all errors. It's easy to accidentally over-match
and suppress more serious errors. Consider one of:

-   When testing APIs that need to deal with unchecked values at runtime, add
    casts to the expected type or to `any` and add an explanatory comment. This
    limits error suppression to a single expression.
-   Suppress the lint warning and document why, similar to
    [suppressing `any` lint warnings](https://google.github.io/styleguide/tsguide.html#any-suppress).

<a id="appendices-conformance-framework"></a>

<a id="conformance"></a>

### Conformance

Google TypeScript includes several *conformance frameworks*,
[tsetse](https://tsetse.info) and [tsec](https://github.com/google/tsec).

These rules are commonly used to enforce critical restrictions (such as defining
globals, which could break the codebase) and security patterns (such as using
`eval` or assigning to `innerHTML`), or more loosely to improve code quality.

Google-style TypeScript must abide by any applicable global or framework-local
conformance rules.

<a id="jsdoc"></a>
<a id="formatting-comments"></a>

<a id="comments-documentation"></a>
