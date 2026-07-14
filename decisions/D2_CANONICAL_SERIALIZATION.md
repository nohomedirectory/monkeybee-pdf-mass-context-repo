---
generated-by: Claude G2 owner (claude-opus-4-8, effort xhigh)
date: 2026-07-14
inputs:
  - CYCLE_0_WORK_ORDER.md §4 resolve-now item 2
  - MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md §9.2, §9.6, §22.3, §22.4, §22.5, §11.9, §35
  - AUDIT_FINDINGS_LEDGER.md R1-4
  - NIST CSRC primary page for SP 800-185 (TupleHash) — see G2_STATE fetch record
status: PROPOSED
evidence-status: provisional-pending-substrate
decision-id: D2
ratification: PROPOSED — awaiting human ratification
couples-with: D1 (content-hash algorithm) — choose as one package, not two knobs
---

# D2 — Canonical serialization grammar for hashing

## The question

What exact byte grammar turns a structured project value — an identity, a manifest, a semantic state, an evidence package — into the input of a hash function?

## First, a distinction that must not blur

Rev 7 contains **two** canonical serialization problems. They share a word and nothing else. Conflating them is the single most likely way this brief gets misread, and duplication drift of exactly this kind produced two of the three Grade-A defects in this project's history (R1-1, R2-N7).

| | **(a) Identity/commitment serialization** | **(b) PDF canonical output serialization** |
|---|---|---|
| What it encodes | MonkeyBee's own structured values: identities, dependency manifests, semantic state, receipts, evidence packages | PDF file bytes emitted by the writer |
| Governed by | §9.2 (versioned grammar, class/version domain separation, length framing, canonical encodings); the versioned protocol IDs `SemanticValueProtocolId`, `RealityCommitmentProtocolId`, `ExpectedStateProtocolId`, `DraftIntentProtocolId` | §22.3 (object allocation, trailer identity), §22.4 (canonical mode), §22.5 (canonical number formatting, bounded PDF decimal grammar) |
| Consumer | The hash function; the independent checker | PDF readers |
| Cycle | **C1 — this decision** | **C4 — the writer cycle; explicitly excluded from C1** |
| Audit row | — | R1-4 (§22.4 needs a scope-totality condition) |

**This brief resolves (a) only.** (b) is a writer decision that lands with the writer, and it must not be pre-resolved here against imagined code — the §34.9 archaeology-first law forbids exactly that. They are linked at one point, and only one: R1-4 established that §22.4's byte-identity claim holds only under a `SemanticScopeId` that is *serialization-total*. That linkage is a constraint on (b) that (a) must be capable of expressing — the scope manifest is itself a structured value that (a) encodes. Nothing more transfers.

## What C1 actually needs from (a)

C1 ships no writer, but it does ship the identity, evidence, report, and checker stack. That stack cannot exist without a canonical encoding for:

- the identity tuples of §9.2 (`SourceRootId`, `RevisionGraphId`, `DocumentViewId`, `DerivationId`, and the rest);
- `SemanticStateId` — a commitment to admitted document meaning, which requires canonically encoding admitted **COS semantic values** (the object graph C1 parses);
- the validated dependency-and-selection manifest of §9.6, on which every cache-reuse and D0 determinism claim rests;
- receipts, report schemas, and evidence packages.

So (a) is genuinely C1-blocking, and G3's delta plan needs its shape.

## The property that matters

Exactly one property is load-bearing, and it is worth stating precisely because it determines everything else:

> **The encoding must be injective on admitted values.** Two structurally different values must never produce the same byte string. One value must always produce the same byte string.

The two failure directions are not symmetric, and the asymmetry should drive the design:

- **Ambiguity** (different values → identical bytes → identical digest) is a **security** failure. It manufactures false identity equality. Under §9.6, semantic equality authorizes cache reuse; under §9.2, a `SemanticStateId` may be shared across roots of equal admitted meaning. A collision *manufactured by a grammar ambiguity* would therefore let an attacker induce reuse of the wrong derived artifact — a silent, correct-looking wrong answer. This is the worst class of bug this system can have, and no amount of hash strength prevents it, because the hash is doing exactly what it was asked to do.
- **Over-strictness** (equal values → different bytes) is a **performance and determinism** failure: cache misses, and D0 claims that fail to replay. Bad, visible, fixable.

Therefore the design bias is explicit: **when the grammar is unsure, it refuses; it never guesses.** Any construct whose canonical form is not uniquely determined is rejected at encode time rather than encoded on a best-effort basis.

## Options

### Option A — Project-defined strict TLV (tag / length / value), hashed with SHA-256

A hand-rolled canonical encoding: a domain prefix carrying class ID and protocol version, then for each field a type tag, a fixed-width big-endian length, and the value bytes; recursively for nested structures.

- **For:** Trivially injective if specified correctly. Minimal, no dependency, easy to reimplement independently (which the checker must do).
- **Against:** Hand-rolled. Every hand-rolled encoding is a small specification that nobody has attacked, and this project's threat model includes a red team paid to attack exactly this. It is not self-describing, so debugging and third-party audit are harder.

### Option B — Deterministic CBOR profile (RFC 8949 core deterministic encoding), hashed with SHA-256 — **recommended**

Adopt CBOR's deterministic encoding requirements as the byte grammar, pinned by a **project profile** that closes every degree of freedom:

- indefinite-length items forbidden;
- **floating-point forbidden entirely** in identity encodings (see the float law below);
- shortest-form integer encoding required;
- map keys sorted bytewise on their encoded form; duplicate keys forbidden (encode-time rejection, not last-wins);
- tags restricted to an explicit allowlist;
- every hashed value wrapped in a domain-separation prefix carrying `(class ID, protocol version)` with explicit top-level length framing.

- **For:** A real specification with existing review, existing test vectors, and multiple independent implementations in multiple languages — which is precisely what an *independently implemented* checker and an external adjudicator need. Self-describing, so a hostile reviewer can decode and inspect what was hashed rather than taking our word for the field order. Deterministic-encoding rules are a standardized answer to the injectivity problem. The project still owns the profile, which is where the remaining risk sits, and that risk is small and reviewable.
- **Against:** "Canonical CBOR" has historically meant more than one thing across specifications and libraries; picking the wrong library or leaving the profile loose reintroduces exactly the ambiguity we are trying to eliminate. The mitigation is that the profile is *pinned and machine-checked*, and that the checker uses a **different** CBOR implementation, so a library-specific canonicalization bug shows up as a differential-test failure instead of a shared premise. Also: a dependency, where Option A has none.

### Option C — TupleHash (NIST SP 800-185), paired with SHA-3/SHAKE

Per NIST, TupleHash is "designed to hash tuples of input strings unambiguously" — the standardized form of §9.2's length-framing law. The framing stops being a project artifact and becomes a cited standard.

- **For:** The strongest answer to "who reviewed your framing?" — the answer is NIST, not us. Removes the hand-rolled-grammar attack surface at the framing layer.
- **Against:** Couples the grammar to the Keccak family, so it is only coherent alongside D1 Option C (SHA-3/SHAKE), with SHA-256's ubiquity advantages given up. TupleHash handles the *tuple framing*; it does not by itself canonicalize a nested, typed value graph — a structured-value encoding still has to sit above it, so this option reduces the hand-rolled surface without eliminating it. Rust ecosystem support for TupleHash specifically is thinner than for SHA-3 `[UNVERIFIED]`, and a thin dependency is one the independent checker must also obtain or write.

### Option D — Canonical JSON (e.g. JCS) or Protobuf — **rejected**

- Canonical JSON: text encoding, floating-point number hazards, Unicode normalization and escaping ambiguity. A grammar whose canonical form depends on Unicode normalization decisions is a grammar with an attack surface in every string. Reject.
- Protobuf: not canonical by construction — field ordering, unknown-field retention, and default-value elision are all implementation-visible. Reject.

Both are recorded so the rejection is explicit rather than an omission a later reviewer must re-litigate.

## Recommendation

**PROPOSED — awaiting human ratification.**

**Package 1 (recommended): SHA-256 (D1 Option A) + deterministic-CBOR profile (D2 Option B) + explicit domain/length framing.**
**Package 2 (coherent alternative): SHA3-256/SHAKE256 (D1 Option C) + TupleHash framing (D2 Option C).**

Ratify a package, not a pair of independent knobs. Package 1 buys stock-tool verifiability and ecosystem depth at the cost of a project-owned profile. Package 2 buys standard-native framing at the cost of ubiquity. Both are defensible; they are not mixable.

Under either package, the following are **laws, not defaults**, and should be machine-checked:

1. **The float law.** No IEEE-754 value ever enters an identity encoding. PDF numbers, coordinates, and any real-valued quantity are encoded either as exact integers or as a bounded decimal *string* under a declared grammar. Rationale: float canonicalization is a swamp (negative zero, NaN payloads, subnormals, and the shortest-round-trip formatting problem), and §22.5 already refuses to delegate PDF number formatting to "a generic shortest-float formatter". Identity encoding must be at least as strict as the writer, and it costs nothing to forbid floats outright here.
2. **Domain separation is mandatory and typed.** Every hashed value carries its class ID and protocol version *inside* the hashed bytes. A `DocumentViewId`'s preimage can never be reinterpreted as a `DerivationId`'s preimage. §9.2 requires this; it is restated as a law because it is the kind of thing an optimizing implementer removes.
3. **Length framing is mandatory.** No unframed concatenation, ever, at any nesting level.
4. **Refuse, never guess.** A value whose canonical form is not uniquely determined by the profile is rejected at encode time.
5. **The grammar is versioned** through the protocol IDs canon already defines (`SemanticValueProtocolId`, `RealityCommitmentProtocolId`, `ExpectedStateProtocolId`, `DraftIntentProtocolId`, §9.2). v1 is what this brief specifies; the version travels inside the hashed bytes.
6. **The canonical encoder is dual-implemented, and its differential test is an acceptance criterion.** See below — this is the most important sentence in the brief.

## The dual-implementation requirement (why this is not optional)

Rev 7 §35's checker-isolation row already demands "dual-implementation collision/ambiguity review" for the evidence-package canonical identity. That requirement should be understood as load-bearing rather than as diligence, and the reason is worth spelling out:

> **If the producer and the checker share one canonical-encoding implementation, an ambiguity bug in that encoder is invisible to the checker.** The checker would encode the attacker's value the same wrong way, compute the same digest, and confirm the producer's claim. The two agree, and they are both wrong — which is precisely the F-01 pattern the FrankenSim re-audit documents and Charter risk #7 names: the whole ecology agreeing on a wrong certificate.

Therefore the canonical encoder is **the single most important component in the system to dual-implement**, ahead of the package parser. D4 (checker isolation) admits sharing exactly one thing — the audited hash primitive — and this is the reason the encoder is not on that list. The differential test between the two implementations, run over an adversarial encoding corpus, is a C1 acceptance criterion and a standing falsifier.

## Rationale

The property that matters is injectivity, and injectivity is a property of the *grammar*, not of the hash. Once that is seen clearly, the hash-family debate (D1) and the grammar debate (D2) separate cleanly, and the grammar debate resolves on a single question: whose reviewed specification is the injectivity resting on?

Option A rests it on ours. Option C rests the framing layer on NIST's. Option B rests it on a widely implemented deterministic-encoding specification *plus* a small project profile, and then — critically — cross-checks that profile with a second independent implementation, converting the residual project-owned risk into a testable differential rather than a shared premise. That combination is the most defensible against a red team, which is the standard this campaign is actually held to.

## Reversibility and migration path

**Moderate — lower than D1's, and the difference is worth understanding.**

The grammar is versioned (§9.2), so a v2 can be introduced. But the grammar determines the *preimage* of every digest, so changing it changes every identity, exactly as changing the hash algorithm does. There is no dual-index trick that makes a v1 digest and a v2 digest comparable: they are different commitments to the same value.

Worse than D1 in one respect: a hash-algorithm migration is mechanical and total (re-hash everything with the new function). A grammar migration additionally requires proving that the *new* grammar is injective and that the *mapping* from old values to new encodings is faithful — a semantic obligation, not a mechanical one. Any value whose v1 encoding was ambiguous cannot be safely migrated at all; it must be quarantined, because you cannot know which value it was.

Practical consequence: **an ambiguity discovered after the substrate commitment is not fully repairable.** This is the strongest argument for the adversarial encoding corpus and the dual implementation landing in C1, before the grammar has hashed anything anyone relies on.

## Dependencies

- **Consumes:** D1 (the hash function this grammar feeds). Ratify as one package.
- **Consumed by:** every identity in §9.2; `SemanticStateId` and therefore all of C1's admitted-document identity; the §9.6 dependency manifest and hence all cache-reuse and D0 determinism claims; D3 (the decoded-container recipe identity is an encoded tuple); D4 (the checker independently implements this); D6 (ledger records are hashed with it).
- **Constrains, but does not decide:** the C4 writer's canonical output mode (§22.4) — see the distinction table above. The scope-totality condition from R1-4 is a *writer* obligation that this grammar must be able to express.
- **Gates:** the entire C1 identity/evidence/report/checker stack.

## Evidence still needed before ratification

1. **Dual-implementation ambiguity review** — required by §35's own row, and by the argument above. Two independent encoders, one adversarial corpus, zero divergences.
2. **A hostile-encoding corpus**: duplicate map keys, non-shortest integer forms, indefinite-length items, out-of-allowlist tags, nested-depth bombs, string/bytes-type confusion, and every construct the profile forbids — each must be *rejected*, and rejection must be tested as a positive requirement, not assumed.
3. **A pinned answer to which CBOR determinism rules the profile adopts, cited to the specification text**, with the specification's own version recorded. This is the loose end in Option B and it must be closed at C1 rather than left to a library's defaults. `[UNVERIFIED here — the exact rule set has not been quoted against a first-party specification in this brief; do not treat the summary above as normative.]`
4. **Confirmation that two independently maintained Rust CBOR implementations exist** with deterministic-encoding support adequate to the profile (the checker needs the second one). `[UNVERIFIED]`
5. **Migration design** — how a v1→v2 grammar transition works, and what happens to values whose v1 encoding is later found ambiguous. Write it before it is needed.

## Blast radius if wrong

| Failure | Consequence | Severity |
|---|---|---|
| The grammar is ambiguous (two values, one encoding) | False identity equality. Under §9.6, this can authorize reuse of a derived artifact belonging to a *different* document — a silent wrong answer with a valid-looking receipt. Every downstream evidence claim built on the affected identity is void. | **Catastrophic and silent.** The defining failure mode of this decision. |
| The grammar is ambiguous *and* the checker shares the implementation | The above, plus the checker confirms it. Q3's evidence chain is worthless and the project does not know. | **Catastrophic and undetectable from inside.** This is why dual implementation is a law. |
| The grammar is over-strict (equal values, different encodings) | Cache misses; D0 determinism claims fail to replay; performance regressions. | Moderate, loud, fixable. |
| Floats admitted into the encoding | Platform- and library-dependent digests; non-reproducible identities; D0/D1 claims silently untrue on some targets. | High — and entirely avoidable, hence the float law. |
| Ambiguity discovered after substrate commitment | Affected commitments cannot be repaired; ambiguous values cannot be safely migrated because their intended value is unrecoverable. | High, partially unrecoverable. |

## Human ratification

This brief proposes; it does not decide (Rev 7 §29.9).

- [ ] **Ratify Package 1** — SHA-256 + deterministic-CBOR profile + domain/length framing (recommended)
- [ ] **Ratify Package 2** — SHA3-256/SHAKE256 + TupleHash framing
- [ ] **Ratify Option A** — project-defined strict TLV (accepting the hand-rolled-grammar surface)
- [ ] **Amend** (record the variant and rationale)
- [ ] **Defer** — noting that C1 cannot build `SemanticStateId` or the dependency manifest without an answer

Ratifier: ______________________ Date: ____________
