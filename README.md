<p align="center"><img src=".claude-plugin/icon.png" width="120" alt="Check Your Head icon"></p>

# Check Your Head

Six Claude skills for the parts of design work that need evidence. Check a design isn't generic. Say no to a dark pattern and offer something better. Decide how you'll measure it, record why you chose it, log what you compromised, and show what it achieved.

Each skill runs on its own, at any point, for any feature. It's free and MIT licensed.

## Why

Most design arguments get lost on evidence. Nobody captured a baseline, nobody wrote down why option B won, and when the outcome is questioned there's nothing to point at. AI-assisted work adds a second problem: it drifts towards the same templates, and often the same manipulative patterns. In one study, more than half of 1,296 LLM-generated ecommerce components contained at least one deceptive pattern ([Chen et al.](https://arxiv.org/abs/2502.13499)).

So paste a Slack thread and get a decision record. Point at a Figma frame and get a sameness check. Forward a stakeholder request and get a pushback brief you can send.

## The skills

| Skill | Use it when | You get |
|---|---|---|
| [design-sameness-check](docs/design-sameness-check.md) | A design looks generic, templated or AI-made | Ratings by area, findings with alternatives specific to your product, and a list of what to protect. Works on screens or code. |
| [deceptive-pattern-pushback](docs/deceptive-pattern-pushback.md) | You're reviewing consent, pricing, checkout, cancel or retention flows, or pushing back on a request | An audit classed Dark, Grey or Mistake, or a one-page pushback brief with an honest alternative and a version short enough for Slack |
| [heart-metrics-plan](docs/heart-metrics-plan.md) | Before release, or when someone asks how a design will be measured | A HEART table with baselines, targets, guardrails, owners and the events engineering needs to add |
| [design-decision-record](docs/design-decision-record.md) | A decision just happened in a meeting, thread or comment | A short, dated record: options, trade-off, who agreed, when to revisit |
| [ux-debt-entry](docs/ux-debt-entry.md) | You've shipped or spotted a compromise, or have review comments to triage | Debt rows or tickets with user impact, severity, cause, fix, effort and the cost of leaving it |
| [design-impact-write-up](docs/design-impact-write-up.md) | A project ends, a review is due, or your portfolio needs a case study | A write-up, case study or 150-word summary, with every figure labelled as measured, proxy or estimate |

## Try it

Once installed, ask in plain language. For example:

- "Run a sameness check on this landing page" (with a screenshot, URL or Figma link)
- "Product want to hide the cancel button in settings. Help me push back."
- "What should we measure for the new onboarding flow before it ships?"
- "Log this decision" (with a pasted Slack thread)
- "Add these review comments to the UX debt register"
- "Write up the impact of the payee setup redesign for my portfolio"

## Install

**Claude (web and desktop):** download the `.plugin` file from the [latest release](https://github.com/alexconner-79/check-your-head/releases) and open it in Claude to install. To install a single skill, upload its folder from `skills/` as a skill instead.

**Claude Code:**

```
/plugin marketplace add alexconner-79/check-your-head
/plugin install check-your-head@check-your-head
```

Or copy any folder from `skills/` into `~/.claude/skills/` (just for you) or `.claude/skills/` (for everyone on a project).

## Works with your tools

The skills read from and write to whatever you have connected: Figma, Jira, Linear, Notion, Confluence, Google Sheets, Slack, Mobbin, a repo in Claude Code, or Claude Design. With nothing connected, you paste things in and get output ready to paste back.

To send records to the right place automatically, add a routing note. Copy [`check-your-head.example.md`](check-your-head.example.md) to your repo root as `check-your-head.md`, or paste it into `CLAUDE.md` or a Claude Project's instructions. Each project can route to different tools, for example decisions to Notion and debt to Jira.

The skills always ask before creating tickets, posting comments or editing shared pages.

## How each skill is built

```
skills/<skill-name>/
├── SKILL.md        Works on its own
├── references/     Depth Claude reads when it needs it
├── templates/      Output formats
└── examples/       A worked example showing the expected quality
```

Every skill carries its own copy of the tool routing guide, so you can install any one without the others.

## FAQ

**Do I need any connectors?**
No. Connectors save copying and pasting; the skills work without them.

**Is the regulatory content in deceptive-pattern-pushback legal advice?**
No. It's orientation on UK and EU rules so you know when to involve legal or compliance. Several provisions are being phased in, so the skill checks current status before citing anything.

**Will it make up numbers in my case study?**
No. The impact write-up labels every figure and won't invent or round up. If evidence is thin, it says so and tells you where to get more.

**Can I change the tell list, patterns or severity rules?**
Yes. They live in each skill's `references/` folder as plain markdown. See [CONTRIBUTING](CONTRIBUTING.md).

**Are the examples real?**
No. Every example uses a fictional company.

## Also by me

- [ill-communication](https://github.com/alexconner-79/ill-communication): UX writing and microcopy skill
- [high-plains-drifter](https://github.com/alexconner-79/high-plains-drifter): Figma to React component alignment

## Licence

[MIT](LICENSE)
