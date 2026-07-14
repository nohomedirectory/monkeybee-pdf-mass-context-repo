---
generated-by: root orchestrator (Codex harness)
date: 2026-07-14
inputs:
  - AGENTS.md
  - OVERNIGHT_GOAL.md
status: DRAFT
evidence-status: provisional-pending-substrate
---

# Orchestration State

## Global state

- Active subgoal: `G3`, with G1/G2/G4/G5 awaiting fresh reviews, G6 triggered by R19, and G7 integrating the first filed round
- Current phase: `G0 DONE; owner wave active; G2, G4, and G5 SUBMIT-FOR-REVIEW`
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
| G1 owner | Constitution v8, shell corpus, fix map | `constitution/**`, `shell/**`, `reports/FIX_APPLICATION.md`, `ledger/owners/G1_STATE.md` | SUBMIT-FOR-REVIEW | 554 headings preserved, 17 OPEN-C0 rows mapped, 40 pending slots, root structural gate passed | Fresh R13-R18 packets, then REVISE |
| G2 owner | resolve-now and deferred decisions | `decisions/**`, `ledger/owners/G2_STATE.md` | SUBMIT-FOR-REVIEW | Nine artifacts and owner self-check persisted at 16:56; root integrity gate passed | Fresh R27/R28 packets, then REVISE |
| G3 owner | Cycle 1 delta plan | `plans/CYCLE_1_DELTA_PLAN.md`, `ledger/owners/G3_STATE.md` | DRAFT | Authority sections ingested; provenance-bearing partial plan exists | Plan reaches 2,500–4,000 substantive lines with all contract families, then SELF-CHECK |
| G4 owner | traceability matrix and C2-C7 briefs | `reports/TRACEABILITY_MATRIX.md`, `plans/cycle_briefs/**`, `ledger/owners/G4_STATE.md` | SUBMIT-FOR-REVIEW | Fifty requirements accounted bidirectionally; six briefs and root integrity check passed | Fresh R23-R26 packets, then REVISE |
| G5 owner | human-action packages | `human_actions/**`, `ledger/owners/G5_STATE.md` | SUBMIT-FOR-REVIEW | P1-P8, tracker, and index persisted; no-action/source checks passed | Fresh human-package evidence-boundary packet, then REVISE |
| G6 owner | conditional charter successors | qualifying `*_v1.1.md` files and `ledger/owners/G6_STATE.md` only | INGEST | R19 filed seven Grade-A Charter-set defects; Sol/ultra owner spawned at 17:22 | Persist trigger/authority checkpoint, draft only affected successors, remain DRAFT through R20-R22 |
| G7 owner | gauntlet records and convergence | `gauntlet/**`, `ledger/owners/G7_STATE.md` | DRAFT | R01-R30 baseline and R31-R32 supplements initialized before any result; zero rounds filed | Admit R01 only after G3 submission hash is bound |
| G8 owner | integrity gate and morning handoff | `MORNING_REPORT.md`, final `INDEX.md`, ledger seal | INGEST | Terminal criteria imported from goal | G0-G7 dispositions are available |

## Reviewer finite-state machine

Every gauntlet instance is a fresh-context, single-shot machine:

`SPAWNED -> INGEST-DECLARED-CHAIN -> APPLY-ONE-LENS -> FILE-GRADED-FINDINGS -> TERMINATED`

It may write only its assigned finding packet. The G7 owner serially integrates packets into `gauntlet/ROUND_LOG.md`; the artifact owner triages and revises before the next round. Exact model identity, lens, count by grade, disposition, and termination are required ledger fields.

## Precommitted baseline gauntlet allocation

Model labels below are exact launch targets: `Sol` means `gpt-5.6-sol` at `max` or `ultra`; `Opus` means `claude-opus-4-8` at `xhigh`. A round may not silently fall back to another model.

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
