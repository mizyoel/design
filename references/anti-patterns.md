# UI/UX Anti-Patterns

Use anti-patterns diagnostically, not dogmatically.

For every suspected issue state:
- **Symptom**
- **Root cause**
- **UX consequence**
- **Better direction**
- **Exception** when valid

Critique behavior before aesthetics.

## Structural anti-patterns

### Everything is a card
Every section gets equal boxed importance.
Repair with hierarchy, spacing, dividers, and real containment only where needed.

### Fake minimalism
Useful labels, state, filters, and actions are hidden for screenshot cleanliness.
Repair by organizing complexity rather than removing operational context.

### Modal labyrinth / overlay onion
`page → drawer → popover → modal → confirmation`
Repair by flattening the flow or promoting deep work to a page/workspace.

### Drawer application / popover application
Temporary surfaces gain tabs, deep navigation, large forms, or long duration.
Promote them.

### Sidebar dumping ground
Primary navigation, object hierarchy, utilities, and settings are mixed.
Separate navigation layers.

### Nested tabs / tabs for workflow
Tabs are peer views, not deep hierarchy or sequential workflow.
Use local nav, sidebar, disclosure, or stepper appropriately.

### Context amnesia
Back/navigation resets filters, scroll, selection, or workspace.
Preserve meaningful working state.

### Hidden scope
User cannot tell which project/selection/filter an action affects.
Expose scope before consequential operations.

## Data anti-patterns

### Giant dropdown
Large entity spaces are search problems. Use combobox/search picker.

### Fake table
Comparison-heavy records become cards.
Use table/grid/list based on task.

### Grid overkill
Read-only data gets spreadsheet semantics and complexity.
Use a semantic table if users mainly read/compare.

### Invisible filters
Closing filter UI hides evidence that scope changed.
Keep active criteria visible.

### Action icon soup
Every row exposes many ambiguous icons.
Keep frequent actions visible; move secondary actions to overflow.

### Dashboard museum / KPI cemetery
Many cards/charts with no decision path.
Organize Attention → Overview → Trend → Detail and support drill-down.

### Metadata wall
Every property has equal prominence.
Prioritize identity, status, important properties, then advanced/raw.

## Form anti-patterns
- placeholder as label
- premature validation
- form wipes after server error
- wizard for trivial work
- giant unstructured form
- accordion maze
- hidden save/autosave failure
- vague destructive confirmation
- free text for controlled values

## State/async anti-patterns
- hover = selected
- disabled mystery
- read-only styled as disabled
- partial success shown as failure
- toast carrying persistent truth
- spinner default
- full-screen spinner for local work
- skeleton replay on refresh
- shimmer storm/endless shimmer
- fake percentage progress
- background job trapped in page
- completion says only "Done"

## Motion anti-patterns
- hover gymnastics
- card lifts everywhere
- animation delaying interaction
- motion as latency camouflage
- reduced motion ignored
- celebration for routine saves

## Responsive anti-patterns
- desktop shrink ray
- three panes squeezed onto narrow width
- automatic table → cards
- hidden capability instead of transformed pattern
- touch retains hover/right-click assumptions
- sticky chrome consumes viewport
- breakpoint patchwork
- state reset on resize
- device stereotype instead of available-space reasoning

## Accessibility anti-patterns
- clickable div without semantics
- invisible focus
- Tab through every child
- right-click-only action
- drag-only workflow
- color-only status
- tiny targets justified by density
- modal without focus/dismissal contract
- hidden responsive controls still focusable
- chart usable only through hover

## AI anti-patterns
- chatbot everywhere
- purple/sparkle as AI strategy
- hidden AI scope
- generated result committed without review
- no diff/undo for consequential mutation
- structured results dumped into chat prose
- fake confidence precision
- fake reasoning theater
- agent black box
- approval fatigue
- agent overreach
- cost surprise
- no manual fallback

## Visual anti-patterns
- card inside card
- badge confetti
- semantic rainbow
- border bureaucracy
- shadow everywhere
- pillification
- bento for repetitive data
- glass everywhere
- giant headings in operational tools
- trend stacking
- everything primary / everything secondary

## Severity
Classify:
- Critical: data loss, dangerous scope, inaccessible core task, serious permission/security misunderstanding
- High: major core-workflow harm
- Medium: recurring friction
- Low: limited polish/craft weakness

Prioritize:
1. workflow
2. dangerous/hidden state
3. context loss
4. wrong pattern
5. accessibility
6. scale
7. responsive
8. hierarchy
9. polish

## Critique format
1. What works
2. Main structural problem
3. Concrete evidence
4. User consequence
5. Better interaction model
6. Keep / Remove / Change

Do not return thirty equal cosmetic complaints.
