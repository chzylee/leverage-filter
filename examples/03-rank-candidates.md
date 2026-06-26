# Example — Rank (the headline mode)

Usage: *find the highest-leverage next move from several candidates.*
This is the mode that beats snap judgment — you can't hold five candidates
against the rubric in your head at once.

## Input

> "Just shared ts-pmo on LinkedIn. What should I do next? Candidates:
> A) Write a thread explaining ts-pmo's design tradeoffs.
> B) Build a small companion tool that scores work for 'leverage'.
> C) Fix three open bugs in ts-pmo.
> D) Start learning a new framework I've been curious about."
> Status: **possible** (all four)

## Read — ranked, highest leverage first

Ordered strictly by the key — tier, then Substance sum, then Signal count:

| # | Candidate | Tier | Substance / Signal | Why |
|---|-----------|------|--------------------|-----|
| 1 | **B — build the leverage tool** | **Post** | 6 / 3 · sweet-spot ✓ | Frontier AI use, self-started, names a real design tradeoff, future-state. |
| 2 | A — tradeoffs thread | Post | 4 / 3 | Pure legibility play: surfaces senior judgment on work you already shipped. Near-zero cost. |
| 3 | C — fix bugs | Raise | 4 / 1 | Real value, invisible. Leverage only if you post the *why* behind a fix. |
| 4 | D — new framework | Skip | 2 / 0 | Low latent value, no signal *yet*. Fine to learn for yourself — just don't center a post on it. |

B and A are both Post; **B outranks A on the key** — equal Signal (3), higher
Substance (6 vs 4), and sweet-spot breaks any remaining tie. The ordering is
mechanical, not a vibe.

## Recommended pick

**Do B next** — it's the rank-1 row: Post on both gates, top Substance, in your
sweet-spot lane. *Supporting (not deciding):* it also rides the ts-pmo momentum —
"I shipped a task manager, then built the lens that finds leverage in the work it
tracks" is a strong arc. Bank A as a same-day, near-free follow-up while the
audience is warm.

## Notes

- D scoring **Skip** is not a judgment on learning the framework — the honesty
  clause applies: do it for yourself, just don't center a post on it.
- This ranking reads off `rubric.yaml`. Edit the rubric and the order can change —
  that's the point.
