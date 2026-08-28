# Overlays & Contextual Surfaces

Choose the smallest surface that fully supports the task.

Escalation:
**Tooltip → Popover → Drawer/Side Sheet → Dialog → Page/Workspace**

Each step increases space, depth, persistence, focus demands, interruption, and navigational responsibility.

## First question
Does the user need the underlying content while completing this task?
- yes → inline, popover, split, drawer, inspector
- no / blocking decision required → dialog or page

## Tooltip
Brief, nonessential supplemental text.
No required instructions, forms, system feedback, or critical errors.
Support hover and keyboard focus; never depend on hover for task completion.

## Toggletip / info popover
User-invoked supplemental explanation with slightly more persistence.
If most users need the information, make it visible instead.

## Popover
Small contextual information or interaction anchored to a clear trigger.
Good for compact filters, date selection, quick settings, simple properties.
Avoid nested popovers and long scrolling workflows.

## Menu
Commands/actions, not general content.
Keep hierarchy shallow.
Context menus accelerate object actions but must not be the only route.

## Drawer / side sheet
Temporary secondary work while parent context remains relevant.
Good for inspect, edit, preview, filter configuration, job detail.
If it gains tabs, deep navigation, long duration, multiple scroll areas, or child overlays, promote it.

## Inspector
Persistent, selection-driven properties/actions.
It is part of workspace architecture, not a temporary drawer.

## Dialog
Use for focused interruption or blocking decision.
Modal means the background is unavailable.
Define focus entry, tab containment, Escape, dismissal, and restoration.
Avoid nested dialogs and modal chains.

## Page
Use when the task deserves navigational identity:
deep linking, history, long duration, complex forms, internal navigation,
collaboration, substantial drafts, broad workspace.

## Dismissal and work loss
Outside click is fine for menus/light popovers.
Do not let accidental outside click destroy meaningful edits.
Use autosave, Save/Cancel, draft, or dirty-state protection.

## Responsive transformation
Desktop popover → mobile bottom sheet
Desktop side sheet → mobile full-screen detail
Desktop inspector → properties route/sheet
Desktop modal → full-screen modal/page when needed

Preserve task identity and state.

## Overlay rules
- Every overlay has a clear owner.
- Placement reinforces origin.
- Avoid nested scroll traps.
- Escape closes the topmost valid temporary layer first.
- Restore focus after close.
- Visual modality must match behavioral modality.
- Z-index is not information architecture.

## Promotion triggers
Promote to page/workspace when users need:
- bookmarking/sharing
- many steps
- tabs/local navigation
- long sessions
- large tables
- collaboration
- substantial drafts
- repeated nested overlays

## Anti-patterns
- tooltip dependency
- help-icon forest
- popover application
- drawer application
- modal labyrinth
- overlay onion
- outside-click data loss
- unclear owner
- no focus restoration
- permanent drawer that should be inspector
