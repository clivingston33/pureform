\# Contributing to Pureform



\---



\## What a skill is



A Pureform skill is a focused, evidence-based instruction set for AI coding tools. It tells the AI how to make specific frontend design decisions — not what to build, but how to build it well.



A skill is not:

\- A component library

\- A design system

\- A collection of vague style suggestions

\- Opinion without evidence



Every rule in a skill file should trace back to an observation in the research doc or be explicitly tagged as a taste preference. Ungrounded rules dilute the library.



\---



\## Before writing a skill



Read the research doc first: `research/Design\_System\_Analysis\_-\_Reference\_Sites\_Research.md`



Identify which sections are relevant to the skill you want to write. Note the confidence tags on the findings you plan to use. Rules derived from `high-confidence` or `observed` findings are stronger than rules derived from `inferred` findings.



Read the community conventions doc if your skill touches taste-level decisions: `research/Pureform\_Community\_Conventions\_and\_Taste\_Policy.md`



\---



\## Skill file format



Use `skills/SKILL\_TEMPLATE.md` as the starting point for every new skill. Do not deviate from the template structure without a reason documented in the skill file itself.



The most important format rules:



\*\*Rules must be instructional, not descriptive.\*\*



```md

\# Wrong — descriptive

All reference systems use base-4 spacing.



\# Right — instructional

Use base-4 spacing. All spacing values must be multiples of 4px (4, 8, 12, 16, 24, 32, 48, 64, 80, 96). If a layout requires 14px gap, use 16px instead.

```



\*\*Constraints need operational definitions.\*\*



```md

\# Wrong — vague

Never use oversized headings.



\# Right — defined

Never use H1 above 72px outside of a display or hero context. Body-level headings must stay within the type scale defined in the type skill.

```



\*\*Decision logic must be explicit.\*\*



If a rule applies conditionally, document the condition. An AI cannot guess context.



\---



\## How to test a skill



Every skill requires a benchmark before it is marked `active`. See `benchmarks/README.md` for the full methodology.



Minimum requirement for a skill to move from `draft` to `active`:

\- A benchmark prompt exists in `benchmarks/\[skill-name]/prompt.md`

\- A baseline run exists (output without the skill)

\- At least one evaluated run exists showing measurable improvement

\- The evaluation notes document what improved and what gaps remain



Do not mark a skill `active` based on subjective impression. Run the benchmark.



\---



\## Skill scope



Each skill should cover one coherent design decision domain. If a skill is trying to do too many things, split it.



Overlap between skills is acceptable but each skill should be independently useful. A user should be able to load only the `layout` skill and get meaningful improvement on layout decisions without needing `taste` or `type`.



\---



\## Submitting a skill



1\. Create the skill file using the template

2\. Add research doc section references to the frontmatter

3\. Run the benchmark and save results to `benchmarks/\[skill-name]/`

4\. Open a pull request with both the skill file and the benchmark results

5\. The PR description should answer: what does this skill improve, what does it not cover, and what evidence supports the rules



\---



\## Editing existing skills



If you find a rule that contradicts evidence from the research doc, flag it with a comment and open an issue before changing it. Rules are not changed based on preference — they are changed based on evidence or benchmark results showing the rule doesn't improve output.



If you want to add a rule that is taste-level rather than evidence-based, it belongs in the community conventions doc, not in a skill file, unless it is explicitly tagged as `pureform-override` with a justification.

