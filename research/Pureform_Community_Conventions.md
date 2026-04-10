---
title: Pureform Community Conventions and Taste Policy
type: policy
status: draft
created: 2026-04-10
updated: 2026-04-10
related_documents: ["Design_System_Analysis_-_Reference_Sites_Research.md"]
tags: [pureform, policy, taste, community-conventions]
---

# Pureform Community Conventions and Taste Policy

> **Orientation:** This file contains taste-based rules, community conventions, and style opinions — NOT evidence extracted from reference sites. Apply with judgment. See Section 1 for how to weight these rules relative to the evidence base.

---

## Confidence Tags

| Tag | Meaning | Weight vs Evidence |
|-----|---------|-------------------|
| `community-opinion` | Common community consensus | Low — verify before use |
| `taste-preference` | Author preference, may not apply universally | Low-medium — context matters |
| `inferred` | Reasoning about why something works | Medium — useful but not proven |
| `high-confidence` | Consistent finding across 3+ reference systems | High — but may not transfer to all contexts |
| `pureform-override` | Explicit Pureform policy decision | Override — use when specified |

---

## 1. How to Use This File

This file complements `Design_System_Analysis_-_Reference_Sites_Research.md`. When rules conflict:

1. **Evidence from research doc wins** — it is directly extracted from production systems
2. **This file provides guidance** where the research doc has no coverage (emerging patterns, taste decisions)
3. **Tag weight indicates reliability** — `high-confidence` here is still lower confidence than `observed` in research doc

**Inter font note:** Section 5 lists Inter as `community-opinion` (banned by some). However, Section 1.1 of this file notes that Vercel, Clerk, and shadcn/ui all use Inter — making it `high-confidence` that Inter is production-valid. The "ban" is a differentiation opinion, not an evidence-based finding.

---

## 2. Typography Conventions

### 2.1 Font Selection

| Rule | Confidence | Notes |
|------|------------|-------|
| Inter is widely used in production (Vercel, Clerk, shadcn/ui) | `high-confidence` | Direct observation across 3 systems |
| Some communities consider Inter "overused" | `community-opinion` | Differentiation preference |
| Geist, Outfit, Satoshi are alternatives with similar metrics | `community-opinion` | Not validated across sites |

**Guidance:** Font choice should be brand-appropriate. Inter is not inherently wrong. The issue is differentiation, not prohibition.

### 2.2 Font Weight Rules

| Rule | Confidence | Notes |
|------|------------|-------|
| Never use more than two font weights in a single component | `high-confidence` | Observed in Linear, Stripe, Vercel |
| Never use three weights (700, 600, 400) in same card | `high-confidence` | Directly observed |
| Never use weight 500 as "semi-important" middle ground | `taste-preference` | Opinion; Vercel uses 500 without issue |

**Note:** "Two weights max" and "three weights banned" are the same rule. The first is the positive statement, the second is the negative corollary.

### 2.3 Typography Scale Conventions

| Rule | Confidence | Notes |
|------|------------|-------|
| Headlines: `text-4xl md:text-6xl tracking-tighter` | `inferred` | Common pattern, not site-specific |
| Body: `text-base leading-relaxed max-w-[65ch]` | `inferred` | Readability convention |
| Never use Serif on dashboards | `taste-preference` | Liveblocks/Linear do follow this |

---

## 3. Color Conventions

### 3.1 Accent Rules

| Rule | Confidence | Notes |
|------|------------|-------|
| Max 1 accent color per interface | `high-confidence` | Linear, Clerk, Vercel all follow this |
| Saturation < 80% for large accent areas | `inferred` | Reasoning from observation |
| Never use AI purple/blue gradients | `community-opinion` | Trend reaction |
| Pure black (#000) on pure white is harsh | `taste-preference` | Use #0a0a0a or gray-900 |

### 3.2 Gradient Rules

| Rule | Confidence | Source |
|------|------------|--------|
| Never use gradient text on headers | `high-confidence` | Not observed in any reference site |
| Never use gradient on buttons | `high-confidence` | Linear's never-list |
| Never use gradient on inputs | `high-confidence` | Linear's never-list |
| Gradients only on large decorative areas | `high-confidence` | Stripe hero, not functional elements |

---

## 4. Layout Conventions

### 4.1 Layout Principles

| Rule | Confidence | Notes |
|------|------------|-------|
| When visual complexity is high, prefer asymmetric layouts | `inferred` | Vercel uses centered + scaffold; Linear uses left-aligned |
| Never use 3-column equal card rows | `taste-preference` | Community convention; not verified |
| Use `border-t`, `divide-y`, or spacing instead of card borders | `inferred` | shadcn/ui, Vercel minimize borders |
| Bento grid is a valid pattern | `community-opinion` | Popularized by precedence |

### 4.2 Card Rules

**"3-column equal card rows" defined:** Three cards of identical width, height, and styling in a single row. This creates visual monotony. If using three cards, vary the widths or add visual differentiation.

**"Oversized H1s" defined:** H1 that exceeds 72px on desktop and is not part of a display/hero context. Body text headlines should stay within the type scale.

**"Default shadcn/ui without customization" defined:** Using shadcn/ui components with their default Tailwind classes unchanged — same colors, same shadows, same radius. Customization means overriding at least one token (color, shadow, radius, or spacing).

---

## 5. Forbidden Patterns (Community Consensus)

| Category | Banned | Confidence | Notes |
|----------|--------|------------|-------|
| Visual | Neon glows | `community-opinion` | Not seen in reference sites |
| Visual | Pure black (#000) | `taste-preference` | Use #0a0a0a or gray-900 |
| Visual | Oversaturated accents | `inferred` | Reference sites all restrained |
| Visual | Gradient text on headers | `high-confidence` | Not observed in any site |
| Typography | Inter font | `community-opinion` | See Section 2.1 — production systems use it |
| Typography | Oversized H1s | `taste-preference` | See Section 4.2 for definition |
| Layout | 3-column equal cards | `taste-preference` | See Section 4.2 for definition |
| Components | Default shadcn/ui | `taste-preference` | See Section 4.2 for definition |

**Forward reference:** For Inter specifically, see Section 2.1's complete treatment before applying the "ban."

---

## 6. Motion Conventions

### 6.1 Animation Rules

| Rule | Confidence | Source |
|------|------------|--------|
| Animate state changes | `high-confidence` | All reference sites do this |
| Never animate layout shifts | `high-confidence` | Causes jank, all sites avoid |
| 150ms max for hover states | `high-confidence` | Clerk's rule |
| Subtle opacity fades only | `inferred` | Clerk, Vercel follow this |

### 6.2 Creative Motion — Decision Required

The following patterns appear in design trend discussions but have not been validated against reference sites:

| Pattern | Confidence | Status |
|---------|------------|--------|
| Liquid glass (backdrop-blur + borders) | `community-opinion` | May be useful, unverified |
| Magnetic buttons (cursor attraction) | `community-opinion` | Trend, not evidence |
| Perpetual motion (Pulse, Float) | `community-opinion` | INTENSITY-based, unverified |

**Recommendation:** These should be tracked separately when a `design-trends.md` file is created, not treated as default generation rules. They may be appropriate for high-variance projects.

---

## 7. Changelog

| Date | Version | Change |
|------|---------|--------|
| 2026-04-10 | v1 | Initial creation — taste rules separated from research doc |
| 2026-04-10 | v2 | Unified tag system to match research doc (`inferred` not `inferred-rule`), fixed forward references, updated creative motion recommendation |

---

## 8. Relation to Research Document

**This file is subordinate to** `Design_System_Analysis_-_Reference_Sites_Research.md`.

When generating:
1. Use the research doc for token values, spacing scales, color tokens
2. Use this file for taste guidance where research doc has no coverage
3. When they conflict, prefer the evidence from the research doc
4. Items here are `taste-preference` or `community-opinion` unless explicitly tagged `high-confidence`
