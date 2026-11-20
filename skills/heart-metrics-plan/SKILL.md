---
name: heart-metrics-plan
description: Creates a HEART metrics plan (Happiness, Engagement, Adoption, Retention, Task success) for a feature or design change, with baselines, targets, guardrails, proxies, data owners and instrumentation asks. Use when asked for success metrics, KPIs, how to measure a design, a measurement plan, or what to baseline before launch.
---

# HEART Metrics Plan

Define how a feature or design change will be measured. Works at any point, but is most valuable before release, because that is the only time a baseline can be captured.

## Inputs

Whatever is to hand: a brief, ticket, Figma link, screenshot, PRD or a one-line description. Read `references/tool-routing.md` for sources. If analytics are connected, pull current values as baselines. Infer the goal from context; ask only if it genuinely can't be inferred.

## Process

1. **State the change and its goal** in one sentence each. If the goal is vague ("improve onboarding"), sharpen it into a user outcome ("more new customers finish setup without calling us").
2. **Pick the dimensions that matter.** Two or three is normal; all five is usually padding. Use `references/heart-guide.md` for signals and metrics per dimension.
3. **Work Goal, Signal, Metric** for each dimension. A signal is the observable behaviour; a metric is how it's counted.
4. **Set baselines.** Use real values where available. Where not, say so plainly and give the fastest way to get one.
5. **Add a guardrail** for each primary metric: the thing that must not get worse (complaints, errors, calls, opt-outs, accessibility defects).
6. **Name a failure signal**: which metric would show the change made things worse.
7. **List instrumentation asks**: the events or data engineering needs to add, so they can be ticketed.

## Output

Use `templates/metrics-plan.md`:

1. Change and goal
2. Metrics table: dimension, goal, signal, metric, baseline, target, guardrail, source, owner
3. Baseline actions: what to capture before release, by whom
4. Failure signal
5. Instrumentation asks
6. Review point: when to read the results (e.g. 2 and 6 weeks after release)

See `examples/bank-onboarding.md` for depth. Offer to save the plan or raise instrumentation asks as tickets, following the routing rules.

## Rules

- Where there are no product analytics, use proxies from `references/heart-guide.md` and label them as proxies.
- Every metric needs a named source and owner. A metric nobody owns never gets pulled.
- Targets are suggestions unless the user supplies them. Label them "suggested".
- Don't promise statistical significance the traffic can't deliver. If volumes are low, say so and favour larger effects, longer windows or qualitative checks.
- Lead with the most important metric. Label edge cases as edge cases.
- Deliver the table as something keepable (file, doc, Sheet or paste-ready), not a wide table squeezed into chat.
- No em dashes.
