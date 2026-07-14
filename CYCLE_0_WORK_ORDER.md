# Cycle 0 Work Order

**Version:** 1.0
**Date:** 2026-07-14
**Governed by:** MONKEYBEE_CAMPAIGN_CHARTER_v1.md
**Scope law:** Cycle 0 is plan-space only. No implementation swarm. Its outputs are documents, commitments, decisions, and the Cycle 1 beads graph.

---

## 0. Definition of done

Cycle 0 is complete when all of the following hold:

1. Rev 7 is restructured into **Constitution v8** + shell reference corpus, with the fixes in §2 applied.
2. The **§34.9 Addendum Protocol** (§3 below) is added to the Constitution.
3. Every §35 decision in the **resolve-now** list (§4) has a recorded resolution with rationale; every deferred decision has a recorded owner-cycle.
4. The **day-zero checklist** (§5) is fully dispatched — each item either done or standing as a first-class bead with dependency edges into the gates it protects.
5. The **Charter is committed** through the tamper-evident substrate (§6), and the ledger's first entries exist.
6. The **Cycle 1 delta plan** is authored per §7, converted to beads (delta only), polished to steady state, `br dep cycles` clean.

## 1. v8 restructuring spec (kernel extraction)

**Into the Constitution (frozen kernel):**
- §6 non-negotiable principles
- §9 Document Reality Graph: identity grammars, roots, views, origins, lineage, symmetry, cache-reuse law (complete)
- §10 evidence algebra: facets, composition rules, outcome model, diagnostics schema, report identity-binding laws, consequence-contract mechanism
- §11 work contexts, budgets, limits, cancellation, capability leases, transactional outputs, panic policy
- §4 clean-room and specification-provenance protocol (SpecCard law)
- Layer law and crate-boundary budget rules (§8 direction table + §30.1.1) — **explicitly not the concrete crate atlas**, which remains provisional shell content per §30
- Canonical hashing/serialization grammars (as resolved in §4 below)
- §33 post-agent evaluation protocol, §34 refinement/freeze protocol, plus the new §34.9

**Stays in the shell (reference corpus for delta plans):** §12–§28 domain sections, §5 workflows, §7 bets, §31 flagships, §24.12–24.16 supremacy doctrine, §30 crate atlas, appendices.

**Superseded by the Charter:** nothing in Rev 7 is deleted; the Charter *adds* the cycle staging above §3.0's envelope table and cites it. Envelope definitions themselves stay in the Constitution's shell interface (they are claim vocabulary, not scheduling).

**Mechanical rules for the extraction:** stable section identifiers preserved; every law gets exactly one normative home; hand-restatements elsewhere are either deleted, converted to citations, or marked `generated-echo` with their source ID; Appendix B is **regenerated from the current schemas**, never hand-edited.

## 2. Rev 7 fixes to apply (from AUDIT_FINDINGS_LEDGER.md)

Apply during extraction, grouped by locus:

**Grade-A / structural**
- R1-1: Regenerate Appendix B examples to carry every §10.6-mandated identity (DocumentViewId, RevisionGraphId, DerivationId, ExpectedStateId, role-labeled input bindings). Add a validator rule: schema examples must carry all mandated fields.
- R2-N1: Envelope fix — add "structural signature/ByteRange discovery" to R0 required consequence; add "signature-impact classification (structural, not trust)" to R2; cryptographic/trust validation remains R3.
- R1-4: Add the scope-totality condition to §22.4 — canonical byte-identity holds only under a semantic-canonical profile whose SemanticScopeId is serialization-total.

**Security/DoS**
- R2-N2: Add the hasher law — attacker-keyed maps require DoS-resistant hashing or ordered structures; performance-motivated hasher swaps require an explicit contract note.
- R2-N3 + R1-8: Add a canonicalization/symmetry work dimension to the §11.2 limits table; add the adversarial-symmetry DoS row to §32; name the complexity class in §22.3.
- R1-6: Add the vulnerability-disclosure/security-response section (intake, triage, embargo, advisory schema, claim-withdrawal linkage).

**Enumeration gaps**
- R1-7: Add encrypted-payload/unencrypted-wrapper documents to §16.8 reachability and §23.12 sanitization classes; add PhoneticAlphabet/Phoneme, Prop_Build, PDF 2.0 UTF-8 text strings, PDF/VT naming, /Tabs, NeedsRendering to their sections' inventories.

**Wording/consistency**
- R1-2: Bet 24 "targets" → "candidate invariants" (aligns with open decision 5).
- R1-3: Flagship D — merge or explicitly differentiate the duplicated forensic-tool bullets (if two lineage-diverse tools are intended, say so).
- R2-N4: Appendix A — fix the `child()` limits story (caller-provided storage, owned Limits, or min-at-check semantics) and add the DiagnosticCollector concurrency sentence.
- R2-N5: One sentence disambiguating §33.5 Baselines C/D from §33.6 ablations (repo-level vs mechanism-level; one experiment may not count twice).
- R1-5: Add the independence-ecology row to §35.1 assumptions (who stewards/reviewers are, cost, and the honest downgrade path).

**Cross-document**
- R2-N7: Stamp ALIEN_ARTIFACT.md superseded-in-part by the re-audit (or regenerate it); the corpus must not contradict itself silently.
- R2-N8: PROJECT_OVERVIEW — add Crypt to the filter list or mark the list non-exhaustive; soften the pdf.js browser-coupling line.

## 3. §34.9 Addendum Protocol (text to add to the Constitution)

> **34.9 Addendum protocol.** Every capability cycle after the kernel cycle proceeds as follows, and no cycle's delta plan may be authored before the previous cycle's close gate passes.
>
> 1. **Archaeology.** The delta plan opens with a repository-reality survey (code, tests, contracts, drift-audit output). Claims about existing structure cite the survey, never a prior plan's description.
> 2. **Kernel-touch declaration.** The delta plan declares `kernel-touch: none` or enumerates the touched kernel laws. Any touch requires: kernel version bump, migration plan for all affected identities/receipts, claim-lapse review, and Charter change-control entry.
> 3. **Contracts before beads.** Every new capability receives a consequence contract citing its SpecCardIds; falsifiers become bead acceptance criteria; the assigned Gauntlet tier is the definition of done.
> 4. **Delta-only conversion.** Beads are generated for the delta plan only. Full-plan reconversion is prohibited (feature-loss and drift vector). Polish to steady state; dependency graph acyclic.
> 5. **Execution.**
> 6. **Close gate (blocking):** (a) drift audit — generated-truth diffs, contract-truth checks, claim-registry consistency, zero Grade-A findings to pass; (b) one held-out extension probe, selected from the sealed pool, with results recorded win-or-lose; (c) SpecCard coverage check for the cycle's surface; (d) sealed cycle trial record into the production ledger: attempts, failures, retries, cost, human interventions, median and best outcomes.
>
> Cycle trial records are the campaign's foundry-distribution evidence; a cycle without a sealed record contributes nothing to any §33 claim regardless of what it shipped.

## 4. §35 decisions: resolve now vs defer

**Resolve at C0 (they gate Cycle 1 code):**
1. Content-hash algorithm and digest widths (every identity depends on it).
2. Canonical serialization grammar for hashing (identity grammars consume it).
3. DecodedStreamId cost/availability model (stream identity in the kernel).
4. Evidence-checker isolation (different-model-family or spec-only authorship — per R1-9).
5. Project license (publication and wedge sales depend on it).
6. Persistent ledger backend default (portable structured files acceptable; upgrade path noted).
7. Rust toolchain pin.

**Defer with named owner-cycle:**
- Raster backend/GPU path → C6 (perf slice).
- PDF/A-1 vs 1.7/2.0 writer conflict → C6 (profiles).
- C-ABI freeze point → post-R4 (preview at C5 per Workflow M).
- Base-font fallback pack licensing → C3 (fonts).
- S6 performance-per-fidelity metric → C7 protocol finalization (measurement design, committed before C7 begins).

Each resolution gets a §34.5-style ledger row: question, options, decision, rationale, date.

## 5. Day-zero checklist (dispatch in parallel with §1–§4)

1. Open the production ledger; first entries: Charter hash, this Work Order, protocol commitments.
2. Establish the commitment substrate (independent steward custody or witnessed append-only log). Record what was obtainable; log honestly what was not.
3. Commit discovery protocols: comparator-field discovery method, inclusion criteria, challenge-window durations. **Windows open now.**
4. Engage the independence layer: corpus steward, commitment custodian, red team (different model family + human), reviewer/adjudicator candidates. Log the misses.
5. Stand up the SpecCard pipeline: ISO 32000-2:2020 + Errata Collection license under current ISO AI-use terms; extraction protocol; two-person meaning-review staffing; coverage registry. Begin card production for the R0 surface immediately — cards run one cycle ahead of implementation.
6. Corpus program: acquire wild-tail sources; stratify; **steward seals held-out splits before any implementation exists.**
7. Draft and adopt the vulnerability-disclosure policy (from §2's new section).
8. Reserve the baseline budget (Baselines A–D, plus E where feasible) as a committed line item — per Charter risk #1, cutting it later is a formal G2 downgrade, never a quiet omission.
9. Declare clause-tagging discipline in the repository constitution: every consequence contract cites SpecCardIds from the first commit.

## 6. Charter commitment mechanics

Commit the Charter, this Work Order, the discovery protocols, and the held-out seal manifests through the substrate in one batch; record the batch hash as ledger entry #1. Any Charter amendment re-commits through the same channel with its change-control classification. Git history alone is never the substrate.

## 7. Cycle 1 delta plan requirements

The C1 delta plan (authored at the end of C0) must contain: the L0–L2 capability surface with consequence contracts (bytes/lexer/COS/xref/revisions/object streams; Flate+predictors, ASCIIHex, ASCII85, RunLength, LZW; recovery-as-hypothesis-search v1; encryption inventory **plus standard-handler read decryption with credentials** — RC4/AESV2/AESV3 and password preparation; identity/evidence/report/checker stack; CLI surface); the immune system as first-class capabilities (generated schemas, claim registry, contract-truth checks, drift auditor) with their own contracts and falsifiers; fuzz targets and the zero-reachable-panics gate; SpecCard citations throughout; the C1 close-gate definition; and explicit exclusions (no rendering, no fonts, no public-key handlers, no writer). Convert to beads, polish to steady state, validate the graph, and Cycle 1 may begin.

## 8. Explicit non-goals of Cycle 0

No implementation code. No rendering decisions beyond deferred-decision ownership. No comparator measurement of any kind. No public claims — the only publishable artifact from C0 is the committed Charter itself, and it claims nothing except the campaign's existence and rules.

---

*End of Work Order v1.0.*
