# Chapter 2 — Meaningful names

Status: draft heuristics derived from [Chapter 2 resource notes](https://github.com/Pythonidaer/clean-code-lms/blob/main/docs/resources/chapter-2-notes.md). This expands CC1-2. Apply with the [scope and qualifications](README.md#scope-and-judgment).

## CC2-1 — Name the meaning, role and units

Name what a value represents or what an operation does. Include units when they matter. Distinguish roles such as source and destination.

Why: a reader should not have to reconstruct the concept from usage.

Check: compare `d` with `daysSinceModification`, or `a1` and `a2` with `source` and `destination`. The improvement must match the actual meaning, not just increase length.

## CC2-2 — Make vocabulary consistent with meaning

Use the same established term for equivalent concepts and different terms for genuinely different concepts.

Why: arbitrary synonyms require mental translation; one term used for different operations can mislead.

Check: review equivalent operations across the relevant module and explain any intentional difference. Do not force identical names onto operations with different semantics.

## CC2-3 — Avoid false clues

Do not choose names that imply the wrong behavior, data or underlying representation.

Why: readers rely on names when choosing operations and anticipating their effects.

Check: confirm that a collection name does not incorrectly promise a particular container type and that an operation name matches what it does.

## CC2-4 — Make names pronounceable and searchable

Prefer names people can discuss aloud and find reliably. Choose the amount of detail with the name's scope and audience in mind.

Why: names support both team communication and navigating the codebase.

Check: can another developer discuss and locate the concept without decoding an invented abbreviation? A conventional counter in a small local scope can be reasonable; a widely used concept needs more context.

## CC2-5 — Explain real distinctions

Replace arbitrary numbering, misspellings and noise words with names that explain the actual distinction.

Why: compiler-valid differences do not necessarily communicate different roles.

Check: explain what `Info`, `Data`, a suffix or a prefix adds. Keep it when it carries a real, established meaning; do not mechanically ban words regardless of context.

## CC2-6 — Supply useful context without clutter

Use surrounding structures and names to clarify a concept. Avoid repeating irrelevant product names or type encodings.

Why: `address.state` communicates context that an isolated `state` lacks; an unrelated product prefix may add little.

Check: identify the ambiguity the context resolves. Do not add a class or namespace solely to lengthen a name, or remove an established convention without examining its purpose.

## CC2-7 — Match the name to the kind of concept

Use nouns for entities, verbs for actions and clear questions for boolean checks.

Why: grammatical cues help readers anticipate the role of a value or operation.

Check: compare an entity such as `Customer`, an action such as `saveLesson` and a predicate such as `isFlagged`. Respect the language and framework's established conventions; Java accessor and factory patterns are not universal requirements.

## CC2-8 — Choose vocabulary the intended reader understands

Use established technical terms for technical mechanisms and problem-domain vocabulary for the subject the application serves.

Why: names should communicate shared concepts rather than demand unnecessary translation.

Check: distinguish `lesson` or `quiz` from a technical choice such as a map or queue. If a term is unfamiliar to the actual audience, explain it and establish shared vocabulary rather than assuming expertise.

## CC2-9 — Rename safely

Update affected references when improving a name and verify behavior. Check exposed names and public contracts before changing them.

Why: a local-looking rename can affect callers or consumers beyond the edited file.

Check: use refactoring tools where appropriate, inspect the diff and verify relevant behavior. Treat a change to an externally consumed name as a compatibility decision, not automatically a private refactor.
