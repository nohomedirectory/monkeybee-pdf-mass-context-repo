---
generated-by: Codex G3 owner
date: 2026-07-14
inputs:
  - AGENTS.md
  - INDEX.md
  - MONKEYBEE_CAMPAIGN_CHARTER_v1.md
  - CAMPAIGN_CHARTER_REASONING.md
  - OVERNIGHT_GOAL.md
  - CYCLE_0_WORK_ORDER.md
  - AUDIT_FINDINGS_LEDGER.md
  - reports/INGEST_REPORT.md
  - MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md
  - ledger/prompts/OWNER_MARCHING_ORDERS.md
  - ledger/ORCHESTRATION_STATE.md
  - DISPUTES.md
  - constitution/MONKEYBEE_CONSTITUTION_v8.md
  - constitution/SPECCARD_PIPELINE.md
  - decisions/DECISION_INDEX.md
  - decisions/DEFERRED_REGISTER.md
  - decisions/D1_CONTENT_HASH.md
  - decisions/D2_CANONICAL_SERIALIZATION.md
  - decisions/D3_DECODED_STREAM_IDENTITY.md
  - decisions/D4_EVIDENCE_CHECKER_ISOLATION.md
  - decisions/D5_PROJECT_LICENSE.md
  - decisions/D6_LEDGER_BACKEND.md
  - decisions/D7_RUST_TOOLCHAIN_PIN.md
  - ledger/owners/G1_STATE.md
  - ledger/owners/G2_STATE.md
status: DRAFT
evidence-status: provisional-pending-substrate
owner: G3
owner-fsm: SUBMIT-FOR-REVIEW
---

# G3 Owner Checkpoint

## Current checkpoint

- Timestamp: `2026-07-14T17:37:01+02:00`
- Phase: `SUBMIT-FOR-REVIEW`
- Active goal: author the self-contained Cycle 1-only delta plan and stop at `SUBMIT-FOR-REVIEW`.
- Exclusive writable paths: `plans/CYCLE_1_DELTA_PLAN.md` and `ledger/owners/G3_STATE.md`.
- Partial output: `plans/CYCLE_1_DELTA_PLAN.md`, 3,091 lines at this SELF-CHECK checkpoint; the full contract catalog/specifications, workflows, fuzz/gate surface, exclusions, cross-owner decision labels, R0 card-registry crosswalk, and trial-ledger contract are on disk.
- Branch observation: work is on `main`. Current repository status also exposes cross-owner untracked `CAMPAIGN_CHARTER_REASONING_v1.1.md`, `CYCLE_0_WORK_ORDER_v1.1.md`, `MONKEYBEE_CAMPAIGN_CHARTER_v1.1.md`, and `ledger/owners/G6_STATE.md`; G3 did not inspect them as authority or modify, stage, or reconcile them.
- External fetches: none.
- Sub-agent activity: none; G3 remains the sole owner and will not route its own review.

## Files read in the required order

1. `AGENTS.md` — full file, including the G0 navigation and evidence-hygiene extension.
2. `INDEX.md` — full file; treated as navigation rather than authority.
3. `MONKEYBEE_CAMPAIGN_CHARTER_v1.md` — full file.
4. `OVERNIGHT_GOAL.md` — full file.
5. `CYCLE_0_WORK_ORDER.md` — full file.
6. `AUDIT_FINDINGS_LEDGER.md` — full file.
7. `ledger/prompts/OWNER_MARCHING_ORDERS.md` — full shared contract and G3 section.

Additional INGEST references read and classified before DRAFT entry:

- `/home/joseph/.codex/skills/planning-workflow/SKILL.md` — full skill; Beads conversion portions deferred by the overnight exception.
- `DISPUTES.md` — full file; D-001 through D-003 preserved.
- `reports/INGEST_REPORT.md` — full file; Grade-A verification and source-unavailable findings ingested without strengthening them.
- `CAMPAIGN_CHARTER_REASONING.md` — full file; C1 boundary and graceful-degradation rationale ingested.
- `ledger/ORCHESTRATION_STATE.md` — routing snapshot only; it is operational rather than campaign authority.
- `MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md` — targeted stable sections: §§0.3–0.6, 1–6, 8–16.6, 25.1–25.8, 26, 27–30.11, 31.1, 32 risk rows relevant to C1, 35–35.1, and Appendices A–C relevant to source, work, outcomes, decoding, checking, reports, and contracts.

Cross-owner artifacts read before SELF-CHECK:

- `DISPUTES.md` D-004 and D-005 were reread after they appeared. `DecodedContainerId` is the sole domain-canon class; `DecodedStreamId` appears only as the higher-layer drift label. Runtime dependency policy and cryptographic providers remain symbolic and implementation-unavailable pending human routing/ratification.
- `decisions/D1_CONTENT_HASH.md`, `D2_CANONICAL_SERIALIZATION.md`, `D3_DECODED_STREAM_IDENTITY.md`, `D4_EVIDENCE_CHECKER_ISOLATION.md`, `D5_PROJECT_LICENSE.md`, `D6_LEDGER_BACKEND.md`, and `D7_RUST_TOOLCHAIN_PIN.md` — each read in full without combined-output truncation.
- `decisions/DECISION_INDEX.md`, `decisions/DEFERRED_REGISTER.md`, and `ledger/owners/G2_STATE.md` — each read in full. All defaults remain `PROPOSED — awaiting human ratification`.
- `constitution/SPECCARD_PIPELINE.md` — full file; `MB-SC-R0-001` through `MB-SC-R0-040` remain empty `PENDING-LICENSED-SOURCE` slots.
- `constitution/MONKEYBEE_CONSTITUTION_v8.md` — full file read in non-truncating chunks; it is a proposed extraction candidate and does not supersede Rev 7 before human ratification and commitment.
- `ledger/owners/G1_STATE.md` — reread after G1 reached `SUBMIT-FOR-REVIEW`; its artifacts are `PROPOSED` and remain provisional pending human ratification/review.

## Authority and classification

- Live human instructions control this owner run.
- The Charter set controls C1 scope, campaign staging, evidence gates, and exclusions.
- Rev 7 remains read-only domain canon until a Constitution or shell artifact supersedes a section through the authorized extraction.
- Generated Constitution, decision, report, and owner-state artifacts remain provisional and cannot silently strengthen canon.
- The requested plan and this checkpoint are generated campaign/operational artifacts, not new canonical authority.

## Locked scope decisions

- Plan space only: no Beads, pseudo-bead inventory, source code, build/config scaffolding, implementation, commit, or push.
- No prohibited PDF-processor source or documentation contact.
- No competitor comparison, artifact acquisition, benchmark execution, or new measurement.
- No SpecCard semantic bodies. Every contract carries registry/slot citations marked exactly `PENDING-LICENSED-SOURCE`.
- Project-authored plan-level semantics and stable Rev 7 section identifiers may be used; unverifiable content is marked `[UNVERIFIED]`.
- The plan covers the entire C1 L0-L2 surface, immune system, CLI, fuzzing, and close gate, with explicit later-cycle exclusions.
- Every atomic capability will have a stable consequence-contract ID and all fields mandated by the G3 marching order.
- Dependencies will be expressed as prose and contract links, not an execution-task inventory.
- Recovery alternatives, partial outcomes, signature-structure discovery, attacker-keyed hashing, canonicalization budgets, credential secrecy, cancellation, and no-claim boundaries are first-class.
- G2 recommendations, if available, remain proposed defaults awaiting human ratification.
- Stop condition for this turn is `SUBMIT-FOR-REVIEW`; G3 will not self-route reviewers or enter `REVISE`.

## Unavailable or not-yet-ingested inputs

- `ALIEN_ARTIFACT.md`: `SOURCE-UNAVAILABLE` per `INDEX.md`; relevant to audit row R2-N7, not a substitute source for G3.
- `PROJECT_OVERVIEW.md`: `SOURCE-UNAVAILABLE` per `INDEX.md`; relevant to audit row R2-N8, not a substitute source for G3.
- Constitution v8, the SpecCard pipeline, and G2 decision artifacts were absent at DRAFT entry but later appeared and were reconciled at their stated provisional status. The shell corpus also appeared, but G3 did not substitute it for the kernel/domain authority already read; the draft Constitution stable sections and G2 outputs were the cross-owner evidence required for this plan.

## Open risks

1. G1/G2 outputs remain proposed. No extracted kernel text, decision default, toolchain, project license, ledger backend, runtime dependency policy, or cryptographic provider is human-ratified by this artifact.
2. Every R0 SpecCard remains an empty `PENDING-LICENSED-SOURCE` slot. Normative implementation stays unavailable until licensed extraction and two-person meaning review.
3. `ALIEN_ARTIFACT.md` and `PROJECT_OVERVIEW.md` remain `SOURCE-UNAVAILABLE`; their dependent audit rows cannot be reconstructed from related files.
4. The human-established commitment substrate and independently stewarded held-out seal are absent. The ordinary R0 wedge can degrade gracefully, but campaign closure cannot pass without them.
5. This owner self-check is not a fresh review. Root must route an independent finding packet before G3 can enter `REVISE`.

## DRAFT reconciliation decisions saved

- D1/D2 remain a coupled proposal. The plan exposes the proposed SHA-256/full-width plus deterministic-CBOR package only with an awaiting-ratification label; the first external or tamper-evident commitment is blocked until human ratification.
- D3 is represented as one recipe `DecodedContainerId` plus a post-commit `DecodedArtifactDigest`, with planned/materialized/transient-no-digest/refused states and verification on durable reuse.
- D4's proposed code/authorship/specification isolation and seeded-defect measurement are carried into checker contracts and the close record; the canonical encoder is not shareable.
- D5, D6, and D7 are visible as proposals at their dependency, ledger, and toolchain use sites. D-005 continues to block runtime dependency-policy and cryptographic-provider selection.
- `C1.CC.IMM.017@1` now owns the gate-bearing trial record and distinguishes a local hash chain from an independently held commitment substrate.
- G1's actual R0 slot IDs are crosswalked without adding a semantic body or treating the crosswalk as sufficient card coverage.

## SELF-CHECK repairs saved

- Reconciled the final G1/G2 artifacts at `PROPOSED`/`SUBMIT-FOR-REVIEW` status without treating them as ratified authority.
- Added the actual `MB-SC-R0-001` through `MB-SC-R0-040` registry crosswalk while keeping every semantic body absent.
- Bound D3 to the sole `DecodedContainerId` recipe class and separate post-commit `DecodedArtifactDigest`; the other spelling remains only the D-004 higher-layer alias-drift label.
- Expanded the D4 isolation axes, seeded-defect falsifiers, trial-record evidence, and human-review horizon without self-awarding independence.
- Added `C1.CC.FDN.016@1` for safe-Rust/unsafe-capsule admission and `C1.CC.IMM.017@1` for the prospective C1 trial record.
- Removed every detected contract-dependency cycle across foundation, revision/filter/security/document, report/immune, CLI, and fuzz relations. Replaced ambiguous same-family and generic downstream prerequisites with explicit acyclic registry or contract inputs.
- Separated capability-manifest generation from downstream truth checks, report-schema generation from manifest validation, and evidence-package production from standalone checking.
- Preserved strict-before-recovery, encrypted-object-stream one-time decryption, transactional plaintext publication, and report/ledger/commitment boundaries during dependency repair.

## SELF-CHECK evidence

| Check | Reproducible result |
|---|---|
| Catalog/spec parity | 118 catalog entries, 118 unique catalog IDs, 118 unique specification blocks, and zero catalog-only/spec-only IDs. |
| Contract grammar | Every one of 118 blocks has exactly one of all 17 mandated fields; every Card-slots field contains `PENDING-LICENSED-SOURCE`. |
| Reference closure | All 118 unique full contract references and all 118 unique shorthand contract references resolve to the closed catalog. |
| Dependency soundness | UTF-8-aware range expansion plus topological sorting over explicit dependency clauses exits successfully with no cycle; same-family generic prerequisites were also reviewed and made explicit. |
| Goal scope | A 42-item matrix covers byte snapshots, syntax/COS/xref/revisions/object streams, all named lossless filters/predictors, bounded recovery, standard-handler credentialed reads, identity/evidence/reports/checker, immune system, CLI, fuzz/panic gate, clause tagging, close gate, first-class risks, and exclusions; zero items are missing. |
| G1/G2 status | All D1–D7 defaults remain visibly awaiting ratification at their blocking uses; D-005 runtime and cryptographic providers remain symbolic and implementation-unavailable. |
| Commitment ordering | D1/D2 ratification is an explicit prerequisite for the first external or tamper-evident commitment and for package/ledger identity activation. |
| Decoded identity | `DecodedContainerId` is the sole domain-canon class; `DecodedStreamId` occurs only in the D-004 decision-row and obscure-slice alias-drift warnings, never as a second type. |
| Clean-room/card boundary | No prohibited processor name occurs in either G3-owned file; no card semantic body, external fetch, artifact acquisition, comparison run, or benchmark result was introduced. |
| Claim vocabulary | Case-insensitive hits are limited to the formal scoped `Complete` outcome, the required formal `best_outcomes` field, and explicit no-supremacy enforcement text. |
| Provenance/unknowns | Both owned files carry provenance/status headers; unavailable sources are recorded; the one exact graph-complexity label not evidenced by an approved source is `[UNVERIFIED]`. |
| Formatting/size | Plan is 3,091 lines, within the 2,500–4,000 target; four code fences are balanced; no tabs, trailing whitespace, or heading-spacing defects occur in either owned file. |
| File scope | G3 changed only its two exclusive paths on `main`; no Beads, pseudo-bead inventory, code/config scaffold, external action, commit, or push occurred. |

## Next transition condition

Stop at `SUBMIT-FOR-REVIEW`. Root may route fresh reviewers under the declared lenses. G3 may enter `REVISE` only after a fresh finding packet is persisted and routed; it must not self-review, self-route, implement, convert to Beads, commit, or push.

## Transition history

| Timestamp | From | To | Evidence saved |
|---|---|---|---|
| `2026-07-14T16:29:51+02:00` | start | `INGEST` | Required reading record, scope lock, risks, unavailable inputs, and next condition persisted in this file. |
| `2026-07-14T16:35:52+02:00` | `INGEST` | `DRAFT` | A 309-line provenance-bearing partial plan, closed contract namespace, clean-room boundary, symbolic decision dependencies, and dependency spine were persisted. |
| `2026-07-14T17:11:47+02:00` | `DRAFT` | `SELF-CHECK` | A 3,069-line plan with every cataloged contract drafted, G1/G2 evidence reconciled at provisional status, D-004/D-005 enforced, and the DRAFT checkpoint persisted. |
| `2026-07-14T17:37:01+02:00` | `SELF-CHECK` | `SUBMIT-FOR-REVIEW` | Final 3,091-line plan persisted after 118/118 catalog/spec/card parity, exact 17-field coverage, closed references, UTF-8-aware acyclic dependency check, 42/42 scope checks, policy/claim/provider guards, and formatting/file-scope checks passed. |
