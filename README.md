# LLM Instruction Toolkit

A central collection of development guidance built from my study notes and experience. Organize instructions by subject so they can be reviewed, reused and refined across projects.

## Topics

| Folder | Focus | Current coverage |
| --- | --- | --- |
| [design](design/README.md) | Deliberate website design and reusable patterns | AI design reset, optional navigation, motion and roadmap, link previews and publishing checks |
| [writing-decisions](writing-decisions/README.md) | Website content, voice and tone | Content guidance, project questions, Mailchimp references and Google writing principles |
| [color-theory](color-theory/README.md) | Intentional color decisions and maintainable color systems | Color fundamentals, hierarchy, accessibility, tokens, interaction states and collaborative review |
| [clean-code](clean-code/README.md) | Code readability, maintainability and safe improvements | Reviewed notes from Chapters 1–3 |

## LLM entry point

When asked to apply this toolkit, start here. Identify the authorized task, then fetch and read the applicable files below before making decisions. Do not assume linked files have already been read. Report inaccessible required files instead of claiming compliance.

| Task | Load and apply |
| --- | --- |
| Writing, reviewing or refactoring code | [Overview](clean-code/README.md), [workflow](clean-code/review-workflow.md), and applicable added chapters: [foundations](clean-code/chapter-1-foundations.md), [names](clean-code/chapter-2-meaningful-names.md), [functions](clean-code/chapter-3-functions.md). Keep improvements within scope. |
| Creating a website or substantially redesigning an interface | All three reset files: [visual styling](design/ai-design-reset/visual-styling.md), [content design](design/ai-design-reset/content-design.md), [layout and information architecture](design/ai-design-reset/layout-and-information-architecture.md). For new websites, also integrate [reset.css](design/ai-design-reset/reset.css) using the [CSS baseline instructions](design/ai-design-reset/visual-styling.md#css-baseline). Reconcile existing framework resets instead of stacking them. For narrow changes, read the relevant reset and preserve approved decisions outside the task. |
| Creating or changing website content | [Writing decisions](writing-decisions/README.md) and [combined content instructions](design/ai-design-reset/content-design.md). Detailed writing sources are already incorporated in the combined file; consult them for clarification, provenance or focused revisions rather than loading everything twice. |
| Choosing or changing colors, themes, contrast or color tokens | [Color Theory](color-theory/README.md). Apply relevant sections. This is evolving guidance, not an adopted brand identity or palette. Preserve established project choices and ask about unresolved brand intent when it affects the task. |
| Creating or publishing a website | [Link previews and discovery](design/publishing/link-previews.md). Prepare applicable metadata and assets; verify deployed URLs when publishing is authorized. Preserve existing settings during narrow maintenance unless affected. |
| A particular menu, roadmap or motion effect | Load the relevant [pattern reference](design/README.md#files) only when requested or explicitly adopted by the user. Patterns are not automatic design defaults. |

For a complete new website involving code, content and design, load all applicable baseline rows. Do not choose just one. Patterns remain optional.

### Working rules

- Follow the audience-and-purpose checkpoint in the content instructions for new websites or substantial content rethinks. Ask unresolved questions and wait for the reply; once the brief is confirmed, proceed with the authorized task without repeated confirmation.
- Reuse supplied answers, explicit user preferences and approved project conventions. Preserve factual accuracy and accessibility.
- Distinguish active instructions, provisional guidance and study notes using [the status guidance](writing-decisions/README.md#how-to-interpret-instructions-and-notes). An unfinished repository does not make every instruction optional.
- Apply overlapping rules once. Resolve genuine conflicts using recorded priorities or a focused question.
- Do not invent brand decisions, impose a preset palette or automatically adopt optional patterns. Familiarity with a topic does not replace reading the user's rules.
- Source maps and historical notes are reference material; read for provenance, conflicts or maintenance.
- Briefly report which rule groups were loaded and any access limits. Loading instructions does not authorize unrelated edits or publication.
- These links require actual retrieval. Storing the toolkit does not automatically activate it in unrelated repositories; point the session here explicitly or integrate this entry point into the consuming project's instructions.

## Use this repository

1. Choose the topic relevant to the work.
2. Read its scope and qualifications before applying individual rules.
3. Supply the relevant files explicitly to the assistant or adapt them into a project's instruction system.
4. Apply them within the requested task; explain tradeoffs and check affected behavior.

The Markdown files are the maintained source guidance. Keeping them here does not automatically activate them in other repositories or install a skill. Tool-specific rules and skill packaging can be decided later, after the guidance has been tested in real work.

Add future subjects in their own folders. Keep project-specific exceptions in the consuming project's guidance and explain why they are needed.
