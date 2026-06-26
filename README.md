# leverage-filter

A lens that tells you how much **visibility leverage** a piece of work carries —
how much it's worth *sharing*, not whether it's worth *doing* — and what to do
about it.

It is two things at once: an **opinion** of what gives work leverage
([`rubric.yaml`](rubric.yaml)), and the **machine that applies any opinion**
([`SKILL.md`](SKILL.md)). The opinion is mine and it's a starting point; edit the
rubric and it becomes yours.

## Install

This is a Claude **skill** — a folder with a `SKILL.md` the agent loads.

1. Copy this folder into your skills directory:
   - **Claude Code:** `~/.claude/skills/leverage-filter/` (or your project's `.claude/skills/`).
   - **Claude desktop / web:** add it via Settings → Customize → Skills (zip the folder, or package it as a `.skill` bundle).
2. In a session where the skill is available, invoke it by intent — e.g.
   *"check the leverage on this: &lt;paste work&gt;"* or *"rank these by leverage: &lt;list&gt;"*.

It reads `rubric.yaml` and `examples/` from this folder, so keep them next to
`SKILL.md`. No build step, no dependencies, nothing to configure.

## Why it exists

A task manager (e.g. [ts-pmo](https://github.com/chzylee/ts-pmo)) governs the
**doing** — what serves your goals. This governs the **showing** — what's worth
making part of your public narrative. Different axes: work can be worth doing and
not worth sharing (a slow personal product), or vice versa. You're doing plenty;
you want a sharp read on which of it is worth putting eyes on, so you spend a
limited visibility budget where it compounds — and never mistake "low leverage to
share" for "not worth doing."

## What it does

You hand it work (current / upcoming / possible). It returns:

1. **How much leverage** — a tier (Skip / Raise / Borderline / Post), not a fake
   number.
2. **How to get more** — the single thing holding it back.
3. **What to do** — raise it, reframe it, post it as-is, or skip the post.

Two modes:
- **Rank** (the headline) — give it several candidate next-moves, get a ranked
  shortlist with one recommended pick. This is the part that beats snap judgment.
- **Appraise** — score one item you're about to start or already working on.

It informs and gets out of the way. It does not nag, track follow-through, or
log outcomes. The honest read is the whole product.

## Layout

| File | What it is |
|---|---|
| [`SKILL.md`](SKILL.md) | The behavior: modes, scoring, output contract. |
| [`rubric.yaml`](rubric.yaml) | The opinion — the visibility-leverage rubric, yours to edit. |
| [`examples/`](examples/) | One worked reference per usage. The behavior spec. |
| [`refine.md`](refine.md) | How to re-ground the rubric — rarely, on purpose. |

## Make it yours

The rubric ships as *an opinion* — mine. Its axis is fixed (how work lands when
shared), but the specific tests and weights are a starting point. Edit
[`rubric.yaml`](rubric.yaml) to match your lane — here are the exact knobs:

- **Substance** (`gate_1_substance`) — rewrite the three tests/scales for what
  carries real value *in your field*.
- **Signal** (`gate_2_signal`) — swap the four dimensions for what *your*
  audience actually rewards.
- **Thresholds** — the Skip-below-4 cutoff and the tier table live in
  [`SKILL.md`](SKILL.md) under *Scoring*; move the cutoffs there.

Keep it on the visibility axis — leverage here is what's worth *sharing*, not
your private goals. And refine **infrequently** — see [`refine.md`](refine.md)
for why over-tuning hurts.
