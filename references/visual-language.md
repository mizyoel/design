# Visual Language

Visual design is the visible expression of interaction architecture.

Do not decorate a weak structure.
Do not mistake novelty for quality.

A strong visual language should make the interface intentional, coherent,
understandable, efficient, trustworthy, distinctive, and resilient.

## Hierarchy first
Before styling establish:
1. primary information
2. secondary information
3. grouping
4. interactivity
5. selection
6. attention
7. what can recede

Use visual channels roughly in this order:
layout → position → size → spacing → typography → contrast → surface → color → elevation → motion.

## Typography
Typography carries much of hierarchy.
Use semantic roles rather than arbitrary per-component sizes.
Professional apps usually benefit from restrained type scales.
Use monospace selectively for IDs, code, paths, and technical values.
Do not make secondary text nearly illegible.

## Spacing
Spacing communicates relationships.
Use a constrained spacing scale.
Less space inside a group, more between groups.
Dense professional UI may legitimately use tighter rhythm.
Whitespace must improve comprehension, not merely make screenshots spacious.

## Surfaces
Use surfaces for real containment/layering.
Do not card every section.
If removing the border does not change meaning, question the card.

## Borders and elevation
Spacing before borders.
Borders for boundary/separation/state.
Elevation for actual layering such as menus, popovers, dialogs, floating tools.
Persistent panels often work better with subtle surface/border hierarchy than dramatic shadow.

## Radius
Use a coherent radius family.
Avoid pillifying every button/input/card.
Fully rounded geometry should communicate a component category or product character.

## Color
Separate:
- neutral structure
- brand/accent
- semantic state
- data visualization

Color spends attention.
Use semantic colors consistently and never as the only cue.
Accent gains power through scarcity.

## Dark mode
Do not invert light mode.
Design surface luminance, contrast, semantic colors, charts, focus, and elevation intentionally.
Avoid pure black + neon by default.

## Glass / translucency
Use when it helps spatial layering, immersive content, or temporary controls.
Do not make every panel translucent.
Readability and hierarchy win over novelty.

## Bento
Use for heterogeneous content with real hierarchy.
Tile size must mean something.
Do not replace tabular operational information with decorative bento.

## Gradients/glow
Use for brand, atmosphere, visualization, or meaningful emphasis.
Do not treat gradient/glow as "premium" or "AI" by default.

## Icons
Use one coherent family.
Prefer familiar glyphs.
Ambiguous/high-consequence actions need labels.
Avoid icon soup.

## Signature
A product can feel distinctive through one or two deliberate motifs:
- navigation geometry
- typography
- selection treatment
- data visualization language
- motion language

Distinctiveness does not require every component to be custom.

## Tokens
Prefer semantic tokens such as:
- surface-primary
- text-muted
- border-selected
- action-primary
- status-error

over raw color/value coupling.
Tokenize meaningful system decisions, not every pixel.

## Trend test
Classify internally:
- Foundation: hierarchy, typography, spacing, alignment, semantics
- System expression: radius, surfaces, elevation, density, icon/motion language
- Trend treatment: glass, extreme bento, neon gradients, glow, oversized type

The foundation must remain strong after removing the trend layer.

## Anti-patterns
- everything rounded
- every section a card
- shadows on every container
- random glass
- gradient title text
- purple as universal AI
- huge whitespace in expert tools
- low-contrast gray everywhere
- chips for ordinary metadata
- mixed icon families
- too many font sizes
- dark mode = black + neon
- selected and hover indistinguishable
- trend stacking
