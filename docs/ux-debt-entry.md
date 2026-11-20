# ux-debt-entry

Logs UX debt the moment it's spotted or accepted: one item, or a whole batch of review comments or audit findings in one go.

## When to use it

- You shipped a known compromise to hit a date
- A review or audit produced a list of issues
- Figma comments need turning into trackable work
- Components have drifted from the design system

## How to ask

- "Add this to UX debt: error messages on upload don't say how to fix the problem"
- "Triage these Figma comments into the debt register"
- "Raise these audit findings as Jira tickets"

## What you get

One row (or ticket) per item, with:

- **Item**, described by its user impact rather than the visual symptom
- **Severity**: High, Medium or Low, with accessibility failures and regulatory exposure High by default
- **Cause**: deadline, technical constraint, stakeholder decision, missing research, inherited, or drift. Factual, never blame.
- **Proposed fix** and **effort** (S, M or L, labelled as an estimate)
- **Interest**: the cost of leaving it unfixed. This is what gets debt prioritised.

Batches are de-duplicated, sorted by severity, and exported as CSV when there are more than five items.

See the worked example: [invoicing portal batch](../skills/ux-debt-entry/examples/invoicing-portal-batch.md). Severity rules, WCAG mapping and Jira and Linear priority mapping are in [`references/severity-and-causes.md`](../skills/ux-debt-entry/references/severity-and-causes.md).

## Tools

| Reads from | Writes to |
|---|---|
| Figma comments, screenshots, audit notes, tickets | Jira or Linear: one issue per item, titled `UX debt: ...`, labelled `ux-debt`, severity mapped to priority. Sheets or Notion: appended rows. Repo: `docs/ux-debt.md`. Otherwise ready to paste or CSV. |

It checks for existing entries before adding, matches your tracker's columns and labels, and asks before creating tickets.
