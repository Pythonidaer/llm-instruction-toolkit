# Staggered content reveal

Status: optional recipe from Shore. Do not automatically animate every website or tie this to the navigation default.

## Independent controls

- Easing controls acceleration through an animation.
- Duration controls how long it runs.
- Delay controls when it starts.
- Stagger controls the start interval between successive elements.
- Trigger controls what event starts it.

Record these separately so one choice can change without inheriting the entire recipe.

## Reference recipe

| Part | Starting values |
| --- | --- |
| Heading words | Opacity 0 → 1; translateY 80% → 0; rotateX −20deg → 0; blur 5px → 0 |
| Heading timing | 1 second duration; 30ms between words |
| Heading geometry | 900px perspective; bottom-center transform origin |
| Supporting block | Opacity 0 → 1; translateY 26px → 0; blur 4px → 0; 900ms duration |
| Second-stage content | Optional 900ms delay before its 900ms reveal |
| Content easing | cubic-bezier(0.165, 0.84, 0.44, 1) |
| Viewport trigger | IntersectionObserver threshold 0.12; bottom root margin −60px; play once |

Give the headline priority, then supporting information. On mobile, supporting copy/link and image/caption groups start on their own viewport entry so they do not finish unseen below the fold. Evaluate triggers for very tall elements rather than assuming the threshold always fires.

## Requirements

- Default content remains visible without the enhancement. Failure or unsupported APIs must not strand invisible content.
- Reduced motion removes movement and delays.
- Keyboard focus entering a group makes its content visible immediately.
- Preserve meaningful heading text and accessible names when splitting words into decorative spans.
- Delayed keyframes need appropriate fill behavior so content does not flash before its entrance.
- Navigation stays responsive; content-reveal timing does not govern menu timing.
- Avoid delays on essential actions and artificial loading waits.

## Check

Test first load, mobile viewport entry, scrolled-past content, keyboard access, reduced motion, and no JavaScript. Check real animation in a browser; classes and computed delays alone do not prove playback.

Sources: [source map](../../sources.md).
