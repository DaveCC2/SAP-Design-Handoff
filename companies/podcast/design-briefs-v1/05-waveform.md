# 05 · 1e — Waveform

## Feeling

Audio-first and unembarrassed about it. A studio, not a media company — the medium is the identity.

## Layout logic

Type anchored top-left in a single measure; the lower band given entirely to sound. No photograph above the fold, so the sentence carries the whole load.

## Key visual choice

A full-bleed waveform used as the horizon line of the page. It is the only graphic element in the design, and it decays left-to-right so the eye lands where the button already is.

## Spec

```
Ground: #0e1216
H1: Newsreader 400, 34px/1.26, -.014em, #eef2f5 — column top 96px, left 52px, width 600px, z-index 2
Waveform: 34 bars, flex:1, gap 3px, strip height 104px, padding 0 52px 40px, z-index 1, opacity .9
  Bar ramp: #1e4d42 → #22574a → #266153 → #2b6b5c → #2f7565 → #357f6d → #3a8a76 → #41957f → #48a189 → #4fad92 → #4fd1a5 (peak)
Accent: #4fd1a5 button, #08140f text
Button copy: Hear the conversation
CONSTRAINT: the text column must stay above the strip, and the tallest bar must top out below the button. Fixed once already.
```

## Honest risk

Clearest statement that this is a podcast. No human face above the fold.

---

H1 for this direction: see `00-shared-spec.md`. Proof slot and `[FILL]` items unresolved.
