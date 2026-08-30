# 00 — Shared spec

Everything in this file is identical across all fifteen directions. Only the feeling,
the layout logic and one visual decision change.

## The one job

Get a stranger to subscribe to the podcast. One ask above the fold. Nothing competes with it:
**no email capture, no social icons, no second button, no newsletter, no nav.**

## The sentence (H1)

> The weekly podcast that turns real conversations about America's toughest issues into a movement — built by people who believe the best and brightest belong in public life, not just finance or tech.

Used verbatim as the H1 in every direction except **1f**, which splits it deliberately as
the shortening test case (12-word sign, full pitch verbatim beneath).

**This is not the manifest's wording.** See `00-decisions-and-flags.md` § 1.
It runs 30 words — still longer than one breath. A sentence pass is worth doing before build.

## The proof element

One line of reassurance about guest range — not a list, not a testimonial, not a quote.
Still unfilled. Rendered as a visible dashed `[FILL]` slot in every direction.
Range matters more than fame: one CEO, one everyday person, one expert.

## The button

One only. Copy varies by direction, drawn from the manifest's three options:

- Subscribe — wherever you listen (1a, 1b, 1d, 1e·no, 1f, 1g, 1j, 1k, 1l, 1m, 1n)
- Start listening (1c, 1h, 1o)
- Hear the conversation (1e, 1i)

Dave picks one for the winner; the spread here is only to show each option in context.

## Type stack

| Role | Family | Notes |
|---|---|---|
| Editorial serif | Newsreader | 300/400 — the default H1 voice |
| Grotesque / display | Archivo | 800 only, for signage and broadcast weight |
| Civic sans | Public Sans | 300/600/700 — buttons everywhere, H1 in the civic directions |
| Mono | IBM Plex Mono | 9–11px labels, timecodes, all `[FILL]` flags |
| High-contrast display | Instrument Serif | 1i only |

No Inter, no Roboto, no Arial. All Google Fonts.

## Assets in use

Real, supplied, unretouched:

- `assets/headshots/Jerremy Headshots/Jerremy happy chest up 2.jpg` — 1c
- `assets/headshots/Jerremy Headshots/Jerremy sitting contemplative.jpg` — 1h
- `assets/headshots/Dave Headshots/dave neutral standing chest up.jpg` — 1c
- `assets/logos/SAP Logo smaller.jpeg` — cover tile, 34–46px, in 14 of 15 (not 1k)

No stock photography. No generated faces. No generated logo. No hand-drawn SVG imagery.

## Hard floor (from the manifest, non-negotiable)

- Mobile first. Sub-second load.
- **WCAG 2 AA.** Every label tier in these briefs is specified at ≥4.5:1; large numerals ≥3:1.
  This was audited and corrected — do not re-lighten the greys during build.
- Real alt text on every image.
- 5th–6th grade reading level.
- No buzzwords: unlock, unleash, empower, leverage, synergy.
- **Jerremy** — two r's. Always.
- Nothing invented: no fake guests, stats, testimonials, paid tier, or party affiliation.
