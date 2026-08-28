# AI-Native UI

AI is a capability, not automatically a chatbot.

Choose the interaction model according to the AI job:
- assistant
- recommender
- generator
- transformer
- analyzer
- classifier
- searcher
- planner
- agent
- monitor

## Interaction ladder
Use the smallest model that fits:
**passive intelligence → contextual suggestion → inline action → command → preview → copilot panel → conversation → agent → background agent**

## Suggestions
Show near the affected object.
Distinguish Suggested from Applied.
Where useful expose reason, uncertainty, accept/reject/edit.

## Inline actions
Use task language:
- Auto-map fields
- Suggest tags
- Summarize session
- Find anomalies
Do not label everything "AI" or "Magic."

## Conversation
Use when intent evolves, follow-up matters, clarification is natural, or exploration is iterative.
Do not replace simple precise direct manipulation with chat.

## Hybrid interaction
Use UI state as context.
Example: user selects 42 records, then asks a natural-language question about that selection.
Do not force users to restate obvious interface context.

## Scope
When consequence matters, users must know what AI operates on:
- current project
- selected objects
- active filters
- current document
- attached sources

Allow context pinning/editing for long tasks when useful.

## Generation
For consequential transformations prefer:
**Configure → Generate → Preview → Refine → Apply**

Do not silently overwrite valuable authoritative state.

Render generated artifacts natively:
- records → table
- mappings → mapping workspace
- media → editor/gallery
- timeline → timeline
- structured plan → structured plan

Conversation can orchestrate; native UI should hold the artifact.

## Diff, versions, undo
Show appropriate before/after or field/object diff.
Allow selective apply when output contains mixed confidence.
Regeneration should not automatically destroy valuable earlier results.
Support Undo/history where technically possible.

## Provenance and uncertainty
Expose evidence/sources/freshness where trust depends on them.
Use confidence only when it drives decisions.
Prefer meaningful categories such as High / Needs review / Uncertain over fake precision.
Explain surprising or consequential recommendations with actionable evidence.

## AI states
Model honestly:
Ready → Preparing/Queued → Running → Needs input/approval → Complete
plus Partial failure / Failed / Canceled.

Streaming can reduce latency but unfinished content must not look final.
Batch work should expose partial results and narrow retry.

## Agents
Agents may plan, call tools, act across steps, wait, resume, and operate in background.

Define appropriate:
- goal
- scope
- permissions
- action boundary
- approval checkpoints
- cost/resource boundary
- progress/activity
- audit/result

Autonomy ladder:
1. suggest
2. prepare
3. execute with approval
4. execute within boundaries
5. monitor and act

Require approval for consequential boundaries, not every harmless step.

## Long-running agents
Move durable work into persistent activity/job surfaces.
Allow leave-and-return, cancel when possible, and clear result handoff.
Do not trap 10-minute work behind "Thinking…".

## Cost
When AI consumes meaningful money/credits/compute, communicate useful estimate/range
before execution and allow guardrails for autonomous work.

## Manual fallback
Where AI augments a core workflow, preserve deterministic/manual paths when feasible.
Degraded AI should not unnecessarily break the whole product.

## Anti-patterns
- chatbot everywhere
- purple/sparkle as AI strategy
- hidden scope
- generated output auto-committed
- no preview or undo
- structured results dumped into prose
- fake confidence precision
- fake reasoning theater
- agent black box
- approval fatigue
- agent overreach
- cost surprise
- no manual fallback
