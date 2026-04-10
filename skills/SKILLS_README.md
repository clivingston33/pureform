\# Skills



This folder contains the Pureform skill files — the actual shipped product.



\---



\## What's here



| File / Folder | Purpose |

|---------------|---------|

| `SKILL\_TEMPLATE.md` | Template for creating new skills |

| `taste/` | Visual hierarchy, restraint, finish quality |

| `layout/` | Spacing, grid, compositional structure |

| `type/` | Typography scale, weight, readability |

| `color/` | Palette, contrast, semantic color usage |

| `components/` | Button, card, input, navigation patterns |

| `states/` | Loading, empty, error, disabled states |

| `dark-mode/` | Dark mode elevation, color, border logic |

| `motion/` | Transition timing, easing, when not to animate |



\---



\## How skills are structured



Each skill folder contains a `SKILL.md` file. That is the file your AI coding tool loads. It is written as direct instructions, not research notes.



The research and evidence behind each skill is in \[`/research`](../research/README.md). If you want to understand why a rule exists, start there.



\---



\## Creating a new skill



Copy `SKILL\_TEMPLATE.md` into a new folder and follow the template. Read `CONTRIBUTING.md` before writing rules — the format requirements exist to keep skills machine-usable.



\---



\## Skill status



Skills move through three stages:



\- `draft` — being written, not benchmarked yet

\- `active` — benchmarked and producing measurable improvement

\- `deprecated` — replaced by a newer skill or merged into another



Check the frontmatter of each `SKILL.md` file for current status.

