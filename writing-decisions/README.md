# Writing decisions

Use this folder to decide what content belongs in a project, how it should sound, and how to write it consistently. Work from the reader's needs toward sentence-level details. Return to earlier decisions when testing exposes a problem.

## Purpose, audience and status

This is primarily Johnny's personal toolkit for controlling LLM decisions in web projects, with possible future use in apps. Developer friends can review it without needing the authoring conversation. It is a work in progress, including documentation that still needs review.

Understanding takes priority over brevity. Use plain, descriptive headings and make individual decisions easy to identify. Keep instructions concise where meaning survives; add explanations or examples when they resolve a specific ambiguity. Google and Mailchimp are sources of writing guidance, not services the user must use or brand personalities to adopt.

## TODO: review and consolidate

These are future review tasks, not instructions to perform the cleanup automatically. Johnny is learning and reviewing the material incrementally. Adding these items does not approve every existing rule or change previously agreed instructions.

- [ ] Review [best-practices.md](best-practices.md). Identify which guidance to keep, revise, clarify or mark provisional.
- [ ] Review [project-questions.md](project-questions.md). Check the questions and brief template against the desired collaborative process.
- [ ] Consolidate [content-design.md](../design/ai-design-reset/content-design.md) toward **one clear instruction per decision**. Distinguish overlapping concepts from duplicated instructions; combine equivalent rules, preserve unique qualifications and context, and keep source attribution and useful explanations nearby. Review examples case by case rather than adding or removing them mechanically.

Some repetition comes from shared concepts: clarity, useful context and factual accuracy support several writing layers. Some comes from compiling several sources that express the same decision. During review, retain meaningful differences in scope and exceptions; use cross-references when one instruction supports multiple layers.

## How to interpret instructions and notes

- **Active instruction:** an explicit, adopted direction with a defined scope. Apply it when relevant.
- **Provisional guidance:** a starting choice to explore and revise; do not present it as a settled project requirement.
- **Study note or open question:** material to understand or revisit; do not execute it as a command.

Use these labels when adding or revising material. Existing files have not all been classified. Do not assume that every sentence is an active instruction, or that a direct instruction is optional merely because the repository is unfinished. When status is unclear and changes the outcome, ask the owner.

## Required behavior when starting website work

For a new website or substantial content rethink, follow the [audience-and-purpose checkpoint](../design/ai-design-reset/content-design.md#required-first-response-audience-and-purpose):

1. Reuse information already supplied. Ask only unresolved questions about audiences, their tasks, the creator's purpose and competing priorities.
2. End the response after asking and wait for the user's reply before drafting, designing or implementing. If the brief is already available but unconfirmed, summarize it and request confirmation once.
3. Once answered and confirmed, proceed with the authorized task. Do not repeatedly request confirmation or reopen settled choices.
4. A provisional brief is enough for exploration. Label assumptions about other people's needs and refine the brief using feedback.

Do not restart this discovery for a narrow maintenance task or an edit to these rules. Explicit instructions to skip it take precedence.

## Which file should an LLM read?

For content-design work, use [the combined content-design instructions](../design/ai-design-reset/content-design.md) as the working entry point. Essential behavior is stated there so it is available even when this README is not loaded.

The files below are detailed study and source references. The combined file already incorporates them; loading them all again is usually redundant. Consult a source file to investigate provenance, an unresolved rule, or a focused revision. Changes to a source file do not automatically synchronize with the combined file: reconcile both deliberately.

For broader website work, [the repository README](../README.md) and [design guidance](../design/README.md) describe the current entry points. A single entry file can route an LLM to relevant instructions; it does not need to contain every rule. Linked documents are not automatically read simply because a link exists, and external repository rules do not activate in unrelated projects unless explicitly loaded or integrated.

## Files in this folder

| Folder | Files | Role |
| --- | --- | --- |
| This folder | `README.md`, `best-practices.md`, `project-questions.md` | Orientation, content reference and project intake |
| `goals-and-principles/` | `google-writing-goals-principles.md`, `mailchimp-writing-goals-principles.md` | Source-based goals and writing principles |
| `grammar-and-mechanics/` | `mailchimp-grammar-mechanics.md` | Detailed conventions and reference examples |
| `voice-and-rules/` | `mailchimp-tone-voice.md` | Combined voice-and-tone source reference |
| `voice-and-rules/voice/` | `voice.md` | Stable product character |
| `voice-and-rules/tone/` | `tone.md` | Situational delivery |

## The layers

| Layer | Question it answers | Example |
| --- | --- | --- |
| Content decisions | What does this person need to know or do? | Explain the upload limit before they choose a file |
| Goals | What should the writing accomplish? | Help someone recover from a failed upload |
| Principles | What qualities guide the writing? | Be clear, useful, concise and respectful |
| Voice | What consistent character should the product communicate? | Knowledgeable and approachable |
| Tone | How should that voice adapt to this situation? | Calm and practical during an error |
| Grammar | How do words form clear sentences? | Choose a tense that accurately describes what happened |
| Mechanics | How do we present written language consistently? | Choose numeral, capitalization and abbreviation conventions |
| Punctuation | How do marks organize meaning? | Decide whether a short interface message needs a period |

Punctuation is usually included under mechanics. Grammar concerns sentence structure; mechanics concerns written conventions. Both can affect meaning.

**These layers overlap.** A publisher's document title does not guarantee that every rule belongs to one category. Google's principles include numeral and punctuation conventions; Mailchimp's mechanics guide also contains broad writing advice. These files retain that overlap for now.

## A practical order for projects

### 1. Establish the reader and task
Use [Project questions](project-questions.md) in small batches. Identify the audience, immediate task, required facts and source of truth.

Use [Content best practices](best-practices.md) to decide what belongs on the page, where it belongs, and which interface states need content. Keep authoring conversations and unnecessary implementation details out of public copy.

### 2. Choose goals and principles
Read [Mailchimp goals and principles](goals-and-principles/mailchimp-writing-goals-principles.md) for broad communication aims: empower, respect, educate, guide and speak truth.

Read [Google writing principles](goals-and-principles/google-writing-goals-principles.md) for practical interface guidance: essential information, direct wording, concise labels and consistent conventions.

Use these as decision criteria. Do not add text merely to demonstrate every goal.

### 3. Establish voice and adapt tone
Use [Voice](voice-and-rules/voice/voice.md) for stable identity and [Tone](voice-and-rules/tone/tone.md) for contextual delivery.

[Mailchimp voice and tone](voice-and-rules/mailchimp-tone-voice.md) remains a combined reference pending further separation. Use its general lessons about clarity, warmth and context; choose each project's voice deliberately.

### 4. Draft in the actual interface
Write headings, labels, instructions, errors and recovery options around the real task. Check what each text element contributes. Keep facts and actions unchanged when comparing tone variants.

### 5. Check grammar and mechanics
Use [Mailchimp grammar and mechanics](grammar-and-mechanics/mailchimp-grammar-mechanics.md) as a lookup reference for numbers, dates, punctuation, capitalization, names and formatting.

The sentence-opening number rule already follows Google's numeral preference. Preserve explicit project decisions, required identifiers and accurate values. If another conflict appears, resolve it explicitly rather than combining incompatible instructions.

### 6. Test and revise
Can someone understand what happened and complete the task without coaching? Review wording and layout together. A correctly punctuated sentence can still be unnecessary or unhelpful.

## Find guidance for your current task

| If you are asking… | Open… |
| --- | --- |
| Does this text belong here? | [Content best practices](best-practices.md) |
| What are we trying to accomplish? | [Mailchimp goals and principles](goals-and-principles/mailchimp-writing-goals-principles.md) |
| How can this interface copy be clearer? | [Google writing principles](goals-and-principles/google-writing-goals-principles.md) |
| What should the product sound like? | [Voice](voice-and-rules/voice/voice.md) |
| How should this particular message feel? | [Tone](voice-and-rules/tone/tone.md) |
| How should this number, date or punctuation mark appear? | [Grammar and mechanics](grammar-and-mechanics/mailchimp-grammar-mechanics.md) |

Select only the references needed for the current task. These files require explicit loading or integration into project instructions; storing them here does not automatically apply them elsewhere.
