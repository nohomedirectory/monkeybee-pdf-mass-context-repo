---
generated-by: Codex G1 owner
date: 2026-07-14
inputs:
  - MONKEYBEE_CAMPAIGN_CHARTER_v1.md
  - CYCLE_0_WORK_ORDER.md
  - AUDIT_FINDINGS_LEDGER.md
  - MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md
  - constitution/MONKEYBEE_CONSTITUTION_v8.md
  - DISPUTES.md
  - "gauntlet/ROUND_LOG.md (bounded R14 lines 1815-2081 only)"
status: PROPOSED
evidence-status: provisional-pending-substrate
shell-version: 8.0-proposed
---

# MonkeyBee v8 Shell Reference Corpus

This file preserves the non-kernel planning corpus for future archaeology-first delta plans. It is provisional reference material, not a frozen kernel, cycle schedule, implementation inventory, or substitute for repository reality. The Charter controls cycle staging. `constitution/MONKEYBEE_CONSTITUTION_v8.md` is the sole proposed normative home for the extracted kernel laws.

## Shell use and generated-echo law

- Revision 7 stable section identifiers are preserved for navigation.
- An inline `generated-echo` marker points to a Constitution law without restating or modifying it.
- `generated-echo-scope: document-wide for any sentence that repeats, specializes, or applies a Constitution law; nearest stable Constitution citation identifies the source.` Domain-specific shell semantics remain provisional and cannot override that source law.
- Appendix B is regenerated from the Constitution §10.6 field obligations and marked as a generated echo; prose in an example cannot strengthen the schema.
- The concrete crate atlas remains provisional. Its §30.1.1 boundary budget is replaced here by a generated echo to the Constitution.
- `ALIEN_ARTIFACT.md` and `PROJECT_OVERVIEW.md` are `SOURCE-UNAVAILABLE` under D-002. This corpus does not reconstruct either file.
- Any future delta plan must start from repository archaeology under Constitution §34.9. This corpus cannot establish that imagined structures exist.

## 0. Status, purpose, and how to use this document

This is the seventh internal revision of the first serious whole-system plan for MonkeyBee PDF. Revision five integrated the competitive-claim and ambition addendum and preserved its nine unresolved conflicts. Revision six retained that history and performed the first full-document post-merge fresh-eyes audit. Revision seven is the second full-document post-merge adversarial audit. It separates semantic equivalence from provenance-bearing reality identity; defines operation-specific `ExpectedStateId` precondition commitments and cross-surface capability consequence contracts; replaces unverifiable open-field language with discovery-protocol-qualified claim scopes; makes predeclaration tamper-evident; tightens embedded-language authority, form execution, Form-XObject caching, cryptographic nonce claims, XML safety, agent-edit idempotency, held-out governance, and foundry baselines; refreshes newly material released competitors; and aligns the alien-artifact evaluation with the canonical distinction among artifact, foundry, and lineage alienness. This remains a **markdown plan in plan space**: a product, architecture, workflow, failure-model, evidence, and tradeoff document intended to keep the whole system visible while global reasoning is still cheap.

It is **not** an execution package. It intentionally contains no issue identifiers, work-item inventory, execution ordering, implementation dependency map, agent-launch schedule, file-reservation scheme, or repository task-routing configuration. Those belong to a later and separate transformation after the markdown plan has converged. Mixing those representations prematurely makes the plan worse at its actual job: deciding what the system is.

The plan is intentionally broad because the project is broad. Its purpose is to make the entire product legible while the entire product still fits inside a reasoning context. It does not claim that every decision is final.

### 0.1 What this version has done

This version:

- Defines the product as more than a parser, renderer, or writer.
- Establishes a shared representation for exact bytes, historical revisions, semantic objects, page execution, appearance, text, structure, security, and compatibility.
- Separates normative interpretation, empirical compatibility, malformed-input recovery, and heuristic inference.
- Defines user workflows and failure behavior before implementation.
- Defines a safe-Rust and clean-room-protocol operating contract.
- Defines a layered architecture and provisional crate atlas as a semantic design hypothesis.
- Defines a PDF-specific assurance program, independent oracles, continuous fuzzing, and held-out corpora.
- Defines public capability envelopes and flagship campaigns that demonstrate integrated consequence rather than isolated features.
- Defines how the project will substantiate, rather than merely proclaim, a post-agent alien-artifact claim.
- Removes all execution-work decomposition from the markdown plan.
- Corrects a standards-registry error that grouped ISO/TS 32005 with PDF 2.0 core technical specifications instead of the PDF/UA/WTPDF accessibility family.
- Adds a versioned effective-dialect model spanning header, catalog override, extension declarations, feature requirements, and selected profile.
- Makes draft/transform lineage and object origins support multiple source roots and composite fragments without invented identity continuity.
- Makes durable byte-exact evidence impossible to mint from an ephemeral or changing source.
- Makes decoder publication, capability use, diagnostic emission, and evidence checking explicitly transactional or least-authority where required.
- Separates project-owned diagnostic collection from non-authoritative host observation.
- Makes evidence identity, evidence availability, and evidence recomputability separate claim dimensions.
- Separates page-program execution state from saved graphics state and makes text clipping/render modes explicit.
- Breaks the page-VM/font cycle through a low-layer font-execution protocol while keeping Type 3 programs in the page interpreter.
- Defines transitive, role-aware page import and merge semantics across source roots.
- Separates private transformation finalization from independently assured host publication.
- Separates content-removal evidence from scoped inference-resistance evidence in redaction.
- Replaces several apparently linear pipelines with typed semantic decision graphs where PDF ordering is feature-dependent.
- Integrates a dated competitor register, per-lane comparison-claim doctrine, six evidence-gated comparison lanes, twelve additional bets, four workflows, four flagship campaigns, and associated scope, risk, protocol, and decision amendments without introducing execution work.
- Performs the directed merge-interaction pass over §§10, 11, and 16, adding the evidence, replay, capability, privacy, and active-content constraints required by the new bets.
- Subjects the integrated field-comparison program to an anti-cherry-picking audit: competitor eligibility, comparison cutoffs, artifact identity, denominator freeze, adjudication, uncertainty, and lifecycle-versus-outcome are now explicit.
- Refreshes the dated competitor snapshot against current primary release and project documentation, removes stale vanity metrics and unsupported absolutes, and records newly material extraction, accessibility, editing, and agent-surface competitors.
- Corrects the receipt-signing model so signatures and transparency logs authenticate scoped assertions and log relations, while replay or checking establishes only its declared recomputation/equivalence relation; correctness remains independently grounded, and project release keys no longer sign arbitrary operation receipts.
- Makes metered AcroForm execution atomic over the field graph, admits bounded static XFA projection without calling it a dynamic runtime, and gives legacy execution, recognition, agent edits, replay, proof artifacts, GPU certificates, log publication, and field-comparison reports explicit layer owners without requiring new crates.
- Adds three competitive claim scopes (`named_set_lead`, `registered_open_field_lead`, and `observed_field_lead`), an `incomparable` outcome, paired/cluster-aware statistical design, stopping and stochastic-run rules, complete denominator accounting, and a versioned competitor-discovery protocol so a lead cannot be manufactured by pseudo-replication, optional stopping, selective omission, or an incomplete market search.
- Refreshes fast-moving challengers to exact observed releases or latest observed artifacts: `oxidize-pdf` 4.0.1, `pdf_oxide` 0.3.74, `stet`/`stet-pdf-reader`/`stet-pdf` 0.2.1, `pdfpurr` 0.4.0, PDFluent 1.0.0-beta.17, `printpdf` 0.10.1, `fop-pdf-renderer` 0.1.2, `pdfsink-rs` 0.2.9, `pdforg-render` 0.1.0, OpenDataLoader 2.4.7, and PDF Reader MCP 3.0.14; rendering, generation, editing, signature, XFA, accessibility, and extraction comparisons may no longer assume the addendum’s originally named projects exhaust the field.
- Hardens transparency publication against split-view/equivocation and irreversible membership disclosure, and hardens §33 baselines/ablations against deliberately weak controls or destructive removals.
- Adds hostile-data, confused-deputy, stale-anchor, recognizer-drift, benchmark-denominator, proof-correspondence, statistical-design, transparency-equivocation, baseline-validity, public-playground, semantic-commitment, and lazy-cache-dependency risks that the revision-five merge did not fully capture.
- Removes the last transform-identity cycle by keeping post-root `TransformId` out of result origins, root-qualifies every cross-root origin edge, defines separate order-independent semantic and provenance-bearing reality commitments, and replaces impossible one-step “actually used capability” cache lookup with a two-stage validated dependency-and-selection manifest.
- Generalizes S4 and S6 challenger selection so named anchors cannot silently stand in for the complete eligible field or non-dominated comparator set.
- Separates `SemanticStateId` from `RealityStateCommitment`: semantically equivalent results may share a semantic identity while retaining different histories, origins, transform intentions, and source roots; provenance-sensitive operations can no longer accidentally reuse a value-only identity.
- Replaces graph-symmetry refusal as the ordinary canonicalization fallback with ordered structures, unordered multisets, equivalence classes, and multiplicity; refusal is reserved for identity-sensitive claims that truly require an unjustified distinction among symmetric nodes.
- Makes evaluation protocols content-addressed and independently time-committed before unblinding or candidate comparison; changing a comparator, metric, denominator, holdout-access rule, or stopping rule creates a new protocol and requires fresh evidence.
- Defines adaptive-holdout budgets, no-feedback windows, and fresh-set replacement so a repeatedly queried hidden corpus cannot remain cosmetically “held out.”
- Makes agent edit batches atomic and crash-safe at the semantic contract: durable idempotency records return the prior outcome, while crash-ambiguous application is `indeterminate` and is never blindly retried.
- Splits structural, empirical, and adaptive maturity and adds consequence-compression measures, so synthetic coverage cannot masquerade as operational history and feature volume cannot masquerade as alien integration.
- Defines canonical operation-specific `ExpectedStateId` commitments so a root/view name, mutable label, timestamp, or stale validation result cannot authorize publication; every included predicate is re-evaluated at mutation/finalization.
- Keeps `ExpectedStateId`, caller authority, idempotency, and publication generations out of `TransformRootId`; they guard and evidence the operation without turning transient host/session state into document reality or leaking it through root identity.
- Defines atomic capability consequence contracts and typed compositions so Rust, CLI, C ABI, WASM, service/agent, reports, benchmarks, and release prose cannot independently regenerate incompatible identity, authority, outcome, evidence, determinism, privacy, or no-claim semantics.
- Adds versioned `FieldDefinitionId`s and separates pure-Rust, all-open, and observed opaque fields, so a narrow ecosystem win cannot be marketed as an unqualified open-field or global result.
- Corrects the signature-determinism model: encryption nonces and salts remain scheme-governed fresh material, while signature creation follows the admitted algorithm’s deterministic, randomized, or hedged nonce law; a deterministic signature profile may claim byte identity only when every signed input and encoding is pinned and independently verified.
- Makes field discovery a three-stage, three-commit process: the search protocol is committed before searching, the resulting field/comparator report is committed after the nomination challenge, and only then is the measurement protocol committed against that frozen set before measurement.
- Replaces the single-frontier-bet attention rule with bounded parallel moonshot probes while retaining the rule that at most one moonshot may block a declared release envelope or force project-wide architectural churn at once.

### 0.2 What this version has not done

This version has not yet:

- Survived four or more **full-document** fresh-context review rounds after the revision-five merge. Revisions six and seven are the first two such integrated-whole reviews; the addendum’s earlier focused rounds remain useful but do not satisfy this condition.
- Been compared against multiple independent competing plans and synthesized.
- Produced a clause-by-clause standards coverage matrix.
- Recorded legal and licensing review for specification access, source use, and test corpora.
- Frozen third-party dependency selections and versions.
- Retired architecture-critical unknowns through bounded, quarantined probes.
- Frozen the first implementation envelope.
- Defined the later execution representation or repository coordination policy.

Those omissions are deliberate at this stage. The project remains in whole-system design.

### 0.3 Planning gates

This document moves only through plan-space gates:

| Gate | Required evidence |
|---|---|
| **Foundation** | Mission, user workflows, clean-room rules, standards registry, stack direction, source policy, and product boundaries are coherent. |
| **Whole-system coverage** | Architecture, data models, APIs, failure behavior, security, performance, testing, compatibility, authoring, transformation, and operational closure are all represented. |
| **Comparative synthesis** | Independent competing plans have been compared, disagreements surfaced, and the strongest ideas reconciled into one internally coherent document. |
| **Review convergence** | Repeated fresh-context reviews produce marginal rather than structural changes. |
| **Plan freeze** | The first implementation envelope, source policy, public claim boundaries, provisional crate semantics, and unresolved research bets are explicit enough to serve as a stable source for a later execution transformation. |
| **Implementation authorization** | Separate implementation-readiness work has occurred outside this markdown plan, and no unresolved architectural issue still requires global redesign. |
| **Ship** | Product workflows, independent evidence, security hardening, operational closure, documentation, and feedback-to-infrastructure capture are complete for the declared release envelope. |

Failure at a gate sends the project backward. It does not authorize optimistic advancement.

### 0.4 Ambition tags

The plan uses three tags:

- **[S] Solid** — established engineering or mathematics; the challenge is excellent implementation and exhaustive evidence.
- **[F] Frontier** — published or demonstrated ideas that are not normal in PDF engines; meaningful engineering or product risk.
- **[M] Moonshot** — novel synthesis or an unusually strong realization; never made a blocking prerequisite for a declared release envelope until evidence justifies promotion.

### 0.5 Source hierarchy

The project’s truth sources, in descending authority, are:

1. Legally obtained, controlling ISO PDF standards plus published ISO amendments and corrigenda, each with edition and status recorded.
2. Normative references incorporated by those standards.
3. Separately identified errata collections, ratified interpretations, and application notes, each authority- and status-limited rather than mislabeled as ISO text.
4. MonkeyBee `SpecCard` paraphrases linked to exact clauses, amendments/corrigenda, and separately identified errata or interpretation records.
5. Machine-readable models such as the Arlington PDF Model, used as complementary evidence rather than a replacement for ISO text.
6. Atomic conformance corpora and independently authored validation profiles.
7. Black-box behavior of named, versioned external processors under explicit compatibility profiles.
8. Real-world documents with known provenance and licensing.
9. Project tests, diagnostics, and prior decisions.

Existing PDF engine source code is not an implementation source.

### 0.6 Fresh-eyes review disposition

Revision seven applies eight classes of check to the integrated whole:

1. **Conceptual identity audit** — whether value equivalence, provenance, history, intent, and operation identity remain separate; whether graph canonicalization handles symmetry without accidental nondeterminism or needless refusal.
2. **PDF-domain audit** — whether fonts, color, signatures, forms, active content, revisions, codecs, XML, encryption, Form XObjects, and rendering semantics remain distinct where they must.
3. **Rust/API and transactional audit** — whether the trait sketches support metering, cancellation, immutable snapshots, transactional publication, scoped capabilities, crash-indeterminate outcomes, idempotency, secure entropy, acyclic identities, and view-scoped reuse.
4. **Security-claim audit** — whether nonce uniqueness, sandbox isolation, sanitizer parity, signature roles, transparency relations, negative evidence, or external-service identities promise more than the mechanism can establish.
5. **Claim-science and discovery audit** — whether competitor discovery, artifact selection, comparator cutoffs, denominators, analysis units, missingness, stopping, adaptive holdout access, benchmark ownership, or precommitment could counterfeit a lead.
6. **Post-agent causal audit** — whether historical and contemporaneous baselines, total search, human attention, task novelty, model drift, ablations, maturity types, and consequence compression support the exact artifact/foundry/lineage proposition claimed.
7. **Plan-space audit** — whether the document contains only whole-system reasoning and avoids issue decomposition, work ordering, launch structure, or other execution representation.
8. **Document audit** — heading structure, fenced-block integrity, table shape, broken internal references, stale identifiers, duplicate separators, revision-history claims, and contradictions among public claims, release envelopes, and crate responsibilities.

This remains an internal review. It does **not** satisfy the requirement for several independent competing plans, completion of the full §34.2 comparative-synthesis gate, legal review, or repeated full-document fresh-context convergence.

## 1. Mission and product thesis

### 1.1 Mission

MonkeyBee PDF’s long-term target is a complete PDF substrate written primarily in memory-safe Rust under a documented clean-room development protocol.

“Complete,” “memory-safe,” and “clean-room” are release claims, not slogans:

- **Complete** always means complete for a machine-readable capability envelope, never “every historical PDF behavior.”
- **Memory-safe** covers project-owned safe Rust plus explicitly audited unsafe capsules and dependencies; it does not claim that compilers, operating systems, third-party code, or hardware are metaphysically incapable of memory defects.
- **Clean-room** describes project-controlled implementation inputs and review separation. Because foundation-model training data are not fully inspectable, MonkeyBee does not claim that model weights have never contained existing PDF-engine source.

It will:

- Read PDF files from PDF 1.0 through PDF 2.0 under a versioned dialect model, using rights-cleared historical specifications and extension declarations rather than treating one header token as the whole language version.
- Preserve the immutable source bytes; expose every discovered revision occurrence and every defensible revision-chain hypothesis, with gaps and ambiguity explicit.
- Parse well-formed files strictly.
- Analyze and recover malformed files without silently pretending they were valid.
- Render pages faithfully into pixels under declared output and compatibility profiles.
- Extract glyphs, text, structure, annotations, metadata, and security-relevant behavior with explicit confidence and provenance.
- Generate valid, interoperable PDF files that are byte-deterministic only for declared entropy-free profiles and reproducibly evidenced for secure randomized profiles.
- Modify existing files in both source-preserving and canonical-rewrite modes.
- Validate documents against the core PDF object model and selected standardized profiles.
- Redact and sanitize content with evidence about what was removed and what remains uncertain.
- Explain important outputs through source-byte/virtual-span lineage for source-backed documents or draft/transform lineage for source-free authoring.
- Operate safely on hostile input under explicit time, memory, recursion, decode, instruction, and output budgets.
- Embed as a Rust library, C ABI, command-line tool, and eventually WebAssembly module without depending on a browser or managed runtime.

### 1.2 Product thesis

The ordinary product category is “PDF library.”

MonkeyBee’s stronger identity is:

> **A document-truth engine that maintains a causal, evidence-carrying relationship among source bytes, document history, object semantics, page execution, visible appearance, text meaning, security state, compatibility behavior, and transformations.**

A conventional engine returns an object, string, page image, or rewritten file.

MonkeyBee returns that result together with the information required to answer:

- Where did it come from?
- Which revision introduced it?
- Which interpretation rule was used?
- Was the input conforming, compatible, recovered, or ambiguous?
- Which resource limits were consumed?
- Which external profiles agree or disagree?
- What changed during a transformation?
- Which claims are exact, normative, empirically validated, heuristic, or refused?

### 1.3 The founding move

MonkeyBee’s founding move is to refuse the idea that a PDF is merely an object tree.

A PDF simultaneously exists as:

- immutable source bytes;
- a chain or graph of incremental revisions;
- cross-reference structures and object histories;
- a COS object graph;
- executable page-content programs;
- a graphics and compositing scene;
- a glyph and text-semantic graph;
- a logical structure and accessibility graph;
- a security, signature, action, and attachment graph;
- and a family of observed behaviors under different conforming or de facto processors.

These are different charts over one document reality. No single chart is privileged for every task.

### 1.4 Why this must be a blank-slate design

A wrapper around an existing renderer could deliver pixels quickly, but by itself would neither establish nor expose the coherent provenance model MonkeyBee requires across parsing, repair, rendering, text extraction, editing, writing, validation, and redaction; the inherited engine’s opaque identity and recovery choices would remain part of the claim boundary.

A port of an existing engine would inherit:

- its object identity choices;
- its recovery heuristics;
- its historical compatibility branches;
- its error boundaries;
- its memory model;
- its rendering decomposition;
- and its licensing constraints.

The project needs one conceptual foundation that treats exact bytes, semantic meaning, recovery, compatibility, and evidence as first-class from the beginning.

---

## 2. Definition of success

MonkeyBee succeeds only if it advances several frontiers together.

### 2.1 Functional frontier

The engine must eventually provide a coherent path through:

```text
bytes
  -> revisions
  -> objects
  -> document structure
  -> page programs
  -> graphics / glyphs / images
  -> pixels and semantic outputs
  -> edits and generated documents
  -> independently checkable evidence
```

Partial libraries can be useful. This project’s defining claim requires continuity across the entire path.

### 2.2 Safety frontier

For arbitrary attacker-controlled bytes:

- no memory unsafety;
- no undefined behavior;
- no uncontrolled recursion;
- no unbounded decode expansion;
- no unmetered embedded-program execution;
- no network access or external process execution by default;
- no silent permission escalation;
- no panics treated as ordinary input errors;
- and no partial transformation presented as completed security work.

### 2.3 Correctness frontier

Correctness is not one scalar.

The engine must distinguish:

- exact byte facts;
- normative PDF semantics;
- output-profile-dependent rendering choices;
- empirically observed compatibility behavior;
- malformed-input recovery;
- and heuristic semantic inference.

A correct engine does not erase those distinctions.

### 2.4 Assurance frontier

Important capabilities require evidence from more than one source.

The project must combine:

- clause-linked requirement cards;
- machine-readable object-model checks;
- atomic conformance fixtures;
- analytic rendering oracles;
- property and metamorphic tests;
- black-box differential behavior;
- independent validators;
- coverage-guided fuzzing;
- resource-exhaustion testing;
- and held-out real-world documents.

### 2.5 Human-attention frontier

The implementation process must not require a human to manually review every generated line.

Human attention is reserved for:

- architectural invariants;
- unresolved standards interpretation;
- legal and clean-room boundaries;
- security claims;
- evidence independence;
- release-envelope decisions;
- and failures that reveal a wrong model rather than a local bug.

### 2.6 Evolution frontier

After the first declared release envelope, MonkeyBee must absorb new:

- errata;
- standards profiles;
- malformed-input families;
- codecs;
- security attacks;
- output profiles;
- language bindings;
- and transformation goals

without creating parallel object models or bypassing the evidence, budget, diagnostic, and provenance systems.

### 2.7 Operational frontier

A complete artifact includes:

- reproducible builds;
- deterministic release artifacts;
- dependency and license auditing;
- fuzzing infrastructure;
- corpus management;
- migration policy for serialized reports;
- stable diagnostic codes;
- API lifecycle policy;
- observability;
- incident intake;
- minimized regression fixtures;
- and a sustainable release process.

### 2.8 The post-agent claim

The project will not call itself a post-agent alien artifact because it has many crates, commits, agents, or tests.

The claim becomes defensible only if:

- the integrated artifact works beyond staged paths;
- the production ledger is bounded and authenticated;
- equal-resource baselines are weaker;
- ablations show that the custom architecture matters;
- held-out extension tasks inherit the whole system;
- and repeated trials demonstrate more than a selected best-of-many result.

---

## 3. Scope and release envelopes

### 3.0 Capability envelopes and staged public releases

The long-term scope below is not one binary v1 promise. Every build publishes a capability manifest, and public releases advance through named functioning envelopes:

| Release envelope | Primary user value | Required consequence | Explicit exclusions at that stage |
|---|---|---|---|
| **R0 — Revision Autopsy** | Safe forensic inspection of hostile PDFs | Immutable source snapshot; exact syntax, xref/revision/object history; common lossless filters; encryption inventory; structural signature and `ByteRange` discovery without cryptographic-trust conclusions; bounded recovery alternatives; structured reports | Encrypted contents remain partial or refused without caller-supplied credentials/key capability; no general page-fidelity claim; advanced image codecs may be refused |
| **R1 — Explainable Display Core** | Safe preview and causal rendering for common documents | Vector paths, common images, common embedded fonts, page VM, transparency subset, text/glyph traces, declared screen-render profile | No blanket print/RIP fidelity; capability gaps are page-local refusals |
| **R2 — Interoperable Writer Core** | Deterministic unencrypted creation and append-only editing | Typed draft root, common text/image/vector authoring, strict reopen, external-reader matrix, source-preserving incremental writes, and structural signature-impact classification (`ByteRange`, `DocMDP`, `FieldMDP`, and field locks) without cryptographic-trust conclusions | Secure random encryption output and advanced structured authoring remain separate profiles |
| **R3 — Transformation and Security** | Evidence-rich rewrite, sanitization, redaction, signature analysis, and optional secure standard-handler output | Canonical rewrite, carry/drop map, active-content reachability, clone-on-write resource surgery, scoped negative evidence, layered signature reports, and D1R re-encryption only when the secure writer profile is present | No absolute claim that semantic secrets hidden in arbitrary vector art can be detected automatically; no signature-creation claim |
| **R4 — Advanced Profiles and Rare Features** | Broad PDF civilization coverage | JPX/JBIG2 default paths if gated, advanced ICC/print profiles, selected PDF/A and PDF/UA profiles, advanced forms/portfolios/media inventory | Unsupported standardized or proprietary extensions remain enumerated |

A release may be extremely useful before R4. The project must never hold safe inspection, common rendering, or interoperable generation hostage to one rare codec or profile.

The first commercial/product wedge is **secure document ingestion and evidence-rich transformation**: inspect hostile files, produce bounded previews and inventories, remove or rewrite dangerous content, and return machine-readable evidence. This wedge exercises MonkeyBee’s differentiating architecture earlier than a generic “replacement for every PDF engine” claim.

### 3.1 Core read support

The long-term reader envelope is the core PDF language from PDF 1.0 through PDF 2.0, including:

- lexical syntax;
- all COS object types;
- cross-reference tables and streams;
- trailers and incremental updates;
- object streams;
- linearized files;
- stream filters;
- the standard security handler and admitted public-key security-handler profiles;
- document catalog and page trees;
- resources and inherited page attributes;
- content streams;
- vector graphics;
- text and fonts;
- images, masks, shadings, and patterns;
- transparency and blend modes;
- annotations, appearances, actions, and forms as data;
- optional content;
- logical structure, marked content, metadata, and associated files;
- signatures as historical and cryptographic structures;
- and PDF 2.0 additions admitted by the standards registry.

### 3.2 Core write support

The staged long-term writer envelope targets:

- deterministic PDF 1.7 output for broad compatibility;
- deterministic PDF 2.0 output for current semantics;
- cross-reference tables and streams;
- object streams;
- incremental updates;
- embedded and subset fonts;
- images and graphics;
- metadata;
- outlines, destinations, links, annotations, and form data;
- optional encryption;
- tagged structure through the structured authoring surface;
- and explicit conformance profiles where the required validation is available.

The current writer-version envelope remains PDF 1.7 and PDF 2.0. Supremacy lane S4 exposes, but does not resolve, a version-scope conflict: PDF/A-1 requires a PDF 1.4-capable serialization profile, while this section does not currently admit one. Open decision 8 in §35 must either scope the lane to PDF/A-2+ and PDF/UA-1 or explicitly widen this envelope; this revision makes neither choice silently.

### 3.3 Transform support

The complete transformation envelope includes:

- lossless inspection and preservation;
- append-only incremental edits;
- full canonical rewrite;
- page insertion, removal, reordering, and import;
- metadata edits;
- annotation and outline edits;
- resource deduplication;
- recompression and image optimization;
- font subsetting or replacement under explicit policy;
- structure repair where evidence permits;
- flattening;
- sanitization;
- secure redaction through full rewrite;
- profile conversion with an evidence report;
- and semantic and visual diff.

### 3.4 Validation profiles

The architecture must support profile modules for:

- core PDF object-model validation;
- PDF/A families;
- PDF/UA families;
- Tagged PDF structure relationships;
- PDF/X and graphic-arts profiles;
- security-hardened ingestion;
- preservation mode;
- and named compatibility profiles derived from black-box evidence.

Not every profile must ship in the first public release. The profile engine and evidence schema must exist early so later profiles do not become disconnected validators.

### 3.5 Explicit initial non-goals

The initial release does not execute:

- general Acrobat JavaScript outside Bet 16’s explicitly bounded, metered AcroForm calculate/format/validate subset;
- dynamic XFA runtime logic outside Bet 16’s static XFA-to-fixed-page projection;
- launch actions;
- arbitrary embedded files;
- multimedia or Flash/SWF playback;
- 3D content;
- external URL retrieval;
- or operating-system integration actions.

The engine parses, preserves, inventories, validates, and can remove those features under policy. Bet 16’s form-JavaScript subset, static XFA projection, and deprecated-construct profile behavior are [M], capability-gated, and non-blocking for every declared release envelope R0–R4. They do not convert full JavaScript sandboxing or full XFA interaction into ordinary scope.

Flash/SWF remains inventory-and-sanitize only by default. A non-core, capability-gated adapter to an existing Rust SWF emulator is permitted in principle, subject to §30’s runtime-dependency allowlist, §4.2 rights classification, §33.3 artifact-boundary accounting, and open decision 6. It is never claimed as core MonkeyBee capability.

Other initial non-goals:

- a full desktop viewer application;
- an OCR engine; Bet 20 adds only a capability protocol and evidence class for external recognizers;
- a general office-document layout system;
- certificate-authority or key-management services;
- PDF digital-signature creation workflows; Bet 23 evidence envelopes are unsigned or use an explicitly governed caller/service/organization/attestation signer role, while project release keys authenticate release/build manifests only;
- cloud hosting as part of the core project;
- high-end prepress separations and trapping;
- or pixel-identical emulation of every historical proprietary renderer.

### 3.6 Future scope admitted by architecture, not promised by v1

- Full JavaScript sandboxing beyond the Bet 16 form-action subset.
- Full XFA rendering and interaction beyond static projection.
- Digital-signature creation workflows.
- High-end prepress separations and trapping.
- Interactive editing UI.
- Printer-driver or RIP integration.
- Distributed rendering service.
- Native OCR and document-understanding models.

The narrow Bet 16 and Bet 20 envelopes do not promote these broader programs. They remain separate until explicit plans and evidence justify them. 3D, multimedia playback, and broad prepress behavior remain refused as breadth without a new conjunction; feature-count restoration and anti-reduction are not reinstated.

---


## 4. Clean-room and specification-provenance protocol

`generated-echo: constitution/MONKEYBEE_CONSTITUTION_v8.md §4`

The Constitution is the sole normative home. No shell restatement is authoritative.

## 5. User workflows

The plan is organized around end-to-end user outcomes rather than subsystems alone.

### 5.1 Workflow A — Safe render

**Input:** a file, byte buffer, random-access source, or eventually a range-capable remote source.

**User intent:** render page N at a specified size and output profile.

**System behavior:**

1. Open under an explicit strictness, recovery, compatibility, and resource policy.
2. Discover revisions and select the active document view.
3. Resolve the page and inherited resources lazily.
4. Execute page and nested programs under budgets.
5. Decode fonts, images, functions, and masks as demanded.
6. Composite into the requested surface.
7. Return pixels and a `RenderReport`.

**Report includes:**

- exact `SourceRootId`, `RevisionGraphId`, selected `DocumentViewId`, and relevant `DerivationId`, plus source integrity class and a complete content hash only when whole-source coverage and authentication are verified;
- selected revision or recovery hypothesis and its selection evidence;
- PDF version/dialect;
- recovery decisions;
- compatibility profile;
- output color profile;
- warnings and refusals;
- resource consumption;
- missing-font substitutions;
- unsupported or policy-blocked features;
- and reproducibility identity.

### 5.2 Workflow B — Document autopsy

**Input:** a suspicious, malformed, signed, or historically edited PDF.

**User intent:** understand every discoverable and analyzed consequence within the declared capability and resource envelope, without changing the input.

**Output:**

- exact discovered byte/revision events plus one or more explicitly evidenced revision-chain hypotheses;
- cross-reference and object history, including unresolved gaps;
- shadowed and unreachable objects;
- signatures and byte ranges;
- encryption state;
- attachments and associated files;
- actions and active content;
- visible, clipped, invisible, and off-page content;
- text and glyph mappings;
- metadata across revisions;
- repair hypotheses;
- and source, virtual-span, object, or derivation-provenance links for every finding; absence of a direct byte span is itself explicit.

### 5.3 Workflow C — Text extraction with epistemic honesty

**Input:** a page or document.

**User intent:** extract text for search, analysis, or accessibility.

**Output:**

- glyph runs in visual coordinates;
- character-code sequences;
- CID and GID paths;
- Unicode mappings where exact;
- inferred mappings where necessary;
- marked-content and structure associations;
- reading-order hypotheses;
- confidence and evidence per span;
- and a no-claim result where mapping is not defensible.

### 5.4 Workflow D — Low-level generation

**Input:** pages, graphics, glyph runs, images, resources, metadata, and output policy.

**User intent:** create a precise PDF without hand-managing object offsets or resources.

**Behavior:**

- typed canvas API;
- balanced graphics and text state by construction;
- automatic resource naming and deduplication;
- deterministic object allocation;
- explicit font and color policy;
- profile validation before finalization;
- serialization and a receipt under the exact D1 or D1R profile: byte identity only when every semantic, dependency, metadata, time, service, and entropy input permits it; otherwise the receipt records the admitted variability without weakening cryptographic freshness.

### 5.5 Workflow E — Structured accessible generation

**Input:** document tree containing sections, paragraphs, lists, tables, figures, links, language, alternate text, and styled glyph runs.

**User intent:** produce a visually correct and semantically tagged PDF.

**Behavior:**

- layout through a separate structured authoring layer;
- explicit shaping adapter;
- logical structure tree generated with content associations;
- artifact/content distinction;
- Unicode and actual-text mappings;
- PDF/UA-oriented validation;
- and a report of unresolved accessibility requirements.

### 5.6 Workflow F — Preserve and edit

**Input:** an existing PDF and an edit transaction.

**User intent:** change as little as possible.

**Behavior:**

- exact source bytes remain immutable;
- the edit session finalizes a private `TransformRoot` candidate against the exact `DocumentViewId` and `ExpectedStateId`;
- unchanged source ranges are copied verbatim where safe;
- preservation serialization appends a new PDF revision only when the incremental-write contract permits;
- signature effects are reported before save;
- and the result includes an object- and byte-level receipt.

### 5.7 Workflow G — Canonicalize and optimize

**Input:** any readable PDF.

**User intent:** create a clean, deterministic representation.

**Behavior:**

- choose a target PDF version and profile;
- rebuild reachable objects;
- normalize serialization;
- deduplicate resources;
- apply approved compression and object-stream policy;
- remove unreachable data when requested;
- validate output;
- compare appearance and semantics;
- and report every material change.

### 5.8 Workflow H — Repair malformed input

**Input:** a damaged or nonconforming PDF.

**User intent:** recover the most defensible document without hiding ambiguity.

**Behavior:**

- strict parser reports the defect;
- repair engine generates bounded hypotheses;
- each hypothesis carries evidence, cost, and affected objects/pages;
- candidate documents can be rendered and compared;
- a user or policy may make a task-local selection among live hypotheses, but the selection never erases alternatives or becomes an unqualified fact about the malformed source;
- writeback is a separate explicit transformation;
- and the operation never mutates the original source; continued storage/retention follows the caller’s explicit source-lifecycle and sensitive-data policy.

### 5.9 Workflow I — Secure redaction

**Input:** a PDF and selected sensitive content.

**User intent:** remove the information, not merely cover it.

**Behavior:**

- resolve selections to source objects, streams, text, images, annotations, metadata, attachments, and historical revisions;
- rewrite affected content;
- remove or replace resource data;
- perform a full rewrite rather than an incremental append;
- attack the output with at least one independently authored forensic adapter when the strongest redaction claim is requested; otherwise return a weaker/partial outcome or refuse that headline;
- compare visible appearance outside redacted regions;
- and emit a redaction evidence package.

### 5.10 Workflow J — Sanitize hostile features

**Input:** an untrusted PDF.

**User intent:** retain static document content while removing active or externally coupled behavior.

**Policy may remove:**

- JavaScript;
- launch actions;
- submit/import actions;
- embedded files;
- rich media;
- external references;
- suspicious optional content;
- hidden metadata;
- and prior revisions.

The output report distinguishes removed, preserved, flattened, and unrecognized features.

### 5.11 Workflow K — Validate

**Input:** document plus one or more profiles.

**Output:**

- rule-level `Pass`, `Fail`, `NotApplicable`, `NotEvaluated`, `Unsupported`, or `Indeterminate` outcomes with separate severity and explicit coverage;
- exact source, virtual-span, object, or semantic locations where available;
- object paths;
- standard references;
- evidence source;
- and repair suggestions separated from validation truth.

### 5.12 Workflow L — Explain viewer disagreement

**Input:** a PDF, page, and named processor profiles.

**User intent:** understand why outputs differ.

**Behavior:**

- reproduce outputs under versioned harnesses;
- localize pixel, glyph, text, or object disagreement;
- reduce the responsible object/program subgraph;
- classify the cause as normative, implementation-dependent, malformed, recovery-specific, font-substitution-specific, color-profile-specific, or unknown;
- and generate a minimized witness where possible.

### 5.13 Workflow M — Stream and embed

**Input:** large documents, partial data, server workloads, or foreign-language hosts.

**Behavior:**

- lazy object and page access;
- bounded caching;
- page-level concurrency;
- cancellation;
- a versioned preview C ABI before the advanced capability envelope and a stable compatibility commitment only after an explicit public-interface freeze;
- deterministic diagnostics;
- no hidden global state;
- and explicit ownership of buffers and callbacks.

---

Workflow lettering continues from §5.13.

### 5.14 Workflow N — Reflowable reading

**Input:** any document for which the extraction layer can produce one or more bounded reading-order hypotheses. **Intent:** read the content at arbitrary width/size, offline. **Behavior:** extraction → hypothesis selection or alternatives → Bet 17 layout core → a declared presentation derivative; uncertain tables, equations, figures, forms, footnotes, vertical/complex-bidi regions, and other unsupported structures remain fixed-layout islands or explicit no-claims rather than being forced into plausible flow. **Report:** source text/glyph/structure evidence, selected hypothesis, region-level fidelity class, fixed-layout islands, and no-claim regions.

### 5.15 Workflow O — Accessibility remediation

**Input:** an untagged or badly tagged real-world PDF. **Intent:** a defensible candidate derivative for a named tagged-PDF or PDF/UA profile—not an unqualified compliance certificate. **Behavior:** structure and order hypotheses; transform with carry/drop/split/merge receipts; independent machine-verifiable profile checks; preservation comparison; explicit human-review obligations; and refusal where semantics cannot be defended. **Report:** what was preserved, inferred, caller-attested, externally recognized, refused, or left for human review; checker rule coverage and verdicts; usability and legal no-claims.

### 5.16 Workflow P — Agent-mediated anchored edit

**Input:** a document plus one typed proposal or an atomic batch of proposals against semantic anchors from a human tool or an agent-protocol adapter. **Intent:** change exactly the declared anchor set under ordinary API-equivalent authority. **Behavior:** bind the exact `RealityRoot`, source-backed `RevisionGraphId` where applicable, `DocumentViewId`, every anchor/substrate digest, canonical `ExpectedStateId`, cross-anchor invariant, policy, caller lease, preservation and signature constraints; treat every document/model string as hostile data; validate without side effects; and at apply re-evaluate the complete expected-state predicate under optimistic concurrency. A batch is all-or-nothing. No prompt text can widen authority, and no stale or ambiguous anchor is silently or fuzzily rebased. The idempotency key is tenant/caller/schema scoped and bound to the exact request plus a durable outcome record: a duplicate returns the original receipt; a crash for which commit visibility cannot be proved returns `indeterminate` and must be reconciled by outcome query rather than replayed. The reservation/tombstone survives at least the full retry and publication-observability window; expiry never silently permits reuse while an old output may still be visible, and request commitments obey the sensitive-hash disclosure policy. **Report:** validation/apply verdict, authority and stale-state checks, atomic-batch outcome, durable idempotency state, exact lineage/receipt, and machine-readable refusal or indeterminacy.

### 5.17 Workflow Q — External-recognition merge

**Input:** a scanned or hybrid document plus a configured Bet 20 recognizer and an explicit disclosure scope. **Intent:** a bounded text/layout attempt with honest epistemics. **Behavior:** send only the admitted page/region/derivative; validate the response as hostile bounded data; bind exact request and response artifacts plus tool/service identity; merge with native text without laundering confidence or overwriting source truth; preserve alternatives and conflicts. A pinned service name does not make the result deterministic or recomputable. **Report:** per-span evidence class, request/response identity and availability, model/service observation, confidence semantics, conflicts, transmitted scope, and replay/recomputation no-claims.

---


## 6. Non-negotiable principles

`generated-echo: constitution/MONKEYBEE_CONSTITUTION_v8.md §6`

The Constitution is the sole normative home. No shell restatement is authoritative.

## 7. The twenty-seven big bets

### Bet 1 — The Honeycomb Document Reality Graph [F]

One exact `RealityRoot` plus one exact admitted `DocumentViewId` is presented through synchronized byte/revision, COS, execution, appearance, text, structure, security, and compatibility views. A source root may admit several historical or recovered views; no root-global semantic state is invented. Conversions among views carry provenance and evidence. This is the compression mechanism from which the rest of the system follows.

### Bet 2 — A vector epistemic model, not a confidence badge [F]

PDF truth is multidimensional. Normative conformance, empirical compatibility, recovered structure, and heuristic semantics are not one ranked scalar. MonkeyBee represents them as composable evidence facets and refuses laundering.

### Bet 3 — Recovery as bounded hypothesis search [F]

Malformed PDFs can have multiple plausible interpretations. The engine builds candidate revision/object graphs, orders them under explicit evidence dimensions and admissibility gates, and preserves the nondominated alternatives instead of hiding the repair path in parser control flow.

### Bet 4 — Source-preserving and canonical modes over one model [F]

The same engine can keep untouched bytes untouched or produce a clean deterministic rewrite. The difference is an explicit transformation policy, not two separate libraries.

### Bet 5 — Pixel-to-source and glyph-to-source provenance [F]

A diagnostic build can trace a pixel, glyph, extracted character, or annotation back through compositing, graphics state, resources, content operators, objects, revisions, and source provenance. Where syntax is directly source-backed, the trace ends at exact byte ranges. Where the causal value exists only after decryption, decompression, font execution, or another many-to-many transform, it ends at an exact virtual span plus the derivation receipt and enclosing source ranges. It does not invent a unique inverse mapping to compressed or encrypted bits unless a codec- or transform-specific trace actually establishes one.

### Bet 6 — Compatibility profiles as versioned experimental science [F]

Observed behavior of external processors becomes a data set of versioned, minimized witnesses. Profiles reproduce named behavior without redefining normative conformance.

### Bet 7 — Evidence-carrying transformations [F]

Editing, optimization, repair, redaction, and profile conversion return a versioned evidence package describing what changed, what did not, what was independently checked, and what remains uncertain. Individual subclaims may be formally proved or cryptographically verified, but the package as a whole is not called a proof when it contains empirical, heuristic, partial, or unavailable evidence.

### Bet 8 — The security-budgeted document VM [S/F]

Every PDF mini-language runs under a common authority, resource, cancellation, diagnostic, and trace contract. This turns algorithmic-complexity and interpreter bugs into local, testable failures.

### Bet 9 — Bidirectional semantics [S/F]

Reader, renderer, text extractor, editor, and writer share typed operators and resources. Generated documents are not validated merely by round-tripping through the same implementation; they are checked externally, but internal semantic drift is structurally difficult.

### Bet 10 — Viewer disagreement becomes an explainable artifact [F]

Differential testing produces a causal divergence report, not a majority vote and not only a screenshot diff.

### Bet 11 — The corpus is institutional memory [S]

Every crash, mismatch, bad repair, security failure, and false assumption becomes at least a tombstone and a generalized regression property. It also becomes a minimized witness and generator seed only when rights, privacy, held-out status, sensitivity, and reproducibility policy permit; otherwise the durable memory is a redacted behavior record, commitment, or generation recipe.

### Bet 12 — Intent-to-interoperable-PDF compilation [M]

A higher-level API accepts document intent and constraints, generates candidate encodings, tests them across profiles and independent processors, and selects the smallest defensible result. This is downstream of the solid writer and assurance layers and cannot gate them.

### Bet 13 — Demand-driven parsing and rendering [F]

The document can answer page- and object-level queries without eagerly materializing the entire file. Range-backed sources, lazy object resolution, bounded caches, and resumable work enable large documents and services.

### Bet 14 — Compatibility-preserving semantic surgery [F]

The engine can repair structure, improve accessibility, replace fonts, remove active content, or compress resources while bounding visual and semantic differences under declared profiles.

### Bet 15 — The foundry is part of the scientific claim [M]

The project records models, harnesses, agents, attempts, failed branches, human interventions, budgets, and runtime dependencies; then evaluates equal-resource baselines, ablations, model substitutions, held-out tasks, and success distributions.

---

Numbering continues from Bet 15. Each bet states the frontier it advances and why it survives the conjunction-or-connectance filter.

### Bet 16 — Hostile legacy execution under the metered VM [M]

A metered, capability-gated JavaScript subset sufficient only for explicitly admitted AcroForm calculate/format/validate events; bounded static XFA-to-fixed-page projection with explicit layout and dynamic-state no-claims; and Acrobat-matched PostScript-XObject *profile behavior* where matching modern viewers normally means a policy-controlled ignore rather than a PostScript interpreter. All three share Bet 8’s authority, budget, cancellation, diagnostic, trace, and executable-feature-registry meta-contract, but each has a tenant-specific capability manifest.

The form tenant statically parses every admitted action and document-level helper into a bounded, source-linked intermediate form before execution. The dependency/effect graph includes every reachable helper and admitted built-in; dynamic loading/import, `eval`, function construction from strings, prototype mutation, reflective escape to unregistered state, and other code-producing paths are absent. The deny-by-default language/built-in manifest grants no ambient application/document object, UI, filesystem, network, process, clock, locale, randomness, or external-resource access, and no event families beyond the admitted set. Regex, date/time, numeric/string formatting, locale, and collection built-ins each have versioned deterministic semantics, explicit input/output/work limits, and either a ReDoS-resistant implementation or refusal. The tenant may read only the explicitly selected field graph and supplied deterministic host facts through typed pure capabilities; event-specific write authority is narrower still. Execution is an atomic state transition over that graph: event order, helper dependencies, reads, writes, effect journal, locale/time inputs, cycles, event storms, termination, and every changed field are receipt-bearing, and no partially computed state is published. Static XFA projection is a bounded XML/layout transformation/appearance operation, not admission of a general XFA runtime. **Conjunction:** an open scripting subset and legacy presentation path under one metered, least-authority, sanitizer-equivalent kernel. The dated register identifies no registered open competitor that publishes this complete conjunction; it does not claim global absence. This bet amends §21.7.1 and §21.9. Flash/SWF remains outside the bet; see §§3.5–3.6 and open decision 6.

### Bet 17 — One text-layout core, three consumers [F]

§22.9 already defines the shaping-adapter boundary and pins Unicode, language, script, direction, normalization, line-breaking, hyphenation, fallback, vertical-layout, shaping-engine, and font inputs. This bet adds one project-owned semantic and measurement core for the conformance-testable layers: UAX #14 line breaking, UAX #29 segmentation, and UAX #9 bidirectional ordering, each pinned to a rights-cleared Unicode data/conformance revision and an explicit tailoring profile. An audited dependency may implement a layer only if it satisfies the same contract, test corpus, identity, and no-claim rules. A prepare/layout split performs expensive analysis once and width-dependent arithmetic repeatedly. Consumers are structured authoring, reflowable presentation, and extraction reading-order support. Glyph-level shaping remains on the adapter/audited-dependency path. Exact embedded font metrics and pinned shaping inputs avoid canvas-style approximations where the source actually supplies those facts; missing/substituted fonts and language-specific tailoring remain profile-dependent.

### Bet 18 — Reflowable presentation with fidelity bounds [F/M]

A local fluid-reading derivative re-typesets extracted, reading-ordered content at arbitrary width. Every output span identifies the source glyph runs, text evidence, structure nodes, and reading-order hypothesis it depends on. The derivative is never an extraction truth, canonical document meaning, or claim that fixed layout was preserved. It publishes region-level fidelity classes and may preserve tables, equations, figures, forms, footnotes, vertical text, complex bidirectional regions, or uncertain blocks as fixed-layout islands rather than inventing a plausible flow. Ambiguous order remains alternatives or an explicit fixed-layout fallback. **Conjunction:** fixed-layout provenance with offline fluid presentation and visible uncertainty.

### Bet 19 — Accessibility remediation with receipts [F/M]

Take an untagged or badly tagged real-world PDF; emit a candidate derivative for a named tagged-PDF or PDF/UA profile; run independent machine-verifiable checks; and attach receipts stating which structure, order, language, replacement text, and associations were preserved, inferred, caller-attested, externally recognized, or refused. A validator pass is scoped to the rules it executed and never proves usability, semantic quality, or regulatory compliance by itself. Human-review obligations remain explicit for alternate-text quality, intended reading order, table meaning, and authorial semantics. OpenDataLoader-class auto-tagging makes basic tag generation contested; MonkeyBee’s intended differentiator is evidence-bearing remediation, hypothesis visibility, preservation analysis, and principled refusal rather than mere emission of tags.

### Bet 20 — Evidence-carrying external-recognition envelope (OCR and layout models) [F]

MonkeyBee still ships no OCR engine (§3.5 stands). It ships a capability protocol for local or explicitly authorized remote OCR/layout recognizers. Requests may be scoped to a page, region, or disclosure-approved derivative rather than assuming whole-document transmission. Responses are hostile untrusted data: schema size, coordinates, text length, confidence domains, object counts, nesting, content types, and provenance fields are validated under budgets before transactionally entering the text graph as `Heuristic` external-tool evidence. Durable external evidence binds the exact admitted request and exact response artifact, their availability classes, the tool/model/service identity claimed or observed, and the invocation environment. A pinned endpoint or model label does **not** by itself make the result deterministic, independently reproducible, or recomputable; those are separate measured claims, and a mutable endpoint normally supports only an operation-local observation plus retained response bytes. Tool confidence is never relabeled as MonkeyBee confidence. The public interface convention passes §4.2 rights review and does not authorize use of competitor implementation source.

### Bet 21 — The PDF Behavior Observatory [F]

The Observatory is the publication-and-governance layer over Flagship E, §24, and §28. It publishes generated snapshots of structured observation records, compatibility decisions, minimized divergence witnesses, expectation manifests, claim withdrawals, and supremacy comparison records. A browser playground over the L8 WASM surface provides legibility without changing the artifact boundary; it defaults to local processing, no upload, no ambient network or storage, strict hostile-input budgets, origin isolation, and explicit disclosure before any external capability is used. Redistributable witnesses may publish bytes; restricted cases publish bounded behavior records and rights-approved recipes. An incumbent citing a MonkeyBee witness is an aspirational external-adoption signal, not a release condition.

### Bet 22 — Agent-native semantic surface [F]

Typed, geometry-aware semantic anchors; propose→validate→approve→apply edits with receipts; atomic multi-anchor batches; and a first-class agent-protocol surface. A proposal binds the exact `RealityRoot`, source-backed `RevisionGraphId` where applicable, `DocumentViewId`, any relevant `DerivationId`, anchor types and digests, canonical `ExpectedStateId`, cross-anchor constraints, policy, caller authority, ownership/preservation constraints, signature impact, exact idempotency identity, and expiry. Apply performs a fresh optimistic-concurrency and authority check and refuses stale anchors or changed policy rather than rebasing silently. A durable idempotency record maps one request identity to one terminal receipt or an explicit crash-indeterminate state; retries query that record and never blindly reapply a mutation whose visibility is unknown. Document text, OCR, annotations, metadata, and model output are untrusted data and cannot become tool instructions, capability grants, policy changes, approval, or executable control merely because an agent consumed them. Transport-level MCP-class compatibility is not the moat—competitors already expose agent servers. The intended conjunction is anchor semantics, least authority, stale-state protection, transactional batch mutation, crash-safe idempotency, pre-apply signature analysis, and evidence-carrying lineage over the shared document reality.

### Bet 23 — Verifiable rendering and transformation receipts [F/M]

Compose reproducible build identities, deterministic classes, operation receipts, evidence packages, and independent checking into a public trust primitive. Roles remain separate: project release keys authenticate release/build manifests; an operation receipt is unsigned or signed by an explicitly named caller, service-instance, organizational, or attestation key under its own policy; and a transparency log proves only its declared commitment/inclusion/consistency/freshness relation. Replay or an independent checker may verify the declared input/build/profile/output or equivalence relation when the required artifacts are available; that proves neither normative correctness nor fidelity beyond the separately admitted oracles and claims. No signature, attestation, log entry, or self-replay alone proves that pixels or bytes were computed correctly.

Any public-log profile includes signed checkpoints/tree heads, inclusion and consistency proofs, and a monitor/gossip or independent-witness policy capable of detecting split views or equivocation. A self-hosted log observed only by its operator makes a weaker append-only claim; it cannot prove that different clients saw one history. Public commitments obey the sensitive-hash disclosure policy before admission. Once a public membership commitment is published, deletion is not a credible remedy: publication stops, a revocation/tombstone is appended, keyed contexts are rotated where relevant, and the potentially irreversible disclosure is handled as an incident. The log protocol is owned by `mb-package`; a self-hosted publisher belongs to `mb-server` or an external adapter only if open decision 4 admits it. This remains distinct from creating a PDF document signature and from operating a general key-management service.

### Bet 24 — Machine-checked kernel proofs [M]

A small mechanized-proof core, represented through §10.2’s `MechanizedProof` facet, treats file-lexer span soundness and termination, filter expansion bounds, and recovery-admissibility gating as candidate invariants for the first proof-kernel scope. The theorem, formal model, extraction or implementation correspondence, proof kernel/version, axioms, trusted code, and generated artifacts are all part of the claim. No open competitor with an equivalent published PDF-kernel proof program is identified in the dated register; this is a scoped observation, not a universal-first claim. Everything outside the proved theorem remains governed by ordinary evidence.

### Bet 25 — Deterministic GPU rendering with CPU-equivalence certificates [M]

A GPU rasterization path whose result is accompanied by a tile-level exact or metric-bounded relation to the deterministic CPU reference. Certificate generation, independent checking, proof coverage, unsupported operations, numerical domain, target/device identity, and verification cost are explicit; a checker that merely reuses the same shader or arithmetic path is not independent evidence. Equivalence to the CPU reference establishes only that relation—it cannot upgrade a wrong CPU interpretation into correct PDF rendering, so the CPU path retains its own standards, analytic, corpus, and differential evidence. Fixed-point or integer protocols may be required around blend order and associativity. The dated register currently identifies no open PDF renderer publishing this certificate contract, but novelty remains a hypothesis until adversarial survey and evidence. The bet is non-blocking for every declared envelope.

### Bet 26 — Calibrated recovery portfolio [F]

Producer phenotype fingerprints become measured priors over recovery-hypothesis ordering, never admissibility gates and never hidden parser branches. Calibration is stratified by producer family/version, defect class, time window, and sampling frame; it records uncertainty, abstention, classifier error, and distribution drift. A producer marker is attacker-controlled and may be missing or spoofed, so the prior can only influence ordering after exact and normative constraints have admitted alternatives. Expired or drifting calibration lapses automatically. Curves use `EmpiricalMeasurement` evidence rather than a new evidence kind.

### Bet 27 — Engine-level deterministic replay [F]

The operational replay pipeline turns a crash, refusal, divergence, or selected anomaly into a caller-authorized trace bundle. The bundle states the replay relation actually promised: byte equality, same-target pixel identity, bounded metric equivalence, seed replay, structural equivalence, or only reproduction of a refusal class. It binds semantic limits, fired limit, build/dependency/profile identities, used capabilities, comparator and tolerance, trace level, artifact availability, and missing external or secret state. Reproducing a result proves repeatability of that scoped relation, not that the repeated result is correct. Full tracing may perturb timing, memory, scheduling, or cache behavior; performance and wall-clock claims therefore state the capture mode and never treat an instrumented replay as an uninstrumented timing reproduction. Partial crash capture remains partial. Export has no ambient networking and obeys sensitivity/retention policy.


## 8. Architecture at a glance

`generated-echo: constitution/MONKEYBEE_CONSTITUTION_v8.md §8–8.1`

The Constitution owns the layer and dependency-direction law. The shell retains the following provisional vertical-slice planning heuristic.

### 8.2 Vertical-slice rule

No layer is considered real merely because its crates compile.

The project advances through end-to-end vertical slices:

```text
source bytes
 -> exact object
 -> page program
 -> visible primitive
 -> pixels and trace
 -> writer round-trip
 -> independent processor check
```

A narrow vertical slice with honest limits is more valuable than a broad collection of unintegrated parsers.


---


## 9–11. Kernel identity, evidence, and work laws

`generated-echo: constitution/MONKEYBEE_CONSTITUTION_v8.md §§9–11`

The Constitution is the sole normative home. Domain sections below cite those laws; they do not redefine them.

## 12. Byte sources, lexing, and revision structure

### 12.1 Byte-source and progressive-source abstractions

The parser accepts:

- owned immutable memory such as `Arc<[u8]>`;
- optionally, a lifetime-scoped borrowed-slice adapter whose document and claims cannot outlive the borrow or enter durable caches until promoted by copy/hash;
- memory-mapped files through an audited adapter;
- seekable files;
- immutable segmented or paged stores;
- bounded spooled streams;
- and progressive linearized sources through a separate host adapter.

The random-access core reads only from an immutable snapshot contract. It performs no ambient network I/O and does not block waiting for missing ranges. A durable in-process `ByteSource` must also provide bounded, cancellation-aware reads or be wrapped by an adapter that performs potentially blocking host I/O in an explicitly isolated/async boundary and publishes only finalized immutable ranges. A path, file descriptor, ETag, or once-computed digest is not by itself an immutable snapshot: the backing bytes must remain stable for every read or the adapter must spool/copy, use a platform snapshot primitive, or revalidate content pages. Memory maps over externally mutable/truncatable files are quarantined behind an unsafe/host-risk adapter because they can violate correctness and process-availability assumptions.

The durable `ByteSource` trait is owned/`'static` by design. A zero-copy borrowed-slice API, if provided, uses a distinct `ScopedByteView<'a>`/`ScopedDocument<'a>` facade rather than pretending the borrow implements durable `ByteSource`. That facade is neither `'static` nor eligible for asynchronous escape, cross-run cache insertion, preservation output, or evidence-package publication. Promotion is an explicit copy-or-snapshot operation that creates a new immutable source root and lineage receipt. The public API never advertises an unconstrained borrowed slice while requiring hidden ownership or a silent copy.

```rust
pub trait ByteSource: Send + Sync + 'static {
    /// Descriptor includes source/root ID, integrity class, declared length,
    /// and the immutable range set available in this snapshot.
    fn snapshot(&self) -> &SourceSnapshot;
    fn read_exact_at(
        &self,
        offset: u64,
        out: &mut [u8],
        cx: &WorkContext<'_>,
    ) -> Result<(), SourceError>; // May return NeedRange/SourceChanged; never fetches implicitly.
}

pub trait ProgressiveSource {
    fn request(&self, ranges: &[ByteRange], cx: &WorkContext<'_>)
        -> Result<RangeRequest, SourceError>;
    fn commit_snapshot(&self, response: RangeResponse)
        -> Result<Arc<dyn ByteSource>, SourceError>;
}
```

A nonseekable stream is either:

- spooled into a complete immutable source under a byte budget;
- exposed as a versioned partial snapshot whose missing ranges are explicit;
- consumed through the linearized-progressive orchestrator;
- or refused for operations that require unavailable random access.

Before preservation or canonical rewrite, the complete source snapshot must be materialized or the operation must explicitly prove that every untouched range can be reproduced. Caller labels never substitute for content or snapshot identity. Re-reading the same range with different bytes is a fatal `SourceChanged` outcome: source-wide identity, durable replay claims, and reusable caches for that snapshot are revoked. Operation-local artifacts may remain as evidence of the exact bytes already observed, but they are marked stale with respect to the changed source and cannot authorize preservation or publication.

### 12.2 Lexer modes

MonkeyBee has separate bounded lexical frontends for languages that only superficially resemble one another:

- **file syntax**, for objects, dictionaries, xrefs, trailers, and stream boundaries;
- **content syntax**, for page operands, operators, and inline-image boundaries;
- **calculator-function syntax**, for Type 4 procedures;
- **CMap syntax**, for mapping programs and `usecmap` inheritance;
- **form-action syntax**, for the closed Bet 16 JavaScript subset, owned as an internal `mb-form` module until the crate-boundary budget justifies a split; and
- font-program token/bytecode frontends owned by their respective font crates.

They may share exact byte/token primitives only where lexical and error semantics are identical. A calculator function is not content syntax, a CMap is not silently parsed by a general PostScript interpreter, and the form-action frontend is not a general ECMAScript engine. The admitted form subset excludes dynamic code loading/evaluation and every unregistered host binding. Every frontend preserves exact spans and exposes malformed bytes to the caller-visible recovery or refusal layer.

### 12.3 Header handling

MonkeyBee records:

- the first valid PDF header candidate;
- its exact offset;
- binary-marker presence;
- declared version;
- catalog version overrides;
- and any bytes before the header.

A header not beginning at byte zero may be compatible or recoverable, but not silently normalized into conformance.

### 12.3.1 Effective dialect and feature admission

The physical header is only one version signal. MonkeyBee computes a versioned `EffectiveDialect` record from:

- physical header version and location;
- catalog `/Version` override where applicable;
- extension dictionaries and extension levels;
- the selected historical/core standard and registered technical-specification profiles;
- object/feature requirements encountered during validation or writing;
- compatibility/recovery assumptions;
- and the caller’s target profile.

The record distinguishes `declared`, `required_by_features`, `selected_for_interpretation`, and `target_for_write`. It is computed per selected revision/effective chain, not once as a timeless document-global scalar: an incremental update may introduce a catalog override or extension declaration that applies only from that revision onward. The document-level summary is therefore a history of effective dialect records plus unresolved conflicts. A later catalog override cannot rewrite historical facts about earlier revisions, and encountering a newer feature does not silently upgrade the file into conformance. Writer admission rejects a target version/profile that cannot legally express every carried feature, or emits the exact required extension declaration under a registered profile.

### 12.4 End-of-file discovery

The strict path interprets the final `startxref` and `%%EOF` according to the selected standard version and `SpecCard` rules.

The compatibility and recovery layers may search bounded trailing regions for candidates.

Every candidate retains:

- source span;
- parsed offset;
- target plausibility;
- and the reasons it was accepted or rejected.

### 12.5 Cross-reference sections

The implementation supports:

- classic xref tables;
- xref streams;
- hybrid-reference files;
- free-list entries;
- compressed object entries;
- multiple subsections;
- `/Prev` chains;
- `/XRefStm` links;
- and malformed variants only through explicit recovery hypotheses.

The xref model distinguishes:

- what one xref section declares;
- the effective object mapping for one revision;
- and all historical object occurrences physically present in the file.

### 12.6 Revision graph

Most ordinary incremental updates form a chain. MonkeyBee models a graph because malformed or conflicting pointers may expose multiple candidates. The graph is a derived artifact over immutable bytes, not part of `SourceRootId`.

A `RevisionGraphRecord` records:

- its exact `SourceRootId`, observed-range coverage, and unavailable ranges;
- discovery/parser/recovery protocol identities and semantic limits that affected candidate admission;
- candidate revision nodes and exact defining byte ranges;
- trailer and xref lineage/provenance;
- object occurrences and candidate object mappings;
- signature-byte-range relationships and other exact history anchors;
- admissible chain alternatives, recovery assumptions, diagnostics, and unresolved gaps;
- and the evidence needed to compare or supersede an older graph over the same bytes.

Canonical serialization mints `RevisionGraphId` only after graph finalization. It contains no caller/task-selected effective chain; that choice belongs to `DocumentViewId`. A parser, errata, policy, limit, or newly available-range change may yield a new graph over the same source root, and both graphs remain inspectable. No old object occurrence is discarded merely because a later revision supersedes it, and no newer graph mutates the historical meaning of an older receipt.

### 12.7 Object occurrence discovery

Strict object locations come from valid xref information.

Recovery may scan for indirect-object headers, but scan discoveries are hypotheses until their boundaries and references are checked. The scanner maintains admitted exclusion intervals for strings, known stream payloads, object-stream decoded regions, and already parsed objects; it does not treat arbitrary `n n obj` byte patterns inside payload data as objects unless a separate broken-boundary hypothesis explicitly reopens that region.

The system distinguishes:

- xref-declared occurrences;
- scan-discovered occurrences;
- object-stream members;
- orphaned but parseable occurrences;
- and byte regions that resemble objects but failed admission.

### 12.8 Stream boundaries

Stream data location is determined using the standard rules and declared `/Length` when valid.

Malformed length recovery may consider:

- a referenced length object;
- bounded search for `endstream` candidates;
- filter-level successful termination;
- following-object structure;
- and external compatibility observations.

The selected boundary remains recovered and carries alternatives.

### 12.9 Object streams

Object streams are decoded once per cache key and indexed by their header pairs.

Members receive `VirtualSpanId`s.

Validation checks:

- object count;
- first-object offset;
- monotonic and bounded offsets;
- duplicate object numbers;
- nested-stream prohibitions;
- xref consistency;
- and decoded-size limits.

Object-stream decryption and decoding are bound to the containing object version and revision security context. Members are not independently decrypted a second time. Historical occurrences may require different effective security/revision contexts; caches include that context and never reuse plaintext across credential, tenant, or revision boundaries.

### 12.10 Linearization

The reader recognizes and validates linearization dictionaries and hint structures.

The progressive reader uses them only when their claims survive structural checks.

A malformed hint table cannot authorize out-of-bounds reads or suppress ordinary fallback parsing.

The writer’s linearization support is a later milestone and has a separate determinism and interoperability gate.

### 12.11 Exact preservation ledger

The byte layer records independent interval facets rather than forcing mutually overlapping facts into one exclusive category. A range may simultaneously be parsed, superseded, cryptographically covered, unexplained in part, preserved raw, and scheduled for removal. At minimum it records:

- parse/semantic ownership;
- raw-preservation requirement;
- explained versus unexplained subranges;
- revision/effective-state status;
- cryptographic coverage;
- disclosure/sensitivity class;
- and transformation carry/drop intent.

Preservation mode is not allowed to “clean up” unexplained bytes without caller authorization.

---

## 13. COS, document structure, and machine-readable object constraints

### 13.1 Raw COS types

The source-preserving COS enum is conceptually:

```rust
pub enum RawCos {
    Null(TokenRef),
    Bool { value: bool, token: TokenRef },
    Number(RawNumber),
    Name(RawName),
    String(RawString),
    Array(RawArray),
    Dictionary(RawDictionary),
    Stream(RawStream),
    IndirectRef(RawIndirectRef),
}
```

No variant assumes that a syntactically present value is semantically valid in its use context.

The raw-string inventory includes the distinct PDF 2.0 UTF-8 text-string form as a pending standards-card surface. This line names the feature only; its syntax, admission, and decoding semantics remain `PENDING-LICENSED-SOURCE` in `MB-SC-R0-039`.

### 13.2 Resolved values

Resolution produces a separate value carrying:

- selected object version;
- reference path;
- cycle status;
- decryption context;
- profile-dependent decisions;
- and evidence.

Callers can choose:

- one-step resolution;
- bounded recursive resolution;
- or graph traversal with cycle events.

### 13.3 Duplicate dictionary keys

Duplicate keys are preserved.

A processing profile may define which occurrence is semantically selected for compatibility purposes, but reports expose all occurrences.

Writer canonicalization chooses one explicit policy and records discarded entries.

### 13.4 Reference cycles

The object graph may contain cycles, including legal logical cycles and malformed recursive structures.

The resolver uses typed visitation states and budgets. It never relies on recursive call depth alone.

Cycle findings identify the exact reference edges.

### 13.5 Document catalog and page tree

The document layer provides typed accessors for:

- catalog;
- pages tree;
- page leaves;
- inherited page attributes (`Resources`, `MediaBox`, `CropBox`, and `Rotate` under the registered dialect rules);
- local/defaulted page attributes such as `BleedBox`, `TrimBox`, `ArtBox`, and `UserUnit` without falsely treating them all as inheritable;
- outlines;
- destinations;
- names and number trees;
- metadata;
- optional-content properties;
- AcroForm;
- structure tree;
- associated files;
- output intents;
- permissions and viewer preferences;
- and extension dictionaries.

Typed accessors return claims and diagnostics rather than unchecked casts.

### 13.6 Page-tree invariants

The page-tree walker checks:

- node types;
- parent links;
- cycles;
- `/Count` consistency;
- excessive depth;
- duplicate reachability;
- inherited attributes;
- and page continuity/lineage evidence across revisions, without treating source-bound ID equality as proof of continuity.

The resolved page view preserves every raw box array and separately records the effective `MediaBox`, `CropBox`, requested rendering box, `Rotate`, and `UserUnit` after profile-governed defaulting and validation. Non-finite coordinates, inadmissible scale values, degenerate or reversed rectangles, and boxes outside a profile's admitted numeric envelope are not silently normalized into truth: strict processing refuses or localizes the defect, while a named recovery profile may produce a normalized device rectangle with the exact repair receipt. `PageExecutionRequest` always names the requested box and fallback rule; no renderer silently substitutes CropBox for MediaBox, or vice versa, because it is convenient.

A recovered page order must say why it was selected.

### 13.7 Name and number trees

Tree handling is iterative, budgeted, and able to expose:

- malformed limits;
- unsorted keys;
- duplicate keys;
- overlapping ranges;
- cycles;
- and compatibility-selected traversal order.

Canonical writing rebalances trees deterministically under a versioned policy.

### 13.8 Arlington PDF Model integration

MonkeyBee imports the Arlington model through a versioned build step into an internal rule representation.

It is used for:

- object existence and type constraints;
- required and optional keys;
- version and extension gating;
- indirect-reference requirements;
- value and relationship constraints;
- and machine-readable documentation generation.

It is not treated as an authority for:

- lexical grammar;
- content streams;
- xref and file layout;
- incremental update semantics;
- linearization;
- rendering algorithms;
- or every ambiguity in normative prose.

Arlington-derived rules always cite both the model version and the relevant project `SpecCard` or unresolved gap.

### 13.9 `SpecCard` registry

A `SpecCard` is a project-authored, clean-room requirement unit.

It contains:

- stable ID;
- standard edition and clause references;
- errata references;
- a paraphrased requirement;
- preconditions;
- normative effect;
- known ambiguity;
- linked atomic fixtures;
- linked implementation contracts;
- linked external profiles;
- and legal provenance.

No large block of copyrighted standards prose is copied into source comments or generated code.

### 13.10 Validation layers

Validation is separated into:

1. lexical and file-structure validity;
2. COS type and object-model validity;
3. cross-object relationship validity;
4. page-program validity;
5. rendering-resource validity;
6. standardized profile validity;
7. accessibility semantics;
8. security-policy findings;
9. interoperability observations.

A pass in one layer says nothing automatic about another.

---

## 14. Malformed-input recovery as bounded hypothesis search

### 14.1 Strict parsing always runs first

Recovery is never the hidden default beneath “open.”

The open workflow records:

- strict result;
- selected recovery policy;
- generated hypotheses;
- and the recovered result separately.

### 14.2 Recovery goals

Recovery attempts to produce a usable interpretation while preserving uncertainty.

It does not attempt to make the original file conforming by declaration.

### 14.3 Hypothesis model

```rust
pub struct RecoveryHypothesis<T> {
    pub value: T,
    pub repairs: Vec<RepairAssumption>,
    pub satisfied_constraints: Vec<ConstraintId>,
    pub violated_constraints: Vec<ConstraintId>,
    pub compatibility_evidence: Vec<ObservationId>,
    pub affected_regions: Vec<Location>,
    pub ordering: RecoveryOrderingRecord,
}
```

`RecoveryOrderingRecord` stores the admissibility outcomes and each named partial-order dimension; it is not a scalar rank in disguise. Nondomination is computed from those dimensions and the engine retains the Pareto frontier of materially distinct hypotheses. Numeric UI preferences may order semantically tied alternatives for presentation, but they never authorize a singular interpretation or security claim.

### 14.4 Recovery ordering principles

The ordering has hard admissibility gates followed by a partial order:

1. memory, resource, and capability safety;
2. exact support from the immutable source snapshot;
3. satisfiable normative constraints and explicit violations;
4. assumption-set inclusion and locality—fewer/narrower repairs dominate broader repairs when other evidence is equal;
5. internal structural and revision consistency;
6. preservation of signatures and historical facts;
7. observed compatibility behavior under named profiles;
8. deterministic tie-breaking only after all semantic criteria tie.

User intent does not change what bytes plausibly mean. A caller may choose one live hypothesis for a declared downstream task, but that selection remains a caller choice over an `Ambiguous` outcome and cannot erase alternatives.

A lower-priority signal may not override a safety gate or exact contradictory source evidence.

### 14.5 Initial recovery families

The first recovery engine supports bounded hypotheses for:

- missing or invalid `startxref`;
- broken `/Prev` chains;
- incorrect xref offsets;
- missing xref sections;
- xref table/stream disagreement;
- wrong stream lengths;
- missing `endstream` or `endobj` markers;
- duplicate object definitions;
- orphaned trailers;
- missing catalog or page-tree links;
- malformed object-stream headers;
- truncated final revisions;
- and common header/EOF placement deviations.

Each family has a contract and specific kill budget.

### 14.6 Bounded search

The engine caps:

- candidate scan regions;
- object-header candidates;
- stream-boundary alternatives;
- revision-chain branches;
- total hypotheses;
- and ordering/comparison work.

When the cap is hit, the result is `Ambiguous` or `Refused`, not “best effort succeeded.”

### 14.7 Material ambiguity

Two hypotheses are materially distinct when they produce different:

- effective objects;
- page order;
- visible appearance;
- extracted text;
- attachment inventory;
- signature interpretation;
- or security conclusions.

Equivalent hypotheses may be coalesced while retaining all source assumptions.

### 14.7.1 Security conclusions across live hypotheses

A whole-document security or absence claim must hold across every live materially distinct recovery hypothesis inside the declared search envelope. If one hypothesis exposes an attachment, action, hidden revision, alternate text, or different signature boundary and another does not, the headline is ambiguous or partial. A caller may choose one hypothesis for a scoped task, but the report must retain the alternatives and cannot present that task-local choice as a fact about the malformed source.

### 14.8 Recovery profiles

Named profiles may include:

- `StrictOnly`;
- `ConservativeRepair`;
- `CommonViewerCompatibility`;
- `ForensicPreserveAll`;
- and explicitly versioned processor-emulation profiles.

Profiles are data, reviewed like code, and included in every receipt.

### 14.9 Repair writeback is separate

Opening a malformed file does not mutate it.

A caller may later request a repair transformation. The output then includes:

- all source defects;
- selected assumptions;
- exact serialized changes;
- removed or orphaned data;
- visual and semantic deltas;
- signature invalidation;
- and independent checks.

### 14.10 Recovery falsifiers

Every recovery family has independent checks where possible:

- reparse the repaired output strictly;
- render with independent processors;
- compare effective object sets;
- run structure validators;
- verify no hidden historical bytes were silently dropped in preservation mode;
- and minimize a divergence witness when processors disagree.

### 14.10.1 Recovery calibration

Recovery quality is measured on withheld malformed corpora with known or independently adjudicated intent. Track:

- singular selections later shown materially wrong;
- ambiguous cases correctly retained;
- refusals that common safe workflows could have recovered;
- security-headline changes across hypotheses;
- search cost and frontier width;
- and calibration by recovery family and producer pattern.

No global “recovery confidence” is published until empirical calibration supports a precisely scoped interpretation of that number.

### 14.11 Recovery kill criterion

If a recovery rule cannot explain its assumptions, cannot be bounded, or repeatedly converts malformed files into plausible but materially wrong documents, it is removed from default profiles and retained only as an opt-in experimental rule.

---

## 15. Stream filters and codecs

### 15.1 Common filter contract

PDF filter semantics and codec implementation are separated.

```rust
/// Immutable decoded-stage source. Metadata inspection and image decoding open
/// independent cursors so an inspector cannot accidentally consume the only
/// stream and change the subsequent decode.
pub trait DecodeSource: Send + Sync {
    fn identity(&self) -> DecodeSourceId;
    fn open_cursor(&self, cx: &WorkContext<'_>)
        -> Result<Box<dyn DecodeCursor + '_>, DecodeError>;
}

pub trait DecodeCursor {
    fn read_chunk(&mut self, max: usize, cx: &WorkContext<'_>)
        -> Result<DecodeChunk<'_>, DecodeError>;
    fn consumed(&self) -> u64;
}

pub trait DecodeSink {
    fn begin<'a>(
        &'a mut self,
        expected: Option<u64>,
        cx: &WorkContext<'_>,
    ) -> Result<Box<dyn DecodeWriteTxn + 'a>, DecodeError>;
}

pub trait DecodeWriteTxn {
    fn write(&mut self, bytes: &[u8], cx: &WorkContext<'_>)
        -> Result<(), DecodeError>;
    fn commit(self: Box<Self>, cx: &WorkContext<'_>)
        -> Result<DecodeCommitReceipt, DecodeCommitFailure>;
    fn abort(self: Box<Self>, cause: &AbortReason, cx: &WorkContext<'_>)
        -> AbortReceipt;
}

pub trait ByteFilterDecoder: Send + Sync {
    fn decode_bytes(
        &self,
        input: &mut dyn DecodeCursor,
        output: &mut dyn DecodeWriteTxn,
        params: &DecodeParams,
        cx: &WorkContext<'_>,
    ) -> Result<DecodeReceipt, DecodeError>;
}

pub trait ImagePlaneSink {
    fn begin<'a>(
        &'a mut self,
        info: &ImageInfo,
        cx: &WorkContext<'_>,
    ) -> Result<Box<dyn ImagePlaneTxn + 'a>, DecodeError>;
}

pub trait ImagePlaneTxn {
    fn plane_rows(&mut self, plane: PlaneId, rows: ImageRows<'_>, cx: &WorkContext<'_>)
        -> Result<(), DecodeError>;
    fn commit(self: Box<Self>, cx: &WorkContext<'_>)
        -> Result<ImageCommitReceipt, ImageCommitFailure>;
    fn abort(self: Box<Self>, cause: &AbortReason, cx: &WorkContext<'_>)
        -> AbortReceipt;
}

pub trait ImageCodecDecoder: Send + Sync {
    fn inspect(
        &self,
        source: &dyn DecodeSource,
        params: &DecodeParams,
        cx: &WorkContext<'_>,
    ) -> Result<ClaimOutcome<ImageStageInfo>, DecodeError>;

    /// Canonical PDF-filter result: decoded sample bytes plus a typed sidecar receipt.
    /// This path is mandatory because a codec filter may be followed by another
    /// declared filter or consumed outside an image fast path.
    fn decode_samples(
        &self,
        source: &dyn DecodeSource,
        output: &mut dyn DecodeWriteTxn,
        params: &DecodeParams,
        cx: &WorkContext<'_>,
    ) -> Result<ImageSampleDecodeReceipt, DecodeError>;

    /// Optional terminal-image optimization. It must be proven equivalent to
    /// `decode_samples` plus ordinary sample unpacking for the admitted profile.
    fn decode_planes(
        &self,
        source: &dyn DecodeSource,
        output: &mut dyn ImagePlaneTxn,
        params: &DecodeParams,
        cx: &WorkContext<'_>,
    ) -> Result<ImageDecodeReceipt, DecodeError>;
}
```

Byte-oriented filters and image-aware codec filters have different metadata needs, but both participate in the one declared filter sequence. The canonical path for every admitted chain is **stage-by-stage byte semantics in exactly the order written in `/Filter`**. DCT, JPX, JBIG2, and CCITT therefore expose canonical decoded sample bytes plus a typed `ImageStageInfo` sidecar; the planner does not assume that a codec is terminal merely because most normal image streams put it last. A later declared byte filter consumes those exact stage bytes. The canonical stage-byte layout is itself versioned and codec-specific: component order, precision, signedness, row/plane packing, color-transform behavior, truncation policy, and end-of-data semantics are fixed by source cards and conformance fixtures rather than inherited from whatever memory layout a generic codec library happens to return.

The sidecar remains attached to its stage provenance. If another filter follows, codec metadata is not automatically authority for the final decoded stream; a registered composition rule must prove which metadata survives, otherwise the sidecar is intermediate diagnostic evidence only. Final image admission reconciles the post-chain bytes with the image dictionary (`Width`, `Height`, `BitsPerComponent`, `ColorSpace`, masks, JPX alpha/color information, and profile rules) and may refuse when no defensible final sample interpretation exists.

A typed-plane path is an optimization only when the codec is the final stage for an image/image-mask consumer and its equivalence to the canonical sample-byte path is covered by shared fixtures, bit/sample-layout checks, and profile-specific evidence. A processor may reject a particular combination because a governing rule forbids it or because support is absent, but it may not impose a blanket “image codecs must be terminal” law that the declared filter model does not establish. MonkeyBee never reorders a malformed or inconvenient chain into something “more legal.” Inspection and decode each open an independent cursor over the same immutable stage identity; neither call relies on rewindable ambient state. A cursor returns either a nonempty chunk no larger than the requested maximum or an explicit end marker; zero-length non-EOF progress is forbidden, `consumed()` is monotone and checked, and borrowed chunk bytes remain valid only for the documented cursor-call lifetime. The filter-chain planner validates array alignment, stage applicability, predictor placement, canonical sample layout, and the special semantics of explicit `Crypt`/`Identity` routing, then either executes, recovery-labels, or refuses that exact declared chain under the selected profile.

Both contracts require:

- streaming where the format permits;
- deterministic output;
- explicit consumed and produced byte counts;
- expansion-ratio checks;
- cancellation checkpoints;
- typed truncation behavior;
- and no unchecked dimension multiplication.

Byte and image sinks are transactional. The filter/image planner—not the codec—owns transaction creation and the single terminal decision. It begins a private transaction, passes only the write-side transaction object to the decoder, commits after decoder completion and downstream admission, and consumes the transaction with `abort` on failure, cancellation, panic containment, or refusal. No decoded artifact becomes cache-visible or downstream-complete until `commit` succeeds; a failed commit reports private/visible/indeterminate state. Transaction objects are not clonable. An explicit consuming `abort` is required to obtain an `AbortReceipt`. Dropping an unterminated transaction prevents normal publication, poisons that transaction identity, and performs only best-effort synchronous cleanup that the implementation can honestly guarantee; it cannot promise async deletion, durable erasure, or a diagnostic callback from `Drop`. Any leftover private artifact keeps its sensitivity label and is reported as retained or unknown when the enclosing operation next reconciles transaction state. Partial bytes may be returned only through an explicitly partial diagnostic/forensic outcome, never by accidentally leaving a half-decoded cache entry.

### 15.2 Filter-chain semantics

The stream layer parses the full admitted shapes: `/Filter` may be one name or an array; `/DecodeParms` may be absent, `null`, one dictionary for one filter, or an aligned array whose entries may themselves be `null`. The same shape rules apply to `/FFilter` and `/FDecodeParms`. Alignment, type, and per-stage applicability are exact in strict mode and profile-defined only for malformed recovery. `/DL` is preserved as an advisory decoded-length hint and plausibility signal; it is never trusted as allocation authority, proof of completeness, or permission to exceed output limits.

The interface ownership is acyclic: `mb-filter` owns normalized stage parameters and decoder protocols; codec crates and `mb-security` implement those protocols; `mb-stream` assembles the declared chain. `mb-filter` never imports security-handler state, and `mb-security` never imports stream orchestration or the object resolver merely to implement a `Crypt` stage. The planner injects the already admitted object/security context. This prevents filter↔security and filter↔codec ownership cycles from hiding inside one nominal layer.

Each stage produces a receipt. A downstream failure reports the exact stage and decoded offset.

Intermediate stages are private pipes or private immutable artifacts until the complete requested chain commits; they need not be materialized merely to obtain transactional semantics. A prefix stage may enter a cache only when the planner deliberately gives that stage its own publication transaction and commits it under a complete stage identity. A half-produced stream, an implicit pipe buffer, or a downstream decoder’s partial consumption never becomes a cache entry; downstream failure does not retroactively change an intentionally committed prefix receipt.

The stream model also parses external-file entries (`/F`, `/FFilter`, `/FDecodeParms`) as data. The core never retrieves an external file implicitly. Resolution requires an explicit host capability, immutable returned-source identity, security policy, and receipt; otherwise the stream outcome is partial or refused.

### 15.3 Solid filters

Initial [S] filters:

- `ASCIIHexDecode`;
- `ASCII85Decode`;
- `RunLengthDecode`;
- `FlateDecode`;
- `LZWDecode` including `EarlyChange`;
- predictor postprocessing for TIFF and PNG predictors;
- and `Crypt` integration with the security layer.

Each gets:

- atomic fixtures;
- malformed-input fixtures;
- streaming tests;
- output-limit tests;
- and cross-implementation vectors.

### 15.4 CCITT Fax [S/F]

The CCITT implementation supports Group 3 and Group 4 parameters used by PDF, including:

- `K` modes;
- columns and rows;
- end-of-line behavior;
- byte alignment;
- black-is-one;
- damaged-row tolerance under explicit recovery;
- and bounded row output.

Analytic bitstream fixtures and image round trips are required before default enablement.

### 15.5 DCT/JPEG [S]

The PDF layer owns:

- marker handling relevant to PDF;
- abbreviated streams and color interpretation;
- decode arrays;
- image-mask semantics;
- and interaction with external color spaces.

A generic permissively licensed pure-Rust JPEG implementation may supply codec primitives after dependency review. MonkeyBee does not copy PDF-specific behavior from other engines.

The PDF adapter explicitly handles `ColorTransform`, embedded or externally supplied color metadata, abbreviated streams with an admitted and provenance-bound source of any required tables (or an explicit refusal when required tables are unavailable), component-count disagreement, and Adobe marker conventions. Generic JPEG-library defaults are not allowed to silently invent missing tables or decide PDF color interpretation.

### 15.6 JPX/JPEG 2000 [F]

JPX is a major risk area.

The plan requires:

- codestream and JP2 box parsing;
- component precision and signedness;
- color-space metadata interaction;
- alpha handling;
- region and resolution decode where practical;
- tile and precinct limits;
- and hostile dimension/packet testing.

Default shipping requires a memory-safe implementation with a sustainable maintenance story. A temporary adapter is acceptable only outside the default memory-safe artifact boundary and must be labeled accordingly.

### 15.7 JBIG2 [F]

JBIG2 support includes:

- segment parsing;
- global and page-local segment sets;
- arithmetic and Huffman coding;
- symbol dictionaries;
- text, generic, halftone, and refinement regions;
- dependency-cycle detection;
- duplicate and missing segment handling;
- page dimension limits;
- and explicit retention semantics.

Because JBIG2 has a history of complex security failures and substitution attacks, the implementation receives an elevated fuzzing and independent-oracle budget.

### 15.8 Decoder output model

Byte-filter decoders emit bytes. Image-aware codec decoders must emit the protocol-defined canonical sample-byte stream plus stage-scoped component, precision, alpha, packing, and color-metadata claims; they may additionally emit bounded image planes through `ImagePlaneSink` only as the proven-equivalent terminal optimization described above. Neither route silently performs PDF output-profile color conversion. Codec-defined sample transforms and embedded metadata are recorded at the stage boundary; PDF image interpretation remains in `mb-image` and `mb-color`.

### 15.8.1 Encoding is a separate capability

Writer-side filter encoding has its own streaming `ByteFilterEncoder` contract and capability manifest. Flate/predictor, ASCII, RunLength, LZW where a target profile permits it, and `Crypt` output semantics are not inferred from decoder presence. Encoders are transactional, versioned, determinism-classified, and independently reopen-tested. Typed image re-encoding remains codec-specific and is never smuggled through the byte-filter interface.

### 15.9 Codec dependency policy

A third-party generic codec is admissible only if:

- it is memory-safe Rust in the default build;
- licensing permits the project’s distribution goals;
- its input limits can be controlled;
- its semantic boundary is narrow;
- its version is pinned;
- it has an independent fuzzing story;
- and MonkeyBee retains PDF-specific validation and provenance.

The dependency is leverage, not hidden project credit.

### 15.9.1 Codec trust tiers and fault isolation

Memory-safe Rust removes major classes of corruption but does not eliminate hangs, panics, algorithmic bombs, or logic vulnerabilities. Codecs are assigned trust tiers:

- in-process default after full gates;
- in-process experimental with strict limits;
- isolated worker process for high-risk/server deployments;
- opt-in external adapter outside the core artifact boundary;
- or safely refused.

The isolated worker protocol carries no ambient filesystem/network access, enforces OS-level memory/CPU limits where available, and returns a content-addressed result plus decode receipt. The core treats every worker response as hostile input: it verifies protocol/version and request binding, source/stage identity, declared dimensions and component metadata, exact output lengths, resource-account totals, status/coverage, and the digest of the returned bytes or planes before publication. Where feasible it also runs cheap semantic invariants or a second decoder on sampled fixtures. A content hash proves only which bytes came back, not that the worker decoded the right image. Core correctness never depends on a worker silently substituting another request, profile, table set, or interpretation.

### 15.10 Codec kill criteria

If a complete pure-Rust JPX or JBIG2 path cannot meet the security and fidelity gates, the project does not fake completeness.

The release matrix may mark the codec:

- unsupported and safely refused;
- available through an opt-in non-core adapter;
- or supported only for a constrained subset.

The rest of the engine must remain complete and safe around that refusal.

---

## 16. Encryption, signatures, permissions, and active-content security

### 16.1 Cryptographic primitive policy

MonkeyBee does not invent modern cryptographic primitives.

It may use narrowly scoped, audited, permissively licensed pure-Rust implementations of:

- AES;
- SHA families;
- MD5 where legacy PDF semantics require it;
- RC4 where legacy compatibility requires it;
- random generation;
- and authenticated signature algorithms.

MonkeyBee owns the PDF-specific security-handler semantics, object-key derivation, crypt-filter routing, and evidence.

### 16.1.1 Entropy, nonce allocation, and determinism are separate policies

Production encryption requires cryptographically secure keying material and the exact IV/salt/nonce law of the admitted construction. Signature creation, if later admitted, follows the selected signature scheme rather than a universal randomness rule: some profiles require randomized or hedged nonces, while approved deterministic ECDSA-style derivation and EdDSA-style schemes may derive per-message values deterministically from protected key/message inputs. Canonical byte determinism must never cause encryption nonce reuse, signature nonce misuse, key reuse outside policy, or accidental replacement of a scheme-specific nonce law with a generic seed.

Writer/signing policy distinguishes:

- `DeterministicUnencrypted` — eligible for byte-identical canonical output;
- `SecureRandomizedEncryption` — explicit CSPRNG/nonce capability plus non-secret health/allocation receipt;
- `CallerEntropyCapability` — an audited entropy capability, never caller-supplied reusable IV/salt/nonce bytes;
- `SignatureNoncePolicy` — an algorithm/profile-bound policy such as approved deterministic derivation, randomized, or hedged generation, supplied only through the signer/key-operation capability; and
- `DeterministicTestOnly` — feature-gated and rejected by release builds.

For any construction whose security requires a per-message nonce or unique value, the profile defines a **per-key allocation/derivation domain**. A coordinated stateful allocator may make a no-reuse claim within its authenticated durable domain. A random-only allocator may make only a quantified collision-bound claim under an explicit key-use cap, entropy assumption, process/distribution model, and health evidence; it does not claim absolute global uniqueness across crashes, clones, hosts, tenants, or caller providers. An approved deterministic signature derivation proves conformance only to its exact algorithm and protected-input contract; optional hedging randomness, side-channel resistance, hardware behavior, and key custody remain separate claims. Local duplicate detection is defense-in-depth, not proof of unseen global history. If the required contract cannot be established, the affected profile refuses before writing/signing.

Encrypted production files are intentionally not byte-identical across runs. Signed output is scheme- and profile-specific: a byte-identical signature artifact may be claimed only when algorithm, key identity, signer role, signed attributes, encoding, document bytes, trusted-time/timestamp policy, revocation material, and every external input are pinned and independent tests establish the declared determinism. Legacy RC4/MD5 behavior is reader compatibility; writers do not emit obsolete protection by default, and any admitted compatibility profile carries severe policy warnings.

### 16.2 Standard security handler

The implementation supports standard-handler revisions applicable to the declared core standard and separately registered technical specifications, including:

- an explicit admitted matrix of `/V` and `/R` combinations, deprecated legacy behavior, required entries, key lengths, and algorithm selection;
- version-specific password preparation;
- owner and user validation;
- file encryption keys, including the applicable role of the trailer `/ID` value in key derivation and revision history;
- per-object keys for legacy revisions;
- core AES variants;
- optional AES-GCM only under its explicit technical-specification profile;
- crypt-filter dictionaries plus `/StmF`, `/StrF`, and `/EFF` defaults and per-stream `/Crypt` `/Name` or `Identity` selection;
- stream, string, metadata, and embedded-file scope, including exact `/EncryptMetadata` behavior;
- encryption-dictionary, xref/xref-stream, and other standard-defined non-encrypted structures;
- one-time decryption of object-stream containers rather than accidental double decryption of members;
- validation of the modern `/Perms` integrity block separately from interpretation of the `/P` permission bits;
- integrity-protection extensions only under their explicit profile;
- and permission bits.

The capability manifest distinguishes core ISO 32000 behavior from ISO/TS extensions; it never calls all of them “PDF 2.0 core.”

Every decrypted value retains a reference to its encrypted source bytes and security context.

### 16.2.1 Public-key security handler [F]

Broad reader completeness eventually requires the PDF public-key security handler in addition to password-based standard security. MonkeyBee initially preserves and inventories these dictionaries even when it cannot decrypt them. A released decryption profile must cover:

- recipient and crypt-filter structures;
- CMS envelope parsing and algorithm policy;
- explicit private-key/key-provider capability;
- certificate-recipient matching without ambient keychain search;
- metadata and embedded-file scope;
- revision/history interaction;
- deterministic structural reporting with secret-free receipts;
- and strict non-export of private key material.

The core never enumerates host keychains or contacts a network service implicitly. Decryption is refused when the caller does not supply a versioned key-provider capability. Signature verification and document decryption share cryptographic primitives but remain separate trust domains.

### 16.3 Password and Unicode handling

Password preparation and truncation rules are version-specific and tested with published vectors.

APIs accept explicit byte or text password forms so callers cannot accidentally rely on platform encoding. Password/key comparisons and primitive use follow vetted constant-time APIs where available, and wrong-credential reporting avoids unnecessary distinguishers. MonkeyBee does not claim whole-process side-channel immunity across allocators, caches, schedulers, operating systems, hardware, or caller-supplied providers; high-assurance deployments require a separate measured threat model.

Sensitive key material is minimized in lifetime and redacted from diagnostics.

### 16.4 Permissions are not authorization

PDF permission bits are document policy claims, not a sandbox boundary against a hostile file owner.

MonkeyBee exposes them and optionally enforces them for cooperative workflows, but reports clearly distinguish:

- cryptographic access control;
- declared permissions;
- host-application policy;
- and actual data recoverability.

### 16.5 Signature structure and profile families

The core signature layer parses:

- signature fields, seed values, locks, and dictionaries;
- signature build-property dictionaries including `Prop_Build`;
- exact `ByteRange` arrays, ordering, overlap, gap, bounds, and trailing-byte conditions;
- covered revision boundaries and shadowed-object relationships;
- `Filter`/`SubFilter` and content-container families;
- transform methods and parameters including `DocMDP` and `FieldMDP`;
- document-modification permissions and field locks;
- RFC 3161 document/signature timestamps where applicable;
- DSS/VRI and other validation-related embedded data;
- and PAdES profile structures under explicitly versioned ETSI source cards.

PDF signature structure, CMS signature integrity, PAdES conformance level, long-term validation material, and application trust are different claim families. Bet 23 evidence-envelope signatures and transparency-log records are outside the PDF file-signature family. Project release keys authenticate release/build manifests only; operation receipts are unsigned or signed by a separately governed, explicitly named caller/service/organizational/attestation role. Signature verification authenticates that role’s assertion, and log verification proves only the declared log relation. Replay or independent checking may establish only the exact recomputation/equivalence relation it executes; none of these establishes the operation’s normative correctness, fidelity, safety, or policy satisfaction by itself. None creates or replaces a PDF document signature.

Certification signatures, approval signatures, document timestamps, and usage-rights signatures (`UR`/`UR3` where encountered) are distinct semantic families. A usage-rights signature may explain viewer-enabled features but does not become a general trust or authorization claim, and an approval signature is not silently treated as a certification signature.

It first answers exact structural questions:

- Which bytes were hashed?
- Which bytes were excluded?
- Which revision was signed?
- What changes followed?
- Are ranges overlapping, out of bounds, or malformed?

### 16.6 Cryptographic and trust validation

Signature checking is layered and never summarized by one unqualified `valid` bit:

1. structural `ByteRange` admissibility;
2. exact digest relation over the declared bytes;
3. CMS/CAdES container and cryptographic signature verification;
4. signed-attribute and algorithm-policy checks;
5. signer-certificate path construction under a declared trust policy;
6. revocation evidence evaluated at an explicit time;
7. signature/document timestamp validation;
8. PAdES level and DSS/VRI/LTV completeness where requested;
9. post-signature modification classification under `DocMDP`, `FieldMDP`, field locks, and application policy.

The core may provide early layers with audited dependencies. Trust stores, trusted time, online revocation, and legal/organizational authorization use explicit host adapters and are never hidden runtime dependencies.

Reports use separate headlines such as `digest_matches`, `cryptographic_signature_verified`, `certificate_path_trusted`, `revocation_status`, `timestamp_status`, `modification_policy`, and `profile_conformance`. MonkeyBee makes no generic legal-validity claim. Verification of a Bet 23 receipt signature or log inclusion is reported through the same separation of cryptographic relation, signer authentication, trust, role authorization, policy admission, and freshness; it cannot upgrade the enclosed PDF or transformation claims by itself.

Unsupported digest/signature algorithms, missing signed content, unavailable trust material, or exhausted revocation budgets produce partial or refused subclaims. The engine never returns `digest_matches = false` when the digest was not actually computable, nor `trusted = false` when trust was merely not evaluated.

### 16.7 Historical validation

Validation is revision-aware.

The engine distinguishes:

- content signed at the original revision;
- allowed subsequent incremental changes;
- disallowed or suspicious changes;
- and present-day trust conclusions.

Canonical rewriting necessarily destroys original byte-range signatures unless a separate archival package retains the source.

### 16.8 Active-content reachability and admitted-execution graph

MonkeyBee builds a reachability/effect graph rather than a flat inventory. It records triggers and actions from catalog/page/annotation/field/widget additional actions, name trees and named actions, JavaScript, launch/URI/remote navigation/submission/import/rendition/visibility/media action families, rich media/3D/alternate presentations, embedded/associated files, encrypted-payload/unencrypted-wrapper documents, XFA packages and form dependencies, external streams/references, and orphaned or historical objects reachable only under forensic traversal.

Every node records trigger, target, revision, visibility, host capability required, executable-feature-registry class, and sanitization state. Unsupported action or XObject behavior—including PostScript and external/reference XObjects—is preserved/inventoried or explicitly refused, never silently safe. External references require an explicit immutable-source capability.

Initial releases do not execute general JavaScript or PostScript, launch programs, submit data, or fetch remote content. Bet 16 may expose only the admitted calculate/format/validate tenant. Its graph binds the selected field set, trigger/event identity, deny-by-default built-ins, supplied locale/time/clock facts, typed reads, event-specific writes, dependency/event order, cycle/event-storm handling, termination, resource charges, and atomic commit/rollback receipt. A capability omitted from this graph cannot be exercised implicitly.

Embedded-file extraction writes only to a caller-provided sink. Suggested filenames are untrusted metadata; path traversal, reserved/device names, alternate separators, and collisions are neutralized by policy. The core never writes an attachment to a host path by implication.

### 16.9 Sanitization policy

Sanitization is an evidence-carrying transformation that may:

- remove or neutralize actions;
- remove embedded files;
- remove rich media and alternate presentations;
- flatten or remove forms;
- discard hidden revisions through canonical rewrite;
- and normalize malformed structures.

The policy is named and versioned. The receipt lists every removed object and every behavior class not fully analyzed. For every admitted Bet 16 tenant, sanitization is checked against the same executable-feature registry and trigger graph used by the interpreter; sanitizer–interpreter disagreement is a critical refusal, not a best-effort warning.

### 16.10 XML and metadata safety

XMP, XFA, and every other XML path uses a hostile-input profile that disables or refuses:

- DTD processing;
- external, general, and parameter entities;
- XInclude;
- external schema, catalog, stylesheet, and namespace-resource resolution;
- network and host-filesystem access; and
- any parser mode whose expansion or callback behavior cannot be bounded.

Budgets cover source bytes, decoded bytes, depth, node count, attributes per element, total attributes, namespace declarations, name length, text length, CDATA, processing instructions, comments, and aggregate output. Entity-like or malformed constructs are preserved as source evidence or refused according to profile; they are never expanded through a host resolver. Static XFA projection receives only explicitly admitted immutable assets and font resources. Metadata extraction and XML-derived layout are separately charged and transactionally published.

---

## 17. The page-program virtual machine

### 17.1 Content programs are programs

A content stream is not parsed as a flat bag of graphics commands.

It is a program with:

- operand syntax;
- operator semantics;
- mutable graphics state;
- scoped resources;
- nested procedure-like forms;
- conditional visibility;
- and several embedded sublanguages.

The VM is deterministic, metered, traceable, and profile-parametric.

A page execution is parameterized by a `PageExecutionRequest` that fixes page box, `Rotate`, `UserUnit`, resolution, annotation inclusion, optional-content usage event (`View`, `Print`, `Export`), output profile, PDF color `RenderingIntent`, overprint policy, and degradation policy. There is no context-free “the pixels” result because PDF does not prescribe one universal rasterizer, antialiasing method, device, font substitute, or print process.

### 17.2 Program representation

The parser produces a source-preserving operator stream:

```rust
pub struct ProgramNode {
    pub id: ProgramNodeId,
    pub operands: Vec<CosOperand>,
    pub operator: OperatorToken,
    pub location: VirtualOrSourceSpan,
    pub parse_evidence: EvidenceSet,
}
```

Typed admission maps known operators into semantic variants while retaining unknown tokens.

### 17.3 Operator families

Contracts are grouped by:

- graphics-state save/restore;
- coordinate transforms;
- path construction;
- path painting and clipping;
- line attributes;
- color and color spaces;
- text objects and text state;
- text positioning and showing;
- XObjects, including Form, Image, and legacy/reference kinds under explicit support or inventory policy;
- images and inline images;
- marked content;
- compatibility sections;
- shading;
- Type 3 metrics;
- and optional content.

Each family has atomic tests and profile-specific error behavior.

### 17.4 Graphics state

The graphics state carries at least:

- current transformation matrix;
- current clip representation;
- stroke and fill color spaces and colors;
- text state;
- line width, cap, join, miter, dash, and flatness;
- rendering intent;
- smoothness tolerance (`SM`) as a profile-visible device hint with bounded/no-claim semantics;
- stroke adjustment;
- overprint settings;
- blend mode;
- alpha constants;
- soft mask;
- alpha-source flag;
- text-knockout state;
- transfer/black-generation/undercolor-removal and halftone references;
- default device color-space substitutions;
- and black-point compensation where the selected standard/profile defines it.

At the page-program layer these are source-linked semantic descriptors, scalar operands, or typed IDs—not compiled ICC transforms, raster clip masks, compositing surfaces, or resolved glyph outlines. Appearance/font services compile the deferred descriptors after the rendering request is known. `mb-gstate` therefore never imports `mb-color`, `mb-composite`, `mb-raster`, or font implementation crates.

The VM separately models execution state that PDF does **not** make part of the saved graphics state. The current path, pending path-clipping rule, operand stack, current text object, text matrix, and text-line matrix are not ordinary `q`/`Q` snapshot fields. `BT` initializes the two text matrices; `Td`, `TD`, `Tm`, `T*`, and text-showing operations update them under text-object rules; `ET` closes the text object and applies any accumulated text clipping. Likewise `W`/`W*` mark a pending clip that is realized only when the current path is ended by a painting or no-paint operator. Strict mode diagnoses stack underflow, unbalanced `q`/`Q`, illegal/nested text-object boundaries, and operators used in invalid state rather than repairing them invisibly.

Save/restore uses persistent or copy-on-write graphics-state values to make tracing cheap and avoid accidental aliasing, while these separate execution-state machines retain their own source-linked transitions. Atomic tests prove that `q`/`Q` does not accidentally restore or discard a current path or text matrix and that path/text clipping is applied at the correct boundary.

### 17.5 Resource resolution

Resources are resolved through an explicit scope stack:

- page resources;
- form resources;
- pattern resources;
- Type 3 font resources;
- and inherited page-tree resources.

Missing resources produce typed diagnostics. Compatibility substitution is never silent.

The resolver distinguishes inherited page resources from local Form, Pattern, Type 3, and annotation-appearance scopes. Resource lookup is cycle-bounded and returns an outcome; it does not replace a missing font, color space, XObject, or property list merely because a host happens to have a similarly named resource.

The `gs` operator resolves one `/ExtGState` resource to a typed graphics-state update. Admission covers the parameter families defined for the effective dialect—including line state, rendering intent, overprint, font/size, black generation and undercolor removal, transfer functions, halftones, flatness/smoothness, stroke adjustment, blend mode, soft mask, stroke/fill alpha, alpha-is-shape, text knockout, black-point compensation, and admitted extensions. Absent entries preserve prior state. Strict execution validates the dictionary into one update before applying it; it does not silently apply the convenient half of a malformed dictionary. A named recovery/compatibility rule may apply recognized entries, but the partial update, ignored entries, and resulting state lineage are explicit. L3 retains source-linked scalar values and deferred function/color/mask/halftone IDs; L4 compiles device-dependent artifacts. Cache identity includes the ExtGState object version, effective dialect/profile, and every transitive function, soft-mask, font, or color dependency actually consumed.

Text-showing execution consumes a format-neutral `FontExecutionService` injected by the caller. The protocol returns source-code segmentation, metrics, glyph selection/provenance, outline or paint-program descriptors, and semantic candidates without exposing TrueType/CFF implementation types to `mb-pagevm`. For Type 3, the service returns the selected char-procedure program, font matrix, resource scope, colorization mode, and metric/bounds evidence; the page VM executes that program in its own bounded subframe. This breaks the otherwise unavoidable pageVM↔font cycle and keeps glyph parsing, page execution, and rasterization independently testable.

### 17.6 Form XObjects

Form processing separates two reusable artifacts:

1. a parsed/admitted Form program keyed by object version, decoded program, resources, dialect, and program-admission policy; and
2. an optional rendered/display artifact whose key includes every caller and backdrop fact that can affect appearance.

A `Do` invocation creates a bounded subprogram frame. The PDF-mandated save/restore applies to graphics state. The interpreter’s subprogram boundary separately contains operand bookkeeping, current path, pending clip, text-object state, and marked-content balance so malformed inner content cannot corrupt caller execution; that containment is an implementation safety boundary and is not mislabeled as `q`/`Q` semantics. The Form matrix is concatenated, the transformed `BBox` constrains painting, Form resources are selected under exact profile rules, and transparency-group behavior is executed where present. Inner imbalance remains a diagnostic even when the caller frame is safely restored.

A rendered Form cache may be reused only when the validated dependency manifest includes the inherited caller graphics-state projection and placement context that matter: CTM, effective clip, fill/stroke color and color spaces where consumed, line/text state where consumed, blend/alpha/soft mask, rendering intent, overprint, optional-content decision, group color space/isolation/knockout, backdrop or backdrop identity for non-isolated groups, output profile, raster scale/tile context, and every transitive resource/selection witness. If a compact sufficient projection cannot be proved, cache only the parsed program or a context-independent intermediate—not final pixels. Repeated object identity alone never authorizes rendered-output reuse.

Cycles are detected by object-version identity and active invocation path, not only depth. A true active-path cycle refuses or recovery-labels the affected invocation without corrupting the caller frame.

### 17.7 Inline images

Inline-image parsing receives a dedicated bounded parser because `EI` termination is context-sensitive and historically error-prone.

The parser considers:

- abbreviated keys and filters;
- expected sample lengths where derivable;
- filter termination;
- surrounding operator syntax;
- bounded candidate search;
- and compatibility profile.

Ambiguity remains visible in the program report.

### 17.8 Compatibility sections

Unknown operators inside `BX`/`EX` sections and outside them are handled according to standard and profile rules.

The VM records whether an unknown operator was ignored, preserved, or treated as an error.

### 17.9 Marked content and logical linkage

The VM emits marked-content stack events with:

- tag;
- property source;
- MCID;
- artifact status;
- ActualText and alternate descriptions;
- structure-owner linkage;
- and source span.

These events feed text and structure views without forcing the renderer to own accessibility semantics.

### 17.10 Optional content

Optional-content visibility is evaluated against a named configuration and usage context.

The result records:

- relevant OCG/OCMD objects;
- configuration;
- event type;
- visibility expression;
- and the decision path.

Hidden content remains discoverable to forensic and redaction workflows.

### 17.11 Functions

The function subsystem supports PDF function types with independent contracts:

- sampled functions;
- exponential interpolation;
- stitching;
- PostScript calculator functions.

Function evaluation is typed by input and output domains, range clipping, and evidence.

### 17.12 Calculator-function VM

The Type 4 VM implements only the language defined for PDF calculator functions.

It has:

- a typed operator table;
- bounded stack;
- bounded procedure nesting;
- bounded instructions;
- no I/O;
- deterministic numeric semantics;
- and a complete execution trace on failure.

It does not embed a general PostScript interpreter.

### 17.13 Display emission

The VM has distinct typed output channels rather than pretending every consequence is paint:

- a `PaintSink` for immediate tiles, provenance-rich display artifacts, or vector appearance export;
- a `SemanticSink` for glyph instances, marked-content events, annotation linkage, and text/structure inputs; and
- an optional bounded `TraceSink` for execution-state transitions and diagnostics.

A fanout coordinator may drive several channels from one ordered execution, but a glyph collector is never implemented as a paint backend and a trace recorder is never allowed to redefine appearance. This preserves the Honeycomb distinction between appearance and semantics while still sharing one operator execution.

Multi-sink execution is not an implicit all-or-nothing accident. Each sink is fallible, metered, and receives the work context. Page sinks are transactional: `begin_page` returns a non-clonable page-transaction object, any error or cancellation explicitly consumes it through `abort`, and only a consuming `commit` makes a page result visible. Dropping an unterminated page transaction prevents normal publication and poisons the page transaction, but cleanup and diagnostic emission are only best effort; an explicit abort is required for an auditable receipt. The fanout policy states whether one sink refusal aborts all sinks, yields a partial multi-result, or allows an independently scoped sink to commit. A diagnostic/text sink hitting its quota cannot silently change paint semantics, and a paint sink failure cannot be presented as complete extraction unless the extraction scope is independent.

---

## 18. Geometry, rasterization, transparency, patterns, and shadings

### 18.1 Geometry primitives

Representation-neutral affine matrices, points/vectors, rectangles, page boxes, source path commands, and finite/conservative-bound primitives live in the foundation `mb-geom` contract because the page VM must construct paths without depending upward on rasterization.

The appearance-level `mb-path` contract owns:

- normalized subpaths;
- winding tests;
- curve flattening;
- stroke outlines;
- clip geometry;
- and conservative device-space bounds after the rendering request is known.

Neither contract knows PDF objects or resource dictionaries. The page VM may depend on `mb-geom`; only appearance code depends on `mb-path`, raster, and compositing.

### 18.2 Numeric policy

Source and user-space coordinates are represented in `f64` after exact token parsing where possible.

Device-space coverage uses a deterministic fixed-point or integer grid where that materially improves cross-platform stability.

Every conversion checks:

- finite values;
- overflow;
- degenerate matrices;
- and coordinate magnitudes against limits.

Before fixed-point conversion, geometry is clipped or translated into a bounded tile-local coordinate frame. Saturating a huge coordinate into an integer and continuing is not a correctness strategy; overflow produces a typed refusal or a conservative clipped result under an explicit degraded profile.

### 18.2.1 Raster-profile boundary

The standard defines document semantics but leaves implementation details of rendering and conformance validation open. MonkeyBee therefore publishes named raster profiles. A profile fixes at minimum:

- page/annotation intent and selected page box;
- pixel-center and coverage conventions;
- antialiasing and sampling;
- hairline and stroke-adjustment policy;
- font resolver and hinting policy;
- image interpolation;
- color/output profile and black-point policy;
- overprint/separation behavior;
- optional-content event;
- and numerical tolerance/determinism class.

“Faithful” means faithful within that declared envelope, not pixel-identical to every conforming processor.

### 18.3 Path construction

Path construction implements:

- move, line, cubic Bézier, close;
- rectangle shorthand;
- current-point rules;
- subpath handling;
- and malformed-sequence diagnostics.

Paths retain source-node lineage per segment.

### 18.4 Curve flattening

Flattening uses an error-bounded adaptive algorithm parameterized by device transform and flatness.

The receipt records the tolerance and maximum recursion or work.

Curves that exceed limits are refused or conservatively approximated only under an explicit degraded-render profile.

### 18.5 Fill rasterization

The primary rasterizer is tile-based and supports:

- nonzero winding;
- even-odd winding;
- anti-aliased coverage;
- clipping intersection;
- large-coordinate robustness;
- and deterministic edge ordering.

An independently implemented slow reference rasterizer is retained as a test oracle.

### 18.6 Stroke semantics

Stroke expansion covers:

- line width including hairlines;
- cap and join styles;
- miter limits;
- dash arrays and phase;
- closed-subpath behavior;
- transformed pen geometry;
- and stroke adjustment profiles.

Analytic and metamorphic tests include rotations, reflections, scale changes, degenerate segments, and dash wraparound.

### 18.7 Clipping

Clips are represented in a form suitable for:

- exact stack semantics;
- conservative bounds;
- tile rejection;
- and provenance.

The implementation may choose mask, edge, or region representations adaptively, but changes in representation must not change semantics beyond the declared raster envelope.

### 18.8 Compositing

The compositing engine may store premultiplied internal samples, but PDF blend functions are evaluated with the required unassociated components in the declared blending color space and then converted back with explicit shape/opacity bookkeeping. Premultiplication is a storage/optimization choice, not a different blend algebra.

It supports:

- normal and separable blend modes;
- nonseparable blend modes;
- alpha constants;
- shape and opacity distinction;
- isolated groups;
- knockout groups;
- transparency group color spaces;
- soft masks;
- backdrop initialization;
- and matte handling.

Each group boundary emits a trace node.

Page-level transparency groups, annotation appearance compositing, text knockout, nonseparable blend color-space selection, and the interaction of shape/opacity are independent atomic test families. An RGB-only path cannot claim correct DeviceN/spot-color group behavior.

### 18.9 Soft masks

Soft-mask evaluation records:

- source group;
- alpha-versus-luminosity mode;
- transfer function;
- backdrop;
- color space;
- effective Form/group transform and placement context;
- and cache identity.

Recursive soft-mask cycles are detected and refused.

### 18.10 Overprint and process separations

Overprint behavior is evaluated in a colorant-aware intermediate representation when the output profile requires it.

A simple RGB renderer may not claim print-faithful overprint.

The render report states whether:

- overprint was simulated;
- process and spot colorants were preserved;
- or a display approximation was used.

### 18.11 Tiling patterns

Pattern support includes:

- colored and uncolored tiling patterns;
- pattern matrices;
- bounding boxes;
- step values;
- paint types and tiling types;
- nested resources;
- recursion detection;
- and tile-cache limits.

Sampling origin and repetition are deterministic under a profile.

### 18.12 Shading patterns and shadings

The shading engine supports PDF shading types 1 through 7: function-based, axial, radial, free-form Gouraud triangle mesh, lattice-form Gouraud triangle mesh, Coons patch mesh, and tensor-product patch mesh.

Mesh shadings use a dedicated bit-packed parser for coordinate/component bit widths, decode arrays, vertex flags, shared-edge/patch continuation, and bounded record counts. They retain patch/vertex provenance and use bounded subdivision or direct evaluation with an error metric. Malformed flags or truncated packed data are recovery hypotheses or refusals, never silently padded geometry.

A shading result states:

- tessellation tolerance;
- function evidence;
- color-space transform;
- and any malformed-data recovery.

### 18.13 Reference rendering path

A correctness-first reference path exists for small fixtures.

It favors simple algorithms and high observability over speed. Optimized paths must match it within declared envelopes and carry the same semantic trace.

### 18.14 Appearance kill criteria

An optimization is not promoted when it:

- loses source traceability;
- changes output outside the profile envelope;
- cannot be cancellation-bounded;
- or introduces a platform-specific path without an independent oracle.


---

## 19. Color management and image semantics

### 19.1 Color is profile-dependent computation

A PDF color value is not an RGB tuple until a declared output pipeline makes it one.

The color layer separates:

- source color space;
- source component values;
- tint and transfer functions;
- blending color space;
- output intent;
- target profile;
- rendering intent;
- black-point behavior;
- overprint state;
- and final device encoding.

### 19.2 Color-space types

The core supports typed variants for:

- DeviceGray;
- DeviceRGB;
- DeviceCMYK;
- CalGray;
- CalRGB;
- Lab;
- ICCBased;
- Indexed;
- Separation;
- DeviceN, including `/Subtype /NChannel` attributes where the registered standard/profile defines them;
- Pattern;
- and default-device-space substitutions.

Color-space construction is fallible and validates component counts, ranges, alternate spaces, and recursive references.

### 19.3 Device spaces

Device spaces are interpreted only through a declared profile.

Examples:

- a screen-preview profile may map DeviceCMYK through a documented display approximation;
- a print-simulation profile may preserve process and spot colorants;
- an archival-check profile may refuse to claim appearance without required output intent information.

The same source value can therefore have multiple valid derived appearances with separate receipts.

### 19.4 Calibrated spaces

CalGray, CalRGB, and Lab implement:

- white and black points;
- gamma;
- matrices;
- ranges;
- and conversion into the selected profile connection space.

Invalid calibration values fail closed or enter a named recovery path.

### 19.5 ICC profiles [F]

The ICC subsystem parses and validates relevant profile classes, tag tables, and transforms under strict byte and complexity limits.

The implementation plan proceeds in rungs:

1. matrix/TRC display profiles;
2. common RGB and CMYK LUT profiles;
3. multidimensional interpolation and intent handling;
4. named-color and device-link cases needed by PDF workflows;
5. independently checked print-oriented coverage.

A generic pure-Rust ICC implementation may be used after audit. Otherwise, MonkeyBee implements the necessary subset behind a contract and expands through held-out profiles.

No release claims full print fidelity until the profile corpus and device/RIP comparisons justify it.

### 19.6 Indexed spaces

Indexed lookup tables preserve exact bytes and support:

- string or stream sources;
- high-value bounds;
- base color-space conversion;
- sample clamping;
- and malformed table-length diagnostics.

### 19.7 Separation and DeviceN

Spot and multichannel spaces retain colorant names and tint-transform provenance.

The renderer can produce:

- a display approximation through the alternate space;
- a colorant-preserving intermediate surface;
- and per-separation output for print analysis.

It records when a tint transform or alternate space is malformed or incomplete.

### 19.8 Device-dependent controls and rendering intents

The graphics/color model represents:

- `DefaultGray`, `DefaultRGB`, and `DefaultCMYK` substitutions;
- rendering intents;
- transfer functions (`TR`/`TR2`);
- black generation (`BG`/`BG2`);
- undercolor removal (`UCR`/`UCR2`);
- halftone dictionaries and transfer behavior;
- smoothness tolerance (`SM`) and whether the selected device profile honors, clamps, or ignores it;
- overprint and overprint mode (`OP`, `op`, `OPM`);
- spot colorants including reserved `All` and `None` semantics;
- DeviceN attributes, including NChannel subtype data and mixing hints;
- output intents and profile selection;
- and black-point compensation where the registered specification/profile defines it.

A display renderer may model, approximate, or refuse device-dependent controls according to its profile. Unsupported print effects become explicit no-claims rather than ignored trivia.

### 19.9 Image XObjects

The image layer interprets:

- dimensions;
- bits per component;
- color space;
- decode arrays;
- interpolation;
- image masks;
- explicit masks;
- soft masks;
- matte values;
- alternate images;
- metadata;
- and optional-content association.

It also records image-structure features that can alter interpretation, including JPX embedded color/alpha, `SMaskInData`, explicit alternates, external-file streams, intent-specific alternate images, thumbnails, and object/revision provenance.

Alternate-image selection is a usage-context decision with an explicit fallback chain. The engine records which alternate, default image, or refusal was selected for `View`, `Print`, or `Export`; it never decodes all alternates and silently chooses whichever succeeded.

Dimension products are checked before allocation.

### 19.10 Sample pipeline

There is no one universal linear image pipeline. MonkeyBee builds a typed image-evaluation plan from the XObject kind, filter/codec metadata, `ImageMask`, `Mask`, `SMask`, `SMaskInData`, `Matte`, `Decode`, interpolation, alternate-image selection, color space, transparency-group context, and output profile.

The plan distinguishes at least:

```text
source bytes -> decrypt/filter/codec -> raw packed samples -> unpacked source samples
                              |                         |
                              |                         +-> Decode mapping / stencil semantics
                              +-> codec color/alpha metadata and admitted overrides

source/color samples + color-key or explicit-mask semantics
 -> source color evaluation / colorant preservation
 -> interpolation in the profile-defined sample domain
 -> soft-mask or embedded-alpha evaluation (including matte/unpremultiply rules)
 -> compositing input
```

The exact branch and ordering are specification/profile facts for that image form, not an optimizer’s preference. Raw samples, decoded component values, mask-comparison values, color-converted values, and final premultiplied pixels remain distinct trace nodes. Every branch is independently budgeted and atomically tested.

### 19.11 Decode arrays

Decode arrays are interpreted per component, including reversed ranges and image-mask defaults.

The raw samples and decoded component values remain distinguishable for explanation and round-trip work.

### 19.12 Masks

The engine distinguishes:

- stencil image masks;
- color-key masks;
- explicit image masks;
- soft masks;
- JPX alpha data;
- and transparency groups used as masks.

Mask composition order is contract-tested with atomic fixtures.

### 19.13 Interpolation

The profile records interpolation policy.

The reference renderer implements at least nearest and bilinear paths with exact edge behavior. Higher-quality resampling is optional and cannot alter the compatibility profile’s declared semantics without a distinct profile.

### 19.14 Image caching

Image cache keys include:

- object version;
- decode parameters;
- security context;
- color profile;
- target resolution or scale class;
- interpolation policy;
- and relevant mask state.

A decoded sample cache and a transformed-tile cache are separate so multiple output profiles do not cross-contaminate.

### 19.15 Image and color falsifiers

Independent checks include:

- analytic ramps and patch charts;
- known ICC reference values;
- codec round trips where valid;
- external renderer comparisons;
- per-channel separation tests;
- metamorphic scaling and cropping;
- and print/RIP comparisons for claims about print behavior.

---

## 20. Fonts, CMaps, glyph execution, and text semantics

### 20.1 Four separate questions

For every text-showing operation MonkeyBee distinguishes:

1. Which source character-code bytes were consumed?
2. Which CID or glyph identifier was selected?
3. Which outline and metrics were used to paint?
4. Which semantic character or text sequence can be justified?

Many PDFs answer only some of these questions.

### 20.2 Font resource model

A font resource contains references to:

- PDF font dictionary and descendants;
- encoding or CMap;
- widths and vertical metrics;
- font descriptor;
- embedded font program;
- `ToUnicode` CMap;
- substitution profile;
- and cache identity.

Font loading is lazy and budgeted. `mb-pagevm` sees only the lower-boundary `FontExecutionService` protocol; the higher font orchestrator and format crates implement it. No format crate calls back into the page VM. Type 3 selection produces a source-linked procedure descriptor that the VM executes, while ordinary fonts produce bounded outline/metrics descriptors.

Composite-font state explicitly includes `CIDSystemInfo`, `CIDToGIDMap`, `DW`/`W`, `DW2`/`W2`, writing mode, descendant subtype, and predefined-CMap identity. Vertical origin/displacement and CID-to-glyph selection are not inferred from horizontal metrics.

### 20.3 Supported font families

The declared target includes:

- Type 1 fonts;
- Type 1 Multiple Master data needed for compatibility;
- CFF Type 1C;
- TrueType and OpenType with TrueType outlines;
- OpenType with CFF/CFF2 where applicable to PDF embedding;
- Type 0 composite fonts;
- CIDFontType0 and CIDFontType2;
- Type 3 fonts;
- and standardized base-font behavior under explicit substitution profiles.

### 20.4 Simple-font encodings

Simple fonts support:

- standard and predefined encodings;
- font-specific encodings;
- Differences arrays;
- glyph-name interpretation;
- symbolic-font behavior;
- and source-preserving invalid entries.

Encoding selection is not conflated with Unicode extraction.

### 20.5 CMaps

The CMap subsystem supports:

- codespace ranges;
- character-code to CID mappings;
- notdef mappings;
- usecmap inheritance;
- vertical writing mode;
- `ToUnicode` mappings;
- range expansion under limits;
- and predefined CMaps from legally distributable sources.

It parses the CMap language through a bounded dedicated interpreter, not the Type 4 calculator VM and not a general PostScript VM. Lexical utilities may be shared only where token semantics are identical. `usecmap` resolution is snapshot-bound and cycle-safe: the resolver maintains a visited identity set, enforces depth and aggregate-entry budgets, rejects or recovery-labels cycles, and records the exact inherited CMap chain in provenance. Predefined CMap identity includes the rights-cleared data-pack version so a cache entry cannot survive a silent mapping update.

### 20.6 Variable-length character codes

Character-code tokenization follows CMap codespaces and retains exact byte spans.

Ambiguous or malformed codespaces produce explicit alternatives or refusals. The text-showing loop cannot simply consume one or two bytes by assumption.

### 20.7 Type 1 and Type 2 charstrings

Charstring interpreters share the embedded-program sandbox contract.

They support:

- subroutines;
- hint operators;
- flex behavior;
- width extraction;
- composite/seac behavior where required;
- bounded stack and call depth;
- deterministic path output;
- and full error traces.

The outline is a derived artifact linked to the exact charstring bytes.

### 20.8 TrueType and OpenType parsing

The parser validates:

- sfnt directory;
- checksums where meaningful;
- table bounds and overlap;
- glyph locations;
- contours and composites;
- cmap tables;
- metrics;
- naming;
- OS/2 and post metadata needed for PDF behavior;
- variations if encountered;
- and embedded-subset naming.

Composite-glyph cycles and point-count explosions are bounded.

OpenType variation tables, CFF2 programs, COLR/SVG/bitmap tables, or other non-core font technology are parsed under bounds and admitted for rendering/embedding only when a registered PDF standard or extension profile defines their use. Encountering such tables is not by itself permission to interpret them as a valid PDF font program.

### 20.9 TrueType hinting [F]

The hinting VM is isolated and metered.

Development proceeds in stages:

1. correct unhinted outlines and metrics;
2. grayscale raster quality sufficient for high-resolution rendering;
3. bounded TrueType instruction execution;
4. compatibility testing across ppem ranges;
5. optional platform-profile behavior where justified.

Until stage 3 passes, low-resolution pixel fidelity claims identify hinting as a known gap.

### 20.10 Type 3 fonts

Type 3 glyphs execute through the page-program VM with:

- font matrix;
- glyph procedure resources;
- colorized versus uncolored behavior;
- width and bounding-box operators;
- recursion limits;
- and glyph-instance provenance.

A Type 3 glyph may emit arbitrary page-appearance primitives; it is not reduced to an outline by assumption.

### 20.11 Widths and positioning

Text layout uses PDF text-state rules and records:

- source widths;
- font-program widths;
- PDF width overrides;
- character and word spacing;
- horizontal scaling;
- rise;
- text matrices;
- TJ adjustments;
- writing mode;
- and final device positions.

Mismatch between font-program and PDF-declared metrics is preserved as a diagnostic and compatibility choice.

### 20.11.1 Text rendering modes and clipping

The page VM implements `Tr` modes 0 through 7 as distinct semantics: fill, stroke, fill-then-stroke, invisible, and the four corresponding clipping variants. Invisible text still advances text state and remains visible to text, structure, provenance, optional-content, and security analysis even though it paints no pixels. Modes 4 through 7 accumulate glyph outlines into the text clipping path; that accumulated text clip is applied to the current clipping path at the standard-defined end of the text object rather than eagerly after each glyph. Fill/stroke colors, line state, glyph procedures, and clipping provenance remain separately traceable, including Type 3-specific behavior.

Character spacing applies according to the text-state rules. Word spacing is not a Unicode-space heuristic: it applies only to the single-byte character code 32 in the circumstances defined by the active simple or composite encoding. A multibyte code that maps to U+0020 does not acquire word spacing merely because later Unicode extraction calls it a space. Atomic fixtures cover all eight modes, clipping interaction with subsequent content, vertical writing, `TJ` adjustments, and malformed text objects.

### 20.12 Base-font substitution

A missing embedded font creates an unavoidable environment dependency.

MonkeyBee defines named substitution profiles:

- no substitution: refuse outline-dependent rendering;
- host-supplied font resolver;
- project-distributed metrically chosen fallback pack, subject to licensing;
- and compatibility-specific resolvers.

Every substituted glyph is labeled. Standard base-font metrics and substitute outlines are separate claims: a profile may preserve nominal advances while still producing profile-dependent pixels. Text extraction from source mappings remains separate from substituted appearance.

### 20.13 Claim-specific Unicode and replacement-text evidence

There is no one global Unicode ladder. Different questions have different authorities:

- source-code-to-Unicode mapping for a font normally consults valid `ToUnicode`, registered character collections/predefined CMaps, encoding/glyph-name rules, and justified font cmap evidence;
- `ActualText` or structure-associated replacement text may define the intended replacement for a marked-content sequence even when it does not describe each painted glyph individually;
- OCR or language-model inference is an external heuristic over appearance and can never rewrite source-encoded text facts;
- conflicts among valid sources remain explicit and are resolved only by the request profile and scope.

Each candidate records source, byte/structure span, algorithm/version, language/script assumptions, and conflict relationships. Extraction APIs distinguish `PaintedGlyphText`, `ReplacementText`, `AccessibilityText`, and `SearchText` rather than collapsing them into one string.

Extraction preserves the original justified Unicode scalar sequence. NFC/NFKC, compatibility folding, case folding, whitespace folding, hyphen repair, and search normalization are optional derived views with named Unicode-data versions and reversible mappings where possible; they never overwrite source/replacement-text claims. Ill-formed surrogate-like or noncharacter situations are represented according to the exact source/profile policy rather than silently repaired by the host string type.

### 20.14 Text extraction graph

The extractor emits glyph-level nodes containing:

- source code bytes;
- font and CMap identities;
- CID/glyph ID;
- Unicode candidates;
- geometric quadrilateral;
- baseline and writing direction;
- marked-content and structure links;
- visibility state;
- and evidence.

Words, lines, blocks, and reading order are derived layers.

### 20.15 Reading order [F]

Reading order is not determined solely by painting order.

MonkeyBee combines, in decreasing authority:

- valid tagged structure and its explicit kid/content-item order;
- marked-content and MCID relationships;
- geometric clustering;
- writing-direction and baseline analysis;
- column and region segmentation;
- and optional external semantic inference.

`ActualText` contributes replacement text inside the marked-content or structure scope to which it applies; it does not by itself order unrelated regions on a page. The result is a graph or ranked alternatives when order is ambiguous.

Within a line or structure region, bidirectional ordering and mirrored/vertical presentation are versioned derived analyses, separate from paint order and source code order. The extractor records whether it returned logical order, visual order, tagged order, or a search-oriented normalized order; a single unlabeled “text string” is not the public truth.

### 20.16 OCR boundary

OCR is not part of the core PDF semantics.

An optional adapter may attach OCR hypotheses to image regions. Those hypotheses are external and heuristic, never confused with text encoded by the PDF.

### 20.17 Font subsetting

The writer’s subsetter preserves:

- required composite components;
- encoding/CID relationships;
- metrics;
- naming conventions;
- `ToUnicode` generation;
- and embedding restrictions.

Subsetting is verified by reopening the output, rendering glyph fixtures, and checking text mappings in independent consumers.

### 20.18 Font and text flagships

The font battery includes:

- mixed one- and two-byte CMaps;
- vertical Japanese text;
- ligatures and glyph-name mappings;
- missing `ToUnicode`;
- malformed cmap tables;
- composite TrueType cycles;
- Type 3 colored glyphs;
- CFF subroutines;
- base-font substitution;
- and invisible or clipped text relevant to redaction.

---

## 21. Logical structure, accessibility, annotations, forms, and document navigation

### 21.1 Tagged-document model

The structure layer models:

- `StructTreeRoot`;
- structure elements;
- kids as elements, marked-content references, and object references;
- parent tree;
- role map;
- class map;
- namespaces;
- ID tree;
- attributes;
- pronunciation-related structure attributes including `PhoneticAlphabet` and `Phoneme`;
- language;
- alternate and expanded text;
- page-level `/Tabs` ordering declarations as linked evidence rather than inferred reading-order truth;
- and revision provenance.

### 21.2 Structure-to-appearance linkage

The engine verifies relationships among:

- page marked-content sequences;
- MCIDs;
- structure parents;
- parent-tree entries;
- annotation structure parents;
- and structure-element kids.

Broken links are localized in both trees and page programs.

### 21.3 Accessibility evidence

MonkeyBee can validate structural rules and report semantic gaps, but it does not claim that automation alone can prove a document is meaningful or usable.

Examples:

- it can prove an image lacks alternate text;
- it cannot prove supplied alternate text is good merely because it exists;
- it can detect heading-level irregularities;
- it cannot infer authorial intent with normative certainty;
- it can validate table-structure relationships;
- it cannot always determine whether the table’s reading order is semantically correct.

Reports distinguish machine-verifiable rules from human-review requirements.

### 21.4 Standardized accessibility profiles

PDF/UA profiles are versioned, independently sourced, and run as explicit validation layers.

Profile support is released only when:

- rule coverage is enumerated;
- unsupported rules are visible;
- atomic corpus tests pass;
- and an independent validator comparison has been run.

### 21.5 Annotations

Annotation support has two deliberately separate products.

The **structural annotation model**, available to R0 inspection without a renderer, includes:

- subtype-specific dictionaries;
- rectangles and quadrilaterals;
- exact appearance-stream references without executing them;
- actions and destinations;
- border and color declarations;
- popup relationships;
- replies and review states;
- file attachments;
- redaction annotations as intent rather than completed redaction;
- and optional-content association.

The **annotation appearance adapter**, admitted only once the page VM and appearance core exist, evaluates valid appearance streams under the standard/profile rules. It selects normal/rollover/down appearance and appearance state from `/AP`, `/AS`, field/widget state, and the request's interaction profile; maps the appearance stream's `BBox` and `Matrix` into the annotation `Rect`; and applies page rotation, annotation flags, `NoZoom`/`NoRotate`, visibility/print intent, optional-content state, and border/appearance-characteristics policy as distinct decisions with provenance. A malformed or missing appearance is not silently replaced by the annotation dictionary's color/border fields.

Named fallback policies may synthesize an appearance only when the subtype policy, font/resource capabilities, dynamic-state boundary, and no-claim language are explicit. Synthesized and source-supplied appearances have different origins and cache identities. Navigation, attachment inventory, and R0 security inspection must never depend transitively on appearance rendering.

### 21.6 Destinations and navigation

The document model resolves:

- explicit destinations;
- named destinations;
- outlines;
- links;
- page labels;
- article threads where encountered;
- and open actions.

Broken destinations retain source references and diagnostics.

### 21.7 AcroForm as data

Initial form support includes:

- field hierarchy;
- widget annotations;
- values and defaults;
- appearance streams;
- calculation order inventory;
- flags;
- resources;
- and signature fields.

MonkeyBee may render and edit field values through explicit APIs.

It does not execute arbitrary JavaScript or XFA behavior in the initial envelope.

### 21.7.1 Dynamic-form state boundary

Stored field values, existing appearance streams, default appearances, `NeedAppearances`, catalog `NeedsRendering`, calculation/format/validate actions, XFA state, and host-script results are distinct. MonkeyBee may:

- display a valid existing appearance;
- generate a policy-defined appearance from a declared stored value;
- compute a new field-state candidate under Bet 16’s admitted metered calculate/format/validate tenant; or
- refuse to claim that the result matches the intended current form state.

The metered outcome binds the exact selected field graph, event manifest and order, script/action identities, deny-by-default built-ins, supplied locale/time/clock/format inputs, typed read set, event-specific write set, cycle/event-storm handling, resource charges, termination, and entire effect journal. The entire field-state transition commits atomically. A script failure, cancellation, budget exhaustion, or unsupported API publishes no partial field update. Keystroke, focus, UI, navigation, submission, application-level, general document, dynamic-code-generation, and ambient host APIs remain excluded unless a future separately admitted tenant says otherwise.

Widget/button appearance state, export values, choice options/indices, rich-text values, default resources, locks, and dependencies remain separate. Editing one stored value does not assert that calculated fields, formatted text, button state, XFA state, or appearances are current. Flattening never implies unsupported dynamic logic ran.

### 21.8 Form appearance generation

The semantics layer defines the dynamic-state/appearance policy and selects existing appearance evidence; actual appearance-stream construction lives in the authoring/transform layer so document semantics never depend upward on the writer.

When requested, appearance generation uses a versioned policy and records:

- field semantics;
- font resolver;
- text layout;
- clipping;
- border/background behavior;
- and compatibility targets.

Existing appearances are preserved in source-preserving mode unless the edit requires regeneration.

### 21.9 XFA

XFA packets are always inventoried, safely extracted, preserved or removed by policy, and structurally parsed only through bounded XML machinery with external entities and ambient I/O disabled.

Bet 16 admits a separately named **static projection** capability: a rights-reviewed, bounded subset may map selected XFA template/data/layout constructs into fixed-page appearance and transformation artifacts. Static projection does not execute a general XFA runtime, network/data connection, dynamic event system, arbitrary script environment, or interactive relayout engine. The output records the packet revision, data binding, admitted construct set, layout profile, fonts/locale, every ignored or approximated construct, and fixed-page provenance. Unsupported dynamic behavior, unresolved binding, pagination/layout ambiguity, script dependence, or resource exhaustion yields a no-claim region or refusal rather than plausible-looking completion.

XFA-to-AcroForm conversion and general interactive XFA behavior remain future transformations. Open decision 3 governs how deep the static subset may become.

### 21.10 Optional content and visibility semantics

Optional-content groups and membership dictionaries are linked to:

- page primitives;
- annotations;
- XObjects;
- and structure nodes.

Forensic workflows can request all content regardless of current state, a symbolic visibility formula, or a bounded enumeration of selected configurations. Because the configuration space can be exponential, hitting the bound returns partial coverage rather than claiming that every visibility state was exhaustively enumerated.

### 21.11 Metadata

The metadata layer preserves and reconciles:

- document information dictionary;
- XMP packets;
- dates and identifiers;
- language;
- output-intent metadata;
- and application-specific extension data.

Conflicts are reported, not silently merged.

### 21.12 Associated and embedded files

Associated files are represented with:

- relationship type;
- file specification;
- embedded stream;
- checksum and size metadata;
- MIME information;
- encryption context;
- revision introduction;
- and structure or annotation links.

Security reports include files reachable only through orphaned or historical objects.

Embedded payload bytes are opaque by default: filenames, MIME types, checksums, and extensions are untrusted metadata. Optional nested-inspection adapters may sniff and inspect PDFs, archives, office formats, or malware under explicit format capabilities, recursion depth, cumulative decoded-byte, time, and privacy budgets. A report that did not run such adapters makes no claim about active content or secrets inside the payload.

Portfolios/Collections and collection schemas, package navigation data, article threads, presentation transitions and navigation steps, renditions/media clips, 3D/RichMedia objects, alternate presentations, web-capture/spider information, page templates, document-part hierarchy, OPI/private production data, page-piece dictionaries, trapping/separation information, geospatial/measurement data, requirements/extension declarations, and proprietary extension dictionaries receive at least preserve-and-inventory support through the rare-document preserve-and-inventory envelope before the reader claims broad document coverage. FDF/XFDF import/export and dynamic interaction are separate future envelopes.

---

## 22. Writing, generation, structured authoring, and layout

### 22.0 Authoring roots are not parsed-document roots

Generation begins from a typed `DraftRoot`, not a fake empty `DocumentReality` with invented byte spans. Caller-supplied intent, assets, explicit COS/page-program content, and explicit positioned layout decisions receive first-class `Draft` origins bound to stable nodes in that frozen draft. Incidental implementation choices made while realizing structured intent are derivations, not retroactive author intent.

A Level-1/Level-2 draft whose positioned semantics are all explicit may proceed directly to a validated write plan. Level-3 structured layout, automatic pagination, inferred structure, candidate optimization, or any other process that materially derives a concrete semantic document first finalizes a `TransformRoot` with the `DraftRoot` as an input and records the exact derivation. Transform-created objects use `Derived` origins: genuine rewrites/imports name rooted parents, while admitted authoring-class operations use `DerivationBasis::Authored` rather than inventing one. Serialization creates a `SourceRoot` plus an exhaustive mapping from the actual semantic input root—Draft or Transform—to bytes and object occurrences. Editing an existing source likewise creates a `TransformRoot` that may later serialize into a new source lineage.

### 22.1 Three authoring levels

MonkeyBee exposes three deliberate levels.

#### Level 1 — COS construction

For experts who need exact object control.

The API is typed but close to PDF objects. It requires the caller to manage semantic correctness explicitly.

#### Level 2 — PDF graphics and document construction

A safe canvas and document builder for:

- pages;
- paths;
- text;
- images;
- resources;
- annotations;
- outlines;
- metadata;
- attachments;
- and structure tags.

This level emits correct resource relationships and balanced content programs by construction.

#### Level 3 — Structured authoring

A layout-oriented model for:

- paragraphs;
- spans;
- headings;
- lists;
- tables;
- figures;
- links;
- page templates;
- and tagged-document structure.

This is not initially a full word processor. It is a deterministic document compiler for bounded, inspectable layouts.

The bounded layout envelope names its pagination features and no-claims: widow/orphan handling, footnotes, floats, complex tables, cross-references, hyphenation, page-template balancing, and script-specific line breaking are supported only when present in the selected layout profile. Unsupported layout constructs refuse or require caller-positioned primitives; they are not approximated into an apparently polished but semantically different document.

### 22.2 Writer invariants

The writer guarantees within its declared mode:

- no dangling indirect references;
- valid xref and trailer structures;
- correct stream lengths;
- deterministic object order and IDs where promised;
- balanced page programs;
- valid resource references;
- bounded output;
- and strict re-openability by MonkeyBee.

External interoperability is a separate gate.

Writer admission is capability-typed. Raw COS construction can produce an inspection artifact, but only `ValidatedWritePlan` can publish a release PDF. Validation includes target-version legality, profile restrictions, extension declarations, unknown-object policy, encryption/entropy policy, and signature-impact policy.

### 22.3 Object allocation and trailer identity

Canonical writing uses deterministic object allocation based on a stable traversal and object-class ordering. Free-entry/generation-number semantics, object-number limits, generation rollover, and whether freed numbers may be reused are defined by the target-version/profile contract rather than ad hoc allocation.

PDF object references may contain cycles. Stable traversal therefore operates over a canonical strongly connected-component condensation, using ordered semantics where order matters and equivalence classes with multiplicity where nodes are genuinely indistinguishable. The semantic-canonical writer expands a symmetry class through a versioned quotient-graph serialization rule; generated object numbers are serialization positions, not durable semantic member identities. A provenance-preserving or history-sensitive writer may instead bind source/draft/origin anchors from the exact `RealityRoot`. It never introduces meaning or public identity merely to order indistinguishable nodes, and it refuses only when the selected output profile requires an identity distinction for which no admissible semantic or provenance anchor exists.

`generated-echo: constitution/MONKEYBEE_CONSTITUTION_v8.md §11.2.3`

Canonical SCC refinement and labeling have graph-isomorphism-class worst cases. Every refinement, partition branch, canonical comparison, symmetry class, multiplicity, and output expansion is charged to the canonicalization/symmetry work budget; exhaustion yields a typed weaker outcome or refusal, never traversal-order canonicalization.

Source-preserving incremental writing retains existing object numbers and allocates new IDs through a deterministic collision-free policy. It preserves or updates trailer `/ID` values according to the applicable standard, encryption, signature, and profile semantics; it never treats file identifiers as decorative random strings. For new unencrypted deterministic documents, identifier derivation is versioned and domain-separated. For encryption profiles, identifier and entropy requirements follow the secure construction and normally break byte identity. Signature profiles follow their algorithm-, signed-attribute-, time-, and service-specific determinism contract; they may be D1 or D1R rather than being classified by slogan.

### 22.4 Serialization modes

#### Canonical mode

- one declared PDF version and extension/profile set;
- explicit policy for malformed duplicate keys, unknown extensions, unexplained bytes, and encrypted inputs;
- normalized lexical forms under a versioned numeric/name/string grammar;
- deterministic project-policy dictionary ordering where the standard does not prescribe order;
- deterministic stream encoding parameters for unencrypted deterministic profiles;
- optional object streams and xref streams only when version/profile permits;
- garbage collection of unreachable objects;
- no historical revisions unless explicitly embedded as evidence;
- and byte-identical output for identical `SemanticStateId` only when its `SemanticScopeId` is serialization-total for the selected semantic-canonical profile, all assets are available, and writer/dependency versions are pinned. A serialization-total scope enumerates every meaning axis and meaning-changing dialect/profile/recovery choice that can affect emitted bytes; omission of any such axis makes the byte-identity claim unavailable. A separate provenance-bearing canonical profile may intentionally bind `RealityStateCommitment` and therefore differ for semantically equal documents with different histories; the profile name and receipt make that distinction explicit.

Secure encryption uses scheme-required fresh/unique material and therefore normally has a reproducibility receipt rather than byte identity. Future signature creation is classified separately: approved deterministic profiles may claim D1 only under the fully pinned contract in §§11.9 and 16.1.1; randomized, hedged, timestamped, revocation-dependent, or mutable-service profiles are D1R.

#### Preservation mode

- unchanged source bytes retained exactly;
- new incremental revision appended;
- modified objects emitted as new versions;
- previous xref and trailer history retained;
- signature effects computed before commit;
- and unexplained bytes preserved.

For encrypted inputs, new encrypted strings/streams use the applicable security handler and fresh entropy **only when the secure-output writer profile is present**; otherwise encrypted incremental editing is refused before publication. Preservation mode never promises byte-identical appended encrypted revisions. Any existing linearization becomes stale after an ordinary append and is reported as such unless a separate full linearized rewrite is performed.

### 22.5 Compression

Compression policies are named and deterministic.

They specify:

- eligible stream classes;
- filter chain;
- compression level;
- predictor choice;
- object-stream grouping;
- and compatibility exclusions.

“Optimize” is not one magical flag.

The R2 core writer does not silently require every decoder to have a matching encoder. Raw admitted image samples can be emitted through Flate/predictor policies; validated already-compressed assets such as JPEG may be embedded without lossy transcode when their exact bytes and PDF metadata are compatible. JPEG/CCITT/JPX/JBIG2 re-encoding is capability- and dependency-specific, never inferred from the existence of a decoder, and every lossy conversion carries an explicit quality/color/evidence receipt.

Canonical number formatting is not delegated to a generic shortest-float formatter. The writer defines a bounded PDF decimal grammar, exact integer preservation, finite-value admission, round-trip requirements to the chosen semantic numeric domain, maximum token length, and external-reader tests. Malformed lexical distinctions are preserved only in preservation mode or converted under an explicit repair policy.

### 22.6 Cross-reference strategy

The writer supports classic xrefs and xref streams according to target version/profile.

Hybrid output is generated only when a named compatibility profile requires it.

### 22.7 Object streams

Object-stream grouping accounts for:

- object eligibility;
- locality;
- incremental-update constraints;
- signature workflow;
- random-access cost;
- and deterministic grouping.

### 22.8 Linearization [F]

Linearized output is a later feature because correctness requires precise ordering, hint streams, lengths, and interoperability.

It ships only after:

- progressive-fetch tests;
- multiple external-reader checks;
- deterministic layout;
- and byte-range/signature interactions are understood.

### 22.9 Text shaping and layout

PDF itself does not provide a general-purpose authoring text-layout system.

MonkeyBee defines a shaping adapter for Unicode text, script, language, direction, font selection, features, and variation coordinates. A complete layout profile pins Unicode and rights-cleared conformance-data versions, normalization policy, script/language itemization, bidirectional algorithm and tailoring, grapheme/cluster handling, line breaking and tailoring, hyphenation data, fallback order, vertical-layout policy, shaping engine/version, font bytes, and measurement rules. No source string is silently normalized.

R2 may initially support caller-supplied shaped runs plus a narrower Latin/common-script paragraph profile. Multiscript paragraphs, language-specific line-breaking tailoring, complex tables, equations, footnotes, floats, advanced pagination, and vertical composition are promoted only after their algorithms, failure behavior, and tagged-output mapping are explicit. Shaping output becomes explicit glyph/CID placement, cluster mappings, replacement text where justified, and `ToUnicode` mappings.

MonkeyBee owns the semantic contract and conformance suite for UAX #14 line breaking, UAX #29 segmentation, and UAX #9 bidirectional ordering. Project-owned implementations are preferred for compression and observability, but an audited implementation may satisfy the contract if its exact data/version, tailoring, tests, and determinism are pinned. A measurement module separates expensive preparation from width-dependent layout arithmetic. Exact embedded font metrics are used when present and valid; substitution, missing programs, synthetic metrics, and host-dependent shaping remain visible profile facts rather than “exact by construction.”

The shaping system is an authoring dependency and does not reinterpret already encoded source-PDF text, except when creating a declared Workflow N presentation derivative. Such a derivative is outside extraction and canonical-semantics claims, binds its source glyph/text/structure evidence and reading-order hypothesis, and assigns each region a fidelity class. Tables, equations, figures, forms, uncertain blocks, complex vertical/bidirectional regions, and other unsupported structures may remain fixed-layout islands or be refused. No flowing layout is invented merely to avoid an honest no-claim.

### 22.10 Font embedding

The generator embeds fonts by default when licensing and profile permit.

It records:

- source font identity and license metadata;
- caller attestation/policy for legal embedding authority (font metadata alone is not a legal opinion);
- subset glyph closure;
- embedding permission bits and resulting policy decision;
- encoding strategy;
- widths;
- `ToUnicode` mapping;
- and external interoperability evidence.

### 22.11 Images and color in generation

The generator requires callers to declare image color interpretation or provide sufficient metadata.

It does not silently tag arbitrary bytes as DeviceRGB.

Output profiles can require ICC output intents and preflight checks.

### 22.12 Tagged output

Structured authoring emits:

- marked content;
- stable MCIDs;
- parent-tree relationships;
- role mappings;
- language;
- alternate descriptions;
- and reading order.

Generated tagged documents are validated before finalization when a profile is requested.

### 22.13 External generation gate

Every generated flagship fixture must:

- parse strictly in MonkeyBee;
- render in MonkeyBee;
- validate under requested profiles;
- open and render in a declared external matrix;
- preserve expected text extraction;
- and survive deterministic rewrite/reopen cycles.

---

## 23. Editing, canonical transformation, repair, sanitization, and redaction

### 23.1 Edit sessions are transactions

```rust
pub struct EditSession {
    inputs: NonEmptyVec<TransformInput>,
    mode: EditMode,
    ops: Vec<EditOp>,
    policy: TransformPolicy,
    idempotency: Option<IdempotencyKey>,
}
```

Edits accumulate against immutable input **views**, not root names. Every document `TransformInput` binds the exact `RealityRoot` and `DocumentViewId`; imported assets bind exact artifact/origin identities. The proposal/admission record separately binds the canonical `ExpectedStateId`, caller/authority domain, capability lease, idempotency identity, and publication preconditions. Constructor validation proves that each view belongs to the named root and that no source-backed view omits its `RevisionGraphId`; admission re-evaluates every expected-state predicate before candidate finalization and again before publication where the contract requires it. A proposal may contain one operation or an atomic multi-anchor batch whose cross-operation invariants are validated as one unit.

The L6 core prepares a private candidate, performs lower-layer semantic/profile/signature checks, serializes into a private sink, and strictly reopens it. Independent validators and external processors remain L7/L8 responsibilities. Publication requires the selected assurance profile and a host transaction whose visibility/durability class is recorded.

For authority-bearing remote or agent surfaces, the exact canonical request is bound to a durable idempotency record. The key namespace includes tenant, authenticated caller/authority domain, operation schema/version, and requested publication domain so unrelated users or protocol revisions cannot collide. Before mutation, admission atomically reserves the key for that request identity. A completed duplicate returns the original receipt; a key reused for different content refuses. If a crash leaves commit visibility unknowable, the durable state is `indeterminate`, no automatic retry may execute the mutation again, and reconciliation queries the output/publication transaction and receipt store. Reservation, terminal receipt, and tombstone retention cover at least the maximum retry plus output/publication observability window; expiration cannot authorize key reuse while an earlier effect may remain externally visible. Canonical request digests are access-controlled or keyed/omitted when ordinary hashes would disclose confidential or low-entropy content. MonkeyBee promises neither magical distributed exactly-once delivery nor safe blind retries; it promises deterministic duplicate handling and explicit uncertainty within the admitted durability domain.

### 23.2 Edit operation algebra

Initial typed operations include:

- set or remove metadata;
- add, remove, reorder, or import pages;
- update annotations;
- set form values;
- add or remove attachments;
- replace images;
- append page content;
- overlay or underlay content;
- update outlines and destinations;
- add structure semantics;
- remove actions;
- and replace object values through expert APIs.

Each op declares whether it is supported in preservation mode.

Edits operate on a shared-object graph. Before mutating a resource used by multiple pages/forms/appearances, the planner computes reachability and either proves the change is intended globally or performs clone-on-write with rewritten references. Page import and resource renaming preserve provenance and avoid accidental changes to unrelated consumers.

### 23.2.1 Cross-document page and object import

Import is a semantic graft, not a shallow copy of a page dictionary. The planner:

- selects a source root, revision/hypothesis, and effective page with explicit provenance;
- materializes inherited page attributes needed by the imported page;
- computes the transitive closure of referenced resources, forms, patterns, fonts, images, color spaces, properties, annotations, and other admitted dependencies under cycle and budget limits;
- allocates new target identities and rewrites every copied indirect reference without aliasing source-root IDs;
- resolves resource-name collisions by deterministic renaming and rewrites affected content programs, including nested forms and appearances;
- applies an explicit carry/drop/remap policy for annotations, destinations, outlines, page labels, article threads, optional-content groups/configurations, associated files, and document-level actions;
- when carrying tagged structure, remaps `StructParents`, MCIDs where necessary, the parent tree, ID tree, role/class maps, namespaces, and structure references as one checked operation, or otherwise drops the structure contribution with an explicit semantic loss;
- never imports the source trailer, xref history, encryption dictionary/keys, file identifiers, signatures, certification permissions, or document-level trust state as ordinary page resources; and
- records every copied, merged, dropped, renamed, or externalized object in the transform receipt.

A page whose required closure contains unsupported encrypted, external, malformed, or dynamically generated state may be imported only under a named partial/rasterized policy with explicit losses, or the operation refuses. The writer must reopen the output and prove that no target reference points back into an unavailable source reality.

### 23.3 Source-preserving mode

This mode optimizes for historical and byte preservation. The default file API writes a new private output containing the original prefix plus the appended revision and then commits that output; it does not mutate the only copy of the source in place. An explicit in-place append adapter is a weaker host capability with crash/trailing-garbage consequences recorded in the receipt.

It is appropriate for:

- annotations;
- signatures with allowed incremental changes;
- metadata updates;
- form filling;
- and audit-sensitive workflows.

It cannot claim removal of old sensitive content because prior revisions remain in the file.

Preserving the signed byte prefix does not by itself mean an appended edit is permitted. Before publication, the writer separately reports cryptographic integrity, `DocMDP`/`FieldMDP`/field-lock classification, and application policy. A prohibited-but-byte-preserving update is not described as signature-preserving.

### 23.4 Canonical-rewrite mode

This mode constructs a new source root from selected effective semantics.

It can:

- remove unreachable objects;
- remove prior revisions;
- normalize object structures;
- recompress streams;
- rebuild page and name trees;
- and enforce a target profile.

It records every source object not carried forward.

Unknown, proprietary, malformed, and unexplained objects follow an explicit carry/drop/quarantine policy. A security-oriented canonical rewrite defaults to dropping or quarantining objects it cannot semantically justify; a preservation-oriented canonicalization may carry them only with provenance and no-claim boundaries. “Unknown” never means “copy because it was reachable.”

For encrypted input, canonical rewrite requires an explicit output-security decision: decrypt to clear output, re-encrypt under a new secure policy and entropy source, or refuse. It never copies encryption dictionaries or keys as if they were ordinary semantic state.

### 23.5 Semantic diff

A document diff reports separately:

- byte and revision changes;
- effective object changes;
- page-program changes;
- visible appearance changes;
- glyph/text changes;
- logical-structure changes;
- metadata and attachment changes;
- action/security changes;
- and signature changes.

One scalar “PDFs differ” is insufficient.

### 23.6 Visual equivalence

Visual comparison supports:

- exact pixel identity;
- bounded per-channel difference;
- structural primitive comparison;
- and secondary perceptual metrics.

Perceptual similarity cannot authorize a security or exact-preservation claim.

### 23.7 Text and structure equivalence

The transformation layer compares:

- source character codes where preserved;
- glyph instances;
- Unicode claims;
- reading order;
- structure roles;
- alternate text;
- and navigation relationships.

It exposes both improvements and regressions.

### 23.8 Secure redaction [F]

Secure redaction is not drawing a rectangle.

The transformation must remove or neutralize target information from:

- page content streams;
- form XObjects;
- patterns and Type 3 glyph procedures;
- images and masks;
- clipped or invisible content;
- optional-content states;
- annotations and appearances;
- metadata;
- structure and ActualText;
- embedded files;
- object streams;
- and prior incremental revisions.

The default secure path is a canonical rewrite.

A secure-redaction headline is admitted only when every potential carrier that remains in the emitted artifact is inspectable under the declared target/search policy, or has been proven absent from the carried object/byte set. Missing credentials, an unsupported codec, unavailable external content, an unexplained retained range, or an unenumerated recovery/visibility branch therefore yields partial coverage or refusal unless that opaque carrier is dropped and the carry/drop proof shows that it cannot reach the output. “We could not decode it” is never treated as evidence that the secret is absent.

The redaction inventory also examines thumbnails, alternate images, portfolios/collections, external-file streams, XFA packets, JavaScript strings, signature dictionaries and certificate metadata when policy requires, page-piece/private data, embedded XML, unknown extension objects, and unexplained source regions. Vector outlines can encode human-readable secrets without text or raster semantics; automatic semantic discovery cannot guarantee finding them, so region/object-targeted redaction and human review remain explicit tools.

### 23.9 Redaction intent model

A redaction request identifies targets by one or more of:

- source byte/object identity;
- text node and Unicode/glyph evidence;
- geometric region;
- structure node;
- annotation or attachment;
- metadata field;
- regular-expression or policy match with explicit evidence requirements;
- or caller-provided object set.

Ambiguous text mappings may require human confirmation or produce multiple targets.

### 23.10 Negative redaction evidence

The redaction package includes independent searches for residual information:

- the complete output byte source, unexplained ranges, and every retained object version;
- all decoded streams and typed codec products;
- all text/glyph nodes;
- all images through OCR adapters if requested;
- all metadata and attachments;
- all content regardless of current optional-content visibility, plus bounded/symbolic checks of declared usage configurations;
- and external forensic-tool adapters.

A negative result is scoped to the search inventory and cannot prove absence outside it.

The package also records oracle lineage and shared detection dependencies. OCR, text extraction, raw-byte search, and an external forensic wrapper that all reuse the same model or parser do not count as four independent checks. External references that were never fetched are either removed/neutralized or remain explicit uninspected dependencies; MonkeyBee cannot prove absence in content it did not possess.

Secure redaction is a claim about the emitted PDF and enumerated related artifacts, not secure deletion from the caller’s source filesystem, backups, cloud versions, logs, caches, printer spools, recipients, or storage media. Those are separate host/organizational controls.

Content absence and inference resistance are also separate claims. Even after target glyphs or strings are removed, surviving `TJ` adjustments, word/character spacing, neighboring glyph positions, line breaks, structure order, object lengths, image silhouettes, or other layout residue may reveal information about the redacted value. A high-assurance policy therefore runs known layout/position side-channel attacks, removes or reflows target runs and adjacent positioning state where necessary, and may rasterize or reconstruct a larger region when the semantic collateral budget permits. The receipt reports `target_content_absent` separately from a scoped `inference_resistance` assessment and never promises zero information leakage against every future inference method.

### 23.11 Content surgery

Removing selected visible primitives from arbitrary content programs is difficult because state and clipping are procedural.

The transformation uses one of three explicit strategies:

1. source-program rewrite with state-aware operator ranges;
2. form or page decomposition and reconstruction;
3. rasterization of an affected region under a declared loss-of-semantics policy.

Strategy 3 never claims preservation of vector/text semantics.

Every redaction policy also carries a collateral-change budget. The receipt reports non-target primitives/resources changed, pixels outside requested regions, text/structure losses, deduplication side effects, and whether shared resources were cloned. “Removed the secret” is not permission to silently damage unrelated content.

### 23.12 Sanitization

Sanitization policies may target:

- active content;
- external references;
- attachments;
- encrypted-payload/unencrypted-wrapper documents;
- hidden layers;
- forms;
- JavaScript;
- rich media;
- signatures;
- malformed structures;
- and historical revisions.

The result states both removals and classes not inspected.

### 23.13 Repair writeback

Repair writeback converts a recovery hypothesis into a strict output.

The receipt maps every repair assumption to concrete serialized changes and reruns strict parsing plus independent checks.

### 23.14 Optimization transformations

Optimization is a policy bundle, potentially including:

- duplicate-resource elimination;
- unreachable-object removal;
- stream recompression;
- object streams;
- image resampling under a visual budget;
- font subsetting;
- metadata pruning;
- and linearization.

Each lossy step requires an explicit budget and evidence.

### 23.15 Flattening

Flattening annotations or forms is a transformation that:

- renders appearances;
- inserts page content;
- updates or removes interactive objects;
- and checks visual output.

It does not execute unsupported scripts to discover dynamic state.

### 23.16 Evidence-carrying transformations

Every security- or preservation-sensitive transform produces:

- exact role-labeled input root/view/expected-state bindings and imported-asset identities;
- policy ID and version;
- operation list;
- output hash;
- exact removed and added object versions;
- visual/text/structure/security diffs;
- signature impact;
- profile results;
- independent falsifier results;
- and remaining no-claims.

---

## 24. Validation, interoperability, and the compatibility laboratory

### 24.1 Validation profiles are versioned programs

A validation profile contains:

- profile identity and version;
- target PDF standard version;
- imported rule sources;
- MonkeyBee `SpecCard` dependencies;
- rule implementation versions;
- unsupported rule inventory;
- and severity policy.

Profiles are data where practical, code where necessary, and always reviewable.

Rule results use at least `Pass`, `Fail`, `NotApplicable`, `NotEvaluated`, `Unsupported`, and `Indeterminate` with explicit coverage. Budget exhaustion, missing credentials, unavailable external tools, or an unimplemented rule never collapse into `Fail` or disappear from an apparently complete profile verdict.

ISO 32000 defines PDF syntax and processor behavior but does not prescribe one universal conformance-validation method. A MonkeyBee validation profile is therefore a versioned implementation of cited requirements and policy; its verdict is scoped to executed rules, unsupported rules, profile version, and checker build. It is not “the ISO validator.”

### 24.2 Initial profile sequence

1. Core file-structure and COS conformance.
2. Full Arlington-covered object-model validation.
3. PDF 2.0 core profile with current errata.
4. Selected PDF/A profile beginning with the corpus having the strongest available support and an independent oracle.
5. Selected PDF/UA profile.
6. Selected PDF/VT profile with its exact named edition and application envelope.
7. Additional archival, engineering, print, and accessibility profiles as evidence matures.

Support is claimed profile by profile, not by saying “standards compliant.”

### 24.3 Independent validators

Where mature independent validators exist, MonkeyBee invokes them through black-box adapters in the development laboratory.

The adapter records:

- tool name and version;
- command/configuration;
- environment;
- output artifact;
- and normalized findings.

Independent validator results do not become runtime dependencies of the core library.

Their evidence records oracle lineage and correlation. Two tools built on the same parser/rule dataset are useful corroboration but not independent failure modes; the lab seeks heterogeneous implementations and human/source adjudication for load-bearing disagreements.

### 24.4 External processors as experimental subjects

External PDF readers, renderers, editors, and RIPs are used only as named black-box subjects.

They are also treated as potentially vulnerable programs receiving hostile files. Adapters use fixed argument vectors rather than shell interpolation, immutable/disposable tool images where practical, read-only inputs, private output directories, no host secrets, no ambient network, CPU/memory/output/time quotas, and process or VM/container isolation proportionate to risk. A crash, hang, or sandbox violation becomes an observation; it must not compromise the corpus host or silently disappear from the experiment record.

MonkeyBee does not derive implementation code from their source. When a released subject is distributed only as source, a contamination-isolated oracle-administration environment may obtain and build it under its license. Implementation contexts receive only the pinned executable/service, declared public interface, normalized observations, and rights-approved documentation; they do not receive source, source-bearing compiler diagnostics, debug/source maps, implementation traces, or symbolized internals. The build recipe, toolchain, features, lockfile, patches (normally none), and artifact digest remain in the lab record.

For each observation the lab records:

- exact executable or service version;
- platform;
- invocation;
- profile/settings;
- input hash;
- output hash;
- and observed behavior.

### 24.5 No majority vote

If five engines agree and one differs, MonkeyBee does not automatically follow five.

The laboratory asks:

- Is the input conforming?
- Does the standard determine one result?
- Does errata change the answer?
- Are all engines inheriting one historical convention?
- Is the disagreement profile-dependent?
- Which result preserves security or data most conservatively?
- Can an atomic witness isolate the cause?

### 24.6 Differential rendering

Comparisons operate at multiple levels:

- page dimensions and boxes;
- exact or bounded pixel deltas;
- edge maps;
- color-channel/separation differences;
- primitive counts and bounds where trace data is available;
- glyph positions;
- and tile-local diagnostics.

The first goal is localization, not a flattering aggregate score.

### 24.7 Divergence minimization

The lab uses deterministic reduction to minimize a disagreeing document while preserving the observation.

Reduction operators include:

- remove pages;
- remove unreachable objects;
- replace resources;
- prune dictionary entries;
- remove content operators;
- simplify paths;
- reduce font tables or glyph sets;
- crop images;
- simplify filter chains;
- and remove revisions.

Every reduction step must preserve more than the final pixel/text predicate. The reducer also pins the witness class and causal envelope selected for the experiment: strict-conformance versus recovery status, effective revision/hypothesis, processing and compatibility profiles, feature/capability set, encryption/signature state relevant to the observation, resource-limit regime, and at least one causal anchor connecting the surviving source/program condition to the divergence. If a mutation changes that class—for example, a conforming color disagreement becomes an unrelated malformed-xref recovery disagreement—the lab forks a new witness lineage and does not call it a minimization of the original cause. Reduction receipts record which invariants were rechecked at every accepted step.

### 24.8 Causal divergence graph

After minimization, the lab emits:

```text
source span/object
 -> semantic rule or malformed condition
 -> page-program state
 -> appearance/text/security consequence
 -> processor observations
```

This graph becomes a permanent corpus artifact and compatibility-policy input.

### 24.9 Compatibility profiles

A compatibility profile may encode a deliberate behavior only when:

- the triggering condition is precise;
- the affected processor family and versions are recorded;
- security consequences are reviewed;
- the behavior is isolated from strict mode;
- a corpus witness exists;
- and a retirement condition is named.

Compatibility branches are not scattered ad hoc throughout the code. They are policy decisions referenced by stable IDs.

### 24.10 Specification ambiguity registry

When standards prose admits multiple plausible readings, MonkeyBee records an ambiguity item containing:

- clause references;
- competing interpretations;
- examples;
- external processor behavior;
- safety impact;
- selected profile behavior;
- and resolution status.

This registry prevents different agents from resolving the same ambiguity differently.

### 24.11 Compatibility rent

Every compatibility rule must pay rent.

Periodic review asks:

- Is the external behavior still relevant?
- Does the rule create security or maintenance cost?
- Can it be expressed as a more general principle?
- Has a standard interpretation resolved it?
- Does the corpus still justify default enablement?

Rules that no longer pay rent are retired from default profiles while remaining available for historical replay.

---

### 24.12 Competitive supremacy doctrine

The plan-legible doctrine is:

> **For every declared atomic capability lane, MonkeyBee seeks an uncertainty-aware `registered_open_field_lead` over the eligible registered open field defined by an exact versioned `FieldDefinitionId` and yielded by a versioned, independently reviewable, pre-search-committed competitor-discovery protocol—or its eligible non-dominated frontier—under a dated, artifact-pinned, tamper-evidently precommitted comparison. A result over only enumerated artifacts is `named_set_lead`. Where lawful reproducible evidence also pins the material closed or opaque systems actually observed, MonkeyBee may seek `observed_field_lead`. Lifecycle, discovery coverage, field status, and outcome remain separate.**

Doctrine rules:

1. **Supremacy is atomic, leading, scope-qualified, and per-lane—never global.** Equivalence/non-inferiority are valuable gates, not supremacy; no aggregate hides a trailing safety, correctness, coverage, resource, or material feature axis.
2. **Field definition plus three scopes prevent market-search laundering.** Every field claim names a versioned `FieldDefinitionId`; “pure-Rust native renderer,” “all open released PDF renderer,” “PDF/A-2 generator,” and “all software” are different fields. `named_set_lead` covers exactly named artifacts. `registered_open_field_lead` covers every eligible open released artifact yielded for that exact field by the frozen search protocol and challenge window—not every system that might exist and not an unstated Rust-only subset. `observed_field_lead` adds material lawfully pinnable closed/opaque systems. Incomplete or uncommitted discovery cannot exceed named-set scope.
3. **Discovery and evaluation form a three-stage, three-commit evidence process.** The search/eligibility protocol is independently committed before searching. The executed discovery report and comparator set are committed after the nomination/challenge window. Only then is the measurement protocol committed against that frozen report before measurement. Search surfaces, registries, languages, terms, dates, scouts, deviations, nominations, exclusions, and inaccessible systems remain visible.
4. **Documentation silence is not absence.** A failed feature search or missing README claim cannot establish capability absence. A newly discovered material released system lapses current-facing registered/observed field claims until characterized.
5. **Claims obey the ordinary evidence algebra.** They are scoped, expiring, uncertain, refusable, and withdrawable.
6. **The measurement protocol is frozen before unblinding.** Corpus, profiles, comparator configurations, tuning budgets, analysis, stopping, missingness, adjudication, utility relation, and claim expiry are content-addressed and independently time-committed after discovery freeze. Material change creates a new protocol and fresh confirmatory evaluation.
7. **The artifact and its strongest eligible configuration are pinned, not merely named.** Release/channel, digest or immutable authority identity, documented production configuration, optional features, dependencies, observation date, and mutable-service limitations are recorded.
8. **Configuration and tuning are symmetric.** Each competitor receives the strongest documented eligible production configuration under the frozen constraints, the same bounded tuning/integration budget, and—where practical—an independent operator plus a maintainer/vendor challenge opportunity. A lab wiring failure is `indeterminate` until triaged; sabotaged defaults or unequal tuning cannot manufacture a lead.
9. **Competitors are experimental subjects, never implementation sources.** §4.1 applies regardless of license or language, and shared implementation/dependency lineage reduces oracle independence.
10. **Benchmarks are evidence inputs, not optimization targets.** Frozen denominators, complete outcomes, rights/privacy, leakage, adaptive-holdout access, benchmark-owner conflicts, and independent held-out guards are explicit.
11. **Statistics match the experiment.** Primary unit, pairing/clusters, uncertainty, effect/precision target, multiplicity, stopping/peeking, missingness, and stochastic attempt/selection policy are predeclared.
12. **No metric laundering.** Atomic scorecards, margins, Pareto relations, or justified utility rules handle tradeoffs. Unresolved tradeoffs are `incomparable`; unsupported/partial/timeout/resource/indeterminate/disqualified cases stay visible.
13. **Lifecycle, discovery coverage, field status, outcome, and scope are orthogonal.** `uncontested` is a dated registered-search result, not superiority or proof of global absence.
14. **Product comparison is not the post-agent conclusion.** It contributes artifact substance and grounding, not foundry disproportion or lineage maturity.

### 24.13 Competitor register

The register is a generated, versioned snapshot over structured observation records rather than hand-maintained market prose. Each record carries: project and capability family; open/closed and release-channel status; exact release/tag/artifact identity where obtainable; observation date; source-vintage identity; whether a statement is project-reported or independently reproduced; license/clean-room relevance; observed capabilities and limitations; lane eligibility; uncertainty; expiry; and superseding record. Mutable vanity statistics are excluded unless a claim truly depends on them.

The snapshot below was re-observed on **2026-07-14** from primary release/project documentation. Project claims remain **[self-reported / unverified]** until MonkeyBee’s harness or an independent source reproduces them. Main-branch documentation is an early-warning record, never a released baseline. This prose snapshot is not proof of field completeness: every claim binds a `CompetitorDiscoveryReport` covering registries, repositories, benchmark entrants, search terms/languages, nomination windows, and exact exclusions. The fresh search that produced revision seven found material renderer candidates omitted by revision six, demonstrating why discovery coverage must be evidence rather than an assumption.

#### 24.13.1 Tier 1 — Primary pure-Rust rendering and generation comparators

**hayro 0.7.1** (released 2026-06-05; rendering). Release documentation describes a CPU rasterizer that forbids unsafe code in its crate, reports more than 1,000 regression PDFs largely drawn from upstream pdf.js/PDFBox suites, and lists encrypted/password-protected files, blending/isolation, knockout groups, and color-key masking among serious limitations. Main-branch documentation reports more than 1,400 fixtures and gives knockout and non-embedded CID fonts only as non-exhaustive examples while saying performance has not yet been a focus. That difference is **documentation drift**, not evidence that omitted limitations have landed; only a release test or release notes can establish closure. `hayro-write` is an internal converter that writes existing PDF pages as XObjects or new pages through `pdf-writer`, not a demonstrated general editor. The project NOTICE records adapted/translated PDFBox and pdf.js implementation material, so hayro remains a direct and transitive clean-room contamination source.

**pdf_oxide 0.3.74** (latest docs.rs artifact observed 2026-07-14; parsing, extraction, optional rendering, creation/editing, bindings, OCR/signature options, and MCP). Current project documentation advertises a rendering feature, creation/editing, broad bindings, an MCP server, OCR availability paths, and extraction benchmarks over 3,830 public-suite PDFs **[self-reported / unverified]**. It is a material candidate for S1, S3, S4, S5, and S6, but exact compiled features, optional native/cryptographic/model dependencies, fallback fonts, color profile, and artifact digest must be pinned; a project-wide “pure Rust” label cannot silently cover every optional configuration.

**stet / stet-pdf-reader / stet-pdf 0.2.1** (released 2026-07-12; rendering, structural reading, encryption, and PDF output). Current docs advertise PDF content interpretation to display lists and RGBA, RC4/AES-128/AES-256 decryption, typed structural access, optional-content handling, ICC/color infrastructure, and a PDF output device preserving CMYK/spot-color and print controls **[self-reported / unverified]**. This makes Stet a material S1/S2/S4/S6 candidate rather than a tracked footnote. Its reader explicitly reuses hayro JPEG 2000, JBIG2, and CCITT crates, so codec results are correlated with hayro on those failure modes and Stet source is another clean-room contamination path; two wrappers over shared codec lineage are not two independent oracles.

**pdfpurr 0.4.0** (released 2026-07-04; early-development reader/writer/editor/renderer). Documentation claims pure-Rust reading, writing, editing, rendering, encryption, forms, signatures, OCR, PDF/A, PDF/UA, and PDF/X support while explicitly warning that the project remains in a foundation/unstable phase **[self-reported / unverified]**. Breadth claims do not establish maturity or profile completeness, but they make `pdfpurr` a mandatory characterization candidate for every intersecting atomic lane.

**krilla 0.8.2** (released 2026-06-04; generation). A high-level generator over `pdf-writer`, with tagged output, multiple PDF versions and archival/accessibility profiles, font subsetting, and broad visual/validation infrastructure. Project documentation reports Arlington and veraPDF checks plus visual tests over six viewers, five in CI. Encryption and PDF-signature creation remain outside the observed generation scope. S4 compares exact output/profile behavior; matching the existence of a test suite is not itself product superiority.

**Assessment.** These are the primary currently identified pure-Rust comparators for rendering and high-level generation, not an assertion of field completeness. They ship or publish quickly, and several already contest generic rendering, editing, signature, accessibility, generation, XFA, and agent-surface language. The register found no independently substantiated publication of MonkeyBee’s exact clean-room/evidence/recovery/transformation conjunction as of the observation date; documentation silence is not proof, and every such statement expires. S1 may not select hayro merely because the addendum originally named it, and S4 may not select krilla as the whole generation field.

Renderer eligibility is **output-contract-specific**. Native PDF-byte-to-raster rendering, PDF-to-SVG conversion, extraction screenshots/layout visualization, and rasterization of a project-owned intermediate layout tree are different capabilities and cannot substitute for one another in S1 or S6. Additional released Rust candidates requiring explicit characterization include:

- **printpdf 0.10.1**, whose current API parses PDF through `lopdf` and exposes PDF-page-to-SVG conversion; it enters only vector-conversion subclaims unless a complete pinned SVG-to-raster pipeline is declared and every dependency/cost is counted;
- **fop-pdf-renderer 0.1.2**, which advertises a PDF-to-RGBA/PNG path **[self-reported / unverified]**;
- **pdfsink-rs 0.2.9**, whose current item documentation exposes `PageImage`/`RenderOptions` while release documentation has shown version drift; its exact byte-to-page raster path, dependency closure, and output profile require artifact-level characterization;
- **pdf-rs/pdf_render**, an established pure-Rust parser/renderer family whose exact released artifact and maintained profile must be pinned;
- **oxidize-pdf 4.0.1**, whose documentation says its parser supports “rendering” but whose published examples do not yet establish a complete page-to-pixels contract; and
- **pdforg-render 0.1.0**, which rasterizes its own `LayoutPage` representation to canvas commands/PNG and therefore is not automatically a PDF-byte-to-raster comparator unless the complete PDF ingestion pipeline is pinned.

**safe-pdf**, **connorskees/pdf**, and layout-preserving editors such as **harumi** remain tracked. Advertisement, a render-named crate, or the presence of an image type does not establish profile completeness, independence, or lane eligibility; every candidate receives a recorded per-subclaim disposition rather than silent inclusion or omission.

#### 24.13.2 Tier 2 — Commercial/opaque Rust SDKs, incumbent engines, and structural tools

**PDFluent 1.0.0-beta.17** (latest observed public crate line; commercial/trial Rust SDK) documents a unified surface for loading, editing, rendering, merging, signing, encryption, redaction, PDF/A, forms, resource limits, and a Phase-1 XFA field model **[self-reported / unverified]**. It directly contests generic claims that no Rust SDK spans rendering, editing, signing, redaction, compliance, or XFA. Because licensing, exact enabled components, implementation lineage, and reproducible artifact access differ from an ordinary open comparator, each lane must classify it explicitly as registered-open or observed/opaque rather than excluding it by convenience. Published component metadata also shows lineage to existing Rust PDF components, so oracle independence and clean-room contamination are assessed per component.

PDFium, MuPDF, Poppler, pdf.js, Ghostscript, Apache PDFBox, QPDF, iText/OpenPDF, ReportLab, and comparable mature processors collectively cover enormous wild-tail, rendering, writing, repair, and transformation territory. Individual tradeoffs differ: native memory-unsafe cores, copyleft or dual licensing, browser/runtime coupling, commercial terms, non-Rust embeddings, and evidence-model gaps are not one uniform disqualification. Open released artifacts enter the applicable `registered_open_field_lead` whenever the `FieldDefinitionId` includes them; closed or operationally opaque artifacts enter `observed_field_lead` where pinning and lawful automation permit. They also remain reference oracles and S6 performance comparators. Rust wrappers around PDFium are a potential adoption pool, not evidence that every wrapper user will convert.

#### 24.13.3 Tier 3 — Rust extraction, manipulation, editing, and agent surfaces

**oxidize-pdf 4.0.1** reports pure-Rust parsing, bounded/lenient recovery, deterministic no-ML RAG chunks, generation, RC4/AES read and write, PKCS#7 verification, PDF/A validation, JBIG2, and split/merge/rotate behavior over a 9,000+ corpus **[self-reported / unverified]**. Current documentation does not by itself establish a general page-to-pixel rendering competitor; that capability is characterized from the exact artifact rather than inferred from broad wording. The project still contests generic recovery, encryption, generation, validation, and structured-extraction claims.

`pdf_oxide 0.3.74` is recorded canonically in Tier 1 because it now spans rendering as well as extraction/editing/MCP. Its presence materially contests generic “agent-native,” editing, multi-language, rendering, and redaction claims: MonkeyBee’s claim must rest on exact root/view/derivation anchors, least authority, stale-safe validation, refusal, and receipts—not the existence of a transport or source-evidence label. **lopdf**, `unpdf`, `pdf_extract`, and other crates remain important structural/extraction comparators.

#### 24.13.4 Tier 4 — Structured extraction, recognition, accessibility, and agent-evidence systems

Docling, Marker, MinerU, OpenDataLoader, LiteParse, MarkItDown, PyMuPDF4LLM, Unstructured, PDF Reader MCP, and related systems use different mixtures of native parsing, layout heuristics, OCR, models, rendering, and agent protocols. Some are local, deterministic in selected modes, and GPU-free; the field cannot be dismissed as uniformly remote or nondeterministic. The sharper MonkeyBee target is exact byte/revision/virtual-span/derivation identity, profile-bound determinism, explicit hypothesis and refusal semantics, least-authority mutation, and evidence-preserving composition with native PDF truth.

**OpenDataLoader 2.4.7** (released 2026-05-27) owns a public benchmark for reading order, tables, and heading hierarchy and reports local no-GPU extraction, optional hybrid recognition, bounding boxes, evidence overlays, and open-source Tagged-PDF auto-tagging with veraPDF validation **[self-reported / unverified]**. Because the benchmark is maintained by a participant, it is useful external evidence but not a neutral sole oracle. Its auto-tagging makes basic accessibility remediation a contested capability; PDF/UA export remains separately scoped in its published product boundary.

**PDF Reader MCP 3.0.14** (registered release observed 2026-07-14) reports a local-first “Agent Document Twin,” page-plus-bounding-box source evidence, visual crops, OCR provenance, trust/accessibility reports, stable IDs, and benchmark-gated release checks **[self-reported / unverified]**. It directly contests generic “evidence-first PDF for agents,” source-evidence, trust-report, and MCP claims. MonkeyBee’s differentiator must therefore be the stronger byte/revision/derivation evidence algebra, hostile-input/recovery model, authority-safe proposal/apply semantics, and independently checked transformation—not the words evidence, trust, source, stable ID, or MCP.

**LiteParse** provides local PDFium-based structured extraction, page screenshots, Tesseract or HTTP OCR, and an agent-oriented interface; it is a surface and interoperability comparator, not proof against MonkeyBee’s deeper evidence conjunction.

#### 24.13.5 Tier 5 — Suites, orchestrators, and independent instruments

**Stirling-PDF** is a widely distributed orchestration suite over multiple mature processors and is a potential integration/customer channel; dynamic star/download counts do not belong in the frozen plan. **pdfcpu** is a substantial Go structural-processing comparator. **veraPDF**, the Arlington PDF Model, public conformance suites, and Digital-Corpora/SafeDocs-class collections are instruments or corpus sources, not competitors merely because they produce verdicts or files. Every use still passes rights, privacy, lineage, and denominator review.

### 24.14 The conjunction gap

The dated strategic proposition is:

> **No open system identified by this register currently publishes and independently substantiates MonkeyBee’s complete conjunction: hostile-input recovery with explicit live alternatives propagated into security claims; one byte/revision/object/program/appearance/text/security reality; bounded memory-safe execution; rendering and generation; stale-safe, signature-impact-aware source-preserving and canonical transformation; and evidence-carrying explanation from exact inputs through outputs.**

Competitors now cross many boundaries the earlier plan treated as empty: hayro renders and converts pages; `pdf_oxide` reports rendering, editing, redaction, many bindings, and MCP; `oxidize-pdf` reports recovery, encryption, generation, signatures, and validation; krilla spans generation and profile checking; OpenDataLoader reports structured extraction and Tagged-PDF auto-tagging; PDF Reader MCP reports source evidence, OCR provenance, and trust reports; incumbents collectively cover most ordinary PDF operations. The opportunity is therefore not “nobody edits,” “nobody recovers,” “nobody tags,” “nobody renders in Rust,” or “nobody exposes evidence/MCP.” It is the exact demonstrated conjunction under one authority, identity, evidence, refusal, and lifecycle model. That proposition is an expiring register observation, not a theorem, novelty proof, or global-best claim.

### 24.15 Supremacy lanes and gates

Each lane names eligible competitors, claim scope, atomic metrics, a canonical denominator or sampling frame, analysis unit, adjudication, Goodhart guard, and fallback. Lane numbering remains S1–S6; S5 is a family of atomic candidate-conjunction records rather than one aggregate victory.

#### 24.15.1 S1 — Rendering equivalence gate, then field lead [F]

**Comparator set and field definitions:** S1 maintains at least two non-interchangeable atomic fields. The initial `pure_rust_native_pdf_to_raster` field includes every material eligible released pure-Rust implementation for the exact predeclared output contract at cutoff; its characterization pool includes hayro 0.7.1, `pdf_oxide` 0.3.74, `stet-pdf-reader` 0.2.1, `pdfpurr` 0.4.0, `fop-pdf-renderer` 0.1.2, `pdfsink-rs` 0.2.9, and `pdf-rs/pdf_render`; `printpdf` 0.10.1 enters PDF-to-SVG subclaims but not native-raster claims by name alone, while `oxidize-pdf` 4.0.1 and `pdforg-render` 0.1.0 remain characterization candidates until their complete PDF-input/output contracts are demonstrated. Exact eligibility is decided by the frozen field/discovery/profile protocol, not by crate naming or prose reputation. A stronger separate `all_open_released_pdf_to_raster` field includes every eligible open implementation regardless of language or runtime—including, where profile-compatible, PDFium, MuPDF, Poppler, Ghostscript, pdf.js, PDFBox, and any stronger release found by discovery. MonkeyBee may lead the pure-Rust field while trailing the all-open field; the two results are never merged or described with one adjective. A report earns `registered_open_field_lead` only against the complete eligible set or non-dominated frontier for its exact `FieldDefinitionId`. Lawfully pinned closed/opaque processors may support a separate `observed_field_lead`; reference-oracle use alone does not silently enlarge the claim scope.

**Denominator:** a rights-cleared canonical manifest derived from upstream public pdf.js and PDFBox fixture sources by a corpus steward who does not expose surrounding prohibited processor source to implementation contexts. The manifest pins source revisions, fixture hashes, duplicates, linked/external assets, renderability, intended purpose, profiles, rights, and every exclusion reason before results are viewed. “Full suite” never means infrastructure files, duplicates, unlicensed links, or engine-specific expected images silently counted as neutral truth. Every included canonical fixture enters a complete accounting category: common supported scope, named-competitor-only gap, MonkeyBee-only gap, both unsupported/refused, partial, indeterminate/adjudication-pending, timeout/resource, or disqualified. Nothing is dropped because neither system likes it.

The scorecard has two stages. **Full-denominator intersection equivalence/non-inferiority** is a paired document-level comparison over the common admitted profile; pages/regions are nested observations and cannot counterfeit independent sample size. It requires predeclared margins, cluster-aware uncertainty, and no material MonkeyBee regression in any safety/correctness/coverage stratum. **Atomic field lead** is then tested under a predeclared decision relation over the full eligible set. Release-documented hayro 0.7.1 gaps—encrypted/password-protected input, blending/isolation, knockout groups, and color-key masking—remain hayro-specific gap strata after refresh; they are not automatically field-wide gaps because `pdf_oxide` or another challenger may support them. Malformed-input recovery is an **inferred MonkeyBee conjunction stratum**, not a register-documented hayro limitation. Gap wins cannot compensate for a material common-capability loss, and beating one named rival cannot establish field lead over an unmeasured challenger.

Reference images are evidence from named processors, not normative truth; unresolved disagreements go through §24.5 standards/analytic/adjudication rather than majority vote. **Goodhart guard:** a separately stewarded S2 sample plus held-out generated combinations. **Fallback:** narrow the first claimed render profile or publish trailing/incomparable/indeterminate status; never relax thresholds or challenger eligibility after seeing failures.

#### 24.15.2 S2 — The Wild-Tail Ledger [F]

**Comparator and scope:** the primary S2 field is `all_open_released_wild_pdf_renderer` for each predeclared profile, including every material eligible released open renderer regardless of implementation language/runtime—or every member of its eligible non-dominated comparator set when no single renderer dominates. A separately reported pure-Rust field may be useful but cannot substitute for the all-open claim; lawfully pinned mature closed/opaque systems may add a separately labeled `observed_field_lead`. **Sampling frame:** a deduplicated, privacy- and rights-reviewed, independently stewarded stratified sample drawn after pipeline, challenger set, and thresholds freeze. Strata record producer, version/dialect, encryption, malformedness, fonts, codecs, transparency, signatures, page count, and known selection bias; reweighting and exclusions are predeclared.

The document is the primary analysis unit; page/region outcomes are paired nested observations with cluster-aware intervals. For each document and declared page/region/output scope, the ledger reports open, render, extract where declared, and typed refusal/partial outcomes. “Correct refusal reason” is an adjudicated claim, not something a reference renderer can decree. Outcomes are `supported-correct`, `supported-incorrect`, `refusal-correct`, `refusal-incorrect`, `partial`, `indeterminate`, `timeout`, `resource`, `credential-blocked`, or `policy-blocked`, with standards cards, multiple observations, and expert adjudication where needed. Unresolved malformed or implementation-dependent cases remain indeterminate. Publishing the ledger is mandatory; only an uncertainty-aware leading subclaim under the stated field scope may be called supremacy. Equivalent, non-inferior, incomparable, or trailing results retain those names.

**Goodhart guard:** new steward sample per release; old samples become regression floors. **Fallback:** none for publication honesty; the supremacy outcome may be trailing.

#### 24.15.3 S3 — Structured extraction, agent evidence, and provenance crossing [F]

**Comparators:** the strongest eligible released systems on the selected public benchmark plus independently stewarded deterministic/local, provenance-aware, and agent-evidence challengers. OpenDataLoader 2.4.7, `pdf_oxide` 0.3.74, `pdfsink-rs` 0.2.9, PDF Reader MCP 3.0.14, LiteParse, and every stronger eligible release are material candidates for the exact subclaims they advertise. **Public evidence:** enter opendataloader-bench or a successor for its actual metrics—reading order, table fidelity, and heading hierarchy—while disclosing benchmark ownership, preserved third-party predictions, runnable-engine differences, and any corpus exposure. Independently reproduce the scoring pipeline and pair it with a neutral held-out set whose authors and documents were not used to design MonkeyBee’s heuristics.

The document/task is the primary analysis unit. Quality, latency, locality, GPU use, determinism, bounding boxes, refusal honesty, page/bbox evidence, OCR provenance, trust reporting, and byte/revision/derivation provenance are separate scorecard axes. Page/bbox citations and stable IDs are real competitor capabilities, not synonyms for exact byte/revision lineage. For stochastic or provider-backed routes, the report fixes attempt budgets, captures model/provider route and seed where available, repeats runs under a predeclared protocol, reports distribution and selection, and never keeps only the best response. A public quality score cannot prove provenance; “highest deterministic/GPU-free/provenance-carrying” is claimable only after auditing every eligible challenger against those definitions. If quality trails model-assisted systems, MonkeyBee reports that result and may compose them through Bet 20 without laundering their evidence.

**Fallback:** claim the strongest demonstrated conjunction actually earned—such as deterministic local extraction with byte/revision provenance—without pretending leaderboard or field leadership.

#### 24.15.4 S4 — Generation validation and writer-extension scorecard [S/F]

**Comparators and field definitions:** krilla’s strongest eligible released artifact at cutoff is the mandatory profile-focused anchor, not the whole field. S4 reports at least a `pure_rust_generator` field and a stronger `all_open_released_generator` field for each atomic version/profile/feature intersection. The pure-Rust field’s initial characterization candidates include `pdf_oxide`, `oxidize-pdf`, `stet-pdf`, `pdfpurr`, `printpdf`/`pdf-writer`, and any stronger release identified by the register; PDFluent enters the separately classified observed/opaque set where lawful. The all-open field additionally includes every eligible open generator regardless of language/runtime—such as PDFBox, iText/OpenPDF, ReportLab, Cairo/other relevant writers, and stronger systems found by discovery—when they implement the exact subclaim. Lawfully pinned closed/opaque generators may add a separately labeled `observed_field_lead`. **Intersection scorecard:** for the same target versions/profile subset and equivalent input features, compare strict reopen, Arlington/veraPDF rule coverage, multi-viewer behavior, tagged output, deterministic serialization where both claim it, file size, and failure/refusal behavior. A challenger that lacks one profile may remain eligible for another atomic feature rather than being excluded wholesale. Matching a competitor’s CI topology is not itself product parity; output behavior on a frozen corpus is.

**Writer-extension axes:** secure standard-handler encryption output under the secure-writer profile and purpose-bound deterministic serialization/operation receipts are separate MonkeyBee writer claims. They are not averaged with generation correctness into one “superior” scalar. Signature-analysis fidelity and source-preserving editing are not generation axes against krilla; they move to exact S5 conjunction records with their own comparator searches. Intersection equivalence is only the gate; a `registered_open_field_lead` statement requires a separately leading atomic result after the complete eligible generator set for that subclaim has been characterized. Open decision 8 remains: parity either excludes PDF/A-1 and covers PDF/A-2+/PDF/UA-1, or §3.2 explicitly admits a PDF 1.4 serialization profile. Nothing here silently resolves it.

#### 24.15.5 S5 — Atomic candidate-conjunction and field-status family [F]

S5 never claims broad categories such as “editing,” “recovery,” “redaction,” “signing,” “XFA,” “accessibility,” “forensics,” or “source evidence” are empty; current competitors—including broad early-stage and commercial Rust SDKs—demonstrably contest those words. It maintains one independently refreshed report per exact candidate conjunction, including:

- a stale-safe typed semantic edit bound to `DocumentViewId`/`DerivationId`, expected substrate state, least-authority apply capability, pre-apply signature impact, and lineage/admission receipt;
- bounded recovery alternatives whose ambiguity propagates into rendering, attachment, action, signature, and security conclusions rather than being collapsed before use;
- canonical redaction with independently falsified byte/object/text/image/history absence plus a separately scoped inference-resistance assessment;
- revision forensics that preserves every discovered occurrence and alternative chain while distinguishing exact history from recovered hypotheses;
- a causal viewer-divergence witness from source/object/program condition through observable difference and minimized witness-class preservation; and
- pixel/glyph/text claims ending at exact source bytes or an exact virtual span plus derivation receipt, without invented inverse attribution.

Each subclaim has its own eligible-comparator search, open/observed field scope, metric, evidence, expiry, and falsifier. `uncontested` is only a dated field-status result after that search; it is not a comparison outcome, proof of global absence, or aggregate victory. If a competitor offers a fragment, MonkeyBee may still lead on the exact conjunction—but only by measuring the whole conjunction without redefining it after observation.

#### 24.15.6 S6 — Performance escalation [F] — proposed amendment to §26.3

**Comparators and fields:** released PDFium and MuPDF builds are mandatory native-throughput anchors, not the complete field. Each atomic workload defines and reports an `all_open_released` performance field for the **same end-to-end output contract**, including every material eligible open implementation or its non-dominated set regardless of language/runtime; a nested `pure_rust` field is reported separately and never substituted for the all-open result. The initial native-raster characterization pool includes hayro 0.7.1, `pdf_oxide` 0.3.74, `stet-pdf-reader` 0.2.1, `pdfpurr` 0.4.0, `fop-pdf-renderer` 0.1.2, `pdfsink-rs` 0.2.9, and `pdf-rs/pdf_render`, subject to artifact-level eligibility. `printpdf` 0.10.1’s PDF-to-SVG path is excluded from a native-raster throughput claim unless a complete end-to-end raster pipeline is pinned and its parser, SVG renderer, rasterizer, intermediates, and all dependency overhead are counted. `oxidize-pdf` and `pdforg-render` enter only after the exact PDF-input-to-output path is demonstrated. APIs, dependencies, profiles, isolation, and output contracts must be equivalent or their mismatch is an explicit scorecard axis rather than an exclusion of convenience. **Decision rule:** no scalar pages-per-second aggregate. Each predeclared §26.2 workload reports latency-to-first-result, steady throughput, tail latency where relevant, peak memory, decoded work, cancellation latency, and correctness/coverage. A claim may use non-inferiority margins per axis or Pareto dominance; a speed win with a material memory, correctness, refusal, determinism, safety, or evidence regression is not superiority. A mixed tradeoff with no predeclared justified winner is `incomparable`.

The document/request is the primary analysis unit; repeated runs estimate machine/run variance rather than pretending to enlarge corpus size. Warmups, run count, stopping rule, machine-health exclusion, cache state, thread count, isolation, font/color resources, output completeness, and evidence overhead are predeclared. Contract-complete and deliberately stripped diagnostic modes are benchmarked separately. A stripped mode is diagnostic sensitivity analysis and cannot support a supremacy claim for the contract-complete product. Non-inferiority/equivalence is an intermediate performance gate; superiority requires an uncertainty-aware leading atomic outcome under the predeclared rule and full challenger set. **Open decision 9 remains unresolved:** until adopted, §26.3’s competitive posture controls. If adopted and later shown to distort the architecture, the escalation lapses rather than weakening safety or claim honesty.

### 24.16 Supremacy assurance, precommitment, discovery, and refresh

Supremacy records are first-class assurance artifacts. A confirmatory field comparison has three irreversible stages:

1. **Pre-search discovery commitment.** A `CompetitorDiscoveryProtocolCommitment` fixes field/capability definitions, eligibility, search surfaces/terms/languages, scouts, cutoff law, nomination/challenge procedure, and planned exclusions before discovery begins.
2. **Discovery execution and field freeze.** Scouts execute the protocol, record deviations, characterize candidates at the eligibility level required, run the nomination/challenge window, and commit a `CompetitorDiscoveryReportId` containing the frozen comparator set and unresolved eligibility. A material discovery-protocol change restarts this stage.
3. **Pre-measurement evaluation commitment.** Only after the discovery report is frozen does an `EvaluationProtocolCommitment` bind that exact report, comparator configurations/tuning budgets, corpus, metrics, statistics, stopping, adjudication, and claim lifecycle before measurement or result inspection.

The evaluation protocol includes:

- atomic claim, exact `FieldDefinitionId`, maximum claim scope, bound discovery protocol/report, cutoff, artifact-pinning method, and challenge disposition;
- strongest documented eligible configuration per artifact, symmetric bounded tuning/integration budget, independent operator where practical, maintainer/vendor challenge opportunity, and triage law for non-running integrations;
- corpus/sampling frame, rights/privacy, frozen denominator, adaptive-access/query budget, outcome taxonomy, exclusions, and replacement rules;
- primary analysis unit, pairing/clusters, dependence/weighting, missingness, effect/precision or power target, uncertainty, multiplicity, stopping/peeking, and adjudication;
- stochastic attempt budget, repeated-run/route/seed policy, selection rule, and drift window;
- profiles/environments, metrics, equivalence/non-inferiority margins, dominance/utility rule, and refusal/partial/timeout/resource/disqualification accounting; and
- benchmark-owner conflicts, oracle/evaluator/dependency lineage, held-out guard, expiry, challenge, withdrawal, and field-status rules.

Each commitment root is independently time-committed through a steward, witnessed/timestamped ledger, or equivalent append-only evidence before the activity it governs. Reveal binds the exact committed bytes. A material amendment creates a new ID, lapses the affected current-facing result where relevant, and requires fresh search or measurement; old and new fields or denominators are never spliced.

If the `FieldDefinitionId` is absent/ambiguous, discovery coverage is incomplete, or its protocol was not prospectively committed, only `named_set_lead` is permitted. `registered_open_field_lead` means lead over the registered open field yielded for that exact field definition by that exact protocol and challenge window, not metaphysical completeness and not a neighboring pure-Rust/all-open field. `observed_field_lead` additionally requires the material pinnable opaque systems actually measured. Documentation absence never establishes capability absence.

Every planning-gate transition and release-claim freeze re-observes the register. Release and main vintages remain separate. A known eligible release available by the associated claim freeze cannot be hidden behind an older cutoff. A newly discovered or released material challenger preserves historical reports but lapses current-facing registered/observed field leads until characterized. S1’s first freeze must directly characterize every known released rendering path, including Stet, pdfpurr, and the other revision-seven discoveries, rather than assuming a remembered subset exhausts the field.

§33 consumes lane results only as artifact-substance and grounding evidence. It still requires its own live production ledger, fair contemporaneous baselines, valid ablations, distributions, maturity distinctions, and evolution evidence.

## 25. Public APIs and product surfaces

### 25.1 Rust facade

The top-level `monkeybee` crate provides stable, high-level entry points while lower crates remain available for expert use.

Representative APIs:

```rust
let opened = MonkeyBee::open(source, OpenRequest::strict(), &cx)?;
let doc = opened.require_complete()?;
let page = doc.page(PageSelector::index(0))?;
let render = page.render(RenderRequest::screen(144.0).with_usage_event(UsageEvent::View), &cx)?;
let text = page.extract_text(TextRequest::evidence_rich(), &cx)?;
let report = doc.validate(ProfileId::pdf_2_0_core(), &cx)?;
```

High-level APIs return report-bearing objects, not naked values.

Open, resolve, recover, render, extract, and validate APIs return `ClaimOutcome<T>` or a domain-specific wrapper. `OpenRequest::strict()` never consults recovery hypotheses: it returns a complete/partial strict result or refuses. A recovery request may return multiple live chains; callers must select one for a declared task or handle ambiguity explicitly.

### 25.2 Synchronous core, asynchronous adapters

Core parsing and computation APIs are synchronous and cancellation-aware.

Async adapters handle:

- remote or segmented byte sources;
- server orchestration;
- progressive rendering;
- and streaming result delivery.

The numerical/rendering core does not require an async runtime.

### 25.3 CLI

The CLI exposes deterministic commands such as:

- `mb inspect`;
- `mb revisions`;
- `mb objects`;
- `mb render`;
- `mb text`;
- `mb validate`;
- `mb compare`;
- `mb explain`;
- `mb repair`;
- `mb rewrite`;
- `mb redact`;
- `mb sanitize`;
- `mb create`;
- `mb corpus`;
- and `mb package check`.

Machine-readable JSON or JSONL output is first-class. Human output is a rendering of the same schemas.

### 25.4 C ABI

The C ABI uses opaque handles, explicit ownership, and copy-out/caller-provided buffers. Custom allocator callbacks are deferred until an audited ABI contract exists; arbitrary host allocators cannot be included inside MonkeyBee’s memory-safety claim.

Requirements:

- no Rust references across ABI;
- no unwinding across ABI, with every entry point using the build's documented panic-containment strategy;
- stable numeric error codes;
- versioned structures with size fields;
- explicit UTF-8 and byte-string distinctions;
- thread-safety and thread-affinity declarations per handle class;
- generation-stamped opaque handles so a stale handle can never alias a newly allocated object in the same slot;
- immutable result snapshots for size-query/copy-out sequences, or a version token that detects intervening mutation;
- no reentrant callback from parser/render/worker internals into foreign code; progress and diagnostics cross through polling or bounded batch-drain APIs unless a separately audited callback profile is admitted;
- and lifetime-safe handle invalidation.

The C ABI’s memory-safety envelope assumes the foreign caller obeys the published pointer/length/alignment and handle-lifetime contract. MonkeyBee validates every value it can validate before dereference and fuzzes the boundary, but it cannot make an arbitrary invalid native pointer safe; that is an explicit no-claim of the embedding boundary rather than a hidden exception to the Rust-core claim.

### 25.5 WebAssembly

The WASM build initially targets:

- in-memory and streamed/spooled sources;
- bounded rendering;
- structural inspection;
- text extraction;
- validation;
- and generation.

It excludes host filesystem and network assumptions.

Codecs or crypto dependencies that cannot compile safely to WASM are reflected in the capability report.

### 25.6 Host capabilities

Optional host services are passed explicitly:

- font resolver;
- trust store;
- certificate/revocation provider;
- external color/device profile store;
- temporary storage;
- trusted-time source for explicitly time-dependent trust/profile checks;
- cryptographic entropy/nonce capability for encryption and randomized or hedged signature profiles;
- signer/key-operation capability with an algorithm-bound deterministic, randomized, or hedged nonce policy;
- deterministic seed/source for non-security layout, sampling, or search heuristics;
- and external forensic/OCR adapters.

A report identifies every host capability used and the immutable effective input that mattered. A resolver label is insufficient: resolved font bytes, ICC/device profiles, trust anchors, revocation objects, timestamps, OCR/forensic tool versions, and external-source snapshots receive content or authority-version identities. Cryptographic entropy is recorded only through a non-secret capability/health receipt and is never confused with a generic reproducible seed. Secure encryption rejects deterministic caller seeds. Signing admission accepts only the selected scheme’s reviewed nonce law through the signer/key-operation capability—approved deterministic derivation is not the same thing as caller-controlled randomness. A mutable host service without a stable snapshot identity can participate only in operation-local results and cannot support persistent deterministic cache or replay claims. Persistent reuse follows §9.6’s two-stage rule: a coarse request index may locate candidates, but reuse is authorized only after the stored actual-dependency and selection-sensitivity manifest is revalidated against the current authority snapshot, including priority or negative-dependency facts that could have changed the selected resource.

### 25.7 Schema stability

Public reports and evidence packages use versioned schemas.

Compatibility rules:

- fields are never silently repurposed;
- unknown fields are ignorable where safe;
- semantic versions are explicit;
- canonical encodings exist for content hashing;
- and migrations are provided for durable packages.

### 25.8 Capability discovery

Each build exposes a machine-readable capability manifest whose entries reference exact §10.10 `ConsequenceContractId`s rather than friendly feature names alone:

- supported PDF versions;
- filters and codecs;
- font types;
- color and ICC coverage;
- validation profiles;
- deterministic classes;
- host adapters;
- and known no-claim boundaries.

No caller needs to discover a missing codec through a late crash.

---

### 25.9 Agent-native semantic surface

MonkeyBee exposes typed, geometry-aware semantic anchors and a propose→validate→approve→apply protocol. Every proposal binds:

- exact `RealityRoot`, `DocumentViewId`, and any required `DerivationId`;
- selected revision/recovery hypothesis, anchor kind, semantic identity, geometry, substrate digest, evidence, coverage, alternatives, and no-claim boundary;
- one anchor or a complete atomic anchor set plus cross-anchor invariants;
- canonical `ExpectedStateId`, proposal schema, caller identity, policy, ownership, confidentiality, preservation, and signature-impact constraints;
- external/model evidence used; and
- tenant/caller/schema-scoped canonical idempotency identity, retention/expiry law, disclosure-safe request commitment, and requested publication durability.

Proposal creation, validation, approval, and application are distinct authorities. Validation is side-effect free. Apply rechecks every bound state and authority. A heuristic/ambiguous anchor may support reading, but high-consequence mutation requires policy-approved confirmation over exposed alternatives or refuses. No stale or changed anchor is redirected to “closest” content.

Batch application is all-or-nothing. The idempotency key is reserved durably for the exact tenant/caller/schema/publication-scoped canonical request before mutation. Reuse with different content refuses; a completed duplicate returns the original receipt. A crash-ambiguous apply returns `indeterminate` and is reconciled by querying the durable request/outcome and publication records; it is never blindly retried. Reservations, outcomes, and tombstones outlive the retry and output-observability window, and expiry cannot silently recycle a key while an earlier effect may remain visible. Request commitments follow the confidential/low-entropy hash policy. The API claims no magical end-to-end exactly-once delivery beyond its admitted storage/publication domain.

Document text, OCR, annotations, actions, links, metadata, and external-model output are hostile data, not control. They cannot widen authority, choose tools, approve mutations, reveal secrets, or create egress. Adapters authenticate peers, isolate tenants/caches, bound schemas/results, prevent confused-deputy delegation, and log authority decisions without protected content by default.

An MCP-class transport may be offered, but no third-party protocol is pinned before freeze. The claim is not “has MCP,” stable IDs, boxes, OCR, or trust reports. It is exact byte/revision/derivation-bound anchors, least authority, ambiguity propagation, transactional multi-anchor mutation, crash-safe idempotency, signature-impact analysis, and lineage/admission receipts.

## 26. Performance and determinism program

### 26.1 Performance is a measured claim

No contract or README may call a path “fast” without:

- workload identity;
- machine fingerprint;
- denominator;
- sample distribution;
- build profile;
- variance;
- and an acceptance band.

### 26.1.1 Profile-aligned benchmarking

External comparisons are valid only when page box, resolution, annotations, optional-content state, font resolver, hinting, image interpolation, color/output profile, overprint behavior, and error policy are aligned or the differences are reported. A faster renderer that skipped an unsupported transparency group is not a performance win.

### 26.2 Workload classes

Benchmarks are stratified by:

- file open and revision indexing;
- object resolution;
- simple vector pages;
- font-heavy text pages;
- image-heavy scans;
- transparency-heavy graphics;
- large engineering drawings;
- malformed recovery;
- text extraction;
- validation;
- canonical rewrite;
- generation;
- and redaction/sanitization.

A single pages-per-second headline is rejected.

Each workload reports at least latency-to-first-result/tile, total latency, throughput, peak resident memory, total decoded bytes/work, output size where applicable, cancellation latency, and warm/cold-cache state. Server profiles also report isolation overhead and tail latency.

### 26.3 Baselines

The benchmark lab compares named versions of mature external processors under reproducible settings.

The goal is not to win every microbenchmark. The adopted baseline remains competitive throughput and memory while preserving MonkeyBee’s stronger safety and evidence contracts.

**Flagged proposed amendment — S6, not adopted:** open decision 9 may escalate a small, predeclared subset of §26.2 workloads to per-axis equivalence/non-inferiority gates and ultimately a leading Pareto or atomic result against mandatory released PDFium and MuPDF anchors plus every material eligible released native/open implementation or non-dominated set and every material eligible pure-Rust implementation for the exact end-to-end output contract, initially including hayro 0.7.1 and `pdf_oxide` 0.3.74 while requiring per-artifact characterization of the broader pool in §24.15.6. The decision rule covers latency-to-first-result, throughput, memory, cancellation, correctness/coverage, determinism, and evidence overhead; it cannot average away a material regression. Profiles, cache state, thread count, host resources, isolation, and output completeness are aligned. Contract-complete and stripped diagnostic modes are reported separately, but stripped mode cannot substantiate a supremacy claim for the ordinary product contract. Benchmark-specific paths that bypass safety, budget, or evidence contracts are disqualified. Until decision 9 is resolved through §34.5, this paragraph does not alter the baseline above.

### 26.4 Lazy and demand-driven work

Core performance principles:

- index revisions before parsing all objects;
- parse objects lazily;
- decode streams lazily;
- render pages independently where history permits;
- rasterize by tiles;
- cull with conservative bounds;
- cache decoded font and image artifacts;
- retain repeated form identity;
- avoid flattening unused semantic views;
- and make cancellation checkpoints correspond to natural work units.

### 26.5 Parallelism

Parallel levels include:

- pages;
- raster tiles;
- independent image/font decodes;
- validation rule groups;
- corpus jobs;
- and differential processor runs.

Within one page, stateful operator execution remains ordered, while emitted independent tiles or primitives may parallelize after safe dependency analysis.

### 26.6 Cache hierarchy

Caches are separated by semantic level:

- source-range pages;
- parsed object versions;
- decoded streams;
- font programs and glyph outlines;
- CMaps;
- image samples;
- color transforms;
- form display artifacts;
- raster tiles;
- text/structure views;
- and validation results.

Every cache has a bounded policy. Candidate lookup may use a conservative request/profile index, but a hit is reusable only under §9.6’s validated actual-dependency manifest, including selection-sensitive priority/absence facts; ‘profile-complete key’ never means guessing all lazy dependencies before execution.

### 26.7 Memory locality

Hot data structures favor:

- compact enums;
- arena or slab allocation scoped to operations;
- structure-of-arrays for raster edges and samples where measured;
- tile-local buffers;
- and avoidance of pointer-rich trees in hot loops.

Architecture changes require measured evidence, not aesthetic preference.

`generated-echo: constitution/MONKEYBEE_CONSTITUTION_v8.md §11.2.3`

Locality work cannot replace DoS-resistant attacker-keyed hashing with an unkeyed fast hasher by convention. Any hasher or collection swap carries the required consequence-contract threat note, complexity bound, evidence, and rollback.

### 26.8 SIMD

SIMD is considered for:

- pixel compositing;
- color transforms;
- image unpacking;
- filters;
- path coverage;
- and hashing.

Scalar reference implementations remain authoritative. Unsafe SIMD capsules must match them under exhaustive boundary fixtures and fuzzing.

### 26.9 Writer determinism

Canonical D1 output determinism—unencrypted by default, or under an explicitly admitted deterministic-signature profile—requires control over:

- admitted semantic input and unknown-extension policy;
- object allocation;
- dictionary order;
- number formatting;
- stream compression;
- object-stream grouping;
- metadata timestamps;
- identifiers;
- and cross-platform line endings.

Callers must explicitly supply or suppress nondeterministic metadata. Secure encryption uses a D1R reproducibility receipt and must not be made byte-deterministic by reusing IV/salt/nonce material. Signature output is D1 or D1R according to the fully pinned scheme/time/service contract in §§11.9 and 16.1.1; no implementation may force determinism by reusing a nonce or force randomness onto a scheme whose approved derivation is deterministic.

### 26.10 Pixel determinism

The renderer defines exact and bounded regions of the pipeline.

Exact same-build output is the first target only for the same complete input tuple: exact `RealityRoot` and `DocumentViewId`, relevant `DerivationId`/state commitment, profiles, semantic limits, feature set, font/color/host capability identities, and deterministic dependency versions. Cross-architecture identity is pursued through fixed-point coverage and pinned math where affordable.

Where ICC interpolation or optimized floating-point paths differ, the profile states a bound and the report names the source.

### 26.11 Regression policy

A performance regression becomes a failing gate only after:

- stable baseline history;
- noise model;
- machine health check;
- and acceptance band exist.

Correctness and safety are never silently weakened to make a dashboard green.

### 26.12 Performance receipts

Each benchmark row records:

- commit/build identity;
- machine and OS;
- compiler/toolchain;
- feature set;
- corpus version;
- profile;
- time and memory statistics;
- output hashes;
- and correctness-gate result.

For an S6 comparison, the receipt additionally records claim scope, lane identity, competitor released version/artifact digest, tool image, exact aligned settings, primary analysis unit, corpus/request pairing, cluster/repeated-run structure, warmup and run count, stopping/peeking rule, machine-health exclusions, minimum effect or precision target, uncertainty interval, predeclared workload/metric, evidence-overhead mode, and the orthogonal lifecycle/field-status/outcome fields. Outcomes are `leading`, `equivalent`, `non_inferior`, `trailing`, `incomparable`, `indeterminate`, or `disqualified`; `uncontested` is a field status, not a performance result.

---

## 27. The Honeycomb Gauntlet

The Gauntlet is the definition of done for claims.

### G0 — Local laws and type invariants

Examples:

- lexer round trips for preserved tokens;
- checked-offset arithmetic;
- reference identity laws, including acyclic transform-root construction, honest parentless transform authorship, and view-scoped ID non-aliasing;
- dictionary duplicate preservation;
- matrix composition;
- winding and blend algebra;
- CMap codespace laws;
- evidence non-laundering;
- report canonicalization;
- and resource-account conservation.

### G1 — Atomic standards fixtures

One fixture isolates one rule or tightly related rule family.

Fixtures are:

- minimal;
- self-describing;
- linked to `SpecCard`s;
- positive and negative where applicable;
- and independently generated or reviewed.

Coverage includes syntax, objects, operators, fonts, images, color, structure, signatures, and writer output.

### G2 — Analytic and independently implemented oracles

Examples:

- exact path geometry;
- known blend-mode equations;
- color patch values;
- font outline and metric fixtures;
- filter test vectors;
- cryptographic vectors;
- signature digests;
- and slow reference rasterization.

The oracle must not merely call the optimized implementation through another wrapper.

### G3 — Differential processor and validator evidence

MonkeyBee is compared with named external tools over a versioned corpus.

Disagreements are classified, minimized, and retained. Agreement is evidence, not proof.

### G4 — Metamorphic and round-trip properties

Examples:

- append-preserving edits leave old bytes unchanged;
- canonical rewrite reopens to equivalent declared semantics;
- page-tree rebalancing preserves order;
- rigid transforms move appearance predictably;
- split/concatenated content streams preserve execution;
- independently encoded fixtures that are semantically equivalent by construction decode to the same admitted byte/sample result (without reordering declared chains);
- object-stream packing preserves objects;
- resource renaming preserves output;
- and generated documents survive third-party open/render/extract cycles.

### G5 — Fuzzing, bombs, and malformed-input storms

Continuous fuzz targets cover:

- lexer;
- COS parser;
- xref and revision discovery;
- object streams;
- every filter and codec;
- CMaps;
- font tables and interpreters;
- content VM;
- calculator functions and the closed Bet 16 form-action frontend/VM;
- bounded static-XFA XML/binding/layout projection;
- hostile external-recognizer responses;
- agent proposal/anchor/protocol messages and prompt-injection payloads;
- ICC profiles;
- structure trees;
- signatures, evidence-envelope signer roles, and transparency proofs;
- supremacy comparison/denominator records;
- replay bundles and standalone checkers;
- writer round trips;
- and recovery search.

Special generators target:

- expansion bombs;
- deep recursion;
- cycles;
- huge dimensions;
- overlapping ranges;
- pathological paths;
- and diagnostic floods.

### G6 — Cancellation, concurrency, determinism, and replay

Tests inject cancellation at every checkpoint class and verify:

- no committed partial output;
- no leaks in tracked resources;
- short reads/writes, disk-full/quota exhaustion, broken pipes, flush/fsync/rename failures, symlink/path-replacement and no-clobber races, permission changes, and crash points around transactional publication;
- stable diagnostics;
- deterministic resume where promised;
- exact replay-relation classification without promoting repeatability into correctness;
- capture-mode observer-effect accounting;
- stale-anchor and optimistic-concurrency refusal;
- cache and tenant isolation by profile, credential, and authority;
- thread-count invariance for declared deterministic paths;
- signer-role/key-separation and log-inclusion fault cases;
- and reproducible fuzz witnesses.

### G6.1 — Toolchain, unsafe, supply-chain, and privacy lanes

Cross-cutting assurance also includes:

- Miri or equivalent interpreter checks where applicable;
- sanitizers and platform hardening for unsafe capsules and dependencies;
- concurrency model checking for cancellation/cache protocols;
- dependency advisory, license, provenance, and duplicate-version audits;
- public-API semver checks once stability is claimed;
- reproducible-build comparison;
- mutation/fault-seeding tests that measure whether the test suite catches plausible implementation defects;
- and taint/privacy fixtures proving that passwords, keys, sensitive source bytes, extracted text, attachments, and private corpus data do not enter ordinary logs or telemetry.

### G7 — End-to-end flagships and held-out evolution

The integrated system must solve the flagship workflows on documents not used to design each subsystem.

It must also absorb held-out extensions after apparent completion, such as:

- a new malformed-xref family;
- a new validation rule set;
- a new font pathology;
- a new transform receipt requirement;
- or a new binding.

The extension must inherit budgets, diagnostics, evidence, fuzzing, schemas, and operational tooling.

### 27.1 Falsifier pairing

Important claim classes require independent falsifiers.

| Claim | Required falsifier examples |
|---|---|
| Strict parse | Independent structural validator or alternate parser fixture. |
| Render fidelity | Analytic oracle, reference renderer, or minimized cross-engine comparison. |
| Unicode mapping | Source mapping cross-check, font cmap check, or held-out manual truth. |
| Secure redaction | Independent raw/decoded-object search and external forensic adapter. |
| Signature digest/cryptographic subclaim | Independent CMS/digest implementation or trusted tool comparison, with trust and legal conclusions kept separate. |
| Canonical determinism | Cross-run, cross-thread, and supported-target hash checks. |
| Recovery choice | Alternative hypothesis rendering/object comparison. |
| Profile conformance | Independent validator and profile corpus. |
| Accessibility remediation | Independent rule checker plus held-out human audit/usability review, with legal compliance kept outside automatic inference. |
| External recognition merge | Retained exact response, alternate recognizer/manual truth, hostile-schema tests, and conflict/no-laundering checks. |
| Agent-mediated edit | Root/digest replay, stale-state adversary, ordinary-API authority equivalence, prompt-injection corpus, and transform lineage audit. |
| Mechanized proof | Independent proof-kernel/checker run plus model-to-code/extraction correspondence review and trusted-base inventory. |
| GPU/CPU equivalence | Independently implemented certificate checker plus separately grounded CPU-reference correctness evidence. |
| Replay relation | Independent replay/checker of the declared relation; correctness remains separately falsified. |
| Supremacy claim | Frozen competitor/denominator/configuration record, independent score reproduction/adjudication, held-out guard, and public challenge process. |
| Performance | Correctness-gated benchmark with machine health baseline. |
| Supremacy comparison | Independent challenger audit, frozen-denominator replay, cluster/statistical reanalysis, and held-out fresh sample; omitted material competitors or optional stopping disqualify the headline. |

### 27.2 Bug-closure gate

A bug is not closed merely because one input stops failing.

Closure requires:

- minimized witness;
- classification of the violated assumption;
- regression property or atomic fixture;
- affected contract update;
- search for sibling sites;
- evidence of the fix;
- tombstone or decision record when the wrong hypothesis could recur;
- and corpus/provenance update.

### 27.3 Golden policy

Goldens are useful but dangerous.

A golden change requires:

- semantic reason;
- upstream coupling inventory;
- independent oracle result;
- review of whether the old or new output is correct;
- and a deliberate re-freeze operation.

No script bulk-regenerates goldens as an ordinary fix.

### 27.4 Release claim matrix

Each release has a machine-readable table derived from the applicable §10.10 capability consequence contracts. It maps claims to:

- `ConsequenceContractId` and supported profile;
- exact input/view identity domain and authority/precondition contract;
- Gauntlet tiers passed;
- corpus coverage;
- external observations and falsifiers;
- outcome/refusal/indeterminate algebra;
- determinism and replay class;
- performance evidence;
- privacy/artifact-availability requirements; and
- no-claim boundaries, expiry, and withdrawal state.

A manually asserted release claim that has no consequence contract—or disagrees with one—is invalid even when the underlying code path exists.

---

## 28. Corpus, institutional memory, and metabolized failure

### 28.1 Corpus classes

The corpus registry distinguishes:

1. atomic normative fixtures;
2. generated construction fixtures;
3. public conformance suites;
4. real-world licensed documents;
5. malformed recovery cases;
6. security and resource-exhaustion cases;
7. external divergence witnesses;
8. historical bug regressions;
9. generation interoperability fixtures;
10. held-out evaluation sets;
11. private or restricted corpora referenced by manifest but not redistributed;
12. hostile protocol fixtures for external recognition, agent proposals, evidence packages, logs, and replay bundles;
13. competitor-comparison denominator/sampling manifests and adjudication records; and
14. mechanized-proof/certificate positive, negative, mutation, and correspondence fixtures.

### 28.2 Every corpus item has a manifest

The manifest records:

- an internal content identity, plus a public commitment only when disclosure policy permits it;
- provenance;
- license and redistribution status;
- source date;
- personal/confidential data status;
- expected claims;
- expected no-claims;
- profile applicability;
- linked incidents, decisions, contracts, and `SpecCard`s;
- minimization history;
- and train/development/held-out partition.

### 28.3 Held-out discipline

Held-out corpora are inaccessible to implementation agents by default. The evaluation service prevents leakage through bytes, summaries, embeddings, caches, dashboards, scorer diagnostics, model-provider retention, and human side channels under project control. Provider behavior that cannot be verified is a known unknown and disqualifies the affected set from strong held-out claims.

Every held-out program has an `EvaluationProtocolId` fixing:

- who may submit, how many submissions/queries are allowed, and whether failed runs consume the budget;
- what aggregate feedback, if any, is returned before final freeze;
- whether per-case diagnostics, labels, gradients, screenshots, or category breakdowns are withheld;
- task/corpus steward, evaluator independence, model/evaluator lineage, and access logs;
- the final reveal rule and conversion of revealed cases into development/regression data; and
- a fresh replacement/reserve set sufficient for replication.

Repeated adaptive tuning against a hidden set makes it development data even if bytes were never revealed. A submission budget does not by itself preserve independence when feedback is too informative. Once a case or aggregate has shaped the implementation beyond the frozen protocol, it cannot support the original strong held-out claim; it becomes a regression fixture and a fresh independently stewarded replacement is required. Evaluation agents receive only the admitted built artifact and protocol.

### 28.4 Corpus privacy

Real documents may contain sensitive information.

The project supports:

- restricted manifests;
- encrypted local storage;
- access logging;
- derived/minimized redistributable witnesses;
- and deletion policies where law or agreement requires them.

Sensitive source bytes never appear in prompts or public logs without authorization. Public corpus manifests do not automatically publish unsalted hashes of confidential or low-entropy material; they omit the commitment, publish an access-controlled keyed commitment, or use a disclosure-approved public digest. Internal addressing, evaluator access, and public reproducibility are separate policy decisions.

### 28.5 Grammar and semantic generators

Generators produce both valid and intentionally invalid PDFs from typed models.

They vary:

- object order;
- whitespace;
- xref style;
- incremental history;
- stream filters;
- resource placement;
- page operators;
- font encodings;
- image parameters;
- structure relationships;
- and signatures.

Invalid generators declare the single violated rule when targeting atomic tests.

### 28.6 Mutation

Mutation is structure-aware where possible:

- byte-level havoc for parser robustness;
- token-level edits;
- object-graph edits;
- revision-graph edits;
- content-program edits;
- font-table edits;
- image-codec mutations;
- and policy-driven adversarial combinations.

### 28.7 Tombstones

A tombstone records a falsified hypothesis or retired rule:

- what was believed;
- which evidence killed it;
- affected code and contracts;
- corpus witnesses;
- compute and human attention spent;
- and the replacement rule.

Before an agent proposes a compatibility workaround or parser heuristic, it searches tombstones for related failures.

### 28.8 Compatibility knowledge base

The knowledge base links:

- processor observations;
- minimized witnesses;
- standard clauses;
- security analysis;
- profile decisions;
- and retirement conditions.

It is generated from structured records, not maintained as disconnected wiki prose.

### 28.9 Searchable failure signatures

Failures are indexed by:

- diagnostic codes;
- object and operator features;
- spec-card IDs;
- stack traces where relevant;
- resource-account patterns;
- visual-diff fingerprints;
- and embeddings over structured summaries.

Retrieval must cite exact authorized witnesses before influencing a new implementation decision. Embeddings and structured summaries inherit the source item's confidentiality, held-out partition, rights, and retention class; they are not a declassification mechanism. Public search indexes contain only redistributable or explicitly redacted derivatives, and deletion/restriction events invalidate downstream indexes and caches.

### 28.10 Memory success metrics

Measure:

- recurrence rate of previously tombstoned failure classes;
- time from new failure to minimized witness;
- percentage of fixes that add a general property rather than one example;
- held-out regression rate;
- and semantic duplication introduced per quarter or release cycle.

If memory grows but recurrence does not fall, retrieval or abstraction is failing.


---

### 28.11 The PDF Behavior Observatory

The PDF Behavior Observatory is the publication and governance layer over Flagship E, the §24 compatibility/supremacy laboratory, and corpus memory. Its public pages are generated views over structured observation, adjudication, claim, expiry, and withdrawal records. The authoritative records preserve source-vintage identity, exact observed artifacts, corpus rights, profiles, settings, oracle lineage, uncertainty, and no-claim boundaries; prose pages and dashboards are rebuildable snapshots rather than a second hand-maintained truth.

It publishes the compatibility ledger, minimized cross-engine divergence witnesses, expectation manifests, denominator manifests, comparison reports, and withdrawn/lapsed claims as versioned datasets and an explorer. A browser playground over the L8 WASM surface defaults to local-only processing, no upload, no ambient network/storage, strict memory/CPU/output budgets, origin isolation, and no execution of PDF active content. Any optional external recognizer or service requires an explicit disclosure and capability grant. The playground is a legibility artifact, not a weaker security profile silently presented as core behavior.

Publication obeys §4.7 and this section’s privacy rules. Redistributable witnesses may publish bytes; unredistributable witnesses publish rights-approved behavior records, redacted derivatives, and generation/retrieval recipes only. Public commitments obey confidential-hash policy. An incumbent citing a MonkeyBee witness is an aspirational external-adoption signal, not a release gate under MonkeyBee’s control.

## 29. Repository constitution and development laws

This section records only repository-level laws that are architectural or evidentiary in nature. It does not define execution units, implementation order, issue structure, coordination topology, branch policy, or launch scheduling.

### 29.1 The markdown plan remains plan space

This document owns:

- product meaning;
- user workflows;
- primitive concepts;
- architecture and layer ownership;
- cross-layer invariants;
- error and refusal semantics;
- public capability envelopes;
- evidence requirements;
- clean-room and source policy;
- major tradeoffs;
- unresolved questions;
- and kill criteria for risky ideas.

It must not drift into an implementation work ledger. When the architecture eventually stabilizes, a separate transformation may package the plan for execution. That later artifact is not authored here and must not be simulated here with numbered pseudo-work items.

### 29.2 `AGENTS.md` is a separate durable operating manual

The repository will maintain a concise `AGENTS.md` for coding-time behavior. This plan states the laws that manual must respect, but it does not attempt to encode the full day-to-day operating procedure.

At minimum, the manual must preserve:

- mission and current public capability envelope;
- truth-source hierarchy;
- clean-room restrictions;
- no-destructive-action policy;
- crate-layer rules;
- contract requirements;
- diagnostic and evidence conventions;
- dependency and unsafe-code policy;
- corpus privacy rules;
- build and test entry points;
- and escalation rules for architectural ambiguity.

### 29.3 Clean-room implementation firewall

Implementation contexts may use only source classes admitted by the project source registry, including:

- project-authored, rights-reviewed `SpecCard`s;
- raw standards or normative references only where the registry explicitly permits model-visible use;
- public errata whose terms permit the intended use;
- machine-readable models under recorded licenses;
- legally usable atomic corpora;
- generic algorithm literature under recorded terms;
- generic permissively licensed Rust dependencies;
- and black-box outputs from external processors under the experiment policy.

Existing PDF-engine source is not an implementation reference.

A contaminated implementation context is quarantined. Its outputs are inventoried, and production work restarts from an approved fresh context under independent review.

### 29.4 One crate, one enforceable contract

Every runtime or tool crate has a `CONTRACT.md` before other crates rely on its semantics.

Required sections include:

- purpose and architectural layer;
- public types and semantics;
- normative source cards;
- invariants;
- error and refusal model;
- evidence semantics;
- resource limits;
- determinism class;
- cancellation behavior;
- unsafe boundary;
- feature flags;
- external dependencies and provenance;
- conformance and fuzz targets;
- performance claims;
- and no-claim boundaries.

Contracts are checked mechanically. A crate boundary that cannot sustain a coherent contract is not a valid boundary.

### 29.5 Generated knowledge must remain derivable

Generated catalogs, diagnostic registries, profile tables, capability matrices, capability consequence contracts and their cross-surface projections, standards-derived indexes, competitor-register snapshots, supremacy claim tables, benchmark denominator manifests, and Observatory indexes must be produced by versioned generators from rights-cleared structured records. Generated output is reviewed through deterministic diffs, source-vintage identities, and source hashes.

A generated competitor or benchmark snapshot records release/main distinction, exact artifact identity, observation date, self-report versus reproduction status, uncertainty, expiry, and superseding records. Dynamic market prose and vanity statistics are never authoritative. No hand-maintained duplicate of machine-derivable truth becomes authoritative.

### 29.6 No broad blind rewrites

Broad semantic rewrites require a syntax-aware transformation, a reviewed match set, and the entire affected test envelope. Regular-expression replacement is not an architectural migration strategy.

### 29.7 No destructive cleanup by assumption

Unexpected files, corpus artifacts, generated witnesses, or concurrent work are not deleted merely because they appear unfamiliar. Destructive filesystem and Git operations require explicit authorization and a reversible plan.

### 29.8 Project memory is promoted structure, not transcript accumulation

Raw model transcripts and session logs are not automatically authoritative, permanently searchable, or publishable. They may contain secrets, personal data, held-out material, proprietary tool output, or standards content whose rights do not permit redistribution or model visibility.

Durable knowledge is promoted into:

- contracts;
- `SpecCard`s;
- decision records;
- minimized witnesses;
- regression properties;
- compatibility records;
- tombstones;
- and public no-claim boundaries.

Promotion passes source-rights, secret/PII, held-out-corpus, and retention review. The goal is metabolized history rather than an ever-growing pile of conversation.

### 29.9 Human authority remains explicit

Humans retain authority over:

- product and claim boundaries;
- architectural constitution;
- legal and clean-room interpretation;
- standards ambiguity adjudication;
- high-consequence security decisions;
- selection of genuinely independent evidence;
- release authorization;
- and termination or demotion of failed research bets.

Agents may generate and test candidate judgments. They do not silently redefine the project’s sources of truth.

### 29.10 Foundry quality is measured by coherent consequence

The development system will eventually be evaluated on:

- human review burden;
- regression rate;
- duplicate-concept formation;
- recurrence of previously understood failures;
- held-out extension success;
- source-policy compliance;
- and the fraction of new capabilities that automatically inherit the project’s budgets, diagnostics, evidence, fuzzing, compatibility, and documentation laws.

Agent count, commit count, generated lines, and raw concurrency are not success metrics.

### 29.11 Vulnerability disclosure and security response

`generated-echo: constitution/MONKEYBEE_CONSTITUTION_v8.md §11.10`

The Constitution owns intake, triage, embargo, advisory, claim-lapse, and closure law. Concrete channels and adoption remain human actions; this shell adds no independent policy text.


## 30. Provisional Rust workspace and crate atlas

This atlas is deliberately provisional. Review may merge or split crates.

The rule is not “one feature per crate.” The rule is one coherent contract per crate, with an acyclic dependency direction and a context small enough for an agent to understand.

### 30.1 Workspace conventions

- Rust 2024 edition or later pinned toolchain selected before implementation.
- Workspace lints deny unsafe code by default.
- `Cargo.lock` committed for reproducibility.
- Runtime dependencies require explicit allowlist review.
- Features identify optional profiles and frontier work; they do not silently change core semantics.
- Each crate declares an architectural layer **and package role** (`runtime`, `adapter`, `lab-tool`, `build-tool`, or `release-tool`) in package metadata.
- Runtime dependencies obey strict downward layer direction. Planning or verification relationships to corpora, external laboratories, or release tooling do not authorize a runtime dependency in the opposite direction.
- Opaque `SpecCardId`/profile/diagnostic identity types live in foundation crates. Lower layers may embed generated opaque IDs, but they do not import the L2 requirement database or the L7 source-rights tool merely to cite a rule.
- `xtask` enforces layer/role direction, contracts, source provenance, unsafe capsules, dependencies, schema versions, and claim references.


### 30.1.1 Crate-boundary budget

`generated-echo: constitution/MONKEYBEE_CONSTITUTION_v8.md §30.1.1`

The Constitution is the sole normative home. The remaining atlas is provisional shell content.

### 30.2 L0 — Foundation

| Crate | Responsibility |
|---|---|
| `mb-core` | Stable IDs, versions, common scalar types, source identities, project-owned `NonEmptyVec<T>`, and bounded utility primitives. |
| `mb-budget` | Work contexts, limits, cancellation, resource accounting, and fallible reservation helpers. |
| `mb-diag` | Structured diagnostics, locations, codes, project-owned bounded collectors, safe observer-batch adapters, schema renderers, and diagnostic budgets. |
| `mb-evidence` | Claims, evidence facets, composition rules, provenance, and refusal semantics. |
| `mb-profile-core` | Opaque profile/snapshot/capability IDs, canonical profile identity, and representation-neutral degradation/trace policy primitives; no PDF-specific composed registry. |
| `mb-hash` | Domain-separated content hashing and canonical identity encodings. |
| `mb-obs` | Structured events, metrics, machine fingerprints, operation receipts, replay-trigger records, and trace-mode/observer-effect envelopes; no ambient export authority. |
| `mb-exec` | Optional shared worker pools and page/tile scheduling over explicit work contexts. |
| `mb-cache` | Bounded content-addressed derivation caches with profile-complete keys and data-sensitivity policy. |
| `mb-geom` | Representation-neutral finite scalar, affine matrix, point/rectangle, path-command, and conservative-bound primitives shared by page execution and appearance. |

### 30.3 L1 — Bytes, syntax, revisions, and streams

| Crate | Responsibility |
|---|---|
| `mb-bytes` | ByteSource implementations, checked ranges, spooling, segmentation, and source manifests. |
| `mb-lex` | File-syntax tokenization with exact spans and source-preserving tokens; content, CMap, calculator, and font languages retain dedicated frontends. |
| `mb-cos` | Raw COS values, exact lexical representation, dictionaries with duplicates, and serialization primitives. |
| `mb-xref` | Classic xrefs, xref streams, hybrid structures, entries, and section validation. |
| `mb-revision` | Revision graph, trailers, effective mappings, object occurrences, and history queries. |
| `mb-stream` | Stream boundaries, decode parameter model, virtual decoded spans, and stream caches. |
| `mb-filter` | PDF filter-chain semantics, normalized stage parameters, transactional canonical sample-byte decoder/encoder protocols, and optional terminal typed-plane fast-path contracts; no security-handler or codec implementation ownership. |
| `mb-codec-ccitt` | CCITT Fax decode/encode and PDF parameter adaptation. |
| `mb-codec-jbig2` | JBIG2 parser/decoder with strict budgets and security-focused contracts. |
| `mb-codec-jpx` | JPEG 2000/JPX parsing and decode adapter or implementation. |
| `mb-codec-jpeg` | PDF DCT/JPEG adaptation over an audited generic codec. |
| `mb-security` | Encryption dictionaries, standard and admitted public-key security handlers, crypt-stage implementation over `mb-filter` protocols, key-provider boundaries, and decrypted-value provenance; no stream-planner or object-resolver dependency. |

### 30.4 L2 — Document and recovery

| Crate | Responsibility |
|---|---|
| `mb-object` | Object-version resolver, cycles, decryption context, and typed object access. |
| `mb-document` | Catalog, page tree, inheritance, names/numbers, destinations, outlines, high-level document facade, and source-preserving structural carriers for rare document-level features. |
| `mb-dialect` | Effective version/dialect computation across header, catalog override, extension declarations, feature requirements, historical revision context, and write targets. |
| `mb-spec` | Compact immutable runtime requirement metadata and indexes keyed by opaque foundation `SpecCardId`s; no raw licensed standards corpus and no downward dependency from foundation/byte crates. |
| `mb-arlington-rules` | Generated normalized Arlington-derived rule data and runtime object-model validation bridge; the importer itself is tool-only. |
| `mb-validate-core` | Lexical, file, COS, and relationship validation framework. |
| `mb-repair` | Bounded recovery hypotheses, admissibility gates, Pareto/partial ordering, alternatives, task-local selection, and recovery reports. |
| `mb-metadata` | Info dictionary, XMP, identifiers, dates, XML safety, and metadata reconciliation. |
| `mb-linearized` | Linearization parsing, hint models, and progressive-access validation only. |

### 30.5 L3 — Page programs

| Crate | Responsibility |
|---|---|
| `mb-content` | Content tokenization, operator nodes, inline-image parsing, and program preservation. |
| `mb-operator` | Typed PDF operator definitions, admission rules, and generated catalogs. |
| `mb-gstate` | Graphics-state values, persistent stack, and state-transition semantics. |
| `mb-resource` | Scoped resource resolution, cache keys, and missing-resource diagnostics. |
| `mb-functions` | PDF function types and the bounded Type 4 calculator VM. |
| `mb-ocg` | Optional-content groups, configurations, expressions, and visibility traces. |
| `mb-font-protocol` | Format-neutral font execution requests/results, source-code segmentation, glyph/metric/outline descriptors, Type 3 procedure descriptors, and the injected `FontExecutionService` trait; no font-format implementation. |
| `mb-pagevm` | Metered page-program execution and appearance/semantic/trace sink orchestration over injected resource/font protocols. |

### 30.6 L4 — Appearance

| Crate | Responsibility |
|---|---|
| `mb-path` | Appearance-level path normalization, curve flattening, stroke expansion, winding, and clip geometry over `mb-geom` primitives. |
| `mb-raster` | Reference and optimized tile rasterizers, coverage, and clip masks; an optional Bet-25 GPU producer may live as an internal/feature-gated path here, but receives no new-crate entitlement and cannot serve as its own certificate verifier. |
| `mb-composite` | Transparency groups, blend modes, soft masks, and premultiplied compositing. |
| `mb-color` | PDF color spaces, tint transforms, rendering intents, and colorant-aware values. |
| `mb-icc` | ICC parsing, transforms, profile caches, and profile-specific no-claims. |
| `mb-image` | Image XObjects, sample unpacking, masks, interpolation, and image provenance. |
| `mb-pattern` | Tiling-pattern semantics and caches. |
| `mb-shading` | Function, axial, radial, and mesh shading evaluation. |
| `mb-font-type1` | Type 1 font and charstring support over `mb-font-protocol`. |
| `mb-font-cff` | CFF/Type 2 charstrings and CID-keyed CFF support over `mb-font-protocol`. |
| `mb-font-truetype` | TrueType/OpenType parsing, outlines, composites, cmaps, and hinting VM over `mb-font-protocol`. |
| `mb-cmap` | PDF CMap and ToUnicode parsing/evaluation over format-neutral mapping types. |
| `mb-font` | PDF font-resource orchestration, format dispatch, resolver/substitution policy, glyph caches, and the concrete `FontExecutionService`; depends on `mb-font-protocol` and format crates, which never depend on `mb-pagevm` or back on the orchestrator. |
| `mb-render` | Page render planner, tile scheduling, output surfaces, and render reports. |

### 30.7 L5 — Semantics and behavior

| Crate | Responsibility |
|---|---|
| `mb-text` | Glyph-instance graph, Unicode evidence, geometry, words/lines, reading-order hypotheses, and schema-validated merging of hostile external-recognition results without evidence laundering. |
| `mb-structure` | Tagged-PDF structure, parent tree, namespaces, attributes, and accessibility linkage. |
| `mb-annot` | Structural annotation types, appearance references, replies, destinations, and policy-neutral annotation semantics; no rendering dependency. |
| `mb-annot-render` | Annotation appearance selection/execution adapter over `mb-annot`, page-program, font, and appearance contracts. |
| `mb-form` | AcroForm field graph, values, widgets, existing-appearance selection, dynamic-state evidence, and an internal closed-language parser/interpreter for optional Bet 16 metered field-state transactions over the shared sandbox protocols; the script-free base path remains independent, and no new crate is implied until the crate-boundary budget is met. |
| `mb-action` | Active-content/action inventory, the shared executable-feature and trigger registry, policy classification, and neutralization planning used by both Bet 16 execution admission and sanitization parity checks. |
| `mb-signature` | Signature fields, ByteRange, CMS/CAdES structure and primitive verification, revision analysis, and reports; trust stores, clocks, and revocation remain explicit host adapters. |
| `mb-attachment` | File specifications, embedded/associated files, extraction, and security inventory. |
| `mb-diff` | Extensible byte/object/program/appearance/glyph/text/structure/security diffs; read-only axes register without depending on the writer/editor. |

### 30.8 L6 — Authoring and transformation

| Crate | Responsibility |
|---|---|
| `mb-write` | Canonical and incremental serialization, object allocation, xrefs, trailers, and stream encoding. |
| `mb-author` | Document builder and typed page/canvas APIs. |
| `mb-layout` | Structured authoring, shaping adapters, line/page layout, tables, and tagged output. |
| `mb-font-subset` | Font glyph closure, subsetting, encoding, embedding, and ToUnicode generation. |
| `mb-edit` | Immutable edit transactions, typed semantic anchors, stale-root/digest validation, propose→validate→apply semantics, lower-layer validation, private candidate finalization, and internal receipts; no laboratory dependency or final external-assurance authority. |
| `mb-transform` | Rewrite policies, canonicalization, optimization, flattening, bounded static-XFA projection orchestration, and transform receipts. |
| `mb-redact` | Redaction intent, content surgery, full-rewrite removal, and negative-evidence checks. |
| `mb-sanitize` | Versioned active-content, attachment, form, metadata, and history sanitization policies. |
| `mb-repair-write` | Serialize recovered hypotheses into strict outputs with explicit repair receipts. |
| `mb-form-appearance` | Policy-defined AcroForm/widget appearance generation and appearance-stream writing without executing unsupported dynamic logic. |
| `mb-linearized-write` | Linearized output planning, hint-stream construction, layout closure, and progressive interoperability. |

### 30.9 L7 — Assurance and laboratory tooling

| Crate | Responsibility |
|---|---|
| `mb-package` | Evidence-package and replay-bundle construction, canonical encoding, content roots, purpose-bound envelopes, explicit signer-role metadata, and the transparency-log protocol (commitments, signed checkpoints/tree heads, inclusion/consistency proofs, revocation/tombstone records, witness/monitor metadata); it does not operate a network log service. Release-manifest, operation-signing, log, and checker roles remain distinct. |
| `mb-validate` | Profile engine and integrated validation report facade. |
| `mb-profile-pdfa` | PDF/A profiles and source/rule imports. |
| `mb-profile-pdfua` | PDF/UA profiles and machine-verifiable accessibility rules. |
| `mb-trace` | Pixel-, glyph-, object-, signature-, and transformation-explanation graphs. |
| `mb-diverge` | External-processor experiment normalization, witness minimization, and divergence reports. |
| `mb-checker` | Minimal hostile-input standalone package checker with no renderer/editor dependency and an independently implemented package parser/canonical-root verifier rather than reusing the producer’s encoder path; optional Bet-25 certificate verification uses an independent scalar/formal relation checker and never reuses the GPU shader or producer arithmetic path. |
| `mb-corpus` | Corpus manifests, partitions, licensing, retrieval, generation, and tombstones. |
| `mb-fuzz-support` | Shared structure-aware generators, mutators, sanitizers, and witness serialization. |
| `mb-bench` | Correctness-gated benchmarks, canonical denominator manifests, competitor artifact/configuration records, paired/cluster-aware analysis, repeated-run/stochastic attempt accounting, stopping and multiplicity rules, non-inferiority/Pareto/incomparability analysis, uncertainty, machine fingerprints, supremacy comparison reports, and regression analysis. |
| `mb-foundry` | Production ledger, agent-run manifests, baselines, ablations, and foundry evaluation. |
| `mb-spec-tool` | Source-rights registry, authorized `SpecCard` workflow, Arlington importer, coverage generation, model-visibility scanning, competitor observation/register generation, and mechanized-proof artifact/correspondence ingestion; never a shipped parser dependency. |

### 30.10 L8 — Product surfaces and policy tools

| Crate | Responsibility |
|---|---|
| `mb-profile` | Versioned caller-facing processing-profile registry and compiler to immutable layer-local policy views; depends downward but is never imported by lower layers. |
| `monkeybee` | High-level Rust facade, semantic-anchor and proposal coordination, capability discovery, and optional assurance/publication coordination across private L6 candidates and released L7 checks; preview until the first public compatibility contract is explicitly frozen. |
| `mb-cli` | Command-line interface and deterministic structured output. |
| `mb-capi` | C ABI and generated headers. |
| `mb-wasm` | WebAssembly bindings and restricted capability surface. |
| `mb-server` | Optional service and MCP-class protocol orchestration, authentication, tenant isolation, least-authority delegation, stale-proposal checks, quotas, streaming, egress control, and audit; if open decision 4 admits a self-hosted transparency service, publication/monitor endpoints live here or in a non-core adapter while `mb-package` retains protocol semantics. |
| `xtask` | Repository policy, generated source, contract, layer, claim, corpus, and release checks. |

### 30.11 Crate-boundary review questions

Before freezing this atlas, ask for every boundary:

- Does it carry a real semantic contract or merely a naming preference?
- Can an agent understand the crate with its dependencies in one context?
- Does the boundary force information loss?
- Does it create circular ownership of a PDF concept?
- Will errors and evidence compose across it?
- Is it likely to require lockstep changes so often that separation adds friction?
- Does it permit an independent reference or fuzz target?

Crates that fail these questions are merged or redesigned before workspace freeze.

For evidence-package assurance, code reuse itself is reviewed as a correlation source. Producer and checker may share stable schema identifiers and audited cryptographic primitives, but not the same canonical decoder, structural completeness walk, or Merkle/root construction implementation. Shared test vectors include independently authored malformed packages designed to make the producer and checker disagree loudly if either interpretation drifts.


---


## 31. Flagship campaigns

The flagships are forcing functions. Each crosses many layers and has an explicit “what breaks first” clause.

### 31.1 Flagship A — The Impossible Document Autopsy

**Input**

A deliberately hostile document containing:

- multiple incremental revisions;
- valid and invalid xref sections;
- object streams;
- hybrid references;
- encryption;
- signatures;
- composite and Type 3 fonts;
- unusual CMaps;
- transparency groups and soft masks;
- patterns and mesh shadings;
- optional content;
- forms;
- JavaScript and launch actions as inert data;
- embedded files;
- tagged structure;
- hidden/clipped text;
- and at least two materially plausible recovery paths.

**Required behavior**

MonkeyBee:

1. produces strict and recovery reports separately;
2. reconstructs the nondominated revision chains admitted within the declared search envelope and marks the result partial when the budget prevents exhaustive search;
3. maps every object occurrence and signature-covered range;
4. inventories hidden, historical, attached, and active content;
5. renders under strict and named compatibility profiles;
6. extracts glyphs/text with evidence;
7. validates structure and selected profiles;
8. explains selected pixels, glyphs, and security findings to bytes;
9. identifies cross-engine disagreements;
10. minimizes at least one disagreement witness;
11. proposes repairs without mutating the source;
12. emits a standalone evidence package.

**Success artifact**

A navigable autopsy bundle in which every headline has a source and every ambiguity is visible.

The deliberately constructed torture file is only the transparent fixture. Release evidence also includes withheld real-world hostile documents selected by an independent corpus steward after the autopsy pipeline is frozen; otherwise the flagship would prove only that the system can explain the pathology it was designed around.

**What breaks first**

Likely pressure points:

- ambiguous recovery combinatorics;
- signature/CMS trust dependencies;
- JPX/JBIG2 corner cases;
- font substitution;
- and nested transparency performance.

The campaign remains honest by allowing bounded partial outputs with exact no-claims.

### 31.2 Flagship B — Semantic Surgery Without Visible Change

**Input**

A real-world, untagged, poorly encoded, image-and-text document with:

- missing or incomplete ToUnicode;
- irregular reading order;
- redundant images and fonts;
- active content;
- annotations;
- metadata conflicts;
- and accessibility failures.

**Requested transformation**

- make text searchable where justified;
- improve reading order;
- add tagged structure and language metadata;
- add or repair alternate text with explicit human/heuristic provenance;
- remove active content;
- optimize file size;
- preserve visible appearance within a declared pixel envelope;
- preserve navigation;
- and produce an accessibility/profile report.

**Required evidence**

- page-by-page visual diff;
- glyph/text diff;
- structure diff;
- security inventory diff;
- external renderer matrix;
- independent accessibility validator comparison;
- and explicit list of semantic decisions requiring human approval.

**What breaks first**

Automated semantic inference, especially reading order and alternate text.

The system must refuse to call heuristic structure “author intent.”

### 31.3 Flagship C — Intent-to-Interoperable-PDF Compiler

**Input**

A declarative document intent containing:

- semantic structure;
- text and language;
- figures and descriptions;
- links;
- tables;
- style constraints;
- target page sizes;
- target file-size budget;
- required PDF/A or PDF/UA profile;
- target viewer matrix;
- and deterministic-build requirement.

**Compiler behavior**

MonkeyBee generates candidate encodings varying:

- font subsets and encodings;
- image compression;
- object streams;
- resource reuse;
- content-stream decomposition;
- color/output-intent choices;
- and layout alternatives.

Candidates are checked against:

- MonkeyBee strict reader/renderer;
- target profiles;
- external processors;
- text extraction;
- accessibility rules;
- size/performance budgets;
- and deterministic output.

The selected artifact is the smallest or cheapest candidate satisfying the complete constraint set, not merely the first valid file.

The compiler reports the complete search envelope: candidate count, generators, retries, evaluation cost, selection rule, rejected alternatives, and whether the result is best-of-many. “Smallest” means smallest among the evaluated admissible candidates under that declared search, never a global optimum unless an independently checkable proof establishes it.

**What breaks first**

Authoring layout breadth and font/shaping interoperability.

The initial compiler supports a constrained document language and expands only through held-out authoring challenges.

### 31.4 Flagship D — Secure Redaction With Negative Evidence

**Input**

A signed, incrementally updated document containing the target information in:

- visible text;
- invisible text;
- clipped content;
- form XObjects;
- optional-content layers;
- annotation appearances;
- metadata;
- ActualText;
- attachments;
- an earlier revision;
- and a raster image.

**Requested transformation**

Remove the target information and produce a new PDF with a declared security policy.

**Required behavior**

- enumerate exact target occurrences and discovered heuristic candidates, while reporting heuristic coverage and unknown regions rather than claiming exhaustive semantic discovery;
- require confirmation where mapping is ambiguous;
- remove historical revisions through canonical rewrite;
- surgically rewrite content or rasterize only under explicit loss policy;
- remove metadata and attachments;
- reopen and render output;
- run raw and decoded byte searches;
- run glyph/text/structure searches;
- run optional OCR adapter on images if requested;
- run one independently authored forensic tool under a recorded protocol;
- run a second independently sourced forensic path, disclose parser/model/data lineage for both paths, and treat shared or unknown lineage as correlated rather than as two independent falsifiers;
- and report signature destruction or replacement.

**Success artifact**

The PDF plus a negative-evidence package whose claim is scoped to the enumerated search and transformation mechanisms.

**What breaks first**

Reliable semantic targeting inside images and badly encoded fonts.

The system preserves uncertainty rather than silently leaving or over-removing content.

### 31.5 Flagship E — Viewer Divergence Atlas

**Input**

A large, license-cleared corpus processed by a matrix of current and historical PDF engines, validators, and selected printer/RIP environments.

**Campaign behavior**

- capture outputs and settings;
- cluster material disagreements;
- minimize representative witnesses;
- locate causal objects/operators;
- compare rights-cleared `SpecCard`s and public errata, with authorized human source adjudication where the controlling standard must be consulted;
- classify conforming, malformed, implementation-defined, or unresolved behavior;
- create compatibility rules only when justified;
- and publish reproducible evidence bundles.

**Success artifact**

A versioned atlas of PDF semantic fault lines that is useful independently of MonkeyBee. Through Bet 21 and §28.11, the atlas also becomes the PDF Behavior Observatory: a public compatibility ledger, witness dataset, expectation-manifest corpus, explorer, and WASM playground, subject to rights and privacy gates.

**What breaks first**

External tool reproducibility, licensing, device availability, and defining material versus inconsequential difference.

### 31.6 Flagship F — The Evolution Trial

After a release candidate satisfies its declared envelope, independent evaluators select three held-out extensions, for example:

- a previously unsupported standardized profile;
- a new font or codec pathology;
- a new streaming requirement;
- a signature attack class;
- or a new host binding.

The foundry must implement them without special architectural exemptions.

Measure whether each extension automatically inherits:

- source provenance;
- budgets;
- diagnostics;
- evidence;
- cancellation;
- fuzzing;
- corpus memory;
- schemas;
- documentation;
- compatibility analysis;
- release claims;
- and rollback.

This is the primary lineage test.

---

Continuing §31, whose campaigns already run A–F (31.1–31.6, ending with the Evolution Trial), these campaigns are G–J at 31.7–31.10. Each is a forcing function with a "what breaks first" clause. Flagships G and H are the competitive-comparison center of gravity.

### 31.7 Flagship G — Hostile Legacy Execution [M]

**Input:** real AcroForm documents whose observable state depends on admitted calculate/format/validate actions; XFA documents with bounded statically projectable content; and documents carrying PostScript XObjects or related deprecated constructs.

**Required behavior:** (1) execute the admitted form-action subset as an atomic field-state transaction with pinned locale/time/clock inputs, event/dependency order, cycle handling, resource receipt, and no partial publication; (2) compare final field values, formatted appearances, and refusals—not merely isolated script return values—against named reference profiles; (3) project the admitted static XFA subset while marking every ignored, dynamic, ambiguous, or fixed-layout no-claim region; (4) apply declared PostScript-XObject policies; (5) make every path cancellable and least-authority; and (6) prove sanitizer/interpreter parity over the shared executable-feature registry.

**Success artifact:** a versioned legacy ledger of matched, bounded-mismatch, partial, indeterminate, and refused outcomes with field-level and region-level receipts.

**What breaks first:** event ordering and cross-field mutation, date/locale quirks, XFA binding/layout, state rollback, and budget calibration. **Honesty clause:** partial coverage with exact no-claims beats emulation theater; no “form works” headline may hide stale or partially committed state.

### 31.8 Flagship H — The Wild-Tail Ledger [F]

**Input:** the S2 rights/privacy-reviewed, deduplicated, stratified, independently stewarded sample drawn after the pipeline, cutoff, comparator eligibility, profiles, and thresholds freeze.

**Required behavior:** open/render/extract where declared; typed partial/refusal accounting; per-stratum uncertainty; standards/multi-oracle/expert adjudication of correctness; and explicit indeterminate treatment for unresolved malformed or implementation-dependent cases. The document is the primary analysis unit; page/region observations remain paired clusters. Credential-blocked, policy-blocked, timeout, resource, unsupported, and incomplete outcomes never disappear into one failure bucket. Competitor artifacts, configurations, claim scope, and stopping rule are pinned.

**Success artifact:** a public, versioned ledger that remains publishable whether MonkeyBee leads or trails. A supremacy headline exists only for uncertainty-aware leading subclaims; equivalent or non-inferior results retain those names.

**What breaks first:** sample representativeness, protected/private files, oracle disagreement, codec/font tail risk, and pressure to tune thresholds. The antidote is predeclared strata and transparent indeterminacy, not a larger flattering aggregate.

### 31.9 Flagship I — The Structured-Extraction Crossing [F]

**Input:** a reproducible run of the selected public benchmark under its actual metrics plus an independently stewarded held-out corpus and a structured-output interoperability set.

**Required behavior:** independently reproduce benchmark scoring; disclose benchmark ownership, non-runnable preserved predictions, corpus exposure, model/GPU/locality settings, per-engine configuration, primary analysis unit, and any stochastic attempt/selection policy; emit text, boxes, hierarchy, tables, and page images only for declared profiles; and preserve per-span byte/revision/derivation or external-recognition evidence. Quality, speed, determinism, locality, refusal honesty, page/bbox source evidence, and exact provenance remain separate axes.

**Success artifact:** a public scorecard and evidence explorer. “Leaderboard crossing” means the quality threshold is actually crossed; otherwise the artifact may still demonstrate the strongest earned deterministic/local/provenance conjunction without misnaming it leadership.

**What breaks first:** multi-column and table order, benchmark leakage, scorer assumptions, OCR/model version drift, and the temptation to treat provenance as bonus points on a quality score. Bet 20 composition is the honest fallback for model-dependent regions.

### 31.10 Flagship J — The Remediation Audit [F/M]

**Input:** untagged or badly tagged documents with independent accessibility audits and competitor auto-tagged outputs, selected after remediation policy freeze.

**Required behavior:** Workflow O end to end; named target profile; structure/order/language/association receipts; caller or external evidence for alternate descriptions; independent machine-verifiable checks; human-review obligations; visual/text/navigation preservation comparison; and explicit refusal where inferred structure cannot be defended.

**Success artifact:** before/after audit deltas and a claim-by-claim comparison with the strongest eligible auto-tagging/remediation system. A validator pass remains one subclaim and cannot establish usability or authorial intent.

**What breaks first:** intended reading order, tables, figures/alternate text, malformed existing tags, shared-object surgery, and checker/oracle correlation. MonkeyBee never hallucinates image descriptions as exact document truth; externally generated descriptions remain external evidence or are refused.

## 32. Risk register, early warnings, and kill criteria

| Risk | Severity | Early warning | Mitigation | Kill or fallback |
|---|---|---|---|---|
| ISO/standards text enters AI context without permission | Critical | Raw normative excerpts appear in prompts, retrieval stores, implementation artifacts, or generated comments | Per-source AI-use rights gate; human-reviewed SpecCards; scanner; legal incident workflow | Stop affected work, quarantine outputs, re-author cards and implementation under approved inputs. |
| Source-only Honeycomb root excludes authoring | Critical | Generator invents fake byte spans or maintains a second object universe | Source/Draft/Transform roots plus first-class draft and derived origins with typed lifecycle transitions | Freeze authoring work until one identity/origin model serves read, write, and transform paths. |
| Evidence facets encode contradictory no-value states | Critical | A `Claim<T>` can be both refused and carry an ordinary value | `ClaimOutcome<T>` outside evidence facets; distinct partial type; capability-gated constructors; claim-specific composition | Reject schema and packages using the old shape; migrate before implementation. |
| Secure encryption is made deterministic | Critical | Repeated IV/salt/nonce material or byte-identical encrypted files | Separate entropy policy; deterministic test mode forbidden in releases; nonce uniqueness gate | Disable encryption writing until secure entropy and vectors pass. |
| Encrypted editing is implied without an output-security implementation | Critical | R2 append/canonical APIs accept encrypted input but fresh encryption semantics have not been designed | R2 explicit refusal; the secure-writer profile in the transformation/security envelope; capability-typed write admission | Refuse encrypted output until the secure profile and external vectors pass. |
| Remote source mutates beneath a cached identity | Critical | Same source ID yields different bytes or stale derivations | Immutable snapshot tokens, verified content IDs, ephemeral cache class, validator recheck | Invalidate root and every derivative; refuse preservation/write from unstable source. |
| Recursive/unsized provenance representation reaches implementation | Critical | Origin graph sketch or schema embeds `OriginRef` inside itself rather than using IDs | ID-backed `OriginRecord`; compile-time schema fixture; canonical graph serialization | Block foundation merge until the type is finite, acyclic-by-storage, and fuzzed. |
| Codec-aware filters are assumed terminal or bypass canonical filter-chain bytes | Critical | Legal or compatibility-relevant declared chains are refused, reordered, or decoded differently by the typed-plane fast path | Exact declared-order canonical sample-byte path for every admitted codec; metadata sidecars; terminal typed-plane optimization only under equivalence evidence | Disable typed-plane fast paths and use canonical byte chaining until the equivalence and stage-layout contracts pass. |
| Codec inspection consumes the only decode stream | High | Metadata inspection changes later decode bytes or requires ad hoc rewind | Immutable `DecodeSource`; independent cursors for inspect/decode; source identity in receipts | Reject codec adapter until cursor-independence tests pass. |
| Partial page sinks become visible after failure | Critical | A failed fanout leaves committed pixels, glyphs, or traces with inconsistent scope | Transactional sink begin/commit/abort; fanout outcome algebra; cancellation tests | Refuse multi-sink release until atomicity/fanout semantics are proven. |
| Mutable host capability breaks replay | High | Same resolver/trust-store label yields different font, color, or trust result | Bind exact effective bytes/snapshot/version; operation-local only when no stable identity exists | Downgrade determinism/cache claim or refuse persistent receipt. |
| Lazy dependency discovery makes cache lookup unsound | Critical | A lookup omits a used resource or an absence/priority fact—such as a newly preferred fallback font—because “actually used” dependencies were not known before execution | Two-stage candidate index plus authenticated actual-dependency and selection-witness manifest; exact deterministic preflight only where proved; rerun selection or match the full relevant authority snapshot; partition candidate indexes by tenant/security/sensitivity/disclosure domain; `DerivationId` minted after validation | Treat as cache miss/refusal, disable affected durable cache/index class, and invalidate entries produced under the unsound key grammar |
| Generic deterministic seed is reused as encryption/signature nonce material | Critical | Authoring RNG and cryptographic key/nonce generation share one capability, caller-supplied seed, or reusable value | Distinct encryption-entropy, signer/key-operation, and non-security seed capabilities; scheme-specific nonce admission; non-secret health/derivation receipt | Disable affected crypto path and rotate/remediate keys or nonce state where applicable. |
| Layer ownership, runtime dependencies, and public capability claims disagree | Critical | Page/document crates depend upward on appearance/writer/lab crates, or one feature compiles only through semantic cycles | Shared foundation geometry; package-role metadata; strict runtime-layer rules; generated dependency audit | Stop downstream work and split or move the semantic owner before implementation. |
| Page execution and font implementation form a semantic dependency cycle | Critical | Page VM imports format crates while Type 3/font code calls back into the VM | Lower `mb-font-protocol`, injected `FontExecutionService`, VM-owned Type 3 subprogram execution | Freeze text rendering until dependency direction and conformance fixtures prove the cycle is gone. |
| Transform core depends upward on validators/laboratories | Critical | Writer/redactor imports external-tool adapters or can publish a strong headline without the independent gate | Private L6 candidate boundary plus L8 assurance/publication coordinator over released L7 checks | Split publication authority; withhold independent-check headline until coordination path exists. |
| Cross-root IDs are treated as globally stable identities | High | Rewrites/imports reuse source-bound IDs or caches alias distinct roots | Root-scoped IDs plus explicit evidence-bearing lineage maps | Invalidate cross-root cache/reference assumption and migrate through mappings. |
| Content identities are treated as collision-proof authority | Critical | Wrong artifacts deduplicate, package claims alias, or attacker-selected bytes inherit another artifact's trust | Versioned domain-separated identity grammar; class/length/byte recheck on insertion; explicit collision quarantine; hashes never authorize policy | Disable cross-artifact deduplication/public commitment for the affected identity version and migrate to a new grammar. |
| Run telemetry contaminates deterministic report identity | High | Same semantic result hashes differently because wall time/timestamp/event order changed | Semantic report body separated from observation envelope | Recompute identities and invalidate affected deterministic-report claims. |
| Source snapshot changes after identity is assigned | Critical | Repeated range reads differ, mmap truncation faults, or hash identity no longer matches bytes | Spool/copy/platform snapshot or page revalidation; `SourceChanged` invalidation; no persistent claim from mutable source | Abort operation, invalidate derivations, reopen as a new root. |
| Sensitive derived data leaks through cache/spool/telemetry | Critical | Decrypted streams, attachments, text, pixels, or corpus bytes appear in ordinary caches/logs/core dumps | Sensitivity classes, secret policy, encrypted temporary storage, protected trace class, host-isolation guidance | Disable persistence/export path and treat as security incident. |
| Decrypted/cache artifacts cross credential or tenant boundaries | Critical | Same encrypted root/profile reuses plaintext derived under another authorization context | Non-secret security-context identity, tenant/cache partitioning, no durable plaintext cache by default, cross-context tests | Invalidate affected caches, disable shared cache class, and treat exposure as security incident. |
| Cryptographic implementation is described as side-channel-proof | High | Timing/cache/provider behavior leaks credential-dependent differences outside tested primitive boundaries | Vetted constant-time primitives, uniform failure paths where practical, explicit whole-process no-claim, isolation guidance | Narrow claim and disable high-assurance profile until measured threat model passes. |
| Published content hashes disclose confidential membership | High | Public package/telemetry digest can be guessed against a low-entropy or known corpus | Separate internal addressing from public commitments; omit or key commitments by disclosure policy | Revoke/publicly replace affected package and rotate keyed commitment context. |
| Writer claims atomicity/durability beyond host sink | Critical | Short write, ENOSPC, crash, rename/fsync failure, symlink/path replacement, pre-existing destination race, or permission drift leaves output described as rolled back or durable | `TransactionalOutput` commit classes; admitted directory capability; exclusive no-follow/no-clobber private file; destination revalidation; fault injection around every publication point | Downgrade receipt, preserve source, and refuse release helper until platform semantics are measured. |
| Embedded payload inventory is mistaken for nested safety | High | Attachment metadata looks benign while nested PDF/archive contains active content or secrets | Opaque-by-default payloads; optional recursive adapters; cumulative budgets; explicit no-claim | Remove/sandbox payload or report uninspected nested content. |
| Diagnostic limits hide the only severe finding | Critical | Report is called complete after truncation or low-severity floods evict security errors | Reserved severity capacity, deterministic summaries, explicit truncation outcome | Revoke affected reports/claims; diagnostic truncation is a release blocker. |
| Host diagnostic observer re-enters, blocks, or leaks protected data | Critical | A callback runs while core locks/state are live, recursively invokes MonkeyBee, stalls progress, or retains source/secrets | Project-owned `DiagnosticCollector`; redacted immutable batches only at safe adapter boundaries; observer has no semantic authority | Disable observer bridge, preserve collector summary, and treat protected-data retention as a security incident. |
| Evidence package checker can be resource-exhausted | Critical | Standalone checker parses unbounded package graphs/blobs | WorkContext/limits on package ingest and checking; content-size/depth caps | Do not publish checker as a security boundary until hostile-package gates pass. |
| Evidence-package identity is ambiguous or serialization-dependent | Critical | Producer and checker hash different semantic objects, map order changes roots, or duplicate/extension fields alias | Versioned domain-separated length-framed canonical grammar, typed ordering, dual implementations, hostile ambiguity corpus | Refuse package-integrity headline and freeze protocol evolution until root equivalence is proved. |
| Package signature is mistaken for authorization | Critical | Detached or replayed signature verifies cryptographically and is treated as release approval | Purpose-bound envelope over exact root/protocol/context/role/freshness; separate integrity, authentication, trust, authorization, and admission outcomes | Ignore signature for release admission; retain only cryptographic observation until policy chain is valid. |
| Candidate receipt is conflated with independently assured release | Critical | Transformation core cites its own checks as external evidence or publishes before assurance completes | Immutable candidate `TransformReceipt`, separate `AssuranceAdmissionReceipt`, L8 publication authority | Keep candidate private or downgrade to internal-check profile; never rewrite history to simulate admission. |
| Page-VM fanout couples unrelated sink failures | High | Text quota changes pixels or renderer failure is reported as complete extraction | Explicit fanout policy, fallible metered sinks, per-result coverage | Disable multi-sink optimization; execute sinks independently until semantics are proven. |
| Page VM conflates saved graphics state with current path/text execution state | Critical | `q`/`Q`, `BT`/`ET`, `W`/`W*`, or Form invocation restores/applies the wrong state and corrupts later content | Separate state machines; boundary-specific clipping; atomic unbalanced-state and Form-containment fixtures | Disable affected renderer path and fall back to traced reference execution until semantics agree. |
| Standards technical specifications are classified under the wrong family | High | Crypto/hash extensions and accessibility/WTPDF rules share one misleading contiguous technical-specification switch | Separate 32001–32004 PDF 2.0 technical profiles from 32005 accessibility reuse; versioned registry review | Revoke affected capability/profile claims and rebuild the registry/cards before implementation. |
| Effective PDF dialect is inferred from the header alone | Critical | Catalog `/Version`, extensions, feature requirements, or historical revisions are ignored or silently “upgraded” | Versioned `EffectiveDialect` record and writer feature-admission checks | Refuse interpretation/write claim until all version signals are reconciled. |
| Multi-source transforms are forced through one parent root | Critical | Page import/merge invents source continuity or loses origin of imported resources | Role-labeled multi-input transform roots and composite nonempty origins | Freeze import/merge APIs until lineage round-trips through receipts. |
| Page import copies a dictionary but not its semantic closure | Critical | Missing inherited resources, dangling references, colliding names, broken tags/destinations, or copied encryption/signature state | Closure-based graft, deterministic rebasing/renaming, explicit document-feature carry policy, structure remap, reopen/reference audit | Refuse semantic import; permit only explicitly lossy rasterized import with a receipt. |
| Ephemeral source reads mint durable byte-exact evidence | Critical | Mutable remote/path source yields cross-run cache/package claims | `ObservedBytes` facet, durable exactness only for verified/stable snapshots, source-change revocation | Invalidate package/cache claims and reopen/promote source under an immutable identity. |
| Coverage is internally contradictory | Critical | Partial outcome says complete coverage or covered/missing regions overlap | Distinct complete/partial outcome types plus one validated coverage partition per alternative | Reject malformed report/package at construction and checker boundary. |
| Broad host capability leaks authority downward | Critical | Decoder or parser can access network, trust store, entropy, or unrelated host resources | Least-authority operation capability leases; used-capability identity | Refuse operation wiring and split capability before release. |
| Byte-filter failure exposes partial decoded output | Critical | Cancelled/truncated stage leaves cache-visible bytes consumed as complete | Transactional decode sink and stage commit receipts | Disable shared decode caching/fanout until abort and fault tests pass. |
| Abandoned transaction is described as durably cleaned up | High | `Drop` path is treated as proof that temp files, worker output, or sensitive buffers were erased and diagnostics persisted | Explicit abort for receipts; drop only prevents publication and performs bounded best-effort cleanup; retained/unknown state remains sensitivity-labeled | Poison transaction/sink, reconcile state, and withhold cleanup/erasure claim. |
| One fixed image pipeline encodes the wrong mask/color order | Critical | Color-key, soft mask, JPX alpha, matte, or interpolation behavior differs by image form | Typed image-evaluation plan with stage-specific trace nodes and atomic fixtures | Remove universal pipeline optimization; fall back to explicit reference paths. |
| Premultiplied storage is mistaken for PDF blend algebra | Critical | Blend modes computed directly on premultiplied values or wrong color space | Unassociated blend computation in declared blending space with explicit conversion | Disable affected transparency profile and revalidate every group fixture. |
| Producer and evidence checker share the same bug | Critical | Same canonical parser/root implementation accepts its own malformed package | Independently implemented checker parser/root walk and lineage disclosure | Withdraw standalone-check claim until cross-implementation adversarial corpus passes. |
| Evidence identity is mistaken for evidence availability | Critical | Checker verifies a digest but cannot obtain the bytes needed to inspect a decision-critical claim | Per-artifact availability class; bounded materialization protocol; partial/refused checker outcomes | Withdraw independent-check headline or embed/pin the required artifact. |
| Scope breadth overwhelms integration | Critical | Many locally plausible subsystems but few end-to-end user workflows | End-to-end flagship gates and explicit capability-envelope discipline | Freeze surface expansion until two workflows close end to end. |
| Self-consistent but wrong standards interpretation | Critical | Tests/docs/code agree while independent engines or experts disagree | SpecCards, ambiguity registry, independent oracles, model diversity | Remove claim; profile-scope behavior; seek external adjudication. |
| Clean-room contamination | Critical | Implementation rationale cites existing engine source or unexplained identical structure | Source attestations, access separation, legal review, provenance checks | Quarantine affected work and independently reimplement or drop. |
| Pure-Rust JPX gap | High | Safe decoder lacks broad fidelity or performance | Early architecture probe, constrained subset, dedicated fuzz corpus | Safely refuse, or opt-in external adapter outside core claim. |
| Pure-Rust JBIG2 complexity/security | Critical | Frequent crashes, substitution errors, or unbounded segment graphs | Isolated crate, elevated fuzzing, independent decoders, budgets | Disable by default until full gate; render placeholder/refusal. |
| ICC/print fidelity overclaim | High | Screen tests pass but RIP/device results diverge | Runged ICC plan, separation-aware surfaces, named device profiles | Claim display approximation only; defer print-faithful profile. |
| Font hinting consumes project | High | Low-resolution text differences dominate while core remains unfinished | Unhinted correctness first, bounded VM, profile-scoped claims | Ship high-resolution/unhinted profile; defer exact platform emulation. |
| Base-font substitution is nondeterministic or legally awkward | High | Host-dependent pixels and metrics | Explicit resolver profiles, audited fallback pack decision | Refuse exact appearance without embedded/resolved font. |
| Recovery heuristics create plausible wrong documents | Critical | External or semantic checks reveal selected repair changed meaning | Alternatives, bounded search, minimal assumptions, recovery labels | Remove rule from default; retain opt-in experimental profile. |
| Provenance/evidence overhead harms throughput | Medium | Large memory/time tax on ordinary rendering | Tiered trace levels; retain compact receipts; lazy detail | Disable full trace by default but never remove core IDs/receipts. |
| Honeycomb views become duplicated ontologies | Critical | Renderer/extractor/editor each introduce private object models | Shared identity reviews, integration metrics, boundary redesign | Stop feature expansion and collapse/rework representations. |
| Page VM becomes unbounded | Critical | Operator bombs or recursive resources exceed latency goals | Universal WorkContext, iterative execution, per-family limits | Refuse page/region with partial report; never disable limits. |
| Nested or parallel work resets global budgets | Critical | Each form/stream/worker receives the full allowance and aggregate work exceeds caller limits | Shared hierarchical `ResourceAccount`, child leases, pre-reservation, race/overflow tests | Disable the affected parallel/recursive path until accounting is compositional. |
| Unsafe SIMD compromises safety | Critical | Miri/fuzz failures or hard-to-review capsules | Scalar authority, capsule registry, tiny modules | Disable optimized path; retain scalar implementation. |
| Third-party Rust dependencies carry hidden semantics | High | Core behavior changes on dependency upgrade | Narrow adapters, pins, claim boundary, source review | Fork/replace dependency or narrow public claim. |
| Patent/SEP/trademark/export encumbrance is mistaken for copyright clearance | High | Codec/profile/algorithm is technically implementable but distribution or branding rights remain uncertain in a target jurisdiction | Per-source encumbrance fields, counsel review for release envelopes, alternative implementations/profiles | Refuse the affected release claim or feature in that jurisdiction until disposition exists. |
| External oracles are correlated | High | Multiple engines agree due to shared lineage | Analytic oracles, alternative model families, device tests | Treat agreement as compatibility only, not normative proof. |
| External comparison tools compromise the lab host | Critical | Hostile corpus triggers crash/exploit, shell injection, network access, or output flood | Fixed argv, no shell interpolation, disposable isolation, no secrets/network, hard quotas | Disable adapter and treat as security incident until sandbox and tool image are repaired. |
| Differential testing becomes majority voting | High | Fixes follow popular output without standards analysis | Causal minimization and ambiguity registry | Block compatibility rule until justification exists. |
| Divergence minimizer changes the witness class or cause | High | A smaller file preserves a pixel delta only by becoming malformed, selecting another revision, or triggering another profile path | Pin conformance/recovery/profile/security envelope and causal anchors; fork lineage when class changes | Reject the reduction as evidence for the original cause. |
| Corpus licensing/privacy blocks reproducibility | High | Key fixtures cannot be redistributed or exposed to agents | Manifests, minimization, restricted evaluation service | Publish derived witnesses; scope public claims to shareable evidence. |
| Fuzzing produces volume without learning | Medium | Many crashes share same root or closed bugs recur | Semantic dedupe, tombstones, general property closure | Reallocate fuzz budget to weak components/generators. |
| Repository decomposition mirrors the file tree rather than semantic behavior | High | Components compile independently but integrated workflows stall | Plan-linked rationale and vertical-slice acceptance campaigns | Revisit the architectural decomposition before implementation continues. |
| Human attention becomes the assurance bottleneck | High | Review becomes superficial while public claims continue expanding | Contracts, independent automated oracles, narrow claim envelopes, and risk-weighted human adjudication | Stop expanding public claims until assurance capacity catches up. |
| Writer passes self-reader only | Critical | Third-party viewers fail generated files | External matrix and independent validators as release gate | No interoperability claim; restrict generator profile. |
| Canonical rewrite loses meaningful historical data | High | Users discover dropped attachments, signatures, or orphaned objects | Carry/drop map, forensic profile, explicit policy | Default to preservation; require opt-in canonical drop policy. |
| Secure-redaction claim exceeds search envelope | Critical | Residual content discovered outside primary page text | Full history/object/image/metadata inventory and independent attack | Revoke claim, patch corpus, publish advisory; narrow envelope. |
| Redaction removes content but leaks the value through layout side channels | Critical | Glyph positions, `TJ` values, spacing, line breaks, or neighboring geometry permit reconstruction | Separate absence/inference claims; side-channel attack suite; reflow/reconstruct/rasterize wider region under collateral budget | Withdraw inference-resistance claim and use a stronger transformation policy. |
| Signature trust is mistaken for digest validity | Critical | Reports call cryptographically intact untrusted signer “valid” | Layered signature report and host trust adapters | Rename/refuse trust headline unless all required layers run. |
| Performance goals distort semantics | High | Fast path changes pixels or removes diagnostics | Correctness-gated benchmarks and scalar reference | Disable fast path; performance claim fails, correctness remains. |
| Determinism across targets is too expensive | Medium | > declared performance tax on common workloads | Tiered determinism classes, fixed-point critical paths | Guarantee same-target identity and cross-target bounds only. |
| Standard or errata changes invalidate cards | High | Source registry sees new amendment/errata | Versioned SpecCards, stale-claim checks, release matrix | Mark affected claims stale until revalidated. |
| Accessibility automation overclaims semantic quality | High | Formally valid tags are unusable or nonsensical | Human-review boundary, heuristic evidence, user testing | Limit claim to machine-verifiable structure. |
| Layout engine becomes a second enormous product | High | Authoring work delays core PDF completion | Constrained declarative authoring language | Keep canvas/builder; defer broad word-processing features. |
| Server surface externalizes missing safety | High | Core relies on process restarts or cloud limits | Core budgets and cancellation first; service is adapter | Do not ship server until library survives hostile local inputs. |
| Public alien-artifact narrative outruns evidence | Critical | Marketing cites code/agent count rather than baselines and operation | Claim ladder, production ledger, ablations, external review | Use “candidate” only; withhold alienness claim. |
| Supremacy register — strongest comparator or gap set changes | High | A new eligible release closes a gap, a tracked entrant becomes stronger, or prior documentation and black-box behavior diverge | Predeclared cutoff and eligibility; artifact pinning; generated register; challenge process; refresh every gate/claim freeze | Lapse the current-facing claim and re-evaluate; preserve the old dated report as history |
| Supremacy benchmarks — benchmark Goodharting or denominator gaming | High | Heuristics improve a public score while held-out quality regresses; exclusions, thresholds, strata, or comparator configuration change after results | Frozen canonical denominator and exclusion log; benchmark-owner conflict disclosure; independent score reproduction; held-out steward; multiplicity policy | Disqualify/withdraw the claim and publish the changed-denominator divergence |
| Supremacy scope — Scope relapse through competitive additions | High | Bet additions arriving without conjunction/connectance justification; crate count inflating; flagship count growing | §34.2 conjunction/connectance filter applied at merge review; crate-boundary budget; [M] non-blocking rule | Strike additions at the comparative-synthesis gate; new competitive material remains strikeable rather than entitled |
| Clean-room — competitor-code contamination | Critical | Any PDF-processor source, generated excerpt, adapted structure, or transitive derivative appears in implementation context, prompts, diffs, or code | §24.12 source firewall; §4.1 named list plus a generated denylist from the refreshed register; provenance scanner; context attestations; special care for hayro’s declared PDFBox/pdf.js adaptations | Quarantine and independently re-author affected components or narrow the clean-room claim |
| Evidence integrity — Repeating competitors' unverified claims | Medium | Register numbers cited in public materials without the [self-reported] marker or reproduction | Register discipline; independent reproduction evidence precedes public citation | Correct publicly; treat as an evidence-integrity incident |
| Observatory publication — Observatory publishes what it may not | High | Witness fixtures with unclear provenance or license queued for release | §4.7 corpus licensing gate; behavior-record + generation-recipe publication path for unredistributable bytes | Pull affected witnesses; publish redacted records only |
| Legacy execution — Legacy execution becomes an attack surface | Critical | JS/XFA tenants exceeding budgets; sandbox escapes in fuzzing; sanitizer/interpreter disagreement | Bet 8 VM contract as sole execution path; Flagship G budget calibration; adversarial corpus | Disable the tenant behind its capability gate; ship inventory/sanitize-only for that construct |
| Supremacy selection — cherry-picked “strongest” competitor | Critical | The comparator is nominated after measurement; an omitted challenger is stronger; version/channel/configuration is ambiguous | Eligibility and cutoff frozen first; all material challengers recorded; independent/public challenge; exact artifact/config pinning | Mark report disqualified; rerun only on a fresh predeclared comparison |
| Supremacy science — aggregate hides a losing axis or stratum | Critical | Overall score rises while a safety, correctness, memory, refusal, or major feature stratum regresses | Atomic claims; scorecards; Pareto/non-inferiority rules; per-stratum uncertainty and missing-case accounting | Withdraw aggregate headline; retain only independently supported subclaims |
| Agent surface — document prompt injection or confused deputy | Critical | PDF/OCR text causes tool calls, egress, secret disclosure, policy changes, or approval through an agent adapter | Data/control separation; least-authority leases; schema validation; no instruction execution from document content; authenticated tenant-isolated adapters | Disable agent transport; preserve read-only structured output until threat model and adversarial corpus pass |
| Agent edits — stale anchor or proposal TOCTOU | Critical | Document/root/policy changes between proposal validation and apply; edit lands on similar but wrong content | Bind root/revision/hypothesis/anchor digest/expected state; optimistic concurrency; no silent fuzzy rebasing; idempotency | Refuse stale proposal and require a new proposal against the new root |
| Receipt trust — signing-key role conflation | Critical | Project release key signs user operations, or a signature/log proof is described as computation verification | Separate release/build, operation, organizational, attestation, and log roles; purpose-bound envelopes; replay/checker required for computation | Revoke affected trust claim, rotate/retire keys if necessary, and reissue role-correct manifests |
| Transparency publication — private membership leaks through commitments | Critical | Public log exposes unsalted document, attachment, or text digests that can be guessed | Disclosure policy before admission, keyed/access-controlled commitments, private logs or omission, data minimization | Stop new publication; append revocation/tombstone, rotate keyed context, notify affected users, and treat already public membership disclosure as potentially irreversible; narrow the public-verifiability claim |
| External recognition — hostile response or mutable model drift | High | Oversized/malformed coordinates/text, embedded instructions, changing outputs behind one endpoint/version label, or cross-tenant leakage | Treat response as hostile; bounded schema; immutable model/service identity where possible; operation-local evidence otherwise; tenant/cache partitioning | Disable endpoint/profile; invalidate durable replay/calibration claims and re-observe |
| Accessibility — validator pass is mistaken for usable or compliant remediation | High | Generated tags pass machine rules while reading order, alternate text, table meaning, or user experience is wrong | Separate rule conformance, human-review obligations, caller attestations, usability evidence, and legal no-claims | Withdraw usability/compliance headline; retain only executed-rule results |
| Recovery portfolio — producer prior is spoofed or drifts | High | Producer metadata is attacker-controlled; calibrated family behavior changes; prior dominates contradictory evidence | Priors only after admissibility; abstention; time/version-stratified calibration; drift expiry; spoof tests | Disable or lapse the prior and return to evidence-only ordering |
| Mechanized proof — theorem/model/code correspondence is overstated | Critical | Proved model omits recovery path, generated code diverges, trusted base expands, or marketing calls subsystem proof whole-engine proof | Scope/axiom/trusted-base records; extraction/correspondence checks; proof artifact pinning; independent review | Withdraw `MechanizedProof` facet for affected build; retain theorem only as model evidence |
| GPU certificates — checker shares the implementation or costs more than the work | High | Certificate verifier reuses shader logic, misses unsupported operations, or verification overhead defeats the lane | Independent scalar/checker path; coverage map; cost receipts; unsupported-operation refusal | Keep GPU path experimental or fall back to CPU reference without certificate claim |
| Observatory playground — hostile witness compromises browser or leaks data | Critical | WASM memory/CPU exhaustion, accidental upload, active-content execution, cross-origin persistence, or external service call | Local-only default; strict budgets; origin isolation; no active-content execution; explicit capability/disclosure for any external service | Disable playground/public witness class; core library claim remains unaffected |
| Identity/provenance — transform-authored content invents a parent or cross-root origin IDs alias | Critical | A newly added annotation, appearance, replacement text, or agent edit receives a fake parent, or one bare local origin ID is interpreted under another root | Root-qualified prior origins; candidate-local IDs confined to finalization; frozen `TransformIntentId`; `DerivationBasis::Authored` versus `From(NonEmptyVec<_>)`; publication maps every candidate origin to its final rooted node | Block transform publication and migrate origins before downstream lineage is trusted |
| Identity/provenance — transform root aliases a recipe, result, or its own lineage | Critical | Root identity omits the admitted semantic result, includes lineage/output IDs that themselves require the root, or a result origin embeds a post-root `TransformId` | Mint only after semantic finalization; hash inputs, policy/schema semantics, local frozen intents, and a canonical result commitment whose origins use only source/draft IDs or pre-root `TransformIntentId`; mint `TransformId` and lineage receipts afterward | Invalidate the identity version and rebuild affected roots/lineage under an acyclic result-bound grammar |
| Identity/provenance — transform binds an input root but not its selected view | Critical | The same source bytes have several revision/recovery views and two transforms alias because both name only `SourceRootId`, or an edit applies after expected state changed | `TransformInput::Document` binds root + exact `DocumentViewId`; proposal/admission/receipt separately binds and revalidates `ExpectedStateId` and authority; constructor proves root/view/graph consistency; optimistic concurrency before publication | Refuse/fail stale input, invalidate aliased roots/receipts, and migrate the transform identity grammar before mutation claims resume. |
| Transient admission state contaminates `TransformRootId` | Critical | Equivalent provenance-bearing results get different roots because caller leases, `ExpectedStateId`, idempotency/publication generations, or mutable authorization snapshots were hashed into document reality; sensitive admission facts leak through public commitments | Root commits exact role-labeled root/`DocumentViewId` inputs, frozen intent, origins, result semantics, and provenance policy only; proposal/admission/`TransformReceipt` binds and revalidates `ExpectedStateId`, authority, idempotency, and publication state | Migrate the identity protocol, invalidate affected cross-run root equivalence/dedup claims, and retain old receipts as versioned historical evidence rather than reinterpreting them |
| Cross-surface consequence contract drifts | Critical | Rust, CLI, C ABI, WASM, service/agent, report, benchmark, and release prose use one capability name but disagree on input identity, authority, preconditions, partial/refused outcomes, determinism, evidence, privacy, or falsifiers | One versioned §10.10 `ConsequenceContractId` per public capability/subclaim; surfaces may only narrow; generated manifests/Appendix-E/docs/checks reject orphan or inconsistent claims | Withdraw the affected surface and release claim, preserve prior contract/version, and restore one canonical outcome/authority/evidence law before re-admission. |
| Identity/provenance — Draft intent is conflated with finalized result | Critical | Unrealized layout/shaping output is hashed into `DraftRootId`, or a Draft root receives a `RealityStateCommitment` for semantics that do not yet exist | Separate `DraftIntentCommitment` from Transform `RealityStateCommitment`; realized layout becomes a Transform result unless already explicit caller intent | Invalidate affected Draft/Transform identities and reclassify derived layout before deterministic or lineage claims resume. |
| Identity/provenance — semantic state depends on in-memory order or invents identity inside symmetry | Critical | Equivalent semantic states hash differently across map/thread order, symmetric members receive arbitrary durable IDs, or materially different states alias because multiplicity/duplicate/unknown-extension semantics were omitted | Versioned domain-separated semantic grammar; ordered structures, multisets, `SymmetryClassId` plus multiplicity; individual identity only from admitted semantic/provenance anchors | Invalidate the semantic protocol and every dependent view/root; use explicit class/alternatives or a weaker noncanonical identity until migration. |
| Identity/provenance — SourceRoot absorbs parser-derived revision discovery | Critical | A parser/recovery update changes `SourceRootId`, or a newer revision graph silently rewrites old object/revision identities and receipts over unchanged bytes | `SourceRootId` binds bytes only; immutable `RevisionGraphId` derivations coexist by protocol/version/coverage/limits; `DocumentViewId` binds the exact graph and selection | Invalidate the affected identity version, reconstruct graphs/views without changing source roots, and withhold history-sensitive claims until migration. |
| Identity/provenance — SemanticScope is an under-specified label | Critical | Two `SemanticStateId`s compare equal while one omits signatures, actions, structure, metadata, historical state, or a meaning-changing dialect/recovery policy | Canonical `SemanticScopeId` manifest enumerating included axes and all meaning-changing choices; no unqualified semantic identity | Invalidate the scope/state protocol and every cache/root/claim that relied on the incomplete equality relation. |
| Cache privacy — candidate index leaks protected artifact existence across domains | Critical | Cross-tenant timing, hit/miss, size, or metadata reveals that a confidential document, font, key context, or derived artifact was previously processed | Tenant/security/sensitivity/disclosure partitioning; no shared protected-class index without a measured side-channel profile; constant-shape or isolated lookup where required | Disable and purge the shared index, rotate keyed commitments where applicable, and treat confirmed disclosure as a security incident. |
| Identity/provenance — hypothesis/profile-dependent view IDs alias | Critical | The same `ProgramNodeId`, `PageId`, primitive, glyph, or semantic ID denotes different results under two recovery hypotheses, profiles, algorithms, or capability sets | Separate root-intrinsic IDs from `DocumentViewId`/`DerivationId`; include every outcome-sensitive input; conversion maps instead of magic equality | Disable cross-view caches/references and migrate reports before claim reuse |
| Replay/certification — repeatability or equivalence is mistaken for correctness | Critical | A deterministic replay, attestation, or GPU certificate reproduces the same wrong result and is marketed as validation | Composition rules keep relation evidence separate from standards, analytic, corpus, and security correctness evidence | Withdraw correctness headline; retain only the proven replay/equivalence relation |
| Supremacy language — equivalence is marketed as a lead | High | A parity/non-inferiority gate is labeled supremacy or “mogging” without an uncertainty-aware leading result | Typed outcomes distinguish `equivalent`, `non_inferior`, and `leading`; only `leading` supports the headline | Correct/withdraw claim and preserve the underlying parity result |
| Supremacy statistics — pseudo-replication or optional stopping | Critical | Pages/pixels/runs are counted as independent documents; run count changes after interim results; only favorable model routes or seeds are retained | Predeclare primary analysis unit, pairing/clusters, effect/precision target, multiplicity, stopping/peeking, attempt budget, and missingness; independent reanalysis | Disqualify the headline and repeat only under a fresh frozen protocol |
| Supremacy scope or field definition is laundered | Critical | A pure-Rust result is marketed as all-open/global, closed/opaque material challengers are ignored while prose says “best,” or a mutable SaaS endpoint is treated as a pinned release | Exact versioned `FieldDefinitionId`; typed `named_set_lead`/`registered_open_field_lead`/`observed_field_lead`; no global-best label; exact artifact eligibility; mutable service kept as scoped observation | Withdraw or narrow claim to the actually measured field and scope |
| Agent anchors — heuristic geometry is treated as exact identity | Critical | A low-confidence OCR/layout anchor authorizes destructive, signature-affecting, or high-collateral mutation | Anchor evidence/coverage/ambiguity in proposal; separate create/validate/approve/apply authorities; explicit confirmation or refusal | Reject mutation and require a new exact or policy-approved proposal |
| Transparency integrity — split-view/equivocating log | Critical | Different clients receive inconsistent histories; self-hosted operator is the only observer; no checkpoint gossip or witness | Signed checkpoints/tree heads, inclusion/consistency proofs, independent monitor/gossip/witness policy, equivocation evidence | Suspend public log claim, publish conflicting checkpoints, rotate/replace substrate, preserve incident evidence |
| Foundry evaluation — weak baseline or destructive ablation manufactures advantage | Critical | Baseline receives worse task information/tools/attention; ablation merely breaks interfaces; evaluator knows condition and tunes judgment | Same source/task envelope and attempt budget; best ordinary replacement; blinded independent evaluation; multiple seeds; interaction analysis | Withhold foundry claim and repeat under a fair predeclared protocol |
| Authoring identity — implementation version pollutes frozen intent | High | Updating a shaping/layout engine changes `DraftRootId` despite identical caller intent, or two implementations produce different output under one unqualified derived ID | Draft binds intent/assets/declared semantic data; implementation/build belongs to `DerivationId`; caller-supplied positioned runs are explicit intent | Migrate root grammar and invalidate affected caches/reports before compatibility freeze |
| Competitor register — material released challenger omitted from a lane | Critical | S1/S6 remains hard-coded to hayro, S4 to krilla, or any atomic lane ignores an eligible stronger/non-dominated release available by cutoff | Generated register, per-subclaim eligibility, mandatory/non-dominated challenger set, public challenge, and cutoff-to-freeze freshness rule | Lapse/disqualify the field-lead claim until every eligible challenger for that subclaim is characterized |
| Semantic equality is conflated with reality/provenance identity | Critical | Semantically equal documents alias signature history, source-preservation authority, origins, or edit permissions—or equivalent values fail to share safe semantic caches | Separate `SemanticStateId` from `RealityStateCommitment`; claim-specific identity domain; lineage only through receipts | Invalidate affected identity/cache protocol and migrate before any history-sensitive claim or mutation. |
| Canonical graph symmetry causes nondeterminism or needless refusal | High | Repeated equal pages/resources hash differently by traversal order, or ordinary symmetric documents cannot finalize | Ordered semantics, unordered multisets with multiplicity, canonical equivalence classes, post-root local IDs; refusal only for truly identity-sensitive unresolved distinctions | Disable affected canonical identity/output profile and use a weaker explicit noncanonical identity until the protocol is repaired. |
| Adversarial symmetry exhausts canonicalization work | Critical | Refinement or canonical-label branching grows beyond the declared node/edge/partition budget, memory rises with symmetric alternatives, or a fallback starts using traversal/allocation order | Constitution §11.2.3 canonicalization/symmetry counters, pre-branch charging, quotient/multiplicity representation, cancellation, and typed weaker outcomes | Refuse the canonical profile or return the declared noncanonical outcome; never retain a canonical identity claim from the fallback. |
| Competitor discovery is incomplete but marketed as a field lead | Critical | New released renderer/extractor is found after a two-project “field” claim; search surfaces/languages/registries were not recorded | `CompetitorDiscoveryProtocolId`, independent scouts, registries/queries/languages, challenge window, exact exclusions; incomplete coverage permits only `named_set_lead` | Lapse/withdraw the field claim and rerun under a fresh frozen discovery/evaluation protocol. |
| Competitor discovery protocol is committed only after searching | Critical | Search terms, languages, registries, or eligibility are reconstructed around the systems already found | Pre-search `CompetitorDiscoveryProtocolCommitment`, then committed discovery report/challenge set, then evaluation commitment | Treat field scope as `named_set_lead` and repeat discovery prospectively. |
| Comparator misconfiguration or asymmetric tuning manufactures a lead | Critical | Competitor runs with weak defaults, missing features/fonts, failed integration, or less tuning/operator help than MonkeyBee | Strongest documented eligible configuration; equal tuning/integration budget; independent operator; maintainer/vendor challenge; triage failures as indeterminate | Disqualify the comparison and rerun under the symmetric frozen configuration protocol. |
| Evaluation predeclaration is reconstructed or edited after outcomes | Critical | Protocol has no pre-result commitment, timestamps follow measurement, or thresholds/comparators/denominator change in place | Content-addressed `EvaluationProtocolId`; independent timestamp/steward/witness before unblinding; append-only amendments; fresh data after material change | Disqualify the confirmatory headline; retain only exploratory results. |
| Embedded-language “no host calls” conflicts with admitted typed effects | Critical | Form scripts gain ambient APIs, or required field access is hidden behind an undocumented exception | Common no-ambient-authority meta-contract; tenant-specific typed pure capabilities and transactional effect journal; deny-by-default built-ins | Disable the tenant and ship inventory/sanitize-only until capability and effect semantics are explicit. |
| Form rendered-cache omits caller graphics/backdrop state | Critical | Same Form object reuses pixels under different CTM, clip, color, blend, soft mask, optional-content, or non-isolated backdrop | Separate parsed-program and rendered caches; validated sufficient caller-state/backdrop/resource manifest | Disable rendered Form cache; retain parsed program or context-independent intermediate only. |
| Nonce uniqueness is overclaimed across distributed/random-only writers | Critical | Cloned/restarted hosts or caller RNGs may reuse a nonce while receipt says “hard invariant” | Per-key allocation domain; coordinated durable allocator for deterministic guarantee; otherwise quantified collision bound, key-use cap, health evidence | Refuse the affected nonce-based profile or narrow the claim before release. |
| Signature determinism is universally denied or falsely forced | Critical | Deterministic ECDSA/EdDSA is forced through random material, or a randomized/hedged/timestamped signer is labeled byte-deterministic | Algorithm/profile-specific nonce law; pin signed attributes, encoding, key identity, time/timestamp/revocation and service inputs; independent repeatability vectors | Withdraw D1/D1R claim and disable signature creation until the exact scheme contract is reviewed. |
| Agent idempotency replays or aliases a crash-ambiguous mutation | Critical | Timeout/retry applies an edit twice, partial batch becomes visible, another tenant/schema collides, tombstone expires while output remains visible, or request hash leaks confidential content | Tenant/caller/schema/publication-scoped reservation, disclosure-safe request binding, atomic batch, retained outcome/tombstone through observability window, `indeterminate` reconciliation, no blind retry | Freeze mutation surface; reconcile outputs, extend retention/migrate namespace, and revoke affected receipts before re-enabling. |
| Adaptive holdout access turns evaluation into hidden development data | Critical | Repeated submissions, per-case diagnostics, or leaderboard feedback guide tuning while set is still called held out | Frozen query/feedback budget, no-feedback window, access log, steward, fresh reserve/replacement set | Demote old set to development/regression and repeat on fresh independently stewarded data. |
| Baseline/model drift makes a historical foundry win look current | High | Current models/harnesses materially outperform the frozen control, or provider behavior changes without rerunning baselines | Historical and contemporaneous baselines; model/harness/provider drift report; exact claim date and expiry | Relabel as historical or lapse the current-facing foundry claim. |
| Retrospective production ledger is presented as prospective precommitment | Critical | Early prompts/attempts/resources are reconstructed after success and used as if contemporaneously committed | Label retrospective records, confidence, gaps, and source basis; strong foundry claims use prospectively committed later trials | Narrow to artifact/historical evidence and rerun the foundry evaluation prospectively. |
| Synthetic assurance is relabeled as empirical or adaptive maturity | High | Fuzz/proof/simulation counts are used to claim real operational seasoning or incident adaptation | Separate structural, empirical, and adaptive maturity ledgers and minimum evidence envelopes | Narrow the maturity/lineage claim to the evidenced class. |
| Feature accumulation defeats consequence compression | High | Each new bet creates a parallel ontology, evidence type, authority path, budget, or operational subsystem | P19 compression gate; specification/verification/integration leverage metrics; strongest ordinary composition baseline | Merge, isolate as non-core, or strike the capability unless extraordinary consequence justifies the seam. |

---

### 32.1 Research-bet governance

Multiple bounded, quarantined [F]/[M] probes may coexist under P18 when each has an explicit semantic owner, budget, evidence instrument, integration boundary, kill criterion, and fallback. At most one major [M] program may block a declared release envelope or force project-wide architectural churn at a time, and aggregate probe concurrency may not exceed integration and assurance capacity.

Candidate [M] programs include:

- generalized recovery hypothesis planning;
- intent-to-interoperable compilation optimization;
- causal divergence minimization at scale;
- and foundry/lineage measurement.

Every non-blocking probe remains a thin experimental layer over the solid spine until its own admission gate; parallel probing never grants parallel entitlement to core architecture or release claims.

### 32.2 Periodic evidence review

Every [F] and [M] feature has:

- a measurable claim;
- a predeclared evidence threshold;
- a review point;
- and a fallback or demotion path.

A feature without its kill measurement instrumented is treated as failed governance, not tacitly successful.

---


## 33–34. Evaluation and refinement kernel

`generated-echo: constitution/MONKEYBEE_CONSTITUTION_v8.md §§33–34.9`

The Constitution is the sole normative home. The Charter adds cycle staging without changing these claim and refinement laws.

## 35. Open decisions before plan freeze

Every row below remains an open shell decision; a “current default assumption” is planning history, not ratification. Under D-005, runtime dependency policy and every cryptographic-crate selection are specifically `PENDING-HUMAN-RATIFICATION`. Candidate classes or capability descriptions in this table do not select a crate, dependency graph, or allowlist.

| Decision | Current default assumption | Evidence needed before commitment |
|---|---|---|
| Standards AI-use rights | Default deny model access unless explicitly permitted | Counsel/source-rights owner and per-source terms matrix. |
| Clean-room claim wording | “Clean-room development protocol,” with opaque model-training data disclosed as unknown | Legal and independent methodology review. |
| First public release envelope | R0 Revision Autopsy, then R1 display, R2 writer, R3 transforms | Product/security review and user validation. |
| Reality root model | Byte-only Source roots, `DraftIntentCommitment`-identified Draft roots, and finalized result-bound multi-input Transform roots whose document inputs bind exact root/views while proposal/admission receipts bind expected state and authority; type-level authored-versus-derived origins and separate lineage receipts | Architecture review and identity/lineage prototype. |
| Evidence outcome model | `ClaimOutcome<T>` outside evidence facets, with a distinct `PartialClaim<T>` and one validated coverage partition per alternative | Type-level adversarial review and hostile package fixtures. |
| Immutable source identity | Verified content, stable snapshot, or ephemeral observed-read source; durable exactness only for the first two | Remote/streaming prototype and cache/evidence threat model. |
| Recovery ordering | Pareto/partial order; user intent selects but does not redefine meaning | Withheld malformed corpus and calibration study. |
| Effective PDF dialect | Header + catalog override + registered extensions + feature requirements + historical revision context | Standards-card review and cross-version corpus. |
| Capability authority | Top-level host registry mints non-copyable least-authority operation leases; children can only inherit or narrow | API threat model and adapter prototype. |
| Decoder publication | Transactional byte/image sinks; no partial cache visibility | Fault/cancellation injection and storage prototype. |
| Codec-filter chaining | Every admitted declared chain has a canonical sample-byte path; typed planes are a proven-equivalent terminal optimization only | Standards-card review, odd-chain corpus, sample-layout fixtures, and dual-path equivalence tests. |
| Evidence oracle lineage | Correlation is recorded; “external” does not imply independence | Assurance-method review and multi-oracle corpus. |
| Entropy/determinism split | Secure randomized crypto; deterministic unencrypted output | Cryptographic review and test vectors. |
| Signature profile baseline | Core structure plus separately versioned PAdES validation profile | ETSI/PAdES source-card rights review and crypto/trust design. |
| Structured authoring v1 | Caller-shaped runs plus bounded paragraph profile before full multiscript layout | Unicode/layout/shaping dependency study. |
| Project license | Permissive adoption-oriented license | Legal review and dependency compatibility. |
| Clean-room protocol details | Standards/cards/black-box behavior allowed; engine source forbidden | Counsel or formal project policy. |
| ISO access and quotation policy | Authorized copies; clause references and paraphrases only | Legal/source registry owner. |
| Rust toolchain | Pinned stable or dated nightly only if essential | Prototype and dependency audit. |
| Minimum supported Rust version | Deferred until dependency set stabilizes | Ecosystem/adoption analysis. |
| Runtime dependency allowlist | `PENDING-HUMAN-RATIFICATION`; Rev 7 candidate policy: pure-Rust, permissive, narrow semantic boundaries | Architecture/security review. |
| Async runtime | None in core; adapters only | Byte-source/service prototype. |
| Persistent ledger backend | Start with portable structured files or SQLite-class safe Rust backend | Throughput, crash-safety, and dependency review. |
| Immutable file/remote snapshots | Spool/copy or verifiable page snapshot; raw mutable mmap/path is not authoritative | Cross-platform prototype and TOCTOU threat review. |
| Sensitive cache/spool policy | Data-classified; no default persistent decrypted/text/attachment cache | Security/privacy owner and host-platform controls. |
| Output publication/durability classes | Core transactional capability plus platform-specific directory-capability helper; no universal atomicity claim and no path-race immunity without measured host primitives | Cross-platform crash/fault and symlink/TOCTOU prototype. |
| Cryptographic crates | `PENDING-HUMAN-RATIFICATION`; Rev 7 candidate class: vetted RustCrypto-class dependencies, with no crate selected | Security audit and vectors. |
| Public-key security handler | Preserve/inventory first; decryption only with explicit key-provider profile | Standards cards, CMS/key-provider prototype, security review. |
| Evidence checker isolation | Separate `mb-checker` with independently implemented package parser/canonical-root verification; only narrow crypto/schema constants may be shared | Threat model, dual-implementation prototype, and adversarial package corpus. |
| Evidence-package canonical identity | Versioned, domain-separated, length-framed canonical semantics with named hash/root algorithms and explicit extension rules | Dual-implementation collision/ambiguity review, hostile encodings, migration design, and cryptographic review. |
| General artifact identity grammar | Typed, domain-separated, length-framed, algorithm-versioned identities; collision observations quarantine rather than alias | Cache/store prototype, algorithm-migration design, and adversarial collision/identity review. |
| Evidence-package signature semantics | Purpose-bound signature envelope; integrity, authentication, trust, role authorization, policy admission, and freshness remain separate outcomes | CMS/signature-profile review, role/policy threat model, replay tests, and hostile detached-signature corpus. |
| Candidate versus release receipt | Immutable core `TransformReceipt` plus separate `AssuranceAdmissionReceipt` that can withhold publication without rewriting candidate history | Cross-layer API review and fault-injected publication rehearsal. |
| JPEG implementation | Audited pure-Rust dependency likely | Fidelity/security benchmark. |
| JPX implementation | Early probe; no default claim yet | Ecosystem survey and corpus spike. |
| JBIG2 implementation | In-house or audited pure-Rust path; elevated gate | Security-focused architecture review. |
| ICC implementation | Runged internal or audited pure-Rust dependency | Profile corpus and device claims. |
| Font shaping for authoring | Adapter with likely pure-Rust shaper | License, script coverage, deterministic behavior. |
| Base-font fallback pack | No silent default; resolver profile required | Font licensing and metric study. |
| TrueType hinting release envelope | Unhinted/high-resolution first if necessary | Pixel corpus and performance evidence. |
| First PDF/A profile | Select by corpus/oracle maturity, not marketing | Standards/profile owner. |
| First PDF/UA profile | Select current supported profile with independent corpus | Accessibility expert and validator. |
| Signature trust provider | Pluggable host adapter | Security API and platform survey. |
| Online revocation | Explicit optional capability, never core hidden I/O | Threat/privacy/availability analysis. |
| Default recovery profile | Conservative, alternatives visible | Recovery corpus and false-positive study. |
| Compatibility profile naming | Versioned data with processor scope | Lab schema review. |
| Page raster surface format | Premultiplied linear internal; explicit output formats | Compositing/color prototype. |
| PDF blend computation | Unassociated components in declared blending color space; premultiplication only at storage boundaries | Transparency formula review and atomic group corpus. |
| Image evaluation ordering | Typed plan per image/mask/alpha form, not one universal pipeline | Normative card review and cross-engine atomic fixtures. |
| Fixed-point coverage precision | To be measured against quality/performance | Reference/optimized raster experiment. |
| Same-target pixel determinism | Required default target | Cross-run/thread tests. |
| Cross-target pixel identity | Aspirational; bounded profile acceptable | Multi-ISA measurement. |
| Canonical dictionary order | Stable bytewise name order unless standard/profile requires otherwise | Writer interoperability experiment. |
| Canonical number formatting | Versioned bounded PDF decimal grammar minimizing length subject to exact semantic round-trip; never an unconstrained generic shortest-float policy | Cross-reader, boundary, and exact-value tests. |
| Canonical compression engine/version | Pinned and profile-bound | Determinism and size benchmark. |
| External renderer matrix | At least three independent families plus browser path | Licensing/automation owner. |
| Printer/RIP access | Limited named device profiles later | Partnerships and reproducibility. |
| Corpus storage | Hash-addressed manifests with restricted tiers | Privacy/legal/infrastructure review. |
| Fuzzing service | cargo-fuzz locally plus continuous service | CI/OSS-Fuzz readiness. |
| C ABI stability point | Preview ABI may ship earlier; first compatibility commitment only through the explicit public-compatibility freeze after the advanced capability envelope stabilizes | API/ABI review and migration rehearsal. |
| WASM codec subset | Capability manifest, no hidden fallback | Build matrix. |
| Service product | Optional; does not define core | Demand and isolation evidence. |
| JavaScript execution | General JavaScript remains a non-goal; Bet 16 admits only a metered AcroForm calculate/format/validate subset [M] with pinned host facts and sanitizer parity | Product need, subset corpus, VM threat model, determinism review, and reference-viewer comparison. |
| XFA runtime | Preserve/inventory by default; static XFA projection [M] is admitted only within a bounded, explicit subset; full interaction remains a non-goal | Demand, bounded projection probe, XML/layout threat model, and no-claim design. |
| Secure PDF encryption output | Standard-handler writer profile in the transformation/security release envelope; no weak legacy emission by default | Cryptographic review, vectors, entropy and interoperability tests. |
| Digital signature creation | Deferred after validation and writer maturity | Key-management and UX design. |
| Public API compatibility policy | Semver plus schema versioning, frozen through the explicit public-compatibility freeze | Maintainer governance. |
| Release cadence | Evidence-gated, not date-driven | Governance decision. |
| Alien-artifact reference class | Public expert agent foundries under bounded resources | Independent methodology review. |
| Semantic/reality commitment protocols | Default split: semantic value identity plus provenance-bearing reality identity | Dual-implementation canonicalization, symmetry corpus, cache/source-preservation threat model, and migration design. |
| Evaluation precommitment substrate | Independent steward or witnessed timestamped append-only commitment; not necessarily Bet 23’s public log | Threat/privacy/availability review, reveal protocol, amendment semantics, and independent-methodology acceptance. |
| AES-GCM nonce allocation profile | Prefer coordinated durable per-key allocator where a no-reuse claim is required; random-only profiles expose collision bound and key-use cap | Cryptographic review, crash/clone/distribution model, interoperability vectors, and allocator fault tests. |
| Agent mutation idempotency store | Durable request reservation/outcome query with explicit `indeterminate`; no global exactly-once claim | Storage/publication crash model, multi-tenant threat model, duplicate/reconciliation tests, and API ergonomics. |
| Empirical/adaptive maturity claim thresholds | No fixed duration or incident count yet; scope each claim to actual exposure | Independent methodology review, user/workload exposure, incident taxonomy, and longitudinal evidence. |
| 1 — Initial public supremacy claim envelope | S1 rendering field scorecard versus S2 wild-tail ledger; unresolved. This selects the first public claim boundary, not work ordering, funding, or execution priority | Corpus rights, frozen-denominator quality, independent steward availability, complete challenger-set viability, claim scope, statistical design, and comparative-synthesis review. |
| 2 — Extraction leaderboard governance | Open: enter the existing benchmark as-is or co-publish a provenance-scored Observatory variant | Benchmark rules and continuity, evaluator independence, oracle lineage, and held-out correlation analysis. |
| 3 — Static XFA projection depth | Open: no subset is claimed until bounded | Representative XFA corpus, layout taxonomy, resource-limit model, and reference-viewer comparison. |
| 4 — Receipt/log trust substrate | Self-hosted versus existing transparency ecosystem, plus explicit release-manifest, operation-signer, attestation, log, monitor/gossip, and witness roles | Verifier-user requirements; computation-versus-assertion semantics; split-view/equivocation resistance; trust, privacy, potentially irreversible membership disclosure, availability, key separation, revocation/tombstones, and artifact-boundary threat model. |
| 5 — Bet 24 first proof-kernel scope | Open: choose two or three among lexer span/termination, filter expansion bounds, and recovery admission | Proof effort, trusted-base size, model-to-code correspondence, and public claim value. |
| 6 — Ruffle-class SWF adapter | Open: permitted non-core adapter versus permanent sanitize-only posture | Demonstrated user need, dependency allowlist, sandbox review, maintenance cost, and §33.3 boundary impact. |
| 7 — GPU lane admission | Default outside all declared envelopes until CPU-equivalence certificates survive a bounded probe | Cross-target determinism, fixed-point/blend feasibility, certificate checker independence, and performance value. |
| 8 — S4 writer version scope | Open: scope parity to PDF/A-2+ and PDF/UA-1, or widen §3.2 with a PDF/A-1-sufficient PDF 1.4 profile | Product demand, standards/profile validation, writer complexity, and interoperability evidence. |
| 9 — S6 performance posture | Open: retain §26.3 competitive posture or adopt equivalence/non-inferiority gates plus a leading target on selected §26.2 workloads; parity alone is not a supremacy claim | Profile-aligned benchmark evidence, determinism/evidence overhead, and proof that safety contracts are not bypassed. |

### 35.1 Assumptions that may be wrong

This revised initial plan assumes:

- a shared multi-view representation is worth its overhead;
- strict parsing and recovery can remain cleanly separated;
- current pure-Rust dependencies are sufficient for most generic codecs and cryptography;
- black-box interoperability testing can be automated legally and reproducibly;
- evidence-rich outputs remain affordable for ordinary workflows through lazy tracing and selective materialization;
- a provisional crate atlas can preserve conceptual clarity without turning into microcrate proliferation;
- the project can obtain enough independent corpora and processor access to ground compatibility claims;
- and the human independence ecology—source-rights owner, two-person SpecCard reviewers, corpus and commitment stewards, independent scouts, red team, reviewers, and adjudicators—can be recruited, scheduled, and funded without being fictionalized as agent capacity. The staffing plan records role separation, conflicts, expected human time/cost, and unavailable roles. If a required role does not materialize, the dependent claim degrades to its supported self-attested or narrower tier rather than blocking the survival wedge or silently claiming independence.

Each assumption must be tested through review, legal analysis, bounded probes, or held-out evidence before it becomes load-bearing.

# Appendices

## Appendix A — Load-bearing trait sketches

These are semantic sketches, not frozen APIs.

### A.1 Byte source

```rust
pub trait ByteSource: Send + Sync + 'static {
    /// The descriptor owns the immutable available-range set.
    fn snapshot(&self) -> &SourceSnapshot;

    fn read_exact_at(
        &self,
        offset: u64,
        dst: &mut [u8],
        cx: &WorkContext<'_>,
    ) -> Result<(), SourceError>; // Can return NeedRange/SourceChanged; never fetches implicitly.

    fn advise(&self, range: ByteRange, advice: ReadAdvice) -> Result<(), SourceError> {
        let _ = (range, advice);
        Ok(())
    }
}
```

A zero-copy borrowed input, if exposed, uses a separate lifetime-scoped facade and does not implement this durable trait. Promotion to an owned immutable snapshot is explicit and receipt-bearing.

### A.2 Work context

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

/// Caller-provided storage retains the validated parent/local intersection for
/// at least as long as the returned child context.
pub struct ChildContextStorage {
    limits: Limits,
}

pub enum ChildContextError {
    InvalidLimits(LimitError),
    Capability(CapabilityError),
}

impl WorkContext<'_> {
    pub fn checkpoint(&self, kind: CheckpointKind) -> Result<(), Cancelled>;
    pub fn reserve_bytes(&self, class: ResourceClass, n: u64)
        -> Result<ResourceLease, LimitError>;
    pub fn child<'b>(
        &'b self,
        lease: &'b ResourceLease,
        local: &Limits,
        requested_capabilities: CapabilityRequest,
        storage: &'b mut ChildContextStorage,
    ) -> Result<WorkContext<'b>, ChildContextError>; // stores parent ∩ local and narrows authority
}
```

`generated-echo: constitution/MONKEYBEE_CONSTITUTION_v8.md §§10.4, 11.1`

`ChildContextStorage` owns the computed intersection; the returned context never borrows a temporary. `DiagnosticCollector` is `Sync` with bounded interior mutability and deterministic worker-batch merge. Its non-re-entrant rule forbids host callback/re-entry during recording, not concurrent recording by child contexts.

### A.3 Evidence-bearing outcomes

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

Construction goes through capability-bearing validators so callers cannot mint normative, empirical, cryptographic, mechanism-proof, or externally checked facets from arbitrary strings. An authenticated caller may issue only a role- and policy-scoped attestation attributable to itself; it cannot mint another principal’s attestation or promote that statement into objective truth. `Claim`, `PartialClaim`, and `ClaimAlternative` fields are private; partial-coverage constructors prove scope equality plus a disjoint/exhaustive partition relative to the requested scope.

### A.4 Raw COS dictionary

```rust
pub struct RawDictionary {
    pub open: TokenRef,
    pub entries: Vec<RawDictEntry>,
    pub close: TokenRef,
}

pub struct RawDictEntry {
    pub key: RawName,
    pub value: RawCos,
    pub occurrence: u32,
}
```

Semantic lookup returns all entries plus the profile-selected occurrence.

### A.5 Object resolution

```rust
pub trait ObjectResolver {
    fn resolve(
        &self,
        key: IndirectKey,
        at: RevisionId,
        policy: ResolvePolicy,
        cx: &WorkContext<'_>,
    ) -> Result<ClaimOutcome<ResolvedObject>, ResolveError>;
}
```

### A.6 Stream decode

```rust
pub trait DecodeSink {
    fn begin<'a>(
        &'a mut self,
        expected: Option<u64>,
        cx: &WorkContext<'_>,
    ) -> Result<Box<dyn DecodeWriteTxn + 'a>, DecodeError>;
}

pub trait DecodeWriteTxn {
    fn write(&mut self, bytes: &[u8], cx: &WorkContext<'_>)
        -> Result<(), DecodeError>;
    fn commit(self: Box<Self>, cx: &WorkContext<'_>)
        -> Result<DecodeCommitReceipt, DecodeCommitFailure>;
    fn abort(self: Box<Self>, cause: &AbortReason, cx: &WorkContext<'_>)
        -> AbortReceipt;
}

pub trait DecodeSource: Send + Sync {
    fn identity(&self) -> DecodeSourceId;
    fn open_cursor(&self, cx: &WorkContext<'_>)
        -> Result<Box<dyn DecodeCursor + '_>, DecodeError>;
}

pub trait DecodeCursor {
    fn read_chunk(&mut self, max: usize, cx: &WorkContext<'_>)
        -> Result<DecodeChunk<'_>, DecodeError>;
    fn consumed(&self) -> u64;
}

pub trait ByteFilterDecoder: Send + Sync {
    fn decode_bytes(
        &self,
        input: &mut dyn DecodeCursor,
        output: &mut dyn DecodeWriteTxn,
        params: &DecodeParams,
        cx: &WorkContext<'_>,
    ) -> Result<DecodeReceipt, DecodeError>;
}

pub trait ImagePlaneSink {
    fn begin<'a>(
        &'a mut self,
        info: &ImageInfo,
        cx: &WorkContext<'_>,
    ) -> Result<Box<dyn ImagePlaneTxn + 'a>, DecodeError>;
}

pub trait ImagePlaneTxn {
    fn plane_rows(&mut self, plane: PlaneId, rows: ImageRows<'_>, cx: &WorkContext<'_>)
        -> Result<(), DecodeError>;
    fn commit(self: Box<Self>, cx: &WorkContext<'_>)
        -> Result<ImageCommitReceipt, ImageCommitFailure>;
    fn abort(self: Box<Self>, cause: &AbortReason, cx: &WorkContext<'_>)
        -> AbortReceipt;
}

pub trait ImageCodecDecoder: Send + Sync {
    fn inspect(&self, source: &dyn DecodeSource, params: &DecodeParams, cx: &WorkContext<'_>)
        -> Result<ClaimOutcome<ImageStageInfo>, DecodeError>;
    fn decode_samples(&self, source: &dyn DecodeSource, output: &mut dyn DecodeWriteTxn,
        params: &DecodeParams, cx: &WorkContext<'_>)
        -> Result<ImageSampleDecodeReceipt, DecodeError>;
    fn decode_planes(&self, source: &dyn DecodeSource, output: &mut dyn ImagePlaneTxn,
        params: &DecodeParams, cx: &WorkContext<'_>)
        -> Result<ImageDecodeReceipt, DecodeError>;
}
```

After a successful `begin`, the sink must reach one explicit terminal state: committed, aborted, or indeterminate-failed. A failed commit is followed by cleanup only when its failure state says the data are still private and abortable; cancellation, panic containment, or downstream refusal cannot be mislabeled as rollback or leave a purportedly complete half-image.

The same terminal-state law applies to `DecodeSink`: a byte-filter stage is not visible as a completed decoded artifact until commit succeeds. `decode_samples` is the canonical PDF-filter contract even for image-aware codecs. `decode_planes` is admitted only as a final-image optimization and must remain semantically equivalent to the canonical sample bytes plus ordinary unpacking; it cannot redefine filter order or hide a later declared stage.

### A.7 Transactional output

```rust
pub trait TransactionalOutput {
    fn commit_class(&self) -> CommitClass;
    fn begin(&mut self, expected: Option<u64>, cx: &WorkContext<'_>)
        -> Result<OutputTxnId, OutputError>;
    fn write(&mut self, txn: OutputTxnId, bytes: &[u8], cx: &WorkContext<'_>)
        -> Result<(), OutputError>; // all bytes accepted into private state or error
    fn commit(&mut self, txn: OutputTxnId, cx: &WorkContext<'_>)
        -> Result<CommitReceipt, CommitFailure>;
    fn abort(&mut self, txn: OutputTxnId, cause: &AbortReason, cx: &WorkContext<'_>)
        -> AbortReceipt;
}
```

`AbortReason` is a structured non-secret cause that can represent an ordinary error, cancellation, downstream refusal, or contained panic without pretending all aborts are `OutputError`s. `AbortReceipt` reports whether private state was removed, retained, or is unknown. `CommitReceipt` states visibility and durability separately; `CommitFailure` carries the last defensible publication state. A failure after host-visible publication is therefore indeterminate-or-committed, never falsely reported as rolled back.

### A.8 Page-program sinks

```rust
pub trait PaintSink {
    fn begin_page<'a>(
        &'a mut self,
        page: PageId,
        state: &PageStart,
        cx: &WorkContext<'_>,
    ) -> Result<Box<dyn PaintPageTxn + 'a>, PaintError>;
}

pub trait PaintPageTxn {
    fn emit(&mut self, op: PaintOp, cause: ProgramCause, cx: &WorkContext<'_>)
        -> Result<(), PaintError>;
    fn commit(self: Box<Self>, cx: &WorkContext<'_>)
        -> Result<PageCommitReceipt, PageCommitFailure>;
    fn abort(self: Box<Self>, cause: &AbortReason, cx: &WorkContext<'_>)
        -> AbortReceipt;
}

pub trait SemanticSink {
    fn begin_page<'a>(
        &'a mut self,
        page: PageId,
        cx: &WorkContext<'_>,
    ) -> Result<Box<dyn SemanticPageTxn + 'a>, SemanticSinkError>;
}

pub trait SemanticPageTxn {
    fn marked_content(&mut self, event: MarkedContentEvent, cx: &WorkContext<'_>)
        -> Result<(), SemanticSinkError>;
    fn glyph(&mut self, glyph: GlyphInstance, cx: &WorkContext<'_>)
        -> Result<(), SemanticSinkError>;
    fn annotation(&mut self, annotation: AnnotationEvent, cx: &WorkContext<'_>)
        -> Result<(), SemanticSinkError>;
    fn commit(self: Box<Self>, cx: &WorkContext<'_>)
        -> Result<PageCommitReceipt, PageCommitFailure>;
    fn abort(self: Box<Self>, cause: &AbortReason, cx: &WorkContext<'_>)
        -> AbortReceipt;
}
```

### A.9 Font execution and host resolution

```rust
pub trait FontExecutionService: Send + Sync {
    fn decode_run(
        &self,
        request: &FontRunRequest,
        cx: &WorkContext<'_>,
    ) -> Result<ClaimOutcome<DecodedGlyphRun>, FontExecError>;

    fn glyph_program(
        &self,
        request: &GlyphProgramRequest,
        cx: &WorkContext<'_>,
    ) -> Result<ClaimOutcome<GlyphProgramDescriptor>, FontExecError>;
}

pub trait FontResolver: Send + Sync {
    fn resolve(
        &self,
        request: &FontRequest,
        cx: &WorkContext<'_>,
    ) -> Result<ClaimOutcome<FontProgramSource>, FontResolveError>;
}
```

`FontExecutionService` is defined in the lower protocol crate and implemented by the higher font orchestrator. A Type 3 `GlyphProgramDescriptor` contains a page-program handle and scoped resources; it does not execute the VM itself. The returned resolver claim must identify substitution or exact embedded origin and bind the exact effective font-program bytes plus resolver policy/version. A host family name, path, or PostScript name is not a replay identity.

### A.10 Color transform provider

```rust
pub trait ColorTransformProvider: Send + Sync {
    fn compile(
        &self,
        source: &ColorSpace,
        target: &OutputProfile,
        intent: RenderingIntent,
        cx: &WorkContext<'_>,
    ) -> Result<ClaimOutcome<Arc<dyn ColorTransform + Send + Sync>>, ColorError>;
}
```

### A.11 Processing profile

```rust
pub struct ProcessingProfile {
    pub id: ProfileId,
    pub strictness: Strictness,
    pub recovery: RecoveryPolicy,
    pub compatibility: CompatibilityPolicy,
    pub output: OutputProfile,
    pub security: SecurityPolicy,
    pub validation: ValidationProfileSet,
    pub write: WritePolicy,
    pub limits_profile: LimitsProfileId,
}

pub struct CompiledProfile {
    snapshot: ProfileSnapshotId,
    open: OpenPolicy,
    recovery: RecoveryPolicy,
    security: SecurityPolicy,
    page: PageExecutionRequest,
    write: WritePolicy,
    validation: ValidationProfileSet,
}
```

`CompiledProfile` fields are private and can be created only by the profile compiler, which validates cross-view consistency and hashes the complete immutable view set. Lower layers receive one needed view plus the snapshot ID, never the mutable caller-facing aggregate.

### A.12 Edit operation

```rust
pub trait EditOperation: Send + Sync {
    fn intent(&self) -> EditIntent;
    fn preservation_support(&self) -> PreservationSupport;

    fn plan(
        &self,
        inputs: &BoundTransformInputView, // exact root + DocumentViewId + ExpectedStateId per document input
        policy: &TransformPolicy,
        cx: &WorkContext<'_>,
    ) -> Result<ClaimOutcome<EditPlan>, EditError>;
}
```

### A.13 Independent checker boundary

```rust
pub trait EvidenceChecker {
    fn check(
        &self,
        package_bytes: &dyn ByteSource,
        policy: &CheckPolicy,
        cx: &WorkContext<'_>,
    ) -> Result<ClaimOutcome<CheckReport>, CheckError>;
}
```

`generated-echo: constitution/MONKEYBEE_CONSTITUTION_v8.md §10.6.1`

The standalone checker accepts raw hostile package bytes and owns its own package parsing, structural walk, canonical-root verification, availability/materialization checks, and coverage accounting. It never receives a producer-parsed `EvidencePackage` as trusted input. The proposed Constitution binding additionally requires different-model-family authorship, a specification-only allowed-source manifest excluding producer source/rationale/fixtures, recorded lineage/correlation, and independently administered per-cycle seeded-defect detection trials; these are unavailable until human ratification and observed evidence exist. The checker distinguishes identity verification from evidence availability: an authenticated digest for an `IdentityOnly` or unavailable artifact does not let the checker inspect or replay that artifact. `Embedded`, `ExternallyRetrievable`, and `Recomputable` artifacts are materialized only through their declared bounded capability/protocol, and missing decision-critical material yields partial coverage or refusal. The checker is fully budgeted. `CheckReport` includes coverage, truncation, unsupported-claim kinds, unavailable-artifact classes, checker capability identity, and the applicable isolation/trial lineage; budget exhaustion returns a partial or refused outcome rather than an apparently complete report. The checker must not depend on rendering or editing crates unless a claim explicitly requires recomputation; such a recomputation requirement is named in the checker protocol and capability manifest.

---


## Appendix B — Representative report schemas

`generated-echo: constitution/MONKEYBEE_CONSTITUTION_v8.md §§10.6, 10.8, 10.10; generation-mode: schema-derived`

These examples are generated views of the Constitution's report-family and common identity-envelope obligations. They are non-normative and cannot add, omit, or weaken a required field. The schema-example validator rejects an example when any §10.6 family field or §10.8 common field is absent, when a run observation does not bind its semantic report one-way, or when run telemetry enters semantic identity. The `semantic-report:*` and `run-observation:*` values below are nonproduction placeholders; their protocol fields remain `PENDING-HUMAN-RATIFICATION-D1-D2` and do not mint identities before §9.2.1 ratification.

Every B.1-B.5 example emits a `SemanticReportProtocolId` marker, `SemanticReportId` placeholder, capability-identity set, and separately versioned run-observation envelope containing its `RunObservationProtocolId` marker, `RunObservationId` placeholder, exact semantic-report backlink, observation coverage/telemetry, and telemetry-exclusion fact.

| Example | Schema source | Identity fields the generator must emit |
|---|---|---|
| B.1 | Constitution §10.6 `OpenReport` | `SourceRootId`; every `RevisionGraphId`; selected `DocumentViewId` or explicit alternatives; exact-preservation interval facets; metadata history; security reachability/effect inventory and coverage |
| B.2 | Constitution §10.6 `RenderReport` | exact `DocumentViewId`; source-backed `RevisionGraphId`; render `DerivationId`; selected revision/hypothesis; effective dialect; resource/unsupported-feature accounting; pixel artifact identity |
| B.3 | Constitution §10.6 `TransformReceipt` | role-labeled root + `DocumentViewId` + `ExpectedStateId` for every document input; artifact/origin for every asset; candidate/output roots |
| B.4 | Constitution §10.6 `DivergenceReport` | `SourceRootId`; `RevisionGraphId`; `DocumentViewId`; relevant `DerivationId`; external input identity; per-processor artifact, version, configuration, environment, and bound independent output identity; exact output-identity projection |
| B.5 | Appendix A.13 checker boundary | package root; checker capability identity; availability and coverage accounting |

### B.1 Open report

```json
{
  "schema": "org.monkeybee.open-report.v8-example",
  "semantic_report_protocol_id": "PENDING-HUMAN-RATIFICATION-D1-D2",
  "semantic_report_id": "semantic-report:open-example-nonproduction",
  "capability_identities": ["capability:open-example"],
  "run_observation": {
    "schema": "org.monkeybee.run-observation.v8-example",
    "run_observation_protocol_id": "PENDING-HUMAN-RATIFICATION-D1-D2",
    "run_observation_id": "run-observation:open-example-nonproduction",
    "semantic_report_id": "semantic-report:open-example-nonproduction",
    "observation_coverage": "no-operational-measurements-recorded",
    "telemetry": {},
    "excluded_from_semantic_identity": true
  },
  "source": {
    "source_root_id": "source-root:example",
    "length": 1839021,
    "identity": {
      "class": "verified-content",
      "algorithm": "PENDING-HUMAN-RATIFICATION-D1-D2",
      "digest": "example-digest",
      "disclosure": "internal-only"
    },
    "availability": "Embedded"
  },
  "revision_graphs": [
    {
      "revision_graph_id": "revision-graph:strict-example",
      "discovery_protocol": "revision-discovery:example",
      "observed_range_coverage": [[0, 1839021]],
      "limits": "limits:example",
      "assumptions": [],
      "supersedes": null,
      "revisions": [
        {"revision_id": "revision:0", "xref": "byte-span:example-0", "signature_coverage": []},
        {"revision_id": "revision:1", "xref": "byte-span:example-1", "signature_coverage": ["signature:1"]}
      ]
    },
    {
      "revision_graph_id": "revision-graph:recovery-example",
      "discovery_protocol": "revision-discovery:recovery-example",
      "observed_range_coverage": [[0, 1839021]],
      "limits": "limits:example",
      "assumptions": ["recovery-assumption:example"],
      "supersedes": null,
      "revisions": []
    }
  ],
  "selected_document_view_id": null,
  "live_document_view_alternatives": [
    "document-view:hypothesis-7",
    "document-view:hypothesis-9"
  ],
  "strict_parse": {
    "outcome": "refused",
    "reason": "invalid_xref_chain",
    "diagnostics": ["MB-XREF-0042"]
  },
  "recovery": {
    "outcome": "ambiguous",
    "discriminators": ["external-observation-required"]
  },
  "encryption_state": "inventoried",
  "signatures_found": ["signature:1"],
  "exact_preservation_interval_facets": {
    "parse_or_semantic_ownership": [
      {"range": [0, 1839021], "owner": "raw-syntax:example"}
    ],
    "raw_preservation_requirement": [[0, 1839021]],
    "explained_subranges": [[0, 1839000]],
    "unexplained_subranges": [[1839000, 1839021]],
    "revision_membership_or_supersession": [
      {"range": [0, 1839021], "revision_graph_id": "revision-graph:strict-example"}
    ],
    "cryptographic_coverage": [
      {"range": [0, 1024], "signature_id": "signature:1"}
    ],
    "disclosure_or_sensitivity_class": [
      {"range": [0, 1839021], "class": "internal-only"}
    ],
    "transformation_carry_or_drop_intent": []
  },
  "metadata_across_revisions": [
    {"revision_id": "revision:0", "metadata_object_ids": ["object-version:metadata-0"]},
    {"revision_id": "revision:1", "metadata_object_ids": ["object-version:metadata-1"]}
  ],
  "security_reachability_effect_inventory": {
    "scope": {
      "revision_graph_ids": ["revision-graph:strict-example", "revision-graph:recovery-example"],
      "document_view_ids": ["document-view:hypothesis-7", "document-view:hypothesis-9"]
    },
    "coverage": {
      "analyzed": ["document-view:hypothesis-7"],
      "unavailable": ["document-view:hypothesis-9:resource-limit"]
    },
    "nodes": [
      {
        "node_id": "behavior-node:example",
        "trigger": "trigger:example",
        "target": "object-version:target-example",
        "revision_id": "revision:1",
        "visibility": "reachable-in-selected-view",
        "required_host_capability": null,
        "executable_feature_class": "inventory-only:example",
        "sanitization_state": "not-transformed",
        "evidence": ["ByteExact"],
        "provenance": ["byte-span:behavior-example"]
      }
    ]
  },
  "unexplained_bytes": [],
  "resource_usage": {"decoded_bytes": 920131, "objects": 834},
  "no_claims": ["cms_trust_not_evaluated"]
}
```

### B.2 Render report

```json
{
  "schema": "org.monkeybee.render-report.v8-example",
  "semantic_report_protocol_id": "PENDING-HUMAN-RATIFICATION-D1-D2",
  "semantic_report_id": "semantic-report:render-example-nonproduction",
  "capability_identities": ["capability:render-example"],
  "document_view_id": "document-view:example",
  "revision_graph_id": "revision-graph:strict-example",
  "derivation_id": "derivation:render-example",
  "selected_revision_or_recovery": {
    "revision_id": "revision:1",
    "recovery_hypothesis_id": null,
    "selection_evidence": ["selected-view-binding:example"]
  },
  "effective_dialect": {
    "record_id": "effective-dialect:example",
    "revision_id": "revision:1"
  },
  "page_selection": {"page_id": "page:12", "box": "CropBox"},
  "processing_profile": "strict-display:example",
  "output_profile": "screen-output:example",
  "compatibility_profile": "strict:example",
  "raster": {"width": 1275, "height": 1650, "format": "rgba8-premul"},
  "color_pipeline": "color-pipeline:example",
  "outcome": "complete",
  "coverage": {"page_region": "full", "operators": "all-admitted"},
  "pixel_artifact": {
    "artifact_id": "artifact:pixels-example",
    "hash_algorithm": "PENDING-HUMAN-RATIFICATION-D1-D2",
    "digest": "example-digest"
  },
  "cache_identity": "derivation-cache:example",
  "determinism": "D2 Same-target pixels",
  "substitutions": [],
  "skipped_or_refused_operators": [],
  "warnings_and_refusals": [],
  "unsupported_or_policy_blocked_features": [],
  "resource_usage": {
    "semantic_counters": {"page_operators": 328, "decoded_bytes": 8192},
    "fired_limit": null
  },
  "run_observation": {
    "schema": "org.monkeybee.run-observation.v8-example",
    "run_observation_protocol_id": "PENDING-HUMAN-RATIFICATION-D1-D2",
    "run_observation_id": "run-observation:render-example-nonproduction",
    "semantic_report_id": "semantic-report:render-example-nonproduction",
    "observation_coverage": "wall-time-and-peak-memory-only",
    "wall_ms": 22.1,
    "peak_bytes": 18432122,
    "excluded_from_semantic_identity": true
  }
}
```

### B.3 Transform receipt

```json
{
  "schema": "org.monkeybee.transform-receipt.v8-example",
  "semantic_report_protocol_id": "PENDING-HUMAN-RATIFICATION-D1-D2",
  "semantic_report_id": "semantic-report:transform-example-nonproduction",
  "capability_identities": ["capability:transform-example"],
  "run_observation": {
    "schema": "org.monkeybee.run-observation.v8-example",
    "run_observation_protocol_id": "PENDING-HUMAN-RATIFICATION-D1-D2",
    "run_observation_id": "run-observation:transform-example-nonproduction",
    "semantic_report_id": "semantic-report:transform-example-nonproduction",
    "observation_coverage": "no-operational-measurements-recorded",
    "telemetry": {},
    "excluded_from_semantic_identity": true
  },
  "transform_id": "transform-operation:example",
  "outcome": "partial",
  "policy": "secure-redaction:example",
  "document_input_bindings": [
    {
      "role": "base",
      "reality_root": "source-root:base-example",
      "document_view_id": "document-view:base-example",
      "expected_state_id": "expected-state:base-example"
    },
    {
      "role": "imported-page-source",
      "reality_root": "source-root:import-example",
      "document_view_id": "document-view:import-example",
      "expected_state_id": "expected-state:import-example"
    }
  ],
  "asset_input_bindings": [
    {
      "role": "replacement-image",
      "artifact_id": "artifact:replacement-example",
      "origin_ref": "origin:replacement-example"
    }
  ],
  "private_candidate_root": "transform-root:candidate-example",
  "serialized_output_source_root": "source-root:serialized-example",
  "edit_intent": "edit-intent:example",
  "changed_bytes": ["byte-span:output-example"],
  "changed_objects": ["object-version:44-example"],
  "changed_revisions": ["revision:output-example"],
  "deltas": {
    "visual": {"allowed_regions": ["rectangle:example"], "unexpected_pixels": 0},
    "text": {"removed_nodes": ["semantic-node:example"], "unexpected_changes": []},
    "structure": {"status": "checked-within-declared-scope"},
    "security": {"active_content": "removed-within-declared-scope"},
    "signature": {"original": "invalidated_by_rewrite", "new": "none"}
  },
  "internal_profile_checks": ["profile-check:example"],
  "candidate_local_falsifiers": [
    {"kind": "raw-and-decoded-search", "status": "pass", "protocol": "negative-search:example"}
  ],
  "coverage": {
    "requested": ["declared-redaction-scope"],
    "covered": ["supported-retained-objects", "supported-decoded-streams"],
    "missing": ["external-recognition:image-example"]
  },
  "unresolved_claims": ["image-semantic-absence-not-evaluated"],
  "no_claims": ["no-whole-document-semantic-absence-claim"]
}
```

### B.4 Divergence report

```json
{
  "schema": "org.monkeybee.divergence-report.v8-example",
  "semantic_report_protocol_id": "PENDING-HUMAN-RATIFICATION-D1-D2",
  "semantic_report_id": "semantic-report:divergence-example-nonproduction",
  "capability_identities": ["capability:divergence-observation-example"],
  "run_observation": {
    "schema": "org.monkeybee.run-observation.v8-example",
    "run_observation_protocol_id": "PENDING-HUMAN-RATIFICATION-D1-D2",
    "run_observation_id": "run-observation:divergence-example-nonproduction",
    "semantic_report_id": "semantic-report:divergence-example-nonproduction",
    "observation_coverage": "no-operational-measurements-recorded",
    "telemetry": {},
    "excluded_from_semantic_identity": true
  },
  "source_root_id": "source-root:example",
  "revision_graph_id": "revision-graph:strict-example",
  "document_view_id": "document-view:example",
  "derivation_id": "derivation:divergence-example",
  "input_artifact_id": "artifact:input-example",
  "processors": [
    {
      "id": "monkeybee:example",
      "executable_or_service_artifact_id": "artifact:monkeybee-example",
      "version": "version:monkeybee-example",
      "configuration": "strict-display:example",
      "environment": "environment:example",
      "output_artifact_id": "artifact:monkeybee-pixels-example"
    },
    {
      "id": "external-subject-a:example",
      "executable_or_service_artifact_id": "artifact:external-a-example",
      "version": "version:external-a-example",
      "configuration": "declared-default:example",
      "environment": "environment:external-a-example",
      "output_artifact_id": "artifact:external-a-pixels-example"
    }
  ],
  "processor_output_artifact_ids": [
    "artifact:monkeybee-pixels-example",
    "artifact:external-a-pixels-example"
  ],
  "profiles": ["strict-display:example", "declared-default:example"],
  "differing_observable_regions": [
    {"kind": "pixel-region", "page": 2, "bounds": [100, 200, 210, 260]}
  ],
  "minimized_causal_subgraph": {
    "object_version_id": "object-version:31-example",
    "program_node_id": "program-node:example"
  },
  "normative_analysis": "malformed-input-under-cited-card-set",
  "compatibility_classification": "profile-scoped",
  "witness_bundle_artifact_id": "artifact:minimized-witness-example"
}
```

### B.5 Evidence-check report

```json
{
  "schema": "org.monkeybee.evidence-check-report.v8-example",
  "semantic_report_protocol_id": "PENDING-HUMAN-RATIFICATION-D1-D2",
  "semantic_report_id": "semantic-report:evidence-check-example-nonproduction",
  "capability_identities": ["checker-capability:example"],
  "run_observation": {
    "schema": "org.monkeybee.run-observation.v8-example",
    "run_observation_protocol_id": "PENDING-HUMAN-RATIFICATION-D1-D2",
    "run_observation_id": "run-observation:evidence-check-example-nonproduction",
    "semantic_report_id": "semantic-report:evidence-check-example-nonproduction",
    "observation_coverage": "no-operational-measurements-recorded",
    "telemetry": {},
    "excluded_from_semantic_identity": true
  },
  "outcome": "partial",
  "package_root": "evidence-package-root:example",
  "checker": {
    "checker_protocol_id": "checker-protocol:example",
    "checker_capability_identity": "checker-capability:example"
  },
  "verified_claims": ["claim:1", "claim:2"],
  "unsupported_claim_kinds": ["historical-device-observation"],
  "artifact_availability": {
    "artifact:embedded-example": "Embedded",
    "artifact:missing-example": "Unavailable"
  },
  "coverage": {
    "requested": ["package-integrity", "declared-claim-checks", "historical-device-observation"],
    "covered": ["package-integrity", "claim:1", "claim:2"],
    "missing": ["historical-device-observation"]
  },
  "truncation": {"diagnostics_truncated": false},
  "limits": {"bytes_read": 1048576, "claims_checked": 2},
  "diagnostics": ["MB-PKG-0017"],
  "no_claims": ["signer-trust-not-evaluated"]
}
```

## Appendix C — Crate contract template

```markdown
# CONTRACT: <crate>

## Purpose and architectural layer

## Normative and external sources
- SpecCard IDs
- standard/profile versions
- algorithm references
- dependency provenance

## Public types and semantics

## Invariants

## Error and refusal model

## Evidence semantics

## Resource limits and complexity

## Determinism class

## Cancellation behavior

## Unsafe boundary

## Feature flags

## External dependencies

## Conformance tests

## Property and metamorphic tests

## Fuzz targets

## Independent falsifiers

## Performance claims and measurement lanes

## No-claim boundaries

## Migration and compatibility notes
```

The contract is reviewed before dependents consume the crate.

---


## Appendix D — Source-registry classes

| Class | Examples | Implementation use |
|---|---|---|
| `NORMATIVE` | Authorized ISO standards and incorporated normative references | May determine semantics; cite clause via SpecCard. |
| `ERRATA` | Formal errata collections and amendments | May modify requirement interpretation; versioned. |
| `MODEL` | Arlington PDF Model | Machine-readable complementary rule source; not a standalone specification. |
| `PROFILE` | PDF/A, PDF/UA, validation profiles | Profile-specific rules; do not redefine core PDF. |
| `CORPUS-PUBLIC` | Public conformance/validation samples | Test evidence subject to license. |
| `CORPUS-RESTRICTED` | Private real-world or security corpus | Held-out/restricted evaluation only. |
| `ALGORITHM` | Papers/books for rasterization, compression, color, fonts, crypto | Generic algorithm guidance with citation. |
| `DEPENDENCY` | Permissively licensed generic Rust crate | Narrow implementation substrate; pinned and audited. |
| `BLACKBOX` | External PDF processor executable/service | Experimental compatibility evidence only. |
| `FORBIDDEN-IMPLEMENTATION` | Existing PDF engine source | Not used to derive MonkeyBee implementation. |
| `PROJECT` | SpecCards, contracts, decision records, tests | Authoritative only within declared scope and version. |

Every implementation context declares which source classes it may access.

---

## Appendix E — Release claim matrix template

| Capability | Profile/version | Evidence tiers | Independent oracle | Determinism | Performance lane | No-claim boundary |
|---|---|---|---|---|---|---|
| Strict file open | PDF 2.0 core @ current errata | G0–G6 | Arlington/independent validator | D0 | open corpus | Recovery not included |
| Page rendering | strict-display@N | G0–G7 | analytic + external renderers | D2/D3 | workload matrix | print overprint profile separate |
| Text extraction | text-evidence@N | G0–G7 | manual truth + external extractors | D0 | text corpus | reading order may be heuristic |
| Canonical write | canonical-unencrypted@N, secure-encrypted@N, or admitted signature-profile@N | G0–G7 | independent readers/validators/crypto vectors | D1 or D1R by exact profile | generation corpus | prior PDF signatures are not preserved by canonical rewrite; encryption varies; signature determinism is scheme/time/service-specific |
| Secure redaction | secure-redaction@N | G0–G7 | independent forensic tools | D1 for unencrypted output; D1R when re-encrypted | redaction corpus | scoped to enumerated search adapters |
| PDF/A validation | profile ID | G0–G7 | independent validator | D0 | validation corpus | unsupported rules listed |
| PDF/UA validation | profile ID | G0–G7 | independent validator + human-review boundary | D0 | tagged corpus | semantic quality, usability, intent, and legal compliance are not fully machine-proved |
| Supremacy S1 — rendering | `supremacy-s1@N`; exact `FieldDefinitionId` (at minimum separate pure-Rust and all-open PDF→raster fields); `named_set_lead`, `registered_open_field_lead`, or `observed_field_lead`; eligible cutoff + exact per-output-contract artifacts (initial native-raster characterization pool: hayro 0.7.1, `pdf_oxide` 0.3.74, `stet-pdf-reader` 0.2.1, `pdfpurr` 0.4.0, `fop-pdf-renderer` 0.1.2, `pdfsink-rs` 0.2.9, `pdf-rs/pdf_render`; printpdf 0.10.1 is PDF→SVG unless a complete raster path is pinned; oxidize-pdf/pdforg-render require contract characterization) + canonical upstream fixture manifest | G0–G7 + §24.16 | analytic/standards adjudication + named renderers + held-out S2 | D2/D3 by profile | full-denominator paired equivalence/non-inferiority gate, then atomic lead | Complete included-fixture accounting is mandatory. PDF→raster, PDF→SVG, screenshot, and intermediate-layout paths are not interchangeable. Hayro’s release gaps are hayro-specific, malformed recovery is an inferred conjunction stratum, and no win against one rival establishes field lead over an unmeasured challenger. |
| Supremacy S2 — wild-tail | `supremacy-s2@N`; claim scope + stewarded stratified sample, sampling frame, cutoff, competitor artifacts | G0–G7 + adjudicated outcome accounting | standards cards + heterogeneous renderers + independent steward/expert adjudication | D0 reports; D2/D3 pixels | document-level paired/cluster-aware strata | Ledger publication does not imply leadership; sample/profile bias, indeterminate malformed cases, credentials, policy, timeout, resource, unsupported, and partial outcomes remain separate. |
| Supremacy S3 — structured extraction/agent evidence/provenance | `supremacy-s3@N`; public benchmark exact revision/config + independently stewarded held-out corpus + material challengers including OpenDataLoader, `pdf_oxide`, and PDF Reader MCP | G0–G7 + §24.16 | independently reproduced scorer + held-out truth + output/provenance checker | D0 where declared; stochastic protocol otherwise | quality, latency, locality, GPU/model, refusal, page/bbox evidence, trust/OCR evidence, and exact provenance axes | Benchmark quality or page/bbox citations cannot prove byte/revision provenance; benchmark-owner conflict, model routes/attempts, and non-runnable preserved predictions are disclosed. |
| Supremacy S4 — generation scorecard | `supremacy-s4@N`; exact `FieldDefinitionId` (separate pure-Rust and all-open generation fields) + claim scope + krilla anchor + every material eligible open generator/non-dominated comparator (including Stet/pdfpurr where eligible) for each atomic target/profile/feature intersection; separately classified opaque systems such as PDFluent where lawful | G0–G7 + §24.16 | strict reopen + Arlington + veraPDF + aligned multi-viewer corpus | D1/D1R by profile | atomic generation, file-size, refusal, and writer-extension scorecards | No scalar combines generation correctness with MonkeyBee-only secure encryption or receipts; no win over krilla alone establishes field lead. Signature analysis/editing are S5 conjunctions. **Open decision 8:** PDF/A-1 remains excluded unless §3.2 admits PDF 1.4. |
| Supremacy S5 — atomic candidate conjunctions | one row per exact conjunction, claim scope, comparator search, date, metric, expiry, and workflow falsifier | G0–G7 | capability-specific independent falsifiers | capability-specific | workflow-specific | `uncontested` is field status after a dated search; it is not an outcome, global absence, aggregate superiority, or proof against closed systems. |
| Supremacy S6 — performance escalation | `supremacy-s6@N`; exact `FieldDefinitionId` (separate all-open and pure-Rust performance fields) + claim scope + PDFium/MuPDF anchors + every material eligible native/open and pure-Rust artifact/non-dominated comparator, workload, machine, profile, cache/thread/isolation state | G0–G6 + correctness/coverage gate | reproducible benchmark lab + output equivalence checks + independent statistical reanalysis | workload-specific | per-axis non-inferiority, Pareto lead, or `incomparable` | **Open decision 9:** inactive while §26.3 retains competitive posture; no win over named anchors alone establishes field lead; no averaging away memory/correctness/safety/evidence regressions; contract-bypassing paths are disqualified. |

Every supremacy row records exact `FieldDefinitionId`, claim scope, lifecycle, field status, and outcome separately; considered challengers and selection rationale; primary analysis unit and paired/cluster structure; denominator/exclusions; effect/precision target, stopping rule, multiplicity, uncertainty, and stochastic attempt selection; refusal/missing accounting; oracle lineage; expiry; and superseding report. Outcomes distinguish `leading`, `equivalent`, `non_inferior`, `trailing`, `incomparable`, `indeterminate`, and `disqualified`. Only uncertainty-aware `leading` under the exact declared field scope supports a supremacy headline. No release process may fill this table with “yes,” “best,” or “mogged” in place of evidence.

## Appendix F — Glossary

**Artifact** — A content-addressed durable output such as decoded bytes, image, report, repaired PDF, or evidence package.

**Canonical rewrite** — A new deterministic source root produced from selected effective semantics, potentially discarding history and unreachable data under policy.

**Compatibility profile** — A named, versioned set of deliberate processing choices justified by external behavior or application needs, isolated from strict conformance.

**Document Reality** — One immutable Source, Draft, or Transform root plus its explicit derived revision graphs/views, claims, origins, lineage, and derivations across byte, semantic, visual, textual, structural, security, and compatibility consequences. A Source root identifies bytes only; it can admit several revision graphs and effective views and therefore has no singular timeless revision or semantic state.

**Source root** — One immutable byte snapshot and its availability/integrity contract. Revision graphs, selected document views, and semantic states are derived identities and never mutate or redefine the source root.

**Revision graph** — One immutable, versioned discovery of revision/object occurrences and admissible chains over a Source root, with exact protocol, coverage, limits, assumptions, and evidence.

**Draft intent commitment** — The canonical frozen intent/assets/declared-data identity used by a Draft root. It does not assert that automatic layout, shaping, pagination, or inferred structure has already been realized.

**Draft root** — A source-free, versioned authoring-intent root identified by `DraftIntentCommitment`. It binds intent, assets, and declared semantic layout/shaping data—not incidental implementation builds, which belong to derivation receipts unless realized output is itself supplied as intent.

**Transform root** — An immutable provenance-bearing finalized result derived from exact role-labeled root/`DocumentViewId` or asset/origin input bindings under a frozen intent log and provenance policy. Operation-specific `ExpectedStateId`, caller authorization, capability leases, idempotency, and publication generations remain in proposal/admission/receipt identity rather than contaminating document-reality identity. Its `RealityStateCommitment` combines the canonical semantic result with admitted inputs, origins, and intents while excluding later receipts, lineage maps, caches, and root-scoped output IDs that would create a cycle.

**Rooted origin** — A provenance reference qualified by its `RealityRoot` and local origin-node identity. Candidate-local origin references may exist only during finalization and must be resolved to rooted references before publication; a bare local origin ID never denotes a cross-root parent.

**Source snapshot** — An immutable complete or partial byte view with a typed identity. Persistent caches require verified content or a stable authority/version contract.

**Evidence facet** — One dimension of justification such as byte exactness, normative basis, bounded approximation, compatibility observation, recovery, heuristic inference, empirical measurement, or an external/cryptographic check. Partiality, ambiguity, and refusal are outcome states, not evidence facets.

**Honeycomb** — The system of synchronized, provenance-linked views over one document reality.

**Material ambiguity** — Two live interpretations that change effective objects, appearance, text, structure, signatures, attachments, or security conclusions.

**No-claim boundary** — A precise statement of what users may not infer from a current implementation or report.

**Preservation mode** — Append-only or minimally invasive output that retains unchanged bytes and revision history.

**Recovery** — Bounded hypothesis search over malformed input, producing assumptions and alternatives rather than silent conformance.

**SpecCard** — A stable project-authored paraphrase of a bounded normative requirement linked to exact source clauses, errata, tests, and contracts.

**Tombstone** — A durable record of a falsified hypothesis or retired rule, including the evidence that killed it.

**Semantic state ID** — A provenance-free commitment to admitted document values, relationships, order/multiplicity, and selected malformed/unknown semantics under one canonical `SemanticScopeId` manifest. The scope enumerates all included axes and meaning-changing policies; there is no unqualified universal semantic identity. It does not imply common bytes, history, origins, signatures, authority, or preservation rights, and may be shared across roots only when those scoped meanings are equal.

**Symmetry class ID** — A canonical semantic equivalence class plus multiplicity for members that have no admissible individual distinction. Stable member identity requires an ordered occurrence, semantic path, rooted origin, explicit intent, or another declared anchor; an allocation slot is not meaning.

**Reality-state commitment** — The finalized semantic state plus exact transform input bindings, origins, frozen intentions, and provenance policy used to identify one Transform result. It is not Draft intent identity.

**Expected state** — An operation-specific canonical precondition commitment binding the exact view, selected anchors/substrate facts, relevant authority/policy/signature/transaction generations, and immutable external snapshots that must still hold at publication. It is revalidated rather than trusted as a mutable label, and excludes unrelated ambient state.

**Capability consequence contract** — The versioned machine contract for one public operation/profile/subclaim across every surface: input identity and semantic scope, authority and expected state, budgets and transactions, outcome/evidence/determinism/replay law, privacy and availability, falsifiers, release claim, expiry, and no-claim boundary. Surfaces may narrow but not widen it.

**Evaluation protocol ID** — The content-addressed, independently time-committed pre-unblinding specification of a comparison or foundry/held-out evaluation. Material amendment creates a new ID.

**Competitor-discovery protocol ID** — The independently committed pre-search field definition and search process—registries, repositories, queries, languages, scouts, nominations, cutoff, and exclusions. The later `CompetitorDiscoveryReportId` commits what that protocol actually found and froze before measurement design.

**Structural / empirical / adaptive maturity** — Respectively: known-invariant coverage; real operational experience under declared exposure; and demonstrated assimilation of genuinely novel conditions. Evidence for one does not automatically establish another.

**Semantic anchor** — A typed `DocumentViewId`/`DerivationId`-bound reference to document meaning and geometry carrying substrate digest, evidence, coverage, ambiguity, and expected state; proposal, validation, approval, and apply authorities remain separate.

**Supremacy comparison cutoff** — The predeclared date and eligibility boundary that determines which released competitor artifacts may be selected for one comparison.

**Field definition** — A versioned canonical comparator-eligibility boundary (`FieldDefinitionId`). Pure-Rust, all-open, observed opaque, native raster, SVG conversion, and other materially different fields are never conflated.

**Supremacy field/scope/status/outcome** — Every result first binds an exact versioned `FieldDefinitionId`; scope is `named_set_lead`, `registered_open_field_lead`, or `observed_field_lead`; lifecycle is proposed/active/lapsed/withdrawn; discovery coverage and field status are separate; outcome is `leading`/`equivalent`/`non_inferior`/`trailing`/`incomparable`/`indeterminate`/`disqualified`. Only a leading registered/observed-field result supports the internal supremacy headline; no global-best inference follows.

**Signer role** — The explicit authority under which a receipt or manifest is signed, such as release/build, caller, service instance, organization, or hardware attestation. Signature verification authenticates that scoped assertion; it does not establish computation by itself.

**Virtual span** — A location inside a decoded or generated artifact linked back through a derivation to source bytes.

---

## Appendix G — Standing fresh-context review questions

1. Is the Honeycomb representation actually smaller in conceptual burden than separate parser/render/text/edit models?
2. Which view owns identity when a malformed file has multiple revision chains?
3. Can exact preservation coexist with dictionary/profile semantics without accidental normalization?
4. Is the evidence vector expressive enough to prevent all important laundering paths?
5. Which claims require stronger formal types rather than report metadata?
6. Can every embedded sublanguage truly share one sandbox contract?
7. Is the page VM boundary placed correctly relative to Type 3 fonts, patterns, forms, and transparency groups?
8. Does the color design honestly distinguish display approximation from print behavior?
9. Is a full-coverage memory-safe JPX/JBIG2 plan credible, and what subset should the first release declare?
10. Does the font plan handle the difference among code, CID, glyph, outline, and Unicode cleanly?
11. Which base-font substitution policy can be shipped legally and deterministically?
12. Does secure redaction cover every historical and indirect representation of information?
13. Can the writer be deterministic while using third-party compression and shaping crates?
14. Are external processor experiments sufficiently reproducible to support compatibility profiles?
15. Does recovery scoring contain hidden subjective weights that could produce fragile behavior?
16. Which crate boundaries will force constant lockstep changes?
17. Which layer boundaries or prerequisite assumptions are missing or overly conservative?
18. Are the flagships adversarial enough to reveal integration failures?
19. What user/operator complexity is still being externalized?
20. Which “alien artifact” evidence would be invalidated by hidden search, selection, or runtime dependencies?
21. What held-out extension is most likely to break the architecture after completion?
22. Which major workflow still lacks a refusal or rollback story?
23. Which standards/profile claims require a domain expert outside the agent ecology?
24. Is the foundry measurable without turning proxy metrics into goals?
25. What should be deleted, merged, or deferred before workspace freeze?
26. Can a transform author genuinely new content without a fake source/draft parent, and can every other derived object prove its required parents?
27. Is every root/content identity grammar acyclic, or does any identity include a receipt or output ID that depends back on it?
28. Can two recovery hypotheses, profiles, capability sets, or algorithm versions accidentally mint the same page/program/primitive/text identity?
29. Does any replay, attestation, proof, validator, or equivalence certificate claim correctness beyond the exact relation it checks?
30. Can any comparator cutoff, eligibility rule, denominator, exclusion, aggregate, or “parity” label counterfeit a supremacy lead?
31. Does every comparative analysis use the true independence unit, paired/cluster structure, predeclared stopping rule, and full attempt distribution?
32. Is a `named_set_lead` being described as a registered/observed field lead, or any scoped field result being described as global?
33. Can a public transparency log show one consistent history to mutually distrustful clients, and is every membership commitment safe to disclose forever?
34. Does a DraftRoot represent caller intent rather than whichever layout/shaping implementation happened to realize it?
35. Does every TransformRoot commit to the admitted result rather than only a recipe, without hashing its own later IDs?
36. Are baselines and ablations strong enough that MonkeyBee wins against the best ordinary alternative rather than a sabotaged control?
37. Can a heuristic/ambiguous semantic anchor ever authorize a destructive edit without explicit policy-approved confirmation?
38. Can a lazy resolver or fallback selector reuse a cache entry after a higher-priority resource appears, disappears, or changes without that selection fact being in the dependency manifest?
39. Is every machine-readable status token canonical across schemas, reports, ledgers, prose examples, and migrations, or can punctuation/capitalization create two meanings for one state?
40. Does every structured-authoring path distinguish caller-declared intent from realized pagination/layout, and can the realized semantic result be independently reproduced or checked without treating an implementation accident as intent?
41. Can two different histories share `SemanticStateId` without sharing authority, signatures, preservation rights, or origins—and can every history-sensitive path prove it binds the exact `DocumentViewId`/`RevisionGraphId` plus `RealityStateCommitment` where applicable?
42. Does canonicalization treat symmetry as multiplicity/equivalence rather than inventing an order or refusing an ordinary document?
43. Was every “predeclared” protocol independently committed before unblinding, and does every amendment force a new protocol ID and fresh confirmatory data?
44. Was the competitor-discovery protocol independently committed before searching, did the later report cover package registries, repositories, benchmark entrants, search languages/terms, scouts and nomination windows, and was that report frozen before measurement design—or is “field” merely the systems the author remembered?
45. Can any sandboxed tenant reach ambient application/document APIs, dynamic code generation, UI, files, network, process, clock, locale, or randomness outside its typed capability manifest?
46. Can a Form display cache be reused across a changed caller CTM, clip, color/blend/soft-mask state, optional-content decision, output profile, or non-isolated backdrop?
47. Does any nonce receipt claim global uniqueness without an authenticated per-key allocation domain, or ignore crashes/clones/distributed writers?
48. Can a crash between edit commit and response lead an agent to reapply the same mutation, and can a multi-anchor batch become partially visible?
49. How many adaptive queries and how much feedback has each held-out set exposed before it ceased to be independent?
50. Is a foundry claim current, historical, maker-relative, or indeterminate after rerunning the strongest contemporaneous baseline?
51. Is synthetic assurance being mislabeled as empirical maturity, or a short evolution trial as a mature lineage?
52. For every new capability, what existing primitive made it cheap in specification, verification, and integration—and what parallel machinery did it add?
53. Does any SourceRoot or root-global object falsely carry one semantic state across distinct revisions or recovery alternatives?
54. Does `SourceRootId` absorb a parser/recovery-derived revision graph, or does every history-sensitive operation bind an explicit immutable `RevisionGraphId` through `DocumentViewId`?
55. Does every `SemanticScopeId` enumerate signatures/security, structure, metadata/navigation, historical state, layout realization, and all meaning-changing policies it claims to compare?
56. Does any public API assign stable individual identity inside a symmetry class without an ordered, semantic, provenance, or caller-intent anchor?
57. Does any signature profile confuse approved deterministic derivation with unsafe nonce reuse, or classify time/provider variability as algorithmic randomness?
58. Did each comparator receive its strongest eligible configuration and the same bounded tuning/integration help, with failed wiring triaged before scoring?
59. Is any S1/S6 denominator treating PDF→SVG, extraction screenshots, intermediate-layout rasterization, and native PDF→raster as interchangeable without a pinned end-to-end adapter and full cost accounting?
60. Can any transform result input name only a root while omitting the exact `DocumentViewId`/source-backed `RevisionGraphId`, or can its separate proposal/admission omit the canonical `ExpectedStateId` and authority recheck?
61. Does any Draft root pretend that derived pagination/layout/shaping is frozen caller intent, or use a finalized-result commitment before a result exists?
62. Do `OpenReport`, render/text/validation reports, recovery reports, and transform receipts all bind the exact root/graph/view identities needed to interpret them later?
63. Can an idempotency key expire or cross tenant/schema boundaries while an earlier mutation remains observable, or can its request commitment leak confidential membership?
64. Which production-ledger entries are prospective and which are retrospective, and is any foundry claim silently relying on the latter?
65. Is every `ExpectedStateId` an operation-specific canonical predicate commitment that is re-evaluated at publication, or can a caller-controlled label/timestamp authorize stale mutation?
66. Does every public capability and atomic claim resolve to one `ConsequenceContractId`, and do all Rust/CLI/C/WASM/service/report/benchmark/release surfaces either match or explicitly narrow its identity, authority, outcome, evidence, determinism, privacy, and no-claim law?
67. Does every field claim bind an exact `FieldDefinitionId`, and are pure-Rust, all-open, closed/opaque-observed, native-raster, SVG, and other materially different fields reported separately rather than merged into one favorable adjective?
68. Does any `TransformRootId` include transient `ExpectedStateId`, caller authority, capability lease, idempotency, or publication-generation facts that belong in admission/receipts rather than document reality?

---

## Coda

The ordinary PDF-engine project asks how to parse enough syntax to display pages and write enough objects to create documents.

MonkeyBee asks a stricter question:

> **Can one memory-safe Rust substrate preserve an honest causal relationship among hostile source bytes, historical revisions, object semantics, executable page programs, appearance, text, logical structure, security state, compatibility behavior, and every transformation made afterward?**

If that relationship exists, the familiar products become projections of one system:

- parser;
- renderer;
- text extractor;
- validator;
- generator;
- editor;
- repair laboratory;
- redaction engine;
- forensic instrument;
- compatibility atlas;
- and evidence-package checker.

The post-agent leap is not that agents can implement all of those modules quickly.

It is that the project can discover and enforce a representation in which those modules cannot quietly disagree, a foundry in which failures become permanent structure, and a lineage in which new capabilities inherit the whole artifact rather than arriving as generated sediment.

This plan is intentionally large because implementation is where unresolved ambiguity becomes expensive.

Revision five preserved the preceding plan’s architectural spine while integrating the dated competitive doctrine, six lanes, new bets/workflows/flagships, risks, and nine unresolved choices. Revision six preserved that merge history and performed the first full-document post-merge correction. Revision seven preserves both histories and closes another layer of false certainty: semantic equality is separated from provenance-bearing reality and from view selection; symmetric graphs use classes/multiplicity rather than invented member IDs; field discovery, comparator freeze, and measurement each have prospective commitments; newly found Rust renderers, generators, broad early-stage libraries, and a commercial SDK enter the register; competitor configuration/tuning is symmetric; typed sandbox capabilities and statically admitted helper graphs replace the contradictory phrase “no host calls”; Form caching binds caller/backdrop state; encryption and signature nonce laws are no longer conflated; XML features are comprehensively denied/bounded; agent batches are atomic, tenant-scoped, retention-safe, and crash-indeterminate retries are not replayed; hidden sets have adaptive-access budgets; retrospective provenance is not mislabeled precommitment; historical foundry wins are checked against contemporaneous baselines; bounded moonshot probes may run in parallel without creating a moonshot critical path; maturity classes remain distinct; artifact, foundry, lineage, and composite alienness receive separate ladders; operation-specific expected-state commitments prevent stale publication without contaminating result-root identity; and atomic consequence contracts keep every public surface and release claim under one semantic law; and `FieldDefinitionId` prevents a pure-Rust or format-adapter result from masquerading as an all-open or global lead. Open decisions 1–9 remain unresolved exactly where the addendum required.

Version 0.7 does not claim that the conjunction has been achieved. It makes the intended wins harder to counterfeit: a later implementation cannot select a convenient opponent, erase exclusions, collapse uncertainty, call parity supremacy, sign an assertion and call it computation, replay the same error and call it correctness, route document text into authority, alias incompatible views, or substitute a benchmark win for the post-agent production proof. Extreme optimization remains welcome; changing the proposition after seeing the result does not.

The first job is not to launch one hundred agents. The first job is to make the object they will collectively build precise enough that one hundred agents do not collectively invent one hundred subtly different PDF engines.
