# Sameness tells

Each tell has a visual description and, where useful, the code signals that tend to produce it. Code signals find candidates only; confirm in context.

## Layout

| Tell | Code signals |
|---|---|
| Centred hero: eyebrow, H1, subhead, two buttons, product screenshot below | `text-center` hero wrapper with a small uppercase `tracking-wide` label above `h1`, then two adjacent buttons |
| Three or six feature cards, each an icon, heading and two lines | `grid-cols-3` with repeated icon, `h3`, `p` children |
| Bento grid used as decoration rather than to show real content | Irregular `col-span` and `row-span` grids filled with placeholder copy or icons |
| Stat band of round, unsourced numbers ("10x", "99.9%", "500+") | Repeated large number plus small label, no source or footnote |
| The full template sequence: hero, logo wall, features, testimonials, pricing, FAQ, CTA band | Section order matches exactly, each section full-width with identical vertical padding |
| Everything centred, every section the same rhythm | Uniform `py-24` or equivalent on every section |
| Split hero with text left, floating device mockup right, tilted | `rotate-` and `perspective` on a device frame |

## Type

| Tell | Code signals |
|---|---|
| One neutral sans for everything with no typographic voice | Only `Inter`, `Geist`, `Roboto`, `system-ui` or `font-sans` declared |
| Gradient-filled headline text | `bg-clip-text text-transparent bg-gradient-to-` |
| Oversized H1 with tight tracking and a muted grey subhead, regardless of content | `text-6xl` or larger `tracking-tight` with `text-muted-foreground` or `text-gray-500` subhead |
| Uppercase letter-spaced labels everywhere | `uppercase tracking-widest text-xs` repeated |

## Colour

| Tell | Code signals |
|---|---|
| Purple to blue or pink to orange gradients | `from-purple-` `to-blue-`, `from-indigo-`, `from-pink-` `to-orange-` |
| Gradient blobs or mesh backgrounds | Absolutely positioned blurred circles: `blur-3xl`, `opacity-30`, `rounded-full` |
| Dark UI with a neon accent by default, regardless of brand | `bg-black` or `zinc-950` base with one saturated accent |
| Glassmorphism | `backdrop-blur`, `bg-white/10`, thin white borders |
| Default library palette unchanged | Unmodified shadcn, Tailwind or Material default tokens |

## Imagery and iconography

| Tell | Code signals |
|---|---|
| Default icon set standing in for meaning | Lucide, Heroicons or Feather icons inside every feature card |
| Emoji as icons | Emoji characters in headings or cards |
| Generic 3D shapes, abstract illustrations, stock people | Generic image file names, illustration packs, stock URLs |
| Large radius cards with soft shadows on every surface | `rounded-2xl` or `rounded-3xl` with `shadow-lg` or `shadow-xl` on most containers |
| Avatars stacked with "Trusted by 10,000+" | Overlapping avatar group next to a count |

## Motion

| Tell | Code signals |
|---|---|
| Fade-up-on-scroll on every block | One reveal animation applied to every section |
| Decorative motion that explains nothing | Floating, pulsing or rotating elements with no state change |
| Marquee logo strips | Infinite horizontal scroll animation |
| Hover lift on every card | `hover:-translate-y-` with `hover:shadow-` on all cards |

## Copy

- Eyebrow text above headings
- Verbs: unlock, supercharge, elevate, empower, transform, revolutionise, streamline
- Adjectives: seamless, effortless, powerful, intuitive, cutting-edge, next-generation
- "Not just X, it's Y" and "X, reimagined"
- Rule-of-three lists and three-word taglines ("Fast. Simple. Secure.")
- Rhetorical questions as headings ("Tired of spreadsheets?")
- Em dashes in body copy
- CTAs that could sit on any site: Get started, Learn more, Book a demo, Start for free
- Headlines that claim a benefit any competitor could claim equally
- Testimonials with no surname, company or specifics

## Not tells

Don't flag these unless they are clearly unexamined defaults:

- Conventional navigation and footer structures
- Standard form controls and validation patterns
- Platform UI (iOS, Android, Material) inside native apps
- Content required by regulation (risk warnings, representative APR, FSCS badges)
- Accessible contrast, focus states and sizes, even when plain
- A neutral sans chosen deliberately as part of a brand system
