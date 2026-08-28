# Motion & Interaction

Motion is interaction architecture, not decoration.

Use motion to communicate:
- response
- causality
- state
- hierarchy
- spatial relationship
- continuity
- progress
- success/failure when useful

## Interaction states
### Hover
Subtle enhancement, never the only route to essential behavior.

### Press
Acknowledge immediately. Do not delay the action to finish animation.

### Focus
Highly visible and distinct from hover/selection.

### Selected
Persistent. May drive inspector/toolbars.

### Reveal
Open from a meaningful spatial origin when that helps causality.

### Expand/collapse
Preserve continuity and avoid disorienting layout jumps.

## Microinteraction model
**Trigger → Response → Result**

Feedback should answer what happened and what state now exists.

## Optimistic interaction
Use for high-confidence, reversible, low-risk actions.
Avoid for payments, irreversible destructive actions, security, or expensive uncertain work.

## Loading
Motion should support the chosen performance strategy:
- skeleton
- local activity
- progress
- staged job
- background work

Shimmer is not a loading strategy by itself.

## Layout transitions
Track objects when continuity matters.
Dense tables and professional workflows often benefit from stability rather than elaborate reflow.

## Shared-object continuity
Useful for transitions such as thumbnail → detail or item → inspector when it clarifies identity.

## Interruptibility
Users should be able to continue acting while safe.
Interaction must outrun decoration.

## Frequency
Reduce animation budget as repetition increases.
A delightful one-time effect can become expensive at 500 repetitions.

## Reduced motion
Preserve meaning with simpler transitions/static states.
Avoid large translation, zoom, parallax, and perpetual decorative motion when reduced motion is requested.

## Anti-patterns
- card lift on everything
- hover gymnastics
- success animation for trivial actions
- animation blocking next interaction
- shimmer storm
- fake progress motion
- motion used to hide latency
- important information encoded only in animation
