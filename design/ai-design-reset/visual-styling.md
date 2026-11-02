# Reset automatic visual styling

Scope: appearance. Read alongside [content design](content-design.md) and [layout](layout-and-information-architecture.md).

## CSS baseline

Use [reset.css](reset.css) as the supplied CSS baseline for new websites. Copy it into the consuming project's stylesheet setup and load it once, before theme and component styles. Keeping it in this toolkit does not load it in another website.

Inspect existing global CSS and framework resets first. If the project already uses a reset or normalization layer, compare its coverage and reconcile differences rather than blindly stacking resets. Preserve established behavior during narrow maintenance tasks.

This file also deliberately removes link underlines, list markers, button surfaces and default spacing; those are styling choices as well as normalization. After applying it:

- Give links a recognizable treatment, including underlines where needed to distinguish them in prose.
- Provide visible button styling, usable targets and appropriate disabled-state presentation; preserve visible keyboard focus.
- Restore list markers or numbering where they communicate meaning. Verify semantic lists remain exposed to assistive technology.
- Define heading, paragraph and fieldset spacing and grouping deliberately.
- Check media and inline SVG usage after the global block-display rule.
- Verify responsive layouts, keyboard interaction and real content. A reset does not guarantee identical rendering across browsers or accessibility.

## Rules

- Choose typography, color roles, spacing, widths, and component treatments for the audience, subject, and existing identity. A distinctive font alone does not establish identity.
- Do not automatically choose Inter or Roboto, purple/indigo palettes, beige/orange alternatives, purple-to-blue gradients, gradient headlines, blurred glows, abstract blobs, or sparkle decoration. These are choices to justify, not a universal blacklist.
- Do not put rounded containers, borders, shadows, pills, or glass effects around every content group. Use alignment and whitespace first; add surfaces when they express a useful relationship or state.
- Do not replace one recognizable recipe with mandatory serif type, green palettes, square corners, or asymmetry.
- Use a coherent spacing scale and clear alignment edges. Let optical alignment and real content justify exceptions.
- Never use emojis in website UI or interface copy. Do not substitute Unicode arrows, stars, crosses, or similar text characters for UI icons. Use a deliberately selected SVG family or clear text.
- Centralize approved icons and action mappings. Use consistent geometry and purposeful placement; do not add an icon to every action. Preserve native artwork in catalogs rather than restyling it to match interface controls.
- Make text, controls, and state indicators readable. Preserve visible focus, usable targets, and non-color cues. Reserve outline and offset clearance so focus is neither clipped nor overlapping neighboring content.
- Use blur, shadow, and motion for a defined purpose. The optional [navigation reference](../patterns/navigation/frosted-header-dropdown.md) has a frosted header and opaque menu; that is not permission for glass surfaces throughout the page.

## Check

Review the full page as well as individual elements. Can the chosen type, palette, imagery, and surface treatments be explained in terms of this project? Check narrow and large screens, enlarged text, contrast, focus, and real content. Remove decoration that competes with the primary task.
