# Chapter 1 — Foundations

Status: draft heuristics derived from [Chapter 1 resource notes](https://github.com/Pythonidaer/clean-code-lms/blob/main/docs/resources/chapter-1-notes.md). Apply with the [scope and qualifications](README.md#scope-and-judgment).

## CC1-1 — Understand before changing

Understand the code's intended behavior, purpose and relevant callers before changing it. Identify the assumptions the change could affect.

Why: editing without context makes accidental behavior changes more likely.

Check: explain what should stay the same and what evidence will show that it does.

## CC1-2 — Make intent readable

Choose names and structure that communicate what the code represents, why it exists and how it is used. Include units when they prevent ambiguity. Apply the detailed [naming rules](chapter-2-meaningful-names.md).

Why: clear intent reduces the context the next reader must reconstruct.

Check: can a reader explain the operation and its inputs without guessing what placeholders mean?

## CC1-3 — Keep responsibilities focused

Keep functions and modules focused on coherent responsibilities. Separate responsibilities when doing so makes their purpose or change boundaries clearer.

Why: unrelated work makes the next change harder to locate and assess.

Check: describe each responsibility and why the proposed boundary improves understanding. Do not split solely to meet a line count.

## CC1-4 — Remove meaningful duplication

Remove duplicated behavior when it expresses the same underlying idea or policy.

Why: repeated implementations of one rule can diverge when only some copies change.

Check: verify that the occurrences really represent the same concept. Do not combine different policies merely because their syntax looks similar.

## CC1-5 — Use abstractions for real needs

Introduce an abstraction when it expresses a useful concept or boundary and reduces unnecessary knowledge of implementation details.

Why: a useful boundary helps readers and callers work at the appropriate level of detail.

Check: name the concept being represented, identify what details it contains and explain how the interface serves actual callers. Avoid speculative structure.

## CC1-6 — Make failures and dependencies deliberate

Handle failures deliberately and make dependencies clear. Ensure callers can understand the relevant success and failure contract.

Why: hidden assumptions and unclear failure behavior make changes difficult to reason about.

Check: identify important dependencies and failure cases and show how they are communicated. Choose mechanisms appropriate to the language and application.

## CC1-7 — Improve in small checked steps

Leave the area being worked on clearer through small, behavior-preserving improvements. Check the affected behavior using suitable existing tests or other meaningful verification.

Why: bounded changes are easier to understand, review and verify.

Check: connect each improvement to a specific issue and report what was checked. Avoid treating a cleanup task as permission for an unrelated rewrite.

## CC1-8 — Explain an actionable finding

Describe the observed problem, its consequence and the reason for the proposed improvement.

Why: a concrete explanation lets a reviewer assess the change instead of accepting a preference on authority.

Check: include a relevant location or example and a suitable verification step. Distinguish a behavior defect from a maintainability concern or preference.

## CC1-9 — Communicate maintenance risks

Communicate relevant code-quality risks while discussing requirements, estimates and schedules.

Why: planning decisions need information about the cost and consequences of changes.

Check: explain the risk, likely impact and a bounded response. Avoid unsupported certainty or assigning all responsibility to one person.

## CC1-10 — Apply judgment rather than slogans

Evaluate recommendations against the task, language, existing design and observable behavior. Practice explaining and applying a technique instead of treating its name as proof.

Why: useful heuristics have contexts and tradeoffs; mechanically optimizing a metric can damage clarity.

Check: explain why the rule applies here, what it costs and what evidence supports the result. Readability and changeability are related but different, and passing tests alone do not prove either.
