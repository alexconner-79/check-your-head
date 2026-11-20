# design-sameness-check

Finds where a design looks like everyone else's, and tells you what to do instead using material only your product has.

## When to use it

- A landing page, screen or prototype feels templated
- You've generated UI with AI and want to catch the defaults
- You want to know if a design would survive the logo swap test against competitors
- Before a design review, to get ahead of "this feels a bit generic"

## How to ask

- "Run a sameness check on this" (screenshot, URL, Figma link or Claude Design artifact)
- "Does this look AI-generated?"
- "Scan the marketing site components for generic patterns" (in Claude Code, on a repo)
- "Compare our hero with our two main competitors and tell me what's generic"

## What it checks

Six areas: layout, type, colour, imagery, motion and copy. The full tell list, including the Tailwind and React patterns that tend to produce each tell, is in [`references/tells.md`](../skills/design-sameness-check/references/tells.md).

It deliberately ignores conventions that help usability: standard navigation, form patterns, platform UI, accessible defaults and content required by regulation. Familiar interaction is good. Generic expression is the problem.

## What you get

1. A two-sentence verdict and the single biggest fix
2. The logo swap test result
3. A Distinct, Mixed or Generic rating for each area, with a reason
4. A findings table: what's generic, why it matters here, the specific alternative, severity, and location (frame name or file and line)
5. **Protect**: what's already distinctive and should survive revision

It uses ratings, not a score out of 100, because a number would suggest more precision than this kind of judgement has.

See the worked example: [fintech landing page](../skills/design-sameness-check/examples/fintech-landing.md).

## Tools

| Reads from | Writes to (if you ask) |
|---|---|
| Screenshots, URLs, Figma, Claude Design, repo code, Mobbin for category patterns | Figma comments on each frame, or tickets in Jira or Linear |

## Make it yours

Add tells your team keeps seeing to `references/tells.md`. Add brand-specific sources of distinctiveness (a typeface, a photography style, a domain) to `references/distinctiveness-sources.md`.
