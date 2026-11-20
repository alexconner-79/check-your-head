# design-decision-record

Captures a single design decision while it's fresh, in a form someone who wasn't there can follow six months later.

## When to use it

- A decision was just made in a meeting, Slack thread or Figma comment
- A stakeholder overrode a design recommendation
- You traded user experience against a deadline, cost, constraint or compliance
- A decision sets a pattern other teams will copy

## How to ask

- "Log this decision" (with a pasted thread, notes or a sentence)
- "Record that we're dropping the stepper for a single page"
- "Turn this meeting summary into decision records" (one record per decision)

## What you get

A short record (aiming for under 250 words): decision, context, options considered, rationale, evidence, the trade-off accepted, who agreed, and an observable trigger for revisiting it. Status is Proposed, Accepted, Superseded or Reversed.

It records what happened, not a cleaned-up version. If design was overruled, it says so factually and without blame. Accepted records are never edited; a later decision supersedes them, and both are linked.

See the worked example: [stepper to single page](../skills/design-decision-record/examples/stepper-to-single-page.md). For what's worth recording, see [`references/what-to-record.md`](../skills/design-decision-record/references/what-to-record.md).

## Tools

| Reads from | Writes to |
|---|---|
| Slack threads, meeting notes, Figma comments, tickets | Repo: `docs/design-decisions/NNNN-title.md`, numbered in sequence. Notion or Confluence: appended to your decisions page. Jira or Linear: a comment on the epic linking the record. Otherwise ready to paste. |

## Why records matter

Decision records are the raw material for [design-impact-write-up](design-impact-write-up.md). Three months of records turn a vague "I led the redesign" into specific decisions, trade-offs and evidence.
