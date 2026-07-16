---
generated-by: Claude G5 owner (claude-opus-4-8)
date: 2026-07-14
inputs:
  - MONKEYBEE_CAMPAIGN_CHARTER_v1.md §3.3, §4 (C7), §7
  - CYCLE_0_WORK_ORDER.md §5.3, §6
  - MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md §24.12, §24.13, §24.15, §24.16, §33.4, §33.5, §33.6, §33.15
status: DRAFT
evidence-status: provisional-pending-substrate
package-id: P4
human-bound: yes
execution-status: NOT EXECUTED — nothing committed, no search performed, no comparator contacted, no measurement taken
---

# P4 — Discovery-protocol commitment texts

## What this is

Two commitment documents, drafted to be **committed verbatim** through the substrate (P3) on day 0, before anyone searches for anything:

- **DC-1** — the `CompetitorDiscoveryProtocolCommitment`: how the comparator field will be discovered, for which exact field definitions, by whom, with what inclusion criteria, and what will be excluded and why. This is Q2's foundation.
- **DC-2** — the **Q3 claim-family precommitment**: the claim ladder targets, the equal-resource baselines, the ablations, the held-out rules, and the evaluator lineage requirements — committed before the results that could tempt anyone to adjust them.

Placeholders in `[BRACKETS]` are the human's to fill *before* committing. Everything else is ready as written.

## Why a human must do this, and why the ordering is one-way

Rev 7 §24.16 makes field comparison a **three-stage, three-commit** process, and the stages are irreversible:

1. **Pre-search discovery commitment** — fixes definitions, eligibility, search surfaces, scouts, cutoff, challenge procedure, planned exclusions. **Committed before discovery begins.**
2. **Discovery execution and field freeze** — scouts execute, record deviations, run the challenge window, and commit the resulting comparator set as a `CompetitorDiscoveryReportId`.
3. **Pre-measurement evaluation commitment** — binds *that exact frozen report* to the measurement protocol, before any measurement or result inspection.

§33.4 states the consequence directly: *one late omnibus document cannot retroactively satisfy all three boundaries.* And §24.16: if the protocol was not prospectively committed or discovery coverage is incomplete, **only `named_set_lead` is permitted** — the weakest scope, covering exactly the artifacts you happened to name.

So the reason a human must do this is not merely that committing is an external act (though it is, and agents are forbidden it). It is that **the first search anyone runs without the commitment invalidates the prospective pre-search boundary.** No agent in this campaign has run a comparator search, and none may. OVERNIGHT_GOAL §1.4 puts it plainly: premature measurement poisons the Q2 evidence chain permanently.

**Only stage 1 is committed at day 0.** Stages 2 and 3 come later, in that order. This package deliberately does *not* draft the measurement protocol, because drafting it now and committing it later, as one bundle, would be exactly the omnibus laundering §33.4 forbids.

## Prerequisites

- **P3 must exist.** A discovery protocol committed through a channel the project controls is not committed.
- **P5** (challenge-window durations) — DC-1 references them and they are committed together.
- Scouts named (they may be the human, contractors, or the corpus steward — but see the independence note in DC-1 §4).

## Relationship to Rev 7's competitor register

Rev 7 §24.13 contains a dated register of candidate comparators, observed on 2026-07-14. **That register is a prior observation, not the field.** DC-1 treats it as a *characterization pool* — a set of candidates that must each receive an explicit recorded disposition — and nothing more. Rev 7 §24.13 says so itself ("This prose snapshot is not proof of field completeness"), and §24.16 requires S1's first freeze to characterize every known released path rather than assuming a remembered subset exhausts the field.

The distinction matters because the register was assembled partly from model-visible sources; model recall does not establish a field boundary.

---

# DC-1 — Competitor Discovery Protocol Commitment

> **Commit this text verbatim through the substrate before any comparator search is performed.**
> `CompetitorDiscoveryProtocolCommitmentId: [ASSIGNED AT COMMIT TIME]`
> `Committed: [DATE]` · `Substrate: [P3 MECHANISM]` · `Committed by: [NAME]`

## 1. Purpose and binding effect

This protocol fixes how MonkeyBee will discover the comparator field for each field claim named below. It is committed **before any search is executed**. Any material change to it restarts discovery under a new ID (§24.16). Results obtained under an amended protocol are exploratory until fresh discovery is executed.

Claims that cite a discovery report not produced by this protocol, or produced after measurement design began, are capped at `named_set_lead`.

## 2. Field definitions

Each claim binds exactly one `FieldDefinitionId`. Fields are **not** interchangeable, and a result in one field is never described with an adjective borrowed from another (§24.12 rule 2).

| `FieldDefinitionId` | Capability boundary (the exact output contract) | Eligibility |
|---|---|---|
| `pdf_clause_completion.all_open_released.v1` | **The Q2 field.** Coverage of the ISO 32000-2 clause surface, scored clause-by-clause by the predeclared coverage matrix, for the same declared clause set and the same evidence rules | Every eligible open released PDF processor that implements any part of the declared clause surface, regardless of implementation language or runtime |
| `pdf_clause_completion.pure_rust.v1` | As above, nested | Pure-Rust open released implementations only. Reported separately; **never substituted for the all-open result** |
| `pure_rust_native_pdf_to_raster.v1` | S1: PDF bytes → raster, native, under the declared output contract | Pure-Rust open released implementations. PDF-to-SVG paths and rasterizers of a project-owned layout tree are **not** eligible unless a complete pinned PDF-byte-to-raster pipeline is declared and all dependency cost is counted (§24.15.1) |
| `all_open_released_pdf_to_raster.v1` | S1, all-open | Every eligible open released implementation, any language/runtime |
| `all_open_released_wild_pdf_renderer.v1` | S2: the wild-tail ledger, per declared profile | Every material eligible released open renderer, any language/runtime, or its non-dominated set |
| `pure_rust_generator.v1` / `all_open_released_generator.v1` | S4: generation, per atomic version/profile/feature intersection | As named |
| `[S3, S6 fields — declare per lane before their first search]` | Structured extraction; per-workload performance, same end-to-end output contract | Per §24.15.3, §24.15.6 |

**Closed or operationally opaque systems** do not enter the registered-open fields. Where they can be lawfully pinned and measured, they support a separately labeled `observed_field_lead` and are never merged into the open-field result.

## 3. Eligibility criteria (applied uniformly, recorded per candidate)

A candidate is **eligible** for a field if all of the following hold, and each is recorded with its evidence:

1. **Released.** A released artifact exists on or before the cutoff — a published release/tag/registry version, not a main-branch state. Main-branch capability is an early-warning record, never a released baseline (§24.13).
2. **Open**, for the registered-open fields: source and artifact obtainable under terms permitting the measurement described in the bound evaluation protocol.
3. **Pinnable.** Release identity, digest or immutable authority identity, documented production configuration, optional features, and dependency closure can be recorded (§24.12 rule 7). A candidate that cannot be pinned is `indeterminate`, not absent.
4. **Implements the exact output contract** of that field. A crate named "render" does not thereby render; advertisement is not capability (§24.13). Conversely, the labor-intensive rule is that **documentation silence never establishes capability absence** (§24.12 rule 4). A missing README claim is not an exclusion; it is an unfinished characterization.
5. **Not excluded** by a recorded exclusion reason from §5 below.

**Cutoff law.** The cutoff date is `[DATE]`, set at commit time. A known eligible release available by the associated claim freeze cannot be hidden behind an older cutoff (§24.16). A challenger released after the cutoff does not invalidate the historical report but **lapses any current-facing field claim until characterized.**

## 4. Search surfaces, terms, languages, and scouts

**Surfaces** (each searched, each recorded, each with its result — including empty results):

- Package registries: `crates.io`; and the principal registries for every language admitted by the field (`[LIST AT COMMIT TIME — e.g. PyPI, npm, Maven Central, pkg.go.dev, NuGet]`)
- Source forges: GitHub, GitLab, Codeberg, SourceForge, and self-hosted forges reachable by the terms below
- Distribution channels: OS package repositories; commercial vendor catalogues (for the `observed` scope only)
- Standards and industry bodies' member/product listings
- Academic and conference publication venues
- Benchmark entrant lists for any benchmark the campaign enters (with the benchmark-owner conflict recorded — §24.12 rule 10)
- General web search, executed by a named scout, with the query log retained

**Terms:** the term list is fixed at commit time and retained verbatim, including the negative terms. It must include at minimum the capability words themselves (render, rasterize, parse, extract, generate, sign, redact, sanitize, validate, repair, recover) and the format words (PDF, PDF/A, PDF/UA, PDF/X, PDF 2.0, ISO 32000). A search that was never run cannot be reported as having found nothing.

**Languages:** searches are executed in `[LIST — at minimum English, plus at least two others; a field claimed as "all open released" that was searched only in English is a field searched in one language and must say so]`.

**Scouts:** `[NAMES/ROLES]`. Scouts record deviations from this protocol as they occur, not afterwards. **Independence note:** a scout who is also an implementer has an incentive to find a small field. Where the same person must do both, that fact is recorded as a limitation of the discovery report rather than omitted.

## 5. Planned exclusions (declared now, so they cannot be invented later)

The following are excluded by policy, with reasons, and each exclusion is recorded per candidate at freeze time:

| Exclusion | Reason | Scope |
|---|---|---|
| Unreleased / main-branch-only artifacts | Not a released baseline (§24.13) | All fields; recorded as horizon items |
| Artifacts that cannot be lawfully obtained or measured | Measurement impossible | Recorded as `inaccessible`, **not** as absent — inaccessibility is a limitation of the report, not evidence about the artifact |
| Systems not implementing the field's exact output contract | Field definition (§24.15.1) | Per field; recorded with the specific contract element missing |
| Closed/opaque systems, from registered-open fields only | Field definition | They remain eligible for a separately labeled `observed_field_lead` |

**No exclusion of convenience.** A candidate is never dropped because it is inconvenient, because integration failed, or because neither system handles the case. A lab wiring failure is `indeterminate` until triaged (§24.12 rule 8); an unhandled case enters the accounting as `both unsupported` (§24.15.1). Nothing is dropped because nobody likes it.

## 6. Nomination and challenge window

Governed by **P5**, committed with this document. In summary: the window opens on the day this commitment is published and runs for the predeclared duration; any party may nominate a candidate; every nomination receives a recorded disposition; maintainers and vendors of any measured artifact receive a challenge opportunity on configuration and eligibility (§24.12 rule 8).

## 7. Deviation, restart, and honesty rules

- Every deviation from this protocol is recorded when it happens, with its reason.
- A **material** change to field definitions, eligibility, surfaces, or the challenge procedure **restarts discovery** under a new commitment ID (§24.16).
- The discovery report records: surfaces searched, terms, languages, dates, scouts, deviations, nominations, exclusions with reasons, inaccessible systems, and unresolved eligibility.
- `uncontested` is a **dated field-status result of this search**, not a claim of superiority and not proof of global absence (§24.12 rule 13).
- Rev 7's §24.13 register is a characterization pool. Every candidate in it receives an explicit disposition in the discovery report. **Absence from the register is not an exclusion**; the register is known to be incomplete, and its authors said so.

## 8. What this commitment does not do

It does not fix the measurement protocol, the corpus, the metrics, the statistics, the margins, or the comparator configurations. Those are **stage 3** (§24.16), committed after the discovery report is frozen and before any measurement. Drafting them here and committing them in one bundle would be the omnibus laundering that §33.4 exists to forbid.

---

# DC-2 — Q3 Claim-Family Precommitment

> **Commit this text verbatim through the substrate on day 0, alongside DC-1.**
> `EvaluationProtocolId: [ASSIGNED AT COMMIT TIME]`
> `Committed: [DATE]` · `Substrate: [P3 MECHANISM]` · `Committed by: [NAME]`

## 1. The claim families this campaign will and will not attempt

Per the §33.15 ladder, MonkeyBee precommits to seeking, and submitting to independent judgment:

- **Artifact ladder:** the `Artifact-alien candidate` rung — an independently judged verdict, submitted at the Cycle-4 checkpoint. **The repository self-awards nothing** (§33.15).
- **Foundry ladder:** `F1` at most, and only if the baselines in §3 below are actually run at equal resources. If they are not run, **no foundry claim is made at any rung** — not a weaker one, none.
- **Lineage ladder:** **no claim.** The campaign's elapsed evolution is days, and Rev 7 §33.13 forbids relabeling a synthetic evolution trial as empirical operating history. The Evolution Trial (Flagship F) at C4 is precommitted here as an explicitly **synthetic** extension rehearsal, and will be reported as such.

Declaring the lineage abstention now fixes the boundary before any result can influence it.

## 2. Reference class, date, and vintages (§33.2)

- **Reference class:** `[SELECT — Rev 7 §35 default: public expert agent foundries under bounded resources]`.
- **Historical baseline vintage:** frozen at campaign start, `[DATE]` — models, harnesses, tools, and practices as they exist on that date, preserved.
- **Contemporaneous baseline vintage:** run near the public claim date with the strongest comparable then-available systems under the same resource envelope.
- A result may remain historically frontier-revealing while lapsing as a current-frontier claim. These are never averaged (§33.5.2).

## 3. Equal-resource baselines (§33.5) — precommitted, with a budget (P8)

| Baseline | What it is | Committed? |
|---|---|---|
| **A** — Direct frontier agents | Same models, human attention, tools, compute, source pack, task — without MonkeyBee's contracts, Honeycomb, memory, or assurance architecture | `[YES/NO]` |
| **B** — Strong conventional plan + agents | A high-quality ordinary architecture and process, without the claimed central representation/evidence mechanism | `[YES/NO]` |
| **C** — Same repository without foundry memory | Tombstone/session retrieval replaced by the strongest ordinary documentation/search alternative | `[YES/NO]` |
| **D** — Same repository without independent oracles | Independent falsifiers replaced by the strongest ordinary self-testing/review path; the assurance loss is *reported*, not treated as a release failure | `[YES/NO]` |
| **E** — Expert human comparison | Bounded expert implementation or defensible project-history evidence, where feasible | `[YES/NO — "where feasible"]` |

**Fairness law (§33.5.1), committed:** every comparison freezes the same task statement, rights-cleared source pack, repository exposure, model/tool access, compute, elapsed feedback, human attention, attempt/branch budget, stopping rule, and held-out boundary — *except* the mechanism under study. Nominal **and consumed** resources are both reported. No condition gets hidden retries, privileged debugging, extra evaluator feedback, or an easier task. The control receives the strongest practical ordinary alternative, not a strawman. **No condition's author is its sole judge.**

**The consequence of cutting a baseline, precommitted here so it cannot be renegotiated later:** a baseline that is cut is a **formal downgrade of G2**, recorded as such, and the disproportion claim it supported is not made by other means (Charter risk #1). Silence is not an option; the ledger records the cut, its date, and its reason.

**Baselines C and D are repository-level; the §33.6 ablations are mechanism-level. One experiment may not be counted as both** (audit finding R2-N5).

## 4. Ablations (§33.6) — precommitted

Ablate, at minimum: Honeycomb identities/receipts · evidence facets · contracts/source cards · tombstones/memory · independent falsifiers · structured multi-model plan refinement.

Each ablation removes one mechanism and supplies **the strongest ordinary replacement** that preserves the task and usable interfaces — an ablation is an intervention, not a demolition. Migration effort, expected effects, interactions, and stopping rules are predeclared. **Null and negative results are reported.** A mechanism that ablates cleanly with no measured loss is a mechanism the project should stop claiming for.

## 5. Held-out commitments (§28.3, §33.4)

- Held-out splits are **sealed by an independent steward before any implementation exists** (P7, P1 Role A). After code exists, nothing new can become held-out.
- The `EvaluationProtocolId` for each held-out program fixes: who may submit; the submission/query budget and whether failed runs consume it; what aggregate feedback is returned before final freeze; whether per-case diagnostics, labels, or breakdowns are withheld; the steward and evaluator lineage; access logs; the reveal rule; and a reserve replacement set.
- **Committed acknowledgment:** repeated adaptive tuning against a hidden set converts it into development data *even if the bytes were never revealed* (§28.3). If that happens, the set is retired to a regression fixture, the strong claim is withdrawn, and a fresh independently stewarded set is required. This is precommitted now so that it cannot be argued about later, when it will be expensive.

## 6. Evaluator and oracle lineage (§33.7, §33.10)

- The red team runs a **different model family** from the implementation swarm (P1 Role C; audit finding R1-9).
- Shared training data, shared tools, shared benchmark exposure, and shared provider routing are recorded as **correlation, not independent replication**.
- A system that never demotes a claim is epistemically suspect (§33.10). Claim demotions are counted and reported as evidence *in favour* of the grounding claim.

## 7. Known unknowns, committed up front

- Foundation-model pretraining corpora are not inspectable. The project claims a **clean-room development protocol**, not ontological source purity (§4.2.2).
- All agent rounds in the Cycle-0 document run share one model family unless recorded otherwise — a known correlated-blind-spot limitation.
- Work performed before the substrate opened (P3) is labeled **`retrospective`** and cannot support a prospective foundry claim (§33.1).

## 8. Amendment

A material change to this commitment creates a **new** `EvaluationProtocolId` and requires fresh confirmatory data; the changed run is exploratory until then. Post-hoc discoveries are hypotheses until replicated under a new committed protocol (§33.4).

---

## Exact steps (for the human)

1. **Fill every `[BRACKET]`** in DC-1 and DC-2: cutoff date, scouts, languages, registries, reference class, baseline YES/NO, and the challenge-window durations from P5. A committed protocol with an unfilled placeholder is not a commitment.
2. **Decide the baseline commitments explicitly** (§3 of DC-2). This is the budget-sensitive item, and Charter risk #1 says skipping it silently selects FrankenSim's outcome. Decide it with P8 open in front of you.
3. **Commit both documents through P3**, in the day-0 batch, before any search.
4. **Publish the discovery commitment** where nominations can reach it (P5 names the venue). Publication is a human act.
5. **Only then** may scouts begin.

## Expected time

1–2 hours to fill the brackets and ratify, assuming the baseline budget decision (P8) has been made. Minutes to commit.

## Evidence returned to the repo

The committed bytes, their commitment proof, and the assigned IDs — recorded in the ledger and referenced by every subsequent Q2/Q3 artifact. The reveal must later prove *these exact bytes* (§33.4).

## Failure and downgrade path

| Failure | Consequence |
|---|---|
| Committed after a search was run | The pre-search boundary is spent. **Only `named_set_lead` is available** (§24.16). The field claim the campaign exists to make is no longer possible in its strong form |
| Committed with brackets unfilled | Ambiguous field definition ⇒ `named_set_lead` ceiling (§24.16) |
| Baselines not funded | No foundry claim at any rung (DC-2 §1). G2 formally downgraded, recorded, and reported. Q3's artifact claim survives — §33.18: a foundry win cannot substitute for a functioning artifact, and neither can its absence erase one |
| Discovery incomplete at claim time | The claim states its scope honestly: `named_set_lead`, or `registered_open_field_lead` bounded by the exact protocol and window that produced it. Never more |

## Open items requiring human verification

| Item | Status | Verification step |
|---|---|---|
| Cutoff date, scouts, languages, registries | `[BRACKETS]` — unfilled by design | Human fills before commit |
| Reference class (§33.2) | Rev 7 §35 default proposed | Human ratifies |
| Baseline A–E commitments | **The load-bearing decision.** Not made by any agent | Human decides with P8 |
| S3/S6 field definitions | Deferred to their lanes' first search | Declare before that search, never after |
| Whether Rev 7 §24.13's register is complete | It is not, and it says so | Every candidate gets a recorded disposition; absence from it excludes nothing |
