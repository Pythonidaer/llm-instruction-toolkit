# Frosted sticky header with opaque dropdown

Status: current default for new website work without an established alternative. Replaceable through [design guidance](../../README.md). Existing branding and explicit project instructions take precedence.

## Appearance and reference values

- Sticky header in normal document flow: start with 68px height, top: 0.
- Translucent project-colored surface: 78% opacity, 14px backdrop blur, 160% saturation.
- After more than 8px scroll, increase opacity to 92% and add a subtle border; transition over 250ms. Provide an opaque fallback without backdrop-filter.
- Keep the dropdown completely opaque, matching the project's surface and readable text. Do not blur the menu or add a page backdrop.
- Above the compact breakpoint, show horizontal links. Start with 1080px and below for the dropdown; adjust if actual labels or enlarged text require it.
- Use one shared destination list. Keep a visible current-destination state.
- Use a circular hamburger button, preferably a 44px target. Reference geometry uses three 16px-wide, 1.5px-thick lines transforming into an X over 250ms; middle line fades over 200ms.
- Use real SVG geometry or the deliberately approved reference CSS geometry, never a Unicode substitute. This reference control can be a documented exception to the project's normal icon family.
- Dropdown spans the header width directly beneath it, fading and moving from −8px to 0 over 220ms. Cap height to the available viewport and allow long menus to scroll.
- Reference interaction easing: cubic-bezier(0.2, 0.7, 0.3, 1).

These values describe a starting recipe, not universal design laws. Choose palette, type, destination count, and prominent actions for the project. Shore's black Contact button is not required everywhere.

## Behavior

- This is a nonmodal disclosure: no focus trap, page backdrop, or body scroll lock.
- Use a real button with an accessible open/close name, aria-expanded, and aria-controls. Hidden mobile links must be unfocusable and unavailable to assistive technology.
- Close on destination selection, Escape, outside pointer interaction, focus leaving the header, and relevant breakpoint changes. Escape returns focus to the trigger.
- Preserve ordinary page scrolling and keyboard movement. Do not allow hidden links to remain interactive.
- Respect reduced motion by removing transitions. Keep visible focus and usable targets.
- Position sticky elements relative to the actual scrolling container. Keep the header outside transformed diagram ancestors; do not add duplicate fixed-header spacers.

## Check and replacement

Check desktop and compact layouts, long menus, keyboard focus, interruption, reduced motion, enlarged text, browser-toolbar changes, and safe areas. Verify opaque menu readability over real page content.

If a modal drawer fits a project better, document that choice and implement its complete containment/dismissal behavior. Do not inherit drawer rules merely because older baseline copies mention them.

Sources and historical qualifications: [source map](../../sources.md).
