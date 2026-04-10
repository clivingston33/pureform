# Pureform

Frontend skill library for AI coding tools — layout, hierarchy, redesign, and finish quality.

```bash
npx skills add clivingston33/pureform
```

---

## What it is

Pureform is a set of skill files that give AI coding tools (Claude Code, Kilo, opencode, etc.) deep frontend design knowledge. Instead of generic output, you get UI that follows the same decisions used by Stripe, Linear, Vercel, and other production design systems.

Each skill is a focused instruction set. You install the ones you need and the AI applies them when generating or editing your frontend code.

---

## Skills

| Skill | Status | Description |
|-------|--------|-------------|
| `taste` | planned | Visual hierarchy, restraint, and finish quality |
| `layout` | planned | Spacing, grid, and compositional structure |
| `type` | planned | Typography scale, weight, and readability |
| `color` | planned | Palette, contrast, and semantic color usage |
| `components` | planned | Button, card, input, and navigation patterns |
| `states` | planned | Loading, empty, error, and disabled state coverage |
| `dark-mode` | planned | Dark mode elevation, color adjustment, and border logic |
| `motion` | planned | Transition timing, easing, and when not to animate |

---

## How it works

Skills are plain markdown files. When you add them to your project, your AI coding tool reads them as context before generating code. The skill files contain specific, evidence-based rules derived from real production design systems — not vague suggestions.

The research behind each skill is in [`/research`](./research/README.md).

---

## Installation

```bash
# Install all skills
npx skills add clivingston33/pureform

# Install a specific skill
npx skills add clivingston33/pureform/layout
```

---

## Benchmarks

Each skill is tested against a set of reference prompts and evaluated against screenshots from the production design systems the skills are derived from. See [`/benchmarks`](./benchmarks/README.md) for methodology and results.

---

## Research

The skills in this library are derived from a systematic analysis of 7 production design systems (Stripe, Vercel, Linear, Clerk, Railway, shadcn/ui, Stripe Docs) plus supplementary sources. The full research and evidence base is in [`/research`](./research/README.md).

---

## Status

Early development. Skills are being written and benchmarked. Not production-ready yet.

---

## Author

[@clivingston33](https://github.com/clivingston33)
