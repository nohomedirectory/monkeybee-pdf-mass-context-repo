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

### Live human control, 2026-07-14 17:39 — fast mode for Codex instances (PROSPECTIVE)

A live human instruction at 17:39 requires **every Codex instance from that instruction forward to run in fast mode**. Root has updated the reviewer protocol and the orchestration ledger. Recorded here because execution conditions are part of a round's identity and must be attestable at the time the round runs.

**Prospective only. It changes no terminated round, and no terminated round is reopened, restated, or re-graded.**

- **R19** (`gpt-5.6-sol`, filed 17:19) ran and terminated **before** the control existed. It is unaffected and stands exactly as filed. Its record is not touched.
- **R20** (`claude-opus-4-8`) is not a Codex instance, so the control does not reach it, even though its filing time (17:40) falls after 17:39.
- **Every future `Sol` round** — R01, R04, R06, R08, R10, R12, R13, R15, R17, R21, R23, R25, R27, R30, and supplemental R31 — must run in fast mode and attest it. A `Sol` round assigned after 17:39 that cannot attest fast mode is a control deviation and is recorded as one, not silently admitted.
- **Every `Opus` round** is unaffected by its terms.

**Consequence for convergence, recorded now rather than discovered later:** this changes an execution condition mid-run, within one model family. Sol rounds run before the control (R19 only) and Sol rounds run after it are therefore **not executed under identical conditions**. Any later comparison across Sol rounds carries that confound, and `CONVERGENCE_REPORT.md` names it rather than presenting the Sol series as homogeneous. This is a limitation to disclose, not a defect to hide, and it does not retroactively weaken R19 — it only means R19 is not a like-for-like control for what follows.

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
| R01 | C1 delta plan | envelope-dependency | Sol (fast) | — | `e019fe8c4bef82e8544147920529980c7d04fef1393e12591a36563eecc94daf` | FILED · VALIDATED · TERMINATED | 8 | 2 | 0 | NO | ROUTED → G3 (artifact owner; in-place revision permitted); G3 triage pending. Gate 3 now armed: no further C1 round until G3 revises and exposes a new hash. |
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
| R19 | Charter-set cross-consistency | envelope-dependency | Sol | — | `718928bb101e00881191d8e9f536cab73b82e80fb955e99867dbe95135570c4a` | FILED · VALIDATED · TERMINATED | 7 | 1 | 0 | NO | ROUTED → G6. **G6 triage returned: A01–A07 all QUALIFY** (bounded repairs, named targets). B01 premise-bounded, both branches preserved, unpromoted. No v1.0 in-place edit. G6 `DRAFT`; successors `PROPOSED — awaiting human ratification`. |
| R20 | Charter-set cross-consistency | Q2/Q3 traceability | Opus | — | `718928bb101e00881191d8e9f536cab73b82e80fb955e99867dbe95135570c4a` | FILED · VALIDATED · TERMINATED | 8 | 2 | 0 | NO | ROUTED → G6. **G6 triage returned: A01–A08 all QUALIFY.** B01, B02 unpromoted. No v1.0 in-place edit. G6 `DRAFT`; successors `PROPOSED — awaiting human ratification`. |
| R21 | Charter-set cross-consistency | duplication/drift | Sol (fast) | — | `718928bb101e00881191d8e9f536cab73b82e80fb955e99867dbe95135570c4a` | FILED · VALIDATED · TERMINATED | 14 | 0 | 0 | NO | ROUTED → G6 (conditional); G6 triage pending. No v1.0 in-place edit. Freshness admissible (see disposition). |
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

## Assignment records

A round becomes `ASSIGNED` only when root has bound it to a specific artifact hash and a specific reviewer identity. G7 records the binding here **before** the reviewer files, so the identity a round was assigned against cannot be reconstructed after the fact from the round's own output.

### R19 — ASSIGNED 2026-07-14 17:07

- Artifact: Charter-set cross-consistency — the four v1.0 Charter-set documents, read-only canon.
- Declared lens: `envelope-dependency`. Exactly one. Matches the precommitted R19 lens.
- Assigned model: `gpt-5.6-sol`, effort `ultra`. Matches the precommitted R19 model label `Sol`, whose exact launch targets are `max` or `ultra`.
- Bound artifact hash: `718928bb101e00881191d8e9f536cab73b82e80fb955e99867dbe95135570c4a`.

**Manifest definition (immutable for every Charter-set round).** The bound hash is the SHA-256 of the manifest formed by the `sha256sum` lines of the four Charter-set documents, sorted, including the final newline:

```text
03a97020fa38ae77f3bedd378bfb75e7a3eb83e6ec0be112d20d2cd7945d2dbf  CYCLE_0_WORK_ORDER.md
51152bb22596a25dee7de93e679e0567d4ea58362d5bf4e97d8fb9583b76e7c6  CAMPAIGN_CHARTER_REASONING.md
56bb8e26c47cc72805450ff4963b239572cecce7d678663b7d3fa672379cb9ca  MONKEYBEE_CAMPAIGN_CHARTER_v1.md
d4574ffb5c01ebc5097f65df296752466b00f7986d9094f7b53817a2ec7e5294  AUDIT_FINDINGS_LEDGER.md
```

**Verification performed by G7 before binding.** G7 recomputed the manifest from the working tree rather than accepting the asserted value: the four per-file digests and the manifest hash reproduce root's value exactly. The four per-file digests are additionally byte-identical to the canonical baseline captured at 15:55 in `ledger/CANONICAL_HASHES.md`, so the read-only canon under review has not drifted since the run opened. Recomputation is what makes the hash evidence; a copied hash proves only that copying occurred.

**Admission gates, checked against this binding.** Gate 1 (artifact ready): satisfied — the Charter set is read-only canon under no owner FSM, so it is permanently stable and needs no `SUBMIT-FOR-REVIEW`. Gate 2 (bound hash): satisfied and independently recomputed. Gate 3 (same-artifact re-round): not engaged; this is the first round on this artifact, and the read-only-canon exception governs any successor. Gate 4 (model): satisfied. Gate 5 (exactly one lens): satisfied. Gate 6 (five-pass prompt): not engaged; R19 is not a block round. Gate 7 (fresh reviewer): root's to guarantee at spawn; the reviewer attests its own identity in the filed entry.

**Execution order is not round order.** R19 is filed first while R01–R18 wait. Round IDs are immutable identities, not a schedule, and nothing here is renumbered or retargeted: R01–R12 remain blocked on G3 reaching `SUBMIT-FOR-REVIEW`, and R19 runs now because its artifact is permanently eligible. Under the per-artifact phase model, R19 is the Charter set's **first** round and is therefore a structural-phase round, notwithstanding its position in the global sequence.

**Where R19's findings go.** Not to an in-place fix. The Charter set is read-only (`AGENTS.md` rule 11; `DISPUTES.md` D-003). A graded defect routes to G6, which may produce a `*_v1.1.md` successor with a changelog citing the finding, or records `NOT-TRIGGERED` when nothing qualifies. Restyling and preference findings never qualify.

**Write law now in force.** G7 makes no further write to this file until root reports reviewer termination. The reviewer appends its own R19 entry under the controlled append-only exception; G7 then validates the entry against the schema, routes it through root, and appends the disposition. G7 does not review, does not pre-empt the reviewer's findings, and does not write into the space reserved for its entry.

### R20 — ASSIGNED 2026-07-14 17:25

- Artifact: Charter-set cross-consistency — the same four v1.0 Charter-set documents fixed by the R19 manifest, read-only canon.
- Declared lens: `Q2/Q3 traceability`. Exactly one. Matches the precommitted R20 lens.
- Assigned model: `claude-opus-4-8`, effort `xhigh`. Matches the precommitted R20 model label `Opus`.
- Bound artifact hash: `718928bb101e00881191d8e9f536cab73b82e80fb955e99867dbe95135570c4a` — the same manifest, unchanged.

**Manifest recomputed and attested at 17:25, independently of R19's binding.** The manifest definition is the one fixed in the R19 assignment record and is immutable for every Charter-set round. G7 recomputed it from the working tree at assignment time rather than carrying R19's value forward: the four per-file digests and the manifest hash reproduce `718928bb…570c4a` exactly, and each per-file digest remains byte-identical to the canonical baseline captured at 15:55 in `ledger/CANONICAL_HASHES.md`. A hash inherited from a previous round attests only that the previous round happened; re-attestation at each binding is what makes the identity evidence. The canon under review has not drifted since the run opened.

**Admission gates, checked against this binding.** Gate 1 (artifact ready): satisfied — read-only canon under no owner FSM. Gate 2 (bound hash): satisfied and recomputed. Gate 3 (same-artifact re-round): satisfied on two independent grounds — R20 declares a **different** lens from R19, which the general rule permits against an unchanged artifact, and the read-only-canon exception for R19–R22 independently admits consecutive rounds here because no revision is possible and none is expected. Gate 4 (model): satisfied. Gate 5 (exactly one lens): satisfied. Gate 6 (five-pass prompt): not engaged; R20 is not a block round. Gate 7 (fresh reviewer): root's to guarantee at spawn; the reviewer attests its own identity in its filed entry.

**R20 is bound to the v1.0 bytes, and G6 does not change that.** G6 triage of R19's findings is pending, and G6 may produce a `*_v1.1.md` successor. A successor would be a **new artifact with a new identity**, not a revision of this one — the v1.0 Charter set is read-only and its bytes cannot change. R20's findings therefore bind to the v1.0 documents at this hash, exactly as R19's do, and remain valid against them whatever G6 concludes. Nothing in R19 is altered, integrated, re-graded, or predicted by this assignment.

**Where R20's findings will go.** Same route as R19: not to an in-place fix. A graded defect routes to G6 under the read-only-canon exception, which may produce a `*_v1.1.md` successor with a changelog citing the finding, or record `NOT-TRIGGERED` when nothing qualifies.

**Write law now in force.** `gauntlet/ROUND_LOG.md` is closed to G7 until root reports R20 reviewer termination. The reviewer appends its own entry under the controlled append-only exception. G7 does not review, does not predict or pre-empt findings, and does not write into the space reserved for that entry.

## Filed rounds

One round is filed: **R19**, the run's first. Its reviewer entry and G7's validation and routing disposition are at the end of this file; the reviewer appended at EOF rather than at the marker below, which is a placement deviation only — no content requirement is affected and no byte elsewhere in this file was touched. G7 records the deviation and does not rewrite reviewer bytes to tidy it.

R01–R12 remain unfiled: the C1 delta plan (`plans/CYCLE_1_DELTA_PLAN.md`) is still `DRAFT` under its owner per `ledger/ORCHESTRATION_STATE.md`, and R01 cannot be admitted until it reaches `SUBMIT-FOR-REVIEW` and root binds a hash. Further reviewer entries and dispositions are appended in arrival order.

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

## R19 — Charter-set cross-consistency — envelope-dependency

- reviewer process: NTM session `monkeybee-pdf-mass-context-repo--r19`, window 1, pane 1 (`%78`, `/dev/pts/16`); fresh stateless R19 process
- model identity: `gpt-5.6-sol`, effort `ultra`; process evidence: PID 3038450 arguments include `-m gpt-5.6-sol -c model_reasoning_effort=ultra`; TUI evidence: live footer displayed `gpt-5.6-sol ultra`
- started / filed: `2026-07-14T17:09:37+02:00` / `2026-07-14T17:19:06+02:00`
- artifact hash: `718928bb101e00881191d8e9f536cab73b82e80fb955e99867dbe95135570c4a`
- authority chain read: `AGENTS.md` in full; `OVERNIGHT_GOAL.md` §§1, 3/G6, 4; `ledger/prompts/GAUNTLET_REVIEWER_PROTOCOL.md` in full; R19 allocation/control facts in `gauntlet/ROUND_LOG.md`; `MONKEYBEE_CAMPAIGN_CHARTER_v1.md`, `CYCLE_0_WORK_ORDER.md`, `AUDIT_FINDINGS_LEDGER.md`, and `CAMPAIGN_CHARTER_REASONING.md` in full; `MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md` §§3, 24.12–24.16, 33, 35; local proposed §34.9 text at `CYCLE_0_WORK_ORDER.md` §3
- reviewer FSM: SPAWNED -> INGEST-DECLARED-CHAIN -> APPLY-ONE-LENS -> FILE-GRADED-FINDINGS -> TERMINATED
- counts: A=7; B=1; C=0
- marginal-only: NO
- no-action statement: No external page or party was contacted; no prohibited-processor source or documentation was read; no benchmark, comparator measurement, or new comparative datum was produced; no SpecCard semantic body, bead, pseudo-bead inventory, code, or scaffold was generated; no canonical artifact, owner state, allocation table, pre-existing round-log byte, or shared ledger was edited; no commit or push was made. The only write was this required EOF append.

### R19-A01 — R0 signature discovery is scheduled at R2

- evidence: `AUDIT_FINDINGS_LEDGER.md` R2-N1 and `CYCLE_0_WORK_ORDER.md` §2 require structural signature/ByteRange discovery in R0 and signature-impact classification in R2. `MONKEYBEE_CAMPAIGN_CHARTER_v1.md` §5/C4 instead schedules both discovery and impact classification in C4. A bounded absence check over Charter §5/C1 and Work Order §7 for `signature|ByteRange` found neither term; the first Charter cycle placement is C4.
- requirement: The Work Order §2 envelope fix must be reflected in the cycle that ships the Charter §5/C1 R0 envelope; only impact classification belongs at R2.
- consequence: C1 can ship R0 without the required structural signature inventory, and the R2 writer reaches incremental-update work in the same cycle that its upstream signature discovery first appears.
- repair boundary: A G6 successor need only place structural ByteRange/signature discovery and its gate evidence in C1 while retaining impact classification at C4; this finding does not supply replacement wording.
- loss guard: Preserve the structural-versus-trust split and keep cryptographic trust validation in C5; do not pull signature creation into any envelope.

### R19-A02 — The C1 sellable wedge lacks its installability producer

- evidence: `MONKEYBEE_CAMPAIGN_CHARTER_v1.md` §§0, 2, and 5/C1 require a sellable R0 wedge at C1 and make it the unconditional graceful-degradation result. Charter §5/C4 first schedules release engineering, packaging, and documentation "so the wedge is installable by customers." `CAMPAIGN_CHARTER_REASONING.md` §2 states that a wedge that cannot be installed is not a wedge. Work Order §7 schedules a CLI for C1 but no packaging, installation, or release-engineering slice.
- requirement: Charter §§2 and 5/C1 require G1 to be shipped and sellable at the C1 boundary, including when C4 and C7 are dropped.
- consequence: The schedule's own installability dependency arrives three cycles after the promised sellable boundary, so graceful degradation before C4 does not yield the promised product state.
- repair boundary: A G6 successor must either schedule the minimum customer-installable release slice and admission evidence in C1 or move/narrow the sellable boundary; this finding does not choose the release mechanism.
- loss guard: Preserve the larger reproducible-build, documentation, and supply-chain program in C4, and do not pull rendering, writer, or G2/G3 machinery into C1.

### R19-A03 — R0 SpecCard coverage is checked after the swarm it gates

- evidence: Charter §3 item 5 makes reviewed SpecCard coverage a gate on each cycle's swarm start, and Charter §8 risk 2 says card production runs one cycle ahead. Yet Charter §5/C0 gates only on an R0 coverage plan, while §5/C1 checks R0 coverage at the C1 close gate. Work Order §5 item 5 says only to begin R0 card production, Work Order §0 item 4 permits a day-zero item to remain a dependency-bearing bead, and Work Order §7 says C1 may begin without an explicit reviewed-coverage admission check. Local §34.9 additionally requires contracts citing SpecCardIds before bead conversion.
- requirement: Charter §3 item 5 requires licensed, two-person-reviewed coverage for the C1 surface before the C1 swarm starts, not merely by C1 close.
- consequence: The stated C0/C1 gates admit implementation before its human-bound semantic input is ready, or force the C1 close gate to attempt a retrospective cure for an invalid start.
- repair boundary: A G6 successor must add one explicit C1 start admission dependency for reviewed R0 coverage, located no later than C0 handoff/C1 admission; this finding does not create card content.
- loss guard: Preserve `PENDING-LICENSED-SOURCE`, the two-person meaning review, and the one-cycle-ahead rule; no model-generated semantics may fill the gap.

### R19-A04 — Open §35 decisions have no exhaustive owner-cycle schedule

- evidence: Charter §5/C0 promises to resolve the §35 decisions that gate C1 and "explicitly defer the rest"; Work Order §0 item 3 requires every deferred decision to have a named owner-cycle. Work Order §4 names seven resolve-now items and only five deferrals. Bounded checks of that section found no entries for Rev 7 §35's `Reality root model`, `Evidence outcome model`, `Immutable source identity`, `External renderer matrix`, `Public-key security handler`, or `First PDF/UA profile`. The first three feed C1's frozen identity/evidence/source kernel; the latter three feed Charter C3/C4, C5, and C6 gates respectively.
- requirement: Charter §5/C0 and Work Order §§0 and 4 require every unresolved §35 dependency either to be decided before its consumer/freeze boundary or to carry an explicit owner-cycle.
- consequence: C0 can freeze the kernel while C1-defining laws remain open, and later envelopes can reach their delta-plan boundary with required access/profile/security decisions that have no scheduled evidence producer or decision deadline.
- repair boundary: A G6 successor needs an exhaustive §35 classification: C0 resolution for kernel/C1 blockers, otherwise a named owner-cycle and must-resolve-before boundary; this finding does not select any option.
- loss guard: Preserve every §35 evidence-needed condition and the provisional status of defaults; do not silently convert a default assumption into a ratified decision.

### R19-A05 — The Q3 baseline precommitment is only a budget reservation

- evidence: Charter §5/C4 requires Baselines A–D(/E) and ablations in the Q3 package, and Charter §8 risk 1 says the baselines are precommitted at day zero. Work Order §5 item 8 reserves only a budget line. A bounded search of all four Charter-set files for `EvaluationProtocolId|baseline task|ablation task` found no scheduled commitment artifact or producer. Rev 7 §§33.2 and 33.4 require historical and contemporaneous baseline vintages plus a pre-result evaluation commitment binding baseline/ablation tasks, resources, held-out boundaries, and evaluator lineage.
- requirement: The Charter's chosen production-disproportion component of Q3 must cross the prospective §33.4 commitment boundary, with the historical vintage frozen near program start; a budget reservation is not that instrument.
- consequence: C4 can fund and run baselines but cannot retroactively create the missing day-zero protocol boundary or a historical vintage, so those results cannot carry the Q3 production-disproportion role assigned in Charter §7.
- repair boundary: A G6 successor must schedule a day-zero baseline/ablation protocol commitment and its custodian/producer, while leaving contemporaneous execution near C4; alternatively it must explicitly downgrade that Q3 component before results.
- loss guard: Preserve baseline/ablation separation, fair equal-resource controls, Baseline E's where-feasible status, and Rev 7 §33.15's separation of artifact and foundry objects.

### R19-A06 — Q2 schedules discovery commitment and field freeze but no discovery execution

- evidence: Charter §3 item 3 and Work Order §5 item 3 schedule the pre-search discovery protocol and challenge-window opening; Charter §5/C7 then schedules comparator-field freeze and measurement. Rev 7 §24.16 requires an intervening stage in which scouts execute the protocol, characterize candidates, process nominations/challenges, record deviations, and commit a `CompetitorDiscoveryReportId`. A bounded search of the four Charter-set files for `CompetitorDiscoveryReport|discovery execution|characterize candidates|scout` found only `AUDIT_FINDINGS_LEDGER.md` R1-5's statement that scouts were an unprovisioned dependency, not a scheduled producer.
- requirement: Rev 7 §24.16's three-stage order requires committed discovery execution/report evidence between pre-search commitment and evaluation design or field measurement.
- consequence: C7 has no scheduled evidence producer from which to freeze the field; under §24.16, absent that report and coverage the result cannot exceed named-set scope, so the Charter's Q2 field outcome is unavailable.
- repair boundary: A G6 successor must assign the ongoing discovery/scout stage, nomination/challenge handling, candidate characterization, deviation record, and report commitment to a boundary before Q2 evaluation design.
- loss guard: Preserve exact field definitions, unresolved-eligibility visibility, the challenge opportunity, and the separation between search, report freeze, and measurement.

### R19-A07 — The Q2 evaluation commitment is ordered before its required discovery report

- evidence: Work Order §4 defers the S6 performance-per-fidelity metric to C7 protocol finalization while requiring the measurement design to be committed before C7 begins. Charter §5/C7 schedules challenge-window closure and comparator-field freeze inside C7, followed by measurement. Rev 7 §24.16 requires the `EvaluationProtocolCommitment` only after the challenge window and `CompetitorDiscoveryReportId` freeze, and before any measurement. The four-file bounded search above found no separately scheduled Q2 evaluation-commitment step.
- requirement: Rev 7 §§24.12 and 24.16 require the irreversible order pre-search commitment -> discovery execution/report freeze -> evaluation commitment -> measurement for every field lane.
- consequence: The present schedule cannot satisfy both "committed before C7" and "committed after the report frozen in C7"; one boundary must become retrospective or measurement must begin without its required commitment.
- repair boundary: A G6 successor must place report freeze before the evaluation commitment and place all C7 measurements after it—either by moving the discovery close earlier or by making the early-C7 sequence explicit and changing the pre-C7 timing promise.
- loss guard: Preserve three distinct commitments, exact report binding, restart-on-material-change, and the prohibition on inspecting measurements before the third commitment.

### R19-B01 — C6 performance admission may depend on a C7 metric decision

- evidence: Charter §5/C2 starts benchmark tracking, and §5/C6 blocks on performance lanes meeting predeclared targets. Work Order §4 defers the S6 performance-per-fidelity metric to C7 protocol finalization; Rev 7 §24.15.6 supplies a multi-axis experiment shape while §35 decision 9 leaves the S6 posture open. The unresolved premise is whether Charter C6's "perf lanes" are internal engineering lanes distinct from S6; the Charter set does not define that distinction.
- requirement: Any target used to admit C6 must be fixed before the optimization and gate it governs; a later Q2 comparison protocol must separately obey §24.16's post-discovery commitment order.
- consequence: If the C6 lanes are S6 lanes, their metric/decision rule arrives after the gate; if they are internal lanes, their target instrument and relationship to S6 are unscheduled, leaving the C6 gate non-reproducible.
- repair boundary: A G6 successor should distinguish the internal C2–C6 regression/admission instrument from the later S6 field-comparison protocol and assign each a pre-use decision boundary; this finding does not select metrics or thresholds.
- loss guard: Preserve determinism, correctness, coverage, safety, resource, and evidence axes; do not replace the multi-axis rule with one scalar or weaken a failing lane after observation.

### Round verdict

G6 owner revision is required; the v1.0 Charter set remains read-only and no in-place repair is authorized. Seven Grade-A findings establish broken or missing envelope dependencies, and one Grade-B finding remains contingent only on the undefined relationship between C6 performance lanes and S6. This envelope-dependency round is not marginal-only. No conclusion is offered under any other lens.

### R19 — G7 validation and routing disposition (2026-07-14 17:21)

Written by the G7 owner after root reported reviewer termination and verified session absence. G7 validates structure and identity. **G7 does not review, re-grade, confirm, refute, or repair a finding.** Nothing below asserts that any R19 finding is correct; that judgment belongs to G6 triage, and the Charter set stays read-only regardless.

**Schema validation: PASS.** Checked against `ledger/prompts/GAUNTLET_REVIEWER_PROTOCOL.md`:

| Check | Result |
|---|---|
| Heading form `## RNN — <artifact> — <one lens>` | Pass |
| Exactly one declared lens (`envelope-dependency`) | Pass — matches the R19 assignment |
| Artifact hash recorded before analysis | Pass — `718928bb…570c4a`, identical to the bound hash |
| Model identity, two independent attestations | Pass — `gpt-5.6-sol` effort `ultra`; PID 3038450 process arguments and live TUI footer. Matches assignment; no `MODEL-MISMATCH`, no silent fallback |
| Reviewer FSM line, complete | Pass — `SPAWNED -> INGEST-DECLARED-CHAIN -> APPLY-ONE-LENS -> FILE-GRADED-FINDINGS -> TERMINATED` |
| Counts present and matching the filed findings | Pass — declared `A=7; B=1; C=0`; recomputed from the entry: 7 A-subsections, 1 B-subsection, 0 C-subsections |
| Monotonic finding IDs within the round | Pass — A01–A07, B01 |
| Empty grade subsections omitted, counts never omitted | Pass — no C subsection; `C=0` still declared |
| Every finding carries evidence, requirement, consequence, repair boundary, loss guard | Pass — recomputed: 8 of each across 8 findings |
| `marginal-only` field present | Pass — `NO`, consistent with the precommitted definition (a round with any Grade-A or Grade-B finding is not marginal-only) |
| No-action statement present | Pass |
| No repair written into the artifact or the log | Pass — each finding bounds a repair without supplying wording |
| Round verdict present | Pass |
| Authority-chain and lens purity | Pass on inspection — all eight findings argue ordering and dependency between committed envelopes, which is the declared lens |

**Deviation recorded, not repaired.** The entry was appended at end-of-file rather than beneath the `APPEND ROUND ENTRIES BELOW THIS LINE` marker. Placement only: every content requirement is met, no pre-existing byte was modified, and G7 independently re-verified after filing that the five-pass prompt remains byte-for-byte identical to the protocol's, that the R19 assignment record is intact, and that all 32 allocation rows survive. G7 does not rewrite reviewer bytes to tidy placement.

**Routing disposition — all eight findings route to G6 (conditional). No v1.0 in-place edit is authorized or performed.**

| Finding | Grade | Routed to | Basis |
|---|---|---|---|
| R19-A01 through R19-A07 | A | **G6 (conditional Charter-set successors)** | Read-only-canon exception for R19–R22, already precommitted in this log. `AGENTS.md` rule 11 and `DISPUTES.md` D-003 forbid editing a v1.0 Charter-set document; a graded defect may only produce a conventionally named `*_v1.1.md` successor with a changelog citing the finding. |
| R19-B01 | B | **G6 (conditional), premise-first** | The Grade-B premise — whether Charter C6's performance lanes are internal engineering lanes distinct from S6 — is itself the routed item. G6 resolves the premise before deciding whether a defect exists. A Grade B is not a confirmed defect and may not be treated as one. |

Root is triggering G6. What G6 owes back, per its own marching order, is a triage per finding: either a qualifying defect with a `*_v1.1.md` successor carrying a changelog that cites the graded finding and the exact repair and preserves every unaffected feature, or an explicit `NOT-TRIGGERED` for anything that does not qualify. Restyling and preference findings never qualify. Each finding's `loss guard` binds any repair G6 makes.

**What this round does and does not establish.** It establishes that one fresh `gpt-5.6-sol` process, reading the four v1.0 Charter-set documents under one lens, filed seven Grade-A and one Grade-B finding against them. It does not establish that those findings are correct — G6 triage decides that — and it does not upgrade or downgrade any other artifact, or any other lens, in either direction. The remaining Charter-set rounds (R20–R22) still declare their own lenses and are unaffected by this result.

**Log released.** G7 returns to `DRAFT`. This file is open for the next root-routed reviewer.

## R20 — Charter set (MONKEYBEE_CAMPAIGN_CHARTER_v1.md · CYCLE_0_WORK_ORDER.md · AUDIT_FINDINGS_LEDGER.md · CAMPAIGN_CHARTER_REASONING.md) — Q2/Q3 traceability

- reviewer process: session/pane `monkeybee-pdf-mass-context-repo--r20 pane 1`
- model identity: `claude-opus-4-8`, effort `xhigh`. **Process evidence:** `/proc/3096698/cmdline` = `/home/joseph/.local/bin/claude --dangerously-skip-permissions --model claude-opus-4-8 --effort xhigh`; `/proc/3096698/status` `PPid` = 3096404, which equals `pane_pid` of `monkeybee-pdf-mass-context-repo--r20` pane 1, binding the attested model process to the assigned pane. **TUI evidence:** that pane renders the live Claude Code TUI for this review session (footer present, session interactive); its retained scrollback no longer holds the startup banner, so the TUI corroborates the pane→process binding but supplies no independent model string of its own. Recorded as a limitation, not a mismatch: no TUI indicator contradicts the process attestation, so neither MODEL-MISMATCH nor STALE-ASSIGNMENT is filed.
- started / filed: 2026-07-14T17:28:10+02:00 / 2026-07-14T17:40:00+02:00
- artifact hash: `718928bb101e00881191d8e9f536cab73b82e80fb955e99867dbe95135570c4a` — recomputed from the working tree at 17:27 under the R19 manifest definition (SHA-256 over the sorted `sha256sum` lines of the four Charter-set documents, final newline included). Reproduces the bound value exactly; the four per-file digests are byte-identical to `ledger/CANONICAL_HASHES.md`. Binding valid.
- authority chain read: `AGENTS.md` (full) · `OVERNIGHT_GOAL.md` §§1, 3/G6, 4 · `ledger/prompts/GAUNTLET_REVIEWER_PROTOCOL.md` (full) · `gauntlet/ROUND_LOG.md` lines 198–213 (R20 assignment control) and lines 179–187 (manifest definition only; R19 findings and results not ingested) · the four Charter-set documents in full · `MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md` §10.3, §§24.12–24.16, §33 (§§33.1–33.18), §34 (§§34.4–34.5), §35 (+ §35.1) · `ledger/CANONICAL_HASHES.md`. Rev 7 §31 (flagships) was **not** read — it is outside this round's declared chain — and its content is treated throughout as an unresolved premise, never supplied from memory.
- reviewer FSM: SPAWNED -> INGEST-DECLARED-CHAIN -> APPLY-ONE-LENS -> FILE-GRADED-FINDINGS -> TERMINATED
- counts: A=8; B=2; C=0
- marginal-only: NO
- no-action statement: No artifact, owner checkpoint, ledger, canon, or other file was edited; the sole write is this appended entry at EOF of `gauntlet/ROUND_LOG.md`, and no pre-existing byte of that file was altered (pre-append SHA-256 `36f9bab683592cbdabb37ff75115dbc3e1ac039d3449433df9548c0b9d354376`, 47210 bytes, 359 lines, EOF newline present). Nothing was committed or pushed. No prohibited PDF-processor source or documentation was contacted; no web access; no competitor observation, benchmark, measurement, or comparison was performed or generated. No SpecCard semantic body was written or inferred; no normative PDF semantics were supplied from model memory. No source code, scaffolding, Beads state, or pseudo-bead inventory was produced. No claim was strengthened: every finding below is `provisional-pending-substrate`, and a no-defect result under this lens would not have upgraded the artifact. No repair was written; repair boundaries name only future G6 `*_v1.1.md` successors, never an in-place edit of read-only canon.

### R20-A01 — §33.4's precommitted `EvaluationProtocolId` — the object that makes Q3 prospective — has no producer, custodian, or ordering position anywhere in the governing set

- evidence: Rev 7 §33.4 ("Tamper-evidently precommit claim families") requires that, *before unblinding or final measurement*, the campaign "create and independently time-commit an `EvaluationProtocolId`" covering the artifact/foundry/lineage claim and exact reference class; profiles, metrics, determinism, performance workloads, **flagships**, failure conditions, claim expiry; the discovery commitment, discovery report, claim scope, denominator, analysis unit, uncertainty, multiplicity, missingness, stopping, and adjudication; **baseline and ablation tasks**, strongest ordinary replacements, model substitutions, resource/human-attention budgets, and evaluator lineage; **held-out task/corpus commitments** and leakage boundaries; and task-novelty/latent-archetype/training-data-exposure analyses. It further requires the commitment be "held by an independent steward, witnessed/timestamped append-only log, or equivalent mechanism **before results**." Charter §3 (day-zero track, 8 items) cites §33.4 at item 2 but imports only its *custody mechanism* ("Tamper-evident commitment substrate established — independent steward custody or witnessed append-only log (Rev 7 §33.4)"); item 3 commits only the *discovery* protocols ("comparator-field discovery method, inclusion criteria, and challenge-window durations"). Work Order §5's day-zero checklist repeats exactly that scope at its item 3. No Charter-set document creates the `EvaluationProtocolId`, names its custodian, or places it before C4. Absence search (whole text of all four Charter-set documents, case-insensitive): `EvaluationProtocol` → 0 hits; `claim famil` → 0; `reference class` → 0; `precommit` → 2 hits, both about the *substrate*/*budget*, neither about a protocol ID (Charter §8 risk 1; ledger C-9). Meanwhile Charter §7's Q2 row already *consumes* this object by reference — "Flagships G/H **under the committed statistical protocol**" — naming a commitment no producer creates.
- requirement: Rev 7 §33.4 (kernel-bound by Work Order §1, which extracts "§33 post-agent evaluation protocol" into the Constitution); §10.3 rule 36 ("A predeclared evaluation is strong only when its canonical protocol commitment existed before unblinding or measurement and was independently time-committed").
- consequence: C4's Baselines A–D(/E), ablations, and Evolution Trial — the entire disproportion leg of the Q3 package submitted on ~day 9 — would run with no precommitted protocol binding their tasks, replacements, budgets, held-out boundaries, or evaluator lineage. Under §33.4's own rule those runs are exploratory, and "post hoc discoveries are hypotheses until replicated under a new committed protocol." The campaign's stated evidentiary advantage over FrankenSim is prospective instrumentation (Reasoning §4: "this campaign's entire evidentiary advantage over its mentor-project is instrumentation, not skill"); the one artifact §33.4 names to deliver it is missing from the only track — day zero — that can produce it in time.
- repair boundary: a future G6 `MONKEYBEE_CAMPAIGN_CHARTER_v1.1.md` + `CYCLE_0_WORK_ORDER_v1.1.md` successor pair adding the `EvaluationProtocolId` as a distinct day-zero producer with a named custodian and an ordering edge into the C4 checkpoint, binding §33.4's enumerated contents. Smallest adequate repair; no in-place edit; the reviewer does not write it.
- loss guard: the repair must keep the day-zero **discovery** commitment (Charter §3.3) a *separate* commitment object — §33.4 states "one late omnibus document cannot retroactively satisfy all three boundaries," so folding discovery and evaluation into a single day-zero document would destroy the very boundary it is meant to create. It must also preserve the graceful-degradation law (Charter §2): the new commitment sits on the G2/G3 track and must not become a G1 wedge dependency.

### R20-A02 — The Charter's Q3 evidence table is presented as a decomposition of the §33.15 artifact rung; §33.15 contains no such decomposition, and one of its six rows imports foundry evidence that §33.15 says is not required and §33.18 forbids borrowing

- evidence: Reasoning §4 asserts, as the basis of the Q3 completeness argument: "The §33.15 artifact-candidate rung decomposes into six conditions; the Charter's evidence-thread table maps each to its producing cycle." Rev 7 §33.15 is a ladder table; its `Artifact-alien candidate` row reads in full: "Independent reviewers judge the functioning artifact a provenance-conditioned extreme outlier in integrated consequence. **Repeatable foundry or lineage evidence is not logically required.**" There is no six-condition decomposition in §33.15 — it carries four artifact rungs (`A0`, `A1`, `A2`, candidate) and one self-award prohibition. The six rows actually in Charter §7 trace to five different homes: substance (§33.18 item 1), provenance (§33.1), grounding under attack (§33.10), **zero Grade-A truth drift** (which is a §34.9 close-gate criterion, not a §33 condition at all), production disproportion (§33.5/§33.6/§33.8 — the *foundry* apparatus), and independence (§33.15's self-award line). The nearest genuine decomposition, §33.18 item 1, lists five elements — "functioning integrated consequence, assurance, operational closure, exact boundary, and provenance-conditioned comparison" — of which **operational closure** and **exact boundary** have no row in Charter §7 at all (see R20-A07).
- requirement: Rev 7 §33.15 (the ladder the Charter's Q3 question cites by name: Charter §0, "Does MonkeyBee earn `Artifact-alien candidate` (Rev 7 §33.15 ladder)"); §33.18 ("Failure of one object never erases evidence for another, and **evidence cannot be borrowed across them**"); §33.17 ("If the foundry fails fair contemporaneous baselines, MonkeyBee can remain an excellent or even artifact-alien candidate; the production-law claim simply failed"); AGENTS.md rule 20 (generated prose cannot strengthen a claim) and Work Order §1's single-normative-home rule.
- consequence: the Charter's Q3 coverage argument rests on a condition list with no normative home — the "six conditions" appear to be back-derived from the Charter's own table, which makes the completeness check circular and unverifiable by any reviewer. Concretely it mis-routes the campaign's most expensive item: Charter §8 risk 1 states that without baselines "there is zero disproportion evidence," and the degradation law (Charter §2) drops the C4 checkpoint under pressure — yet §33.15 and §33.17 both say the artifact rung survives foundry-baseline failure. The governing set therefore cannot answer whether a baseline cut kills Q3 or merely downgrades an unclaimed foundry rung.
- repair boundary: a future G6 `CAMPAIGN_CHARTER_REASONING_v1.1.md` (with the Charter §7 successor) that either cites the true normative home of each of the six rows, or restates the §33.15 rung verbatim and derives the rows from it explicitly, and states which rows are artifact-necessary versus foundry-supporting.
- loss guard: **do not delete the baselines/ablations/distribution rows.** §33.18 item 1 still makes "provenance-conditioned comparison with what that production envelope was expected to produce" constitutive of artifact disproportion, and Charter §8 risk 1's committed-budget rule is the countermeasure to the campaign's top-lethality risk. The repair reclassifies and re-homes this evidence; it must not drop it, and must not weaken risk 1's "a baseline cut is a formal downgrade, never a quiet omission."

### R20-A03 — §33.2's historical baseline vintage has no producer: the only baseline event in the campaign is at C4, and the Reasoning classes baselines as compute-compressible

- evidence: Rev 7 §33.2 requires that "**Every** current-facing production claim uses **both**: a **historical baseline** frozen near the project/claim program's start, preserving what frontier displacement meant then; and a **contemporaneous baseline** run near the public claim date." §33.5 adds: "Historical and contemporaneous vintages are both retained where the frontier has moved materially," and §33.5.2's drift law requires the advantage to survive scrutiny of "model/harness/provider changes **between baseline and claim date**." §33.2 warns that "unversionable provider behavior, unavailable old systems, or material baseline asymmetry becomes explicit uncertainty, not silent credit." Charter §3's day-zero track (8 items) contains no baseline freeze of any kind; Charter §5/C4 schedules the campaign's only baseline event ("equal-resource **Baselines A–D** (plus E, expert comparison, where feasible)") inside the C4 checkpoint at days 7–9; Charter §8 risk 1 says "baselines are **precommitted at day 0 with budget reserved**" — a budget reservation, not a vintage freeze. Reasoning §3 explicitly classifies baselines with the *compressible* work: "Unlimited compute compresses: implementation, tests, fuzz-hours, **baselines**, ablations, the coverage matrix, documentation. It compresses **none** of: [steward recruitment, SpecCard review, challenge windows, held-out corpus sealing, verdict latency]." Absence search (whole text, all four Charter-set documents, case-insensitive): `historical baseline` → 0 hits; `contemporaneous` → 0 hits; `§33.2` → 0 citations.
- requirement: Rev 7 §33.2, §33.5, §33.5.2; and the Charter's own §7 Q3 table, which makes "Production disproportion → C4 Baselines A–D(/E)" a load-bearing Q3 row.
- consequence: a baseline first executed at C4 *is* the contemporaneous vintage. The historical vintage is then unobtainable prospectively and can only become a §33.1 `retrospective` reconstruction, which that section says "cannot by itself support a strong prospectively precommitted foundry claim." This is a day-zero-shaped obligation — structurally identical to held-out corpus sealing, which the Charter *did* catch (§3.6: "after code exists, nothing new can become held-out") — and the Reasoning's compressibility list is what conceals it: the *historical vintage* of a baseline is a calendar object, not a compute object, so unlimited compute cannot recover it after the frontier moves. Charter §8 risk 1 sees baselines only as a budget risk and therefore cannot surface the timing risk.
- repair boundary: a future G6 `MONKEYBEE_CAMPAIGN_CHARTER_v1.1.md` (with `CAMPAIGN_CHARTER_REASONING_v1.1.md`) adding the historical-baseline freeze — at minimum the day-0 model/harness/tool/vintage manifest and task statement needed to reproduce it — to the day-zero track, and correcting Reasoning §3's compressibility list.
- loss guard: the C4 contemporaneous run and §33.5.1's equal-resource fairness law ("Every comparison freezes the same task statement, rights-cleared source pack, repository exposure, model/tool access, compute … except for the mechanism under study") must survive intact. The repair **adds a vintage**; it must not relocate the C4 checkpoint, thin Baselines A–D(/E), or move evidence apparatus onto the G1 wedge's critical path.

### R20-A04 — Charter §6 declares the close gate universal for C1–C7, but the C4 and C7 gates omit it; C7 then consumes "cycle trial records #1–#6," a set the Charter's own emissions table never produces

- evidence: Charter §6 states "Every cycle C1–C7 runs the same loop," whose step 6 is the "**Cycle-close gate (mandatory, blocking):** drift audit … + one held-out extension probe + SpecCard coverage check + **sealed cycle trial record** into the ledger." In Charter §5, the gates for C1, C2, C3, C5, and C6 each end with the close gate ("drift audit + probe + trial record"); the **C4 gate is only** "Q3 package submitted to independent review on ~day 9," and the **C7 gate is only** "Q2 package submitted ~day 15." Charter §4's "Q2/Q3 evidence emitted" column names "Cycle trial record #1" (C1), "Trial #2" (C2), "Trial #3" (C3), **no trial for C4**, "Trial #5" (C5), "Trial #6" (C6), and **no trial for C7** — the numbering resumes at #5 after C4, so slot #4 is reserved yet never emitted. Charter §5/C7's scope then states: "compile the foundry distribution from **cycle trial records #1–#6**." Work Order §3 (the §34.9 protocol text) closes with: "Cycle trial records are the campaign's foundry-distribution evidence; **a cycle without a sealed record contributes nothing to any §33 claim regardless of what it shipped.**" Reasoning §4 states: "**Seven** instrumented cycles are a foundry evaluation as a byproduct of shipping."
- requirement: Charter §6 (universal C1–C7 close gate); Work Order §3 §34.9(6) (blocking close gate; no record → no §33 contribution); Rev 7 §33.8 ("One spectacular branch proves reachability; reliability requires the distribution"); Charter §7's Q3 rows, which make "sealed cycle trial records" load-bearing for provenance and disproportion.
- consequence: the two cycles that **produce the Q3 and Q2 packages** are precisely the two whose close gates are unstated. Under §34.9's own rule, C4 — the Q3 checkpoint — would contribute nothing to any §33 claim. And the size of the foundry distribution that Q3's disproportion row depends on is not determinable from the governing set: C7's scope asserts six records (#1–#6), the emissions table produces five (#1, #2, #3, #5, #6), and the Reasoning describes seven. Three different values of *n* for the campaign's central §33.8 evidence object, inside one governing set.
- repair boundary: a future G6 `MONKEYBEE_CAMPAIGN_CHARTER_v1.1.md` restating the C4 and C7 gates to carry the §6 close gate, fixing the §4 emissions enumeration, and reconciling the record count with `CAMPAIGN_CHARTER_REASONING_v1.1.md`.
- loss guard: C4's pause-and-assemble checkpoint semantics, the ~day-9 / ~day-15 submission dates, and the tempo-independence rule (Charter §9) must all survive. The repair **adds the missing gates and fixes the count**; it must not add a cycle, delay a submission, or convert C7 into a build cycle (Reasoning §2: "C7 = pure measurement because mixing building and measuring in one cycle invites exactly the evaluator-optimization the protocol forbids").

### R20-A05 — The §24.16/§33.4 three-stage commitment order is inverted at two independent points in the governing set

- evidence: Rev 7 §24.16 fixes a **three-stage, irreversible** order for any confirmatory field comparison: (1) a `CompetitorDiscoveryProtocolCommitment` "before discovery begins"; (2) scouts execute, "**run the nomination/challenge window, and commit a `CompetitorDiscoveryReportId` containing the frozen comparator set**"; (3) "**Only after the discovery report is frozen** does an `EvaluationProtocolCommitment` bind that exact report … before measurement or result inspection." §33.4 restates it as kernel law: "For field claims, the discovery commitment predates search, **the discovery report predates comparator-specific measurement design**, and the evaluation commitment predates measurement; one late omnibus document cannot retroactively satisfy all three boundaries." Two inversions: **(i)** Charter §3.3 opens the challenge windows at day 0 to "run concurrent with the build," while Charter §5/C7 **freezes the comparator field at C7** ("freeze the comparator field per the day-zero committed discovery protocol") and closes the windows only at C7's end ("challenge windows close on their predeclared schedule"; Charter §4's C7 row pairs window closure with the day-15 submission). The field is therefore frozen, measured, bundled, and submitted **while its own nomination window is still open** — the reverse of stage 2. **(ii)** Work Order §4's defer list schedules the campaign's only named measurement-design commitment as "S6 performance-per-fidelity metric → C7 protocol finalization (**measurement design, committed before C7 begins**)" — i.e. committed *before* the C7 discovery freeze, which is exactly the ordering §33.4 forbids ("the discovery report predates comparator-specific measurement design"). Absence search (all four Charter-set documents, case-insensitive): `CompetitorDiscovery` → 0 hits; `nomination` → 0 hits; `§24.16` → 0 citations; the shell's stage objects are never named in the governing set.
- requirement: Rev 7 §33.4 (kernel) and §24.16; §10.3 rule 35 (`registered_open_field_lead` "additionally requires an exact `FieldDefinitionId`, prospectively committed discovery protocol, **frozen discovery report, and independent challenge window** over that declared open released field"); §24.12 rule 4 and §24.16 ("A newly discovered … material challenger … **lapses** current-facing registered/observed field leads until characterized").
- consequence: on the Charter's ordering, any nomination arriving during the window's remaining life lands after the freeze and after measurement — and under §24.12 rule 4 it then *lapses the very claim the window exists to legitimize*, at or after the day-15 submission. Under the alternative reading — that the Charter's "challenge window" is a post-publication claim-challenge window rather than §24.16's nomination window — then stage 2's nomination/challenge window is simply **absent** from the governing set. Both readings are defects, and the governing set never distinguishes the two window kinds, so the ordering cannot be checked at all. Inversion (ii) independently means the only measurement-design commitment the campaign schedules is scheduled in the forbidden stage.
- repair boundary: a future G6 `MONKEYBEE_CAMPAIGN_CHARTER_v1.1.md` + `CYCLE_0_WORK_ORDER_v1.1.md` pair that names the three §24.16 stage objects, distinguishes the nomination/challenge window (which must close **before** the discovery-report freeze) from any post-publication challenge window, and re-orders C7 as freeze → evaluation commitment → measurement.
- loss guard: the property Charter §3.3 exists to protect — windows opened at day 0 and long enough that "no one can later claim they were rigged short" — must survive the reordering. The repair must lengthen or advance the *discovery* window, not shorten it, and must not license a shorter post-publication challenge period.

### R20-A06 — Q2's field discovery has no human producer: the Charter's independence layer omits the scouts that §24.16 requires, while AUDIT_FINDINGS_LEDGER R1-5 — which named them — is recorded as RESOLVED-CHARTER

- evidence: Rev 7 §24.16 stage 1 requires the day-zero discovery commitment itself to fix "field/capability definitions, eligibility, search surfaces/terms/languages, **scouts**, cutoff law, nomination/challenge procedure, and planned exclusions"; stage 2 states "**Scouts execute the protocol**, record deviations, characterize candidates…". §24.12 rule 3 requires that "Search surfaces, registries, languages, terms, dates, **scouts**, deviations, nominations, exclusions, and inaccessible systems remain visible." AUDIT_FINDINGS_LEDGER R1-5 records, as Grade A (absence): "The evidence machinery assumes an unprovisioned human ecology (stewards ×23, **scouts**, adjudicators, two-person SpecCard review) with no recruitment/cost/degradation plan" — with status "OPEN-C0 + **RESOLVED-CHARTER** (day-zero track, degradation law)." But Charter §3.4's independence layer engages only "stewards (corpus custody, commitment custody), red team (different model family + humans…), external reviewers/adjudicators identified," and Work Order §5.4 engages only "corpus steward, commitment custodian, red team (different model family + human), reviewer/adjudicator candidates." Absence search (all four Charter-set documents, case-insensitive, term `scout`): **exactly 1 hit — the R1-5 ledger row itself**, i.e. the only mention of the role in the entire governing set is the finding that says it is unprovisioned, and that finding is marked resolved.
- requirement: Rev 7 §24.16 stages 1–2; §24.12 rule 3; §24.16's closing rule ("If the `FieldDefinitionId` is absent/ambiguous, **discovery coverage is incomplete**, or its protocol was not prospectively committed, **only `named_set_lead` is permitted**"); AGENTS.md rule 16 (do not reconstruct unavailable inputs) and the Charter's own honest-degradation law (§2, §3.4: "What cannot be obtained is logged honestly").
- consequence: R1-5's resolution is recorded against a Charter that does not, in fact, provision the role. Nobody executes Q2's comparator discovery; and because §24.16 stage 1 requires the *scouts to be named inside the day-zero commitment*, the day-zero discovery commitment (Charter §3.3) cannot even be authored completely as specified. Under §24.16's closing rule, incomplete discovery caps every Q2 field claim at `named_set_lead` — collapsing the Q2 question as stated in Charter §0, which asks for a field-scoped `leading` outcome against a frozen comparator field.
- repair boundary: a future G6 `MONKEYBEE_CAMPAIGN_CHARTER_v1.1.md` + `CYCLE_0_WORK_ORDER_v1.1.md` adding scouts to the independence layer and to the day-zero discovery commitment's contents, plus an `AUDIT_FINDINGS_LEDGER_v1.1.md` successor correcting R1-5's status to reflect the surviving gap. (The ledger's own closing rule — "Next audit round should append, never rewrite" — is satisfied by a versioned successor with a changelog, not an in-place status edit.)
- loss guard: the honest-degradation path must be preserved and made explicit rather than removed: if the scout role cannot be filled, Q2's scope must visibly degrade to `named_set_lead` per §24.16 rather than proceed silently. The repair must not weaken Charter §3.4's "What cannot be obtained is logged honestly," and must not convert scouting into an in-ecology automated task, which §24.12 rule 9 and §33.10's oracle-lineage law would treat as correlated rather than independent.

### R20-A07 — §33.3 (artifact and operational boundary) is orphaned, and the Charter's single citation of it points at a rule that lives in §33.1

- evidence: Charter §3.1 reads: "**Production ledger opens** before any implementation agent runs: models, harness versions, attempts, failed branches, discarded candidates, cost, human hours, selection decisions. Retrospective entries are labeled `retrospective` and never support prospective claims **(Rev 7 §33.3)**." The cited rule is not in §33.3. It is in **§33.1**: "Earlier work receives a bounded retrospective reconstruction labeled `retrospective`, with source confidence and known gaps; it may explain history but cannot by itself support a strong prospectively precommitted foundry claim." Rev 7 **§33.3** is "Define the artifact and operational boundary": "Classify original runtime code, generic dependencies, construction-time agents/processors, runtime host adapters/models/services, development-only validators, corpora, human procedures, and external infrastructure. **The boundary is the minimum operational closure needed to reproduce and sustain the claimed behavior.** A runtime model/service remains part of the substrate and is not claimed as self-contained MonkeyBee capability." Absence search (all four Charter-set documents, case-insensitive): `operational boundary` → 0 hits; `§33.3` → exactly 1 hit, the mis-citation above. No cycle, gate, day-zero item, or evidence row produces the boundary.
- requirement: Rev 7 §33.3; §33.18 item 1, which makes "operational closure" and "**exact boundary**" constitutive of the artifact-substance-and-disproportion judgment that Q3 asks for; §33.16, whose public bundle must carry the boundary's consequences; Work Order §1's mechanical rule that "every law gets exactly one normative home" and that restatements become citations — a citation to the wrong home is the failure mode that rule exists to prevent.
- consequence: the Q3 package assembled at C4 would carry no declared artifact/operational boundary, so no reviewer could apply §33.3's substrate rule — the one that prevents a runtime model or service from being counted as self-contained MonkeyBee capability. This is also the precise gap R20-A02 predicts independently: §33.18 item 1's five elements include operational closure and exact boundary, and Charter §7's six-row Q3 table has a row for neither. The mis-citation is what conceals the orphan: §33.3 *appears* discharged because the Charter cites it.
- repair boundary: a future G6 `MONKEYBEE_CAMPAIGN_CHARTER_v1.1.md` correcting the citation to §33.1 and adding a §33.3 boundary declaration with a producing cycle and a re-declaration point at each claim envelope.
- loss guard: the retrospective-labeling rule the sentence currently carries ("Retrospective entries are labeled `retrospective` and never support prospective claims") is correct law from §33.1 and must survive the re-homing — the repair fixes the pointer and adds the missing obligation; it must not delete either.

### R20-A08 — The v8 extraction assigns Q2's entire supremacy doctrine to the *refinable shell* while the laws that consume it are frozen kernel, giving the field-scope law two normative homes with different lifecycles

- evidence: Work Order §1 extracts into the frozen Constitution "§10 evidence algebra: facets, **composition rules**, outcome model…" and "§33 post-agent evaluation protocol, §34 refinement/freeze protocol, plus the new §34.9" — so §10.3 and §33.4 are **kernel**. The same section assigns to the shell: "**Stays in the shell (reference corpus for delta plans):** §12–§28 domain sections, §5 workflows, §7 bets, §31 flagships, **§24.12–24.16 supremacy doctrine**, §30 crate atlas, appendices." Charter §1 defines that class as "the reference corpus that delta plans draw from and **refine against the real codebase**." But §10.3's kernel rules 29, 30, 35, and 36 and §24.12/§24.15/§24.16 are **the same law stated twice**: the three claim scopes (`named_set_lead` / `registered_open_field_lead` / `observed_field_lead`), the discovery-protocol and challenge-window preconditions, and the pre-measurement commitment rule all appear in both. The operative machinery — the `FieldDefinitionId` law, the S1–S6 lane furniture ("Each lane names eligible competitors, claim scope, atomic metrics, a canonical denominator or sampling frame, analysis unit, adjudication, Goodhart guard, and fallback"), and §24.16's three named commitment objects — exists **only** in the shell half. Work Order §1's own mechanical rule states: "every law gets exactly one normative home; hand-restatements elsewhere are either deleted, converted to citations, or marked `generated-echo` with their source ID."
- requirement: Work Order §1 (single normative home; kernel/shell split); Charter §1 (kernel "Frozen after C0"; shell refinable); Rev 7 §33.4 and §24.16 (commitments are immutable — "A material amendment creates a new ID, lapses the affected current-facing result where relevant, and requires fresh search or measurement"); AUDIT_FINDINGS_LEDGER R1-10, whose Grade-A duplication-drift finding is marked "RESOLVED via v8 split (one normative home per law)."
- consequence: Q2's claim-scope and commitment law is placed in a document class the Charter licenses delta plans to refine against the evolving codebase — a category error for a *precommitment* regime, whose entire force is that it cannot move once committed. A field-scope law that can be refined against the code it scores is the Goodhart failure §24.12 rule 10 forbids ("Benchmarks are evidence inputs, not optimization targets"). And the split re-creates R1-10's disease inside the very fix that ledger row certifies as its cure: two homes, two freeze semantics, no stated precedence. The same structure applies to "§31 flagships," which §33.4 requires the precommitment to name and which Charter §5 makes the Q3 (Flagship F, C4), CDR (Flagship D, C5), and Q2 (Flagships G/H, C7) producers — though §31 was outside this round's authority chain and is not read here, so that leg is corroborating rather than established.
- repair boundary: a future G6 `CYCLE_0_WORK_ORDER_v1.1.md` that either (a) extracts the §24.12/§24.16 claim-scope and three-stage commitment law into the frozen kernel alongside §10.3 and §33, leaving only the dated competitor register (§24.13) and the lane parameters in the shell, or (b) states an explicit precedence rule and marks the shell restatements `generated-echo` with their kernel source IDs. The choice is the owner's; this round establishes only that the current split leaves the law in two homes.
- loss guard: the §24.13 competitor register **must remain refreshable and dated** — §24.16 requires that "Every planning-gate transition and release-claim freeze re-observes the register," and §34.4 that "a stale register blocks the claim." A repair that freezes the register into the kernel to fix the home problem would break the refresh law and violate §24.12 rule 4. Freeze the *law*; keep the *observations* live.

### R20-B01 — The two §35 decisions that gate Q3's reference class and Q2's first public claim envelope are routed nowhere, though Charter §5/C0 obligates C0 to "explicitly defer the rest"

- evidence: Charter §5/C0 scopes Cycle 0 to "resolve the §35 decisions that gate C1 code (hash algorithm, canonical serialization grammar, DecodedStreamId cost model, evidence-checker isolation, license) and **explicitly defer the rest**." Work Order §4 partitions §35 into a 7-item resolve-now list and a 5-item defer list (raster backend → C6; PDF/A-1 vs 1.7/2.0 writer conflict → C6; C-ABI freeze → post-R4; base-font fallback pack → C3; S6 performance-per-fidelity metric → C7). Rev 7 §35's table contains the row "**Alien-artifact reference class** | Public expert agent foundries under bounded resources | Independent methodology review," and its numbered open decision "**1 — Initial public supremacy claim envelope** | S1 rendering field scorecard versus S2 wild-tail ledger; unresolved. **This selects the first public claim boundary**…". Neither appears in either Work Order list. Absence search (all four Charter-set documents, case-insensitive): `reference class` → 0 hits.
- requirement: Rev 7 §33.4 (the precommitted `EvaluationProtocolId` must name the "artifact/foundry/lineage claim and **exact reference class**"); §33.2 ("Claims state whether they are relative to an ordinary public-agent user, expert public-agent operator, strong publicly documented foundry, conventional expert team, or an incompletely observable private frontier"); §24.12 rule 2 (every field claim names its versioned `FieldDefinitionId`); Charter §5/C0 ("explicitly defer the rest"); Work Order §0.3 ("every deferred decision has a recorded owner-cycle").
- consequence: the reference class is the denominator of the entire Q3 question — "extreme outlier" is meaningless without it — and no Charter-set document states MonkeyBee's, resolves it, or assigns it an owner cycle before the C4 gate that consumes it. Open decision 1 selects Q2's first public claim boundary and has no owner cycle before C7. Both would arrive at their consuming gates unresolved.
- repair boundary: a future G6 `CYCLE_0_WORK_ORDER_v1.1.md` routing every §35 decision — at minimum the reference class (resolve-now, since §33.4's day-zero commitment consumes it) and open decision 1 (owner cycle named) — or stating the partition rule that governs the unlisted rows.
- loss guard: the existing 12 routings and their owner cycles must be preserved unchanged; the repair adds routings, and must not silently resolve a §35 row that Rev 7 marks open (Work Order §8: Cycle 0 makes "no rendering decisions beyond deferred-decision ownership").
- unresolved premise (why B, not A): every §35 table row carries a "Current default assumption" column, so the unlisted rows may be intended to stand at their printed defaults and count as implicitly deferred. The governing set never states whether Work Order §4's two lists are an exhaustive partition of §35 or an enumeration of only the campaign-critical rows. Under the first reading this is a confirmed omission; under the second it is an unstated abbreviation. The Charter's "explicitly defer the rest" favors the first reading but does not settle it.

### R20-B02 — Q2's headline object — a PDF-completion field lead — corresponds to no §24.15 lane, and "full-field" is not one of the three admitted claim scopes

- evidence: Charter §0 states Q2 as: "Does MonkeyBee earn an uncertainty-aware `leading` outcome on a predeclared, **full-field PDF-completion `FieldDefinitionId`**, plus **supremacy-lane results**, against the frozen comparator field?" Rev 7 §10.3 rule 29 and rule 35, and §24.12 rule 2, admit exactly three claim scopes — `named_set_lead`, `registered_open_field_lead`, `observed_field_lead` — and §24.16 closes: "If the `FieldDefinitionId` is absent/ambiguous … only `named_set_lead` is permitted." "Full-field" is none of these and is defined nowhere in the governing set; absence search (all four Charter-set documents): `named_set_lead` → 0 hits, `registered_open_field_lead` → 0 hits, `observed_field_lead` → 1 hit (Reasoning §5, which commits Q2 to the *strongest* scope: "what make a C7 `leading` outcome an *observed_field_lead* instead of a curated victory lap"), `FieldDefinitionId` → 1 hit (the Charter §0 line above). Rev 7 §24.15 defines the lane inventory — "Lane numbering remains S1–S6" — as S1 rendering, S2 wild-tail, S3 structured extraction, S4 generation, S5 atomic candidate-conjunction, S6 performance; **none is a clause-completion lane**, and §24.15 requires that "Each lane names eligible competitors, claim scope, atomic metrics, a canonical denominator or sampling frame, analysis unit, adjudication, Goodhart guard, and fallback." Charter §5/C7 supplies the only mapping in the governing set: "execute the supremacy lanes — **Flagships G and H by name**." Absence search: `§24.15` → 0 citations; `S1`…`S6` lane identifiers → 0 substantive uses in the Charter set.
- requirement: Rev 7 §24.12 rule 1 ("Supremacy is atomic, leading, scope-qualified, and **per-lane—never global**"); §24.15 (mandatory lane furniture); §10.3 rules 29/30/35; §24.16 (scope caps).
- consequence: Q2's central claim — completion leadership — cannot be traced from the Charter's own §7 traceability table to a lane with a denominator, an adjudication rule, a Goodhart guard, and a fallback. `observed_field_lead`, which Reasoning §5 commits to, additionally requires "the material **lawfully pinnable** closed/opaque systems actually observed," and no Charter-set document names who determines lawful pinnability, or what happens to Q2's scope when a closed system cannot be lawfully pinned. The Charter's Q2 scope vocabulary is therefore both non-admitted ("full-field") and stronger, in the Reasoning, than anything its producers are shown to earn.
- repair boundary: a future G6 `MONKEYBEE_CAMPAIGN_CHARTER_v1.1.md` naming Q2's scope from the three admitted values, defining the completion `FieldDefinitionId` (or citing the lane that carries it), and stating the S1–S6 → producing-cycle mapping. The reviewer does not supply the mapping.
- loss guard: **do not narrow Q2 to `named_set_lead` by default.** The day-zero discovery commitment exists precisely to earn the registered-open/observed scopes; a repair that resolves the ambiguity by retreating to the weakest scope would discard the campaign's most expensive day-zero investment. Equally, the repair must not strengthen the scope beyond what the discovery and pinning evidence supports.
- unresolved premise (why B, not A): Rev 7 §31 (flagships) is outside this round's declared authority chain and was not read, so what Flagships G and H denote — and whether they carry the completion lane's denominator, Goodhart guard, and fallback — is unresolved here. If G/H do carry that furniture, the substantive gap narrows to the undefined "full-field" scope term and the missing S-lane mapping; the *Charter-level* trace edge remains broken either way, because the Charter is the campaign's governing traceability instrument and closes neither.

### Round verdict

Owner revision is **required**, and it is G6's to make, not this artifact's: the Charter set is read-only canon, so every repair boundary above names a future `*_v1.1.md` successor and none was written. The ten findings are not ten independent slips; eight of them are one structural pattern. The governing set imports §33's and §24's **custody mechanisms** (a substrate, a ledger, a window, a budget line) while omitting the **commitment objects** those mechanisms were built to hold and the **producers** that would create them: the `EvaluationProtocolId` (A01), the historical baseline vintage (A03), the discovery report and its stage order (A05), the scouts who execute discovery (A06), the §33.3 operational boundary (A07), and the reference class (B01). The campaign's own thesis — that its evidentiary advantage over FrankenSim is prospective instrumentation rather than skill (Reasoning §4) — is precisely what these omissions put at risk, because each missing object is one whose value is destroyed by being created late. Two findings (A02, A07) further show the Q3 evidence table cannot be checked against §33 at all: its six conditions have no normative home, and its citation to §33.3 points at a rule that lives in §33.1.

This lens is **not** marginal-only: A=8 and B=0 is not the shape of a converged artifact, and marginal-only requires A=0 **and** B=0, which fails on both counts (A=8, B=2). No finding rests on model recollection of PDF normative semantics, on competitor observation, or on any text outside the declared chain; §31 was deliberately not read and is carried as an explicit unresolved premise in A08 and B02 rather than reconstructed. What remains uncertain: whether Work Order §4's decision lists are an exhaustive partition of §35 (B01), and what Flagships G/H denote (B02) — both resolvable by an owner with authority to read outside this chain, neither resolvable by strengthening the evidence available here.

All evidence in this entry is `provisional-pending-substrate`. Nothing here upgrades any claim; a clean round under this lens would not have either.

TERMINATED

### R20 — G7 validation and routing disposition (2026-07-14 17:42)

Written by the G7 owner after root reported reviewer termination and verified session absence. G7 validates structure and identity. **G7 does not review, re-grade, confirm, refute, or repair a finding.** Nothing below asserts that any R20 finding is correct; that judgment is G6's, and the Charter set stays read-only regardless.

**Append-only integrity: PROVEN, not asserted.** The pre-append prefix of this file — first 47,210 bytes — hashes to `36f9bab683592cbdabb37ff75115dbc3e1ac039d3449433df9548c0b9d354376`, recomputed by G7 and identical to the value the reviewer recorded in its no-action statement and to root's independent value. No byte preceding R20's entry was altered: R19's entry, its findings, its validation record, and its routing disposition are byte-intact by cryptographic evidence rather than by anyone's word. Reviewer bytes are preserved; G7 appends below them and rewrites nothing.

**Schema validation: PASS.** Recomputed by G7 from the entry, not taken from the packet:

| Check | Result |
|---|---|
| Heading form, exactly one declared lens (`Q2/Q3 traceability`) | Pass — matches the R20 assignment |
| Artifact hash recorded before analysis | Pass — `718928bb…570c4a`, identical to the bound hash; G7 re-attested the manifest from the working tree at 17:25 and again at integration. No `STALE-ASSIGNMENT` |
| Counts match the filed findings | Pass — declared `A=8; B=2; C=0`; G7 recount: 8 A-headings (A01–A08), 2 B (B01–B02), 0 C |
| Every finding carries evidence, requirement, consequence, repair boundary, loss guard | Pass — G7 recount: 10 of each across 10 findings |
| Monotonic IDs; empty grade subsection omitted while `C=0` still declared | Pass |
| Reviewer FSM complete through `TERMINATED`; verdict present | Pass |
| `marginal-only: NO` | Pass — consistent with the precommitted definition; any Grade-A or Grade-B finding defeats marginal-only |
| No repair written into artifact or log | Pass — every repair boundary names a future G6 `*_v1.1.md` successor and stops there |
| Lens purity | Pass on inspection — all ten findings argue Q2/Q3 requirement-to-producer traceability |

**Two deviations recorded transparently, neither rewritten, neither a mismatch.**

1. **TUI model string not recoverable from reviewer scrollback.** The reviewer attested its model from process evidence — `/proc/3096698/cmdline` showing `--model claude-opus-4-8 --effort xhigh`, with `PPid` 3096404 equal to the assigned pane's `pane_pid`, binding the attested process to the assigned pane — but its retained scrollback no longer held the startup banner, so the TUI corroborated the pane→process binding without supplying an independent model string. The reviewer itself recorded this as a limitation rather than claiming a second attestation it did not have, which is the correct behavior under the model identity law. Root independently captured the live TUI **before** assignment, showing Opus 4.8 at `xhigh`, and process and pane binding agree. **Disposition:** the two-attestation requirement is satisfied — process evidence from the reviewer, TUI evidence from root's pre-assignment capture — and no indicator anywhere contradicts the process attestation. Neither `MODEL-MISMATCH` nor `STALE-ASSIGNMENT` is filed. The gap in the reviewer's own scrollback is disclosed here rather than smoothed over, because the strength of an attestation is exactly the evidence behind it.
2. **One local typo in the round verdict.** The verdict reads "A=8 and B=0 is not the shape of a converged artifact" and then, in the same sentence, states the marginal-only rule and the correct counts: "which fails on both counts (A=8, B=2)." The declared counts (`A=8; B=2; C=0`) and the filed headings (8/2/0) reconcile exactly, and the round's `marginal-only: NO` determination is identical under either reading. **Disposition:** an obvious local slip with no effect on counts, grades, or the verdict. G7 records it and does not rewrite reviewer bytes to correct it; the log is append-oriented and a reviewer's filed entry is its own.

**Routing disposition — all ten findings route to G6 (conditional). No v1.0 in-place edit is authorized or performed.**

| Findings | Grade | Routed to | Basis |
|---|---|---|---|
| R20-A01 – R20-A08 | A | **G6 (conditional Charter-set successors)** | Read-only-canon exception, precommitted at initialization. `AGENTS.md` rule 11 and `DISPUTES.md` D-003 forbid editing a v1.0 Charter-set document; a graded defect may only produce a `*_v1.1.md` successor with a changelog citing the finding. |
| R20-B01, R20-B02 | B | **G6 (conditional), premise-first** | Each carries one unresolved premise — whether Work Order §4's decision lists exhaustively partition Rev 7 §35 (B01), and what Flagships G/H denote (B02), which the reviewer deliberately did not read into and carried as an open premise rather than reconstructing from memory. G6 resolves the premise before deciding whether a defect exists. **A Grade B is not a confirmed defect and is not recorded as one.** |

Several findings name repairs spanning more than one Charter-set document (for example a Charter successor paired with a Work Order or Reasoning successor). That is the reviewer's stated repair boundary, not a G7 instruction: G6 decides what qualifies, what a successor contains, and what records `NOT-TRIGGERED`. Each finding's `loss guard` binds any repair G6 makes — several explicitly forbid deleting the baseline, ablation, and distribution evidence they re-home, and G7 carries that constraint forward verbatim rather than paraphrasing it away.

**What this round establishes, and what it does not.** One fresh `claude-opus-4-8` process, reading the four v1.0 Charter-set documents under one lens, filed eight Grade-A and two Grade-B findings. It does **not** establish that those findings are correct — G6 triage decides that — and it does not upgrade or downgrade any other artifact or any other lens. R21 and R22 still declare their own lenses and are unaffected by this result.

**Note for any later verifier — the 47,210-byte prefix hash will not reproduce from the current file, and that is expected.** The append-only proof above was computed at integration time, *before* G7 wrote this disposition and before G7 recorded the 17:39 fast-mode control in the model identity law. That control record sits above the 47,210-byte offset, so G7's own legitimate edit to its own section changed the prefix. The proof was valid when taken and is what it claims: at the moment R20's reviewer terminated, no pre-existing byte of this file had been altered. Recomputing `head -c 47210 | sha256sum` today yields a different value because G7 has written since — not because reviewer bytes moved. R19's and R20's reviewer entries remain byte-intact and are the things the proof was protecting.

**Claim-vocabulary (AGENTS rule 13) scan disposition.** A scan of this file returns `supremacy` inside R20's findings — "§24.12–24.16 supremacy doctrine," "supremacy lanes," "initial public supremacy claim envelope." These are **not** leakage. Each is a scoped citation of Rev 7's own named doctrine and its claim structures, which rule 13 expressly permits ("outside properly scoped claim structures (Rev 7 §10.3/§24)"), and each appears inside quoted or cited normative text where the reviewer is arguing about the doctrine's placement, not asserting supremacy on MonkeyBee's behalf. They are also reviewer-owned bytes, which G7 preserves regardless. No unscoped supremacy phrasing appears anywhere in G7-authored text.

**Log released.** G7 returns to `DRAFT`. This file is open for the next root-routed reviewer. R01 is **not** assigned; root will issue that assignment separately.

## R01 — ASSIGNED 2026-07-14 17:47

The run's first round against the flagship artifact, and the first round of any kind whose admission gate 1 had to be *earned* rather than waived.

- Artifact: `plans/CYCLE_1_DELTA_PLAN.md` — the C1 delta plan, the campaign's flagship deliverable and the single non-negotiable output of this run (OVERNIGHT_GOAL §0.1).
- Declared lens: `envelope-dependency`. Exactly one. Matches the precommitted R01 lens.
- Assigned model: `gpt-5.6-sol`, effort `ultra`, **fast mode, service tier priority**. Matches the precommitted `Sol` label and the live human control of 17:39.
- Bound artifact hash: `e019fe8c4bef82e8544147920529980c7d04fef1393e12591a36563eecc94daf`.

**Artifact and owner state recomputed and attested at 17:47, before assignment.** `sha256sum plans/CYCLE_1_DELTA_PLAN.md` reproduces the bound value exactly. `ledger/owners/G3_STATE.md` records `owner-fsm: SUBMIT-FOR-REVIEW`, transitioned at 17:37:01 after G3's own self-check. The artifact is 3,091 lines, inside the 2,500–4,000-line band OVERNIGHT_GOAL §3/G3 requires. Both the hash and the owner state were verified from disk, not taken from the assignment.

**Admission gate 1 is satisfied for the first time in this run.** Every prior C1 round refusal in this log rested on it: the plan was `DRAFT`, so no stable artifact existed to bind a hash to. G3 has now reached `SUBMIT-FOR-REVIEW`, the hash is stable, and the gate opens. This is the gate working as designed, not a gate being relaxed — nothing about the rule changed, the artifact simply became reviewable.

**Admission gates, checked against this binding.** Gate 1 (artifact ready): satisfied — G3 at `SUBMIT-FOR-REVIEW`, verified on disk. Gate 2 (bound hash): satisfied and recomputed. Gate 3 (same-artifact re-round): **not engaged** — this is the first round on this artifact, so there is no prior revision to gate against. Gate 4 (model): satisfied. Gate 5 (exactly one lens): satisfied. Gate 6 (five-pass prompt): not engaged; R01 is not a block round, and the immutable prompt governs R04–R08 only. Gate 7 (fresh reviewer): root's to guarantee at spawn.

**Third attestation required for this round: fast mode.** R01 is the **first Sol round to run under the 17:39 live human control**. Beyond the standing two attestations of model identity (process arguments and live TUI), root requires the TUI footer to attest `ultra fast` **before the review task is sent**. A Sol round that cannot attest fast mode is a recorded control deviation, not a silent admission.

This also makes live the confound already recorded in the model identity law above: R19 is the only Sol round that ran *before* the control, and every Sol round from R01 forward runs under it. The Sol series is therefore not a homogeneous sequence, and `CONVERGENCE_REPORT.md` says so rather than presenting it as one. Nothing about R19 changes; it simply is not a like-for-like control for what follows.

**Same lens, different artifact — and that distinction is load-bearing.** R01 declares `envelope-dependency`, the same lens R19 applied to the Charter set. It is not a repeat: coverage is per artifact, and R19 said nothing about the C1 plan. R01 is this lens's *first* application to this artifact, so under the per-artifact phase model it is a structural-phase round, and its findings — whatever they are — carry no inference from R19's, in either direction. A quiet R01 would not be corroborated by R19's eight findings, and a heavy R01 would not be predicted by them.

**Where R01's findings will go.** To **G3**, the artifact's owner, which may revise in place — unlike the Charter-set rounds, whose findings route to G6 because their artifact is read-only canon. G3 triages and repairs; it does not self-review, and it may enter `REVISE` only after a fresh finding packet is persisted and routed. Every subsequent C1 round then requires a new artifact hash, per admission gate 3.

**Write law now in force.** `gauntlet/ROUND_LOG.md` is closed to G7 until root reports R01 reviewer termination. The reviewer appends its own entry under the controlled append-only exception. G7 does not review, does not predict or pre-empt findings, and does not write into the space reserved for that entry. The R01–R32 allocation and all filed reviewer bytes are preserved.

## R01 — plans/CYCLE_1_DELTA_PLAN.md — envelope-dependency

- reviewer process: `monkeybee-pdf-mass-context-repo--r01` pane 1; PID 3169762
- model identity: `gpt-5.6-sol`, `model_reasoning_effort=ultra`; PID 3169762 process arguments show `-m gpt-5.6-sol -c model_reasoning_effort=ultra`; live TUI footer shows `gpt-5.6-sol ultra fast`; scrollback shows `Service tier set to priority`
- started / filed: 2026-07-14T17:49:17+02:00 / 2026-07-14T18:04:25+02:00
- artifact hash: `e019fe8c4bef82e8544147920529980c7d04fef1393e12591a36563eecc94daf`; `ledger/owners/G3_STATE.md` says `owner-fsm: SUBMIT-FOR-REVIEW`
- authority chain read: `AGENTS.md` in full; `OVERNIGHT_GOAL.md` §§1, 3/G3, 4; `ledger/prompts/GAUNTLET_REVIEWER_PROTOCOL.md` in full; `gauntlet/ROUND_LOG.md` lines 524–543 only; `plans/CYCLE_1_DELTA_PLAN.md` in full; `MONKEYBEE_CAMPAIGN_CHARTER_v1.md` §§1, 3–6, 8–11; `CYCLE_0_WORK_ORDER.md` §§0, 3, 6–8 (the document has no §9); `AUDIT_FINDINGS_LEDGER.md` OPEN-C0 rows R1-1–R1-9 and R2-N1–R2-N8 plus C1 dependency rows C-1, C-3, C-4, C-7, C-8; `CAMPAIGN_CHARTER_REASONING.md` §§3–8; `MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md` §§3–6, 10–16.6, 25–30.11, 33–35
- reviewer FSM: SPAWNED -> INGEST-DECLARED-CHAIN -> APPLY-ONE-LENS -> FILE-GRADED-FINDINGS -> TERMINATED
- counts: A=8; B=2; C=0
- marginal-only: NO
- no-action statement: Reviewed plan documents only. No processor source or documentation was contacted; no browsing, measurement, comparison, external action, code, scaffold, Beads state, pseudo-bead inventory, SpecCard semantic body, memory-supplied normative fact, or claim strengthening occurred. No plan, owner checkpoint, ledger, canon, or other file was changed; no commit or push occurred. This append is the sole write, and all evidence remains `provisional-pending-substrate`.

### R01-A01 — Source admission is ordered before its required work context

- evidence: `plans/CYCLE_1_DELTA_PLAN.md` §9.1 step 1 admits a source through BYT.001–BYT.003, then step 2 creates the FDN.004–FDN.008 context. BYT.001 explicitly depends on FDN.001–FDN.013 and performs budgeted, cancellation-aware reads; BYT.003 explicitly depends on FDN.004–FDN.013.
- requirement: Rev 7 §§11.1 and P6 require budgets to precede work; Rev 7 §34.4 requires every public promise to have an acyclic prerequisite path; this plan §0 says contract links are semantic prerequisites.
- consequence: The common envelope has no valid first operation: source snapshotting/spooling either runs before its required admission, budget, cancellation, authority, and disclosure context, or consumes a context the workflow has not produced.
- repair boundary: G3 should either place operation/context admission before metered source admission or split a narrowly defined host-supplied source descriptor/capability from the later context-bound snapshot operation, then reconcile §9.1 and BYT.001–BYT.003 edges.
- loss guard: Preserve immutable snapshot identity, explicit partial ranges, scoped-borrow promotion, no ambient I/O, non-resettable accounting, cancellation, and sensitivity inheritance.

### R01-A02 — Strict document-view construction has a resolver/dialect/security bootstrap cycle

- evidence: DOC.001 requires an exact `DocumentViewId` and effective mapping. DOC.002 is the producer of that view/mapping but explicitly depends on DOC.001 and DOC.003. DOC.003 itself takes a selected graph/view/revision, depends on DOC.001, and is consumed by DOC.002. The cycle is reinforced by DOC.001 -> REV.006 -> SEC.008, while SEC.008 requires an exact selected document view.
- requirement: Work Order §3.4 requires an acyclic dependency graph; Rev 7 §34.4 forbids circular semantic ownership; Charter §§5/C1 requires a functioning strict R0 view and object history.
- consequence: No contract can mint the first strict `DocumentViewId`, so object resolution, effective dialect, encrypted object-stream indexing, DOC.009 strict open, and every downstream report/gate lack a constructible prerequisite envelope.
- repair boundary: G3 should introduce explicit pre-view bootstrap records/contracts for chain selection, raw effective mapping, limited resolution, dialect signals, and pre-view security context, then make the finalized view consume those records without any bootstrap producer requiring `DocumentViewId`.
- loss guard: Preserve view-scoped identities, graph/view non-aliasing, exact duplicate/history evidence, capability-sensitive cache partitioning, and one-time object-stream decryption.

### R01-A03 — Recovery hypothesis and candidate view require each other first

- evidence: DOC.002 consumes a selected recovery hypothesis to emit a candidate `DocumentViewId`. REC.001 consumes a candidate view/value, explicitly depends on DOC.002, and emits the `RecoveryHypothesisId` required by REC.003–REC.009. No pre-view hypothesis identity or finalization edge is defined.
- requirement: Rev 7 §§14.3–14.7 requires source-bound hypotheses and retained alternatives; Rev 7 §34.4 and Work Order §3.4 require acyclic ownership and dependency structure.
- consequence: The first recovery candidate cannot be named without its view, and the view cannot be named without the candidate hypothesis. Implementers must invent an uncontracted provisional identity or collapse the two artifacts, undermining replay, cache, report, and alternative-retention roots.
- repair boundary: G3 should define a two-phase edge: a hypothesis-basis identity derived from source/graph/registered assumptions first, a candidate view bound to that basis second, and a consequence/ordering receipt finalized afterward.
- loss guard: Preserve strict-first admission, immutable source facts, explicit assumptions, nondominated alternatives, task-local selection, and the no-writeback boundary.

### R01-A04 — Revision graph, preservation ledger, and signature ranges form a closed producer loop

- evidence: BYT.005 is defined as an interval ledger over a revision graph and takes revision status plus signature coverage. REV.004 consumes BYT.005 and signature ranges to produce the immutable revision graph. REV.008 then consumes REV.004 and BYT.005 to produce structural signature ranges. REV.005 also consumes BYT.005 and an unnamed graph candidate while REV.004 consumes REV.005.
- requirement: Charter §§5/C1 and ledger row R2-N1 require structural signature evidence inside R0; Rev 7 §§12.6, §12.11, and §34.4 require immutable graph identity, independent interval facets, and no circular ownership.
- consequence: There is no first reproducible graph, ledger, or signature artifact. Any implementation must omit required inputs, mutate an allegedly immutable artifact, or invent an unowned graph-candidate/facet staging protocol, so the revision-autopsy and structural-signature gates cannot bind one defensible envelope.
- repair boundary: G3 should separate pre-graph source intervals and occurrence facts, base graph finalization, post-graph signature analysis, and a versioned graph/ledger overlay or superseding derivation with explicit identities and consumers.
- loss guard: Preserve exact raw spans, overlapping interval facets, unexplained ranges, immutable historical graph versions, structural-only signature scope, and later supersession without rewriting old evidence.

### R01-A05 — The strict OpenReport edge is downstream of recovery that requires the strict result

- evidence: DOC.009's strict result is consumed by REC.002, RPT.001, and RPT.003. RPT.001 nevertheless has an unqualified dependency on REC.001–REC.009 outputs, while RPT.003 depends on REC.007/REC.008. DOC.009 also says it outputs a strict `OpenReport`, although RPT.001 is the owning report-body contract.
- requirement: Rev 7 §14.1 and P4 require a separately recorded strict result before recovery; plan §9.2 promises strict inspection without recovery; Charter §§5/C1 requires Workflow B to retain strict/recovery separation.
- consequence: A strict-only request cannot close its formal OpenReport/security-report envelope without post-strict recovery artifacts, but recovery admission needs that strict artifact first. Report ownership is also duplicated between DOC.009 and RPT.001.
- repair boundary: G3 should define one immutable strict result and base OpenReport producer with no REC prerequisite, then attach an optional, separately rooted recovery/security-across-hypotheses report or enrichment receipt after REC.002–REC.009 run.
- loss guard: Preserve the original strict defect, optional recovery, all live alternatives, security conclusions across hypotheses when recovery is requested, and the prohibition on hidden repair.

### R01-A06 — The capability manifest must contain the audit that audits that same manifest

- evidence: RPT.006 produces the candidate manifest consumed by IMM.008, IMM.010, and IMM.012. RPT.006 says the candidate is not gate-admissible until those truth checks and the blocking audit pass for its exact root, yet its provenance also binds the drift-audit result. IMM.012 consumes that manifest and is in turn consumed by RPT.006.
- requirement: Charter §§5/C1 and §6 require a blocking drift audit over the exact candidate; Rev 7 §§10.10, §27.4, and §34.4 require generated truth to be acyclic and artifact-bound.
- consequence: One immutable manifest root cannot both be the audit input and include the later audit result. Regenerating it with that result changes the root and makes the audit stale; omitting the result violates RPT.006's own evidence envelope. Product-gate rows 8–9 therefore cannot bind the same candidate as written.
- repair boundary: G3 should keep the candidate manifest immutable, make IMM.012 emit a separate audit/admission receipt over that root, and let discovery/release surfaces expose the pair or an outer admission envelope without changing the candidate root.
- loss guard: Preserve exact build/toolchain/dependency binding, decision/card/provider blocks, lifecycle states, pre-work discovery, and the rule that a manifest never self-awards gate passage.

### R01-A07 — Prospective C1 ledger evidence has no producer before C1 candidate work

- evidence: Charter §3 requires the production ledger to open before any implementation agent runs. IMM.017 is itself a C1 capability whose precondition says that ledger is already open before candidate generation, but IMM.017 depends on FDN.001–FDN.016, RPT.004–RPT.006, and IMM.012–IMM.016—artifacts produced only after substantial C1 work. Plan §11.5 then requires an IMM.017 trial record for campaign closure.
- requirement: Charter §§3 and §6 plus Work Order §3 require prospective attempt/failure capture and a sealed trial record; Rev 7 §§33.1 forbids reconstructed history from supporting prospective foundry evidence.
- consequence: Implementing IMM.017 inside the cycle it must observe leaves the earlier interval without its producer. Those entries can only be retrospective under IMM.017's own law, so the C1 sealed-trial envelope either has a permanent evidence gap or cannot close.
- repair boundary: G3 should name a pre-C1 bootstrap ledger implementation/interface and record schema, its human/D1/D2/D6 admission, and an append-only handoff or verification path into IMM.017; otherwise candidate generation must remain blocked until that producer exists.
- loss guard: Preserve every failed/discarded attempt, explicit retrospective status, writer isolation, correction links, secret/restricted-text exclusion, and the distinction between a local chain and the human-held commitment substrate.

### R01-A08 — Required assurance lanes and the fuzz baseline have no gate-bearing result producer

- evidence: Charter §§4 says C1 emits a fuzz baseline and Charter §§5/C1 requires G0–G3-subset lane results. Plan §10.2 calls the fuzz baseline a versioned evidence artifact and §11.4 requires G0/G1/G2/G3-subset/G5/G6 evidence, but the closed contract catalog provides target families and FUZ.011's reachable-panic aggregate only. IMM.009 expressly says its edge coverage is inventory evidence, not proof that a fixture or capability works. No contract produces the G0–G3 run/result envelope or the §10.2 baseline consumed by IMM.017 and the close gate.
- requirement: Work Order §7 requires fuzz targets, falsifiers, and the zero-reachable-panics gate as first-class C1 evidence; plan §5 requires every gate-bearing capability to have a stable consequence contract; Charter §6 requires a reproducible blocking close gate.
- consequence: The close gate can prove metadata linkage and panic status but cannot bind the exact executions, outcomes, coverage, rights/card roots, cancellations, failures, and candidate build for the other required assurance lanes or the promised baseline.
- repair boundary: G3 should assign stable producer contracts for assurance-run manifests, lane-result aggregation, and the fuzz-baseline artifact (or explicitly widen an existing contract to own them), then link their exact roots into FUZ.011, IMM.017, and product/campaign gates.
- loss guard: Preserve failed/cancelled runs, exact build/toolchain/corpus/card/rights scope, independent-oracle lineage, the unavailable G3-subset branch, no premature comparison, and no universal inference from corpus survival.

### R01-B01 — Card-registry bootstrap state is not separated from its generated runtime projection

- evidence: Plan §3.4 requires applicable cards before implementation admission. IMM.001 depends on FDN.001–FDN.016 while stating that every normative C1 contract consumes IMM.001. The existing G1 registry is described only as an empty draft input; the plan does not state whether its later human-reviewed form is the pre-FDN authority artifact or whether the FDN-rooted IMM.001 output is required.
- requirement: Charter §3 requires the SpecCard pipeline and reviewed coverage before the C1 swarm; Rev 7 §§4.3 and §34.4 require an authoritative reviewed source path with no circular semantic ownership.
- consequence: Strong local evidence indicates an activation cycle: FDN contracts need card admission, while the formal registry depends on those same FDN contracts. A separately governed human registry could break the cycle, but that producer/handoff is not explicit.
- repair boundary: G3 should distinguish the pre-implementation human-reviewed authority registry from its later canonical/generated runtime projection and state which identity/status gates FDN implementation and how the projection verifies without superseding it.
- loss guard: Preserve `PENDING-LICENSED-SOURCE`, rights flags, two-person meaning review, no model-memory semantics, immutable review provenance, and exact SC.C1-to-MB-SC linkage.

### R01-B02 — Checker isolation lacks pre-run and post-trial lifecycle states

- evidence: IMM.013 explicitly depends on IMM.014. IMM.014 takes seeded-defect trial records as inputs, emits detections/misses in `OracleLineage`, and says incomplete lineage blocks the stronger checker row; those trial records must be produced by exercising the checker. Plan §11.5 requires the resulting D4 roots in the cycle record.
- requirement: Charter §3 and Reasoning §§4 require different-model-family checking and measured seeded-defect detection; Rev 7 §§10.2.1 and §27.1 require explicit oracle lineage and scoped independent falsifiers.
- consequence: The plan does not identify which IMM.014 state permits the first IMM.013 trial. It therefore appears to require post-trial evidence before the checker run that produces it, unless an unstated preliminary lineage record is intended.
- repair boundary: G3 should separate a pre-run isolation plan/lineage admission from seeded-defect trial results and the final supportable checker-claim record, with explicit identities and gate consumers for each stage.
- loss guard: Preserve different-model-family authorship, specification isolation, prohibition on shared parser/encoder/root construction and producer fixtures, known correlations, and Grade-A treatment of seeded misses under the ratified profile.

### Round verdict

G3 revision is required after reviewer termination. Eight confirmed envelope defects block first-producer construction or exact gate closure; two probable defects require explicit bootstrap/lifecycle staging. This lens is not marginal-only. Repairs are bounded above and route to G3; none was applied by R01. All findings and the verdict remain `provisional-pending-substrate`.

### R01 — G7 validation and routing disposition (2026-07-14 17:52 — ⚠ TIME LABEL SUPERSEDED, see correction below)

> **The `17:52` label in this heading is impossible and is superseded.** R01's reviewer entry is filed at `2026-07-14T18:04:25+02:00`; this disposition necessarily followed it. The label is preserved unedited as audit history. Corrected bound: this integration occurred **after `18:04:25`** and **at or before `18:11:10`** (clock-verified). The exact second was not recorded at the time and is **not** invented here. Every hash, count, attestation, routing decision, and gate statement in this disposition was verified against disk and stands unchanged; only the time label was defective. Full correction trail: `ledger/owners/G7_STATE.md`, entry `18:11 — CORRECTION ENTRY`.

Written by the G7 owner after root reported reviewer termination and verified session absence. G7 validates structure and identity. **G7 does not review, re-grade, confirm, refute, promote, or repair a finding.** Nothing below asserts that any R01 finding is correct; that judgment is G3's.

**Append-only integrity: PROVEN.** The pre-entry prefix — first 103,283 bytes, 543 lines — hashes to `1d73757aa203bbba823df07b27ed8d4dbe39b2666ad408ba7f935a30554843e2`, recomputed by G7 and identical to root's committed value. No byte preceding R01's entry was altered: R19's and R20's reviewer entries, findings, and dispositions are byte-intact by cryptographic evidence. Reviewer bytes are preserved; G7 appends below them and rewrites nothing.

**Artifact stability: PROVEN.** `plans/CYCLE_1_DELTA_PLAN.md` still hashes to `e019fe8c…4daf`, identical to the value bound at assignment and to the value the reviewer recorded before analysis. The plan did not change under the reviewer. No `STALE-ASSIGNMENT`.

**Schema validation: PASS**, recomputed by G7 from the entry rather than taken from the packet:

| Check | Result |
|---|---|
| Exactly one declared lens (`envelope-dependency`) | Pass — matches the R01 assignment |
| Artifact hash recorded before analysis | Pass — equals the bound hash; owner state `SUBMIT-FOR-REVIEW` independently noted by the reviewer |
| Counts match filed findings | Pass — declared `A=8; B=2; C=0`; G7 recount: 8 A (A01–A08), 2 B (B01–B02), 0 C |
| Every finding carries evidence, requirement, consequence, repair boundary, loss guard | Pass — G7 recount: 10 of each across 10 findings |
| Monotonic IDs; empty grade subsection omitted while `C=0` declared | Pass |
| `marginal-only: NO` | Pass — consistent with the precommitted definition |
| No repair written into artifact or log | Pass — repair boundaries are named and bounded; none applied |
| Round verdict present | Pass |
| Lens purity | Pass on inspection — all ten findings argue envelope dependency and producer/gate ordering |

**Model identity: three attestations, all satisfied.** Process arguments (PID 3169762) show `-m gpt-5.6-sol -c model_reasoning_effort=ultra`; the live TUI footer shows `gpt-5.6-sol ultra fast`; scrollback shows `Service tier set to priority`. R01 is the **first Sol round to run under the 17:39 live human fast-mode control**, and it attested it: the required `ultra fast` footer was verified before the review task was sent. No `MODEL-MISMATCH`, no control deviation.

**Presentation deviation recorded, not repaired.** No standalone `TERMINATED` line follows the round verdict; termination is carried in the required reviewer-FSM field (`SPAWNED -> INGEST-DECLARED-CHAIN -> APPLY-ONE-LENS -> FILE-GRADED-FINDINGS -> TERMINATED`). **Disposition: the protocol's requirement is met.** It requires the reviewer to "state `TERMINATED` in the entry," and the entry states it in the schema field built to carry it. The standalone trailing line used by R19 and R20 is a convention those reviewers adopted, not a schema field the protocol defines. Recorded for transparency because root asked; G7 does not rewrite reviewer bytes to normalize presentation, and this deviation costs no evidence.

**Post-filing compaction, recorded.** The reviewer compacted **after** filing, then on root's exact reminder reread `AGENTS.md` in full and made **no change** before normal termination. Two things follow, and both matter for how much this entry can be trusted. First, the compaction cannot have influenced the findings — they were already on disk when it happened. Second, because no post-compaction edit was made, the filed bytes are the pre-compaction bytes: the entry validated here is the entry the reviewer wrote while it still held its full reading context. Compaction after filing is the harmless ordering; the harmful one would be compaction *during* analysis, and that is not what occurred.

**Routing disposition — all ten findings route to G3. This is the first round whose findings may be repaired in place.**

| Findings | Grade | Routed to | Basis |
|---|---|---|---|
| R01-A01 – R01-A08 | A | **G3 (artifact owner)** | `plans/CYCLE_1_DELTA_PLAN.md` is a generated campaign artifact under an active owner, not read-only canon. G3 triages and repairs in place — unlike R19/R20, whose findings route to G6 precisely because the Charter set cannot be edited. |
| R01-B01, R01-B02 | B | **G3, premise-first** | Each is a probable defect requiring explicit bootstrap/lifecycle staging, with one unresolved premise. G3 resolves the premise before deciding whether a defect exists. **A Grade B is not a confirmed defect, is not promoted here, and is not to be treated as one.** |

Each finding's `loss guard` binds any repair G3 makes. The governing constraint on this artifact is OVERNIGHT_GOAL §4's standing instruction — **DO NOT LOSE FEATURES** — and a repair that resolves an envelope defect by deleting the capability it depends on is a worse artifact, not a fixed one. G3 does not self-review and may enter `REVISE` only after this packet is persisted and routed.

**Gate 3 is now armed on this artifact.** No further C1 round may be admitted until G3 enters `REVISE`, dispositions and repairs R01, returns to `SUBMIT-FOR-REVIEW`, and exposes a **new** artifact hash. R02 is not assigned and will not be admitted against `e019fe8c…4daf`. This is the rule that makes the R01–R12 sequence a convergence series rather than twelve independent reads of the same bytes.

**What this round establishes, and what it does not.** One fresh `gpt-5.6-sol` process, reading the 3,091-line C1 delta plan under one lens, filed eight Grade-A and two Grade-B findings. It does **not** establish that those findings are correct — G3 triage decides that — and it says nothing about any lens R01 did not apply. The flagship has now been reviewed once, under one of its twelve allocated lenses.

**Log released.** G7 returns to `DRAFT`. R02 is **not** assigned; root issues it after G3's revision and a new hash.

## R21 — ASSIGNED 2026-07-14T18:17:08+02:00

Assignment timestamp read from the system clock immediately before this record was written. No inferred second appears in this entry.

- Artifact: Charter-set cross-consistency — the same four v1.0 Charter-set documents fixed by the R19 manifest, read-only canon.
- Declared lens: `duplication/drift`. Exactly one. Matches the precommitted R21 lens.
- Assigned model: `gpt-5.6-sol`, effort `ultra`, **fast mode, service tier priority**. Matches the precommitted `Sol` label and the 17:39 live human fast-mode control.
- Bound artifact hash: `718928bb101e00881191d8e9f536cab73b82e80fb955e99867dbe95135570c4a` — the same immutable manifest bound for R19 and R20.
- Reviewer session: `monkeybee-pdf-mass-context-repo--r21` pane 1, identity `PearlDuck`, PID 3231216.
- **No review prompt has been sent.** The reviewer process exists and is idle at assignment time.

**Manifest recomputed and attested at assignment, independently of R19 and R20.** The manifest hash reproduces `718928bb…570c4a` exactly, and the four per-file digests remain byte-identical to `ledger/CANONICAL_HASHES.md`. The Charter set has not drifted since the run opened. Re-attesting at every binding is the rule; an inherited hash attests only that a previous round happened.

**Reviewer identity: measured, not accepted.** G7 read the live process rather than transcribing the assignment. `/proc/3231216/cmdline` = `codex --dangerously-bypass-approvals-and-sandbox -m gpt-5.6-sol -c model_reasoning_effort=ultra -c model_reasoning_summary_format=experimental --search`. `/proc/3231216/status` `PPid` = 3230983, which equals the `pane_pid` of `monkeybee-pdf-mass-context-repo--r21` pane 1 — binding the attested model process to the assigned pane. Root independently attested the same process arguments, `Service tier set to priority`, and a live `ultra fast` footer. Two independent observations agree; neither was derived from the other.

**Admission gates, checked against this binding.** Gate 1 (artifact ready): satisfied — read-only canon under no owner FSM. Gate 2 (bound hash): satisfied and recomputed. Gate 3 (same-artifact re-round): satisfied on two independent grounds — R21 declares a **different** lens from R19 (`envelope-dependency`) and R20 (`Q2/Q3 traceability`), which the general rule permits against an unchanged artifact; and the read-only-canon exception for R19–R22 independently admits consecutive rounds because no revision is possible. Gate 4 (model): satisfied, including the fast-mode control. Gate 5 (exactly one lens): satisfied. Gate 6 (five-pass prompt): not engaged; R21 is not a block round. Gate 7 (fresh reviewer): a new process with no authoring context; root guarantees it at spawn.

**Freshness constraint on the authority chain — load-bearing for this lens.** The reviewer must **not** ingest R19's or R20's filed findings. It may read the manifest definition and this assignment record; it may not read the prior rounds' results. A `duplication/drift` reviewer primed with fifteen existing Grade-A findings is no longer a fresh-context reviewer, and its agreement with them would prove correlation, not corroboration. R20's reviewer observed the same discipline and recorded it. This is what makes an independent round independent.

**R21 binds to the v1.0 bytes; G6's pending successors do not change that.** G6 has returned `QUALIFY` triage on the fifteen Charter-set Grade-A findings and may produce `*_v1.1.md` successors. A successor is a **new artifact with a new identity** — the v1.0 Charter set is read-only and its bytes cannot change. R21 reviews the v1.0 documents at this hash, exactly as R19 and R20 did.

**Where R21's findings will go.** To **G6** (conditional), under the read-only-canon exception. Not to an in-place fix.

**Write law now in force.** `gauntlet/ROUND_LOG.md` is closed to G7 until root reports R21 reviewer termination. The reviewer appends its own entry under the controlled append-only exception. G7 does not review, does not predict or pre-empt findings, and does not write into the space reserved for that entry. All filed reviewer bytes (R19, R20, R01) and the full R01–R32 allocation are preserved.

## R21 — Charter-set cross-consistency — duplication/drift

- reviewer process: session `monkeybee-pdf-mass-context-repo--r21`, pane 1, identity `PearlDuck`, PID 3231216
- model identity: `gpt-5.6-sol`, effort `ultra`; `/proc/3231216/cmdline` showed `-m gpt-5.6-sol -c model_reasoning_effort=ultra`; live TUI showed `Service tier set to priority` and the `gpt-5.6-sol ultra fast` footer
- started / filed: 2026-07-14T18:17:08+02:00 / 2026-07-14T18:26:36+02:00
- artifact hash: `718928bb101e00881191d8e9f536cab73b82e80fb955e99867dbe95135570c4a`
- authority chain read: `AGENTS.md` in full; `OVERNIGHT_GOAL.md` §§1, 3 G6, 4; `ledger/prompts/GAUNTLET_REVIEWER_PROTOCOL.md` in full; R21 allocation row, immutable manifest definition, and R21 assignment in `gauntlet/ROUND_LOG.md`; `MONKEYBEE_CAMPAIGN_CHARTER_v1.md`, `CYCLE_0_WORK_ORDER.md`, `AUDIT_FINDINGS_LEDGER.md`, and `CAMPAIGN_CHARTER_REASONING.md` in full; `MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md` only assigned §§3, 10.3, 24.12–24.16, 33.1–33.18, 34.4–34.5, 35–35.1; `ledger/CANONICAL_HASHES.md` in full
- reviewer FSM: SPAWNED -> INGEST-DECLARED-CHAIN -> APPLY-ONE-LENS -> FILE-GRADED-FINDINGS -> TERMINATED
- counts: A=14; B=0; C=0
- marginal-only: NO
- no-action statement: No web or prohibited processor source/documentation was contacted; no measurement or comparison was performed; no SpecCard semantic body or G6 successor was read or generated; no artifact, owner state, allocation row, prior byte, commit, or remote state was changed. The only write is this EOF append. No R19/R20 finding body or disposition was read or used. An R21 locator inadvertently surfaced one aggregate prior-round count line, and a section-boundary probe exposed a few Appendix A lines; neither supplied finding semantics or informed this review, and the boundary deviation is disclosed here.

### R21-A01 — The R0 signature fix drifted back to R2

- evidence: `CYCLE_0_WORK_ORDER.md` §2 and `AUDIT_FINDINGS_LEDGER.md` R2-N1 require structural signature/ByteRange discovery in R0 and impact classification in R2. The Charter's C1/R0 scope and the Work Order's §7 C1 requirements omit discovery, while Charter §5 C4 assigns both discovery and impact classification to R2 (`MONKEYBEE_CAMPAIGN_CHARTER_v1.md`, C1 and C4).
- requirement: `CYCLE_0_WORK_ORDER.md` §2 R2-N1; Rev 7 §34.4 architectural coherence forbids a release envelope from depending on a capability it excludes.
- consequence: R0 can ship without the signature inventory its governing fix requires, and the intended R0-discovery/R2-classification/R3-trust lifecycle collapses back into the defect the Work Order says C0 must remove.
- repair boundary: Align the C1 delta requirements and cycle map with the already-selected three-stage ownership; do not broaden cryptographic trust work into R0 or R2.
- loss guard: Preserve R0 structural-only discovery, R2 structural impact classification for incremental writing, and C5/R3 cryptographic trust validation as distinct capabilities.

### R21-A02 — Ledger entry 1 has two incompatible identities

- evidence: Charter §10 says the committed Charter hash is the campaign's first ledger entry, and `AUDIT_FINDINGS_LEDGER.md` C-9 repeats `Charter hash = ledger entry #1`. Work Order §6 instead requires one batch containing the Charter, Work Order, discovery protocols, and held-out seal manifests, then makes the batch hash ledger entry 1; Work Order §5.1 separately calls the Charter hash one of several first entries.
- requirement: Rev 7 §§33.1 and 33.4 require exact, append-only, time-committed artifact/protocol identities; Charter §§10–11 require amendments to preserve that lineage.
- consequence: An implementer cannot determine whether entry 1 authenticates the Charter alone or a multi-artifact batch, so later amendment and reveal checks can follow different roots while each claims the same ordinal identity.
- repair boundary: Select one canonical entry-1 object and define the relation of the Charter digest and the batch root without changing the committed-artifact set.
- loss guard: Preserve independent/witnessed commitment, exact Charter addressability, the multi-artifact commitment batch, amendment lineage, and the rule that git history alone is insufficient.

### R21-A03 — G1's zero-dependency promise conflicts with its blocking C1 gate

- evidence: Charter §§0 and 2 say the C1 G1 wedge is gated on zero §33 machinery and depends on zero stewards; Reasoning §8 says C4 and C7 are the only §33-gated elements. Yet the Charter's C1 gate requires a held-out probe and sealed trial record, Charter §6 makes that close gate blocking, and Work Order §3 selects the probe from a steward-sealed pool and defines the trial record as §33 foundry-distribution evidence.
- requirement: Charter §2 graceful-degradation law: no G1 deliverable may be gated on G2/G3 machinery, and evidence apparatus may not sit on the wedge's critical path.
- consequence: With no corpus steward or §33 ledger machinery, the stated unconditional C1 deliverable cannot pass its own mandatory gate.
- repair boundary: Separate product-release necessities from optional claim-evidence admission, or narrow the zero-dependency promise to the exact machinery that may detach.
- loss guard: Preserve clean-room/SpecCard gates, hostile-input safety gates, honest claim downgrade, stewarded held-out evidence when available, and the prohibition on silently awarding §33 credit.

### R21-A04 — The C1 sellable wedge is not customer-installable until C4

- evidence: Charter §§0, 2, and C1 call the end-of-C1 R0 artifact a sellable wedge. Charter C4 says release engineering only begins there—packaging, documentation, reproducible builds, and supply-chain lanes—so the wedge becomes installable by customers; Reasoning §2 states that an un-installable wedge is not a wedge.
- requirement: Charter's G1 survival-wedge timing and Reasoning §2's stated cycle-boundary rationale must describe the same deliverable lifecycle.
- consequence: The campaign claims the commercial survival milestone roughly three cycles before the work its own rationale says makes that milestone real.
- repair boundary: Reconcile the minimum C1 commercial-release surface with the later C4 release-engineering program, or narrow the C1 milestone's status.
- loss guard: Preserve the C1 inspection/CLI value, the larger C4 reproducibility and packaging program, and the claim boundary between an internal artifact and a customer-installable release.

### R21-A05 — Campaign termination both answers the questions and precedes their answers

- evidence: Charter §0 says the campaign ends with Q2 and Q3 answered by independent adjudication. Charter §§4, 5 C7, and 9 instead say the campaign ends at package submission and verdicts arrive later on external calendars; Reasoning §§7 and 9 reinforce `submission ≠ verdict`.
- requirement: Charter §§0, 4, 5, and 9 and Reasoning §7 must use one endpoint identity while preserving the ban on self-award.
- consequence: “Campaign end” alternates between an internally controlled submission event and an externally controlled adjudication event, changing whether the campaign can meet its own terminal condition.
- repair boundary: Give submission and adjudicated answer distinct named milestones and bind campaign termination to only one.
- loss guard: Preserve day-9/day-15 submission targets, external adjudicator control, unbounded verdict latency, and the prohibition on treating submission as a verdict.

### R21-A06 — The cycle-trial population alternates between six and seven

- evidence: Charter §5 C7 compiles records `#1–#6`; C4's cycle-map row omits record #4 while C5 resumes at #5. Charter §6 nevertheless applies the sealed-record loop to every cycle C1–C7, Charter §7 says each cycle is a trial, and Reasoning §4 calls the evidence population “Seven instrumented cycles” while Reasoning §2 defines C7 as measurement-only with nothing new built.
- requirement: Work Order §3 §34.9 requires a sealed record for each capability cycle; Rev 7 §33.8 requires a determinate attempt population for distributional reporting.
- consequence: The foundry denominator and C4/C7 close-gate obligations depend on which restatement is followed, permitting either an omitted C4 record or an invented C7 production trial.
- repair boundary: Define the exact record-bearing cycle set and restore the missing ordinal/gate reference without turning C7 measurement into candidate construction.
- loss guard: Preserve C1–C6 production history, the C4 checkpoint, C7 evaluator separation, and visible failed/abandoned attempts.

### R21-A07 — Trial-record restatements drop mandatory distribution fields

- evidence: Work Order §3 calls its sealed record the campaign's foundry-distribution evidence but lists attempts, failures, retries, cost, human interventions, median, and selected extremum. Charter §6 reduces this to attempts, failures, cost, and outcomes; Reasoning §4 uses a third list. Rev 7 §33.8 additionally requires success rate, percentiles, restart behavior, time, defect distribution, representative failures, discarded branches, evaluator-guided repairs, and provider-routing disclosure.
- requirement: Rev 7 §§33.1 and 33.8; Work Order §3's statement that the record is the evidence interface for the foundry distribution.
- consequence: A record satisfying the new §34.9 text can still be insufficient for the §33 distribution claim it is said to support, and generators following the shorter Charter echo lose more fields.
- repair boundary: Establish one versioned trial-record schema or normative reference and make all cycle summaries point to it rather than redefining its fields.
- loss guard: Preserve retries, human interventions, drift/probe outcomes, privacy/redaction limits, discarded paths, routing uncertainty, and distribution—not only the selected run.

### R21-A08 — Most §35 decisions have no disposition owner, and the resolve list itself drifts

- evidence: Rev 7 §35 contains 83 decision rows. Work Order §4 classifies seven as resolve-now and five as deferred with owners, leaving the remainder without the owner-cycle Charter C0 says must be explicit. Charter C0 names only five resolve-now items, omitting the Work Order's persistent-ledger and Rust-toolchain decisions. Work Order §0.3 nevertheless requires every deferred decision to have an owner-cycle.
- requirement: Charter §5 C0; `CYCLE_0_WORK_ORDER.md` §§0.3 and 4; Rev 7 §35's decision registry.
- consequence: Load-bearing C1/kernel questions can be treated as silently accepted defaults, indefinitely open items, or deferred work depending on which list is used.
- repair boundary: Make the C0 classification exhaustive or define an explicit default disposition/owner rule, and reconcile the five-item and seven-item resolve-now identities.
- loss guard: Preserve all 83 decision records, their evidence-needed columns, the existing seven resolve-now choices, the five named deferrals, and every genuinely open state.

### R21-A09 — The three-stage comparison lifecycle is collapsed before measurement

- evidence: Charter §3 and Work Order §5.3 schedule only a day-zero discovery-protocol commitment and open the challenge window. Charter C7 then freezes the field, runs the matrix/lanes, assembles the bundle, and only afterward says challenge windows close; no Charter-set step schedules a post-window `CompetitorDiscoveryReportId` followed by a distinct `EvaluationProtocolCommitment` before measurement.
- requirement: Rev 7 §24.16's irreversible order—pre-search commitment, discovery plus challenge and report freeze, then pre-measurement evaluation commitment—and Rev 7 §33.4's ban on one late omnibus commitment.
- consequence: C7 can measure against a field before nominations are closed and without an evaluation protocol bound to the frozen discovery report, capping any result below the intended field-claim scope.
- repair boundary: Represent all three commitment objects and their ordering in the cycle/day-zero map before any comparison run is admitted.
- loss guard: Preserve the day-zero search commitment, long challenge duration, strongest-configuration fairness, independent timestamping, fresh IDs after material amendment, and honest named-set downgrade.

### R21-A10 — The held-out lifecycle forbids its governing replacement path

- evidence: Charter §3 says that after any code exists, nothing new can become held out; Reasoning §3 repeats that sealing must precede implementation or nothing is held out. Rev 7 §10.3 rule 37 says an adaptively consumed hidden set becomes development data and only a fresh independently stewarded replacement restores the stronger claim; Rev 7 §§24.16 and 33.4 likewise require replacement rules.
- requirement: Rev 7 §10.3 rule 37 and §§24.16/33.4; Charter's own aim to preserve held-out evidence across successive cycles.
- consequence: Once the original pool's query budget is consumed, the Charter's absolute rule makes the required fresh reserve impossible and strands later confirmatory evaluation.
- repair boundary: Distinguish construction-era sealing from a later prospectively sealed, independently stewarded replacement relative to a frozen candidate/evaluation.
- loss guard: Preserve the day-zero main split, query budgets, the rule that exposed/tuned data cannot be relabeled held out, and independent custody of every replacement.

### R21-A11 — Findings ownership is split between two incompatible ledgers

- evidence: `AUDIT_FINDINGS_LEDGER.md` says it is the single home for every finding and ends by directing the next audit round to append there. The live reviewer protocol instead permits only an append to `gauntlet/ROUND_LOG.md` and forbids editing any other file; `OVERNIGHT_GOAL.md` §4 also assigns round findings to the Round Log. The canonical Audit Ledger contains no supersession or routing note.
- requirement: `AGENTS.md` rules 11, 15, and 18; `ledger/prompts/GAUNTLET_REVIEWER_PROTOCOL.md` FSM/write law; the Audit Ledger's own single-home purpose.
- consequence: Owners have two plausible authoritative finding stores with different mutability, so severity, disposition, and successor coverage can diverge silently.
- repair boundary: Define a versioned handoff or mapping from immutable historical ledger IDs to live Round Log IDs without editing the v1 canonical bytes.
- loss guard: Preserve the v1 audit history, current append-only round evidence, canonical read-only status, monotonic IDs, and every unresolved finding.

### R21-A12 — Grade B has two incompatible meanings

- evidence: `AUDIT_FINDINGS_LEDGER.md` defines Grade B as “confirmed by close reading.” The governing reviewer protocol defines B as a probable defect with one unresolved premise; its A grade is the confirmed-defect class.
- requirement: `ledger/prompts/GAUNTLET_REVIEWER_PROTOCOL.md` Grade law; Rev 7 §34.4 requirement that terminology remain stable.
- consequence: A reader combining historical and gauntlet counts cannot know whether B is confirmed or provisional, and may silently promote or demote the historical findings.
- repair boundary: Version/name the historical grading scheme and provide an explicit non-destructive mapping to the gauntlet scheme.
- loss guard: Preserve original grades and reviewer provenance; do not retroactively regrade rows without a versioned successor and changelog.

### R21-A13 — “Two Grade-A defects” contradicts the ledger's own rows

- evidence: Audit Ledger standing observation 3 and Reasoning §1 say the two Grade-A defects found across three rounds were R1-1 and R2-N7. The ledger tables themselves mark numerous other rows A (including R1-3 through R1-7 and R2-N1 through R2-N4). Charter risk 4 uses the narrower and internally consistent phrase “Two Grade-A drifts.”
- requirement: Rev 7 §34.4 terminology/steady-state checks; `AUDIT_FINDINGS_LEDGER.md` purpose as the severity/count source.
- consequence: The prose undercounts confirmed defects and misstates convergence, while the likely intended fact—two Grade-A duplication-drift examples—is already expressed differently in the Charter.
- repair boundary: Scope the count to the duplication-drift category rather than changing any finding row or total.
- loss guard: Preserve every Grade-A row and preserve R1-1/R2-N7 as the two cited drift examples.

### R21-A14 — R1-10 is marked resolved by work that the set still schedules as future

- evidence: Audit Ledger R1-10 uses `RESOLVED via v8 split`, a status absent from the ledger's declared status-code vocabulary. Work Order §§0–2 still make the v8 extraction and one-normative-home conversion pending C0 work, and the ledger's own standing observation calls the split a countermeasure whose effectiveness begins at the C1 close gate.
- requirement: `AUDIT_FINDINGS_LEDGER.md` status-code law; Work Order §§0–2 extraction lifecycle; `AGENTS.md` rule 15 that generated/operational state cannot silently supersede canon.
- consequence: A future mitigation is recorded as an accomplished resolution, allowing R1-10 to disappear from C0 verification before its owning transformation exists in this immutable set.
- repair boundary: Use a declared status that distinguishes selected remedy from verified application, with the transition evidenced only after the versioned extraction lands.
- loss guard: Preserve R1-10, the chosen one-normative-home design, the read-only v1 ledger, and the requirement to verify rather than infer the transition.

### Round verdict

G6 owner revision is required through versioned successors; the immutable v1.0 set must not be edited in place. Fourteen confirmed duplication/drift defects remain, spanning release ownership, commitment identity, gate dependencies, lifecycle/cardinality, evidence schema, decision ownership, and audit vocabulary. This lens is not marginal-only. No Grade-B or Grade-C item was needed because each filed item has a direct local contradiction, omission, or violated local rule. The disclosed locator/boundary deviation supplied no finding content, but root should retain it in the round-admission record rather than silently erase it. Reviewer state: TERMINATED.

### R21 — G7 validation and routing disposition (2026-07-14T18:30:16+02:00)

Timestamp read from the system clock immediately before writing. Written after root reported reviewer termination and verified session absence. **G7 does not review, re-grade, confirm, refute, or repair a finding.** Nothing below asserts that any R21 finding is correct.

**Byte integrity: PROVEN on both sides of the append.** G7 recomputed both bounds independently of root:

| Region | Bytes | SHA-256 | Result |
|---|---|---|---|
| Committed prefix | 131,379 (709 lines) | `490a9e8574bc5f1d06c190a1c0ba448ec8694d91c9b664cec6b78b5227ed2c1b` | Reproduces root's value. No pre-existing byte altered |
| R21 suffix `[131379, 149665)` | 18,286 | `8327eddd67895fc6c0f44229efb6f5e341ded766eb70c5ed87152227b1e0dcbe` | Reproduces root's value. The entry is exactly what root read |

R19's, R20's, and R01's entries, findings, and dispositions are byte-intact by cryptographic evidence. The suffix hash additionally pins *the reviewer's own bytes*, so this disposition is bound to a specific entry rather than to a mutable region of a file.

**Schema validation: PASS**, recomputed by G7 rather than taken from the packet. Declared `A=14; B=0; C=0` matches G7's recount (A01–A14; no B, no C headings). All five required fields present **14 times each** across 14 findings. One lens (`duplication/drift`), artifact hash equals the bound manifest, FSM complete through `TERMINATED`, verdict present, no repair written. Model identity attested three ways as the fast-mode control requires: `/proc/3231216/cmdline` showing `-m gpt-5.6-sol -c model_reasoning_effort=ultra`, the live `gpt-5.6-sol ultra fast` footer, and `Service tier set to priority`. Root's independent recount agrees on every number.

**Grade distribution, recorded without editorializing.** R21 filed 14 Grade-A and zero Grade-B or Grade-C findings — an unusual shape. The reviewer's stated reason is that each item carries a direct local contradiction, omission, or violated local rule, so no item needed the Grade-B hedge. That is the reviewer's grading call and G7 does not disturb it. G6 triage is the test that matters, and it is pending on all fourteen.

#### Deviation 1 — the `started` timestamp is the assignment timestamp, not the review start

The entry records `started / filed: 2026-07-14T18:17:08+02:00 / 2026-07-14T18:26:36+02:00`. But `18:17:08` is the **R21 assignment timestamp**, and the assignment record states plainly that **no review prompt had yet been sent** at that moment. The reviewer therefore could not have started analysis then; it carried the assignment's time into its own `started` field.

**Corrected bound, not an invented second:** R21's review began **after `18:17:08`** and **before `18:18:35`** (root's clock read). The exact start second was not measured by anyone and **is not manufactured here.** The filed timestamp `18:26:36` and the terminal state are unaffected.

Recorded rather than repaired: reviewer bytes are preserved, and the defect is a mislabeled start field, not a defect in the review. G7 notes without irony that this is the same failure class G7 itself committed twice earlier today — a plausible timestamp taken from context instead of measured. It is disclosed on the same terms.

#### Deviation 2 — incidental exposure to prior-round material; **freshness admissibility: PRESERVED**

The reviewer self-disclosed that an R21 locator inadvertently surfaced **one aggregate prior-round count line**, and a section-boundary probe exposed **a few Appendix A lines**. It states that no R19/R20 finding body or disposition was read or used, and that the disclosed material supplied no finding semantics.

The R21 assignment imposed the freshness constraint explicitly, and this lens is the one most vulnerable to it, so the question is answered on the record rather than waved through.

**Ruling: the round is admissible. Its findings stand as an independent round.** Reasoning, in the order that decides it:

1. **What the constraint protects.** The prohibition on ingesting prior findings exists to prevent a reviewer's output from being *derived from or anchored to* earlier findings — so that agreement between rounds is corroboration, not correlation. It is not a rule about incidental bytes; it is a rule about the provenance of conclusions.
2. **An aggregate count carries no finding semantics.** A count line conveys how many findings prior rounds filed. It contains no location, no claim, no evidence, no requirement, no repair boundary. **No duplication/drift finding can be derived from an integer.** All fourteen findings must and do carry their own local evidence, requirement, consequence, repair boundary, and loss guard — the schema enforces exactly this, and G7 verified all 14 instances of all 5 fields.
3. **The Appendix A lines were never prohibited.** Appendix A is Rev 7 domain canon, and the R21 authority chain expressly permits Rev 7 stable sections on demand as the lens requires. This was permitted reading reached by an untidy route. The deviation is in the probe's boundary discipline, not in the material.
4. **No finding body or disposition was read.** That is the actual prohibition, and it held.

**The residual, stated rather than dismissed.** The count line does convey one bit the reviewer would not otherwise have had: *prior rounds on this artifact were not marginal-only.* That could raise a reviewer's prior that defects exist and bias it toward finding **something** — it cannot bias it toward any **specific** finding, because no specific content crossed. The effect is bounded and non-zero, and it is recorded here rather than being declared harmless, because "no effect" is a stronger claim than the evidence supports. It does not reach the threshold that would void the round, and G7 does not pretend to quantify it.

**The disclosure itself is evidence of reviewer integrity.** Nothing compelled the reviewer to report an incidental exposure that no one would have detected. It reported it anyway, bounded it, and asked that it be retained in the admission record rather than erased. A gauntlet whose reviewers hide their boundary slips is worth substantially less than one whose reviewers disclose them — this is the behavior the instrument depends on, and it is recorded as a credit, not filed as a fault.

**Routing disposition — all fourteen findings route to G6 (conditional). No v1.0 in-place edit is authorized or performed.**

| Findings | Grade | Routed to | Basis |
|---|---|---|---|
| R21-A01 – R21-A14 | A | **G6 (conditional Charter-set successors)** | Read-only-canon exception, precommitted at initialization. `AGENTS.md` rule 11 and `DISPUTES.md` D-003 forbid editing a v1.0 Charter-set document. A qualifying defect may only produce a `*_v1.1.md` successor with a changelog citing the finding; restyling and preference findings never qualify. |

No Grade-B or Grade-C findings exist in this round, so nothing is premise-bounded and nothing is promoted. Each finding's `loss guard` binds any repair G6 makes — several explicitly require preserving retries, human interventions, drift and probe outcomes, discarded paths, and the full distribution rather than the selected run.

**Round telemetry** (reported by root; recorded, not independently reproducible by G7): total 198,881 tokens — input 161,082 plus 2,854,400 cached, output 37,799, reasoning 27,171. Codex exited normally; the idle shell exited; the tmux session is absent.

**Log released.** G7 returns to `DRAFT`. **R22 is not assigned** and will not be until root separately authorizes it.
