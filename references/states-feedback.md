# States & Feedback

Treat the interface as a state machine wearing a visual system.

## State grammar

### Interaction
default, hover, pressed, focus, selected, active, dragged, drop target

### Availability
enabled, disabled, read-only, hidden, locked, permission-restricted

### Data
empty, populated, incomplete, invalid, stale, dirty, saved, synced, conflicted

### Operation
idle, queued, loading, processing, saving, uploading, generating, retrying, canceling

### Outcome
success, warning, error, partial success, canceled

### Connectivity
online, reconnecting, offline, sync pending, sync failed

## Rules
- State is not merely styling.
- Hover is temporary; selection is persistent.
- Focus and selection are distinct.
- Disabled, read-only, locked, hidden, and permission-restricted mean different things.
- Saved and synced may differ.
- Warning allows continuation; error blocks or invalidates.
- Pending/queued/processing are not interchangeable.
- Partial success is first-class.
- Preserve input/work on recoverable failure.
- Use local feedback for local state and global feedback for global state.
- Avoid impossible compound states.

## Empty states
Differentiate:
- first-use empty
- filtered empty
- search empty
- permission empty
- error-induced empty

## Save model
Expose dirty/saving/saved/sync-failed states where work loss matters.
For autosave, hidden failure is unacceptable.

## Selection
Make scope clear in multi-select and batch workflows.
Selection may drive inspector, toolbar, and bulk operations.
Preserve selection intentionally across refresh/navigation where useful.

## Destructive actions
Use confirmation proportionally to risk.
For reversible lower-risk actions, prefer action + Undo.
State object/count/scope explicitly.

## Permissions
If permission changes during work, preserve the user's valid input where possible
and explain what can be done next.

## Feedback surfaces
- field → field message
- object → inline/object status
- section → section message
- page → banner
- transient low-risk event → toast
- persistent system/work state → persistent status/activity

## State matrix
For substantial features define:
- entry state
- trigger
- transition
- success
- error
- retry/recovery
- persistence across navigation/refresh

## Anti-patterns
- hover and selected look identical
- disabled mystery
- read-only styled as unavailable
- hidden save model
- color-only status
- warning treated as error
- partial success shown as failure
- transient toast carrying persistent truth
- stale/dirty/conflict not modeled
