# Example: metrics plan for a fictional digital bank onboarding redesign

Input: "We're replacing the 9-step account opening with a single scrolling form plus ID check. Need metrics before we ship next month." Analytics connected; contact centre data available on request.

---

# Metrics plan: Account opening redesign

**Change:** Replace the 9-step account opening wizard with a single page form followed by the ID check.
**Goal:** More applicants finish opening an account in one sitting, without needing to contact us.
**Release:** Sprint 24 · **Owner:** Design lead, onboarding squad

## Metrics

| Dimension | Goal | Signal | Metric | Baseline | Target | Guardrail | Source | Owner |
|---|---|---|---|---|---|---|---|---|
| Task success | Applicants finish in one sitting | Application submitted in the same session it started | Same-session completion rate | 41% (last 8 weeks) | 50% (suggested) | ID check failure rate must not rise above 12% (now 11%) | Product analytics | Squad analyst |
| Task success | Fewer errors | Field validation errors shown | Errors per completed application | 3.2 | Below 2 (suggested) | n/a | Product analytics, new event needed | Squad analyst |
| Happiness | Feels easy | Post-submit ease rating | Single Ease Question, 1 to 7 | Not captured | 5.5 or above (suggested) | n/a | In-product survey | Research lead |
| Task success (proxy) | Fewer people need help | Onboarding contacts | Contacts tagged "account opening" per 1,000 applications | Not captured; request last quarter's count | 20% lower (suggested) | n/a | Contact centre reporting | Ops manager |

## Baseline actions

- [ ] Request last quarter's contact count tagged "account opening" from the ops manager, before release
- [ ] Add the ease question to the current flow now, for two weeks, to get a pre-change score

## Failure signal

Same-session completion flat or down while ID check failures rise: the shorter form is pushing unready applicants into the ID step. Rethink if ID failures exceed 13% for two consecutive weeks.

## Instrumentation asks

- `validation_error` event with field name, fired on each inline error (needed for errors per application)
- `session_id` carried through to submission, to measure same-session completion

## Review points

- 2 weeks after release: check for breakage and ID failure spike
- 6 weeks after release: read all metrics against baseline
