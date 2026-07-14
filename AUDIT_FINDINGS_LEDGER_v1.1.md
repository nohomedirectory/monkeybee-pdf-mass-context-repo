---
generated-by: Codex G6 conditional Charter-set successor owner
date: 2026-07-14
inputs:
  - AUDIT_FINDINGS_LEDGER.md
  - MONKEYBEE_CAMPAIGN_CHARTER_v1.md
  - CYCLE_0_WORK_ORDER.md
  - CAMPAIGN_CHARTER_REASONING.md
  - ledger/prompts/GAUNTLET_REVIEWER_PROTOCOL.md
  - gauntlet/ROUND_LOG.md (R20–R22)
  - MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md §10.3, §§24.12–24.16, §33, §§34.4–34.5
status: PROPOSED
ratification: awaiting human
evidence-status: provisional-pending-substrate
owner-fsm: DONE
---

# Consolidated Audit Findings Ledger

**Version:** 1.1 (PROPOSED — awaiting human ratification)
**Date:** 2026-07-14
**Covers:** Three full fresh-eyes audit rounds over MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md, frankensim_alienartifactness_reaudit.md, ALIEN_ARTIFACT.md, PROJECT_OVERVIEW.md, and the campaign layer itself.
**Purpose:** Immutable historical consolidation of the three v1.0 audit rounds, their severities, and their fix paths, with the versioned live-gauntlet handoff below. It is not the append target for later gauntlet packets.

**Historical v1.0 grade namespace:** Grade A = directly confirmed in the artifact by grep/derivation; Grade B = confirmed by close reading; Grade C = judgment call. These letters preserve their original historical meaning and are not silently mapped to a later scheme.
**Status codes:** `OPEN-C0` (fix at Cycle 0 per Work Order §2) · `RESOLVED-CHARTER` (incorporated into Charter v1.0) · `RESOLVED-REASONING` (correction recorded in Reasoning doc) · `NOTED` (no action required) · `SOFTENED` (finding downgraded on re-examination) · `PROPOSED-CHARTER-v1.1` (bounded successor repair awaiting human ratification) · `PROPOSED-KERNEL-SPLIT-v1.1` (selected remedy only; neither ratified nor applied until the versioned extraction lands and is verified).
**Successor relation:** Carries Audit Findings Ledger v1.0 forward in full. The bounded status, fix-description, and handoff changes are enumerated in the changelog; no original finding statement, grade, or provenance is silently regraded, and no proposed repair becomes ratified merely by appearing here.

## v1.1 changelog

| Filed finding | Exact repair in this successor |
|---|---|
| `R20-A06` | R1-5 no longer says the scout gap was resolved by Charter v1.0. It remains `OPEN-C0` and points to the proposed Charter/Work Order v1.1 scout provisioning and `named_set_lead` downgrade path. |
| `R20-A08` | R1-10 no longer treats the v1.0 kernel/shell split as a finished single-home repair. It points to the proposed Work Order v1.1 extraction of immutable §§24.12/24.16 law while the dated register and lane parameters stay refreshable. |
| `R21-A02` | C-9 now assigns ledger entry #1 to the canonical commitment-batch record/root while preserving the Charter digest as an independently addressable manifest member. |
| `R21-A11` | This successor versions the ownership handoff from historical R1–R3 consolidation to append-only Round Log packets, owner-state dispositions, and successor changelog mappings. |
| `R21-A12` | The historical v1.0 grade namespace is named explicitly and kept non-comparable to the gauntlet grade namespace without an explicit mapping; no row is regraded. |
| `R21-A13` | Standing observation 3 now counts two cited Grade-A duplication-drift examples, not the ledger's total Grade-A population. |
| `R21-A14` | R1-10 remains `OPEN-C0`; `PROPOSED-KERNEL-SPLIT-v1.1` is defined as a selected remedy awaiting ratification, landed extraction, and verification—not a completed resolution. |
| `R22-B02` (grade B; premise-supported, not promoted) | Standing observation 2 now confines its defect-surface conclusion to the three hunts run; the zero-finding result, six named areas, and coordination/evidence-plumbing observation remain unchanged in substance. |

---

## Versioned finding-store and grade handoff

- `AUDIT_FINDINGS_LEDGER.md` v1.0 remains the byte-immutable historical consolidation for R1–R3. This v1.1 successor preserves those IDs and bodies.
- Filed live-gauntlet reviewer packets remain append-only in `gauntlet/ROUND_LOG.md` under their own monotonic round-local IDs. They are not copied here or rewritten as historical rows.
- Owner qualification, `NOT-TRIGGERED` decisions, and repair routing live in the applicable owner checkpoint. A conventional successor changelog maps each qualifying live-round ID to the exact repair without changing the reviewer packet.
- Historical Audit Ledger grades use the v1.0 namespace above. Gauntlet grades use the governing reviewer protocol (`A` confirmed local defect, `B` probable with one unresolved premise, `C` judgment/optional concern). Identical letters across the two namespaces are not aggregate-compatible and never authorize implicit promotion, demotion, or regrading.

---

## Round 1 — Plan document (Rev 7)

| ID | Finding | Grade | Status |
|---|---|---|---|
| R1-1 | Appendix B report examples violate §10.6 identity laws: zero occurrences of DocumentViewId, RevisionGraphId, DerivationId, ExpectedStateId across B.1–B.4; also falsifies §0.6 check-8's audit-coverage claim | A | OPEN-C0 |
| R1-2 | Bet 24 states all three proof-kernel invariants declaratively while §34.5.1 decision 5 keeps scope open | B → downgraded round 3: "choose two or three" permits all three; wording asymmetry only | SOFTENED / OPEN-C0 (reword) |
| R1-3 | Flagship D contains near-duplicate forensic-tool bullets (merge residue, or an unstated two-tool lineage-diversity requirement) | A | OPEN-C0 |
| R1-4 | §22.4 canonical byte-identity keyed on SemanticStateId is formally unsatisfiable without a serialization-total scope condition | A | OPEN-C0 |
| R1-5 | The evidence machinery assumes an unprovisioned human ecology (stewards ×23, scouts, adjudicators, two-person SpecCard review) with no recruitment/cost/degradation plan; absent from §35.1 assumptions | A (absence) | OPEN-C0 + PROPOSED-CHARTER-v1.1 (independent scouts + explicit downgrade; awaiting ratification) |
| R1-6 | No vulnerability-disclosure / security-response policy anywhere (zero hits: CVE, embargo, coordinated disclosure) | A (absence) | OPEN-C0 |
| R1-7 | PDF-domain enumeration gaps: encrypted-payload wrapper documents (security-relevant to §16.8/§23.12); PhoneticAlphabet/Phoneme; /Prop_Build; PDF 2.0 UTF-8 text strings; PDF/VT unnamed | A (absence) | OPEN-C0 |
| R1-8 | §22.3 symmetry canonicalization is graph-canonicalization (GI-hard); adversarial cost unnamed; no budget dimension | B | OPEN-C0 (with R2-N3) |
| R1-9 | mb-checker "independence" is intra-ecology; shared premise (the F-01 killer) not countered by shared-code prohibition alone | B | OPEN-C0 (checker-isolation decision, Work Order §4.4) |
| R1-10 | Meta: the plan hand-restates its laws 4–6× each (idempotency ~25, nonce ~23), violating its own §29.5 single-source principle; R1-1 is the empirical proof of the resulting drift | A | OPEN-C0 + PROPOSED-KERNEL-SPLIT-v1.1 (selected single-home remedy for §§24.12/24.16 with §10.3/§33; resolution requires ratification, landed versioned extraction, and verification) |
| R1-11 | Minor: "availability" used for two vocabularies; cosmetic punctuation in §32; "later milestone" brushes execution-vocabulary rule | C | NOTED |

Round-1 verification also confirmed (non-findings, recorded to prevent re-litigation): inheritable-attribute set; Tm/Tlm and current path outside q/Q; word-spacing byte-32 rule; text-clip at ET; unassociated-alpha blending; object-stream single decryption; /Perms vs /P; ISO/TS 32003/32005 assignments; RFC 6979/EdDSA; GCM nonce bounds vs SP 800-38D; shading types 1–7; hybrid /XRefStm; 27-bet and workflow-letter counts; register version consistency.

## Round 2 — Plan, sketches, cross-document

| ID | Finding | Grade | Status |
|---|---|---|---|
| R2-N1 | Release-envelope dependency gap: Workflow F + §23.3 require structural signature analysis for R2 incremental writes (and Workflow B promises signatures at R0), but the capability sits only in R3 — a live instance of §34.4's own forbidden pattern | A | OPEN-C0 |
| R2-N2 | Hash-flooding DoS unaddressed: attacker-keyed maps everywhere; §26.7 performance pressure invites non-SipHash swaps; no hasher law | A (absence) | OPEN-C0 |
| R2-N3 | No canonicalization/symmetry work dimension in the §11.2 limits table | A (absence) | OPEN-C0 |
| R2-N4 | Appendix A sketch bugs: `WorkContext::child` cannot store a computed Limits intersection behind `&'b` as written ("intersects limits" comment misattributes); shared `&DiagnosticCollector` across parallel children needs an interior-mutability/Sync statement vs §10.4's non-re-entrant claim | A (sketch) | OPEN-C0 |
| R2-N5 | §33.5 Baselines C/D duplicate two §33.6 ablations; double-counting risk of one experiment as two evidence classes | B | OPEN-C0 (one sentence) |
| R2-N6 | Micro-omissions: /Tabs (PDF/UA-relevant), /NeedsRendering | C | OPEN-C0 (inventory lines) |
| R2-N7 | ALIEN_ARTIFACT.md is Grade-A stale against the re-audit: "spot-checked code held to the same standard," certificates "honestly state where they stop holding," "agent attention does distribute uniformly" — contradicted by F-01/F-02/F-04 two days later; no supersession note. The corpus exhibits the exact truth-drift disease it documents | A | OPEN-C0 (stamp or regenerate) |
| R2-N8 | PROJECT_OVERVIEW nits: filter list omits Crypt (reads exhaustive); pdf.js "coupled to a browser environment" overstates | C | OPEN-C0 |

Round-2 also fully verified the FrankenSim re-audit (F-01 math re-derived correct; Frobenius fallback sound; scoring table consistent with verdict) with two nits: filename drift in its evidence map; half-point score precision that invites over-trust despite the §7.1 disclaimer. Round-2 self-corrections to round 1: "running code" overstated FrankenSim's verified status (no compilation performed — source-confirmed only); the "no incumbent attempts the conjunction" line should have carried §24.14's expiring-observation hedge.

## Round 3 — Campaign layer (first draft) and strategic claims

Campaign-draft bugs, historically labeled **RESOLVED-CHARTER** in v1.0. This successor preserves that history while the changelog identifies any residual defect whose correction exists only in the proposed v1.1 set:

| ID | Finding | Fix in Charter v1.0 |
|---|---|---|
| C-1 | Read-side decryption misplaced in C5; R0 exclusion clause makes credentialed decryption R0-scope; C3 wild-tail gate hits encrypted files | Standard-handler read decryption → C1; public-key → C5; C5 keeps secure output only |
| C-2 | SpecCard pipeline never scheduled despite being the sole legal semantics channel and human-bound | Day-zero track item 5; per-cycle coverage gates; cards run one cycle ahead |
| C-3 | API surfaces unscheduled (CLI/WASM/C-ABI); Observatory playground needs WASM | CLI C1; WASM C4; C-ABI preview C5; freeze post-R4; playground deferred to WASM |
| C-4 | §26 performance program absent from all cycles | D-classes kernel (C1); benchmark tracking C2; hardening slice C6 |
| C-5 | Structured-authoring/layout engine landed nowhere | C6 Track B (UAX #14/#29/#9, tagged generation) |
| C-6 | Corpus sealing and release engineering dropped between messages | Corpus sealed day 0 (pre-implementation); release engineering C4–5 |
| C-7 | Crate atlas wrongly frozen into the kernel; "never re-converted" ambiguous | Kernel freezes layer law + budget rules; atlas stays provisional; kernel beads exactly once (C1) |
| C-8 | Coverage-matrix "built alongside C6" implied retro-tagging | Tagging from C1 (already mandated); C6 builds the scorer only |
| C-9 | Charter-as-precommitment via git alone is weak under §33.4 | Proposed v1.1 residual repair: commitment substrate required; canonical commitment-batch record/root = ledger entry #1, with the Charter digest independently addressable in its manifest |
| C-10 | Evolution Trial silently mutated into "probes" between messages; Flagships G/H unnamed at C7 | Flagship F formal at C4 checkpoint; probes at every close gate; G/H named |
| C-11 | Day-map arithmetic (14 vs 15) | Day 15 |
| C-12 | Baseline cost concentration under-stated; Baseline E omitted from "A–D" | Risk #1 with committed-budget rule; E acknowledged "where feasible" |

Strategic corrections, all **RESOLVED-REASONING**:

| ID | Correction |
|---|---|
| S-1 | "Permanently capped at underdetermined — forever" overclaimed FrankenSim's ceiling. Unrecoverable: construction-era ledger (attempts/search/selection/cost) → foundry/provenance claims stay underdetermined. Recoverable late: artifact-level assurance (sealed bundles, external audits, adversarial hunts per re-audit §11). The moat is provenance-specific. |
| S-2 | 6–18-month and 15-day estimates reconciled: different assumptions (compute, serialization, human latency in/out of critical path) and different endpoints (verdict vs submission). Both stated in Reasoning §7. |
| S-3 | The park-§33 → unpark-§33 reversal across turns, unflagged at the time; synthesized as the graceful-degradation law (G1 never gated on G2/G3 machinery). |
| S-4 | `mb autopsy` was an invented illustrative CLI name (a CLI exists, §25.3); "~85% structured" was rhetoric, not measurement. |

## Standing observations (no fix; carry forward)

1. Three rounds in, findings migrated from the documents (rounds 1–2) to the newest layer (round 3: the campaign draft) — the convergence pattern the methodology predicts. Expect round 4's yield to concentrate on these four artifacts.
2. Zero PDF-normative errors found across three deliberate hunts (inheritance, text state, encryption scoping, filter chaining, blend algebra, CMaps). Under those hunts, the observed defect surface was coordination and evidence plumbing rather than PDF domain content.
3. Two cited Grade-A duplication-drift examples are R1-1 and R2-N7; this is a category-specific illustration, not the ledger's total Grade-A count. The proposed v8 single-normative-home split and blocking drift audits are the selected countermeasures; effectiveness can be evaluated only after the versioned extraction lands and the applicable close gates run.

---

*End of proposed Ledger v1.1. Live gauntlet packets append only to `gauntlet/ROUND_LOG.md`; any change to this historical consolidation requires an authorized successor. Ledger v1.0 remains byte-for-byte unchanged.*
