# Sources and consolidation decisions

Reviewed 2026-10-18; content and tone guidance added 2026-10-19. This folder synthesizes existing guidance; it does not replace or edit the source repositories.

| Source snapshot | Material used |
| --- | --- |
| [design-practice](https://github.com/Pythonidaer/design-practice/tree/2a050335fac6cd3b191e1f6510df823f3143736b) | WEBSITE_DESIGN_BASELINE.md, AGENTS.md, DESIGN_DECISIONS.md, MUSCULOSKELETAL_DESIGN_ADAPTATIONS.md |
| [typography-learning](https://github.com/Pythonidaer/typography-learning/tree/220111ac8f52ccbf2a490c0e2b1491b16e1c32bb) | AGENTS.md, DESIGN_DECISIONS.md, dist/roadmap/ROADMAP_DESIGN_RULES.md |
| [master-icon-library](https://github.com/Pythonidaer/master-icon-library/tree/f88e0b70ac96847a401cf89754ef229a81873ab7) | AGENTS.md, PROJECT_DESIGN_ADDITIONS.md, DESIGN_DECISIONS.md, LOADING_AND_BROWSING_OPTIONS.md |

All three repositories preserve the same Website Design Baseline 1.2 blob: 4ed9dae66685cc8eafbf9556d01788b6c4f6f124.

## What changed during consolidation

- Split baseline principles into visual styling, content design, and layout/information architecture.
- Retain deliberate exceptions rather than converting font/color avoidance into absolute bans.
- Promote the explicit no-emoji/no-character-substitute UI icon preference.
- Record frosted sticky header plus opaque nonmodal dropdown as the current default, per Johnny's approval on 2026-10-18.
- Keep motion and roadmap as optional patterns. Separate motion easing, duration, delay, stagger, and trigger.
- Keep exact icon families, palettes, item numbers, deployment setups, and product-specific actions in consuming projects.
- Use the later navigation adaptation rather than the baseline's older full-height drawer and one-second-slide preference. Dropdown and modal drawer semantics must remain distinct.
- Do not import Master Icon Library's stale infinite-scroll recommendations as a default. Its latest decision log selects explicit Load more and nonsticky icon search/count; older README and browsing-options statements conflict with those later records.
- Preserve source verification limits. Prior source checks and deployment do not establish that every browser, device, or accessibility behavior has been verified.

## Future changes

Update the relevant principle or pattern and explain its scope. Keep historical experiments in project decision logs rather than presenting all past options as simultaneous requirements. Review changed source documents before synchronization; this folder does not automatically track them.

## Content and tone extension

Reviewed the 26 lesson decks in [content-design-lms at 3c697fc613370c58a03facd7b590eb181497e434](https://github.com/Pythonidaer/content-design-lms/tree/3c697fc613370c58a03facd7b590eb181497e434) using [course.json](https://github.com/Pythonidaer/content-design-lms/blob/3c697fc613370c58a03facd7b590eb181497e434/course.json) and [source-manifest.json](https://github.com/Pythonidaer/content-design-lms/blob/3c697fc613370c58a03facd7b590eb181497e434/source-manifest.json). The source manifest maps the course to 27 resources. The LMS uses original summaries and exercises; this extension synthesizes guidance rather than copying a complete source site or its style-guide dictionaries.

- [Content and tone guidance](content-and-tone/best-practices.md) covers the course's planning, writing, accessibility, lifecycle, evaluation and tone topics.
- [Project questions](content-and-tone/project-questions.md) is an authored intake and brief template, not a questionnaire published by GOV.UK or NN/g.
- Verified the primary [GOV.UK content-design overview](https://guidance.publishing.service.gov.uk/writing-to-gov-uk-standards/plan-manage-content/understand-content-design/), [GOV.UK tone guidance](https://guidance.publishing.service.gov.uk/writing-to-gov-uk-standards/writing-guidelines/right-tone/), [NN/g four-dimension framework](https://www.nngroup.com/articles/tone-of-voice-dimensions/) and [Mailchimp voice/tone distinction](https://styleguide.mailchimp.com/voice-and-tone/) on 2026-10-19.
- Keep an initial profile across all four dimensions and adapt it to context. The ten tone qualities are an authored LMS reference, not an exhaustive official taxonomy.
- Keep GOV.UK publishing rules and Mailchimp's brand personality scoped to their publishers. Do not turn a baseline suggestion into a global requirement.
- Carry forward the principle of avoiding repeated general helper copy. This toolkit update does not remove or rewrite LMS slides, alter its voice implementation, or transfer private session transcripts or diagnostic traces.
