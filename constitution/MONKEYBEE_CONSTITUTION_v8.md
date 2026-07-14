---
generated-by: Codex G1 owner
date: 2026-07-14
inputs:
  - MONKEYBEE_CAMPAIGN_CHARTER_v1.md
  - CYCLE_0_WORK_ORDER.md
  - AUDIT_FINDINGS_LEDGER.md
  - MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md
  - DISPUTES.md
  - decisions/D1_CONTENT_HASH.md
  - decisions/D2_CANONICAL_SERIALIZATION.md
  - decisions/D3_DECODED_STREAM_IDENTITY.md
  - decisions/D4_EVIDENCE_CHECKER_ISOLATION.md
  - decisions/DEFERRED_REGISTER.md
  - "gauntlet/ROUND_LOG.md (bounded R14 lines 1815-2081 only)"
  - "gauntlet/ROUND_LOG.md at commit 3d866bd00d518414bc0fd04b6548c205c0197671 (R15 bytes [544857,573917) only)"
status: PROPOSED
evidence-status: provisional-pending-substrate
constitution-version: 8.0-proposed
---

# MonkeyBee Constitution v8

This document is the frozen-kernel candidate extracted under Cycle 0 Work Order §1. It supersedes Revision 7 only for the sections reproduced here and only after the required human ratification and commitment step. Until then, it is a proposed extraction, not evidence that a commitment, licensed-source review, or external action occurred.

## Extraction contract

- Stable Revision 7 section identifiers are preserved.
- This file is the single normative home for §§4, 6, the §8 architecture and dependency-direction law, §§9–11, §30.1.1, and §§33–34. Shell references to these laws are marked `generated-echo` and cannot amend them.
- The concrete crate atlas remains provisional shell content. Only the crate-boundary budget is in the kernel.
- Revision 7 wording is preserved except where an `OPEN-C0` finding, the supplied §34.9 text, or a human-routed premise-qualified repair requires a change. `reports/FIX_APPLICATION.md` identifies every change.
- Concrete hash-algorithm, digest-width, and canonical-serialization bindings remain `PROPOSED — awaiting human ratification`. D1 proposes SHA-256 at 256 bits and requires joint ratification with D2; neither proposal is treated as law here. Section 9.2's domain separation, framing, versioning, canonical-encoding, and collision-quarantine requirements remain the governing extracted law, but an unresolved concrete binding cannot mint a production identity. Hash and grammar ratification must precede the campaign's first external/tamper-evident commitment because re-hashing later cannot preserve the original commitment time.
- Runtime dependency and cryptographic-crate choices remain pending under D-005. This Constitution defines capability, isolation, evidence, and migration requirements without selecting a crate by model preference.
- SpecCard semantic bodies remain absent. Registry and review slots live in `constitution/SPECCARD_PIPELINE.md` and are all `PENDING-LICENSED-SOURCE`.

## 4. Clean-room and specification-provenance protocol

The clean-room boundary is a product feature, a legal boundary, and a coordination invariant.

### 4.1 Prohibited implementation inputs

Implementation agents must not derive production code from:

- Poppler source;
- MuPDF source;
- PDFium source;
- pdf.js source;
- Ghostscript source;
- qpdf source;
- PDFBox source;
- hayro source;
- krilla or pdf-writer source;
- lopdf source;
- oxidize-pdf source;
- pdf_oxide source;
- safe-pdf source;
- pdf-rs or pdf_render source;
- printpdf source;
- pdfsink-rs source;
- fop-pdf-renderer or pdforg-render source;
- stet, stet-pdf-reader, or stet-pdf source;
- pdfpurr source;
- PDFluent, pdf-engine, pdf-render, or related PDFluent component source;
- proprietary SDK source;
- decompiled binaries;
- or code copied from any PDF processor. A deliberate reuse decision would require a separately isolated non-core adapter, legal review, and an explicit abandonment or narrowing of the clean-room claim for that component; a compatibility preference alone is never permission to copy implementation.

Existing processors may be invoked as black boxes in dev-only harnesses. The prohibition applies equally to permissively licensed Rust processors: source-license permissiveness does not convert competitor implementation into a clean-room input. hayro is additionally treated as a transitive contamination vector because its published notices identify adapted or translated code from processors already prohibited by name.

The named bullets are defense-in-depth, not an exhaustive allow-by-omission list. A generated context/implementation denylist is derived from the current competitor register plus the incumbent/oracle registry; every source repository classified as a PDF processor automatically enters source scanners and model-context policy. A newly discovered processor remains prohibited immediately even before this prose list is revised. Documentation, interface specifications, and black-box artifacts still require their own §4.2 rights and clean-room classification rather than inheriting permission from source unavailability.

### 4.2 Permitted inputs

Implementation may derive only from a source whose **implementation use, redistribution use, and AI-assisted use have each been classified**. Potentially permitted classes include:

- project-authored, rights-reviewed `SpecCard` paraphrases;
- open, machine-readable standards models with compatible licenses;
- academic papers and general algorithms whose terms permit the intended use;
- independently authored conformance tests and corpora with recorded licenses;
- black-box observations collected under a reviewed experiment protocol;
- public format descriptions whose licenses permit implementation and AI-assisted use;
- project-generated fixtures;
- and standards or normative references only through a path explicitly authorized for the human or tool performing the work.

“Available at no cost,” “legally obtained,” and “permitted to place in an AI prompt” are different facts. The registry records them separately.

### 4.2.1 AI-use rights gate [critical]

The default policy is **deny model access to standards text unless the controlling license or written permission explicitly allows that use**.

For every source, the registry records independent rights flags:

- human reading and note-taking;
- machine parsing by non-generative tools;
- inclusion in model prompts or retrieval context;
- use for model training or fine-tuning;
- test/corpus execution;
- quotation in project artifacts;
- redistribution;
- black-box experimental use;
- patent, standards-essential-patent, trademark, export-control, and other implementation/distribution encumbrance review status where relevant; and
- approved jurisdictions or deployment constraints when a source or algorithm is not globally uniform.

Copyright permission is not the only legal boundary: a technically public algorithm, codec, profile, logo, or test asset may still carry patent, trademark, export, contract, or field-of-use constraints. The registry records “not reviewed” rather than silently treating absence of a known restriction as clearance.

Current ISO public copyright language specifically requires permission for using ISO content to prompt or otherwise enable AI. Therefore:

1. raw ISO publication text is never placed in agent prompts, retrieval indexes, chat logs, generated implementation artifacts, or model-visible CI artifacts unless counsel records an explicit permission basis;
2. an authorized human standards team—or approved non-generative extraction tool—creates concise project-authored `SpecCard`s without copying unnecessary prose;
3. each card undergoes a two-person meaning review against the controlling source;
4. implementation agents receive the card, public errata material whose terms permit use, machine-readable models, and test obligations—not the restricted source;
5. a source-rights scanner rejects unapproved excerpts and records the incident;
6. cards carry a rights provenance distinct from their technical provenance.

The same gate applies to ETSI, ICC, Unicode, font, cryptographic, and other normative or quasi-normative documents. No-cost access is not presumed to grant AI-use or redistribution rights.

### 4.2.2 Clean-room claim boundary for foundation models

MonkeyBee can control active project inputs; it cannot fully inspect proprietary pretraining corpora or prove that a general foundation model never encountered existing PDF-engine code.

Accordingly, the project claims a **clean-room development protocol**, not ontological source purity. Additional defenses are:

- task-local allowed-source manifests;
- source attestations for generated patches;
- rationale tied to `SpecCard`s and generic algorithms;
- code-similarity and suspicious-structure review where legally appropriate;
- independent reimplementation of contaminated work;
- and explicit known-unknown disclosure in the production ledger.

### 4.3 Specification-provenance firewall

The repository contains a `spec/` registry with no casually copied standards prose.

Each requirement becomes a `SpecCard` with:

- stable project ID;
- standard and edition;
- exact clause/table/algorithm reference;
- relevant errata resolution;
- normative level (`shall`, `should`, informative, implementation-dependent);
- project-authored paraphrase;
- input preconditions;
- required behavior;
- failure behavior;
- affected compatibility profiles;
- test obligations;
- linked atomic fixtures;
- linked implementation or consequence contracts;
- linked external profiles;
- known ambiguities;
- and provenance author/reviewer.

Agents implement against rights-cleared cards and contracts. Authorized human reviewers or explicitly approved non-generative tooling maintain the link to the controlling source. A card is not authoritative merely because an agent wrote it; it requires a recorded source review.

### 4.4 Standards registry

The registry records:

- ISO 32000-1 and ISO 32000-2 editions;
- current errata collection identifiers;
- active amendments or technical specifications;
- normative-reference versions;
- PDF/A, PDF/UA, PDF/X, and related profiles;
- Arlington model revision;
- veraPDF corpus/profile revision;
- and project interpretation decisions.

A standards update never silently changes behavior. It creates a registry revision, compatibility assessment, migration notes, and new or updated cards.

**[UNVERIFIED — inherited Revision 7 identifier and status assertions; no licensed or public standards source was contacted in this no-fetch run.]**

For this plan dated 2026-07-14, the inherited identifier-only planning baseline names ISO 32000-2:2020 and the PDF Association’s June 2026 Errata Collection 3 bundle; neither current status nor source authority was verified in this no-fetch run. The registry distinguishes an ISO edition, amendment, or corrigendum from a PDF Association errata-collection publication and records the authority and status of every resolution instead of describing all corrections generically as “formal ISO errata.” ISO 32000-1 remains a historical/compatibility source. ISO/TS 32001, 32002, 32003, and 32004 are registered as separate PDF 2.0 technical-specification profiles rather than folded into “PDF 2.0 core.” ISO/TS 32005:2023 is registered separately with the PDF/UA-2/WTPDF-related accessibility family, not as a core encryption or hash-extension profile. Published amendments become new registry revisions only after their status and source rights are confirmed; drafts under development are tracked as non-authoritative horizon items. This paragraph records identifiers only; access, model visibility, quotation, and implementation use still pass the rights gate above.

The following inherited source line is retained only as byte-exact extraction-membership evidence. It is quarantined from status, authority, claim, and implementation use and supplies no external confirmation:

```text
For this plan dated 2026-07-14, the public planning baseline is ISO 32000-2:2020 (confirmed current by ISO in 2026) plus the PDF Association’s June 2026 Errata Collection 3 bundle. The registry distinguishes an ISO edition, amendment, or corrigendum from a PDF Association errata-collection publication and records the authority and status of every resolution instead of describing all corrections generically as “formal ISO errata.” ISO 32000-1 remains a historical/compatibility source. ISO/TS 32001, 32002, 32003, and 32004 are registered as separate PDF 2.0 technical-specification profiles rather than folded into “PDF 2.0 core.” ISO/TS 32005:2023 is registered separately with the PDF/UA-2/WTPDF-related accessibility family, not as a core encryption or hash-extension profile. Published amendments become new registry revisions only after their status and source rights are confirmed; drafts under development are tracked as non-authoritative horizon items. This paragraph records identifiers only; access, model visibility, quotation, and implementation use still pass the rights gate above.
```

### 4.5 Clean-room audit trail

Every crate contract lists:

- specification cards implemented;
- external algorithm references;
- dev-only comparison engines;
- imported data and license;
- and any code-generation inputs.

Every implementation record and review note includes its governing card IDs.

### 4.6 Black-box oracle firewall

Dev-only adapters may invoke external tools and collect:

- success/failure;
- diagnostics;
- rendered pixels;
- extracted text;
- object inventories;
- and transformed output hashes.

The adapter layer must not:

- expose external headers or APIs to production crates;
- copy implementation-specific internal data structures;
- or treat one processor’s behavior as normative truth.

### 4.7 Corpus licensing

Each corpus item carries:

- an internal content identity and a separately governed public commitment;
- source;
- license or use basis;
- redistribution policy;
- privacy classification;
- whether it may be committed;
- whether only a hash/retrieval recipe may be committed;
- and whether it belongs to training, development, validation, or held-out evaluation.

---


## 6. Non-negotiable principles

### P1 — Safe Rust is the default law

Workspace lints deny unsafe code. Any exception must live in a registered leaf capsule with a `SAFETY.md`, narrow API, independent tests, Miri/sanitizer coverage where applicable, and explicit justification.

### P2 — Clean-room provenance is enforceable

No production implementation is accepted without specification cards and source provenance. Existing engines are black-box oracles, not code donors.

### P3 — Exact bytes are never silently discarded

The source snapshot is immutable. Source-backed syntax and values retain exact source or virtual-span lineage plus the applicable revision-graph/view identity; draft- or transform-derived values retain explicit non-byte origins instead of invented spans. Lossless preservation is a first-class mode, not a debugging afterthought.

### P4 — Strict parsing and recovery are different products

Strict parsing reports what the input means under declared rules. Recovery proposes repairs. A repair must never be smuggled into a “successful parse” without a receipt.

### P5 — Results carry evidence

Important values travel with provenance and epistemic status. A heuristic Unicode mapping or compatibility observation cannot become an exact or normative fact merely because downstream code is deterministic.

### P6 — Budgets precede work

Parsing, decoding, rendering, font execution, transformations, and validation run under explicit limits and cancellation. Potentially unbounded work is a design error.

### P7 — Determinism is classified

Every crate states whether its output is byte-stable, same-platform bit-stable, numerically bounded, profile-dependent, or intentionally fast/noncanonical.

### P8 — Compatibility is data, not folklore

Quirks are named, versioned, evidenced, and scoped to profiles. No anonymous `if broken_file` branches.

### P9 — Transformations are transactions

No mutating operation publishes a partial file. Every transformation declares its semantic, visual, security, signature, and provenance effects.

### P10 — Security-sensitive claims require adversarial evidence

“Removed,” “redacted,” “sanitized,” “signature-valid,” and comparable high-consequence trust claims are stronger than visibility or producer self-report. They require claim-specific independent falsifiers and explicit coverage/no-claim boundaries.

### P11 — Rendering and generation share one semantic core

The writer cannot generate structures that the reader treats through a different ontology. The same typed document and graphics semantics govern both directions.

### P12 — Embedded programs execute under one metered meta-contract

Content streams, calculator functions, font charstrings, TrueType hints, Type 3 procedures, and the bounded Bet 16 form-action tenant are different languages with different capabilities. Every interpreter shares the §11.8 authority, budget, cancellation, dependency-manifest, trace, cycle, transaction, refusal, and rollback laws; no language inherits another tenant’s capabilities by belonging to the same meta-contract.

### P13 — Independent oracles are mandatory

The code, tests, docs, and reviewer may share a mistake. Important claims need heterogeneous evidence.

### P14 — No network or host actions by default

A PDF document never gains ambient authority. External resources, URLs, file launches, and scripts are inert data unless a host explicitly supplies a capability.

### P15 — Operational closure belongs to the artifact

Builds, fuzzing, corpus management, diagnostics, bindings, release engineering, and incident metabolism are core work, not postscript.

### P16 — Agent-first artifacts remain human-legible

Contracts, diagnostics, receipts, and reports are machine-readable and concise enough for agents, while preserving explanations, source references, and stable terminology for humans.

### P17 — No unsupported success

Unsupported, ambiguous, partially covered, resource-exhausted, cancelled, policy-blocked, or crash-indeterminate behavior returns the corresponding typed `Partial`, `Ambiguous`, `Refused`, `Cancelled`, or `Indeterminate` outcome defined by the owning contract. It never produces a best-effort value with a flattering complete/success status.

### P18 — No unbounded moonshot critical path

The solid spine advances continuously. Multiple quarantined [F]/[M] probes may run in parallel when each has its own budget, owner-of-meaning, evidence instrument, integration contract, kill criterion, and fallback. At most one moonshot may block a declared release envelope or demand project-wide architectural churn at a time, and aggregate research concurrency may not exceed the project’s integration and assurance capacity. Parallel search is leverage; parallel semantic debt is not.

### P19 — Compression before accumulation

A new capability should normally be a consequence of existing identities, evidence, budgets, authority, transactions, and operational laws. If it requires a second ontology, a parallel evidence model, an unrelated budget system, a new ambient authority path, or a separate operational constitution, it is presumed to be sediment until it demonstrates extraordinary consequence that cannot be obtained by composition. Irreducible PDF-specific semantics may justify a new local law, but the seam, information loss, and inheritance contract must be explicit. Feature count is never an architectural success metric.

---


## 8. Architecture at a glance

```text
+--------------------------------------------------------------------------------+
| L8 SURFACES                                                                    |
| Rust API | CLI | C ABI | WASM | host adapters | structured reports              |
+--------------------------------------------------------------------------------+
| L7 ASSURANCE                                                                   |
| validators | profiles | evidence checker | differential lab | corpus/fuzz/bench  |
| release claims | foundry evaluation | source-rights and provenance tooling      |
+--------------------------------------------------------------------------------+
| L6 AUTHORING & TRANSFORMATION                                                  |
| writer | deterministic serialization | incremental edits | canonical rewrite   |
| layout adapter | font subsetting | repair writeback | redaction | sanitization  |
+--------------------------------------------------------------------------------+
| L5 SEMANTICS                                                                   |
| text graph | Unicode evidence | logical structure | accessibility | annotations |
| forms as data | actions inventory | signatures | associated files               |
+--------------------------------------------------------------------------------+
| L4 APPEARANCE                                                                  |
| geometry | path/stroke | fonts/glyphs | images | color | patterns | shadings     |
| transparency | compositing | rasterization | page renderer                     |
+--------------------------------------------------------------------------------+
| L3 PAGE PROGRAM                                                                |
| content lexer | typed operators | graphics state | resources | forms | Type 3    |
| calculator functions | optional content | metered interpreter                  |
+--------------------------------------------------------------------------------+
| L2 DOCUMENT                                                                    |
| resolved objects | object histories | catalog | page tree | names/numbers      |
| metadata | Arlington-backed object validation | recovery hypotheses             |
+--------------------------------------------------------------------------------+
| L1 BYTES, RAW COS & REVISIONS                                                  |
| byte sources | spans | file lexer | raw COS | xref tables/streams              |
| object streams | incremental revisions | filters | encryption | preservation    |
+--------------------------------------------------------------------------------+
| L0 FOUNDATION                                                                  |
| budgets | cancellation | diagnostics | evidence | hashing | deterministic math   |
| affine/path primitives | fallible allocation | versioned schemas | unsafe policy |
+--------------------------------------------------------------------------------+
```

### 8.1 Dependency direction

Lower layers never depend on higher layers.

- Foundation knows nothing about PDF object semantics; it may provide representation-neutral affine geometry/path primitives and opaque profile/capability identities, but not a composed PDF recovery/render/security/validation configuration.
- Bytes/revisions own exact lexical tokens and raw COS/storage semantics, not pages or rendering.
- Document resolves object histories into typed relationships, not how page operators paint.
- Page Program knows execution semantics, not output raster details.
- Appearance converts display operations into surfaces.
- Semantics may consume page and appearance data but cannot redefine parsing.
- Authoring may orchestrate all lower layers but does not bypass their contracts.
- Assurance/runtime validators may consume lower-layer outputs; laboratory and foundry tools are dev/release-only and never become hidden core runtime dependencies.
- Surface crates are top-level adapters that may compose released runtime validators and lower layers; they do not own core behavior.
- When a lower semantic engine needs a service implemented by a higher subsystem, the protocol lives at the lower boundary and the higher implementation is injected. In particular, the page VM depends on a format-neutral `FontExecutionService` protocol, while font/CMap/outline implementations depend downward on that protocol; Type 3 procedures return page-program handles for the VM to execute rather than calling upward into it.
- Producing a private writer/transform candidate and independently assuring it are separate stages. L6 never imports L7 laboratories. An L8 assurance coordinator may hold the final `TransactionalOutput`, ask L6 to prepare a private candidate, ask released L7 checkers/adapters to inspect it, and only then authorize publication under the requested claim profile. A core-only caller may choose a weaker internal-check profile, but it cannot receive the stronger independently checked headline.


## 9. The Honeycomb Document Reality Graph

The Honeycomb Document Reality Graph is the central representation of MonkeyBee.

It is not a single giant mutable graph. It is an immutable, typed root lineage plus a family of lazily materialized, content-addressed views connected by explicit derivation receipts.

### 9.1 Reality roots, origins, and operation context

The v0.1 root was source-only and therefore could not represent a document before its first serialization. MonkeyBee instead has three explicit root families with three deliberately different identity commitments: byte snapshot, frozen draft intent, and finalized provenance-bearing transform result:

```rust
#[derive(Clone, Copy, PartialEq, Eq, Hash)]
pub enum RealityRoot {
    Source(SourceRootId),       // one immutable byte snapshot only
    Draft(DraftRootId),         // frozen authoring intent with no source bytes yet
    Transform(TransformRootId), // finalized provenance-bearing result before serialization
}

#[derive(Clone, Copy, PartialEq, Eq, Hash)]
pub enum OriginRef {
    Rooted { root: RealityRoot, node: OriginNodeId },
    Candidate(LocalOriginId), // valid only during root finalization
}

pub enum DerivationBasis {
    Authored,
    From(NonEmptyVec<OriginRef>),
}

pub enum OriginRecord {
    Source { root: SourceRootId, spans: NonEmptyVec<ByteSpanId> },
    Virtual {
        root: SourceRootId,
        container: DecodedContainerId,
        spans: NonEmptyVec<VirtualSpanId>,
    },
    Draft { root: DraftRootId, node: DraftNodeId },
    Derived { intent: TransformIntentId, basis: DerivationBasis },
    Composite { relation: OriginRelation, parts: NonEmptyVec<OriginRef> },
}

pub struct DraftIntentCommitment {
    protocol: DraftIntentProtocolId,
    root: Digest,
}

pub struct SemanticStateId {
    protocol: SemanticValueProtocolId,
    scope: SemanticScopeId,
    root: Digest,
}

pub struct ExpectedStateId {
    protocol: ExpectedStateProtocolId,
    root: Digest,
}

pub enum TransformInput {
    Document {
        role: TransformInputRole,
        root: RealityRoot,
        view: DocumentViewId,
    },
    Asset {
        role: TransformInputRole,
        artifact: ArtifactId,
        origin: OriginRef,
    },
}

pub struct RealityStateCommitment {
    protocol: RealityCommitmentProtocolId,
    semantic: SemanticStateId,
    provenance_root: Digest,
}

pub struct TransformRootRecord {
    inputs: NonEmptyVec<TransformInput>,
    policy: TransformPolicyId,
    operations: TransformLogId,
    result: RealityStateCommitment,
}

pub struct DocumentReality {
    root: RealityRoot,
    identities: IdentityStore,
    revision_graphs: RevisionGraphStore,
    views: DocumentViewStore,
    origins: OriginStore,
    lineages: LineageStore,
}

pub struct EffectiveDocumentView {
    id: DocumentViewId,
    root: RealityRoot,
    revisions: Option<RevisionGraphId>, // Some for source-backed views
    semantic: SemanticStateId,
}
```

A `SourceRoot` binds only one immutable byte snapshot, its availability/integrity contract, and exact byte reality. It does **not** absorb a parser-derived revision graph or one timeless semantic identity. Revision discovery produces immutable, content-addressed `RevisionGraphId` artifacts under an exact discovery protocol/version, observed-range coverage, relevant limits, and recovery/admission assumptions; several graphs may legitimately coexist over the same bytes after a parser, policy, or evidence revision. Opening/resolving returns one or more `EffectiveDocumentView`s that bind the exact source root, revision graph, selected chain/recovery alternative, evidence, coverage, and `SemanticStateId`. Draft/Transform views carry no revision graph until serialization creates source bytes. A `DraftRoot` binds frozen caller intent, role-labeled assets, semantic authoring profiles/data revisions, and explicitly imported roots; concrete layout/shaping implementations remain derivations unless the caller supplies their realized runs as intent. A mutable builder is not a root.

A `SemanticStateId` commits only to admitted document meaning under an explicit `SemanticScopeId`: values, order-sensitive and order-insensitive relationships, multiplicity, and the selected duplicate/unknown-extension semantics. `SemanticScopeId` is itself a canonical manifest—not a friendly label—and enumerates every included meaning axis and every meaning-changing dialect/profile/recovery choice. Current-effective object semantics, full historical semantics, logical structure/accessibility, actions/security/signatures, metadata/navigation, source-positioned page semantics, and realized structured-layout semantics are distinct scopes unless one manifest deliberately includes them together. There is no unqualified universal “semantic identity.” The state ID does not encode which source graph, revision, recovery assumption, or transform history produced that meaning. Two distinct `DocumentViewId`s may therefore share a `SemanticStateId` only under the same exact scope when their admitted meanings are equal, while remaining different interpretations with different evidence, authority, signature history, preservation status, and provenance.

A `DraftIntentCommitment` identifies frozen authoring intent, role-labeled assets/parents, and declared semantic data/profile revisions; it does not pretend that unrealized pagination, shaping, or inferred structure already exists. An `ExpectedStateId` is an operation/admission-specific canonical commitment to the exact preconditions that must still hold before a mutation or finalization may publish: the bound `DocumentViewId`; selected anchors, substrate/range/artifact digests, and semantic predicates; relevant ownership, preservation, signature, policy, authority, capability, and transaction/publication generations; and any immutable external authority snapshots on which the decision depends. It is constructed by validated precondition logic, never from a caller label, timestamp, or mutable version string. Unrelated ambient state is excluded so harmless changes do not cause false staleness; every included predicate is re-evaluated at apply/finalization, and an unavailable or mismatching predicate refuses or returns the explicitly defined indeterminate outcome.

A `RealityStateCommitment` is different: it composes the finalized `SemanticStateId` with the entire admitted origin DAG, exact role-labeled transform input bindings, frozen pre-root transform intentions, and provenance policy. Every document input binding includes the existing root and exact `DocumentViewId`; a root name alone cannot select among historical/recovery interpretations. The operation-specific `ExpectedStateId`, caller/role authorization, capability leases, idempotency/publication generations, and revalidation outcome live in the proposal/admission/`TransformReceipt`, not in the result root: transient host/session state is not document reality, may be sensitive, and must not make semantically and provenance-identical results acquire different `TransformRootId`s. The reality commitment is used to mint a `TransformRootId`, not an unrealized Draft root. Carry/drop/split/merge correspondence remains a separately committed `LineageMap` keyed to already-defined roots and is not fed back into the root whose identity it describes. Post-root `TransformId`s likewise never enter result origins or any pre-root commitment.

Both commitment grammars are versioned, domain-separated, and independent of map, allocation, traversal, scheduling, or thread order. The grammar uses semantic order where order matters, canonical keyed order where keys matter, and unordered multisets with multiplicity where order does not. Structurally indistinguishable semantic nodes form a canonical `SymmetryClassId` plus multiplicity; the public semantic model does not mint arbitrary stable member IDs merely because an implementation allocated several equal nodes. A member becomes individually stable only through an admitted distinguishing anchor such as an ordered occurrence, semantic path, rooted origin, or explicit caller intent. APIs that require an individual stable anchor expose the whole symmetry class/alternatives or refuse when no such anchor exists; ephemeral implementation handles are never serialized as semantic identity. Root-local provenance IDs may still distinguish members through source/draft/origin facts. Finalization refuses only when an advertised identity-sensitive relation truly requires a distinction that neither semantics nor provenance can justify within the declared budget—not for ordinary repeated pages, equal resources, or duplicate equivalent nodes.

Profiles, default limits, host capabilities, caches, and mutable derivation stores are **not part of document truth**. They live in the operation/session environment. The same root may yield different appearances or validation findings under different profiles without becoming a different source document.

Every semantic object has an `OriginRef`; not every object has one contiguous source byte span. `Rooted` references always qualify the owning root. `Candidate` references are confined to finalization and must be mapped to rooted canonical nodes before publication. `Source` and `Virtual` constructors validate ownership; cross-root combinations use `Composite`. `Derived` binds a frozen `TransformIntentId` and distinguishes admitted parentless authorship from actual derivation with nonempty parents. Constructors reject cycles, invented/missing parents, unqualified cross-root IDs, unresolved public candidate references, and unbounded expansion.

### 9.1.1 Immutable source and result identities

A caller-supplied label is provenance, not proof of byte identity. Source identity is typed:

```rust
pub enum SourceIdentity {
    VerifiedContent { algorithm: HashAlgorithm, digest: Digest, len: u64 },
    StableSnapshot { authority: AuthorityId, version_digest: Digest, len: Option<u64> },
    Ephemeral { snapshot_nonce: SnapshotNonce, available: RangeSet },
}
```

For `StableSnapshot`, `AuthorityId` identifies a versioned authority contract, not a service label. Subject to the §9.2.1 ratification gate, that contract fixes the authority scope and contract version, authentication method, canonical version-token input grammar, named digest algorithm and class domain separation, digest width, and the rule that one `(AuthorityId, version_digest)` tuple is never reused for different byte states within that scope. The `version_digest` is the contract-authenticated commitment to the authority's canonical snapshot version input; a mutable name, timestamp, or unverified version string is insufficient. If the authority cannot establish those guarantees, the source is `Ephemeral`. Observation of different bytes under one tuple invokes §9.2 collision quarantine in addition to revocation; no production `AuthorityId` or `version_digest` is minted while the governing identity package remains unratified.

Persistent cross-run caches require `VerifiedContent` or a `StableSnapshot` whose authority contract guarantees immutability. `Ephemeral` identities may use only operation-local caches and may support only `ObservedBytes`, never durable whole-source `ByteExact` evidence. A range inside an authority-stable partial snapshot may be byte-exact for that range, but durable **whole-source** exactness additionally requires a committed final length, whole-source coverage, and successful authentication of every byte; `len: None` or a partial range set cannot be promoted by prose. Source change revokes the snapshot and every reusable claim about its present contents while preserving operation-local evidence of bytes already observed.

A `DraftRoot` hashes its `DraftIntentCommitment`. A `TransformRoot` is minted only after candidate finalization and hashes exact role-labeled root/`DocumentViewId` or asset/origin input bindings, policy/schema semantics, the ordered frozen operation log, and the `RealityStateCommitment`. The associated proposal/admission/receipt binds `ExpectedStateId`, caller authority, capability leases, idempotency, and publication state, but those transient facts are excluded from the root hash. Neither root includes a later `TransformId`, lineage-map ID, root-scoped output ID, or incidental build identity. The `SemanticStateId` inside the reality commitment may be shared by another root whose admitted meaning is equal, but that sharing never authorizes cross-root source preservation, signature conclusions, origin explanation, edit authority, or evidence reuse requiring history.

After finalization, an operation-level `TransformId` is minted from the already-defined `TransformRootId`, its pre-root `TransformIntentId`, and the finalization-receipt class. A validated constructor enforces transform input roles, root/view consistency, expected-state equality, singular-role uniqueness, symmetric-merge semantics, semantic/reality commitment consistency, and resolution of every candidate origin. `NonEmptyVec<TransformInput>` alone is not proof of those constraints.

### 9.1.2 Typed lifecycle states

MonkeyBee shares primitives and provenance across reading and writing, but it does not pretend one mutable object type safely represents every lifecycle state:

```text
Raw syntax
 -> admitted revision/object view
 -> effective semantic document
 -> optional draft/edit/transform intent
 -> finalized DraftRoot or TransformRoot + derivation/lineage receipts
 -> validated write plan
 -> serialized source root
```

Transitions are fallible and receipt-bearing. Expert APIs may construct raw objects, but only admitted documents or validated write plans can reach release writers.

### 9.2 Stable identities

The system uses stable, typed identities rather than bare integers or memory addresses.

| Identity | Meaning |
|---|---|
| `SourceRootId` | One immutable byte snapshot, availability/integrity contract, and exact byte reality; no parser-derived revision graph. |
| `AuthorityId` | One versioned canonical authority contract for `StableSnapshot`: authority scope, authentication, snapshot-version input grammar, digest parameters/domain, and non-reuse/change law. |
| `DraftRootId` | One frozen authoring-intent root identified by `DraftIntentCommitment`; it need not contain a realized semantic document. |
| `DraftIntentProtocolId` | One versioned canonical grammar for frozen authoring intent. |
| `DraftIntentCommitment` | The intent/assets/declared-data commitment used to identify a Draft root, distinct from a finalized result. |
| `TransformRootId` | One immutable provenance-bearing multi-input transform result; transient admission/authorization/publication state remains in receipts, not root identity. |
| `SemanticValueProtocolId` | One versioned canonical grammar for value-and-relationship semantics. |
| `SemanticScopeId` | The canonical manifest of included meaning axes and every meaning-changing dialect/profile/recovery choice whose equality is asserted. |
| `FieldDefinitionId` | One versioned canonical eligibility boundary for a comparative field: atomic capability/output contract, openness/channel/license, implementation-language/runtime restrictions if any, platform/jurisdiction, and other inclusion rules. |
| `SemanticStateId` | A provenance-free commitment to admitted document meaning under one scope. |
| `ExpectedStateProtocolId` | One versioned canonical grammar for operation-specific publication preconditions. |
| `ExpectedStateId` | One validated commitment to the exact view, anchors, substrate/policy/authority predicates, and generations that must still hold before mutation/finalization may publish. |
| `SymmetryClassId` | One canonical semantic equivalence class plus multiplicity when individual members have no admissible stable distinction. |
| `RealityCommitmentProtocolId` | One versioned grammar for combining semantic state with origins, inputs, and frozen intents. |
| `RealityStateCommitment` | The provenance-bearing finalized semantic-result commitment used by a Transform root; not a substitute for Draft intent identity. |
| `TransformLogId` | One immutable ordered log of frozen transform intentions. |
| `TransformIntentId` | One pre-root-local intention qualified by its `TransformLogId`. |
| `OriginNodeId` | One canonical root-local origin DAG node; cross-root references qualify the root. |
| `RevisionGraphId` | One immutable, content-addressed discovered revision/object-occurrence graph over a `SourceRootId`, qualified by discovery protocol/version, coverage, limits, and assumptions. |
| `RecoveryHypothesisId` | One bounded recovered interpretation over an exact `RevisionGraphId`, with an exact assumption/evidence set. |
| `DocumentViewId` | One immutable effective interpretation binding its root, optional source-backed `RevisionGraphId`, selected revision/recovery alternative, dialect, semantic/security policy, outcome-sensitive limits, coverage, semantically relevant capability identities, and resulting `SemanticStateId`. |
| `DerivationId` | One derived-view context binding parent state/artifacts, algorithm, profile, validated dependency/selection manifest, limits, and build identity where required. |
| `ByteSpanId` | A half-open byte range in a source. |
| `RevisionId` | One candidate revision occurrence/node scoped to a `RevisionGraphId`. |
| `IndirectKey` | PDF object number and generation number. |
| `ObjectVersionId` | One defining occurrence of an indirect object in one `RevisionId`/`RevisionGraphId`; cross-graph continuity is evidence, not ID equality. |
| `DecodedContainerId` | One decoded container under a source/object/security/filter/algorithm identity. |
| `VirtualSpanId` | A logical range inside one identified decoded container. |
| `DraftNodeId` | One stable node of frozen authoring intent. |
| `PageId` | One page node inside a specific `DocumentViewId`. |
| `ProgramNodeId` | One operator or operand group inside a specific program derivation. |
| `PrimitiveId` | One emitted appearance primitive. |
| `GlyphInstanceId` | One painted glyph instance. |
| `SemanticNodeId` | One extracted text, structure, annotation, or accessibility node. |
| `ClaimId` | One evidence-bearing statement. |
| `ClaimRegistryId` | One versioned generated snapshot of atomic claim-to-consequence-contract links, composition edges, lifecycle, evidence scope, and no-claim boundaries under §10.10. |
| `SpecCardId` | One versioned project-authored clean-room requirement unit whose authority remains conditional on the §4 source and review record. |
| `ConsequenceContractId` | One versioned machine contract for an atomic operation, profile-qualified capability, or atomic comparison subclaim under §10.10. |
| `EvaluationProtocolId` | One immutable pre-unblinding evaluation-protocol commitment under §10.6. |
| `CompetitorDiscoveryProtocolId` | One immutable pre-search field-discovery protocol commitment under §10.6. |
| `CompetitorDiscoveryReportId` | One immutable, independently frozen execution report for a `CompetitorDiscoveryProtocolId` under §10.6. |
| `SemanticReportProtocolId` | One versioned canonical value grammar for semantic report bodies, including the report-family schema/version and every identity-bearing field. |
| `SemanticReportId` | One content commitment to a semantic report body only; run observations and operational telemetry are outside its domain. |
| `RunObservationProtocolId` | One independently versioned canonical value grammar for run observation envelopes and their linkage to semantic reports. |
| `RunObservationId` | One content commitment to a run observation envelope that binds exactly one `SemanticReportId`. |
| `TransformId` | One post-root operation/receipt identity; never an input to its root. |
| `ArtifactId` | One content-addressed output artifact. |
| `LineageMapId` | One versioned correspondence set between already-defined roots. |

Root-intrinsic, revision-discovery, semantic-value, reality/provenance, and derived-view identities are different domains. Byte spans are source-root-scoped; revision and object-version occurrences are revision-graph-scoped; page/program/appearance/text IDs are view/derivation-scoped. A new parser or recovery protocol may produce a new `RevisionGraphId` over unchanged source bytes without rewriting source truth. Semantic equality says nothing about common source bytes, lineage, signatures, authorization, or preservation; reality equality says nothing about a particular rendering profile. Cross-root, cross-graph, and cross-view continuity therefore travels only through exact byte anchors or evidence-bearing conversion/lineage receipts.

Content-addressed identities use a project-wide versioned grammar with class/version domain separation, length framing, a named hash algorithm, canonical encodings, and collision quarantine. A digest is an index—not authority, authorization, or proof of semantic interchangeability. Insertion rechecks class, length, canonical metadata, and bytes where available. Same-identifier/different-content observations quarantine both records and trigger identity-protocol migration; “first writer wins” is forbidden.

### 9.2.1 Identity-encoding ratification gate

Section 9.2 is the normative home for the identity grammar's required properties. This subsection does not select an octet grammar, hash family, or digest width. D1 and D2 offer coupled alternatives and remain `PROPOSED — awaiting human ratification`; a proposal in those records is not Constitution law merely because it is usable for planning.

Before a production identity may be minted, the ratified protocol manifest must fix the exact identity/commitment serialization grammar, protocol and class domain separation, length framing, canonical treatment of every admitted value, extension and rejection rules, named hash algorithm, and digest width. The selected encoding must be deterministic and injective over admitted values, reject ambiguous encodings, keep the identity/commitment grammar distinct from PDF output serialization, and preserve §9.2 collision quarantine. Producer and independently authored checker encoders require separate implementations and adversarial differential vectors if the D2/D4 proposal is ratified. Until the package is ratified, identity construction and independent-checker support are unavailable rather than inferred.

The ratification must occur before the campaign's first external or tamper-evident commitment. A digest committed under an unratified algorithm/grammar cannot later be replaced while preserving the original commitment's timestamp semantics.

`DecodedContainerId` remains the sole Rev 7 canonical name. D3 proposes a pre-decode recipe identity under the source/object/security/filter/algorithm tuple plus a distinct post-commit `DecodedArtifactDigest`; that availability/cost split remains `PROPOSED — awaiting human ratification` and does not amend §9.2 in this extraction. `DecodedStreamId` is campaign-layer drift recorded in D-004, not an alias to expose and not a second identity class. Runtime dependency and cryptographic-crate selection remain pending under D-005.

### 9.3 The eight primary views

#### View A — Byte and revision reality

Represents:

- exact bytes and spans;
- header and EOF markers;
- `startxref` candidates;
- cross-reference sections;
- trailers;
- object occurrence locations;
- incremental update relationships;
- signature byte ranges;
- and unexplained byte regions.

This view answers “what bytes exist, and when did they enter history?”

#### View B — COS and document-object reality

Represents:

- primitive COS values;
- arrays and dictionaries;
- streams;
- indirect references;
- object versions;
- catalog and page-tree relationships;
- inherited attributes;
- names and number trees;
- metadata;
- and standardized object-model constraints.

This view answers “what object relationships does the file assert?”

#### View C — Executable page-program reality

Represents:

- content-stream token boundaries;
- operands and operators;
- resource scopes;
- graphics-state transitions;
- nested forms;
- marked-content boundaries;
- optional-content gates;
- Type 3 character procedures;
- calculator functions;
- and execution refusals.

This view answers “what program does a page ask a conforming processor to run?”

#### View D — Appearance reality

Represents:

- paths;
- strokes and fills;
- clipping regions;
- glyph outlines;
- images and masks;
- patterns and shadings;
- transparency groups;
- compositing operations;
- output-profile color transforms;
- and final raster tiles.

This view answers “what visible consequence was produced under this declared profile?”

#### View E — Glyph and text reality

Represents:

- character-code spans;
- CMap interpretation;
- font-program glyph selection;
- glyph positioning;
- Unicode candidates;
- actual-text and alternate-description sources;
- word and line hypotheses;
- and reading-order hypotheses.

This view answers “what was painted, and what textual meaning can be justified?”

#### View F — Logical structure and accessibility reality

Represents:

- structure elements;
- marked-content references;
- object references;
- role and class maps;
- namespaces;
- parent-tree relationships;
- alternate descriptions;
- language declarations;
- annotation associations;
- and conformance-profile findings.

This view answers “what logical document did the producer claim to encode?”

#### View G — Security and behavior reality

Represents:

- encryption state;
- permissions;
- signatures and revision coverage;
- actions;
- JavaScript presence without execution;
- launch and URI behavior;
- embedded files;
- rich media;
- XFA packages;
- optional-content visibility;
- hidden or clipped content;
- and sanitization findings.

This view answers “what behavior or retained information matters for trust?”

#### View H — Compatibility reality

Represents observations under named, versioned profiles:

- strict ISO interpretation;
- MonkeyBee compatibility policies;
- external viewer or renderer behavior;
- printer or RIP behavior when available;
- archival validators;
- accessibility validators;
- and deliberately emulated historical quirks.

This view answers “which processors do what, and why do they disagree?”

### 9.4 Raw and interpreted COS values

The core object layer distinguishes source-preserving syntax from interpreted value.

A number is not stored only as `f64` or `i64`. It may carry:

- raw token bytes;
- parsed mathematical value;
- integer-versus-real lexical form;
- overflow or underflow status;
- normalization eligibility;
- and source span.

A name carries:

- exact escaped source spelling;
- decoded name bytes;
- and whether decoding required recovery.

A string carries:

- exact literal or hexadecimal syntax;
- encrypted source bytes;
- decrypted bytes when authorized;
- escape interpretation;
- and text-decoding claims separately.

A dictionary preserves:

- entry order;
- duplicate keys;
- exact key and value spans;
- and the selected semantic winner under each profile.

This is mandatory for source preservation, forensics, divergence explanation, and honest handling of malformed files.

### 9.5 Virtual provenance inside compressed containers

Objects inside object streams and instructions inside decoded streams do not have direct source-file byte ranges for their decoded forms.

MonkeyBee represents both levels:

```text
file byte span
  -> filter/decryption derivation
  -> decoded-container artifact
  -> virtual decoded span
  -> parsed object or program node
```

Every virtual span therefore carries:

- the source stream object version;
- source file span;
- filter chain and decode parameters;
- cryptographic context;
- decoded artifact hash;
- logical offset and length;
- and diagnostics generated during decoding.

A report must never invent a direct file offset for data that exists only after decoding. Container-level provenance is not automatically byte-granular causality: compression, encryption, prediction, color transforms, and executable font programs may map many source bits to many derived values. Exact inverse attribution is a separate optional claim requiring a transform-specific trace; otherwise the defensible endpoint is the virtual span, derivation identity, and enclosing source range.

### 9.6 Lazy derivation and invalidation

Views are materialized on demand. A page thumbnail does not require full text extraction, full structure validation, or unrelated attachment decoding.

A derivation declares which identity domain it consumes. A pure normalization over a serialization-total semantic scope may key from `SemanticStateId`. Byte-only source operations bind `SourceRootId`; revision discovery binds `SourceRootId` plus its discovery protocol; every selected-history, recovery, signature, preservation, explanation, mutation, render, extraction, or security operation binds the exact `DocumentViewId` and therefore its `RevisionGraphId` when source-backed. Provenance-bearing Draft operations additionally bind `DraftIntentCommitment`; finalized Transform operations bind `RealityStateCommitment`. Semantic equality alone never authorizes history-, evidence-, authority-, or preservation-sensitive reuse.

A committed `DerivationId` and cache entry bind parent identity in the proper domain; input objects/origins/spans; algorithm/version; exact layer-local policy views; outcome-sensitive limits; isolation/security context; feature flags; entropy where intentional; build identity where reproducibility requires it; and a validated dependency-and-selection manifest. The manifest includes positive resources consumed and every selection-set snapshot, priority witness, negative dependency, authority version, absence fact, or fallback condition whose change could alter the result.

Because lazy work cannot know that manifest at first lookup, reuse is two-stage. A conservative candidate index may locate possible entries, but it never authorizes reuse. The engine then reruns deterministic selection or authenticates the entire relevant authority snapshot under the current least-authority lease and proves that every manifested dependency, selection witness, policy relevance, availability, sensitivity class, and isolation domain still matches. The candidate index itself is partitioned by tenant, security context, sensitivity/disclosure class, and cache-isolation domain; protected classes do not share an existence-revealing index unless a separate side-channel profile admits and measures lookup timing, hit/miss, size, and metadata disclosure. A deterministic preflight may bypass candidate search only where its contract proves the exact manifest needed for the computation. Mutable, newly relevant, unavailable, unauthorized, ambiguous, or changed dependencies cause a miss or refusal. `DerivationId` is minted only after execution or successful manifest validation.

D0/D2 promises and replay bundles bind this validated manifest—not a vague list of resources noticed after the fact. Candidate indexing may over-select for efficiency; semantic reuse is legal only after validation. Generated documents and edit transactions form new roots, and derived artifacts are reused only when the proper identity domain plus every manifested dependency matches.

### 9.7 View-conversion receipts

Every transition between views produces a receipt containing:

- input IDs;
- output IDs;
- algorithm and semantic version;
- applied `SpecCard` IDs;
- active profiles;
- consumed limits;
- diagnostics;
- evidence facets;
- determinism class;
- and no-claim boundaries.

The receipt is small enough to retain even when large intermediate data is evicted.

### 9.8 No global flattening

MonkeyBee will not irreversibly flatten every page into one display list as its canonical internal truth.

Flattened or optimized display lists are derived artifacts. They may be excellent rendering accelerators, but they can discard:

- resource-scope structure;
- operator boundaries;
- marked content;
- source spans;
- repeated form identity;
- and distinctions required for editing or explanation.

The source program remains authoritative for program semantics.

### 9.9 Honeycomb kill criterion

The representation is justified only if it reduces cross-feature duplication.

After the first renderer, extractor, validator, and editor vertical slices exist, measure:

- number of duplicate parsers or object models;
- percentage of user-visible outputs with end-to-end provenance;
- change-propagation cost for one held-out feature;
- and number of forced conversions that discard information.

If the Honeycomb design adds substantial overhead while each subsystem still builds its own ontology, stop adding views and redesign the shared identities before expanding scope.

---


## 10. Evidence, claims, diagnostics, and provenance

### 10.1 Evidence is a vector, not a confidence score

MonkeyBee does not assign one universal confidence number to a result.

A claim may be exact in one dimension and uncertain in another. For example:

- the source bytes for a glyph code may be exact;
- selection of a glyph ID may be normative;
- the Unicode mapping may be heuristic;
- and the reading order may remain ambiguous.

The evidence model therefore stores independent facets **inside an outcome model that says whether a singular value exists at all**.

```rust
pub struct Claim<T> {
    value: T,
    evidence: EvidenceSet,
    provenance: Provenance,
    scope: ClaimScope,
    diagnostics: DiagnosticSetId,
}

pub enum CandidateCoverage {
    Complete,
    Partial(PartialCoverage),
}

pub struct PartialCoverage {
    requested: ClaimScope,
    covered: NonEmptyVec<CoverageRegion>,
    missing: NonEmptyVec<MissingRegion>,
}

pub struct PartialClaim<T> {
    claim: Claim<T>,
    coverage: PartialCoverage,
}

pub struct ClaimAlternative<T> {
    claim: Claim<T>,
    coverage: CandidateCoverage,
}

pub enum ClaimOutcome<T> {
    Complete(Claim<T>),
    Partial(PartialClaim<T>),
    Ambiguous {
        alternatives: NonEmptyVec<ClaimAlternative<T>>,
        discriminators: Vec<Discriminator>,
    },
    Refused {
        reason: RefusalReason,
        provenance: Provenance,
        diagnostics: DiagnosticSetId,
    },
}
```

`Refused` has no fabricated `T`. `Partial` contains a distinct `PartialClaim<T>` and therefore cannot carry `Complete` coverage even accidentally. `Ambiguous` carries alternatives rather than a value plus a contradictory flag, and each alternative may have different coverage. Validated constructors require a partial coverage record to match the enclosed claim scope and partition that scope into disjoint covered and missing regions; coverage cannot claim completeness while a second field says something is missing. Cancellation and transport failures remain operation results, not epistemic facets.

### 10.2 Core evidence facets

| Facet | Meaning |
|---|---|
| `ByteExact` | Directly determined from an identified verified-content or authority-stable immutable snapshot and exact byte range; eligible for durable replay only while that snapshot contract remains valid. |
| `ObservedBytes` | Exact bytes returned during one operation from an ephemeral or incompletely authenticated source; useful evidence of that read, but not a durable identity or whole-source claim. |
| `DeterministicallyDerived` | Reproducibly derived under a versioned algorithm; this does **not** imply mathematical exactness or normative correctness. |
| `BoundedApproximation` | Carries a declared metric, domain, and numerical or visual error bound. |
| `UnboundedApproximation` | Uses an approximation but has no defensible bound; downstream claims retain that weakness. |
| `NormativeBasis` | Cites rights-cleared `SpecCard`s and states the preconditions under which the rule applies. |
| `ProfileDefined` | Chosen by an explicit processing profile where the controlling specification or application contract permits alternatives. |
| `CompatibilityObserved` | Observed from named external processors or devices under a reproducible experiment. |
| `Recovered` | Depends on explicit malformed-input repair assumptions. |
| `Heuristic` | Inferred by a versioned algorithm that is useful but not normatively determined. |
| `ExternalCheck` | Checked by a separately authored validator, oracle, device, or tool under a named protocol and scope; the payload records known shared code, data, model, standards interpretation, and institutional lineage rather than asserting absolute independence. |
| `CallerAttestation` | A statement made by an identified caller or reviewer, such as legal embedding authority or human-approved alternate text; proves who attested under which policy, not that the statement is objectively true. |
| `EmpiricalMeasurement` | Anchored to measured behavior with environment, calibration, and uncertainty metadata. |
| `MechanizedProof` | A named theorem was checked by a named proof kernel/version under an explicit trusted base, axioms, model-to-code correspondence, and scope. It proves only that theorem under those assumptions, not the whole artifact. |
| `CryptographicCheck` | A specified cryptographic relation was verified; trust, authorization, and legal validity remain separate claims. |

Facets can coexist. They do not form a simple total order. Outcome state (`Complete`, `Partial`, `Ambiguous`, `Refused`) is intentionally outside this set.

`EvidenceSet` is a validated, canonically ordered keyed structure rather than an unrestricted `Vec<EvidenceFacet>`. Each facet is scoped to a named subclaim, metric, region, profile, source snapshot, and protocol version. Duplicate-identical observations deduplicate; distinct corroborating observations remain separate; and mutually incompatible payloads for the same key are rejected or represented as an explicit higher-level ambiguity. This prevents callers from attaching, for example, two contradictory bounds or two incompatible normative interpretations to one singular claim while still calling the evidence set “composed.”

### 10.2.1 Oracle lineage and correlation

“External” is not synonymous with independent. Two validators may share the same rule data, parser library, model family, corpus, or standards interpretation. Every corroborating observation therefore records a compact `OracleLineage` containing producer, implementation family, shared dependencies/data where known, protocol author, environment, and adjudication relationship. Reports summarize evidence diversity and known correlation; they do not count ten correlated wrappers as ten independent falsifiers. Unknown lineage is explicit uncertainty, not assumed independence.

### 10.3 Claim composition rules

Composition is not generic set union. Each operation registers a claim algebra describing required inputs, scope propagation, approximation metrics, and refusal conditions; unknown compositions fail closed.

1. A derived claim inherits every decision-critical weakness of its inputs.
2. Deterministic computation cannot upgrade heuristic meaning into normative meaning.
3. External processor agreement cannot make malformed input conforming.
4. Compatibility evidence cannot silently redefine the standard.
5. A recovered object remains recovered even when later rendering is deterministic.
6. A partial scan cannot authorize a whole-document security claim.
7. A source-preserving rewrite cannot claim semantic preservation unless semantics were actually checked.
8. A visually equivalent rewrite cannot claim secure redaction unless historical and hidden representations were independently searched.
9. A majority of external engines is not a normative oracle.
10. A claim with unresolved alternatives must expose them or refuse a singular headline.
11. A deterministic floating-point or raster computation is not `ByteExact`; it is deterministic and, where justified, bounded.
12. `NormativeBasis` proves only that a rule is the declared basis; satisfaction of that rule is a separate claim.
13. An external validator’s “pass” is scoped to its version, profile, executed rules, and input; it cannot mint an unscoped `ExternallyValidated` badge.
14. Cryptographic digest validity cannot promote signer identity, trust, authorization, modification permission, or legal effect.
15. Claim constructors are issuer-capability-gated. Ordinary callers cannot manufacture `NormativeBasis`, `ExternalCheck`, `EmpiricalMeasurement`, `MechanizedProof`, `CryptographicCheck`, or a signer/role-bearing `CallerAttestation` from strings. An authenticated caller may issue only its own scoped attestation under the admitted policy; proof kernels, validators, measurement harnesses, cryptographic verifiers, and standards authorities each mint only their own facet class and scope.
16. `ObservedBytes` cannot be promoted to durable `ByteExact` without completing or authenticating the source snapshot under an admitted identity contract.
17. `CallerAttestation` can authorize a policy decision but cannot upgrade a heuristic, legal, semantic, or factual claim by itself.
18. Corroboration strength is reduced when oracle lineage is shared or unknown; quantity of observations never substitutes for diversity of failure modes.
19. External-recognition output carries `Heuristic` plus tool/protocol provenance and, where measured, `EmpiricalMeasurement`; a recognizer-provided confidence number does not become MonkeyBee confidence or exact source text.
20. A `MechanizedProof` is scoped to its theorem, formal model, proof checker, assumptions, and correspondence evidence. It cannot upgrade unrelated empirical, compatibility, implementation, or build claims into proof.
21. A supremacy result is a dated comparison claim, not a normative truth. It must name the competitor’s released version, corpus, metric, threshold, environment, refusal accounting, and observation expiry; agreement or victory cannot launder malformed input into conformance.
22. A transparency-log inclusion or consistency check proves only the stated log relation for the signed receipt. It does not prove that the underlying render, transform, profile, binary, or source claim is true.
23. A producer-phenotype recovery prior carries `Heuristic` and `EmpiricalMeasurement`, applies only after recovery admissibility gates, and remains scoped to its producer classifier, corpus, calibration interval, drift status, and uncertainty; a missing or spoofed producer marker cannot create admissibility or erase nondominated alternatives.
24. A receipt signature authenticates a scoped assertion by a named signer role; it does not establish that the asserted computation occurred correctly. Project release keys authenticate release/build manifests and are not reused as general operation-signing keys.
25. A transparency-log proof establishes only the declared commitment, inclusion, consistency, or freshness relation. A checker or replay establishes only the exact recomputation/equivalence relation it executes; normative correctness, fidelity, safety, and policy satisfaction still require their separately grounded claims and oracles.
26. External recognizer, agent-protocol, validator, and competitor outputs are hostile data. Their text, metadata, confidence, links, or embedded instructions cannot mint capabilities, alter policy, select tools, or authorize a transformation.
27. A benchmark aggregate cannot combine incommensurate axes into a superiority headline unless a predeclared decision rule and tradeoff interpretation are justified. Missing, unsupported, timed-out, indeterminate, and disqualified observations remain visible rather than disappearing from the denominator.
28. A profile or accessibility-validator pass is scoped to executed rules and input; it cannot prove semantic quality, usability, human intent, legal compliance, or absence of human-review obligations.
29. Supremacy-claim lifecycle (`proposed`, `active`, `lapsed`, `withdrawn`), comparison outcome (`leading`, `equivalent`, `non_inferior`, `trailing`, `incomparable`, `indeterminate`, `disqualified`), field status (`contested`, `uncontested`, `not_assessed`), exact `FieldDefinitionId`, and claim scope (`named_set_lead`, `registered_open_field_lead`, or `observed_field_lead`) are orthogonal. Two-sided equivalence and one-sided non-inferiority are not interchangeable; a published ledger may remain active while MonkeyBee trails or is incomparable.
30. Only an uncertainty-aware `leading` outcome under its exact declared field scope supports a supremacy headline. Equivalence/non-inferiority are intermediate gates; `incomparable` records a predeclared tradeoff with no justified winner; `uncontested` is a comparator-search status and is neither superiority nor global absence. No report may call itself globally best.
31. Product-lane superiority contributes artifact-substance evidence only. It does not establish foundry or lineage alienness, equal-resource production disproportion, or the final §33 label.
32. Replay, reproducibility, remote attestation, or GPU/CPU equivalence cannot upgrade the correctness of the repeated or reference computation; each proves only its declared relation.
33. Comparative empirical evidence must name its primary analysis unit, paired/cluster structure, dependence assumptions, minimum effect or precision target, multiplicity policy, stopping/peeking rule, and missingness treatment. Pages, pixels, glyphs, or repeated runs nested inside one document are not independent documents.
34. A stochastic or mutable competitor/model run records seeds where available, provider/model route observations, attempt budget, repeated-run protocol, selection/best-of-N rule, and drift window. Optional stopping after a favorable run or hiding failed attempts disqualifies the headline.
35. `named_set_lead` is a result only over the exact enumerated artifacts. `registered_open_field_lead` additionally requires an exact `FieldDefinitionId`, prospectively committed discovery protocol, frozen discovery report, and independent challenge window over that declared open released field. `observed_field_lead` adds the material lawfully pinnable closed/opaque systems actually observed under the same field definition. Incomplete discovery can support only `named_set_lead`; silence or documentation absence never proves field absence.
36. A predeclared evaluation is strong only when its canonical protocol commitment existed before unblinding or measurement and was independently time-committed. Any material post-commit change creates a new `EvaluationProtocolId`; old and new results cannot be spliced.
37. Repeated access to a hidden corpus consumes a declared query/submission budget. Once feedback permits adaptive tuning beyond the frozen policy, the set is development data, not held-out evidence; only a fresh independently stewarded replacement restores the stronger claim.
38. Semantic-state equality cannot upgrade provenance, common-history, authorization, signature, source-preservation, or origin claims. Those require the exact reality/provenance identity and receipts.
39. Structural, empirical, and adaptive maturity are distinct claim families. Proofs, fuzzing, and simulation can establish structural maturity; they cannot be relabeled as elapsed operational experience.
40. Feature count, repository size, or surface breadth cannot substitute for consequence compression. A claimed architectural mechanism must show specification, verification, or integration leverage over a strong ordinary alternative.

### 10.4 Diagnostics are durable values

A diagnostic is not an English string.

```rust
pub struct Diagnostic {
    pub code: DiagnosticCode,
    pub severity: Severity,
    pub category: Category,
    pub primary: Option<Location>, // None for a genuinely root/global condition
    pub related: Vec<Location>,
    pub spec_cards: Vec<SpecCardId>,
    pub policy_contexts: Vec<PolicyContextId>,
    pub message_args: DiagnosticArgs,
    pub suggested_actions: Vec<ActionHint>,
    pub evidence: EvidenceSet,
}
```

Diagnostic codes are stable within a major schema version.

Messages may improve without changing codes. Reports carry structured arguments so tools never need to scrape prose.

A diagnostic budget never turns a truncated report into a complete report. When events exceed the budget, the sink retains deterministic first examples, severity/code counts, affected-scope summaries, and a `diagnostics_truncated` outcome marker. Security-critical severities use reserved capacity so low-value floods cannot evict the only high-consequence finding.

Core operations do not call arbitrary host diagnostic callbacks while parser, VM, allocator, transaction, or lock state is live. `WorkContext` carries a project-owned, bounded `DiagnosticCollector` whose storage policy is part of the operation. The collector is `Sync` and uses bounded interior mutability so parallel child contexts may record diagnostics without sharing unsynchronized mutation. Recording executes no host code; reservations and per-worker batches merge by a versioned deterministic ordering rule, with severity-reserved capacity preserved across workers. Here, non-re-entrant means that recording cannot invoke a host observer or recursively enter the semantic operation, not that parallel children are forbidden. Optional host observers receive redacted, immutable batches only at documented safe boundaries through an adapter outside the semantic core. An observer may stop observing, but it cannot block engine progress, call back into the operation, retain protected payloads outside policy, unwind across the core boundary, or change the operation outcome. Observer failure leaves the collector's deterministic reserved summary intact and marks `diagnostic_observer_failed`; it cannot erase the original error or make a report appear complete.

### 10.5 Diagnostic locations

Locations may identify:

- source byte spans;
- virtual decoded spans;
- object versions;
- dictionary entries including duplicate occurrence index;
- page-program nodes;
- appearance primitives;
- glyph instances;
- structure nodes;
- transform operations;
- or external-observation artifacts.

A diagnostic can therefore connect “invalid `ToUnicode` range” to both the CMap bytes and the affected glyphs.

### 10.6 Required report families

#### `OpenReport`

Records:

- exact `SourceRootId` and source identity/availability class;
- every produced `RevisionGraphId`, discovery protocol/version, observed-range coverage, limits/assumptions, and supersession relation;
- selected `DocumentViewId` or explicit live alternatives;
- strict-parse result;
- recovery status;
- encryption state;
- for caller-credential standard-handler read decryption, the requested operation/profile and scope, non-secret capability identity and admission result, canonical outcome (`NotRequested`, `InventoryOnly`, `Refused`, `Partial`, `Complete`, or `Indeterminate`), refusal or indeterminacy reason, exact revision/object/range coverage, produced `DocumentViewId` and `DerivationId` where applicable, deterministic diagnostics, and evidence; passwords, keys, and credential-derived secrets are never report fields;
- every header candidate and its exact offset, binary-marker presence, declared version, pre-header bytes, conflicts, evidence, and recovery assumptions;
- per-revision/effective-chain `EffectiveDialect` history with `declared`, `required_by_features`, `selected_for_interpretation`, and `target_for_write` facts, extension/profile inputs, unresolved conflicts, and evidence, rather than one timeless document-wide version scalar;
- signatures found;
- the exact-preservation interval ledger as independent, overlapping facets for parse/semantic ownership, raw-preservation requirement, explained/unexplained subranges, revision membership/supersession, cryptographic coverage, disclosure/sensitivity class, and transformation carry/drop intent;
- metadata inventory and reconciliation across revisions;
- the security/behavior reachability-and-effect inventory across every admitted revision/view/hypothesis, with per-node trigger, target, revision, visibility, required host capability, executable-feature class, sanitization state, evidence/provenance, and explicit analyzed/unavailable coverage;
- unexplained bytes;
- resource-limit usage;
- and overall no-claim boundaries.

The `unexplained bytes` field is the exact normalized union projection of the ledger's `unexplained subranges` facet for the report's declared source coverage. Empty and absent remain distinct where the schema says so; a projection mismatch is invalid. The other interval facets remain independent and may overlap.

#### `RenderReport`

Records:

- exact `SourceRootId`, source availability and integrity class, and a whole-source content identity only when final length, whole-source coverage, and authentication establish it; otherwise the content identity is absent with an explicit reason;
- exact `DocumentViewId`, `RevisionGraphId` where source-backed, and render `DerivationId`;
- selected revision or recovery hypothesis and its selection evidence;
- effective dialect for that selected revision/view;
- page and box selection;
- output profile;
- compatibility profile;
- raster dimensions;
- color pipeline;
- substitutions;
- skipped or refused operators;
- warnings and refusals;
- unsupported or policy-blocked features beyond the operator surface;
- resource-limit usage and any fired semantic limit;
- cache identity;
- determinism class;
- and pixel-artifact hash.

#### `TextReport`

Records:

- exact `DocumentViewId`, `RevisionGraphId` where source-backed, and extraction `DerivationId`;
- glyph count;
- exact character-code spans;
- text-view class (`PaintedGlyphText`, `ReplacementText`, `AccessibilityText`, or `SearchText`);
- per-span source-code, font/CMap, CID/GID, visibility, and evidence facts;
- Unicode coverage by evidence class;
- missing or conflicting mappings;
- reading-order algorithm;
- returned order type (logical, visual, tagged, or search-oriented) and ranked alternatives where order is ambiguous; an order label does not assert correctness;
- structure linkage;
- zero or more exact `SemanticReportId` links to `ExternalRecognitionReport` evidence, with native and recognized spans/alternatives kept separately classified;
- and omitted regions.

#### `ExternalRecognitionReport`

Records:

- exact `SourceRootId`, source-backed `RevisionGraphId`, `DocumentViewId`, recognition/merge `DerivationId`, and admitted page, region, or derivative-artifact scope;
- exact request and response `ArtifactId`s with availability classes, external capability identity, endpoint/tool/model observation, and the host admission/authority result without treating a service label as stable behavior;
- transmitted scope, sensitivity class, egress/retention policy, least-disclosure decision, and request/response truncation or refusal;
- hostile-response schema/limit validation and every rejected, unavailable, or indeterminate part;
- per-span native and recognized alternatives, conflicts, evidence class, confidence semantics, and merge decision without overwriting source truth or laundering confidence; and
- replay/recomputation relation, mutable-service limitations, deterministic diagnostics, coverage, evidence, and no-claim boundaries.

#### `ValidationReport`

Records:

- exact `DocumentViewId` and source-backed `RevisionGraphId` whose meaning/history was validated;
- exact validation `DerivationId`, checker build identity, and checker protocol/schema version;
- profile and profile version;
- rule set;
- per-rule implementation identity and version;
- canonical per-rule outcome (`Pass`, `Fail`, `NotApplicable`, `NotEvaluated`, `Unsupported`, or `Indeterminate`) plus separate severity and coverage;
- source, virtual-span, object, semantic, or global locations as applicable;
- external-validator comparisons;
- and unsupported rule classes.

#### `RecoveryReport`

Records:

- exact `SourceRootId` and input `RevisionGraphId`;
- each generated hypothesis and resulting candidate `DocumentViewId`;
- evidence and violations;
- ordering dimensions, admissibility gates, and nondominance relations;
- caller/task-local selection, including the policy identity, or an explicit statement that no singular selection was made;
- materially distinct alternatives;
- search budget;
- and downstream objects affected.

#### `TransformReceipt`

Records the immutable **private candidate** produced by the transformation core:

- exact role-labeled input bindings: reality root, `DocumentViewId` and expected state for each document input, or exact artifact/origin for each asset; plus candidate/output roots;
- edit intent;
- bytes, objects, and revisions changed;
- visual, text, structure, security, and signature deltas that the core itself can establish;
- internal profile checks;
- candidate-local falsifiers;
- for a proposal-mediated apply, a distinct apply-admission subrecord binding the rechecked `ExpectedStateId`, authority/capability/policy snapshots, validation and apply outcomes, all-or-nothing batch result, durable idempotency request/outcome identity and retention state, crash-reconciliation status, and publication visibility/durability; a candidate not produced by that route marks the subrecord `NotApplicable`;
- and unresolved claims.

The apply-admission subrecord is receipt evidence, not an input to `TransformRoot`, and it neither grants authority nor replaces the later independent `AssuranceAdmissionReceipt`.

The receipt does not self-award an independently checked release headline. A later `AssuranceAdmissionReceipt` binds the exact candidate receipt/root, admitted checker protocols and versions, independent outcomes and their oracle lineage, publication policy, final claim envelope, and host publication result. It appends evidence without mutating or replacing the candidate receipt. Failure to obtain the admission receipt leaves the candidate private or available only under a deliberately weaker profile.

#### `AssuranceAdmissionReceipt`

Records:

- exact candidate root and `TransformReceipt` identity;
- requested and admitted release-claim profiles;
- checker protocol identities, versions, budgets, and capability manifests;
- independent outcomes, coverage, unavailable evidence, and oracle-lineage correlation;
- policy waivers or refusals;
- host publication transaction and its visibility/durability state;
- signer authentication/trust results where signatures are used; and
- the final no-claim boundary.

#### `EvaluationProtocolCommitment`

Records the immutable pre-unblinding protocol for a comparison, foundry trial, ablation, or held-out evaluation:

- `EvaluationProtocolId`, canonical protocol schema/version, and content root;
- claim, reference class, artifact boundary, comparator/discovery rules, denominator/sampling frame, holdout-access budget, metrics, uncertainty, multiplicity, missingness, adjudication, stopping, and reveal policy;
- exact source/corpus manifests or blinded steward commitments;
- commitment time, independent custodian/timestamp/witness evidence, reveal time, and authorized amendments;
- evaluator and oracle lineage, conflicts, and confidentiality/rights constraints; and
- superseded protocol IDs and the fresh-data requirement triggered by any material change.

A reconstructed or privately mutable document is not predeclaration. Material amendments never overwrite the committed protocol.

#### `CompetitorDiscoveryProtocolCommitment`

Records the immutable **pre-search** field-discovery protocol:

- `CompetitorDiscoveryProtocolId`, field/capability definitions, eligibility law, jurisdictions/languages, registries, package indexes, repositories, benchmark/suite sources, search terms, scout roles, nomination/challenge procedure, cutoff rule, and exact planned exclusions;
- protocol commitment time, independent custodian/timestamp/witness evidence, reveal policy, rights/privacy constraints, and amendment law; and
- the maximum field-coverage claim that the search design could support if executed faithfully.

The protocol is committed before the discovery search begins. Search terms, surfaces, languages, scouts, or eligibility cannot be reconstructed after promising competitors appear. Material amendment creates a new protocol ID and restarts the affected discovery window.

#### `CompetitorDiscoveryReport`

Records:

- `CompetitorDiscoveryReportId`, canonical report schema/content root, the bound pre-search `CompetitorDiscoveryProtocolId`, proof of faithful execution, actual queries/surfaces/languages/dates, deviations, and cutoff;
- independent freeze/commit time, custodian/timestamp/witness evidence, challenge-window closure, reveal law, and any superseding report ID;
- independent scout/reviewer identities, nomination and public challenge windows, discovered candidates, deduplication, inclusion/exclusion rationale, exact released artifacts/configuration families, and unresolved eligibility;
- documentation, executable, and black-box coverage separately; absence of a documented feature is never proof of absence;
- discovery limitations, inaccessible/opaque systems, stale records, and field-coverage status; and
- the maximum claim scope the discovery evidence permits.

The report is immutable after its independently witnessed freeze. A late candidate or corrected eligibility finding creates a superseding report and lapses current-facing claims as required; it never edits the comparator set in place.

#### `SupremacyComparisonReport`

Records:

- atomic lane/subclaim identity, exact versioned `FieldDefinitionId` (capability/output contract, language/runtime/implementation restrictions, openness/license/channel, platform/jurisdiction, and other eligibility boundaries), and claim scope (`named_set_lead`, `registered_open_field_lead`, or `observed_field_lead`);
- bound `CompetitorDiscoveryProtocolId`, `CompetitorDiscoveryReportId`, and `EvaluationProtocolId`, with commitment/reveal dates and proof that discovery preceded comparator freeze and measurement followed the frozen evaluation protocol;
- lifecycle (`proposed`, `active`, `lapsed`, or `withdrawn`), field status (`contested`, `uncontested`, or `not_assessed`), field-coverage status, and outcome (`leading`, `equivalent`, `non_inferior`, `trailing`, `incomparable`, `indeterminate`, or `disqualified`) as separate fields;
- competitor eligibility, discovered/considered challengers, exact inclusion/exclusion rationale, independent nomination/challenge record, and release cutoff;
- competitor release, distribution channel, artifact digest/authority identity, strongest documented eligible configuration, dependency graph, symmetric tuning budget and consumed tuning, integration triage, maintainer/vendor challenge disposition where practical, observation date, and mutable-service limitations;
- MonkeyBee build/artifact identity and complete aligned profile;
- canonical corpus manifest, source snapshot, inclusion/exclusion, deduplication, sampling frame, partition, rights posture, frozen denominator, and adaptive-access history;
- primary analysis unit, pairing/clusters, weighting, missingness, effect/precision or power target, uncertainty, multiplicity, stopping/peeking, and adjudication;
- stochastic/provider routes, attempt budget, repeated-run protocol, selection/best-of-N rule, and drift window;
- metric family, equivalence/non-inferiority margins, dominance/utility rule, and any `incomparable` tradeoff;
- complete per-stratum supported, partial, refused, unsupported, timeout, resource, indeterminate, and disqualified accounting;
- oracle lineage, benchmark-owner conflicts, shared-corpus risk, held-out/Goodhart guard, refresh/expiry, superseding report, withdrawal reason, and exact no-claim boundary.

Only a leading `named_set_lead`, `registered_open_field_lead`, or `observed_field_lead` may support the internal supremacy headline. A `named_set_lead` remains useful comparative evidence but is not renamed field supremacy.

#### `ExecutionReplayBundle`

Records:

- triggering crash, refusal, divergence, or selected operational anomaly;
- exact proper-domain input identities—`SourceRootId`, `RevisionGraphId`, `DocumentViewId`, `DraftIntentCommitment`, `RealityStateCommitment`, and `ExpectedStateId` as applicable—plus artifact availability classes;
- semantic report identity separately from host run observations;
- determinism class and the exact replay relation that class and capture mode permit;
- comparator, tolerance/error metric, expected equivalence class, and acceptance scope;
- semantic limits, fired limit, seed where applicable, and used capability identities;
- build, dependency, profile, algorithm, target, and device identities;
- trace/capture level and known observer effects on timing, memory, scheduling, and caches;
- sensitivity, retention, redaction, and export authorization;
- completeness of crash capture;
- and any missing secret, remote, host, or external-tool state that makes replay partial or refused.

A replay bundle is never emitted through ambient networking. Export is a caller-authorized host action outside the semantic core. D3, D4, D5, wall-clock-stopped, partially captured, or mutable-external-service runs receive only the relation their evidence supports; none acquires a fictional bit-identical replay promise.

D1R replay reproduces the admitted semantic plan and non-secret receipt but never asserts output-byte identity; secure encryption, randomized or hedged signing, trusted-time/timestamp/revocation inputs, mutable signer services, and other protected or variable inputs retain their §11.9 limits.

#### `DivergenceReport`

Records:

- an unordered processor-result set keyed by exact processor identity, each record binding that processor to its exact executable/service artifact, version, configuration, environment, and independently identified output `ArtifactId`;
- exact `SourceRootId`, `RevisionGraphId`, `DocumentViewId`, relevant `DerivationId`, external input artifact identities, the exact set of bound output artifact identities, and profiles;
- differing observable regions;
- minimized causal object/program subgraph;
- normative analysis;
- compatibility classification;
- and a reproducible witness bundle.

Processor-to-output meaning comes only from the same processor-result record, never from shared array position. If a serialization also emits a `processor_output_artifact_ids` summary, that field is an exact generated set projection of the independently identified outputs in the processor-result records; a missing, duplicate, extra, or conflicting binding is invalid. Canonical ordering is solely an encoding concern and confers no processor priority, baseline role, winner, or majority semantics.

#### `EvidencePackage`

Records a content-addressed bundle of claims, outcomes, reports, artifacts, exact reality/root/graph/view/state/derivation identities as applicable, tool versions, checker protocols, and coverage/no-claim boundaries. Package production is an assurance-layer operation over typed opaque lower-layer artifacts; no reader, renderer, writer, editor, or transform crate depends upward on package construction. The hostile-input standalone checker is separately reviewable and does not reuse the producer's parser/canonical-root implementation.

The package identity is not “hash whatever the producer happened to serialize.” It is defined by a versioned protocol containing:

- a named hash algorithm and semantic version;
- a domain separator for every root and leaf class;
- length-framed scalar and byte-string fields;
- canonical numeric and string encodings;
- deterministic ordering by typed stable identity rather than map insertion or memory order;
- explicit handling of duplicate, unknown-critical, and optional-extension fields;
- an artifact-availability commitment distinct from the artifact’s content commitment; and
- a canonical root-construction grammar implemented independently by producer and checker.

A package parser may ingest noncanonical hostile bytes, but an integrity claim is always over the protocol-defined canonical semantic package and must disclose whether the supplied serialization itself was canonical. Semantically duplicate identities, conflicting artifact records, non-minimal critical encodings, or ambiguous extension interpretation refuse the strong integrity claim.

Package signing is optional and separately authenticated. A purpose-bound signature envelope binds at least the exact package root, root protocol/version, intended checker protocol, claim or release context, signer role, and any freshness/clock policy. It is an **evidence-envelope signature**, not creation of a PDF document signature and not evidence that any enclosed PDF signature is valid. Cryptographic signature verification, certificate/path trust, role authorization, policy admission, and package integrity are separate outcomes. Detached signature bytes never authorize themselves or upgrade a package merely by existing.

### 10.6.1 Evidence-checker isolation binding

The C0 proposed isolation binding has five explicit axes:

1. **Code isolation.** A separately authored checker accepts raw hostile package bytes, owns its parser, structural walk, canonical root construction, availability/materialization logic, and coverage accounting, and never accepts a producer-parsed package as trusted input. It may share only frozen wire/schema constants and identity class IDs, audited cryptographic primitives behind separate call boundaries, and independently authored conformance vectors whose provenance is recorded. It does not share the producer's package parser, semantic tree builder, canonical encoder, root-construction implementation, acceptance shortcuts, or test oracle.
2. **Authorship isolation.** The checker is authored by a different, recorded model family from the producer. Both exact authoring routes and their verification basis enter the production ledger.
3. **Specification isolation.** The checker author's task-local allowed-source manifest contains only the normative package protocol, ratified canonical-encoding grammar, applicable approved SpecCards, and independently authored hostile vectors. Producer source, rationale, and producer-authored fixtures are excluded.
4. **Measured detection.** At every cycle close, an independently administered seeded-defect trial records per-class attempts, detections, misses, unavailable cases, and checker configuration. Seed classes include wrong identity, ambiguous encoding, coverage overstatement, forged availability, stale dependency manifest, transplanted receipt, identity equivocation, and root/binding mismatch. A miss is a Grade-A finding; architecture alone cannot substitute for this observation.
5. **Lineage and review.** Model/authorship/source lineage and known correlation are report data, not an independence badge. A red-team hostile-package corpus and human adversarial review of canonical-root and coverage paths are required by the Q3 checkpoint; if unavailable, the independence claim degrades explicitly.

Producer and checker implementations must agree on independently generated positive and hostile vectors before a package-integrity claim is admitted. This binding is `PROPOSED — awaiting human ratification`; until ratified, implemented, and measured, checker independence is unavailable rather than inferred.

### 10.7 Explanation queries

The public explanation API supports questions such as:

- `explain_pixel(page, x, y, profile)`;
- `explain_glyph(glyph_instance)`;
- `explain_unicode(text_node)`;
- `explain_object(object_version)`;
- `explain_visibility(primitive)`;
- `explain_signature(signature_id)`;
- `explain_change(transform_id, output_location)`;
- and `explain_divergence(divergence_id)`.

An explanation is a graph of typed causes, not generated prose. Prose is an optional rendering. For compressed, encrypted, predicted, or executed inputs, the graph distinguishes exact virtual-span lineage from any stronger transform-specific inverse-attribution claim; an enclosing source-stream span is not mislabeled as the unique source bytes responsible for one output pixel or glyph.

### 10.8 Semantic report identity versus run observation

A report has two linked but differently versioned parts:

- a **semantic report body** containing outcomes, coverage, profiles, exact proper-domain root/graph/view/state/derivation identities, deterministic diagnostics, capability identities, and claim evidence; and
- a **run observation envelope** containing wall-clock timings, scheduler events, memory high-water marks, host timestamps, machine load, and other operational measurements.

Every report family instantiates one closed value-level semantic-body grammar. That body contains its `SemanticReportProtocolId`; exact report-family schema identity and version; every mandatory family field; exact proper-domain identities; processing, render, and security profile versions as applicable; capability identities; canonical outcome, coverage, deterministic diagnostics, evidence, and no-claim fields; and explicitly typed optional extensions admitted by that protocol version. `SemanticReportId` is the §9.2 content commitment over exactly that body. Unknown critical fields, ambiguous aliases, or missing mandatory fields refuse identity; absence and an explicitly present empty value are distinct where the family schema distinguishes them.

Every retained run observation instantiates a separately versioned envelope grammar containing its `RunObservationProtocolId`; observation-schema identity and version; exactly one `semantic_report_id` backlink; observation/capture coverage; operational measurements; and disclosure, truncation, and no-claim facts applicable to those measurements. `RunObservationId` is the §9.2 content commitment over exactly that envelope. The link is intentionally one-way: a semantic body never contains a `RunObservationId`, so one semantic report may have zero or many independently identified observations without changing semantic identity or forming a commitment cycle.

The two protocol identities and their concrete encoding/hash parameters remain governed by §§9.2-9.2.1. These paragraphs close the typed value and linkage domains but do not select an octet grammar, hash family, or digest width; no production `SemanticReportId` or `RunObservationId` is available until D1/D2 ratification. A material semantic-body or observation-envelope grammar change creates the corresponding new protocol version without silently changing the other.

Only the semantic body participates in D0 structural identity unless a measurement claim explicitly makes selected observations part of a separate measurement artifact. Bet 27 replay bundles bind this semantic body and retain the run observation envelope as evidence, but they reproduce only the guarantee of the declared determinism class: D0/D1/D2 identity where admitted; D1R semantic-plan and non-secret-receipt reproduction without output-byte identity; D3 bounds; D4 seed replay; and no stronger claim for D5. The semantic commitment binds its report-family schema version, identity grammar, processing/render/security profile versions, capability identities, and canonical encoding once ratified. Wall time, timestamps, process IDs, randomized temporary names, and nondeterministic event order never silently poison semantic report identities. Evidence packages can retain both parts and bind each observation to its semantic body through the typed IDs above.

### 10.9 Provenance retention policy

Small receipts and hashes are retained by default.

Large intermediates may be evicted according to a documented cache policy, but an evidence package must state when an explanation would require recomputation.

Every referenced source or derived artifact has an explicit availability class:

- `Embedded` — the exact bytes needed by the checker are inside the package;
- `ExternallyRetrievable` — a named immutable authority, capability, access policy, and expected identity are required;
- `Recomputable` — the package carries the admitted inputs, algorithm/profile identities, and bounded procedure needed to rebuild it;
- `IdentityOnly` — the package can authenticate an identity but cannot independently materialize the bytes; or
- `Unavailable` — the evidence is known to be missing.

`ByteExact` establishes the relation between an admitted immutable source and a range; it does not by itself make those bytes independently available to a later checker. A checker that lacks a decision-critical artifact returns partial coverage or refusal rather than treating an identity digest as a replay. Security-critical transformation packages pin or embed every artifact needed for the advertised independent check; otherwise the stronger headline is unavailable.

### 10.10 Capability consequence contracts

Crate contracts, `SpecCard`s, API signatures, release matrices, benchmark rows, and prose claims can all be locally correct while describing subtly different products. MonkeyBee therefore gives every atomic public operation, profile-qualified capability, and atomic supremacy subclaim one machine-readable `ConsequenceContractId`. Composite workflows, flagships, release envelopes, and public narratives reference typed compositions of those atomic contracts rather than hiding several outcome/authority laws inside one giant contract.

A capability consequence contract binds at least:

- operation/capability identity, lifecycle, owner layer, and exact input identity domain (`SourceRootId`, `RevisionGraphId`, `DocumentViewId`, `DraftIntentCommitment`, `RealityStateCommitment`, or another declared domain);
- request schema, `SemanticScopeId`, applicable `ExpectedStateId` grammar, preconditions, authority/capability lease, secret/privacy/disclosure class, and external/runtime substrate;
- budgets, cancellation/checkpoint law, transactional effects/publication class, idempotency/retry semantics, and state-change/signature consequences;
- claim outcome algebra (`Complete`, `Partial`, `Ambiguous`, `Refused`), operation-terminal `Cancelled`/`Indeterminate` and publication states where applicable, domain-specific canonical statuses, diagnostics, evidence facets, provenance/availability obligations, determinism class, and replay relation;
- required independent falsifiers, oracle-lineage constraints, performance/benchmark profile, release-claim row, expiry/withdrawal law, and no-claim boundary; and
- every surface that exposes it—Rust, CLI, C ABI, WASM, service/agent protocol, reports, packages, documentation, and capability discovery.

The contract is a semantic spine, not another implementation layer or work ledger. Existing source cards, crate contracts, profile records, report schemas, Gauntlet obligations, risk controls, and release rows are referenced or generated from it rather than copied into a new ontology. A surface may narrow a contract, but may not widen authority, coverage, determinism, evidence, or success language. Two surfaces that use the same friendly capability name but require different semantics receive different IDs. Material change creates a new version and migration/claim-impact record; a prose edit cannot silently redefine the machine contract.

Repository checks derive the public capability manifest, Appendix-E rows, API/documentation assertions, and assurance obligations from these contracts and reject orphan claims, missing falsifiers, inconsistent identity domains, or a surface whose failure semantics differ from the canonical outcome algebra. This is a primary post-agent compression mechanism: one resolved judgment propagates through specification, implementation boundaries, verification, operation, and public claims instead of being independently regenerated by many agents.

The claim registry is a versioned generated projection, not an independently authored claim source. Each atomic row binds exactly one `ClaimId` to exactly one `ConsequenceContractId`, its exact exposed surfaces, lifecycle and withdrawal/expiry state, admitted outcome/evidence/coverage, and no-claim boundary. A composite claim record references typed child `ClaimId`s and composition law without assigning one atomic claim to several contracts or strengthening any child. `ClaimRegistryId` commits the generated snapshot and its contract inputs; a missing, stale, orphaned, or contradictory link invalidates the affected registry row and release projection.

Report-family schemas together with the common §10.8 semantic-body/run-observation contract are the sole field sources for representative examples. An example generator consumes both inputs and emits explicit placeholders for every mandatory family field, `SemanticReportProtocolId`, `SemanticReportId`, capability-identity set, canonical outcome, coverage, deterministic diagnostics, evidence, no-claim boundaries, separately versioned run-observation schema and `RunObservationProtocolId`, `RunObservationId`, semantic-report backlink, observation coverage/telemetry, and telemetry-exclusion fact. While §9.2.1 remains pending, generated examples use explicit pending-ratification protocol markers and nonproduction identity placeholders rather than selecting an encoding.

A schema-example validator rejects any example that omits a required family, common identity field, canonical outcome, coverage, deterministic diagnostics, evidence, or no-claim boundary; uses a friendly alias where the schema requires a typed ID; breaks the one-way semantic-report backlink; includes run telemetry in semantic identity; or introduces a field that would strengthen the report's claim. For `DivergenceReport`, it additionally requires each processor-result record's separate artifact, version, configuration, environment, and output identities and verifies that `processor_output_artifact_ids` is the exact order-independent projection of those bindings. Appendix B is a non-normative `generated-echo` of §§10.6, 10.8, and 10.10 and is never hand-authoritative.

---


## 11. Work contexts, budgets, cancellation, and safety

### 11.1 Every operation is budgeted

Every potentially expensive operation receives a `WorkContext`.

```rust
pub struct WorkContext<'a> {
    pub cancel: &'a CancellationToken,
    pub limits: &'a Limits,
    pub account: &'a ResourceAccount,
    pub diagnostics: &'a DiagnosticCollector,
    pub profile_snapshot: ProfileSnapshotId,
    pub capabilities: CapabilityLease<'a>,
    pub secrets: &'a SecretHandlingPolicy,
    pub run_identity: RunIdentity,
}

/// Private fields; intentionally neither `Copy` nor freely constructible.
pub struct CapabilityLease<'a> {
    authority: &'a OperationCapabilitySet,
    grant: CapabilityGrant,
}

impl<'a> CapabilityLease<'a> {
    pub fn narrow<'b>(&'b self, request: CapabilityRequest)
        -> Result<CapabilityLease<'b>, CapabilityError>;
}
```

Every project-controlled potentially large allocation, loop, recursion, decode expansion, emitted artifact, and externally delegated unit of work is admitted and charged through this context. Small language/runtime bookkeeping may still allocate through Rust or dependencies; those no-claim boundaries are bounded by input admission, dependency contracts, and process isolation rather than described as magically impossible.

Budgets are hierarchical and non-resettable. A nested form, pattern, image, object stream, font program, validator rule, recovery branch, or parallel worker receives a child lease over the parent `ResourceAccount`: it may add a stricter local cap, but it cannot create a fresh global allowance. Global cumulative counters and per-item counters are both enforced, sibling work reserves before launch, cancellation returns unused reservations, and account overflow/refund races are conformance-tested. Recursion, retry, worker replacement, and parallel fan-out therefore cannot multiply a caller’s decoded-byte, instruction, output, diagnostic, or memory budget.

A child context that intersects parent and local limits must retain the computed intersection for the child's full lifetime. It may own that `Limits` value or borrow caller-provided storage that outlives the child context; it may not return a reference to a temporary or merely comment that two borrowed limits were intersected. Limit checks read the retained intersection and continue charging the shared non-resettable account.

A `WorkContext` belongs to an operation, not to `DocumentReality`. It binds an opaque `ProfileSnapshotId`, a least-authority non-`Copy` `CapabilityLease`, and a secret/PII handling policy. Lease fields are private and can be minted only by top-level admission from a host registry. A child context either borrows the same lease or receives a provable subset through `CapabilityLease::narrow`; no public constructor, clone, deserializer, retry, worker replacement, or child operation can add authority. A top-level host registry may know about fonts, trust stores, clocks, entropy, external sources, network adapters, or isolation workers, but it mints only the exact typed handles needed by the admitted operation. A byte decoder therefore cannot discover a trust store, a renderer cannot obtain entropy, and a validator cannot fetch a URL merely because the host supports those capabilities elsewhere.

The L8 profile compiler resolves a caller-facing `ProcessingProfile` into immutable layer-local views (`OpenPolicy`, `RecoveryPolicy`, `SecurityPolicy`, `PageExecutionRequest`, `RenderProfile`, `WritePolicy`, and `ValidationProfile`). Each operation receives only the view it needs; no lower layer imports the composed registry or pattern-matches on unrelated high-level policy. Diagnostics and observability sinks must reject or redact source bytes, passwords, keys, certificate data, embedded-file contents, and user text unless the caller deliberately enables a protected trace class.

Every cache, spool, temporary sink, crash artifact, and evidence package carries a data-sensitivity class. Decrypted streams, extracted attachments, private corpus material, and rendered/text outputs are not persisted merely because they are content-addressable. The policy controls in-memory retention, encrypted-at-rest temporary storage, swap/core-dump exposure assumptions, explicit zeroization attempts, and publication. Rust can minimize secret lifetimes and overwrite buffers, but MonkeyBee does not promise perfect erasure against compiler, allocator, OS, crash-dump, or hardware copies; high-assurance hosts require process/OS isolation and documented platform controls.

Content hashes are identifiers, not encryption. Publishing an unsalted digest of a confidential or low-entropy document, password-derived value, attachment, or extracted string can reveal membership through guessing. Public packages and telemetry therefore apply a disclosure policy: omit the commitment, use an access-controlled keyed commitment, or publish it only when the underlying artifact is already authorized for disclosure. Internal content addressing and public provenance are separate decisions.

External recognizers, competitor processors, transparency logs, and replay export are explicit host capabilities, never ambient powers of a parser, renderer, form tenant, or document. Each invocation binds a disclosed input scope, exact request artifact, exact response/result artifact and availability class, endpoint/tool/model observation, egress and retention policy, time/CPU/output quotas, and a sensitivity-classified transactional result. A stable endpoint label is not a promise of stable behavior; deterministic recomputability must be separately demonstrated. An HTTP-shaped protocol does not imply that network access is enabled by default.

### 11.2 Limit dimensions

The default limits object includes at least:

| Limit | Protects against |
|---|---|
| Source bytes | Unexpectedly large inputs or remote fetches. |
| Objects and object versions | Huge object graphs and xref attacks. |
| Reference depth | Cycles and pathological indirection. |
| Container nesting | Deep arrays, dictionaries, functions, and structure trees. |
| Total decoded bytes | Compression bombs. |
| Per-stream decoded bytes | One malicious stream. |
| Decode expansion ratio | Tiny compressed input expanding catastrophically. |
| Image pixels and planes | Raster allocation bombs. |
| Tile cache bytes | Unbounded rendering memory. |
| Page operators | Pathological content streams. |
| Graphics-state depth | Unbounded `q`/`Q` nesting. |
| Form and pattern recursion | Recursive resource cycles. |
| Type 3 glyph recursion | Recursive char procedures. |
| Function instructions | Type 4 calculator-function loops. |
| CMap tokens, mappings, `usecmap` depth, and aggregate entries | CMap interpreter expansion, inherited-chain cycles, and oversized mapping programs. |
| Form-script events, instructions, heap, and field writes | AcroForm JavaScript recursion, event storms, mutation loops, and memory growth. |
| Hostile XML/XMP bytes, depth, nodes, attributes, names/text, namespace declarations, comments/instructions, and parse output | XML expansion and parser-combinatoric attacks independently of any projection step. |
| Static-XFA nodes, layout boxes, and projection output | XML/layout combinatorics and oversized fixed-page projection. |
| External recognizer/tool calls and result bytes | Runaway external work, output floods, or repeated model invocation. |
| Font instructions | TrueType and charstring execution. |
| Path segments | Geometric denial of service. |
| Clip complexity | Exploding clip representations. |
| Transparency depth | Nested group explosions. |
| Recovery hypotheses | Combinatorial repair search. |
| Canonicalization and symmetry work | Adversarial graph refinement, partition branching, canonical-label search, quotient construction, and multiplicity expansion. |
| Wall time | Operational latency control. |
| CPU quanta | Fair scheduling and cancellation. |
| Output bytes | Writer and decompression safety. |
| Diagnostics | Adversarial error floods. |

Limits are versioned and included in receipts.

### 11.2.1 Semantic work limits versus wall-clock limits

Deterministic replay is governed by semantic counters—bytes, objects, instructions, pixels, path segments, hypotheses, and explicitly scheduled work units—not by elapsed wall time. A wall-clock deadline is an operational cancellation source whose firing depends on host load; an outcome stopped by that deadline cannot claim the same D0/D2 identity as one that completed under semantic limits. Receipts record which limit fired and whether replay requires the same semantic budget or only the same operational deadline.

### 11.2.2 Shared work and cache accounting

A physical decode, font load, or render artifact is charged once to the operation that produced it; logical consumers receive attribution without multiplying the physical counter. Cache hits still charge bounded lookup/materialization/output work and cannot reset global allowances. Concurrent consumers reserve against worst-case private work before launch, while shared immutable artifacts have one owner and explicit retention charge. This prevents both double charging and “free” amplification through a shared cache.

### 11.2.3 Attacker-keyed collections and canonicalization work

Every map or set whose keys can be influenced by hostile document bytes, decoded content, package fields, external-tool output, or untrusted caller data uses either a DoS-resistant keyed hash with operation/process-secret seeding or an ordered structure with a documented comparison and memory bound. A performance-motivated hasher substitution requires an explicit consequence-contract note naming the input trust boundary, collision/flooding model, worst-case complexity, benchmark evidence, affected profiles, and rollback. A fast unkeyed hasher cannot be introduced by local optimization convention.

Canonical graph labeling and semantic-symmetry handling are charged before branching and at every refinement, comparison, quotient, and emitted member. General canonical labeling has graph-isomorphism-class worst cases; no linear or polynomial bound is assumed merely because ordinary documents are easy. Each protocol declares node, edge, refinement-round, partition-state, branch, canonical-comparison, symmetry-class, multiplicity, memory, and output limits. Budget exhaustion returns an explicit partial/refused noncanonical outcome or a weaker profile; it never falls back to allocation or traversal order while retaining a canonical identity claim.

### 11.3 Hard and soft limits

- **Hard limits** abort the operation before the invariant would be violated.
- **Soft limits** allow graceful degradation when the caller explicitly permits it.

Examples of graceful degradation:

- lower-resolution page preview;
- skip an untrusted high-cost optional-content branch;
- stop recovery and return remaining hypotheses;
- emit glyph positions without Unicode;
- render an image placeholder with a structured refusal;
- or return a partial validation report.

A degraded result is never labeled complete.

### 11.4 Fallible allocation

Large allocations must be explicitly reserved through budget-aware helpers.

The code may not rely on process abort as the ordinary response to allocation failure.

Where Rust or platform behavior prevents fully fallible allocation, the no-claim boundary is documented and allocations are bounded before construction.

### 11.5 Cancellation semantics

Cancellation is:

```text
request
 -> observe at a bounded checkpoint
 -> stop producing new work
 -> drain or discard private partial state
 -> finalize accounting and diagnostics
 -> return a typed cancellation result
```

No partially mutated `DocumentReality` is committed. Output visibility and durability are properties of the selected host sink, not magic the core can promise for every `Write` implementation.

The writer targets a `TransactionalOutput` capability with declared commit semantics. A filesystem helper normally receives an already admitted destination-directory capability rather than repeatedly resolving an untrusted path; creates its private file exclusively with no-follow/no-clobber behavior where the platform supports it; records ownership, permissions, and overwrite policy; keeps the temporary file on the destination filesystem; handles short writes and quota/disk-full failures; flushes; optionally requests data/directory durability; revalidates the destination identity at commit; and renames atomically only where the platform contract supports the exact operation. Symlink substitution, path-component replacement, cross-filesystem rename, pre-existing destination races, permission changes, and platforms lacking the necessary directory-handle primitives therefore produce a weaker receipt or refusal rather than a fictitious atomic commit. Other sinks may offer weaker `Buffered`, `AtomicVisibility`, or `DurableCommit` classes, which appear in the receipt. Cancellation or failure before commit invokes abort/cleanup; failure after a host has acknowledged commit is reported as a committed outcome, not rolled back by fiction.

### 11.6 Panic policy

- Malformed or hostile PDF input must not trigger a panic.
- Public library boundaries use `Result` or iterator-level diagnostic results.
- Internal invariant panics are allowed only for programmer errors that input validation made unreachable; fuzzing treats reachable panics as defects.
- C ABI and WASM boundaries catch unwinding where the platform and panic strategy permit it; production builds may use abort only with a documented host-isolation story.
- Unsafe code may never be used to turn a fallible parse into an assumed invariant.

### 11.7 Unsafe-code policy

The default workspace lint denies unsafe code.

An unsafe capsule requires:

- a narrowly scoped module;
- a safe public façade;
- `SAFETY.md` with invariants;
- size and purpose limits;
- targeted Miri or architecture tests where applicable;
- fuzz coverage;
- and registration in a machine-checked capsule registry.

Expected candidate capsules are limited to:

- SIMD intrinsics;
- carefully audited allocation or mapping primitives;
- and foreign ABI boundaries.

PDF semantics never justify unsafe code.

### 11.8 Embedded-program sandbox contract

PDF contains several programmable sublanguages. MonkeyBee uses one common **meta-contract**, not one falsely uniform capability set:

- no ambient host authority, I/O, network, filesystem, process, UI, clock, locale, randomness, or external-resource discovery;
- only explicit pure intrinsics and narrowly typed, tenant-specific capabilities admitted by the operation profile;
- capability leases that can be inherited or narrowed but never widened by code inside the document;
- bounded operand/call stacks, instructions, output, allocations, effects, recursion, cycles, and event fan-out;
- deterministic execution under the declared inputs and validated dependency/selection manifest;
- explicit numeric and error behavior; transactional effect journals where mutation is admitted; and
- traceable termination, cancellation, refusal, and rollback.

Type 4 functions, font hinting/charstrings, and Type 3 procedures normally receive no document mutation capability. CMap interpretation is a distinct bounded tenant: it uses the dedicated CMap frontend/interpreter, never the Type 4 VM or a general PostScript interpreter; `usecmap` resolution is snapshot-bound and cycle-safe; and predefined mappings enter only through an explicit rights-cleared, version-identified data-pack capability. Bet 16’s form-action tenant receives only a typed view of the explicitly selected field graph, supplied deterministic host facts, and event-specific write authority. Its deny-by-default manifest excludes dynamic code generation, `eval`, ambient application/document APIs, keystroke/UI/navigation/submission events, and any built-in not separately admitted. Reads, writes, event order, cycles, event storms, resource charges, and the entire effect journal commit atomically or not at all.

Static XFA projection is bounded XML/layout derivation with explicit asset/font capabilities, not script execution or an interactive runtime. PostScript XObject compatibility remains ignore/refuse policy, not an interpreter. General JavaScript and dynamic XFA remain inventory-only.

The sanitizer and every executable tenant consume one shared versioned executable-feature registry. A construct cannot be executable yet invisible to sanitization, and a sanitizer cannot claim removal of a behavior class outside its enumerated interpreter surface.

### 11.9 Determinism classes

| Class | Promise |
|---|---|
| `D0 Structural` | Identical proper-domain parent identity, algorithm versions, profiles, semantic limits, and validated actual dependency/selection manifest produce identical structural/report identities. |
| `D1 Serialized` | Canonical output is byte-identical under a declared mode and pinned dependencies; an admitted deterministic-signature profile qualifies only when its algorithm, encoding, key/signing inputs, signed attributes, time policy, and every external input are fixed and independently verified. |
| `D1R Entropy/external-input-bearing serialized` | The admitted semantic plan and non-secret receipt are reproducible, but byte identity is not promised for secure encryption, randomized/hedged signing, trusted-time/timestamp/revocation inputs, mutable signer services, or any other explicitly variable dependency. |
| `D2 Same-target pixels` | The same reality/view, page request, profiles, semantic limits, feature set, validated dependency/selection manifest, deterministic build identity, and target produce bit-identical raster output; an elapsed deadline that fired is not part of this class. |
| `D3 Cross-target bounded` | Different supported targets remain within a declared exact or metric envelope. |
| `D4 Statistical` | Project-controlled seeded randomness is replayable only under the pinned generator, dependency, scheduling, and host contract; the outcome distribution and complete attempt process are the claim. Mutable external stochastic services may support observation replay but not fictional seed determinism. |
| `D5 Fast` | Some scheduling or floating-point variation is permitted and recorded. |

Every public operation declares its class. Engine-level replay reproduces the promise of that class rather than using “bit-identical” as a universal adjective. A wall-clock deadline that fired, a mutable unversioned host capability, missing secrets, or a D5 fast path yields partial replay or refusal, not a promoted D0/D2 claim.

### 11.10 Vulnerability disclosure and security response

The project maintains one versioned security-response policy with the following mandatory records. Concrete contact channels and service targets remain `PENDING-HUMAN-ADOPTION`; this document does not create or operate an external intake channel.

1. **Intake.** Reports receive a confidential case ID, receipt time, reporter contact/consent constraints, affected artifacts and versions, reproduction material handling class, and conflict/embargo request. Restricted standards text, corpus data, credentials, or private documents follow their existing rights and sensitivity policy.
2. **Triage.** An authorized security owner records reproducibility, affected envelopes/profiles, exploit preconditions, confidentiality/integrity/availability impact, evidence and claim impact, suspected shared dependency, and the next decision deadline. Unknowns remain unknown; inability to reproduce does not become a false rejection.
3. **Containment and correction.** The case links mitigations, affected identity/schema versions, temporary feature or claim withdrawal, patch/release candidates, regression/fuzz/corpus artifacts where rights permit, dependency coordination, and migration or revocation needs. No private reporter artifact enters an ordinary corpus by default.
4. **Embargo and coordination.** Disclosure timing, vendor/dependency coordination, credit, and exception authority are recorded per case. An embargo may be shortened for active exploitation or user-protection needs only by the named human authority with a written rationale; agents do not promise or lift embargoes.
5. **Advisory schema.** A released advisory identifies the case/advisory ID, affected and unaffected versions/profiles, severity basis, impact, preconditions, mitigations, corrected artifacts and verification evidence, credit, disclosure timeline, known limitations, and machine-readable links to superseded advisories. Publication remains a human external action.
6. **Claim linkage.** A vulnerability that invalidates a safety, determinism, evidence, redaction, sanitization, signature, or field-comparison premise immediately moves the affected claim to `lapsed` or `withdrawn` under its owning law until correction and re-admission evidence exist. Historical receipts are not rewritten.
7. **Closure and learning.** Closure records root cause, detection gap, affected consequence contracts and SpecCards, regression coverage, response telemetry, residual risk, and why the claim state may resume. A closed case never implies that related classes were exhaustively eliminated.

---


## 30. Kernel boundary interface

The concrete workspace and crate atlas remain in the shell. The following stable subsection is the sole frozen crate-boundary law.

### 30.1.1 Crate-boundary budget

The provisional atlas is a semantic decomposition, not permission to create every crate on day one. Early implementation begins with a smaller set of workspace packages and internal modules. A module becomes a crate only when at least two of these are true:

- it has a stable public contract consumed by multiple packages;
- it needs independent feature/dependency isolation;
- it needs an independently testable unsafe/security boundary;
- it has a distinct release/version lifecycle;
- or splitting materially reduces agent collision/context size.

Track cross-crate lockstep changes, compile fan-out, duplicated types, and adapter boilerplate. Crates that change together repeatedly are merged. This prevents “one capability = one crate” from turning architecture into filesystem shrapnel.

Source-rights tooling, standards-card generation, corpus administration, and external-lab adapters live in tool/assurance packages, not in the shipped runtime merely because they govern it.


## 33. Post-agent alien-artifact evaluation protocol

The project’s ambition is not accepted as evidence. Artifact, foundry, and lineage alienness are different propositions. A project may support one without the others; the strongest composite target requires all three, but the pure artifact claim is never withheld merely because repeatable foundry or long-horizon lineage evidence is absent.

### 33.1 Freeze the claim context and begin the live production ledger

For each public claim, record date; planning/code revision; models, harnesses, tools, hardware, services, dependencies, and runtime support; human participants and roles; elapsed calendar; inference/compute; imported code/data; attempts, discarded branches, retries, and prior prototypes; and known unknowns.

For all work after this rule is adopted, the production ledger begins **before candidate generation and evaluation**, not after a successful artifact appears. Earlier work receives a bounded retrospective reconstruction labeled `retrospective`, with source confidence and known gaps; it may explain history but cannot by itself support a strong prospectively precommitted foundry claim. Entries are append-only or correction-linked and cryptographically committed under a versioned protocol with independently witnessed/timestamped checkpoints where practical. It records branch/attempt relationships, resource consumption, model/provider routing where known, human interventions, selection decisions, and artifact commitments without assuming raw private reasoning, secrets, restricted standards text, or private corpus bytes may be retained. Public exports use reviewed redaction/commitment policies.

Human attention includes architecture, prompting, source-card creation, corpus curation, benchmark/scorer design, evaluation administration, debugging, review, selection, repair, legal/security adjudication, and release decisions—not only final code edits.

### 33.2 Define the reference class, date, and baseline vintages

Claims state whether they are relative to an ordinary public-agent user, expert public-agent operator, strong publicly documented foundry, conventional expert team, or an incompletely observable private frontier. The default serious target is public-frontier alienness under a sharply bounded envelope.

Every current-facing production claim uses both:

- a **historical baseline** frozen near the project/claim program’s start, preserving what frontier displacement meant then; and
- a **contemporaneous baseline** run near the public claim date using the strongest comparable currently available models/harnesses/practices under the same resource envelope.

A result may remain historically alien while lapsing as a current frontier claim. Unversionable provider behavior, unavailable old systems, or material baseline asymmetry becomes explicit uncertainty, not silent credit.

### 33.3 Define the artifact and operational boundary

Classify original runtime code, generic dependencies, construction-time agents/processors, runtime host adapters/models/services, development-only validators, corpora, human procedures, and external infrastructure. The boundary is the minimum operational closure needed to reproduce and sustain the claimed behavior. A runtime model/service remains part of the substrate and is not claimed as self-contained MonkeyBee capability.

### 33.4 Tamper-evidently precommit claim families

Before unblinding or final measurement, create and independently time-commit an `EvaluationProtocolId` covering:

- artifact/foundry/lineage claim and exact reference class;
- supported profiles, security envelope, metrics, determinism, performance workloads, flagships, failure conditions, and claim expiry;
- pre-search competitor-discovery commitment; committed discovery report/comparator set; claim scope, artifacts/cutoff, lane metrics/margins, denominator, refusal accounting, analysis unit, clusters, uncertainty, multiplicity, missingness, stopping, stochastic attempts, configuration/tuning fairness, and adjudication;
- baseline and ablation tasks, strongest ordinary replacements, model substitutions, resource/human-attention budgets, and evaluator lineage;
- held-out task/corpus commitments, submission/query and feedback budgets, reveal/replacement rules, and leakage boundaries; and
- task-novelty, latent-archetype, training-data/corpus exposure, and benchmark-owner conflict analyses.

The commitment is held by an independent steward, witnessed/timestamped append-only log, or equivalent mechanism before results. Reveal proves exact protocol bytes. A material change creates a new ID and requires fresh confirmatory data; the changed run is exploratory until then. Post hoc discoveries are hypotheses until replicated under a new committed protocol.
For field claims, the discovery commitment predates search, the discovery report predates comparator-specific measurement design, and the evaluation commitment predates measurement; one late omnibus document cannot retroactively satisfy all three boundaries.

### 33.5 Equal-resource baselines

Run at least:

#### Baseline A — Direct frontier agents

The same models, human attention, tools, compute, source pack, and task without MonkeyBee’s contracts, Honeycomb, persistent memory, or assurance architecture.

#### Baseline B — Strong conventional plan plus agents

A high-quality ordinary architecture and coordination process, without MonkeyBee’s claimed central representation/evidence mechanism.

#### Baseline C — Same repository without foundry memory

Replace tombstone/session retrieval with the strongest ordinary documentation/search alternative while retaining code/tests.

#### Baseline D — Same repository without independent oracles

Replace independent falsifiers with the strongest ordinary self-testing/review path; report the resulting assurance loss rather than simply breaking release admission.

#### Baseline E — Expert human comparison

Where feasible, bounded expert implementation, review, or defensible project-history evidence.

Historical and contemporaneous vintages are both retained where the frontier has moved materially.

### 33.5.1 Baseline fairness and normalization law

Every comparison freezes the same task statement, rights-cleared source pack, repository exposure, model/tool access, compute, elapsed feedback, human attention, attempt/branch budget, stopping rule, and held-out boundary except for the mechanism under study. Report nominal and consumed resources. No condition receives hidden retries, privileged debugging, extra evaluator feedback, or a weaker task.

The control receives the strongest practical ordinary alternative. Evaluators are blinded where feasible; rubrics and indeterminate/tie rules are frozen; replications estimate variance; and no condition author is sole judge. Unavoidable asymmetry receives sensitivity analysis.

### 33.5.2 Drift, novelty, and leakage law

A foundry advantage must survive scrutiny of:

- model/harness/provider changes between baseline and claim date;
- task similarity to common learned archetypes, public repositories, templates, prior MonkeyBee work, or benchmark examples;
- model training-data uncertainty and evaluator/corpus leakage;
- scaffold or repository information that encodes the answer; and
- whether the baseline had the same opportunity to learn from prior attempts.

The protocol may conclude “historically frontier-revealing,” “current frontier-revealing,” “maker-relative,” or “indeterminate”; it never averages these scopes.

### 33.6 Central ablations

Ablations are interventions, not demolition. Remove one claimed mechanism while supplying the strongest ordinary replacement that preserves task and usable interfaces. Predeclare migration effort, expected effects, interactions, and stopping. Use factorial/interaction-aware designs when mechanisms complement one another. Report null and negative results.

Baselines C/D are repository-level control conditions used to estimate end-to-end production or assurance difference under equal resources. The similarly named central ablations are mechanism-level interventions used to estimate causal contribution and interaction. One experimental run may inform both analyses descriptively, but it cannot count as both evidence classes in a claim bundle; each class requires its separately committed protocol, denominator, and analysis.

Ablate at least: Honeycomb identities/receipts; evidence facets; contracts/source cards; tombstones/memory; independent falsifiers; and structured multi-model plan refinement. Measure duplicate concepts, trace completeness, false upgrades, drift, review burden, recurrence, external failures, rework, and extension cost.

### 33.7 Model and harness substitution

Repeat selected tasks with different frontier model families, weaker capable models, mixed implementer/reviewer families, and at least one materially different harness/coordination style where available. Shared training, tools, benchmark exposure, and provider routing are recorded as correlation, not independent replication.

### 33.8 Distributional reporting

Report attempts, success rate, median/percentiles, best-of-N, retries/restarts, interventions, time/cost, defect distribution, and representative failures. The ledger includes discarded branches and evaluator-guided repairs. One spectacular branch proves reachability; reliability requires the distribution. Optional stopping, selective branch retention, or unreported provider routing invalidates a reliability claim.

### 33.9 Integration-surplus metrics

Measure cross-layer invariant violations, duplicate concepts, provenance completeness, automatic inheritance of budgets/diagnostics/evidence/fuzzing/schemas, change-propagation breadth, integration defects, and human review per merged consequence. No scalar defines coherence; metrics triangulate it.

### 33.10 Grounding-surplus metrics

Measure independent/analytic oracle coverage, held-out failure, external disagreement, security findings from independent attack paths, oracle-lineage diversity, and claim demotion after new evidence. A system that never demotes a claim is epistemically suspect.

### 33.11 Operational-surplus metrics

Measure clean installation, reproducible builds, hostile-input stability, quotas, migration, rollback, diagnostics, incident handling, support burden, and operator/user labor. Missing complexity shifted outside the declared boundary invalidates the operational claim.

### 33.12 Consequence-compression audit

For each central mechanism and major new capability, measure:

- **specification leverage** — new task-specific intent versus inherited archetype/scaffolding;
- **verification leverage** — how much assurance is inherited without a new parallel evaluator;
- **integration leverage** — which semantics, authority, history, evidence, diagnostics, migration, recovery, and rollback arrive automatically;
- marginal primitive/ontology/evidence/authority/operational-law count; and
- outcome quality/cost against the strongest ordinary composition.

A feature that adds more independent machinery than integrated consequence is accumulation, not alien compression.

### 33.13 Maturity taxonomy

Report separately:

- **Structural maturity** — known invariants/failure classes covered by design, proof, testing, fuzzing, simulation, and independent checks.
- **Empirical maturity** — lessons demonstrated through real operation over a declared duration, user/workload exposure, incident population, and environment.
- **Adaptive maturity** — successful recognition and safe assimilation of genuinely novel failures, requirements, adversaries, and dependency/environment changes.

Synthetic history can strengthen structural maturity and bounded adaptive rehearsal; it cannot be relabeled as years of empirical operation. A lineage claim states actual elapsed evolution and exposure or explicitly calls itself a synthetic evolution trial.

### 33.14 Evolution-surplus test

After release-candidate freeze, independent evaluators select held-out extensions under a query/feedback budget. Measure planning/implementation effort, touched concepts, regressions, duplication, schema migration, compatibility, new evidence/corpus artifacts, rollback, and preserved identity. Repeat across several extensions and, for a strong lineage claim, across real elapsed releases/incidents.

### 33.15 Separate claim ladders

| Object | Rung | Permitted statement |
|---|---|---|
| Artifact | `A0` | “An ambitious agent-built Rust PDF project.” |
| Artifact | `A1` | “A substantively integrated PDF artifact with documented provenance and scoped evidence.” |
| Artifact | `A2` | “A frontier-revealing artifact relative to the declared date/reference class.” |
| Artifact | `Artifact-alien candidate` | Independent reviewers judge the functioning artifact a provenance-conditioned extreme outlier in integrated consequence. Repeatable foundry or lineage evidence is not logically required. |
| Foundry | `F1` | “A production system that beats fair equal-resource baselines on selected held-out tasks.” |
| Foundry | `F2` | “A repeatable advantage across tasks, runs, contemporaneous baselines, and model/harness substitutions.” |
| Foundry | `Foundry-alien candidate` | Independent reviewers judge the production law itself a robust extreme outlier. |
| Lineage | `L1` | “A lineage that absorbs held-out extensions with low measured semantic decay.” |
| Lineage | `L2` | “The advantage persists across real releases, novel incidents, migrations, and environment change.” |
| Lineage | `Lineage-alien candidate` | Independent reviewers judge the evolution law itself a robust extreme outlier. |
| Composite | `Composite alien-system candidate` | Artifact, foundry, and lineage candidates all hold under compatible boundaries and dates. This is the strongest project target, not the definition of each component. |

The repository self-awards none of the candidate labels.

### 33.16 Public evaluation bundle

Publish where lawful and safe: reviewed ledger export and commitment chain; protocol commitments/reveals; plan/revision history; model/tool/harness manifests and drift; total search; baseline/ablation protocols and distributions; held-out definitions after evaluation plus access budgets; evaluator/oracle lineage; task-novelty/leakage analysis; capability/claim matrix; maturity classification; independent reviews; and known unknowns.

### 33.17 Evaluation kill criterion

If the foundry fails fair contemporaneous baselines, MonkeyBee can remain an excellent or even artifact-alien candidate; the production-law claim simply failed. If empirical/lineage evidence is immature, label structural maturity and synthetic evolution honestly. Failure of one object never erases evidence for another, and evidence cannot be borrowed across them.

### 33.18 Alienness synthesis and non-implication law

The final judgment keeps three objects separate:

1. **Artifact substance and disproportion** — functioning integrated consequence, assurance, operational closure, exact boundary, and provenance-conditioned comparison with what that production envelope was expected to produce.
2. **Foundry disproportion** — live ledger, total search, historical/contemporaneous equal-resource baselines, ablations, substitutions, human attention, and distributions.
3. **Lineage disproportion** — real or explicitly synthetic evolution, maturity class, incident metabolism, migrations, identity/invariant preservation, and semantic decay.

Product supremacy cannot substitute for causal disproportion. A foundry win cannot substitute for a functioning artifact. A clean release cannot establish empirical lineage. Conversely, the canonical pure definition permits artifact alienness without a repeatable foundry or mature lineage. The project’s strongest composite aspiration is all three.

The optimization target is maximal **independently demonstrated integrated consequence and consequence compression per fully credited production process**, without weakening safety, legality, truthfulness, or operational closure. Extreme engineering effort is admissible; evidence substitution and feature-count theater are not.


## 34. Plan refinement and freeze protocol

This revision-seven (v0.7) document is intentionally not implementation-ready. Revision seven preserves revision five as the addendum-integration history and revision six as the first full-document post-merge audit; it remains a whole-system markdown plan until architecture, product meaning, claim science, and unresolved decisions have converged.

Plan validation tooling is itself phase-scoped. It checks Markdown structure, internal references, schema/code-block consistency, forbidden execution-packaging vocabulary, release/claim contradictions, and stale section identifiers. It must not require work inventories, dependency edges, execution statistics, or any other artifact from a later representation. A validator that expects removed execution metadata is stale and is replaced rather than appeased.

### 34.1 Independent competing plans

Commission multiple fresh whole-system plans from independent contexts or model families using the same rights-cleared source pack. At minimum, obtain distinct treatments optimized for:

- hostile-input security and recovery;
- rendering fidelity and performance;
- authoring, transformation, and long-term evolution;
- and assurance, interoperability, and operational closure.

Each plan must be self-contained. It must design the project rather than merely critique this document.

### 34.2 Comparative synthesis

A separate synthesis pass receives all competing plans and must:

- identify common load-bearing decisions;
- surface genuine disagreements;
- compare user workflows and failure models;
- choose one architecture with explicit rationale;
- retain minority alternatives where uncertainty remains;
- reject mutually incompatible ideas rather than concatenating them;
- and produce one coherent revised markdown plan.

Revision five applied the **integration mechanics** of this rule to one competitive-claim and ambition addendum: adopted material was placed at its semantic owner, addendum-local labels were retired, conflicts remained open, and execution decomposition was rejected. That merge did **not** satisfy the full comparative-synthesis gate, which still requires several independent whole-system plans as §34.1 specifies. Revision six corrects any wording that could have implied otherwise.

### 34.3 Fresh-context review rounds

Run repeated reviews in fresh contexts. Recommended lenses are:

1. **Self-containment and workflow coverage** — can a new reader understand every promised workflow, degraded mode, and refusal?
2. **Architecture correctness** — are primitives sufficient, layers coherent, ownership unambiguous, and information loss explicit?
3. **Hostile adversarial review** — malformed inputs, security, clean-room boundaries, standards ambiguity, false assurance, and denial-of-service behavior.
4. **Rendering and font review** — geometry, color, transparency, text, CMaps, hinting, accessibility linkage, and compatibility behavior.
5. **Authoring and transformation review** — preservation, canonicalization, incremental updates, redaction, sanitization, evidence, and transactional publication.
6. **Product and operational closure** — APIs, bindings, packaging, diagnostics, migration, rollback, support burden, and user-visible capability discovery.
7. **Post-agent anti-self-deception** — baselines, ablations, provenance, independent evidence, and total-search accounting.

Rounds continue until findings are marginal rather than structural.

### 34.4 Validation after every review

Every revised plan is checked for the categories below.

At every transition among the §0.3 planning gates, the §24.13 competitor register is re-observed before any supremacy claim or lane category is carried forward. Release/main vintages, observation dates, and lapsed claims are recorded; a stale register blocks the claim, not the entire plan gate.

#### Self-containment

- no unexplained load-bearing terms;
- every promised user workflow;
- explicit failure and refusal behavior;
- explicit stack and dependency choices where they are already justified;
- and no hidden “implementation will decide the semantics” gaps.

#### Architectural coherence

- no circular semantic ownership;
- no public promise without a clear owning layer;
- no lower layer importing higher policy merely for convenience;
- no representation conversion whose information loss is unspecified;
- and no release envelope accidentally dependent on a capability it excludes.

#### Justification

- major decisions explain why;
- alternatives and tradeoffs are named;
- frontier bets have kill criteria;
- no-claim boundaries are explicit;
- and numerical or performance claims are sourced or framed as future measurements.

#### Steady state

- review findings are mostly local;
- no new central representation appears late;
- no major user workflow lacks a coherent story;
- terminology and public claim language remain stable;
- and the provisional crate atlas no longer churns structurally.

### 34.5 Decision ledger

Every structural review decision is recorded with:

- question;
- selected answer;
- alternatives;
- rationale;
- evidence;
- affected plan sections;
- reversal trigger;
- and date/reviewer.

The ledger prevents settled architectural questions from reopening without new evidence while still allowing explicit reversal.

### 34.5.1 Revision-five merge ledger

The following entries record the addendum’s nine unresolved decisions without selecting an answer. “Open” is a deliberate disposition: the rationale states why comparative synthesis did not silently decide the issue.

| Question | Disposition and alternatives | Rationale for remaining open | Affected sections | Reversal or decision trigger | Date/reviewer |
|---|---|---|---|---|---|
| 1 — Which lane defines the initial public supremacy claim envelope: S1 or S2? | **Open.** S1 offers faster public legibility; S2 tests the deeper wild-tail moat. | This is a claim-boundary decision, not execution ordering. It depends on corpus rights, steward independence, denominator quality, and which lane can support a defensible predeclared claim without distorting product scope. | §§24.15.1–24.15.2, 31.8, 35 | Comparative-synthesis evidence on corpus and claim-method viability. | 2026-07-13 / revision-five merge; wording corrected in revision six |
| 2 — Enter the existing extraction benchmark only, or co-publish a provenance-scored variant? | **Open.** Existing board versus Observatory extension. | The former gives comparability; the latter better measures MonkeyBee’s differentiator but risks becoming a self-authored evaluator. | §§24.15.3, 28.11, 31.9, 35 | Benchmark-governance and oracle-lineage review. | 2026-07-13 / revision-five merge |
| 3 — How deep is static XFA projection? | **Open.** Select a bounded layout subset and explicit no-claim boundary. | The input language and layout combinatorics are too broad to word honestly without a bounded probe and rights-reviewed corpus. | §§3.5–3.6, 7 Bet 16, 21.7.1, 31.7, 35 | Quarantined XFA capability probe and corpus review. | 2026-07-13 / revision-five merge |
| 4 — Which transparency-log substrate serves Bet 23? | **Open.** Self-hosted append-only log versus existing public ecosystem. | Trust, key separation, availability, monitor/gossip/witness topology, split-view resistance, privacy, irreversible membership disclosure, revocation, and artifact-boundary consequences differ materially. | §§7 Bet 23, 10, 16, 33.3, 35 | Threat model and verifier-user requirements. | 2026-07-13 / revision-five merge; threat model deepened in revision six |
| 5 — Which invariants enter the first proof kernel? | **Open.** Lexer span/termination, filter bounds, and recovery admission are candidates. | Proof value must be weighed against trusted-base size, model-to-code correspondence, and maintenance cost. | §§7 Bet 24, 10.2–10.3, 35 | Formal-method review and bounded proof prototype. | 2026-07-13 / revision-five merge |
| 6 — Admit a Ruffle-class SWF adapter or keep sanitize-only permanently? | **Open.** Permitted non-core adapter versus permanent refusal. | The adapter adds dependency and artifact-boundary cost to a behavior modern reference viewers no longer execute. | §§3.5–3.6, 30, 33.3, 35 | Concrete user demand plus dependency/security review. | 2026-07-13 / revision-five merge |
| 7 — Does the GPU lane remain outside every declared envelope? | **Open, default outside.** | CPU-equivalence certification is unproven and cannot become a hidden prerequisite for common rendering. | §§7 Bet 25, 26, 35 | Bounded equivalence probe with stable certificate semantics. | 2026-07-13 / revision-five merge |
| 8 — Does S4 include PDF/A-1 by adding a PDF 1.4 writer profile? | **Open.** Scope to PDF/A-2+/PDF/UA-1 versus widen §3.2. | S4’s parity target conflicts with the current writer-version envelope; matching a competitor is not sufficient reason to widen product scope. | §§3.2, 24.15.4, Appendix E, 35 | Product demand, standards/profile review, and writer cost evidence. | 2026-07-13 / revision-five merge |
| 9 — Adopt S6 performance superiority for selected workloads? | **Open, current §26.3 retained.** | Superiority may distort safety/evidence architecture; only a predeclared, profile-aligned, correctness-gated subset could justify escalation. | §§24.15.6, 26.2–26.3, Appendix E, 35 | Benchmark-lab evidence showing no contract erosion. | 2026-07-13 / revision-five merge |

### 34.5.2 Directed interaction findings from §§10, 11, and 16

The merge review found six interactions not fully expressed by the addendum and incorporated them into their owning sections:

1. Bet 24 required a first-class `MechanizedProof` evidence facet and non-laundering rules; otherwise the plan could not represent the proof it proposed.
2. Bet 27’s phrase “replays bit-identically under the declared determinism class” overreached D3, D4, D5, and wall-clock-stopped runs, while “ships home” conflicted with least-authority networking and sensitive-data policy. Replay now reproduces only the class guarantee and exports only through an explicit capability.
3. Bet 16 required script/XFA-specific budgets, pinned locale/time/clock inputs, no ambient entropy or host authority, and one shared executable-feature registry so sanitization can cover what execution admits.
4. Bet 20’s HTTP-shaped recognizer contract required explicit egress/privacy capability, transactional result bounds, and evidence composition that keeps tool output heuristic.
5. Bet 23’s transparency log required a rule that log inclusion proves only the log relation, plus explicit separation from PDF signature creation, key-management services, signer authorization, and computational verification. Revision six additionally corrected the revision-five key-role error: release keys authenticate builds, not arbitrary operation receipts.
6. Supremacy lanes required a typed comparison report with expiry, refusal accounting, profile alignment, and oracle lineage; revision six extends it with competitor eligibility, artifact pinning, denominator freeze, uncertainty, adjudication, and orthogonal lifecycle/outcome.

### 34.5.3 Revision-six full-document fresh-eyes ledger

Revision six records the following adopted corrections. None resolves open decisions 1–9.

| Question/finding | Adopted correction and rationale | Affected sections | Reversal trigger | Date/reviewer |
|---|---|---|---|---|
| Did revision five satisfy comparative synthesis? | **No.** It applied integration mechanics to one input; the §34.2 gate still requires several independent whole-system plans. | §§0.2, 34.2 | Execution of the actual §34.1–34.2 protocol. | 2026-07-13 / revision-six fresh eyes |
| Could the “strongest competitor” be selected after results? | **No.** Eligibility, challengers, cutoff, artifact identity, configuration, and challenge process are predeclared. | §§10.3, 24.12, 24.16, 32, Appendix E | A stronger anti-selection protocol with equal or better auditability. | 2026-07-13 / revision-six fresh eyes |
| Was “full pdf.js/PDFBox suites” a defensible denominator? | **Not as written.** A canonical rights-cleared manifest, deduplication, fixture classification, exclusions, and frozen denominator are required; engine-specific expected images are not neutral truth. | §§24.15.1, 31.8, 32 | Independently stewarded upstream manifest proving the same conditions automatically. | 2026-07-13 / revision-six fresh eyes |
| Did a signed/logged receipt verify its computation? | **No.** It authenticates a scoped assertion/log relation. Release, operation, attestation, and log keys are separate; replay/checking can establish only its declared recomputation/equivalence relation, while correctness remains separately evidenced. | §§7 Bet 23, 10.3, 16, 32, 35 | A stronger attestation system whose trust, relation, and correctness semantics are explicitly proved. | 2026-07-13 / revision-six fresh eyes |
| Did static XFA remain future-only? | **Contradiction corrected.** Bet 16 admits bounded static projection while general XFA runtime and conversion remain future work. | §§7 Bet 16, 21.9, 30, 31.7 | Open decision 3 or evidence changes the admitted subset. | 2026-07-13 / revision-six fresh eyes |
| Could form JS publish one computed value while partially mutating others? | **No.** The admitted subset runs as an atomic field-state transaction with event/dependency trace and rollback/no-publication on failure. | §§7 Bet 16, 21.7.1, 31.7 | A formally stronger state model with equivalent atomicity. | 2026-07-13 / revision-six fresh eyes |
| Was the agent surface safe merely because it had ordinary API authority? | **No.** Data/control separation, prompt-injection resistance, stale-anchor checks, tenant isolation, idempotency, and confused-deputy prevention are now explicit. | §§7 Bet 22, 25.9, 30, 32 | A replacement protocol proving equivalent or stronger authority semantics. | 2026-07-13 / revision-six fresh eyes |
| Were Tier-4 systems uniformly GPU/model-dependent and nonlocal? | **No.** The register now distinguishes local/deterministic modes and sharpens the gap to byte/revision provenance, evidence, and refusal. | §§24.13.4, 24.15.3 | New reproduced observations. | 2026-07-13 / revision-six fresh eyes |
| Was accessibility remediation uncontested? | **No.** OpenDataLoader-class auto-tagging is now an explicit comparator; MonkeyBee’s claim is evidence-bearing remediation and refusal, not tag generation alone. | §§7 Bet 19, 24.13.4, 31.10 | Competitor refresh or reproduced comparison. | 2026-07-13 / revision-six fresh eyes |
| Was an MCP/agent server itself a differentiator? | **No.** Existing Rust competitors advertise MCP and editing; MonkeyBee’s differentiator is the anchor/authority/validation/receipt conjunction. | §§7 Bet 22, 24.13.3, 25.9 | New evidence that transport semantics themselves create a unique capability. | 2026-07-13 / revision-six fresh eyes |
| Could S4 or S6 average unlike axes into “superior”? | **No.** S4 is an intersection-plus-extension scorecard; S6 uses per-axis non-inferiority or Pareto relations. Open decisions 8 and 9 remain. | §§24.15.4, 24.15.6, 26.3, Appendix E | A predeclared utility function accepted by independent review. | 2026-07-13 / revision-six fresh eyes |
| Did product supremacy establish post-agent alienness? | **No.** It is artifact-substance/grounding evidence only; foundry and lineage claims retain separate baselines and tests. | §§24.12, 24.16, 33.16 | Never by inference; only the complete §33 protocol can advance the claim. | 2026-07-13 / revision-six fresh eyes |
| Could an edit-created object be explained when it had no source/draft parent? | **Not with the prior type.** `Derived` now binds a frozen transform intent and permits zero parents only for admitted authoring-class operations; true transformations still require parents. | §§9.1–9.2, 23, 30, 32 | A simpler origin algebra proving the same honesty and constructor constraints. | 2026-07-13 / revision-six fresh eyes |
| Could `TransformRootId` hash its own lineage/output IDs? | **No.** Root identity is constructed first from inputs/policy/local intents; lineage is a separately committed receipt over already-defined roots. | §§9.1–9.2, 10, 32 | A formally acyclic alternative identity grammar. | 2026-07-13 / revision-six fresh eyes |
| Could one root-global ID name different profile/hypothesis results? | **No.** Root-intrinsic IDs are separated from `DocumentViewId`/`DerivationId`; page/program/appearance/text identities include outcome-changing context. | §§9.2, 9.6, 25, 32 | A proven canonical cross-view identity relation with no aliasing. | 2026-07-13 / revision-six fresh eyes |
| Did equivalence or non-inferiority mean supremacy? | **No.** Those are intermediate typed outcomes; only an uncertainty-aware lead supports a supremacy headline. | §§10.3, 24.12, 24.15, 26.3, 31.8, 32, Appendix E | A future doctrine explicitly renaming the program away from supremacy. | 2026-07-13 / revision-six fresh eyes |
| Did form-action parsing have an owner and lexical boundary? | **Not explicitly.** The closed subset is now an internal `mb-form` parser/interpreter under the common sandbox; it is not general ECMAScript and creates no crate entitlement. | §§11.8, 12.2, 30.7 | Crate-boundary evidence justifies a separately contracted package. | 2026-07-13 / revision-six fresh eyes |
| Was hayro still the only mandatory S1 pure-Rust renderer? | **No.** `pdf_oxide` 0.3.74 advertises a material renderer and enters the mandatory challenger set; `oxidize-pdf` is refreshed to 4.0.1. Hard-coding the addendum’s original rival would invalidate a field claim. | §§24.13, 24.15.1, 24.15.6, 32, Appendix E | Reproduced capability evidence or a later eligible release changes the set. | 2026-07-13 / revision-six fresh eyes |
| Could a supremacy comparison force every multi-axis tradeoff into winner/loser? | **No.** `incomparable` is a first-class outcome when the predeclared relation yields mixed tradeoffs without a justified winner. | §§10.3, 24.12, 24.15, 26.12, Appendix E | An independently accepted utility relation resolves that exact tradeoff prospectively. | 2026-07-13 / revision-six fresh eyes |
| Could pages, pixels, or repeated runs be counted as independent documents? | **No.** Primary analysis unit, pairing/clusters, minimum effect/precision, stopping, multiplicity, missingness, and stochastic attempt selection are now mandatory comparison evidence. | §§10.3, 10.6, 24.12–24.16, 26.12, 27.1, 32 | A stronger domain-specific statistical protocol. | 2026-07-13 / revision-six fresh eyes |
| Did “open-field lead” mean best across every language/runtime, or against every closed or mutable system? | **No.** Every result binds an exact `FieldDefinitionId`; pure-Rust and all-open fields are separate, as are `registered_open_field_lead` and `observed_field_lead`. No global-best inference is permitted, and mutable unversioned SaaS remains only a scoped observation. | §§10.3, 24.12–24.16, Appendix E/F | A broader lawfully reproducible eligible field. | 2026-07-13 / revision-six fresh eyes |
| Could a DraftRoot bind incidental layout/shaping implementation versions? | **No.** Frozen intent binds semantic profiles/data and assets; concrete implementation/build belongs to `DerivationId` unless realized runs are supplied as intent. | §§9.1–9.2, 22, 32 | A proven intent model in which implementation identity is itself user meaning. | 2026-07-13 / revision-six fresh eyes |
| Did TransformRoot identity bind only a recipe? | **Insufficient.** It is minted after semantic finalization and includes a canonical result commitment while excluding its later root-scoped IDs and lineage receipt. | §§9.1–9.2, 23, 32 | A formally simpler result-bound acyclic grammar. | 2026-07-13 / revision-six fresh eyes |
| Could a derived origin embed the post-root transform operation ID? | **No.** That would feed a root-dependent `TransformId` back into the semantic state that determines the root. `OriginRecord::Derived` carries only pre-root `TransformIntentId` plus an authored/from-parent basis; operation IDs and lineage live in post-root receipts. | §§9.1–9.2, 22.0, 23.1, 32 | A formally specified fixed-point identity system with a compelling interoperability need; none is presently justified. | 2026-07-13 / revision-six fresh eyes |
| Was the semantic result commitment sufficiently defined? | **Only partly.** Revision six required a versioned order-independent result grammar and exposed symmetry, but still mixed semantic equality with origin history and overused refusal. Revision seven supersedes that portion with `SemanticStateId`, `RealityStateCommitment`, symmetry classes, and multiplicity. | §§9.1–9.2, 32, §34.5.4 | An independently checked canonicalization protocol with stronger guarantees. | 2026-07-13 / revision-six fresh eyes; superseded in part 2026-07-14 |
| Can a cache key contain only dependencies “actually used” before lazy execution discovers them? | **No.** Reuse is two-stage: a broad candidate index followed by exact validation of the stored actual-dependency manifest, or a proved deterministic preflight manifest. | §§9.2, 9.6, 11, 26.6, 32 | A static dependency analysis proven complete for the affected derivation class. | 2026-07-13 / revision-six fresh eyes |
| May S4 treat krilla—or the Rust ecosystem—as the entire open generation field? | **No.** Krilla remains the mandatory profile-focused anchor. Pure-Rust and all-open `FieldDefinitionId`s are separate, and every material eligible generator or non-dominated set enters the applicable atomic field before `registered_open_field_lead`. | §§24.12–24.16, 26.3, 32, Appendix E | A register refresh proving one comparator dominates every admitted S4 subclaim at cutoff. | 2026-07-13 / revision-six fresh eyes |
| Can an origin reference cross roots as an unqualified local ID? | **No.** Prior-root edges are root-qualified; candidate-local origin IDs are confined to finalization and mapped to rooted canonical nodes before publication. | §§9.1–9.2, 22.0, 23, 32 | A globally content-addressed origin-node protocol proving collision, cycle, and privacy properties without root qualification. | 2026-07-13 / revision-six fresh eyes |
| Can structured authoring serialize directly from an intent root after implementation-dependent layout? | **Not without losing result identity.** Explicit positioned drafts may serialize directly; derived layout/pagination/optimization first finalizes a result-bound `TransformRoot` with its derivation receipt. | §§9.1–9.2, 22.0–22.1, 32 | A DraftRoot grammar that makes every material layout choice explicit caller intent. | 2026-07-13 / revision-six fresh eyes |
| Are consumed resources alone sufficient for a lazy cache dependency manifest? | **No.** Selection-sensitive derivations also bind the resolver/authority snapshot, priority witness, or negative dependencies whose absence chose the result. | §§9.6, 11, 25.6, 26.6, 32 | A proved selection algorithm whose result depends only on the listed positive resources. | 2026-07-13 / revision-six fresh eyes |
| May S6 treat PDFium and MuPDF as the complete native performance field? | **No.** They are mandatory anchors; every material eligible native/open and pure-Rust renderer or the non-dominated set enters each atomic workload before a field-lead claim. | §§24.12–24.16, 26.3, 32, Appendix E | A register refresh and predeclared metrics proving those anchors dominate the eligible set. | 2026-07-13 / revision-six fresh eyes |
| Did page/bbox evidence or “trust report” remain an uncontested agent differentiator? | **No.** PDF Reader MCP 3.0.14 directly contests those surface claims; MonkeyBee’s target is exact byte/revision/derivation evidence plus authority-safe mutation and independent transformation checking. | §§7 Bet 22, 24.13.4, 24.15.3, 25.9 | Reproduced competitor comparison changes the exact boundary. | 2026-07-13 / revision-six fresh eyes |
| Could a transparency log prove one history without outside observation? | **No.** Strong profiles require signed checkpoints/tree heads plus monitor/gossip or independent witnesses; public membership disclosure may be irreversible. | §§7 Bet 23, 10.3, 16, 30, 32, 35 | A different anti-equivocation construction with equal auditability. | 2026-07-13 / revision-six fresh eyes |
| Could a foundry win be manufactured with a weak baseline or destructive ablation? | **No.** Baselines receive equal information/resources and the best ordinary alternative; ablations substitute rather than merely break, with blinded evaluation and interaction-aware analysis. | §§32, 33.5–33.6 | A stronger independent methodology review. | 2026-07-13 / revision-six fresh eyes |
| Could a heuristic semantic anchor authorize destructive mutation by default? | **No.** Anchors carry evidence/coverage/ambiguity, authorities are separated across propose/validate/approve/apply, and high-consequence edits require explicit policy-approved confirmation or refusal. | §§7 Bet 22, 25.9, 32 | A formally verified rebasing/approval model with equal safety. | 2026-07-13 / revision-six fresh eyes |


### 34.5.4 Revision-seven second full-document adversarial ledger

| Question | Selected answer | Rationale / affected sections | Reversal trigger | Date / reviewer |
|---|---|---|---|---|
| May semantic equality include provenance/origin history? | **No.** `SemanticStateId` is value/relationship equality under a declared scope; `RealityStateCommitment` adds roots, origins, and frozen intents. | Prevents semantically equal documents from becoming unequal solely because of history while blocking history-sensitive reuse through a value-only identity. §§9, 22, 23, 32. | A formally simpler single identity proving both safe semantic deduplication and non-aliasing of every history/authority claim. | 2026-07-14 / revision-seven fresh eyes |
| Must graph symmetry force finalization refusal? | **Only for a genuinely identity-sensitive unresolved distinction.** Ordinary symmetry uses ordered structures, multisets, multiplicity, and equivalence classes. | Repeated equal pages/resources are common; arbitrary ordering is not semantics. §§9, 22, 32. | An independently verified canonical-label protocol with lower complexity and equal no-arbitrary-choice guarantees. | 2026-07-14 / revision-seven fresh eyes |
| Can a search over two named renderers be called an open-field lead? | **No.** It is `named_set_lead`; registered field scope requires a versioned discovery protocol and challenge window. | Revision-seven search found printpdf, fop-pdf-renderer, and pdfsink-rs omissions. §§10, 24, 32, Appendix E/F. | A universal authoritative registry with complete capability metadata; none exists. | 2026-07-14 / revision-seven fresh eyes |
| Is prose marked “predeclared” sufficient? | **No.** The canonical protocol must be independently time-committed before unblinding; material amendment creates a new ID and fresh evaluation. | Prevents reconstructed thresholds, denominators, stopping, or comparator sets. §§10, 24, 28, 33, 32. | A stronger externally audited precommitment mechanism. | 2026-07-14 / revision-seven fresh eyes |
| Does the sandbox forbid every host call? | **It forbids ambient authority.** Tenant-specific typed pure capabilities may be admitted explicitly; mutations use an atomic effect journal. | Resolves contradiction with form-field access without opening ambient application APIs. §§7 Bet 16, 11.8, 16.8, 21.7.1, 31.7, 32. | A proof that an even smaller pure-state interface covers the admitted corpus. | 2026-07-14 / revision-seven fresh eyes |
| Can Form rendered pixels be cached by Form identity/resources alone? | **No.** Caller graphics state, placement, optional content, group/backdrop context, output profile, and selection dependencies must be in a proved manifest; otherwise cache only the program/intermediate. | Form appearance is context-dependent, especially non-isolated transparency. §§17.6, 26.6, 32. | A formally proved context-independent intermediate for a narrower profile. | 2026-07-14 / revision-seven fresh eyes |
| Can random AES-GCM nonce generation claim absolute uniqueness? | **No.** Only a coordinated durable per-key allocator may claim deterministic no-reuse in its domain; random-only profiles publish collision bounds and use caps. | Distributed clones/restarts make absolute unseen-history claims impossible. §§16.1.1, 32, 35. | A cryptographic profile with a different nonce-misuse-resistance contract and reviewed source cards. | 2026-07-14 / revision-seven fresh eyes |
| Is an idempotency key enough for safe agent retries? | **No.** It binds an exact request to a durable outcome; crash-ambiguous apply is `indeterminate`, queried rather than replayed, and batches are atomic. | Avoids duplicate destructive edits and fictitious exactly-once claims. §§5.16, 7 Bet 22, 23.1, 25.9, 32. | A stronger transactional transport/storage proof covering the whole boundary. | 2026-07-14 / revision-seven fresh eyes |
| Can a repeatedly queried hidden corpus remain held out? | **Not after adaptive feedback exceeds the frozen access policy.** It becomes development data and needs a fresh reserve. | Prevents leaderboard-style overfitting without byte disclosure. §§24.16, 28.3, 33.4, 32. | A privacy-preserving evaluation proof with equivalent anti-adaptation guarantees. | 2026-07-14 / revision-seven fresh eyes |
| Does a historical baseline support a current foundry claim indefinitely? | **No.** Current-facing claims need a contemporaneous baseline and drift report; the old result may remain historical. | Post-agent frontiers move rapidly. §§33.1–33.8, 32. | A stable reference class whose capability can be shown not to have changed. | 2026-07-14 / revision-seven fresh eyes |
| Must artifact alienness wait for foundry and lineage alienness? | **No.** They are separately evidenced objects; all three are required only for the strongest composite label. | Aligns the plan with the canonical post-agent definition’s non-implication law. §33. | A revised canonical definition adopted by the project. | 2026-07-14 / revision-seven fresh eyes |
| Can structural assurance be called empirical maturity? | **No.** Structural, empirical, and adaptive maturity remain separate. | Fuzzing/proofs/simulation do not manufacture elapsed operational history. §§33.13–33.18, 32. | Longitudinal evidence demonstrating the missing maturity class. | 2026-07-14 / revision-seven fresh eyes |
| Is feature breadth itself evidence of alienness? | **No.** New capabilities must show specification, verification, or integration compression over strong ordinary composition. | Agents make feature accumulation cheap; post-agent surplus lies in integrated consequence. P19, §§9.9, 33.12, 32. | Empirical evidence that a seemingly separate mechanism creates extraordinary net consequence. | 2026-07-14 / revision-seven fresh eyes |
| Does a SourceRoot have one semantic-state ID? | **No.** Semantic state belongs to each admitted `EffectiveDocumentView`; distinct revision/recovery views may differ or may share meaning while retaining distinct evidence. | Prevents one immutable byte history from collapsing all historical/recovery interpretations into a fictitious timeless meaning. §§9.1–9.2, 14, 25. | A formal source model proving one unique interpretation for the declared source class. | 2026-07-14 / revision-seven fresh eyes |
| Does `SourceRootId` include the discovered revision graph? | **No.** It identifies immutable bytes only; `RevisionGraphId` is a versioned derived artifact and `DocumentViewId` binds the selected graph/alternative. | Parser, recovery, limits, and available evidence can change without changing the bytes; old receipts must remain interpretable. §§9.1–9.2, 12.6, 14, 25, 32. | A proof that revision discovery is uniquely and permanently determined by source bytes for the admitted class. | 2026-07-14 / revision-seven fresh eyes |
| May a transform identify a document input by `RealityRoot` alone? | **No.** Result identity binds root plus exact `DocumentViewId`; the separate proposal/admission/receipt binds and revalidates `ExpectedStateId` and authority. | A root can admit several historical/recovery views; root-only inputs can alias different transformations, while missing admission state can authorize a stale edit. §§9.1–9.2, 10.6, 23.1, 32. | A proof that the input root has exactly one admissible immutable view for the transform class. | 2026-07-14 / revision-seven fresh eyes |
| Does a Draft root use the same commitment as a finalized Transform result? | **No.** Draft uses `DraftIntentCommitment`; Transform uses `RealityStateCommitment` after semantic finalization. | Intent and realized pagination/layout are different facts, and not every Draft has a complete semantic state. §§9.1–9.2, 22.0, 32, Appendix F/G. | A unified formal commitment that preserves this distinction without implying unrealized semantics. | 2026-07-14 / revision-seven fresh eyes |
| Is `SemanticScopeId` merely a human-readable profile name? | **No.** It is a canonical manifest of included meaning axes and every meaning-changing policy/data revision. | Prevents equality that silently ignores signatures, actions, structure, metadata, history, or layout realization. §§9.1–9.2, 32, Appendix F/G. | A smaller formal semantic kernel that proves omitted axes can never affect any consumer of the scope. | 2026-07-14 / revision-seven fresh eyes |
| Are all render-named Rust crates interchangeable S1/S6 comparators? | **No.** Eligibility is atomic and output-contract-specific: PDF→raster, PDF→SVG, extraction screenshots, and intermediate-layout rasterization are different paths. | Corrects printpdf/pdforg over-inclusion and prevents benchmark denominator manipulation while still requiring every candidate to receive a recorded disposition. §§24.13, 24.15, 26.3, 32, Appendix E. | A frozen standard adapter proving equivalent end-to-end semantics and charging every conversion/dependency. | 2026-07-14 / revision-seven fresh eyes |
| Must every future PDF signature be randomized and byte-variable? | **No.** Signing follows the scheme-specific deterministic, randomized, or hedged nonce law; D1 requires every signed input/time/service fact to be pinned and tested. | RFC 6979-style deterministic ECDSA and EdDSA invalidate the universal-randomness claim. §§11.9, 16.1.1, 22, 25.6, 26.9, 32, Appendix E. | A future standards profile that deliberately excludes every deterministic signature scheme. | 2026-07-14 / revision-seven fresh eyes |
| Can field discovery and measurement share one late precommitment? | **No.** Search protocol is committed before search; the resulting field report is frozen after challenge; measurement protocol is committed only afterward. | Prevents search-space cherry-picking and comparator-set retrofitting. §§10.6, 24.12–24.16, 33.4, 32. | A stronger independently audited continuous registry with equivalent prospective guarantees. | 2026-07-14 / revision-seven fresh eyes |
| May MonkeyBee win by choosing a weak competitor configuration? | **No.** Strongest documented eligible configuration, symmetric tuning/integration budget, independent operation, and challenge/triage are part of the protocol. | Prevents sabotage by defaults, missing assets, or unequal engineering help. §§10.6, 24.12, 24.16, 32. | A domain-standard immutable benchmark container accepted by all competitors. | 2026-07-14 / revision-seven fresh eyes |
| Must all moonshot probes be serialized? | **No.** Bounded quarantined probes may run in parallel; only one may block a release envelope or force project-wide architecture at once. | Post-agent leverage should parallelize search without parallelizing semantic debt. P18, §32.1. | Evidence that integration/assurance capacity can safely admit a broader blocking set. | 2026-07-14 / revision-seven fresh eyes |
| Can pre-existing production history satisfy a prospective ledger rule? | **Only as labeled retrospective evidence.** Strong foundry claims require later trials whose ledger and evaluation were committed before candidate generation. | Avoids laundering reconstructed history into precommitment. §§33.1, 33.4, 32. | Independently witnessed contemporaneous records covering the earlier period. | 2026-07-14 / revision-seven fresh eyes |
| Does operation admission belong inside `TransformRootId`? | **No.** The result root binds exact root/view inputs, frozen intent, origins, result semantics, and provenance policy; `ExpectedStateId`, caller authority, capability leases, idempotency, and publication generations remain in proposal/admission/receipt identity. | §§9.1–9.2, 10.6, 23.1, 25.9, 32, Appendix F/G | A future identity theorem showing a specific admission fact is intrinsic document provenance rather than transient operation state. | 2026-07-14 / revision-seven alien audit |
| How is one public capability kept semantically identical across every surface and claim? | **By one versioned capability consequence contract.** Rust/CLI/C/WASM/service surfaces may narrow it but cannot independently redefine identity, authority, outcomes, evidence, determinism, privacy, or no-claims. | Prevents polished local consistency from hiding cross-surface semantic drift and turns one judgment into specification/verification/integration leverage. §§10.10, 25.8, 27.4, 29.5, 32, Appendix E/G. | A smaller formally verified interface-description system proving equal propagation and drift detection. | 2026-07-14 / revision-seven fresh eyes |

### 34.6 Quarantined architectural probes

Small probes may be used before plan freeze only to retire architecture-critical uncertainty, such as:

- codec ecosystem viability;
- immutable remote-source snapshots;
- fallible output publication;
- ICC transform coverage;
- shaping and variable-font support;
- cryptographic profile support;
- or the performance cost of pervasive provenance.

A probe is disposable evidence, not production code. It lives outside the production dependency path and cannot silently become the implementation.

### 34.7 Plan freeze

A frozen planning revision contains:

- stable section identifiers;
- resolved decisions for the first public capability envelope;
- a coherent provisional crate atlas;
- source registry and clean-room rules;
- initial capability and no-claim matrix;
- explicit unresolved research bets;
- and reversal triggers for provisional choices.

Freeze means “stable source for a later execution transformation,” not “never change.”

### 34.8 Structural change after freeze

A structural change requires:

- a decision record;
- impact analysis across workflows, layers, contracts, public claims, and evidence;
- migration or invalidation policy;
- updated no-claim boundaries;
- and explicit refreeze.

The plan may evolve. It may not drift invisibly.



### 34.9 Addendum protocol

Every capability cycle after the kernel cycle proceeds as follows, and no cycle's delta plan may be authored before the previous cycle's close gate passes.

1. **Archaeology.** The delta plan opens with a repository-reality survey (code, tests, contracts, drift-audit output). Claims about existing structure cite the survey, never a prior plan's description.
2. **Kernel-touch declaration.** The delta plan declares `kernel-touch: none` or enumerates the touched kernel laws. Any touch requires: kernel version bump, migration plan for all affected identities/receipts, claim-lapse review, and Charter change-control entry.
3. **Contracts before beads.** Every new capability receives a consequence contract citing its SpecCardIds; falsifiers become bead acceptance criteria; the assigned Gauntlet tier is the definition of done.
4. **Delta-only conversion.** Beads are generated for the delta plan only. Full-plan reconversion is prohibited (feature-loss and drift vector). Polish to steady state; dependency graph acyclic.
5. **Execution.**
6. **Close gate (blocking):** (a) drift audit — generated-truth diffs, contract-truth checks, claim-registry consistency, zero Grade-A findings to pass; (b) one held-out extension probe, selected from the sealed pool, with results recorded win-or-lose; (c) SpecCard coverage check for the cycle's surface; (d) sealed cycle trial record into the production ledger: attempts, failures, retries, cost, human interventions, median and best outcomes.

Cycle trial records are the campaign's foundry-distribution evidence; a cycle without a sealed record contributes nothing to any §33 claim regardless of what it shipped.

For Constitution v8.0-proposed, “assigned Gauntlet tier” in item 3 is a versioned dependency on `shell/MONKEYBEE_SHELL_CORPUS_v8.md` §27. It binds the entire G0–G7 taxonomy, the G6.1 toolchain/unsafe/supply-chain/privacy lanes, every §27.1 falsifier family, and §27.4's consequence-contract-derived release matrix without copying those shell sections into the kernel. A later change to that taxonomy, its falsifier pairing, or its release-matrix validity law is a declared kernel touch under item 2; no provisional shell edit silently changes the definition of done.
