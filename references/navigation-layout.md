# Navigation & Layout

Navigation creates the product's spatial mental model. Layout defines which contexts coexist.

Always answer:
- Where am I?
- What scope am I in?
- What is selected?
- Where can I go?
- What stays visible?
- What is temporary?
- How do I return?

## Navigation layers
Separate:
1. Global context: organization/project/environment
2. Primary product navigation: major destinations
3. Local navigation: peer views of current object
4. Object navigation: tree/list/previous-next
5. Temporary surfaces: drawer/dialog/popover

Do not express every layer with the same pattern.

## Primary patterns
- Sidebar: persistent labeled destinations, strong for professional desktop apps.
- Rail: compressed stable destinations when horizontal space is tight.
- Top nav: shallow products with few destinations.
- Bottom nav: a few peer high-frequency mobile destinations.
- Drawer: hidden navigation when persistent navigation cannot fit.
- Workspace switcher: changes high-level scope; active scope must remain obvious.
- Breadcrumb: hierarchical location, not history or workflow.
- Tabs: peer views of same object/context, not global app navigation.
- Stepper: ordered workflow, not hierarchy.

## Workspace models

### Master-detail
Use for repeated collection → object inspection.
Selection updates detail without destroying list state.

### Three-pane
`Navigator | Workspace | Inspector`
Use only when all three contexts are repeatedly needed.

### Split view
Use when two contexts must be simultaneously compared or coordinated.

### Inspector
Persistent selection-driven properties/actions.
If rarely needed, prefer drawer.

### Side sheet
Temporary secondary work while parent remains relevant.
If it gains tabs, deep navigation, long duration, or complex forms, promote it.

### Immersive workspace
Editors/media/canvas may reduce shell chrome temporarily. Preserve an obvious route back.

## Spatial rules
- Stable shell placement builds spatial memory.
- Persistent regions must earn permanent space.
- Allocate width by task importance, not symmetry.
- Avoid uncontrolled nested scrolling.
- Keep toolbars close to the content they control.
- Put actions near the scope they affect.
- Preserve list/filter/scroll state through drill-down and back.

## Responsive transformation
Preserve the mental model.

Example:
- Wide: Sidebar | Navigator | Workspace | Inspector
- Medium: Rail | Workspace | collapsible inspector
- Narrow: collection → detail → properties, navigation via drawer

Re-architect when simultaneous panes no longer remain usable.

## URL/history
Give URL identity to meaningful navigation:
- page
- object
- significant tab
- shareable selected record
- useful search/filter state

Do not put transient tooltips/popovers into browser history.

## Anti-patterns
- five-level sidebar hierarchy
- nested tabs
- breadcrumb used as history
- stepper used as navigation
- app-inside-drawer
- deep work inside modal
- arbitrary panel sides
- back resets filters/scroll
- three panes squeezed onto mobile
- navigation hidden for screenshot cleanliness
