# design

A professional product-design reasoning skill for GitHub Copilot and other
`SKILL.md`-compatible coding agents.

It helps an agent reason like a senior product designer / UX architect before
jumping into implementation or visual polish.

## What it is good at

- feature and page redesign
- data-heavy professional applications
- tables, grids, filtering, selection, bulk workflows
- schema mapping and DAG/editor UX
- forms and configuration
- navigation and workspace architecture
- loading, progress, skeletons, and background jobs
- AI-native product interaction
- responsive/adaptive design
- accessibility
- visual language and critique

The skill uses a compact core plus selectively loaded references so complex
design tasks get depth without loading the whole library for every button.

## Install locally

From the directory containing this package:

```bash
npx skills add ./design -a github-copilot
```

For a global install:

```bash
npx skills add ./design -a github-copilot -g
```

GitHub Copilot also supports placing the `design` directory directly under
one of its supported skill locations, such as:

```text
.github/skills/design/
~/.copilot/skills/design/
~/.agents/skills/design/
```

## Publish to GitHub

If this repository contains the `design/` directory at its root, users can
install it with the `skills` CLI, for example:

```bash
npx skills add OWNER/REPO --skill design -a github-copilot
```

or from the direct skill path:

```bash
npx skills add https://github.com/OWNER/REPO/tree/main/design -a github-copilot
```

## Interactive design loop

An explicit non-trivial `/design` invocation is intentionally interactive:

```text
inspect
→ present 2–3 professional design directions
→ native Decision Round
→ Converge / Explore / Deeper Questions / Challenge Assumptions
→ final recommendation
→ implementation/document/critique next actions
```

The model should not jump directly to a final recommendation merely because it
can infer a plausible answer.

Small pattern questions and requests that explicitly ask for no questions may
still be answered directly.

## Closed-loop implementation review

`/design` does not end when implementation finishes.

After each meaningful implementation milestone it should:

```text
implement
→ inspect the actual result
→ compare against the agreed UX
→ review states/responsive/accessibility/visual hierarchy
→ fix safe local gaps when possible
→ suggest the strongest continuation choices
→ continue until the user explicitly stops
```

Passing tests is not considered sufficient evidence that the design is finished.

## Invocation

User-invocable:

```text
/design redesign this schema mapping page
```

The frontmatter also allows model invocation, so a compatible agent may load
the skill automatically when the request materially benefits from product
design or UX reasoning.

## Package structure

```text
design/
├── SKILL.md
└── references/
    ├── principles.md
    ├── pattern-selection.md
    ├── navigation-layout.md
    ├── data-heavy-ui.md
    ├── forms-input.md
    ├── overlays-context.md
    ├── ai-native-ui.md
    ├── states-feedback.md
    ├── perceived-performance.md
    ├── motion-interaction.md
    ├── responsive.md
    ├── accessibility.md
    ├── visual-language.md
    └── anti-patterns.md
```

## Version

Closed-loop design release: **v0.3.0**

The best next step is to test it against diverse real tasks and use the
failures to tune routing, question behavior, and reference depth before adding
large example libraries.
