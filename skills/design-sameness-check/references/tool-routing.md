# Tool routing

Every Check Your Head skill uses this file to decide where to read from and where to write to. The skill works with nothing connected; tools only make it faster.

## 1. Find the routing note

Before reading widely or writing anywhere, look for a routing note, in this order:

1. `check-your-head.md` at the root of the current repo (Claude Code, or a connected folder)
2. A "Check Your Head" section in `CLAUDE.md`
3. The claude.ai Project instructions, or a Project doc named "Check Your Head"

The note lists where decisions, debt, metrics and write-ups live, plus market and sector. If there is no note, infer the destination from what the user said or attached. If that fails, return paste-ready output and mention once that a routing note would save the step next time.

## 2. Reading inputs

Use what the user pasted or attached first. Then use connected tools, checking which ones actually exist in this session before assuming:

| Source | How to read | Use for |
|---|---|---|
| Figma (Figma MCP or figma-console) | Screenshot or design context for a frame; comments for feedback | Screens, flows, components, review comments |
| Claude Design or artifacts | Read the artifact | Designs and prototypes made in Claude |
| Repo (Claude Code or device shell) | Read files; search components, copy strings, CSS and tokens | Code-level checks, existing records |
| Jira, Linear, Asana | Read the issue or epic | Requirements, acceptance criteria, existing debt |
| Notion, Confluence, Google Docs | Read the page | Briefs, existing logs, research |
| Slack or Teams | Read the thread | Stakeholder requests, decisions made in chat |
| Mobbin | Search screens or flows | Competitor and category patterns |
| Analytics (if connected) | Query the metric | Baselines and outcomes |

If nothing usable is available, ask once for a paste, screenshot or link, then proceed with what arrives.

## 3. Writing outputs

| Record | Repo | Notion or Confluence | Jira or Linear | Sheet | Nothing connected |
|---|---|---|---|---|---|
| Decision record | `docs/design-decisions/NNNN-short-title.md`, one file per decision, next number in sequence | Append to the decisions page, newest at the top | Comment on the relevant epic, linking the full record | Append a row | Paste-ready markdown |
| UX debt | `docs/ux-debt.md`, one table row per item | Append to the register page | One issue per item: title starts `UX debt:`, label `ux-debt`, severity mapped to priority | Append a row | Paste-ready table, or CSV for batches |
| Metrics plan | `docs/metrics/<feature>.md` | New page under the metrics parent | Instrumentation tasks as issues, if asked | One row per metric | Paste-ready table |
| Pushback brief | Not stored by default | Page, if asked | Comment on the ticket, if asked | n/a | Paste-ready brief plus Slack-length version |
| Impact write-up | `docs/case-studies/<project>.md` | New page under write-ups | n/a | n/a | A Docs artifact in claude.ai, otherwise markdown |
| Sameness report | Not stored by default | Page, if asked | Findings as issues, if asked | n/a | Inline report |

Figma: never edit frames. Post comments or annotations only when the user asks, pinned to the relevant node.

## 4. Write rules

- **Confirm before writing to shared tools.** Creating tickets, posting comments and editing team pages are visible to other people. Show exactly what will be created, then create it once the user agrees. Skip the confirmation only if the routing note says `confirm-before-writing: no`.
- **Append, never overwrite.** Existing records are history. Supersede, don't edit.
- **Match the destination.** Use the existing page's or register's columns, ID format, labels and tone rather than this pack's defaults.
- **Link both ways** where possible: debt to the decision that created it, write-ups to the decisions they cite, tickets to Figma frames.
- **If a connector fails**, retry once, then give paste-ready output in the destination's format and say which write didn't happen.

## 5. Surface notes

- **Claude Code**: prefer repo files as the system of record; records live next to the code and get reviewed in pull requests. Code-level checks (sameness, dark patterns) can search the codebase directly.
- **claude.ai and Claude Design**: rely on connectors. With none, deliver as an artifact (Docs for write-ups, Sheets for registers) so the user can keep and export it.
- **Figma**: a source of truth for screens, not for records. Read from it; write back only comments.
