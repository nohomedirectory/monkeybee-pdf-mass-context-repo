---
generated-by: Claude G2 owner (claude-opus-4-8, effort xhigh)
date: 2026-07-14
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
| The evidence checker is independently implemented and receives raw hostile bytes | §35 checker-isolation row, Appendix A.13, audit row R1-9 | **The identity algorithm must be cheap for a second, independent party to reimplement and for an external adjudicator to verify with stock tools.** This is the decisive project-specific criterion, and it is easy to miss. |

That last row deserves emphasis, because it inverts the usual ranking. In most systems you pick a content hash on throughput. Here, the artifact's *purpose* is to be checked by someone who does not trust us (Charter §7: "Independence"; §33). An identity algorithm that a third-party reviewer cannot recompute with a command-line tool they already have imposes friction on precisely the party whose independence the campaign's Q3 verdict depends on. Verifiability outranks speed.

## Options

### Option A — SHA-256 (FIPS 180-4 family), 256-bit digests

- **For:** Universally available in every language, every platform, and every auditor's shell (`sha256sum`). Hardware-accelerated on current x86-64 (SHA-NI) and aarch64. Mature, permissively licensed pure-Rust implementations exist in the RustCrypto ecosystem. FIPS-approved, which matters to the regulated buyers of the G1 secure-ingestion wedge. Cheapest algorithm in the world for an independent checker author to reimplement or, better, to take from a different audited crate.
- **Against:** Merkle–Damgård construction, therefore vulnerable to length-extension. The relevance of this is bounded and must be stated precisely rather than waved at: length-extension is exploitable when a digest is used as a MAC over `secret || message`. MonkeyBee's digests are content identity, never MACs, never authority (§9.2). The residual risk is *ambiguity*, not length-extension: hashing concatenated fields without framing lets two different structures produce one digest. That risk is eliminated by D2's framing grammar, not by the hash choice — and it would exist with any hash function.
- **Standards status:** FIPS 180-4 is the Secure Hash Standard. NIST announced (2023-03-07) a decision to revise it. The algorithms are not withdrawn; the document is under revision. Whether a revised document has since published is `[UNVERIFIED]` and is a counsel/first-party verification step below.

### Option B — SHA-512/256 (truncated SHA-512, same standard)

- **For:** Length-extension resistant by truncation. Faster than SHA-256 on 64-bit CPUs that lack SHA-NI. Still FIPS-approved.
- **Against:** Meaningfully less ubiquitous in tooling. An external adjudicator's reflexive `sha256sum` does not reproduce it, and the failure mode is a confused reviewer, which is the one failure mode this campaign can least afford. Buys a property (length-extension resistance) that the framing grammar already makes irrelevant for our use.

### Option C — SHA3-256 or SHAKE256 (FIPS 202), with TupleHash framing (SP 800-185)

- **For:** Sponge construction, so no length-extension by design. SP 800-185's **TupleHash** is, per NIST's own description, "designed to hash tuples of input strings unambiguously" — which is the standardized, reviewed form of exactly the length-framing and domain-separation law §9.2 demands. Choosing this package means the framing is a cited standard rather than a project-authored grammar, and a project-authored grammar is a thing a hostile reviewer gets to attack. That is a real and honest argument in this campaign's favour, and it is the strongest case against the recommendation below.
- **Against:** Generally slower in software than SHA-2 on hardware with SHA-2 acceleration and without Keccak acceleration `[UNVERIFIED — no benchmark has been run; running one is forbidden this phase and is named as evidence needed]`. Less ubiquitous for third-party verification than SHA-256, though far more so than SHA-512/256. Rust ecosystem maturity for TupleHash specifically (as opposed to SHA-3/SHAKE) is thinner `[UNVERIFIED]`, and a thin dependency is a dependency the independent checker must also find or write.
- **Status:** FIPS 202 is final (Aug 2015; SHA3-224/256/384/512, SHAKE128/256). NIST posted a 2025-03-13 note that it has decided to update the publication. SP 800-185 is final (Dec 2016).

### Option D — BLAKE3

- **For:** Fast; internally parallel/tree-structured, which suits large PDFs; native keyed and key-derivation modes that give domain separation as a primitive; extendable output.
- **Against, and decisively for this project:** Not a NIST/FIPS standard, which forecloses FIPS-dependent buyers of the G1 wedge. Younger, with less adversarial review-years than the SHA families. Most importantly, its tree mode is a **larger specification surface that the independent checker must reimplement exactly**. The checker-isolation law (audit row R1-9, and D4) requires a genuinely independent implementation; every unit of algorithmic complexity in the identity hash is a unit of cost and a unit of risk imposed on the one component whose independence carries the Q3 claim. Optimizing the identity hash for throughput while taxing the independent checker is the wrong trade for this artifact.

## Recommendation

**PROPOSED — awaiting human ratification.**

1. **`HashAlgorithm::Sha256` is the single named default identity algorithm for kernel v1.** All identity digests are the full 256 bits. No truncation below 256 bits for any identity, cache key, or commitment.
2. **Ratify D1 and D2 as one package.** The recommended package is **SHA-256 + the deterministic framing grammar in D2**. The coherent alternative package is **SHA3-256/SHAKE256 + TupleHash framing (Option C)**, which trades ecosystem ubiquity for standard-native framing. Mixing across packages — for example SHA-256 with hand-waved framing, or TupleHash framing with a SHA-2 core — is not offered, because the framing and the hash family are what make each package sound.
3. **The `HashAlgorithm` registry ships in C1 with more than one variant defined**, even though only one is used, so that the migration path is exercised rather than merely asserted. An algorithm-agile grammar that has never carried a second algorithm is an untested claim.
4. **Legacy algorithms are namespace-fenced by an explicit law:** MD5, RC4, and SHA-1 may appear only where PDF semantics or standard security handlers require them (§16.1). They may never name a MonkeyBee identity, key a cache, or appear in a receipt as an identity digest. This should be a machine-checked lint, not a convention.
5. **Digests are indexes, not authority** (§9.2), and collision observation quarantines both records. This is restated here only to be explicit that ratifying SHA-256 does not smuggle in an assumption of collision-freedom.

### Continuity note, offered as fact and not as an argument

This run's own canonical byte baseline (`ledger/CANONICAL_HASHES.md`) already uses SHA-256, as does the G0 verification evidence. Ratifying SHA-256 makes the existing baseline continuous with the kernel's identity grammar; ratifying a different algorithm requires re-hashing that baseline, which is cheap and harmless today. This is a small convenience, and it should not be mistaken for a reason. It is recorded so the human can see the cost of the alternative accurately rather than discovering it later.

## Rationale

The decisive criterion is not throughput; it is the cost imposed on independent verification. The campaign's entire Q3 claim rests on an evidence chain that an outside party checks (Charter §7; §33). Two consumers of this decision are adversarial or independent by construction — the `mb-checker` (Appendix A.13, which "never receives a producer-parsed `EvidencePackage` as trusted input") and the external adjudicator. SHA-256 minimizes the friction and the reimplementation risk for both, and it is the only option a reviewer can verify with a tool already on their machine.

Every argument against SHA-256 concerns length-extension, and length-extension does not reach a digest that is never a MAC and never an authority. The ambiguity risk that *does* reach us belongs to the encoding grammar, which is D2's subject and is eliminated there. Choosing SHA-3 to solve a problem that framing already solves would pay in ubiquity for a property we do not use — unless the human prefers Option C's standard-native framing, which is a legitimate preference and the reason Option C is presented as a whole package rather than dismissed.

## Reversibility and migration path

**Technically: high. Evidentially: bounded, with one genuinely irreversible edge.**

The grammar is algorithm-versioned by design (§9.2), so migration is: define the new `HashAlgorithm` variant; dual-index durable artifacts during a transition window; re-hash and re-issue every durable receipt and cache key; retire the old variant. Painful and mechanical, not architectural.

**The irreversible edge.** A digest committed through the tamper-evident substrate (§33.4) cannot be re-hashed later without destroying the timestamp semantics that give the commitment its value. The point of an independently held, time-stamped commitment is that it was made *then*, under an algorithm chosen *then*. Re-issuing it under a new algorithm produces a new commitment with a new date, and the original claim's provenance value does not transfer.

This has a scheduling consequence the human should see explicitly:

> **Charter §10 makes this Charter the first artifact committed through the substrate, and its hash "the campaign's first ledger entry."** The content-hash algorithm therefore needs ratification **before** the first substrate commitment, or the campaign's founding evidence entry stands under an unratified algorithm. Recorded as finding F-G2-3 in `ledger/owners/G2_STATE.md` and raised to the ratification queue as an ordering constraint, not merely a preference.

If a break in SHA-256 ever became credible, the correct response is not retroactive re-hashing of committed evidence. It is: freeze the affected claims, disclose the algorithm's status in the ledger, migrate forward, and let the committed history stand under its stated algorithm with its weakness disclosed. That is the honest path and it should be written into the kernel's migration protocol now, while it costs nothing, rather than improvised under pressure.

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
| Algorithm is broken (collision-practical) during the campaign | Every identity, cache key, receipt, and commitment is in question. Semantic-equality reuse could be induced across genuinely different documents — the worst class, because it is a *silent correctness* failure, not a crash. | High, externally: a break in SHA-256 would be public news. The quarantine law (§9.2) means the system reacts to an *observed* collision rather than assuming impossibility. |
| Algorithm is merely a poor fit (slow on our workloads) | Performance cost, absorbed by the C1 benchmark lane; migrate at a cycle boundary. | High; ordinary profiling. |
| Digest width truncated for cache-key convenience | Birthday bound collapses (128-bit truncation → ~2⁶⁴ work); accidental collisions become reachable; the quarantine machinery starts firing on non-adversarial inputs. | Medium. This is the realistic self-inflicted wound, which is why the recommendation forbids truncation as a law rather than a default. |
| Chosen before the substrate commitment, then changed after it | The founding ledger entry stands under a superseded algorithm; the provenance value of the campaign's first commitment is impaired and cannot be repaired by re-hashing. | Certain, and unrecoverable — hence the ordering constraint above. |

The honest summary: **being wrong about the algorithm is recoverable; being wrong about the *ordering* is not.** The migration machinery exists. The timestamp semantics of an external commitment do not admit a do-over.

## What would change this recommendation

- The human values standard-native framing (TupleHash) over stock-tool verifiability → Option C, as a whole package with D2.
- A FIPS-validation requirement is confirmed as a hard buyer constraint → strengthens A or C; eliminates D.
- No FIPS constraint exists, and C1 profiling shows identity hashing on the critical path → BLAKE3 becomes arguable, but only if the independent checker's reimplementation cost is separately funded and its detection-rate trial (D4) still passes.

## Human ratification

This brief proposes; it does not decide. Rev 7 §29.9 reserves architectural constitution and high-consequence security decisions to humans.

- [ ] **Ratify** SHA-256 / 256-bit / package with D2 as recommended
- [ ] **Ratify Option C** (SHA3-256 or SHAKE256 + TupleHash framing) as the alternative package
- [ ] **Amend** (record the variant and rationale)
- [ ] **Defer** — and record what C1 may assume in the meantime, noting that C1 cannot build the identity stack without an answer

Ratifier: ______________________ Date: ____________
