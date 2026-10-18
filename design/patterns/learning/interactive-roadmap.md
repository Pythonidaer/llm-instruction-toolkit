# Interactive learning roadmap

Status: optional pattern. Preserve the typography roadmap's approved implementation when editing that project; other subjects need deliberate content and geometry decisions.

## Reusable structure

- Use a compact diagram for an overview, with one concise concept per node. Put definitions, examples, practice, and further reading in the opened topic.
- Define stable node IDs and explicit relationships. Make solid/dotted lines, hierarchy, and a small legend correspond to meaning.
- Keep connectors behind nodes, terminate at boundaries, and preserve label clearance.
- Fit the diagram to available width while reserving its scaled dimensions. Preserve native pinch zoom and panning; avoid accidental document overflow.
- Keep navigation and reading controls independent of diagram scaling.
- Use real topic buttons with accessible names and visible focus.
- Use an opaque full-screen reading modal on mobile and a full-height right-side reading panel on larger screens. Both remain modal, with Escape/backdrop dismissal, focus containment, and return to the originating topic.
- Preserve useful source links while keeping repetitive provenance and implementation labels out of the lesson.

## Typography reference profile

These are scoped reference choices, not required values for every future roadmap.

| Aspect | Approved reference |
| --- | --- |
| Content | 43 vocabulary terms with source IDs; six main groups |
| Canvas | 1000 units; 16-unit text; 38-unit node height; 44-unit branch pitch |
| Node widths | 240-unit main; 280-unit supporting; 4-unit corner radius |
| Connections | Blue #3378ba; solid 4-unit main sequence; dotted 3-unit supporting links with 1 7 dash pattern and curved branches |
| Mobile reading | Full viewport at 700px and below; 18px definition text, 1.7 line height |
| Desktop reading | Above 700px: right-edge 600px-wide panel, capped to viewport; full height |
| Overlay and motion | 25% black, unblurred overlay; immediate opening/closing without slide or fade |
| Close control | Approved 18px SVG in a transparent 40px button; safe-area and focus clearance |

The approved compact overview deliberately has small fit-scale targets. Native zoom remains available; do not claim those compressed targets satisfy ordinary target-size guidance. Future accessible alternatives need deliberate review rather than silent removal or an unsupported compliance claim.

The typography version intentionally has no zoom toolbar, search, list view, progress, or Next topic controls. These are project choices, not prohibitions for every learning product. It keeps Roadmap last in navigation and omits repetitive footer branding.

## Integration and checks

Keep the approved roadmap's CSS scoped and separate from catalogue styles. Use the actual scrolling container for the sticky header, outside transformed diagram ancestors.

Check vocabulary parity, unique IDs, valid edges, label bounds, fit at 320/375/390/430/768px and desktop, native zoom, topic reading, keyboard navigation, and focus return. Check real mobile and desktop behavior separately from source assertions.

Source profile: [source map](../../sources.md).
