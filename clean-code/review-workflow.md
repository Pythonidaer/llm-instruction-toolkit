# Applying the Clean Code guidance

A repeatable review procedure derived from Chapters 1–2. This is maintained workflow guidance; tool-specific skill packaging is deferred.

## 1. Establish the task

Identify the code and outcome the user wants reviewed or changed. Read applicable project instructions, conventions and relevant behavior checks. Keep the work within the authorized scope.

## 2. Understand the current behavior

Explain the operation's purpose, inputs, outputs, important effects and callers. Distinguish required application behavior from the mechanisms used to implement it. Identify uncertainties before proposing a behavior-dependent change.

## 3. Select relevant rules

Consult [Chapter 1](chapter-1-foundations.md) for general readability and improvement principles and [Chapter 2](chapter-2-meaningful-names.md) for naming decisions. Apply a rule only when its rationale fits a concrete issue.

## 4. Describe the finding

For each material finding, state:

- **Location and rule ID:** where it occurs and which guidance applies.
- **Observation:** what the code currently does or communicates.
- **Consequence:** why that creates a behavior or maintenance problem.
- **Proposal and tradeoff:** a bounded improvement and its cost or limitation.
- **Verification:** evidence that would support accepting the change.

Avoid inventing findings to satisfy a checklist. Record intentional exceptions with a reason.

## 5. Make a bounded improvement when requested

Preserve intended behavior during refactoring. Use refactoring tools where helpful, update affected references and inspect public contracts. Do not turn a readability review into permission for unrelated architecture changes.

## 6. Verify and report

Run checks appropriate to the change. Reuse relevant existing tests and add tests when they meaningfully address an unresolved behavior risk. Do not add tests that merely repeat the implementation or equate a passing test with proof of design quality.

Report what changed, why it helps, what was checked and any unresolved limitation. Distinguish completed work from suggestions for later.

## Maintenance feedback

When a rule repeatedly produces ambiguity or a poor result, revise its wording or qualification here. Keep chapter source links and stable IDs so future consolidation can trace the reasoning. Do not silently promote unanswered learning questions into mandatory development rules.
