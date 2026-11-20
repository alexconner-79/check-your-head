---
name: design-decision-record
description: Writes a design decision record for a single decision, covering context, options considered, rationale, evidence, trade-off, who agreed and when to revisit, and files it where the team keeps decisions. Use when asked to log, record, capture or document a design decision, or when a Slack thread, meeting note or Figma comment contains a decision worth keeping.
---

# Design Decision Record

Capture one design decision, now, in a form that will still make sense in six months to someone who wasn't there. One decision per run. Several decisions in one input means several records.

## Inputs

Whatever the user gives: a sentence, a Slack thread, meeting notes, a Figma comment, a ticket, before and after screens. Read `references/tool-routing.md` for sources. Extract the decision. Ask at most one question, only for something that can't be inferred (usually who agreed, or what was rejected).

## Process

1. **Check it's worth recording** against `references/what-to-record.md`. If it isn't, say so in a line and offer to record it anyway.
2. **Extract** the decision, context, options, rationale and evidence from the input. Don't invent options that weren't considered; if only one option was discussed, say so.
3. **Find the trade-off.** Every real decision gives something up. If none is stated, infer the obvious one and mark it "(inferred)".
4. **Set the status**: Proposed, Accepted, Superseded or Reversed.
5. **Check for an earlier record** on the same subject in the destination. If this changes it, mark the new one as superseding the old one and link both.
6. **File it** following the routing rules. In a repo, use `docs/design-decisions/NNNN-short-title.md` with the next number in sequence.

## Output

Use `templates/decision-record.md`. See `examples/stepper-to-single-page.md` for depth.

## Rules

- Record what happened, not a cleaned-up version. If a stakeholder overrode the design recommendation, record it factually and without blame: "Design recommended X; [role] decided Y because Z."
- Use roles and names as the team does; don't add names that weren't in the input.
- Keep it short. A record nobody reads is worthless. Aim for under 250 words.
- Never edit an accepted record's substance. Supersede it.
- No em dashes.
