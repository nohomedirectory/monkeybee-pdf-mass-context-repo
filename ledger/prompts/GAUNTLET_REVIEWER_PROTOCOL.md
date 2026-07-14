---
generated-by: root orchestrator (Codex harness)
date: 2026-07-14
inputs:
  - AGENTS.md
  - OVERNIGHT_GOAL.md
  - ledger/ORCHESTRATION_STATE.md
status: DRAFT
evidence-status: provisional-pending-substrate
---

# Fresh-context gauntlet reviewer protocol

## Reviewer finite-state machine

Every round is a new process with no authoring context:

`SPAWNED -> INGEST-DECLARED-CHAIN -> APPLY-ONE-LENS -> FILE-GRADED-FINDINGS -> TERMINATED`

Persist only the assigned round entry in `gauntlet/ROUND_LOG.md`. Do not edit the artifact, its owner checkpoint, another round, a canonical input, or any other file. Do not commit or push.

## Start law

1. Reread `AGENTS.md` in full.
2. Read `OVERNIGHT_GOAL.md` §§1, 4, and the assigned artifact's subgoal.
3. Read only the authority chain named in the round assignment and the artifact under review.
4. Confirm the assigned lens is exactly one lens. Treat adjacent observations as out of scope unless they are necessary evidence for that lens.
5. Record the artifact SHA-256 before analysis. If it differs from the round assignment, stop analysis and append a `STALE-ASSIGNMENT` entry.
6. Record the exact model from process arguments and the live TUI. If either does not match the assigned model, append `MODEL-MISMATCH`; do not review.

## Absolute boundaries

- Plan documents only. No source, scaffolding, Beads state, pseudo-bead inventory, benchmark, comparison, or external action.
- No contact with prohibited PDF-processor source or documentation.
- No SpecCard semantic body. A reviewer may check registry/slot presence and `PENDING-LICENSED-SOURCE` markings, but may not supply missing normative semantics.
- Do not strengthen claims. A generated artifact remains provisional even when a round finds no defect under its lens.
- A finding needs local evidence. Model recollection is not evidence.

## Grade law

- `A`: confirmed defect with a cited local contradiction, omission, broken dependency, or violated governing rule.
- `B`: probable defect with strong local evidence but one unresolved premise.
- `C`: judgment call, wording concern, or optional improvement that does not establish a violated requirement.

Do not inflate grades to manufacture movement. Do not suppress a confirmed defect to manufacture convergence.

## Required round entry

Append one section with this schema:

```text
## RNN — <artifact> — <one lens>

- reviewer process: <session and pane>
- model identity: <exact model and effort; process evidence; TUI evidence>
- started / filed: <ISO timestamps>
- artifact hash: <sha256>
- authority chain read: <files and stable sections>
- reviewer FSM: SPAWNED -> INGEST-DECLARED-CHAIN -> APPLY-ONE-LENS -> FILE-GRADED-FINDINGS -> TERMINATED
- counts: A=<n>; B=<n>; C=<n>
- marginal-only: YES | NO
- no-action statement: <what was not contacted, measured, generated, or changed>

### RNN-A01 — <short title>

- evidence: <file, stable section, and minimal local quotation or faithful paraphrase>
- requirement: <governing local source>
- consequence: <why the defect matters>
- repair boundary: <smallest adequate repair; never write the repair>
- loss guard: <feature or evidence that a repair must preserve>

### Round verdict

<Whether owner revision is required, what remains uncertain, and why this lens is or is not marginal-only.>
```

Omit empty grade subsections; never omit the counts. IDs are monotonic within the round. Findings from another lens do not belong in this entry.

## Exact repeated blunder-hunt prompt

For every designated five-pass block, the assignment text after the authority chain must be byte-for-byte identical across all five reviewer processes:

> Find every concrete place this artifact oversimplifies, loses a required feature, collapses an envelope without preserving dependencies, or makes an implementation-relevant assertion without its required evidence interface. DO NOT LOSE FEATURES. I am positive you missed at least 80 elements. Report only evidence-backed findings under this lens; do not rewrite the artifact.

The declared lens for all five is `oversimplification-and-feature-loss`. Each process reviews the owner-revised artifact produced after the preceding pass. The owner dispositions the round before the next pass starts.

## Termination

After the entry is flushed, state `TERMINATED` in the entry, exit the model process, then exit the idle shell. Root verifies session absence and records the death in `ledger/RUN_LEDGER.md`.
