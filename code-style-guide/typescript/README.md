# TypeScript / JavaScript style guidance

A section-by-section adaptation of Google's [TS/JS Style Guide](https://google.github.io/styleguide/tsguide.html). The original explicitly warns that Google's internal constraints may not fit external projects. This toolkit uses it as a documented baseline, not a universal definition of good code.

## Status and precedence

Active review guidance when this topic is explicitly invoked through the toolkit. The detailed source sections are retained so exceptions and rationale are not lost in a short checklist. This is an adaptation with local review checks; it is not an official Google document.

Apply, in order: the user's authorized task; consuming-project instructions and framework/build contracts; the [React/Vite applicability profile](react-vite-profile.md); applicable detailed source rules; existing conventions for unsettled choices. Record conflicts that cannot be resolved from those priorities. Do not silently convert a preference into a requirement.

Read this overview, the profile and the relevant section files before claiming compliance. For unfamiliar corner cases, read their full source subsections. Do not load unrelated class/decorator guidance for a small function-component change.

## Sections

| # | File | Google section |
| --- | --- | --- |
| 1 | [introduction.md](introduction.md) | Introduction |
| 2 | [source-file-basics.md](source-file-basics.md) | Source file basics |
| 3 | [source-file-structure.md](source-file-structure.md) | Source file structure |
| 4 | [language-features.md](language-features.md) | Language features |
| 5 | [naming.md](naming.md) | Naming |
| 6 | [type-system.md](type-system.md) | Type system |
| 7 | [toolchain.md](toolchain.md) | Toolchain requirements |
| 8 | [comments-and-documentation.md](comments-and-documentation.md) | Comments and documentation |
| 9 | [policies.md](policies.md) | Policies |

[Coverage and provenance](sources.md) maps every source heading to a destination.

## Apply alongside Clean Code

Use [Clean Code overview](../../clean-code/README.md) and [workflow](../../clean-code/review-workflow.md) for bounded findings and design tradeoffs. Avoid duplicate findings when a naming problem fits both rule groups. Styling does not prove correctness, accessibility or sound architecture.

## Attribution

Based on Google's TS/JS Style Guide, Google and contributors, [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/). See [sources](sources.md) for immutable source references, modifications and license details.
