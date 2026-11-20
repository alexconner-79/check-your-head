# Example: pushback brief for a fictional streaming add-on

Input: Slack message from a product owner. "Retention is down 4% this quarter. Can we move cancel into Settings > Account > Manage plan and add two more save screens before the confirm? Need designs by Friday." Market: UK. Sector: telecoms add-on billed through the mobile account.

---

# Pushback brief: Cancel flow for the Streamplus add-on

**Request:** Move the cancel entry point three levels deeper and add two more retention screens before confirmation, to recover a 4% retention drop. Requested by the product owner in #streamplus, due Friday.

**Pattern:** Roach motel with a save-offer loop · **Classification:** Dark

**Where:** Add-on management, cancel journey (currently one retention screen, then confirm)

**Who it affects:** Every customer trying to cancel. Hardest on customers with access needs or limited confidence online, who are more likely to give up or call instead.

**Risk:**
- **Regulatory:** making exit harder than sign-up is a known target of UK consumer law under the DMCC Act, and subscription-specific cancellation rules are being introduced (check current status). Ofcom also scrutinises contract exit in telecoms.
- **Commercial:** customers who can't cancel online call instead (cost per contact), dispute charges, or complain. Retention gained this way tends to reverse at the next bill, with a complaint attached.
- **Trust:** cancellation friction is a common subject of press and social complaints in telecoms.

**The goal behind the request:** Recover retention.

**Alternative:**
1. Keep cancel where it is. Replace the current generic save screen with one offer based on the reason they give: pause for 1 or 3 months, a cheaper tier, or a discount if price is the reason.
2. Add an exit reason picker (one tap, optional) so we learn why retention dropped, rather than hiding the symptom.

**How we'd measure it:** Save rate at the offer screen and 90-day retention of saved customers, against the current flow. Guardrail: cancel-related complaints and call volume must not rise.

**Decision needed:** Product owner to agree the alternative by Wednesday so designs land Friday.

*Not legal advice. Recommend a quick check with the regulatory team before release.*

---

**Short version:**

Burying cancel and adding more save screens is the pattern UK regulators are actively targeting, and it usually turns into complaints and calls rather than retention. I'd suggest a pause or downgrade offer matched to the cancel reason, plus a one-tap reason picker so we find out why retention dropped. We can measure it on save rate and 90-day retention against the current flow. Can we agree this by Wednesday to hit Friday?
