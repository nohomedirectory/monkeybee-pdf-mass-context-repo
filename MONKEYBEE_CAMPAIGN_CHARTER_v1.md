# MonkeyBee Campaign Charter

**Version:** 1.0 (draft pending commitment)
**Date:** 2026-07-14
**Source plan:** MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md (v0.7), to be restructured into v8 per the Cycle 0 Work Order
**Companions:** CAMPAIGN_CHARTER_REASONING.md (rationale), CYCLE_0_WORK_ORDER.md (first executable step), AUDIT_FINDINGS_LEDGER.md (defect provenance)
**Incorporates:** All round-3 audit corrections C-1 through C-12 and strategic corrections S-1 through S-4 (see ledger)

---

## 0. What this document is, and is not

This Charter is the campaign-level staging document for MonkeyBee: it defines how many plan→beads→swarm cycles the project runs, what each cycle claims, what evidence each cycle must emit, and how the campaign ends with the Q2 and Q3 questions answered by independent adjudication rather than self-award.

**Division of labor with the plan-space law.** Revision 7 forbids execution packaging (issue IDs, work inventories, agent assignments) inside the plan. This Charter deliberately owns *claim staging and cycle sequencing* — the same class of content as Rev 7's §3.0 release envelopes — so that the Constitution and the per-cycle delta plans can remain execution-free. The Charter still contains **no bead identifiers, no agent counts, no work assignments, and no implementation ordering below cycle granularity.** Beads exist only downstream of each cycle's delta plan.

**Two questions this campaign exists to answer, by its end:**

- **Q3:** Does MonkeyBee earn `Artifact-alien candidate` (Rev 7 §33.15 ladder) under a bounded, authenticated production ledger — a determinate verdict where FrankenSim's construction-era claims are capped at underdetermined?
- **Q2:** Does MonkeyBee earn an uncertainty-aware `leading` outcome on a predeclared, full-field PDF-completion `FieldDefinitionId`, plus supremacy-lane results, against the frozen comparator field?

**One goal this campaign must never sacrifice to those questions:**

- **G1 (survival wedge):** a sellable secure-ingestion product (Rev 7 §3.0: "the first commercial/product wedge is secure document ingestion and evidence-rich transformation") live at the end of Cycle 1 and improving every cycle thereafter, gated on **zero** §33 machinery.

---

## 1. Document architecture

Rev 7 splits at Cycle 0 into three artifact classes. This split is what makes every later cycle cheap: no cycle's plan or beads graph ever holds the whole project in context.

| Artifact | Contents | Lifecycle |
|---|---|---|
| **Constitution** (v8 kernel) | Identity grammars (§9), evidence algebra and outcome model (§10), work-context/budget/capability law (§11), clean-room protocol (§4), **layer law and crate-boundary budget rules** (§8, §30.1.1 — *not* the concrete crate atlas, which stays provisional per §30), canonical hashing grammars, non-negotiable principles (§6), the §33 evaluation protocol | Frozen after C0. Converted to beads **exactly once**, in Cycle 1, never again. Kernel changes thereafter require a version bump, migration plan, and claim-lapse review — the campaign's design target is **zero kernel-touch from Cycle 2 onward**. |
| **Charter** (this document) | Cycle map, goals, day-zero track, evidence threading, risks, degradation law | Committed through the tamper-evident substrate at day 0 (§10 below). Amendable only via the change-control rule (§11 below). |
| **Delta plans** (one per cycle, C1–C7) | ~2,000–4,000 lines each; the new surface for that cycle only, written **against repo reality** (archaeology first), consequence contracts for new capabilities, kernel-touch declaration, cycle gates | Authored at each cycle boundary; converted to beads for the **delta only**; superseded by the next cycle's archaeology. |

Rev 7 shell content not in the kernel (domain sections §12–§28, workflows, bets, flagships) remains the reference corpus that delta plans draw from and refine against the real codebase.

---

## 2. Campaign goals and the graceful-degradation law

**G1 — Survival wedge (unconditional).** R0 secure ingestion/inspection sellable after Cycle 1; content-disarm-and-reconstruction complete after Cycle 5. G1 depends on zero stewards, zero windows, zero baselines.

**G2 — Q3 verdict (conditional on independence layer).** Artifact-alien candidate package submitted at the Cycle 4 checkpoint; verdict awarded externally on the reviewers' calendar, never self-awarded.

**G3 — Q2 verdict (conditional on G2 machinery + R4).** Completion measurement and supremacy lanes (Flagships G/H) executed at Cycle 7 against the field frozen by the day-zero discovery commitments.

**The graceful-degradation law.** If resources, humans, or priorities collapse at any point: drop the Cycle 4 checkpoint and Cycle 7, keep everything else. The campaign then terminates as G1 — a shipped, evidenced, sellable product line — with no stranded work, because no G1 deliverable is ever gated on G2/G3 machinery. This law is a design constraint on every delta plan: **evidence apparatus may consume cycle capacity; it may never sit on the wedge's critical path.**

---

## 3. The day-zero parallel track

Everything below starts at day 0, runs concurrently with all cycles, and is **human- or calendar-bound — the only things compute cannot compress.** Each item is a first-class entry in the Cycle 0 beads graph with dependency edges into the release gates it protects, so `br ready` surfaces them immediately and the swarm cannot ship past them.

1. **Production ledger opens** before any implementation agent runs: models, harness versions, attempts, failed branches, discarded candidates, cost, human hours, selection decisions. Retrospective entries are labeled `retrospective` and never support prospective claims (Rev 7 §33.3).
2. **Tamper-evident commitment substrate established** — independent steward custody or witnessed append-only log (Rev 7 §33.4). A bare git timestamp is insufficient. **This Charter is itself the first committed artifact.**
3. **Discovery protocols committed:** comparator-field discovery method, inclusion criteria, and **challenge-window durations predeclared now** — windows open immediately and run concurrent with the build, so no one can later claim they were rigged short.
4. **Independence layer engaged:** stewards (corpus custody, commitment custody), red team (different model family + humans; runs continuously, not inside Cycle 4), external reviewers/adjudicators identified. **What cannot be obtained is logged honestly**, and every claim that needed it degrades to its self-attested tier rather than silently proceeding.
5. **SpecCard pipeline stood up** (critical path for every cycle): ISO 32000-2 + errata license acquired under ISO's current AI-use terms; extraction protocol; **two-person meaning review** staffing; card coverage registry. Card coverage for each cycle's surface is a gate on that cycle's swarm start.
6. **Corpus program:** wild-tail acquisition (public corpora + crawl per Rev 7 §28), stratification, and **steward-sealed held-out splits created before any implementation exists** — after code exists, nothing new can become held-out.
7. **License and disclosure decisions:** project license chosen (Rev 7 §35 default: permissive); vulnerability-disclosure/security-response policy drafted (intake channel, triage, embargo, advisory format) — required before the wedge has customers.
8. **Clause-tagging discipline declared:** from Cycle 1, every consequence contract cites its SpecCardIds (already mandated by Rev 7); the Cycle 6 coverage scorer only *reads* this tagging — it never retro-tags.

---

## 4. The cycle map

| Cycle | Days | Layers | Envelope | Headline | Q2/Q3 evidence emitted |
|---|---|---|---|---|---|
| **C0** | 0–1 | — | — | Charter, v8 restructure, C1 delta plan + beads | Charter + protocol commitments; ledger opens |
| **C1** | 1–3 | L0–L2 | **R0 ships** | Kernel, immune system, autopsy wedge, read decryption, CLI | Cycle trial record #1; fuzz baseline; drift audit #1 |
| **C2** | 3–5 | L3 + raster | — | Render engine minus real text | Trial #2; benchmark tracking begins; D2 determinism receipts |
| **C3** | 5–7 | L4 | **R1 ships** | Text stack, ICC, divergence harness, Observatory records | Trial #3; wild-tail gate results; divergence corpus |
| **C4** | 7–9 | L5–L6 (partial) | **R2 ships** | Writer, WASM, release engineering — **Q3 checkpoint** | **Q3 package submitted day 9**: baselines, ablations, red-team results, Evolution Trial, ledger-to-date |
| **C5** | 9–11 | L5–L7 | **R3 ships** | Transforms, redaction, signature validation, secure output, agent surface, C ABI preview | Trial #5; Flagship D results; CDR product complete |
| **C6** | 11–13 | L4–L7 | **R4 ships** | Fidelity track + authoring track + perf hardening + coverage scorer | Trial #6; coverage matrix runnable; perf lanes green |
| **C7** | 13–15 | — | — | Measurement: coverage matrix, Flagships G/H, foundry distribution, §33.16 bundle | **Q2 package submitted day 15**; challenge windows close; adjudication begins |

Timeline is the aggressive case; §9 states the tempo-independence rule. Q3/Q2 *verdicts* land on external calendars after submission — by design.

---

## 5. Cycle specifications

### C0 — Charter and restructure (plan-space only; no implementation swarm)

Scope: execute the Cycle 0 Work Order in full — kernel extraction into the Constitution; apply the Rev 7 fixes from the Audit Findings Ledger (Appendix B regeneration against §10.6, R0/R2 signature-envelope fix, §22.4 scope-totality condition, hasher law, symmetry budget row, disclosure-policy section, enumeration gaps); add the §34.9 addendum protocol; resolve the §35 decisions that gate C1 code (hash algorithm, canonical serialization grammar, DecodedStreamId cost model, evidence-checker isolation, license) and explicitly defer the rest; author the C1 delta plan; convert C1 delta + day-zero track to beads; run bead polish to steady state.
Gate: Charter committed through the substrate; C1 beads pass `br dep cycles` clean; SpecCard coverage plan for the R0 surface exists.

### C1 — Kernel + immune system + R0 wedge

Scope: L0–L2. Byte sources and snapshots; file lexer; COS objects; xref tables and streams; revision discovery; object streams; common filters (Flate + predictors, ASCIIHex, ASCII85, RunLength, LZW); recovery-as-bounded-hypothesis-search v1; encryption **inventory plus standard-handler read decryption with caller-supplied credentials** (RC4, AESV2, AESV3, version-specific password preparation) — read decryption is R0-scope per the R0 exclusion clause and is needed before the C3 wild-tail gate; the complete identity/evidence/report/checker stack; **the immune system: generated report schemas, claim registry generated from consequence contracts, contract-truth checks (API existence, dependency agreement, claim-registry linkage — never heading checks), drift auditor as a repository gate**; coverage-guided fuzzing from hour one; **CLI surface** (§25.3) so the wedge is invocable; clause-tagging live from the first contract.
Explicitly excluded: rendering, fonts, public-key handlers, any writer.
Gate: Workflow B end-to-end on hostile files (complete OpenReport with recovery alternatives and security inventory); zero reachable panics under the fuzz corpus; G0–G3-subset lanes green; SpecCard coverage for the R0 surface complete; cycle-close drift audit + held-out probe + sealed trial record.
Deliverable: **the sellable inspection wedge.**

### C2 — Render engine minus real text

Scope: content-stream lexer; page-program VM and graphics state; paths, clipping, winding rules; transforms; baseline images (DCT/JPEG, Flate-backed) in device color spaces; the rasterizer; RenderReports with D2 same-build pixel determinism; transparency subset per R1's declared profile. Text shows as explicit substitution-or-refusal receipts under the page-local refusal law — honest, not embarrassing. **Benchmark tracking begins here** and runs every cycle so performance regressions surface continuously instead of at C7 measurement.
Gate: G2 render lanes on the non-text corpus slice; D2 receipts reproducible; drift audit + probe + trial record.

### C3 — Text stack + color, R1 ships

Scope: L4. Font parsing (TrueType, CFF, Type1, CID/Type0, Type3); CMaps; budgeted glyph execution behind the FontExecutionService protocol; text extraction (Workflow C); ToUnicode and text-semantics claims; the ICC color pipeline proper; the external-processor divergence harness (PDFium, MuPDF, Poppler, pdf.js) and **Observatory seed as records + minimized witnesses only** — the browser playground waits for the WASM surface (C4+), per Bet 21's own architecture.
Gate: **strict-open + render over the steward-sealed wild-tail corpus, including credentialed encrypted documents** (decryption landed in C1); divergence reports generated and classified; R1 claim envelope published with page-local refusal accounting; drift audit + probe + trial record.

### C4 — Writer, R2 ships — the Q3 checkpoint

Scope: draft roots and the builder API; canonical and preservation serializers; incremental updates; font subsetting and embedding; **structural signature discovery and impact classification** (ByteRange, DocMDP/FieldMDP/lock classification — the envelope fix; cryptographic trust validation stays in C5); external-reader matrix; round-trip metamorphic gauntlet; **WASM surface lands** (enables the Observatory playground); **release engineering begins** (reproducible builds, packaging, docs, G6.1 supply-chain lanes) so the wedge is installable by customers.
Then the checkpoint — build pauses, evidence assembles: equal-resource **Baselines A–D** (plus E, expert comparison, where feasible), mechanism **ablations**, red-team results from the window that has been running since day 0, the **Evolution Trial (Flagship F)** run formally against the R2 artifact as the addendum-safety rehearsal, and the ledger to date.
Gate: **Q3 package submitted to independent review on ~day 9.** The verdict pends on the reviewers' calendar; the campaign continues without waiting.

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

Scope: freeze the comparator field per the day-zero committed discovery protocol; run the clause-by-clause coverage matrix across MonkeyBee and the field; execute the supremacy lanes — **Flagships G and H by name**; compile the foundry distribution from cycle trial records #1–#6 (attempts, medians, failures — the loop itself is the foundry evidence); assemble and publish the §33.16 evaluation bundle; challenge windows close on their predeclared schedule; independent adjudication begins.
Gate: **Q2 package submitted ~day 15.** Campaign ends at submission; verdicts arrive when they arrive.

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

| Q3 requirement (§33 ladder) | Where it comes from |
|---|---|
| Substance that works beyond staged paths | C1–C4 artifact + wild-tail gate + external-reader matrix |
| Prospective, bounded, authenticated provenance | Ledger from day 0; sealed cycle trial records; commitment substrate |
| Grounding that survives attack | Continuous red team; independent falsifiers; Flagship D lineage diversity; seeded-defect trials |
| Zero Grade-A truth drift | Immune system from C1; per-cycle drift audits |
| Production disproportion | C4 Baselines A–D(/E) + ablations + full attempt distribution |
| Independence | Day-zero engagement; self-award prohibited; honest degradation logging |

| Q2 requirement | Where it comes from |
|---|---|
| The measurement instrument | Clause tagging from C1; scorer at C6 |
| The surface to measure | R0–R4 across C1–C6, including the authoring track |
| The field | Day-zero discovery commitments; C7 freeze; predeclared challenge windows |
| The comparison | C7 coverage matrix + Flagships G/H under the committed statistical protocol |
| The credibility | Everything in the Q3 column, already in motion |

**The reframe that governs the whole campaign:** each cycle, closed properly, *is* one foundry trial and one lineage data point. The loop is not overhead on the way to the verdicts — it is the evidence generator. FrankenSim ran the same loop uninstrumented and received zero evidentiary credit for it.

---

## 8. Campaign risks, ordered by lethality

1. **Baseline cost concentration.** Baselines A–D mean funding multiple full vanilla-agent rebuild attempts at equal budget — the most expensive, least fun, most skippable item, and skipping it silently selects FrankenSim's outcome, because without baselines there is zero disproportion evidence. Mitigation: baselines are precommitted at day 0 with budget reserved; the Charter treats a baseline cut as a formal downgrade of G2, never a quiet omission.
2. **SpecCard human latency.** Two-person meaning review is the slowest step in a compute-unlimited campaign and gates every cycle's swarm. Mitigation: pipeline stands up day 0; card production runs one cycle ahead of implementation.
3. **Independence layer non-materialization.** Mitigation: the graceful-degradation law; honest logging; claims cap at self-attested tiers rather than pretending.
4. **Drift at swarm tempo.** Two Grade-A drifts occurred in this ecology at documentation stage, before any code. Mitigation: the immune system ships in C1 before growth; cycle-close gates are blocking.
5. **Kernel-touch addendum.** A C3+ discovery that forces an identity-grammar change invalidates receipts. Mitigation: C4's Evolution Trial rehearses extension safety; kernel-touch protocol makes the cost explicit instead of silent.
6. **Verdict latency.** External reviewers' calendars bound Q3/Q2 answers. Mitigation: none, by design — the verdicts' value comes precisely from not controlling them.
7. **Own-goal falsifier failure (the F-01 pattern).** The whole ecology can agree on a wrong certificate. Mitigation: red team from a different model family; seeded-defect detection-rate trials; external oracles the generator cannot redefine.

---

## 9. Timeline and tempo independence

Day map (aggressive case): C0 days 0–1; C1 1–3; C2 3–5; C3 5–7; C4 7–9 (**Q3 package day 9**); C5 9–11; C6 11–13; C7 13–15 (**Q2 package day 15**). Submission dates are campaign-controlled; verdict dates are not.

**Tempo independence:** the structure is identical whether the campaign takes two weeks or six — same seven delta plans, same gates, same evidence thread. Cycle duration is set by observed telemetry (beads-per-cycle the polish rounds can hold, drift-audit findings per boundary), not by the calendar.

**Compressed 5-cycle variant** (merge C2+C3 into one rendering cycle; C5+C6 into one transforms-plus-fidelity cycle): permitted only if C1 telemetry shows the polish rounds holding the larger graphs at steady state and the C1 drift audit is clean. Default is the 7-cycle spacing.

---

## 10. Commitment mechanics for this Charter

This Charter becomes evidence only when committed through the tamper-evident substrate (independent steward custody or witnessed append-only log) alongside the discovery protocols — a git commit alone is decoration. The committed Charter hash is the campaign's first ledger entry. Amendments follow §11 and are committed the same way; the diff history of the Charter is itself part of the lineage evidence.

## 11. Change control

Charter amendments require: a written rationale entry in the ledger; classification as `scope`, `sequence`, `gate`, or `goal` change; and re-commitment through the substrate. A `goal` change (touching G1/G2/G3 or the degradation law) additionally requires an explicit note in every subsequently published claim that the campaign's goals changed mid-course, with the date. Silent goal drift is the failure mode this clause exists to prevent.

---

*End of Charter v1.0. First action: execute CYCLE_0_WORK_ORDER.md.*
