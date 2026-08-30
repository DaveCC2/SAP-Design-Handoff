# Handoff: Solving America's Problems — Homepage Hero

## Overview

Fifteen visual directions for the above-the-fold hero of the Solving America's Problems
podcast homepage. The fold has exactly one job: **get a stranger to subscribe to the podcast.**

**This is a pre-decision package.** Dave has not yet picked a winner. Nothing here should be
built yet unless you have been told which direction won. When a winner is named, build that one
and delete the other fourteen — the project's own rule is one writer of code, and leftover
variants confuse the next session.

## About the design files

The files in this bundle are **design references created in HTML** — prototypes showing intended
look and layout, not production code to copy directly. The task is to **recreate the winning
design in the target codebase's existing environment** (React, Vue, Astro, plain HTML, whatever
the site uses) using its established patterns and libraries. If no environment exists yet, choose
an appropriate one — this is a marketing page with a sub-second load budget, so a static site
generator or hand-written HTML/CSS is more appropriate than a client-side framework.

`SAP Homepage - 15 Directions.dc.html` is a **comparison canvas**, not a page. It renders all
fifteen heroes side by side at 900×600 inside annotation cards. Do not port its structure. Read
the hero you need out of it and rebuild that hero at real viewport scale.

## Fidelity

**High-fidelity for visual language, low-fidelity for viewport.**

- Colors, typography, weights, letter-spacing, accent choices and layout logic are final and
  exact. Use the hex values as given.
- The mocks are authored inside a 900×600 frame, treated as a small laptop viewport. Type sizes
  are correct *for 900px wide*. Scale up for real breakpoints — a 40px H1 in the mock is roughly
  a 56–64px H1 at 1440px. Keep the ratios, not the absolute pixels.
- No mobile layouts were designed. Mobile-first is a hard requirement of the brief, so the
  responsive behavior below must be designed during build.

## Screens / views

One screen: the homepage hero, in fifteen variants. Full per-direction specs are in
`design-briefs-v1/01-*.md` through `15-*.md` — each carries feeling, layout logic, the one key
visual choice, an exact spec block, and an honest risk note.

### Shared across all fifteen

**Purpose.** A first-time visitor arrives, understands what the show is in one breath, sees one
line of reassurance about guest caliber, and clicks one button to subscribe.

**Content, in order:**

1. Wordmark — the show name set as type, with the cover-art tile beside it (see Assets)
2. H1 — the sentence, verbatim:
   > The weekly podcast that turns real conversations about America's toughest issues into a
   > movement — built by people who believe the best and brightest belong in public life, not
   > just finance or tech.
3. Proof line — one line on guest range. **Still unwritten.** Rendered as a visible dashed
   `[FILL]` slot. Do not invent it. Do not ship the placeholder.
4. Button — one only.

**What must NOT appear above the fold:** email capture, social icons, a second button, a nav bar,
a newsletter signup, testimonials, statistics. The single ask is the entire point of the fold.

### The fifteen directions, condensed

| # | Name | Ground | H1 | Accent / button | The one choice |
|---|---|---|---|---|---|
| 1a | Sunday Night | `#0b0d10` + warm radial | Newsreader 300 40/1.24 `#f6f3ec` | `#e0a458` on `#14161a` | A pool of warm light instead of an image |
| 1b | Broadsheet | `#f7f5f0` / `#12100e` | Newsreader 400 41/1.14 | solid `#12100e` | Hairline rules + dateline replace the nav |
| 1c | Two Voices | photo split | Newsreader 400 27/1.28 on `#faf7f1` card | solid `#17150f` | Halves graded warm vs cool |
| 1d | Ballot | `#e6e3da` / sheet `#fdfdfa` | Public Sans 600 28/1.3 | `#1b2a4a` ballot oval | Button drawn as a filled ballot oval |
| 1e | Waveform | `#0e1216` | Newsreader 400 34/1.26 `#eef2f5` | `#4fd1a5` on `#08140f` | Waveform as the page's horizon line |
| 1f | Shop Sign | `#1d3a34` / `#f4efe4` | Archivo 800 52/.98 | cream on green | Splits the sentence — the shortening test |
| 1g | Transcript | `#fcfcfa` | Newsreader 400 32/1.32 | solid `#16150f` | Timecode gutter; two speaker colors |
| 1h | Kitchen Table | `#efe9df` | Newsreader 400 31/1.28 | solid `#221f19` | Photo bleeds off 3 edges, no scrim at all |
| 1i | The Question | `#f5f2ec` | Instrument Serif 60/1.06 display; H1 demoted to 17/1.5 | solid `#1a1813` | Inverted hierarchy — question over answer |
| 1j | Index | `#faf9f6` | Public Sans 600 27/1.3 | solid `#15150f` | Heavy pale numerals as the rhythm |
| 1k | No Jersey | `#ffffff` / `#111111` | Public Sans 300 36/1.3 | `#2f6f5e` | One accent, deliberately not red or blue |
| 1l | Marquee | `#0e0e0f` | Archivo 800 46/1.02 | outlined `#dcae4a` | Ticker strip carries every standing fact |
| 1m | Field Notes | `#f8f7f2` | Newsreader 400 33/1.3 | solid `#1b1a15` | Monospace marginalia beside the pitch |
| 1n | The Hour | `#fdfcf9` | Newsreader 300 35/1.3 | solid `#1c1b15` | A 60-minute scale closes the fold |
| 1o | Threshold | `#0f1211` | Newsreader 400 25/1.34 | solid `#1a1710` | One arch, one radius, one gradient |

## Interactions & behavior

Deliberately minimal — this is a conversion fold, not an app.

- **The button** is the only interactive element above the fold. It should link to the show's
  universal listen page: `https://solving-americas.captivate.fm/listen`. Per-platform links
  (Apple, Spotify, Amazon) belong behind that page or in a chooser below the fold, not competing
  in the hero.
- **Hover** on the button: darken or lift by one step. No scale transforms, no glow. Never animate
  the H1.
- **Focus** must be visibly distinct, not just a color shift — a real outline offset. Keyboard
  users are part of AA.
- **No entrance animations on the H1.** Every extra frame before the sentence is readable is
  conversion lost against the sub-second budget.
- **Loading / error / form states:** none. There is no form in the hero.
- **Responsive** (must be designed, not specified): single column at every width; the H1 is the
  only thing that must never wrap awkwardly; the button goes full-width below ~480px; hit target
  never below 44px. In 1c the split should stack (Jerremy above, Dave below, card between) rather
  than shrink. In 1h the photo should move above the type. In 1o the arch should narrow but keep
  its radius ratio.

## State management

None. This is a static fold — no state variables, no data fetching, no client-side JS required
beyond whatever the site already loads. If the proof line eventually rotates through guests, that
is a below-the-fold carousel concern, not hero state.

## Design tokens

**Grounds (light):** `#ffffff` `#fdfdfa` `#fdfcf9` `#fcfcfa` `#faf9f6` `#f8f7f2` `#f7f5f0`
`#f5f2ec` `#efe9df` `#e6e3da`

**Grounds (dark):** `#0b0d10` `#0e0e0f` `#0e1216` `#0f1211` `#1d3a34`

**Inks:** `#111111` `#12100e` `#14181f` `#15150f` `#16150f` `#1a1813` `#1a1710` `#1b1a15`
`#1c1b15` `#221f19`

**Accents (one per direction, never combined):**
`#e0a458` amber · `#4fd1a5` mint · `#dcae4a` gold · `#2f6f5e` deep green · `#1b2a4a` navy ·
`#b4551f` rust (labels only) · `#9c4515` rust-dark (flags on light grounds)

**Label greys — audited for AA, do not lighten:**
on light: `#615b4d` `#625b4c` `#635d4e` `#646054` `#66635b` `#67645c` `#6a675f` `#6b6860`
`#5c584f` `#5e5a4f` — on dark: `#9c968a` `#9aa8b3` `#a5a29a` `#9aa5a0` `#8db3a8`
Large numerals (26px/800) may go to `#8f8b7c` / `#8a8577` — 3:1 floor.

**Hairlines:** `#e2e0d8` `#e4e2da` `#d5d1c4` `#d9d6ca` `#ddd8cc` — and `#12100e` at 28% for
broadsheet rules.

**Dashed `[FILL]` borders:** `#b6b0a2` `#c2bbab` `#c3bdac` `#c4bcaa` `#cfcbbf` `#d3d0c5`
`#d5d1c5` `#d6d3ca` `#37424b` (dark) `#4a4a44` (dark) `#3f5f56` (dark)

**Typography scale (at 900px — scale up proportionally):**
display 60–52 · H1 46–25 · body 17–15 · label 11–9

**Type stack:** Newsreader (300/400, editorial serif, default H1 voice) · Archivo (800 only,
signage and broadcast) · Public Sans (300/600/700, buttons everywhere) · IBM Plex Mono (400/500/600,
all labels, timecodes, `[FILL]` flags) · Instrument Serif (1i only). All Google Fonts. No Inter,
no Roboto, no Arial.

**Radius:** 0 everywhere, with two deliberate exceptions — the ballot oval in 1d (`12px`), the
portal in 1o (`235px 235px 0 0`), and 3px on waveform bars in 1e.

**Shadows:** used only to lift a card off a photograph — `0 30px 70px -20px rgba(0,0,0,.6)` in 1c,
`0 18px 40px -18px rgba(20,24,32,.35)` in 1d. No shadows on buttons.

## Assets

Included in `assets/`, all real and supplied by Dave — **no stock photography, no generated
faces, no generated logo, no hand-drawn SVG imagery anywhere in this package.**

- `assets/headshots/Jerremy Headshots/Jerremy happy chest up 2.jpg` — used in 1c (left half),
  `object-position: 50% 22%`
- `assets/headshots/Jerremy Headshots/Jerremy sitting contemplative.jpg` — used in 1h,
  `object-position: 46% 26%`, no scrim
- `assets/headshots/Dave Headshots/dave neutral standing chest up.jpg` — used in 1c (right half),
  `object-position: 50% 20%`
- `assets/logos/SAP Logo smaller.jpeg` — 1:1 crop, used as the cover tile at 34–46px in fourteen
  of fifteen directions
- `assets/logos/SAP Logo.jpeg` — 4:3 crop of the same artwork, unused, included for reference

Two further Jerremy frames and two further Dave frames are in the bundle unused, for crop options.
The full expression sets (13 Dave, 20 Jerremy) live in the source repo.

**Important — the logo is cover art, not a wordmark.** It is a dark photographic flag relief with
the show name baked into the image. It cannot carry the header role: at 36px on a cream ground it
reads as a small dark square and the name inside it is illegible. In every direction the name is
set as **type** and the artwork sits beside it at cover-art size. Do not scale the artwork down to
serve as a logo, and do not extract or trace the lettering out of it.

Real alt text is required on every image. The alt used for the artwork:
*"Solving America's Problems cover art: a weathered American flag relief with the show name."*

## Hard floor — non-negotiable, from the client's own brief

- Mobile first. **Sub-second load.** Every extra second burns conversion.
- **WCAG 2 AA.** Every label tier above is specified at ≥4.5:1 (large numerals ≥3:1). This was
  audited and corrected across 33 values — **do not re-lighten the greys** for visual softness.
- Real alt text on every image. Visible focus states.
- Copy at 5th–6th grade reading level.
- Banned words on the page: unlock, unleash, empower, leverage, synergy.
- **Jerremy** is spelled with two r's. Always. Never "Jeremy."
- Nothing invented: no fake guests, no invented statistics, no testimonials, no paid tier, no
  pricing, no party affiliation, no manufactured urgency.

## Blocking items — read before you build

1. **The proof line is unwritten.** Every direction shows a dashed `[FILL]` slot. Do not invent a
   guest, a role, or a caliber claim. Ship blocked until Dave supplies it.
2. **1i requires one line of new copy** (a question). Placeholder shown and flagged. Approve,
   replace, or drop the direction.
3. **1k omits the cover art on purpose** — its argument is a palette with no red and no blue, and
   the artwork is a red-white-and-blue flag. If 1k wins it needs a mark that is not the flag. That
   is separate brand work, not started.
4. **The client's build manifest still contains banned copy.** Its elevator pitch closes on a
   career framing that the current Rosetta Stone (v1.5) classifies as a hard fail, and the manifest
   instructs that pitch be used verbatim as the H1. The H1 in this package uses the corrected
   wording. If you regenerate copy from the manifest rather than from this README, you will
   reintroduce the problem. See `design-briefs-v1/00-decisions-and-flags.md` § 1.

## Files

- `SAP Homepage - 15 Directions.dc.html` — the comparison canvas, all fifteen heroes rendered
- `design-briefs-v1/README.md` — how the brief set is organised
- `design-briefs-v1/00-shared-spec.md` — what is identical across all fifteen
- `design-briefs-v1/00-decisions-and-flags.md` — every judgement call and open item
- `design-briefs-v1/01-*.md` … `15-*.md` — one full brief per direction
- `assets/` — headshots and logo artwork

Note on paths: the canvas file references images at `companies/podcast/assets/...`, which is
correct once committed at this location in the repo. The headshots and logo artwork are already
in the repo under that path — they are not duplicated here.

Scope note: this package covers the hero only. The remaining homepage blocks — proof carousel,
"what this is", dive-deeper links, the action, FAQ, footer — are specified in the client's build
manifest but were not designed here. Host bios and social handles are to be used verbatim and were
not rewritten.
