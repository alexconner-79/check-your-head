---
name: ux-debt-entry
description: Logs UX debt (known compromises, inconsistencies, accessibility gaps or design defects) with user impact, severity, cause, proposed fix and effort, and files it in the team's register or tracker such as Jira, Linear, a Sheet or a repo file. Use when asked to add, log or record UX debt, raise design debt tickets, or triage audit findings, review comments or a list of issues into a debt register.
---

# UX Debt Entry

Record a known UX compromise the moment it's spotted or accepted. Handles one item, or a batch (audit findings, Figma comments, a list) in one pass.

## Inputs

A description, screenshot, Figma link or comments, audit notes, ticket or list. Read `references/tool-routing.md` for sources. Infer details; ask only if severity or location genuinely can't be judged.

## Process

1. **Split** the input into distinct items. Merge duplicates and say which were merged.
2. **Describe each item** by its user impact, not its visual symptom. "Error messages on the payee form don't say how to fix the problem, so users retry blindly" beats "error states inconsistent".
3. **Rate severity** using `references/severity-and-causes.md`. Accessibility failures and regulatory exposure are High by default.
4. **Record the cause** factually: deadline, technical constraint, stakeholder decision, missing research, or inherited.
5. **Propose a fix** and size effort (S, M, L, labelled as an estimate).
6. **Estimate the interest**: what it costs to leave it (contacts, errors, rework, risk). One line. This is what gets debt prioritised.
7. **Check the destination** for existing entries on the same issue before adding. Update or link rather than duplicate.
8. **File it** following the routing rules. For Jira or Linear, one issue per item, title starting `UX debt:`, label `ux-debt`, severity mapped to priority as in the reference. Confirm before creating tickets.

## Output

One row per item using `templates/debt-row.md`, sorted by severity. For batches over five items, also produce a CSV using `templates/debt-register.csv` so it can be imported. See `examples/invoicing-portal-batch.md`.

## Rules

- User impact first, always.
- Cause is factual and blame-free.
- Link debt to the decision record that created it where one exists.
- Match the destination's existing columns, IDs and labels over these defaults.
- No em dashes.
