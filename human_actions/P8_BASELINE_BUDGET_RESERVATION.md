---
generated-by: Claude G5 owner (claude-opus-4-8)
date: 2026-07-14
inputs:
  - MONKEYBEE_CAMPAIGN_CHARTER_v1.md §8 (risk 1), §2 (degradation law), §7
  - CYCLE_0_WORK_ORDER.md §5.8
  - MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md §33.5, §33.5.1, §33.6, §33.8, §33.17, §33.18
status: DRAFT
evidence-status: provisional-pending-substrate
package-id: P8
human-bound: yes
execution-status: NOT EXECUTED — no budget committed, nothing purchased, no compute reserved
---

# P8 — Baseline budget reservation

## What this is

A decision package for the campaign's most expensive, least enjoyable, and most quietly skippable line item: **funding the equal-resource baselines** (A–D, plus E where feasible) that are the *only* source of disproportion evidence for Q3.

Charter §8 ranks this **risk #1**, and states the trap precisely: skipping the baselines silently **selects FrankenSim's outcome**, because without them there is zero disproportion evidence — no matter how good the artifact is.

## Why a human must do this

Money. An agent cannot reserve a budget, cannot buy compute, and cannot hire an expert for Baseline E. More to the point, an agent cannot make the trade-off this package exists to force: **is the Q3 verdict worth funding several full rebuild attempts that will, by design, produce nothing shippable?**

That question deserves a clear-eyed answer at day 0, when it is cheap to answer honestly, rather than at day 8, when the money is spent and the honest answer has become inconvenient.

## The trap, stated before the numbers

Baselines are the experiment that costs the most and shows the least. Every other line item produces something you can hold: a wedge, a renderer, a corpus. Baselines produce *a control group* — several deliberately unassisted rebuild attempts, at equal resources, whose entire output is a number that makes the main result mean something.

Cutting them is the single easiest decision in the campaign to defend in the moment ("we can add them later"; "the artifact speaks for itself"). It is also the decision that converts the campaign's central claim into an unfalsifiable assertion. **The artifact never speaks for itself. That is the whole finding of the FrankenSim re-audit sitting in this repository.**

Hence the Charter's rule, which this package operationalizes: **a baseline cut is a formal downgrade of G2, recorded and published as such — never a quiet omission.**

## The sizing problem nobody can precommit their way around

Rev 7 §33.5.1 requires **equal resources**: the same task statement, source pack, model/tool access, compute, elapsed feedback, human attention, attempt/branch budget, and stopping rule — everything except the mechanism under study. Both **nominal and consumed** resources get reported.

That has a consequence for budgeting which is easy to miss and expensive to discover late:

> **The baseline budget cannot be fixed in absolute terms on day 0, because it is defined relative to what MonkeyBee itself consumes — and that number is not known until MonkeyBee is built.**

So a fixed cap is not a budget; it is a bet that the campaign will stay small. If MonkeyBee consumes more than the cap allows the baselines to match, then the baselines are *under-resourced*, and an under-resourced baseline is **worse than no baseline**: it manufactures a favourable comparison out of an unfair one, and §33.5.1 forbids exactly that ("no condition receives... a weaker task").

**Reserve a formula, plus a cap, plus a rule for what happens when they collide:**

- **Formula:** `baseline_budget ≥ k × (MonkeyBee's consumed resources)`, where `k` is the number of baselines actually run at equal resource. For A–D, `k = 4`. With E, add the expert's bounded time.
- **Cap:** `[AMOUNT — the human's number]`.
- **Collision rule, precommitted:** if the cap cannot fund `k` baselines at *equal* resource, the project does **not** run cheap baselines and call them baselines. It either (a) runs **fewer** baselines at full equal resource, and records which mechanisms therefore have no control; or (b) declares the resource asymmetry explicitly and runs the sensitivity analysis §33.5.1 requires for unavoidable asymmetry. **What it never does is quietly under-fund a control and report the resulting margin as evidence.**

This rule is the entire reason to write it down at day 0.

## What each baseline costs, in kind

| Baseline | What must be bought | Rough shape of the cost |
|---|---|---|
| **A** — Direct frontier agents | A full rebuild attempt: same models, tools, compute, source pack, human attention — **without** MonkeyBee's contracts, Honeycomb, memory, or assurance architecture | ≈ one campaign's compute + a meaningful slice of human attention |
| **B** — Strong conventional plan + agents | A second full attempt, with a good ordinary architecture and process | ≈ one campaign, plus the planning effort a competent team would spend |
| **C** — Same repo without foundry memory | A rerun of selected tasks with tombstone/session retrieval replaced by the strongest ordinary documentation/search alternative | Task-scoped, not whole-campaign — cheaper, but only if scoped honestly |
| **D** — Same repo without independent oracles | Selected tasks with independent falsifiers replaced by ordinary self-testing/review; **the assurance loss is measured and reported**, not treated as a release failure | Task-scoped |
| **E** — Expert human comparison | Bounded expert implementation, review, or defensible project-history evidence | Expert hours at market rate; "where feasible" is doing real work in that sentence |

**C and D are repository-level; the §33.6 ablations are mechanism-level. One experiment may not be counted as both** (audit finding R2-N5). Budget them separately or you will be tempted, later, to count them twice — which is precisely the double-counting the finding names.

## Exact steps

1. **Answer the question honestly** (30 min): is the Q3 verdict worth `k ×` the campaign's cost? A defensible "no" is *far* better than an undefended "yes" that quietly becomes a cut in week two.
2. **If yes:** reserve the budget as a **committed line item** — formula, cap, and collision rule — and commit it through the substrate (P3) with the day-0 batch. Precommitment is what makes a later cut visible.
3. **If no, or if uncertain:** say so now, in the ledger, and **downgrade G2 formally at day 0.** The campaign then proceeds as G1 plus an artifact-substance claim, which is a real and defensible outcome (§33.18: a foundry win cannot substitute for a functioning artifact — and the converse holds too: the absence of foundry evidence does not erase a functioning artifact). What it must never do is proceed as though the baselines are coming, and then discover at day 8 that they are not.
4. **Set the tracking discipline** (15 min): the production ledger records **nominal and consumed** resources for MonkeyBee from day 0 (P3). Without that record, the equal-resource requirement cannot be met even with unlimited money, because nobody will know what "equal" was.
5. **Record the decision** as a §34.5-style row: question, options, decision, rationale, date.

## Expected time

1–2 hours. It is a decision, not a purchase — and its cost is decided by how honestly it is made, not by how long it takes.

## Evidence returned to the repo

The committed budget line (formula, cap, collision rule), its commitment proof, and its ledger row. If the answer is no: the recorded G2 downgrade, its date, and the claim tiers that consequently cap.

## Failure and downgrade path

| Failure | Consequence |
|---|---|
| Baselines cut silently | **The failure this package exists to prevent.** Q3's "production disproportion" row (Charter §7) has no evidence, and the campaign's central claim becomes unfalsifiable — while everyone continues to believe it is supported |
| Baselines cut formally | G2 downgraded, recorded, published. **Foundry claims are not made at any rung** (P4, DC-2 §1). The artifact claim survives on its own evidence, which is exactly what §33.18 says it may do |
| Baselines under-resourced | Worse than cutting them: an unfair comparison that produces a favourable number. §33.5.1 forbids it |
| Baselines run, MonkeyBee loses | **A legitimate, publishable result** — §33.17's kill criterion: the production-law claim simply failed, and the artifact can still be excellent, or even an artifact-alien candidate. Publish it. A campaign that cannot report this outcome was never running an experiment |

The last row is the one worth reading twice. If there is no budget under which MonkeyBee could *lose*, there is no experiment — only an expensive way to agree with oneself.

## Open items requiring human verification

| Item | Status | Verification step |
|---|---|---|
| The cap | `[AMOUNT]` — not set by any agent | Human's decision |
| Whether Baseline E is feasible | Rev 7 says "where feasible"; feasibility is a budget-and-people question | Human, with P1 |
| MonkeyBee's own consumed resources | Unknown until it runs; **the ledger must capture them from day 0** | P3's ledger opening — without it, equal-resource baselines are impossible regardless of budget |
