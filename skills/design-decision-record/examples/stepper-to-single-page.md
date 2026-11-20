# Example: decision record from a Slack thread

Input (pasted thread, summarised): Design proposed replacing the 4-step stepper in the payee setup flow with a single page. Engineering preferred to keep the stepper because validation is per step in the API. Usability test last week: 3 of 6 participants used Back to check details on earlier steps; 2 entered the sort code in the wrong step. Product lead agreed single page, with engineering adding a combined validation endpoint. Accessibility lead asked that errors summarise at the top.

---

# 0014. Payee setup uses a single page instead of a 4-step stepper

**Date:** 2026-11-12 · **Status:** Accepted
**Project:** Ledgerly business app · **Area:** Payee setup
**Links:** Figma "Payee setup v3", usability round 4 findings, ticket LEDG-212

## Decision

Replace the 4-step payee setup stepper with a single page form.

## Context

Usability round 4 showed people going back to check earlier steps and entering details in the wrong step. The stepper exists because the API validates per step.

## Options considered

1. **Single page form**: all fields visible, one submit, combined validation.
2. **Keep the stepper, add a review step**: rejected; adds a fifth step and doesn't fix wrong-step entry.
3. **Keep the stepper as is**: rejected; usability evidence shows it causes errors.

## Rationale

Payee setup has 7 fields, few enough for one page. Seeing everything at once removes the back-and-forth checking and the wrong-step entries.

## Evidence

Usability round 4: 3 of 6 participants used Back to check details; 2 of 6 entered the sort code in the wrong step.

## Trade-off accepted

Engineering builds a combined validation endpoint, adding about one sprint.

## Agreed by

Product lead, engineering lead, design. Accessibility lead added the condition that errors are summarised at the top of the form.

## Revisit if

Payee setup fields grow beyond about 12, or same-session completion drops below the stepper baseline.
