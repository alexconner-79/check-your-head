# heart-metrics-plan

Defines how a feature or design change will be measured, using Google's HEART framework: Happiness, Engagement, Adoption, Retention and Task success.

## When to use it

- Before release, while you can still capture a baseline
- When someone asks "how will we know this worked?"
- When there's no analytics and you need credible proxies
- When engineering needs to know which events to add

## How to ask

- "What should we measure for the new onboarding flow?"
- "Write a HEART plan for this redesign" (with a brief, ticket or Figma link)
- "We don't have analytics. How do we measure this?"

## What you get

1. The change and its goal, one sentence each
2. A metrics table covering only the dimensions that matter (usually two or three): goal, signal, metric, baseline, target, guardrail, source, owner
3. Baseline actions: what to capture before release, and who does it
4. A failure signal: which metric would show the change made things worse
5. Instrumentation asks for engineering
6. Review points: when to read the results

Targets are labelled "suggested" unless you supply them. Proxies are labelled as proxies.

See the worked example: [bank onboarding](../skills/heart-metrics-plan/examples/bank-onboarding.md).

## Without analytics

The [HEART guide](../skills/heart-metrics-plan/references/heart-guide.md) lists proxies: contact and complaint volume, usability benchmarks, form errors from server logs, backend funnel counts, accessibility defects, audit findings and design rework. It also covers guardrail metrics, regulated sectors, and what to do when traffic is too low for percentages to mean much.

## Tools

| Reads from | Writes to (if you ask) |
|---|---|
| Briefs, tickets, Figma, PRDs, connected analytics for baselines | A Notion, Confluence or Sheet page; instrumentation asks as Jira or Linear tickets; a repo file |
