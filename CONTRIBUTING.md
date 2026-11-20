# Contributing

Improvements are welcome, especially new tells, patterns, proxies and regulatory updates from markets outside the UK and EU.

## Easy contributions

- **A sameness tell**: add a row to `skills/design-sameness-check/references/tells.md` with the visual description and, if you know them, the code signals.
- **A deceptive pattern**: add a row to `skills/deceptive-pattern-pushback/references/patterns.md` with what it is and the signals to look for.
- **A regulatory update**: edit `skills/deceptive-pattern-pushback/references/regulation-uk-eu.md`, or add a reference file for another market. Link to the regulator's own source in your pull request.
- **A metrics proxy**: add to the proxies list in `skills/heart-metrics-plan/references/heart-guide.md`.
- **An example**: add a worked example to a skill's `examples/` folder. Use a fictional company.

## Rules for every change

- **Keep skills standalone.** A skill must work with only its own folder installed. If you change `references/tool-routing.md`, change it in all six skills.
- **Keep SKILL.md lean.** Put detail in `references/`. Aim for under 700 words in SKILL.md.
- **No em dashes** anywhere. Use commas, colons, parentheses or a new sentence.
- **British English.**
- **Fictional examples only.** No real clients, colleagues or customer data.
- **No legal advice.** Regulatory content orients; it doesn't advise.

## Testing a change

Install the changed skill, then run it on its own worked example and on one real input of your own. Check that the output matches the template, labels every figure, and contains no em dashes.

## Releasing

Bump the version in `.claude-plugin/plugin.json`, add an entry to `CHANGELOG.md`, and attach the packaged `.plugin` file to the GitHub release.
