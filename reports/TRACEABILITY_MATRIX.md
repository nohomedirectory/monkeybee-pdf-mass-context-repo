---
generated-by: Claude G4 owner (NTM session `monkeybee-pdf-mass-context-repo--g4`, `claude-opus-4-8`)
date: 2026-07-14
inputs:
  - MONKEYBEE_CAMPAIGN_CHARTER_v1.md (§0, §2, §3, §4, §5, §6, §7, §8, §9)
  - CYCLE_0_WORK_ORDER.md (§3 addendum protocol, §4 decisions, §5 day-zero checklist)
  - AUDIT_FINDINGS_LEDGER.md (R1-5, R2-N1, R2-N5)
  - MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md (§0.2, §3.0, §3.5, §4.6, §10.10, §11.9, §13.9, §24.12–24.16, §26.2–26.3, §27–27.4, §28.3, §30.5–30.10, §31.4–31.10, §33.1–33.18, §35)
  - AGENTS.md, OVERNIGHT_GOAL.md, INDEX.md, DISPUTES.md
status: PROPOSED
evidence-status: provisional-pending-substrate
artifact-status: self-check passed; routed for fresh-context review
owner-fsm-authority: `ledger/owners/G4_STATE.md` is the single normative home of the G4 owner phase. This header never states owner phase.
---

# Q2/Q3 Traceability Matrix

This matrix maps every requirement of the campaign's two precommitted questions to the cycle that produces it, the artifact that carries it, the gate that admits it, the authority that mandates it, its prerequisites, and what happens to the claim when the requirement is not met. It then runs the map backwards — from artifact and gate to the requirement each one supports — and reports what fails the zero-orphan rule in either direction.

The matrix is an audit instrument, not a plan. It authors no cycle scope, resolves no dispute, and awards no claim. Where it finds a gap, it names the gap and the canon that creates it; the disposition belongs to the human and, where a canonical document is implicated, to the dispute channel.

**Reading the status column.** `OWNED` — a cycle, artifact, and gate exist and are named in canon. `PARTIAL` — a producer exists but the requirement is not fully discharged by it, or the gate does not test it. `GAP` — canon requires it and no Charter cycle, day-zero item, or gate produces it. `EXTERNAL` — discharged outside the campaign's control by design (reviewer calendars, human ratification).

**Grade vocabulary for findings** follows `AUDIT_FINDINGS_LEDGER.md`: A = directly confirmed in the artifact (grep or derivation); B = confirmed by close reading; C = judgment call.

---

## 0. Scope and the two questions

From Charter §0, verbatim in substance:

- **Q3** — Does MonkeyBee earn `Artifact-alien candidate` on the Rev 7 §33.15 ladder, under a bounded, authenticated production ledger?
- **Q2** — Does MonkeyBee earn an uncertainty-aware `leading` outcome on a predeclared, full-field PDF-completion `FieldDefinitionId`, plus supremacy-lane results, against the frozen comparator field?

Two consequences of the ladder govern everything below, and the matrix enforces them rather than assuming them.

**The claimed rung is the Artifact rung only.** Rev 7 §33.15 separates Artifact (`A0`/`A1`/`A2`/`Artifact-alien candidate`), Foundry (`F1`/`F2`/`Foundry-alien candidate`), and Lineage (`L1`/`L2`/`Lineage-alien candidate`) objects. §33.18 states the non-implication law and §33.17 states that evidence cannot be borrowed across objects. The campaign claims the Artifact rung. Therefore evidence classes that belong to the Foundry or Lineage objects — model/harness substitution (§33.7), repeatability across runs (`F2`), real elapsed evolution (`L2`) — are **not** requirements of Q3 as scoped, and this matrix does not manufacture them as gaps. Where the Charter emits such evidence anyway (the C7 foundry distribution; the C4 Evolution Trial), the matrix records which object it serves so that it cannot silently reinforce the Artifact rung it does not belong to.

**Baselines serve the Artifact rung here.** Charter §7's "Production disproportion" row could be misread as a foundry claim. Under §33.18 clause 1, artifact disproportion is precisely a "provenance-conditioned comparison with what that production envelope was expected to produce" — which is what Baselines A–D(/E) establish. The matrix maps baselines to the Artifact rung and says so explicitly, because the alternative reading would have the campaign asserting a foundry rung it never claims and cannot support at `F2` in fifteen days.

---

## 1. Q3 requirement register — forward direction

Requirement → producing cycle → artifact → gate → authority → prerequisites → failure/downgrade.

### 1.1 Substance: a functioning, integrated artifact (§33.18 cl. 1)

| ID | Requirement | Authority | Producing cycle | Artifact | Gate | Prerequisites | Failure / downgrade | Status |
|---|---|---|---|---|---|---|---|---|
| Q3-SUB-1 | Integrated artifact that works beyond staged paths (R0–R2 surface at minimum, by the C4 checkpoint) | Charter §7 row 1; §33.18 cl. 1 | C1–C4 | The R0/R1/R2 releases | C1, C2, C3, C4 close gates | SpecCard coverage per cycle surface; decisions in Work Order §4 | Artifact caps at `A1` ("substantively integrated … scoped evidence"); no `A2`, no candidate rung | OWNED |
| Q3-SUB-2 | Behavior on real hostile inputs, not curated fixtures | Charter §7 row 1; §33.13 empirical maturity | C3 | Wild-tail gate results over the steward-sealed corpus | C3 gate ("strict-open + render over the steward-sealed wild-tail corpus, including credentialed encrypted documents") | Corpus sealed **before** any implementation (day-zero item 6); C1 read decryption | Substance claim narrows to the curated corpus; `A2` unreachable — "beyond staged paths" is exactly what is unproven | OWNED |
| Q3-SUB-3 | Interoperability observed by processors MonkeyBee does not control | Charter §7 row 1; §24.4; §4.6 | C4 | External-reader matrix over writer output | C4 (R2 ships) | Writer (C4); black-box adapter firewall (§4.6); AGENTS rule 9 permits external observation only after day-zero item 3 is committed | Writer claims stay self-attested; round-trip metamorphic evidence loses its independent leg | OWNED |
| Q3-SUB-4 | Operational closure: clean install, reproducible builds, packaging, docs, quotas, migration, rollback, incident handling, support burden (§33.11) | §33.11; §33.18 cl. 1 | C4 (release engineering begins), C5–C6 | Packaging, docs, G6.1 supply-chain lanes | C4 gate names release engineering in scope; **no gate tests the §33.11 metric set** | Toolchain pin (Work Order §4.7); license (§4.5) | §33.11: "Missing complexity shifted outside the declared boundary invalidates the operational claim" — the artifact rung loses one of its four constituents | PARTIAL — see F-6 |
| Q3-SUB-5 | Declared artifact and operational boundary: runtime code, generic dependencies, construction-time agents, runtime host adapters/models/services, dev-only validators, corpora, human procedures, external infrastructure (§33.3) | §33.3 | **none named** | — | — | — | Without the boundary, "integrated consequence" has no denominator and the reviewers cannot locate the claim. §33.3 is a precondition of the Artifact rung, not an accessory | GAP — see F-5 |
| Q3-SUB-6 | Integration-surplus metrics: cross-layer invariant violations, duplicate concepts, provenance completeness, automatic inheritance of budgets/diagnostics/evidence/fuzzing/schemas, change-propagation breadth, integration defects, human review per merged consequence (§33.9) | §33.9 | **none named** | — | The C1 immune system *generates* several of these signals; nothing *measures or reports* them as §33.9 metrics | Immune system (C1); drift audits (all cycles) | The Artifact rung is judged on "integrated consequence." §33.9 is the instrument that measures it. Without it, reviewers are asked to judge integration by inspection | GAP — see F-5 |
| Q3-SUB-7 | Consequence-compression audit: specification leverage, verification leverage, integration leverage, marginal primitive/ontology count, outcome quality/cost against the strongest ordinary composition (§33.12) | §33.12 | **none named** | — | — | Contracts and claim registry (C1) supply the raw material | §33.12: "A feature that adds more independent machinery than integrated consequence is accumulation, not alien compression." This is the discriminating test between the candidate rung and `A1`; unrun, the discrimination is not made | GAP — see F-5 |

### 1.2 Provenance: prospective, bounded, authenticated (§33.1, §33.4)

| ID | Requirement | Authority | Producing cycle | Artifact | Gate | Prerequisites | Failure / downgrade | Status |
|---|---|---|---|---|---|---|---|---|
| Q3-PRV-1 | Production ledger opened **before any implementation agent runs**; models, harnesses, attempts, discarded branches, cost, human hours, selection decisions | Charter §3 item 1; §33.1 | Day zero | Production ledger | "before any implementation agent runs" (Charter §3.1) — a precondition on C1, not a close gate | Ledger backend decision (Work Order §4.6) | Entries become `retrospective` (§33.1) and cannot support a prospectively precommitted claim. The artifact rung survives with weakened provenance; the foundry rung would not | OWNED |
| Q3-PRV-2 | Tamper-evident commitment substrate: independent steward custody or witnessed append-only log. A bare git timestamp is insufficient | Charter §3 item 2, §10; §33.4; Work Order §6 | Day zero (human-bound) | Commitment substrate; Charter hash = ledger entry #1 | Charter §10 makes commitment the condition of the Charter being evidence at all | Human action; independent steward availability | **Load-bearing for both questions.** §24.16: without prospective commitment, Q2 caps at `named_set_lead`. §33.4: without it, claim families are not precommitted and the Q3 package is exploratory. Degradation: honest log, self-attested tiers | OWNED (human-bound; not yet executed — D-001) |
| Q3-PRV-3 | Precommitted claim families under one `EvaluationProtocolId`: artifact/foundry/lineage claim and reference class; supported profiles, metrics, determinism, failure conditions, claim expiry; baseline and ablation tasks; held-out commitments and access budgets; task-novelty, latent-archetype, training-data exposure, and benchmark-owner conflict analyses | §33.4 | **partially day zero** — Charter §3 item 3 commits the *discovery* protocols only | Discovery-protocol commitment | Day-zero dispatch | Substrate (Q3-PRV-2) | The C4 package's baselines, ablations, held-out probes, and novelty/leakage analyses would be measured under a protocol that was never committed before measurement — §33.4: "Post hoc discoveries are hypotheses until replicated under a new committed protocol" | PARTIAL — see F-7 |
| Q3-PRV-4 | Sealed cycle trial records ×6: attempts, failures, retries, cost, human interventions, median and best outcomes | Charter §6 cl. 6(d); Work Order §3 cl. 6(d); §33.1, §33.8 | C1–C6 | Six sealed trial records in the ledger | Every cycle close gate, blocking | Ledger open (Q3-PRV-1) | §34.9: "a cycle without a sealed record contributes nothing to any §33 claim regardless of what it shipped" | OWNED |
| Q3-PRV-5 | Total search and the full attempt distribution: success rate, median/percentiles, best-of-N, retries, interventions, defect distribution, representative failures, discarded branches | §33.8; Charter §5/C7 | C7 (compiled from trial records #1–#6) | Foundry distribution | C7 (Q2 package) | Q3-PRV-4 | §33.8: "Optional stopping, selective branch retention, or unreported provider routing invalidates a reliability claim." Note the object: this is Foundry-rung evidence (§33.18 cl. 2) | OWNED — but see the object note in F-9 |

### 1.3 Grounding that survives attack (§33.10, §27.1)

| ID | Requirement | Authority | Producing cycle | Artifact | Gate | Prerequisites | Failure / downgrade | Status |
|---|---|---|---|---|---|---|---|---|
| Q3-GRD-1 | Red team from a different model family **plus humans**, running continuously from day 0 — not inside C4 | Charter §3 item 4, §7 row 3, §8 risk 7 | Day zero → continuous | Red-team findings; results folded into the C4 package | C4 (Q3 package includes "red-team results from the window that has been running since day 0") | Independence layer engaged (human-bound) | Charter §3.4: what cannot be obtained is logged honestly and the dependent claim degrades to its self-attested tier. §33.10 grounding surplus loses its adversarial leg | OWNED (human-bound) |
| Q3-GRD-2 | Independent falsifiers with disclosed oracle lineage; lineage-diverse forensic tools for redaction | §27.1; §33.10; Charter §7 row 3; Flagship D (§31.4) | C1–C6 per contract; C5 for Flagship D | Falsifier pairing per consequence contract; Flagship D negative-evidence package | C5 gate ("Flagship D passes with disclosed tool lineage") | R1-3 fix (Flagship D's duplicated forensic-tool bullets must resolve into a stated two-tool lineage-diversity requirement) | §33.10: "A system that never demotes a claim is epistemically suspect." Shared-lineage oracles are correlation, not independence (§10.2.1) | OWNED |
| Q3-GRD-3 | Seeded-defect detection-rate trials | Charter §7 row 3, §8 risk 7; §27 G6.1 ("mutation/fault-seeding tests that measure whether the test suite catches plausible implementation defects") | **no cycle gate names it** | — | — | Immune system and falsifier stack (C1) | The F-01 pattern — the whole ecology agreeing on a wrong certificate — is the failure this trial is designed to catch. Charter §7 cites it as a Q3 evidence source; no gate requires it | GAP — see F-8 |
| Q3-GRD-4 | One held-out extension probe at **every** close gate, results recorded win-or-lose, drawn from the sealed pool | Charter §6 cl. 6(b); Work Order §3 cl. 6(b); §28.3 | C1–C6 | Probe results in each trial record | Every close gate, blocking | Held-out splits sealed by a steward **before any implementation exists** (day-zero item 6) | §28.3: once a case has shaped the implementation beyond the frozen protocol it becomes a regression fixture and a fresh independently stewarded replacement is required. Without steward sealing, no strong held-out claim exists at all | OWNED |
| Q3-GRD-5 | Recorded claim demotions after new evidence | §33.10 | C1–C6 (implicit in the evidence algebra) | Claim registry lifecycle states (`proposed`/`active`/`lapsed`/`withdrawn`, §10.3 cl. 29) | Drift audit reads the claim registry; no gate requires a demotion *record* | Claim registry (C1) | Reviewers cannot distinguish "never demoted because always right" from "never demoted because never checked" | PARTIAL — see F-8 |

### 1.4 Zero Grade-A truth drift

| ID | Requirement | Authority | Producing cycle | Artifact | Gate | Prerequisites | Failure / downgrade | Status |
|---|---|---|---|---|---|---|---|---|
| Q3-DFT-1 | Immune system as first-class capabilities: generated report schemas, claim registry generated from consequence contracts, contract-truth checks (API existence, dependency agreement, claim-registry linkage — never heading checks), drift auditor as a repository gate | Charter §5/C1, §7 row 4, §8 risk 4 | C1 | The immune-system capabilities with their own contracts and falsifiers | C1 gate | Kernel (C1); clause tagging live from the first contract | The two Grade-A defects in this ecology to date are both duplication drift (R1-1, R2-N7), both at *documentation* stage before any code. Without the immune system, C2+ inherits that failure mode at swarm tempo | OWNED |
| Q3-DFT-2 | Blocking per-cycle drift audit; zero Grade-A findings to pass | Charter §6 cl. 6(a); Work Order §3 cl. 6(a) | C1–C6 | Drift-audit output per cycle | Every close gate, blocking | Q3-DFT-1 | A cycle that ships with a Grade-A drift finding has broken the campaign's central claim about itself | OWNED |

### 1.5 Production disproportion (Artifact-rung reading — §33.18 cl. 1)

| ID | Requirement | Authority | Producing cycle | Artifact | Gate | Prerequisites | Failure / downgrade | Status |
|---|---|---|---|---|---|---|---|---|
| Q3-DIS-1 | Equal-resource Baselines A–D (plus E where feasible), under the §33.5.1 fairness and normalization law: same task, source pack, repository exposure, model/tool access, compute, elapsed feedback, human attention, attempt budget, stopping rule, held-out boundary — everything except the mechanism under study | §33.5, §33.5.1; Charter §5/C4, §8 risk 1 | C4 | Baseline results with nominal and consumed resources reported | C4 (Q3 package) | **Committed budget reserved at day 0** (Charter §8 risk 1; Work Order §5.8) | Charter §8 risk 1: skipping baselines "silently selects FrankenSim's outcome, because without baselines there is zero disproportion evidence." A cut is a **formal G2 downgrade**, never a quiet omission | OWNED (budget human-bound) |
| Q3-DIS-2 | Mechanism ablations (§33.6), each supplying the strongest ordinary replacement; predeclared migration effort, expected effects, interactions, stopping; null and negative results reported | §33.6; Charter §5/C4 | C4 | Ablation results | C4 (Q3 package) | R2-N5 fix: §33.5 Baselines C/D and §33.6 ablations must be disambiguated (repo-level vs mechanism-level); one experiment may not count as two evidence classes | Double-counting Baselines C/D as ablations would inflate the evidence base with a single experiment — an own-goal in the exact class §33 exists to prevent | OWNED |
| Q3-DIS-3 | Both baseline vintages: a **historical** baseline frozen near the program's start and a **contemporaneous** baseline run near the public claim date | §33.2 | **none named** — the Charter runs baselines once, at C4 | — | — | Q3-DIS-1 | §33.2: "A result may remain historically alien while lapsing as a current frontier claim." The Q3 verdict lands on the reviewers' calendar, by design, at an unbounded distance from the day-9 submission. Nothing refreshes the contemporaneous leg | GAP — see F-9 |
| Q3-DIS-4 | Drift, novelty, and leakage analysis: model/harness/provider changes; task similarity to learned archetypes and public repositories; training-data uncertainty; scaffold information that encodes the answer; whether the baseline had the same opportunity to learn | §33.5.2; §33.4 | **none named** | — | — | Precommitment (Q3-PRV-3) | §33.5.2 is what stands between a disproportion claim and an artifact whose task was already in the training distribution. A PDF engine is a heavily represented archetype; this analysis is not optional decoration | GAP — see F-7 |
| Q3-DIS-5 | Maturity taxonomy reported separately: structural, empirical, adaptive (§33.13) | §33.13 | **none named**; C7's §33.16 bundle lists maturity classification among its contents | §33.16 bundle (C7) | C7 | Trial records; Flagship F | §33.13: "Synthetic history … cannot be relabeled as years of empirical operation." A 15-day campaign has near-zero empirical maturity. Saying so is the requirement | PARTIAL — see F-5 |
| Q3-DIS-6 | Evolution-surplus test / Evolution Trial (Flagship F) against the R2 artifact | §33.14; §31.6; Charter §5/C4 | C4 | Evolution Trial results | C4 (Q3 package) | Independent evaluators select the extensions (§33.14) | §31.6 calls this "the primary lineage test." Under §33.17 its evidence belongs to the **Lineage** object, which the campaign does not claim. It legitimately supports *adaptive maturity* (§33.13) and the campaign's own addendum-safety rehearsal — and must not be presented as Artifact-rung disproportion | OWNED — object noted in F-9 |

### 1.6 Independence

| ID | Requirement | Authority | Producing cycle | Artifact | Gate | Prerequisites | Failure / downgrade | Status |
|---|---|---|---|---|---|---|---|---|
| Q3-IND-1 | Independence layer engaged at day 0: corpus steward, commitment custodian, red team (different model family + human), external reviewers/adjudicators | Charter §3 item 4, §7 row 6; §33.4 | Day zero (human-bound) | Outreach and role agreements (G5 packages) | Charter §3.4: "What cannot be obtained is logged honestly" | Human action; R1-5 (the plan assumed an unprovisioned human ecology; §35.1 must carry the recruitment/cost/degradation row) | Every claim that needed the missing party degrades to its self-attested tier rather than silently proceeding. Charter §8 risk 3 | OWNED (human-bound) |
| Q3-IND-2 | No self-award: the verdict is rendered by independent reviewers on their calendar | §33.15 ("The repository self-awards none of the candidate labels"); Charter §2/G2 | C4 submission → external | The Q3 package | C4 gate is **submission**, not verdict | Q3-IND-1 | If no independent reviewer is obtained, there is no verdict — the question is not answered, and no internal substitute is permitted | EXTERNAL |
| Q3-IND-3 | Honest degradation logging wherever the independence layer does not materialize | Charter §2 (degradation law), §3 item 4 | All cycles | Ledger entries; not-done list | Morning report; §33.16 bundle | — | This is the campaign's antidote to the FrankenSim pattern; failure here is the failure the whole repository exists to prevent | OWNED |

### 1.7 The bundle

| ID | Requirement | Authority | Producing cycle | Artifact | Gate | Prerequisites | Failure / downgrade | Status |
|---|---|---|---|---|---|---|---|---|
| Q3-BND-1 | §33.16 public evaluation bundle: reviewed ledger export and commitment chain; protocol commitments/reveals; plan/revision history; model/tool/harness manifests and drift; total search; baseline/ablation protocols and distributions; held-out definitions after evaluation plus access budgets; evaluator/oracle lineage; task-novelty/leakage analysis; capability/claim matrix; maturity classification; independent reviews; known unknowns | §33.16; Charter §5/C7 | C7 | The §33.16 bundle | C7 | Every row above | The bundle is assembled at **day 15**; the Q3 package went to reviewers at **day 9**. Six of the bundle's thirteen contents are not in the C4 package's stated scope | PARTIAL — see F-7 |
| Q3-BND-2 | Reference class and claim expiry declared; historical vs contemporaneous scope never averaged | §33.2, §33.5.2 ("it never averages these scopes"); §10.3 | Day zero (reference class); C4/C7 (expiry) | Claim registry rows | — | Q3-PRV-3 | §35's open row "Alien-artifact reference class" is unresolved. Work Order §4 does not route it to C0 or to a deferred owner cycle | GAP — see F-7 |

---

## 2. Q2 requirement register — forward direction

### 2.1 The measurement instrument

| ID | Requirement | Authority | Producing cycle | Artifact | Gate | Prerequisites | Failure / downgrade | Status |
|---|---|---|---|---|---|---|---|---|
| Q2-INS-1 | Clause tagging live from C1: every consequence contract cites its `SpecCardId`s; the C6 scorer only reads this tagging and never retro-tags | Charter §3 item 8, §5/C1; C-8 in the audit ledger | C1 | Clause-tagged consequence contracts | C1 gate (SpecCard coverage for the R0 surface) | SpecCard pipeline (Q2-INS-2) | Retro-tagging at C6 would make the coverage instrument a post-hoc artifact of the thing it measures. C-8 exists because an earlier draft implied exactly that | OWNED |
| Q2-INS-2 | SpecCard pipeline: ISO 32000-2 + errata license under current ISO AI-use terms; extraction protocol; two-person meaning review; coverage registry; cards run one cycle ahead of implementation | Charter §3 item 5, §8 risk 2; Work Order §5.5; Rev 7 §4, §13.9 | Day zero (human-bound) → continuous | Card registry; per-cycle coverage maps | Card coverage for each cycle's surface gates that cycle's swarm start | **ISO license acquisition — human-bound, legally gated, and on the critical path of every cycle** | No license → no legal semantics channel (§4) → no cards → no clause tagging → no completion denominator → **Q2 has no instrument at all**. This is the longest hard-dependency chain in the campaign | OWNED (human-bound; not yet executed) |
| Q2-INS-3 | Coverage-matrix scorer, built over the clause tagging that has existed since C1 | Charter §5/C6 | C6 | The scorer | C6 gate ("coverage matrix runnable end-to-end") | Q2-INS-1, Q2-INS-2 | Without the scorer there is no matrix; Q2 degrades to the supremacy lanes alone | OWNED |
| Q2-INS-4 | The completion **denominator**: the clause set that "PDF completion" is measured against, and the per-clause atomic fixtures that make a clause observable (§13.9 cards carry "linked atomic fixtures"; §27/G1 produces them) | §24.12 rule 2 (field definition prevents laundering); §24.12 rule 10 (frozen denominators); §13.9; §27/G1 | **none named** | — | — | Q2-INS-2; card coverage **beyond MonkeyBee's own surface**, including clauses MonkeyBee declines under §3.5 | Card coverage is gated per *cycle surface*. A completion denominator spans the standard, including territory MonkeyBee refuses by design. Nothing produces cards or fixtures for the clauses MonkeyBee does not implement — yet those clauses are exactly where a completion comparison is decided | GAP — see F-3 |
| Q2-INS-5 | The **field-side** measurement instrument: a black-box path that scores each eligible field member clause-by-clause under §4.6 (external tools may be driven for success/failure, diagnostics, pixels, text, inventories, output hashes — never read as source) with the §24.15.2 outcome taxonomy | Charter §5/C7 ("run the clause-by-clause coverage matrix across MonkeyBee **and the field**"); §4.6; §24.12 rule 4 | **none named** | — | C3 builds an external-processor divergence harness for four *renderers*; that is a divergence instrument over rendering, not a clause-coverage instrument over the field | Q2-INS-4; frozen field (Q2-FLD-2) | Without it, the "field" side of the matrix can only be filled from competitor documentation — and §24.12 rule 4 is explicit: "Documentation silence is not absence. A failed feature search or missing README claim cannot establish capability absence." A matrix built that way is inadmissible for a field lead | GAP — see F-3 |

### 2.2 The surface to measure

| ID | Requirement | Authority | Producing cycle | Artifact | Gate | Prerequisites | Failure / downgrade | Status |
|---|---|---|---|---|---|---|---|---|
| Q2-SUR-1 | R0–R4 across C1–C6, including the C6 authoring track | Charter §7 Q2 row 2, §4 cycle map | C1–C6 | The five release envelopes (§3.0) | Each cycle's close gate | The whole C1–C6 chain | A surface that stops at R3 can still support atomic lane results, but a *completion* claim over an unfinished surface measures a partial artifact against a whole field | OWNED |

### 2.3 The field (§24.16's three irreversible stages)

| ID | Requirement | Authority | Producing cycle | Artifact | Gate | Prerequisites | Failure / downgrade | Status |
|---|---|---|---|---|---|---|---|---|
| Q2-FLD-1 | **Stage 1** — pre-search discovery commitment: `CompetitorDiscoveryProtocolCommitment` fixing field/capability definitions, eligibility, search surfaces/terms/languages, scouts, cutoff law, nomination/challenge procedure, planned exclusions — committed **before discovery begins** | §24.16 stage 1; §24.12 rule 3; Charter §3 item 3; Work Order §5.3 | Day zero (human-bound) | The committed discovery protocol | Charter §3.3: "windows open immediately" | Substrate (Q3-PRV-2) | §24.16: "If the `FieldDefinitionId` is absent/ambiguous, discovery coverage is incomplete, or its protocol was not prospectively committed, only `named_set_lead` is permitted." Q2 as asked would be unanswerable — a named-set result is not a field lead | OWNED (human-bound) |
| Q2-FLD-2 | **Stage 2** — discovery execution and field freeze: scouts execute the protocol, record deviations, characterize candidates to the required eligibility level, run the nomination/challenge window, and commit a `CompetitorDiscoveryReportId` containing the frozen comparator set | §24.16 stage 2; §24.12 rule 3 | **none named** — the Charter commits the protocol at day 0 and freezes the field at C7, with nothing in between | — | — | Q2-FLD-1; **scouts**, who appear in no Charter roster (§3 item 4 names stewards, red team, reviewers, adjudicators — not scouts) | A field frozen at C7 without an executed, committed discovery report and a run challenge window cannot exceed `named_set_lead`. The challenge window must also have *duration*, which requires the report to exist well before C7 | GAP — see F-4 |
| Q2-FLD-3 | **Stage 3** — pre-measurement `EvaluationProtocolCommitment`, bound to the frozen report, fixing comparator configurations, tuning budgets, corpus, metrics, statistics, stopping, adjudication, claim lifecycle — before any measurement or result inspection | §24.16 stage 3; §24.12 rules 6, 11 | C7 (implied by "under the committed statistical protocol") | The evaluation commitment | C7 | Q2-FLD-2 | §33.4: "one late omnibus document cannot retroactively satisfy all three boundaries." Collapsing stages 1–3 into a single day-zero or single-C7 document voids the field claim | PARTIAL — see F-4 |
| Q2-FLD-4 | An exact versioned `FieldDefinitionId` for the completion field: atomic capability/output contract, openness/channel/license, language/runtime restrictions, platform/jurisdiction, inclusion rules | §24.12 rule 2; §9.2 identity grammar; Charter §0 Q2 | **none named** — Charter §0 asserts "a predeclared, full-field PDF-completion `FieldDefinitionId`"; no cycle authors it | — | — | Q2-INS-4 (a field is only as definable as its denominator) | Rev 7 §24.15 defines lanes S1–S6. **None of them is a completion lane.** §0.2 lists "a clause-by-clause standards coverage matrix" among what the plan has *not* done. The Charter's Q2 therefore names a field that canon has not defined | GAP — see F-3 |
| Q2-FLD-5 | Challenge windows: durations predeclared at day 0, windows open immediately and run concurrent with the build, close on their predeclared schedule at C7 | Charter §3 item 3, §5/C7; §24.16 stage 2 | Day zero → C7 | Window records; nomination dispositions | C7 ("challenge windows close on their predeclared schedule") | Q2-FLD-1; a *published* field for challengers to challenge | A window nobody can see is not a challenge window. Stage 2's absence (F-4) means there is no published comparator set to nominate against for most of the campaign | PARTIAL — see F-4 |
| Q2-FLD-6 | Artifact pinning and symmetric treatment: strongest documented eligible configuration per artifact; equal bounded tuning/integration budget; independent operator where practical; maintainer/vendor challenge opportunity; triage law for non-running integrations (`indeterminate`, never a manufactured win) | §24.12 rules 7, 8; §24.16 | C7 | Comparator artifact records | C7 | Q2-FLD-2 | §24.12 rule 8: "A lab wiring failure is `indeterminate` until triaged; sabotaged defaults or unequal tuning cannot manufacture a lead" | OWNED (via C7's committed protocol) |

### 2.4 The comparison

| ID | Requirement | Authority | Producing cycle | Artifact | Gate | Prerequisites | Failure / downgrade | Status |
|---|---|---|---|---|---|---|---|---|
| Q2-CMP-1 | The clause-by-clause coverage matrix run across MonkeyBee and the frozen field | Charter §5/C7, §7 Q2 row 4 | C7 | The coverage matrix | C7 (Q2 package) | Q2-INS-3, Q2-INS-4, Q2-INS-5, Q2-FLD-2, Q2-FLD-4 | Three of its five prerequisites are GAPs. This is the direct answer path to Q2's headline and it is the least-provisioned requirement in the campaign | PARTIAL — blocked by F-3, F-4 |
| Q2-CMP-2 | Flagship H — the Wild-Tail Ledger (S2): stratified steward-drawn sample after freeze; typed partial/refusal accounting; per-stratum uncertainty; document as the primary analysis unit; published whether MonkeyBee leads or trails | Charter §5/C7; §31.8; §24.15.2 | C7 | The wild-tail ledger | C7 (Q2 package) | C3 wild-tail corpus and gate; steward; external-processor harness | §31.8: "publishable whether MonkeyBee leads or trails." This is the only Q2 lane whose instrument, corpus, and statistical law all exist in the campaign as briefed | OWNED |
| Q2-CMP-3 | Flagship G — Hostile Legacy Execution: admitted AcroForm calculate/format/validate action execution as an atomic field-state transaction; static XFA projection; PostScript-XObject policy; sanitizer/interpreter parity over the shared executable-feature registry | Charter §5/C7 ("Flagships G and H **by name**"); §31.7 | **its capability surface is scheduled by no cycle** | — | C7 is scheduled to *execute* it | Bet 16's metered form-action interpreter (`mb-form`, L5); bounded static-XFA projection (`mb-transform`, L6); `mb-action` executable-feature registry; §17.12 calculator VM (C2) | Rev 7 §3.5 places Bet 16's form-JavaScript subset and static XFA projection **outside R0–R4** — "[M], capability-gated, and non-blocking for every declared release envelope." The Charter builds R0–R4. C7 cannot execute a flagship whose surface no cycle builds | GAP — see F-1 |
| Q2-CMP-4 | "Plus supremacy-lane results" — the S1/S3/S4/S6 lanes named by Q2's own statement and defined in §24.15 | Charter §0 Q2; §24.15 | **none named** — C7 names only Flagships G and H; C6 calls its perf slice "the S6/S1 prerequisite" | — | — | Frozen field per lane; each lane has its own eligible-comparator search | C6 explicitly schedules itself as the prerequisite for lanes that no cycle then executes. This is the §34.4 envelope-dependency pattern — the same class as R2-N1, in the campaign layer this time | GAP — see F-2 |
| Q2-CMP-5 | Predeclared statistics and honest outcome vocabulary: primary analysis unit, pairing/clusters, uncertainty, effect target, multiplicity, stopping/peeking, missingness; no metric laundering; outcomes reported as `leading`/`equivalent`/`non_inferior`/`trailing`/`incomparable`/`indeterminate`/`disqualified` | §24.12 rules 11, 12; §10.3 cl. 29 | C7 | Scorecards | C7 (under the committed protocol) | Q2-FLD-3 | Only an uncertainty-aware `leading` result under the exact declared field scope supports the headline. Everything else keeps its own name | OWNED |
| Q2-CMP-6 | Goodhart guards and held-out guards per lane | §24.15.1, §24.15.2; §28.3 | C7 | Steward samples; held-out sets | C7 | Sealed pools (day zero) | §24.15.1: "never relax thresholds or challenger eligibility after seeing failures" | OWNED |

### 2.5 Credibility and lifecycle

| ID | Requirement | Authority | Producing cycle | Artifact | Gate | Prerequisites | Failure / downgrade | Status |
|---|---|---|---|---|---|---|---|---|
| Q2-CRD-1 | Everything in the Q3 column: the credibility of a Q2 result rests on the same ledger, substrate, independence, and drift discipline | Charter §7 Q2 row 5 | Day zero → C7 | — | — | All of §1 above | Q2 inherits every Q3 gap. Charter §2/G3 already states it: "Q2 verdict (conditional on G2 machinery + R4)" | OWNED (by reference) |
| Q2-CRD-2 | Claim lifecycle after submission: a newly discovered or released material challenger preserves historical reports but **lapses** current-facing registered/observed field leads until characterized; every planning-gate transition and release-claim freeze re-observes the register | §24.16; §24.12 rules 4, 5 | **none named** — the campaign ends at C7 submission | — | — | — | Between day-15 submission and an external verdict of unbounded latency, an unowned register drifts. A lapsed claim that nobody lapses is a false claim | GAP — see F-9 |

---

## 3. Reverse direction — artifact and gate back to requirement

Zero-orphan rule, reverse leg: every artifact the campaign produces and every gate it enforces must support at least one Q2/Q3 requirement, or be justified as G1 (survival-wedge) work that carries no evidentiary burden. G1 work is legitimate and is *not* an orphan — the degradation law (Charter §2) requires precisely that G1 deliverables stand alone.

| Producer | Artifact / gate | Requirements supported | Verdict |
|---|---|---|---|
| Day zero | Production ledger | Q3-PRV-1, Q3-PRV-4, Q3-PRV-5 | Supported |
| Day zero | Commitment substrate | Q3-PRV-2, Q3-PRV-3, Q2-FLD-1, Q2-FLD-3 | Supported — both questions degrade without it (see chain 2, §6) |
| Day zero | Discovery protocols + challenge windows | Q2-FLD-1, Q2-FLD-5 | Supported |
| Day zero | Independence layer | Q3-GRD-1, Q3-IND-1, Q3-IND-2, Q2-CMP-2 (steward) | Supported |
| Day zero | SpecCard pipeline | Q2-INS-1, Q2-INS-2, Q2-INS-3 | Supported |
| Day zero | Corpus program + sealed held-out splits | Q3-SUB-2, Q3-GRD-4, Q2-CMP-2, Q2-CMP-6 | Supported |
| Day zero | License + vulnerability-disclosure policy | G1 (wedge sales, customer trust); R1-6 fix | G1 — no evidentiary burden, correctly so |
| Day zero | Baseline budget reservation | Q3-DIS-1 | Supported |
| Day zero | Clause-tagging declaration | Q2-INS-1 | Supported |
| C1 | R0 wedge (L0–L2, decryption, CLI) | Q3-SUB-1, Q2-SUR-1, **G1** | Supported |
| C1 | Immune system | Q3-DFT-1, Q3-DFT-2, Q3-SUB-6 (raw signal only), Q3-GRD-5 (claim registry mints the lifecycle states; no gate requires the demotion record — F-8) | Supported |
| C1 | Fuzz baseline; zero-reachable-panics gate | Q3-SUB-1, Q3-GRD-2 | Supported |
| C1–C6 | Sealed cycle trial records | Q3-PRV-4, Q3-PRV-5 | Supported |
| C1–C6 | Held-out probe at each close gate | Q3-GRD-4 | Supported |
| C1–C6 | Drift audit at each close gate | Q3-DFT-2 | Supported |
| C2 | Render engine minus real text; D2 receipts | Q3-SUB-1, Q2-SUR-1 | Supported |
| C2 | Benchmark tracking (self-regression) | Q2-SUR-1 (indirectly); C6 perf gate | Supported — **but see the boundary note below** |
| C3 | Text stack, ICC, R1 | Q3-SUB-1, Q2-SUR-1 | Supported |
| C3 | Wild-tail gate over the sealed corpus | Q3-SUB-2, Q2-CMP-2 | Supported |
| C3 | External-processor divergence harness | Q3-GRD-2, Q3-SUB-3 (partly), Q2-CMP-2 (instrument) | Supported |
| C3 | Observatory seed (records + minimized witnesses) | Q3-GRD-2 | Supported |
| C4 | Writer, WASM, release engineering, R2 | Q3-SUB-1, Q3-SUB-3, Q3-SUB-4, Q2-SUR-1 | Supported |
| C4 | Baselines A–D(/E) | Q3-DIS-1 | Supported |
| C4 | Ablations | Q3-DIS-2 | Supported |
| C4 | Evolution Trial (Flagship F) | Q3-DIS-6 — **Lineage-object evidence** (§33.18 cl. 3), plus adaptive-maturity (§33.13) and the campaign's own addendum rehearsal | Supported, object-tagged |
| C4 | Q3 package submission | Q3-IND-2 | Supported |
| C5 | Transforms, redaction, signatures, secure output, agent surface, C ABI preview; R3 | Q3-SUB-1, Q2-SUR-1, **G1 (CDR product)** | Supported |
| C5 | Flagship D with lineage-diverse forensic tools | Q3-GRD-2 | Supported |
| C6 | Track A fidelity + Track B authoring; R4 | Q2-SUR-1, Q3-SUB-1 | Supported |
| C6 | Performance-hardening slice | Declared in Charter §5/C6 as "the S6/S1 prerequisite" — **the lanes it is a prerequisite for are executed by no cycle** | **Reverse orphan** — F-2 |
| C6 | Coverage-matrix scorer | Q2-INS-3 | Supported (its field-side counterpart is missing — F-3) |
| C7 | Field freeze | Q2-FLD-2 (partially), Q2-FLD-6 | Supported |
| C7 | Coverage matrix across MonkeyBee and the field | Q2-CMP-1 | Supported in intent; blocked by F-3/F-4 |
| C7 | Flagship H | Q2-CMP-2 | Supported |
| C7 | Flagship G | Q2-CMP-3 — **its capability surface is built by no cycle** | **Forward orphan** — F-1 |
| C7 | Foundry distribution | Q3-PRV-5 — **Foundry-object evidence** (§33.18 cl. 2) for a rung the campaign does not claim | Supported, object-tagged — F-9 |
| C7 | §33.16 bundle | Q3-BND-1, Q3-DIS-5 (maturity classification is a bundle content with no upstream producer — F-5) | Supported (six contents unsourced — F-7) |
| C7 | Q2 package submission | Q2-CMP-1, Q2-CMP-2, Q2-CMP-3, Q2-CMP-4, Q2-CMP-5, Q2-CMP-6 | Supported |
| All cycles | Ledger entries; not-done list; honest degradation records | Q3-IND-3 | Supported |

**Boundary note on C2 benchmark tracking.** AGENTS rule 9 forbids measurement of or comparison against other PDF libraries before the discovery protocols are committed through the substrate. Charter §5/C2's "benchmark tracking begins here" is therefore **self-regression tracking only** — MonkeyBee against its own prior builds, per §26.2's workload classes. Comparative measurement against external processors (§26.3's baseline lab; lane S6) is a C7 activity under a committed evaluation protocol. A C2 implementer who reads "benchmark tracking" as "start benchmarking against the incumbents" would poison the Q2 evidence chain permanently and irreversibly. The C2 brief states this explicitly.

---

**Reverse-coverage ledger.** All fifty requirement IDs defined in §1 and §2 are accounted for in exactly one of three dispositions, and the accounting is mechanically checkable — every ID is written out in full, so a `grep -oE "Q[23]-[A-Z]{3}-[0-9]+"` over this file reproduces the audit without reading prose:

- **Discharged by a named producer** — the rows above.
- **Discharged by reference** — Q2-CRD-1 alone. Q2's credibility requirement *is* the Q3 column; giving it a separate producer would be circular, and Charter §2/G3 already states the dependency ("Q2 verdict, conditional on G2 machinery + R4").
- **Not discharged** — the fourteen forward orphans in §4, plus the eight `PARTIAL` rows whose producer exists but whose gate does not test it (Q3-SUB-4, Q3-PRV-3, Q3-GRD-5, Q3-DIS-5, Q3-BND-1, Q2-FLD-3, Q2-FLD-5, Q2-CMP-1).

## 4. Orphan audit

**Forward orphans** (a requirement with no producer): Q3-SUB-5, Q3-SUB-6, Q3-SUB-7, Q3-GRD-3, Q3-DIS-3, Q3-DIS-4, Q3-BND-2, Q2-INS-4, Q2-INS-5, Q2-FLD-2, Q2-FLD-4, Q2-CMP-3, Q2-CMP-4, Q2-CRD-2. **Fourteen.**

**Reverse orphans** (an artifact or gate supporting no requirement): the C6 performance-hardening slice, whose stated purpose is to be the prerequisite of lanes S1/S6 that no cycle executes. **One.**

**Not orphans, and deliberately so:** the G1 wedge deliverables (R0 inspection at C1, CDR at C5), the license, and the vulnerability-disclosure policy. Under the graceful-degradation law they carry no evidentiary burden by design — "no G1 deliverable is ever gated on G2/G3 machinery" (Charter §2). Their appearance outside the evidence thread is the law working, not a defect.

---

## 5. Findings

Each finding names the canon that creates the requirement and the grep or derivation that establishes the absence. Dispositions are recommendations to the human and to root; this owner does not edit canonical documents and does not write to the shared dispute channel.

### F-1 — Flagship G's capability surface is scheduled by no cycle · Grade A

Charter §5/C7 schedules C7 to "execute the supremacy lanes — **Flagships G and H by name**." Rev 7 §31.7 defines Flagship G as hostile-legacy execution: admitted AcroForm calculate/format/validate actions executed as atomic field-state transactions, bounded static-XFA projection, PostScript-XObject policy, and sanitizer/interpreter parity over the shared executable-feature registry.

Evidence of absence: `grep -niE "xfa|bet 16|form.action|javascript|postscript|legacy"` over `MONKEYBEE_CAMPAIGN_CHARTER_v1.md` returns **zero** matches. C6 Track A schedules the "AcroForm model and appearance generation" — and `mb-form-appearance` is defined in §30.8 as generating appearances "**without executing unsupported dynamic logic**," which is the opposite of what Flagship G requires. Rev 7 §3.5 is explicit that Bet 16's form-action subset and static XFA projection are "[M], capability-gated, and **non-blocking for every declared release envelope R0–R4**." The Charter's cycle map builds R0–R4 and nothing else.

So C7 is scheduled to execute a flagship whose capability lies outside every envelope the campaign builds. This is a live instance of the §34.4 forbidden pattern — a consequence scheduled without its prerequisite — which is the same bug class as the already-ledgered R2-N1, one layer up.

**Recommended disposition (human):** either (a) add the Bet 16 metered form-action surface and bounded static-XFA projection to a cycle — C6 Track A is the only plausible home, and it would enlarge an already two-track cycle; or (b) strike Flagship G from C7 and record the Q2 claim as resting on the coverage matrix plus Flagship H, with the hostile-legacy conjunction explicitly out of scope. Option (b) costs a lane; option (a) costs cycle capacity on an [M]-tagged moonshot that Rev 7 §P18 forbids putting on the critical path. This matrix recommends (b) and notes that it is a `sequence`/`scope` change under Charter §11.

### F-2 — Supremacy lanes S1, S3, S4, S6 are required by Q2's own statement and executed by no cycle · Grade A

Charter §0 defines Q2 as an uncertainty-aware `leading` outcome on the completion field "**plus supremacy-lane results**." Rev 7 §24.15 defines those lanes: S1 rendering, S2 wild-tail, S3 structured extraction, S4 generation, S5 atomic conjunctions, S6 performance. C7's scope names only Flagships G and H — and Flagship H is S2 (§31.8 draws its input from "the S2 … sample"). S1, S3, S4, S5, and S6 have no producing cycle.

The internal contradiction is sharpest at C6, whose own text calls its performance-hardening slice "**the S6/S1 prerequisite**" — the Charter schedules the prerequisite and omits the consequence. `grep` over the Charter finds `S1` and `S6` **only** in that one line, and `S2`/`S3`/`S4` nowhere at all.

**Recommended disposition (human):** decide which lanes Q2's "plus supremacy-lane results" actually names, and either schedule them into C7's scope with their own comparator searches (each lane requires its own eligible-comparator discovery under §24.15 and §24.16 — this is not free) or narrow Q2's statement in a Charter successor. Note that Rev 7 §35 open decision 1 — "Initial public supremacy claim envelope: S1 rendering field scorecard versus S2 wild-tail ledger; unresolved" — is precisely this decision, and Work Order §4 routes it to **neither** the resolve-now list nor the deferred register. It is unowned.

### F-3 — The Q2 completion field has no denominator, no `FieldDefinitionId`, and no field-side instrument · Grade A

Q2's headline is a `leading` outcome on "a predeclared, full-field PDF-completion `FieldDefinitionId`." Three things that claim requires do not exist in canon:

1. **The lane.** Rev 7 §24.15's lanes are S1–S6. None is a completion lane. §0.2 lists "Completed a clause-by-clause standards coverage matrix" among the things the plan has **not** done. The completion field is a Charter-level construct with no Rev 7 definition behind it.
2. **The denominator.** A completion score needs a clause set and, per §13.9, per-clause atomic fixtures to make each clause observable. SpecCard coverage is gated **per cycle surface** ("Card coverage for each cycle's surface is a gate on that cycle's swarm start"). A completion denominator spans the standard — including the clauses MonkeyBee declines under §3.5. No producer makes cards or fixtures for territory MonkeyBee does not implement, and that territory is exactly where a completion comparison is decided.
3. **The field-side instrument.** C6's scorer is "built over the clause tagging" — MonkeyBee's own contracts citing its own `SpecCardId`s. Scoring a *competitor's* clause coverage requires driving that competitor as a black-box subject over per-clause fixtures (§4.6 permits exactly this and forbids reading its source). C3's divergence harness drives four renderers for rendering divergence; that is not a clause-coverage instrument, and the field is not four renderers.

Without (3), the field column of the coverage matrix can be filled only from competitor documentation — and §24.12 rule 4 forbids that conclusion in one sentence: "**Documentation silence is not absence.**"

**Recommended disposition (human):** treat the completion field as an unresolved design item that must be authored **before** the day-zero discovery commitment freezes (§24.16 stage 1 fixes "field/capability definitions" — a field you cannot define you cannot commit). If it cannot be authored, Q2 narrows honestly to the lane results it can actually earn, and the "full-field PDF-completion" phrasing leaves the Charter.

### F-4 — Discovery stage 2 is unscheduled and unstaffed · Grade B

§24.16 makes field discovery three irreversible stages: commit the protocol before searching; **execute the search, characterize candidates, run the nomination/challenge window, and commit a frozen `CompetitorDiscoveryReportId`**; only then commit the measurement protocol. §33.4 adds: "one late omnibus document cannot retroactively satisfy all three boundaries."

The Charter commits stage 1 at day 0 and freezes the field at C7. Stage 2 — the executed search, the characterization, the challenge window with actual duration, the committed report — is assigned to no cycle. Its executors, the **scouts** named in §24.16 and §33.1, appear nowhere in the Charter: `grep -i scout` returns zero. The independence layer (§3 item 4) rosters stewards, red team, reviewers, and adjudicators.

There is also a sequencing problem inside the Charter's own text: §3 item 3 says challenge windows "open immediately … so no one can later claim they were rigged short." A challenge window is a window for *challengers to nominate systems against a published comparator set*. Until stage 2 publishes one, there is nothing to challenge.

**Recommended disposition (human):** assign scouts (they may be agents; they may not be the same context that authors the measurement), schedule stage-2 execution early enough that the challenge window's predeclared duration elapses before C7, and separate the day-zero commitment (stage 1) from the field freeze (stage 2 close) in the Charter's day map.

### F-5 — Four §33 obligations that constitute the Artifact rung have no producer · Grade B

The Artifact rung is defined at §33.15 as reviewers judging the functioning artifact "a provenance-conditioned extreme outlier in **integrated consequence**." §33 supplies the instruments that make that phrase measurable, and Charter §7's six-row table does not carry them:

| Obligation | Rev 7 | Charter occurrences |
|---|---|---|
| Artifact and operational boundary declaration | §33.3 | zero (`grep -i "artifact boundary"`) |
| Integration-surplus metrics | §33.9 | zero (`grep -i surplus`) |
| Consequence-compression audit | §33.12 | zero (`grep -i compression`) |
| Maturity taxonomy (structural / empirical / adaptive) | §33.13 | zero (`grep -i maturity`) |

§33.12 is not an accessory: it is the test that separates "alien compression" from "accumulation," which is the exact discrimination between the candidate rung and `A1`. §33.11's operational-surplus metrics are named in the Charter only through C4's "release engineering," and no gate tests them.

**Recommended disposition (human):** these are C4-package contents. Either the C4 checkpoint's package manifest expands to carry them (with §33.3's boundary declaration authored at day 0, since it must precede the ledger's classification of construction-time agents), or the Q3 package arrives at independent review missing the instruments its own protocol specifies.

### F-6 — The operational-closure requirement has a producer but no gate · Grade C

Q3-SUB-4 maps to C4's release engineering. C4's gate is "Q3 package submitted." No cycle gate tests clean installation, reproducible builds, quotas, migration, rollback, incident handling, or support burden as §33.11 requires. C6's gate names "PDF/A + PDF/UA validation profiles operational," which is a different sense of the word.

**Recommended disposition:** fold the §33.11 metric set into the C4 and C6 close gates, or accept that operational closure will be self-attested at review time.

### F-7 — Precommitment covers discovery but not evaluation; the §33.16 bundle outruns its sources · Grade B

§33.4 requires a single `EvaluationProtocolId` committed **before unblinding or final measurement**, covering baselines, ablations, held-out commitments and access budgets, model substitutions, evaluator lineage, and the task-novelty / latent-archetype / training-data-exposure / benchmark-owner-conflict analyses. Charter §3 item 3 commits the **discovery** protocols. `grep -i "EvaluationProtocolId"` over the Charter: zero. `grep -iE "novelty|leakage"`: zero.

The C4 package is stated as "baselines, ablations, red-team results, Evolution Trial, ledger-to-date." The §33.16 bundle assembled at C7 additionally requires model/tool/harness manifests and drift, total search, task-novelty/leakage analysis, capability/claim matrix, maturity classification, and known unknowns. Six of thirteen bundle contents have no upstream producer, and the bundle is assembled at day 15 for a package that was submitted at day 9.

Separately, §35's "Alien-artifact reference class" row (§33.2 requires the reference class to be declared) is routed by Work Order §4 to neither the resolve-now list nor the deferred register.

**Recommended disposition (human):** add an `EvaluationProtocolId` commitment to the day-zero checklist alongside the discovery commitment; resolve the reference-class row; reconcile the C4 package manifest with §33.16's contents.

### F-8 — Seeded-defect trials and claim-demotion records are cited as evidence and gated nowhere · Grade B

Charter §7 lists "seeded-defect trials" as a source of Q3's grounding evidence, and §8 risk 7 names them as the mitigation for the F-01 pattern — the failure mode where the entire ecology agrees on a wrong certificate. No cycle gate requires them. §27's G6.1 lane has "mutation/fault-seeding tests" as a standing assurance lane, which is a different thing from a measured detection-rate trial.

§33.10 adds that "a system that never demotes a claim is epistemically suspect." Nothing requires the claim registry's demotions to be *reported* as grounding evidence.

**Recommended disposition:** name the seeded-defect detection-rate trial in the C1 and C4 close gates (C1 to establish the baseline detection rate against the immune system; C4 to report it to reviewers), and require the claim-demotion record in each trial record.

### F-9 — Object hygiene: three evidence classes serve rungs the campaign does not claim, and no one owns the post-submission lapse · Grade C

§33.17 and §33.18 forbid borrowing evidence across the Artifact, Foundry, and Lineage objects. Three Charter artifacts sit on the wrong side of that line unless explicitly tagged:

- The **C7 foundry distribution** is Foundry-object evidence (§33.18 cl. 2). The campaign claims no foundry rung. It should be published as what it is, not read as reinforcing the Artifact rung.
- The **C4 Evolution Trial** is, in §31.6's own words, "the primary lineage test." The campaign claims no lineage rung. It legitimately supports *adaptive maturity* under §33.13 and the campaign's addendum-safety rehearsal; it is not artifact disproportion.
- **Baselines A–D** are Artifact-rung evidence under §33.18 cl. 1 (provenance-conditioned comparison against what the production envelope was expected to produce) — not, as Charter §7's "Production disproportion" phrasing may suggest, a foundry claim.

And §33.2's two vintages: the Charter runs baselines **once**, at C4. §33.2 requires a historical baseline frozen near the program's start **and** a contemporaneous baseline near the public claim date. The verdict lands on the reviewers' calendar at an unbounded remove from day 9 (Charter §8 risk 6 accepts this "by design"). §24.16 says the same for Q2: a newly released material challenger "lapses current-facing registered/observed field leads until characterized." The campaign ends at submission. **No one owns the refresh, and a lapsed claim that nobody lapses is a false claim.**

**Recommended disposition (human):** tag each evidence class with its ladder object in the §33.16 bundle; and either declare both claims explicitly *historical* and dated at submission (cheap, honest, and immediately available) or name a post-campaign owner for the contemporaneous refresh.

---

## 6. Critical prerequisite chains

Two chains carry most of the campaign's risk. Both begin with a human-bound action on day zero and terminate at a question.

**Chain 1 — Q2's instrument.**
ISO 32000-2 + errata license under AI-use terms (human, legal, day 0) → SpecCard extraction protocol + two-person meaning review (human latency; Charter §8 risk 2) → card registry → clause tagging on every consequence contract from C1 → per-cycle card-coverage gates C1–C6 → C6 scorer → **C7 coverage matrix** → Q2.
Every link is blocking. The first link is not obtainable by any agent in this repository. If it does not land, Q2 has no measurement instrument at all — and note that F-3 shows the chain is *also* insufficient even when it lands, because it produces only the MonkeyBee side of the matrix.

**Chain 2 — Q2's field and Q3's precommitment.**
Tamper-evident substrate (human, day 0) → discovery-protocol commitment (§24.16 stage 1) → **[GAP: stage-2 execution, characterization, challenge window, frozen report]** → evaluation-protocol commitment (§24.16 stage 3) → C7 measurement → Q2 field lead.
The same substrate carries §33.4's claim-family precommitment, on which Q3's whole package depends. Without the substrate, §24.16 caps Q2 at `named_set_lead` and §33.4 makes the Q3 package exploratory. One human action gates both questions.

---

## 7. The reality-check question

> **If every cycle completes as briefed, do Q2 and Q3 actually get answered? Why or why not?**

**Q3: yes, conditionally — the answer is reachable, but the package as currently specified is missing instruments its own protocol requires.**

If C1–C4 land as briefed and the day-zero human-bound items are executed, the campaign submits a Q3 package with a functioning R2 artifact, wild-tail evidence, an external-reader matrix, a prospective ledger, sealed trial records, red-team results, drift audits with zero Grade-A findings, equal-resource baselines, ablations, and an Evolution Trial. Independent reviewers can render a verdict on that. The verdict may be `A1`, `A2`, or the candidate rung — and a verdict of `A1` is a real answer to Q3, not a failure of the campaign.

What stops it from being an unqualified yes is F-5: four §33 obligations that *constitute* the Artifact rung — the artifact-boundary declaration (§33.3), integration-surplus metrics (§33.9), the consequence-compression audit (§33.12), and the maturity taxonomy (§33.13) — have no producer in any cycle. The candidate rung asks reviewers to judge the artifact an outlier "in integrated consequence." §33.9 and §33.12 are the instruments that measure integrated consequence and separate compression from accumulation. Submitted without them, the package supports the rungs below the candidate rung and asks reviewers to take the top rung on inspection. That is precisely the move the FrankenSim re-audit in this repository catalogues. These gaps are cheap to close — they are C4-package contents and a day-zero boundary declaration, not new cycles — and closing them is the difference between a Q3 answer and a Q3 answer that can reach its target.

**Q2: no, not as briefed.**

Three independent blockers, any one of which is sufficient:

1. **The field asked about does not exist as a definable object.** Q2's headline is a `leading` outcome on a "full-field PDF-completion `FieldDefinitionId`." Rev 7 defines no completion lane, §0.2 lists the clause-by-clause coverage matrix as not-yet-done, and no cycle authors the denominator — the clause set plus per-clause fixtures — that a completion score would have to be computed over. A `FieldDefinitionId` you cannot define you cannot predeclare, and §24.16 permits no field claim without one (F-3).
2. **The comparison has no field-side instrument.** C6's scorer reads MonkeyBee's own clause tagging. Nothing scores the competitors clause-by-clause, and §24.12 rule 4 forbids inferring their coverage from documentation. The matrix's second column cannot be filled by any means the campaign builds (F-3).
3. **The discovery process skips its middle stage.** §24.16's three commitments are irreversible and ordered. The Charter commits stage 1 at day 0 and freezes at C7 with no scheduled stage-2 execution, no scouts, and a challenge window that opens before there is anything published to challenge. §24.16's own remedy is unambiguous: incomplete or uncommitted discovery caps the result at `named_set_lead` — which is not a field lead, and therefore not an answer to Q2 as asked (F-4).

Add two further reductions that shrink what remains: Flagship G's capability surface is built by no cycle and cannot be executed at C7 (F-1), and the S1/S3/S4/S6 lanes named by Q2's own "plus supremacy-lane results" are scheduled nowhere while C6 declares itself their prerequisite (F-2).

**What Q2 *can* honestly yield if every cycle completes as briefed:** Flagship H — the wild-tail ledger — is fully provisioned. Its corpus is sealed at day 0, its gate runs at C3, its harness exists, its statistical law is written, and §31.8 requires it to be published whether MonkeyBee leads or trails. That is a real, publishable, uncertainty-aware comparative result. It is not "a `leading` outcome on a full-field PDF-completion field."

**The honest summary:** Q3 is answerable and the gaps that stand between the package and its target rung are closable inside the existing cycle structure. Q2, as worded in Charter §0, is not answerable by the campaign as briefed — not because a cycle is expected to fail, but because the question names an instrument, a field, and a set of lanes that no cycle builds. The remedy is not more work at C7; it is a decision, before the day-zero commitments freeze, about what Q2 is actually asking. That decision belongs to the human, and §24.16 makes it irreversible once the discovery protocol is committed: a field definition authored after the search has begun is not a predeclared field.

---

## 8. No-claim boundary

This matrix claims nothing about MonkeyBee's capabilities, no comparative fact about any other system, and no verdict on either question. It asserts only relations between documents that exist in this repository at the date above: where a requirement is written, where its producer is (or is not) written, and what the governing text says happens when the producer is absent.

Absence findings state the file searched, the search vocabulary, and the section that creates the requirement, per AGENTS rule 17. They are falsifiable by exhibiting the missing producer. Every finding grade is this owner's judgment and is subject to fresh-context review; the dispositions are recommendations, and the human ratifies.

Two named inputs remain `SOURCE-UNAVAILABLE` under D-002 (`ALIEN_ARTIFACT.md`, `PROJECT_OVERVIEW.md`). Neither is load-bearing for any row above.

The matrix is `provisional-pending-substrate`: like every other artifact in this repository, it becomes evidence only when the commitment channel exists.
