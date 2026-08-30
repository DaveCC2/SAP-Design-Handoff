# 15 · 1o — Threshold

## Feeling

An opening rather than an argument. Warm light coming from the other side of something — the show as the door, which is the manifest's own framing.

## Layout logic

A single arched aperture rising from the bottom edge holds all the content; everything outside it is dark and empty. The button sits inside the opening, so the click and the threshold are the same object.

## Key visual choice

The portal is drawn purely with one radius and a light gradient — no illustration, no photograph, no borrowed civic architecture.

## Spec

```
Ground: #0f1211
Portal: box-sizing border-box, 470×492px, bottom 0, centred, radius 235px 235px 0 0
  fill linear-gradient(180deg, #f6efe2 0%, #efe4cf 46%, #e6d6b8 100%)
  padding 104px 52px 46px (top padding must keep the first text line inside the curve), gap 20px
  glow 0 -20px 90px rgba(232,203,146,.22)
H1: Newsreader 400, 25px/1.34, -.01em, #1a1710, centred
Wordmark: IBM Plex Mono 500 10px/.24em #9aa5a0 above the arch; cover tile 36px
Button: #1a1710 ground, #f6efe2 text
Button copy: Start listening
CONSTRAINT: content-box sizing beheads the arch. Keep border-box.
```

## Honest risk

Most distinctive silhouette. Narrowest measure of the fifteen — pressures the sentence hardest.

---

H1 for this direction: see `00-shared-spec.md`. Proof slot and `[FILL]` items unresolved.
