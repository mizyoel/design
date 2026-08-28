# Data-Heavy UI

Design professional interfaces around work, not decoration.

High density is not inherently clutter. Low density is not inherently simple.
Optimize **orientation + throughput + trust**.

A data interface should answer:
- Where am I?
- What am I looking at?
- What is selected?
- What changed?
- What needs attention?
- What can I do to this scope?
- Where did this data come from?
- What happens next?

## Start from the operation
Do not start with "we need a table."
Identify the repeated job:
- browse
- triage
- compare
- edit
- approve
- investigate
- map
- monitor
- bulk operate

## Workspace model
Think in four layers:
1. Scope
2. Navigation/filtering
3. Primary workspace
4. Context/detail

Preserve high-value working state:
filters, sort, search, scroll, selection, inspector, saved view.

## Tables and grids
Use table for reading/comparison.
Use grid when users also edit/select/keyboard-navigate/copy-paste/configure columns.

Design:
- stable primary identifier
- semantic column order
- honest column widths
- sort state
- sticky headers when useful
- pinned identity columns when needed
- user column show/hide/reorder/pin for repeated expert work
- virtualization for scale when accessibility/focus behavior is tested

Do not cardify tabular comparison by default.

## Filtering
Layer by frequency:
- frequent visible filters
- active filter chips/summary
- More filters
- advanced query builder only when needed

Always expose active scope after filter surfaces close.

Facets should support meaningful counts when useful.
Filtered/search empty states must be distinct from true empty data.

## Saved views
A saved view may persist:
- filters
- search
- sort
- grouping
- columns
- density
- visualization
- scope

Define ownership: private/shared/team/project/default.

## Selection
Selection is explicit state.
Support:
- single selection driving inspector/detail
- multiselect with clear count/scope
- page vs all-matching distinction
- hidden selections awareness
- selection tray for long-lived cross-page selection

## Bulk actions
Show contextual actions after selection.
Make scope explicit.
Support progress, partial failure, retry, and Undo where reasonable.

## Detail
Choose by frequency:
- frequent repeated inspection → inspector/master-detail
- occasional detail → drawer
- deep administration → page
- supplementary detail only → expandable row

## Provenance and trust
For important data expose appropriate:
- source
- lineage
- version
- derived value
- transformation
- freshness
- audit
- data quality

Raw data is an expert layer, not the primary UI.

## Triage mode
For queues, optimize:
`queue → object → decision → next`
Support keyboard shortcuts and stable context.

## Dashboards
Organize:
**Attention → Overview → Trend → Detail**
Charts must answer actual questions and drill into data.
Avoid one-number-card cemeteries and chart museums.

## Async
Preserve stable headers/filter/selection during refresh.
Long-running ingestion/export/AI should become persistent jobs with object identity,
progress, partial failure, and result links.

## Scale test
Stress at:
- 10 rows
- 1,000 rows
- 1,000,000 rows
- long labels
- dense state
- multi-select
- slow data
- narrow screen

## Anti-patterns
- giant dropdown for entities
- invisible filters
- hidden selection scope
- cards for comparison-heavy data
- every value as badge
- row action icon soup
- app-wide spinner for local operation
- no partial failure
- metadata wall
- no provenance in consequential data workflows
