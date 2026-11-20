# Example: impact write-up from mixed evidence

Input: decision record 0014 (single page payee setup), usability round 4 and round 5 notes, analytics showing payee setup completion 68% before, 79% six weeks after. A pricing page change also shipped that month but doesn't touch payee setup. Ops say payee queries "feel lower" but have no numbers.

---

# Payee setup redesign: impact write-up

**Period:** Sep to Nov 2026 · **Team:** 1 designer, 3 engineers, product lead · **My role:** Lead designer; ran usability rounds 4 and 5

## Problem

Corporate customers set up payees through a 4-step wizard. A third of attempts didn't finish, and in testing people went back to check earlier steps or put details in the wrong one. Failed payee setup blocks payments, the core job of the dashboard.

## What I did

Ran usability round 4, which surfaced the wrong-step errors. Proposed and designed a single page form, negotiated the combined validation endpoint with engineering, and ran round 5 to validate it.

## Key decisions

1. **Single page instead of the stepper**: cost engineering about a sprint to build combined validation.
2. **Error summary at the top of the form**: added at the accessibility lead's request; more vertical space, but screen reader users get every error in one place.

## Outcome

- Payee setup completion rose from 68% to 79% in the six weeks after launch (measured, before and after). No other change shipped to this journey in that period.
- Usability round 5: 6 of 6 participants completed payee setup without going back, against 3 of 6 in round 4 (measured, small sample).
- Ops report fewer payee queries (qualitative; not yet quantified).
- **Didn't move:** time to complete stayed roughly flat; the single page is faster to navigate but people read it more carefully.

## What it made possible

The combined validation endpoint is now reusable, and the beneficiary edit flow is being rebuilt on the same pattern.

## Portfolio summary

Corporate customers were failing to set up payees in a 4-step wizard, blocking payments. Testing showed people checking earlier steps and entering details in the wrong step. I led the redesign to a single page form, negotiated a combined validation endpoint with engineering, and added a top-of-form error summary with our accessibility lead. Completion rose from 68% to 79% in the six weeks after launch, and in testing all six participants finished without going back, compared with three of six before. The validation endpoint is now being reused for beneficiary editing.

## Evidence gaps

- Ops contact counts for payee queries, before and after (ask the ops manager for last two quarters)
- Payment volume from newly created payees, if finance can provide it
