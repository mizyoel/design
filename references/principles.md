# Design Principles

Use these principles as the governing layer for every `/design` task.

## Architecture
- Design the task, not the screenshot.
- Understand before proposing; inspect before redesigning.
- Preserve strong existing behavior and learned conventions.
- Solve structural problems structurally.
- Interaction architecture comes before visual styling.
- Favor the user's mental model over backend/database structure.
- Preserve useful context, scope, selection, and working state.

## Complexity
- Simplicity is not minimalism.
- Organize real complexity through hierarchy, grouping, density, and progressive disclosure.
- Keep frequent/important/state-defining controls visible.
- Move rare and advanced behavior deeper.
- High density can be excellent expert UX.

## Pattern quality
- Use the smallest sufficient pattern.
- Familiarity before novelty.
- Innovation must materially improve speed, comprehension, context, precision, or capability.
- Trend treatments must never compensate for weak architecture.
- Choose patterns by behavioral contract, not appearance.

## Frequency, scale, risk
Always ask:
- What happens after 500 repetitions?
- Does this work with 5, 500, and 500,000 objects?
- What does a mistake cost?

High-risk actions need scope clarity, review, audit, and recovery.
Low-risk reversible actions often benefit from immediate execution + Undo.

## State and async
- Design failure, retry, cancellation, conflict, offline, and partial success alongside success.
- Preserve useful existing content during refresh when possible.
- Waiting is an interaction. Match feedback to duration, structure, progress, and freedom.
- Be honest about queued, processing, saved, synced, and completed states.

## AI
- AI belongs inside the workflow.
- Direct manipulation beats conversation for simple precise work.
- Conversation is strongest when intent evolves or clarification matters.
- Expose scope, consequence, provenance, approval, cost, and undo when they matter.
- Suggest before automating when uncertainty/risk remains high.

## Accessibility and responsive
- Accessibility affects pattern choice from the start.
- Keyboard and focus behavior are part of product architecture.
- Drag should usually be an accelerator, not the only path.
- Responsive design preserves relationships and mental models, not coordinates.
- Adapt to available space, input, content pressure, zoom, and environment.

## Visual craft
- Structure before decoration.
- Every boundary should communicate something.
- Color spends attention.
- Typography and spacing carry most hierarchy.
- Use a restrained number of expressive motifs.
- Visual polish is the visible consequence of good decisions.

## Questions and convergence
- Ask only questions that materially change the design.
- Discover before asking.
- Ask progressively, not as a giant interview.
- Explore structurally different directions when real alternatives exist.
- When uncertainty becomes low, take a position.

## Final test
Optimize simultaneously for:
**clarity, context, throughput, trust, recovery, accessibility, and craft.**
