# Refining the rubric

The rubric is grounded in **external reception** — how work is received in the
world. The world moves, so the rubric can drift. This is how you re-ground it.

## Do this rarely

The single most important rule: **refine infrequently.** Re-tuning against last
week's feed overfits to noise and erodes a standard that was already sound.
Over-verification is the failure mode, not under-verification. Trust the rubric
between refreshes. Refine only when *you* sense real drift — a criterion that
keeps mis-scoring things you know are strong (or weak) — not on a schedule, and
never automatically.

## The manual loop (the default)

1. Go read 5–10 genuinely high-performing pieces in your lane — posts, repos,
   launches that drew the eye of people hiring or scaling.
2. Ask what they have in common that the rubric *doesn't* currently reward, or
   what the rubric rewards that no longer earns attention.
3. Make **one small edit** to `rubric.yaml`: reword a test, nudge a scale, add at
   most one criterion. Bounded edits only — never a rewrite. A rubric you can
   still recognize next month is the point.

That's it. No infrastructure, human in the loop, done in ten minutes.

## Someday-maybe: automated harvest

If manual sourcing ever becomes the actual friction (it probably won't at
personal scale), the external feed could be automated with an Apify LinkedIn
post-search scrape of recent high-engagement posts in your lane, distilled into
*proposed* edits you still accept by hand.

Deliberately **not** in v1: it's fragile (LinkedIn DOM/auth), costs money, and
serves the rarest path. It also measures *attention*, not attention *from hiring
eyes* — so even with it, the human judgment in step 2 stays the real work. Add it
only when you've felt the manual loop break, never before.
