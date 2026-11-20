---
name: deceptive-pattern-pushback
description: Audits designs, flows, copy or code for deceptive and manipulative patterns (dark patterns), classifies each as Dark, Grey or Mistake, and writes a calm pushback brief with risk and an honest alternative that still meets the business goal. Use when asked to check for dark patterns, review a checkout, cancellation, consent, pricing or retention flow, push back on a stakeholder request, or say no to a manipulative design.
---

# Deceptive Pattern Pushback

Spot deceptive design, then turn "I don't think we should do this" into something a stakeholder can say yes to. The brief wins by meeting the business goal honestly, not by moralising.

## Modes

Pick from the request. Run both when an audit surfaces something that needs a decision.

- **Audit**: sweep a UI, flow, copy deck or codebase and report every finding.
- **Brief**: respond to a specific request or design ("make the cancel button less obvious", "add a countdown") with a one-page pushback brief.

## Inputs

Read `references/tool-routing.md` for sources. Establish market and sector from the routing note, context or one question, since regulatory risk depends on both. For code audits, read copy strings, default values, form state, consent logic and timers, and report file locations. State that static review cannot see runtime behaviour such as server-side timers or A/B variants.

## Step 1: Diagnose

Match against `references/patterns.md`, which includes interface patterns and AI and chatbot patterns. For each finding:

- **Name** the pattern precisely.
- **Classify intent**:
  - **Dark**: benefits the business at the user's expense, by design.
  - **Grey**: persuasive, could tip into harm depending on execution or audience.
  - **Mistake**: unintended harm from poor design (unclear copy, buried information).
- **Apply three tests**:
  - **Newspaper test**: would we be comfortable seeing this described in a news story about us?
  - **Vulnerable customer test**: does it work worse for someone stressed, older, with low literacy or an access need?
  - **Symmetry test**: is leaving, declining or cancelling as easy as joining, accepting or buying?

Also say when something is legitimate persuasion: a genuine limited offer, a sensible default, one honest retention offer. Overcalling destroys credibility.

## Step 2: Assess risk

Cover only the kinds that genuinely apply, most material first:

1. **User harm**: who is hurt and how.
2. **Regulatory**: use `references/regulation-uk-eu.md` for the relevant regimes. Check the current status of any provision before citing it; several are being phased in. This is not legal advice; recommend legal or compliance review where risk is real.
3. **Commercial**: complaints, refunds, chargebacks, churn after a manipulated conversion, ombudsman cases, app store policy.
4. **Trust and brand**: press, social, regulator attention.

## Step 3: Find the honest alternative

Identify the business goal behind the request (retention, opt-in rate, revenue, conversion). Propose one or two alternatives that pursue it honestly, each with a metric and a comparison so the alternative can win on the business's own terms.

## Output

- **Audit**: use `templates/audit-report.md`. Findings table sorted by classification (Dark first) then severity.
- **Brief**: use `templates/pushback-brief.md`. One page, then a three or four sentence version for Slack or a ticket comment.

See `examples/cancel-flow-brief.md` for tone and depth. Offer to post the brief as a ticket comment or the findings as Figma comments, following the routing rules.

## Tone

- Assume good intent. The stakeholder is usually chasing a target.
- Frame as risk to the business and its customers, not as the designer's ethics.
- Name the specific element and the specific fix. Never vague, never preachy.
- Lead with the most material risk; label minor issues as edge cases.
- No em dashes.
