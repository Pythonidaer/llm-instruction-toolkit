# Reset automatic layout and information architecture

Scope: what information belongs together, its order, and how people find it. Read alongside [visual styling](visual-styling.md) and [content design](content-design.md).

## Rules

- Establish audience, primary task, and needed information before selecting sections or components.
- Do not automatically use hero → logos → feature cards → statistics → closing call to action. Each section needs its own purpose.
- Choose structures from relationships: comparable items may use cards, sequences use ordered steps, and exact comparisons may use tables. Avoid uniform three- or four-card grids as a page-building reflex.
- Use hierarchy, whitespace, and alignment before adding containers. Match emphasis to importance; a pill needs a clear role such as a filter or status, not merely visual variety.
- Group recognizable destinations and distinguish navigation, example selection, and contextual actions. Integrate new destinations with the existing system.
- Define mobile reading order, content widths, gutters, and responsive changes. Preserve useful context when dividing long content into sections or nested subsections.
- Avoid repeating pitches, metadata, counts, and calls to action. Give the footer a useful role appropriate to the site; do not append a stock multi-column footer or closing promotional section.
- Select interaction semantics deliberately. A nonmodal dropdown allows normal page focus and scrolling; a modal drawer or dialog needs containment, dismissal, and focus return. Do not mix their behavior.
- Use the [current navigation default](../patterns/navigation/frosted-header-dropdown.md) where no project choice exists. Preserve an established alternative during unrelated changes.
- Separate essential information from optional depth without hiding material needed to understand the main point.
- Keep one clear owner for component layout and state. Replace conflicting implementations rather than accumulating overrides.

## Check

Sketch the page using only section names and destinations. Does the order support the visitor's task? Check scanability, mobile order, empty/loading/error states, long labels, keyboard navigation, and enlarged text. A successful build or deployment does not establish visual correctness.
