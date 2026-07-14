---
generated-by: root orchestrator (Codex harness)
date: 2026-07-14
inputs:
  - AGENTS.md
  - OVERNIGHT_GOAL.md
status: DRAFT
evidence-status: provisional-pending-substrate
updated-at: 2026-07-14T23:39:10+02:00
timestamp-correction: the initially written literal 2026-07-14T19:26:00+02:00 was a future, unmeasured value and is preserved here as invalid; the exact update second is not inferred
---

# Orchestration State

## Global state

- Active subgoal: `G3` gauntlet. R15 is mechanically integrated and routed unpromoted to G1; R24 alone is bound and unsent against pushed G4 manifest `22749762…02c6`. Root is sealing the G7/control commit before parallel R24 reviewer and G1 owner dispatch. G3 continues its independent R05 revision.
- Current phase: `G0/G6 DONE; G1 SUBMIT-FOR-REVIEW / R15 owner route ready; G2/G5 SUBMIT-FOR-REVIEW with exact Sol ultra/fast replacement panes pre-staged; G3 REVISE on committed R05 packet; G4 SUBMIT-FOR-REVIEW / R24 bound-unsent at 22749762…02c6; continuing G7 DRAFT / log closed at corrective EOF; 13 filed rounds at A=93/B=56/C=18 with 7 Sol/6 Opus; G8 INGEST with a live exact-model owner and disk checkpoint`
- Priority rule: preserve G0, ledger, G3, G3 gauntlet, G1, and `MORNING_REPORT.md`; shed work only from the bottom of the governing ladder.
- Canonical-input mutation allowance: none.
- Bead/code allowance: none.
- External human-bound actions: drafts only.
- Review artifacts: findings only; reviewers never edit owner artifacts.

## Owner finite-state machines

Each owner must persist a checkpoint below and in its partial output at every transition:

`INGEST -> DRAFT -> SELF-CHECK -> SUBMIT-FOR-REVIEW -> REVISE -> DONE`

| Owner | Scope | Files owned | State | Last checkpoint | Next transition condition |
|---|---|---|---|---|---|
| G0 owner | orientation, inventory, Grade-A verification | `INDEX.md`, `reports/INGEST_REPORT.md`, `ledger/owners/G0_STATE.md`, permitted AGENTS extension | DONE | All five fresh-review findings resolved; closure suite and root verification passed | None; terminate owner process |
| G1 owner | Constitution v8, shell corpus, fix map | `constitution/**`, `shell/**`, `reports/FIX_APPLICATION.md`, `ledger/owners/G1_STATE.md` | SUBMIT-FOR-REVIEW | R15 filed 14 Grade-A and 7 Grade-B allegations at manifest `dd5266aa…d8e9`; the packet is schema-valid, process-qualified for two disclosed non-evidentiary chain-scope slips, and reviewer/session termination is verified | After G7 integration, receive the bounded unpromoted R15 packet, persist `SUBMIT-FOR-REVIEW -> REVISE`, premise-test all 21 items, and resubmit before R16 |
| G2 owner | resolve-now and deferred decisions | `decisions/**`, `ledger/owners/G2_STATE.md` | SUBMIT-FOR-REVIEW | Nine artifacts and owner self-check persisted at 16:56; root integrity gate passed. Fresh `g2b` is preattested exact Sol ultra/fast with no task/context | Fresh R27/R28 packets, then REVISE |
| G3 owner | Cycle 1 delta plan | `plans/CYCLE_1_DELTA_PLAN.md`, `ledger/owners/G3_STATE.md` | REVISE | `g3b` reproduced the exact committed R05 byte suffix, persisted receipt plus `SUBMIT-FOR-REVIEW -> REVISE`, survived a context compaction with immediate and root-prompted `AGENTS.md` rereads, and keeps all 41 grades unpromoted | Premise-test every item, persist dispositions and bounded repairs, restart the full suite after any self-check repair, and resubmit before R06 |
| G4 owner | traceability matrix and C2-C7 briefs | `reports/TRACEABILITY_MATRIX.md`, `plans/cycle_briefs/**`, `ledger/owners/G4_STATE.md` | SUBMIT-FOR-REVIEW | Replacement premise-tested all six R33 allegations, ran four explicit self-check restart cycles, reproduced the seven-file manifest `22749762…02c6`, and stopped idle; commit `a5c9c29` is pushed | Bind R24 after the current serialized R15 review/revision gate releases the Round Log |
| G5 owner | human-action packages | `human_actions/**`, `ledger/owners/G5_STATE.md` | SUBMIT-FOR-REVIEW | P1-P8, tracker, and index persisted; no-action/source checks passed. Fresh `g5b` is preattested exact Sol ultra/fast with no task/context | Fresh R32 source-scope/no-action packet, then REVISE |
| G6 owner | conditional charter successors | qualifying `*_v1.1.md` files and `ledger/owners/G6_STATE.md` only | DONE | R19–R22 incorporated; root review repair applied; four successors remain PROPOSED; exact 83-row §35 schedule and v1.0 hashes preserved; commit `03285ba` pushed | None; owner process terminated normally |
| Continuing G7 owner | gauntlet records and convergence | `gauntlet/**`, `ledger/owners/G7_STATE.md` | DRAFT | R15 integrated at A=14/B=7/C=0; aggregate A=93/B=56/C=18 across 7 Sol/6 Opus. R24 alone is `ASSIGNED` to manifest `22749762…02c6`; a non-unique-anchor placement defect is disclosed and a corrective control record closes the true EOF | Hold the log closed while root commits/pushes and dispatches R24; later integrate only R24 after verified reviewer termination |
| G8 owner | integrity gate and morning handoff | `MORNING_REPORT.md`, `ledger/owners/G8_STATE.md` only; root retains final `INDEX.md` and ledger seal | INGEST | Session `g8` attested `gpt-5.6-sol`/`ultra`/live `fast`; first disk checkpoint SHA-256 `be635034…f94e2`; every terminal input marked expected-not-yet-terminal; `MORNING_REPORT.md` absent by design | Root supplies the bounded terminal evidence packet after all reviews/revisions; G8 rereads `AGENTS.md`, enters `DRAFT`, and writes the nine-part report |

## Reviewer finite-state machine

Every gauntlet instance is a fresh-context, single-shot machine:

`SPAWNED -> INGEST-DECLARED-CHAIN -> APPLY-ONE-LENS -> FILE-GRADED-FINDINGS -> TERMINATED`

It may write only its assigned finding packet. The G7 owner serially integrates packets into `gauntlet/ROUND_LOG.md`; the artifact owner triages and revises before the next round. Exact model identity, lens, count by grade, disposition, and termination are required ledger fields.

## Precommitted baseline gauntlet allocation

Model labels below are exact launch targets: `Sol` means `gpt-5.6-sol` at `max` or `ultra`; for every Codex process spawned after the human's 17:39 instruction it additionally requires `/fast`, service tier `priority`, verified in the live TUI before assignment. `Opus` means `claude-opus-4-8` at `xhigh`. A round may not silently fall back to another model or mode.

| Rounds | Artifact | Declared lens | Model sequence |
|---|---|---|---|
| 01 | C1 delta plan | envelope-dependency | Sol |
| 02 | C1 delta plan | PDF-normative-fact | Opus |
| 03 | C1 delta plan | clean-room contamination | Opus |
| 04–08 | C1 delta plan | exact repeated blunder/oversimplification hunt; preserve features | Sol, Opus, Sol, Opus, Sol |
| 09 | C1 delta plan | obscure-section self-containment | Opus |
| 10 | C1 delta plan | dependency soundness | Sol |
| 11 | C1 delta plan | security/DoS | Opus |
| 12 | C1 delta plan | claim vocabulary and de-slopification | Sol |
| 13 | Constitution + fix map | identity-law consistency | Sol |
| 14–18 | Constitution + fix map | exact repeated blunder/oversimplification hunt; preserve features | Opus, Sol, Opus, Sol, Opus |
| 19 | Charter-set cross-consistency | envelope-dependency | Sol |
| 20 | Charter-set cross-consistency | Q2/Q3 traceability | Opus |
| 21 | Charter-set cross-consistency | duplication/drift | Sol |
| 22 | Charter-set cross-consistency | claim-vocabulary legality | Opus |
| 23 | traceability + cycle briefs | Q2/Q3 zero-orphan audit | Sol |
| 24 | traceability + cycle briefs | dependency soundness | Opus |
| 25 | traceability + cycle briefs | oversimplification hunt | Sol |
| 26 | traceability + cycle briefs | clean-room contamination | Opus |
| 27 | decision briefs | reversibility and dependency blast radius | Sol |
| 28 | decision briefs | security/DoS | Opus |
| 29 | whole repository | clean-room contamination | Opus |
| 30 | whole repository | coherence and de-slopification | Sol |

Baseline cross-model count: 15 Opus rounds. Rounds 02, 03, 11, 26, and 29 directly weight the PDF-normative, security, and clean-room lenses requested by the human. Extra five-pass blocks may be added for traceability, decisions, and human-action packages only after the priority floor is safe.

## Root-authorized supplemental rounds

These close two pre-result coverage gaps without renumbering or weakening the R01-R30 baseline.

| Round | Artifact | Declared lens | Exact model | Placement |
|---|---|---|---|---|
| R31 | C1 delta plan | kernel-touch audit | `gpt-5.6-sol`, effort `ultra` | Immediately after R12 and its owner disposition |
| R32 | `human_actions/**` | source-scope-and-no-action integrity | `claude-opus-4-8`, effort `xhigh` | After the R01-R30 priority floor |

Total planned rounds: 32. Planned cross-model count: 16 Opus, 16 Sol. These are supplemental single-lens rounds, not substitutes for any baseline round.

## Stop conditions

The run reaches `DONE` only after the wake-up test passes, required artifacts and gauntlet records exist, integrity scans have dispositions, the ledger is sealed provisionally, `MORNING_REPORT.md` names every ratification and omission, changes are committed and pushed, and `git status --short` is empty on `main`.
