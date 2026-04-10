\# Benchmarks



This folder contains test prompts, reference screenshots, and results for each Pureform skill.



Benchmarks are how we know the skills actually work. A skill file that doesn't measurably improve AI output quality is not a finished skill.



\---



\## Methodology



Each skill is tested with a standard prompt against a baseline (no skill) and evaluated by comparing the output to reference screenshots from the production design systems the skill is derived from.



\### Process



1\. \*\*Baseline run\*\* — Generate a UI component using only the task prompt, no skill files. Screenshot the output.

2\. \*\*Skill run\*\* — Generate the same component with the skill file loaded. Screenshot the output.

3\. \*\*Reference\*\* — Pull the equivalent component from the relevant reference site (Stripe, Linear, Vercel, etc.).

4\. \*\*Evaluate\*\* — Compare baseline vs skill output against the reference. Document what improved and what didn't.

5\. \*\*Iterate\*\* — Update the skill file based on gaps identified in evaluation. Repeat until the skill produces consistent improvement.



\### What counts as improvement



A skill passes if it produces measurable improvement in at least three of these areas:



\- Spacing discipline (base-4 grid adherence)

\- Typography hierarchy (correct scale ratios, weight usage)

\- Color restraint (single accent, no oversaturation)

\- Component finish (states covered, transitions present)

\- Visual hierarchy (clear primary element, suppressed secondary elements)



\### Benchmark prompts



Each prompt is written to be representative of a real use case, not optimized to make the skill look good. Prompts are fixed — they don't change between benchmark runs so results are comparable across iterations.



\---



\## Structure



```

benchmarks/

├── README.md               ← this file

├── taste/

│   ├── prompt.md           ← the test prompt

│   ├── reference/          ← reference screenshots from production sites

│   │   └── stripe-card.png

│   ├── baseline/           ← output without skill loaded

│   │   └── run-1.png

│   └── results/            ← output with skill loaded + evaluation notes

│       ├── run-1.png

│       └── evaluation.md

├── layout/

│   └── ...

├── type/

│   └── ...

└── ...

```



\---



\## Running benchmarks



Benchmarks are run manually using Kilo CLI with the target model specified in the prompt file. Each prompt file includes the model used so results are reproducible.



```bash

\# Example — run taste benchmark with Claude Sonnet

kilo run benchmarks/taste/prompt.md --model claude-sonnet-4-6

```



Results are saved to the `results/` folder for that skill with a timestamp.



\---



\## Status



| Skill | Benchmark written | Baseline captured | Passing |

|-------|------------------|-------------------|---------|

| taste | no | no | no |

| layout | no | no | no |

| type | no | no | no |

| color | no | no | no |

| components | no | no | no |

| states | no | no | no |

| dark-mode | no | no | no |

| motion | no | no | no |

