# HEART guide

HEART was developed at Google as a framework for user-centred metrics. Work each dimension as Goal, then Signal, then Metric.

## Dimensions

| Dimension | Asks | Typical signals | Typical metrics |
|---|---|---|---|
| Happiness | How do users feel about it? | Survey responses, ratings, sentiment in feedback | CSAT, ease score (SEQ), NPS (use with care), sentiment of support contacts |
| Engagement | How much and how often do they use it? | Sessions, actions per visit, feature use | Frequency per user per week, depth of use, return visits to the feature |
| Adoption | Are new users taking it up? | First use of a feature or product | % of eligible users who use it within N days, time to first use |
| Retention | Do they keep using it or stay customers? | Repeat use, renewals, churn | N-day retention, churn rate, renewal rate |
| Task success | Can they do what they came to do? | Completions, errors, time, abandonment | Completion rate, time on task, error rate, drop-off by step |

Task success is usually the most defensible for design work, because the link between design and outcome is shortest.

## Choosing dimensions

- **New feature**: Adoption and Task success, with Happiness as a check.
- **Redesign of an existing flow**: Task success first, with a guardrail on Retention or contact volume.
- **Content or copy change**: Task success (comprehension, errors) and contact volume.
- **Retention or engagement initiative**: Retention, with Happiness as a guardrail against manipulation.
- **Design system work**: not really HEART territory. Use adoption by teams, defects, delivery speed and consistency instead, and say so.

## Proxies when there are no product analytics

Label all of these as proxies in the output.

- Contact centre volume and contact reasons for the journey
- Complaint volume and themes
- Support ticket tags
- Usability benchmark: task success and time on task with 5 to 8 participants, before and after
- Form error rates from server logs
- Drop-off from backend funnel data (applications started vs submitted)
- Accessibility defects found in audit
- Compliance or audit findings
- Design and build rework (handoff questions, defects raised against design)
- App store review themes

## Guardrails

A guardrail stops a win on one metric hiding damage elsewhere. Common ones:

- Complaints or contacts about the journey
- Error rates
- Opt-out or unsubscribe rates
- Refunds, chargebacks or cancellations within 30 days
- Accessibility defects
- Time on task (when completion goes up because people are forced through)

## Regulated contexts

In financial services, telecoms and energy, add a consumer outcome check: does the change help customers understand and act in their interest? Under the FCA Consumer Duty, firms are expected to monitor outcomes, so consumer understanding and support metrics are often already collected. Ask for them.

## Low traffic

If a journey has low volume, a percentage change can be noise. Options: lengthen the measurement window, look for larger effects only, use qualitative benchmarks, or combine several related signals. Say which in the plan.

## Baseline fast paths

- Analytics pull of the last 4 to 12 weeks
- Last quarter's contact and complaint counts for the journey
- A quick unmoderated usability benchmark on the current version
- Backend counts from engineering (started, submitted, failed)
