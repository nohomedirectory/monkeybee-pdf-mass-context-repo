---
generated-by: Codex G6 conditional Charter-set successor owner
date: 2026-07-14
inputs:
  - CAMPAIGN_CHARTER_REASONING.md
  - MONKEYBEE_CAMPAIGN_CHARTER_v1.md
  - CYCLE_0_WORK_ORDER.md
  - AUDIT_FINDINGS_LEDGER.md
  - gauntlet/ROUND_LOG.md (R19–R22)
  - DISPUTES.md
  - MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md §10.3, §§24.12–24.16, §31 G/H, §33, §§34.4–34.5, §35
status: PROPOSED
ratification: awaiting human
evidence-status: provisional-pending-substrate
owner-fsm: DONE
---

# Campaign Charter Reasoning

**Version:** 1.1 (PROPOSED — awaiting human ratification)
**Date:** 2026-07-14
**Companion to:** MONKEYBEE_CAMPAIGN_CHARTER_v1.1.md if that proposed successor is human-ratified; otherwise v1.0 remains governing canon
**Purpose:** Every structural choice in the Charter, justified. Per the planning methodology's own law — a plan without *why* forces future agents to guess, and guessing is where coherence dies. This document is the *why*. It is reference material for delta-plan authors and review rounds; it is never converted to beads.
**Successor relation:** Carries Reasoning v1.0 forward with only the graded repairs below. It does not supersede v1.0 unless the human ratifies the linked Charter-set successors.

## v1.1 changelog

| Finding | Exact repair in this successor |
|---|---|
| `R19-A02` | The cycle-boundary rationale now places minimum customer installability in C1 and describes C4 as the expansion into the broader release-engineering program. |
| `R19-A06` | The day-zero and Q2 rationale now names protocol execution by scouts, challenge handling, and discovery-report freeze rather than treating a pre-search commitment as the field producer. |
| `R19-A07` | The C7 and timeline rationale now preserves report freeze -> evaluation commitment -> measurement, plus a scope-limited dated package and later-addendum branch if windows remain open. |
| `R19-B01` | No repair is admitted in this draft. R20–R22 did not resolve the internal-performance-versus-S6 premise; the existing rationale is not silently reinterpreted and remains pending human evidence. |
| `R20-A02` | The Q3 rationale no longer invents a six-condition §33.15 decomposition; it separates artifact properties, artifact-assurance gates, and foundry-supporting evidence. |
| `R20-A03` | Section 3 now distinguishes compute-compressible baseline execution from the calendar-bound historical-vintage freeze. |
| `R20-A05` | The Q2/timeline rationale now distinguishes the discovery nomination/challenge window from later claim challenge and keeps the three-stage order explicit. |
| `R20-A07` | The Q3 rationale now includes exact §33.3 artifact/operational boundary and operational closure as artifact properties. |
| `R20-B02` (grade B; premise-supported, not promoted) | The Q2 rationale now treats clause completion as a separate comparison, reports S1–S6 separately, and limits the headline to the strongest admitted scope actually earned. |
| `R21-A03` | The graceful-degradation rationale now separates mandatory product integrity from optional §33 evidence admission, so unavailable independent custody cannot block G1 or receive silent claim credit. |
| `R21-A04` | The existing R19-A02 rationale is retained: minimum customer installability lands in C1 and the broader release program expands in C4. |
| `R21-A05` | The timeline rationale now names the internally controlled build-and-submit close and the externally controlled adjudication tail as distinct endpoints. |
| `R21-A06` | The Q3 rationale now distinguishes six construction-cycle records from C7's evaluation-cycle record; the latter is lineage/evaluation evidence, not candidate construction. |
| `R21-A07` | The rationale now cites one versioned `CycleTrialRecordSchemaId` rather than restating an incomplete field subset. |
| `R21-A09` | The existing three-stage discovery/report/evaluation order remains explicit and precedes measurement. |
| `R21-A10` | The day-zero rationale retains the main pre-implementation split and adds the independently stewarded fresh-replacement path after adaptive exhaustion without relabeling exposed data. |
| `R21-A13` | “Two Grade-A defects” is narrowed to the two cited Grade-A duplication-drift examples; no ledger row or grade changes. |
| `R22-A01` | The existing ordered scope repair is retained: day-zero discovery commitment alone earns no field scope, and `observed_field_lead` additionally requires the material lawfully pinnable closed/opaque systems actually measured. |
| `R22-A02` | The C5 rationale now says the named R3 CDR envelope reaches its sellable gate, rather than using unscoped completeness vocabulary; the boundary and feature rationale remain intact. |
| `R22-A03` | The unsupported, undated competitor-gap premise and magnitude are deleted. Parse-and-preserve/out-cover remains a strategy to test only under the committed discovery and evaluation protocols; no comparator was observed or contacted for this repair. |
| `R22-A04` | The unsupported priority and historic-significance predicates are deleted while preserving the distinction between a decidable claim, inherited method, instrumentation, invention, and superior skill. |
| `R22-B01` (grade B; premise-supported, not promoted) | The existing R20-B02 repair makes the post-report evaluation commitment select one admitted scope and states that `full-field` is not a fourth scope; no scope is pre-awarded. |

---

## 1. Why restructure Rev 7 at all (Constitution / Charter / delta plans)

Three forcing facts:

**Context economics.** Rev 7 is ~75,000 words. The planning methodology's ceiling — a plan a fresh agent can hold and act on — is strained at that size, and every addendum makes it worse. A campaign of seven cycles against one monolithic, growing plan means every cycle pays the full context cost and every polish round defends the full surface. Splitting means each cycle holds: kernel (stable, memorized by reference), Charter (short), one delta plan (~2–4k lines). Nothing else.

**Drift mechanics.** The two cited Grade-A *duplication-drift examples* from the historical audits are Appendix B falling out of sync with §10.6 and ALIEN_ARTIFACT.md falling out of sync with its own re-audit; they are not the ledger's total Grade-A population. Rev 7 hand-restates its central laws in four to six places each (idempotency ~25 mentions, nonce ~23). Every addendum cycle multiplies restatement sites. The split assigns each law exactly one normative home (the Constitution), makes everything else a generated echo or a reference, and gives the drift auditor a tractable target.

**Kernel stability is the addendum enabler.** The entire economics of "plan against the repo, bead the delta, swarm, repeat" collapses if an addendum can change the identity grammar — every receipt, cache key, and claim downstream invalidates. Declaring the kernel and forbidding casual touch converts "hopefully nothing breaks" into a checkable per-cycle declaration. The kernel freezes *laws*, not *inventory*: the crate atlas stays provisional (per Rev 7 §30 itself) because P19 merges and boundary-budget splits are normal evolution, while layer direction and the budget rules are law.

## 2. Why seven cycles, and why each boundary sits where it does

The decomposition rule: a cycle boundary belongs wherever (a) a claim envelope can ship, (b) the beads graph would otherwise exceed what polish rounds hold at steady state, or (c) an evidence checkpoint needs a stable artifact. Applying it:

- **C0 separate from C1** because plan-space work and swarm work have different failure modes; mixing them is how restructuring errors ship into code.
- **C1 = kernel + immune system + R0** because (i) R0 is independently sellable — the wedge exists before anything renders, so its minimum customer-installable CLI slice and admission evidence also land here; (ii) the immune system must predate growth — drift appeared in this ecology at documentation stage, so building six cycles of code before the drift auditor exists is knowingly repeating FrankenSim F-09..F-12; (iii) the kernel beads exactly once, so it must be first. Read-side standard-handler decryption lands here — not later — because the R0 exclusion clause makes credentialed decryption R0-scope, and the C3 wild-tail gate hits encrypted files immediately (this was Charter correction C-1; the first campaign draft misplaced it in C5).
- **C2/C3 split (rendering before text)** because fonts are the single largest domain in the project — five formats, CMaps, glyph execution sandboxing, text semantics. One beads graph holding VM + raster + fonts + ICC is precisely the graph the polish protocol cannot hold; and the plan's page-local refusal law makes a text-less renderer *honest*, not embarrassing — refusal receipts are the product working as designed.
- **C4 = writer + Q3 checkpoint** because Q3 is achievable at R2: the ladder's artifact-candidate rung needs substance-that-works plus provenance plus disproportion, none of which require R4 fidelity. Checkpointing here rather than at campaign end means the verdict clock (external, uncontrollable) starts six days earlier, and a negative review arrives while there is still campaign left to respond with. WASM lands here because Bet 21's Observatory playground runs on it; the release program expands here from C1's minimum installable slice into reproducible builds, broader packaging and documentation, and supply-chain evidence.
- **C5 = transforms/security** because redaction, sanitization, and signature *trust* validation bring the declared R3 commercial CDR envelope to its sellable gate, and because the agent/EditSession surface needs a writer to mutate through — it cannot come earlier.
- **C6 = two tracks** because fidelity (codecs, transparency, profiles) and authoring (layout engine, UAX ownership, tagged generation) are disjoint domains that only share the R4 label; running them as tracks keeps each beads graph coherent. The performance-hardening slice lives here — not earlier as a dedicated cycle, not later as a scramble — because D-class determinism discipline is kernel (C1) and benchmark *tracking* starts C2, so by C6 the perf work is targeted optimization against six cycles of telemetry rather than blind tuning. The coverage *scorer* is built here, but the *tagging* it reads began at C1 — retro-tagging five cycles of features at C6 would itself be a drift factory.
- **C7 = pure measurement** because mixing building and measuring in one cycle invites exactly the evaluator-optimization the protocol forbids. By C7, nothing new is built. It emits evaluation-cycle record #7 for measurement attempts, failures, interventions, and lineage, but that record is never pooled as candidate construction with construction-cycle records #1–#6. The day-zero pre-search commitment has governed scout execution and the nomination/challenge process; after the applicable window closes, the discovery report freezes the field, then the bound evaluation protocol is committed without result inspection, and only then does measurement begin. If a ratified window remains open at the dated C7 boundary, that package remains scope-limited and the field measurement moves to a later addendum under the same order.

Seven, not five, by default: the compressed variant is real but earns its use only from C1 telemetry. Seven, not ten: the remaining plausible splits (C1 into kernel/R0, C6 tracks into cycles) buy graph size relief at the cost of two more archaeology+delta+gate overheads, and the graphs at seven are already inside the polish protocol's demonstrated range.

## 3. Why the day-zero track exists: what compute cannot compress

Unlimited compute compresses: implementation, tests, fuzz-hours, **contemporaneous baseline execution**, ablations, the coverage matrix, documentation. It cannot recreate a **historical baseline vintage** after the frontier moves: the day-zero task statement and model/harness/tool manifest are calendar-bound evidence even when later execution is cheap. It also compresses **none** of: steward and reviewer recruitment (humans), two-person SpecCard meaning review (humans, and on *every* cycle's critical path), discovery nomination/challenge windows (calendar objects whose credibility is proportional to their duration — a 48-hour window on a field claim reads as theater to exactly the adversarial reviewer who matters), the main construction-era held-out split, and external verdict latency. The main split must precede implementation; exposed or adaptively consumed data can only become development/regression data. A later stronger confirmatory claim may use a fresh-ID replacement only when an independent steward prospectively seals it relative to a frozen candidate and evaluation protocol. Discovery execution is real campaign work: named independent human scouts must run the committed search, characterize candidates, process nominations/challenges, record deviations, and produce the report that later measurement binds.

Therefore every uncompressible item moves off the build's critical path and onto a parallel track that starts at hour zero. This is the single largest structural difference between this campaign and the FrankenSim trajectory, whose tempo it otherwise shares: evidence apparatus at swarm tempo, from the start, or the two-week pace produces a two-week FrankenSim — temporal concentration 4.5, grounding 2.0, verdict underdetermined.

## 4. Theory of victory: Q3

The §33.15 artifact-candidate rung does **not** decompose into six campaign-authored conditions. It requires independent judgment of a functioning, provenance-conditioned artifact; §33.18 supplies the artifact properties of integrated consequence, assurance, operational closure, exact boundary, and provenance-conditioned comparison. The Charter's evidence-thread table therefore labels artifact properties, supporting assurance gates, and foundry evidence separately instead of borrowing one object into another. The design insights worth stating:

- **Substance is deliberately sized down.** R0–R2 with closed provenance beats R0–R4 with open questions; a smaller artifact whose causal account closes is *more* alien-eligible than a bigger one that impresses. This is why the checkpoint is C4, not C7.
- **The loop is foundry evidence, not a substitute for the artifact.** Work Order §3's versioned `CycleTrialRecordSchemaId` is the sole normative field interface. Construction-cycle records #1–#6 may enter the foundry production-attempt distribution only after the independent evidence-admission extension; evaluation-cycle record #7 stays separate. A missing extension removes §33 credit without blocking the product. A foundry failure does not logically bar the artifact rung, and a foundry win cannot supply missing integrated consequence, assurance, operational closure, or exact boundary. FrankenSim ran the identical loop and got zero credit because nothing was committed prospectively—this campaign's evidentiary advantage on provenance and production comparison is instrumentation, not skill.
- **The red team is continuous, not a phase.** The F-01 lesson: the killer failure is a false certificate the whole ecology agrees on — source, tests, contract, and campaign prose sharing one wrong premise. Countermeasures that share the ecology (same model family writing checker and checked) are structurally weak; hence the different-model-family requirement and seeded-defect detection-rate trials, which measure the falsifiers instead of trusting them.
- **Honest degradation beats silent pretending.** Every independence element that cannot be obtained is logged, and the affected claims cap at self-attested tiers. A campaign that says "we could not get an external adjudicator; this claim is therefore internal-only" is *more* credible on its remaining claims, not less.

## 5. Theory of victory: Q2

Q2 is a PDF-clause-completion comparison plus separately reported S1–S6 lane outcomes. It reuses the commitment, provenance, independence, and uncertainty infrastructure developed for Q3, but it does not borrow an artifact or foundry verdict into a product comparison. Flagship H instantiates the S2 wild-tail campaign; optional Flagship G is a separate legacy-execution campaign and supplies neither the completion denominator nor the missing S1–S6 lanes. Its requirements:

- **The instrument before the claim.** Clause completion is unmeasurable without the clause-by-clause matrix (Rev 7 §0.2 concedes it doesn't exist). Tagging from C1 + scorer at C6 produces the instrument as a side effect of disciplined building rather than a retrofit. The post-report evaluation commitment fixes the completion `FieldDefinitionId`, licensed-card denominator, eligibility, analysis unit, adjudication, Goodhart guard, fallback, and one of the three admitted claim scopes; `full-field` is not a fourth scope.
- **The denominator is friendlier than folk intuition.** Strict ISO 32000-2 scoring drops XFA (deprecated), Movie/Sound (deprecated), PostScript XObjects (deprecated) from the field — Acrobat's most famous exclusives largely exit the denominator — and specifies ECMAScript *actions*, not Acrobat's full JS API. What remains genuinely in-spec and excluded from MonkeyBee's envelope: 3D artwork and rich media. The campaign's honest options are implement-to-a-declared-tier or score them parse-and-preserve and out-cover elsewhere. The second remains a strategy to test under the prospectively committed discovery and evaluation protocols; this successor asserts no comparator capability gap at C0.
- **The field is frozen through an ordered evidence chain that starts before the code.** The discovery protocol, inclusion criteria, independent human scouts, and discovery nomination/challenge-window duration are committed at day 0; scouts execute that protocol and close that window; the resulting `CompetitorDiscoveryReportId` freezes the field; and only then may the bound evaluation protocol be committed before measurement. Any post-publication claim-challenge period is separate. That chain, not the first commitment alone, permits `registered_open_field_lead`; `observed_field_lead` additionally requires the same evaluation to lawfully pin and actually measure the material closed/opaque systems observed under that field definition. If the chain remains unfinished, the vocabulary keeps the result at `named_set_lead` rather than laundering it into a field claim.

## 6. FrankenSim lessons → campaign countermeasures

| Re-audit finding | Campaign countermeasure |
|---|---|
| F-01 false certificate survived source+tests+contract+campaign | Different-model-family red team; seeded-defect trials; external oracles the generator cannot redefine |
| F-02 contract described a removed, unsound API | Contract-truth checks: named-API existence, dependency agreement, claim-registry linkage — in C1, before growth |
| F-04 checker verified headings, not truth | Same; plus the explicit rule that heading checks never count as verification |
| F-05/F-06 license metadata and toolchain instructions wrong | Day-zero license decision; generated quick-start from pinned toolchain |
| F-08/F-09/F-10/F-11/F-12 five stale truth surfaces | Single normative home per law; generated echoes; blocking per-cycle drift audit |
| F-13 orphaned scaffolds as sediment | Quarantine-with-tombstone rule in the repository constitution |
| F-14 no head-specific public execution proof | Evidence-admitted records under the versioned `CycleTrialRecordSchemaId`, with logs, inventory, host identity, and no-credit disclosure when independent sealing is absent |
| F-15 counts mistaken for depth | Counts are inventory facts; only Gauntlet-tier evidence supports claims |
| §8.10 selection effects unknown | The ledger records the distribution, not the winning trajectory |
| §11.3 no construction ledger, unrecoverable | Ledger opens at day 0 — the one advantage that cannot be retrofitted |

## 7. Timeline reconciliation (the 6–18-month and 15-day estimates are both real)

Two duration estimates were given in this project's planning conversation, and they differ by an order of magnitude because they price different things. The 6–18-month figure assumed normal compute, serial cycles, and human latency (recruitment, review, windows) *inside* the critical path, and measured to *verdict*. The 15-day figure assumes effectively unlimited parallel compute, every human-bound item moved to the day-zero concurrent track, and measures to a *dated package boundary*—with verdicts explicitly external. If the ratified discovery nomination/challenge window has closed, the ordered field package may be ready at that boundary; if it remains open, the package is scope-limited and the field measurement follows in a later addendum after report freeze and evaluation commitment. A separate post-publication challenge period does not close discovery retroactively. The internally controlled `build-and-submit close` ends campaign execution after the final admissible submission or explicit G1-only close; the externally controlled `adjudication tail` may later return, qualify, reject, or never return Q2/Q3 verdicts. The Charter adopts the tempo-independence rule so that the structure survives either reality: same seven plans, same gates, whether two weeks or six months. Submission never answers a question by itself, and no field package or verdict is promised in two weeks regardless of human windows.

## 8. The graceful-degradation design

The campaign serves two goals that fail in opposite directions: the foundry/production-comparison evidence dies by under-instrumenting, while the survival goal dies by over-instrumenting when claim-evidence apparatus starves the sellable product. A baseline cut formally downgrades the Q3 package but does not logically erase an otherwise earned artifact-candidate judgment. The resolution is architectural, not motivational: **no G1 deliverable depends on G2/G3 evidence admission.** Every cycle retains a blocking product-integrity close—clean-room/SpecCard, functional and hostile-input safety, installability where applicable, drift audit, and an operational record. The independently stewarded probe and record seal are a separate §33 extension: absence removes claim credit and is logged, but the wedge may still ship. The checkpoint (C4's package) and measurement package (C7) require that extension and detach cleanly. This clause exists in writing because mid-campaign resource pressure will test it, and the failure mode it prevents—quietly cannibalizing the evidence budget while still talking like the verdicts are coming—is worse than either honest outcome.

## 9. Honest limits: how this campaign can fail, and what it cannot claim

- **The gauntlet can fail on the merits.** Baselines A–D might not lose — vanilla agents at equal budget might reproduce the integration, in which case the foundry production-disproportion claim fails and the artifact comparison reports the result without borrowing it across objects. This outcome is *allowed*; a campaign that cannot fail proves nothing.
- **The artifact can grow its own F-01.** A false certificate the whole ecology agrees on, surviving the red team. The seeded-defect trials estimate the probability; they do not zero it.
- **Reviewers can say no**, or say nothing for months. Submission ≠ verdict.
- **The moat is narrower than it sounds.** What FrankenSim permanently lacks is the *construction-era* ledger — attempts, search, selection, cost — so its foundry/provenance claims stay underdetermined. Its *artifact-level* assurance (sealed verification bundles, external audits, adversarial certificate hunts) can be earned late, any time its author chooses. MonkeyBee's structural advantage is specifically on provenance and disproportion axes, not a general and permanent superiority. Stated here because the Charter's earlier drafting history contained the overclaim ("permanently capped, forever") and this document is where the correction lives.
- **A yes on Q2/Q3 is not a proof of superior skill.** It is proof of a decidable claim. The method being executed is inherited; instrumenting an inherited method is a different achievement from inventing it, and the campaign's public claims must keep that distinction or forfeit exactly the credibility they exist to earn.

## 10. Corrections incorporated (drafting provenance)

Charter v1.0 already contains the round-3 audit fixes to its own first draft: C-1 (read decryption moved to C1), C-2 (SpecCard pipeline on the day-zero track with per-cycle coverage gates), C-3 (CLI C1, WASM C4, C-ABI preview C5, freeze post-R4), C-4 (D-classes C1, benchmarks C2, hardening slice C6), C-5 (authoring track added to C6), C-6 (corpus sealing day 0; v1.1 adds minimum installability at C1 while retaining the broader release program at C4–5), C-7 (kernel freezes layer law, not the crate atlas; kernel beads exactly once), C-8 (tagging C1, scorer C6), C-9 (Charter through the commitment substrate), C-10 (Evolution Trial formalized at C4; probes at every boundary; Flagships G/H named at C7), C-11 (day-15 arithmetic), C-12 (baseline-cost risk promoted to #1; Baseline E acknowledged). Strategic corrections S-1 through S-4 are reflected in §7 and §9 above. Future audits verify against this list; the Audit Ledger retains the historical R1–R3 consolidation, while live gauntlet packets and owner dispositions follow its versioned handoff.

---

*End of proposed Reasoning v1.1.*
