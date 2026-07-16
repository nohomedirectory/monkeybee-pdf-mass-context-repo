---
generated-by: Claude G2 owner (claude-opus-4-8, effort xhigh)
date: 2026-07-14
revised-by: Codex G2 owner
revised-date: 2026-07-16
inputs:
  - CYCLE_0_WORK_ORDER.md §4 resolve-now item 1
  - MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md §9.1.1, §9.2, §9.6, §16.1, §16.1.1, §11.9, §33.4, §35
  - MONKEYBEE_CAMPAIGN_CHARTER_v1.md §10
  - AUDIT_FINDINGS_LEDGER.md R1-9
  - ledger/CANONICAL_HASHES.md
  - NIST CSRC primary pages for FIPS 180-4, FIPS 202, SP 800-185 (see G2_STATE fetch record)
status: PROPOSED
evidence-status: provisional-pending-substrate
decision-id: D1
ratification: PROPOSED — awaiting human ratification
couples-with: D2 (canonical serialization grammar) — choose as one package, not two knobs
---

# D1 — Content-hash algorithm and digest widths

## The question

Which hash algorithm, at which digest width, names every content-addressed identity in the MonkeyBee kernel?

## Why this resolves at Cycle 0

Every identity in Rev 7 §9.2 is content-addressed, and §9.1.1's `SourceIdentity::VerifiedContent { algorithm, digest, len }` consumes the answer directly. Nothing in the kernel can be built without it. Rev 7 §9.2 states the law the algorithm must satisfy:

> Content-addressed identities use a project-wide versioned grammar with class/version domain separation, length framing, a named hash algorithm, canonical encodings, and collision quarantine. A digest is an index — not authority, authorization, or proof of semantic interchangeability.

Rev 7 never names the algorithm. `HashAlgorithm` appears once, as a type placeholder in §9.1.1; no hash function is named anywhere in the plan. The option space below is therefore constructed from first principles against the constraints canon does state, not selected from a canon default.

**Two hash namespaces must not be conflated.** PDF's own cryptography forces MD5 (standard security handler) and the SHA-2 family (AESV3 / revision-6 key derivation) into the implementation; §16.1 admits these as legacy and standards compatibility. That is a *PDF semantics* obligation. This decision concerns MonkeyBee's *own* identity grammar — the algorithm that names `SourceRootId`, `DocumentViewId`, `DerivationId`, receipts, and evidence packages. The two namespaces are separate, and an algorithm admitted for PDF compatibility is never thereby admitted for project identity.

## Constraints canon already fixes

| Constraint | Source | Consequence for this decision |
|---|---|---|
| The identity grammar is already algorithm-versioned | §9.2 ("algorithm-versioned identities"), §9.1.1 (`algorithm` is a field) | Migration is a designed-for operation, not a catastrophe. This lowers the cost of being wrong — but see the substrate exception below. |
| Same-identifier/different-content observations quarantine both records; "first writer wins" is forbidden | §9.2 | The system must survive a collision observation without corrupting state. Collision resistance is required, but the design does not *assume* it. |
| A digest is an index, not authority | §9.2 | The digest is not used as a MAC or a capability. This materially changes which weaknesses matter (below). |
| MonkeyBee does not invent primitives; it uses audited, permissively licensed, pure-Rust implementations | §16.1 | Rules out anything exotic or self-implemented. |
| The evidence checker is independently implemented and receives raw hostile bytes | §35 checker-isolation row, Appendix A.13, audit row R1-9 | The identity algorithm must have a separately evidenced implementation and verification path for the checker and external adjudicator. Cost and stock-tool availability are evidence questions, not assumptions. |

That row changes the selection criterion. Here, the artifact's *purpose* is to be checked by someone who does not trust us (Charter §7: "Independence"; §33). An identity algorithm that a third-party reviewer cannot readily recompute imposes friction on precisely the party whose independence the campaign's Q3 verdict depends on. Independent reproducibility is therefore a stated criterion; no throughput ranking is asserted in this plan-space brief.

## Options

### Option A — SHA-256 (FIPS 180-4 family), 256-bit digests

- **For:** The consulted NIST page identifies SHA-256 within FIPS 180-4, and this checkout can reproduce ordinary SHA-256 file digests with `sha256sum`. Those facts support a low-friction local verification path. Cross-platform availability, hardware acceleration, current Rust implementation quality/licensing, buyer requirements, and third-party tooling prevalence are `[UNVERIFIED]` here and must not carry the recommendation without the named dependency and buyer checks below.
- **Against:** Merkle–Damgård construction, therefore vulnerable to length-extension. The relevance of this is bounded and must be stated precisely rather than waved at: length-extension is exploitable when a digest is used as a MAC over `secret || message`. MonkeyBee's digests are content identity, never MACs, never authority (§9.2). The residual risk is *ambiguity*, not length-extension: hashing concatenated fields without framing lets two different structures produce one digest. That risk is eliminated by D2's framing grammar, not by the hash choice — and it would exist with any hash function.
- **Standards status:** FIPS 180-4 is the Secure Hash Standard. NIST announced (2023-03-07) a decision to revise it. The algorithms are not withdrawn; the document is under revision. Whether a revised document has since published is `[UNVERIFIED]` and is a counsel/first-party verification step below.

### Option B — SHA-512/256 (truncated SHA-512, same standard)

- **For:** Truncation changes the length-extension surface; exact security and approval characterization remains subject to the cited standard. Relative performance and hardware behavior are `[UNVERIFIED]` and receive no decision credit here.
- **Against:** `sha256sum` does not reproduce SHA-512/256 directly in the locally demonstrated path. Broader tooling prevalence and relative software performance are `[UNVERIFIED]`. Its length-extension properties do not remove D2's requirement for an injective structured-value encoding.

### Option C — A 256-bit SP 800-185 TupleHash profile

- **For:** SP 800-185's **TupleHash** is, per NIST's own page, "designed to hash tuples of input strings unambiguously." It is therefore a candidate standardized tuple-hash construction for the §9.2 framing requirement.
- **Against:** TupleHash is itself the hash construction; it is **not** a framing wrapper that can be placed around SHA3-256, SHAKE256, or SHA-256. D2 would still need a separate, injective encoding for nested typed values before their byte strings become TupleHash inputs. The exact TupleHash function/parameter profile, tooling availability, Rust implementation support, independent-checker implementation path, and relative performance are `[UNVERIFIED]` until checked against the first-party specification and admitted dependencies. No benchmark is performed here.
- **Status:** The consulted NIST pages identify FIPS 202 as final (Aug 2015) and SP 800-185 as final (Dec 2016); the FIPS 202 page carries a 2025-03-13 update-planning note. Whether later publications or parameter guidance exist is `[UNVERIFIED]` here.

### Option D — BLAKE3

- **For:** Its tree, keyed, derivation, and extendable-output characteristics are candidate engineering benefits, but those characterizations and their relevance are `[UNVERIFIED]` in this brief.
- **Against for the present decision:** This brief carries no first-party standards-status, dependency, buyer-requirement, or independent-checker evidence sufficient to select it. It therefore remains an unevidenced option rather than a rejected primitive. Reconsideration requires the evidence named below; no performance or standards comparison is inferred from absence.

## Recommendation

**PROPOSED — awaiting human ratification.**

1. **`HashAlgorithm::Sha256` is the single named default identity algorithm for kernel v1.** All identity digests are the full 256 bits. No truncation below 256 bits for any identity, cache key, or commitment.
2. **Ratify D1 and D2 as one package.** The recommended package is **SHA-256 + the deterministic structured-value grammar in D2**. The alternative candidate is **a separately specified 256-bit TupleHash profile + a D2 structured-value encoding**. TupleHash is not offered as a wrapper around another hash. The alternative remains `[UNVERIFIED]` until its exact first-party parameter profile and independent implementation path are recorded.
3. **The `HashAlgorithm` registry ships in C1 with more than one variant defined**, even though only one is used, so that the migration path is exercised rather than merely asserted. An algorithm-agile grammar that has never carried a second algorithm is an untested claim.
4. **Legacy algorithms are namespace-fenced by an explicit law:** MD5, RC4, and SHA-1 may appear only where PDF semantics or standard security handlers require them (§16.1). They may never name a MonkeyBee identity, key a cache, or appear in a receipt as an identity digest. This should be a machine-checked lint, not a convention.
5. **Digests are indexes, not authority** (§9.2), and collision observation quarantines both records. This is restated here only to be explicit that ratifying SHA-256 does not smuggle in an assumption of collision-freedom.

### Continuity note, offered as fact and not as an argument

This run's own canonical byte baseline (`ledger/CANONICAL_HASHES.md`) already uses SHA-256, as does the G0 verification evidence. Ratifying SHA-256 makes the existing baseline continuous with the kernel's identity grammar; ratifying a different algorithm requires a newly identified baseline. No external commitment exists yet, so this is an administrative difference rather than a selection argument.

## Rationale

The selection criterion used here is the cost imposed on independent verification, not an unmeasured throughput comparison. The campaign's Q3 evidence chain is intended for outside checking (Charter §7; §33). One locally demonstrated verification path exists for SHA-256 through `sha256sum`; broader reviewer-machine availability is `[UNVERIFIED]`. The recommendation therefore rests on the NIST identity, the local reproducibility path, and D2's separate ambiguity controls—not on a universal tooling or performance claim.

Length-extension does not reach the proposed use as a MAC because project identity digests are neither MACs nor authority. Grammar ambiguity is a separate D2 risk and no hash choice removes it. The recommendation does not compare SHA-2, SHA-3, TupleHash, or BLAKE3 performance or adoption; those dimensions remain `[UNVERIFIED]`. Option C remains visible because a standardized tuple-hash construction may be a human preference once its exact profile and implementation evidence exist.

## Reversibility and migration path

**Technically: high. Evidentially: bounded, with one irreversible commitment boundary.**

The grammar is algorithm-versioned by design (§9.2), so migration is: define the new `HashAlgorithm` variant; dual-index durable artifacts during a transition window; re-hash and re-issue every durable receipt and cache key; retire the old variant. Painful and mechanical, not architectural.

**The irreversible edge.** A digest committed through the tamper-evident substrate (§33.4) cannot be re-hashed later without destroying the timestamp semantics that give the commitment its value. The point of an independently held, time-stamped commitment is that it was made *then*, under an algorithm chosen *then*. Re-issuing it under a new algorithm produces a new commitment with a new date, and the original claim's provenance value does not transfer.

This has a scheduling consequence the human should see explicitly:

> **Charter §10 makes this Charter the first artifact committed through the substrate, and its hash "the campaign's first ledger entry."** The content-hash algorithm therefore needs ratification **before** the first substrate commitment, or the campaign's founding evidence entry stands under an unratified algorithm. Recorded as finding F-G2-3 in `ledger/owners/G2_STATE.md` and raised to the ratification queue as an ordering constraint, not merely a preference.

If a break in SHA-256 ever became credible, the response is not retroactive re-hashing of committed evidence. It is: freeze the affected claims, disclose the algorithm's status in the ledger, migrate forward, and let the committed history stand under its stated algorithm with its weakness disclosed. The kernel migration protocol should record that response before the first commitment.

## Dependencies

- **Consumes:** nothing. This is a root decision; it can be ratified independently of every other brief.
- **Consumed by:** D2 (the grammar hashes with it — ratify as one package), D3 (the decoded-artifact digest), D4 (the checker recomputes it; shared crypto primitive is the one admitted code-sharing exception), D6 (the ledger's hash chain), and every identity in Rev 7 §9.2.
- **Gates:** the C1 identity/evidence/report/checker stack in its entirety. G3's Cycle 1 delta plan builds against `Sha256` as a proposed default and must label that dependency as awaiting ratification.
- **Blocks:** the first tamper-evident substrate commitment (see the irreversible edge above).

## Evidence still needed before ratification

1. **Counsel/first-party confirmation of standards status** — whether the announced FIPS 180-4 revision has published, and whether it changes SHA-256's approved status. `[UNVERIFIED]` here by construction; this is a human verification step.
2. **A throughput measurement on the project's own workloads**, taken during C1 when benchmarking is legal (measurement is forbidden this phase, and Charter/Work Order forbid comparator measurement before the discovery protocols are committed). If SHA-256 hashing shows up as a material cost in the C1 profile, that is evidence to reconsider — it is not a reason to guess now.
3. **A dependency review of the chosen pure-Rust implementation** against §16.1 (audited, permissively licensed) and §15.9's admissibility conditions.
4. **Confirmation that the independent checker can source a *different* audited SHA-256 implementation**, so that the one admitted shared primitive (D4) can, if the human prefers, become a dual implementation instead.

## Blast radius if wrong

| Failure | Consequence | Detectability |
|---|---|---|
| Algorithm is broken (collision-practical) during the campaign | Every identity, cache key, receipt, and commitment is in question. Semantic-equality reuse could be induced across genuinely different documents — a severe class because it is a *silent correctness* failure, not a crash. | High, externally: a break in SHA-256 would be public news. The quarantine law (§9.2) means the system reacts to an *observed* collision rather than assuming impossibility. |
| Algorithm is merely a poor fit (slow on our workloads) | Performance cost, absorbed by the C1 benchmark lane; migrate at a cycle boundary. | High; ordinary profiling. |
| Digest width truncated for cache-key convenience | Birthday bound collapses (128-bit truncation → ~2⁶⁴ work); accidental collisions become reachable; the quarantine machinery starts firing on non-adversarial inputs. | Medium. This is the realistic self-inflicted wound, which is why the recommendation forbids truncation as a law rather than a default. |
| Chosen before the substrate commitment, then changed after it | The founding ledger entry stands under a superseded algorithm; the provenance value of the campaign's first commitment is impaired and cannot be repaired by re-hashing. | Certain, and unrecoverable — hence the ordering constraint above. |

**Summary:** the algorithm can migrate prospectively; an externally timestamped commitment cannot be recreated with its original time semantics.

## What would change this recommendation

- The human prefers the standardized tuple-hash candidate and the exact SP 800-185 profile plus independent implementation evidence is supplied → Option C, as a whole package with D2's structured-value encoding.
- A FIPS-validation requirement is confirmed as a hard buyer constraint → re-evaluate every option against the exact validated-module and deployment requirements; this brief does not infer which passes.
- No FIPS constraint exists, and C1 profiling shows identity hashing on the critical path → BLAKE3 becomes arguable, but only if the independent checker's reimplementation cost is separately funded and its detection-rate trial (D4) still passes.

## Human ratification

This brief proposes; it does not decide. Rev 7 §29.9 reserves architectural constitution and high-consequence security decisions to humans.

- [ ] **Ratify** SHA-256 / 256-bit / package with D2 as recommended
- [ ] **Ratify Option C** (an exact 256-bit SP 800-185 TupleHash profile + D2 structured-value encoding), only after the named first-party and implementation evidence is supplied
- [ ] **Amend** (record the variant and rationale)
- [ ] **Defer** — and record what C1 may assume in the meantime, noting that C1 cannot build the identity stack without an answer

Ratifier: ______________________ Date: ____________
