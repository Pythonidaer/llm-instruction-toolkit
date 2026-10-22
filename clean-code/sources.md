# Sources and coverage

These files adapt Johnny's reviewed Resources summaries in [clean-code-lms](https://github.com/Pythonidaer/clean-code-lms), inspired by Robert C. Martin's *Clean Code*. They are concise working instructions, not a reproduction of the book or a claim of universal authority.

Chapters 1–2 checked: 18 October 2026. Reviewed LMS snapshot: [8155dce](https://github.com/Pythonidaer/clean-code-lms/commit/8155dce34d7c79f53a776258f0e9f280887d6a01).

| Resource | Source file | Rule coverage |
| --- | --- | --- |
| Chapter 1 — My clean-code notes | [chapter-1-notes.md](https://github.com/Pythonidaer/clean-code-lms/blob/8155dce34d7c79f53a776258f0e9f280887d6a01/docs/resources/chapter-1-notes.md) | CC1-1 through CC1-10, in source rule order |
| Chapter 2 — My clean-code notes | [chapter-2-notes.md](https://github.com/Pythonidaer/clean-code-lms/blob/8155dce34d7c79f53a776258f0e9f280887d6a01/docs/resources/chapter-2-notes.md) | CC2-1 through CC2-9, in source rule order |

Chapter 3 was checked separately against [this LMS snapshot](https://github.com/Pythonidaer/clean-code-lms/commit/6ae717e22873995e8ea1bca3782d551a6ef6f4d2). Its [resource notes](https://github.com/Pythonidaer/clean-code-lms/blob/6ae717e22873995e8ea1bca3782d551a6ef6f4d2/docs/resources/chapter-3-notes.md) map to CC3-1 through CC3-12 in source rule order. The draft rules are spread across three source sections: purpose and structure, inputs and effects, and failures and refinement.

The rule text preserves the drafts' intent and adds explicit reasons, checks and qualifications from the surrounding resource explanations. The review workflow operationalizes those existing principles; it does not add chapter coverage.

## Current boundary

- Chapters 1–3 have Resources summaries represented here.
- Later LMS lessons are not automatically promoted to rules before the learner completes and summarizes them.
- Open questions, historical background, glossary expansion and game ideas stay in the LMS Resources as learning material.
- CC1-2 gives the general readability principle; CC2-1 through CC2-9 develop its naming implications. Avoid duplicating both as independent mandates in future consolidated files.

- Chapter 3 develops Chapter 1's function responsibility, duplication and safe-refinement guidance. CC3-5 applies Chapter 2's naming rules to functions. Cross-reference these overlaps rather than reporting the same finding several times.

## Adding a chapter

1. Read the current chapter resource and its qualifications.
2. Add a clearly named chapter rule file with stable IDs, a source link, a rationale and a practical check for each rule.
3. Reconcile overlaps and cross-reference existing rules. Preserve intentional distinctions.
4. Update this source map and the topic index.
5. Validate the guidance on an appropriately scoped example before promoting it into a tool-specific rule or skill workflow.

If the source summaries change, review the affected guidance deliberately rather than assuming the toolkit synchronizes automatically.
