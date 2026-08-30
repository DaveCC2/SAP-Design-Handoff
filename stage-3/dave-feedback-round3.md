# Dave's feedback — Round 3 (Grok's second set, the 15 rooms)

**Date:** 2026-08-30
**Status:** Captured in chat, now committed so any future build can load it without relying on chat memory.

**Next chat starts at [`START-HERE.md`](START-HERE.md).** Round-two stills (the set this verdict is about) live in [`../stage-2/visual-directions/`](../stage-2/visual-directions/).

**Count lock (2026-08-30):** The next round is **six treatments**. Not fifteen. Not three. Not eight-to-ten.

## The honest verdict

Disappointing. Fifteen rooms, one layout. The only real differences were headshot choice and color scheme. No visual storytelling, no motion, no depth, no scroll story. It read the brief as decoration instead of constraints.

The "Near the ask" strip is a designer's note, not copy — it leaked into the page. Room treatments as backgrounds are a kill category.

We are at a 2–3 out of 10. Goal is 8–9.

## Hard rules (any treatment violating these is dead)

1. **No room treatments.** Ever. Backgrounds that are literal rooms are a kill category.
2. **No circular motifs.** Old, and three-circle layouts read wrong.
3. **No green.** That's Jerremy's main site; we differentiate. (Notes sometimes typed "Jeremy." Always write **Jerremy**.)
4. **No childish treatments.** Casual is fine; cartoonish isn't.
5. **Guests never above the button.** "Who sat in the chair" (or any guest strip) sits after the bios, near the bottom. Hard no on it being high.
6. **Photos centered, faces fully visible.** The warm-Jerremy / cool-Dave pairing is a keep — generous, never a jab.
7. **Legal footer is simple and human-readable.** Cookie policy, California opt-out, tracking cookies only. No modal, no timer, no "keep/don't keep" popup you have to dismiss. Social URLs live in the footer (Instagram, TikTok, X) or a subscribe-to-all — never a popup.
8. **Navigation is a design problem.** Design proposes the concept and the labels that fit the treatment. Do not leave a blank three-item fill.
9. **Mobile-first is non-negotiable.** Desktop-only layouts die.
10. **No shade on jobs.** The only approved bridge: "politicians treat it as a career; we don't." Statement about them, not a jab at the listener. Locked sentence stays verbatim; any paraphrase reintroducing "careers" as a target is an automatic fail.
11. **Bios revert to the long versions** with the better photo set. Short clipped bios are out.
12. **"Before you ask" beats FAQ.** Anchor it to the community-to-candidacy arc: community first, candidacy the movement, both the point. Say plainly that Jerremy is running for office.

## Keeps worth carrying

- Logo and branding at the top — genuine win across the set.
- **Conversation becomes a movement** — the one hook worth keeping. Echoes the stone's "conversation to candidacy" without copying it. Alliteration is a nice-to-have, not required.
- Big together-photos with name-and-title overlays (from 14) — first one that did something different with the photos.
- Banners at the top + conversation-becomes-a-movement (from 11).
- Rich gold-blue-red palette (from 10) — design's call against Jill, not mine.
- Photo choices from 06 even though the room treatment itself is dead.
- Warm-Jerremy / cool-Dave photo treatment — survived both rounds.
- Role tags mandatory: co-host and candidate / co-host and producer.
- The funnel order: Start listening → "when you're ready" (email + optional phone popup) → social → resources (coming soon) → this week (rolling last three episodes from the short link) → before you ask → bios → guests at the bottom.
- "This week" as a rolling list of the last three episodes.

## Kills

- Room treatments as backgrounds.
- Circular motifs.
- Green.
- Childish treatments.
- Guests high.
- "Near the ask" as visible copy.
- Weak hooks: "You're invited" (party), "Still here" (went somewhere), "Come in" (not a room), "Before Monday" (confusing), "This hour includes you" (maybe), "Listen" (weird), "Come as you are" (song lyric), "Start the week" (morning show), "Talk then act" (command, says little), "They showed up" (wrong — they're already talking).
- Only one hook to keep: conversation becomes a movement.

## Modern techniques (2026) — the gap the next round must close

The last set swung on color and motif, not on visual storytelling. The next six must actually use current techniques:

- **Scroll-driven animations** — native CSS `animation-timeline: scroll()` and `view()`. Parallax, reveals, progress — no JavaScript, runs on the compositor thread. This is the big one.
- **View transitions** — page-to-page and element morphing without jank.
- **Kinetic typography** — headlines that respond to scroll or hover; variable fonts that shift weight and width.
- **Micro-interactions** — button feedback, hover states, subtle breathing loops. Purpose over decoration. Under 300ms for UI feedback.
- **Glassmorphism** — sparingly, if it earns its place.
- **Bento grids / asymmetric layouts** — for personality without chaos.
- **Noise / texture** for organic feel.
- **Magnetic buttons + custom cursor** — only if it doesn't fight mobile.

Do NOT default to 2014-era parallax that hijacks scroll. Subtle, purposeful, accessible (`prefers-reduced-motion`).

## What I need from you (the next build)

**Six treatments.** Each must have a genuinely different visual move — name it by the move ("scroll-reveal faces," "kinetic headline," "depth field"), not by an evocative room name. Force divergence. Different rooms, not tighter versions of Sunday Night. Color swap is not a different move.

Every treatment must answer: **what stops the scroll in one to three seconds?**

Load these files first:
1. `stage-3/START-HERE.md`
2. `stage-3/dave-feedback-round3.md` (this file)
3. `stage-3/copy-lock.md` (wins over `visual-directions/_shared.md` on public copy)
4. `stage-2/dave-notes.md`
5. `rosetta-stone.md`
6. Round-1 strong examples: `visual-directions/` 01, 02, 07, 11, 03
7. Round-2 keep stills: `stage-2/visual-directions/` 11, 14, 10, 06, 03

Do not load Claude's `design-briefs-v1` folder. Do not load any prior chat. Fresh context, full memory from the files.

Output per treatment: feeling, layout logic, key visual choice (the actual technique), palette, type, navigation concept + proposed labels, one hero mock (phone + desktop), hard-fail check. No production code.
