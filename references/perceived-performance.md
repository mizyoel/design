# Perceived Performance

Performance UX designs the gap between user intention and system completion.

## Classify the wait
Examples:
- initial load
- navigation
- local request
- save/submit
- sync/refresh
- filter/search/query
- upload/download/import
- processing
- AI generation
- multi-stage job
- background work

## Decision model
1. Is it effectively immediate? → no loader; still acknowledge interaction.
2. Does valid content already exist? → preserve it and show local updating state.
3. Is final structure predictable? → skeleton.
4. Is progress measurable? → determinate progress.
5. Is it long-running? → persistent/background job.
6. Is the operation reversible and high-confidence? → consider optimistic UI.

## Priority
Prefer:
**immediate acknowledgement → optimistic result → preserve existing content → progressive load → local activity → skeleton → determinate progress → background job**

Use blocking only when continued interaction is unsafe.

## Skeleton
Use for predictable absent structure.
Approximate final geometry.
Do not skeleton stable navigation/toolbars/labels.
Avoid replaying skeleton for routine refresh when valid content already exists.

## Shimmer
Optional skeleton treatment that communicates activity, not progress.
Keep subtle, synchronized, and reduced-motion compatible.
Do not use for indefinite long processes.

## Spinner/activity
Use for localized unknown-duration operations when structure/progress cannot be shown.
Avoid full-screen spinner for local work.

## Progress
Use determinate progress only when real progress can be measured.
Multi-stage jobs may communicate stages better than fake percentage.

Examples:
Queued → Reading → Processing → Validating → Complete

## Background work
Long jobs should allow users to continue where safe.
Expose persistent identity, progress, cancel/retry where supported, and result link.

## Refresh
Prefer stale-while-refresh behavior:
keep valid content, mark updating, replace when ready.
Avoid context-destroying blank states.

## Search
Debounce remote execution when useful, but keep input acknowledgement immediate.
Prevent older responses from overwriting newer queries.

## Partial results/failure
Expose usable partial results.
Retry only the failed subset where possible.
Cancellation semantics must be clear.

## AI
Use structured streaming, stage/progress, preview, and background activity according to task.
Do not hide variable latency behind theatrical "Thinking…" indefinitely.

## One loading narrative
A surface should normally have one dominant explanation of what is happening.
Avoid spinner + shimmer + progress bar + toast all describing the same wait.
