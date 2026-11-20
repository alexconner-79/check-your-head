# deceptive-pattern-pushback

Spots deceptive and manipulative design, then helps you say no in a way a stakeholder can agree to: by meeting the same business goal honestly.

## When to use it

- Reviewing consent, cookie, pricing, checkout, subscription, cancellation or retention flows
- Someone asks for a countdown timer, a pre-ticked box or a harder-to-find cancel button
- Checking AI-generated UI. In one study, more than half of 1,296 LLM-generated ecommerce components contained at least one deceptive pattern ([Chen et al.](https://arxiv.org/abs/2502.13499))
- Reviewing a chatbot or assistant experience

## How to ask

- "Audit this checkout for dark patterns"
- "Product want two more save screens in the cancel flow. Help me push back."
- "Is this consent banner OK for the UK?"
- "Scan the signup code for deceptive defaults" (in Claude Code)

## Two modes

**Audit** sweeps a design, flow, copy deck or codebase and reports every finding. Each one is classed:

- **Dark**: benefits the business at the user's expense, by design
- **Grey**: persuasive; could tip into harm depending on execution or audience
- **Mistake**: unintended harm from unclear design

and run through three tests: the newspaper test, the vulnerable customer test, and the symmetry test (is leaving as easy as joining?). It also says when something is legitimate persuasion, so you don't overcall.

**Brief** turns a specific request into a one-page pushback brief: the request, the named pattern, who it affects, the risk (user, regulatory, commercial, trust), the goal behind the request, an honest alternative, how to measure it, and the decision needed. Plus a three or four sentence version for Slack.

See the worked example: [cancel flow brief](../skills/deceptive-pattern-pushback/examples/cancel-flow-brief.md).

## Coverage

The [pattern catalogue](../skills/deceptive-pattern-pushback/references/patterns.md) covers consent, pricing, subscriptions, pressure tactics, interface interference, and AI and chatbot patterns.

The [regulation reference](../skills/deceptive-pattern-pushback/references/regulation-uk-eu.md) covers UK and EU regimes including the DMCC Act, FCA Consumer Duty, UK GDPR and PECR, Ofcom rules, the Digital Services Act and the AI Act.

**This is not legal advice.** Several provisions are being phased in, so the skill checks current status before citing anything and recommends legal or compliance review where the risk is real.

## Tools

| Reads from | Writes to (if you ask) |
|---|---|
| Screens, Figma, flows, copy decks, repo code, Slack threads, tickets | Ticket comments, Figma comments, a Notion or Confluence page |

## Make it yours

Add patterns to `references/patterns.md`. Add your market or sector rules (for example, a regulator outside the UK and EU) to `references/regulation-uk-eu.md` or a new reference file.
