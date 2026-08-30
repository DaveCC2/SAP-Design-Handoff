# 00 — Decisions and flags

Read this before building anything.

## 1. The sentence was changed. Deliberately. ⚠

`build-manifest-v1.md` § 1 gives the elevator pitch ending in the career framing that
**Rosetta Stone v1.5 names a hard fail** — and § 3 instructs that pitch be used verbatim as the H1.
The manifest was therefore propagating the banned framing into every design built from it.
This is the most likely mechanism behind the thirty homepage designs that had to be redone.

**Resolution:** the closing clause is replaced in all fifteen with the stone's own softened
wording from v1.4 item 3 — *"belong in public life, not just finance or tech"* — which preserves
the intent without disparaging anyone's job. Nothing was invented; the substitute is the stone's
own sentence.

**Action required upstream:** the manifest still carries the old pitch in two places —
§ 1 Elevator pitch, and the identical line in the Rosetta appendix § 2. Fix both, or the next
tool that loads the manifest reintroduces it.

## 2. The logo is cover art, not a wordmark ⚠

The supplied artwork is a photographic dark flag relief with the show name baked into the image.
It cannot do a wordmark's job: at header size on a light ground it reads as a small dark square
and the name inside it is illegible.

**Resolution:** the name is set as type in every direction, and the artwork sits beside it at
cover-art size — the role it actually plays. Nothing was redrawn or recoloured.

**Consequence:** it is red, white and blue. **1k No Jersey** omits it entirely, because its whole
argument is a palette with no red and no blue. If 1k wins it needs a mark that is not the flag.

**Recommendation:** a wordmark or monogram that works small and on light grounds is a separate
piece of brand work, distinct from the cover art. Not started — awaiting Dave.

## 3. Still open in the manifest (rendered as visible `[FILL]` slots, never filled)

1. **Button copy** — which of the three options.
2. **Three anchor guests** + 5–7 carousel entries (name, role, conversation line). 1j and 1m degrade
   most without these.
3. **"What this is"** — final 2–3 sentences.
4. **The specific action** for Block 5 — what a serious person does this week. This is the end state
   the whole page points at, and it is still undefined.
5. **Dive-deeper links** — newsletter URL, resources link.

## 4. 1i needs one line of new copy

The only direction requiring copy that is not in the manifest: a question line, shown as
*"What if the best and brightest actually served?"* and flagged in the mock as needing approval.
Approve, replace, or drop the direction.

## 5. Scope of this package

Hero / above the fold only. Blocks 2–7 of the manifest (proof carousel, what-this-is, dive-deeper,
action, FAQ, footer) are not designed here. Bios and social handles are held verbatim for those
sections and were not rewritten.

## 6. Fixes already applied — do not regress

- **1e** — text column above the waveform strip; tallest bar clears the button. The CTA must stay
  fully unobstructed.
- **1n** — centred column padded below the absolute header row.
- **1o** — portal is `box-sizing: border-box`; content-box sizing beheads the arch.
- **Contrast** — 33 colour values corrected to clear AA. Do not re-lighten.
