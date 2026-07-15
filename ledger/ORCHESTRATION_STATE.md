---
generated-by: root orchestrator (Codex harness)
date: 2026-07-14
inputs:
  - AGENTS.md
  - OVERNIGHT_GOAL.md
status: DRAFT
evidence-status: provisional-pending-substrate
updated-at: 2026-07-15T09:15:30+02:00
timestamp-correction: the initially written literal 2026-07-14T19:26:00+02:00 was a future, unmeasured value and is preserved here as invalid; the exact update second is not inferred
---

# Orchestration State

## Global state

- Active subgoal: G7 integration of the pushed G3 R48 owner disposition and binding of untouched R08. G1, G2, G3, G4, and G5 remain at `SUBMIT-FOR-REVIEW` after bounded owner gates; R08 remains unbound and undispatched until G7 seals the control and root commits, pushes, and revalidates it.
- Current phase: `G0/G6 DONE; G1 SUBMIT-FOR-REVIEW after R15; G2/G5 SUBMIT-FOR-REVIEW with exact Sol ultra/fast owner panes retained; G3 SUBMIT-FOR-REVIEW after pushed R48 accept=2/narrow=2 repairs and full credited gate; G4 SUBMIT-FOR-REVIEW after bounded R38 repairs; G7 DRAFT / R08-BIND-PENDING from AWAITING-OWNER-DISPOSITION; G8 INGEST with a live exact-model owner and disk checkpoint`
- Priority rule: preserve G0, ledger, G3, G3 gauntlet, G1, and `MORNING_REPORT.md`; shed work only from the bottom of the governing ladder.
- Canonical-input mutation allowance: none.
- Bead/code allowance: none.
- External human-bound actions: drafts only.
- Review artifacts: findings only; reviewers never edit owner artifacts.
- Live NTM retention census: 23 intentional MonkeyBee sessions, comprising seven owner/control panes plus sixteen still-needed reviewer panes; 15 Codex and eight Claude; zero dead panes, missing model children, cwd mismatches, or host zombies at `2026-07-15T09:12:00+02:00`. Every retained Codex is exact `gpt-5.6-sol` / `ultra` with live `fast`; every retained Claude is exact Opus 4.8/xhigh. The separate live `agents` root-orchestrator pane is not one of the 23 named NTM sessions. No retained session was removed.
- R48 route checkpoint: valid Opus/xhigh R48 is filed `CHAIN-QUALIFIED` at A=0/B=1/C=3; G3 independently dispositioned it accept=2/narrow=2/reject=0 and returned the repaired plan to `SUBMIT-FOR-REVIEW`. Commit `b38aa4db7374227f741efaf4ecaf0e0a7d495c4b` is pushed and is the fixed control base for the R08 bind.

## Owner finite-state machines

Each owner must persist a checkpoint below and in its partial output at every transition:

`INGEST -> DRAFT -> SELF-CHECK -> SUBMIT-FOR-REVIEW -> REVISE -> DONE`

| Owner | Scope | Files owned | State | Last checkpoint | Next transition condition |
|---|---|---|---|---|---|
| G0 owner | orientation, inventory, Grade-A verification | `INDEX.md`, `reports/INGEST_REPORT.md`, `ledger/owners/G0_STATE.md`, permitted AGENTS extension | DONE | All five fresh-review findings resolved; closure suite and root verification passed | None; terminate owner process |
| G1 owner | Constitution v8, shell corpus, fix map | `constitution/**`, `shell/**`, `reports/FIX_APPLICATION.md`, `ledger/owners/G1_STATE.md` | SUBMIT-FOR-REVIEW | Root handoff snapshot repair passed; three substantive artifacts remain frozen, report is `06faddd7…2f602`, four-artifact manifest `24327520…60292`, state `48951eb4…b408` | Root commits the bounded owner group; R16 then becomes eligible after higher-priority G3 routing |
| G2 owner | resolve-now and deferred decisions | `decisions/**`, `ledger/owners/G2_STATE.md` | SUBMIT-FOR-REVIEW | Nine artifacts and owner self-check persisted at 16:56; root integrity gate passed. Fresh `g2b` is preattested exact Sol ultra/fast with no task/context | Fresh R27/R28 packets, then REVISE |
| G3 owner | Cycle 1 delta plan | `plans/CYCLE_1_DELTA_PLAN.md`, `ledger/owners/G3_STATE.md` | SUBMIT-FOR-REVIEW | R48 owner dispositions are accept=2/narrow=2/reject=0; plan `af3f349d…8fd0`, state `f8556102…d6d6`, both pushed at `b38aa4d…95c4b`; all bounded gates pass | G7 binds R08 to the pushed plan hash; any filed R08 allegations route through root for premise-first owner disposition |
| G4 owner | traceability matrix and C2-C7 briefs | `reports/TRACEABILITY_MATRIX.md`, `plans/cycle_briefs/**`, `ledger/owners/G4_STATE.md` | SUBMIT-FOR-REVIEW | R38-A01 accepted with bounded Q3-DIS-5/tally regrade; R38-C01 qualified with conditional C4/C6 dependency notes. Full suite passed after two disclosed state-only restarts; seven-artifact manifest `0e72a420…5d87a`, checkpoint `f1b4e789…759dc` | Root commits the bounded owner group; R25 and R26 then become eligible after higher-priority G3 routing permits |
| G5 owner | human-action packages | `human_actions/**`, `ledger/owners/G5_STATE.md` | SUBMIT-FOR-REVIEW | P1-P8, tracker, and index persisted; no-action/source checks passed. Fresh `g5b` is preattested exact Sol ultra/fast with no task/context | Fresh R32 source-scope/no-action packet, then REVISE |
| G6 owner | conditional charter successors | qualifying `*_v1.1.md` files and `ledger/owners/G6_STATE.md` only | DONE | R19–R22 incorporated; root review repair applied; four successors remain PROPOSED; exact 83-row §35 schedule and v1.0 hashes preserved; commit `03285ba` pushed | None; owner process terminated normally |
| G7 control owner | gauntlet records and convergence | `gauntlet/**`, `ledger/owners/G7_STATE.md` | DRAFT / R08-BIND-PENDING | R48 filed/qualified control is pushed at `49bffc4…89c44`; G3's R48 disposition and repaired submission are pushed at `b38aa4d…95c4b`; untouched R08 is exact Sol/ultra/live-fast at pane `%90` | Persist owner-disposition integration and terminal `BOUND-UNSENT` without contacting R08; root then independently checks, commits, pushes, revalidates, and dispatches only the sealed control |
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
