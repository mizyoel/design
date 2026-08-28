# Accessibility

Accessibility is interaction architecture, not a final audit.

Before choosing a custom interaction ask whether it works without:
- precise pointer movement
- hover
- drag
- color perception
- animation
- vision
- tiny targets
- fast reaction
- remembering hidden state

## Semantics
Prefer native semantic elements when they meet the behavior.
ARIA describes semantics but does not implement keyboard/focus behavior.
For complex widgets follow established interaction patterns.

## Keyboard
Every important workflow must be operable without a pointer.
Keyboard accessibility does not mean Tab through every child.

Composite widgets may use managed focus:
- tabs/radio/menu/tree/grid → Tab enters/leaves; arrows navigate within when appropriate
- preserve standard text-editing keys
- expose useful expert shortcuts without making them the only route

## Focus
Focus is visible interaction state.
It is different from hover and selection.

Define:
- entry
- logical order
- containment for modal UI
- Escape behavior
- restoration after temporary surfaces close

Sticky/floating UI must not hide focused controls.

## Labels and names
Every control needs an understandable accessible name.
Prefer visible labels for important controls.
Visible wording and accessible naming should align.

## Pointer/touch
Provide comfortable target areas.
Dense visual UI can still use larger invisible hit regions.
Do not make critical behavior right-click-only or hover-only.

## Drag
When drag performs an action, provide a simpler non-drag route unless the drag itself is genuinely essential.

Examples:
- reorder → Move up/down
- mapping → select source + Connect to target
- kanban → Move to…

## Color and contrast
Do not communicate state by color alone.
Use labels/icons/shape/position as additional cues.
Muted text must remain readable.
Read-only content must not be styled like unavailable disabled content.

## Motion
Respect reduced-motion preferences.
Do not encode meaning only in motion.
Avoid flashing and uncontrolled auto-moving content.

## Zoom/reflow
Support substantial zoom/text enlargement without clipping, lost controls, or page-wide horizontal overflow for ordinary content.
Complex tables/timelines/diagrams may use localized horizontal scrolling.

## Forms
Use persistent labels.
Associate helper/error text.
Errors must say what is wrong and how to recover.
Preserve input on failure.
Long forms may add error summaries and meaningful focus guidance.

## Dynamic status
Use live announcements at useful granularity.
Do not flood screen readers with every streamed token or progress tick.
Critical persistent truth should not exist only in transient toasts.

## Data and visualization
Prefer semantic tables for tabular reading/comparison.
Use interactive grid semantics only when the richer interaction is needed.
Charts need an accessible route to the meaningful data/task.
Hover-only chart tooltips are insufficient.

## Canvas/DAG/media
Provide structured navigation/search/list alternatives where meaningful.
Spatial interaction should not be the only way to find or manipulate objects.

## AI
AI results follow ordinary accessibility rules.
Structured AI output should render as structured UI.
AI streaming should not create announcement floods.
Approval/diff must communicate scope and change without color-only meaning.

## Severity
- Blocking: task cannot be completed
- Severe: task is materially difficult/ambiguous
- Friction: quality/efficiency reduced

Fix blocking and severe issues before visual polish.

## Anti-patterns
- clickable div replacing native button without semantics
- invisible focus
- keyboard trap
- hover-only required action
- drag-only workflow
- color-only status
- tiny adjacent targets
- modal without focus contract
- responsive hidden content still focusable
- skeleton nodes cluttering accessibility tree
- chart usable only through hover
- AI token stream flooding announcements
