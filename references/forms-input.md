# Forms & Input

Forms are workflows, not collections of fields.

Start with the outcome the user is trying to produce, then choose the editing model.

## Editing models
Choose among:
- simple form
- long structured form
- wizard/stepper
- inline editing
- inspector editing
- grid editing
- autosave workspace
- draft + publish
- bulk editor
- query builder
- direct manipulation

Do not default to a giant form.

## One page vs wizard
Prefer one page when users benefit from seeing relationships and revisiting fields.
Use wizard when sequence, dependency, or cognitive load creates meaningful stages.
Do not split trivial workflows merely to appear simple.

## Progressive disclosure
Reveal dependent controls near the choice that activates them.
Hide genuinely irrelevant controls rather than showing disabled complexity.
Keep layout changes causally understandable.

## Field design
Each field may need:
- persistent label
- optional/required cue
- input
- helper text
- validation
- unit
- action

Placeholder supplements; it never replaces the label.
Control width may communicate expected input size.

## Choose the right input
- known small choice → radio/segmented
- known manageable choice → select
- large searchable entity set → combobox
- independent options → checkbox
- persistent binary state → switch
- exact number → numeric input
- approximate adjustment → slider, ideally paired with number if precision matters
- known date → allow direct entry; calendar when browsing nearby dates helps
- path → direct entry + browse when experts benefit
- file/folder → explicit formats/scope/progress/retry plus non-drag browse route

## Defaults
Use safe smart defaults from context, product conventions, or user preference.
Do not silently choose consequential defaults.
Persist deliberate repeated preferences, not every accidental last value.

## Save model
Make persistence explicit:
- explicit Save
- autosave
- draft
- Apply
- Publish

Saved, synced, draft, and published are different states.

Autosave needs visible failure/offline/conflict behavior.
Explicit save needs dirty-state and navigation-loss behavior.

## Validation timing
Choose based on field behavior:
- during input when early feedback is useful
- debounce for remote checks
- blur when intermediate values are normally incomplete
- submit for conventional forms where interruption would harm flow
- server validation for authoritative constraints

Preserve entered work on validation failure.
Field errors should say what is wrong and how to fix it.
Large forms may add an error summary.

## Risk
Use confirmation for high-impact or irreversible actions.
Prefer Undo for low-risk reversible actions.
Preview/diff before broad, expensive, permission, schema, or AI transformations.

## Bulk edit
Support mixed state, explicit selection scope, consequence preview, partial failure, retry.

## Keyboard
Tab order follows logical task order.
Respect standard editing keys.
Add visible shortcuts for repeated expert work where useful.

## Anti-patterns
- placeholder-only labels
- every field full-width
- free text for controlled data
- premature validation
- server error wipes form
- giant form
- wizard for trivial work
- dependent fields far from trigger
- hidden save model
- destructive setting beside routine controls
- drag-only upload
- slider without precise entry in technical contexts
- raw backend schema rendered as text fields
