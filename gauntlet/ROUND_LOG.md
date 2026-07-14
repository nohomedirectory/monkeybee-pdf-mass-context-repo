---
generated-by: G7 gauntlet/convergence owner (NTM session `monkeybee-pdf-mass-context-repo--g7`, pane 1; `claude-opus-4-8`, effort `xhigh`)
date: 2026-07-14
inputs:
  - AGENTS.md
  - OVERNIGHT_GOAL.md
  - ledger/prompts/OWNER_MARCHING_ORDERS.md
  - ledger/prompts/GAUNTLET_REVIEWER_PROTOCOL.md
  - ledger/ORCHESTRATION_STATE.md
  - ledger/RUN_LEDGER.md
  - MONKEYBEE_CAMPAIGN_CHARTER_v1.md
  - CYCLE_0_WORK_ORDER.md
  - AUDIT_FINDINGS_LEDGER.md
  - DISPUTES.md
  - INDEX.md
status: DRAFT
evidence-status: provisional-pending-substrate
owner-fsm: DRAFT
---

# Gauntlet Round Log

The single record of every fresh-context review round in this run. Append-oriented: entries are added, never rewritten. A correction names the entry it supersedes and states what changed; it never erases the original.

This log records evidence. It does not strengthen any claim. A round that finds no defect under its lens leaves its artifact exactly as provisional as it was before, and an unreviewed lens is never reported as covered.

## Control facts

- Round writers: fresh, stateless reviewer processes spawned and routed by root. Each appends only its own assigned round entry, under the controlled append-only exception in `ledger/prompts/OWNER_MARCHING_ORDERS.md` §G7. Root guarantees one active round writer at a time.
- The G7 owner does not review. G7 initializes this log, validates each filed entry against the schema, routes it to the artifact owner through root, appends the owner's disposition, and tracks convergence. G7 never edits a reviewed artifact, never writes a finding, and never writes a repair.
- Artifact owners triage and revise. Reviewers never edit the artifact they review.

## Model identity law

Model labels below are exact launch targets carried from `ledger/ORCHESTRATION_STATE.md`. A round may not silently fall back to another model.

| Label | Exact model | Effort |
|---|---|---|
| `Sol` | `gpt-5.6-sol` | `max` or `ultra` |
| `Opus` | `claude-opus-4-8` | `xhigh` |

Every filed entry states the exact model with two independent attestations: process arguments and the live TUI. A reviewer whose observed identity does not match its assignment appends `MODEL-MISMATCH` and does not review. Harness context-usage estimators have reported generic `gpt4` / `sonnet` labels for pinned panes in this run (`ledger/RUN_LEDGER.md`, 16:40); those estimates are not identity evidence and are never recorded here as such.

## Round entry schema

Reviewers append one section per round in exactly the schema fixed by `ledger/prompts/GAUNTLET_REVIEWER_PROTOCOL.md` — heading `## RNN — <artifact> — <one lens>`, then reviewer process, model identity, started/filed timestamps, artifact hash, authority chain read, reviewer FSM, counts (`A=<n>; B=<n>; C=<n>`), `marginal-only`, and a no-action statement; then one subsection per finding carrying evidence, requirement, consequence, repair boundary, and loss guard; then a round verdict. Empty grade subsections are omitted; counts are never omitted. Findings from another lens do not belong in the entry.

G7 validates each filed entry against that schema and records the validation result in the round's status. G7 does not repair a malformed entry by rewriting the reviewer's findings; a malformed entry is routed back through root.

## Immutable five-pass prompt

Two designated five-pass blocks exist in the baseline allocation: **R04–R08** (C1 delta plan) and **R14–R18** (Constitution + fix map). For every round inside a block, the assignment text following the authority chain is byte-for-byte identical across all five reviewer processes. The declared lens for all five is `oversimplification-and-feature-loss`. Each pass reviews the owner-revised artifact produced after the preceding pass, and the owner dispositions the round before the next pass starts.

The prompt body, reproduced exactly as fixed by the reviewer protocol:

```text
Find every concrete place this artifact oversimplifies, loses a required feature, collapses an envelope without preserving dependencies, or makes an implementation-relevant assertion without its required evidence interface. DO NOT LOSE FEATURES. I am positive you missed at least 80 elements. Report only evidence-backed findings under this lens; do not rewrite the artifact.
```

This text is immutable. G7 may not reword, shorten, expand, or "improve" it, and refuses any block round whose assignment text deviates from it. The model rotates within a block (see the allocation); the prompt does not. Rotating the model while holding the prompt fixed is deliberate: it separates what repetition finds from what a different model family finds.

## Precommitted allocation R01–R30

Carried verbatim in substance from the precommitted allocation in `ledger/ORCHESTRATION_STATE.md`, which itself implements the OVERNIGHT_GOAL §4 budget (C1 delta plan 12 · Constitution + fixes 6 · Charter-set cross-consistency 4 · traceability + cycle briefs 4 · decision briefs 2 · whole-repo coherence 2 = 30). Round IDs are immutable. A round is never renumbered, reused, or retargeted; a round that cannot run is closed with a status and reason, and any replacement takes a new ID in the R31+ range.

Independently recomputed at initialization: block sizes are 12/6/4/4/2/2 = 30, and the model sequence yields 15 `Sol` and 15 `Opus` rounds, matching the precommitted baseline cross-model count.

Hash, status, counts, and disposition are slots. They are filled only from filed evidence.

| Round | Artifact | Declared lens (exactly one) | Model | Block | Artifact hash | Status | A | B | C | Marginal-only | Owner disposition |
|---|---|---|---|---|---|---|---|---|---|---|---|
| R01 | C1 delta plan | envelope-dependency | Sol | — | PENDING | PRECOMMITTED | — | — | — | — | — |
| R02 | C1 delta plan | PDF-normative-fact | Opus | — | PENDING | PRECOMMITTED | — | — | — | — | — |
| R03 | C1 delta plan | clean-room contamination | Opus | — | PENDING | PRECOMMITTED | — | — | — | — | — |
| R04 | C1 delta plan | oversimplification-and-feature-loss | Sol | 5-pass A (1/5) | PENDING | PRECOMMITTED | — | — | — | — | — |
| R05 | C1 delta plan | oversimplification-and-feature-loss | Opus | 5-pass A (2/5) | PENDING | PRECOMMITTED | — | — | — | — | — |
| R06 | C1 delta plan | oversimplification-and-feature-loss | Sol | 5-pass A (3/5) | PENDING | PRECOMMITTED | — | — | — | — | — |
| R07 | C1 delta plan | oversimplification-and-feature-loss | Opus | 5-pass A (4/5) | PENDING | PRECOMMITTED | — | — | — | — | — |
| R08 | C1 delta plan | oversimplification-and-feature-loss | Sol | 5-pass A (5/5) | PENDING | PRECOMMITTED | — | — | — | — | — |
| R09 | C1 delta plan | obscure-section self-containment | Opus | — | PENDING | PRECOMMITTED | — | — | — | — | — |
| R10 | C1 delta plan | dependency soundness | Sol | — | PENDING | PRECOMMITTED | — | — | — | — | — |
| R11 | C1 delta plan | security/DoS | Opus | — | PENDING | PRECOMMITTED | — | — | — | — | — |
| R12 | C1 delta plan | claim vocabulary and de-slopification | Sol | — | PENDING | PRECOMMITTED | — | — | — | — | — |
| R13 | Constitution + fix map | identity-law consistency | Sol | — | PENDING | PRECOMMITTED | — | — | — | — | — |
| R14 | Constitution + fix map | oversimplification-and-feature-loss | Opus | 5-pass B (1/5) | PENDING | PRECOMMITTED | — | — | — | — | — |
| R15 | Constitution + fix map | oversimplification-and-feature-loss | Sol | 5-pass B (2/5) | PENDING | PRECOMMITTED | — | — | — | — | — |
| R16 | Constitution + fix map | oversimplification-and-feature-loss | Opus | 5-pass B (3/5) | PENDING | PRECOMMITTED | — | — | — | — | — |
| R17 | Constitution + fix map | oversimplification-and-feature-loss | Sol | 5-pass B (4/5) | PENDING | PRECOMMITTED | — | — | — | — | — |
| R18 | Constitution + fix map | oversimplification-and-feature-loss | Opus | 5-pass B (5/5) | PENDING | PRECOMMITTED | — | — | — | — | — |
| R19 | Charter-set cross-consistency | envelope-dependency | Sol | — | PENDING | PRECOMMITTED | — | — | — | — | — |
| R20 | Charter-set cross-consistency | Q2/Q3 traceability | Opus | — | PENDING | PRECOMMITTED | — | — | — | — | — |
| R21 | Charter-set cross-consistency | duplication/drift | Sol | — | PENDING | PRECOMMITTED | — | — | — | — | — |
| R22 | Charter-set cross-consistency | claim-vocabulary legality | Opus | — | PENDING | PRECOMMITTED | — | — | — | — | — |
| R23 | Traceability + cycle briefs | Q2/Q3 zero-orphan audit | Sol | — | PENDING | PRECOMMITTED | — | — | — | — | — |
| R24 | Traceability + cycle briefs | dependency soundness | Opus | — | PENDING | PRECOMMITTED | — | — | — | — | — |
| R25 | Traceability + cycle briefs | oversimplification hunt | Sol | — | PENDING | PRECOMMITTED | — | — | — | — | — |
| R26 | Traceability + cycle briefs | clean-room contamination | Opus | — | PENDING | PRECOMMITTED | — | — | — | — | — |
| R27 | Decision briefs | reversibility and dependency blast radius | Sol | — | PENDING | PRECOMMITTED | — | — | — | — | — |
| R28 | Decision briefs | security/DoS | Opus | — | PENDING | PRECOMMITTED | — | — | — | — | — |
| R29 | Whole repository | clean-room contamination | Opus | — | PENDING | PRECOMMITTED | — | — | — | — | — |
| R30 | Whole repository | coherence and de-slopification | Sol | — | PENDING | PRECOMMITTED | — | — | — | — | — |

### Status vocabulary

| Status | Meaning |
|---|---|
| `PRECOMMITTED` | Allocated at initialization. No artifact hash bound, no reviewer spawned. |
| `ASSIGNED` | Root bound the round to a specific artifact hash and spawned a fresh reviewer. |
| `FILED` | The reviewer appended its entry and terminated. Awaiting G7 schema validation. |
| `VALIDATED` | Entry passed schema validation and was routed to the artifact owner through root. |
| `DISPOSITIONED` | The artifact owner's triage and repair decisions are appended. The round is closed. |
| `STALE-ASSIGNMENT` | The artifact hash changed under the reviewer. Filed per protocol; no findings admitted. |
| `MODEL-MISMATCH` | Observed model identity did not match the assignment. Filed per protocol; no review performed. |
| `REALLOCATED` | Closed unused because its artifact converged; capacity moved. The reallocation is logged below. |
| `NOT-RUN` | Closed unused for a stated reason (time, budget, or an unmet precondition). Never silently dropped. |

## Root-authorized supplemental rounds R31–R32

Authorized by root at 17:04 on 2026-07-14, **before any round had filed**. That timing is the fact that makes these rounds legitimate evidence rather than a moving target: no result existed to tune them against, no curve was visible, and no artifact had yet survived anything. Both rounds close coverage gaps G7 recorded at initialization under "Open process observations for root" — the unallocated `kernel-touch audit` lens and the absence of any dedicated round over `human_actions/**`.

The precommitted R01–R30 baseline is **unaltered**. No baseline round is renumbered, retargeted, re-lensed, or reassigned. These rounds take new IDs in the R31+ range, exactly as the round-ID law requires, and they are reported as supplemental everywhere they appear so that baseline coverage and supplemental coverage are never conflated.

Supplemental rounds are governed by every law that governs a baseline round: the same entry schema, the same grade law, the same admission gates, the same model identity law with two attestations, exactly one declared lens, and the same termination law (file the entry, state `TERMINATED`, exit the model process, then the idle shell; root verifies session absence and records the death in `ledger/RUN_LEDGER.md`).

| Round | Artifact | Declared lens (exactly one) | Model | Precondition to admit | Artifact hash | Status | A | B | C | Marginal-only | Owner disposition |
|---|---|---|---|---|---|---|---|---|---|---|---|
| R31 | C1 delta plan (`plans/CYCLE_1_DELTA_PLAN.md`) | kernel-touch audit | `gpt-5.6-sol`, effort `ultra` | Runs immediately after R12 **and** the owner's revision of the R12 disposition; a new artifact hash must be bound | PENDING | AUTHORIZED | — | — | — | — | — |
| R32 | `human_actions/**` | source-scope-and-no-action integrity | `claude-opus-4-8`, effort `xhigh` | Runs after the R01–R30 priority floor is satisfied; G5 must have reached `SUBMIT-FOR-REVIEW` | PENDING | AUTHORIZED | — | — | — | — | — |

`AUTHORIZED` is a supplemental-round status: allocated by root after initialization, not yet bound to an artifact hash and not yet spawned. It becomes `ASSIGNED` on binding and then follows the ordinary status path.

### R31 — notes on admission and reading

R31 satisfies admission gate 3 by construction: it follows R12's disposition and the owner's revision, so a new artifact hash exists to bind. Its lens has never been applied to the plan.

A caution for whoever reads the C1 curve later: R31 sits at position 13 in C1's sequence, which the phase model calls polish, but it is the **first** application of its lens. Grade-A findings from it would not contradict a falling curve, and its position does not license reading it as a polish-phase result. G7 will report it as a first-look round under a previously unreviewed lens, at whatever position it lands.

Correspondingly, a marginal-only R31 does not on its own establish C1 convergence. One clean application of one lens by one process is the weakest evidence class this gauntlet recognizes, and the convergence rule exists to detect an exhausted defect surface, not to be satisfied by a lens that has only just started looking.

### R32 — notes on admission and reading

`human_actions/**` is a directory, so R32 needs a reproducible artifact identity the same way the whole-repository rounds do. Precommitted here, before the round runs: the bound artifact hash for R32 is the SHA-256 of a manifest built as the sorted list of `<sha256>  <path>` lines over every file under `human_actions/`, one per line. At 17:04 that scope holds ten files (`README.md`, `OUTREACH_TRACKER.md`, and `P1`–`P8`); the hash is bound at assignment time over whatever the directory then contains, and the manifest is what fixes it.

The declared lens, `source-scope-and-no-action integrity`, is a root-authorized lens that does **not** appear in the OVERNIGHT_GOAL §4 rotation. This is recorded rather than smoothed over: root has the authority to declare it, and the convergence report tracks it in a separate row so that "lenses from the goal's rotation" and "lenses root added" stay distinguishable. It is well-matched to the artifact — these packages carry licence, rights, and disclosure claims bound for a human to send, so whether every stated fact traces to first-party evidence or is marked `[UNVERIFIED]`, and whether every package is genuinely unsent, is precisely what needs an adversarial read.

## Admission gates

G7 refuses to admit a round, and says so on the record, when any of the following holds:

1. **The artifact is not ready.** Its owner has not reached `SUBMIT-FOR-REVIEW` in the owner checkpoint, so there is no stable artifact to bind a hash to.
2. **No bound artifact hash.** A round with no recorded SHA-256 taken before analysis cannot be reproduced and is not evidence.
3. **A same-artifact re-round without revision.** After a dispositioned round, the next round on that artifact waits for the owner's revision and a **new** artifact hash. A second review of an unchanged artifact under a fresh lens is permitted; a repeat of the same lens on an unchanged artifact is not, because it cannot distinguish convergence from a stalled owner. Five-pass block rounds are governed by the block rule: each pass reviews the artifact as revised after the preceding pass.
4. **Model deviation.** The assignment's model does not match the round's precommitted model, or the reviewer's two attestations disagree.
5. **Lens deviation.** The assignment declares zero lenses or more than one.
6. **Prompt deviation inside a five-pass block.** Any departure from the immutable prompt above.
7. **The reviewer is not fresh.** A process carrying authoring context is not a reviewer.

A refusal is recorded with its reason. It is not a finding, and it is not a defect in the artifact.

### Read-only-canon exception for R19–R22

R19–R22 review the four v1.0 Charter-set documents, which repository law holds read-only (`AGENTS.md` rule 11; `DISPUTES.md` D-003). Their artifact hashes therefore cannot change between rounds, and gate 3 above cannot be satisfied by revision. For these rounds only: consecutive rounds are admitted against an unchanged hash, because no revision is possible and none is expected. Their dispositions do not route to an in-place fix. A graded defect routes to G6, which may produce a `*_v1.1.md` successor with a changelog, or records `NOT-TRIGGERED` when nothing qualifies. Restyling and preference findings never qualify.

### Whole-repository hash rule for R29–R30

A "whole repository" artifact needs a reproducible identity. For R29 and R30, the bound artifact hash is the SHA-256 of a manifest built as the sorted list of `<sha256>  <path>` lines over every tracked file outside `.git/**` and `.ntm/**`, one per line. `.ntm/**` is excluded because it is local control-plane state, non-normative and changing as panes start and stop (`AGENTS.md` rule 19). This method is precommitted here so both whole-repo rounds are comparable and any later verifier can reproduce the binding.

## Filed rounds

No rounds have been filed. The C1 delta plan (`plans/CYCLE_1_DELTA_PLAN.md`), which R01–R12 review, is still `DRAFT` under its owner per `ledger/ORCHESTRATION_STATE.md`; R01 cannot be admitted until it reaches `SUBMIT-FOR-REVIEW` and root binds a hash. Reviewer entries and owner dispositions are appended below this line, in round order, as they arrive.

<!-- APPEND ROUND ENTRIES BELOW THIS LINE -->

## Reallocation log

No reallocation has occurred. Governing rule (OVERNIGHT_GOAL §4): when an artifact converges early — two consecutive marginal-only rounds — its remaining rounds are reallocated to the C1 delta plan. Each reallocation records the closed round IDs, the evidence that triggered it, the new round IDs created in the R31+ range, and their lens and model. Capacity is never moved without that record.

## Open process observations for root

These are process observations about the gauntlet's own coverage, recorded because `CONVERGENCE_REPORT.md` may not report an unreviewed lens as covered. They are not findings against any artifact, and G7 does not act on them unilaterally: the allocation is precommitted in a root-owned ledger, and changing it is root's call, not mine.

1. **`kernel-touch audit` is an unallocated lens.** OVERNIGHT_GOAL §4 names it in the lens rotation, and the Charter treats kernel-touch as risk #5 with a `zero from Cycle 2 onward` design target. No round in R01–R30 declares it. Consequence: if the baseline runs exactly as precommitted, the kernel-touch lens is unreviewed, and the convergence report will say so rather than let broad coverage imply it. A reallocated round (R31+) is the natural home if root wants it covered.
2. **The G5 human-action packages receive no baseline round.** The precommitted allocation covers the C1 plan, the Constitution and fix map, the Charter set, traceability and briefs, the decision briefs, and the whole repo. `human_actions/**` is reviewed only if the whole-repo rounds happen to reach it, or if root adds a block, which `ledger/ORCHESTRATION_STATE.md` permits only after the priority floor is safe. These packages contain outreach text, licence and rights claims, and disclosure policy bound for a human to send; they are the artifacts whose defects leave the repository. Recorded as an honest coverage gap, prioritized below the floor.
3. **`marginal-only` needs one fixed definition before it can drive reallocation.** The reviewer protocol requires the field but does not define it, and OVERNIGHT_GOAL §4 makes two consecutive marginal-only rounds the convergence trigger. G7 precommits, now and before any round runs, so the threshold cannot be tuned after seeing results: **a round is marginal-only when it files zero Grade-A and zero Grade-B findings.** Grade-C judgment calls do not defeat it. This is G7's operationalization of a term the goal left open; root or the human may overrule it, and it is on the ratification queue.

### Dispositions

The observations above are preserved as written. Their dispositions are appended here; nothing above is erased.

- **Observation 1 (unallocated `kernel-touch audit` lens) — CLOSED by root, 17:04.** Root authorized supplemental round R31 over the C1 delta plan under exactly that lens, `gpt-5.6-sol` at `ultra`, after R12 and the owner's revision. The lens moves from unallocated to allocated. It does not thereby become covered: coverage requires a filed entry.
- **Observation 2 (no dedicated round over `human_actions/**`) — CLOSED by root, 17:04.** Root authorized supplemental round R32 over `human_actions/**` under the `source-scope-and-no-action integrity` lens, `claude-opus-4-8` at `xhigh`, after the R01–R30 priority floor. The ordering respects the goal's priority ladder: the floor is protected first, and the packages are reviewed rather than left unreviewed.
- **Observation 3 (`marginal-only` definition) — OPEN.** Still G7's own operationalization of a term the goal left open. It remains on the morning ratification queue.
