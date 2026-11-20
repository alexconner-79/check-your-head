---
name: design-sameness-check
description: Reviews a design, page, mockup, prototype or UI codebase for generic, templated or AI-default patterns and suggests distinctive alternatives grounded in the brand and product. Use when asked to check if something looks generic, AI-generated, templated or "like everyone else", to de-slop a design, or to run a sameness check on Figma frames, screenshots, URLs, Claude Design output or React and Tailwind code.
---

# Design Sameness Check

Find where a design looks like everyone else's and say exactly what to do instead. The aim is distinctive expression, not novelty for its own sake.

## The core distinction

Familiar interaction is good. Generic expression is the problem.

- Do NOT flag conventions that help usability: standard navigation placement, form patterns, recognisable controls, platform conventions, accessible defaults, legally required content.
- DO flag layout, type, colour, imagery, motion and copy choices that exist because they are the default, not because they serve this brand or these users.

## Modes

Pick the mode from what was provided. Run both if both visuals and code are available.

- **Visual review**: screenshots, Figma frames, URLs, Claude Design artifacts.
- **Code scan**: a repo or component files. Search for the code signals listed in `references/tells.md` and report file locations. Code scan finds candidates; confirm each one visually or from context before reporting it, since a token can be legitimate in one place and generic in another.

## Inputs

Read `references/tool-routing.md` for where to get inputs. Also establish, from context or one question: the brand, the product, the audience, and one to three competitors. If none are available, proceed and state the assumption.

## Process

1. **Logo swap test.** If a competitor's logo replaced this one, what would give it away? Name it, or say nothing would.
2. **Scan against the tell list** in `references/tells.md`, area by area: layout, type, colour, imagery and iconography, motion, copy.
3. **Check the category.** If Mobbin or browsing is available, check whether a pattern is common in this specific category. A pattern that is everywhere in fintech is more damaging to a fintech than a rare one.
4. **Find what is already distinctive** and list it under Protect. Always include this section, even if short.
5. **Propose alternatives** drawn from `references/distinctiveness-sources.md`: the product's own truth, real content and data, domain material, brand assets, typographic voice. Never swap one trend for another.

## Output

Use `templates/report.md`. In summary:

1. **Verdict**: two sentences. How generic it reads overall, and the single biggest fix.
2. **Area ratings**: Layout, Type, Colour, Imagery, Motion, Copy, each rated Distinct, Mixed or Generic with a one-line reason. Use ratings, not a numeric score; a score implies precision this judgement doesn't have.
3. **Findings table**: area, what's generic, why it matters here, specific alternative, severity (Generic, Borderline, or Edge case). For code scan, add file and line.
4. **Protect**: what is distinctive and must survive revision.
5. **Next step**: offer to post findings as Figma comments or tickets, following the routing rules.

See `examples/fintech-landing.md` for the expected depth and specificity.

## Rules

- Be specific. "The hero is generic" is useless. "The hero uses the eyebrow, H1 and two-button pattern; lead with the actual approval screen and a headline about the 48-hour wait it removes" is useful.
- Alternatives must come from this product. If an alternative would fit any competitor equally well, it is not an alternative.
- Do not pad. If three things are generic, report three.
- Eyebrow text above headings is always a finding.
- Lead with the most significant finding. Label minor ones as edge cases.
- No em dashes in the output.
