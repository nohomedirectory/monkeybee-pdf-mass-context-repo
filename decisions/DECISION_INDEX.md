---
generated-by: Claude G2 owner (claude-opus-4-8, effort xhigh)
date: 2026-07-14
inputs:
  - decisions/D1_CONTENT_HASH.md
  - decisions/D2_CANONICAL_SERIALIZATION.md
  - decisions/D3_DECODED_STREAM_IDENTITY.md
  - decisions/D4_EVIDENCE_CHECKER_ISOLATION.md
  - decisions/D5_PROJECT_LICENSE.md
  - decisions/D6_LEDGER_BACKEND.md
  - decisions/D7_RUST_TOOLCHAIN_PIN.md
  - decisions/DEFERRED_REGISTER.md
status: PROPOSED
evidence-status: provisional-pending-substrate
audience: G3 (Cycle 1 delta plan) and the human ratification queue
---

# Decision Index

A compact map of the seven resolve-now decisions, for the C1 delta-plan author and for the morning ratification queue.

## Read this first

**Every default below is PROPOSED. None is ratified.** Rev 7 §29.9 reserves architectural constitution, high-consequence security decisions, legal interpretation, and the selection of genuinely independent evidence to humans. G2 proposes; the human decides.

For G3: build the C1 plan against these defaults, and **label every dependency on them as awaiting ratification** at the point of use — not once in a preface. A plan that silently hard-codes an unratified default is how a proposal becomes a decision without anyone making it.

## The seven

| # | Decision | Proposed default (one line) | Blast radius if wrong | Reversibility |
|---|---|---|---|---|
| **D1** | Content-hash algorithm and digest widths | **SHA-256, full 256-bit digests**, in an algorithm-versioned registry; legacy MD5/RC4/SHA-1 fenced to PDF semantics only, never project identity | Every identity, receipt, cache key, and commitment | Technically high (migration is designed for) — but **a digest already committed to the external substrate cannot be re-hashed** |
| **D2** | Canonical serialization grammar for hashing | **Deterministic-CBOR profile** + mandatory domain separation and length framing; floats forbidden; refuse rather than guess; **encoder dual-implemented** | Grammar ambiguity manufactures false identity equality — silent, catastrophic | Moderate; **worse than D1** — ambiguous values cannot be safely migrated at all |
| **D3** | Decoded-container identity (Work Order's "DecodedStreamId") | **Hybrid:** recipe identity (`DecodedContainerId`, pre-decode, cheap) + content digest (`DecodedArtifactDigest`, post-commit, verified on reuse) | Recipe-only + durable caching → wrong bytes under a valid identity, silently | High — the most reversible of the identity-adjacent set |
| **D4** | Evidence-checker isolation | **Code + authorship (different model family) + specification isolation + measured seeded-defect detection rate**, from C1; human adversarial review by C4 | The entire Q3 evidence chain; a premise-sharing checker blesses the producer's bugs (the F-01 pattern) | Structurally reversible; **evidentially not** — evidence produced under a compromised checker must be re-verified and its claims lapse |
| **D5** | Project license | **MIT OR Apache-2.0 (dual)** + runtime dependency-license allowlist; **DCO vs CLA must be decided now** | Adoption, patent exposure, and — non-obviously — Q2 `FieldDefinitionId` eligibility | License: moderate. **Permissive → copyleft is effectively one-way** once outside contributions land |
| **D6** | Persistent ledger backend | **Hash-chained append-only JSONL** (per-writer shards) as source of truth + derived regenerable index | Independent readability of the Q3 provenance record | **Highest in the set.** The real risk is a *late* ledger, not a wrong one |
| **D7** | Rust toolchain pin | **Two pinned toolchains by package role:** exact stable (runtime/release) + date-pinned nightly (fuzz/Miri/sanitizer lanes only); edition 2024; toolchain is a determinism input | D0/D1/D2 replayability; the C1 fuzz gate; reproducible builds | Technically high; receipts issued *before* a pin are permanently unreplayable |

## Couplings G3 must respect

1. **D1 + D2 are one package, not two knobs.** The recommended package is SHA-256 + deterministic-CBOR framing. The coherent alternative is SHA3-256/SHAKE256 + TupleHash framing. Mixing across packages is not offered. If the human ratifies the alternative, **both** briefs change together — plan accordingly and do not bind C1 text to the hash family in more places than necessary.
2. **D2 → D4.** The canonical encoder is the one component that must **not** be shared between producer and checker, because a shared encoder makes an encoding ambiguity invisible to the checker. Its dual implementation and their differential test are C1 acceptance criteria.
3. **D3 → D1 + D2.** The recipe identity is a canonically encoded tuple hashed with the D1 algorithm; it cannot be specified ahead of them.
4. **D6 → D1 + D2.** Ledger records are canonically encoded and hash-chained. The D2 ambiguity analysis applies to ledger records exactly as it applies to identities.
5. **D5 → the Q2 field.** `FieldDefinitionId` (§9.2) includes "openness/channel/license" in the comparator field's eligibility boundary, so the license and the day-zero discovery-protocol commitment must be settled coherently — the license first.

## What C1 must assume, and how to label it

| C1 component | Assumes | Label to carry in the plan |
|---|---|---|
| Identity/evidence/report/checker stack | D1 (SHA-256), D2 (deterministic-CBOR profile) | "PROPOSED default — awaiting ratification (D1/D2). If the alternative package is ratified, the hash family and framing change together." |
| Filters, decoders, object streams | D3 (hybrid identity + availability states) | "PROPOSED default — awaiting ratification (D3). Canonical name is `DecodedContainerId` per Rev 7 §9.2; `DecodedStreamId` is a campaign-layer alias, see F-G2-1." |
| `mb-checker` | D4 (different model family + spec-only authorship + seeded-defect trial) | "PROPOSED default — awaiting ratification (D4). Addresses audit row R1-9." |
| Fuzz targets, zero-reachable-panics gate | D7 (nightly assurance lane) | "PROPOSED default — awaiting ratification (D7)." |
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

Ordered by the cost of getting it wrong, not by the order the Work Order lists them.

| Priority | Item | Why it is urgent |
|---|---|---|
| 1 | **D1 + D2 as a package** | **Ordering constraint (F-G2-3):** Charter §10 makes the Charter the first artifact committed to the tamper-evident substrate, and its hash the first ledger entry. A committed digest cannot be re-hashed without destroying its timestamp semantics — so the algorithm must be ratified **before the first substrate commitment**, not merely before C1 code. |
| 2 | **D5 — the DCO/CLA instrument** | The relicensing option expires quietly, with no event to mark it, the first time an external contribution lands under a bare permissive license. Nothing else in the set has a deadline that passes by inattention. |
| 3 | **D4** | Must be right from C1. Evidence produced under a premise-sharing checker cannot be rehabilitated; sealed cycle trial records containing its verdicts cannot be quietly amended. |
| 4 | **D6** | Not hard to choose — but the ledger must be *open* before the first implementation agent runs (Charter §3.1). A late ledger is unrecoverable; a wrong backend is a migration. |
| 5 | **D7** | Cheap to ratify; blocks the first replayable determinism receipt. |
| 6 | **D3** | Needed for the C1 decoder surface; depends on D1/D2 being settled first. |
| 7 | **GAP-2 routing** (dependency policy) | G3's C1 plan cannot fully specify its decoder and decryption surface without it. |

## Files

| File | Contents |
|---|---|
| `D1_CONTENT_HASH.md` | Content-hash algorithm and digest widths |
| `D2_CANONICAL_SERIALIZATION.md` | Canonical serialization grammar for hashing |
| `D3_DECODED_STREAM_IDENTITY.md` | Decoded-container identity: cost and availability model |
| `D4_EVIDENCE_CHECKER_ISOLATION.md` | Evidence-checker isolation (audit row R1-9) |
| `D5_PROJECT_LICENSE.md` | Project license, contribution instrument, dependency allowlist |
| `D6_LEDGER_BACKEND.md` | Persistent ledger backend |
| `D7_RUST_TOOLCHAIN_PIN.md` | Rust toolchain pin |
| `DEFERRED_REGISTER.md` | The five deferred decisions, their guards, and two identified gaps |
