# Responsive & Adaptive Design

Responsive design preserves the product's **mental model**, not its coordinates.

Design for available space, input method, content pressure, platform capability,
zoom, and user preferences. Do not reason only in device labels.

## Invariants
Identify what must survive:
- current object
- scope
- primary action
- selection
- filters
- unsaved state
- critical status
- navigation recovery

## Adaptation ladder
Use the smallest sufficient change:
1. resize
2. reposition
3. reflow
4. collapse
5. show/hide
6. transform pattern
7. re-architect

## Content-pressure breakpoints
Break when the task becomes unusable, not because a fashionable device width was reached.
Define meaningful layout classes rather than dozens of patch breakpoints.

Example:
- Wide: sidebar | navigator | workspace | inspector
- Medium: rail | workspace | collapsible inspector
- Narrow: collection → detail → properties, navigation via drawer

## Pattern transformations
- sidebar → rail → drawer/bottom nav
- inspector → collapsible panel → properties sheet/page
- popover → bottom sheet
- side sheet → full-screen detail
- master-detail → sequential list → detail
- hover preview → tap/select persistent preview

## Tables
Do not automatically cardify.
Choose based on task:
- horizontal scroll
- priority columns
- sticky identifier
- column visibility
- row detail
- list transformation

Preserve comparison when comparison is the job.

## Filters/search
Desktop may expose persistent filters; mobile may use a sheet.
Active filters and active search state must remain visible after surfaces collapse.

## Input modality
Do not infer touch/mouse solely from width.
Essential behavior must not require hover/right-click.
Drag needs a touch/keyboard alternative.
Dense visuals can still provide comfortable hit areas.

## Zoom/text scaling
Treat zoom as responsive pressure.
Avoid fixed heights that clip labels/errors/localization.
At high zoom ordinary content should reflow; local horizontal scrolling may remain appropriate for tables/timelines/code.

## State persistence
Resize/orientation/layout changes should not clear:
- forms
- selection
- filters
- active job
- drafts
- media position

Geometry changed; user intent did not.

## Sticky budget
Headers + filters + tabs + action bars can consume the viewport.
On small screens prioritize one or two persistent layers and transform the rest.

## Specialized workspaces
Canvas/media/DAG apps should preserve primary content and move secondary chrome into temporary/collapsible surfaces.
Mobile may legitimately support review/inspection rather than full authoring if the authoring task is not practical, but make that product decision explicit.

## Anti-patterns
- desktop shrink ray
- capability removed instead of transformed
- three panes squeezed into tiny widths
- mobile table automatically converted to cards
- hidden active filters
- hover dependency
- touch targets too small
- breakpoint patchwork
- state reset on resize
- ultrawide content stretched without useful context
