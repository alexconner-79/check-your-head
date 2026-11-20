# Severity, cause and effort

## Severity

| Severity | Definition | Examples | Jira priority | Linear priority |
|---|---|---|---|---|
| High | Blocks or misleads users, fails accessibility, or creates regulatory or financial exposure | WCAG A or AA failure on a core journey; misleading price display; error that loses user input; consent defaults that are non-compliant | High | High (2) |
| Medium | Causes friction, errors or inconsistency on a core journey; or High-type issues on a rare path | Inconsistent error patterns; unclear labels; extra steps; components drifting from the design system | Medium | Medium (3) |
| Low | Polish, consistency or minor friction on low-traffic paths | Spacing off-token; icon mismatch; copy tone inconsistency | Low | Low (4) |

Bump one level if the journey is high-traffic or used by vulnerable customers. Drop one level for internal-only tools with trained users, unless it's an accessibility failure.

## Accessibility mapping

- WCAG Level A failure: High
- WCAG Level AA failure: High on core journeys, Medium elsewhere
- AAA or best practice only: Low, labelled "best practice"

Always cite the WCAG success criterion number.

## Cause

| Cause | Use when |
|---|---|
| Deadline | Shipped knowingly to hit a date |
| Technical constraint | Platform, API or legacy limitation |
| Stakeholder decision | Design recommendation overridden (link the decision record) |
| Missing research | Built on assumption, now shown wrong |
| Inherited | Predates the current team or product |
| Drift | Diverged from the design system over time |

## Effort

| Size | Rough meaning |
|---|---|
| S | Copy, token or config change; under a day |
| M | Component or single-screen change; a few days |
| L | Flow, API or cross-team change; a sprint or more |

Always label effort as an estimate.

## Interest

The cost of leaving it, in one line. Examples: "Drives an estimated 40 contacts a month (ops estimate)", "Every new feature copies the wrong pattern", "Blocks AA conformance statement". If unknown, say "not quantified" rather than guessing.
