<img width="1600" height="560" alt="Check your head. Claude skill pack: 6 tools for ux design" src="https://github.com/user-attachments/assets/b64d76b5-135b-4348-bfee-ce3bcfb5e619" /><br>

**So what'cha want? Evidence, mostly.** 

Six Claude skills for the parts of design work that end in someone asking "and what's that based on?"

Design rarely loses an argument on craft. It loses on receipts. Nobody captured a baseline, nobody wrote down why option B won, the compromise shipped on a Friday was never logged, and the case study says "improved the experience" because the numbers went wherever numbers go. Meanwhile, in one study, more than half of AI-generated ecommerce components shipped with a dark pattern nobody asked for.

These skills fix that at the moment it happens, not in a retro three months later. Paste a Slack thread, get a decision record. Point at a Figma frame, get told whether it looks like 400 other fintechs. Forward a request to bury the cancel button, get a brief that says no politely and still hits the target.

Built by a UX designer who has lost those arguments, for people who'd rather not.

## The six skills

**01 design-sameness-check.**<br>
For when the landing page could belong to anyone. Rates layout, type, colour, imagery, motion and copy as Distinct, Mixed or Generic, then suggests alternatives only your product could use. It leaves usability conventions alone; familiar interaction is fine, generic expression is the problem. Works on screens or straight on the code. [Docs](docs/design-sameness-check.md)

**02 deceptive-pattern-pushback.**<br> 
For when someone asks you to "make the opt-out less prominent". Audits flows and classes each finding Dark, Grey or Mistake, or turns the request into a one-page brief: the pattern, the risk, an honest alternative and how to measure it. Comes with a Slack-length version, because nobody reads the page. [Docs](docs/deceptive-pattern-pushback.md)

**03 heart-metrics-plan.** <br>Baselines before launch, not three months later when someone asks "did it work?" Goals, signals, metrics, targets, guardrails and who owns each one, plus the events engineering needs to add. No analytics? It has proxies. [Docs](docs/heart-metrics-plan.md)

**04 design-decision-record.** <br>Because "we decided that in a meeting in March" is not a record. One decision, what was rejected, what was given up, who agreed, and when to revisit. If design was overruled, it says so, without the passive aggression. [Docs](docs/design-decision-record.md)

**05 ux-debt-entry.** <br>The compromises you shipped to hit a date, written down before everyone forgets them. Severity, cause, fix, effort, and the cost of leaving it, which is the only column anyone prioritises from. Takes one item or a pile of Figma comments. [Docs](docs/ux-debt-entry.md)

**06 design-impact-write-up.** <br>Case studies without the made-up 40%. Builds a write-up, case study or 150-word summary from whatever evidence exists, labels every figure as measured, proxy or estimate, and tells you what's missing. It will not round up. [Docs](docs/design-impact-write-up.md)

Each one runs on its own, whenever you need it. None of them assumes another has run first, because real projects don't happen in order.

## Try it

- "Run a sameness check on this landing page"
- "Product want two more save screens in the cancel flow. Help me push back."
- "What should we measure before the new onboarding ships?"
- "Log this decision" (with a pasted thread)
- "Add these review comments to UX debt"
- "Write up the payee setup redesign for my portfolio"

Or name the skill if you want to be sure: "use ux-debt-entry on these".

## Works with your tools

The skills read from and write to whatever you've connected: Figma, Jira, Linear, Notion, Confluence, Google Sheets, Slack, Mobbin, a repo in Claude Code, or Claude Design. Nothing connected? You paste in, it pastes back.

To stop telling it where things live, add a routing note. Copy [`check-your-head.example.md`](check-your-head.example.md) to your repo root as `check-your-head.md`, or paste it into `CLAUDE.md` or a Claude Project's instructions. Decisions to Notion, debt to Jira, write-ups to wherever you keep the good stuff.

It always asks before creating tickets, posting comments or editing shared pages. Nobody wants to explain 40 surprise Jira issues to a delivery manager.

## What's inside

```
check-your-head/
├── skills/
│   └── <skill-name>/
│       ├── SKILL.md       Works on its own
│       ├── references/    The depth: tell lists, pattern catalogues,
│       │                  severity rules, evidence ladder, tool routing
│       ├── templates/     Output formats
│       └── examples/      A worked example, so you know what good looks like
├── docs/                  One page per skill
└── check-your-head.example.md   Routing note template
```

Every skill carries its own copy of the tool routing guide, so you can install one without the other five.

## Installation

### Claude Code

```
/plugin marketplace add alexconner-79/check-your-head
/plugin install check-your-head@check-your-head
```

Or cherry-pick: copy any folder from `skills/` into `~/.claude/skills/`.

### Claude.ai / Claude Desktop

Download `check-your-head.plugin` from [Releases](https://github.com/alexconner-79/check-your-head/releases) and open it in Claude. Want just one skill? Upload its folder from `skills/` in Settings instead.

## A word on the legal bits

deceptive-pattern-pushback knows its way around the DMCC Act, FCA Consumer Duty, UK GDPR, PECR, Ofcom rules, the DSA and the AI Act. It is not a lawyer and won't pretend to be one. Several of those rules are still being phased in, so it checks current status before citing anything and tells you when to call compliance.

## The name

Check Your Head is the Beastie Boys album. These skills check your work before someone else does. Same naming policy as [ill-communication](https://github.com/alexconner-79/ill-communication), same level of restraint.

## Lineage and credits

- **HEART** is from Kerry Rodden, Hilary Hutchinson and Xin Fu at Google, *Measuring the User Experience on a Large Scale* (CHI 2010)
- **Decision records** borrow from Michael Nygard's architecture decision records, moved to the design side of the table
- **Deceptive patterns** build on Harry Brignull's work at [deceptive.design](https://www.deceptive.design), the Center for Democracy & Technology's 2026 taxonomy of dark patterns in AI chatbots, and the Dark, Grey and Mistake classes used in Uxcel's dark patterns audit
- **The AI-generated dark patterns stat** is from Chen et al., [Deception at Scale](https://arxiv.org/abs/2502.13499): more than half of 1,296 LLM-generated ecommerce components contained at least one deceptive pattern
- **The anti-slop instinct** owes a nod to Anthropic's frontend-design skill and its stand against purple gradients

## Also by me

- [ill-communication](https://github.com/alexconner-79/ill-communication): UX writing, not fighting
- [high-plains-drifter](https://github.com/alexconner-79/high-plains-drifter): Figma to React component alignment

## Licence

MIT. See [LICENSE](LICENSE). Contributions welcome, especially new tells and patterns; see [CONTRIBUTING](CONTRIBUTING.md).
