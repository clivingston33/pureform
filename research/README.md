# Research

This folder contains the evidence base that Pureform skills are derived from. It is reference material, not the shipped product.

---

## Files

### Design_System_Analysis_-_Reference_Sites_Research.md

The primary evidence document. Contains quantitative metrics and qualitative observations extracted from 7 production design systems through screenshot analysis and HTML/CSS source inspection.

Covers: typography systems, color architecture, spacing scales, component structures, shadow and border patterns, animation timing, responsive breakpoints, compositional patterns, constraint rules, state coverage, motion decisions, and dark mode specifics.

Every claim is tagged with a confidence level. Token extraction sections (1-11) are direct observations. Analytical sections (12+) use confidence tags to indicate how strongly each finding is supported.

**Primary sources:** Stripe, Vercel, Linear, Clerk, Railway, shadcn/ui, Stripe Docs

**Supplementary sources:** Airbnb, Liveblocks Dashboard (system-specific observations only)

### Pureform_Community_Conventions_and_Taste_Policy.md

A separate file for taste-based rules, community conventions, and style opinions that are not directly extractable from the reference sites. These complement the research doc but carry lower evidential weight.

Every item is tagged with a confidence level (`community-opinion`, `taste-preference`, `inferred`, `high-confidence`). When rules in this file conflict with the research doc, the research doc wins.

---

## How the research becomes skills

```
Reference site screenshots + HTML/CSS source
                ↓
Design_System_Analysis (evidence extraction)
                ↓
Community_Conventions (taste layer)
                ↓
SKILL.md files (instructional, AI-facing)
                ↓
Benchmark testing against reference screenshots
                ↓
Refined skill files
```

The research docs are human-readable synthesis. Skill files are written for AI consumption — short, instructional, phrased as rules rather than observations.

---

## Confidence tag system

Both research files use a shared tag vocabulary:

| Tag | Meaning |
|-----|---------|
| `observed` | Directly extracted from source code or screenshots |
| `high-confidence` | Consistent finding across 3+ reference systems |
| `inferred` | Reasoning about patterns, not direct extraction |
| `system-specific` | Applies to one reference system only |
| `taste-observation` | One brand's decisions, not cross-validated |
| `community-opinion` | Community consensus, not verified against reference sites |
| `taste-preference` | Author judgment, may not apply universally |
| `pureform-override` | Explicit Pureform policy, may override evidence |

---

## Limitations

- Screenshots capture a single point in time. Sites change.
- Motion, hover states, and focus rings cannot be captured statically.
- Consumer product hierarchy, editorial layouts, and documentation-specific patterns are underrepresented. Do not generalize current evidence to those domains.
- Not all pages from each site were analyzed.
