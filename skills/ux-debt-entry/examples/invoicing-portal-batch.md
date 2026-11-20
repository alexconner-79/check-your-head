# Example: triaging review comments into debt

Input: six Figma comments from a fictional invoicing portal review.
1. "Error on upload just says 'Something went wrong'"
2. "Error on upload doesn't help, users just try again"
3. "Table headers aren't buttons, can't sort with keyboard"
4. "Date format is DD/MM on dashboard, MM/DD on statements"
5. "This card padding is 20, should be 24"
6. "Download CSV button is hidden in an overflow menu, ops say people call to ask for exports"

---

Merged comments 1 and 2 (same issue). Five items, sorted by severity.

| ID | Item (user impact) | Where | Severity | Cause | Proposed fix | Effort | Interest | Owner | Status | Links |
|---|---|---|---|---|---|---|---|---|---|---|
| UXD-31 | Keyboard users can't sort statement tables, so they can't find transactions efficiently | Statements table | High | Inherited | Make headers buttons with `aria-sort`; visible focus state | M (estimate) | Fails WCAG 2.1.1 Keyboard on a core journey | | Open | WCAG 2.1.1 |
| UXD-32 | Upload errors don't say what went wrong or how to fix it, so users retry blindly | Document upload | High | Deadline | Specific messages for size, type and network failures, each with the fix | S (estimate) | Repeated failed uploads; likely contact driver (not quantified) | | Open | |
| UXD-33 | People can't find CSV export and call ops to request it | Transactions, overflow menu | Medium | Stakeholder decision | Promote "Download CSV" to a visible secondary button | S (estimate) | Ops report calls for exports (volume not quantified) | | Open | |
| UXD-34 | Dates show in two formats, risking misread payment dates | Dashboard vs Statements | Medium | Drift | Use DD MMM YYYY everywhere via a shared formatter | S (estimate) | Misread dates on financial records | | Open | |
| UXD-35 | Card padding is off-token | Dashboard cards | Low | Drift | Use spacing token 24 | S (estimate) | Inconsistency spreads if copied | | Open | |

Want me to raise these as five Jira issues with the `ux-debt` label?
