# React/Vite applicability profile

These are **toolkit adaptations**, not claims about what Google requires. Use for React applications built with Vite; inspect the actual project before applying them elsewhere.

## Formatting and JSX

**RV1.** Follow the project's configured formatter. When no formatter exists and adding one is authorized, use Prettier as a practical project default: two-space indentation, semicolons, single quotes in JS/TS, double quotes in JSX, trailing commas where supported and printWidth 80 as a wrapping target. These exact choices are local policy, not a claim of exact Google formatting conformance. Keep formatter options in configuration rather than relying on an LLM's memory.

**RV2.** Keep source readable: expand dense JSX attributes, effects and multi-step handlers; separate statements onto lines. Prefer braces for edited control flow, including single-line guards, even though Google permits a one-line-if exception. A formatter does not identify good component boundaries.

**RV3.** Preserve text-node whitespace, copy, class names, DOM IDs, focus behavior, ARIA, SVG attributes and CSS import order. A formatting diff can still change rendered JSX text; inspect it. Do not hand-wrap SVG path data or user-facing strings solely to meet a line target.

## Modules and framework contracts

**RV4.** Prefer named exports for new ordinary modules, but retain default exports required by frameworks or an existing public contract. Do not rename every file to snake_case: retain the consuming repository's file conventions (including React component names and main.tsx). Google's filename/import conventions are not a migration mandate.

**RV5.** Use type-only imports when required by the project's compiler options. Keep CSS side-effect imports intentional. Do not replace ES modules with namespaces, static container classes or CommonJS.

## Type safety and modern targets

**RV6.** Infer obvious primitive locals. Use named interfaces for reusable object contracts and type aliases for state unions. Annotate boundaries where useful; avoid ceremonial annotations on every callback or JSX return. Do not introduce generic abstractions simply to make a portfolio look advanced. A checked object annotation is preferable to an assertion that hides missing fields; a project may use satisfies when its supported TypeScript version and inference needs justify it.

**RV7.** Narrow nullable DOM lookups and unknown external values at runtime, or document a proven invariant. Types do not validate API responses, localStorage strings or environment values. Avoid using any, non-null assertions or double assertions as a quick way to make checks pass.

**RV8.** Google's #private-field, static-dispatch, quoted-key, decorator and optimizer-related restrictions include environment-specific reasoning. Do not blanket-ban modern runtime-private fields or rewrite quoted JSON-style keys in a Vite app solely because of those restrictions. TypeScript private is a compile-time boundary; #private also enforces privacy at runtime. Check browser targets, compiler settings and security intent. Do not add decorators where the application has no need for them; inspect supported decorator semantics before changing existing framework code.

**RV9.** Treat caught external values as unknown and narrow before reading their properties. Google's assumption that an entire codebase only throws Error objects is not automatically true at third-party boundaries. Throw Error instances in our own code; explain deliberately ignored failures, such as unavailable optional preference persistence. Preserve a useful UI fallback without leaking user form content into logs.

## React-specific review supplement

**RV10.** Keep hooks unconditional and dependencies accurate. Extract a hook only for a coherent stateful responsibility, not to hide a long effect. Retain cleanup for timeouts and matchMedia listeners; use the same listener reference when removing it. Do not remove dependencies or add memoization merely to silence a review concern. This is React-specific guidance, not a section of Google's language guide.

**RV11.** Keep state near its owner. Name state for the domain concept it represents; use boolean names that clearly communicate a condition and include units where useful. Do not rename mechanically across unrelated files.

**RV12.** Extract components only when their responsibilities and props clarify the interface. Keep the entry point focused on mounting. Avoid splitting every element into a file. Prefer cohesive data structures over parallel arrays when records describe the same entity.

## Verification and scope

**RV13.** Use existing checks first. Inspect the consuming project’s package scripts and compiler configuration. Confirm that verification actually checks types rather than only transpiling. Report absent checks accurately; this guidance does not install tooling.

**RV14.** Separate formatting, naming, component/hook extraction and behavior fixes in reviewable steps. Record baseline failures rather than attributing them to the refactor. Check affected user interactions, accessibility, persistence and failure states with appropriate isolated checks. Never send a real form submission as a cleanup test without authorization.

**RV15.** LLM-written application source is maintained source, not generated build output. A draft generated by an assistant still needs human-understandable names, types and review. Preserve deployed behavior and do not publish application changes just because this toolkit was updated.
