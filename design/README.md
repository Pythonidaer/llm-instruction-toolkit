# Website design guidance

Build clear, usable websites with deliberate identity. Interrupt automatic design habits, then choose coherent patterns that serve the content.

## Read and apply

1. Confirm the intended repository, current source, audience, primary task, and existing project instructions.
2. Apply the three [AI design reset](ai-design-reset/visual-styling.md) files together: appearance, content, and structure. Follow the [CSS baseline instructions](ai-design-reset/visual-styling.md#css-baseline) to integrate [reset.css](ai-design-reset/reset.css) when applicable.
3. For content work, read [Writing decisions](../writing-decisions/README.md) and the combined content-design instructions. Consult already-incorporated source files separately only for clarification or revision.
4. Use [frosted header with dropdown](patterns/navigation/frosted-header-dropdown.md) only when requested or explicitly adopted by the user.
5. Select [content reveals](patterns/motion/staggered-content-reveal.md) or the [interactive roadmap](patterns/learning/interactive-roadmap.md) only when requested or explicitly adopted by the user.
6. For every website created or published, apply [Link previews and discovery](publishing/link-previews.md) before deployment and verify the published assets afterward. Preserve the intended audience and indexing policy.
7. Record intentional choices, exceptions, and verification limits in the consuming project.

Preserve existing approved project design during unrelated work. Navigation, motion and roadmap patterns are optional references, not automatic defaults or retrofit instructions. Explicit project requirements and user decisions take precedence.

## Files

| File | Role |
| --- | --- |
| [CSS reset](ai-design-reset/reset.css) | CSS baseline loaded before project styles; reconcile with an existing reset first |
| [Visual styling](ai-design-reset/visual-styling.md) | Fonts, color, surfaces, decoration, and icon treatment |
| [Content design reset](ai-design-reset/content-design.md) | Wording pitfalls, repetition, misleading feedback and tone defaults |
| [Content and tone guidance](../writing-decisions/best-practices.md) | User needs, writing, tone, evaluation and maintenance |
| [Mailchimp writing goals and principles](../writing-decisions/goals-and-principles/mailchimp-writing-goals-principles.md) | Content goals, practical writing principles and review questions |
| [Mailchimp voice and tone](../writing-decisions/voice-and-rules/mailchimp-tone-voice.md) | Optional voice profile, contextual tone rules, examples and review checks |
| [Mailchimp grammar and mechanics](../writing-decisions/grammar-and-mechanics/mailchimp-grammar-mechanics.md) | Optional house style for grammar, punctuation, numbers, naming and formatting |
| [Project questions](../writing-decisions/project-questions.md) | A small-batch intake and adaptable project tone brief |
| [Layout and information architecture](ai-design-reset/layout-and-information-architecture.md) | Hierarchy, grouping, page structure, and navigation |
| [Frosted header and dropdown](patterns/navigation/frosted-header-dropdown.md) | Optional navigation reference |
| [Staggered content reveal](patterns/motion/staggered-content-reveal.md) | Optional motion recipe with independently adjustable timing |
| [Interactive roadmap](patterns/learning/interactive-roadmap.md) | Optional learning diagram and topic-reading pattern |
| [Link previews and discovery](publishing/link-previews.md) | Share images, page metadata, icons, search discovery, and deployed-asset verification |
| [Sources](sources.md) | Provenance, scope, and superseded guidance |

## Maintaining the system

The reset challenges defaults; it does not prescribe a permanent theme or guarantee brand identity. Fonts, colors, cards, and gradients can be useful when selected for a reason. No emojis or text-character substitute UI icons is an explicit preference.

Keep shared principles here and exact project choices in project documentation. Load optional pattern references only when requested or explicitly adopted; preserve existing projects' choices unless asked to migrate them. Record a decision, reason, alternative, and practical check. Separate implementation, automated checks, deployment, and visual verification.

These Markdown files require explicit loading or integration into a project's instructions. They do not automatically activate across repositories. When adopting this guidance in a website, add the publishing rule from [Link previews and discovery](publishing/link-previews.md#integrate-into-website-instructions) to its existing `AGENTS.md` or equivalent entry point, using an accessible repository URL or maintained local copy.
