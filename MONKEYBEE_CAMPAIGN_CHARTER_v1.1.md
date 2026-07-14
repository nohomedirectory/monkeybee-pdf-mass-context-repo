---
generated-by: Codex G6 conditional Charter-set successor owner
date: 2026-07-14
inputs:
  - MONKEYBEE_CAMPAIGN_CHARTER_v1.md
  - CYCLE_0_WORK_ORDER.md
  - AUDIT_FINDINGS_LEDGER.md
  - CAMPAIGN_CHARTER_REASONING.md
  - gauntlet/ROUND_LOG.md (R19, R20)
  - DISPUTES.md
  - MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md §§3, 24.12–24.16, 33, 35
status: PROPOSED
ratification: awaiting human
evidence-status: provisional-pending-substrate
owner-fsm: DRAFT
---

# MonkeyBee Campaign Charter

**Version:** 1.1 (PROPOSED — awaiting human ratification)
**Date:** 2026-07-14
**Source plan:** MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md (v0.7), to be restructured into v8 per the Cycle 0 Work Order
**Companions:** CAMPAIGN_CHARTER_REASONING_v1.1.md (proposed rationale successor), CYCLE_0_WORK_ORDER_v1.1.md (proposed work-order successor), AUDIT_FINDINGS_LEDGER_v1.1.md (proposed bounded status-correction successor; v1.0 remains canonical defect provenance)
**Incorporates:** All round-3 audit corrections C-1 through C-12 and strategic corrections S-1 through S-4 (see ledger)
**Successor relation:** Carries Charter v1.0 forward with only the graded repairs below. It does not supersede v1.0 unless the human ratifies and recommits it under §11.

## v1.1 changelog

| Finding | Exact repair in this successor |
|---|---|
| `R19-A01` | C1 now owns structural signature/ByteRange discovery and its gate evidence; C4 retains structural impact classification; C5 retains cryptographic trust validation. |
| `R19-A02` | C1 now includes the minimum customer-installable CLI release slice and installation admission evidence; C4 retains the broader reproducible-build, packaging, documentation, and supply-chain program. |
| `R19-A03` | A blocking C1 start admission now requires licensed, two-person-reviewed R0 SpecCard coverage; the C1 close-time coverage check remains. |
| `R19-A04` | C0 now points to the row-exhaustive Rev 7 §35 routing in Work Order v1.1 §4 and bars provisional defaults from being treated as ratified choices. |
| `R19-A05` | The day-zero track now commits the Q3 baseline/ablation protocol and freezes the historical baseline vintage, while C4 retains contemporaneous execution. |
| `R19-A06` | The day-zero track now assigns discovery execution, candidate characterization, nomination/challenge handling, deviations, and the discovery-report producer before field freeze. |
| `R19-A07` | C7 now states the irreversible report-freeze -> evaluation-commitment -> measurement order and preserves a later-addendum branch when windows remain open at the dated package boundary. |
| `R19-B01` | No repair is admitted in this draft. The C6/S6 language is carried forward pending R20–R22 and human evidence; both premises recorded in `ledger/owners/G6_STATE.md` remain live. |
| `R20-A01` | The day-zero G2/G3 track now produces a separately committed §33.4 `EvaluationProtocolId`, names its commitment custodian and contents, and makes it an admission edge into C4 without merging it with field discovery. |
| `R20-A02` | Section 7 now gives each Q3 evidence row its normative object/home, separates artifact-necessary evidence from foundry-supporting evidence, and adds operational closure and exact boundary without deleting the baseline program. |
| `R20-A03` | The historical baseline freeze now binds the day-zero task plus model/harness/tool vintage manifest; C4 retains the contemporaneous run. |
| `R20-A04` | C4 and C7 now carry the universal close gate and emit sealed trial records #4 and #7; the foundry distribution consistently consumes #1–#7. |
| `R20-A05` | The discovery nomination/challenge window is now distinct from any later claim-challenge window, and the former closes before discovery-report freeze. |
| `R20-A06` | Independent human scouts now appear in both the discovery commitment and independence layer, with an explicit downgrade to `named_set_lead` if that role is unavailable. |
| `R20-A07` | The retrospective rule now cites §33.1, while a separate §33.3 producer declares the artifact/operational boundary at C0 and every claim envelope. |
| `R20-A08` | The immutable claim-scope and three-stage commitment law from §§24.12/24.16 now joins the kernel; dated observations and lane parameters remain refreshable shell material. |
| `R20-B02` (grade B; premise-supported, not promoted) | Q2 now uses the strongest earned admitted scope, defines clause-completion comparison separately from S1–S6, and makes the S1–S6/Flagship G/H trace edges explicit without awarding a scope in advance. |

---

## 0. What this document is, and is not

This Charter is the campaign-level staging document for MonkeyBee: it defines how many plan→beads→swarm cycles the project runs, what each cycle claims, what evidence each cycle must emit, and how the campaign ends with the Q2 and Q3 questions answered by independent adjudication rather than self-award.

**Division of labor with the plan-space law.** Revision 7 forbids execution packaging (issue IDs, work inventories, agent assignments) inside the plan. This Charter deliberately owns *claim staging and cycle sequencing* — the same class of content as Rev 7's §3.0 release envelopes — so that the Constitution and the per-cycle delta plans can remain execution-free. The Charter still contains **no bead identifiers, no agent counts, no work assignments, and no implementation ordering below cycle granularity.** Beads exist only downstream of each cycle's delta plan.

**Two questions this campaign exists to answer, by its end:**

- **Q3:** Does MonkeyBee earn `Artifact-alien candidate` (Rev 7 §33.15 ladder) under a bounded, authenticated production ledger — a determinate verdict where FrankenSim's construction-era claims are capped at underdetermined?
- **Q2:** Does MonkeyBee earn an uncertainty-aware `leading` outcome for a predeclared PDF-completion `FieldDefinitionId` under the strongest admitted scope actually earned (`named_set_lead`, `registered_open_field_lead`, or `observed_field_lead`), plus separately reported S1–S6 lane results, against the frozen comparator field?

**One goal this campaign must never sacrifice to those questions:**

- **G1 (survival wedge):** a sellable secure-ingestion product (Rev 7 §3.0: "the first commercial/product wedge is secure document ingestion and evidence-rich transformation") live at the end of Cycle 1 and improving every cycle thereafter, gated on **zero** §33 machinery.

---

## 1. Document architecture

Rev 7 splits at Cycle 0 into three artifact classes. This split is what makes every later cycle cheap: no cycle's plan or beads graph ever holds the whole project in context.

| Artifact | Contents | Lifecycle |
|---|---|---|
| **Constitution** (v8 kernel) | Identity grammars (§9), evidence algebra and outcome model (§10), work-context/budget/capability law (§11), clean-room protocol (§4), **layer law and crate-boundary budget rules** (§8, §30.1.1 — *not* the concrete crate atlas, which stays provisional per §30), canonical hashing grammars, non-negotiable principles (§6), the §33 evaluation protocol, and the immutable claim-scope/three-stage commitment law from §§24.12 and 24.16 under one normative home with §10.3/§33 | Frozen after C0. Converted to beads **exactly once**, in Cycle 1, never again. Kernel changes thereafter require a version bump, migration plan, and claim-lapse review — the campaign's design target is **zero kernel-touch from Cycle 2 onward**. |
| **Charter** (this document) | Cycle map, goals, day-zero track, evidence threading, risks, degradation law | Committed through the tamper-evident substrate at day 0 (§10 below). Amendable only via the change-control rule (§11 below). |
| **Delta plans** (one per cycle, C1–C7) | ~2,000–4,000 lines each; the new surface for that cycle only, written **against repo reality** (archaeology first), consequence contracts for new capabilities, kernel-touch declaration, cycle gates | Authored at each cycle boundary; converted to beads for the **delta only**; superseded by the next cycle's archaeology. |

Rev 7 shell content not in the kernel (domain sections §12–§28 except the extracted §§24.12/24.16 law, workflows, bets, flagships) remains the reference corpus that delta plans draw from and refine against the real codebase. The dated §24.13 register and §24.15 lane parameters stay refreshable; any overlap with the kernel law is a citation or `generated-echo`, not a second normative home.

---

## 2. Campaign goals and the graceful-degradation law

**G1 — Survival wedge (unconditional).** R0 secure ingestion/inspection sellable after Cycle 1; content-disarm-and-reconstruction complete after Cycle 5. G1 depends on zero stewards, zero windows, zero baselines.

**G2 — Q3 verdict (conditional on independence layer).** Artifact-alien candidate package submitted at the Cycle 4 checkpoint; verdict awarded externally on the reviewers' calendar, never self-awarded.

**G3 — Q2 verdict (conditional on G2 machinery + R4).** The PDF-completion comparison and separately reported S1–S6 lanes execute only after the committed discovery protocol has been run, the applicable discovery nomination/challenge window has closed, its `CompetitorDiscoveryReportId` has frozen the field, and the bound evaluation protocol has then been committed. The outcome uses only the strongest admitted scope the evidence earns. If those prerequisites remain open at the dated C7 package boundary, that package stays within its supported scope and the field measurement waits for a later addendum.

**The graceful-degradation law.** If resources, humans, or priorities collapse at any point: drop the Cycle 4 checkpoint and Cycle 7, keep everything else. The campaign then terminates as G1 — a shipped, evidenced, sellable product line — with no stranded work, because no G1 deliverable is ever gated on G2/G3 machinery. This law is a design constraint on every delta plan: **evidence apparatus may consume cycle capacity; it may never sit on the wedge's critical path.**

---

## 3. The day-zero parallel track

Everything below starts at day 0, runs concurrently with all cycles, and is **human- or calendar-bound — the only things compute cannot compress.** Each item is a first-class entry in the Cycle 0 beads graph with dependency edges into the release gates it protects, so `br ready` surfaces them immediately and the swarm cannot ship past them.

1. **Production ledger opens** before any implementation agent runs: models, harness versions, attempts, failed branches, discarded candidates, cost, human hours, selection decisions. Retrospective entries are labeled `retrospective` and never support prospective claims (Rev 7 §33.1).
2. **Tamper-evident commitment substrate established** — independent steward custody or witnessed append-only log (Rev 7 §33.4). A bare git timestamp is insufficient. **This Charter is itself the first committed artifact.**
3. **Discovery protocol committed and then executed:** comparator-field discovery method, inclusion criteria, named independent human scouts, and **discovery nomination/challenge-window durations predeclared now** — that window opens immediately and runs concurrent with the build, so no one can later claim it was rigged short. The scouts execute the frozen protocol: record search surfaces and deviations, characterize candidates, process nominations and challenges, preserve unresolved eligibility, close that window, and only then produce the committed `CompetitorDiscoveryReportId` before any field-specific evaluation protocol is designed. Any post-publication claim-challenge window is a separate lifecycle object and cannot substitute for or shorten the discovery window.
4. **Independence layer engaged:** stewards (corpus custody, commitment custody), independent human discovery scouts named in the pre-search commitment, red team (different model family + humans; runs continuously, not inside Cycle 4), external reviewers/adjudicators identified. **What cannot be obtained is logged honestly**, and every claim that needed it degrades rather than silently proceeding. In particular, absent independent scouts or incomplete discovery caps the field outcome at `named_set_lead`; scouting is not silently reassigned to the implementation ecology.
5. **SpecCard pipeline stood up** (critical path for every cycle): ISO 32000-2 + errata license acquired under ISO's current AI-use terms; extraction protocol; **two-person meaning review** staffing; card coverage registry. Card coverage for each cycle's surface is a gate on that cycle's swarm start.
6. **Corpus program:** wild-tail acquisition (public corpora + crawl per Rev 7 §28), stratification, and **steward-sealed held-out splits created before any implementation exists** — after code exists, nothing new can become held-out.
7. **License and disclosure decisions:** project license chosen (Rev 7 §35 default: permissive); vulnerability-disclosure/security-response policy drafted (intake channel, triage, embargo, advisory format) — required before the wedge has customers.
8. **Clause-tagging discipline declared:** from Cycle 1, every consequence contract cites its SpecCardIds (already mandated by Rev 7); the Cycle 6 coverage scorer only *reads* this tagging — it never retro-tags.
9. **Q3 `EvaluationProtocolId` committed:** before candidate generation or result inspection, the commitment custodian independently time-commits the §33.4 protocol for the Q3 object and exact reference class. It binds the supported profiles and security envelope; metrics, determinism, workloads, flagships, failure conditions, and expiry; baseline/ablation tasks and strongest ordinary replacements; model substitutions; resource and human-attention budgets; held-out/query/reveal boundaries; evaluator lineage; novelty/leakage analyses; and the rule that one experiment cannot count as both a baseline and an ablation. Its historical baseline vintage binds the day-zero task statement and model/harness/tool manifest; the contemporaneous runs remain at C4 and Baseline E remains where feasible. This G2/G3 commitment is separate from the pre-search discovery commitment and never gates the G1 wedge.
10. **Artifact and operational boundary declared:** C0 classifies runtime code, generic dependencies, construction-time agents/processors, runtime adapters/models/services, validators, corpora, human procedures, and external infrastructure under §33.3. Every public claim envelope re-declares the exact minimum operational closure; the C4 package binds the R2 boundary rather than counting runtime substrate as self-contained capability.

---

## 4. The cycle map

| Cycle | Days | Layers | Envelope | Headline | Q2/Q3 evidence emitted |
|---|---|---|---|---|---|
| **C0** | 0–1 | — | — | Charter, v8 restructure, C1 delta plan + beads | Charter + separate protocol commitments; initial operational boundary; ledger opens |
| **C1** | 1–3 | L0–L2 | **R0 ships** | Kernel, immune system, autopsy wedge, read decryption, structural signature discovery, CLI, minimum installable release | Cycle trial record #1; fuzz baseline; drift audit #1; installability evidence |
| **C2** | 3–5 | L3 + raster | — | Render engine minus real text | Trial #2; benchmark tracking begins; D2 determinism receipts |
| **C3** | 5–7 | L4 | **R1 ships** | Text stack, ICC, divergence harness, Observatory records | Trial #3; wild-tail gate results; divergence corpus |
| **C4** | 7–9 | L5–L6 (partial) | **R2 ships** | Writer, WASM, expanded release engineering — **Q3 checkpoint** | Trial #4; **Q3 package submitted day 9**: committed baselines and ablations, red-team results, Evolution Trial, exact R2 boundary, ledger-to-date |
| **C5** | 9–11 | L5–L7 | **R3 ships** | Transforms, redaction, signature validation, secure output, agent surface, C ABI preview | Trial #5; Flagship D results; CDR product complete |
| **C6** | 11–13 | L4–L7 | **R4 ships** | Fidelity track + authoring track + perf hardening + coverage scorer | Trial #6; coverage matrix runnable; perf lanes green |
| **C7** | 13–15 | — | — | Ordered field freeze -> evaluation commitment -> measurement, when the predeclared windows have closed | Trial #7; Q2 field package only after the ordered commitments; otherwise a scope-limited dated package and later addendum |

Timeline is the aggressive case; §9 states the tempo-independence rule. Q3/Q2 *verdicts* land on external calendars after submission — by design.

---

## 5. Cycle specifications

### C0 — Charter and restructure (plan-space only; no implementation swarm)

Scope: execute the Cycle 0 Work Order in full — kernel extraction into the Constitution; apply the Rev 7 fixes from the Audit Findings Ledger (Appendix B regeneration against §10.6, R0/R2 signature-envelope fix, §22.4 scope-totality condition, hasher law, symmetry budget row, disclosure-policy section, enumeration gaps); add the §34.9 addendum protocol; resolve every C0 row and assign every remaining Rev 7 §35 row to an owner cycle and a must-resolve-before boundary through Work Order v1.1 §4, without treating a default as ratified; author the C1 delta plan; convert C1 delta + day-zero track to beads; run bead polish to steady state.
Gate: Charter committed through the substrate; C1 beads pass `br dep cycles` clean; SpecCard coverage plan for the R0 surface exists. That plan does not satisfy the separate C1 start admission below.

### C1 — Kernel + immune system + R0 wedge

Start admission (blocking): licensed-source R0 SpecCards cover the C1 surface, two independent meaning reviewers have accepted them, and every C1 consequence contract cites the accepted card IDs. A coverage plan, registry slot, or `PENDING-LICENSED-SOURCE` placeholder does not admit the swarm.

Scope: L0–L2. Byte sources and snapshots; file lexer; COS objects; xref tables and streams; revision discovery; object streams; common filters (Flate + predictors, ASCIIHex, ASCII85, RunLength, LZW); recovery-as-bounded-hypothesis-search v1; encryption **inventory plus standard-handler read decryption with caller-supplied credentials** (RC4, AESV2, AESV3, version-specific password preparation) — read decryption is R0-scope per the R0 exclusion clause and is needed before the C3 wild-tail gate; **structural signature and ByteRange discovery**, inventory only at this envelope, with impact classification deferred to C4 and cryptographic trust validation deferred to C5; the complete identity/evidence/report/checker stack; **the immune system: generated report schemas, claim registry generated from consequence contracts, contract-truth checks (API existence, dependency agreement, claim-registry linkage — never heading checks), drift auditor as a repository gate**; coverage-guided fuzzing from hour one; **CLI surface** (§25.3) so the wedge is invocable; a **minimum customer-installable release slice** for that CLI with a declared supported install path, installation/use instructions, and installation smoke evidence; clause-tagging live from the first contract.
Explicitly excluded: rendering, fonts, public-key handlers, any writer.
Gate: Workflow B end-to-end on hostile files (complete OpenReport with recovery alternatives and security inventory, including structural signature/ByteRange inventory); zero reachable panics under the fuzz corpus; G0–G3-subset lanes green; the declared supported install path exercises the packaged CLI and emits its report; SpecCard coverage for the R0 surface remains valid at close; cycle-close drift audit + held-out probe + sealed trial record.
Deliverable: **the sellable inspection wedge.**

### C2 — Render engine minus real text

Scope: content-stream lexer; page-program VM and graphics state; paths, clipping, winding rules; transforms; baseline images (DCT/JPEG, Flate-backed) in device color spaces; the rasterizer; RenderReports with D2 same-build pixel determinism; transparency subset per R1's declared profile. Text shows as explicit substitution-or-refusal receipts under the page-local refusal law — honest, not embarrassing. **Benchmark tracking begins here** and runs every cycle so performance regressions surface continuously instead of at C7 measurement.
Gate: G2 render lanes on the non-text corpus slice; D2 receipts reproducible; drift audit + probe + trial record.

### C3 — Text stack + color, R1 ships

Scope: L4. Font parsing (TrueType, CFF, Type1, CID/Type0, Type3); CMaps; budgeted glyph execution behind the FontExecutionService protocol; text extraction (Workflow C); ToUnicode and text-semantics claims; the ICC color pipeline proper; the external-processor divergence harness (PDFium, MuPDF, Poppler, pdf.js) and **Observatory seed as records + minimized witnesses only** — the browser playground waits for the WASM surface (C4+), per Bet 21's own architecture.
Gate: **strict-open + render over the steward-sealed wild-tail corpus, including credentialed encrypted documents** (decryption landed in C1); divergence reports generated and classified; R1 claim envelope published with page-local refusal accounting; drift audit + probe + trial record.

### C4 — Writer, R2 ships — the Q3 checkpoint

Scope: draft roots and the builder API; canonical and preservation serializers; incremental updates; font subsetting and embedding; **signature-impact classification** over C1 structural discoveries (ByteRange, DocMDP/FieldMDP/lock classification; cryptographic trust validation stays in C5); external-reader matrix; round-trip metamorphic gauntlet; **WASM surface lands** (enables the Observatory playground); **release engineering expands** beyond C1's minimum installable slice into reproducible builds, broader packaging and documentation, and G6.1 supply-chain lanes.
Q3 checkpoint admission: the day-zero Q3 `EvaluationProtocolId` and historical-vintage manifest must already be committed before any Q3 candidate evaluation, baseline run, or ablation run begins. If that commitment is absent, C4's G1 writer and release work may continue, but the Q3 checkpoint is removed rather than run retrospectively.
Then the checkpoint — build pauses, evidence assembles under the day-zero `EvaluationProtocolId`: historical and contemporaneous equal-resource **Baselines A–D** (plus E, expert comparison, where feasible), mechanism **ablations** kept evidentially distinct from baselines, red-team results from the window that has been running since day 0, the **Evolution Trial (Flagship F)** run formally against the R2 artifact as the addendum-safety rehearsal, the exact §33.3 R2 artifact/operational boundary, and the ledger to date.
Gate: the universal close suite passes — drift audit, held-out probe, SpecCard coverage check, and sealed cycle trial record #4 — then the **Q3 package is submitted to independent review on ~day 9.** The verdict pends on the reviewers' calendar; the campaign continues without waiting.

### C5 — Transforms + security, R3 ships

Scope: decryption matrix completion (public-key security handlers); canonical rewrite with carry/drop maps; sanitization; **redaction with the inference-resistance battery and Flagship D** (independent, lineage-diverse forensic tools); layered **cryptographic** signature validation (CMS, DSS/VRI, timestamps); secure-output profile (D1R re-encryption, nonce law); semantic diff; EditSession/agent surface with idempotency and stale-state protection; **C ABI preview** (Workflow M: before the advanced envelope).
Gate: R3 lanes green; Flagship D passes with disclosed tool lineage; secure-output D1R receipts verified; drift audit + probe + trial record.
Deliverable: **the complete content-disarm-and-reconstruction product.**

### C6 — Advanced fidelity + authoring, R4 ships (two tracks)

**Track A — fidelity:** JPX, JBIG2, CCITT completion; Separation/DeviceN and rendering intents; full transparency (isolation, knockout, all blend modes); shading types 4–7; tagged-PDF structure semantics; AcroForm model and appearance generation; PDF/A and PDF/UA validation families; portfolios and the preserve-and-inventory tail.
**Track B — authoring:** the structured-authoring layout engine — UAX #14 line breaking, UAX #29 segmentation, UAX #9 bidi, shaping ownership per Bet 17; tagged-output authoring so PDF/UA-conformant *generation* exists, not just validation.
**Plus:** the dedicated **performance-hardening slice** (parallel page rendering, arena/SoA layouts, D2 determinism preserved under optimization — the S6/S1 prerequisite); the **coverage-matrix scorer** built over the clause tagging that has existed since C1.
Gate: R4 lanes; PDF/A + PDF/UA validation profiles operational; coverage matrix runnable end-to-end; perf lanes meet predeclared targets; drift audit + probe + trial record.

### C7 — Measurement and the verdict package

Scope follows one irreversible order. First, after the applicable predeclared discovery nomination/challenge window closes, the scouts finish candidate characterization, record deviations and unresolved eligibility, dispose of nominations/challenges, and commit the `CompetitorDiscoveryReportId` that freezes the comparator field. Second, without inspecting comparison results, commit an `EvaluationProtocolCommitment` bound to that exact report, including configurations, budgets, corpus, metrics, statistics, stopping, adjudication, and lifecycle. Third, and only then, run the PDF-clause-completion comparison under its exact `FieldDefinitionId` and earned admitted scope; run the separately reported S1–S6 lanes; execute Flagship H as the S2 wild-tail campaign; and execute Flagship G only under its separately admitted optional legacy-execution envelope, never as a substitute for completion or S1–S6. The universal close suite then seals cycle trial record #7; compile the foundry distribution from records #1–#7 (attempts, medians, failures — the loop itself is the foundry evidence), assemble the §33.16 evaluation bundle, and begin independent adjudication.

Conditional timing: if every applicable window has closed by the aggressive C7 boundary, the ordered sequence may run in C7. If a ratified window remains open at the dated package boundary, the dated package reports only evidence and claim scope then supported, at most `named_set_lead` for an incompletely frozen field; it records the field result as pending and schedules a later addendum that repeats the report-freeze -> evaluation-commitment -> measurement order. It does not inspect early measurements or upgrade the earlier package retroactively.

Gate: after the three ordered stages, the universal close suite passes — drift audit, held-out probe, SpecCard coverage check, and sealed cycle trial record #7 — before the Q2 field package is submitted. A scope-limited dated package may still be assembled around day 15; verdicts arrive on the independent reviewers' calendar.

---

## 6. The per-cycle protocol (summary; full text in the Work Order as Rev 7 §34.9)

Every cycle C1–C7 runs the same loop:

1. **Archaeology first.** The delta plan is written against repository reality — grep, tests, contracts — never against the previous plan's description of the code.
2. **Kernel-touch declaration.** Target `none` from C2 onward; any touch triggers version bump + migration + claim-lapse review.
3. **Consequence contracts → bead families.** One ConsequenceContractId per capability; falsifiers become acceptance criteria; the assigned Gauntlet tier is the definition of done; SpecCardIds cited on every contract.
4. **Beads for the delta only.** Never a full reconversion — full reconversion is the proven feature-loss and drift vector. Polish to steady state; `br dep cycles` clean.
5. **Swarm.**
6. **Cycle-close gate (mandatory, blocking):** drift audit (generated-truth diffs, contract-truth checks, claim-registry consistency) + one held-out extension probe + SpecCard coverage check + sealed cycle trial record into the ledger (attempts, failures, cost, outcomes).

No cycle's delta plan may be authored before the previous cycle's close gate passes.

---

## 7. Evidence threading: how the cycles compose into Q3 and Q2

| Q3 evidence component | Object and normative home | Where it comes from |
|---|---|---|
| Functioning integrated consequence | Artifact; §33.15 candidate rung and §33.18 item 1 | C1–C4 artifact + wild-tail gate + external-reader matrix |
| Assurance and grounding that survive attack | Artifact assurance; §§33.10 and 33.18 item 1 | Continuous red team; independent falsifiers; Flagship D lineage diversity; seeded-defect trials |
| Operational closure and exact boundary | Artifact; §§33.3 and 33.18 item 1 | C0 boundary declaration, per-envelope re-declaration, exact R2 boundary in the C4 package |
| Prospective, bounded, authenticated provenance | Artifact comparison support and foundry provenance; §§33.1, 33.4, and 33.18 | Ledger from day 0; Q3 `EvaluationProtocolId`; sealed cycle trial records; commitment substrate |
| Zero Grade-A truth drift | Supporting artifact assurance gate; §34.9, not a separate §33.15 rung | Immune system from C1; per-cycle drift audits |
| Provenance-conditioned production comparison | Artifact comparison context under §33.18 item 1; foundry evidence under §§33.5–33.8 | Historical and contemporaneous Baselines A–D(/E), ablations kept distinct, substitutions, and full attempt distribution |
| Independent adjudication | Candidate-award procedure; §33.15 | Day-zero engagement; self-award prohibited; honest degradation logging |

Foundry evidence cannot be borrowed to satisfy a missing artifact property, and failure of the foundry comparison does not logically bar the artifact candidate rung (§§33.17–33.18). It remains a separately reported, budget-protected evidence program because it supplies the production comparison and any foundry claim; a cut is a formal downgrade, never a silent omission.

| Q2 requirement | Where it comes from |
|---|---|
| The measurement instrument | Clause tagging from C1; scorer at C6 |
| The surface to measure | R0–R4 across C1–C6, including the authoring track |
| The field | Day-zero pre-search commitment; ongoing scout execution; closed challenge window; committed `CompetitorDiscoveryReportId` before evaluation design |
| The claim scope | Strongest actually earned among `named_set_lead`, `registered_open_field_lead`, and `observed_field_lead`; no scope is pre-awarded |
| The completion comparison | Distinct PDF-clause-completion `FieldDefinitionId`; licensed-card clause denominator, field eligibility, analysis unit, adjudication, Goodhart guard, and fallback fixed in the post-report evaluation commitment |
| The comparison | Post-report evaluation commitment, then C7 or later-addendum completion matrix and separately reported lanes under that committed protocol |
| The credibility | Everything in the Q3 column, already in motion |

| Q2 lane / campaign | Producing cycles and measurement edge |
|---|---|
| Completion comparison (distinct from S1–S6) | Clause tagging C1–C6; scorer C6; frozen-field measurement C7 or later addendum |
| S1 rendering | Render surface C2–C3; fidelity expansion C6; field measurement C7 or later addendum |
| S2 wild-tail | Stewarded gates from C3; Flagship H measurement C7 or later addendum |
| S3 structured extraction | Evidence/source stack C1 and text/structure surface C3–C6; field measurement C7 or later addendum |
| S4 generation | Writer C4 and profile/authoring surface C6; field measurement C7 or later addendum |
| S5 atomic conjunction family | Producing capabilities C1–C6; each atomic record measured separately at C7 or later addendum |
| S6 performance | Tracking from C2 and hardening C6; field measurement only after its valid post-report commitment |
| Flagship G | Optional legacy-execution campaign under its own admitted envelope; never completion or S1–S6 evidence by substitution |

**The reframe that governs the whole campaign:** each cycle, closed properly, *is* one foundry trial and one lineage data point. The loop is not overhead on the way to the verdicts — it is the evidence generator. FrankenSim ran the same loop uninstrumented and received zero evidentiary credit for it.

---

## 8. Campaign risks, ordered by lethality

1. **Baseline cost concentration.** Baselines A–D mean funding multiple full vanilla-agent rebuild attempts at equal budget — the most expensive, least fun, most skippable item. Without them there is no foundry production-disproportion evidence and the artifact's provenance-conditioned production comparison is weaker; §33.17 still permits the artifact candidate rung if its own properties and independent judgment hold. Mitigation: the task and model/harness/tool historical vintage, baseline/ablation design, fairness controls, evaluator lineage, and budget are committed at day 0; a cut is a formal downgrade of G2's evidence package, never a quiet omission.
2. **SpecCard human latency.** Two-person meaning review is the slowest step in a compute-unlimited campaign and gates every cycle's swarm. Mitigation: pipeline stands up day 0; card production runs one cycle ahead of implementation.
3. **Independence layer non-materialization.** Mitigation: the graceful-degradation law; honest logging; claims cap at self-attested tiers rather than pretending.
4. **Drift at swarm tempo.** Two Grade-A drifts occurred in this ecology at documentation stage, before any code. Mitigation: the immune system ships in C1 before growth; cycle-close gates are blocking.
5. **Kernel-touch addendum.** A C3+ discovery that forces an identity-grammar change invalidates receipts. Mitigation: C4's Evolution Trial rehearses extension safety; kernel-touch protocol makes the cost explicit instead of silent.
6. **Verdict latency.** External reviewers' calendars bound Q3/Q2 answers. Mitigation: none, by design — the verdicts' value comes precisely from not controlling them.
7. **Own-goal falsifier failure (the F-01 pattern).** The whole ecology can agree on a wrong certificate. Mitigation: red team from a different model family; seeded-defect detection-rate trials; external oracles the generator cannot redefine.

---

## 9. Timeline and tempo independence

Day map (aggressive case): C0 days 0–1; C1 1–3; C2 3–5; C3 5–7; C4 7–9 (**Q3 package day 9**); C5 9–11; C6 11–13; C7 13–15 (**scope-limited dated package around day 15**). A Q2 field package is campaign-controlled only after the applicable windows close and the report-freeze -> evaluation-commitment -> measurement sequence runs; it may therefore be a later addendum. Verdict dates are not campaign-controlled.

**Tempo independence:** the structure is identical whether the campaign takes two weeks or six — same seven delta plans, same gates, same evidence thread. Cycle duration is set by observed telemetry (beads-per-cycle the polish rounds can hold, drift-audit findings per boundary), not by the calendar.

**Compressed 5-cycle variant** (merge C2+C3 into one rendering cycle; C5+C6 into one transforms-plus-fidelity cycle): permitted only if C1 telemetry shows the polish rounds holding the larger graphs at steady state and the C1 drift audit is clean. Default is the 7-cycle spacing.

---

## 10. Commitment mechanics for this Charter

This Charter becomes evidence only when committed through the tamper-evident substrate (independent steward custody or witnessed append-only log) alongside the separate discovery commitment, Q3 `EvaluationProtocolId`, historical-vintage manifest, and initial artifact/operational-boundary declaration — a git commit alone is decoration. The committed Charter hash is the campaign's first ledger entry. Amendments follow §11 and are committed the same way; the diff history of the Charter is itself part of the lineage evidence.

## 11. Change control

Charter amendments require: a written rationale entry in the ledger; classification as `scope`, `sequence`, `gate`, or `goal` change; and re-commitment through the substrate. A `goal` change (touching G1/G2/G3 or the degradation law) additionally requires an explicit note in every subsequently published claim that the campaign's goals changed mid-course, with the date. Silent goal drift is the failure mode this clause exists to prevent.

---

*End of proposed Charter v1.1. If ratified, first action: execute CYCLE_0_WORK_ORDER_v1.1.md.*
