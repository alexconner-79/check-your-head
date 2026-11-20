# Example: sameness check on a fictional SME lending landing page

Input: three Figma frames for "Ledgerly", a lender offering small business loans with decisions in 48 hours. Competitors given: Tallyfund, Brightloan (both fictional).

---

# Sameness check: Ledgerly landing page, desktop

**Reviewed:** Hero, Features, Social proof frames · **Brand:** Ledgerly · **Compared against:** Tallyfund, Brightloan

## Verdict

Reads as a generic fintech template: with the logo swapped it would pass for either competitor. The biggest fix is the hero, which hides the one thing Ledgerly has that the others don't (a decision in 48 hours from bank data alone) behind a gradient and a tilted phone.

**Logo swap test:** Nothing gives it away. The green accent is the only brand signal, and Brightloan also uses green.

## Area ratings

| Area | Rating | Why |
|---|---|---|
| Layout | Generic | Exact template sequence: hero, logos, three features, testimonials, CTA band |
| Type | Mixed | Inter throughout, but the tabular figures in the rate table are good |
| Colour | Generic | Purple to green hero gradient with blurred blobs |
| Imagery | Generic | Tilted phone mockup and Lucide icons in feature cards |
| Motion | Mixed | Fade-up on every section, but the repayment slider animation explains something |
| Copy | Generic | "Funding that moves at the speed of your business", eyebrow labels, "Get started" |

## Findings

| # | Area | What's generic | Why it matters here | Specific alternative | Severity | Location |
|---|---|---|---|---|---|---|
| 1 | Layout | Centred hero with eyebrow, H1, subhead, two buttons, tilted phone | The 48-hour decision is the differentiator and it is invisible | Lead with the actual decision screen showing a real offer and timestamp; headline "A decision in 48 hours. We only need your bank data." | Generic | Hero |
| 2 | Copy | "Funding that moves at the speed of your business" | Every competitor claims speed; this proves nothing | Use the specific number and its condition, with a footnote on what 48 hours depends on | Generic | Hero |
| 3 | Copy | Eyebrow "FAST BUSINESS LOANS" above H1 | Template tell; repeats the H1 | Remove | Generic | Hero |
| 4 | Imagery | Three cards with Lucide icons: Fast, Flexible, Fair | Icons carry no meaning; "Fair" is unsupported | Replace with three real borrower situations (VAT bill, stock before Christmas, a late-paying client) using actual figures | Generic | Features |
| 5 | Colour | Purple to green gradient with blurred blobs | Borrowed startup aesthetic; undermines a lender's seriousness | Use the ledger itself: ruled lines, tabular numerals, paper tone, green reserved for approved amounts | Generic | Hero background |
| 6 | Copy | Testimonials with first name only | Unverifiable; reads as invented | Full name, business, loan purpose and amount, with permission | Borderline | Social proof |
| 7 | Motion | Fade-up on every section | Adds latency, signals template | Keep motion only on the repayment slider and the decision timeline | Edge case | All sections |

## Protect

- Tabular figures and right-aligned numbers in the rate table
- The repayment slider that shows total cost changing in real time
- The plain-English representative example under the rate table

## Next step

Want these posted as comments on the three Figma frames, or raised as tickets?
