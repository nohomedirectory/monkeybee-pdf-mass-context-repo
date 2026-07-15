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
  - DISPUTES.md
  - reports/INGEST_REPORT.md
  - MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md
  - ledger/prompts/OWNER_MARCHING_ORDERS.md
  - constitution/MONKEYBEE_CONSTITUTION_v8.md
  - constitution/SPECCARD_PIPELINE.md
  - decisions/D1_CONTENT_HASH.md
  - decisions/D2_CANONICAL_SERIALIZATION.md
  - decisions/D3_DECODED_STREAM_IDENTITY.md
  - decisions/D4_EVIDENCE_CHECKER_ISOLATION.md
  - decisions/D5_PROJECT_LICENSE.md
  - decisions/D6_LEDGER_BACKEND.md
  - decisions/D7_RUST_TOOLCHAIN_PIN.md
  - decisions/DECISION_INDEX.md
  - decisions/DEFERRED_REGISTER.md
  - ledger/owners/G1_STATE.md
  - ledger/owners/G2_STATE.md
status: DRAFT
evidence-status: provisional-pending-substrate
owner: G3
owner-fsm: SUBMIT-FOR-REVIEW
kernel-touch: initial-kernel-adoption
---

# Cycle 1 Delta Plan — Kernel, Immune System, and R0 Revision Autopsy

## 0. How to use this plan

This document defines the Cycle 1 capability delta only. It is plan space: a semantic and evidentiary specification for later conversion with the human present. It is not an issue list, implementation schedule, agent assignment, source scaffold, or substitute for the real dependency graph.

The intended reader is a fresh implementation agent who has read `AGENTS.md` and the ratified Cycle 0 decisions. Every public or gate-bearing capability below has one stable consequence-contract ID. Contract links express semantic prerequisites and downstream consumers; they do not prescribe execution order.

Authority is inherited, not created here. Live human instructions and the Charter set control campaign scope. A proposed Constitution v8 extraction now exists and preserves the stable kernel section IDs, but its own extraction contract says it supersedes Rev 7 only after human ratification and commitment. This plan reconciles citations to that candidate while retaining Rev 7 as the controlling domain source until the required act occurs. It never upgrades generated prose, a proposed decision, a registry slot, or a passing self-check into canonical law.

### 0.1 Artifact state

- Repository reality at drafting start: documents only; no source tree, build system, test harness, Constitution v8, shell extraction, or G2 decision brief existed.
- Cross-owner reality at SELF-CHECK: the proposed Constitution and SpecCard pipeline are at G1 `SUBMIT-FOR-REVIEW`, and D1–D7 plus the deferred register are at G2 `SUBMIT-FOR-REVIEW`. The G1 kernel still awaits human ratification/commitment and every G2 default remains `PROPOSED — awaiting human ratification`; submission supplies reviewable evidence, not ratification.
- Cycle boundary: C1 owns L0–L2, the R0 inspection wedge, the immune system, the initial CLI, and the C1 evidence gate.
- Planned kernel interaction: C1 adopts the initial frozen identity, evidence, budget, capability, hashing, serialization, clean-room, layer, and evaluation laws once ratified. It does not amend them.
- Mutation boundary: no file other than this plan and `ledger/owners/G3_STATE.md` is changed by G3.
- Evidence state: all prose is `provisional-pending-substrate`; a git timestamp alone would not strengthen it.

### 0.2 Stop lines

Cycle 1 does not include rendering, page-program execution, rasterization, color, fonts, CMaps, text extraction, writer output, incremental writing, canonical rewriting, repair writeback, sanitization, redaction, cryptographic signature verification, trust validation, signature creation, public-key decryption, WASM, C ABI, service hosting, external publication, field comparison, benchmark measurement, or any later-cycle profile.

The reader may structurally inventory data that later layers interpret, but an inventory must not claim the later semantic result. In particular, a located signature dictionary or `ByteRange` is not a verified signature; an encryption dictionary is not proof that every payload is encrypted; a located action carrier is not proof of execution or harmlessness; a recovered object graph is not a conforming parse.

### 0.3 Required formal vocabulary

The only singular-value success outcome is the scoped `Complete` variant of the canonical claim algebra. Other outcomes are `Partial`, `Ambiguous`, and `Refused`; operation termination may additionally be `Cancelled` or `Indeterminate`. Publication state is separate. Ordinary prose in this plan avoids supremacy wording and never converts a narrower result into a broader claim.

## 1. Cycle 1 outcome and release boundary

Cycle 1 produces an invocable inspection wedge for hostile source bytes. Within admitted source coverage, credentials, budgets, and card coverage, the wedge can preserve an immutable source snapshot; expose exact lexical and structural evidence; discover xref, revision, object, object-stream, encryption, signature-range, and bounded recovery alternatives; decode the named lossless filter surface; read standard-handler encrypted values with caller-supplied credentials; and return structured reports with explicit partiality, ambiguity, refusal, and no-claim boundaries.

The wedge serves four user intents:

1. Strict inspection asks what the admitted bytes establish without recovery.
2. Revision autopsy asks what histories and object occurrences are structurally discoverable.
3. Bounded recovery asks which materially distinct interpretations survive explicit assumptions and limits.
4. Credentialed inspection asks what additional values become available under a narrowly scoped, non-exporting credential capability.

The wedge remains useful if every campaign-level independence dependency fails to materialize. Stewards, challenge windows, baselines, external adjudication, and field measurement may gate later claims; they do not gate ordinary R0 user value. The C1 campaign evidence gate still records honestly which evidence could not be sealed.

## 2. Authority map for implementation

| Subject | Governing source until superseded | C1 use |
|---|---|---|
| Clean-room and source rights | Proposed Constitution v8 §4; Rev 7 §4 remains controlling until ratification; AGENTS Rules 7–10 | Admission law for every context, card, fixture, dependency, and generated artifact. |
| Non-negotiable product laws | Proposed Constitution v8 §6; Rev 7 §6 remains controlling until ratification | Safety, evidence, budget, determinism, transaction, authority, and no-unsupported-success invariants. |
| Layer direction | Proposed Constitution v8 §§8–8.1 and §30.1.1; Rev 7 remains controlling until ratification | Dependency direction and crate-boundary budget; concrete crate names remain provisional. |
| Identity domains | Proposed Constitution v8 §§9.1–9.7, especially §9.2.1; Rev 7 remains controlling until ratification | Source, graph, view, derivation, virtual-span, and provenance identities; ratification gate for identity encoding. |
| Outcomes, evidence, diagnostics, reports | Proposed Constitution v8 §§10.1–10.10, especially §10.6.1; Rev 7 remains controlling until ratification | Contract algebra, generated report obligations, and proposed checker-isolation binding. |
| Work, authority, secrets, determinism | Proposed Constitution v8 §§11.1–11.9; Rev 7 remains controlling until ratification | WorkContext, limits, cancellation, panic, capability, privacy, and replay law. |
| Byte/revision/COS behavior | Rev 7 §§12–13 | L1/L2 source-level plan semantics, pending card review. |
| Recovery | Rev 7 §14 | Strict-first bounded hypotheses and material ambiguity. |
| Filters | Rev 7 §§15.1–15.3 | Declared-order lossless decode surface and transactional publication. |
| Encryption and signatures | Rev 7 §§16.1–16.5 | Inventory, credentialed read decryption, and structural signature discovery only. |
| Inert security-carrier inventory | Rev 7 §§13.5 and 16.8–16.10, with Work Order §2 R1-7 constraining the enumeration | Card-reviewed structural presence, opacity, encryption state, and later-layer handoff only; no effect/reachability graph or verdict, execution, sanitization, XML processing or safety verdict, or semantic threat claim. |
| CLI and capability discovery | Rev 7 §§25.1–25.3, 25.7–25.8 | Rust facade semantics projected into the C1 CLI. |
| Assurance | Rev 7 §§27–29 | Falsifier pairing, fuzzing, corpus discipline, contracts, and generated-truth law. |
| Cycle close | Charter §§5–6; Work Order §§3 and 7; proposed Constitution v8 §34.9 | Blocking drift/card/probe/trial-record gate. |

## 3. Clean-room, rights, and no-contamination boundary

### 3.1 Denied sources

No implementation or plan refinement may clone, fetch, read, quote, summarize, cite, or derive from source or documentation of a PDF processor, including the named denylist in Rev 7 §4.1 and any later discovered processor. The denylist is automatic by class; absence of a name is not permission. This prohibition includes permissively licensed implementations and transitive translations.

No raw standards text enters model prompts, retrieval, generated comments, fixtures, or implementation artifacts unless a ratified rights record explicitly permits that exact use. Availability, purchase, human reading, model visibility, quotation, implementation use, test execution, and redistribution are independent rights flags.

### 3.2 Admitted inputs

Implementation may consume only an approved, task-local source manifest. Candidate classes are rights-reviewed project-authored SpecCards, licensed machine-readable models, generic algorithm literature, project-generated fixtures, independently authored conformance material, and black-box observations only after their protocol and rights gates have been committed. No candidate class is self-admitting.

The plan may state PDF behavior only at the level already present in project canon. It does not create normative meaning. Every normative slot in this document is a registry reference marked `PENDING-LICENSED-SOURCE`.

### 3.3 Contamination response

If unapproved processor material or restricted standards text reaches an implementation context:

- stop the affected work;
- record the source, exposure boundary, artifacts, and uncertainty without copying restricted content;
- quarantine outputs so no production or test path consumes them;
- invalidate affected source attestations and evidence;
- restart in a fresh approved context from admitted inputs;
- require independent review before readmission; and
- preserve the incident and disposition in the campaign ledger.

Generated prose, passing tests, and model confidence cannot cleanse a contaminated lineage.

### 3.4 Card authority, slot staging, and runtime projection

Every consequence contract carries one or more project slot IDs. A slot contains only identity, ownership, expected review state, and linkage metadata. It contains no paraphrased semantic body during this plan-space run. Every slot is written as `PENDING-LICENSED-SOURCE`.

`PENDING-LICENSED-SOURCE` remains the uniform plan-space marker on every contract-local and actual registry slot throughout this document. It records the live no-body boundary, not a later linkage decision. Neither the pre-C1 resolution manifest nor a runtime projection changes that marker in this plan or makes a slot active.

The sequence is two-stage. Before any C1 implementation admission, the authorized human/source pipeline must produce an immutable `ReviewedCardAuthoritySnapshotId`/`CardAuthoritySnapshotId` after rights checks, project paraphrase, and two-person meaning review. C1 IMM.001 may then create a runtime coverage projection of that snapshot. The projection is not authority, cannot activate a pending slot, and cannot repair a missing upstream review.

Implementation admission consumes the pre-C1 authority snapshot and may additionally use IMM.001’s projection for runtime discovery. If a needed card is absent, disputed, unavailable, or lacks model-use rights, the capability remains unavailable or returns a narrower outcome. An agent must not fill the gap from memory. The preimplementation gate refuses candidate work unless the reviewed authority snapshot and the IMM.018 prospective-ledger bootstrap both predate it.

### 3.5 R0 registry reconciliation

G1's draft `constitution/SPECCARD_PIPELINE.md` now provides the actual empty R0 registry `MB-SC-R0-001` through `MB-SC-R0-043`. Every one remains `PENDING-LICENSED-SOURCE`; an ID proves only that a slot exists. The `SC.C1.*` names in individual contract blocks are contract-local coverage-link slots, not alternative SpecCards and not semantic authority. Before activation, each such link must resolve to the applicable `MB-SC-R0-*` entries or to an explicit reviewed project-law disposition that no external normative card is needed.

| C1 surface | Actual G1 R0 registry linkage | Current state |
|---|---|---|
| Header, dialect, lexer, raw COS, and stream bounds | `MB-SC-R0-001` through `MB-SC-R0-006`, plus `MB-SC-R0-013` where duplicate selection matters and `MB-SC-R0-041`/`MB-SC-R0-042` for the pending override/extension inventory labels | `PENDING-LICENSED-SOURCE` |
| Terminal markers, xref tables/streams, hybrid history, revisions, object streams, and linearization inventory | `MB-SC-R0-006` through `MB-SC-R0-012` | `PENDING-LICENSED-SOURCE` |
| Catalog, page/name/number structure, metadata, and `NeedsRendering` inventory | `MB-SC-R0-014`, `MB-SC-R0-015`, `MB-SC-R0-037`, `MB-SC-R0-040` | `PENDING-LICENSED-SOURCE` |
| Declared lossless filter pipeline | `MB-SC-R0-005`, `MB-SC-R0-016` through `MB-SC-R0-022` | `PENDING-LICENSED-SOURCE` |
| Standard-handler inventory and caller-credential read decryption | `MB-SC-R0-023` through `MB-SC-R0-031` | `PENDING-LICENSED-SOURCE` |
| ISO/TS encryption and integrity variant inventory only | `MB-SC-R0-043` | `PENDING-LICENSED-SOURCE` |
| Structural signature and `ByteRange` inspection | `MB-SC-R0-032` through `MB-SC-R0-034` | `PENDING-LICENSED-SOURCE` |
| Inert action, attachment, metadata, encrypted-wrapper, UTF-8-string, and rendering-need inventory | `MB-SC-R0-035` through `MB-SC-R0-040` as applicable | `PENDING-LICENSED-SOURCE` |
| Recovery | Every syntax or structure slot implicated by a hypothesis; recovery ordering itself remains project policy | `PENDING-LICENSED-SOURCE` |

This crosswalk is intentionally only a coverage relation. It does not assert sufficiency, quote a requirement, resolve an ambiguity, or populate a semantic body. Licensed extraction may split slots or add new empty IDs without allowing a local contract label to substitute for them.

Before implementation admission, the authorized pre-C1 human/source pipeline is the sole authoring owner of an immutable `CardLinkResolutionManifestId`. It binds the exact plan root, contract-registry root, `ReviewedCardAuthoritySnapshotId`/`CardAuthoritySnapshotId`, and all 157 `SC.C1.*` IDs. Each local ID has exactly one resolution record selecting either (a) one or more applicable `MB-SC-R0-*` entries proven active by the reviewed authority snapshot or (b) an explicit human-reviewed project-law disposition. A project-law record binds a stable project-law authority ID, authorized reviewer identities, a review record, and a rationale limited to why no external normative card is required; it contains no semantic body.

No agent inference, empty mapping, ambiguous branch, or default “no card needed” decision is admissible. Every applicable actual R0 card has at least one local consumer; an extraction-time split or added empty ID blocks admission until a successor manifest records its consumers. The manifest is linkage evidence only: it is not a second normative home, does not assert sufficiency, cannot activate any slot, and leaves every slot in this plan exactly `PENDING-LICENSED-SOURCE`. IMM.001 owns only its runtime projection, and IMM.009 owns only the bidirectional zero-orphan check.

## 4. Decision dependencies

The following G2 artifacts and expressly routed disputes appeared after the DRAFT transition. They are planning inputs only: D1–D7 and D-004 remain `PROPOSED — awaiting human ratification`. The plan may expose a proposed default so reviewers can see its consequences, but the corresponding capability remains unavailable until the human ratifies it. Every point of use repeats that status rather than relying on this preface alone.

| Dependency | C1 consumers | Proposed planning default and current handling | Ratification effect |
|---|---|---|---|
| `D1` — content-hash algorithm and digest widths | every stable identity, cache key, report root, package root, and external commitment | **PROPOSED default — awaiting ratification (D1/D2):** SHA-256 at the full 256 bits, packaged with D2; active contracts retain symbolic `HashProtocolId` and no external commitment may occur first | Ratified package fixes protocol v1 and migration rules; ratification must precede the first external or tamper-evident commitment. |
| `D2` — canonical serialization grammar | every identity, generated schema, package, checker, and ledger chain | **PROPOSED default — awaiting ratification (D1/D2):** deterministic-CBOR profile, typed domain separation, length framing, no floats, refuse ambiguity, and separately implemented producer/checker encoders | Ratified package becomes the sole v1 identity/commitment grammar; the alternative hash/framing package changes both D1 and D2 together. |
| `D3` — `DecodedContainerId` cost/availability | decoded containers, virtual spans, caches, reports | **PROPOSED default — awaiting ratification (D3):** pre-decode recipe `DecodedContainerId` plus post-commit `DecodedArtifactDigest`, verified on durable reuse; `DecodedStreamId` appears only as D-004's higher-layer alias drift | Ratification fixes four typed availability states and the metadata-versus-decode cost boundary; no second decoded identity class is minted. |
| `D-004` — decoded-identity name-drift routing | D3, FLT.010, decoded provenance/caches/reports, and plan-to-execution conversion | **PROPOSED authority resolution — awaiting human ratification (D-004):** apply DISPUTES.md D-004: `DecodedContainerId` is the sole domain-canon class and `DecodedStreamId` is retained only when identifying the campaign-layer wording drift | Ratification authorizes the campaign-layer correction and closes the alias-routing gate without minting or accepting a second decoded identity class. |
| `D4` — checker isolation | standalone checker and drift evidence | **PROPOSED default — awaiting ratification (D4):** separate code, different-model-family authorship, specification isolation, and seeded-defect trial observations from C1; human adversarial review by C4 | Ratification fixes permitted narrow sharing, prohibited shared semantics, lineage disclosure, and the seeded close-gate trial. |
| `D5` — project license | dependency admission, contribution posture, fixtures, and wedge distribution | **PROPOSED default — awaiting ratification (D5):** MIT OR Apache-2.0 plus a runtime-license rider; DCO versus CLA and all legal characterizations require human/counsel action | Ratification admits the distribution posture. D-005 still prevents this plan from treating the runtime dependency policy or any provider as selected. |
| `D6` — persistent ledger backend | production/trial records, drift records, and schema migrations | **PROPOSED default — awaiting ratification (D6):** hash-chained append-only JSONL per-writer shards as source of truth, with only a regenerable derived index | Ratification fixes durability, record schema, crash law, and migration adapter; the hash chain is not the independent commitment substrate. |
| `D7` — Rust toolchain pin | reproducibility, schema generation, fuzzing, Miri, and sanitizer lanes | **PROPOSED default — awaiting ratification (D7):** exact stable for runtime/release and date-pinned nightly for assurance findings only; exact versions remain human-filled. Rust 2024 edition, a committed lockfile, and deny-unsafe default are extracted kernel requirements rather than an invented pin | Ratification fixes build identities and supported checks; toolchain changes become determinism-impact events. |
| `D-005-RUNTIME-DEPS` — runtime dependency allowlist routing | generic compression and cryptographic primitive adapters; byte-source/service isolation adapters and any async runtime | selection remains symbolic and implementation-unavailable; the core stays synchronous and cancellation-aware, and async is adapter-only if later admitted | Human routing/ratification admits a policy and dependency set; no adapter may silently select an async runtime or pull it into the core. |
| `D-005-CRYPTO-CRATES` — cryptographic crate selection routing | password validation, RC4, AESV2, AESV3, hashing if shared | primitive providers remain symbolic and implementation-unavailable | Human routing/ratification admits exact providers, versions, provenance, and review obligations. |

No symbolic dependency may silently fall back to a library default. A later decision change creates a protocol migration and claim-impact review rather than reinterpretation of old artifacts.

### 4.1 Deferred-decision guards active in C1

| Deferred item | C1 guard |
|---|---|
| GPU/raster backend, owner C6 | No C1 API, trait, schema, or profile assumes a GPU path; rendering is outside C1. |
| PDF/A-1 writer profile, owner C6 | No C1 type assumes a PDF 1.4 writer profile; all writing is outside C1. |
| C-ABI freeze, post-R4 with C5 preview | No C1 public core type is shaped for FFI convenience and no compatibility promise is made. |
| Base-font fallback, owner C3 | No font is vendored and no silent substitution path is assumed; fonts are outside C1. |
| S6 performance metric, owner C7 | No optimization bypasses a safety, budget, evidence, or refusal contract; C1 performs no supremacy measurement. |
| MSRV, proposed owner C1-close | No MSRV is advertised before declaration; the exact stable/nightly pins remain distinct from an MSRV promise. |
| Async runtime, routed through D-005 | None in the synchronous core; a bounded isolated host adapter may use one only after exact dependency ratification, and scoped borrows never escape into it. |
| Bet 24 first proof-kernel scope, Rev 7 open decision 5 | Lexer span/termination, filter expansion bounds, and recovery admission remain ordinary tested C1 contracts. No proof obligation enters the C1 critical path; a later human decision must name the selected theorem, assumptions, correspondence evidence, and trusted base before a mechanized-proof claim exists. |

These guards are not decisions by omission. Each remains open until its stated trigger and ratification path are satisfied.

## 5. Consequence-contract grammar

Every contract block below is normative for this delta only after higher authority ratifies its dependencies. Each block supplies these fields:

- stable ID, lifecycle, owner layer, and capability identity;
- exact input identity domain and request shape;
- preconditions and card-slot state;
- semantic and operational budgets;
- cancellation checkpoints and terminal behavior;
- caller authority, capability lease, secret class, and disclosure class;
- output, coverage, outcome, and publication state;
- stable diagnostics and truncation behavior;
- evidence facets, origins, artifact availability, and report linkage;
- determinism class and admitted replay relation;
- independent falsifiers and Gauntlet tier;
- every exposed surface;
- dependencies and downstream consumers;
- expiry, migration, and withdrawal behavior; and
- a precise no-claim boundary.

Surfaces may narrow a contract but may not widen authority, coverage, outcome language, evidence, determinism, or disclosure. Friendly names that differ semantically receive different IDs.

Dependency clauses use a closed grammar. A prerequisite segment is introduced by the exact phrase “depends on,” optionally after an explicit scope label such as “strict mode,” and ends at the first semicolon. Every catalog-token expression in that segment creates graph edges. A single FAMILY.NNN token denotes one catalog ID; an inclusive FAMILY.NNN–FAMILY.NNN range expands in numeric order within one family; slash-separated tokens or ranges are a union. Every expansion is resolved against the closed §6 catalog and IMM.002 stores the exact sorted expanded prerequisite-edge list in the candidate root. Named non-contract decisions or inputs and descriptive qualifiers in the segment create no graph edge; bare family names or prose used in place of catalog IDs are invalid.

A `targets` segment after the prerequisite semicolon is a separately indexed assurance-coverage relation: its exact catalog tokens name contracts exercised by a target, never semantic prerequisites of that target or the exercised contract. Every FUZ.002–FUZ.010 target separately depends on FUZ.001 so rights, provenance, partition, and held-out admission precede use of any seed. Conditional alternate-mode `consumes` clauses are separately indexed state-transition relations with an explicit source phase, target phase, and guard; they do not enter the prerequisite DAG. IMM.002 stores both relation sets, and IMM.007 proves the prerequisite DAG acyclic while also proving that every conditional transition consumes an already minted artifact and strictly advances the declared phase. Downstream-consumer descriptions, workflow labels, and other prose after the semicolon create no edge unless they name exact contracts in one of those two admitted relations. This grammar is about semantic contract dependencies and coverage only; it does not create implementation tasks.

## 6. Contract catalog

The catalog below is the closed C1 contract namespace. Adding an atomic public capability requires a new ID and a coverage update; implementation helpers remain internal and do not become public contracts merely because they exist.

### 6.1 Foundation contracts

- `C1.CC.FDN.001@1` — typed digest and domain separation.
- `C1.CC.FDN.002@1` — canonical scalar and collection encoding.
- `C1.CC.FDN.003@1` — collision detection and quarantine.
- `C1.CC.FDN.004@1` — operation admission and `WorkContext`.
- `C1.CC.FDN.005@1` — hierarchical resource accounting and reservation.
- `C1.CC.FDN.006@1` — cancellation and terminal-state accounting.
- `C1.CC.FDN.007@1` — least-authority leases and profile snapshots.
- `C1.CC.FDN.008@1` — sensitivity, secret lifetime, and disclosure policy.
- `C1.CC.FDN.009@1` — bounded structured diagnostics.
- `C1.CC.FDN.010@1` — claim outcomes and evidence composition.
- `C1.CC.FDN.011@1` — provenance and typed locations.
- `C1.CC.FDN.012@1` — determinism and replay classification.
- `C1.CC.FDN.013@1` — cache isolation and attacker-keyed collection policy.
- `C1.CC.FDN.014@1` — canonicalization and symmetry-work budget.
- `C1.CC.FDN.015@1` — public schema evolution and migration.
- `C1.CC.FDN.016@1` — safe-Rust and unsafe-capsule admission.

### 6.2 Byte, syntax, revision, filter, and security contracts

- `C1.CC.BYT.001@1` — durable immutable byte source.
- `C1.CC.BYT.002@1` — scoped borrowed bytes and explicit promotion.
- `C1.CC.BYT.003@1` — bounded spool, segmented, and partial snapshots.
- `C1.CC.BYT.004@1` — checked ranges, spans, and source-change detection.
- `C1.CC.BYT.005@1` — exact preservation interval ledger.
- `C1.CC.BYT.006@1` — pre-graph source interval facts.
- `C1.CC.SYN.001@1` — file-syntax lexer.
- `C1.CC.SYN.002@1` — header and binary-marker discovery.
- `C1.CC.SYN.003@1` — `startxref` and EOF discovery.
- `C1.CC.SYN.004@1` — raw COS parser.
- `C1.CC.SYN.005@1` — exact scalar token interpretation.
- `C1.CC.SYN.006@1` — duplicate-preserving dictionaries.
- `C1.CC.SYN.007@1` — stream-boundary discovery.
- `C1.CC.REV.001@1` — classic xref sections.
- `C1.CC.REV.002@1` — xref streams.
- `C1.CC.REV.003@1` — hybrid links and historical chains.
- `C1.CC.REV.004@1` — immutable base revision graph.
- `C1.CC.REV.005@1` — object-occurrence discovery.
- `C1.CC.REV.006@1` — object-stream indexing.
- `C1.CC.REV.007@1` — linearization inspection.
- `C1.CC.REV.008@1` — structural signature and `ByteRange` discovery.
- `C1.CC.REV.009@1` — finalized revision graph and history-anchor overlay.
- `C1.CC.FLT.001@1` — declared filter-chain planning.
- `C1.CC.FLT.002@1` — transactional decoded-stage publication.
- `C1.CC.FLT.003@1` — ASCIIHex decode.
- `C1.CC.FLT.004@1` — ASCII85 decode.
- `C1.CC.FLT.005@1` — RunLength decode.
- `C1.CC.FLT.006@1` — Flate decode.
- `C1.CC.FLT.007@1` — TIFF/PNG predictor postprocessing.
- `C1.CC.FLT.008@1` — LZW decode with admitted `EarlyChange` handling.
- `C1.CC.FLT.009@1` — explicit Crypt/Identity stage routing.
- `C1.CC.FLT.010@1` — decoded-container identity and virtual spans.
- `C1.CC.SEC.001@1` — encryption dictionary and scope inventory.
- `C1.CC.SEC.002@1` — credential capability admission.
- `C1.CC.SEC.003@1` — version-specific password preparation and validation.
- `C1.CC.SEC.004@1` — standard-handler matrix and key derivation.
- `C1.CC.SEC.005@1` — RC4 read decryption.
- `C1.CC.SEC.006@1` — AESV2 read decryption.
- `C1.CC.SEC.007@1` — AESV3 read decryption.
- `C1.CC.SEC.008@1` — crypt-filter and object/string/stream scope.
- `C1.CC.SEC.009@1` — plaintext provenance, cache partitioning, and disposal.

### 6.3 Document and recovery contracts

- `C1.CC.DOC.001@1` — object-version resolution.
- `C1.CC.DOC.002@1` — effective object mapping and document views.
- `C1.CC.DOC.003@1` — effective dialect by selected history.
- `C1.CC.DOC.004@1` — catalog and typed structural access.
- `C1.CC.DOC.005@1` — page-tree structure and inheritance inventory.
- `C1.CC.DOC.006@1` — name and number tree structure.
- `C1.CC.DOC.007@1` — card-linked object-model validation.
- `C1.CC.DOC.008@1` — inert security-carrier inventory.
- `C1.CC.DOC.009@1` — strict-open orchestration.
- `C1.CC.DOC.010@1` — pre-view selection and mapping basis.
- `C1.CC.DOC.011@1` — limited pre-view resolver.
- `C1.CC.DOC.012@1` — encrypted-payload and unencrypted-wrapper structural inventory.
- `C1.CC.DOC.013@1` — PDF 2.0 UTF-8 text-string structural inventory.
- `C1.CC.DOC.014@1` — catalog `NeedsRendering` structural inventory.
- `C1.CC.DOC.015@1` — metadata inventory, reconciliation, and bounded XML structure.
- `C1.CC.REC.001@1` — recovery hypothesis-basis representation.
- `C1.CC.REC.002@1` — strict-before-recovery admission.
- `C1.CC.REC.003@1` — EOF/xref/revision recovery families.
- `C1.CC.REC.004@1` — stream/object-boundary recovery families.
- `C1.CC.REC.005@1` — catalog/page-link/object-stream recovery families.
- `C1.CC.REC.006@1` — bounded hypothesis search.
- `C1.CC.REC.007@1` — admissibility, partial order, and coalescing.
- `C1.CC.REC.008@1` — task-local selection with alternatives retained.
- `C1.CC.REC.009@1` — recovery report and writeback separation.
- `C1.CC.REC.010@1` — candidate-view consequence finalization.

### 6.4 Report, immune-system, CLI, and fuzz contracts

- `C1.CC.RPT.001@1` — `OpenReport` semantic body.
- `C1.CC.RPT.002@1` — `RecoveryReport` semantic body.
- `C1.CC.RPT.003@1` — structural security inventory report.
- `C1.CC.RPT.004@1` — semantic report versus run observation envelope.
- `C1.CC.RPT.005@1` — JSON/JSONL/human schema projections.
- `C1.CC.RPT.006@1` — capability manifest.
- `C1.CC.RPT.007@1` — recovery/security enrichment envelope.
- `C1.CC.RPT.008@1` — capability-admission envelope.
- `C1.CC.RPT.009@1` — `ExecutionReplayBundle` semantic body.
- `C1.CC.RPT.010@1` — `ValidationReport` semantic body for C1 layers 1–3.
- `C1.CC.IMM.001@1` — SpecCard/clause-tagging runtime projection and coverage registry.
- `C1.CC.IMM.002@1` — consequence-contract registry.
- `C1.CC.IMM.003@1` — generated claim registry.
- `C1.CC.IMM.004@1` — generated report schemas.
- `C1.CC.IMM.005@1` — generated diagnostic registry.
- `C1.CC.IMM.006@1` — named-API existence truth check.
- `C1.CC.IMM.007@1` — dependency/layer agreement truth check.
- `C1.CC.IMM.008@1` — claim-to-contract linkage truth check.
- `C1.CC.IMM.009@1` — schema/card/fixture coverage truth check.
- `C1.CC.IMM.010@1` — generated-echo and schema drift check.
- `C1.CC.IMM.011@1` — source-rights and model-context scanner.
- `C1.CC.IMM.012@1` — blocking drift auditor.
- `C1.CC.IMM.013@1` — hostile-input standalone evidence checker.
- `C1.CC.IMM.014@1` — checker isolation plan and pre-run lineage admission.
- `C1.CC.IMM.015@1` — contract migration, lapse, and withdrawal.
- `C1.CC.IMM.016@1` — minimal evidence-package assembly.
- `C1.CC.IMM.017@1` — prospective C1 event append and ledger continuation.
- `C1.CC.IMM.018@1` — pre-C1 production-ledger bootstrap and handoff.
- `C1.CC.IMM.019@1` — sealed C1 cycle trial record.
- `C1.CC.IMM.020@1` — seeded-checker trial and final lineage assessment.
- `C1.CC.CLI.001@1` — `inspect` surface.
- `C1.CC.CLI.002@1` — `revisions` surface.
- `C1.CC.CLI.003@1` — `objects` surface.
- `C1.CC.CLI.004@1` — recovery-alternative surface.
- `C1.CC.CLI.005@1` — secure credential-input surface.
- `C1.CC.CLI.006@1` — machine/human output projection.
- `C1.CC.CLI.007@1` — process status and outcome mapping.
- `C1.CC.CLI.008@1` — capability/schema discovery surface.
- `C1.CC.CLI.009@1` — evidence-package check surface.
- `C1.CC.CLI.010@1` — C1 layers 1–3 validation surface.
- `C1.CC.FUZ.001@1` — fuzz input manifest and rights gate.
- `C1.CC.FUZ.002@1` — byte-source/range target family.
- `C1.CC.FUZ.003@1` — lexer/COS target family.
- `C1.CC.FUZ.004@1` — xref/revision target family.
- `C1.CC.FUZ.005@1` — object-stream target family.
- `C1.CC.FUZ.006@1` — lossless-filter target family.
- `C1.CC.FUZ.007@1` — password/decryption target family.
- `C1.CC.FUZ.008@1` — resolver/recovery target family.
- `C1.CC.FUZ.009@1` — report/checker target family.
- `C1.CC.FUZ.010@1` — resource/cancellation/concurrency target family.
- `C1.CC.FUZ.011@1` — reachable-panic release gate.
- `C1.CC.FUZ.012@1` — witness minimization and tombstones.
- `C1.CC.FUZ.013@1` — corpus partition and held-out isolation.
- `C1.CC.FUZ.014@1` — assurance-run manifest and execution receipt.
- `C1.CC.FUZ.015@1` — assurance-lane result aggregation.
- `C1.CC.FUZ.016@1` — C1 fuzz-baseline artifact.

## 7. Dependency spine

The semantic spine begins outside candidate generation with two human-bound authority artifacts: the reviewed-card authority snapshot and the open prospective-ledger handoff. Neither is generated by C1 runtime code. For each product operation, an inert host request/source offer is inspected without reading source bytes; resource, cancellation, authority, sensitivity, and diagnostic facilities then mint `WorkContext`; only afterward may snapshot, hashing, spooling, promotion, or range work begin.

Source parsing produces raw occurrence and interval facts. Those facts finalize an immutable base revision graph; a pre-view basis then selects one strict chain or one already minted recovery-hypothesis basis without requiring a final view. Limited bootstrap resolution and pre-view security planning permit object-stream indexing. Structural signature analysis and the preservation overlay consume the base graph, and a separate finalizer emits the full immutable `RevisionGraphId`. Effective dialect and security records then allow `DocumentViewId` finalization; ordinary object resolution is downstream of that view. Recovery uses the same stages in three steps: hypothesis basis, candidate view, then consequence/ordering receipt.

Strict results and strict reports have no recovery prerequisite. Optional recovery emits separately rooted reports and an enrichment envelope. A candidate capability manifest is immutable and unaudited; truth checks emit a separate audit receipt, and an outer admission envelope binds the pair. The fuzz baseline is rooted before run manifests; runs emit terminal receipts, the reachable-panic gate consumes them, and lane aggregation follows. Checker isolation similarly has pre-run admission, checker execution, and post-trial assessment states. The pre-opened ledger records every candidate event through a low-dependency continuation contract, while a later contract seals the cycle record from those prospective events and final evidence roots.

No lower layer imports CLI, policy aggregation, laboratory adapters, or publication machinery. No security primitive discovers stream or object state through an upward dependency; the planner injects the admitted object/security context. No report schema becomes a second normative home for a contract.

## 8. Contract specifications

### 8.1 Foundation contracts

#### `C1.CC.FDN.001@1` — Typed digest and domain separation

- Identity, lifecycle, layer: active only after ratification as a C1 kernel contract in L0; capability identity is the ratified `HashProtocolId`, never a friendly algorithm label.
- Inputs and identity domain: typed class tag, protocol version, canonical payload length, canonical payload bytes, and the ratified digest-width policy.
- Preconditions: D1 and D2 are human-ratified as one package; the caller supplies a registered identity class and canonical payload produced by `C1.CC.FDN.002@1`. **PROPOSED default — awaiting ratification (D1/D2):** SHA-256 at the full 256 bits plus the deterministic-CBOR profile; if the coherent alternative is ratified, hash family and framing change together.
- Card slots: `SC.C1.FDN.HASH-IDENTITY.001` — `PENDING-LICENSED-SOURCE`; no algorithm semantics are supplied here.
- Budgets: bytes hashed, canonical bytes materialized, incremental chunks, and retained digest state charge the parent `WorkContext`; no size is inferred into an unchecked allocation.
- Cancellation: checkpoints occur before admission, between bounded chunks, and before publication; a cancelled digest is never registered as an artifact identity.
- Authority and secrets: hashing grants no authorization; sensitive or low-entropy inputs follow `C1.CC.FDN.008@1`, and public disclosure may omit or key the commitment.
- Outputs and outcomes: returns a typed digest record or canonical refusal/cancellation/indeterminacy; raw digest bytes without class and protocol are not a stable ID.
- Diagnostics: distinguish unratified protocol, unknown class, noncanonical payload, length overflow, budget exhaustion, and disclosure refusal without echoing sensitive bytes.
- Evidence and provenance: records encoder protocol, class tag, input availability, byte count, and source artifact identity where disclosure permits.
- Determinism and replay: D0 structural only for the exact protocol and canonical payload; host timing, chunking, thread order, and map order are excluded.
- Falsifiers and Gauntlet: domain-collision fixtures, chunk-boundary metamorphism, length-framing ambiguity attacks, and independent encoder/root vectors at G0–G2 after rights admission.
- Surfaces: internal identity API, schema roots, capability manifest, report identities, and checker protocol; CLI never exposes an unscoped digest as authority.
- Dependencies and consumers: depends on FDN.002, FDN.004–FDN.008; consumed by every source, graph, view, container, report, registry, and package identity.
- Migration and withdrawal: algorithm, width, domain tag, or framing change creates a new protocol version; old IDs remain typed historical records and never alias new IDs.
- No-claim boundary: a digest does not prove content availability, semantic equality, source rights, trust, integrity of an unobserved source, or caller authority.
- Rationale: one typed grammar prevents local crates from inventing incompatible hashes or treating equality of bytes as equality of meaning.

#### `C1.CC.FDN.002@1` — Canonical scalar and collection encoding

- Identity, lifecycle, layer: active only after ratification as a C1 kernel contract in L0; capability identity is the ratified canonical-encoding protocol version.
- Inputs and identity domain: typed scalars, byte strings, sequences, keyed maps, ordered sets, unordered multisets with multiplicity, optional fields, and extension records.
- Preconditions: D1/D2 are ratified as one package; every input has a registered schema and explicit order/multiplicity semantics. **PROPOSED default — awaiting ratification (D1/D2):** deterministic-CBOR profile with typed domain separation and length framing, floats forbidden, ambiguous values refused, and separately implemented producer/checker encoders.
- Card slots: `SC.C1.FDN.CANONICAL-ENCODING.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: encoded bytes, nesting, item count, sorting/canonicalization work, and symmetry work are separately reserved; FDN.014 owns the latter two limits.
- Cancellation: checkpoints precede container descent, bounded sort/canonicalization units, and sink publication; no prefix is accepted as a semantic object.
- Authority and secrets: encoding has no ambient I/O and obeys field-level disclosure classes; secret-bearing fields are rejected from public schemas unless explicitly admitted.
- Outputs and outcomes: emits one canonical byte sequence plus a schema/protocol receipt, or a typed refusal for ambiguity, unsupported extension, missing required field, or budget exhaustion.
- Diagnostics: identify field paths and schema codes without dumping protected values; duplicate and unknown-critical fields remain explicit.
- Evidence and provenance: receipt binds input schema, canonical semantics, multiplicity rules, extension policy, and consumed limits.
- Determinism and replay: D0 structural for the same typed input and protocol; insertion, allocation, traversal, locale, and thread order cannot affect bytes.
- Falsifiers and Gauntlet: non-minimal scalar encodings, duplicate-key ambiguity, unknown-critical fields, permutation tests, multiset multiplicity tests, and producer/checker dual encodings.
- Surfaces: identity construction, generated schemas, reports, contract/claim registries, evidence packages, and standalone checker.
- Dependencies and consumers: depends on FDN.004–FDN.006 and FDN.014; consumed by FDN.001 and every content-addressed C1 artifact.
- Migration and withdrawal: semantic rule changes version the protocol and require an old-to-new migration record; byte-only re-encoding cannot reinterpret an older semantic root.
- No-claim boundary: canonical bytes do not prove that the typed input was normatively correct or that an upstream parser admitted the right meaning.
- Rationale: explicit sequence, key, and multiset rules eliminate hidden dependence on host collection behavior and preserve symmetric structures honestly.

#### `C1.CC.FDN.003@1` — Collision detection and quarantine

- Identity, lifecycle, layer: active C1 kernel contract in L0; capability identity is the identity-store collision policy version.
- Inputs and identity domain: a typed content identity, class/version metadata, declared length, canonical metadata, and bytes or an availability reference.
- Preconditions: FDN.001 and FDN.002 have produced typed records; the store can compare every locally available decision-critical field.
- Card slots: `SC.C1.FDN.COLLISION-QUARANTINE.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: metadata comparison, byte recheck, quarantine storage, and incident diagnostics charge explicit limits; adversarial repeats cannot flood the store silently.
- Cancellation: cancellation before admission leaves no visible entry; cancellation during a collision investigation leaves both candidates quarantined and the outcome explicit.
- Authority and secrets: quarantine metadata inherits the more restrictive sensitivity class; incident export requires a separate protected capability.
- Outputs and outcomes: returns admitted, already-identical, quarantined-conflict, refused-unavailable, cancelled, or indeterminate-store state; “first writer wins” is forbidden.
- Diagnostics: distinguish same semantic record, missing comparison material, same-ID/different-class, length mismatch, metadata mismatch, and byte mismatch.
- Evidence and provenance: retains both provenance chains, comparison coverage, availability, protocol versions, and the exact reason admission stopped.
- Determinism and replay: D0 for local comparison given the same available records; storage crash behavior is separately observed under the ledger/backend contract.
- Falsifiers and Gauntlet: injected digest aliases, unavailable-byte cases, simultaneous insertions, crash points, and class-confusion fixtures.
- Surfaces: identity stores, caches, registries, schema/package checker, drift auditor, and protected incident record.
- Dependencies and consumers: depends on FDN.001, FDN.002, FDN.005, FDN.008, and FDN.009; all content-addressed stores consume it.
- Migration and withdrawal: a confirmed collision freezes affected cross-artifact reuse and starts a new identity protocol; old artifacts retain historical labels with a quarantine marker.
- No-claim boundary: quarantine detects an observed conflict; it does not estimate collision probability or certify an algorithm’s cryptographic strength.
- Rationale: typed collision handling turns an unlikely identity failure into a contained protocol event rather than silent artifact aliasing.

#### `C1.CC.FDN.004@1` — Operation admission and `WorkContext`

- Identity, lifecycle, layer: active C1 kernel contract in L0; each admitted operation receives a unique `RunIdentity` and immutable profile snapshot.
- Inputs and identity domain: caller request, exact operation contract ID, inert host source offer metadata/capability class, FDN.007-compiled layer-local policy view and profile snapshot, limits profile, cancellation token, resource account, diagnostic collector, capability request, secret policy, and disclosure policy. The offer is not a byte snapshot, read receipt, or source identity.
- Preconditions: contract version is active; requested capabilities are known; limit values are valid; caller authority and compiled profile view are mutually consistent; the parsing/computation core is synchronous and cancellation-aware; validating the offer performs no source read, hash, spool, promotion, range request, parser work, or async-runtime selection.
- Card slots: `SC.C1.FDN.WORK-CONTEXT.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: admission itself charges bounded validation work; the context exposes non-resettable shared counters and local ceilings for every downstream unit.
- Cancellation: admission observes cancellation before authority minting; child contexts inherit the token and cannot suppress or replace it.
- Authority and secrets: top-level host admission alone mints a private, non-copyable least-authority lease; retry, deserialization, cloning, and child construction cannot widen it.
- Outputs and outcomes: returns an immutable admitted context or typed refusal/cancellation; no partially initialized context is published.
- Diagnostics: report unknown contract, invalid limit, denied capability, incompatible policy, and unavailable secret handling without including credentials or protected request material.
- Evidence and provenance: admission receipt binds request schema, contract, caller/role identity as policy permits, profile snapshot, granted capability set, and limits.
- Determinism and replay: semantic results bind the immutable context inputs that can affect meaning; the opaque run ID and host observations remain outside D0 identity.
- Falsifiers and Gauntlet: capability-escalation attempts, forged/deserialized leases, invalid limits, retry replacement, cross-tenant context reuse, and child-context lifetime tests.
- Surfaces: all Rust operations; CLI constructs contexts only through its top-level adapter; no lower layer exposes a free constructor.
- Dependencies and consumers: depends on FDN.005–FDN.009 and ratified profile law; every C1 contract consumes an admitted context.
- Migration and withdrawal: a context schema change versions admission receipts; old contexts cannot cross a process or schema boundary by reinterpretation.
- No-claim boundary: the context bounds project-controlled work but cannot promise perfect control of compiler, allocator, OS, dependency, or hardware behavior.
- Rationale: central admission makes budgets, authority, cancellation, diagnostics, and secret policy inherited consequences instead of optional conventions.

#### `C1.CC.FDN.005@1` — Hierarchical resource accounting and reservation

- Identity, lifecycle, layer: active C1 kernel contract in L0; one `ResourceAccount` is scoped to an admitted operation and its child leases.
- Inputs and identity domain: global counters, per-item ceilings, requested reservation, resource class, hard/soft classification, explicit caller-permitted degradation modes, child-local limits, and current account generation.
- Preconditions: parent context is admitted; arithmetic is checked; child limits can only equal or narrow effective parent limits.
- Card slots: `SC.C1.FDN.RESOURCE-ACCOUNTING.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: dimensions include source bytes, objects/versions, reference depth, container depth, total decoded bytes, per-stream decoded bytes, expansion ratio, recovery branches, canonicalization/symmetry work, diagnostics, CPU quanta, wall deadline, and output bytes. Child per-stream ceilings narrow the same non-resettable total account and never mint fresh capacity.
- Cancellation: unused reservations return through a linear lease path; cancellation races and refund overflow are explicit states rather than counter resets.
- Authority and secrets: resource leases grant capacity only, never data or host authority; account labels and telemetry follow disclosure policy.
- Outputs and outcomes: reserve, consume, split, refund, and close return typed receipts; a hard limit aborts before its invariant would be violated, while a soft limit may return any explicitly caller-permitted typed `Partial` or degraded outcome declared by the owning consequence contract, including a partial recovery frontier or validation report. The outcome carries the exact covered/missing scope and fired limit. Exhaustion is a canonical limit outcome, not an ordinary parser defect, and no degraded result is `Complete`.
- Diagnostics: include resource class, requested/remaining bounded values, semantic versus operational limit, hard/soft class, permitted degradation, and deterministic truncation summaries.
- Evidence and provenance: receipts bind limits profile, starting values, consumed totals, fired limit, child ownership, and reconciliation status.
- Determinism and replay: semantic limits participate in D0 identity when outcome-sensitive; wall-clock firing is an operational cancellation observation.
- Falsifiers and Gauntlet: overflow/underflow, double refund, sibling fan-out, worker replacement, recursion, cache-hit charging, cancellation races, and conservation properties.
- Surfaces: internal budget API, reports, fuzz harness, CLI limit profiles, drift/checker hostile-input admission.
- Dependencies and consumers: this is a base contract with no C1 contract prerequisite; FDN.006/FDN.009/FDN.004 and every parser, filter, recovery branch, generator, and checker consume it.
- Migration and withdrawal: limit dimension additions version profiles and receipts; missing a new outcome-sensitive dimension invalidates affected claim reuse.
- No-claim boundary: pre-admission bounding reduces exposure but does not make every dependency allocation fallible or make process abort impossible; soft degradation never authorizes a whole-document absence, security, or conformance conclusion from partial work.
- Rationale: non-resettable hierarchical accounting prevents recursion, retry, or parallel fan-out from multiplying a caller’s allowance.

#### `C1.CC.FDN.006@1` — Cancellation and terminal-state accounting

- Identity, lifecycle, layer: active C1 kernel contract in L0; cancellation belongs to an operation, not document truth.
- Inputs and identity domain: cancellation token generation, checkpoint kind, private transaction states, outstanding leases, and operation contract.
- Preconditions: operation uses an admitted context and registers bounded checkpoint classes before expensive or externally blocking work.
- Card slots: `SC.C1.FDN.CANCELLATION.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: checkpoint latency is bounded by semantic work units; cancellation cleanup and final diagnostics retain reserved capacity.
- Cancellation: request → bounded observation → stop new work → drain or discard private state → reconcile accounts → typed terminal result.
- Authority and secrets: only the operation controller may request cancellation; cleanup obeys sensitivity policy and cannot export private bytes.
- Outputs and outcomes: returns a cancellation receipt with observed checkpoint, private/visible/indeterminate publication state, resource reconciliation, and cleanup limits.
- Diagnostics: cancellation never overwrites the causal error; contained panic, downstream refusal, host failure, and caller cancellation remain distinct causes.
- Evidence and provenance: semantic reports record fired semantic limits; run envelopes record wall-time cancellation and checkpoint observation.
- Determinism and replay: a wall-deadline-stopped run does not share a D0 result with semantic-limit execution; injected checkpoint cancellation is replayable only for the declared schedule.
- Falsifiers and Gauntlet: cancellation at every checkpoint class, double request, cancellation during commit, blocked adapter, leaked reservation, and stable diagnostic tests.
- Surfaces: every operation result, transactional decode, strict/recovery open, checker, CLI interrupt handling, and fuzz harness.
- Dependencies and consumers: depends on FDN.005; FDN.007/FDN.009/FDN.004 and all cancellable operation contracts consume it.
- Migration and withdrawal: adding or moving a checkpoint that changes observable semantic coverage versions the owning contract or replay relation.
- No-claim boundary: cancellation cannot promise rollback after host-visible publication or instant termination of an uncooperative dependency.
- Rationale: explicit terminal accounting prevents a stopped operation from leaking partial artifacts or being mislabeled as an ordinary success.

#### `C1.CC.FDN.007@1` — Least-authority leases and compiled profile snapshots

- Identity, lifecycle, layer: active C1 L0/L8 boundary contract; the L8 compiler alone turns one caller-facing `ProcessingProfile` into one immutable `ProfileSnapshotId` plus layer-local views, and one non-copyable capability lease accompanies each operation.
- Inputs and identity domain: caller-facing `ProcessingProfile`, versioned profile registry, operation contract, host registry snapshot, requested capability set, tenant/security domain, and child narrowing request.
- Preconditions: this contract's L8 compiler validates cross-policy consistency and recognizes only registered profile data; the host registry authenticates every offered capability and immutable authority snapshot. C1 recovery data names `StrictOnly`, `ConservativeRepair`, and `ForensicPreserveAll`; `CommonViewerCompatibility` and processor-emulation profiles remain unavailable until a later lawfully committed observation protocol exists.
- Card slots: `SC.C1.FDN.CAPABILITY-LEASE.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: profile parsing/compilation, registry entries, local-view fields, capability lookup, selection-manifest authentication, and child narrowing charge bounded work.
- Cancellation: capability acquisition checks cancellation before an external or blocking adapter is invoked; a child inherits the parent token.
- Authority and secrets: leases have private fields, cannot be freely cloned/serialized, and may only be borrowed or narrowed; decoders receive no trust store, network, clock, writer, or unrelated secret capability.
- Outputs and outcomes: returns a hash-bound immutable snapshot plus only the C1-relevant `OpenPolicy`, `RecoveryPolicy`, `SecurityPolicy`, and `LimitsPolicy` views and narrowed handles, or refuses unknown, stale, cross-view-inconsistent, denied, broader, or mutable-unpinned authority. Page execution, rendering, writing, and later validation-profile views remain explicitly unavailable in C1.
- Diagnostics: name capability class and authority version without exposing protected handles, credentials, endpoints, or tenant data.
- Evidence and provenance: used-capability manifests bind exact effective immutable inputs, selection witnesses, negative dependencies, and authority versions.
- Determinism and replay: the complete compiled snapshot and exact local view used are outcome-sensitive D0 inputs; reuse requires revalidation of the actual dependency/selection manifest, and a stable service or profile label alone is insufficient.
- Falsifiers and Gauntlet: unknown or cross-view-inconsistent profile, hidden default, later-view leakage, compatibility/emulation admission in C1, confused-deputy requests, broader child request, forged lease, authority rotation, negative-dependency change, tenant crossing, and mutable service tests.
- Surfaces: profile compiler, source adapters, credential provider, temporary storage, checker materialization, CLI admission, and capability manifest.
- Dependencies and consumers: depends on FDN.006 and FDN.008; FDN.004 plus byte sources, decryption, caches, reports, checker, and CLI consume it.
- Migration and withdrawal: a capability’s semantic or authority contract change versions its identity; stale snapshots cause miss/refusal, not implicit upgrade.
- No-claim boundary: possession of a typed handle proves admitted authority within one operation; it does not prove the host service is correct or immutable beyond its contract, and a recovery profile controls search/admission policy rather than what source bytes mean.
- Rationale: narrow injection preserves downward architecture and blocks hostile documents from turning data into ambient host action.

#### `C1.CC.FDN.008@1` — Sensitivity, secret lifetime, and disclosure policy

- Identity, lifecycle, layer: active C1 kernel contract in L0; every artifact and field carries a sensitivity/disclosure class independent of content addressing.
- Inputs and identity domain: source/data class, tenant, credential class, retention policy, trace class, cache class, public-commitment policy, and host isolation assumptions.
- Preconditions: caller policy is explicit; unknown classification defaults to the more restrictive admissible class.
- Card slots: `SC.C1.FDN.SECRET-DISCLOSURE.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: protected memory, spool bytes, retention, zeroization attempts, redaction, and disclosure checks are metered.
- Cancellation: cancelled work keeps private remnants classified; cleanup reports removed, retained, or unknown rather than promising erasure.
- Authority and secrets: credentials, derived keys, plaintext, attachments, source bytes, extracted text, and protected corpus data never enter ordinary diagnostics, telemetry, filenames, environment variables, or public commitments.
- Outputs and outcomes: returns admitted storage/export/cache disposition and a non-secret policy receipt; denied disclosure or unsafe persistence yields refusal or narrower availability.
- Diagnostics: use stable redacted codes; trace opt-in is separately authorized and cannot alter semantic outcomes.
- Evidence and provenance: records policy identity, host isolation assumptions, retention/disposal attempts, and disclosure decision without secret values.
- Determinism and replay: secret presence and effective capability identity may affect admissibility; secret bytes are not copied into non-secret receipts or semantic report hashes.
- Falsifiers and Gauntlet: taint fixtures, low-entropy digest guessing, log/telemetry scans, crash-remnant states, cross-tenant cache attempts, and diagnostic floods.
- Surfaces: every cache, spool, report, diagnostic, CLI credential path, evidence package, fuzz witness, and run ledger projection.
- Dependencies and consumers: this is a base policy contract with no C1 contract prerequisite; FDN.007/FDN.009/FDN.004 and all contracts that touch source or derived bytes consume it.
- Migration and withdrawal: a policy-classification error triggers invalidation/export withdrawal and incident handling; old records retain their historical policy ID.
- No-claim boundary: overwrite attempts do not promise perfect erasure from allocator, compiler, OS, swap, crash dump, hardware, or caller copies.
- Rationale: internal content identity and external disclosure are different decisions; merging them would turn useful hashes and caches into privacy leaks.

#### `C1.CC.FDN.009@1` — Bounded structured diagnostics

- Identity, lifecycle, layer: active C1 kernel contract in L0; diagnostic codes are stable within a major schema and message text is a rendering.
- Inputs and identity domain: code, severity, category, typed locations, card slots, policy contexts, structured arguments, actions, and evidence.
- Preconditions: producer is registered for the code family; locations and evidence match the current identity domain.
- Card slots: `SC.C1.FDN.DIAGNOSTICS.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: total count, bytes, per-code examples, related locations, and rendered output are bounded; reserved capacity protects security-critical summaries.
- Cancellation: collector finalization remains available after cancellation; observer failure cannot block or erase the semantic diagnostic set.
- Authority and secrets: the shared collector uses explicit interior mutability and a `Send`/`Sync` contract if shared across workers; arbitrary host callbacks are excluded while core state is live.
- Outputs and outcomes: yields a deterministic diagnostic set plus counts, affected-scope summaries, and `diagnostics_truncated` when limits fire.
- Diagnostics: meta-diagnostics report truncation, observer failure, invalid location, and code misuse without recursively flooding the collector.
- Evidence and provenance: each diagnostic links exact source/virtual/object/graph/view/contract locations and the issuer’s permitted evidence class.
- Determinism and replay: deterministic first examples and summaries belong to semantic identity; host timestamps and callback scheduling remain in the run envelope.
- Falsifiers and Gauntlet: concurrent writers, reentrancy attempts, low-severity floods, reserved-capacity tests, redaction tests, truncation, and observer panic/failure.
- Surfaces: all operations, reports, JSON/JSONL, human rendering, CLI stderr, fuzz witnesses, drift auditor, and checker.
- Dependencies and consumers: depends on FDN.005, FDN.006, and FDN.008; FDN.004 and every diagnostic-producing contract consume it. Provenance later binds diagnostic locations without making diagnostics depend on a provenance root.
- Migration and withdrawal: code semantics never change silently; changed meaning creates a new code or major schema, with durable migration notes.
- No-claim boundary: diagnostic presence is not proof that the operation covered every relevant region; truncation forbids an all-scope absence claim.
- Rationale: structured, bounded diagnostics remain machine-usable while preventing adversarial error floods and unsafe reentrant observers.

#### `C1.CC.FDN.010@1` — Claim outcomes and evidence composition

- Identity, lifecycle, layer: active C1 kernel contract in L0; validated constructors own outcome and evidence authority.
- Inputs and identity domain: requested claim scope, candidate values or alternatives, coverage partitions, evidence facets, provenance, optional `OracleLineageId` for every corroborating observation, diagnostics, and issuer capability.
- Preconditions: the issuer may mint each facet; coverage is disjoint and exhaustive relative to the requested scope; unsupported compositions fail closed.
- Card slots: `SC.C1.FDN.CLAIM-ALGEBRA.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: alternative count, coverage regions, evidence records, provenance depth, diagnostics, and composition work are bounded.
- Cancellation: cancellation is an operation terminal state outside epistemic evidence; it never manufactures a partial value.
- Authority and secrets: ordinary callers cannot mint normative, external-check, empirical, cryptographic, or proof facets from strings; caller attestations remain role- and policy-scoped.
- Outputs and outcomes: canonical algebra is singular scoped success, partial coverage, retained alternatives, or value-less refusal; terminal cancellation/indeterminacy stay separate. `OracleLineageId` records producer, implementation family, shared dependencies/data where known, protocol author, environment, adjudication relationship, and explicit unknowns without assigning a numeric independence score.
- Diagnostics: identify invalid coverage, incompatible evidence, unlicensed facet issuance, unknown composition, and unavailable decision-critical material.
- Evidence and provenance: weakness, recovery assumptions, heuristic status, and artifact availability propagate through registered claim algebras.
- Determinism and replay: deterministic computation cannot upgrade normative meaning; D0 identity covers the structured outcome under the same proper-domain inputs.
- Falsifiers and Gauntlet: contradictory coverage, fabricated facets, incompatible bounds, alternative collapse, partial-as-singular serialization, missing/forged lineage, correlated-wrapper multiplication, and evidence-laundering properties.
- Surfaces: every Rust result wrapper, report, CLI status, contract registry, claim registry, and standalone checker.
- Dependencies and consumers: depends on FDN.001–FDN.009 and FDN.011; all semantic contracts consume it.
- Migration and withdrawal: outcome or facet meaning change versions schemas/contracts and lapses affected claims; prose cannot redefine an existing ID.
- No-claim boundary: evidence records why a scoped statement is supported; it does not transform source availability, external agreement, or a hash into normative truth.
- Rationale: separating “no singular value” from evidence prevents refused, ambiguous, or partial work from carrying a flattering ordinary value.

#### `C1.CC.FDN.011@1` — Provenance and typed locations

- Identity, lifecycle, layer: active C1 kernel contract in L0; provenance nodes are typed and root-qualified, with virtual spans distinct from file spans.
- Inputs and identity domain: source roots, byte spans, revision graphs, object versions, decoded containers, virtual spans, derivation IDs, composite origins, and policy.
- Preconditions: parent IDs already exist; root ownership is validated; candidate-local IDs cannot escape finalization; cycles and invented parents are rejected.
- Card slots: `SC.C1.FDN.PROVENANCE.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: origin nodes, parent edges, span counts, composite depth, canonicalization, and retained receipts are bounded.
- Cancellation: unpublished candidate nodes are discarded or retained as private failed state; published parent graphs are immutable.
- Authority and secrets: location access obeys source and disclosure policy; a public diagnostic may retain an opaque protected location without revealing bytes.
- Outputs and outcomes: returns rooted origin/location IDs, conversion receipts, or typed refusal for cross-root ambiguity, cycle, unavailable parent, or budget exhaustion.
- Diagnostics: distinguish exact file span, observed range, virtual decoded span, enclosing container, inferred location, and location unavailable.
- Evidence and provenance: every conversion binds input/output IDs, algorithm/profile, limits, card slots, evidence facets, and no-claim boundary.
- Determinism and replay: D0 for the same typed graph and canonical protocol; ephemeral allocation handles never enter durable identity.
- Falsifiers and Gauntlet: cross-root aliasing, virtual-as-file span confusion, cyclic origins, missing parents, symmetric duplicates, and serialization-order tests.
- Surfaces: tokens, COS values, xref/revision records, decoded streams, diagnostics, reports, explanations, checker, and fuzz witnesses.
- Dependencies and consumers: depends on FDN.001–FDN.009; FDN.010–FDN.013 and all source-derived capabilities consume it.
- Migration and withdrawal: identity grammar changes version affected origin/location types and invalidate reuse that depended on old equality.
- No-claim boundary: an enclosing stream span or derivation proves container provenance, not unique inverse causality for a decoded byte or semantic finding.
- Rationale: typed provenance preserves exactness without inventing file offsets for values that exist only after decode, decryption, or recovery.

#### `C1.CC.FDN.012@1` — Determinism and replay classification

- Identity, lifecycle, layer: active C1 kernel contract in L0; every public contract declares one determinism class and an exact replay relation.
- Inputs and identity domain: proper-domain parent identities, algorithm/profile versions, semantic limits, actual dependency/selection manifest, build/target identity where required, and run observations.
- Preconditions: all outcome-sensitive inputs are identified; missing mutable host state, secrets, or fired wall deadlines are explicit.
- Card slots: `SC.C1.FDN.DETERMINISM.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: manifest validation, capture bytes, replay work, and observer effects are bounded separately from the operation being observed.
- Cancellation: fired wall deadlines and injected cancellations are recorded and cannot masquerade as semantic-limit replay.
- Authority and secrets: replay export is caller-authorized; protected inputs may be identity-only or unavailable and therefore narrow replay.
- Outputs and outcomes: returns determinism class, admitted equivalence relation, capture/availability record, and partial/refused replay reasons.
- Diagnostics: name missing inputs, changed dependency selection, build mismatch, wall-time stop, capture truncation, and unsupported relation.
- Evidence and provenance: semantic report body is separate from host run observations; replay proves only the declared relation.
- Determinism and replay: C1 semantic structures target D0; byte decoding is deterministic under admitted inputs; performance timing is never part of D0.
- Falsifiers and Gauntlet: cross-thread/order tests, manifest-change tests, timing-envelope changes, missing-secret cases, capture truncation, and repeatable-wrong-result separation.
- Surfaces: every contract registry row, report, `ExecutionReplayBundle`, capability manifest, fuzz witness, CLI metadata, and standalone checker result.
- Dependencies and consumers: depends on FDN.001–FDN.011 and FDN.013; every public operation consumes it.
- Migration and withdrawal: a broader replay promise requires a new contract version and evidence; old receipts never gain strength retroactively.
- No-claim boundary: repeatability, reproducibility, or equivalence does not prove correctness, conformance, safety, or trust.
- Rationale: classification prevents “deterministic” from becoming an unqualified adjective that hides mutable dependencies or operational timing.

#### `C1.CC.FDN.013@1` — Cache isolation and attacker-keyed collection policy

- Identity, lifecycle, layer: active C1 kernel contract in L0; caches and attacker-keyed collections are policy-bearing derived stores, not document truth.
- Inputs and identity domain: candidate index key, proper-domain parent identity, actual dependency/selection manifest, tenant/security/sensitivity domain, collection key source, and hasher/ordering policy.
- Preconditions: source identity supports the requested lifetime; cache class is bounded; collection policy is DoS-resistant or ordered for attacker-controlled keys.
- Card slots: `SC.C1.FDN.CACHE-HASHER.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: entries, bytes, lookup/probe work, eviction, manifest validation, negative-dependency checks, and materialization are charged.
- Cancellation: lookup and materialization observe cancellation; an unfinished artifact never becomes a hit or visible entry.
- Authority and secrets: indexes are partitioned by tenant, credential/security context, sensitivity, disclosure, and isolation domain; protected existence is not leaked across partitions.
- Outputs and outcomes: hit requires full manifest revalidation; otherwise miss, refused, stale, quarantined, or private-failure state is returned.
- Diagnostics: distinguish candidate hit from authorized reuse, changed selection witness, stale authority, sensitive partition denial, and hasher-policy violation.
- Evidence and provenance: entry receipt binds producer operation, proper-domain inputs, actual dependencies, security context identity, sensitivity, size, and retention.
- Determinism and replay: cache presence cannot change semantic output; candidate index order and eviction remain outside document identity.
- Falsifiers and Gauntlet: hash-flood inputs, priority/absence changes, cross-tenant timing attempts, credential crossing, source change, cancellation, and concurrent insert/evict races.
- Surfaces: source page cache, parsed objects, decoded containers, revision graphs, reports, checker caches, and repository policy checks.
- Dependencies and consumers: depends on FDN.001–FDN.011; FDN.012 plus byte, stream, object, recovery, and report derivations consume it.
- Migration and withdrawal: performance-motivated hasher changes require an explicit contract note and DoS review; unsound key grammar invalidates the cache class.
- No-claim boundary: a cache hit proves only validated reuse under its manifest; it does not grant authority or broaden source/evidence coverage.
- Rationale: two-stage reuse captures lazy dependencies while the hasher law closes the hash-flooding gap identified by audit row R2-N2.

#### `C1.CC.FDN.014@1` — Canonicalization and symmetry-work budget

- Identity, lifecycle, layer: active C1 kernel contract in L0; canonicalization work is a distinct budget dimension with an algorithm/profile identity.
- Inputs and identity domain: graph/collection shape, ordered relations, keyed relations, unordered multisets, symmetry classes, multiplicities, distinguishing anchors, and requested identity sensitivity.
- Preconditions: semantic ordering rules are declared; arbitrary allocation or traversal identity is excluded; required distinctions have admissible anchors.
- Card slots: `SC.C1.FDN.CANONICALIZATION-BUDGET.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: node/edge visits, refinement rounds, partition states, comparisons, search branches, memory, and wall cancellation are recorded separately.
- Cancellation: exhausted semantic work returns partial/refused identity construction; no noncanonical fallback is mislabeled as canonical.
- Authority and secrets: canonicalization has no host capabilities; protected graph material retains its sensitivity in diagnostics and witnesses.
- Outputs and outcomes: yields a canonical ordering/class representation plus multiplicity, or explicit unresolved symmetry and identity-sensitive refusal.
- Diagnostics: report fired canonicalization dimension, unresolved class, missing anchor, coalescing decision, and affected identity scope.
- Evidence and provenance: receipt binds algorithm/version, input identity, ordering semantics, limits, resulting class IDs, and unresolved distinctions.
- Determinism and replay: D0 only when the budgeted algorithm reaches its admitted terminal result; wall-time interruption cannot share that identity.
- Falsifiers and Gauntlet: graph permutations, repeated equal nodes, adversarial symmetry families, multiplicity changes, budget boundaries, and thread-order tests.
- Surfaces: semantic encoding, revision/recovery alternative coalescing, registry ordering, report roots, and standalone checker.
- Dependencies and consumers: depends on FDN.005, FDN.006, and FDN.009; FDN.002 and every canonical graph/content root and drift checker consume it.
- Migration and withdrawal: algorithm or ordering-law changes version affected identity protocols and trigger claim-lapse review.
- No-claim boundary: audit row R1-8 classifies the risk as graph-canonicalization complexity; the exact complexity label remains `[UNVERIFIED]` until an approved generic source is registered.
- Rationale: a separate dimension prevents canonical identity work from hiding inside object or CPU limits and avoids arbitrary refusal on ordinary duplicates.

#### `C1.CC.FDN.015@1` — Public schema evolution and migration

- Identity, lifecycle, layer: active C1 kernel contract in L0; each durable schema has an immutable semantic version and migration graph.
- Inputs and identity domain: schema ID/version, field definitions, criticality, defaults, extension rules, canonical encoding, prior versions, and migration policy.
- Preconditions: one normative registry entry exists; generated projections match it; unknown-field handling is explicitly safe or refusing.
- Card slots: `SC.C1.FDN.SCHEMA-EVOLUTION.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: parse depth, field count, migration steps, retained unknown data, diagnostics, and output bytes are bounded.
- Cancellation: migration is transactional over private output; cancellation leaves the original artifact unchanged and no new schema root visible.
- Authority and secrets: migration cannot declassify fields, mint stronger evidence, or fill absent normative meaning.
- Outputs and outcomes: returns migrated artifact plus loss/coverage receipt, unchanged compatible view, or refusal for ambiguous/unsupported/lossy change.
- Diagnostics: identify version path, unknown critical fields, repurposed fields, dropped information, and required human decision.
- Evidence and provenance: migration receipt binds source/target roots, schema versions, generator identity, transformations, losses, and checker result.
- Determinism and replay: D0 for the same source artifact, migration protocol, dependencies, and limits.
- Falsifiers and Gauntlet: unknown fields, field repurposing, downgrade/upgrade loops, duplicate semantic fields, protected-field loss, and producer/checker drift.
- Surfaces: reports, diagnostics, contract/claim registries, capability manifest, CLI JSON/JSONL, evidence packages, and ledger records.
- Dependencies and consumers: depends on FDN.001–FDN.014; consumed by RPT, IMM, CLI, and checker contracts.
- Migration and withdrawal: breaking semantic change creates a new major version; migrations never rewrite the historical source artifact in place.
- No-claim boundary: a successful structural migration does not prove that old evidence remains current or that newly added fields were historically observed.
- Rationale: durable reports and registries must evolve without silent field repurposing or retrospective invention.

#### `C1.CC.FDN.016@1` — Safe-Rust and unsafe-capsule admission

- Identity, lifecycle, layer: active C1 L0/repository-gate contract; safe Rust is the default implementation law and every admitted unsafe capsule is a separately versioned leaf boundary.
- Inputs and identity domain: exact source/build root, edition and toolchain identity, dependency/feature graph, workspace lint policy, lockfile identity, unsafe-site inventory, capsule registry, `SAFETY.md` records, public façades, and assurance evidence.
- Preconditions: D7 is ratified; the C1 build uses the Constitution's Rust 2024 edition baseline, an exact stable runtime/release pin, a committed lockfile, and deny-unsafe workspace policy. The only candidate capsule classes are SIMD intrinsics, carefully audited allocation or mapping primitives, and foreign ABI boundaries; every other class refuses before review. Any exception has explicit human admission and a registered leaf scope. The expected C1 capsule count is zero unless the human separately admits an exact leaf. **PROPOSED default — awaiting ratification (D7):** a separate date-pinned nightly supplies assurance findings only.
- Card slots: `SC.C1.FDN.SAFE-RUST-UNSAFE-CAPSULE.001` — `PENDING-LICENSED-SOURCE`; this project-law slot contains no external standard semantics.
- Budgets: source sites, dependency/features/configurations, capsule size, façade surface, Miri/sanitizer/fuzz cases, diagnostics, and evidence bytes are bounded.
- Cancellation: an interrupted inventory or assurance lane cannot admit a capsule or pass the gate; prior evidence remains scoped to its exact source/build/toolchain.
- Authority and secrets: ordinary implementers cannot waive the deny policy or expand a capsule; capsule review exposes only approved source/evidence and never grants ambient host authority.
- Outputs and outcomes: safe-only pass with zero admitted C1 capsules, registered-capsule pass with exact admitted class/scope/evidence, inadmissible-class or unregistered/reachable-unsafe failure, dependency no-claim finding, cancelled, or indeterminate coverage.
- Diagnostics: unsafe syntax/site, lint bypass, feature-only exposure, transitive native boundary, missing/stale `SAFETY.md`, façade widening, missing Miri/sanitizer/fuzz evidence, and build/toolchain mismatch.
- Evidence and provenance: gate record binds source/build/toolchain/lock/dependency roots, lint configuration, unsafe inventory, capsule reviewer/authority, invariants, façade, and executed assurance roots.
- Determinism and replay: inventory and policy result target D0 under exact source/build/features/toolchain; assurance observations retain their own replay relation and cannot be generalized to an untested target.
- Falsifiers and Gauntlet: seed unsafe behind every feature/target gate, lint override, macro/generated site, transitive native dependency, façade escape, stale invariant, missing target, Miri/sanitizer fault, and source change after review.
- Surfaces: repository/build admission, dependency truth check, capability manifest, fuzz/assurance gates, trial record, and release/cycle-close evidence; PDF semantic layers never invoke an unsafe exception by convenience.
- Dependencies and consumers: depends on D7, FDN.004–FDN.015, and the exact dependency manifest; IMM.006/IMM.007/IMM.012/IMM.019, FUZ.010/FUZ.011/FUZ.014–FUZ.016, and the C1 gates consume it. IMM.017 may record its root as opaque event payload without acquiring a semantic dependency.
- Migration and withdrawal: a new unsafe site, feature, dependency, façade, compiler, or invariant invalidates the affected admission evidence and may withdraw the capability until re-reviewed; history is not rewritten.
- No-claim boundary: safe Rust and passing capsule evidence do not prove compiler, dependency, OS, hardware, FFI, or all logic behavior memory-safe; they establish only the declared source/policy/capsule relation over the exact build envelope.
- Rationale: memory-safety posture is gate-bearing architecture, not an implied property of language choice or a local lint someone may disable.

### 8.2 Byte-source and preservation contracts

#### `C1.CC.BYT.001@1` — Durable immutable byte source

- Identity, lifecycle, layer: active C1 L1 contract; each source root binds one immutable snapshot and availability/integrity contract, never parser results.
- Inputs and identity domain: admitted `WorkContext`, inert host source offer, owned bytes, immutable paged store, audited file snapshot, a decision-blocked audited memory-mapped snapshot adapter, or another durable random-access source with a typed `SourceIdentity`.
- Preconditions: `WorkContext` exists before the first source read/hash/copy; snapshot length/range availability and immutability authority are explicit; a path, descriptor, ETag, or label alone is insufficient. The core interface is synchronous and cancellation-aware. A memory-mapped offer is unavailable unless it proves a stable immutable snapshot and, where unsafe is present, has a separately human-admitted FDN.016 mapping capsule; raw externally mutable or truncatable mappings are quarantined/refused and never authoritative.
- Card slots: `SC.C1.BYT.IMMUTABLE-SOURCE.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: admitted source bytes, range reads, page cache, I/O isolation, and revalidation work charge the operation account.
- Cancellation: bounded synchronous reads observe the context or are isolated by a separately admitted host adapter that publishes only finished immutable ranges; core code never waits indefinitely and does not import an async runtime.
- Authority and secrets: no ambient network or filesystem discovery; the caller supplies the source capability, sensitivity, retention, and disclosure class.
- Outputs and outcomes: creates `SourceRootId` with verified-content, stable-snapshot, or ephemeral identity and exact range availability; missing range/source change remain typed outcomes.
- Diagnostics: distinguish unavailable range, short read, length change, byte change, stale authority, isolation failure, and integrity mismatch without dumping source bytes.
- Evidence and provenance: exact ranges read carry `ByteExact` only under verified/stable snapshot law; ephemeral reads carry `ObservedBytes`.
- Determinism and replay: D0 byte facts require the same immutable source identity and observed range; host read timing stays outside the semantic report.
- Falsifiers and Gauntlet: mutation between reads, truncation, sparse ranges, short reads, huge offsets, raw mutable/truncatable mmap refusal, audited mapping-capsule gate, stale snapshot token, and concurrent read tests.
- Surfaces: Rust source facade, CLI file/stdin spooling adapter, lexer, hashing, xref discovery, reports, and fuzz harness.
- Dependencies and consumers: depends on FDN.001–FDN.013; consumed by every C1 byte-, graph-, view-, and checker-domain contract.
- Migration and withdrawal: observed source change revokes reusable claims/caches and requires a new source root; prior operation-local byte evidence remains historical and marked stale.
- No-claim boundary: source identity does not include a revision graph, conformance, semantics, or whole-source exactness when length/coverage/authentication is partial; a mapping's address stability or host label is not an immutability proof.
- Rationale: immutable byte truth is the base of preservation, forensics, replay, and source-change safety.

#### `C1.CC.BYT.002@1` — Scoped borrowed bytes and explicit promotion

- Identity, lifecycle, layer: active C1 L1 adapter contract; a borrowed view is lifetime-scoped and deliberately not a durable `ByteSource`.
- Inputs and identity domain: admitted `WorkContext`, caller-owned byte slice, lifetime token, sensitivity policy, and operation-local availability.
- Preconditions: the context and operation cannot outlive the borrow; no byte is inspected before admission; async retention/escape, cross-run cache insertion, preservation output, and public package use are disabled. Any asynchronous host adapter must first promote to its own immutable owned range and cannot retain the scoped borrow.
- Card slots: `SC.C1.BYT.SCOPED-BORROW.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: reads charge source-byte work; explicit promotion reserves copy/hash bytes and destination storage before starting.
- Cancellation: borrowed operations stop at ordinary checkpoints; cancelled promotion publishes no new root.
- Authority and secrets: borrow grants read access only for the caller lifetime; promotion requires an owned-storage capability and inherits sensitivity.
- Outputs and outcomes: returns a scoped document/view or a promotion receipt producing a new durable source root with explicit lineage.
- Diagnostics: report lifetime-ineligible operation, escape attempt, unavailable promotion storage, budget exhaustion, and source mutation detected by the caller contract.
- Evidence and provenance: scoped reads are operation-local; promotion records exact copied bytes or verified snapshot relation and the new root.
- Determinism and replay: scoped byte facts are D0 only within the operation; durable replay begins only after successful promotion.
- Falsifiers and Gauntlet: type/lifetime compile checks, attempted cache escape, asynchronous retention, cancellation during copy, and promotion identity tests.
- Surfaces: Rust expert facade only; CLI does not expose borrowed lifetimes.
- Dependencies and consumers: depends on BYT.001 for promotion and FDN.004–FDN.013; scoped lexer/COS operations may consume it.
- Migration and withdrawal: promotion protocol changes version its receipt; an old scoped view is never retroactively reclassified as durable.
- No-claim boundary: zero-copy use does not imply source immutability after the borrow or eligibility for preservation and public evidence.
- Rationale: a separate type prevents hidden copies or unsound `'static` promises while retaining an efficient local facade.

#### `C1.CC.BYT.003@1` — Bounded spool, segmented, and partial snapshots

- Identity, lifecycle, layer: active C1 L1 adapter contract; each committed snapshot is immutable even when its producer was streaming or segmented.
- Inputs and identity domain: admitted `WorkContext`, nonseekable stream, segmented store, admitted range response, source authority, expected ranges/length, spool policy, and source budget.
- Preconditions: the context, cumulative reservations, and host capability exist before the first read or allocation; host I/O occurs outside the random-access core; returned ranges are authenticated to one snapshot generation.
- Card slots: `SC.C1.BYT.PARTIAL-SNAPSHOT.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: spool bytes, requested ranges, gaps, requests, temporary storage, source bytes, and output bytes are bounded cumulatively.
- Cancellation: a cancelled spool/range request leaves no durable root unless an explicitly committed partial snapshot with exact coverage exists.
- Authority and secrets: range acquisition needs an explicit host capability; the parser cannot initiate network, path, or external retrieval.
- Outputs and outcomes: yields a full or versioned partial `ByteSource`, exact `RangeSet`, declared/unknown length, and missing-range outcomes.
- Diagnostics: include requested/received ranges, overlap/conflict, missing length, immutable-authority failure, source change, and spool-limit exhaustion.
- Evidence and provenance: each range records authority snapshot, exact observed bytes, availability, and whether whole-source authentication is possible.
- Determinism and replay: parsing the same committed range snapshot is D0; request timing and remote availability are operational observations.
- Falsifiers and Gauntlet: reordered/overlapping ranges, conflicting duplicates, unknown length, stalled response, partial EOF, spool exhaustion, and authority rotation.
- Surfaces: host adapter, CLI stdin spool, inert progressive-coordinator planning metadata boundary, open reports, and source fuzz targets; C1 exposes no active progressive access orchestrator.
- Dependencies and consumers: depends on BYT.001, FDN.004–FDN.013; xref/open contracts consume explicit range availability.
- Migration and withdrawal: newly available ranges create a new snapshot/view derivation, never mutate old receipts in place.
- No-claim boundary: a partial snapshot cannot support durable whole-source exactness, preservation output, all-history absence, or all-file security conclusions; the inert coordinator boundary cannot schedule hint-directed reads or claim progressive correctness.
- Rationale: explicit partiality lets inspection make bounded progress without letting hidden I/O or incomplete coverage impersonate a whole file.

#### `C1.CC.BYT.004@1` — Checked ranges, spans, and source-change detection

- Identity, lifecycle, layer: active C1 L1 contract; byte ranges are half-open, root-scoped, and constructed through checked arithmetic.
- Inputs and identity domain: source root, offset, length, available range set, declared/observed source length, and read generation.
- Preconditions: offset-plus-length is representable; requested range lies in admitted availability or yields `NeedRange`.
- Card slots: `SC.C1.BYT.CHECKED-RANGE.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: range count, coalescing/splitting work, read bytes, comparison bytes, and retained span metadata are bounded.
- Cancellation: long comparison/revalidation checks checkpoint by bounded chunks; a stopped comparison cannot authenticate the range.
- Authority and secrets: span access inherits source capability and disclosure class; location reporting may redact offsets under protected policy.
- Outputs and outcomes: creates typed `ByteSpanId`, exact read receipt, or overflow/out-of-range/missing/source-changed outcome.
- Diagnostics: stable codes distinguish arithmetic overflow, beyond-length, missing range, conflicting reread, and root mismatch.
- Evidence and provenance: successful stable reads bind source root, range, read generation, integrity class, and observed bytes identity.
- Determinism and replay: D0 for the same immutable source and range; reread conflict revokes reuse.
- Falsifiers and Gauntlet: boundary values, zero length, adjacent/overlapping spans, maximum offsets, truncated source, conflicting page, and root mix-ups.
- Surfaces: every token/location, xref/object span, signature range, report, preservation ledger, and checker.
- Dependencies and consumers: depends on BYT.001/BYT.003 and FDN.001–FDN.013; all source-backed contracts consume it.
- Migration and withdrawal: range representation changes version the span grammar; root-scoped old spans cannot be imported by bare coordinates.
- No-claim boundary: a valid range proves only an address relation; semantic ownership and cryptographic coverage are separate interval facets.
- Rationale: checked half-open ranges eliminate wraparound and ambiguous endpoint conventions at the base of every source claim.

#### `C1.CC.BYT.005@1` — Exact preservation interval ledger

- Identity, lifecycle, layer: active C1 L1 contract; `PreservationOverlayId` is an immutable derived interval-facet overlay over one source root, one `BaseRevisionGraphId`, and one exact input-fact set. A separately rooted `GraphHistoryOverlayId` is its canonical graph-neutral projection over only source/revision/history facts; carry/drop and other transformation intent cannot enter that projection.
- Inputs and identity domain: BYT.006 pre-graph facts, immutable base graph, REV.008 structural signature ranges, parse ownership, explained/unexplained state, revision status, sensitivity, raw-preservation need, and carry/drop intent.
- Preconditions: the base graph and every input fact already exist; every facet issuer is authorized; overlapping facets are allowed and never collapsed into one exclusive label.
- Card slots: `SC.C1.BYT.PRESERVATION-LEDGER.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: intervals, splits, overlaps, facet count, canonicalization, and diagnostic summaries are bounded.
- Cancellation: partial construction stays private; a published ledger states exact observation coverage and unresolved ranges.
- Authority and secrets: transformation intent is inventory-only in C1 and cannot authorize writing; protected intervals remain redacted in public projections.
- Outputs and outcomes: yields immutable `PreservationOverlayId`, interval records, and coverage summary, including unexplained gaps, signature facets, carry/drop intent, ambiguity, truncation, or refusal; it also yields `GraphHistoryOverlayId` plus an inclusion/exclusion receipt proving that only graph-neutral source/revision/history facets and their availability entered the projection.
- Diagnostics: identify facet conflicts, uncovered admitted bytes, invalid cross-root span, noncanonical overlap, and truncated interval accounting.
- Evidence and provenance: each facet binds issuer contract, source/base-graph identity, evidence, revision, and observation coverage; the full ledger and graph-history projection remain separately identifiable. A provenance link records their relation, but the full overlay root and excluded intent are not inputs to `GraphHistoryOverlayId`.
- Determinism and replay: D0 for the same facts, protocol, and limits; interval insertion order cannot affect either canonical root, and an intent-only change cannot change `GraphHistoryOverlayId`.
- Falsifiers and Gauntlet: overlapping facets, nested signature ranges, unexplained tails, duplicate facts, partial snapshots, permutation tests, and carry/drop-only mutations that leave the graph-history projection unchanged.
- Surfaces: open/revision reports, structural signature inventory, later preservation handoff, CLI byte maps, and drift/schema checks.
- Dependencies and consumers: depends on BYT.006, REV.004, REV.008, FDN.002, and FDN.009–FDN.014; REV.009 consumes only `GraphHistoryOverlayId`, while DOC.009/RPT.001 and later preservation handoff may consume the complete `PreservationOverlayId`. Neither REV.004 nor REV.008 consumes this post-base overlay.
- Migration and withdrawal: facet semantics version independently; old records remain historical and cannot silently acquire a new “explained” classification.
- No-claim boundary: retained raw bytes and interval accounting do not claim a later writer can preserve, remove, or interpret them safely.
- Rationale: independent facets retain simultaneous truths such as parsed, superseded, signed, unexplained, and sensitive.

#### `C1.CC.BYT.006@1` — Pre-graph source interval facts

- Identity, lifecycle, layer: active C1 L1 staging contract; `SourceIntervalFactsId` names immutable source-backed interval facts before any revision graph or signature relation exists.
- Inputs and identity domain: source root/coverage, BYT.004 spans, lexer/COS ownership facts, terminal/xref/link/occurrence facts, raw exclusion intervals, sensitivity, issuer identity, and limits.
- Preconditions: every fact is root-scoped and source-backed or explicitly marked unresolved; no input requires `BaseRevisionGraphId`, `RevisionGraphId`, `DocumentViewId`, signature coverage, or transformation intent.
- Card slots: `SC.C1.BYT.PREGRAPH-INTERVAL-FACTS.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: facts, intervals, overlaps, issuer records, canonicalization, diagnostics, and output bytes are bounded.
- Cancellation: a cancelled build publishes no all-scope fact set; an explicit partial set carries exact issuer and source coverage.
- Authority and secrets: issuers may add only their registered facet classes; source sensitivity and disclosure restrictions propagate without granting write authority.
- Outputs and outcomes: emits `SourceIntervalFactsId`, exact raw facts, exclusions, unresolved gaps, coverage, and typed partial/refused/cancelled states.
- Diagnostics: root mismatch, invented span, unauthorized facet, overlapping contradiction, missing issuer, source change, cap exhaustion, and partial coverage remain distinct.
- Evidence and provenance: every fact links its BYT.004 span, issuer contract, parser/discovery protocol, cards, source generation, and observation status.
- Determinism and replay: D0 for the same source-backed facts, issuers, protocol, and semantic limits; arrival order cannot affect the fact-set root.
- Falsifiers and Gauntlet: reordered issuers, duplicate/contradictory facts, payload lookalikes, uncovered regions, source mutation, partial snapshots, and cancellation.
- Surfaces: base-graph construction, signature discovery, preservation overlay, revision reports, fuzz targets, and drift checks.
- Dependencies and consumers: depends on BYT.004, SYN.001–SYN.007, REV.001–REV.003, REV.005, and FDN.001–FDN.014; REV.004, REV.008, and BYT.005 consume it.
- Migration and withdrawal: issuer/facet/protocol changes create a new fact-set ID; older facts remain immutable and may be superseded without reinterpretation.
- No-claim boundary: pre-graph facts do not assert revision membership, effective history, signature coverage, document meaning, or write intent.
- Rationale: a root-scoped fact stage gives graph and preservation producers a reproducible first input without making either depend on its own later overlay.

### 8.3 File-syntax and raw-COS contracts

#### `C1.CC.SYN.001@1` — File-syntax lexer

- Identity, lifecycle, layer: active C1 L1 contract; this lexer owns only file syntax, not content, CMap, calculator, or font languages.
- Inputs and identity domain: exact source root/range, lexer mode/version, dialect admission context, limits, and strictness.
- Preconditions: source range is available; applicable card slots have passed later rights and meaning review.
- Card slots: `SC.C1.SYN.FILE-LEXER.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: bytes scanned, tokens, token length, whitespace/comments, nesting handoff, diagnostics, and lookahead are bounded.
- Cancellation: checkpoints occur between bounded scan units and before allocating large token payloads; no half-token becomes public.
- Authority and secrets: lexer has read-only source authority and no host actions; token bytes inherit sensitivity.
- Outputs and outcomes: emits exact source-preserving tokens and spans, lexical error/refusal, or partial end at unavailable range.
- Diagnostics: invalid byte/token form, token too long, unterminated construct, missing range, and recovered-token requests remain distinct.
- Evidence and provenance: tokens carry source span, raw bytes identity, lexer protocol, evidence, and no inferred semantics.
- Determinism and replay: D0 for the same source range, mode, cards, limits, and lexer version.
- Falsifiers and Gauntlet: byte-by-byte fuzzing, token round trips, boundary splits, comment/whitespace storms, invalid delimiters, and no-progress properties.
- Surfaces: raw parser, xref parser, CLI token/byte inspection only through report schemas, and fuzz harness.
- Dependencies and consumers: depends on BYT.001–BYT.004 and FDN.001–FDN.014; SYN.002–SYN.007 and REV contracts consume it.
- Migration and withdrawal: token semantic changes version lexer protocol and dependent derivations; source bytes remain unchanged.
- No-claim boundary: recognizing a token does not establish COS contextual validity, object-model validity, or conformance.
- Rationale: a dedicated exact lexer preserves source reality and prevents superficially similar embedded languages from sharing wrong error rules.

#### `C1.CC.SYN.002@1` — Header and binary-marker discovery

- Identity, lifecycle, layer: active C1 L1 contract; discovery records candidates and one strict interpretation per selected policy.
- Inputs and identity domain: source root, admitted prefix range, lexer result, strictness/recovery profile, and dialect-card slots.
- Preconditions: required prefix bytes are available and source identity remains stable.
- Card slots: `SC.C1.SYN.HEADER.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: prefix search bytes, candidate count, token work, and diagnostics are bounded.
- Cancellation: scanning stops at bounded checkpoints and returns observed coverage, never an implied absence beyond it.
- Authority and secrets: read-only source; no external lookup or version upgrade.
- Outputs and outcomes: records first valid candidate, exact offset, declared version token, binary marker state, leading bytes, and strict/recovered status.
- Diagnostics: no candidate in searched region, nonzero offset, malformed version, multiple candidates, binary-marker issue, and unavailable prefix.
- Evidence and provenance: every candidate binds exact span and acceptance/rejection reason.
- Determinism and replay: D0 for the same source coverage, cards, profile, and limits.
- Falsifiers and Gauntlet: embedded false headers, prefix junk, truncated markers, multiple candidates, boundary offsets, and partial prefix snapshots.
- Surfaces: open report, effective dialect input, CLI inspect, and recovery hypotheses.
- Dependencies and consumers: depends on SYN.001, BYT.004, FDN.009–FDN.012; consumed by DOC.003, DOC.009, and REC.003.
- Migration and withdrawal: card or acceptance changes create a new derivation/view; old candidate records remain inspectable.
- No-claim boundary: a header token alone does not determine effective dialect, feature legality, or file-wide conformance.
- Rationale: recording position and alternatives prevents compatibility handling from rewriting malformed placement into strict truth.

#### `C1.CC.SYN.003@1` — `startxref` and EOF discovery

- Identity, lifecycle, layer: active C1 L1 contract; strict terminal discovery and recovery candidate search remain distinct modes.
- Inputs and identity domain: source root, available trailing ranges, declared/observed length, lexer, strictness/recovery policy, and search bounds.
- Preconditions: the requested terminal range is available or missing coverage is explicit.
- Card slots: `SC.C1.SYN.EOF-STARTXREF.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: trailing bytes scanned, candidates, parsed offsets, plausibility checks, and diagnostics are bounded.
- Cancellation: candidate search checkpoints by bounded range; a stopped search returns coverage and no all-tail absence claim.
- Authority and secrets: read-only source; no implicit request for missing ranges.
- Outputs and outcomes: strict terminal result plus candidate list with spans, offsets, plausibility, and acceptance/rejection evidence.
- Diagnostics: malformed/missing marker, offset overflow, target unavailable/out of bounds, trailing bytes, multiple candidates, and search-limit exhaustion.
- Evidence and provenance: each candidate carries exact source span and rule/profile basis.
- Determinism and replay: D0 under the same snapshot, range coverage, cards, profile, and semantic search budget.
- Falsifiers and Gauntlet: false markers in streams, huge offsets, duplicate tails, truncated final revision, trailing junk, and partial-source tests.
- Surfaces: open/revision reports, CLI revisions, xref discovery, and recovery.
- Dependencies and consumers: depends on SYN.001, BYT.003–BYT.004; REV.001–REV.004 and REC.003 consume it.
- Migration and withdrawal: changed recovery search protocol yields new hypotheses/graph IDs without changing source root.
- No-claim boundary: a plausible marker is not proof of a valid xref target or singular revision history.
- Rationale: explicit candidates and search bounds make malformed terminal handling auditable and DoS-bounded.

#### `C1.CC.SYN.004@1` — Raw COS parser

- Identity, lifecycle, layer: active C1 L1 contract; raw values preserve syntax and never assume contextual semantic validity.
- Inputs and identity domain: source root/range, token stream, parse mode, dialect context, recursion/container limits, and recovery prohibition or explicit hypothesis.
- Preconditions: lexer tokens are source-bound; card slots are rights-reviewed later; strict mode receives no recovery substitutions.
- Card slots: `SC.C1.SYN.RAW-COS.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: values, container nesting, array/dictionary entries, string/name bytes, number length, recursion, and diagnostics are bounded.
- Cancellation: checkpoints occur between values/entries and before nested descent; private partial trees do not enter caches.
- Authority and secrets: read-only source; encrypted strings remain raw ciphertext until SEC contracts admit decryption.
- Outputs and outcomes: emits raw null/bool/number/name/string/array/dictionary/stream/reference values with exact token spans, or typed parse outcome.
- Diagnostics: distinguish lexical error, structural delimiter error, invalid reference shape, limit, missing range, and encrypted/uninterpreted state.
- Evidence and provenance: every node binds source tokens/spans, parser protocol, strict/recovered status, and diagnostic set.
- Determinism and replay: D0 under the same source, token stream, cards, mode, and semantic limits.
- Falsifiers and Gauntlet: recursive nesting, delimiter storms, malformed references, encrypted bytes, allocation failures, cancellation, and token-to-tree round trips.
- Surfaces: xref stream dictionaries, object occurrences, resolver inputs, CLI objects, reports, and fuzz harness.
- Dependencies and consumers: depends on SYN.001, BYT.001–BYT.004, and FDN.001–FDN.014; most REV/FLT/SEC/DOC contracts consume it.
- Migration and withdrawal: parser/card change creates new derivations; raw token/source identities remain stable.
- No-claim boundary: syntactic admission does not claim object-model validity, resolved meaning, decryption, or recovery-free conformance.
- Rationale: raw/interpreted separation preserves exact bytes and prevents early casts from erasing malformed or duplicate evidence.

#### `C1.CC.SYN.005@1` — Exact scalar token interpretation

- Identity, lifecycle, layer: active C1 L1 contract; scalar interpretation retains lexical form beside parsed mathematical/byte value.
- Inputs and identity domain: one raw number, name, literal/hex string, boolean, null, or reference token group with source spans and dialect context.
- Preconditions: tokens are admitted by SYN.001 and belong to one source root; decryption is a later separate derivation.
- Card slots: `SC.C1.SYN.SCALAR-VALUES.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: token bytes, numeric digits, escape work, decoded name/string bytes, and diagnostics are bounded.
- Cancellation: long escape/numeric processing checkpoints by bounded chunks; no partial decoded scalar is published.
- Authority and secrets: raw/encrypted string bytes retain sensitivity; interpretation never logs contents by default.
- Outputs and outcomes: records raw spelling, parsed value, lexical class, overflow/underflow, normalization eligibility, recovery status, and source span.
- Diagnostics: invalid escape/digit, overflow, underflow, malformed hex, unexpected delimiter, and unsupported interpretation remain separate.
- Evidence and provenance: parsed values are deterministically derived from exact tokens; text decoding and normative contextual meaning are excluded.
- Determinism and replay: D0 for the same token, parser version, cards, and limits; locale does not participate.
- Falsifiers and Gauntlet: numeric boundaries, noncanonical spellings, escape permutations, odd hex forms, huge tokens, and raw round-trip properties.
- Surfaces: raw COS, dictionaries, xrefs, encryption dictionaries, reports, and CLI object rendering.
- Dependencies and consumers: depends on SYN.001/SYN.004 and FDN.001–FDN.014; all structural consumers use it.
- Migration and withdrawal: interpretation change versions the derivation; exact raw tokens remain authoritative source facts.
- No-claim boundary: parsed string bytes are not Unicode text, decrypted content, or a contextually valid field value.
- Rationale: retaining raw and parsed forms enables source preservation, diagnostics, and later profile-specific decisions without re-lexing.

#### `C1.CC.SYN.006@1` — Duplicate-preserving dictionaries

- Identity, lifecycle, layer: active C1 L1 contract; each dictionary entry has ordered occurrence identity and exact key/value spans.
- Inputs and identity domain: raw dictionary tokens/values, source root, occurrence order, and later profile-specific selection request.
- Preconditions: SYN.004 produced all entries without deduplicating; selection policy is explicit and card-linked.
- Card slots: `SC.C1.SYN.DICTIONARY-DUPLICATES.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: entries, duplicate groups, key bytes, lookup work, selection alternatives, and diagnostics are bounded.
- Cancellation: construction/lookup checkpoints between entries; no partially deduplicated map is published.
- Authority and secrets: lookup has no host authority; protected values remain classified.
- Outputs and outcomes: exposes ordered entries, all occurrences per key, and separately a selected occurrence claim or ambiguity/refusal.
- Diagnostics: duplicate key, invalid key type, conflicting occurrences, selection-policy absence, and budget truncation carry exact entry locations.
- Evidence and provenance: selected meaning cites every candidate occurrence, profile, cards, and reason; discarded evidence is never erased.
- Determinism and replay: D0; source order is semantic input where the profile says so, never host-map iteration order.
- Falsifiers and Gauntlet: duplicate storms, equal/different values, permutation-sensitive fixtures, lookup truncation, and selection-profile changes.
- Surfaces: raw COS, xref/trailer, stream/encryption dictionaries, resolver, reports, and CLI objects.
- Dependencies and consumers: depends on SYN.004/SYN.005, FDN.013–FDN.014; structural and semantic dictionary consumers use it.
- Migration and withdrawal: changed selection policy produces a new document view; raw dictionary identity remains source-bound.
- No-claim boundary: one selected occurrence under a profile does not make the original dictionary unique or conforming.
- Rationale: preserving duplicates is required for forensics, compatibility explanation, and honest recovery.

#### `C1.CC.SYN.007@1` — Stream-boundary discovery

- Identity, lifecycle, layer: active C1 L1 contract; strict boundaries and recovered alternatives are separate source-backed claims.
- Inputs and identity domain: raw stream dictionary/object occurrence, source root, declared length value/reference, candidate payload range, lexer, and policy.
- Preconditions: enclosing object structure is admitted; strict mode follows only rights-reviewed card behavior.
- Card slots: `SC.C1.SYN.STREAM-BOUNDARY.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: declared-length resolution, candidate search bytes, boundary alternatives, filter-termination probes, and diagnostics are bounded.
- Cancellation: search/probes checkpoint; partial search returns coverage and alternatives rather than a chosen boundary.
- Authority and secrets: read-only source; probing does not decrypt or decode unless an explicit dependent contract and capability are admitted.
- Outputs and outcomes: exact strict payload/end markers or recovered candidates with evidence, affected spans, and material ambiguity.
- Diagnostics: missing/invalid length, unresolved reference, out-of-range length, missing markers, conflicting candidates, and search-limit exhaustion.
- Evidence and provenance: each candidate binds source spans, declared facts, probes used, cards/profile, and recovered status.
- Determinism and replay: D0 for the same source, view inputs, protocol, capabilities, and semantic limits.
- Falsifiers and Gauntlet: marker bytes inside payload, wrong lengths, missing markers, truncated streams, filter-termination disagreement, and huge searches.
- Surfaces: stream records, xref/object streams, filter planner, recovery report, CLI objects, and fuzz harness.
- Dependencies and consumers: depends on SYN.004–SYN.006 and BYT.001–BYT.004; optional DOC.001/FLT probes are downstream consumers that may evaluate an already recorded candidate through an acyclic orchestration adapter. REV.002/REV.006/FLT.001 also consume it.
- Migration and withdrawal: recovered boundary protocol changes yield new hypotheses and document views; source spans never mutate.
- No-claim boundary: a recovered boundary does not make the stream syntactically conforming or its decoded content singular.
- Rationale: treating malformed length handling as an evidenced hypothesis prevents silent “successful” parsing of payload markers.

### 8.4 Xref, revision, object-stream, and signature-structure contracts

#### `C1.CC.REV.001@1` — Classic xref sections

- Identity, lifecycle, layer: active C1 L1 contract; one record represents what one classic section declares, not the effective document mapping.
- Inputs and identity domain: source root, candidate xref offset/span, file lexer, trailer dictionary, selected dialect/cards, and strictness.
- Preconditions: target range is available; candidate origin is recorded; strict and recovered inputs are not conflated.
- Card slots: `SC.C1.REV.XREF-TABLE.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: subsections, entries, object numbers, line/token bytes, free-list checks, trailer size, and diagnostics are bounded.
- Cancellation: checkpoints between subsections/entries; private partial sections carry observed coverage and never become effective mappings.
- Authority and secrets: read-only source; no host or decryption capability is needed for the classic section itself.
- Outputs and outcomes: emits section entries, trailer, exact spans, validation findings, and strict/recovered outcome.
- Diagnostics: malformed subsection, overlap, duplicate entry, offset/generation overflow, invalid flag, free-list issue, and unavailable target.
- Evidence and provenance: every entry binds exact source span and section/candidate identity.
- Determinism and replay: D0 under the same source, cards, protocol, strictness, and limits.
- Falsifiers and Gauntlet: huge counts, overlapping ranges, malformed widths, duplicate object entries, invalid offsets, cancellation, and round-trip fixtures.
- Surfaces: revision graph, open report, CLI revisions/objects, and fuzz target.
- Dependencies and consumers: depends on SYN.001, SYN.003–SYN.006, BYT.001–BYT.004, and FDN.001–FDN.014; REV.003/REV.004 consume it.
- Migration and withdrawal: parser/card change yields new section derivations; exact declaration bytes remain stable.
- No-claim boundary: a parsed xref declaration does not prove the object exists at that offset or that the section belongs to the singular effective history.
- Rationale: declaration/effective/history separation prevents a malformed or superseded table from overwriting physical object evidence.

#### `C1.CC.REV.002@1` — Xref streams

- Identity, lifecycle, layer: active C1 L1 contract; xref stream parsing is a bounded composition of raw stream, declared filter chain, and xref entry interpretation.
- Inputs and identity domain: exact object occurrence, raw dictionary, strict stream boundary, committed FLT.002 bootstrap-stage output/receipt, source/revision context, and cards; no `DecodedContainerId` is an input.
- Preconditions: xref-stream non-encryption rules and permitted filters are later card-reviewed; the non-cryptographic FLT.001–FLT.008 chain commits through FLT.002 before entry interpretation.
- Card slots: `SC.C1.REV.XREF-STREAM.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: decoded bytes/ratio, entry widths/counts, index ranges, object numbers, trailer keys, and diagnostics are bounded.
- Cancellation: decode and entry iteration checkpoint; no partial entry table is published as a section.
- Authority and secrets: planner injects context; xref streams cannot obtain credentials or host actions and are not decrypted unless a later card explicitly admits a case.
- Outputs and outcomes: emits section entries, trailer-equivalent data, exact source spans plus virtual decoded offsets/lengths rooted in the bootstrap stage output, decode receipt, and strict/refused status.
- Diagnostics: invalid widths/index/count, decoded length mismatch, forbidden encryption, filter refusal, duplicate/overflow entry, and truncation.
- Evidence and provenance: each entry links its virtual decoded offset/length → committed FLT.002 bootstrap stage/output receipt → exact source stream occurrence and ordered filter receipts; this bootstrap chain is explicitly not a decoded-container identity.
- Determinism and replay: D0 under the same source/occurrence, filter protocol, cards, and semantic limits.
- Falsifiers and Gauntlet: width arithmetic overflow, truncated rows, huge index, illegal filters, malformed dictionary, decode bombs, virtual bootstrap-span attribution, and rejection of `DecodedContainerId`/security-context injection.
- Surfaces: revision graph, open report, CLI revisions/objects, and fuzz targets.
- Dependencies and consumers: depends on SYN.004–SYN.007 and the non-cryptographic lossless stages FLT.001–FLT.008; REV.003/REV.004 consume it. Decoded-container identity and document security are downstream and cannot enter xref bootstrap.
- Migration and withdrawal: filter/card/parser change yields a new section derivation and potentially new revision graph ID.
- No-claim boundary: successful decoding does not prove the stream is the selected xref or that its object mapping is globally consistent.
- Rationale: explicit composition avoids an xref parser bypassing filter budgets, provenance, or non-encryption rules.

#### `C1.CC.REV.003@1` — Hybrid links and historical chains

- Identity, lifecycle, layer: active C1 L1 contract; link records preserve `/Prev`, `/XRefStm`, trailer, and section relationships as asserted evidence.
- Inputs and identity domain: classic/xref-stream sections, exact link values/spans, source root, candidate terminal marker, and selected cards/profile.
- Preconditions: section identities exist; link arithmetic and target ranges are checked; recovery links remain hypotheses.
- Card slots: `SC.C1.REV.HYBRID-HISTORY.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: link traversals, visited offsets, branches, cycles, sections, and diagnostics are bounded.
- Cancellation: traversal returns observed subgraph and unresolved frontier; it never selects the last visited chain as truth.
- Authority and secrets: read-only source; links cannot trigger missing-range retrieval.
- Outputs and outcomes: emits typed edges, cycles, broken links, hybrid relationships, candidate chains, and exact unresolved gaps.
- Diagnostics: target missing/out of range, cycle, self-link, conflicting section, hybrid disagreement, branch cap, and unavailable range.
- Evidence and provenance: every edge binds source field span, target evidence, cards/profile, and strict/recovered status.
- Determinism and replay: D0 under the same sections, ranges, protocol, and semantic limits.
- Falsifiers and Gauntlet: cycles, forks, broken pointers, xref-table/stream disagreement, duplicate offsets, partial sources, and traversal order permutations.
- Surfaces: revision graph, recovery, open/revision report, CLI revisions, and fuzz harness.
- Dependencies and consumers: depends on REV.001/REV.002, SYN.003, BYT.004; REV.004 and REC.003 consume it.
- Migration and withdrawal: changed admission rules create a new graph derivation; older link evidence remains inspectable.
- No-claim boundary: one traversable chain is not automatically singular, current, or conforming when alternatives survive.
- Rationale: graph-shaped history is required for malformed forks and hybrid disagreement that a single linked list would erase.

#### `C1.CC.REV.004@1` — Immutable base revision graph

- Identity, lifecycle, layer: active C1 L1 staging contract; `BaseRevisionGraphId` is a content-addressed derivation over one source root and pre-graph fact set, not the finalized `RevisionGraphId` and not part of `SourceRootId`.
- Inputs and identity domain: source root/coverage, discovered sections/links, raw object occurrences, BYT.006 interval facts, protocol/version, limits, recovery assumptions, and unresolved gaps.
- Preconditions: all nodes/edges are source-bound; candidate effective-chain selection is excluded from the graph identity.
- Card slots: `SC.C1.REV.REVISION-GRAPH.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: nodes, edges, occurrences, chain alternatives, canonicalization/symmetry work, coverage map, and diagnostics are bounded.
- Cancellation: partial graph stays private or is published only as an explicit partial observation artifact without an effective-view claim.
- Authority and secrets: graph discovery is read-only; protected source locations remain access-controlled.
- Outputs and outcomes: emits immutable base graph, `BaseRevisionGraphId`, coverage, admissible chain bases, assumptions, gaps, and supersession relation to older base graphs.
- Diagnostics: inconsistent link, orphan section, conflicting raw mapping, unexplained region, cap exhaustion, and source change; signature and decoded-member relations are explicitly pending post-base stages.
- Evidence and provenance: graph records exact source root, observed ranges, discovery/parser protocols, cards, limits, and every source-backed node/edge.
- Determinism and replay: D0 for the same source snapshot, coverage, protocols, cards, assumptions, and semantic limits.
- Falsifiers and Gauntlet: permutation/canonicalization, graph forks/cycles, protocol changes over same source, partial range extension, and old-receipt stability.
- Surfaces: pre-view bootstrap, security planning, object-stream indexing, signature discovery, final graph construction, recovery-family generation, and revision fuzzing.
- Dependencies and consumers: depends on REV.001–REV.003, REV.005, BYT.006, and FDN.001–FDN.014; REV.006/REV.008/REV.009, DOC.010, SEC bootstrap, and recovery-family contracts consume it.
- Migration and withdrawal: new parser/cards/ranges/limits create a new graph ID that may supersede but never mutate an older graph.
- No-claim boundary: the base graph does not select one effective document view, include post-base decoded members/signature relations, or assert that every physical object belongs to a valid history.
- Rationale: an immutable base graph gives post-base analyzers a first graph identity; REV.009 later binds their overlays without mutating this evidence.

#### `C1.CC.REV.005@1` — Object-occurrence discovery

- Identity, lifecycle, layer: active C1 L1 contract; occurrences are physical/virtual definitions classified by discovery source and admission status.
- Inputs and identity domain: xref declarations including compressed-entry locators, source scan regions, SYN/BYT exclusion facts, lexer/parser, source root, and policy.
- Preconditions: strict occurrences originate in admitted raw xref evidence; scan discoveries remain recovery-hypothesis candidates until checked; decoded object-stream indexes and graph identities are unavailable inputs here.
- Card slots: `SC.C1.REV.OBJECT-OCCURRENCE.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: scan bytes, header candidates, parsed candidates, exclusion intervals, overlap checks, and diagnostics are bounded.
- Cancellation: scan returns exact coverage/frontier and no all-source absence conclusion.
- Authority and secrets: read-only source; scanner cannot open missing ranges or decrypt arbitrary payloads.
- Outputs and outcomes: classifies xref-declared, scan-discovered, compressed-entry locator, orphaned parseable, rejected lookalike, and unexplained regions; decoded object-stream members are a later REV.006 overlay.
- Diagnostics: false header in payload, invalid boundary, overlap, duplicate definition, unavailable range, and admission cap.
- Evidence and provenance: each occurrence binds exact source span or unresolved compressed locator, discovery path, defining revision candidate, parser outcome, and assumptions.
- Determinism and replay: D0 for the same source/coverage, exclusion map, protocol, and semantic limits.
- Falsifiers and Gauntlet: `obj` patterns inside strings/streams, overlapping objects, truncated tails, orphan objects, huge candidate storms, and exclusion-boundary tests.
- Surfaces: revision graph, object resolver, open report, CLI objects, recovery, and fuzz target.
- Dependencies and consumers: depends on SYN.001/SYN.004/SYN.007, REV.001–REV.003, and BYT.004; BYT.006, REV.004/REV.006/REV.008, DOC.010, and recovery-family contracts consume the raw occurrence inventory.
- Migration and withdrawal: improved scanning creates new graph/occurrence derivations; source-backed old occurrence records remain historical.
- No-claim boundary: a parseable header does not prove valid indirect-object membership, effective visibility, or indexed object-stream membership.
- Rationale: explicit rejected and orphan classes keep forensics from discarding physical evidence or promoting payload lookalikes.

#### `C1.CC.REV.006@1` — Object-stream indexing

- Identity, lifecycle, layer: active C1 L1 contract; members are virtual occurrences within one decoded container and revision security context.
- Inputs and identity domain: containing raw occurrence, `BaseRevisionGraphId`, `DocumentViewBasisId`, strict stream boundary, explicit `SecurityContextId`, decryption/filter context when applicable, decoded container, object-count/offset header, and cards.
- Preconditions: the containing revision/security identity is exact; an unencrypted/Identity context needs no credential or plaintext transaction, while a declared encrypted context requires at-most-once container decryption and a committed decoded transaction.
- Card slots: `SC.C1.REV.OBJECT-STREAM.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: decoded bytes/ratio, member count, header pairs, offsets, parsed members, virtual spans, cache bytes, and diagnostics are bounded.
- Cancellation: indexing/parsing checkpoints between pairs/members; no partial index becomes cache-visible as a finished container index.
- Authority and secrets: plaintext inherits credential/tenant/sensitivity partition; members never request credentials or decrypt themselves again.
- Outputs and outcomes: emits immutable basis-qualified `ObjectStreamOccurrenceSetId`, monotone bounded index, virtual member spans, duplicate/missing member findings, and per-member parse outcomes for later graph finalization. One set cannot finalize or select a graph by itself and may enter graph finalization only through the complete discovery/recovery-protocol frontier validated by REV.008, never a caller/task-filtered subset.
- Diagnostics: invalid count/first offset, nonmonotone/out-of-range offset, duplicate object number, nested-stream violation, xref mismatch, and decode failure.
- Evidence and provenance: member → virtual span → decoded container → encrypted/filtered source object chain is retained.
- Determinism and replay: D0 under exact container, security/filter context, cards, and semantic limits.
- Falsifiers and Gauntlet: double-decryption traps, huge counts, duplicate/nonmonotone offsets, truncated data, nested stream, credential crossing, cache isolation, and task-filtered omission from a declared graph frontier.
- Surfaces: object occurrence/resolver, open report, CLI objects, recovery, and fuzz target.
- Dependencies and consumers: depends on REV.004/REV.005, DOC.010, SYN.004–SYN.007, FLT.001–FLT.010, SEC.001/SEC.008, and conditionally SEC.004–SEC.009 for declared encrypted contexts; REV.009, DOC.001, and later recovery/report contracts consume it.
- Migration and withdrawal: changed decode/security/parser protocol yields a new container/index identity; plaintext caches under old context are invalidated.
- No-claim boundary: indexed membership does not make the member independently source-spanned, independently encrypted, or contextually valid.
- Rationale: one-time container decryption plus virtual provenance closes double-decryption and invented-offset failures.

#### `C1.CC.REV.007@1` — Linearization inspection

- Identity, lifecycle, layer: active C1 L1 contract; C1 only recognizes and structurally validates linearization data for inspection.
- Inputs and identity domain: source root/coverage, first-object candidate, raw dictionaries, hint-stream candidates, xref/revision evidence, and cards.
- Preconditions: required ranges are present; no hint claim is trusted before structural checks.
- Card slots: `SC.C1.REV.LINEARIZATION-READ.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: dictionaries, hint bytes, ranges, page/object references, validation work, and diagnostics are bounded.
- Cancellation: validation returns observed scope; no hint table authorizes reads after cancellation or beyond availability.
- Authority and secrets: inspection has read-only source authority and cannot fetch ranges implicitly.
- Outputs and outcomes: inventory of declared linearization, validated/invalid fields, hint structure status, missing ranges, and fallback requirement.
- Diagnostics: malformed dictionary, impossible offset/length, inconsistent xref/page data, invalid hint range, and unavailable dependency.
- Evidence and provenance: every finding binds exact source span, graph/view input, cards, and validation coverage.
- Determinism and replay: D0 under the same snapshot, range coverage, cards, and limits.
- Falsifiers and Gauntlet: malicious offsets, overlapping hints, partial source, inconsistent counts, hint bombs, and ordinary fallback equivalence.
- Surfaces: open report, capability manifest, CLI inspect, progressive host planning metadata, and fuzz target.
- Dependencies and consumers: depends on SYN.001–SYN.007, REV.001–REV.005, and BYT.001–BYT.004 raw-source artifacts; BYT.005 is a later preservation overlay. DOC.005 may later enrich page relations, and RPT.001 may report the resulting structural inventory.
- Migration and withdrawal: future writer or progressive behavior gets separate contracts; this inspection contract is not widened in place.
- No-claim boundary: recognizing linearization does not claim progressive correctness, writer support, or that hint-directed access is safe without validation.
- Rationale: early inventory supports R0 forensics while keeping writer and active progressive orchestration outside C1.

#### `C1.CC.REV.008@1` — Structural signature and `ByteRange` discovery

- Identity, lifecycle, layer: active C1 cross-cutting L1/L2 contract required by R0; it answers structural byte/history questions only.
- Inputs and identity domain: source root, immutable base graph, raw object occurrences, one complete declared graph-overlay frontier manifest enumerating every graph-relevant admitted basis/security context and its REV.006 `ObjectStreamOccurrenceSetId` entries with availability, candidate source-backed or virtual signature fields/dictionaries, duplicate-preserved raw `ByteRange`, `/Filter`, `/SubFilter`, seed-value, lock, and transform-parameter carrier occurrences, BYT.006 interval facts, and source/virtual-member coverage.
- Preconditions: the frontier manifest is complete for the exact discovery/recovery protocol, limits, and coverage and contains no caller/task filtering; applicable structure and object-stream cards are later reviewed. A virtual member is classified only when active reviewed authority admits that applicability. While the required card is pending, unsupported, or unavailable, member coverage remains explicitly pending/unsupported/unavailable and cannot be inferred from carrier shape or model memory. Candidate discovery uses exact source or virtual provenance and does not require CMS/trust processing.
- Card slots: `SC.C1.SEC.SIGNATURE-STRUCTURE.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: raw and virtual candidate fields/dictionaries, frontier entries, ranges, arithmetic, overlap/gap analysis, revision relationships, and diagnostics are bounded.
- Cancellation: scanning returns exact coverage and candidates found; it cannot claim no signatures outside observed scope.
- Authority and secrets: read-only source; no trust store, clock, revocation, signer, or network capability is requested.
- Outputs and outcomes: validates and emits canonical `GraphOverlayFrontierId`, then emits immutable `StructuralSignatureSetId` and inventories admitted source-backed and virtual signature candidates, raw `/Filter`/`/SubFilter` family labels, seed-value/lock/transform carriers without impact interpretation, exact ranges, ordering/overlap/bounds/trailing-byte conditions, covered base-revision candidates, structural ambiguity, and exact pending/unsupported/unavailable virtual-member coverage.
- Diagnostics: malformed array, odd count, overflow, overlap, out-of-bounds, uncovered gaps, trailing bytes, missing/duplicate/unclassified family or seed/lock carrier, unresolved field relation, incomplete graph frontier, pending or unsupported virtual-member applicability, and partial source/member coverage.
- Evidence and provenance: the frontier root binds its complete manifest, base graph, protocol, limits, coverage, and every entry/availability class; each range and field links exact tokens, source occurrence or REV.006 virtual member/container chain, base graph, frontier entry, applied cards, and coverage. No virtual span is relabeled as a file span.
- Determinism and replay: D0 under the same source/base graph/fact/frontier sets, cards, availability, and semantic limits.
- Falsifiers and Gauntlet: overlapping/nested/out-of-order ranges, integer overflow, raw and card-admitted virtual family/seed/lock carriers, pending-card member cases, duplicate occurrences, multi-revision signatures, shadowed fields, incomplete frontiers, partial sources/members, and false candidate carriers.
- Surfaces: OpenReport, structural security report, preservation ledger, CLI inspect/revisions/objects, and recovery ambiguity checks.
- Dependencies and consumers: depends on SYN.004–SYN.006, REV.004–REV.006, BYT.004, and BYT.006; BYT.005, REV.009, DOC.008, RPT, and close-gate workflows consume structural signature candidates.
- Migration and withdrawal: later R2 signature-impact classification and R3 cryptographic/trust validation receive new contract IDs; they do not reinterpret this output as stronger evidence.
- No-claim boundary: discovery and raw family naming do not compute a digest, parse or validate CMS, trust a certificate, classify DocMDP/FieldMDP/lock modification impact, or assert legal validity.
- Rationale: moving structural range discovery into R0 closes audit row R2-N1 without pulling later cryptographic trust into C1.

#### `C1.CC.REV.009@1` — Finalized revision graph and history-anchor overlay

- Identity, lifecycle, layer: active C1 L1 finalization contract; `RevisionGraphId` is minted once from an immutable base graph and exact post-base overlays, never by mutating `BaseRevisionGraphId`.
- Inputs and identity domain: `BaseRevisionGraphId`; one closed canonical `GraphOverlayFrontierId` containing every graph-relevant admitted `ObjectStreamOccurrenceSetId` entry keyed by containing occurrence, base graph, view basis, and `SecurityContextId` with per-entry availability; `StructuralSignatureSetId`; graph-neutral `GraphHistoryOverlayId`; source coverage; finalization protocol; cards; and semantic limits. Frontier membership is produced by the exact discovery/recovery protocol and records all admitted alternatives; no caller/task-selected basis or subset is an identity input.
- Preconditions: every supplied overlay is source/base-graph consistent and immutable; the declared basis/security-context frontier is complete for its protocol/limits/coverage and includes every admitted alternative; collection order cannot change its canonical root. A missing decision-critical set or incomplete frontier yields partial/refused finalization rather than an invented empty set, and transformation intent is rejected from graph identity.
- Card slots: `SC.C1.REV.FINAL-GRAPH.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: overlay nodes/edges, member occurrences, signature relations, interval links, canonicalization/symmetry work, diagnostics, and output bytes are bounded.
- Cancellation: finalization is transactional; a cancelled canonicalization publishes neither a `RevisionGraphId` nor a misleading current-graph alias.
- Authority and secrets: finalization is read-only; protected object/member/signature locations retain source and plaintext disclosure policy.
- Outputs and outcomes: emits immutable full `RevisionGraphId`, exact base/frontier/overlay roots, coverage, every frontier graph alternative, history anchors, supersession links, and typed partial/refused/cancelled states.
- Diagnostics: overlay/base mismatch, duplicate/missing container key, stale member/security context, incomplete or task-filtered frontier, selected-basis contamination, transformation-intent contamination, missing signature state, uncovered fact, noncanonical symmetry, source change, and finalization limit remain distinct.
- Evidence and provenance: the final graph binds source root, base graph, closed frontier, every overlay/availability class, parser/recovery/security/filter/card protocols, limits, and superseded graph IDs; task-local selection remains downstream in `DocumentViewId`.
- Determinism and replay: D0 for identical base/overlays/protocol/cards/semantic limits; concurrency and overlay arrival order cannot affect the final root.
- Falsifiers and Gauntlet: stale or cross-base overlays, two or more basis-qualified container sets, duplicate container keys, reordered members/sets/signatures, omitted or task-filtered basis, intent-only preservation change, omitted unexplained interval, partial availability, source change, cancellation, and old-graph stability.
- Surfaces: final document views, ordinary resolver, recovery, Open/Recovery reports, CLI revisions/objects, caches, evidence package, and C1 gates.
- Dependencies and consumers: depends on REV.004, REV.006, REV.008, and BYT.005; DOC.001/DOC.002, REC, RPT, CLI, and final-graph consumers use it.
- Migration and withdrawal: changed base or overlay protocol creates a new `RevisionGraphId`; older base/final graphs and overlays remain immutable, linked, and independently inspectable.
- No-claim boundary: final graph history does not select a document view or task, import carry/drop intent, prove conformance, verify a signature, or erase alternative base/final graph versions.
- Rationale: explicit frontier finalization satisfies the full graph record without forcing a base graph, signature analyzer, or preservation overlay to consume its own later output or letting one selected interpretation rename history.

### 8.5 Lossless-filter and decoded-container contracts

#### `C1.CC.FLT.001@1` — Declared filter-chain planning

- Identity, lifecycle, layer: active C1 L1 contract; the planner owns exact declared-order stage semantics while decoder implementations own only their injected stage protocol.
- Inputs and identity domain: raw stream dictionary; distinct duplicate-preserving occurrences and admitted shapes for `/Filter`, `/DecodeParms`, `/F`, `/FFilter`, and `/FDecodeParms`; raw `/DL`; object/security context; requested decoded scope; and cards.
- Preconditions: dictionary occurrences are preserved; strict versus recovered shape interpretation is explicit; every requested stage has an active contract and reviewed card slot.
- Card slots: `SC.C1.FLT.CHAIN-SHAPE.001`, `SC.C1.FLT.DECODE-PARAMS.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: stages, parameters, input/output bytes, cumulative/per-stage expansion ratio, nesting, diagnostics, and planner work are bounded.
- Cancellation: planner and each stage checkpoint; cancellation aborts the private chain transaction and reports the last reconciled stage.
- Authority and secrets: no external file is fetched; optional resolution requires a separate explicit source capability not admitted by default in C1.
- Outputs and outcomes: emits normalized internal and inert external-chain records with exact declared order, aligned parameters, stage applicability, raw `/DL` advisory/plausibility evidence, transaction policy, or strict/recovered refusal. No external chain is executed without a separate admitted source capability.
- Diagnostics: internal/external filter/decode-parameter shape mismatch, unknown/unsupported stage, invalid parameters, forbidden reordering, invalid `/DL` hint, external source unavailable, and policy block.
- Evidence and provenance: plan receipt binds stream object/version, source/view/security context, every raw entry occurrence, cards, stage contracts, and limits.
- Determinism and replay: D0 under the same stream occurrence, context, cards, stage versions, and semantic limits.
- Falsifiers and Gauntlet: internal and external name/array/null parameter shapes, duplicate dictionary keys, odd declared chains, `/DL` smaller/larger/malformed hints, external-file entries, stage-order permutations, and unsupported stages.
- Surfaces: stream resolver, xref/object stream decode, CLI object inspection, reports, and fuzz target.
- Dependencies and consumers: depends on SYN.006/SYN.007 and FDN.001–FDN.014; FLT.002–FLT.010 consume its plan. A raw Crypt occurrence remains an inert stage descriptor until FLT.009 injects ratified SEC.008 context.
- Migration and withdrawal: new stage or shape behavior versions the planner/card set; no decoder presence silently widens the capability manifest.
- No-claim boundary: a valid plan does not assert that stages will finish, output is semantically usable, or an external file was inspected.
- Rationale: central planning prevents decoders from reordering chains, inventing parameters, or hiding cyclic security/object dependencies.

#### `C1.CC.FLT.002@1` — Transactional decoded-stage publication

- Identity, lifecycle, layer: active C1 L1 contract; every decode stage writes to one private non-clonable transaction with explicit terminal state.
- Inputs and identity domain: normalized stage plan, immutable stage source identity able to open independent inspection and decode cursors, private sink, expected output hint, stage decoder, and `WorkContext`.
- Preconditions: inspection and decode each open an independent cursor over the same immutable stage identity and never share rewindable ambient state; each cursor returns either a nonempty chunk no larger than the requested maximum or explicit end, zero-length non-end progress is forbidden, `consumed()` is monotone and checked, and borrowed chunk bytes cannot outlive the documented cursor-call lifetime. The sink is private and output/expansion reservations succeed before large writes.
- Card slots: `SC.C1.FLT.TRANSACTIONAL-DECODE.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: consumed/produced bytes, expansion ratio, chunks, allocations, private spool, diagnostics, and commit work are charged cumulatively.
- Cancellation: decoder observes bounded checkpoints; cancellation consumes abort when private, or reports indeterminate/visible state if commit status cannot be proved. Dropping an unterminated transaction prevents normal publication, permanently poisons that transaction identity, and performs only the bounded synchronous cleanup the implementation can honestly report.
- Authority and secrets: write transaction grants only the selected private sink; sensitivity is inherited and publication to shared cache requires a separate committed stage identity.
- Outputs and outcomes: committed decode receipt, aborted receipt, refused/error outcome, or indeterminate commit state; half-output is never an ordinary decoded artifact.
- Diagnostics: cursor alias/rewind attempt, zero/oversized chunk, nonmonotone consumption, short/overlong output, ratio/byte limit, decoder failure, downstream refusal with exact stage and virtual decoded offset, poisoned drop, abort cleanup state, and commit ambiguity.
- Evidence and provenance: receipt binds input/stage/output identities, bytes consumed/produced, exact virtual decoded failure offset where applicable, parameters, limits, cancellation, and terminal publication state.
- Determinism and replay: decoded bytes target D0 under exact stage inputs; chunk sizes and pipe scheduling cannot change output.
- Falsifiers and Gauntlet: independent inspect/decode cursor interference, oversized/empty chunks, nonmonotone consumption, borrow escape, cancellation/panic at every boundary, sink short write, commit failure, dropped/abandoned transaction poisoning, decoded-offset localization, diagnostic flood, and partial cache visibility.
- Surfaces: every filter, xref/object stream decode, decoded-container cache, reports, and fuzz harness.
- Dependencies and consumers: depends on FLT.001, FDN.004–FDN.013, and BYT.004; FLT.003–FLT.010 and REV.002/REV.006 consume it.
- Migration and withdrawal: terminal-state semantics cannot change without a new contract; old ambiguous commits remain ambiguous rather than being repaired by assumption.
- No-claim boundary: abort or drop reconciliation reports observable cleanup only; `Drop` never promises async deletion, durable erasure, or diagnostic callback delivery for private bytes or untracked dependency buffers.
- Rationale: transactional publication makes failure, cancellation, and cache visibility composable across filter chains.

#### `C1.CC.FLT.003@1` — ASCIIHex decode

- Identity, lifecycle, layer: active C1 L1 atomic decoder contract for the named lossless stage.
- Inputs and identity domain: immutable stage cursor, normalized parameters, strict/recovery policy, source/virtual provenance, and semantic limits.
- Preconditions: `SC.C1.FLT.ASCIIHEX.001` has later two-person meaning review; FLT.001 admits the stage and FLT.002 owns output transaction.
- Card slots: `SC.C1.FLT.ASCIIHEX.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: input bytes, output bytes, expansion ratio, ignored lexical material admitted by cards, diagnostics, and chunks are bounded.
- Cancellation: checkpoints by bounded input units; cancellation aborts the private transaction.
- Authority and secrets: byte-only decoder has no host capabilities and inherits sensitivity from the stream.
- Outputs and outcomes: deterministic decoded bytes plus consumed/produced counts and termination/truncation status, or typed refusal/error.
- Diagnostics: malformed symbol, termination issue, truncation, trailing data policy, output limit, and missing input range use stable codes.
- Evidence and provenance: output links stage plan, exact input spans/container, decoder version, cards, and transaction receipt.
- Determinism and replay: D0 for exact input, cards, profile, decoder version, and semantic limits.
- Falsifiers and Gauntlet: atomic positive/negative fixtures after card admission, rights-admitted generic/analytic vectors or a separately implemented project oracle with recorded lineage, chunk-boundary metamorphism, truncation, output limits, cancellation, and arbitrary-byte fuzzing.
- Surfaces: stream decode, object inspection, xref/object stream only where permitted, capability manifest, and fuzz target.
- Dependencies and consumers: depends on FLT.001/FLT.002, FDN.001–FDN.014, and BYT.004 provenance; FLT.010 and stream consumers use its committed output.
- Migration and withdrawal: semantic/card change versions the decoder contract; unsupported forms refuse rather than enter compatibility folklore.
- No-claim boundary: decoder success establishes stage-byte transformation only, not stream semantic validity or text meaning.
- Rationale: one atomic contract keeps malformed termination and output-limit behavior consistent across every surface.

#### `C1.CC.FLT.004@1` — ASCII85 decode

- Identity, lifecycle, layer: active C1 L1 atomic decoder contract for the named lossless stage.
- Inputs and identity domain: immutable stage cursor, normalized parameters, strict/recovery policy, provenance, and semantic limits.
- Preconditions: the later reviewed `SC.C1.FLT.ASCII85.001` is active; planner and transaction contracts admit the stage.
- Card slots: `SC.C1.FLT.ASCII85.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: input/output bytes, expansion ratio, group state, diagnostics, and chunks are bounded with checked arithmetic.
- Cancellation: checkpoints between bounded groups/chunks; private output aborts on cancellation.
- Authority and secrets: no host authority; inherited stream sensitivity applies to buffers and witnesses.
- Outputs and outcomes: committed decoded bytes with counts/termination status, or malformed/truncated/resource/refusal outcome.
- Diagnostics: invalid symbol/group, shorthand misuse as defined later by cards, termination/trailing-data issue, overflow, and output limit.
- Evidence and provenance: receipt binds exact input ranges, stage plan, cards, decoder version, and output identity.
- Determinism and replay: D0 under the exact admitted inputs and semantic limits.
- Falsifiers and Gauntlet: card-derived fixtures, rights-admitted generic/analytic vectors or a separately implemented project oracle with recorded lineage, group-boundary chunking, short final groups, malformed symbols, cancellation, output limits, and fuzzing.
- Surfaces: stream decode, object inspection, capability manifest, reports, and fuzz target.
- Dependencies and consumers: depends on FLT.001/FLT.002; FLT.010 and stream consumers use its output.
- Migration and withdrawal: card/profile changes version behavior; recovered variants retain explicit recovered evidence.
- No-claim boundary: decoded bytes do not establish conformance of the enclosing stream or later filter applicability.
- Rationale: stage-specific errors and receipts prevent generic ASCII handling from hiding format distinctions.

#### `C1.CC.FLT.005@1` — RunLength decode

- Identity, lifecycle, layer: active C1 L1 atomic decoder contract for the named lossless stage.
- Inputs and identity domain: immutable stage cursor, normalized parameters, provenance, strict/recovery profile, and limits.
- Preconditions: later reviewed `SC.C1.FLT.RUNLENGTH.001` is active; transactional sink and expansion reservation exist.
- Card slots: `SC.C1.FLT.RUNLENGTH.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: input/output bytes, expansion ratio, run length arithmetic, chunks, and diagnostics are bounded before emission.
- Cancellation: checkpoints between runs and bounded output chunks; cancellation cannot expose a partial run.
- Authority and secrets: no host capability; output sensitivity inherits the stream.
- Outputs and outcomes: committed decoded bytes and explicit end/truncation status, or malformed/resource/refusal result.
- Diagnostics: invalid/truncated run, missing terminator as later defined, arithmetic overflow, ratio/byte limit, and trailing-data policy.
- Evidence and provenance: output receipt binds run decoder version, exact input provenance, cards, counts, and transaction state.
- Determinism and replay: D0 under exact inputs, profile, cards, and semantic limits.
- Falsifiers and Gauntlet: rights-admitted generic/analytic vectors or a separately implemented project oracle with recorded lineage, maximal runs, boundary arithmetic, truncated literal/repeat runs, chunk splits, bombs, cancellation, and arbitrary-byte fuzzing.
- Surfaces: stream decode, object inspection, capability manifest, reports, and fuzz target.
- Dependencies and consumers: depends on FLT.001/FLT.002; FLT.010 and document consumers use output.
- Migration and withdrawal: semantic/card changes create a new decoder version; unsafe expansion behavior withdraws the stage from active manifest.
- No-claim boundary: bounded decode does not claim an unbounded input is safe or the stream’s declared decoded length is accurate.
- Rationale: pre-reserved run expansion closes a direct amplification path before bytes reach downstream parsers.

#### `C1.CC.FLT.006@1` — Flate decode

- Identity, lifecycle, layer: active C1 L1 atomic decoder adapter contract for Flate stage bytes; generic primitive choice remains decision/dependency-reviewed.
- Inputs and identity domain: immutable stage cursor, normalized parameters, strict/recovery policy, decoder dependency identity, provenance, and limits.
- Preconditions: later reviewed `SC.C1.FLT.FLATE.001` is active; dependency source/license/AI-use/provenance is admitted; FLT.002 owns output.
- Card slots: `SC.C1.FLT.FLATE.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: compressed/output bytes, expansion ratio, internal window/state cap, chunks, CPU quanta, diagnostics, and output transaction are bounded.
- Cancellation: adapter checkpoints around bounded primitive calls/chunks; an uncooperative dependency is isolated or the profile refuses.
- Authority and secrets: no host authority; dependency receives only stage bytes and private sink, with sensitivity retained.
- Outputs and outcomes: committed decoded bytes, exact consumed/produced counts, stream-end/trailing/truncation status, or typed dependency/resource/refusal outcome.
- Diagnostics: malformed stream, dictionary requirement if applicable, truncation, trailing bytes policy, dependency panic/limit, and output bomb.
- Evidence and provenance: receipt binds dependency artifact/version, adapter protocol, cards, input/source context, output identity, and limits.
- Determinism and replay: D0 under pinned dependency, exact inputs, cards, profile, and semantic limits.
- Falsifiers and Gauntlet: project-generated/card-derived vectors, mutation, expansion bombs, chunk boundaries, dependency panic containment, cancellation, and cross-path reference checks after admission.
- Surfaces: stream/xref/object-stream decode, object inspection, capability manifest, reports, and fuzz target.
- Dependencies and consumers: depends on FLT.001/FLT.002 and ratified license/toolchain decisions; FLT.007/FLT.010 and revision/document consumers use output.
- Migration and withdrawal: dependency or adapter change versions the derivation; a security advisory may withdraw the active stage/profile without rewriting prior receipts.
- No-claim boundary: memory-safe dependency selection does not prove freedom from hangs, panics, logic defects, or side channels.
- Rationale: a narrow PDF-owned adapter preserves budget, provenance, and error semantics while allowing a reviewed generic primitive.

#### `C1.CC.FLT.007@1` — TIFF/PNG predictor postprocessing

- Identity, lifecycle, layer: active C1 L1 atomic post-filter contract; predictor work is a declared stage consequence, not an implicit decoder option.
- Inputs and identity domain: committed decoded bytes from an admitted preceding stage, normalized predictor parameters, row/sample geometry, cards, and limits.
- Preconditions: later reviewed predictor slots are active; all dimension arithmetic is checked before row allocation or output.
- Card slots: `SC.C1.FLT.PREDICTOR-TIFF.001`, `SC.C1.FLT.PREDICTOR-PNG.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: rows, columns, colors, bits/components as card-defined later, input/output bytes, scratch bytes, expansion, and diagnostics are bounded.
- Cancellation: checkpoints between bounded rows/chunks; partial postprocessed output stays private.
- Authority and secrets: no host capability; inherited sensitivity and transaction policy apply.
- Outputs and outcomes: committed postprocessed bytes plus geometry/count receipt, or invalid-parameter, length, arithmetic, resource, or refusal outcome.
- Diagnostics: unsupported predictor, impossible geometry, row-length mismatch, truncated row, overflow, and output limit.
- Evidence and provenance: receipt links predicted output → preceding stage identity → source stream and exact parameter occurrences.
- Determinism and replay: D0 under exact bytes, parameters, cards, algorithm version, and semantic limits.
- Falsifiers and Gauntlet: row boundaries, extreme dimensions, malformed parameters, short/extra rows, chunk splits, bombs, cancellation, and reference properties.
- Surfaces: stream decode, object inspection, capability manifest, reports, and fuzz target.
- Dependencies and consumers: depends on FLT.001/FLT.002 and typically FLT.006 or FLT.008 as declared; FLT.010 and stream consumers use output.
- Migration and withdrawal: predictor/card changes version the stage; unsupported combinations refuse rather than use library defaults.
- No-claim boundary: correct predictor bytes do not determine image color/sample meaning or authorize rendering.
- Rationale: explicit postprocessing prevents unchecked dimension multiplication and hidden behavior inside Flate/LZW adapters.

#### `C1.CC.FLT.008@1` — LZW decode with admitted `EarlyChange` handling

- Identity, lifecycle, layer: active C1 L1 atomic decoder contract for LZW stage bytes and explicit parameter identity.
- Inputs and identity domain: immutable stage cursor, normalized `EarlyChange` occurrence/value, strict/recovery profile, provenance, and limits.
- Preconditions: later reviewed `SC.C1.FLT.LZW.001` is active; parameter selection is explicit; transactional sink exists.
- Card slots: `SC.C1.FLT.LZW.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: input/output bytes, expansion ratio, dictionary entries/state, code width, chunks, CPU quanta, and diagnostics are bounded.
- Cancellation: checkpoints by bounded code/chunk units; dictionary state and partial output remain private on stop.
- Authority and secrets: no host capability; output sensitivity inherits the stream.
- Outputs and outcomes: committed decoded bytes, consumed/produced counts, parameter receipt, and end/truncation state, or typed malformed/resource/refusal result.
- Diagnostics: invalid code/state, dictionary limit, parameter issue, premature end, output bomb, and trailing-data policy.
- Evidence and provenance: receipt binds exact raw parameter occurrence, decoder/cards, source context, limits, and output identity.
- Determinism and replay: D0 under exact input, parameter, cards, version, and semantic limits.
- Falsifiers and Gauntlet: rights-admitted generic/analytic vectors or a separately implemented project oracle with recorded lineage, dictionary reset/growth boundaries as later card-derived, both admitted parameter cases, malformed codes, bombs, cancellation, chunking, and fuzzing.
- Surfaces: stream/object-stream decode, object inspection, capability manifest, reports, and fuzz target.
- Dependencies and consumers: depends on FLT.001/FLT.002; FLT.007/FLT.010 and document consumers use output.
- Migration and withdrawal: card or algorithm changes version the contract; missing/ambiguous parameter remains explicit rather than silently defaulted from model memory.
- No-claim boundary: LZW decode presence does not imply writer-side encoding support or target-profile permission.
- Rationale: parameter identity must be retained because a friendly “LZW supported” label is too coarse for reproducible bytes.

#### `C1.CC.FLT.009@1` — Explicit Crypt/Identity stage routing

- Identity, lifecycle, layer: active C1 L1 boundary contract; it routes an already admitted security context into a declared Crypt or Identity stage without owning key semantics.
- Inputs and identity domain: normalized filter stage, raw `/Name` occurrence, object/version/revision context, security-handler selection, credential capability identity, and cards.
- Preconditions: SEC.001–SEC.008 admit the exact context; xref/object non-encryption rules and stage applicability have later reviewed cards.
- Card slots: `SC.C1.FLT.CRYPT-STAGE.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: routing/lookup work, input/output bytes, cryptographic operations, diagnostics, and security-context manifest are bounded.
- Cancellation: checks occur before key use and between bounded cryptographic chunks; secret state is reconciled under SEC.009.
- Authority and secrets: planner injects a narrow decrypt capability; filter code cannot discover credentials, keys, host keychains, or unrelated security state.
- Outputs and outcomes: selects Identity or one admitted crypt-filter context and returns stage receipt, or unsupported/missing-credential/policy/refusal outcome.
- Diagnostics: unknown filter name, missing handler, denied credential, scope mismatch, forbidden target structure, and unsupported algorithm remain secret-safe.
- Evidence and provenance: receipt binds raw filter occurrence, object/security context, handler/profile/card IDs, and non-secret credential capability identity.
- Determinism and replay: plaintext bytes are D0 when required secret input is available under the same context; public replay may be partial when secrets are unavailable.
- Falsifiers and Gauntlet: explicit Identity, unknown names, object/revision mismatches, missing credentials, wrong scope, double-decrypt attempt, and cross-tenant isolation.
- Surfaces: stream planner, object/string resolution, object-stream decode, reports, and fuzz target.
- Dependencies and consumers: depends on FLT.001/FLT.002 and SEC.001–SEC.009; FLT.010 and stream consumers use output.
- Migration and withdrawal: new crypt-filter semantics receive new security contracts/cards; this router remains a narrow dispatch boundary.
- No-claim boundary: routing does not prove password correctness, algorithm security, permissions, or that every document payload is encrypted.
- Rationale: injected routing keeps filter and security ownership acyclic and makes explicit Crypt/Identity choices auditable.

#### `C1.CC.FLT.010@1` — Decoded-container identity and virtual spans

- Identity, lifecycle, layer: active C1 L1 contract; one decoded container is qualified by source object/version, security/filter chain, algorithms, parameters, and availability.
- Inputs and identity domain: one immutable `PlannedRecipe` containing the source/object/version/span, explicit `SecurityContextId`, normalized chain and parameter identities, decoder versions, semantic limits, and ratified D3 policy; plus, only after execution, a separately linked `MaterializationRecord` containing transaction commit state, ordered stage receipts, availability, and outcome-required `DecodedArtifactDigest`.
- Preconditions: D3 and its D1/D2 dependencies are ratified; only `PlannedRecipe` fields mint the sole pre-decode `DecodedContainerId`; materialization fields are forbidden before execution and never change that ID. A durable/cached/evidence-referenced Materialized outcome requires commit plus digest, an operation-local transient Materialized outcome requires commit and explicitly forbids durable reuse, and Refused carries no materialized bytes. **PROPOSED default — awaiting ratification (D3):** one pre-decode recipe `DecodedContainerId` plus a distinct post-commit `DecodedArtifactDigest`.
- Card slots: `SC.C1.FLT.DECODED-CONTAINER.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: identity computation, retained output, virtual spans, cache insertion, recomputation, and provenance metadata are bounded.
- Cancellation: cancelled identity/materialization cannot publish a durable container; committed bytes may remain private with explicit availability.
- Authority and secrets: container and cache keys include non-secret credential/security/tenant context and sensitivity partition without exposing credential material.
- Outputs and outcomes: produces exactly one typed state: `Planned` with recipe identity and no content claim; `Materialized` with verified `DecodedArtifactDigest`; transient `Materialized` with digest not computed and therefore operation-local only; or `Refused` with cause. Successful committed materialization may additionally expose bounded virtual spans and stage provenance.
- Diagnostics: unratified policy, planned/materialized grammar violation, receipt-before-commit, required/forbidden digest mismatch, unavailable bytes, identity budget, security-context mismatch, stage inconsistency, cache denial, and collision quarantine.
- Evidence and provenance: every virtual span links decoded offset/length to container, chain receipts, enclosing source object/span, and limits.
- Determinism and replay: recipe identity targets D0 under exact proper-domain inputs, chain versions, security context, and semantic limits. A retained, cached, or evidence-referenced artifact computes its digest incrementally during decode and verifies it on reuse; a transient no-digest artifact cannot support durable reuse or byte-exactness.
- Falsifiers and Gauntlet: same bytes/different context, different bytes/same injected digest, deferred identity, virtual-span bounds, eviction/recompute, and credential crossing.
- Surfaces: object-stream members, decoded stream inspection, reports, caches, checker, and fuzz witness serialization.
- Dependencies and consumers: depends on FLT.001–FLT.009, FDN.001–FDN.014, SEC.001/SEC.008, and conditionally SEC.009 for decrypted material; REV.006/DOC.001/RPT.001–RPT.003/RPT.007/RPT.009 consume it. REV.002 uses only FLT.002 bootstrap-stage provenance and is not a decoded-container consumer.
- Migration and withdrawal: D3 remains a proposal until human ratification. A later decoded-identity cost/grammar change versions the container protocol and invalidates incompatible cache reuse.
- No-claim boundary: container identity does not claim unique inverse source-byte attribution, semantic validity, or public availability of plaintext.
- Rationale: metadata-only recipe naming preserves laziness and bounds reference cost, while the post-commit digest tests the bytes before durable reuse. `DecodedContainerId` is the sole class; the alternative spelling is only the D-004 higher-layer drift label.

### 8.6 Encryption-inventory and credentialed-read contracts

#### `C1.CC.SEC.001@1` — Encryption dictionary and scope inventory

- Identity, lifecycle, layer: active C1 L1/L2 contract; inventory records declared security structure before any credential or decryption attempt.
- Inputs and identity domain: `BaseRevisionGraphId`, `DocumentViewBasisId`, DOC.011 bootstrap resolution set, trailer/catalog reference locators, raw encryption dictionaries including distinct `/P`, `/Perms`, and `/EncryptMetadata` occurrences, crypt-filter dictionaries, public-key recipient and declared-algorithm carriers, metadata/embedded-file indicators, registered core-versus-technical-specification profile class, and cards.
- Preconditions: raw values and pre-view object occurrences are available; final `DocumentViewId` is not required; no dictionary field is filled from memory when a card is absent.
- Card slots: `SC.C1.SEC.ENCRYPTION-INVENTORY.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: dictionaries, entries, reference depth, crypt-filter records, revision contexts, diagnostics, and alternatives are bounded.
- Cancellation: inventory returns exact observed scope and cannot claim unencrypted absence outside it.
- Authority and secrets: no credential is required; inventory has read-only access and emits no keys/password-derived values.
- Outputs and outcomes: emits one non-secret `SecurityContextId` with unencrypted/Identity, declared-handler, unsupported, ambiguous, or unavailable state; records declared handler, `/V`/`/R`/length, duplicate-preserved raw `/P`, `/Perms`, `/EncryptMetadata`, public-key recipient/crypt-filter/declared-algorithm carriers, and related entries as raw/validated fields; and preserves crypt-filter defaults, metadata/file scope, an unverified/pending core-versus-technical-specification profile classification, unsupported profiles, and ambiguity. Credential-free states contain no handler key or credential claim.
- Diagnostics: missing/invalid/conflicting entries, unsupported matrix row, unverified or unknown technical-specification profile, unresolved public-key carrier, unresolved reference, revision inconsistency, and partial source.
- Evidence and provenance: every field links exact dictionary occurrence, base graph/view basis, cards, strict/recovered-basis status, and coverage.
- Determinism and replay: D0 under the same source/base graph/view basis, cards, and limits.
- Falsifiers and Gauntlet: absent encryption dictionary, Identity routing, duplicate keys including `/EncryptMetadata`, conflicting revisions, missing entries, distinct `/P`/`/Perms` mutations, raw public-key recipient/algorithm carriers without CMS parsing, core/technical-specification classification, unknown filters, malformed values, partial source, and inventory-without-credential tests.
- Surfaces: OpenReport, security report, CLI inspect/objects, decryption admission, capability manifest, and fuzz target.
- Dependencies and consumers: depends on SYN.004–SYN.006, REV.004/REV.005, DOC.010, and DOC.011 bootstrap records; SEC.002–SEC.009, REV.006, DOC.002/DOC.001, and RPT consume it.
- Migration and withdrawal: new handler/profile cards version inventory interpretation; raw evidence remains source-bound.
- No-claim boundary: a declared encryption dictionary, public-key carrier, or technical-specification label does not prove every payload is encrypted, confidentiality is strong, a CMS envelope is parsed, a technical-specification behavior is implemented, credentials are correct, or permissions are authorization.
- Rationale: credential-free structural inventory provides R0 value and separates “what the file declares” from successful decryption.

#### `C1.CC.SEC.002@1` — Credential capability admission

- Identity, lifecycle, layer: active C1 L0/L1 boundary contract; credentials are supplied through a narrow operation capability, never ambient state.
- Inputs and identity domain: explicit byte-password or text-password request, credential role intent naming the owner-role or user-role class without assigning its pending semantics, caller/tenant identity, secret policy, target source/view-basis or finalized-view security context, and provider capability.
- Preconditions: caller is authorized for the target operation; input form is explicit; CLI and API avoid platform-default encoding.
- Card slots: `SC.C1.SEC.CREDENTIAL-ADMISSION.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: credential attempts, preparation bytes, KDF/validation work, memory, diagnostics, and retry count are bounded.
- Cancellation: checks occur before secret import and between bounded preparation/validation units; secret buffers follow reconciliation policy.
- Authority and secrets: lease is non-copyable/narrowable, scoped to one source/view/security context and operation; no export, logging, caching, environment discovery, or host keychain search.
- Outputs and outcomes: yields an opaque owner-role or user-role credential-use lease and non-secret admission receipt, or denied/malformed/exhausted/cancelled outcome; role meaning and validation remain unavailable until the relevant cards activate.
- Diagnostics: secret-safe codes distinguish input-form error, denied capability, attempt limit, unsupported profile, and generic credential rejection policy.
- Evidence and provenance: receipt binds provider/capability identity, target context, input form, attempt number, and policy—never password or derived key.
- Determinism and replay: semantic decryption can be D0 when the secret is re-supplied; public replay may be identity-only/unavailable.
- Falsifiers and Gauntlet: capability forgery, cross-source/view reuse, byte/text confusion, environment/argv leak, logging scans, attempt floods, and cancellation.
- Surfaces: Rust API, CLI secure input, strict/recovery open with credentials, and fuzz harness using synthetic non-secret fixtures.
- Dependencies and consumers: depends on FDN.004–FDN.008 and SEC.001; SEC.003–SEC.009 consume it.
- Migration and withdrawal: provider/input schema changes version the lease; old receipts cannot authorize a new operation.
- No-claim boundary: admission proves caller authorization under one policy, not credential correctness, the semantic consequences of an owner/user role, ownership, legal access, or side-channel immunity.
- Rationale: capability-scoped credentials prevent library-global passwords and cross-tenant plaintext reuse.

#### `C1.CC.SEC.003@1` — Version-specific password preparation and validation

- Identity, lifecycle, layer: active C1 L1 atomic security contract; each admitted handler revision has a distinct preparation/validation profile.
- Inputs and identity domain: opaque credential lease, explicit byte/text form, SEC.001 matrix row, exact encryption dictionary/object values, source/view/revision context, and cards.
- Preconditions: later reviewed version/profile cards and approved generic crypto vectors exist; unsupported rows refuse.
- Card slots: `SC.C1.SEC.PASSWORD-PREP.001`, `SC.C1.SEC.PASSWORD-VALIDATE.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: input length, normalization/preparation work, validation attempts, cryptographic operations, memory, and diagnostics are bounded.
- Cancellation: checkpoints occur around bounded cryptographic units; cancellation produces no reusable partial key.
- Authority and secrets: password and intermediate values stay inside the secret boundary, use vetted constant-time primitives where available, and are never returned or logged.
- Outputs and outcomes: returns an opaque validated owner-role or user-role context and key-derivation input only under active cards, wrong/indeterminate credential, unsupported profile, or policy refusal.
- Diagnostics: externally visible failures avoid needless distinctions; protected traces may separate internal causes only under explicit authority.
- Evidence and provenance: non-secret receipt binds profile/cards, dictionary context, attempt, primitive identities, and terminal status without secret values.
- Determinism and replay: deterministic under exact secret/context/profile; replay requires re-supplying the secret and cannot be reconstructed from the receipt.
- Falsifiers and Gauntlet: approved vectors after rights admission, boundary lengths, byte/text cases, wrong credentials, attempt caps, timing-shape checks within stated threat model, and fuzzing.
- Surfaces: decryption admission, OpenReport status, CLI credential flow, and synthetic fuzz harness.
- Dependencies and consumers: depends on SEC.001/SEC.002, FDN.001–FDN.015, and ratified toolchain/license; SEC.004–SEC.009 consume opaque output.
- Migration and withdrawal: profile/card/primitive change versions the contract and invalidates cached derived keys.
- No-claim boundary: use of constant-time primitives does not establish whole-process side-channel resistance across allocator, cache, scheduler, OS, hardware, or provider.
- Rationale: explicit version profiles prevent one Unicode/platform convention from silently governing incompatible historical handler revisions.

#### `C1.CC.SEC.004@1` — Standard-handler matrix and key derivation

- Identity, lifecycle, layer: active C1 L1 atomic security contract; it selects only a later card-admitted `/V` and `/R` matrix row and derives opaque read keys.
- Inputs and identity domain: SEC.001 inventory, SEC.003 validated role/context, exact trailer ID/revision facts where applicable, object/version context, crypt-filter selection, raw `/Perms` occurrence where applicable, and cards.
- Preconditions: matrix row, required entries, key lengths, algorithms, and deprecated-read policy are later rights-reviewed; no output-writing policy is admitted.
- Card slots: `SC.C1.SEC.STANDARD-HANDLER-MATRIX.001`, `SC.C1.SEC.KEY-DERIVATION.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: derivation operations, object-key derivations, key bytes/lifetime, attempts, diagnostics, and per-operation object count are bounded.
- Cancellation: key derivation checks cancellation at bounded units; cancelled/intermediate keys are not cached or returned.
- Authority and secrets: keys remain opaque secret handles scoped to source/view/revision/object/security context and credential lease.
- Outputs and outcomes: emits admitted handler context plus opaque file/object read-key capability and a separate typed `/Perms` validation outcome of valid, invalid, not-applicable, unsupported, or unavailable; or emits unsupported/malformed/wrong-credential/policy outcome. `/P` interpretation remains a distinct non-authorization observation.
- Diagnostics: distinguish unsupported matrix internally while keeping external credential rejection policy; no key material or password-dependent bytes appear.
- Evidence and provenance: non-secret receipt binds cards, raw dictionary occurrences, source/view/revision, role class, primitive versions, and scope.
- Determinism and replay: deterministic under exact secret and context; receipt alone cannot reproduce plaintext.
- Falsifiers and Gauntlet: approved vectors, wrong trailer ID/context, object-generation boundaries, duplicate dictionaries, valid/invalid/unavailable `/Perms` distinct from `/P`, unsupported rows, key-lifetime, and cross-revision tests.
- Surfaces: RC4/AES read decoders, Crypt routing, object/string/stream resolution, OpenReport, and fuzz target.
- Dependencies and consumers: depends on SEC.001–SEC.003, REV.004/REV.005 object context, and FDN.001–FDN.015; SEC.005–SEC.009 consume it.
- Migration and withdrawal: a changed matrix/card/primitive versions handler context; deprecated read support can be withdrawn by profile without enabling writer emission.
- No-claim boundary: derived read keys do not imply cryptographic strength, permission enforcement, write encryption, public-key support, or key export.
- Rationale: one explicit matrix prevents handler selection and object-key context from scattering across parsers and filters.

#### `C1.CC.SEC.005@1` — RC4 read decryption

- Identity, lifecycle, layer: active C1 L1 atomic legacy-read contract; RC4 is admitted only for later card-reviewed compatibility rows.
- Inputs and identity domain: encrypted stage/string bytes, opaque key capability from SEC.004, exact object/version/revision/crypt-filter context, and limits.
- Preconditions: selected matrix row explicitly admits RC4 read behavior; primitive dependency is rights/provenance reviewed; output emission is not admitted.
- Card slots: `SC.C1.SEC.RC4-READ.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: input/output bytes, key use, chunks, CPU quanta, plaintext memory, diagnostics, and attempt count are bounded.
- Cancellation: checkpoints by bounded chunks; plaintext transaction aborts and SEC.009 reconciles remnants.
- Authority and secrets: opaque key cannot be exported; decoder has no host capabilities; plaintext is sensitivity-partitioned.
- Outputs and outcomes: committed plaintext bytes and secret-safe receipt, or malformed/context/resource/cancelled/refused outcome.
- Diagnostics: context/key/profile mismatch, primitive failure, output limit, and cancellation are redacted; plaintext is never embedded.
- Evidence and provenance: plaintext links encrypted source span, security context, algorithm/profile/cards, object identity, and transaction receipt.
- Determinism and replay: D0 when secret/context is available; public packages may carry identity-only or unavailable plaintext.
- Falsifiers and Gauntlet: approved vectors, chunk boundaries, wrong object/context/key, empty/large inputs, cancellation, cache isolation, and primitive fault containment.
- Surfaces: string/stream/object-stream read path, OpenReport status, CLI credentialed inspection, and fuzz target.
- Dependencies and consumers: depends on SEC.004/SEC.008/SEC.009 and FLT.002; DOC.001 and decoded-container contracts consume output.
- Migration and withdrawal: security policy may disable legacy read profiles; old receipts remain labeled legacy compatibility and never authorize emission.
- No-claim boundary: compatibility read support does not endorse RC4 security, writer use, permissions, or whole-process side-channel resistance.
- Rationale: isolating legacy read behavior prevents an R0 requirement from leaking into default output policy.

#### `C1.CC.SEC.006@1` — AESV2 read decryption

- Identity, lifecycle, layer: active C1 L1 atomic AESV2 read contract under exact handler/crypt-filter context.
- Inputs and identity domain: encrypted bytes, opaque key capability, object/version/revision context, crypt-filter selection, primitive dependency identity, cards, and limits.
- Preconditions: later reviewed matrix/algorithm cards admit AESV2; input framing/context is validated before plaintext publication.
- Card slots: `SC.C1.SEC.AESV2-READ.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: input/output bytes, block/framing work, plaintext memory, CPU quanta, diagnostics, and attempts are bounded.
- Cancellation: checks before key use and between bounded chunks; private plaintext aborts on stop.
- Authority and secrets: key and plaintext remain opaque/protected; no entropy, writer, signer, network, or trust capability is present.
- Outputs and outcomes: committed plaintext with non-secret algorithm/context receipt, or malformed/context/resource/cancelled/refused result.
- Diagnostics: invalid framing/length as later card-defined, context mismatch, primitive failure, output limit, and cancellation are secret-safe.
- Evidence and provenance: output binds exact ciphertext span/container, object context, handler/filter/cards, primitive identity, and transaction state.
- Determinism and replay: D0 when secret/context is supplied; no public plaintext commitment when disclosure policy forbids it.
- Falsifiers and Gauntlet: approved vectors, malformed framing, wrong object/context/key, chunking, cancellation, cache partition, and fault injection.
- Surfaces: string/stream/object-stream read path, OpenReport, credentialed CLI, and fuzz target.
- Dependencies and consumers: depends on SEC.004/SEC.008/SEC.009 and FLT.002; DOC.001/FLT.010 consume output.
- Migration and withdrawal: primitive/card/policy changes version this read profile; output-writing support remains separate.
- No-claim boundary: successful plaintext recovery does not prove document confidentiality, credential ownership, permission authorization, or integrity.
- Rationale: atomic algorithm contracts keep exact context, evidence, and refusal semantics visible instead of hiding them behind “decrypt.”

#### `C1.CC.SEC.007@1` — AESV3 read decryption

- Identity, lifecycle, layer: active C1 L1 atomic AESV3 read contract under exact modern handler/crypt-filter context.
- Inputs and identity domain: encrypted bytes, opaque validated file-key capability, revision/security context, crypt-filter selection, primitive identity, cards, and limits.
- Preconditions: later reviewed matrix/algorithm cards admit AESV3 and preceding credential/key validation finished.
- Card slots: `SC.C1.SEC.AESV3-READ.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: input/output bytes, framing/block work, plaintext memory, CPU quanta, diagnostics, and attempts are bounded.
- Cancellation: checkpoints before sensitive operations and between bounded chunks; private plaintext aborts under SEC.009.
- Authority and secrets: file key and plaintext never leave opaque secret boundaries; no output-encryption or host-service authority is present.
- Outputs and outcomes: committed plaintext and secret-free receipt, or malformed/context/resource/cancelled/refused result.
- Diagnostics: validation/framing/context/primitive failures use redacted codes and do not echo protected values.
- Evidence and provenance: plaintext binds exact ciphertext provenance, handler/filter/cards, revision/view, primitive version, and terminal transaction.
- Determinism and replay: D0 when the same secret/context exists; replay package availability may remain unavailable.
- Falsifiers and Gauntlet: approved vectors, wrong credential/key/context, malformed inputs, chunk boundaries, cancellation, isolation, and dependency fault tests.
- Surfaces: string/stream/object-stream read path, OpenReport, credentialed CLI, and fuzz target.
- Dependencies and consumers: depends on SEC.003/SEC.004/SEC.008/SEC.009 and FLT.002; DOC.001/FLT.010 consume output.
- Migration and withdrawal: algorithm/card/dependency changes version the contract and invalidate derived-key/plaintext caches.
- No-claim boundary: read decryption does not admit AES-GCM extensions, secure encrypted output, public-key decryption handlers, or cryptographic integrity beyond the exact profile.
- Rationale: a separate AESV3 contract prevents modern handler assumptions from contaminating legacy object-key behavior.

#### `C1.CC.SEC.008@1` — Crypt-filter and object/string/stream scope

- Identity, lifecycle, layer: active C1 L1 orchestration contract; it computes one explicit encryption/decryption scope per selected base-revision/view-basis and object occurrence, before final view construction.
- Inputs and identity domain: SEC.001 `SecurityContextId`, optional admitted handler context, duplicate-preserved raw `/StmF`/`/StrF`/`/EFF`/`/EncryptMetadata` and per-stream Crypt/Identity declarations, metadata policy, object category, xref/object-stream rules, and cards.
- Preconditions: raw dictionary occurrences, `BaseRevisionGraphId`, and `DocumentViewBasisId` are exact; final `DocumentViewId` is not an input; all scope rules are later card-reviewed. An unencrypted/Identity context requires no SEC.002–SEC.004 credential/key result.
- Card slots: `SC.C1.SEC.CRYPT-FILTER-SCOPE.001`, `SC.C1.SEC.ENCRYPTED-OBJECT-SCOPE.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: lookup/selection work, filter records, object occurrences, revision contexts, diagnostics, and dependency manifest are bounded.
- Cancellation: scope planning checkpoints before key acquisition; no partially selected context is cached.
- Authority and secrets: planner receives opaque handler/credential identities and returns narrow per-object handles; no key export or host discovery.
- Outputs and outcomes: exact unencrypted/Identity/RC4/AESV2/AESV3/unsupported scope record for each admitted value, with one-time object-stream container rule and metadata/file scope.
- Diagnostics: missing/default conflict, unknown filter, category mismatch, forbidden xref encryption, double-decrypt attempt, unsupported extension, and ambiguity.
- Evidence and provenance: scope record links every duplicate-preserved raw declaration including `/EncryptMetadata`, object/version/base-revision/view-basis, cards, handler contract, selection witnesses, and alternatives; final views bind the scope ID later.
- Determinism and replay: D0 under the same view basis, declarations, cards, capability context, and semantic limits.
- Falsifiers and Gauntlet: default/per-stream conflicts, Identity routing, metadata and embedded-file cases, xref exclusions, object-stream double-decrypt traps, and revision changes.
- Surfaces: filter planner, scalar/object resolution, decoded containers, OpenReport, CLI objects, and fuzz target.
- Dependencies and consumers: depends on SEC.001 and conditionally SEC.002–SEC.004 for declared handlers, REV.004/REV.005, and exact DOC.010/DOC.011 pre-view context; SEC.005–SEC.007/SEC.009, FLT.009, REV.006, and DOC.002 consume it.
- Migration and withdrawal: scope/card changes create new view/derivation identities and invalidate affected plaintext cache entries.
- No-claim boundary: calculated scope reflects admitted declarations and cards; it does not prove ciphertext strength, all-file confidentiality, or host authorization.
- Rationale: central scope selection prevents accidental double decryption and inconsistent treatment of strings, streams, metadata, and embedded files.

#### `C1.CC.SEC.009@1` — Plaintext provenance, cache partitioning, and disposal

- Identity, lifecycle, layer: active C1 L0/L1 cross-cutting contract; decrypted artifacts remain derivations with encrypted-source lineage and protected availability.
- Inputs and identity domain: plaintext transaction, ciphertext provenance, source/view-basis or finalized-view/revision/object/security context, credential capability identity, tenant, sensitivity, cache/disposal policy, and limits.
- Preconditions: a read algorithm transaction finished; disclosure policy explicitly admits any retention or cache class.
- Card slots: `SC.C1.SEC.PLAINTEXT-HANDLING.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: plaintext bytes, memory lifetime, cache/spool bytes, retention, disposal attempts, provenance metadata, and diagnostics are bounded.
- Cancellation: private plaintext aborts where possible; retained/unknown remnants stay classified and appear in the operation receipt.
- Authority and secrets: no durable shared plaintext cache by default; every cache/index partitions tenant, credential/security context, sensitivity, disclosure, and revision.
- Outputs and outcomes: returns protected plaintext artifact/virtual provenance with availability class, or memory-only/refused/cleanup-unknown state.
- Diagnostics: cache denial, partition mismatch, retention limit, cleanup state, disclosure refusal, and source/context mismatch never include plaintext.
- Evidence and provenance: every plaintext byte range links ciphertext source/container, handler/filter/algorithm/cards, credential context identity, and transaction.
- Determinism and replay: plaintext derivation is D0 when secret/context exists; retention and disposal are operational evidence, not semantic identity.
- Falsifiers and Gauntlet: cross-tenant/credential/revision cache attacks, log scans, cancellation, crash remnants, source change, public digest disclosure, and zeroization no-claim checks.
- Surfaces: object/string/stream resolution, decoded containers, reports, CLI credentialed output, fuzz witnesses, and caches.
- Dependencies and consumers: depends on FDN.008/FDN.013, SEC.002/SEC.004/SEC.008, and FLT.002; SEC.005–SEC.007, DOC.001, FLT.010, REV.006, and reports consume its partition/disposal law.
- Migration and withdrawal: a leak or unsound partition invalidates/purges affected cache class and triggers incident handling; receipts remain historical.
- No-claim boundary: disposal attempts do not prove physical erasure; memory safety does not imply confidentiality against all host/process side channels.
- Rationale: plaintext must inherit both provenance and secrecy or content addressing will silently turn decryption into cross-context disclosure.

### 8.7 Resolved-document and strict-open contracts

#### `C1.CC.DOC.001@1` — Object-version resolution

- Identity, lifecycle, layer: active C1 L2 contract; resolution is view- and revision-graph-scoped and never keyed by bare object number alone.
- Inputs and identity domain: exact `DocumentViewId`, `RevisionGraphId`, revision node, `IndirectKey`, occurrence/effective mapping, resolve policy, security context, and cards.
- Preconditions: graph/view relationship is validated; requested mapping exists or remains explicit; credentials are supplied only through SEC leases.
- Card slots: `SC.C1.DOC.OBJECT-RESOLUTION.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: references, visited objects, depth, cycles, container nesting, decrypted/decoded bytes, diagnostics, and retained paths are bounded.
- Cancellation: iterative traversal checkpoints between edges and expensive decode/decrypt units; private partial results cannot enter durable caches as singular values.
- Authority and secrets: resolver receives narrow source/security/filter capabilities; it cannot discover credentials, external files, network, writer, or higher-layer policy.
- Outputs and outcomes: returns one-step/bounded-recursive/graph-traversal claim with selected object version, path, cycle events, decryption context, evidence, and partiality.
- Diagnostics: missing/free/invalid reference, cycle, depth/limit, ambiguous mapping, decode/decrypt refusal, wrong view/graph, and source change use exact locations.
- Evidence and provenance: resolved value links raw occurrence, revision, graph/view, path, security/filter receipts, cards, and coverage.
- Determinism and replay: D0 under the exact view, policy, capabilities, cards, dependencies, and semantic limits.
- Falsifiers and Gauntlet: cycles, deep chains, missing/free objects, generation mismatch, shadowed definitions, encrypted object-stream members, and cache cross-view tests.
- Surfaces: high-level document facade, catalog/page/security inventory, CLI objects, OpenReport, recovery, and fuzz target.
- Dependencies and consumers: depends on REV.006/REV.009, DOC.002, FLT.001–FLT.010, SEC.001–SEC.009, SYN.004–SYN.006, and FDN.001–FDN.015; DOC.004–DOC.009/DOC.012–DOC.015/REC.005–REC.010/RPT.001–RPT.003/RPT.007/RPT.010 consume it.
- Migration and withdrawal: resolver/card/policy change yields new view/derivation identities and invalidates incompatible cached resolution.
- No-claim boundary: resolution under one view does not establish source-level uniqueness, conformance, historical continuity, or safety of a referenced active feature.
- Rationale: view-scoped iterative resolution preserves revision history and makes cycles, security context, and recovery assumptions observable.

#### `C1.CC.DOC.002@1` — Effective object mapping and document views

- Identity, lifecycle, layer: active C1 L2 contract; `DocumentViewId` binds one admitted interpretation over an exact root/graph/selection, never just source bytes.
- Inputs and identity domain: source root, final `RevisionGraphId`, `DocumentViewBasisId`, selected strict chain or `RecoveryHypothesisBasisId`, DOC.003 dialect record, SEC.001 `SecurityContextId`, SEC.008 scope record when declared-handler or explicit Crypt/Identity routing applies, outcome-sensitive limits, coverage, capability identities, and semantic scope.
- Preconditions: graph is immutable; selection is singular or the operation returns alternatives; semantic-scope manifest is explicit and card-covered.
- Card slots: `SC.C1.DOC.EFFECTIVE-VIEW.001`, `SC.C1.DOC.SEMANTIC-SCOPE-R0.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: effective mappings, versions, duplicate resolution, semantic commitment, canonicalization/symmetry work, and diagnostics are bounded.
- Cancellation: incomplete view construction remains private; cancellation cannot turn a traversed prefix into a whole-document view.
- Authority and secrets: view identity records semantically relevant capability identities, not secret values or transient caller leases.
- Outputs and outcomes: emits immutable effective view, object mapping, `SemanticStateId` for the declared R0 scope, coverage, selected strict-chain or recovery-basis identity, evidence, and no-claim set; it does not mint a finalized recovery hypothesis. The R0 semantic scope is not claimed serialization-total and carries no canonical byte-identity consequence.
- Diagnostics: unresolved chain, conflicting object mapping, under-specified scope, missing range/card, capability dependence, and budget exhaustion.
- Evidence and provenance: view record binds exact source root, graph, selection, dialect/security choices, limits, capabilities, coverage, and semantic state.
- Determinism and replay: D0 under the same full input manifest; two views may share scoped semantics without sharing history, authority, signatures, or provenance.
- Falsifiers and Gauntlet: same source/different graph, strict/recovered alternatives, profile changes, capability changes, partial ranges, symmetry, and semantic-scope omission.
- Surfaces: resolver, open/recovery reports, CLI inspect/revisions/objects, caches, and all R0 workflows.
- Dependencies and consumers: depends on REV.009, DOC.010, DOC.003, SEC.001 and conditionally SEC.008, and FDN.001–FDN.015; DOC.001, DOC.004–DOC.009, DOC.012–DOC.015, recovery finalization, and report contracts consume it. Ordinary resolution and DOC.007 findings are downstream and cannot define bootstrap identity.
- Migration and withdrawal: any meaning-changing input or scope change creates a new view/state protocol; old receipts stay bound to old IDs.
- No-claim boundary: semantic equality cannot upgrade common history, signature coverage, source preservation, authorization, provenance, serialization-totality, or canonical byte identity; C1 cites and does not amend the kernel's scope-totality law.
- Rationale: source bytes can support several histories and recovery interpretations; binding the exact selected graph/view prevents cache and report aliasing.

#### `C1.CC.DOC.003@1` — Effective dialect by selected history

- Identity, lifecycle, layer: active C1 L2 contract; dialect is a per-selected-revision record and a history, not one header scalar.
- Inputs and identity domain: physical header candidate, DOC.011-limited catalog version override where available, extension declarations, encountered raw feature signals, selected base graph/view basis/revision, profile, and cards.
- Preconditions: all available version signals are source-bound; absent cards or unresolved conflicts remain explicit.
- Card slots: `SC.C1.DOC.EFFECTIVE-DIALECT.001`, `SC.C1.DOC.EXTENSION-ADMISSION.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: revisions, declarations, feature observations, reference resolution, conflicts, and diagnostics are bounded.
- Cancellation: partial computation returns exact processed revision scope and cannot label later history.
- Authority and secrets: dialect computation has read-only source/object access and no external standards lookup at runtime.
- Outputs and outcomes: records declared, feature-required, selected-for-interpretation, and future-write-target fields separately, with per-revision history and unresolved conflicts.
- Diagnostics: invalid override/declaration, unsupported extension, header conflict, newer-feature observation, missing card, and partial history.
- Evidence and provenance: every signal links exact token/object/revision/view basis and card/profile basis.
- Determinism and replay: D0 for the same view basis, bootstrap observations, cards, profile, and semantic limits.
- Falsifiers and Gauntlet: header/override disagreement, revision-local override, unknown extension, newer feature in older declaration, partial graph, and duplicate keys.
- Surfaces: OpenReport, capability admission, object-model validation, CLI inspect/revisions, and recovery alternatives.
- Dependencies and consumers: depends on SYN.002, REV.004, DOC.010, DOC.011, and the pre-C1 card-authority snapshot; DOC.002, DOC.004–DOC.009, DOC.012–DOC.015, and RPT consume the effective dialect result.
- Migration and withdrawal: registry/card revision creates a new dialect derivation/view; historical records are not rewritten.
- No-claim boundary: encountering a feature does not silently upgrade declared conformance, and a dialect record does not validate every object.
- Rationale: history-scoped dialect prevents a later catalog override from changing facts about earlier revisions.

#### `C1.CC.DOC.004@1` — Catalog and typed structural access

- Identity, lifecycle, layer: active C1 L2 contract; typed accessors project raw/resolved structures without unchecked casts or later-layer semantics.
- Inputs and identity domain: exact document view, effective root mapping, catalog candidate(s), resolver, dialect, duplicate policy, cards, and limits.
- Preconditions: strict root resolution is available or alternatives/refusal are returned; card slots cover every admitted accessor family, including destination-carrier linkage.
- Card slots: `SC.C1.DOC.CATALOG.001`, `SC.C1.DOC.STRUCTURAL-ACCESSORS.001`, `SC.C1.DOC.DESTINATION-CARRIERS.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: object resolutions, accessor calls, references, container depth, returned carriers, and diagnostics are bounded.
- Cancellation: accessors observe the shared context and return no partially initialized typed carrier as a singular value.
- Authority and secrets: read-only document authority; typed carriers for actions/files/signatures remain inert and cannot invoke hosts.
- Outputs and outcomes: returns claims for catalog, pages root, names, outlines, destination carriers, metadata, optional content, forms, structure, associated files, intents, permissions, preferences, and extensions as structurally admitted; a destination carrier exposed through a name/number-tree root delegates only structural tree traversal to DOC.006.
- Diagnostics: missing/wrong-type/ambiguous root, unresolved reference, duplicate selection, unavailable card, recovery assumption, and partial coverage.
- Evidence and provenance: every accessor result links raw entries, object path, view/graph, dialect, cards, and resolution evidence.
- Determinism and replay: D0 under the exact view, cards, resolver/profile, capabilities, and limits.
- Falsifiers and Gauntlet: missing/multiple catalogs, wrong types, cycles, duplicates, encrypted entries, stale cache, and partial-source cases.
- Surfaces: Rust document facade, CLI inspect/objects, structural inventories, OpenReport, and recovery.
- Dependencies and consumers: depends on DOC.001–DOC.003, SYN.006, and FDN.001–FDN.015; DOC.005–DOC.009/DOC.012–DOC.015/REC.005/RPT consume it.
- Migration and withdrawal: accessor/card semantic changes version result types/contracts; raw carriers remain available where safe.
- No-claim boundary: locating a structural carrier does not claim semantic destination resolution, behavior execution, rendering, accessibility, signature trust, reachability, or external-resource safety.
- Rationale: typed but evidence-bearing access gives R0 useful structure without smuggling L3–L6 behavior into L2.

#### `C1.CC.DOC.005@1` — Page-tree structure and inheritance inventory

- Identity, lifecycle, layer: active C1 L2 contract; C1 inventories page-tree topology and later-layer inputs without executing page content.
- Inputs and identity domain: document view, pages root, resolver, dialect, raw page/tree dictionaries including distinct `/Tabs` occurrences, inheritance cards, optional caller `PageGeometryRequestId` naming requested box and fallback rule, and limits.
- Preconditions: catalog accessor yields a candidate pages root; strict/recovery status is retained.
- Card slots: `SC.C1.DOC.PAGE-TREE.001`, `SC.C1.DOC.PAGE-INHERITANCE.001`, `SC.C1.DOC.PAGE-TABS.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: nodes, edges, depth, reference resolutions, page leaves, duplicate reachability, cross-revision continuity candidates, inherited-value walks, and diagnostics are bounded.
- Cancellation: iterative walk returns exact coverage/frontier; it cannot claim all pages or global absence after early stop.
- Authority and secrets: read-only; content streams and resources are references/inventory only and cannot execute or render.
- Outputs and outcomes: page/tree nodes, order alternatives, parent/cycle/count findings, bounded cross-revision page continuity/lineage evidence with explicit alternatives and unknowns, raw `/Tabs` carrier occurrence/status without accessibility meaning, and a `PageAttributeInventoryId` that preserves raw arrays plus separately records inherited/local/defaulted `Resources`, `MediaBox`, `CropBox`, `BleedBox`, `TrimBox`, `ArtBox`, `Rotate`, and `UserUnit`; a supplied `PageGeometryRequestId` remains an inspection identity and produces only strict/refused or named-recovery geometry evidence, never rendering.
- Diagnostics: wrong node type, missing/bad parent, cycle, count mismatch, duplicate reachability, continuity evidence conflict/unknown, source-bound-ID equality offered as continuity proof, invalid inherited/local carrier, missing/duplicate/unclassified `/Tabs`, non-finite coordinate, inadmissible scale, degenerate/reversed rectangle, requested-box/fallback mismatch, silent-normalization attempt, and depth/coverage limit.
- Evidence and provenance: every page/node/attribute, continuity alternative, and requested-box result links object version/path, exact current/prior view and revision graphs, each raw occurrence/array, inheritance/default witness, selection or named-recovery policy, request identity, and cards; source-bound object/occurrence ID equality is evidence only and never continuity identity.
- Determinism and replay: D0 under exact view, cards, resolver, and semantic limits.
- Falsifiers and Gauntlet: deep/cyclic trees, wrong counts, shared leaves, duplicate parents, cross-revision continuation/replacement/unknown alternatives, false continuity from equal object IDs, recovery-hypothesis divergence, inheritance/locality confusion, every named box, non-finite/degenerate/reversed geometry, requested-box fallback substitution, raw/effective divergence, duplicate/malformed `/Tabs`, encrypted objects, and cancellation.
- Surfaces: CLI inspect/objects, OpenReport summary, recovery materiality, capability discovery, and later C2 handoff.
- Dependencies and consumers: depends on DOC.001–DOC.004; REC.005, DOC.009, and RPT may consume structural results.
- Migration and withdrawal: later rendering semantics receive new contracts; this topology contract is not widened by page execution.
- No-claim boundary: page discovery, continuity evidence, `/Tabs` inventory, and geometry-request evidence do not claim page identity or historical fact, accessibility meaning/compliance, paintability, visual fidelity, valid resources, font support, page-program execution, or page-content conformance.
- Rationale: structural page inventory helps determine material recovery differences while respecting C1’s no-rendering boundary.

#### `C1.CC.DOC.006@1` — Name and number tree structure

- Identity, lifecycle, layer: active C1 L2 contract; tree traversal exposes raw order, key/range defects, cycles, and profile-selected traversal separately.
- Inputs and identity domain: document view, candidate roots, resolver, typed key domain, cards/profile, and limits.
- Preconditions: a catalog/name-tree accessor identifies the root; key interpretation slots have later review.
- Card slots: `SC.C1.DOC.NAME-TREE.001`, `SC.C1.DOC.NUMBER-TREE.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: nodes, depth, keys/values, comparisons, duplicate/overlap alternatives, references, and diagnostics are bounded.
- Cancellation: iterative traversal returns processed scope and frontier; partial output cannot assert global sort/range properties.
- Authority and secrets: read-only; referenced embedded/action data remain inert and sensitivity-protected.
- Outputs and outcomes: raw entries, typed traversal claim, malformed limits, ordering, duplicates, overlaps, cycles, and selected order evidence.
- Diagnostics: invalid limits/key, unsorted entries, duplicate key, overlap, cycle, wrong type, and budget/coverage exhaustion.
- Evidence and provenance: every entry and selected traversal links exact object path, view/graph, raw token, cards, and recovery/profile choice.
- Determinism and replay: D0 under exact view, card/profile, resolver, and semantic limits.
- Falsifiers and Gauntlet: deep/cyclic trees, duplicate/unsorted keys, overlapping limits, wrong types, partial sources, and traversal permutations.
- Surfaces: CLI objects/inspect, structural security inventory, OpenReport, and later-cycle document features.
- Dependencies and consumers: depends on DOC.001–DOC.004 and FDN.014; DOC.008/DOC.009/REC.005/RPT consume it.
- Migration and withdrawal: card/traversal change creates new derivation/view semantics; raw tree evidence remains.
- No-claim boundary: traversing an entry does not semantically resolve a destination, validate the referenced feature, execute an action, establish reachability, or establish canonical-write behavior.
- Rationale: explicit malformed-tree evidence prevents convenience maps from hiding duplicates, order defects, and cycles.

#### `C1.CC.DOC.007@1` — Card-linked C1 validation layers 1–3

- Identity, lifecycle, layer: active C1 L2 contract for separate lexical/file-structure, COS/object-model, and cross-object-relationship validation layers; semantic rule execution is unavailable until rights-reviewed cards and admitted machine-readable rule data exist.
- Inputs and identity domain: exact source/final revision graph/document view, lexer/file-structure facts, raw/resolved objects and relationships, dialect, immutable runtime rule data, exact rule/card versions, profile, coverage request, and limits.
- Preconditions: every rule links an active two-person-reviewed card; any imported model has recorded license/provenance and no prohibited-source lineage.
- Card slots: `SC.C1.DOC.LEXICAL-FILE-VALIDATION.001`, `SC.C1.DOC.OBJECT-MODEL-VALIDATION.001`, `SC.C1.DOC.RELATIONSHIP-VALIDATION.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: objects, rules, relationships, reference depth, diagnostics, rule results, canonicalization, and external data reads are bounded.
- Cancellation: validation returns processed rule/object coverage and never converts unrun rules into passes.
- Authority and secrets: validator is read-only, has no external lookup, and can mint only its registered rule-outcome/evidence class.
- Outputs and outcomes: three explicitly separate layer records, each with canonical per-rule pass/fail/not-applicable/not-evaluated/unsupported/indeterminate status, separate severity/coverage, and exact locations; a pass in one layer has no automatic consequence for another.
- Diagnostics: missing card/rule data, unsupported rule, invalid input type, dependency gap, resource limit, and rule-engine fault remain distinct.
- Evidence and provenance: each result binds card/rule/profile versions, view/object path, executed coverage, engine identity, and diagnostics.
- Determinism and replay: D0 under exact view, rule/card data, profile, dependencies, and semantic limits.
- Falsifiers and Gauntlet: atomic positive/negative fixtures in each of layers 1–3 after card admission, cross-layer non-transitivity, rule mutation, missing-card refusal, generated-data drift, partial coverage, and alternate checker cases.
- Surfaces: OpenReport validation slice, CLI inspect/objects, capability manifest, immune-system coverage, and close gate.
- Dependencies and consumers: depends on BYT.001–BYT.006, SYN.001–SYN.007, REV.001–REV.009, DOC.001–DOC.006, the pre-C1 reviewed-card authority snapshot, ratified rights/license decisions, and FDN.001–FDN.015; IMM.001 supplies only a runtime coverage projection. DOC.009/RPT.001/RPT.010 consume validation results.
- Migration and withdrawal: rule/card change versions the profile and results; generated rule data never silently update behavior.
- No-claim boundary: no card means no normative validation; imported rule data do not replace controlling licensed sources; C1 layers 1–3 do not cover page-program, rendering-resource, standardized-profile, accessibility, security-policy, or interoperability validation.
- Rationale: an early validation framework allows later rules to inherit evidence and coverage without generating normative meaning during this run.

#### `C1.CC.DOC.008@1` — Inert security-carrier inventory

- Identity, lifecycle, layer: active C1 L2 structural contract; it inventories carriers that may matter to security while executing none of them.
- Inputs and identity domain: exact view, catalog/page/name-tree carriers, raw/resolved dictionaries, revision history, attachments/actions/forms/metadata/signature candidate slots, and cards.
- Preconditions: only card-covered structural patterns are classified; unknown carriers remain unknown rather than harmless.
- Card slots: `SC.C1.DOC.SECURITY-CARRIERS.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: objects, references, embedded-file descriptors, action carriers, metadata packages, revisions, payload sizes inspected structurally, and diagnostics are bounded.
- Cancellation: returns exact scanned carriers/coverage and cannot claim absence across unvisited objects, alternate hypotheses, or opaque payloads.
- Authority and secrets: no action, JavaScript, URL, launch, embedded payload, form program, external reference, or nested document is executed/opened/fetched by default.
- Outputs and outcomes: inventory of recognized, unknown, opaque, encrypted, unsupported, and policy-blocked carriers with object/revision/view provenance.
- Diagnostics: unknown action/carrier, unresolved/opaque payload, nested content uninspected, external reference inert, encrypted value unavailable, and coverage truncation.
- Evidence and provenance: every finding links raw entries, object path, revision/view, cards, decryption state, and observation coverage.
- Determinism and replay: D0 under exact view, cards, decryption capabilities, and semantic limits.
- Falsifiers and Gauntlet: hidden/shadowed carriers, name-tree cycles, encrypted carrier dictionaries, unknown types, nested opaque payloads, alternate recovery views, and partial sources.
- Surfaces: OpenReport/security report, CLI inspect/objects, recovery security comparison, capability manifest, and close gate.
- Dependencies and consumers: depends on DOC.001–DOC.006, REV.008, SEC.001–SEC.009; DOC.009/DOC.012/REC.008/RPT consume it.
- Migration and withdrawal: later L5 semantic/action/attachment models receive new contracts; this structural inventory cannot be silently renamed semantic safety analysis.
- No-claim boundary: absence within scanned recognized carriers is not whole-document absence, sanitization, nested-payload safety, or proof that unknown data are inert.
- Rationale: R0 needs a useful security inventory without violating layer direction or claiming later behavior semantics.

#### `C1.CC.DOC.009@1` — Strict-open orchestration

- Identity, lifecycle, layer: active C1 L2/L8 facade contract; strict open composes source, syntax, revision, view, security inventory, and reports without invoking recovery.
- Inputs and identity domain: immutable/partial source root, explicit strict request, profile snapshot, limits, optional credential capability, requested coverage, and active contract/card manifest.
- Preconditions: source admission succeeds; required cards/contracts are active; strict request contains no recovery profile.
- Card slots: `SC.C1.DOC.STRICT-OPEN.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: all lower-layer counters share one non-resettable account; open-specific orchestration/retained result/report budgets are explicit.
- Cancellation: orchestrator stops new work, aborts private decode results, finalizes accounting/diagnostics, and returns typed cancellation.
- Authority and secrets: caller gets only requested read/decrypt capabilities; no writer, external source, action, trust, or network authority is introduced.
- Outputs and outcomes: immutable `StrictOpenResultId` plus source/graph/view alternatives as allowed by strict facts, object/security inventories, coverage, explicit unavailable capabilities, and a view-keyed `OccurrenceVisibilityMapId` over every retained physical/virtual occurrence classified as visible, shadowed, unreachable, or unknown after bounded DOC.001 traversal; RPT.001 alone owns the base `OpenReport` body.
- Diagnostics: lower-layer codes are retained; orchestration adds only composition, occurrence-without-classification, reachability frontier/limit, missing-contract/card, authority, and coverage-summary codes.
- Evidence and provenance: strict result binds source root, every base/final graph, selected view or live alternatives, every occurrence/classification/path or unknown frontier, security/decryption state, limits, and no-claims; report construction is downstream.
- Determinism and replay: semantic body targets D0 under the exact input manifest; I/O timing and wall observations remain separate.
- Falsifiers and Gauntlet: well-formed atomic fixtures after card admission; a project-authored or rights-admitted independently authored structural checker/alternate-parser fixture oracle with general `OracleLineageId` that does not call the strict target path; visible/shadowed/unreachable/unknown occurrences across revisions and object streams; alternate views; malformed inputs proving no recovery leakage; partial source, credentials, cancellation, diagnostic truncation, and source change.
- Surfaces: Rust `open` facade, CLI `inspect` strict mode, reports, capability discovery, and Workflow B strict leg.
- Dependencies and consumers: depends on applicable BYT.001–BYT.006, SYN.001–SYN.007, REV.001–REV.009, FLT.001–FLT.010, SEC.001–SEC.009, and DOC.001–DOC.008/DOC.010–DOC.015 contracts; RPT.001/RPT.003/RPT.010 and REC.002 consume its strict result.
- Migration and withdrawal: a material composition change versions the contract and report claim row; narrower surfaces cannot claim more than this contract.
- No-claim boundary: strict open does not render, extract text, validate trust, repair, write, or silently select a recovery interpretation; unreachable means only “not reached under the exact bounded view/traversal,” never harmless, absent, sanitized, or semantically inert.
- Rationale: one facade makes strictness observable end to end and prevents lower recovery conveniences from leaking into ordinary “open.”

#### `C1.CC.DOC.010@1` — Pre-view selection and mapping basis

- Identity, lifecycle, layer: active C1 L2 staging contract; `DocumentViewBasisId` binds a source, immutable base graph, one selected strict chain or already minted recovery-hypothesis basis, raw effective mapping, profile, and semantic limits without claiming a final view.
- Inputs and identity domain: source root, `BaseRevisionGraphId`, raw occurrence/compressed-locator inventory, selected strict chain or `RecoveryHypothesisBasisId`, profile/capability identities, coverage, and outcome-sensitive limits.
- Preconditions: base graph and selection input already exist; strict invocation has no recovery dependency; recovered invocation is permitted only after REC.002 and an independently minted hypothesis basis.
- Card slots: `SC.C1.DOC.PREVIEW-BASIS.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: mapping entries, duplicate/history selection, unresolved locators, canonicalization/symmetry work, diagnostics, and output bytes are bounded.
- Cancellation: an incomplete basis remains private; no traversal prefix becomes a selected chain or mapping.
- Authority and secrets: the basis records non-secret capability/security-context identities only and grants no credential, plaintext, writer, network, or external-source authority.
- Outputs and outcomes: emits immutable `DocumentViewBasisId`, `BootstrapMappingId`, exact selection witness, raw mapping, dialect/security signal locators, unresolved compressed members, coverage, and no-claims.
- Diagnostics: invalid chain/basis, raw mapping conflict, missing occurrence/range, unresolved locator, capability mismatch, symmetry limit, and source change remain distinct.
- Evidence and provenance: basis binds source root, base graph, strict-chain or recovery-basis identity, every raw selection witness, cards/profile, capabilities, coverage, and limits.
- Determinism and replay: D0 for the same source/base graph/selection/raw mapping/profile/capabilities/cards/semantic limits.
- Falsifiers and Gauntlet: strict/recovered basis confusion, same source/different base graph, duplicate-map permutations, missing compressed locator, capability change, partial range, and cancellation.
- Surfaces: limited bootstrap resolver, security inventory/scope, object-stream indexing, dialect derivation, final view construction, recovery candidates, and fuzz targets.
- Dependencies and consumers: strict mode depends on REV.004/REV.005, SYN.004–SYN.007, BYT.006, and FDN.001–FDN.015; recovered mode, in state transition `strict-admitted -> recovery-basis-available`, additionally consumes REC.001/REC.003–REC.005 only after REC.002 strict admission and after the named basis artifacts are minted. DOC.011, SEC.001/SEC.008, REV.006, DOC.002/DOC.003, and REC.010 consume the basis.
- Migration and withdrawal: selection/mapping/basis protocol changes create a new basis; older bases remain immutable and cannot be relabeled as final views.
- No-claim boundary: a view basis is not `DocumentViewId`, does not resolve arbitrary objects, and cannot erase strict defects or live recovery alternatives.
- Rationale: naming the chain and raw mapping before value resolution breaks the resolver/view/security cycle while preserving graph/view separation.

#### `C1.CC.DOC.011@1` — Limited pre-view resolver

- Identity, lifecycle, layer: active C1 L2 staging contract; `BootstrapResolutionSetId` resolves only the registered references needed for dialect/security/view finalization under one `DocumentViewBasisId`.
- Inputs and identity domain: view basis, bootstrap mapping, explicit requested locator set, raw COS values, base-graph occurrences, source coverage, cards, and limits.
- Preconditions: each requested locator belongs to the registered bootstrap allowlist; resolution needing a decoded object-stream member, final `DocumentViewId`, unminted credential context, or higher-layer semantics returns unavailable/refused.
- Card slots: `SC.C1.DOC.LIMITED-PREVIEW-RESOLUTION.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: requested references, depth, visited objects, raw bytes, cycles, diagnostics, and result bytes are tightly bounded and narrower than ordinary DOC.001 limits.
- Cancellation: partial traversal publishes only an explicit incomplete bootstrap set and cannot authorize final view construction where a required locator is unresolved.
- Authority and secrets: read-only raw-source capability only; no ambient credentials, network, external file, writer, or ordinary object facade.
- Outputs and outcomes: emits `BootstrapResolutionSetId`, exact raw values/paths, cycles, unavailable object-stream locators, coverage, and typed partial/refused/cancelled states.
- Diagnostics: allowlist violation, cycle/depth, missing/free object, compressed-member dependency, encrypted-unavailable value, range gap, card gap, and source change remain distinct.
- Evidence and provenance: every result links view basis, raw mapping entry, occurrence/span, traversal path, cards, limits, and availability.
- Determinism and replay: D0 for the same basis/request set/raw values/cards/semantic limits; request order cannot change the set root.
- Falsifiers and Gauntlet: arbitrary-reference escalation, cycles, compressed encryption locator, missing catalog/encryption reference, duplicate key, partial source, and cancellation.
- Surfaces: SEC.001 inventory, DOC.003 dialect derivation, DOC.002 finalization inputs, diagnostics, bootstrap fuzzing, and reports of unavailable bootstrap signals.
- Dependencies and consumers: depends on DOC.010, REV.004/REV.005, SYN.004–SYN.006, BYT.004, and FDN.004–FDN.014; SEC.001, DOC.003, and DOC.002 consume it.
- Migration and withdrawal: allowlist or resolution-law change versions the contract and invalidates affected basis finalization; old resolution sets remain scoped.
- No-claim boundary: bootstrap resolution does not provide the ordinary object API, prove whole-view reachability, decrypt members, or validate document structure.
- Rationale: a narrow fail-closed resolver supplies only the signals needed to finish the view without requiring that final view as its own input.

#### `C1.CC.DOC.012@1` — Encrypted-payload and unencrypted-wrapper structural inventory

- Identity, lifecycle, layer: active C1 L2 atomic inventory contract; it records card-admitted encrypted-payload/unencrypted-wrapper structural relations without evaluating later reachability or sanitization.
- Inputs and identity domain: exact document view, final revision graph, raw/resolved wrapper and payload candidates, SEC.001 encryption-scope inventory, DOC.008 carrier records, cards, coverage, and limits.
- Preconditions: `MB-SC-R0-038` has an active rights-reviewed body and two-person meaning review before classification; until then the capability is unavailable rather than inferred from generic carrier shape or model memory.
- Card slots: `SC.C1.DOC.ENCRYPTED-WRAPPER-INVENTORY.001` → `MB-SC-R0-038` — `PENDING-LICENSED-SOURCE`.
- Budgets: candidate objects, references, revision occurrences, wrapper/payload relation records, inspected structural bytes, diagnostics, and retained evidence are bounded.
- Cancellation: returns exact visited candidates and frontier; an interrupted inventory cannot assert absence or collapse unknown/opaque/encrypted states.
- Authority and secrets: read-only structural authority; no payload is opened, executed, fetched, sanitized, or decrypted except through an already admitted narrower SEC capability whose plaintext remains protected.
- Outputs and outcomes: immutable per-view inventory records for card-recognized candidates, exact wrapper/payload relation status, encryption/availability state, unknown or opaque classification, coverage, and explicit unavailable outcomes.
- Diagnostics: pending or missing card, unclassified candidate, unresolved reference, wrapper/payload ambiguity, encrypted-unavailable value, alternate revision, opaque nested content, coverage limit, and cancellation remain distinct.
- Evidence and provenance: every record binds raw object paths/spans, graph/view/revision, DOC.008 and SEC.001 inputs, card/link state, decryption availability without secret material, limits, and observation coverage.
- Determinism and replay: D0 under the exact view/graph/cards/classifier protocol/capabilities and semantic limits; traversal order cannot change the inventory root.
- Falsifiers and Gauntlet: admitted atomic fixtures after card activation, encrypted/unencrypted combinations, unknown shapes, alternate revisions/views, cycles, partial sources, opaque nested payloads, and cancellation.
- Surfaces: strict/recovery structural inventories, RPT.003/RPT.007, CLI inspect/objects, capability discovery, IMM.009 coverage, FUZ.008, and the C1 product gate.
- Dependencies and consumers: depends on REV.009, DOC.001–DOC.004, DOC.008, SEC.001, the pre-C1 reviewed-card authority snapshot, and FDN.001–FDN.015; DOC.009, REC.010, RPT.001/RPT.003/RPT.007, IMM.009, and FUZ.008 consume it.
- Migration and withdrawal: card/classifier changes version the inventory contract and derivation; historical raw carrier evidence and pending/unknown states are never relabeled in place.
- No-claim boundary: inventory does not establish whole-document absence, payload safety, encryption completeness, semantic reachability, an execution path, a sanitization result, or permission to open nested content.
- Rationale: an explicit atomic owner discharges the declared R0 inventory surface without pretending that DOC.008's generic opaque-carrier record performed the card-specific classification.

#### `C1.CC.DOC.013@1` — PDF 2.0 UTF-8 text-string structural inventory

- Identity, lifecycle, layer: active C1 L2 atomic inventory contract; it records card-admitted candidate occurrences for the named R0 string surface while leaving text semantics to reviewed authority and later layers.
- Inputs and identity domain: exact document view, raw string-token bytes and spans from SYN.005, object paths/revisions, effective dialect record, cards, requested coverage, and limits.
- Preconditions: `MB-SC-R0-039` has an active rights-reviewed body and two-person meaning review before any candidate is classified; pending authority yields unavailable coverage, not a locally invented decoder or rule.
- Card slots: `SC.C1.DOC.UTF8-TEXT-STRING-INVENTORY.001` → `MB-SC-R0-039` — `PENDING-LICENSED-SOURCE`.
- Budgets: objects, string candidates, raw bytes inspected, paths, revision occurrences, diagnostics, retained evidence, and output records are bounded.
- Cancellation: publishes only exact visited occurrence coverage and frontier; it cannot promote unvisited strings to absence or a partial byte sequence to decoded text.
- Authority and secrets: read-only; raw strings inherit source/plaintext sensitivity and no normalization, text extraction, rendering, external lookup, or host interpretation is authorized.
- Outputs and outcomes: immutable per-view structural occurrence inventory with raw-byte identity/location, card-classification status, dialect/view/revision binding, coverage, and explicit pending/unsupported/indeterminate outcomes.
- Diagnostics: pending or missing card, unavailable/decrypted source bytes, unclassified candidate, dialect/card mismatch, malformed or partial token, coverage cap, unsafe disclosure, and cancellation remain distinct.
- Evidence and provenance: every entry binds exact raw token/span, object path, view/graph/revision, SYN.005 record, dialect, card/link state, limits, and availability without inventing character meaning.
- Determinism and replay: D0 under exact raw tokens/view/dialect/cards/classifier protocol and semantic limits; scan order cannot alter the inventory root.
- Falsifiers and Gauntlet: admitted atomic fixtures after card activation, byte-boundary splits, partial/encrypted strings, alternate revisions/views, duplicate occurrences, unsafe disclosure, permutation, and cancellation.
- Surfaces: RPT.001 structural inventory, CLI inspect/objects, capability discovery, IMM.009 coverage, FUZ.008, and the C1 product gate.
- Dependencies and consumers: depends on SYN.005, REV.009, DOC.001–DOC.004, the pre-C1 reviewed-card authority snapshot, and FDN.001–FDN.015; DOC.009, REC.010, RPT.001/RPT.007, IMM.009, and FUZ.008 consume it.
- Migration and withdrawal: reviewed card/classifier change versions the inventory and its derivations; old raw evidence remains scoped and is never reinterpreted in place.
- No-claim boundary: an inventory entry is not decoded Unicode text, normalization, semantic string validity, text extraction, accessibility, searchability, layout, or rendering evidence.
- Rationale: direct ownership keeps the declared UTF-8 string inventory visible while the pending card firewall prevents model-memory semantics from entering C1.

#### `C1.CC.DOC.014@1` — Catalog `NeedsRendering` structural inventory

- Identity, lifecycle, layer: active C1 L2 atomic inventory contract; it records the named catalog carrier as structure only and never performs or predicts rendering.
- Inputs and identity domain: exact document view, DOC.004 catalog claim, raw duplicate-preserving catalog entries from SYN.006, effective dialect, cards, coverage, and limits.
- Preconditions: `MB-SC-R0-040` has an active rights-reviewed body and two-person meaning review before classification; a pending card leaves the inventory unavailable and does not license interpretation of the carrier's value.
- Card slots: `SC.C1.DOC.NEEDS-RENDERING-INVENTORY.001` → `MB-SC-R0-040` — `PENDING-LICENSED-SOURCE`.
- Budgets: catalog alternatives, entry occurrences, references, raw bytes inspected, duplicate-policy alternatives, diagnostics, and output evidence are bounded.
- Cancellation: returns exact examined catalog/entry coverage and frontier; partial work cannot assert absence or choose a duplicate alternative silently.
- Authority and secrets: read-only catalog authority; no page program, renderer, external resource, sanitizer, writer, or host callback is available.
- Outputs and outcomes: immutable per-view structural occurrence inventory with raw carrier identity/location, duplicate/ambiguity state, card-classification status, coverage, and explicit pending/unsupported/indeterminate outcomes.
- Diagnostics: pending or missing card, missing/multiple catalog, absent or duplicate carrier, wrong/unclassified raw type, unresolved reference, recovery alternative, coverage cap, and cancellation remain distinct.
- Evidence and provenance: every result binds raw catalog entry/token/span, object path, view/graph/revision, DOC.004/SYN.006 evidence, dialect, card/link state, duplicate policy, limits, and coverage.
- Determinism and replay: D0 under exact view/catalog evidence/dialect/cards/policy and semantic limits; traversal or duplicate encounter order cannot alter the inventory root.
- Falsifiers and Gauntlet: admitted atomic fixtures after card activation, missing/multiple catalogs, duplicate entries, alternate views, partial/encrypted catalogs, permutation, and cancellation.
- Surfaces: RPT.001 structural inventory, CLI inspect/objects, capability discovery, IMM.009 coverage, FUZ.008, and the C1 product gate.
- Dependencies and consumers: depends on SYN.006, REV.009, DOC.001–DOC.004, the pre-C1 reviewed-card authority snapshot, and FDN.001–FDN.015; DOC.009, REC.010, RPT.001/RPT.007, IMM.009, and FUZ.008 consume it.
- Migration and withdrawal: reviewed card/classifier change versions the inventory and derivation; old raw catalog evidence and unresolved alternatives remain immutable.
- No-claim boundary: carrier presence, absence, or value does not establish that rendering is required, possible, attempted, successful, safe, or within C1; no rendering or semantic rendering-need verdict is produced.
- Rationale: a dedicated structural owner satisfies the declared R0 slot without widening the no-rendering stop line or treating a generic catalog accessor as completed inventory.

#### `C1.CC.DOC.015@1` — Metadata inventory, reconciliation, and bounded XML structure

- Identity, lifecycle, layer: active C1 L2 metadata contract; one immutable `MetadataInventoryId` preserves document-information and XMP evidence per exact view/revision without silently merging conflicts.
- Inputs and identity domain: exact source/final revision graph/document view, DOC.004 metadata carriers, duplicate-preserved information-dictionary entries, raw or admitted decoded XMP packet artifacts, dates/identifiers/language/output-intent and extension-data carriers, security/availability context, cards, profile, coverage, and limits.
- Preconditions: every normative field interpretation has an active rights-reviewed card; XML processing uses the fixed hostile-input policy and no external resolver. A pending metadata/XML slot leaves the affected classification unavailable rather than inferred from carrier names or model memory.
- Card slots: `SC.C1.DOC.METADATA-RECONCILIATION.001`, `SC.C1.DOC.XML-SAFETY.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: source and decoded XML bytes, depth, nodes, attributes per element, total attributes, namespace declarations, name/text/CDATA lengths, processing instructions, comments, references, revision occurrences, diagnostics, and aggregate output are separately bounded under the non-resettable account.
- Cancellation: parsing/reconciliation checkpoints by bounded input/node units; an interrupted packet stays private or yields exact processed coverage/frontier and never a whole-packet or all-revision conclusion.
- Authority and secrets: read-only; DTDs, external/general/parameter entities, XInclude, external schemas/catalogs/stylesheets/namespace resources, network, host filesystem, and ambient callbacks are disabled or refused. Metadata/plaintext inherits source, credential, tenant, and disclosure policy.
- Outputs and outcomes: emits immutable per-view/per-revision Info/XMP/date/identifier/language/output-intent/extension carrier records, a bounded source-preserving XML structure when admitted, explicit conflicts rather than merged truth, availability/coverage, and typed pending/unsupported/partial/ambiguous/refused outcomes; publication is transactional.
- Diagnostics: pending card, duplicate/conflicting field, malformed or entity-like XML construct, forbidden external-resolution request, depth/node/attribute/text/output limit, encrypted-unavailable packet, revision conflict, unsafe disclosure, truncation, and cancellation remain distinct.
- Evidence and provenance: every field and conflict links the exact raw occurrence or decoded virtual span/container/stage receipt, object path, view/graph/revision, cards/profile, XML policy, limits, security context, and observation coverage.
- Determinism and replay: D0 under exact artifacts/view/cards/profile/parser version and semantic limits; external resources and ambient host state are absent, and unavailable protected inputs narrow replay explicitly.
- Falsifiers and Gauntlet: duplicate and conflicting Info/XMP values across revisions, DTD/entity/XInclude/external-resource attempts, depth/node/attribute/name/text/CDATA/comment/instruction bombs, malformed packets, encrypted/unavailable metadata, cancellation, transactional publication, and no-silent-merge properties.
- Surfaces: strict/recovery Open/Validation reports, CLI inspect/objects, capability discovery, FUZ.008 metadata/XML target slice, IMM.009 coverage, and the C1 product gate.
- Dependencies and consumers: depends on REV.009, DOC.001–DOC.004, FLT.001–FLT.010, SEC.001/SEC.008, the pre-C1 reviewed-card authority snapshot, and FDN.001–FDN.015; declared encrypted metadata, in state transition `metadata-structural-inventoried -> metadata-decrypted-value-available`, additionally consumes SEC.009 only after its exact-view/security-context committed-decryption receipt is minted. DOC.009, REC.010, RPT.001/RPT.007/RPT.010, IMM.009, and FUZ.008 consume it.
- Migration and withdrawal: card/parser/XML-policy or reconciliation-rule change versions the inventory; prior raw packets, conflicts, pending states, and report roots remain immutable.
- No-claim boundary: bounded structural XML parsing and metadata reconciliation do not establish sanitization, external-resource safety beyond the denied profile, document conformance, semantic equivalence, authenticity, privacy, rendering, or a universal metadata-safety verdict.
- Rationale: a distinct L2 owner makes metadata across revisions observable while forcing every XML path through real limits and the pending-source firewall.

### 8.8 Bounded-recovery contracts

#### `C1.CC.REC.001@1` — Recovery hypothesis-basis representation

- Identity, lifecycle, layer: active C1 L2 contract; `RecoveryHypothesisBasisId` identifies one registered assumption/evidence basis before a candidate document view exists.
- Inputs and identity domain: exact source, final strict revision graph, strict-open defects, proposed repair assumptions, affected source locations, family/profile identity, initial direct/shared cost observations under the existing work account, cards, and semantic limits; no candidate view or candidate-derived value is an input.
- Preconditions: REC.002 admitted the session; every assumption is registered and card/contract-linked; source and strict-graph facts are immutable; basis creation cannot invoke ordinary resolution.
- Card slots: `SC.C1.REC.HYPOTHESIS.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: assumptions, affected regions, source evidence, family records, canonicalization, and diagnostics are bounded.
- Cancellation: an unpublished basis remains private; retained partial family state states its frontier and cannot become a candidate view or selected result.
- Authority and secrets: basis creation has only the admitted read/decrypt capabilities needed for raw evidence; caller preference cannot alter byte facts or mint normative evidence.
- Outputs and outcomes: immutable `RecoveryHypothesisBasisId` containing assumptions, source support, affected scope, family/profile, initial constraint obligations, cards, limits, explicit unresolved consequences, and `RecoveryHypothesisCostVectorId`. Each existing budget dimension records direct, shared-attributed, shared-unallocated, or unavailable cost; the vector is not a scalar confidence or probability.
- Diagnostics: unknown assumption, conflicting source, missing strict parent, unbounded repair, card gap, graph mismatch, and budget exhaustion.
- Evidence and provenance: the basis binds the exact strict result, source/final strict graph, algorithm/profile, cards, limits, every assumption, raw supporting locations, and a `RecoveryCostAttributionReceiptId` that reconciles direct/shared/unavailable attribution; it contains no derived-view claim.
- Determinism and replay: D0 under exact strict inputs/protocol/semantic budget; family enumeration order cannot change basis identity.
- Falsifiers and Gauntlet: candidate-view input smuggling, invented source bytes, hidden assumptions, graph mismatch, equivalent-basis permutations, affected-scope/cost omission, shared-cost double counting, cost-to-confidence laundering, and cancellation.
- Surfaces: recovery family registry, candidate-view bootstrap, recovery report, CLI alternatives, held-out probe record, and fuzz harness.
- Dependencies and consumers: depends on REC.002, REV.009, and FDN.001–FDN.015; REC.003–REC.006, DOC.010, and REC.010 consume it.
- Migration and withdrawal: assumption or basis-identity grammar changes version the basis; old bases remain historical and never silently acquire candidate consequences.
- No-claim boundary: a basis is not a hypothesis verdict, candidate view, conforming parse, or authority to repair/write the source.
- Rationale: separating raw assumption support from candidate consequences breaks the recovery/view cycle while keeping every heuristic explicit.

#### `C1.CC.REC.002@1` — Strict-before-recovery admission

- Identity, lifecycle, layer: active C1 L2 orchestration contract; recovery may begin only after a separately recorded strict-open result.
- Inputs and identity domain: exact DOC.009 strict result and independently rooted RPT.001 base `OpenReport`, recovery request, exact FDN.007 `RecoveryPolicy` view/profile version, source/graph coverage, caller authority, and limits.
- Preconditions: strict result is immutable and retained; the recovery profile is explicit registered data and no calling surface labels recovery as strict. `StrictOnly` starts no recovery session; C1 may admit only `ConservativeRepair` or `ForensicPreserveAll` after their policy/card gates. `CommonViewerCompatibility`, processor-emulation profiles, and hidden defaults are unavailable in C1.
- Card slots: `SC.C1.REC.STRICT-FIRST.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: admission checks, strict-artifact retention, recovery reservation, profile validation, and diagnostics are bounded.
- Cancellation: cancellation before search records no hypotheses; strict result remains available and unchanged.
- Authority and secrets: recovery receives at most the strict operation’s read/decrypt capabilities, narrowed for its request.
- Outputs and outcomes: admitted recovery session linked to strict result and immutable profile view/version, or refusal for missing strict evidence, strict-only/incompatible/unregistered/later-cycle profile, source change, or insufficient budget.
- Diagnostics: absent/stale strict run, profile mismatch, changed source, capability mismatch, card gap, and reservation failure.
- Evidence and provenance: admission receipt binds strict result, base report, source/final strict graph, recovery profile, caller/task, capabilities, and search budget.
- Determinism and replay: D0 admission for exact inputs; later search has its own deterministic semantic limits.
- Falsifiers and Gauntlet: attempt recovery without strict run, `StrictOnly` recovery attempt, compatibility/emulation admission, unversioned or hidden default profile, changed source/graph, wider capability, cancellation, and report-label checks.
- Surfaces: Rust recovery facade, CLI explicit recovery mode, separately linked RecoveryReport/enrichment, and Workflow B.
- Dependencies and consumers: depends on DOC.009, RPT.001, and FDN.004–FDN.012; REC.001/REC.003–REC.010 consume it.
- Migration and withdrawal: recovery-profile change versions admission; old strict reports never acquire recovery outcomes in place.
- No-claim boundary: admitting a named profile controls search policy and does not redefine source meaning, promise a usable candidate, exhaustive search, or singular selection.
- Rationale: a hard boundary enforces the product law that strict parsing and repair are different products.

#### `C1.CC.REC.003@1` — Header/EOF/xref/revision recovery families

- Identity, lifecycle, layer: active C1 L2 family contract for common header/EOF-placement deviations, malformed terminal markers, `/Prev`, xref offsets/sections, table/stream disagreement, orphaned trailers, and truncated final revisions.
- Inputs and identity domain: admitted session, strict result, source/final strict graph coverage, SYN.002 exact header candidates/offsets/leading-byte spans/strict status, terminal/xref/link candidates, section parsers, graph protocol, recovery profile, cards, and limits.
- Preconditions: each family has registered assumptions, admissibility tests, and kill budget; missing ranges are not guessed.
- Card slots: `SC.C1.REC.HEADER-PLACEMENT-FAMILIES.001`, `SC.C1.REC.XREF-FAMILIES.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: prefix/tail scan regions, header/marker/offset/section candidates, retained leading-byte evidence, branches, graph nodes/edges, hypotheses, comparisons, and diagnostics are bounded.
- Cancellation: search returns generated candidates and exact frontier; unexplored branches remain missing coverage.
- Authority and secrets: read-only source; no implicit range retrieval or external processor observation.
- Outputs and outcomes: source-bound `RecoveryHypothesisBasisId` records for each admitted family, rejected bases/reasons, affected revisions/objects, and unresolved gaps; a header-placement basis preserves its exact candidate offset, leading-byte span, original strict status, and unchanged source identity; no candidate view or invented header byte is produced.
- Diagnostics: family/assumption ID, strict defect, header/terminal candidate location, nonzero header offset or EOF-placement deviation, violated constraints, cap, and material-effect status are stable.
- Evidence and provenance: each basis links the exact strict finding, SYN.002/SYN.003 source candidates as applicable, exact offsets and leading-byte evidence, final strict graph, cards, family algorithm, limits, and unresolved candidate-view obligations.
- Determinism and replay: D0 under the same source/coverage, profile, cards, and semantic search budget.
- Falsifiers and Gauntlet: every initial family, nonzero header offsets with preserved prefix bytes, false header/EOF markers in payload, multiple header candidates, huge candidate storms, forks/cycles, truncation, and intentionally ambiguous fixtures.
- Surfaces: recovery report/CLI alternatives, open facade, held-out probe, and fuzz target.
- Dependencies and consumers: depends on REC.001/REC.002, SYN.002/SYN.003, REV.001–REV.005/REV.009; DOC.010, REC.006, and REC.010 consume results.
- Migration and withdrawal: a family that cannot explain assumptions/bounds or produces materially wrong candidates is removed from defaults and tombstoned.
- No-claim boundary: family support does not mean every malformed header/xref is recoverable or that a generated chain is singular; a recovered header cannot normalize or invent bytes, change `SourceRootId`, rewrite the base/final strict graph, mutate the strict `OpenReport`, or establish strict conformance.
- Rationale: explicit families localize assumptions and let unsafe or misleading heuristics be killed without contaminating strict parsing.

#### `C1.CC.REC.004@1` — Stream/object-boundary recovery families

- Identity, lifecycle, layer: active C1 L2 family contract for wrong stream lengths, missing markers, bad object boundaries, duplicate definitions, and scan-discovered occurrences.
- Inputs and identity domain: strict stream/object failures, source regions, declared lengths, boundary/object candidates, optional admitted filter termination evidence, cards, and limits.
- Preconditions: each probe is bounded; payload exclusion intervals are honored unless an explicit broken-boundary hypothesis reopens them.
- Card slots: `SC.C1.REC.STREAM-OBJECT-FAMILIES.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: scan bytes, boundary/header candidates, decode probes, alternatives, hypotheses, output bytes, and diagnostics are bounded.
- Cancellation: returns observed regions/candidates and preserves ambiguity; no last-candidate selection.
- Authority and secrets: read-only; decryption/filter probes need existing narrow capabilities and retain secret/tenant partition.
- Outputs and outcomes: hypothesis bases with exact proposed boundaries/occurrences, assumptions, probe evidence, affected objects/streams, rejected bases, and unresolved view consequences.
- Diagnostics: wrong length, missing marker, payload lookalike, duplicate definition, probe disagreement, decode refusal, and cap exhaustion.
- Evidence and provenance: every basis binds raw source span, enclosing occurrence, optional decode receipt, strict graph, cards, profile, and search budget without claiming a derived view.
- Determinism and replay: D0 under exact source/context/protocol/semantic budget.
- Falsifiers and Gauntlet: embedded marker/header bytes, truncated payloads, filter disagreement, encrypted streams, huge scans, overlapping objects, and cancellation.
- Surfaces: recovery report/CLI alternatives, object resolver, open facade, and fuzz target.
- Dependencies and consumers: depends on REC.001/REC.002, SYN.007, REV.005, and FLT.001–FLT.010/SEC.001–SEC.009 as explicitly injected; DOC.010, REC.006, and REC.010 consume results.
- Migration and withdrawal: unsafe/unbounded family is disabled/tombstoned; improved family gets a new protocol and hypotheses.
- No-claim boundary: recovered boundaries/objects remain recovered and do not establish original conformance or safe writeback.
- Rationale: bounded probes expose why a boundary is plausible without letting raw payload patterns become objects by accident.

#### `C1.CC.REC.005@1` — Catalog/page-link/object-stream recovery families

- Identity, lifecycle, layer: active C1 L2 family contract for missing catalog/page links, malformed object-stream headers, and related structural gaps named by Rev 7 §14.5.
- Inputs and identity domain: strict graph/view/object failures, raw candidates, page/catalog/object-stream structural records, recovery profile, cards, and limits.
- Preconditions: candidate repairs are local and explicit; generated links cannot invent unavailable objects or source bytes.
- Card slots: `SC.C1.REC.DOCUMENT-LINK-FAMILIES.001`, `SC.C1.REC.OBJECT-STREAM-FAMILIES.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: candidate roots/links, tree walks, object-stream headers, alternatives, graph changes, hypotheses, and diagnostics are bounded.
- Cancellation: candidate exploration stops with exact frontier; partially connected trees/indexes are not singular views.
- Authority and secrets: read-only; encrypted object-stream candidates require admitted credential context and retain secrecy.
- Outputs and outcomes: hypothesis bases proposing structural links or object-stream interpretations, exact assumptions, affected page/object inventory, raw support, violations, and unresolved view consequences.
- Diagnostics: missing root/link, multiple candidates, cycle, impossible object-stream offset/count, unresolved encrypted candidate, and cap.
- Evidence and provenance: proposed links/indexes cite source objects/spans, strict failures, strict graph/view basis, cards, security context, and search protocol; no derived candidate view is cited.
- Determinism and replay: D0 under exact source/graph/context/cards and semantic budget.
- Falsifiers and Gauntlet: multiple catalog candidates, cyclic/orphan page trees, malformed object-stream headers, encrypted containers, no-source candidate rejection, and ambiguity.
- Surfaces: recovery report/CLI alternatives, page/security materiality checks, OpenReport, and fuzz target.
- Dependencies and consumers: depends on REC.001/REC.002, REV.005/REV.006, DOC.004/DOC.005, and SEC.009 using only the strict snapshot; DOC.010, REC.006, and REC.010 consume results.
- Migration and withdrawal: failed/misleading family is removed/tombstoned; raw source and prior hypotheses remain.
- No-claim boundary: reconstructed links/indexes do not establish producer intent, conformance, visual page order, or writer-ready repair.
- Rationale: structural recovery is useful only when it preserves candidate multiplicity and source-bounded justification.

#### `C1.CC.REC.006@1` — Bounded hypothesis search

- Identity, lifecycle, layer: active C1 L2 orchestration contract; one search explores registered families under a shared non-resettable account.
- Inputs and identity domain: strict result, admitted recovery session, family registry, source/final strict graph/context, generated hypothesis bases and their cost vectors, candidate views and consequence receipts, semantic search limits, and cancellation.
- Preconditions: every family declares assumptions, kill budget, output contract, and materiality projection; no unregistered heuristic executes.
- Card slots: `SC.C1.REC.BOUNDED-SEARCH.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: scan regions, candidates, branches, hypotheses, ordering/comparisons, canonicalization/symmetry work, decoded bytes, and diagnostics are independent dimensions.
- Cancellation: checkpoints between bounded candidate/family units; stopping returns frontier, limits, and retained candidates without a singular promotion.
- Authority and secrets: family work inherits/narrows source/decrypt leases; parallel branches cannot multiply capabilities or budgets.
- Outputs and outcomes: returns generated/rejected bases and finalized hypotheses, candidate-view consequence receipts, each basis/candidate/final-hypothesis `RecoveryHypothesisCostVectorId`, aggregate budget reconciliation without double counting shared work, frontier, fired limits, family coverage, and partial/ambiguous/refused search result.
- Diagnostics: family/candidate cap, canonicalization cap, resource exhaustion, cancellation, dependency/card gap, and internal family fault remain distinct.
- Evidence and provenance: search receipt binds strict report, source/final strict graph, profile, family versions, cards, exact semantic limits, attempts, every cost-attribution receipt, and every retained/rejected basis, candidate view, and finalized hypothesis ID.
- Determinism and replay: D0 under exact semantic limits and deterministic schedule-independent candidate identity; wall deadline firing narrows replay.
- Falsifiers and Gauntlet: branch explosion, sibling budget conservation, direct/shared/unavailable cost reconciliation, retry/worker replacement, cancellation, family failure containment, ordering permutation, and diagnostic floods.
- Surfaces: recovery facade/report, CLI alternatives, trial record, held-out probe, and fuzz harness.
- Dependencies and consumers: depends on REC.001–REC.005, DOC.002, REC.010, and FDN.004–FDN.014; REC.007–REC.009 consume result.
- Migration and withdrawal: search/family registry change versions the protocol; prior attempt distributions are preserved and cannot be selected away.
- No-claim boundary: budget exhaustion cannot be relabeled as a successful singular recovery or exhaustive search.
- Rationale: explicit multi-dimensional caps prevent combinatorial repair from becoming the wedge’s denial-of-service path.

#### `C1.CC.REC.007@1` — Admissibility, partial order, and coalescing

- Identity, lifecycle, layer: active C1 L2 contract; safety gates precede a named partial order, and deterministic tie-breaks apply only after semantic equality.
- Inputs and identity domain: finalized hypotheses, their basis/view/consequence receipts and seven-axis `RecoveryMaterialityProjectionId` records, source support, constraint outcomes, assumption sets/locality, structural/history consistency, compatibility evidence if later lawfully available, and exact equality evidence or explicit unavailable/indeterminate state for effective objects, page order, visible appearance, extracted text, attachment inventory, signature interpretation, and security conclusions.
- Preconditions: each ordering and materiality dimension is registered; no scalar score substitutes for the ordering record; external observations are absent unless committed protocols later admit them. Coalescing requires equality on all seven materiality axes. An unavailable or indeterminate axis blocks coalescing and any non-material-distinction conclusion unless an admitted exact identity proof establishes equality for that axis; C1 performs no appearance or text derivation to manufacture such a proof.
- Card slots: `SC.C1.REC.ORDERING.001`, `SC.C1.REC.MATERIAL-AMBIGUITY.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: pairwise comparisons, nondominance frontier, equivalence/coalescing, symmetry work, materiality projections, and diagnostics are bounded.
- Cancellation: incomplete ordering yields explicit unranked/partial frontier and cannot choose a preferred candidate.
- Authority and secrets: caller preference is excluded from truth ordering; protected candidate artifacts remain classified.
- Outputs and outcomes: admissible/rejected set, nondominated frontier, named dimension records, coalesced equivalence classes with every retained source assumption only after the seven-axis equality gate, and uncoalesced materially distinct or equivalence-unresolved alternatives with per-axis availability.
- Diagnostics: failed safety/source gate, incomparable dimensions, missing evidence, unavailable/indeterminate materiality axis, prohibited coalescing, comparison/canonicalization cap, invalid scalar ranking, and materiality unknown.
- Evidence and provenance: every dominance/coalescing or equivalence-unresolved relation cites both hypotheses, all seven axis results and any exact equality proof, dimensions, evidence, limits, cards, and affected outputs.
- Determinism and replay: D0 under exact hypotheses, ordering protocol, cards, and semantic budget; enumeration order cannot change frontier identity.
- Falsifiers and Gauntlet: Pareto examples, cycles in claimed dominance, equivalent hypotheses with different assumptions retained, unavailable appearance/text axes, different views with equal structural summaries, later appearance/text distinction after C1 retention, material-effect changes, scalar-rank injection, and budget boundaries.
- Surfaces: recovery report/CLI alternatives, task selection, security-across-hypotheses check, and trial record.
- Dependencies and consumers: depends on REC.006/REC.010, FDN.010/FDN.014, and DOC.002/DOC.005/DOC.008/DOC.015/REV.008 materiality inputs; REC.008/REC.009 consume frontier.
- Migration and withdrawal: dimension/order change versions the contract and invalidates old selection claims; old ordering evidence remains historical.
- No-claim boundary: nondominated does not mean correct, most probable, or authorized for writeback; an equivalence-unresolved pair cannot be reported as non-materially-distinct or used to narrow a whole-document security/absence claim.
- Rationale: a partial order preserves genuine tradeoffs and avoids a confidence-like number that hides assumptions, while the closed seven-axis gate prevents C1's missing appearance/text layers from erasing alternatives needed by later cycles.

#### `C1.CC.REC.008@1` — Task-local selection with alternatives retained

- Identity, lifecycle, layer: active C1 L2 contract; selection authorizes one downstream read task while preserving the ambiguous source-level outcome.
- Inputs and identity domain: nondominated frontier, finalized hypothesis and candidate `DocumentViewId` pairs, seven-axis materiality results including unavailable/indeterminate axes and equivalence-unresolved relations, declared task/policy, caller authority, requested coverage, relevant security results, and selection evidence.
- Preconditions: selected candidate is admissible; materially distinct and equivalence-unresolved alternatives plus discriminators are retained; policy cannot override safety, contradictory source evidence, or an unavailable materiality axis.
- Card slots: `SC.C1.REC.TASK-SELECTION.001`, `SC.C1.REC.SECURITY-ACROSS-HYPOTHESES.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: candidate comparison, material/security projections, selection record, alternative retention, diagnostics, and downstream reservation are bounded.
- Cancellation: no selection is published after cancellation; frontier remains intact.
- Authority and secrets: caller can choose for the named task only; choice grants no mutation/write authority and cannot erase protected alternative findings.
- Outputs and outcomes: task-scoped selected `DocumentViewId` plus policy/evidence, or explicit no-selection/ambiguity/refusal; all materially distinct and equivalence-unresolved alternatives remain report-linked with per-axis availability.
- Diagnostics: inadmissible/stale candidate, unsupported task, unresolved material/security difference, unavailable materiality axis, missing authority, and changed frontier.
- Evidence and provenance: receipt binds every candidate, all seven materiality-axis results, task/policy, caller role, discriminators, security conclusions, and exact selected view.
- Determinism and replay: policy-deterministic D0 when all inputs are exact; caller choice is an attestation, not source truth.
- Falsifiers and Gauntlet: selection erasure attempts, stale frontier, unavailable appearance/text axes, attachment/action/signature difference across alternatives, wider downstream claim, and retry consistency.
- Surfaces: recovery facade, CLI explicit selection, Open/Recovery reports, and downstream object inspection.
- Dependencies and consumers: depends on REC.007/REC.010, DOC.002, DOC.008, REV.008, and FDN.010; REC.009 and recovery-report enrichment consume it.
- Migration and withdrawal: changed policy/frontier creates a new selection receipt; prior selection never becomes unqualified source history.
- No-claim boundary: whole-document security/absence claims must hold across every live materially distinct or equivalence-unresolved hypothesis; one task selection cannot supply them.
- Rationale: task-local selection enables useful work while preserving the epistemic fact that malformed bytes admit alternatives.

#### `C1.CC.REC.009@1` — Recovery report and writeback separation

- Identity, lifecycle, layer: active C1 L2/report-boundary contract; recovery produces analysis artifacts only and exposes no output writer.
- Inputs and identity domain: strict report, basis set, candidate-view consequence receipts, finalized hypotheses, search result, frontier, task selections, affected regions/objects/pages/security findings, and limits.
- Preconditions: every hypothesis/selection has a stable ID and source/graph binding; report schema is active.
- Card slots: `SC.C1.REC.REPORT-WRITEBACK-BOUNDARY.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: alternatives, affected locations, evidence, diagnostics, retained candidate metadata, and serialized report bytes are bounded.
- Cancellation: report finalization after search cancellation records exact frontier/coverage; no repaired bytes are emitted.
- Authority and secrets: report respects source/plaintext sensitivity; write/transform capabilities are absent.
- Outputs and outcomes: immutable `RecoveryReport` input record and candidate views for inspection; any future repair request is a separate later-cycle transformation.
- Diagnostics: missing hypothesis evidence, stale graph/view, report truncation, protected artifact unavailable, and attempted writeback route.
- Evidence and provenance: binds strict result, source/graph, every hypothesis/selection, cards, budgets, run observation link, and no-claims.
- Determinism and replay: semantic report is D0 for exact inputs; host timing and candidate materialization observations stay separate.
- Falsifiers and Gauntlet: attempted source mutation, report alternative omission, truncated diagnostic coverage, stale candidate, secret leakage, and schema drift.
- Surfaces: RecoveryReport, RPT.007 link to the immutable base OpenReport, CLI output, trial record, and checker.
- Dependencies and consumers: depends on REC.001–REC.008/REC.010; RPT.002/RPT.007 plus C1 workflows and the gate consume its immutable recovery record.
- Migration and withdrawal: later repair-write contract is distinct; this analysis contract is never widened into publication.
- No-claim boundary: producing a recovery report does not repair, normalize, serialize, or change the original source.
- Rationale: a hard writeback boundary prevents an inspection wedge from presenting a guessed rewrite as harmless analysis.

#### `C1.CC.REC.010@1` — Candidate-view consequence finalization

- Identity, lifecycle, layer: active C1 L2 contract; it finalizes a `RecoveryHypothesisId` only after a hypothesis basis has produced an independently identified candidate `DocumentViewId`.
- Inputs and identity domain: one `RecoveryHypothesisBasisId`, its initial `RecoveryHypothesisCostVectorId`, candidate view from DOC.002, candidate-view mapping/coverage, satisfied and violated constraints, structural/history/security consequences, per-axis value/evidence or explicit unavailable/indeterminate state for effective objects, page order, visible appearance, extracted text, attachment inventory, signature interpretation, and security conclusions, consequence-pass cost attribution, cards, and limits.
- Preconditions: basis and candidate view share the exact source, strict parent graph, recovery profile, and view-basis lineage; candidate construction did not consume a finalized hypothesis; every required consequence check and every one of the seven materiality axes has a typed result or explicit unavailable/indeterminate state. C1 records visible-appearance and extracted-text axes as unavailable unless an admitted exact identity proof establishes equality without executing either deferred layer.
- Card slots: `SC.C1.REC.CANDIDATE-CONSEQUENCE.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: candidate values, constraint checks, affected objects/pages, security/materiality projections, evidence records, canonicalization, and diagnostics are bounded.
- Cancellation: an interrupted consequence pass emits only a partial receipt and cannot mint a finalized hypothesis or admissible candidate.
- Authority and secrets: consequence checks inherit narrowed read/decrypt leases from the admitted session; they cannot mutate bytes, widen credentials, or turn caller preference into evidence.
- Outputs and outcomes: immutable `RecoveryConsequenceReceiptId`, one `RecoveryMaterialityProjectionId` carrying the closed seven-axis values/evidence/availability, and, only when every mandatory check has a typed outcome, `RecoveryHypothesisId` binding basis, candidate view, constraints, affected scope, ordering dimensions, material consequences, and reconciled `RecoveryHypothesisCostVectorId` with direct/shared/unavailable attribution.
- Diagnostics: source/basis/view mismatch, missing consequence or materiality axis, violated hard constraint, missing/inconsistent cost attribution, shared-cost double count, security unknown, materiality unavailable/indeterminate, card gap, stale view, budget exhaustion, and cancellation.
- Evidence and provenance: receipt binds strict result, final strict graph, basis, view-basis lineage, candidate view, every check/result, the seven-axis projection and any exact equality proof, cards, profile, limits, and availability; it never rewrites raw basis evidence.
- Determinism and replay: D0 under exact basis/view/check protocols/cards/semantic limits; evaluation order cannot change the receipt or finalized-hypothesis identity.
- Falsifiers and Gauntlet: view-before-basis inversion, basis/view source mismatch, missing constraint or materiality axis promoted to pass/equality, altered candidate after check, unavailable appearance/text hidden, security-laundering, affected-scope/cost omission, shared-cost double count, cost-to-confidence laundering, permutation, and cancellation.
- Surfaces: recovery search/order/selection, recovery report enrichment, CLI alternatives, held-out probe, and fuzz target.
- Dependencies and consumers: depends on REC.001–REC.005, DOC.002, DOC.008, DOC.012–DOC.015, REV.008/REV.009, and FDN.001–FDN.015; REC.006–REC.009 and RPT.002/RPT.007 consume it.
- Migration and withdrawal: consequence protocol or hypothesis identity change versions the receipt/hypothesis; old receipts remain scoped and cannot silently validate rebuilt views.
- No-claim boundary: finalization records consequences and availability for one explicit candidate; it does not establish cross-candidate equality on an unavailable axis, source conformance, singular recovery, exhaustive search, or write authority.
- Rationale: two-stage identity preserves raw recovery assumptions while allowing candidate-derived consequences to be checked without a dependency cycle.

### 8.9 Report contracts

#### `C1.CC.RPT.001@1` — `OpenReport` semantic body

- Identity, lifecycle, layer: active C1 L2/L8 report contract; the semantic body is an immutable derived artifact with one schema/version/root.
- Inputs and identity domain: exact `SourceRootId`, source identity/availability, every produced base/final strict revision graph plus discovery protocol/version and supersession relation, strict `DocumentViewId` or strict ambiguity, DOC.009 strict result and `OccurrenceVisibilityMapId`, DOC.005 page-attribute/geometry/continuity inventory, strict RPT.003 security inventory, RPT.010 C1 validation report, DOC.012 encrypted-wrapper inventory, DOC.013 UTF-8-string inventory, DOC.014 `NeedsRendering` inventory, DOC.015 metadata inventory, limits, diagnostics, and active operation capabilities; no recovery hypothesis, candidate view, or recovery-derived finding is an input.
- Preconditions: all referenced strict artifacts exist and are root/graph/view consistent; missing decision-critical artifacts carry explicit availability; recovery has not enriched this immutable body.
- Card slots: `SC.C1.RPT.OPEN-REPORT.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: graph/view references, findings, diagnostics, interval summaries, capability records, no-claims, canonicalization, and serialized bytes are bounded.
- Cancellation: a report may describe a cancelled operation only with exact observed coverage, terminal state, and private/public artifact status.
- Authority and secrets: passwords, keys, plaintext, protected source snippets, and confidential unsalted digests are excluded or protected by policy.
- Outputs and outcomes: base `OpenReportId` records source class/ranges; every produced base/final strict graph identity, discovery protocol/version, observed-range coverage, limits/assumptions, and supersession relation; strict selection or ambiguity; strict status; `recovery_status_at_strict_finalization` (`not requested`, `separately requested but not yet linked`, or `unknown/unavailable`, never a recovery result); every visible/shadowed/unreachable/unknown occurrence classification and frontier; page structural/geometry/continuity evidence; encryption; structural signatures; the bounded DOC.012–DOC.015 inventories and RPT.010 validation layers or their explicit unavailability; unexplained bytes, resource use, and no-claims.
- Diagnostics: schema construction rejects missing mandated identities, inconsistent root/graph/view, contradictory coverage, absent terminal state, and unsafe disclosure.
- Evidence and provenance: every finding links typed source/virtual/object/graph/view locations, evidence facets, cards/contracts, and availability.
- Determinism and replay: the strict semantic body targets D0; recovery enrichment and run observations are linked only through RPT.007 and RPT.004 and excluded from its root.
- Falsifiers and Gauntlet: mandated-field omission, omitted base/final graph or supersession relation, graph/view mismatch, recovery-derived data inserted into the strict root, missing/absence recovery-status confusion, partial-as-all-scope, diagnostic truncation, secret leak, unknown fields, and producer/checker canonical-root tests.
- Surfaces: Rust report API, CLI inspect JSON/JSONL/human rendering, evidence package, capability manifest, and close gate.
- Dependencies and consumers: depends on BYT.001–BYT.006, REV.001–REV.009, DOC.001–DOC.015, SEC.001–SEC.009, RPT.003/RPT.010, and FDN.001–FDN.015 outputs in strict mode; REC.002, RPT.004/RPT.005/RPT.007/RPT.009, IMM.004, and IMM.016 consume it.
- Migration and withdrawal: schema change follows FDN.015; older report roots remain immutable and claim rows may lapse without deletion.
- No-claim boundary: the base report covers only executed strict contracts, observed ranges, strict selections/ambiguities, credentials, cards, and budgets; its finalization-time recovery status cannot prove no later alternatives exist, and every recovery artifact or later link remains separate through RPT.007.
- Rationale: binding every root/graph/view identity closes the schema drift identified by audit row R1-1.

#### `C1.CC.RPT.002@1` — `RecoveryReport` semantic body

- Identity, lifecycle, layer: active C1 L2/L8 report contract; it preserves search alternatives and strict/recovery separation.
- Inputs and identity domain: source root, final strict revision graph, strict result/base report reference, recovery profile/search receipt, each hypothesis basis, candidate-view consequence receipt, finalized hypothesis and candidate view, every `RecoveryHypothesisCostVectorId` and attribution receipt, frontier/order records, task selection, affected scope, and no-claims.
- Preconditions: bases, views, receipts, and finalized hypotheses are stable and source/strict-graph-bound; report never substitutes one selected candidate for the frontier.
- Card slots: `SC.C1.RPT.RECOVERY-REPORT.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: hypotheses, alternatives, discriminators, affected locations, assumption/evidence records, diagnostics, and serialized bytes are bounded.
- Cancellation: search cancellation produces exact frontier, fired limit, and coverage; report finalization cannot hide unvisited candidates.
- Authority and secrets: protected candidate/plaintext artifacts use availability references; caller selection is recorded as scoped attestation.
- Outputs and outcomes: records each basis/candidate-view/finalized-hypothesis chain, proposed repairs, satisfied/violated constraints, per-hypothesis direct/shared/unavailable cost vector with aggregate reconciliation, ordering/nondominance, selection or no selection, material alternatives, budgets, and affected objects/pages/security findings.
- Diagnostics: missing alternative, inconsistent frontier, unbound view, hidden assumption, contradictory coverage, unsafe disclosure, and truncation.
- Evidence and provenance: each report element links basis/view/consequence/hypothesis/search/strict IDs, exact locations, cards/contracts, evidence, and artifact availability.
- Determinism and replay: semantic body is D0 for exact search result/protocol/limits; wall observations remain separate.
- Falsifiers and Gauntlet: alternative omission, order permutation, coalescing loss, stale selection, security difference hidden, cancellation, schema ambiguity, and checker tests.
- Surfaces: Rust recovery API, CLI recovery output, OpenReport link, evidence package, held-out probe, and trial record.
- Dependencies and consumers: depends on REC.001–REC.010 and FDN.001–FDN.015; RPT.004/RPT.005/RPT.007, IMM.004, and IMM.016 consume it.
- Migration and withdrawal: schema/order changes version reports and may lapse old selection claims; historical search distributions remain.
- No-claim boundary: report publication does not repair or write the source and does not make a selected hypothesis source truth.
- Rationale: alternatives, ordering dimensions, and affected scope make recovery evidence useful without epistemic laundering.

#### `C1.CC.RPT.003@1` — Structural security inventory report

- Identity, lifecycle, layer: active C1 L2/L8 component-report contract; it composes encryption, structural signature, inert carrier, and plaintext-availability findings.
- Inputs and identity domain: exact strict view/final strict graph, SEC.001 inventory including raw `/P` and `/Perms`, SEC.004 typed `/Perms` validation outcome, REV.008 ranges, DOC.008 carriers, DOC.012 encrypted-wrapper inventory, credential/decryption statuses, strict result, and coverage; no recovery hypothesis is an input.
- Preconditions: each component uses active cards/contracts; conclusions remain bounded to the strict view and observed coverage, with ambiguity or unavailability explicit.
- Card slots: `SC.C1.RPT.SECURITY-INVENTORY.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: findings, objects/revisions/ranges, payload summaries, diagnostics, and serialized bytes are bounded.
- Cancellation: report exposes scanned strict coverage and never asserts absence after truncation or unvisited strict regions.
- Authority and secrets: no key/password/plaintext or protected payload content is emitted; cryptographic/trust/authorization providers are absent.
- Outputs and outcomes: strict encryption declarations/scope including raw `/EncryptMetadata`, public-key carriers, and core-versus-technical-specification profile class; credentialed availability; raw `/P` observation and separate `/Perms` valid/invalid/not-applicable/unsupported/unavailable outcome; declared permissions, host-application policy, and actual data recoverability over only the content successfully decoded within exact coverage as four distinct fields; signature family/seed/lock carriers and ranges; recognized/unknown/opaque security carriers; the bounded encrypted-payload/unencrypted-wrapper structural inventory or explicit unavailability; strict ambiguity; and exact no-claims.
- Diagnostics: unsupported handler/carrier, encrypted-unavailable value, malformed range, opaque/nested payload, strict ambiguity, and coverage/diagnostic truncation.
- Evidence and provenance: every finding binds view/graph/revision/object/span, cards/contracts, decryption context identity, and coverage.
- Determinism and replay: D0 under exact strict view/graph/cards/capabilities and semantic limits.
- Falsifiers and Gauntlet: encrypted/unencrypted carrier and wrapper/payload combinations, `/EncryptMetadata`, public-key and technical-specification carrier inventory without decryption, distinct `/P` and `/Perms` mutations/outcomes, recoverable/unavailable content distinct from permissions and host policy, shadowed signatures/actions within the strict view, partial source, unknown carriers, truncation, and secret scans.
- Surfaces: OpenReport component, CLI inspect/objects/revisions, evidence package, and C1 close gate.
- Dependencies and consumers: depends on SEC.001–SEC.009, REV.008/REV.009, DOC.008, DOC.012, and DOC.009; RPT.001/RPT.007 and IMM.016 consume it.
- Migration and withdrawal: later cryptographic validation/sanitization reports receive separate IDs; this structural report cannot be widened by prose.
- No-claim boundary: it does not assert signature validity/trust, absence of semantic secrets, sanitized output, payload safety, or permission enforcement; recoverability says only what the executed bounded path actually decoded.
- Rationale: one component makes the R0 “security inventory” gate precise while retaining structural-only limits.

#### `C1.CC.RPT.004@1` — Semantic report versus run observation envelope

- Identity, lifecycle, layer: active C1 L0/L8 contract; semantic results and operational observations have linked but distinct schema identities.
- Inputs and identity domain: strict, recovery, security, validation, replay, or recovery-enrichment semantic report root/body, host timestamps, wall time, scheduler events, memory high-water observations, process/machine facts, and trace mode.
- Preconditions: every observation field is classified as semantic input, semantic output, or run-only data; no ambiguous field participates in both.
- Card slots: `SC.C1.RPT.SEMANTIC-RUN-SEPARATION.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: event count, observation bytes, sampling, trace overhead, redaction, diagnostics, and retention are bounded.
- Cancellation: run envelope records request/observation timing and checkpoint; semantic body retains its own canonical terminal outcome.
- Authority and secrets: telemetry export is explicit host authority; ordinary envelope excludes source, plaintext, credentials, protected paths, and low-entropy public commitments.
- Outputs and outcomes: semantic report ID plus separate run-observation ID, capture level, observer effects, missing observations, and disclosure status.
- Diagnostics: semantic/run contamination, unsupported observation, clock/machine fact unavailable, trace truncation, protected field, and export refusal.
- Evidence and provenance: link binds the exact semantic body, operation/run identity, host observation source, trace mode, and retention policy.
- Determinism and replay: run observations never poison D0 semantic roots; they support only separately scoped operational evidence.
- Falsifiers and Gauntlet: timestamps/order/process IDs varied over same semantic result, observer failure, trace truncation, secret taint, and schema migration.
- Surfaces: Open/Recovery/security/Validation reports, `ExecutionReplayBundle`, trial records, fuzz witnesses, CLI metadata, and evidence package.
- Dependencies and consumers: depends on FDN.008/FDN.009/FDN.012/FDN.015 and RPT.001–RPT.003/RPT.007/RPT.010; RPT.009, IMM.016, and the close gate consume it.
- Migration and withdrawal: observation schema may evolve independently; a measurement artifact, if later admitted, receives its own protocol rather than changing semantic identity.
- No-claim boundary: run telemetry is not a performance comparison, correctness proof, or deterministic semantic input unless a later scoped protocol explicitly says so.
- Rationale: separating the envelopes preserves stable report identity without discarding useful operational evidence.

#### `C1.CC.RPT.005@1` — JSON/JSONL/human schema projections

- Identity, lifecycle, layer: active C1 L8 projection contract; machine encodings are authoritative generated views and human text is a rendering of the same schemas.
- Inputs and identity domain: validated strict/recovery/security/validation/replay/enrichment report or registry object, target projection/version, disclosure policy, output sink with declared `Buffered`, `AtomicVisibility`, or `DurableCommit` class, and limits.
- Preconditions: source object passed its schema constructor; projection is generated from the normative registry; unknown-critical fields follow schema law.
- Card slots: `SC.C1.RPT.PROJECTIONS.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: serialized bytes, nesting, records/lines, formatting work, diagnostics, and output transaction are bounded.
- Cancellation: output stays private until the selected sink’s terminal contract; JSONL prefix, if deliberately streamed, carries explicit partial-stream framing and terminal record.
- Authority and secrets: field-level disclosure/redaction is schema-driven; human rendering cannot reveal data hidden from machine projection.
- Outputs and outcomes: versioned JSON, JSONL event stream, or human view plus schema/root metadata, declared sink class, visibility and durability state, and truncation/terminal state; a post-visibility failure is committed or indeterminate rather than fictional rollback.
- Diagnostics: unrepresentable value, schema mismatch, redaction failure, output limit, sink failure, and projection drift use stable codes.
- Evidence and provenance: projection receipt binds source semantic ID, projection version, disclosure policy, sink class/host guarantees, output identity, visibility/durability observation, and losses/redactions.
- Determinism and replay: canonical JSON form is D0 where declared; human formatting is deterministic for a pinned renderer but not an identity substitute.
- Falsifiers and Gauntlet: round trips, field omission, unknown fields, line truncation, Unicode/byte distinction, secret redaction, each sink class, post-visibility fault, indeterminate durability, and schema examples.
- Surfaces: CLI stdout/stderr, saved reports, evidence package inputs, tests, documentation examples, and checker fixtures.
- Dependencies and consumers: depends on FDN.002/FDN.008/FDN.015 and RPT.001–RPT.004/RPT.007; CLI, RPT.008, and IMM.004/IMM.016 consume it.
- Migration and withdrawal: projection change versions output schema; examples are regenerated and validator-checked, never hand-patched.
- No-claim boundary: readable formatting cannot strengthen the underlying report or fill missing identities/coverage.
- Rationale: one schema source eliminates drift between machine output, human output, examples, and documentation.

#### `C1.CC.RPT.006@1` — Capability manifest

- Identity, lifecycle, layer: active C1 L8 report contract; every entry references exact consequence-contract/card/profile versions rather than friendly feature labels alone.
- Inputs and identity domain: active contract registry, card coverage, build/toolchain/dependency identities, enabled profiles/features, surface projections, and no-claim/lifecycle state.
- Preconditions: the contract/card/claim/schema inputs are structurally generated and all proposed/active/withdrawn distinctions are explicit. The candidate manifest is not gate-admissible until the downstream IMM truth checks and blocking drift audit pass for that exact root.
- Card slots: `SC.C1.RPT.CAPABILITY-MANIFEST.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: entries, cross-links, dependency records, schema/card coverage, canonicalization, diagnostics, and output bytes are bounded.
- Cancellation: manifest generation is transactional; a stale/partial manifest is not published as current.
- Authority and secrets: manifest contains no secret/provider material beyond disclosure-approved immutable capability identities.
- Outputs and outcomes: each row reports source types, dialect/read profiles, filters, decryption profiles with core-versus-unverified/pending technical-specification classification, reports, CLI surfaces, determinism, Gauntlet tiers actually passed, corpus identity/coverage and unavailable partitions, known refusals/no-claims, and decision-blocked capabilities.
- Diagnostics: orphan contract, surface mismatch, inactive/missing card, unknown dependency, decision not ratified, schema drift, and lifecycle contradiction.
- Evidence and provenance: candidate manifest binds exact build/toolchain, registry roots, card-coverage root, dependency manifest, generator, and its own construction receipt; no downstream audit result is an input or member of this root.
- Determinism and replay: D0 for the same generated inputs/build identity; runtime observations do not alter declared capability.
- Falsifiers and Gauntlet: missing codec/algorithm, core/technical-specification collapse, missing or fabricated passed-tier/corpus coverage, disabled feature still advertised, friendly-name alias, surface widening, withdrawn contract, and generator drift.
- Surfaces: Rust discovery API, CLI capability/schema command, OpenReport link, RPT.008 admission-envelope input, docs generation, and checker.
- Dependencies and consumers: depends on IMM.001–IMM.005, FDN.015, and the exact contract-registry snapshot; IMM.006/IMM.008–IMM.010/IMM.012 and RPT.008 consume the candidate manifest. The manifest entry describing this contract comes from the static registry declaration and does not recursively include the generated manifest root.
- Migration and withdrawal: contract/card/build change regenerates a new manifest root; old manifests remain dated artifact evidence.
- No-claim boundary: the manifest states candidate-declared support boundaries; it is not an admission result and does not prove that any implementation gate passed.
- Rationale: callers should discover absence or policy blocks before processing, not through a late crash.

#### `C1.CC.RPT.007@1` — Recovery/security enrichment envelope

- Identity, lifecycle, layer: active C1 L2/L8 composition contract; it links immutable strict reports to recovery-only findings without modifying the base `OpenReportId` or strict RPT.003 root.
- Inputs and identity domain: RPT.001 base report, RPT.002 recovery report, RPT.003 strict security inventory, REC.009 analysis record, all live candidate-view consequence receipts/selections, DOC.012–DOC.015 candidate inventories or explicit unavailability, cross-hypothesis security/materiality results, schema, and limits.
- Preconditions: all inputs share one source and strict parent graph; the strict report roots are retained unchanged; every live recovery alternative is represented or explicitly unavailable.
- Card slots: `SC.C1.RPT.RECOVERY-SECURITY-ENRICHMENT.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: links, alternatives, affected objects/pages/ranges, cross-hypothesis findings, availability records, diagnostics, canonicalization, and serialized bytes are bounded.
- Cancellation: partial enrichment states exact processed alternatives/coverage and cannot replace or narrow the underlying strict or recovery reports.
- Authority and secrets: envelope adds no source/decrypt/write authority; protected candidate or plaintext evidence remains availability-referenced under the strict disclosure policy.
- Outputs and outcomes: immutable `RecoverySecurityEnrichmentId` linking base report, recovery report, strict inventory, candidate-specific findings, across-alternative conclusions, affected scope, explicit ambiguity, and no-claims; it supplies the later recovery-session status and exact enrichment root for projections of the base report. An unavailable link stays unknown and is never evidence that no alternatives exist.
- Diagnostics: source/graph mismatch, omitted live alternative, stale selection, missing consequence receipt, security/materiality unknown, unsafe disclosure, schema gap, and truncation.
- Evidence and provenance: every added finding binds its basis/view/consequence/hypothesis IDs, strict parent roots, cards/contracts, locations, coverage, and availability; base report bytes are not rewritten.
- Determinism and replay: semantic envelope is D0 for exact input roots/protocol/cards/semantic limits; host observations stay in RPT.004.
- Falsifiers and Gauntlet: base-root mutation, recovery result inserted into strict body, alternative omission, candidate-specific security generalized to all, stale selection, partial-as-full coverage, and checker disagreement.
- Surfaces: recovery-aware inspect output, CLI recovery, evidence package, held-out probe, trial record, and close gate.
- Dependencies and consumers: depends on RPT.001–RPT.003, REC.001–REC.010, DOC.008, DOC.012–DOC.015, and FDN.001–FDN.015; RPT.004/RPT.005/RPT.009, IMM.004/IMM.016, and the close gate consume it.
- Migration and withdrawal: enrichment schema or recovery-root change creates a new envelope; strict roots remain stable and prior envelopes remain scoped historical artifacts.
- No-claim boundary: enrichment does not make a recovery candidate source truth, establish whole-document security, repair bytes, or widen the strict result.
- Rationale: a separate envelope preserves strict-first report identity while making recovery-specific security consequences visible.

#### `C1.CC.RPT.008@1` — Capability-admission envelope

- Identity, lifecycle, layer: active C1 L7/L8 gate-composition contract; it binds one immutable candidate capability manifest to independently produced drift, panic, assurance-lane, and checker-lineage results without inserting them into the candidate root.
- Inputs and identity domain: exact RPT.006 candidate manifest root, exact IMM.012 `DriftAuditResultId`, exact FUZ.011 reachable-panic result, FUZ.015 `AssuranceLaneAggregateId`, IMM.020 `CheckerLineageAssessmentId`, checked contract/card/claim/schema/surface/build roots, audit/assurance policy versions, lifecycle state, and availability.
- Preconditions: candidate manifest was finalized before audit or assurance; every later receipt binds that unchanged candidate/build and its mandatory scope; no unresolved blocking, missing, cancelled, stale, failed, or indeterminate result is hidden or relabeled.
- Card slots: `SC.C1.RPT.CAPABILITY-ADMISSION.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: manifest rows, audit findings, cross-links, lifecycle states, canonicalization, diagnostics, and projection bytes are bounded.
- Cancellation: interrupted composition yields no admitted envelope; the candidate manifest and partial audit remain separate non-admitted artifacts.
- Authority and secrets: admission has no authority to activate missing cards, ratify decisions, select providers, or reveal protected evidence; it only reflects recorded inputs.
- Outputs and outcomes: immutable `CapabilityAdmissionEnvelopeId` with manifest root, drift/panic/lane/checker roots, exact admitted/blocked/indeterminate status, row-level dispositions including passed Gauntlet/corpus evidence, decision blocks, missing-lane state, and availability.
- Diagnostics: root mismatch, audit-before-manifest, missing truth check, unresolved blocking finding, stale build/registry, lifecycle contradiction, unavailable evidence, and projection failure.
- Evidence and provenance: envelope binds the preexisting candidate manifest, every later audit/assurance/lineage receipt, their protocols, all checked roots, composer identity, and construction receipt; no later result claims membership in or provenance from the candidate manifest root.
- Determinism and replay: D0 for exact manifest/audit/policy inputs; new build, registry, card, surface, or audit result requires a new envelope.
- Falsifiers and Gauntlet: self-audited manifest root, audit/assurance-result injection into candidate manifest, stale-root substitution, missing/cancelled/indeterminate lane treated as pass, omitted panic or checker miss, blocked-row advertisement, lifecycle drift, and cancellation.
- Surfaces: Rust discovery response, CLI capability/schema output, evidence package, product gate, cycle-close gate, and trial record.
- Dependencies and consumers: depends on RPT.005/RPT.006, IMM.012/IMM.020, FUZ.011/FUZ.015, and FDN.015; CLI.008, IMM.016/IMM.019, and the product/close gates consume it.
- Migration and withdrawal: any manifest/audit/policy input change creates a new envelope and withdraws superseded admission status without deleting historical roots.
- No-claim boundary: the envelope reports gate state for one exact candidate and exact audit/assurance scope; it does not self-prove implementation behavior, infer unexecuted lanes, or ratify pending decisions.
- Rationale: binding an earlier candidate root to later independent gate receipts removes the manifest/auditor cycle while preventing a passable-looking admission object from omitting whether assurance ran.

#### `C1.CC.RPT.009@1` — `ExecutionReplayBundle`

- Identity, lifecycle, layer: active C1 L7/L8 atomic replay-evidence contract; one immutable bundle describes one triggering anomaly and only the replay relation supported by its determinism class and capture state.
- Inputs and identity domain: triggering crash, refusal, divergence, or selected operational anomaly; exact applicable `SourceRootId`, `RevisionGraphId`, `DocumentViewId`, `DraftIntentCommitment`, `RealityStateCommitment`, and `ExpectedStateId`; artifact availability classes; semantic report identity separate from RPT.004 host-run observations; comparator/tolerance/equivalence inputs; semantic limits/fired limit/seed/capabilities; and exact build, dependency, profile, algorithm, target, and device identities.
- Preconditions: every applicable proper-domain identity and availability class is explicit; capture mode and determinism class authorize the stated relation; comparator, tolerance or error metric, expected equivalence class, and acceptance scope are named when comparison is meaningful; missing protected or external state is never reconstructed.
- Card slots: `SC.C1.RPT.EXECUTION-REPLAY.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: referenced artifacts, trace events, capture bytes, replay attempts, comparator work, diagnostics, redaction, retention, and serialized bundle bytes are bounded.
- Cancellation: cancelled capture or replay records the exact checkpoint, missing state, and artifact availability; it cannot emit a stronger replay relation or acceptance result.
- Authority and secrets: a bundle is never emitted through ambient networking; export is a caller-authorized host action; sensitivity, retention, redaction, and export authorization are explicit, and secrets or protected artifacts may remain unavailable.
- Outputs and outcomes: immutable `ExecutionReplayBundleId` containing trigger; proper-domain identities and availability; distinct semantic-report and host-observation roots; determinism class and exact permitted replay relation; comparator, tolerance/error metric, expected equivalence class, and acceptance scope where applicable; limits/fired limit/seed/capabilities; build/dependency/profile/algorithm/target/device identities; trace level and observer effects; disclosure controls; crash-capture completeness; missing secret/remote/host/external-tool state; and replay/refusal outcome.
- Diagnostics: missing applicable identity, semantic/run contamination, unsupported replay relation, comparator or acceptance scope absent, partial crash capture, stale build/profile/capability, protected export refusal, unavailable external state, fired limit, trace truncation, and bundle canonicalization failure.
- Evidence and provenance: the bundle binds the exact triggering record, semantic report, separately captured host observations, input/artifact availability, capture/replay protocol, capabilities, limits, environment identities, comparator configuration, disclosure decision, and construction receipt.
- Determinism and replay: the declared class and capture mode govern exactly; D3, D4, D5, wall-clock-stopped, partial-capture, or mutable-external-service runs receive only their supported relation and never a universal bit-identical promise.
- Falsifiers and Gauntlet: swap any domain/build/profile/capability identity, merge semantic and host observations, omit fired limits or missing state, overstate partial capture, vary comparator/tolerance, forge availability, attempt ambient export, redact inconsistently, replay with unavailable secrets, cancel, and truncate trace or bundle.
- Surfaces: report API, CLI diagnostic/replay reference, RPT.004 observation link, minimized fuzz witness, evidence package, sealed trial, and close-gate evidence.
- Dependencies and consumers: depends on FDN.008/FDN.009/FDN.012/FDN.015, RPT.001–RPT.004/RPT.007/RPT.010, and the exact triggering artifact contract; RPT.004 projections, FUZ.009, IMM.004/IMM.016, CLI.005, and the close gate consume its schema or identity.
- Migration and withdrawal: replay schema, capture protocol, determinism relation, comparator, or environment-identity change versions the bundle; superseded bundles remain immutable and scoped to their original evidence.
- No-claim boundary: a replay bundle does not prove correctness, conformance, causal uniqueness, anomaly absence, secret recoverability, external-state preservation, or a replay relation stronger than the recorded class and capture permit.
- Rationale: an atomic bundle makes reproduction limits inspectable without laundering host observations into semantic identity or inventing unavailable state.

#### `C1.CC.RPT.010@1` — C1 `ValidationReport`

- Identity, lifecycle, layer: active C1 L2/L8 validation-report contract; it records three separate validation layers for one exact view/history domain without collapsing their outcomes.
- Inputs and identity domain: exact `DocumentViewId`, source-backed `RevisionGraphId`, active profile and profile version, active rule-set identity/version, DOC.007 per-rule results for structural consistency, declared-constraint consistency, and independently sourced model checks, DOC.009 strict coverage, rule locations, and artifact availability.
- Preconditions: the view/graph/profile/rule set are immutable and mutually bound; every normative rule is backed by an active reviewed card; each layer executes and reports separately; an unrun or unsupported rule cannot pass.
- Card slots: `SC.C1.RPT.VALIDATION-REPORT.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: rules, layers, findings, source/virtual/object/semantic/global locations, coverage intervals, diagnostics, canonicalization, and serialized report bytes are bounded.
- Cancellation: interrupted validation preserves exact per-layer/per-rule coverage and terminal state; unvisited rules become `NotEvaluated` or `Indeterminate`, never `Pass`.
- Authority and secrets: validation is read-only and card/profile bounded; protected locations or evidence are redacted by policy, no external validator is invoked in C1, and no ambient I/O is authorized.
- Outputs and outcomes: immutable `ValidationReportId` with exact view/graph/profile/profile-version/rule-set identities; separate layer 1–3 summaries; canonical per-rule `Pass`, `Fail`, `NotApplicable`, `NotEvaluated`, `Unsupported`, or `Indeterminate`; separate severity and coverage; typed source, virtual-span, object, semantic, or global locations; explicit C1 external-comparison status `unavailable/not run`; unsupported rule classes; limits; diagnostics; and availability.
- Diagnostics: identity mismatch, inactive/pending card, unknown rule, duplicate outcome, layer collapse, illegal outcome transition, missing severity/coverage/location, unsupported class, cancellation, disclosure refusal, and canonicalization failure.
- Evidence and provenance: every result binds view/graph/profile/rule-set/layer/rule/card identities, per-rule algebra, input evidence and typed locations, exact observed coverage, producer/build, availability, and construction receipt.
- Determinism and replay: semantic validation report is D0 under exact view/graph/profile/rules/cards/limits; RPT.004 keeps host observations separate and RPT.009 records any admitted replay relation.
- Falsifiers and Gauntlet: layer pass inferred from another layer, aggregate pass with failed/unrun rule, non-transitive pass laundering, profile or rule-set swap, stale view/graph, card withdrawal, partial-as-whole coverage, missing unsupported class, invented external comparison, cancellation, and checker disagreement.
- Surfaces: OpenReport component, validation report API/schema, CLI inspect projection, evidence package, capability manifest, held-out probe, and close-gate evidence.
- Dependencies and consumers: depends on DOC.007/DOC.009 and FDN.001/FDN.008/FDN.009/FDN.012/FDN.015; RPT.001/RPT.004/RPT.005/RPT.009, IMM.004/IMM.016, FUZ.009, and the product/close gates consume it.
- Migration and withdrawal: profile, rule-set, per-rule algebra, location schema, or layer-definition change versions the report; withdrawn cards lapse affected results without deleting historical reports.
- No-claim boundary: a layer or rule pass does not imply another layer, whole-document conformance, renderer behavior, external-validator agreement, source safety, repair authority, or any unexecuted rule outcome.
- Rationale: a typed report preserves non-transitive validation evidence while making profile, rules, coverage, unsupported classes, and C1 comparison absence machine-checkable.

### 8.10 Immune-system contracts

#### `C1.CC.IMM.001@1` — SpecCard/clause-tagging runtime projection and coverage registry

- Identity, lifecycle, layer: active C1 L7 runtime-metadata projection contract; it projects a pre-C1 human/source-pipeline authority snapshot and never creates, approves, or supersedes card authority.
- Inputs and identity domain: immutable pre-C1 `ReviewedCardAuthoritySnapshotId`/`CardAuthoritySnapshotId`, immutable `CardLinkResolutionManifestId`, all 157 stable local link IDs, owning capability/contracts, source class, edition/clause/table/algorithm tag fields, rights status, reviewer roles, lifecycle, and coverage links. Every unreviewed source-location field remains `PENDING-LICENSED-SOURCE`; no tag is guessed.
- Preconditions: the authority snapshot and resolution manifest predate implementation admission; the snapshot records licensed access, AI-use rights, project paraphrase, and two-person meaning review for every active card, while the manifest binds every local link to one reviewed-card branch or explicit human-reviewed project-law disposition. Absent, pending, ambiguous, or unreviewed authority stays blocked. G3 supplies slots only and supplies no semantic body.
- Card slots: `SC.C1.IMM.CARD-REGISTRY.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: slots, links, review records, rights fields, coverage checks, diagnostics, and generated outputs are bounded.
- Cancellation: registry update is transactional; partial extraction/review cannot mark a slot active.
- Authority and secrets: only authorized standards/rights reviewers may create the pre-C1 snapshot, and only the authorized pre-C1 human/source pipeline may author the resolution manifest and its project-law dispositions; this projection can reject or narrow either input but cannot mutate them or populate/approve bodies. Implementation agents receive only the approved projection, never restricted raw text.
- Outputs and outcomes: runtime `CardRegistryProjectionId`, linkage projection of `CardLinkResolutionManifestId`, clause-tagging coverage map, R0 coverage map, pending/blocked/active state copied from upstream authority, exact gaps, reviewer provenance, and rights flags.
- Diagnostics: missing source/rights/reviewer, model-use denied, duplicate ID, body present without authorization, stale edition, unmapped or multiply mapped local link, unauthorized project-law disposition, missing applicable-card consumer, and orphan link.
- Evidence and provenance: every projected entry binds the pre-C1 authority-snapshot root, resolution-manifest root, source-rights record, author/reviewers, dates, source reference—not copied prose—and linked contracts/tests.
- Determinism and replay: D0 projection root under exact authority snapshot and canonical metadata; review decisions remain upstream attestations with explicit authority.
- Falsifiers and Gauntlet: semantic-body scan in pending slots, raw-source excerpt detection, one-person approval, missing/default/ambiguous resolution branch, unauthorized project-law disposition, actual-card reverse orphan, stale status, and model-context leak.
- Surfaces: contract registry, capability manifest, validation admission, generated docs/tests, drift auditor, and close gate.
- Dependencies and consumers: depends on the pre-C1 human/source pipeline’s immutable authority snapshot and `CardLinkResolutionManifestId` plus FDN.001–FDN.016 for runtime projection; IMM.002–IMM.005/IMM.009/IMM.011 and RPT.006 consume the projection. Normative implementation admission consumes the two pre-C1 artifacts, not authority minted by IMM.001.
- Migration and withdrawal: source/card revision versions the entry and triggers coverage/claim-impact review; old reviewed card remains historical.
- No-claim boundary: a resolution record, projection, slot ID, empty clause tag, or agent-authored text is not normative evidence and cannot activate a slot; `PENDING-LICENSED-SOURCE` admits no implementation semantics, citation accuracy, or coverage sufficiency.
- Rationale: explicit upstream authority prevents a runtime registry from bootstrapping its own normative inputs while preserving the clean-room firewall.

#### `C1.CC.IMM.002@1` — Consequence-contract registry

- Identity, lifecycle, layer: active C1 L7 generated-truth contract; it is the single structured home for every cataloged capability’s semantic spine.
- Inputs and identity domain: contract ID/version, lifecycle, owner layer, input domain, preconditions, budgets, authority, outcomes, evidence, determinism, falsifiers, surfaces, dependencies, exact §5 grammar-expanded prerequisite IDs and separately indexed consumers, cards, and no-claims.
- Preconditions: every field validates; every dependency token expands uniquely against the closed catalog; bare-family/prose prerequisites are rejected; dependencies exist and layer direction is legal; card slots are present even when pending.
- Card slots: `SC.C1.IMM.CONTRACT-REGISTRY.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: contracts, fields, dependency edges, schema bytes, canonicalization, diagnostics, and generated projections are bounded.
- Cancellation: registry generation is transactional; no partially updated root becomes current.
- Authority and secrets: registry contains no credential/source content; contract lifecycle changes require authorized governance records.
- Outputs and outcomes: canonical registry root, per-contract records, exact sorted prerequisite-edge and consumer indexes, lifecycle/migration links, and validation findings.
- Diagnostics: duplicate ID, missing field/card/falsifier/surface, unknown/bare/ambiguous dependency token, range expansion outside one family, illegal dependency, unknown outcome, lifecycle contradiction, and orphan contract.
- Evidence and provenance: registry binds plan/Constitution authority references, generator/build identity, source records, and review/change record.
- Determinism and replay: D0 under exact structured inputs/generator/toolchain; file/order changes cannot alter semantic root.
- Falsifiers and Gauntlet: duplicate/missing fields, dependency cycles, layer violation, prose/registry mismatch, surface widening, and migration cases.
- Surfaces: claim/capability/report generation, repository gates, documentation, checker, and close gate.
- Dependencies and consumers: depends on FDN.001–FDN.016 and IMM.001; IMM.003–IMM.010/IMM.012/RPT.006 consume it.
- Migration and withdrawal: material contract change mints a version/migration/claim-impact link; prior record is immutable.
- No-claim boundary: registry presence does not prove an implementation path exists or passes falsifiers; truth checks establish those separate relations.
- Rationale: one machine spine prevents contracts, APIs, reports, docs, and release rows from describing different products.

#### `C1.CC.IMM.003@1` — Generated claim registry

- Identity, lifecycle, layer: active C1 L7 generated-truth contract; claim rows are derived from consequence contracts, never headings or hand lists.
- Inputs and identity domain: contract registry, active profiles, report schemas, surface manifest, evidence/gate requirements, lifecycle/expiry/withdrawal state, and claim vocabulary.
- Preconditions: each claim has an exact contract/profile/input domain, evidence requirement, falsifier, outcome scope, and no-claim boundary.
- Card slots: `SC.C1.IMM.CLAIM-REGISTRY.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: claim rows, compositions, evidence links, vocabulary checks, canonicalization, diagnostics, and output bytes are bounded.
- Cancellation: generation is transactional; stale/partial claim tables cannot be current.
- Authority and secrets: only governance-approved lifecycle changes activate public rows; registry contains no protected artifacts.
- Outputs and outcomes: canonical claim registry, contract-to-claim links, profile/lifecycle/expiry/withdrawal fields, and rejected orphan assertions.
- Diagnostics: orphan claim, missing falsifier/evidence/no-claim, broader surface language, forbidden vocabulary, inactive card, and stale row.
- Evidence and provenance: root binds contract/profile/schema/generator versions and governance state; generated prose is an echo.
- Determinism and replay: D0 under exact registries/generator/toolchain.
- Falsifiers and Gauntlet: invented heading, deleted API, renamed contract, wider docs/CLI claim, expired/withdrawn row, and composition mismatch.
- Surfaces: capability manifest, report claim rows, docs, repository gate, evidence package, and close gate.
- Dependencies and consumers: depends on IMM.001/IMM.002 and FDN.015; IMM.008/IMM.010/IMM.012/RPT.006 consume it.
- Migration and withdrawal: contract/profile changes regenerate rows; withdrawal preserves prior evidence and reason rather than deleting history.
- No-claim boundary: registry controls language/links but cannot self-award correctness, independence, release, campaign, or field outcomes.
- Rationale: derivation from contracts closes the F-04 class where a checker verifies headings instead of truth.

#### `C1.CC.IMM.004@1` — Generated report schemas

- Identity, lifecycle, layer: active C1 L7 generated-truth contract; schemas and examples derive from typed report/contract registries.
- Inputs and identity domain: RPT contract records, field/type registry, identity obligations, outcome/coverage algebra, diagnostic registry, migration rules, and generator.
- Preconditions: every report family names exact proper-domain identities and validates required fields before example generation.
- Card slots: `SC.C1.IMM.REPORT-SCHEMA-GENERATION.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: schemas, fields, examples, validation cases, generated bytes, canonicalization, and diagnostics are bounded.
- Cancellation: generation is transactional; old generated artifacts stay current until a new root passes validation.
- Authority and secrets: examples use synthetic non-secret sentinel values and may not contain source/credential/standards prose.
- Outputs and outcomes: schemas, canonical encoders, validators, migrations, synthetic examples, and schema-to-contract/identity links.
- Diagnostics: missing `SourceRootId`/`RevisionGraphId`/`DocumentViewId`/`DerivationId`/`ExpectedStateId` where mandated, contradictory coverage, unsafe field, and stale example.
- Evidence and provenance: generated artifact header binds registry/generator/toolchain roots and validation results.
- Determinism and replay: D0 generation under pinned toolchain/input roots.
- Falsifiers and Gauntlet: remove each mandated identity in turn, role-label mismatch, ambiguous optional field, stale hand edit, malformed example, and producer/checker round trip.
- Surfaces: Rust schema types, JSON/JSONL, CLI, docs examples, evidence packages, checker, and drift audit.
- Dependencies and consumers: depends on IMM.002/IMM.005 and FDN.015; IMM.002 supplies all RPT.001–RPT.010 contract declarations without making schema generation depend on runtime report instances. RPT.005/RPT.006/RPT.008–RPT.010/IMM.010/IMM.012/IMM.016 consume generated schemas as applicable.
- Migration and withdrawal: schemas/examples regenerate together; hand-patching generated examples is forbidden.
- No-claim boundary: schema validity proves structural obligations only, not truth of the observations encoded.
- Rationale: field-level generation directly prevents recurrence of Appendix-B identity drift from audit row R1-1.

#### `C1.CC.IMM.005@1` — Generated diagnostic registry

- Identity, lifecycle, layer: active C1 L7 generated-truth contract; diagnostic definitions have one canonical structured source.
- Inputs and identity domain: code, category, severity range, argument schema, allowed locations/evidence/cards, redaction class, producer contracts, and lifecycle.
- Preconditions: code is unique; argument/location/evidence types exist; protected fields have explicit rendering policy.
- Card slots: `SC.C1.IMM.DIAGNOSTIC-REGISTRY.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: codes, arguments, render templates, localization/human projections, validation cases, and diagnostics are bounded.
- Cancellation: generation is transactional; partial code tables never become current.
- Authority and secrets: messages cannot introduce raw standards prose or protected values; producers may emit only registered codes.
- Outputs and outcomes: code registry, typed constructors, schema/render projections, producer indexes, lifecycle/migration records, and validation findings.
- Diagnostics: duplicate/reused code, incompatible arguments, unsafe redaction, orphan producer, missing card/location, and stale rendering.
- Evidence and provenance: registry root binds contract/card/schema/generator/toolchain inputs and review record.
- Determinism and replay: D0 generation under exact roots/toolchain.
- Falsifiers and Gauntlet: duplicate code, field leak, incompatible schema change, unregistered producer, truncation meta-diagnostic, and generated-file edit.
- Surfaces: core diagnostics, reports, CLI human/JSON output, docs, checker, and drift audit.
- Dependencies and consumers: depends on FDN.009/FDN.015, IMM.001/IMM.002; IMM.004/IMM.010/IMM.012 consume it.
- Migration and withdrawal: meaning changes use a new code or major schema; old code remains interpretable.
- No-claim boundary: a registered code does not prove the condition was detected across all inputs or that the suggested action is authorized.
- Rationale: a single registry keeps stable machine codes independent of evolving prose and prevents redaction drift.

#### `C1.CC.IMM.006@1` — Named-API existence truth check

- Identity, lifecycle, layer: active C1 L7 repository-gate contract; it verifies structured API facts, not Markdown headings.
- Inputs and identity domain: contract surface records, generated API inventory from source/build metadata once code exists, schema bindings, feature matrix, concrete-crate inventory, each concrete crate's `CONTRACT.md`, and build identity.
- Preconditions: D7 is human-ratified; API inventory generation itself is reproducible and scoped to the admitted build/features. **PROPOSED default — awaiting ratification (D7):** an exact stable runtime/release toolchain and a separate date-pinned nightly used only by assurance lanes; no exact version is inferred here.
- Card slots: `SC.C1.IMM.API-TRUTH-CHECK.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: packages/modules/items/features/signatures, schema links, comparisons, diagnostics, and generated bytes are bounded.
- Cancellation: cancelled check cannot pass; prior passing evidence stays bound to its old build only.
- Authority and secrets: read-only repository/build metadata; no external fetch or code modification.
- Outputs and outcomes: per-contract API existence/signature/feature/surface match; per-concrete-crate `CONTRACT.md` existence and coherence with owned layer, role, public surface, invariants, dependencies, safety section, and contract IDs; missing/extra/unbound items; and exact build coverage.
- Diagnostics: missing item or `CONTRACT.md`, incompatible signature/outcome, crate-contract ownership/coherence mismatch, wrong feature, unbound surface, stale inventory, and tool failure.
- Evidence and provenance: report binds build/toolchain, source/artifact root, contract registry, generator/checker version, and compared symbols.
- Determinism and replay: D0 under exact build/registry/toolchain.
- Falsifiers and Gauntlet: delete/rename API, remove error variant, remove or stale a concrete crate's `CONTRACT.md`, contradict its owned contracts/layer/dependencies/safety section, feature-gate mismatch, stub/heading-only declaration, stale generated inventory, and checker mutation.
- Surfaces: repository gate, drift audit, claim/capability admission, cycle-close evidence, and trial record.
- Dependencies and consumers: depends on IMM.002–IMM.004, FDN.016, and ratified toolchain; IMM.012 and close gate consume it.
- Migration and withdrawal: checker schema/version changes require evidence migration; passing old build evidence cannot cover a new build.
- No-claim boundary: API existence does not establish implementation behavior, safety, card conformance, or fuzz coverage.
- Rationale: structural truth closes the F-02/F-04 class of contracts describing removed APIs while superficial checks pass.

#### `C1.CC.IMM.007@1` — Dependency/layer agreement truth check

- Identity, lifecycle, layer: active C1 L7 repository-gate contract; it validates runtime dependency direction, package role, contract declarations, the prerequisite DAG, the separately guarded state-transition graph, and candidate-bound dependency hygiene.
- Inputs and identity domain: exact candidate source/build/toolchain/lockfile roots; package/module and resolved feature/target dependency graphs; §5 grammar-expanded prerequisite DAG; separately labeled guarded state-transition graph; layer/role metadata; contract ownership; every concrete crate's `CONTRACT.md`; feature/dependency manifests; allowlist decisions; phase labels/guards; an admitted date-pinned local dependency-advisory snapshot with provenance/availability; duplicate-version policy and explicit allowlist decisions; and build identity.
- Preconditions: concrete boundaries follow the crate-boundary budget; D5, D7, and D-005 routing are ratified as applicable. The candidate hygiene lane has an exact lockfile/build/feature/target graph and a locally supplied, provenance-recorded advisory snapshot; a missing, stale, unavailable, or unsupported snapshot yields indeterminate rather than clean. **PROPOSED default — awaiting ratification (D5):** MIT OR Apache-2.0 with a dependency-license rider, subject to counsel; D-005 still leaves runtime policy and every provider symbolic. **PROPOSED default — awaiting ratification (D7):** exact stable for runtime/release plus date-pinned nightly for assurance findings only.
- Card slots: `SC.C1.IMM.DEPENDENCY-TRUTH-CHECK.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: graph nodes/edges/features/configurations, advisory records, duplicate-version groups/paths, cycle detection, fan-out records, diagnostics, and canonicalization are bounded.
- Cancellation: cancelled check cannot pass; old result covers only its exact graph/build.
- Authority and secrets: read-only repository and supplied local audit metadata; no registry/network access, advisory retrieval, dependency update, or provider activation occurs in the check itself.
- Outputs and outcomes: illegal upward edge/cycle, prerequisite cycle, state-transition phase/guard violation, transition mislabeled as prerequisite, undeclared dependency, role or crate-contract mismatch, unratified provider, boundary-budget warning, and separate clean results for each graph and concrete boundary; plus one immutable `DependencyHygieneResultId` with per-advisory affected path/status/disposition, duplicate-version groups and allowed/refused/indeterminate decisions, exact feature/target coverage, snapshot freshness/availability, and clean/fail/indeterminate aggregate state.
- Diagnostics: graph class, edge path, phase/guard, owner layers/roles, violated law, feature/build context, advisory/snapshot identity and freshness, duplicate versions and paths, allowlist decision, missing or incoherent crate contract, and decision block are explicit.
- Evidence and provenance: report binds exact candidate/source/build/toolchain/lockfile roots, resolved dependency graphs, contract registry, advisory-snapshot identity/date/provenance/availability, every advisory and duplicate-version disposition, allowlist decision IDs, and checker version; later clean snapshots do not erase historical findings.
- Determinism and replay: D0 under exact graph/audit inputs; a snapshot, lockfile, feature, target, disposition, or build change creates a new result.
- Falsifiers and Gauntlet: inject upward edge/cycle, inject a prerequisite cycle, merge a guarded recovered-mode transition into the prerequisite DAG, reverse or remove a transition phase/guard, remove or contradict a crate `CONTRACT.md`, add runtime dependency on tool/lab, hide a feature dependency, select an unratified crypto provider, seed an advisory, omit or stale the advisory snapshot, split an unreviewed duplicate version, forge an allowlist disposition, change a feature/target path, and omit metadata.
- Surfaces: repository gate, capability admission, drift audit, cycle close, and contract review.
- Dependencies and consumers: depends on IMM.002, FDN.016, D5/D7 and D-005 ratification state, and layer law; IMM.012 consumes it.
- Migration and withdrawal: layer/boundary law changes require kernel change control; concrete merges/splits, lockfile changes, snapshot updates, and advisory/duplicate dispositions version their result and retain the historical record.
- No-claim boundary: an acyclic graph or clean dependency-hygiene result does not prove boundaries are semantically useful or dependencies are correct, secure, advisory-free beyond the exact snapshot/date, or licensed beyond the separate rights record.
- Rationale: dependency agreement prevents nominal layers from hiding cycles or assurance/runtime contamination, while one candidate-bound hygiene result prevents a clean layer graph from concealing known advisories or unreviewed duplicate-version splits.

#### `C1.CC.IMM.008@1` — Claim-to-contract linkage truth check

- Identity, lifecycle, layer: active C1 L7 repository-gate contract; every public assertion must resolve to an active exact contract/profile row.
- Inputs and identity domain: generated claim registry, contract registry, reports, capability manifest, API/CLI/docs assertion records, lifecycle/expiry state, and build identity.
- Preconditions: assertions are machine-marked rather than inferred from headings; surface projections expose stable IDs.
- Card slots: `SC.C1.IMM.CLAIM-LINK-TRUTH.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: assertions, links, profiles, surfaces, vocabulary tokens, diagnostics, and output records are bounded.
- Cancellation: cancelled scan cannot pass and cannot preserve a partial “clean” summary.
- Authority and secrets: read-only artifacts; check does not activate/ratify claims.
- Outputs and outcomes: linked/exact/narrowed assertion, orphan/widened/stale/withdrawn assertion, missing no-claim, and vocabulary violation.
- Diagnostics: exact file/schema location, assertion ID, surface, contract mismatch, outcome/evidence/authority widening, and lifecycle state.
- Evidence and provenance: report binds scanned artifact roots, registries, build/generator, parser/checker version, and coverage.
- Determinism and replay: D0 for exact artifact/registry roots.
- Falsifiers and Gauntlet: orphan docs sentence, CLI help widening, renamed friendly feature, withdrawn contract, stronger outcome word, and hidden surface.
- Surfaces: repository gate, drift audit, close gate, capability/docs generation, and trial record.
- Dependencies and consumers: depends on IMM.002/IMM.003/IMM.006, RPT.006, and the versioned candidate CLI command/help declarations; the declarations are registry inputs rather than an admitted CLI surface. IMM.012 and CLI.008 consume the check result.
- Migration and withdrawal: corrected assertions regenerate; historical withdrawn artifacts retain their dated state.
- No-claim boundary: linkage consistency does not establish that linked evidence actually passes.
- Rationale: exact links keep public language from drifting away from the canonical authority/outcome/evidence contract.

#### `C1.CC.IMM.009@1` — Schema/card/fixture coverage truth check

- Identity, lifecycle, layer: active C1 L7 repository-gate contract; it checks bidirectional coverage among contracts, cards, schemas, fixtures, fuzz targets, and gate rows.
- Inputs and identity domain: contract/card/report/diagnostic registries, exact `CardLinkResolutionManifestId`, fixture and fuzz manifests, capability surface, and cycle-gate matrix.
- Preconditions: every manifest uses stable IDs and lifecycle states; every `SC.C1.*` ID has exactly one authorized resolution record, every applicable actual R0 card has a local consumer, and pending cards cannot count as active coverage.
- Card slots: `SC.C1.IMM.COVERAGE-TRUTH-CHECK.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: registry nodes/edges, graph traversal, cycles/orphans, diagnostics, and output records are bounded.
- Cancellation: cancelled traversal cannot assert zero orphans; exact visited scope is reported.
- Authority and secrets: read-only metadata; held-out fixture content is unavailable, and only steward commitments/manifests are visible.
- Outputs and outcomes: missing/orphan/duplicate/stale links, invalid resolution branches, unauthorized project-law dispositions, pending-card blocks, uncovered surface/outcome/falsifier, and bidirectional coverage summary.
- Diagnostics: source and target IDs, resolution branch/reviewer record, missing edge type, lifecycle mismatch, held-out leakage, and generated/manual conflict.
- Evidence and provenance: report binds all registry roots, resolution-manifest root, graph/checker version, held-out manifest identities, and traversal coverage.
- Determinism and replay: D0 under exact roots/protocol.
- Falsifiers and Gauntlet: remove each edge class, omit or multiply map a local link, default to no-card-needed, forge a project-law disposition, orphan an applicable actual card, orphan a fixture, remove a refusal test, hide a surface, count pending as active, and leak held-out content.
- Surfaces: repository gate, capability manifest, drift audit, card gate, fuzz gate, and cycle close.
- Dependencies and consumers: depends on IMM.001–IMM.005, the exact pre-C1 `CardLinkResolutionManifestId`, and versioned target/fixture declarations; later fuzz and gate manifests consume its coverage result, while IMM.012 and the close gate consume its audit output.
- Migration and withdrawal: registry changes regenerate coverage; historical results remain bound to old roots.
- No-claim boundary: edge coverage is inventory evidence, not proof that a fixture is correct or a capability works.
- Rationale: zero-orphan checking prevents impressive counts from hiding missing semantic consumers or untested refusal paths.

#### `C1.CC.IMM.010@1` — Generated-echo and schema drift check

- Identity, lifecycle, layer: active C1 L7 repository-gate contract; generated artifacts must reproduce their canonical source root exactly or declare themselves non-authoritative renderings.
- Inputs and identity domain: canonical structured registries, generated files/examples/docs/help/manifests, the rights-admitted versioned Arlington source artifact and source-vintage identity when present, its tool-only importer and generated validation-rule data, generator versions, provenance headers, and expected roots.
- Preconditions: generated outputs carry source/generator identity; manually maintained prose does not claim generated authority. Arlington import is unavailable until source rights and the exact source artifact are admitted; the importer runs only as a tool and DOC.007 remains a fail-closed non-authority bridge.
- Card slots: `SC.C1.IMM.GENERATED-DRIFT.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: files/records, regeneration/diff bytes, canonicalization, provenance validation, diagnostics, and output summaries are bounded.
- Cancellation: cancelled regeneration cannot pass; old generated outputs remain stale and blocked.
- Authority and secrets: generator/importer reads only admitted structured sources, has no ambient fetch or runtime authority, and cannot copy restricted card/source bodies into broader outputs.
- Outputs and outcomes: exact match, stale/mutated/missing/unattributed echo, source-root mismatch, schema-example drift, protected-data incident, and—only after rights admission—a versioned Arlington generated-rule-data echo bound to importer identity and exact source vintage.
- Diagnostics: artifact path/ID, expected/observed roots, differing record field, generator version, and authority class.
- Evidence and provenance: report binds canonical roots, generated artifact digests, toolchain/generator/importer identity, exact admitted source-vintage/root where applicable, rights record, and diff coverage.
- Determinism and replay: D0 under exact roots/toolchain/generator.
- Falsifiers and Gauntlet: edit generated example, omit identity field, stale CLI help, duplicate hand table, wrong provenance, Arlington source-vintage or importer mismatch, runtime use of importer data as standalone authority, unauthorized source input, and restricted-content injection.
- Surfaces: repository gate, docs/help/schema generation, capability manifest, drift audit, and close gate.
- Dependencies and consumers: depends on IMM.002–IMM.005, RPT.005/RPT.006, DOC.007, the admitted source-rights record when Arlington import is present, and versioned CLI projection declarations/fixtures; the active CLI surfaces are downstream consumers. IMM.012 and CLI.008 consume the check result.
- Migration and withdrawal: regenerate rather than hand-patch; source/generator change creates a new artifact root.
- No-claim boundary: exact generated equality says nothing about whether the canonical source judgment is correct.
- Rationale: derivability targets the duplication-drift class observed twice in the planning corpus.

#### `C1.CC.IMM.011@1` — Source-rights and model-context scanner

- Identity, lifecycle, layer: active C1 L7 tool contract; it enforces task-local allowed-source manifests and detects known prohibited/restricted material without treating scans as legal judgment.
- Inputs and identity domain: source-rights registry, processor-source deny class, restricted-text signatures/policies, repository/model-context artifacts, dependency provenance, and scan scope.
- Preconditions: registry and scan policy are reviewed; scanner does not ingest prohibited sources to improve detection during this run.
- Card slots: `SC.C1.IMM.SOURCE-RIGHTS-SCAN.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: files/bytes, archive depth, generated contexts, findings, quarantine metadata, and diagnostics are bounded.
- Cancellation: cancelled scan cannot clear an artifact; exact unscanned scope remains blocking.
- Authority and secrets: read-only local scope; findings avoid reproducing restricted content and follow incident confidentiality.
- Outputs and outcomes: admitted/unknown/prohibited/restricted-source finding, provenance gap, dependency-license block, and quarantine instruction.
- Diagnostics: source class, artifact/path, policy/rule ID, exposure scope, uncertainty, and required human/legal review without copying suspect text.
- Evidence and provenance: scan record binds policy/registry, scanned artifact identities, tool version, coverage, and reviewer disposition.
- Determinism and replay: D0 for exact artifacts/policy/tool; legal conclusions remain human authority.
- Falsifiers and Gauntlet: seeded prohibited-name/context markers, raw standards excerpt marker, archive/generated artifact, unknown dependency, false-positive disposition, and cancellation.
- Surfaces: repository gate, model-context preparation, dependency review, drift audit, incident handling, and close gate.
- Dependencies and consumers: depends on IMM.001, source-rights registry, FDN.008/FDN.015; IMM.012 and close gate consume it.
- Migration and withdrawal: policy/registry/tool changes version results; a later clean scan cannot erase a documented exposure without disposition.
- No-claim boundary: scanner output is not legal advice, ontological model-training purity, or proof that no unknown copied structure exists.
- Rationale: a mechanical gate turns clean-room rules into enforceable context policy while preserving honest known unknowns.

#### `C1.CC.IMM.012@1` — Blocking drift auditor

- Identity, lifecycle, layer: active C1 L7 gate contract; it composes generated-truth diffs and contract-truth checks and blocks on unresolved Grade-A findings.
- Inputs and identity domain: immutable RPT.006 candidate-manifest root, canonical/generated roots, API/dependency/claim/coverage/source scans, schema migrations, build, findings/dispositions, and audit protocol.
- Preconditions: candidate manifest was finalized before audit; every component check ran over that unchanged manifest and exact candidate artifact/build; findings are graded with stable evidence locations.
- Card slots: `SC.C1.IMM.DRIFT-AUDITOR.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: component reports, findings, cross-links, rescans, diagnostics, and final artifact bytes are bounded.
- Cancellation: cancelled/missing component is a blocking indeterminate result, never a pass.
- Authority and secrets: auditor is read-only and cannot auto-waive findings; disposition/waiver authority is explicit and recorded.
- Outputs and outcomes: immutable `DriftAuditResultId` with pass, fail, or indeterminate state, Grade A/B/C counts, unresolved findings, exact candidate-manifest/component roots, waivers, and coverage.
- Diagnostics: missing/stale component, candidate mismatch, unresolved Grade A, invalid waiver, source incident, and auditor self-failure.
- Evidence and provenance: audit root binds the preexisting RPT.006 candidate-manifest root, candidate build/artifacts, every component report, protocol/checker version, reviewer dispositions, and timestamps in the separate run envelope.
- Determinism and replay: semantic audit outcome is D0 under exact inputs/protocol; review judgment remains attributed.
- Falsifiers and Gauntlet: seed deleted API, layer cycle, orphan claim, stale schema, pending card, prohibited context marker, invalid waiver, and cancelled component.
- Surfaces: repository gate, RPT.008 capability-admission envelope, trial record, morning report, and evidence package.
- Dependencies and consumers: depends on IMM.006–IMM.011, IMM.015, and RPT.006; RPT.008, IMM.016/IMM.019, and the C1 close gate consume it.
- Migration and withdrawal: auditor/protocol change versions results; passing evidence covers only its exact candidate and cannot be reused after changes.
- No-claim boundary: a clean drift audit establishes cross-artifact consistency within scope, not PDF correctness or independent adjudication.
- Rationale: drift already appeared at document stage, so the immune system must predate code growth.

#### `C1.CC.IMM.013@1` — Hostile-input standalone evidence checker

- Identity, lifecycle, layer: active C1 L7 contract; checker accepts raw package bytes and owns its parsing, structural walk, canonical-root verification, availability, and coverage accounting.
- Inputs and identity domain: immutable hostile package source, check policy, checker capability manifest, bounded materialization capabilities, schema/contract versions, pre-run `CheckerIsolationPlanId`/`PreRunOracleLineageId`, optional seeded-defect trial ID, and `WorkContext`.
- Preconditions: D4 and its D1/D2 dependencies are ratified; IMM.014 pre-run admission exists; package size/depth/artifact limits are active; checker does not trust producer-parsed objects. **PROPOSED default — awaiting ratification (D4):** separate code, recorded different-model-family authorship, specification isolation, and seeded-defect trials during C1; the numerical outcome is not known before those trials.
- Card slots: `SC.C1.IMM.EVIDENCE-CHECKER.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: package bytes, fields/nodes/claims/artifacts, depth, canonicalization/symmetry work, materialization, diagnostics, and output are bounded.
- Cancellation: stops at checkpoints, reconciles private materializations, and returns partial/refused coverage rather than a passing prefix.
- Authority and secrets: no ambient network/filesystem; external retrieval/recomputation uses explicit narrow capabilities and disclosure policy.
- Outputs and outcomes: check report with package integrity, schema/root status, verified/unsupported claims, artifact availability, coverage, diagnostics, and no-claims; a terminal non-cancelled check additionally emits `CheckedPackageHandleId` scoped to the immutable raw package source, checker build/protocol, policy, exact checked-claim set, coverage, availability, and report root, including failed/partial/refused status rather than acting as a pass token; seeded inputs additionally emit `SeededCheckerTrialReportId` with injected class and detected/missed/indeterminate outcome.
- Diagnostics: hostile encoding, duplicate/conflicting identity, unknown critical field, missing artifact, unavailable secret, budget cap, and producer/checker disagreement.
- Evidence and provenance: binds raw package source, checker build/protocol/capabilities, pre-run lineage plan, policy, materialized artifact identities, seeded-defect identity where applicable, limits, and exact checked claims.
- Determinism and replay: semantic check targets D0 under exact package/policy/checker/dependencies/semantic limits.
- Falsifiers and Gauntlet: malformed packages, root ambiguity, duplicate IDs, missing identity fields, identity-only artifact, stale/transplanted `CheckedPackageHandleId`, bombs, cancellation, producer-generated false package, and independent vectors.
- Surfaces: Rust checker API, CLI package check, drift/close-gate evidence, and evidence-package round trip.
- Dependencies and consumers: depends on FDN.001–FDN.016, IMM.002–IMM.005, IMM.014, and ratified D4; IMM.016 outputs are hostile inputs rather than an implementation prerequisite, while CLI.009 and IMM.020 consume checker results.
- Migration and withdrawal: checker/schema protocol changes version results; old checker evidence remains scoped and may lapse.
- No-claim boundary: package/root/signature identity does not prove enclosed computations, normative correctness, trust, or unavailable artifacts.
- Rationale: parsing producer output through the producer’s own implementation would reproduce the shared-bug failure the checker exists to catch.

#### `C1.CC.IMM.014@1` — Checker isolation plan and pre-run lineage admission

- Identity, lifecycle, layer: active C1 L7 pre-run governance/architecture contract; it defines permitted code/data/model/source sharing before checker implementation or seeded evaluation begins.
- Inputs and identity domain: ratified D4 isolation decision, planned producer/checker dependency boundaries, authorship/model/source assignments, proposed shared constants/primitives, test/corpus separation, reviewer relationships, and unresolved lineage questions; no seeded result is an input.
- Preconditions: exact planned shared and separate components are classified; unknown lineage remains uncertainty rather than independence; no trial result or achieved detection statement is represented as preexisting. **PROPOSED default — awaiting ratification (D4):** separately authored checker code, a different recorded model family using specification-only inputs, seeded-defect trials at each cycle close, and human adversarial review by C4.
- Card slots: `SC.C1.IMM.CHECKER-ISOLATION.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: planned graph/manifest records, lineage relationships, review findings, separation controls, and diagnostics are bounded.
- Cancellation: incomplete pre-run lineage review cannot admit checker work or support an independence label.
- Authority and secrets: lineage records disclose only approved metadata; independent reviewer/author roles are authenticated and conflicts recorded.
- Outputs and outcomes: immutable `CheckerIsolationPlanId` and `PreRunOracleLineageId` with planned separations, known correlations, prohibited sharing, admitted narrow sharing, unknowns, reviewer assignments, admission status, and pre-run claim ceiling; no attempt/detection/miss field is populated.
- Diagnostics: same parser/root walk, shared test-only oracle, unrecorded model/source, unknown author relation, decision mismatch, and stale manifest.
- Evidence and provenance: binds the D4 decision, planned source/dependency/model manifests, role assignments, separation controls, review record, and unresolved questions; it contains no fixture outcome.
- Determinism and replay: the structured pre-run plan root is D0; governance judgments/unknowns remain attributed and dated.
- Falsifiers and Gauntlet: planned shared canonical encoder, common producer fixture, hidden dependency, same generated corpus, unknown model family, unauthenticated reviewer, prefilled detection claim, stale plan, and changed assignment.
- Surfaces: checker admission, assurance-run manifests, seeded-trial execution, evidence-package planning, capability blocks, and later final lineage assessment.
- Dependencies and consumers: depends on D4, D1/D2, IMM.007/IMM.011, and FDN.015; IMM.013/IMM.016/IMM.020 and the preimplementation gate consume it. Under the proposed D4 profile, only frozen schema/class constants and an audited cryptographic primitive may be narrowly shared; the canonical encoder, parser, semantic tree, root construction, and producer fixtures may not be shared.
- Migration and withdrawal: new planned sharing/dependency/model assignment versions the plan and can revoke admission before further trials.
- No-claim boundary: pre-run separation is a scoped plan and lineage admission, never a trial result, absolute independence statement, or proof of correctness.
- Rationale: separating planned isolation from observed seeded outcomes prevents future evidence from being embedded in a pre-run artifact.

#### `C1.CC.IMM.015@1` — Contract migration, lapse, and withdrawal

- Identity, lifecycle, layer: active C1 L7 governance contract; contract versions and claim lifecycle are append-only semantic records.
- Inputs and identity domain: old/new contract IDs, material diff, affected identities/schemas/surfaces/evidence, migration plan, claim-impact review, dates, and authority.
- Preconditions: materiality is classified; old artifact roots remain immutable; human authority is required where kernel or release boundaries change.
- Card slots: `SC.C1.IMM.CONTRACT-LIFECYCLE.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: affected graph traversal, migration records, rescans, diagnostics, retained history, and output bytes are bounded.
- Cancellation: incomplete impact review cannot activate the new version or preserve old current-facing status.
- Authority and secrets: lifecycle changes require authenticated governance role; migration never declassifies protected artifacts.
- Outputs and outcomes: successor/predecessor links, migrated/refused artifacts, active/lapsed/withdrawn state, reason, affected claims, and fresh-evidence requirements.
- Diagnostics: silent redefinition, missing migration, identity incompatibility, stale surface, unauthorized activation, and incomplete impact graph.
- Evidence and provenance: binds old/new registry roots, diff protocol, reviewer/authority, migration results, rescans, and decision records.
- Determinism and replay: structured impact graph is D0; governance judgment is attributed and time-scoped.
- Falsifiers and Gauntlet: same ID/material change, missing consumer, incompatible identity, old claim still active, protected-field loss, and rollback fiction.
- Surfaces: contract/claim/schema registries, capability manifest, drift audit, reports, checker, and close gate.
- Dependencies and consumers: depends on IMM.002/IMM.003 and FDN.015; IMM.006–IMM.012 and every lifecycle-sensitive consumer use its migration/lapse rules. Fresh truth checks run after a migration rather than serving as a prerequisite for defining the migration.
- Migration and withdrawal: this contract defines that very process; changes to it require kernel change control and claim-lapse review.
- No-claim boundary: migration preserves declared relations/losses; it cannot recreate evidence or observations that were never recorded.
- Rationale: append-only lifecycle prevents prose edits from upgrading old artifacts or hiding withdrawn claims.

#### `C1.CC.IMM.016@1` — Minimal evidence-package assembly

- Identity, lifecycle, layer: active C1 L7 contract; C1 packages reports, registries, evidence, and availability records without PDF-signature creation or external publication.
- Inputs and identity domain: exact strict/recovery/enrichment/validation/replay/capability-admission report roots including RPT.009 and RPT.010 when applicable, contract/claim/schema/card roots, artifacts and availability classes, checker protocol, every corroborating observation’s general `OracleLineageId`, checker-specific pre-run/final lineage roots, declared output-sink class, no-claims, disclosure policy, and canonical package protocol.
- Preconditions: D1/D2 and D4 plus disclosure policy are ratified; all inputs are immutable and schema-valid. **PROPOSED defaults — awaiting ratification (D1/D2/D4):** the coupled SHA-256/deterministic-CBOR package and the staged checker-isolation profile; neither is activated by this plan.
- Card slots: `SC.C1.IMM.EVIDENCE-PACKAGE.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: package bytes, claims, artifacts, graph depth, canonicalization/symmetry work, embedding/materialization, diagnostics, and output transaction are bounded.
- Cancellation: private assembly aborts; no prefix or indeterminate root is published as a package.
- Authority and secrets: embedding/export follows artifact policy; no ambient network, signer, timestamp, log, or publication capability exists in C1 assembly.
- Outputs and outcomes: canonical semantic package root, serialized package, artifact availability map, construction receipt stating sink class (`Buffered`, `AtomicVisibility`, or `DurableCommit`) plus observed visibility/durability state, checker target protocol, and exact no-claims.
- Diagnostics: missing identity/availability, conflicting artifact, noncanonical/duplicate field, protected disclosure, unratified protocol, output limit, and transaction failure.
- Evidence and provenance: package binds exact report/registry/artifact roots, producer protocol/build, disclosure policy, limits, and construction diagnostics.
- Determinism and replay: unsigned package semantics target D0 under exact inputs/protocol; serialization canonicality is separately disclosed and checked.
- Falsifiers and Gauntlet: producer/checker dual roots, duplicate/conflicting records, omitted/forged/unknown observation lineage, correlated-wrapper inflation, missing artifacts, unavailable secrets, protected hashes, bombs, cancellation, and schema migration.
- Surfaces: Rust package builder, CLI package check input, C1 trial record/evidence handoff, and standalone checker.
- Dependencies and consumers: depends on FDN.001–FDN.016, RPT.001–RPT.010, IMM.002–IMM.005, IMM.014, and IMM.020; IMM.013 independently consumes its raw output rather than producer objects, while CLI.009, IMM.019, and the close gate consume package/checker results.
- Migration and withdrawal: package protocol changes version roots; old packages remain checkable by their protocol and never gain new evidence.
- No-claim boundary: no package is externally committed, signed, published, or independently adjudicated by this plan; hash ratification must precede any later external commitment.
- Rationale: a minimal package closes the report→checker loop while keeping commitment substrate and external assurance human-bound.

#### `C1.CC.IMM.017@1` — Prospective C1 event append and ledger continuation

- Identity, lifecycle, layer: active only after ratification as a C1 L7 campaign-tooling contract; one invocation appends one prospective event to a ledger already bootstrapped by IMM.018 and never seals the cycle by itself.
- Inputs and identity domain: `ProductionLedgerBootstrapId`, versioned event schema, writer identity and verified model route where available, event class, attempt/branch relation, opaque artifact/build/toolchain/protocol roots available at that moment, payload, evidence status, retrospective flag, prior writer-shard digest, and disclosure policy.
- Preconditions: D1/D2/D6 are human-ratified; IMM.018 completed before implementation candidate work; writer-shard ownership is exclusive; retrospective status is structurally mandatory. **PROPOSED default — awaiting ratification (D6):** hash-chained append-only JSONL per-writer shards as source of truth plus a regenerable derived index.
- Card slots: `SC.C1.IMM.CYCLE-EVENT-APPEND.001` — `PENDING-LICENSED-SOURCE`; this project-law slot contains no standards semantics.
- Budgets: event bytes, canonicalization, chain verification, fsync/batch policy, merge-index work, diagnostics, and protected metadata are bounded.
- Cancellation: before append, cancellation emits no record and remains an observable missing-event failure; after acknowledgement, cancellation cannot retract it. A torn final record receives a correction-linked diagnostic rather than silent repair.
- Authority and secrets: each writer appends only to its own shard; payload redaction follows disclosure policy; secrets, restricted source text, and private corpus bytes do not enter an ordinary event merely because the ledger is append-oriented.
- Outputs and outcomes: `ProspectiveEventRecordId` and new shard head, duplicate-idempotent observation where schema permits, or typed refused/cancelled/indeterminate storage outcome. Derived indexes are disposable and never source of truth.
- Diagnostics: unknown bootstrap, schema/version mismatch, missing/false retrospective declaration, prior-digest mismatch, torn record, writer collision, protected-field leak, unratified protocol, and backend failure remain explicit.
- Evidence and provenance: each event binds bootstrap, prior/new shard heads, writer, event/attempt relation, exact then-available roots, evidence status, disclosure result, and append receipt; later final roots cannot be backfilled into it.
- Determinism and replay: canonical event semantics and per-writer chaining target D0 under exact ratified protocols; timestamps and host write observations remain separate. Merge order is a versioned derived view and cannot rewrite shard history.
- Falsifiers and Gauntlet: append before bootstrap, concurrent writers, torn line, prior-digest corruption, retrospective omission, missing failed attempt, secret injection, index/source disagreement, crash around acknowledgement, and chain-head substitution.
- Surfaces: campaign event capture, IMM.019 sealing input, reviewed ledger export, next-cycle archaeology, and later external-commitment handoff; no engine layer imports it.
- Dependencies and consumers: depends on IMM.018 and ratified D1/D2/D6 only; IMM.019, §9.7, §11.2, and §11.5 consume the prospective stream.
- Migration and withdrawal: event schemas are versioned and old shards stay immutable; corrections link rather than overwrite. A late or missing interval remains retrospective and cannot be upgraded into prospective evidence.
- No-claim boundary: the local chain supplies durability and repository-local tamper detection, not tamper evidence against a repository writer; hash/canonicalization ratification must precede the first external commitment, and this plan performs none.
- Rationale: a low-dependency append path can capture attempts as they happen instead of requiring the final artifacts it is meant to evidence.

#### `C1.CC.IMM.018@1` — Pre-C1 production-ledger bootstrap and handoff

- Identity, lifecycle, layer: active only after ratification as a pre-C1 L7 campaign-governance contract; it opens the production ledger before any implementation candidate, trial, or assurance execution.
- Inputs and identity domain: human-ratified D1 identity/hash decision, D2 canonicalization decision, D6 ledger backend/schema decision, human-approved writer roster/roles, disclosure policy, genesis rule, retention policy, and independently established substrate availability.
- Preconditions: D1/D2/D6 are ratified and recorded; writer identities/ownership are assigned; schema and disclosure policy are fixed for bootstrap; this operation precedes all C1 candidate work. Hash/canonicalization ratification precedes any first external commitment.
- Card slots: `SC.C1.IMM.LEDGER-BOOTSTRAP.001` — `PENDING-LICENSED-SOURCE`; this project-law slot contains no standards semantics.
- Budgets: writer shards, genesis records, schema bytes, validation, storage initialization, diagnostics, and handoff metadata are bounded.
- Cancellation: cancellation or partial initialization leaves the production ledger unopened; no provisional shard head authorizes prospective capture.
- Authority and secrets: only the human-established campaign-governance role may approve bootstrap; writer capabilities are shard-scoped; genesis and handoff exclude restricted source text, secrets, and corpus bytes.
- Outputs and outcomes: immutable `ProductionLedgerBootstrapId`, ratified schema/protocol roots, per-writer genesis heads, ownership map, start-boundary receipt, disclosure/retention state, and open/refused/indeterminate status.
- Diagnostics: unratified decision, schema/protocol mismatch, duplicate writer, missing ownership, unavailable substrate, protected genesis field, partial initialization, and validation failure.
- Evidence and provenance: bootstrap binds the three ratified decisions, human approvals, substrate identity/availability, writer roster, schema/genesis roots, initialization observations, and explicit pre-candidate boundary.
- Determinism and replay: semantic bootstrap record targets D0 under exact decisions/roster/schema/genesis rule; host initialization observations remain separate.
- Falsifiers and Gauntlet: bootstrap after candidate artifact, unratified hash/canonicalization/backend, writer alias collision, mutable genesis, partial shard set accepted, secret injection, and substituted substrate.
- Surfaces: campaign preflight, writer handoff, IMM.017 event append, preimplementation gate, ledger audit, and later commitment preparation; no engine runtime surface imports it.
- Dependencies and consumers: depends on human-ratified D1/D2/D6 and the human-established ledger/commitment substrate only; IMM.017 and the preimplementation gate consume it. It has no dependency on C1 FDN, report, checker, fuzz, or candidate artifacts.
- Migration and withdrawal: bootstrap/protocol changes require a versioned successor and linked shard continuation; an after-the-fact bootstrap cannot repair a missing prospective interval.
- No-claim boundary: opening a local ledger does not establish external anchoring, independent custody, immutability against its writers, or any product/campaign outcome.
- Rationale: the ledger must exist before the events it is expected to preserve, so bootstrap is a separate pre-C1 gate rather than a close artifact.

#### `C1.CC.IMM.019@1` — Sealed C1 cycle trial record

- Identity, lifecycle, layer: active only after ratification as a C1 L7 close-record contract; it seals one bounded C1 interval from prospective IMM.017 event shards and final artifact roots without rewriting either.
- Inputs and identity domain: bootstrap ID, interval start/end heads, every prospective event/attempt/failure/retry/intervention, final build/toolchain/dependency/card/report/capability/audit/checker/fuzz/probe/package roots, availability, gate dispositions, missing telemetry, and no-claim state.
- Preconditions: the bootstrap predates the interval; all writer shards verify from genesis to end heads; final roots are immutable and refer to recorded events or explicit retrospective gaps; D1/D2/D6 remain the ratified protocols.
- Card slots: `SC.C1.IMM.CYCLE-TRIAL-SEAL.001` — `PENDING-LICENSED-SOURCE`; this project-law slot contains no standards semantics.
- Budgets: events, shards, attempts, artifact roots, availability records, canonicalization, chain verification, diagnostics, and sealed-record bytes are bounded.
- Cancellation: interrupted sealing yields no sealed record; prospective events remain intact and a later retry records its own attempt.
- Authority and secrets: sealer can read declared shards/roots and write only the seal artifact; disclosure policy excludes secrets, restricted source, and private corpus content while retaining protected identities/availability.
- Outputs and outcomes: immutable `CycleTrialRecordId`, interval/shard-head set, attempt distribution, discarded-candidate and intervention history, final root matrix, missing/retrospective gaps, gate states, artifact availability, and seal receipt.
- Diagnostics: chain break, missing writer shard/event, retrospective gap, root without event lineage, stale build, conflicting gate state, unavailable artifact, disclosure failure, unratified protocol, and seal transaction failure.
- Evidence and provenance: record binds bootstrap, verified shard/event roots, final RPT.008/IMM.012/IMM.020/FUZ.011/FUZ.015/FUZ.016 and other scoped roots, human dispositions, sealer identity, protocol, limits, and construction receipt.
- Determinism and replay: sealed semantic record targets D0 under exact ordered shard/event roots, final artifacts, decisions, and protocol; run timestamps/host observations remain linked but outside the semantic root.
- Falsifiers and Gauntlet: omitted failed attempt, post-hoc inserted event, head substitution, final root without event, stale audit/candidate pair, missing checker miss, fuzz-baseline mismatch, secret injection, cancellation, and alternate merge-order test.
- Surfaces: C1 close gate, evidence package, reviewed ledger export, morning report input, next-cycle archaeology, and later external-commitment preparation; no engine layer imports it.
- Dependencies and consumers: depends on IMM.017/IMM.018, RPT.004/RPT.007/RPT.008, IMM.012–IMM.016/IMM.020, FUZ.011–FUZ.016, and final gate/probe/card roots; §11.5 and the next-cycle archaeology record consume it.
- Migration and withdrawal: seal schema/protocol changes version the record; corrections append linked successor records and never overwrite events or the original seal.
- No-claim boundary: a sealed local record supports only its recorded interval/availability; it is not externally anchored, independently adjudicated, or evidence of an unexecuted surface. Ratification must precede any later external commitment.
- Rationale: sealing after final artifacts preserves prospective history while avoiding a dependency cycle between event capture and close-gate evidence.

#### `C1.CC.IMM.020@1` — Seeded-checker trial and final lineage assessment

- Identity, lifecycle, layer: active C1 L7 post-trial assurance contract; it compares the pre-run isolation plan with observed implementation lineage and seeded-checker outcomes after the runs occur.
- Inputs and identity domain: IMM.014 plan/pre-run lineage roots, actual producer/checker source/build/dependency/model/data manifests, IMM.013 `SeededCheckerTrialReportId` set, FUZ.014 run receipts, seed-class registry, review findings, ratified D4, and limits.
- Preconditions: the IMM.014 root predates checker implementation/trials; every seeded report binds an exact seed, checker build, run receipt, and expected detection class; missing runs remain missing rather than inferred.
- Card slots: `SC.C1.IMM.CHECKER-LINEAGE-ASSESSMENT.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: manifest relations, seed classes/attempts, detections/misses, coverage, reviews, canonicalization, diagnostics, and report bytes are bounded.
- Cancellation: interrupted assessment emits only partial coverage and cannot support the stronger checker row or close gate.
- Authority and secrets: assessment is read-only; it cannot waive a miss, alter seed expectations, activate a claim, or expose protected fixtures/model/source details beyond approved metadata.
- Outputs and outcomes: immutable `OracleLineageId`/`CheckerLineageAssessmentId`, planned-versus-actual sharing diff, known correlations/unknowns, seeded attempts/detections/misses/indeterminate results by class, coverage, and maximum supportable checker claim. Under the proposed D4 profile, any seeded miss is Grade A.
- Diagnostics: pre-run root missing/stale, unplanned sharing, hidden dependency/model/source, run/seed/build mismatch, missing seed class, miss, indeterminate trial, coverage overstatement, and unauthorized waiver.
- Evidence and provenance: assessment binds D4, pre-run plan, actual manifests, every seed definition/report/run receipt, reviewer disposition, checker/producers roots, limits, and protected availability.
- Determinism and replay: structured outcome is D0 under exact manifests/reports/protocol; review judgments remain attributed and dated.
- Falsifiers and Gauntlet: shared canonical encoder, common producer fixture, hidden generated corpus, forged detection, omitted miss, stale checker build, transplanted receipt, wrong expected class, changed plan after run, and cancellation.
- Surfaces: checker claim registry, RPT.008 blocking inputs where applicable, evidence package, trial seal, product/cycle-close gates, and future lineage review.
- Dependencies and consumers: depends on IMM.013/IMM.014, FUZ.014, IMM.007/IMM.011, and ratified D4; IMM.016/IMM.019 and the product/close gates consume it.
- Migration and withdrawal: new sharing/build/model/seed protocol versions the assessment and lapses prior checker language until affected trials rerun.
- No-claim boundary: observed seeded detection supports only the declared seeds/classes/builds/runs and does not establish absolute independence, universal defect detection, or PDF correctness.
- Rationale: post-run evidence belongs in a post-run assessment, leaving the pre-run isolation plan causally and temporally honest.

### 8.11 CLI contracts

#### `C1.CC.CLI.001@1` — `mb inspect`

- Identity, lifecycle, layer: active C1 L8 command contract; `mb inspect` is the primary R0 wedge and projects DOC.009 plus explicit recovery/credential options.
- Inputs and identity domain: one admitted source, strict/recovery request, optional credential lease, limits/profile, requested report components, projection, and output sink.
- Preconditions: source/card authority and the RPT.008 capability-admission envelope admit the request; recovery must be explicitly enabled and credentials use CLI.005.
- Card slots: `SC.C1.CLI.INSPECT.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: source/open/recovery/decode work shares one account; CLI parsing, projection, output, diagnostics, and temporary storage are also bounded.
- Cancellation: interrupt requests operation cancellation; the command waits only for bounded reconciliation and emits a terminal machine record when the sink permits.
- Authority and secrets: no ambient network, external file, action execution, or writer authority; credential input is never accepted through ordinary argv/environment fields.
- Outputs and outcomes: emits the immutable strict OpenReport and optional separately linked Recovery/security enrichment components, exact machine outcome, report identities, and exit mapping.
- Diagnostics: usage errors are separate from document outcomes; parser/recovery/security diagnostics retain stable codes and locations.
- Evidence and provenance: command receipt binds source identity, request/profile/limits, used capabilities, report roots, projection, build/toolchain, and run envelope.
- Determinism and replay: semantic reports target D0; terminal rendering and host observations follow RPT.004/RPT.005.
- Falsifiers and Gauntlet: strict mode cannot recover, partial source, recovery alternatives, credentials, cancellation, broken output pipe, diagnostic truncation, and secret scans.
- Surfaces: executable command, generated help/schema, examples, capability manifest, and shell exit state.
- Dependencies and consumers: depends on DOC.009, REC.002–REC.010, RPT.001–RPT.005/RPT.007/RPT.008, and CLI.005–CLI.007; product gate consumes it.
- Migration and withdrawal: option/schema semantic changes version the command contract; aliases cannot widen behavior.
- No-claim boundary: `inspect` does not render, extract text, repair, rewrite, sanitize, trust signatures, or execute active content.
- Rationale: one explicit command exposes the sellable inspection workflow without inventing the previously cautioned `autopsy` name.

#### `C1.CC.CLI.002@1` — `mb revisions`

- Identity, lifecycle, layer: active C1 L8 command contract; it projects revision graph/history evidence without choosing hidden recovery alternatives.
- Inputs and identity domain: source/open artifact, saved OpenReport, or evidence package plus its scoped `CheckedPackageHandleId`; graph selector, strict/recovery policy, output projection, and limits.
- Preconditions: selected graph ID exists or all graphs are requested; a saved OpenReport passes generated schema/root checks; an evidence-package path is admitted only when IMM.013 checked the exact immutable raw package bytes and its handle covers the requested graph claims/artifact availability. A failed/partial/refused handle cannot be widened.
- Card slots: `SC.C1.CLI.REVISIONS.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: graph nodes/edges/occurrences/ranges, source reads, diagnostics, and output bytes are bounded.
- Cancellation: traversal returns explicit partial output only under JSONL terminal framing; ordinary report projection stays transactional.
- Authority and secrets: read-only; protected spans/metadata are redacted by policy.
- Outputs and outcomes: source/graph identities, candidate revisions/chains, xref/trailer links, object occurrence summaries including visible/shadowed/unreachable/unknown classifications when available, signature ranges, gaps, assumptions, and selection state.
- Diagnostics: unknown graph, stale package/report, source unavailable, partial coverage, ambiguous selection, output limit, and schema mismatch.
- Evidence and provenance: output binds source/report/package, exact graph(s), request/profile, projection, and build.
- Determinism and replay: D0 semantic projection for exact graph/request; human rendering is derived.
- Falsifiers and Gauntlet: multiple graphs, forks/cycles, partial source, unknown selector, saved-report mismatch, unchecked/stale/transplanted package handle, hidden occurrence classification, cancellation, redaction, and output round trips.
- Surfaces: executable command, generated help/schema, capability manifest, and examples.
- Dependencies and consumers: depends on REV.004/REV.008/REV.009, RPT.001/RPT.005/RPT.007, IMM.013 for package-backed requests, and CLI.006/CLI.007; Workflow B and product gate consume it.
- Migration and withdrawal: selector/output schema changes version the command; old graph IDs remain valid only in their source/protocol domain.
- No-claim boundary: displayed history is bounded by discovery coverage/protocol and does not assert a singular conforming chain when alternatives survive.
- Rationale: a dedicated revision view makes history/gaps inspectable without forcing users to parse one giant report.

#### `C1.CC.CLI.003@1` — `mb objects`

- Identity, lifecycle, layer: active C1 L8 command contract; it exposes raw occurrences and view-scoped resolution as distinct projections.
- Inputs and identity domain: source/open artifact or evidence package plus its scoped `CheckedPackageHandleId`, graph/view selector, object key/occurrence/range query, resolve depth policy, optional credential lease, projection, and limits.
- Preconditions: selector IDs are exact; raw and resolved modes are explicit; plaintext output follows disclosure policy. A package-backed query requires IMM.013 coverage of the exact raw package, requested claim/artifact, and availability; direct source/open paths require no checker handle.
- Card slots: `SC.C1.CLI.OBJECTS.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: queried/visited objects, reference depth, decode/decrypt bytes, output bytes, diagnostics, and result count are bounded.
- Cancellation: traversal/decode checkpoints; no partial value is emitted as a singular resolved object.
- Authority and secrets: read-only; encrypted values remain ciphertext/refused without credential capability; plaintext requires protected output policy.
- Outputs and outcomes: raw occurrence(s) with visible/shadowed/unreachable/unknown classification or explicit unavailable frontier, effective resolved claim, paths/cycles, exact spans/virtual spans, revision/view/security context, and diagnostics.
- Diagnostics: unknown selector/key, ambiguous occurrence, missing/free object, cycle, decode/decrypt refusal, protected output denial, and limit.
- Evidence and provenance: every object/value projection binds source/graph/view/occurrence/path, cards/contracts, and decryption/filter receipts.
- Determinism and replay: D0 semantic projection under exact inputs/capabilities/limits.
- Falsifiers and Gauntlet: shadowed/unreachable/unknown objects, object-stream members, unchecked/stale/transplanted package handle, cycles, wrong generation, duplicate dictionaries, encrypted values, redaction, and cancellation.
- Surfaces: executable command, generated help/schema, capability manifest, and examples.
- Dependencies and consumers: depends on REV.005/REV.006/REV.009, DOC.001/DOC.002/DOC.009, SEC.001–SEC.009, FLT.001–FLT.010, RPT.005/RPT.007, IMM.013 for package-backed requests, and CLI.005–CLI.007; product gate consumes it.
- Migration and withdrawal: query/output schema changes version the contract; friendly object labels never replace typed graph/view IDs.
- No-claim boundary: a raw or resolved object projection does not validate higher-layer page, font, action, attachment, or security semantics.
- Rationale: separating occurrences from effective values preserves the forensic distinction between physical history and selected meaning.

#### `C1.CC.CLI.004@1` — Recovery-alternative surface

- Identity, lifecycle, layer: active C1 L8 sub-surface contract; recovery is an explicit mode of `mb inspect` and a report query, not a hidden default command path.
- Inputs and identity domain: strict report, recovery profile, search limits, alternative selector/task policy, optional credential lease, projection, and output sink.
- Preconditions: REC.002 admission succeeds; selector is a stable finalized hypothesis/view pair or no singular selection is requested.
- Card slots: `SC.C1.CLI.RECOVERY-ALTERNATIVES.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: search and output use shared limits; alternatives, assumptions, affected-scope summaries, diagnostics, and serialized bytes are bounded.
- Cancellation: search/projection terminal state is explicit; cancellation cannot select the last generated candidate.
- Authority and secrets: selection is task-scoped read authority only; no repair/write authority is introduced.
- Outputs and outcomes: frontier, ordering dimensions, evidence, material differences, security differences, discriminators, selection receipt or no-selection state, and exit mapping.
- Diagnostics: hidden recovery attempt, unknown/stale selector, inadmissible candidate, unresolved security difference, cap, and output truncation.
- Evidence and provenance: binds strict/recovery/enrichment report roots, source/final strict graph, every basis/view/consequence/hypothesis chain, profile/limits, all alternatives, selection policy, and caller role.
- Determinism and replay: D0 for exact search result/request; caller choice remains an attributed attestation.
- Falsifiers and Gauntlet: default-recovery leakage, alternative omission, stale selector, wider claim after selection, security conflict, cancellation, and round trips.
- Surfaces: `mb inspect` recovery options, saved RecoveryReport query, generated help/schema, and capability manifest.
- Dependencies and consumers: depends on REC.002–REC.010, RPT.002/RPT.005/RPT.007, and CLI.006/CLI.007; Workflow B consumes it.
- Migration and withdrawal: recovery option/profile changes version the surface; prior selections remain scoped to prior frontier.
- No-claim boundary: CLI selection does not turn malformed bytes into conformance, erase alternatives, or authorize writeback.
- Rationale: explicit alternatives keep the user workflow practical without hiding ambiguity behind a scalar preference.

#### `C1.CC.CLI.005@1` — Secure credential-input surface

- Identity, lifecycle, layer: active C1 L8 adapter contract; credential transport is separate from password preparation/decryption semantics.
- Inputs and identity domain: interactive protected prompt or explicitly supplied dedicated descriptor/handle, byte-versus-text form, target source/view, caller/tenant, and secret policy.
- Preconditions: channel can suppress ordinary echo/logging as documented; source input and credential channel cannot alias ambiguously.
- Card slots: `SC.C1.CLI.CREDENTIAL-INPUT.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: credential bytes, attempts, prompt reads, descriptor reads, memory lifetime, diagnostics, and timeout/cancellation are bounded.
- Cancellation: interrupted input yields cancellation without starting decryption; buffers enter secret disposal policy.
- Authority and secrets: plaintext credentials are rejected from command-line arguments, URLs, config serialization, ordinary environment variables, reports, and shell-completion history.
- Outputs and outcomes: opaque SEC.002 admission request with explicit byte/text form, or channel/authority/cancellation/refusal result.
- Diagnostics: channel unavailable, echo protection unknown, descriptor invalid, input too long, form missing, and attempt limit—never credential bytes.
- Evidence and provenance: non-secret receipt records channel class, target context, form, policy, and attempt; no secret identity is publicly committed.
- Determinism and replay: secret input is intentionally unavailable in `C1.CC.RPT.009@1` `ExecutionReplayBundle` artifacts; semantic decryption replay requires re-entry and the bundle records the missing-secret state.
- Falsifiers and Gauntlet: argv/env/process-list scans, terminal echo failure, descriptor reuse, stdin/source collision, huge inputs, cancellation, crash/log taint, and cross-tenant reuse.
- Surfaces: CLI adapter only; Rust callers use SEC.002 directly.
- Dependencies and consumers: depends on SEC.002, FDN.008, and CLI.007; CLI.001/CLI.003/CLI.004 consume it, while RPT.009 records only the exact missing-secret/re-entry boundary when a replay bundle is requested.
- Migration and withdrawal: unsafe channel is disabled; new transport class needs separate threat review and contract version.
- No-claim boundary: a protected prompt reduces ordinary exposure but cannot guarantee secrecy from a compromised terminal, OS, debugger, shell, or caller.
- Rationale: keeping credentials out of argv/environment avoids predictable host-level leakage while preserving explicit byte/text semantics.

#### `C1.CC.CLI.006@1` — Machine/human output projection

- Identity, lifecycle, layer: active C1 L8 adapter contract; JSON/JSONL are first-class schema projections and human output is generated from the same report.
- Inputs and identity domain: semantic report or registry, requested format/schema version, disclosure policy, stdout/stderr sinks with declared `Buffered`, `AtomicVisibility`, or `DurableCommit` class, color/locale policy for human rendering, and limits.
- Preconditions: source object is schema-valid; machine output is not mixed with human diagnostics on the same channel unless framed explicitly.
- Card slots: `SC.C1.CLI.OUTPUT-PROJECTION.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: records, bytes, rendering, redaction, diagnostics, and sink work are bounded.
- Cancellation: transactional output or terminal JSONL record states cancellation/truncation; broken pipes retain command outcome separately.
- Authority and secrets: disclosure policy applies identically across formats; terminal styling cannot reveal hidden fields.
- Outputs and outcomes: schema-tagged JSON, framed JSONL, or deterministic human rendering plus semantic report ID and projection receipt stating declared sink class and observed visibility/durability state.
- Diagnostics: format/schema unknown, framing error, redaction failure, sink short write/broken pipe, output limit, and rendering issue.
- Evidence and provenance: receipt binds semantic input root, projection version, disclosure, sink class, output identity, and losses/redactions.
- Determinism and replay: canonical machine projection is D0 where declared; terminal capabilities affect human rendering only and are recorded.
- Falsifiers and Gauntlet: JSON round trip, JSONL interruption, stdout/stderr separation, Unicode/bytes, secret taint, broken pipe, no-color mode, and schema drift.
- Surfaces: all C1 CLI commands, docs examples, shell automation, and saved reports.
- Dependencies and consumers: depends on RPT.005, FDN.008/FDN.015; CLI.001–CLI.004/CLI.008–CLI.010 consume it.
- Migration and withdrawal: projection schema change versions output; human copy cannot independently redefine fields.
- No-claim boundary: human legibility cannot strengthen report coverage or evidence and machine validity cannot establish report truth.
- Rationale: one projection path prevents CLI prose and automation schemas from drifting into different products.

#### `C1.CC.CLI.007@1` — Process status and outcome mapping

- Identity, lifecycle, layer: active C1 L8 contract; exit status is a coarse transport projection and machine output remains semantically authoritative.
- Inputs and identity domain: command admission result, canonical claim/operation outcome, publication/output state, usage state, and internal-invariant state.
- Preconditions: one terminal outcome exists; output sink state is known or indeterminate.
- Card slots: `SC.C1.CLI.EXIT-STATUS.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: negligible bounded mapping and terminal diagnostic work; reserved capacity survives diagnostic floods.
- Cancellation: interrupt maps to exit `6` only after cancellation reconciliation; an indeterminate publication maps to `7`.
- Authority and secrets: exit status leaks only coarse class; protected reason details stay in authorized structured output.
- Outputs and outcomes: `0` requested scoped `Complete`; `2` usage/admission error; `3` Partial; `4` Ambiguous; `5` Refused; `6` Cancelled; `7` Indeterminate; `8` contained internal defect.
- Diagnostics: if machine output cannot be written, stderr emits a bounded stable terminal code without changing semantic outcome.
- Evidence and provenance: run receipt binds semantic outcome, sink/publication state, numeric status, command contract, and build.
- Determinism and replay: mapping is D0 for the exact terminal record; signal/host termination outside reconciliation is reported by the host, not invented.
- Falsifiers and Gauntlet: every outcome/status pair, broken output, cancellation during commit, usage/document distinction, internal defect, and shell automation fixtures.
- Surfaces: all CLI commands, documentation, tests, and orchestration adapters.
- Dependencies and consumers: depends on FDN.006/FDN.010, RPT.005, and CLI.006; all other CLI command contracts consume it.
- Migration and withdrawal: numeric meanings are stable within major CLI contract; new semantic classes require major version/change record.
- No-claim boundary: status `0` applies only to the exact requested scope and never means whole-document or campaign-wide success.
- Rationale: stable coarse codes support automation while structured reports preserve nuance.

#### `C1.CC.CLI.008@1` — Capability/schema discovery surface

- Identity, lifecycle, layer: active C1 L8 command contract; `mb capabilities` and `mb schema <schema-id>` expose generated runtime truth.
- Inputs and identity domain: RPT.006 candidate capability manifest, IMM.012 audit receipt, RPT.008 admission envelope, schema registry, optional contract/profile/filter, requested projection, and output limits.
- Preconditions: the admission envelope binds the unchanged candidate manifest and matching audit receipt for the running build; requested schema ID/version exists. A candidate manifest alone is never presented as admitted.
- Card slots: `SC.C1.CLI.CAPABILITY-DISCOVERY.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: entries/fields/links, filter query, projection, diagnostics, and output bytes are bounded.
- Cancellation: cancelled generation cannot emit a current-looking partial manifest without an explicit partial terminal record.
- Authority and secrets: discovery exposes no protected dependency secrets, credentials, source contents, or restricted card bodies.
- Outputs and outcomes: exact contract/card/profile/lifecycle/no-claim rows, decision blocks, report schema, candidate-manifest root, audit-receipt root, admission-envelope root/status, and running-build identity.
- Diagnostics: stale/missing registry, unknown schema/contract/profile, inactive/pending card, output limit, and build mismatch.
- Evidence and provenance: output binds running build/toolchain, separate manifest/audit/admission/schema roots, generator, query, and projection without folding audit provenance into the candidate manifest.
- Determinism and replay: D0 under exact build/registry/query.
- Falsifiers and Gauntlet: candidate-only admission, manifest/audit root mismatch, disabled feature still listed, pending card advertised active, unknown schema, stale build, hidden no-claim, secret field, and output round trip.
- Surfaces: executable commands, generated help, automation, OpenReport link, and docs.
- Dependencies and consumers: depends on RPT.006/RPT.008, IMM.004/IMM.010/IMM.012, and CLI.006/CLI.007; product/close gates consume it.
- Migration and withdrawal: command/schema change versions surface; old manifest remains artifact-scoped.
- No-claim boundary: discovery declares what the build admits; it does not prove a requested input will exercise every path or pass its gate.
- Rationale: early discovery turns unsupported profiles/algorithms into predictable admission outcomes instead of runtime surprises.

#### `C1.CC.CLI.009@1` — `mb package check`

- Identity, lifecycle, layer: active C1 L8 command contract; it is a narrow adapter over the hostile-input standalone checker.
- Inputs and identity domain: one immutable package byte source, check policy, explicit artifact materialization capabilities, limits, projection, and output sink.
- Preconditions: checker isolation is ratified; IMM.014 pre-run admission exists; running checker capability manifest/schema matches the requested package protocol. IMM.020 is required only when the requested evidence scope claims final assessed lineage; if that assessment is absent, raw checking remains available but lineage-dependent language and status are narrowed or unavailable.
- Card slots: `SC.C1.CLI.PACKAGE-CHECK.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: package/check/materialization/output work shares one account; no package-controlled value resets limits.
- Cancellation: interrupt reconciles private materializations and emits partial/refused coverage, never a passing prefix.
- Authority and secrets: no ambient retrieval; protected artifacts require explicit capabilities and output disclosure.
- Outputs and outcomes: checker report, package/root/schema status, checked/unsupported claims, availability/coverage, diagnostics, exit mapping, and checker identity.
- Diagnostics: hostile package failures remain separate from command usage/sink errors and include no protected payload excerpts by default.
- Evidence and provenance: command receipt binds package source, checker build/protocol/capabilities, policy/limits, report root, projection, and run envelope.
- Determinism and replay: semantic check targets D0 under exact inputs; materialization availability may narrow replay.
- Falsifiers and Gauntlet: malformed/bomb packages, missing artifact, unavailable secret, cancellation, broken pipe, checker mismatch, producer assembler unavailable, and producer/checker disagreement when an optional producer package is supplied.
- Surfaces: executable command, generated help/schema, capability manifest, and C1 evidence handoff.
- Dependencies and consumers: depends on IMM.013/IMM.014, CLI.006/CLI.007, and BYT.001; in state transition `pre-run-check-enabled -> final-lineage-claim-enabled`, additionally consumes IMM.020 only after the requested evidence scope requires and supplies the matching final assessment. Raw IMM.016 outputs are optional hostile interoperability inputs rather than an implementation prerequisite; close gate may consume the command result.
- Migration and withdrawal: checker/package protocol change versions the command row; old reports remain scoped.
- No-claim boundary: a passing package-root check does not validate unavailable evidence or the underlying PDF semantics.
- Rationale: exposing the checker as a separate command makes its trust boundary visible and usable by a fresh evaluator.

#### `C1.CC.CLI.010@1` — `mb validate`

- Identity, lifecycle, layer: active C1 L8 command contract; it is a thin invocable projection of DOC.007 and RPT.010 for the exact C1 validation layers 1–3.
- Inputs and identity domain: one admitted source/open artifact, exact source-backed `RevisionGraphId` and `DocumentViewId` selector, active C1 validation profile/profile version, rule-set identity/version, requested layer/rule projection, limits, disclosure policy, and output sink.
- Preconditions: source/open and exact view/graph admission succeed; every executed normative rule has an active reviewed card; the requested profile contains only C1 structural-consistency, declared-constraint-consistency, and independently sourced model-check layers. Unsupported, unavailable, pending, or unrun rules remain explicit and cannot pass.
- Card slots: `SC.C1.CLI.VALIDATE.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: open/validation work shares one account; selected rules/layers, findings, source and virtual locations, canonicalization, diagnostics, projection, and output bytes are bounded.
- Cancellation: interruption preserves exact per-layer/per-rule coverage through RPT.010 and maps unvisited rules to `NotEvaluated` or `Indeterminate`; a completed-looking prefix is never emitted.
- Authority and secrets: read-only and card/profile bounded; no external validator, ambient I/O, trust provider, writer, repair, or disclosure beyond the selected policy is authorized.
- Outputs and outcomes: emits the immutable RPT.010 `ValidationReportId`, separate layer 1–3 summaries and per-rule outcomes/coverage/locations, unsupported classes, exact machine outcome, projection receipt, and CLI.007 exit mapping.
- Diagnostics: usage/selector/profile/rule-set errors remain separate from validation outcomes; pending card, unsupported layer/profile, unavailable artifact, identity mismatch, cancellation, output failure, and rule-engine fault retain distinct codes.
- Evidence and provenance: command receipt binds source/open root, exact graph/view, profile/rule/card set, RPT.010 root, requested projection, limits, disclosure, build/toolchain, used capabilities, and run envelope.
- Determinism and replay: semantic validation is D0 under the exact view/graph/profile/rules/cards/limits; CLI.006 owns projection and RPT.004/RPT.009 retain observation/replay boundaries.
- Falsifiers and Gauntlet: layer pass inferred from another layer, unrun/pending rule promoted to pass, unsupported standardized profile request, stale graph/view, partial coverage, cancellation, broken output, secret/location redaction, schema round trip, and inspect-versus-validate RPT.010 root agreement.
- Surfaces: executable `mb validate`, generated help/schema, capability manifest, saved RPT.010 report, automation, and the C1 product/close gates.
- Dependencies and consumers: depends on DOC.007/DOC.009, RPT.010, and CLI.006/CLI.007; FUZ.010 and the product/close gates consume it.
- Migration and withdrawal: command/profile/rule/projection semantics change versions the surface; a withdrawn card lapses only affected results and never rewrites historical reports.
- No-claim boundary: `mb validate` covers only active C1 layers 1–3; it does not establish whole-document conformance, PDF/A/PDF/UA or another standardized profile, renderer behavior, external-validator agreement, source safety, signature trust, or repair authority.
- Rationale: the active C1 validation report needs its own deterministic §25.3 command without importing later standardized-profile validation.

### 8.12 Fuzz, hostile-input, and corpus contracts

#### `C1.CC.FUZ.001@1` — Fuzz input manifest and rights gate

- Identity, lifecycle, layer: active C1 L7 tool contract; every seed/generator/mutator/corpus item has provenance, rights, partition, sensitivity, expected claim, and expected no-claim metadata.
- Inputs and identity domain: seed/generator artifact, source/provenance, license/use/model-visibility flags, contract/cards, partition, sensitivity, and manifest protocol.
- Preconditions: item is rights-admitted for the exact fuzz/model/CI use; held-out bytes are inaccessible to implementation agents.
- Card slots: `SC.C1.FUZ.INPUT-MANIFEST.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: manifest items/bytes, retrieval, generated cases, retention, diagnostics, and witness output are bounded.
- Cancellation: interrupted import/generation cannot admit an unreviewed seed or mispartition an item.
- Authority and secrets: private/held-out inputs remain access-controlled; public digests follow confidential/low-entropy disclosure policy.
- Outputs and outcomes: admitted/quarantined/refused item record, exact target links, partition, expected behavior/no-claim, and provenance/rights evidence.
- Diagnostics: unknown license/source, model-use denied, prohibited lineage, missing card/contract, partition leak, sensitive disclosure, and duplicate identity.
- Evidence and provenance: root binds item identity/availability, rights record, source date, partition steward, linked contracts/cards/incidents, and tool version.
- Determinism and replay: generated item identity is D0 under pinned generator/seed/protocol where applicable; mutable external generators are not admitted silently.
- Falsifiers and Gauntlet: unknown-license seed, held-out leak, prohibited marker, low-entropy digest, wrong partition, stale card, and cancelled import.
- Surfaces: every fuzz target, corpus registry, witness minimizer, tombstone, drift/card gate, and trial record.
- Dependencies and consumers: depends on IMM.001/IMM.011, FDN.008/FDN.015; FUZ.002–FUZ.016 consume it.
- Migration and withdrawal: rights/partition change quarantines affected items/results and requires fresh evidence; records are not deleted.
- No-claim boundary: manifest admission does not prove a seed is correct, representative, independent, or held out beyond its access controls.
- Rationale: fuzzing cannot become a clean-room, privacy, or holdout backdoor.

#### `C1.CC.FUZ.002@1` — Byte-source/range target family

- Identity, lifecycle, layer: active C1 L7 target contract; it attacks source adapters, snapshot identity, ranges, spooling, partial availability, and source-change handling.
- Inputs and identity domain: manifest-admitted byte programs/adapters, operation scripts, range responses, mutations, limits, and oracle properties.
- Preconditions: harness cannot access real mutable hosts/network implicitly; simulated source changes are explicit.
- Card slots: `SC.C1.FUZ.BYTE-SOURCE.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: fuzz input, operations, ranges, spool/cache bytes, execution time/quanta, diagnostics, and witness bytes are bounded.
- Cancellation: harness injects cancellation at read/spool/promotion/revalidation checkpoints and verifies accounting/terminal state.
- Authority and secrets: synthetic/non-secret by default; no path/network authority beyond isolated fixtures.
- Outputs and outcomes: crash/panic/hang/resource/source-identity/range/provenance findings with deterministic witness and target/build identity.
- Diagnostics: distinguish target defect, expected source error, limit, cancellation, harness fault, and invalid seed.
- Evidence and provenance: finding binds manifest item, mutation/generator, target contract/build, limits, trace, and minimized witness.
- Determinism and replay: witness replays the declared semantic property; nondeterministic host faults remain explicitly classified.
- Falsifiers and Gauntlet: overflow, short/conflicting reads, truncation, mutable mmap adapter, sparse/overlapping ranges, promotion cancellation, and cache invalidation.
- Surfaces: continuous/local fuzz harness and C1 panic/resource gate.
- Dependencies and consumers: depends on FUZ.001; targets BYT.001–BYT.005 plus FDN.003–FDN.013; FUZ.011/FUZ.012 consume findings.
- Migration and withdrawal: target/harness change versions coverage; a non-replaying witness remains open/harness-indeterminate.
- No-claim boundary: corpus survival does not establish safety for all inputs or hosts.
- Rationale: source mutability and offset arithmetic are foundational failure points that downstream fuzzing may not isolate.

#### `C1.CC.FUZ.003@1` — Lexer/COS target family

- Identity, lifecycle, layer: active C1 L7 target contract; separate targets cover tokenization, raw scalar/container parsing, duplicates, and stream syntax boundaries.
- Inputs and identity domain: arbitrary bytes plus grammar-aware generated token/COS structures, mode, limits, and property oracle.
- Preconditions: normative expectations use only reviewed cards/fixtures; arbitrary-byte robustness properties need no guessed semantics.
- Card slots: `SC.C1.FUZ.LEXER-COS.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: input bytes, tokens/containers/depth, allocations, diagnostics, execution, and witness bytes are bounded.
- Cancellation: injected at token/container/boundary checkpoints with no visible partial tree/cache.
- Authority and secrets: in-memory synthetic source; no host capabilities.
- Outputs and outcomes: reachable panic/hang/resource-account/round-trip/span/duplicate/terminal-state finding with reproducible witness.
- Diagnostics: expected parse refusal remains separate from harness/target invariant defect.
- Evidence and provenance: binds seed/generator, cards where used, target/build, semantic limits, trace, and minimization.
- Determinism and replay: D0 property under exact witness/build/limits.
- Falsifiers and Gauntlet: arbitrary bytes, deep nesting, token storms, huge numbers/names/strings, duplicate maps, marker payloads, allocation failure, and cancellation.
- Surfaces: lexer/COS continuous/local targets and C1 panic gate.
- Dependencies and consumers: depends on FUZ.001; targets SYN.001–SYN.007 and FDN.004–FDN.014; FUZ.011/FUZ.012 consume findings.
- Migration and withdrawal: target/card changes version coverage; stale coverage cannot support a new parser build.
- No-claim boundary: a fuzz target does not provide standards conformance by itself.
- Rationale: raw syntax has the widest attacker-controlled state space and must be exercised before semantic layers.

#### `C1.CC.FUZ.004@1` — Xref/revision target family

- Identity, lifecycle, layer: active C1 L7 target contract; it attacks tables, streams, hybrid links, terminal discovery, graphs, occurrences, and signature ranges.
- Inputs and identity domain: arbitrary/structure-generated sources, xref/revision mutation program, cards/fixtures where admitted, profile, and limits.
- Preconditions: any normative expected result is card-linked; robustness properties remain structural.
- Card slots: `SC.C1.FUZ.XREF-REVISION.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: source/decoded bytes, sections/entries/nodes/edges/candidates, scans, canonicalization, diagnostics, execution, and witness bytes are bounded.
- Cancellation: injected through terminal scan, section parse, link walk, graph finalization, and signature-range analysis.
- Authority and secrets: synthetic in-memory source; no external observations or retrieval.
- Outputs and outcomes: panic/hang/overflow/graph/canonicalization/provenance/coverage/terminal-state defect with minimized witness.
- Diagnostics: expected malformed/recovery result is separate from invariant failure.
- Evidence and provenance: finding binds mutation/seed, target/build, card/profile/limits, graph/report identities, and trace.
- Determinism and replay: D0 property for exact witness/build/protocol/limits.
- Falsifiers and Gauntlet: huge/overlapping entries, link cycles/forks, false markers/objects, table-stream disagreement, partial source, range overflow, raw signature `/Filter`/`/SubFilter` family and seed/lock carrier mutations without cryptographic interpretation, symmetry, and cancellation.
- Surfaces: xref/revision continuous/local targets and C1 gate.
- Dependencies and consumers: depends on FUZ.001; targets SYN.003, BYT.006, REV.001–REV.009, and FDN.014; FUZ.011/FUZ.012/FUZ.014 consume findings.
- Migration and withdrawal: parser/graph protocol changes version coverage and corpus expectations.
- No-claim boundary: fuzzing cannot establish one historical interpretation for all malformed files.
- Rationale: revision graphs combine arithmetic, cycles, scanning, and canonicalization, making them a distinct hostile-input family.

#### `C1.CC.FUZ.005@1` — Object-stream target family

- Identity, lifecycle, layer: active C1 L7 target contract; it attacks header indexing, offsets, virtual spans, decode/decrypt context, and member parsing.
- Inputs and identity domain: generated/mutated containers, xref records, security/filter context, credentials from synthetic fixtures, cards, and limits.
- Preconditions: secrets are synthetic/non-retained; expected semantics are card-linked.
- Card slots: `SC.C1.FUZ.OBJECT-STREAM.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: compressed/plain bytes, members, offsets, parse work, cache bytes, diagnostics, execution, and witness bytes are bounded.
- Cancellation: injected through decrypt/decode/index/member parse/commit and cache publication.
- Authority and secrets: isolated synthetic contexts; partition assertions ensure no cross-credential/tenant plaintext.
- Outputs and outcomes: panic/hang/double-decrypt/offset/provenance/cache/transaction defect with replayable witness.
- Diagnostics: expected malformed/decryption refusal is not a target defect.
- Evidence and provenance: binds container seed/context, stage receipts, target/build/cards/limits, trace, and minimized witness.
- Determinism and replay: D0 property under exact synthetic secret/context/witness/build.
- Falsifiers and Gauntlet: wrong first/count, duplicate/nonmonotone offsets, truncation, nested streams, double decrypt, cross-context cache, and cancellation.
- Surfaces: object-stream continuous/local target and C1 gate.
- Dependencies and consumers: depends on FUZ.001; targets REV.006, FLT.001–FLT.010, SEC.009, and FDN.013; FUZ.011/FUZ.012 consume findings.
- Migration and withdrawal: context/parser changes version target coverage; secret fixtures rotate without changing claimed semantics.
- No-claim boundary: object-stream fuzzing does not cover arbitrary document semantics or all cryptographic profiles.
- Rationale: container membership and one-time decryption are subtle enough to need an isolated target.

#### `C1.CC.FUZ.006@1` — Lossless-filter target family

- Identity, lifecycle, layer: active C1 L7 target contract; each named C1 filter and predictor has a standalone target plus declared-chain composition target.
- Inputs and identity domain: arbitrary/stage-aware bytes, distinct internal `/Filter`/`/DecodeParms` and external `/FFilter`/`/FDecodeParms` shapes, raw `/DL` hints, chain definitions, independent inspect/decode cursor programs, transactional sink/drop/durability fault script, cards/fixtures, and limits.
- Preconditions: normative vectors/expectations are rights/card-admitted; arbitrary-byte robustness runs independently.
- Card slots: `SC.C1.FUZ.LOSSLESS-FILTERS.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: input/output/ratio, decoder state, chain stages, sink faults, CPU, diagnostics, execution, and witness bytes are bounded.
- Cancellation: injected at chunks/stages/commit/abort; no partial cache-visible output is permitted.
- Authority and secrets: synthetic non-secret streams; Crypt-stage composition uses FUZ.007 contexts.
- Outputs and outcomes: panic/hang/bomb/no-progress/wrong-count/cursor/unterminated-drop/virtual-offset/transaction/durability/provenance/determinism finding with minimized witness.
- Diagnostics: expected decode refusal/resource limit is separate from invariant failure.
- Evidence and provenance: binds exact filter contract/version/parameters, seed/mutation, cards, build, limits, receipts, and trace.
- Determinism and replay: D0 property for exact witness/decoder/build/limits; chunk-boundary metamorphism is required.
- Falsifiers and Gauntlet: ASCIIHex, ASCII85, RunLength, Flate, predictors, LZW/EarlyChange, internal/external chain shapes/order/alignment, malformed and adversarial `/DL` hints that never allocate or prove sufficiency, independent inspect/decode cursors, empty non-EOF chunk, nonmonotone or unchecked consumption, borrow escape, unterminated-drop poisoning, exact stage plus virtual decoded failure offset, each declared sink durability class, bombs, sink faults, cancellation, and no-progress.
- Surfaces: per-filter/chain continuous/local targets and C1 gate.
- Dependencies and consumers: depends on FUZ.001; targets FLT.001–FLT.010, FDN.004–FDN.006, FDN.009, and FDN.012–FDN.014; FUZ.011/FUZ.012 consume findings.
- Migration and withdrawal: each decoder/adapter change invalidates only its scoped coverage plus affected composition lanes.
- No-claim boundary: filter target survival does not establish dependency freedom from all logic defects or image/render correctness.
- Rationale: atomic and composition targets catch both decoder defects and planner/transaction drift.

#### `C1.CC.FUZ.007@1` — Password/decryption target family

- Identity, lifecycle, layer: active C1 L7 target contract; it covers inventory, byte/text credential forms, handler matrix, password preparation, key/object context, RC4/AESV2/AESV3, routing, and plaintext isolation.
- Inputs and identity domain: rights-admitted synthetic encrypted fixtures/vectors, wrong credentials, dictionary mutations including independent `/P`, `/Perms`, and `/EncryptMetadata` occurrences plus raw public-key and technical-specification carriers, object/revision contexts, owner/user role labels, secret policy, and limits.
- Preconditions: crypto provider selections remain symbolic/unavailable until D-005 ratification; normative vectors are approved and card-linked.
- Card slots: `SC.C1.FUZ.STANDARD-HANDLER-READ.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: attempts, KDF/crypto work, input/plaintext bytes, memory, diagnostics, execution, and witness retention are bounded.
- Cancellation: injected before/within preparation, derivation, decrypt, commit, cache, and disposal.
- Authority and secrets: synthetic credentials/plaintext never enter ordinary logs/witness metadata; target verifies partitions and disposal receipts.
- Outputs and outcomes: panic/hang/wrong-context/plaintext-leak/double-decrypt/diagnostic/transaction defect with protected witness recipe.
- Diagnostics: expected wrong credential/unsupported profile/resource outcome remains separate from target defect.
- Evidence and provenance: binds fixture rights/cards, provider/build, security/object context, limits, non-secret trace, and protected witness availability.
- Determinism and replay: D0 property requires re-supplying synthetic secret; public metadata cannot reconstruct it.
- Falsifiers and Gauntlet: byte/text boundaries, owner/user role labels, wrong credential/context, revision/object generation, filter defaults, valid/invalid/not-applicable/unsupported/unavailable `/Perms` independently varied from `/P`, duplicate-preserved `/EncryptMetadata`, raw public-key recipient/crypt-filter/declared-algorithm inventory without decryption, core versus unverified/pending technical-specification classification, actual recoverability independently varied from cryptographic access/declared permissions/host policy, object streams, malformed ciphertext, cancellation, and cross-tenant cache.
- Surfaces: security continuous/local targets and C1 credentialed gate.
- Dependencies and consumers: depends on FUZ.001; targets SEC.001–SEC.009 and FLT.009; FUZ.011/FUZ.012 consume findings.
- Migration and withdrawal: provider/card/matrix change versions coverage; a secret leak quarantines affected witnesses/caches and triggers incident handling.
- No-claim boundary: tests do not establish whole-process side-channel immunity, algorithm strength, public-key decryption support, permission enforcement, or encryption output.
- Rationale: security correctness depends on exact version/object/filter context, not just primitive test vectors.

#### `C1.CC.FUZ.008@1` — Resolver/recovery target family

- Identity, lifecycle, layer: active C1 L7 target contract; it attacks reference cycles, effective views, structural trees, recovery families/search/order/selection, and security-across-alternatives.
- Inputs and identity domain: generated/mutated graph/document structures, strict defects, header/EOF-placement candidates, DOC.012–DOC.015 inventory candidates including metadata-revision conflicts and hostile XML shapes, recovery profiles/budgets, optional synthetic credentials, cards, and property oracle.
- Preconditions: normative structural expectations are card-linked; recovery generators declare violated rule/family when atomic.
- Card slots: `SC.C1.FUZ.RESOLVER-RECOVERY.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: objects/references/depth, hypotheses/branches/comparisons, canonicalization, decoded bytes, diagnostics, execution, and witness bytes are bounded.
- Cancellation: injected throughout resolution/search/order/selection/report; no partial singular result or leaked lease.
- Authority and secrets: synthetic read/decrypt only; no writer or external observation.
- Outputs and outcomes: panic/hang/resource-account/alternative-loss/wrong-selection/provenance/cache/security-laundering finding with witness.
- Diagnostics: expected cycle/ambiguity/refusal/limit is separate from invariant defect.
- Evidence and provenance: binds generator/family/cards, graph/view/search protocol, limits, build, trace, and minimized witness.
- Determinism and replay: D0 property under exact witness/protocol/semantic limits.
- Falsifiers and Gauntlet: cycles/depth, missing catalogs/page links, page-continuity alternatives and forbidden object/source-ID equality inference, every initial recovery family including common header/EOF-placement deviations, all four named R0 inventory owners, cross-revision Info/XMP conflicts, DTD/entity/XInclude/external-resource attempts, XML depth/attribute/text/name/namespace limits, branch storms, Pareto permutations, security differences, stale selection, and cancellation.
- Surfaces: resolver/recovery continuous/local targets and C1 gate.
- Dependencies and consumers: depends on FUZ.001; targets DOC.001–DOC.015, REC.001–REC.010, and FDN.014; FUZ.011/FUZ.012/FUZ.014 consume findings.
- Migration and withdrawal: family/order changes version target expectations; misleading hypotheses become tombstones/regressions.
- No-claim boundary: withheld recovery intent and corpus survival do not yield a universal recovery confidence score.
- Rationale: recovery’s oracle problem needs properties about bounds, alternatives, and non-laundering, not only one expected document.

#### `C1.CC.FUZ.009@1` — Report/checker target family

- Identity, lifecycle, layer: active C1 L7 target contract; it treats reports/packages as hostile schema/canonicalization/availability inputs.
- Inputs and identity domain: generated/mutated Open/Recovery/security/enrichment/validation/replay/capability-admission reports, packages, schemas, identities, artifacts/availability classes, pre-run/final checker-lineage records, check policies, and limits.
- Preconditions: schemas/registries are active; producer and checker target implementations remain isolated per IMM.014.
- Card slots: `SC.C1.FUZ.REPORT-CHECKER.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: bytes/nodes/depth/claims/artifacts, canonicalization, materialization, diagnostics, execution, and witness bytes are bounded.
- Cancellation: injected through parse/walk/root/materialization/report; a checked prefix cannot pass.
- Authority and secrets: generated non-secret by default; protected-artifact cases use identity-only synthetic handles and taint assertions.
- Outputs and outcomes: panic/hang/ambiguous-root/schema/coverage/availability/producer-checker-drift/leak finding with witness.
- Diagnostics: expected hostile rejection/resource outcome is separate from checker invariant failure.
- Evidence and provenance: binds schema/package/checker/build roots, mutation, limits, trace, and minimized witness.
- Determinism and replay: D0 property under exact witness/checker/protocol/limits.
- Falsifiers and Gauntlet: duplicate/conflicting IDs, missing mandated identities, validation-layer collapse or illegal per-rule outcome, replay-relation/capture/comparator overstatement, missing secret/host/tool state, unknown critical fields, unavailable artifacts, bombs, cancellation, run/semantic contamination, and shared-bug seeds.
- Surfaces: schema/package/checker continuous/local targets and C1 gate.
- Dependencies and consumers: depends on FUZ.001; targets RPT.001–RPT.010 and IMM.004/IMM.013–IMM.016/IMM.020; FUZ.011/FUZ.012/FUZ.014 consume findings.
- Migration and withdrawal: schema/checker change versions target corpus/coverage.
- No-claim boundary: checker robustness does not prove underlying PDF observations or independent correctness.
- Rationale: evidence machinery is itself an attacker-facing parser and must inherit the same hostile-input laws.

#### `C1.CC.FUZ.010@1` — Resource/cancellation/concurrency target family

- Identity, lifecycle, layer: active C1 L7 cross-cutting target contract; it injects budgets, cancellation, allocation/sink faults, parallelism, and cache races across C1.
- Inputs and identity domain: operation scenario including CLI.001–CLI.010 request/option parsing, saved-artifact admission, projection/framing, output sink, and interrupt paths; checkpoint schedule, resource/fault script, worker/cache schedule, source/credential partitions, exact command/candidate build, and limits.
- Preconditions: target operation exposes registered checkpoints and resource classes; concurrency model matches admitted implementation.
- Card slots: `SC.C1.FUZ.RESOURCE-CANCEL-CONCURRENCY.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: schedules/steps, workers, faults, memory, diagnostics, execution, state captures, and witness bytes are bounded.
- Cancellation: this target controls injection and verifies bounded observation, no new work, private-state handling, resource conservation, and terminal result.
- Authority and secrets: schedules cannot widen leases; tenant/credential partitions are asserted under every interleaving.
- Outputs and outcomes: panic/deadlock/livelock/race/leak/double-refund/partial-publication/nondeterminism/isolation finding with replay relation.
- Diagnostics: distinguish injected fault/expected outcome, harness schedule limit, non-replayable race, and target invariant defect.
- Evidence and provenance: binds scenario/schedule/faults, build/contracts, limits, trace/capture mode, observer effects, and witness.
- Determinism and replay: deterministic schedulers target exact replay; native races retain probabilistic observation and repeated witness metadata without stronger claims.
- Falsifiers and Gauntlet: every checkpoint class, CLI unknown/duplicate/oversized option and hostile value, unchecked saved package, schema mismatch, JSON/JSONL terminal framing, output truncation, broken pipe, redaction, interrupt/reconciliation, sibling reservations/refunds, commit/abort, cache insert/evict, diagnostic collector, source change, credential crossing, and thread count.
- Surfaces: all C1 targets, cancellation gate, panic gate, drift evidence, and trial record.
- Dependencies and consumers: depends on FUZ.001; targets FDN.004–FDN.014, CLI.001–CLI.010, and every transactional/cache-bearing contract; FUZ.011/FUZ.012/FUZ.014 consume findings.
- Migration and withdrawal: new checkpoint/resource class requires target coverage; old results do not cover changed concurrency semantics.
- No-claim boundary: explored schedules do not prove absence of all concurrency faults or host failures.
- Rationale: concurrency and cancellation can violate safety/evidence without malformed syntax, so they need an orthogonal target family.

#### `C1.CC.FUZ.011@1` — Reachable-panic release gate

- Identity, lifecycle, layer: active C1 L7 gate contract; any panic reachable from admitted hostile input at a public boundary is a defect.
- Inputs and identity domain: exact candidate build, FUZ.016 baseline root, active target/corpus roots, FUZ.014 run manifests/receipts, panic/crash/hang findings, dispositions, and coverage manifest.
- Preconditions: every C1 hostile-input public/parser/decoder/checker surface maps to a target; build/toolchain/profile are exact; D7 is ratified. **PROPOSED default — awaiting ratification (D7):** the runtime/release candidate uses an exact stable pin while fuzz/Miri/sanitizer findings use a separate date-pinned nightly and never supply the shipped artifact.
- Card slots: `SC.C1.FUZ.REACHABLE-PANIC-GATE.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: gate aggregation, witness replay, target/corpus records, diagnostics, and report bytes are bounded; execution campaigns are separately resource-governed.
- Cancellation: cancelled/missing target runs make the gate indeterminate/failing; they cannot count as no finding.
- Authority and secrets: protected witnesses use restricted availability; gate summary contains no secret/source payload.
- Outputs and outcomes: pass only with zero unresolved reachable panics over the declared target/corpus/build envelope; failures list witnesses, target, status, and sibling search.
- Diagnostics: unreachable internal programmer panic proof gap, reachable panic, abort strategy limitation, missing target/run, stale build, non-replaying witness, and harness fault.
- Evidence and provenance: gate root binds candidate build/toolchain, pre-run fuzz baseline, target/corpus/run manifests and receipts, every finding/disposition, replay results, and coverage graph.
- Determinism and replay: gate is D0 over recorded results; it does not infer unexecuted input space.
- Falsifiers and Gauntlet: seeded reachable panic in each family, panic during diagnostic/abort/drop, dependency panic, missing-run attempt, and stale-build substitution.
- Surfaces: product/cycle-close gate, capability manifest, trial record, and evidence package.
- Dependencies and consumers: depends on FUZ.001–FUZ.010/FUZ.012/FUZ.014/FUZ.016, FDN.016, and IMM.009/IMM.012; FUZ.015 and the C1 gates consume it.
- Migration and withdrawal: any candidate change invalidates pass evidence until scoped reruns/replay cover affected targets; new reachable panic withdraws affected capability row. A toolchain change is a versioned determinism event and reruns affected D-class, fuzz, and reproducibility lanes before admission.
- No-claim boundary: zero unresolved panics in the declared corpus/run envelope is not a universal proof of no panic, memory safety, or availability.
- Rationale: the gate states exactly what was exercised while treating every input-reachable panic as unacceptable.

#### `C1.CC.FUZ.012@1` — Witness minimization and tombstones

- Identity, lifecycle, layer: active C1 L7 operational-memory contract; every defect retains a minimized witness or explicit minimization limit plus the killed assumption.
- Inputs and identity domain: original finding/witness, target/build, minimization transforms, semantic predicate, cards/contracts, sibling-site search, fix evidence, consumed compute, consumed human attention, disclosure classes, and retention policy.
- Preconditions: minimization preserves the triggering property under exact build/limits; protected data is not declassified.
- Card slots: `SC.C1.FUZ.WITNESS-TOMBSTONE.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: attempts, executions, compute, human-attention accounting, witness bytes, semantic checks, sibling searches, diagnostics, and retained artifacts are bounded.
- Cancellation: interrupted minimization keeps the smallest verified-so-far witness and exact attempt/frontier record.
- Authority and secrets: corpus promotion/redistribution follows rights/privacy; tombstone can refer to restricted witness by protected identity.
- Outputs and outcomes: minimized witness, regression property/fixture link, violated assumption, affected contracts, sibling search, fix evidence, tombstone/replacement rule, exact consumed compute and human attention with disclosure class/availability, and limits.
- Diagnostics: non-reproducing candidate, property drift, privacy/right block, minimization cap, stale build, missing sibling search, and false closure.
- Evidence and provenance: record binds original/minimized identities, every attempted transform/outcome, build/target, cards/contracts, compute/attention accounting source and disclosure state, and reviewer disposition.
- Determinism and replay: witness supports only its exact property/replay relation; nondeterministic failures retain attempt distribution and limits.
- Falsifiers and Gauntlet: minimizer deleting trigger, secret leak, one-input-only fix, missing contract update, stale corpus, repeated tombstoned heuristic, and cancellation.
- Surfaces: bug closure, corpus registry, drift audit, target seeds, trial record, and evidence package.
- Dependencies and consumers: depends on FUZ.001–FUZ.010 and IMM.002/IMM.009/IMM.012; FUZ.011 and the close gate consume minimized-witness/unresolved status.
- Migration and withdrawal: tombstones are append-only; a replacement failure adds a successor record rather than deleting history.
- No-claim boundary: a minimized witness demonstrates one failure class, not frequency or representativeness.
- Rationale: metabolized failures stop local patches and retired heuristics from recurring without context.

#### `C1.CC.FUZ.013@1` — Corpus partition and held-out isolation

- Identity, lifecycle, layer: active C1 L7 governance contract; development, regression, private, and steward-held-out partitions are distinct and access-controlled.
- Inputs and identity domain: item manifests, partition/steward commitments, access policy/log, submission/feedback budget, reveal rule, replacement reserve, and disclosure policy.
- Preconditions: held-out seal predates implementation access; unavailable steward/seal is recorded and cannot be reconstructed.
- Card slots: `SC.C1.FUZ.CORPUS-PARTITION.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: submissions/queries, feedback, access events, corpus bytes where authorized, evaluation output, and diagnostics are bounded.
- Cancellation: cancelled submission consumes budget according to committed protocol and returns no hidden per-case leakage.
- Authority and secrets: implementation agents cannot access held-out bytes/summaries/embeddings/caches/dashboards; only admitted artifact/protocol reaches evaluator.
- Outputs and outcomes: partition registry, seal/access/submission record, aggregate feedback as predeclared, reveal/demotion state, and fresh replacement requirement.
- Diagnostics: pre-seal access, unauthorized reveal, feedback excess, provider-retention unknown, missing steward, partition alias, and confidential commitment risk.
- Evidence and provenance: record binds steward/protocol, item commitments/availability, access log, artifact submission, feedback, and reveal/demotion events.
- Determinism and replay: evaluation record is D0 for logged events/protocol; hidden artifact bytes may remain unavailable.
- Falsifiers and Gauntlet: seeded access leak, cache/embedding leak, repeated adaptive feedback, missing/changed seal, unauthorized dashboard, and demotion after reveal.
- Surfaces: held-out C1 probe, corpus registry, trial record, close gate, and future cycle evidence.
- Dependencies and consumers: depends on FUZ.001, human day-zero sealing, commitment substrate, FDN.008/FDN.015; FUZ.014–FUZ.016 and the C1 campaign gate consume it.
- Migration and withdrawal: once feedback shapes implementation beyond policy, the set becomes development/regression and a fresh sealed replacement is required.
- No-claim boundary: without a pre-implementation independent seal/access protocol, a test set is not represented as held out or independent.
- Rationale: held-out status is an access history, not a filename or secret label.

#### `C1.CC.FUZ.014@1` — Assurance-run manifest and execution receipt

- Identity, lifecycle, layer: active C1 L7 execution-record contract; one manifest declares one bounded assurance run before launch and one receipt records its terminal observation without rewriting the declaration.
- Inputs and identity domain: FUZ.016 baseline, lane/target/run-class IDs including general suite mutation/fault-seeding, exact candidate and guidance-instrumented build/toolchain/dependency roots, corpus/fixture/seed roots and rights, target configuration, versioned guidance metric/schema, initial queue/corpus state, semantic/resource limits, schedule/fault profile, declared mutation/fault seeds with expected detection class, worker identity, general `OracleLineageId`, pre-run manifest root, and prospective-ledger event IDs.
- Preconditions: baseline admits the lane; target/corpus/card/rights coverage is active; coverage-guided lanes bind exact instrumentation and feedback policy before launch; runtime and crypto-provider choices remain symbolic until their human ratifications; start event is prospectively appended through IMM.017 before execution.
- Card slots: `SC.C1.FUZ.ASSURANCE-RUN-RECEIPT.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: input cases, executions, mutations/schedules, CPU/memory/storage, findings, witness bytes, diagnostics, and receipt bytes are bounded by the declared run envelope.
- Cancellation: cancelled/expired/crashed/harness-failed runs retain exact terminal state, processed scope, outstanding work, and reconciliation; none can be represented as a passing run.
- Authority and secrets: executor receives only declared local fixtures/corpora and narrow capabilities; no external retrieval, unratified provider activation, secret export, or held-out content access is implied.
- Outputs and outcomes: immutable `AssuranceRunManifestId` and `AssuranceRunReceiptId`, start/end event links, run class, executed scope, terminal state, finding/witness IDs, fired limits, missing work, environment/build roots, `OracleLineageId`, and explicit pass/fail/indeterminate contribution. General suite mutation/fault-seeding receipts bind each declared seed, expected detection class, observed detector/diagnostic, detection or miss, and disposition. Coverage-guided receipts additionally bind observed feedback scope, queue additions/rejections, corpus evolution, merge/minimization decisions, and a `FuzzGuidanceReceiptId`; absent/stale/incompatible guidance is indeterminate, never a green run.
- Diagnostics: baseline/target/build mismatch, stale corpus, rights/card block, unratified dependency/provider, missing start event, harness fault, cancellation, resource limit, receipt truncation, and protected-data violation.
- Evidence and provenance: receipt binds unchanged pre-run manifest, fuzz baseline, candidate/instrumented build/toolchain/dependencies, target/corpus/seed/schedule, guidance schema and before/after queue/corpus roots, merge/minimization receipts, general lineage, limits, executor, prospective start/end events, raw finding roots, and terminal observations.
- Determinism and replay: manifest identity is D0; deterministic runs state exact replay, while randomized/native-schedule runs bind seeds/schedules and support only their recorded observations.
- Falsifiers and Gauntlet: manifest created after run, candidate/instrumented build substitution, guidance schema drift, fabricated feedback, hidden queue rejection, corpus-root rewrite, general mutation/fault seed omission or post-run invention, forged detection, hidden miss, cancelled-as-pass, missing failed case, forged event or lineage link, correlated-wrapper inflation, rights leak, provider inference, stale receipt, and replay mismatch.
- Surfaces: local/continuous assurance runner, reachable-panic gate, seeded checker trials, lane aggregation, cycle seal, and evidence package.
- Dependencies and consumers: depends on FUZ.001–FUZ.010/FUZ.013/FUZ.016, IMM.009/IMM.011/IMM.014/IMM.017, FDN.016, and ratified D7/D-005 state as applicable; FUZ.011/FUZ.015, IMM.020, and IMM.019 consume receipts.
- Migration and withdrawal: target/baseline/build/toolchain/corpus/protocol change creates a new manifest; prior receipts remain scoped and cannot cover the changed run.
- No-claim boundary: a run receipt reports only declared executed scope and terminal observations; it does not infer unexecuted inputs, compare libraries, or establish universal safety.
- Rationale: a named pre-run envelope and terminal receipt make missing, cancelled, stale, and substituted assurance work mechanically visible.

#### `C1.CC.FUZ.015@1` — Assurance-lane result aggregation

- Identity, lifecycle, layer: active C1 L7 aggregation contract; it combines exact run receipts and gate outcomes by predeclared lane without converting missing work into success.
- Inputs and identity domain: FUZ.016 baseline, all expected/observed FUZ.014 manifests/receipts and `FuzzGuidanceReceiptId` records including the general suite mutation/fault-seeding run class, FUZ.011 panic-gate result, FUZ.012 unresolved witnesses/tombstones, IMM.020 seeded-checker assessment, every general `OracleLineageId`, held-out protocol status, optional predeclared recovery-calibration protocol with REC.006–REC.010 outcome links and known/independently adjudicated intent, lane policy, dispositions, and availability.
- Preconditions: baseline and candidate/instrumented build roots match every included result; expected lane/run set is closed for this aggregate; duplicate, stale, cancelled, missing, unavailable, or lineage-unknown inputs remain explicit. A recovery-calibration lane requires FUZ.013 access/seal compliance, frozen denominators/strata, and adjudicated-intent provenance; otherwise its envelope is unavailable or indeterminate.
- Card slots: `SC.C1.FUZ.ASSURANCE-LANE-AGGREGATE.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: lanes, runs, findings, witnesses, seed classes, cross-links, diagnostics, canonicalization, and aggregate bytes are bounded.
- Cancellation: interrupted aggregation yields indeterminate and cannot produce an admitted lane summary.
- Authority and secrets: aggregator is read-only and cannot waive findings, alter run receipts, expose protected witnesses, access held-out bytes, or ratify dependencies/providers.
- Outputs and outcomes: immutable `AssuranceLaneAggregateId` with per-lane expected/executed/missing/cancelled/failed/indeterminate sets, general suite mutation/fault-seed expected/detected/missed/disposed accounting, guidance-feedback and queue/corpus evolution accounting, lineage diversity/known-correlation/unknown summaries without numeric independence inflation, unresolved findings, separately retained checker-specific misses, coverage links, candidate root, and exact gate contribution. When predeclared, it also emits `RecoveryCalibrationEnvelopeId` with denominators and typed outcomes for materially wrong singular selections, correctly retained ambiguity, safe-workflow refusals, security-headline changes, search cost/frontier width, family/producer strata, uncertainty/drift, and unavailable/indeterminate observations; it emits no global recovery-confidence score.
- Diagnostics: baseline/build/instrumentation mismatch, missing/duplicate/stale guidance or run receipt, feedback/queue/corpus reconciliation failure, omitted/forged/unknown lineage, unresolved panic, omitted/forged general mutation seed, general detection miss, checker-specific miss, unavailable witness, invalid disposition, held-out/calibration protocol gap, denominator/stratum drift, and aggregation fault.
- Evidence and provenance: aggregate binds baseline, every run manifest/receipt, panic result, witness status, checker assessment, held-out status, policy, dispositions, composer, and construction receipt.
- Determinism and replay: D0 for exact baseline/results/policy; new receipt, disposition, candidate, or policy produces a new root.
- Falsifiers and Gauntlet: omit failed run or guidance receipt, count cancelled as executed-pass, stale-build inclusion, corpus-root rewrite, duplicate-run/correlated-lineage dilution, omit a general mutation/fault seed, hide or relabel its miss, conflate it with IMM.020 checker seeds, hide a checker-specific miss, omit a calibration denominator, launder scalar confidence, leak a protected witness, overstate held-out status, and cancel.
- Surfaces: product/cycle-close gates, capability-admission evidence, cycle seal, evidence package, and future assurance planning.
- Dependencies and consumers: depends on FUZ.011/FUZ.012/FUZ.014/FUZ.016, IMM.020, and FUZ.013 protocol status; IMM.019 and the product/close gates consume it.
- Migration and withdrawal: lane policy or baseline change versions the aggregate and lapses old gate contribution; prior receipts remain immutable.
- No-claim boundary: aggregation and recovery calibration report only the declared assurance envelope; they do not convert executed cases into universal correctness, absolute independence, a global recovery-confidence number, default-profile authority without its separate policy gate, or cross-library comparison.
- Rationale: an explicit aggregate prevents target declarations or isolated green receipts from standing in for the expected assurance lanes.

#### `C1.CC.FUZ.016@1` — C1 fuzz-baseline artifact

- Identity, lifecycle, layer: active C1 L7 pre-run contract; one immutable baseline names the exact C1 candidate-facing target, corpus, toolchain, run, and disposition envelope before assurance execution.
- Inputs and identity domain: candidate scope, FUZ.001–FUZ.010/FUZ.013 contract versions, target/corpus/fixture/rights manifests, required lanes/run classes including general suite mutation/fault-seeding separately from IMM.020 checker-specific trials, exact guidance instrumentation/build relation, guidance metric/schema and queue/corpus evolution/merge/minimization policy, toolchain-role decision, symbolic dependency/provider constraints, semantic/resource ceilings, witness/disposition policy, and gate mapping.
- Preconditions: D1/D2 and D7 are human-ratified; target/card/rights gaps are blocked rather than guessed; D-005/runtime/crypto-crate selections remain symbolic until their separate ratification; baseline is rooted before FUZ.014 manifests launch.
- Card slots: `SC.C1.FUZ.BASELINE.001` — `PENDING-LICENSED-SOURCE`.
- Budgets: target/lane/run declarations, corpus roots, policy links, canonicalization, diagnostics, and artifact bytes are bounded; each later run has its own resource envelope.
- Cancellation: interrupted baseline construction publishes no current baseline; prior baseline remains tied to its old candidate/scope.
- Authority and secrets: baseline can reference protected/held-out partitions by approved identity/availability only; it cannot fetch data, activate a provider, expose secrets, or launch a run.
- Outputs and outcomes: immutable `FuzzBaselineId` with exact candidate, target/lane matrix, expected run classes including general suite mutation/fault-seeding and separately retained checker-specific seeded trials, corpus/fixture roots and availability, guidance instrumentation/metric/schema, initial queue and corpus roots, evolution/merge/minimization policy, toolchain roles, symbolic provider blocks, limits, witness policy, gate links, and known gaps.
- Diagnostics: missing target/lane/card/rights, unratified hash/toolchain/provider, corpus alias, held-out access conflict, unmapped gate row, inconsistent limit, and stale candidate.
- Evidence and provenance: baseline binds ratified decisions, candidate/contract/target/corpus manifests, rights/card roots, policy authors/review, construction tool, known gaps, and pre-run timestamp in a separate envelope.
- Determinism and replay: semantic baseline is D0 under exact declarations/decisions/policy; timestamps and host observations are outside its root.
- Falsifiers and Gauntlet: baseline after run, omitted hostile surface, missing CLI target, missing or conflated general mutation/fault-seeding class, duplicated corpus partition, absent/stale guidance instrumentation, feedback schema without queue/corpus receipt, hidden provider selection, target without gate, run class without receipt schema, stale candidate, and protected identity leak.
- Surfaces: assurance preflight, run-manifest creation, reachable-panic gate, lane aggregation, cycle seal, and next-cycle baseline diff.
- Dependencies and consumers: depends on FUZ.001–FUZ.010/FUZ.013, IMM.001/IMM.009/IMM.011, FDN.016, and ratified D1/D2/D7 plus D-005 state; FUZ.011/FUZ.014/FUZ.015 and IMM.019 consume it.
- Migration and withdrawal: any candidate/target/corpus/toolchain/policy change creates a successor baseline; old run receipts remain bound to the old root.
- No-claim boundary: the baseline is an assurance commitment artifact, not evidence that any run occurred or any target passed.
- Rationale: a named pre-run root gives run receipts and close gates one exact declared assurance scope.

## 9. End-to-end R0 workflows

### 9.1 Common admission envelope

Every R0 workflow begins with the same admission sequence:

1. The caller and host check the pre-C1 reviewed-card authority snapshot and RPT.008 admission envelope for the requested build/profile using only registry metadata; the underlying RPT.006 candidate manifest and IMM.012 audit receipt remain separately identifiable.
2. The host presents an inert request and source offer containing only source class, declared availability/capability classes, ownership/lifetime proposal, and requested operation. No source byte is read, copied, spooled, promoted, hashed, or range-probed at this step.
3. FDN.007 compiles the exact versioned C1 `ProcessingProfile` into immutable open/recovery/security/limit views; FDN.004–FDN.008 then validate the offer and bind those views, limits, cancellation, least-authority capabilities, sensitivity, and disclosure policy into one admitted `WorkContext`, or return refusal before source work.
4. Only after that context exists may BYT.001–BYT.003 admit an immutable, scoped-borrowed, spooled, segmented, or partial source; every hash/read/copy/promotion/spool/range charge is made to the same context. The semantic core is synchronous; any async host path is an isolated adapter whose scoped borrows cannot escape.
5. The operation rejects any pending normative slot needed by the request. It never fills a slot from model memory, generated prose, or library behavior.
6. All lower work shares FDN.005’s non-resettable counters. Retry, recovery branches, object streams, filter stages, and checker materialization cannot create fresh allowances.
7. Semantic outputs use FDN.010’s outcome algebra. Source gaps, credentials, cards, unsupported profiles, budget exhaustion, cancellation, and publication uncertainty keep distinct statuses.
8. Diagnostics flow through FDN.009, and semantic results remain separate from host observations through RPT.004.

Admission failure is itself a structured result. The CLI returns usage status only for malformed CLI requests; a well-formed request refused because a card, capability, source range, or decision is unavailable remains a document/capability outcome with a report where defensible.

### 9.2 Strict inspection composition

Strict inspection is the composition:

```text
source snapshot
  -> checked byte ranges
  -> exact file tokens and raw COS
  -> strict terminal/xref/stream/object and source-interval facts
  -> immutable base revision graph
  -> pre-view chain/mapping basis and limited bootstrap resolution
  -> object-stream index + structural-signature/preservation overlays
  -> immutable final revision graph
  -> exact strict document view or explicit live strict alternatives
  -> structural document, page-continuity, metadata/XML, encryption, signature-range, and security-carrier inventory
  -> three separately reported validation layers
  -> strict OpenReport/ValidationReport/security report + optional replay/evidence package
```

The composition has these laws:

- SYN and REV contracts never call REC contracts.
- A strict defect remains in the report even if the caller later opens a recovery session.
- A partial source can yield exact facts for observed stable ranges, but no whole-source or all-history conclusion.
- Duplicate keys, unexplained bytes, orphan occurrences, link conflicts, encrypted-unavailable values, unsupported carriers, and diagnostic truncation stay visible.
- A credential may widen the values inspectable under the same source/view, but it does not alter the raw ciphertext or strict structural result.
- Every cache hit revalidates its proper-domain input and actual dependency/selection manifest.
- The report identifies the base and every finalized revision graph; it cannot silently present the newest discovery as timeless source state.
- Metadata reconciliation preserves revision-scoped Info/XMP conflicts and hostile XML limits; it never resolves external resources or upgrades structural evidence into metadata safety/conformance.
- Each validation layer reports its own rule algebra, coverage, severity, and locations; a pass in one layer cannot imply another.

Strict inspection unblocks revision/object queries, evidence packaging, and an explicit recovery request. It does not unblock repair, render, write, or a security-absence headline.

### 9.3 Revision autopsy composition

Revision autopsy starts from the strict source/graph artifacts and emphasizes physical history:

- `mb revisions` exposes terminal candidates, xref sections/streams, hybrid links, graph forks/cycles, chain alternatives, revision nodes, object occurrences, unexplained ranges, and structural signature ranges.
- `mb objects` can show all physical occurrences of an indirect key separately from the effective resolved value in one exact view.
- The preservation interval ledger retains simultaneous facts such as parsed, superseded, signature-covered, unexplained, sensitive, and raw-preservation-required.
- Object-stream members are reported through virtual spans and their container/filter/security derivation, never invented source offsets.
- Page-tree continuity evidence across revisions records alternatives and typed provenance; object-number or source-ID equality alone never proves page identity.
- Linearization is inspected as declared structure. Hints cannot authorize unsafe reads or imply future writer support.
- Every history summary states source range coverage and graph protocol. An unavailable tail or superseding graph is not hidden.

The R0 value is forensic visibility under declared limits, not a promise that malformed history has one answer.

### 9.4 Credentialed inspection composition

Credentialed inspection is strict or recovered inspection plus a narrow secret capability:

1. CLI.005 or a Rust host supplies an explicit byte/text credential form to SEC.002. Ordinary argv, environment, report, and log channels are excluded.
2. SEC.003 selects later card-reviewed password preparation/validation for the exact handler revision.
3. SEC.004 binds the exact encryption dictionary, source/view/revision, trailer facts where applicable, object/version, crypt-filter, and opaque key context.
4. SEC.008 determines string/stream/metadata/embedded-file/Identity scope, preserves raw duplicate `/EncryptMetadata` occurrences, and enforces the object-stream one-time container rule.
5. Exactly one of SEC.005, SEC.006, or SEC.007 handles the admitted RC4, AESV2, or AESV3 read profile. Raw public-key recipient/crypt-filter/declared-algorithm carriers and unverified/pending technical-specification profile identifiers are inventoried only; public-key decryption and unsupported matrix rows refuse.
6. FLT.009 injects the selected Crypt/Identity context into the chain without letting filter code discover credentials.
7. SEC.009 preserves ciphertext lineage, plaintext sensitivity, tenant/credential/revision cache partition, and cleanup uncertainty.
8. Open/security reports record only non-secret capability/profile/status evidence, name owner/user input roles without supplying their semantics from memory, and keep cryptographic access, declared permissions, host policy, and actual executed-scope recoverability as four separate fields.

Wrong credentials, unsupported profiles, missing cards, denied disclosure, and resource exhaustion have different machine outcomes. Externally visible credential failures avoid needless detail, while protected diagnostics may retain the exact internal cause under explicit policy.

Credentialed inspection does not enforce PDF permission bits as hostile-file authorization or cooperative application policy. It reports declared permissions separately from cryptographic access, host policy, and actual executed-scope recoverability; cooperative enforcement remains deferred.

### 9.5 Recovery composition

Recovery begins only after DOC.009’s strict report is immutable:

```text
strict defect set
  -> explicit recovery profile and search budget
  -> registered source-bounded hypothesis bases without candidate views
  -> per-basis pre-view mapping and candidate DocumentViewId
  -> candidate-view consequence receipt and finalized hypothesis
  -> hard admissibility gates
  -> named partial-order dimensions
  -> nondominated frontier retaining materially distinct and equivalence-unresolved alternatives
  -> optional task-local selection
  -> RecoveryReport + recovery/security enrichment; source and strict reports remain unchanged
```

The initial family surface is exactly the C1 set from Rev 7 §14.5: common header/EOF-placement deviations; terminal/xref/revision defects; wrong stream lengths and missing boundaries; duplicate/scan-discovered objects; orphaned trailers; missing catalog/page links; malformed object-stream headers; and truncated final revisions. Header-placement recovery consumes SYN.002's exact candidate offset and leading-byte evidence behind REC.001/REC.002 strict-first admission; it never changes the source identity, strict graph/report, or bytes. A new heuristic is not admitted merely because it helps one sample. It needs a registered contract, card coverage, bound, falsifier, materiality projection, and kill criterion.

Safety and exact contradictory source evidence are hard gates. Surviving candidates are ordered by source support, constraint satisfaction, assumption inclusion/locality, structural/history consistency, signature preservation, and only later any lawfully admitted observation. No scalar rank replaces this record.

Materiality uses the closed Rev 7 §14.7 axes: effective objects, page order, visible appearance, extracted text, attachment inventory, signature interpretation, and security conclusions. REC.010 records a typed value/evidence or explicit unavailable/indeterminate state for every axis. Because C1 has neither page-program execution nor text extraction, different candidate views cannot be coalesced merely because the five structural axes agree: an unavailable appearance/text axis keeps the pair equivalence-unresolved unless an admitted exact identity proof already establishes equality for that axis. Every such alternative remains live for later C2/C3 assessment, and no whole-document security/absence conclusion may exclude it.

A task-local selection may enable object inspection. It cannot erase alternatives, widen security claims, or authorize writeback. RPT.003 remains the immutable strict security inventory. If a live recovery alternative changes an attachment, action, hidden revision, signature range, or other security conclusion, RPT.007 records ambiguity/partiality across the live alternatives.

### 9.6 Obscure self-contained slice: encrypted object stream under ambiguous revision history

This slice is deliberately specified so it can be implemented without reading another section of this plan.

Scenario: one immutable source contains conflicting xref evidence. Two admissible revision chains point to different occurrences of an encrypted object stream. The caller supplies a password credential. At least one object-stream header or boundary is malformed.

Required behavior:

1. Bind the immutable bytes to one `SourceRootId`; do not include parser or credential facts in that ID.
2. Parse strict xref/table/stream declarations separately. Preserve disagreement and every exact occurrence/span.
3. Create one immutable `BaseRevisionGraphId` from strict source facts for the exact discovery protocol, source coverage, cards, assumptions, and semantic limits. Do not choose a chain inside the graph identity.
4. Record the strict defect before creating any recovery hypothesis.
5. Generate only registered, bounded `RecoveryHypothesisBasisId` records for the broken link/boundary/header. Each basis binds the final strict parent graph, raw evidence, and exact assumptions but contains no candidate view.
6. For every admitted basis, create a `DocumentViewBasisId`, perform only the limited bootstrap resolution, and index each admitted object-stream container. Present the complete declared basis/security-context frontier manifest to REV.008; it validates and mints one canonical `GraphOverlayFrontierId` for the exact discovery/recovery protocol while running card-gated post-member structural-signature coverage. Then derive the graph-neutral `GraphHistoryOverlayId` and finalize one immutable `RevisionGraphId` containing all frontier alternatives without mutating the base graph, importing carry/drop intent, or filtering by caller/task selection.
7. For each basis, bind that basis, the same finalized graph, dialect/security policy, outcome-sensitive limits, coverage, capability identities, and scoped semantic state into its own candidate `DocumentViewId`.
8. Run REC.010 consequence checks and only then mint the finalized `RecoveryHypothesisId`; an incomplete receipt cannot enter ordering.
9. Apply hard safety/source gates, then compute the nondominated frontier. Enumeration or thread order cannot change basis, view, receipt, or hypothesis identities.
10. Inventory the encryption dictionary and exact crypt-filter context for each view. A credential lease is source/view/security-context scoped and non-exporting.
11. Prepare/validate the password using the later reviewed handler-revision card. Derive only an opaque read-key capability under the exact revision/object context.
12. Before decoding, mint the metadata-cost recipe identity `DecodedContainerId` only under ratified D3. It is the sole decoded identity class. `DecodedStreamId` is mentioned only as D-004's higher-layer alias drift and must not appear as a second type.
13. Decrypt the containing object stream exactly once. Members are never decrypted independently.
14. Execute the declared filter chain transactionally while computing `DecodedArtifactDigest` incrementally. A downstream decoder error or policy refusal records its exact error or value-less `Refused` branch and aborts only while output is private and provably abortable. An observed cancellation returns `Cancelled` after reconciliation. If visibility or commit state cannot be proved, return `Indeterminate`; neither cancellation nor commit uncertainty is relabeled `Refused`, and no branch can publish a half-decoded cache entry as an ordinary artifact.
15. On successful commit, publish the materialized state and content digest together. A deliberately transient no-digest state stays operation-local and cannot support byte-exact evidence, retention, or durable cache reuse.
16. Treat a recipe-key cache hit as a candidate only. Validate the dependency/selection manifest and verify `DecodedArtifactDigest` before reuse.
17. Index the decoded object-stream header with checked count/offset arithmetic. Give members `VirtualSpanId`s linked through the container to the encrypted source occurrence.
18. Partition any plaintext/container/member cache by tenant, non-secret credential/security context, revision/view, sensitivity, and disclosure domain.
19. If the two live views produce different effective objects or security conclusions, retain both. A caller may select one for a named read task, but the report remains ambiguous at source scope.
20. Emit the unchanged strict OpenReport/security report plus separately rooted RecoveryReport and RPT.007 enrichment containing source, graph, every basis/view/receipt/hypothesis chain, container/virtual provenance, credentials-used status without secret material, limits, diagnostics, and no-claims.

Required typed non-success branches include contract-specific `Refused` or exact-scope `Partial` outcomes for a missing card, unsupported handler row, public-key decryption handler, wrong/denied credential, unavailable range, exhausted decode/search/canonicalization budget, unresolved identity-sensitive symmetry, or unsafe plaintext disclosure; `Cancelled` for observed cancellation after reconciliation; and `Indeterminate` when transaction visibility or commit state cannot be proved.

Explicit no-claims: no direct file span for decoded members; no double decryption; no singular malformed-file truth when alternatives survive; no signature trust; no permission authorization; no plaintext public availability; no writer or repaired output.

### 9.7 Report/package/checker loop

Before candidate work, IMM.018 opens the prospective ledger under ratified D1/D2/D6 and IMM.017 appends each attempt/failure/intervention event without waiting for final artifacts. RPT.001/RPT.003/RPT.010 produce immutable strict and validation semantics; RPT.002/RPT.007 add separately rooted recovery semantics; RPT.004 keeps host observations separate; RPT.009 packages only the exact replay relation supported by its capture/determinism class and never uses ambient networking. RPT.006 is an unaudited candidate manifest, IMM.012 emits the later audit receipt, and RPT.008 binds that manifest to the independently produced IMM.012, FUZ.011, FUZ.015, and IMM.020 roots without rewriting any input.

IMM.014 admits the pre-run checker-isolation plan. IMM.013 parses raw hostile package bytes independently and emits ordinary or seeded trial reports without trusting producer objects or treating a digest as artifact availability. IMM.020 compares the pre-run plan with actual lineage and seeded outcomes. IMM.016 then assembles a private unsigned evidence package only after D1/D2/D4 are ratified. Every artifact has `Embedded`, `ExternallyRetrievable`, `Recomputable`, `IdentityOnly`, or `Unavailable` availability. `mb package check` returns the exact checked claim/coverage set and refuses or narrows unavailable decision-critical material.

At close, IMM.019 seals the prospective IMM.017 interval with final audit, report, checker, FUZ.015 aggregate, and FUZ.016 baseline roots. The seal does not backfill or rewrite earlier events.

The loop can establish structural consistency and declared checker relations. It cannot create external commitment, signature, publication, independent adjudication, or truth for an unchecked underlying PDF observation.

### 9.8 Workflow dependency matrix

| Workflow | Required contract families | Primary artifact | Blocks or unblocks |
|---|---|---|---|
| Strict hostile inspection | FDN, BYT, SYN, REV, DOC, RPT, CLI | `OpenReport` plus `ValidationReport` and structural security/metadata components | Unblocks raw R0 use and explicit recovery; blocks on required pending cards. |
| Revision autopsy | strict inspection + BYT.005/BYT.006, REV.004–REV.009, CLI.002/CLI.003 | graph/history projection | Unblocks physical-history queries; never unblocks writeback. |
| Credentialed inspection | strict/recovery + FLT + SEC + CLI.005 | Open/security report with protected derivations | Unblocks values authorized by exact credential context; not public-key profiles. |
| Bounded recovery | immutable strict reports + REC bases/consequences + DOC view identities + RPT.007 | `RecoveryReport`, enrichment, and candidate views | Unblocks task-local read selection; blocks singular source/security claim if alternatives differ. |
| Evidence check | RPT.001–RPT.010 + IMM.013/IMM.014/IMM.016/IMM.020 + CLI.009/CLI.010 | replay/validation/checker records and final lineage assessment | Unblocks scoped package consistency, C1 layers 1–3 validation, and exact replay-relation evidence; does not self-award release/campaign claims. |

## 10. Fuzzing, falsifiers, and the reachable-panic gate

### 10.1 Target-to-surface inventory

| Target family | Primary surfaces | Required invariant classes |
|---|---|---|
| FUZ.002 | source snapshots, ranges, spools, promotion, preservation ledger | checked arithmetic, immutable identity, source-change revocation, bounded I/O, cache invalidation, cancellation. |
| FUZ.003 | lexer, raw COS, scalars, duplicates, stream boundaries | no reachable panic, exact spans/raw round trips, bounded nesting/allocation, no recovery leakage, transactional privacy. |
| FUZ.004 | terminal/xref/hybrid/revision/occurrence/signature-range and raw signature family/seed/lock carriers | graph/source separation, checked offsets, structural-only carrier inventory, coverage honesty, order-independent identity, bounded search. |
| FUZ.005 | object streams and virtual provenance | one-time decryption, bounded indexing, virtual spans, context isolation, no partial cache publication. |
| FUZ.006 | ASCIIHex, ASCII85, RunLength, Flate, predictors, LZW, internal/external chain planner, `/DL` hint handling, cursors, drop, and sink durability | declared order and shape alignment, advisory-only hint, deterministic bytes, checked monotone progress, scoped borrows, exact virtual failure offset, expansion/byte limits, poisoned unterminated drop, sink terminal/visibility/durability state. |
| FUZ.007 | encryption inventory, credentials, preparation, matrix, `/P`/`/Perms`/`/EncryptMetadata`, raw public-key/technical-specification carriers, owner/user roles, RC4/AESV2/AESV3, Crypt routing | exact context, separate access/permission/host-policy/recoverability outcomes, secret non-export, wrong-credential behavior, plaintext partition, raw-only public-key inventory, no writer/enforcement widening. |
| FUZ.008 | resolver, document/page structure/geometry/continuity, occurrence visibility, views, DOC.012–DOC.015 inventories including hostile XML, every recovery family including header/EOF placement, order/selection | cycles/limits, bounded inventory coverage, alternatives retained, strict-first, exact header evidence, page-continuity non-identity, metadata conflict preservation, XML external-resource refusal, raw/effective geometry, partial-order validity, security non-laundering. |
| FUZ.009 | RPT.001–RPT.010 reports, schemas, packages, checker | mandatory identities, validation-layer non-transitivity, replay-relation/capture honesty, canonical ambiguity refusal, availability/coverage honesty, producer/checker disagreement. |
| FUZ.010 | every checkpoint, resource lease, transaction, cache, shared diagnostic collector, and CLI.001–CLI.010 request/parser/saved-artifact/projection/framing/sink/interrupt boundary | conservation, checked package and exact-view validation admission, bounded observation, redaction, broken-pipe/cancellation terminal state, race/isolation safety, stable diagnostics. |

Every atomic contract also names its local falsifiers. The inventory above is the cross-contract orchestration view. IMM.009 must prove bidirectional links: every hostile-input contract has a target, and every target supports at least one active contract/gate.

### 10.2 Fuzz baseline artifact

FUZ.016 is the named, versioned pre-run C1 fuzz baseline. It is a scope commitment, not a run result, performance artifact, or competitor comparison. Before any FUZ.014 launch it records:

- exact candidate build, toolchain, feature/profile, and dependency identities;
- active target/harness versions and expected lane/run classes, including general suite mutation/fault-seeding separately from checker-specific seeded trials;
- seed/corpus/generator/mutator manifest roots and rights/partition state;
- exact guidance-instrumented build relation, guidance metric/schema, initial queue/corpus roots, and queue evolution/merge/minimization policy;
- semantic resource limits and host isolation;
- target/contract/card/claim/gate linkage;
- protected corpus/fixture availability and no-claim boundaries; and
- symbolic runtime/crypto-provider blocks until human ratification.

Each FUZ.014 pre-run manifest binds that baseline and each terminal receipt records executed scope, failed/interrupted work, crashes, panics, hangs, fired resource limits, harness failures, witness roots, exact guidance feedback, queue/corpus evolution, and any predeclared general mutation/fault seeds with detection or miss. FUZ.011 evaluates reachable panics from the exact receipts. FUZ.012 retains minimized witnesses, sibling-site searches, fixes, regression properties, tombstones, and disclosure-classified compute/human-attention consumption. FUZ.015 then aggregates the expected lanes, missing/cancelled/failed/indeterminate runs, general seed detections/misses, guidance receipts, general oracle lineage, panic result, separately retained checker assessment, and any predeclared recovery-calibration envelope. No run or aggregate in this authoring artifact has executed or measured anything.

No artifact hides discarded runs or promotes target survival into a universal guarantee. A new build, semantic contract, parser/decoder/security dependency, target, corpus, or affected card invalidates the relevant baseline and every dependent run/gate/aggregate root until replaced.

### 10.3 Reachable-panic rule

Malformed or hostile PDF/package input, caller credentials, limit profiles, cancellation, sink faults, and admitted host responses must not reach a panic through public boundaries. An internal panic is acceptable only when a programmer invariant is proven unreachable from all admitted inputs; a comment is not that proof.

FUZ.011 passes only for the exact declared build/target/corpus/run envelope with zero unresolved reachable panics. Missing/cancelled runs, stale builds, non-replaying crashes, or uncovered public surfaces yield fail/indeterminate. Production abort mode, dependency panic behavior, and C ABI/WASM containment are separate later surface decisions; C1 cannot hide a reachable parser panic behind process abort.

### 10.4 Bug closure

A finding closes only when the record contains:

1. original and minimized witness, or a documented minimization limit;
2. violated assumption and affected contract/card/gate;
3. regression property or atomic fixture;
4. sibling-site search across the same invariant;
5. fix evidence on the exact candidate build;
6. corpus/provenance/rights/partition update;
7. tombstone if the bad heuristic or model could recur, including disclosure-classified compute and human-attention consumption without turning it into a work ledger; and
8. drift-audit confirmation that schemas, claims, docs, surfaces, and manifests agree.

Changing a golden, suppressing a panic, or making one witness stop failing is insufficient by itself.

### 10.5 Independent falsifiers without premature comparison

C1 may use project-authored properties, rights-admitted atomic fixtures, generic algorithm/cryptographic vectors, independently authored internal reference logic, and the separately implemented package checker. No prohibited processor source/documentation may be contacted.

Black-box processor evidence belongs only to a protocol/right/custody path committed before execution. Until the day-zero discovery/evaluation commitments and rights classifications exist, no C1 agent downloads, runs, measures, or compares any processor artifact. If a Charter G3-subset lane requires such evidence and the commitment is absent, that lane remains unavailable; the ordinary product wedge does not pretend otherwise.

## 11. C1 close gate

### 11.1 Gate architecture: product value versus campaign closure

The graceful-degradation law creates two linked but non-conflated results:

- The R0 product gate decides whether the inspection wedge may be made available under its exact self-attested capability/no-claim envelope. It depends on zero steward, challenge window, baseline, or external adjudicator.
- The C1 campaign close gate decides whether Cycle 1 contributes a sealed foundry trial and whether a later delta plan may be authored. It adds the independently sealed probe, commitment substrate, and trial-record obligations.

Failure of campaign independence does not strand the wedge. It does block campaign closure, later-cycle progression under §34.9, and any claim that depends on the missing evidence. A report must not say “C1 closed” merely because the product gate passed.

### 11.2 Pre-implementation admission gate

C1 source bootstrap and later candidate admission are separate gates. Before the human-authorized plan-to-execution conversion creates any source tree, manifest, or lockfile, every applicable pre-source prerequisite below must be evidenced. A row that requires source/build artifacts is a post-bootstrap candidate gate: it must pass before the affected implementation is admitted to product or campaign evidence, not before the first legal source artifacts can be created. No bootstrap pass self-admits a candidate.

| Gate item | Passing evidence | Failure behavior |
|---|---|---|
| Hash/digest | Human-ratified D1/D2 package, with the proposed SHA-256/full-256-bit default still labeled as a proposal until that act; protocol fixed before the first external commitment | Identities remain symbolic; no implementation identity or external commitment. |
| Canonical encoding | Human-ratified D1/D2 package and separate producer/checker encoder plan; the proposed deterministic-CBOR profile remains only a proposal until ratified | Identity/package/report-root/ledger-chain paths unavailable. |
| Decoded identity | Human-ratified D3 hybrid cost/availability model; sole `DecodedContainerId`, post-commit `DecodedArtifactDigest`, and separately human-ratified D-004 name-drift disposition | Decoded container identity/caching unavailable; `DecodedStreamId` remains only a proposed higher-layer drift label and no second identity class is created. |
| Checker isolation | Human-ratified D4 sharing/authorship/specification boundary and seeded-defect protocol plus pre-run IMM.014 `CheckerIsolationPlanId`/`PreRunOracleLineageId` | Standalone-check/independence row unavailable; no post-run result is invented. |
| Project license | Human/counsel-ratified D5 project license and contribution instrument; proposed dual-license default remains unadopted until then | Distribution and outside-contribution posture unavailable. |
| Production ledger | Human-ratified D6 backend/schema plus D1/D2 and a verified IMM.018 `ProductionLedgerBootstrapId` that predates candidate work; proposed per-writer hash-chained JSONL remains unadopted until ratified | Durable prospective event append unavailable; local notes or a late bootstrap cannot be upgraded. |
| Rust source bootstrap — pre-source | Explicit human conversion authorization; human-ratified D7 role split with exact stable and exact dated-nightly identities; Rust 2024 edition; deny-unsafe-by-default policy; dependency/feature/target and capsule-admission rules; zero assumed capsules | No source tree, manifest, lockfile, build, or implementation work may begin. |
| Safe-source and unsafe-capsule verification — post-bootstrap candidate | Exact committed lockfile, source/build/toolchain roots, full feature/target/dependency graph, unsafe-site inventory, registered capsule records, public façades, and build-scoped FDN.016 plus executed assurance evidence | Bootstrap artifacts remain historical but the candidate, reproducible-build row, unsafe admission, product gate, and affected assurance lanes remain unavailable. |
| Runtime dependencies/crypto providers | D-005 routing and human ratification of exact symbolic providers/versions/provenance, including sync-core/isolated-async-adapter placement | Dependent Flate/password/RC4/AES contracts and any async adapter remain unavailable; no provider or runtime is inferred. |
| SpecCards | A pre-C1 immutable `ReviewedCardAuthoritySnapshotId`/`CardAuthoritySnapshotId` proves every applicable `MB-SC-R0-*` rights record, project-authored body, and two-person meaning review; a pre-C1 immutable `CardLinkResolutionManifestId` maps every `SC.C1.*` ID through exactly one record to one or more applicable reviewed `MB-SC-R0-*` entries or an explicit human-reviewed project-law disposition; IMM.001 only projects those artifacts and IMM.009 proves bidirectional zero-orphan linkage. Every slot in this plan retains the exact `PENDING-LICENSED-SOURCE` marker and no linkage record activates it | A required actual card still pending, a missing/default/ambiguous link, an unauthorized project-law disposition, or an applicable-card reverse orphan leaves the affected capability absent/refused; no runtime self-authorization or memory-derived fill. |
| Held-out seal | Exact steward/protocol commitment if campaign probe is to run | Product work may proceed; campaign close cannot pass. |

### 11.3 R0 product gate

The wedge passes its product gate only when all rows below bind the same candidate build, immutable RPT.006 candidate-manifest root, IMM.012 audit receipt, and RPT.008 capability-admission envelope:

1. Strict hostile inspection produces immutable RPT.001/RPT.003/RPT.010 reports with every source/base-and-final-graph/strict-view identity, exact observation coverage, raw/history/object inventory including visible/shadowed/unreachable/unknown occurrence classifications, page attribute/geometry/request and cross-revision continuity evidence, metadata Info/XMP reconciliation and bounded hostile-XML handling, three separately reported validation layers, structural signatures, encryption/security inventory, resource accounting, diagnostics, and no-claims; none of these strict roots has a recovery dependency.
2. Bounded recovery exercises every initial C1 family, explicitly including common header/EOF-placement deviations, through basis → candidate view → REC.010 consequence finalization; preserves SYN.002 offsets/leading bytes and strict truth; records all seven materiality axes with visible-appearance/extracted-text unavailability explicit; retains materially distinct and equivalence-unresolved alternatives; carries evidence, per-hypothesis cost vectors with reconciled shared/unavailable attribution, and affected objects/pages; and emits RPT.002/RPT.007 without modifying strict reports, graphs, source identity, or source bytes.
3. DOC.012, DOC.013, and DOC.014 each link directly to active two-person-reviewed `MB-SC-R0-038`, `MB-SC-R0-039`, and `MB-SC-R0-040` authority respectively; DOC.015's metadata-reconciliation and XML-safety links likewise require active pre-C1 reviewed-card or human-reviewed project-law dispositions. All four emit bounded report/diagnostic/coverage evidence and pass IMM.009/FUZ.008 checks. A pending slot blocks its inventory, and no row may substitute generic `DOC.008` opacity, decoded-text meaning, rendering, execution, reachability, sanitization, XML safety/conformance, or another safety verdict.
4. Credentialed inspection covers the admitted standard-handler matrix including RC4, AESV2, AESV3, version-specific password preparation, duplicate-preserved raw `/EncryptMetadata`, owner/user role names, and a typed `/Perms` validation outcome kept separate from `/P`, with caller-supplied credentials and secret/cache isolation. It inventories raw public-key and technical-specification carriers without decryption and reports cryptographic access, declared permissions, host policy, and actual executed-scope recoverability separately; the technical-specification inventory remains unavailable while `MB-SC-R0-043` is pending, and cooperative permission enforcement remains absent.
5. Every named lossless filter and predictor contract is active for its card-reviewed profile; internal `/Filter`/`/DecodeParms` and external `/FFilter`/`/FDecodeParms` shapes, advisory-only `/DL`, independent cursor laws, chain order, parameters, transactional publication/drop state, sink visibility/durability class, limits, and exact virtual failure provenance pass local falsifiers.
6. Structural signature/`ByteRange` plus raw and, only when reviewed cards admit applicability, virtual-member signature family/seed/lock carrier discovery is present and explicitly stops before digest, CMS, cryptographic/trust, or transform-impact validation. Pending, unsupported, unavailable, or incomplete object-stream member coverage is reported exactly and blocks any all-occurrence signature conclusion.
7. `mb inspect`, `mb revisions`, `mb objects`, `mb validate` for C1 layers 1–3, recovery alternatives, capability/schema discovery, secure credential input, output projection, and stable exit mapping agree with their contracts; package-backed revision/object queries require an exact IMM.013 `CheckedPackageHandleId`, while direct-source and saved-report paths remain available under their own checks. `mb validate` preserves every pending/unsupported/unavailable/not-evaluated rule and does not expose standardized-profile validation.
8. FUZ.016 names the pre-run target/corpus/lane and coverage-guidance envelope, including CLI hostile surfaces and the general suite mutation/fault-seeding class; every expected run has a matching FUZ.014 run/guidance/detection receipt as applicable; FUZ.011 reports zero unresolved reachable panics for that exact envelope; missing/cancelled/stale/instrumentation-mismatched work or an undisposed general seed miss is failing or indeterminate.
9. IMM.006–IMM.012 pass for the candidate: API and per-concrete-crate `CONTRACT.md` existence/coherence, prerequisite-DAG and guarded-state-transition-graph agreement, runtime dependency/layer agreement, exact candidate/build/lockfile/feature/target-bound `DependencyHygieneResultId` with a provenance-recorded date-pinned local advisory snapshot and every duplicate-version disposition, claim linkage, coverage, generated drift including any rights-admitted Arlington echo/source vintage, clean-room scan, and aggregate drift audit with zero unresolved Grade-A findings. Missing, stale, unavailable, failed, or indeterminate dependency-hygiene evidence blocks affected customer-facing admission.
10. RPT.006 reports only candidate rows and every decision/card/provider block; RPT.008 alone reports admission by binding that unchanged manifest to the later IMM.012, FUZ.011, FUZ.015, and IMM.020 roots. A missing, cancelled, failed, stale, or indeterminate required root cannot pass.
11. FDN.016 and its IMM/FUZ consumers establish the exact safe-source/unsafe-capsule status for the candidate; no unregistered reachable unsafe site or stale capsule evidence remains.
12. IMM.020 records actual checker lineage and every seeded detection/miss/indeterminate outcome against the earlier IMM.014 plan; under the proposed D4 profile, any miss is unresolved Grade A and blocks the stronger checker row.
13. FUZ.015 accounts for every expected assurance lane, general mutation/fault seed and detection/miss/disposition, guidance receipt, queue/corpus transition, and general `OracleLineageId`, while retaining IMM.020 checker-specific seeds/misses separately; it does not count missing, cancelled, stale, failed, indeterminate, or undisposed-miss work as a passing contribution. A lineage-unknown observation remains explicit scoped uncertainty and cannot count as independent/diverse or strengthen a claim. Its typed `RecoveryCalibrationEnvelopeId`, when predeclared and available, reports the Rev 7 §14.10.1 outcomes, denominators, uncertainty, drift, search cost/frontier width, and family/producer strata; unavailable calibration cannot support a calibrated/default-profile claim and never yields a global recovery-confidence score.
14. The product report states that no rendering, fonts, text extraction, semantic destination resolution, writer, public-key decryption handler, signature trust, active execution, reachability verdict, sanitization, repair writeback, or external adjudication is present.
15. Customer availability is blocked until the human-owned `VulnerabilityResponsePolicyStatusId` records an adopted draft covering intake channel, triage, embargo, advisory format, and claim-withdrawal linkage. A missing/unadopted status does not erase internal product evidence or campaign records, but the wedge is not offered to customers; this plan drafts no policy body and takes no external action.

The formal Workflow B gate in C1 is the R0 projection of the long-term Document Autopsy workflow: hostile-source open, revision/object history, recovery alternatives, encryption/signature/security inventory, structured evidence, and explicit unsupported later-layer findings. It does not pretend that C1 supplies the later rendering/text/action-semantic branches of the long-term workflow.

### 11.4 Gauntlet gate

The C1 gate requires these assurance lanes:

- G0: local laws for checked ranges/arithmetic, resource conservation, outcome non-laundering, identity domain separation, duplicate preservation, transaction state, canonical schemas, and cache isolation.
- G1: atomic positive/negative fixtures linked to reviewed cards for every admitted syntax, xref, filter, security, document, and recovery rule.
- G2: rights-admitted analytic/generic vectors and independently implemented internal oracles that do not merely call the target path.
- G3-subset: only lawfully committed, rights-cleared black-box structural evidence under the predeclared protocol. If unavailable, the campaign lane stays unavailable; it does not block the ordinary R0 product gate.
- G4: C1-local metamorphic properties for chunk boundaries, order/permutation invariance, parse/encode round trips where the contract already supplies both directions, and independently defined relation checks; no third-party processor comparison enters this lane.
- G5/G6 subset: hostile fuzz/bomb/malformed storms plus cancellation, concurrency, determinism, cache/tenant, replay, privacy, Miri/sanitizer evidence where applicable, unsafe-capsule falsifiers, candidate-bound offline dependency advisory/license/provenance/duplicate-version audits, and a general suite mutation/fault-seeding lane retained separately from IMM.020 checker-specific seeded trials.

Agreement is not normative proof. Every corroborating observation carries the general `OracleLineageId`; shared or unknown lineage is disclosed, and a correlated wrapper does not count as another independent falsifier. IMM.014/IMM.020 remain the richer checker-specific specialization rather than a second general lineage schema.

### 11.5 Campaign close additions

After the product gate, campaign closure additionally requires:

1. one probe selected from the independently stewarded pre-implementation sealed pool;
2. the frozen probe protocol, access/submission budget, exact candidate artifact, results whether favorable or unfavorable, and post-reveal partition transition;
3. a cycle-close drift audit over the exact probed candidate with zero unresolved Grade-A findings;
4. required card coverage with no required slot pending/blocked for the declared C1 envelope;
5. an IMM.018 bootstrap predating candidate work and verified IMM.017 prospective event interval containing attempts, failures, retries, and interventions;
6. FUZ.016 baseline, all FUZ.014 receipts, FUZ.011 panic result, FUZ.015 aggregate, and IMM.020 checker-lineage assessment bound to the exact candidate;
7. an IMM.019 sealed `CycleTrialRecordId` over those prospective events and final roots under ratified D1/D2/D6; and
8. commitment of that sealed record through the human-established substrate, not a bare git timestamp, only after hash/canonicalization ratification.

The sealed record includes exact model/harness/build/toolchain/dependency identities where available; task/attempt boundaries; every prospective attempt, failure, retry, discarded candidate, and selection decision; compute/cost and human intervention/time where available; protocol-scoped median and `best_outcomes` fields required by Work Order §3; drift, fuzz baseline/run/aggregate, probe, card, gate, checker, and D4 seeded-defect detection/miss roots; artifact availability; missing telemetry; retrospective gaps; and no-claim/downgrade state. **PROPOSED default — awaiting ratification (D6):** events enter append-only per-writer JSONL shards and IMM.019 seals them with only a derived regenerable index; the local chain is not the independent commitment substrate. `best_outcomes` is a formal distribution field, not supremacy language and never permits hiding other attempts.

If the commitment substrate is unavailable, the record stays `provisional-pending-substrate`. It may support local operations, but it contributes no prospective sealed-cycle evidence.

### 11.6 Gate failure and downgrade law

| Failure | Product consequence | Campaign consequence |
|---|---|---|
| Required card/provider/decision missing | Affected capability absent/refused; product gate may pass only if the declared R0 envelope is narrowed consistently by higher authority | C1 Charter envelope does not close until resolved or formally amended. |
| Reachable panic or transaction leak | Affected surface withheld; gate fails | Trial records failure; no closure. |
| Unresolved Grade-A drift/clean-room finding | Candidate withheld/quarantined | No closure; incident/finding retained. |
| Credentialed matrix gap | Encrypted slice advertises exact gap; required Charter gate fails | No closure unless higher authority changes envelope. |
| Steward/seal/probe unavailable | Ordinary wedge may still be released under self-attested product evidence after its product gate | No sealed C1 trial; no later delta plan under §34.9. |
| Checker isolation unavailable | Package/checker surface narrowed or withheld | No independent-check support; campaign claim tier degrades. |
| External G3-subset unavailable | No change to ordinary product behavior | Lane marked unavailable; no fabricated comparison evidence. |

## 12. Exclusions and handoff

### 12.1 Explicit exclusions by later owner cycle

| Excluded from C1 | Earliest Charter owner cycle | C1 handling |
|---|---|---|
| Content-stream/page-program execution, graphics state, paths, rasterization, baseline images, transparency | C2 | Preserve/inventory raw streams and references; no execution or visual claim. |
| Fonts, CMaps, glyph execution, Unicode/text extraction, ICC/color pipeline | C3 | Preserve/inventory raw carriers; no glyph, text, color, or meaning claim. |
| Compatibility/emulation recovery profiles, including `CommonViewerCompatibility` and named processor-emulation behavior | C3 | C1 compiles only `StrictOnly`, `ConservativeRepair`, and `ForensicPreserveAll`; no observation, compatibility, or emulation profile is available. |
| Writer, deterministic serialization output, incremental edits, signature-impact classification, WASM, release packaging | C4 | Source remains immutable; structural signature ranges only; no writer API. |
| Active progressive-fetch orchestrator or hint-authorized scheduling | C4 | BYT.003 retains inert planning metadata and explicit gaps only; no hint table authorizes a read. |
| Public-key decryption; named DSS/VRI and other LTV validation-data structure/linkage interpretation; cryptographic signature/trust/profile validation; transforms, redaction, sanitization, secure output, agent surface, C ABI preview | C5 | C1 preserves raw objects and generic unknown/opaque security carriers through DOC.001/DOC.008 but invents no DSS/VRI/LTV classification. C5 must surface admitted validation-data presence/linkage before any stronger certificate, revocation, path, trust, or LTV conclusion; no transform/security-output claim exists in C1. |
| Cooperative application enforcement of declared permission bits | C5 | C1 reports cryptographic access, declarations, host policy, and actual recoverability separately; it supplies no enforcement behavior. |
| Dedicated typed explanation graph and `mb explain` query surface | C5 | C1 object provenance, resolution paths/cycles, exact/virtual/enclosing spans, and visible/shadowed/unreachable/unknown occurrence state remain queryable through RPT.001 and the existing `mb inspect`/`mb revisions`/`mb objects` projections. C1 adds no dedicated explanation API, pixel/glyph/text/signature-impact/transform/divergence explanation, or unique inverse attribution; FDN.011's enclosing-span no-causality boundary remains controlling. |
| `/Prop_Build` named domain row | C5 boundary review, then C6 if the licensed card classifies it as profile-only | Preserve the exact name as an unresolved registry gap at `PENDING-LICENSED-SOURCE`; the human SpecCard pipeline assigns the semantic owner, and C1 invents no interpretation or behavior. |
| Rare codecs, advanced color/transparency, profiles, forms/appearance generation, authoring/layout, performance hardening, coverage scorer | C6 | Capability manifest marks absent; no speculative implementation detail. |
| Public `mb corpus` operator CLI | C6 | C1 corpus contracts remain steward/tool-only; held-out bytes, summaries, embeddings, caches, dashboards, and adaptive feedback stay inaccessible to implementation agents. |
| `PhoneticAlphabet`/`Phoneme` named domain rows | C6 | Named inventory gap only at `PENDING-LICENSED-SOURCE`; no C1 decoding, text, pronunciation, accessibility, or conformance semantics. |
| PDF/VT named profile row | C6 | Named inventory gap only at `PENDING-LICENSED-SOURCE`; no C1 profile semantics, validation, rendering, or conformance claim. |
| Field measurement, comparison, Flagships G/H, foundry distribution publication, final evaluation bundle | C7 | No measurement or comparator contact in C1 planning/execution before committed protocols. |

### 12.2 R0 no-claim matrix

| Observed C1 fact | Forbidden upgrade |
|---|---|
| Header/version token | File-wide conformance or effective dialect without other signals. |
| Parsed xref section | Singular valid history or proof every offset/object is correct. |
| `RevisionGraphId` | Selected document meaning; selection belongs to `DocumentViewId`. |
| Selected recovered view | Unqualified truth about malformed source or erased alternatives. |
| Raw/resolved object | Higher-layer page/font/action/attachment semantics. |
| R0 `SemanticStateId` | Serialization-total scope, canonical file bytes, writer identity, or byte-identity equivalence. |
| Decoded bytes / `DecodedContainerId` | Text/image meaning, public plaintext availability, or unique inverse source causality. |
| Info/XMP metadata reconciliation or bounded XML parse | Metadata truth, sanitization, XML safety/conformance, external-resource resolution, or file-wide semantic consistency. |
| Encryption dictionary | Strong confidentiality, all-payload encryption, credential ownership, or permissions as authorization. |
| Successful RC4/AESV2/AESV3 read | Writer encryption support, algorithm endorsement, integrity, or public-key support. |
| Signature field/`ByteRange` | Digest match, CMS verification, certificate trust, modification-policy verdict, or legal validity. |
| Security-carrier inventory | Absence of unknown/nested/semantic threats, sanitization, or safe execution. |
| Passing schema/root checker | Truth of underlying observations or availability of identity-only artifacts. |
| A validation rule or layer `Pass` | Pass in another layer, whole-document conformance, external-validator agreement, renderer behavior, safety, or repair authority. |
| Fuzz gate over declared runs | Universal panic freedom, universal security, or operational maturity. |
| Clean drift audit | PDF correctness or independent adjudication. |
| RPT.006 candidate capability-manifest row | Admission or gate passage without the matching IMM.012 receipt and RPT.008 envelope. |
| Product gate | Sealed campaign trial, Q2/Q3 verdict, external review, or field outcome. |

### 12.3 Kernel-touch declaration

`kernel-touch: initial-kernel-adoption` means C1 consumes and instantiates the ratified v8 kernel once. It may not change identity grammars, canonical encoding, evidence algebra, work/budget/capability law, clean-room law, layer direction, crate-boundary budget, report identity, or evaluation law.

If implementation reveals a kernel defect, work stops at the affected boundary. A kernel version bump, migration for every affected ID/cache/report/package/receipt, claim-lapse review, and Charter change-control record are required before resumption. A local type alias, serializer patch, or prose edit is not a substitute.

The concrete crate atlas remains provisional. Modules may be grouped or split under the boundary budget so long as owner semantics, runtime layer direction, contracts, evidence, and source policy remain intact.

### 12.4 Preconditions for later plan-to-execution conversion

Conversion occurs only with the human present and after:

- the Constitution/shell extraction is available and citations in this plan are reconciled;
- G2 decisions and D-004/D-005 routing are human-ratified where they block C1;
- fresh review has dispositioned all findings and this artifact has left `SUBMIT-FOR-REVIEW` through the owner FSM;
- the plan stays within C1 delta scope and every contract/gate/surface remains bidirectionally linked;
- card slots remain slots until the licensed human-reviewed pipeline populates them;
- no prohibited-source contact, measurement, external action, Bead creation, code scaffold, commit, or push has occurred in this authoring run; and
- the human explicitly authorizes the separate real conversion step.

This document contains no pseudo-Bead names, agent assignments, implementation ordering, or task graph. Contract dependency links are semantic inputs for that later transformation, not a simulated transformation.

### 12.5 Review packet questions

Fresh reviewers should answer with graded findings rather than editing this plan:

1. Does every Charter/Work Order C1 capability have exactly one atomic contract, surface, falsifier, and gate consumer?
2. Does any contract cross rendering/font/writer/public-key/trust/transform boundaries?
3. Can any strict path call recovery or hide a live alternative?
4. Can any source/graph/view/container identity alias a different proper domain?
5. Can any filter/security/object-stream path double-decrypt, publish partial plaintext, or cross tenant/credential/revision context?
6. Does any pending card contain semantic content or permit implementation from memory?
7. Can any runtime/crypto provider be inferred before D-005 ratification?
8. Does every report/example carry required source/graph/view/derivation/expected-state identities when its family mandates them?
9. Do API/dependency/claim checks verify structured truth instead of headings?
10. Does any claim vocabulary, capability row, CLI exit, product gate, or fuzz result imply more than exact evidence supports?
11. Can the encrypted-object-stream slice be implemented as written without another plan section?
12. Does graceful degradation keep the wedge usable while honestly blocking campaign closure when independence evidence is missing?

### 12.6 C1 authoring handoff

At the renewed `SUBMIT-FOR-REVIEW`, this plan remains `DRAFT` and `provisional-pending-substrate`. R01–R05 have been owner-premise-checked and dispositioned by G3, but that does not self-award passage or promote reviewer grades. Root may route any fresh review under the declared lenses. G3 does not route a reviewer, create execution artifacts, or claim Cycle 1 implementation readiness.
