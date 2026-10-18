# Clean Code — code-quality guidance

Help the next reader understand the code and make the next change safely. These draft review heuristics come from my completed chapter notes in the Clean Code LMS. They are a growing working standard, not a finished summary of the entire book.

## Files

| File | Purpose |
| --- | --- |
| [chapter-1-foundations.md](chapter-1-foundations.md) | Readability, focused responsibilities, deliberate boundaries and small checked improvements |
| [chapter-2-meaningful-names.md](chapter-2-meaningful-names.md) | Names that communicate meaning, roles, units and useful context |
| [review-workflow.md](review-workflow.md) | A repeatable way to apply the rules to an authorized task |
| [sources.md](sources.md) | Source notes, coverage and future maintenance |

## Scope and judgment

- Use these rules when writing, reviewing or refactoring code. Choose the relevant rules rather than forcing a change for every rule.
- Understand the intended behavior, existing conventions and public contracts first.
- Prefer evidence about a concrete problem over a stylistic preference. Preserve intentional behavior during refactoring.
- A shorter function, more classes, fewer parameters or the presence of tests does not by itself establish quality.
- Do not convert historical Java conventions into universal JavaScript, TypeScript or React requirements.
- Names may not explain all reasoning: comments can still document constraints, rationale or warnings.
- An abstraction or extraction must clarify a real concept. Similar syntax alone does not establish a shared responsibility.
- Raise material maintenance risks without assuming every organizational problem is an individual developer's fault.

## Growth

Keep chapter files as the traceable source of rules. Use stable IDs when reporting findings or recording exceptions. Chapter 1's general naming rule is expanded by Chapter 2 rather than copied into a second master list.

When another chapter's notes are ready, add its rules, update the index and source map, and reconcile overlaps before creating tool-specific rules or skills. Questions, vocabulary and speculative ideas remain learning material until they support a clear instruction and a way to assess it.
