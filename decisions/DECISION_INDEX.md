---
generated-by: Claude G2 owner (claude-opus-4-8, effort xhigh)
date: 2026-07-14
revised-by: Codex G2 owner
revised-date: 2026-07-16
inputs:
  - decisions/D1_CONTENT_HASH.md
  - decisions/D2_CANONICAL_SERIALIZATION.md
  - decisions/D3_DECODED_STREAM_IDENTITY.md
  - decisions/D4_EVIDENCE_CHECKER_ISOLATION.md
  - decisions/D5_PROJECT_LICENSE.md
  - decisions/D6_LEDGER_BACKEND.md
  - decisions/D7_RUST_TOOLCHAIN_PIN.md
  - decisions/DEFERRED_REGISTER.md
  - ledger/owners/G6_STATE.md dispositions R19-A04 and R21-A08 (operational disposition evidence only)
  - CYCLE_0_WORK_ORDER_v1.1.md §4.1 (PROPOSED routing overlay; not governing canon)
status: PROPOSED
evidence-status: provisional-pending-substrate
audience: G3 (Cycle 1 delta plan) and the human ratification queue
---

# Decision Index

A compact map of the seven resolve-now decisions, for the C1 delta-plan author and for the morning ratification queue.

## Read this first

**Every default below is PROPOSED. None is ratified.** Rev 7 §29.9 reserves architectural constitution, high-consequence security decisions, legal interpretation, and the selection of genuinely independent evidence to humans. G2 proposes; the human decides.

For G3: build the C1 plan against these defaults, and **label every dependency on them as awaiting ratification** at the point of use — not once in a preface. A plan that silently hard-codes an unratified default is how a proposal becomes a decision without anyone making it.

**Post-submission routing boundary.** Admitted R19-A04 and R21-A08 owner dispositions establish that Work Order v1.0 routes only 12 of Rev 7 §35's 83 rows. `CYCLE_0_WORK_ORDER_v1.1.md` proposes an 83-row routing overlay but remains `PROPOSED — awaiting human ratification`. The seven briefs below are still only the original resolve-now set; they neither ratify nor erase the other unresolved rows. `DEFERRED_REGISTER.md` records this boundary for MORNING_REPORT disclosure.

## The seven

| # | Decision | Proposed default (one line) | Blast radius if wrong | Reversibility |
|---|---|---|---|---|
| **D1** | Content-hash algorithm and digest widths | **SHA-256, full 256-bit digests**, in an algorithm-versioned registry; legacy MD5/RC4/SHA-1 fenced to PDF semantics only, never project identity | Every identity, receipt, cache key, and commitment | Technically high (migration is designed for) — but **a digest already committed to the external substrate cannot be re-hashed** |
| **D2** | Canonical serialization grammar for hashing | **Deterministic-CBOR profile** + mandatory domain separation and length framing; floats forbidden; refuse rather than guess; **encoder dual-implemented** | Grammar ambiguity manufactures false identity equality — silent, catastrophic | Moderate; ambiguous historical values cannot be safely migrated |
| **D3** | Decoded-container identity (Work Order's "DecodedStreamId") | **Hybrid:** recipe identity (`DecodedContainerId`, pre-decode, metadata-only) + sensitive content digest (`DecodedArtifactDigest`, post-commit, verified on reuse) | Recipe-only + durable caching → wrong bytes under a valid identity, silently; digest disclosure can create a confirmation oracle | High, except for evidence already produced under recipe-only reuse |
| **D4** | Evidence-checker isolation | **Code + human-accepted authorship-family classification + specification isolation + separated pre-run/trial/post-trial records**, with seeded-defect observations; human adversarial review proposed by C4 | Checker-backed Q3 evidence; a premise-sharing checker can bless producer bugs (the F-01 pattern) | Structurally reversible; prior checker-backed evidence requires re-verification and claim-lapse handling |
| **D5** | Project license | **MIT OR Apache-2.0 (dual), subject to counsel**; contribution instrument chosen before outside contributions; dependency-license policy remains separate GAP-2 | Distribution, rights history, and Q2 `FieldDefinitionId` coherence | Path-dependent on verified grants and rightsholders; no direction is pre-characterized as easy or one-way |
| **D6** | Persistent ledger backend | **Hash-chained append-only JSONL per-writer shards** + canonical shard-head manifest committed externally + derived regenerable index | Q3 provenance representation, shard inclusion, and chronology integrity | Designed for versioned migration, which still needs a lossless test; omitted prospective events cannot be upgraded from retrospective evidence |
| **D7** | Rust toolchain pin | **Exact stable for release artifacts** + date-pinned nightly only for locally verified assurance needs; edition 2024; toolchain is a determinism input | D0/D1/D2 replayability; assurance-lane availability; reproducible-build inputs | Technically high; receipts issued *before* a pin are permanently unreplayable |

## Couplings G3 must respect

1. **D1 + D2 are one package, not two knobs.** The recommended package is SHA-256 + a first-party-pinned deterministic-CBOR profile. The alternative candidate is an exact 256-bit SP 800-185 TupleHash profile + a separate structured-value encoding. TupleHash is itself a hash construction, not a framing wrapper around SHA-3, SHAKE, or SHA-256. The alternative remains `[UNVERIFIED]` until its parameter and implementation evidence is supplied.
2. **D2 → D4.** The canonical encoder is the one component that must **not** be shared between producer and checker, because a shared encoder makes an encoding ambiguity invisible to the checker. Its dual implementation and their differential test are C1 acceptance criteria.
3. **D3 → D1 + D2.** The recipe identity is a canonically encoded tuple hashed with the D1 algorithm; it cannot be specified ahead of them.
4. **D6 → D1 + D2.** Typed ledger records and shard-head manifests are canonically encoded and hash-chained. Multiple shards have no singular head; the externally committed canonical manifest binds every admitted shard. Timestamps do not prove global order.
5. **D5 → the Q2 field.** `FieldDefinitionId` (§9.2) includes "openness/channel/license" in the comparator field's eligibility boundary, so the license and the day-zero discovery-protocol commitment must be settled coherently. Neither silently ratifies or must be tuned around the other.

## What C1 must assume, and how to label it

| C1 component | Assumes | Label to carry in the plan |
|---|---|---|
| Identity/evidence/report/checker stack | D1 (SHA-256), D2 (deterministic-CBOR profile) | "PROPOSED default — awaiting ratification (D1/D2). If the alternative package is ratified, the hash construction and structured-value grammar change together." |
| Filters, decoders, object streams | D3 (hybrid identity + availability states) | "PROPOSED default — awaiting ratification (D3). Canonical name is `DecodedContainerId` per Rev 7 §9.2; `DecodedStreamId` is a campaign-layer alias, see F-G2-1." |
| `mb-checker` | D4 (human-accepted authorship-family class + spec-only authorship + separate pre-run/trial/post-trial records) | "PROPOSED default — awaiting ratification (D4). Addresses audit row R1-9; checker failure blocks only claims that require checker support." |
| Fuzz targets, zero-reachable-panics gate | D7 (pinned assurance toolchain; nightly only if locally required) | "PROPOSED default — awaiting ratification (D7); nightly need remains `[UNVERIFIED]` until local tool admission." |
| Dependency choices (Flate, LZW, RC4/AES/MD5/SHA) | **Unrouted gap — GAP-2** | "Dependency policy is `PENDING HUMAN ROUTING` (GAP-2). Name no crate as a committed choice; illustrate only, and mark illustrations as such." |

## Do not build on these (deferred — guards from `DEFERRED_REGISTER.md`)

C1 through C5 must not assume answers to any of these. A guard violated is a Grade-A finding at the next cycle-close drift audit, not an accomplished fact.

- **GPU/raster backend (C6):** no API, trait, or schema shaped around a GPU path existing.
- **PDF/A-1 writer profile (C6):** no C1–C5 work assumes a PDF 1.4 writer profile; the writer's version/profile contract stays parameterized.
- **C-ABI freeze (post-R4):** no public Rust type shaped for FFI convenience; the C5 preview is not a compatibility commitment and must say so at its surface.
- **Base-font fallback (C3):** no silent font substitution, ever — substitution-or-refusal receipts only; no font vendored before its license is reviewed.
- **S6 performance metric (C7):** no optimization bypasses a safety contract, budget, or evidence obligation; C2's benchmark tracking is regression detection and is never reported as a supremacy measurement.
- **MSRV (GAP-1, C1-close):** none advertised until declared.

## Ratification queue (for `MORNING_REPORT.md`)

Proposed handling order based on the explicit dependency and timing boundaries below. No quantitative cost ranking has been measured, and the human may reorder it.

| Priority | Item | Why it is urgent |
|---|---|---|
| 1 | **D1 + D2 as a package** | **Ordering constraint (F-G2-3):** Charter §10 makes the Charter the first artifact committed to the tamper-evident substrate, and its hash the first ledger entry. A committed digest cannot be re-hashed without destroying its timestamp semantics — so the algorithm must be ratified **before the first substrate commitment**, not merely before C1 code. |
| 2 | **D5 — license and contribution-rights path** | Counsel and the human must define the grants before outside contributions are accepted; this brief does not infer what DCO, CLA, or project-license terms preserve. |
| 3 | **D4** | Checker-backed evidence starts in C1. If premise sharing is later found, affected evidence requires re-verification and claim-lapse handling; sealed records are not silently rewritten. |
| 4 | **D6** | The ledger must be *open* before the first implementation agent runs (Charter §3.1). A storage format can migrate; absent prospective events cannot be upgraded from retrospective evidence. |
| 5 | **D7** | The exact stable pin remains a human input and precedes the first replayable determinism receipt. |
| 6 | **D3** | Needed for the C1 decoder surface; depends on D1/D2 being settled first. |
| 7 | **GAP-2 routing** (dependency policy) | G3 can remain symbolic, but C1 dependency admission cannot proceed until the policy and provider routes are human-resolved. |

## Files

| File | Contents |
|---|---|
| `D1_CONTENT_HASH.md` | Content-hash algorithm and digest widths |
| `D2_CANONICAL_SERIALIZATION.md` | Canonical serialization grammar for hashing |
| `D3_DECODED_STREAM_IDENTITY.md` | Decoded-container identity: cost and availability model |
| `D4_EVIDENCE_CHECKER_ISOLATION.md` | Evidence-checker isolation (audit row R1-9) |
| `D5_PROJECT_LICENSE.md` | Project license and contribution instrument; GAP-2 dependency policy remains separately routed |
| `D6_LEDGER_BACKEND.md` | Persistent ledger backend |
| `D7_RUST_TOOLCHAIN_PIN.md` | Rust toolchain pin |
| `DEFERRED_REGISTER.md` | The five deferred decisions, their guards, and two identified gaps |
