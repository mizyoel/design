# Pattern Selection

Choose patterns from user intent, not trend.

## Decision dimensions

Evaluate:
- Intent: navigate, select, edit, inspect, compare, configure, create, monitor
- Object: item, collection, hierarchy, relationship, timeline, canvas
- Cardinality: one, few, many
- Scale: small, large, unbounded
- Frequency: rare, repeated
- Comparison need
- Context preservation need
- Task depth
- Expertise
- Input modality
- Risk
- Persistence

## Fast map

### Choice/input
- 2–5 visible exclusive options → radio / segmented control
- one known choice from manageable list → select/dropdown
- large searchable set → combobox
- several independent values → checkboxes
- multiple selections → multiselect
- free text + suggestions → editable combobox/autocomplete

### Actions
- frequent action → visible button/toolbar
- secondary action set → overflow menu
- object-local expert actions → context menu plus visible equivalent
- global expert navigation/action → command palette

### Context surfaces
- brief nonessential explanation → tooltip
- small contextual interaction → popover
- persistent selected-object properties → inspector
- temporary secondary work → drawer/side sheet
- focused blocking decision/task → modal
- deep/navigable/persistent work → page

### Collections
- compare structured attributes → table
- interactive structured work → data grid
- visual browsing → cards/gallery
- heterogeneous browsing → list
- hierarchy → tree
- hierarchy + columns → treegrid
- relationships/dependencies → graph/DAG only when relationships are the task
- time → timeline
- stages → kanban
- heterogeneous high-level overview → dashboard/bento

### Workspace
- repeated browse + inspect → master-detail
- navigator + primary work + properties → three-pane workspace
- simultaneous comparison → split view
- spatial authoring → canvas
- source-target relationships → mapping workspace

## Pattern conflict tests

Ask:
- Is this a peer view or a workflow stage? Tabs vs stepper.
- Is this navigation or selection? Sidebar/tabs vs segmented.
- Is content temporary or persistent? Drawer vs inspector.
- Does the user need underlying context? Drawer/split vs page/modal.
- Is comparison primary? Table/grid before cards.
- Are relationships primary? Graph only if yes.
- Is the option space searchable? Combobox before giant dropdown.
- Is direct manipulation faster than language? Prefer direct UI.

## Frequency adaptation
Occasional work can tolerate more guidance.
Repeated expert work should reduce modal interruptions, repeated clicks, and hidden controls.

## Density adaptation
Dense professional surfaces should prefer stable alignment, compact controls,
persistent context, and keyboard acceleration.

## Recommendation format
For major decisions state:
- **Pattern**
- **Why**
- **Instead of**
- **Trade-off**

Reject any rationale whose main justification is simply "modern."
