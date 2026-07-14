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

# Owner Marching Orders

## Shared owner contract

Before any task action, read every line of `AGENTS.md`, `OVERNIGHT_GOAL.md`, `INDEX.md`, the Charter, the Work Order, and the Audit Findings Ledger. Then follow the authority chain named for the assigned subgoal. After context compaction, reread `AGENTS.md` and resume from the disk checkpoint.

Run this finite-state machine and persist every transition in `ledger/owners/GN_STATE.md`:

`INGEST -> DRAFT -> SELF-CHECK -> SUBMIT-FOR-REVIEW -> REVISE -> DONE`

Each checkpoint records timestamp, phase, files read, partial outputs, decisions, open risks, and the next transition condition. Stop the first turn at `SUBMIT-FOR-REVIEW`; a fresh reviewer must produce a finding packet before `REVISE`.

Repository rules remain controlling: plan space only; no Beads or pseudo-beads; no source/build/config scaffolding; no canonical mutation; no prohibited processor source or documentation; no comparative measurement; no human-bound external action; no SpecCard semantic body; no claim-vocabulary leakage. Every card slot says `PENDING-LICENSED-SOURCE`. Use stable Rev 7 section IDs and project-authored plan-level semantics only. Mark unverifiable content `[UNVERIFIED]`. Record any permitted web fetch in the owner state for later transfer to the shared ledger.

Use `apply_patch` for file edits. Preserve concurrent changes. Do not commit, push, branch, worktree, stash, delete, or edit another owner's paths. Every new campaign document begins with `generated-by`, `date`, `inputs`, and `status: DRAFT | PROPOSED`, plus `evidence-status: provisional-pending-substrate` where applicable.

The planning-workflow quality bar applies within the overnight exception that defers Beads: self-contained for a fresh implementation agent; dependency-aware in prose; every non-obvious choice justified; the most obscure section usable alone; no orphan capability or gate. Manually de-slopify human-facing prose without weakening technical precision.

## G1 owner: Constitution v8, shell, and fix application

Exclusive paths: `constitution/**`, `shell/**`, `reports/FIX_APPLICATION.md`, `ledger/owners/G1_STATE.md`.

Extract the kernel specified by Work Order §1 into a new v8 Constitution while preserving stable section identifiers. Include §§4, 6, 9, 10, 11, the §8 direction law, §30.1.1 boundary budget, canonical identity/serialization grammars under proposed C0 decisions, §§33–34, and the supplied §34.9. Keep the concrete crate atlas and domain corpus in the shell. Give every law one normative home; replace duplicates with citations or explicit `generated-echo` markers.

Reorganize the shell corpus so later delta-plan authors can navigate §§3, 5, 7, 12–32, §35, and appendices without treating it as frozen kernel. Preserve features. Apply every OPEN-C0 fix that has an available source. Regenerate Appendix B examples from §10.6 obligations and map every audit ID to exact output locations and disposition in `reports/FIX_APPLICATION.md`. For absent `ALIEN_ARTIFACT.md` and `PROJECT_OVERVIEW.md`, follow `DISPUTES.md`; do not invent replacements.

Create a SpecCard registry, R0 coverage-slot map, extraction protocol, and review template only. Slots must not contain normative semantics and must say `PENDING-LICENSED-SOURCE`.

## G2 owner: decisions

Exclusive paths: `decisions/**`, `ledger/owners/G2_STATE.md`.

Create one brief per Work Order §4 resolve-now item: content hash/digest width; canonical serialization grammar; DecodedStreamId cost/availability; checker isolation; project license; persistent ledger backend; Rust toolchain pin. Each brief states options, `PROPOSED — awaiting human ratification` recommendation, rationale, reversibility, migration path, evidence still needed, and blast radius if wrong. Use the local pinned-tool evidence where relevant. Current library/legal facts require first-party evidence or `[UNVERIFIED]`; do not browse any PDF processor source or documentation.

Create `decisions/DEFERRED_REGISTER.md` for the five deferred items with owner cycle, trigger, evidence needed, and why premature resolution would be harmful. Provide one compact decision index for G3. Recommendations are proposed defaults, never human ratifications.

## G3 owner: Cycle 1 delta plan

Exclusive paths: `plans/CYCLE_1_DELTA_PLAN.md`, `ledger/owners/G3_STATE.md`.

This is the flagship and receives priority over every lower owner. Target 2,500–4,000 lines of substantive plan text. Build the C1-only delta against the document-only repository reality. Use Rev 7 stable section IDs until new Constitution citations are available, then reconcile before self-check. Read proposed G2 defaults when they appear; label every dependency on them as awaiting ratification.

Cover the full L0–L2 C1 surface required by the goal and Work Order: byte sources/snapshots, lexer, COS, xref tables/streams, revision discovery, object streams, all named lossless filters and predictors, bounded recovery search, encryption inventory, caller-credential standard-handler read decryption including the named algorithm families and password-preparation profiles, identity/evidence/report/checker stack, immune-system capabilities, CLI, fuzz inventory, zero-reachable-panics gate, clause-tagging slots, C1 close gate, and explicit exclusions.

Every atomic capability receives a consequence contract with stable ID, inputs and identity domain, preconditions, budgets, cancellation, authority, outputs/outcomes, diagnostics, evidence, determinism, falsifiers, surfaces, dependencies, no-claim boundary, and `PENDING-LICENSED-SOURCE` SpecCard slot citations. Express dependencies as prose and contract links, never task inventories. Treat recovery alternatives, partial outcomes, signature-structure discovery, attacker-keyed hashing, canonicalization work budgets, and credential secrecy as first-class. Preserve every feature under revision.

## G4 owner: traceability and cycle briefs

Exclusive paths: `reports/TRACEABILITY_MATRIX.md`, `plans/cycle_briefs/**`, `ledger/owners/G4_STATE.md`.

Build a bidirectional zero-orphan matrix for every Q3 requirement in Charter §7 / Rev 7 §33.15 and every Q2 requirement: requirement to producing cycle, artifact, gate, authority, dependencies, and failure/downgrade outcome; then artifact/gate back to supported requirement. Close with a direct answer to the governing reality-check question and name every missing prerequisite.

Write one 1–3 page brief for each C2–C7 with scope boundary, consequence-contract families, decision dependencies, known risks, evidence emissions, close-gate sketch, kernel-touch expectation, and why the boundary exists. Do not write future full delta plans or describe imagined code reality. Preserve the archaeology-first restriction.

## G5 owner: human-action packages

Exclusive paths: `human_actions/**`, `ledger/owners/G5_STATE.md`.

Draft sign-and-send packages for every Work Order §5 human-bound day-zero item named by the overnight goal: steward/reviewer/red-team outreach with independence requirements; ISO license/acquisition and AI-use rights steps; commitment-substrate options and setup; verbatim discovery-protocol commitment texts; challenge-window proposal; vulnerability-disclosure policy; corpus acquisition and sealing; baseline-budget reservation and clause-tagging adoption if needed for closure.

Each package states what it is, why automation cannot ratify or execute it, exact human actions, expected time, prerequisites, evidence returned to the repo, failure/downgrade path, and a ready-to-send draft. Send, purchase, publish, recruit, acquire, or change visibility nowhere. Current terms must cite first-party evidence or be marked `[UNVERIFIED]` with a human verification step. SpecCard bodies remain absent.
