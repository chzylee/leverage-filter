---
name: leverage-filter
description: >-
  Rate how much *visibility leverage* a piece of work carries — how much it's
  worth sharing publicly, not whether it's worth doing. Triggers on
  "check the leverage on this", "is this worth doing/posting", "what's my
  highest-leverage next move", "rank these by leverage", "how do I get more
  leverage out of what I'm doing". Takes current / upcoming / possible work,
  scores it against an external-criteria rubric, names the one thing holding it
  back, and hands you a move (raise / reframe / post-as-is / skip). Informs and
  gets out of the way — it does not track whether you follow through.
---

# leverage-filter

A lens for one question: **is this worth sharing?**

Leverage here means **visibility leverage** — the payoff from making a piece of
work part of your public narrative (posts, build-in-public, conversation). It is
NOT a judgment of whether the work is worth *doing*. Those are different axes:

- A task manager (e.g. ts-pmo) governs the **doing** — what serves your goals.
- This governs the **showing** — what's worth putting eyes on.

A thing can be deeply worth doing and low-leverage to share (a slow personal
product), or modest to do and high-leverage to share (a sharp small pattern). The
filter speaks only to the second axis.

**A low score never means "don't do it."** It means "don't center your public
narrative here." Keep doing what serves you — just spend a limited visibility
budget where it compounds.

You hand it work. It tells you three things, in order:
1. **How much visibility leverage** it carries (a tier, not a fake number).
2. **How to get more** (the single thing holding it back).
3. **What to do about sharing it** (raise / reframe / post-as-is / don't center).

It is a filter, not a manager. It gives an honest read and gets out of the way.
It does not nag, score your follow-through, or track outcomes over time.

---

## Two modes

### Rank — the headline. "What's my highest-leverage next move?"
Use when you have several candidate things you *could* do next and want the one
worth doing. This is the mode that beats snap judgment — nobody can hold 5
candidates against the rubric in their head at once.

- **Input:** a list of candidate work (you enumerate them, or paste a batch of
  current/upcoming items from wherever they live).
- **Process:** appraise each against the rubric (below).
- **Order (use this exact key — don't improvise):**
  1. By **tier**: Post > Borderline > Raise > Skip.
  2. Within a tier, by **Substance sum** (higher first).
  3. Still tied, by **Signal count** (higher first).
  4. Still tied, **sweet-spot** wins; then **cheapest lift** (least effort to act).
- **Output:** a ranked shortlist, highest leverage first, with **one recommended
  pick and a single line: "do this next, because ___."** The recommended pick is
  the rank-1 row. A momentum/timing reason may be *named* as support, but it does
  not override the key — if you ever promote a lower row, state the reason
  explicitly and own that you're overriding rank. A ranking with a call, not N
  readouts to diff in your head.

### Appraise — "how much leverage does this one thing have?"
Use to check a single item: something you're **about to start** (is it worth it?),
or something **in progress** (what leverage can I pull out of it?).

- **Input:** one piece of work, described in a sentence or two, with its status
  (current / upcoming / possible).
- **Output:** the tier + the binding-constraint line + a move. (See Output
  contract.)

If the user hasn't said which mode, infer from the input: one thing → Appraise;
several → Rank.

**Thin input:** if status or a key fact is missing, ask one clarifying question,
or score on explicit assumptions and flag them in the read. Never emit a confident
tier from a vague paste without surfacing what you assumed.

---

## Scoring: sequential gates → a tier (never a summed number)

Do **not** produce a blended "X out of 10." The rubric is two different kinds of
measurement and summing them is false precision. Run the gates in order.

**What the two gates measure — keep them on their own axes:**
- **Substance** = *is there something worth seeing here?* Would an audience find
  real value in work like this — not "is it useful to me" (that's the doing axis,
  your manager's job).
- **Signal** = *is it made visible?* Is that substance surfaced in a way the
  world's eye actually rewards.
- Visibility leverage needs both: real substance, made legible. High substance +
  zero legibility = Raise; loud about nothing won't pass Substance.

**Gate 1 — Substance** (is there latent external value at all?). Score each 0–2,
sum 0–6:
- `pain_density`, `frequency`, `leverage` (see rubric.yaml for the tests).
- `leverage` is the **gate-flipping** dimension — alone it can move a 3 to a 4
  and flip Skip→Raise. When unsure, score it **down**; only score 2 with concrete
  reason to believe many would adopt.
- **If sum < 4 → STOP.** Tier = **Skip**. Output why, and the honest option.

**Gate 2 — Signal** (is the latent value made legible?). Only if Substance
passed. Count how many of the four are **surfaced in the work as described** (0–4):
- `frontier_tool_use`, `self_starting`, `named_tradeoff`, `future_state`.
- **Latent ≠ counted.** A quality that exists but isn't shown — e.g. a tradeoff
  you made but never articulated — does **not** count. Don't tally it; name it as
  the cheapest lift in the binding-constraint line.

**Sweet-spot check:** if it's schlep-automation or gives clean form to
unstructured data/process, note it. It **tips Borderline → Post** (inherently
high-leverage work, once it's already legible, is worth shipping) and breaks
within-tier ties in Rank. It does **not** rescue a Raise or a Skip — invisible
work stays invisible regardless of category.

**Tier mapping** (apply the sweet-spot tip *after* reading the table):
| Condition | Tier | Meaning |
|---|---|---|
| Substance < 4 | **Skip** | Low share-leverage. Skip the post — don't center your narrative here. Keep doing it if it serves you; post only for fun, tone-shifted. |
| Substance ≥ 4, Signal ≤ 1 | **Raise** | Real substance, invisible. Surface it before you share — make it seen. |
| Substance ≥ 4, Signal = 2 | **Borderline** | Shareable with a lift. Cheapest lift decides it — sweet-spot tips it to Post. |
| Substance ≥ 4, Signal ≥ 3 | **Post** | High share-leverage. Make it a centerpiece — ship it and show it. |

---

## Output contract

Every read returns, tersely:

1. **Tier** + the vector behind it, e.g. `RAISE · Substance 5/6 · Signal 1/4 · sweet-spot: yes`.
2. **The binding constraint — mandatory, one line.** Name the single dimension
   that is load-bearing right now. Not "improve the signal" — *"Substance is
   strong but Signal is 1/4: it's competent and invisible. The fastest lift is
   naming the tradeoff you made and what it bought."*
3. **The move**, drawn from the tier:
   - **Skip** → skip the post; keep doing it if it serves you, or post-as-fun with
     a shifted, honest tone (low share-leverage is valid information, not a failure).
   - **Raise** → the specific missing Signal dimension to add, concretely.
   - **Borderline** → the cheapest single lift that tips it to Post.
   - **Post** → ship it; apply *show-don't-tell* (prove the trait through what you
     did — delete the self-describing adjectives).

Keep the whole thing skimmable. The read is the deliverable; don't pad it.

---

## The rubric

Lives in [`rubric.yaml`](rubric.yaml). It is **an opinion, and it is yours to
edit** — but its *axis* is fixed: every criterion is about how work lands when
shared, not whether it serves your private goals. When you refine it, keep that
axis. Edit the file directly; the skill reads whatever is there.

Worked references for each usage are in [`examples/`](examples/) — read them as
the behavior spec.

---

## Refreshing the rubric (rarely, and on purpose)

The rubric is grounded in external reception, so it can drift as the world moves.
[`refine.md`](refine.md) is how you re-ground it — **but do it infrequently.**
Over-verifying is counterproductive: re-tuning against last week's feed overfits
to noise and erodes a standard that was sound. Trust the rubric between
refreshes. Refine when *you* sense real drift, not on a schedule.

---

## Honesty

- A low score is information, not a verdict on you. Say it plainly.
- "Post it anyway, for fun, with a shifted tone" is a real, valid output.
- The filter informs; you decide. It does not care whether you take the advice,
  and it never tracks whether you did.
