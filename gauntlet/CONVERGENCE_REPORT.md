---
generated-by: G7 gauntlet/convergence owner (NTM session `monkeybee-pdf-mass-context-repo--g7`, pane 1; `claude-opus-4-8`, effort `xhigh`)
date: 2026-07-14
inputs:
  - gauntlet/ROUND_LOG.md
  - OVERNIGHT_GOAL.md
  - ledger/prompts/GAUNTLET_REVIEWER_PROTOCOL.md
  - ledger/ORCHESTRATION_STATE.md
  - AGENTS.md
status: DRAFT
evidence-status: provisional-pending-substrate
owner-fsm: DRAFT
---

# Gauntlet Convergence Report

## What this report is, and what it may never do

It reports what the review gauntlet actually found, round by round, and whether the findings-per-round curve is falling. Its only source is filed evidence in `gauntlet/ROUND_LOG.md`.

It may never upgrade a claim. An artifact that survives every allocated round is an artifact no allocated round refuted; it is not an artifact shown to be correct, and it stays exactly as provisional as its own status line says. It may never report an unreviewed lens as covered, and it may never let a falling curve stand in for coverage: a curve can fall because the artifact improved, because the lenses stopped looking where the defects are, or because five processes from the same family share one blind spot. This report distinguishes those cases where the evidence allows and says so where it does not.

**Current state: two rounds filed (R19, R20), 30 allocated rounds unfiled.** Two data points under **two different lenses** are not a convergence curve. Nothing here yet establishes convergence, non-convergence, or a trend for any artifact, and neither round can speak to the lenses it did not apply.

## Findings per round

Filled from filed round entries only. Grades are the reviewer's, per the protocol's grade law: `A` confirmed defect with a cited local contradiction, omission, broken dependency, or violated rule; `B` probable defect with strong local evidence and one unresolved premise; `C` judgment call. Grades are never re-graded here to smooth a curve, and a suppressed Grade-A finding would defeat the entire instrument.

| Round | Artifact | Lens | Model | A | B | C | Marginal-only | Phase |
|---|---|---|---|---|---|---|---|---|
| R19 | Charter-set cross-consistency | envelope-dependency | `gpt-5.6-sol` (`ultra`) | 7 | 1 | 0 | NO | Structural (Charter set, round 1 of 4) |
| R20 | Charter-set cross-consistency | Q2/Q3 traceability | `claude-opus-4-8` (`xhigh`) | 8 | 2 | 0 | NO | Structural (Charter set, round 2 of 4) |

Totals by grade: **A=15; B=3; C=0**, across 2 filed rounds.

**Read this pair carefully, because the naive reading is wrong.** R19 and R20 applied **different lenses** to the **same unchanged bytes**. The move from 8 to 10 findings is therefore *not* a rising convergence curve and *not* evidence that the artifact is getting worse — nothing about the artifact changed between them, and nothing could have: the Charter set is read-only canon, its hash was identical for both rounds, and no repair was made in between. What the pair shows is that a second, different lens found a second, different class of defect in bytes the first lens had already read. That is what lens rotation is for.

A convergence curve requires **the same lens** applied to **successive revisions** of an artifact — the shape the five-pass blocks are built to produce. No such series exists yet in this run. Any later reading of "18 findings in two rounds" as a trend would be a misuse of this table, and it is flagged here rather than left available.

Both rounds are routed to G6 and **no G6 triage has returned**. Fifteen filed Grade-A findings are fifteen *claimed* defects, not fifteen adjudicated ones. If G6 returns `NOT-TRIGGERED` on any of them, this table keeps the filed grade and records the triage outcome beside it; the count is never retroactively lowered to make the review look cleaner than it was.

R19 is filed, validated against the reviewer protocol's schema by G7, and routed to G6 (conditional Charter-set successors). Its seven Grade-A and one Grade-B findings are the reviewer's grades, recorded as filed. G7 has not re-graded them, and no G6 triage has returned: **a filed Grade-A finding is a claimed defect, not yet an adjudicated one.** Should G6 return `NOT-TRIGGERED` on any finding, this table keeps the filed grade and records the triage outcome beside it rather than retroactively lowering the count — the gauntlet's own record is not edited to look cleaner than the review was.

Execution order is not round order: R19 filed first because its artifact is read-only canon and permanently eligible, while R01–R12 wait on the C1 delta plan reaching `SUBMIT-FOR-REVIEW`. Its phase is structural because phases are counted per artifact, and R19 is the Charter set's first round.

## Convergence curves by artifact

One curve per gauntleted artifact, reported honestly whether it falls, stalls, or rises. A rising curve late in an artifact's block is a signal about the artifact or about the revisions, not a reporting error to be smoothed.

| Artifact | Allocated rounds | Filed | Curve (A+B per round, in order) | Two consecutive marginal-only? | Converged? |
|---|---|---|---|---|---|
| C1 delta plan | 13 — 12 baseline (R01–R12) + 1 supplemental (R31) | 0 | — | No | Not established |
| Constitution + fix map | 6 (R13–R18) | 0 | — | No | Not established |
| Charter-set cross-consistency | 4 (R19–R22) | 2 | R19: 8 · R20: 10 (different lenses — not a convergence series) | No | Not established |
| Traceability + cycle briefs | 4 (R23–R26) | 0 | — | No | Not established |
| Decision briefs | 2 (R27–R28) | 0 | — | No | Not established |
| Whole repository | 2 (R29–R30) | 0 | — | No | Not established |
| `human_actions/**` | 1 — supplemental (R32) | 0 | — | No | Not established |

"Not established" is the honest default and stays until filed rounds say otherwise. It does not mean "not converged"; it means no evidence exists either way.

Supplemental rounds are counted in their artifact's curve and in the grade totals, and they are labeled supplemental wherever they appear so baseline coverage is never silently inflated by them. One rule constrains how they may be read: **a round applying a lens for the first time cannot, by itself, establish convergence for its artifact.** A single clean application of a single lens by a single process is the weakest evidence class this instrument recognizes, and the two-consecutive-marginal-only rule exists to detect an exhausted defect surface — not to be satisfied by a lens that has only just begun looking. This constraint is fixed here, before any round runs.

## Phase model

OVERNIGHT_GOAL §4 tracks convergence against the process guide's phase model. Phases are counted **per artifact**, over that artifact's own round sequence, not over the global round number — the C1 plan's first round is its structural round even though it is also the run's first round.

| Phase | Rounds within an artifact's sequence | What the phase expects to surface |
|---|---|---|
| Structural | 1–3 | Missing sections, broken envelopes, absent contracts, wrong shape |
| Architecture | 4–7 | Dependency and layering defects, feature loss, collapsed envelopes |
| Refinement | 8–12 | Local correctness, self-containment, security and DoS, normative facts |
| Polish | 13+ | Wording, claim vocabulary, de-slopification |

Only the C1 delta plan has enough allocated rounds (12) to traverse structural through refinement. The other artifacts' blocks are shorter than the model's span; their rounds are reported at the phase their position implies, and the report does not claim polish-phase confidence from a structural-phase budget.

## Convergence rule and reallocation policy

An artifact is treated as converged when it files **two consecutive marginal-only rounds**. `marginal-only` is precommitted in `gauntlet/ROUND_LOG.md` as *zero Grade-A and zero Grade-B findings in the round*; Grade-C judgment calls do not defeat it. The definition was fixed before any round ran, so the threshold cannot be tuned after the results are visible. It is G7's operationalization of a term OVERNIGHT_GOAL §4 left open, and it sits on the morning ratification queue.

On convergence, the artifact's remaining rounds reallocate to the C1 delta plan (OVERNIGHT_GOAL §4). Every reallocation is logged in the round log with the closed round IDs, the triggering evidence, and the new R31+ IDs. Convergence is never inferred from a quiet round, an owner's confidence, or a schedule.

## Cross-model accounting

The correlated-blind-spot limitation is the reason this is tracked at all: a gauntlet run entirely by one model family cannot see what that family cannot see, and the campaign's own risk register calls this the F-01 pattern — the whole ecology agreeing on a wrong certificate.

| Model | Baseline rounds (R01–R30) | Supplemental rounds (R31–R32) | Total allocated | Filed rounds |
|---|---|---|---|---|
| `gpt-5.6-sol` (`max`/`ultra`) | 15 | 1 (R31, `ultra`) | 16 | 1 (R19) |
| `claude-opus-4-8` (`xhigh`) | 15 | 1 (R32, `xhigh`) | 16 | 1 (R20) |

**Execution-condition change, 2026-07-14 17:39 (disclosed, not smoothed).** A live human control requires every Codex instance from that moment forward to run in **fast mode**. It is prospective and changes no terminated round: R19 (`gpt-5.6-sol`) ran and terminated before it, and R20 is not a Codex instance. But it means the `Sol` series is **not homogeneous across the run** — R19 ran under the pre-control condition, and every later Sol round (R01, R04, R06, R08, R10, R12, R13, R15, R17, R21, R23, R25, R27, R30, R31) runs under fast mode. Any comparison across Sol rounds therefore carries a mid-run condition change as a confound. This report names it rather than presenting the Sol series as a controlled sequence. It does not retroactively weaken R19; it means R19 is not a like-for-like control for what follows.

The baseline runs two model families in a 15/15 split, verified against the allocation at initialization. Root's two supplemental rounds preserve the balance at 16/16; neither model family reviews its own family's blind spots any more than it did before. This is a genuinely different model family for half the rounds, which is what the goal asks for and better than the single-family fallback it tells us to confess to. It is not independence: both families are large language models reviewing documents, both are subject to the shared-premise failure the re-audit catalogs, and neither is the different-model-family **plus human** red team the Charter's day-zero track requires. This report does not present the 15/15 split as adjudication, as external review, or as a substitute for the independence layer that remains unengaged.

Actual per-model filed counts are recorded here as rounds land. If any round falls back to a model other than its assignment, it is filed as `MODEL-MISMATCH`, no findings are admitted from it, and the mismatch appears in this table rather than being absorbed silently.

## Five-pass repeated-prompt blocks

Two blocks are designated, each repeating one byte-for-byte-identical prompt across five consecutive fresh processes under the `oversimplification-and-feature-loss` lens. The prompt is immutable and reproduced in `gauntlet/ROUND_LOG.md`. The technique's premise is that each pass finds what the last one missed, so the per-pass yield within a block is the interesting number — a block whose yield does not decay tells us something about the artifact or about the prompt, and either way it gets reported.

| Block | Artifact | Rounds | Models in order | Filed | Per-pass A+B yield |
|---|---|---|---|---|---|
| 5-pass A | C1 delta plan | R04–R08 | Sol, Opus, Sol, Opus, Sol | 0 | — |
| 5-pass B | Constitution + fix map | R14–R18 | Opus, Sol, Opus, Sol, Opus | 0 | — |

The model rotates within each block while the prompt is held fixed. That is a deliberate confound and is named here so no one later reads a decaying yield as pure repetition effect: within a block, a drop between passes may be repetition exhausting the artifact's defects, or it may be one family's blind spot landing on that pass. The blocks cannot separate these, and this report does not pretend they can.

## Lens coverage

Every lens OVERNIGHT_GOAL §4 names, and whether the precommitted baseline actually reviews it. An unallocated lens is unreviewed, and no amount of adjacent coverage changes that.

| Lens (OVERNIGHT_GOAL §4 rotation) | Allocated rounds | Coverage |
|---|---|---|
| envelope-dependency | R01, R19 | **R19 filed** (Charter set) · R01 allocated, unfiled (C1 plan) |
| identity-law consistency | R13 | Allocated |
| PDF-normative-fact check | R02 | Allocated |
| security/DoS | R11, R28 | Allocated |
| clean-room contamination scan | R03, R26, R29 | Allocated |
| self-containment | R09 | Allocated |
| dependency-soundness | R10, R24 | Allocated |
| duplication/drift | R21 | Allocated |
| claim-vocabulary legality | R12, R22, R30 | Allocated |
| Q2/Q3 traceability | R20, R23 | **R20 filed** (Charter set) · R23 allocated, unfiled (traceability matrix + briefs) |
| oversimplification hunt | R04–R08, R14–R18, R25 | Allocated |
| de-slopification | R12, R30 | Allocated |
| **kernel-touch audit** | **R31 (supplemental)** | **Allocated — was UNREVIEWED at initialization; closed by root authorization at 17:04, before any round filed** |

The kernel-touch gap was real, and it is now allocated rather than absorbed. The Charter makes kernel-touch risk #5, with a design target of zero touches from Cycle 2 onward and a version bump, migration plan, and claim-lapse review as the price of any touch; the §34.9 protocol requires each delta plan to declare `kernel-touch: none` or enumerate what it touches. The baseline allocation assigned the lens no round, G7 recorded that at initialization, and root authorized supplemental round R31 to cover it. The original gap is preserved in the record rather than edited away — the sequence matters, because the gap was found and closed before any result existed to shape it.

Root-authorized lenses outside the OVERNIGHT_GOAL §4 rotation are tracked separately, so that "the goal's lenses" and "lenses root added" never blur together:

| Lens (root-authorized, not in the §4 rotation) | Allocated rounds | Coverage |
|---|---|---|
| source-scope-and-no-action integrity | R32 (supplemental) | Allocated |

Allocated is not the same as covered. A lens becomes covered only when its round files an entry, and a lens whose round is later closed `NOT-RUN` or `REALLOCATED` returns to unreviewed. Both supplemental rounds are allocated and unfiled; at this moment the kernel-touch lens and the source-scope lens have each been applied exactly zero times.

Coverage is per artifact, not global. R19 applied the envelope-dependency lens to the **Charter set**; it says nothing about that lens over the C1 delta plan, which is R01's job and is still unfiled. One lens covering one artifact never generalizes to another artifact, however similar the reasoning looks.

## Artifact coverage

| Artifact | Baseline rounds | Supplemental rounds | Total |
|---|---|---|---|
| `plans/CYCLE_1_DELTA_PLAN.md` | 12 | 1 (R31) | 13 |
| `constitution/**`, `shell/**`, `reports/FIX_APPLICATION.md` | 6 | — | 6 |
| The four v1.0 Charter-set documents | 4 | — | 4 |
| `reports/TRACEABILITY_MATRIX.md`, `plans/cycle_briefs/**` | 4 | — | 4 |
| `decisions/**` | 2 | — | 2 |
| Whole repository | 2 | — | 2 |
| `human_actions/**` | 0 | 1 (R32) | 1 |

The human-action packages are the artifacts whose defects leave the repository — outreach text, licence and rights claims, a disclosure policy, corpus-acquisition steps. The baseline gave them no dedicated round; root's supplemental R32 gives them one, scheduled after the R01–R30 priority floor so the goal's priority ladder is respected rather than reshuffled. One round over ten packages is coverage, not saturation, and this report will describe it as exactly that.

The whole-repo rounds (R29–R30) may reach these files incidentally under their own lenses. Incidental contact is not a review, and this report will not count it as one.

## Limitations of this instrument

1. **Reviewers are model processes, not adjudicators.** They read documents in a fresh context under one lens. They do not execute code, and in this run there is no code to execute.
2. **No round is external.** Every reviewer runs inside this campaign's own ecology, on the human's machine, under root's orchestration. Nothing here is the independent review the Charter's day-zero track requires, and no gauntlet result may be presented as one.
3. **A clean round is weak evidence.** Absence of findings under one lens, from one process, in one context, is the weakest evidence class this campaign recognizes. It is recorded, and it is not promoted.
4. **The curve is not the artifact.** Convergence describes the review process, not the truth of what was reviewed. The campaign's own history is the argument: three fresh-eyes audit rounds converged, and the two Grade-A defects they surfaced were both duplication drift that earlier rounds had walked past.
5. **This report is provisional.** Like every artifact in this run, it is `provisional-pending-substrate` until the tamper-evident commitment channel exists. It is not itself evidence of anything until it is committed through that channel.
