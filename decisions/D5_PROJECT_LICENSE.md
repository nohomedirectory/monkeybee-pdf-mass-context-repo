---
generated-by: Claude G2 owner (claude-opus-4-8, effort xhigh)
date: 2026-07-14
revised-by: Codex G2 owner
revised-date: 2026-07-16
inputs:
  - CYCLE_0_WORK_ORDER.md §4 resolve-now item 5
  - MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md §3.0, §4.2.1, §4.7, §9.2 (FieldDefinitionId), §15.9, §35
  - MONKEYBEE_CAMPAIGN_CHARTER_v1.md §2 (G1 wedge), §4 (C4 release engineering)
  - AUDIT_FINDINGS_LEDGER.md R1-6
status: PROPOSED
evidence-status: provisional-pending-substrate
decision-id: D5
ratification: PROPOSED — awaiting human ratification
legal-status: ALL LEGAL CHARACTERIZATIONS IN THIS BRIEF ARE [UNVERIFIED] AND REQUIRE COUNSEL
---

# D5 — Project license

## Standing caveat, stated once and meant throughout

**Every legal characterization in this brief is `[UNVERIFIED]` and requires counsel.** G2 is not qualified to give legal advice, Rev 7 §29.9 reserves "legal and clean-room interpretation" to humans, and Rev 7 §35's own row for this decision names "legal review and dependency compatibility" as the evidence needed. What follows is a structured statement of the *engineering and campaign* consequences of each option, so that counsel and the human are deciding with the project's constraints visible — not a legal opinion.

## The question

Under what license is MonkeyBee published?

## Why this resolves at Cycle 0

Rev 7 §35's default is "permissive adoption-oriented license," and the Work Order places this in the resolve-now set because "publication and wedge sales depend on it." Two harder reasons make it genuinely urgent:

1. **The rights-history dependency** (below). Future licensing options can change after outside contributions arrive, but the exact effect depends on the grants and rightsholders and remains a counsel question.
2. **It touches the Q2 measurement.** See the `FieldDefinitionId` coupling below — a non-obvious interaction that a license discussion would normally miss entirely.

## Two couplings that are easy to miss

### Coupling 1 — the license is part of the Q2 comparator field's eligibility boundary

Rev 7 §9.2 defines `FieldDefinitionId` as:

> One versioned canonical eligibility boundary for a comparative field: atomic capability/output contract, **openness/channel/license**, implementation-language/runtime restrictions if any, platform/jurisdiction, and other inclusion rules.

The license is therefore *inside* the definition of the field MonkeyBee will be measured against at C7. This has a consequence nobody would look for in a licensing discussion:

> **The project license and the field's precommitted openness/channel/license rule can be inconsistent.** Whether a particular license qualifies depends on the independently committed field rule; MonkeyBee's own license must not be used to tune that denominator after the fact.

This does not decide the question. It means the license and the day-zero discovery-protocol commitment (Charter §3.3, which is human-bound and being packaged by G5) must be decided coherently. Neither artifact ratifies the other, and neither may be tuned after measurement.

### Coupling 2 — patent exposure is unusually relevant in this domain

Whether any relevant patent exposure remains is `[UNVERIFIED]` and is a counsel question, not one G2 can answer. The narrower structural point is that the candidate licenses contain different express patent terms; counsel must decide whether that difference matters for this project. No current patent, buyer, or adoption fact is established here.

## Options

### Option A — MIT OR Apache-2.0, dual permissive candidate — **recommended**

- **For:** A permissive dual-license candidate aligned with Rev 7 §35's stated direction. Apache-2.0 contains express patent terms; MIT offers a shorter permissive path. Compatibility with GPLv2-only downstreams, dependency licenses, corporate policies, and any particular `FieldDefinitionId` remains `[UNVERIFIED]` and requires counsel plus the actual dependency and field manifests.
- **Against:** No copyleft protection. A competitor may fork, embed, and ship without contributing anything back — including, pointedly, a competitor who takes the clean-room engine and does not inherit the evidence discipline that makes it trustworthy. The license does not itself monetize anything.

### Option B — Apache-2.0 only

- **For:** Single-license administration; express patent terms and NOTICE obligations, subject to counsel's interpretation.
- **Against:** GPLv2-only compatibility and downstream policy effects are `[UNVERIFIED]`; counsel must compare the actual texts and intended distribution paths.

### Option C — MPL-2.0 (file-level weak copyleft)

- **For:** A weak-copyleft candidate whose file-level obligations may fit a human preference for reciprocity while permitting some proprietary combination. Exact obligations are `[UNVERIFIED]` and require counsel.
- **Against:** File-level scope and downstream policy treatment add review questions. Adoption effects are `[UNVERIFIED]`; none is inferred here.

### Option D — AGPL/GPL with a commercial dual license (open-core / sell exceptions)

- **For:** A candidate for a business model that offers separately licensed proprietary use, subject to ownership/grant structure and counsel review.
- **Against:** Contribution rights, network-copyleft scope, dual-licensing authority, adoption effects, and field eligibility are all `[UNVERIFIED]`. This option cannot be selected from engineering inference alone.

## Recommendation

**PROPOSED — awaiting human ratification.**

1. **License: MIT OR Apache-2.0 (dual), subject to counsel and human ratification.** It follows Rev 7 §35's stated permissive direction and exposes an express-patent-term option. No GPL, dependency, buyer, adoption, or field-eligibility result is pre-awarded.

2. **Contribution instrument: choose a DCO, CLA, or other counsel-approved path before accepting outside contributions.** This brief does not establish which instrument grants relicensing authority. If preserving future licensing options is a human requirement, counsel must specify the necessary grant before contributions are accepted.

3. **Separate unresolved item — runtime dependency license policy.** Rev 7 §15.9 requires dependency licensing to fit distribution goals, but the Work Order v1.0 did not route the runtime allowlist or cryptographic-crate rows. `DEFERRED_REGISTER.md` GAP-2 preserves that gap. A candidate allowlist (MIT, Apache-2.0, BSD-2/3-Clause, ISC, Zlib, Unicode-DFS or counsel-approved equivalents) is `[UNVERIFIED]` and is **not ratified through D5**. The human must route the policy separately; each actual dependency still requires review by package role.

4. **Corpus licensing is a separate regime and is not resolved here.** Rev 7 §4.7 governs it, and it is human-bound day-zero work (Charter §3.6, packaged by G5). A permissive *code* license says nothing about whether a corpus item may be redistributed. Recorded so the two are never conflated.

## Reversibility and migration path — rights history makes it path-dependent

**The direction and cost of a later licensing change are `[UNVERIFIED]` until counsel evaluates the actual grants and rightsholders.** Existing releases retain rights already granted under their published terms. Future distributions may use different terms only to the extent the project has authority over all included contributions. Outside contributions can therefore change the option set, but neither "permissive to copyleft is one-way" nor "copyleft to permissive is easy" is safe as a general rule.

The operational consequence is narrower and supportable: before accepting outside contributions, the human should choose a contribution path and have counsel record what rights it does and does not preserve. A DCO, CLA, assignment, or project-license contribution rule must not be described from memory as granting a particular relicensing power. The decision remains human/legal and unresolved until that review exists.

## Rationale

The recommendation follows canon's stated default and surfaces two questions canon's one-line row does not answer: whether express patent terms matter here, and how the project license interacts with the precommitted Q2 field rule. Both require human evidence before ratification.

The contribution-instrument point argues for a decision boundary rather than a specific outcome. G2 has no authority to choose the monetization model or characterize legal grants. It records that accepting contributions before defining the rights path creates avoidable uncertainty.

## Dependencies

- **Consumes:** nothing technical. Ratifiable independently of D1–D4, D6, D7.
- **Consumed by:** the C4 release-engineering slice (packaging, distribution, NOTICE files — Charter §5/C4); the Q2 `FieldDefinitionId` and hence the day-zero discovery-protocol commitment (Charter §3.3); the separately routed dependency-license policy for C1's decoder and crypto dependencies.
- **Coordinates with:** the day-zero discovery-protocol commitment, whose independently fixed openness/channel/license rule must state how MonkeyBee's license is treated. Neither decision silently blocks or ratifies the other.
- **Human-bound:** requires counsel. G5's human-action packages carry the outreach; this brief carries the engineering consequences.

## Evidence still needed before ratification

1. **Counsel review** of the license choice, the patent-grant question in the PDF codec domain, and the DCO-versus-CLA instrument. `[UNVERIFIED]` throughout this brief by construction.
2. **A business decision on monetization model**, followed by counsel's mapping from that model to a project license and contribution-rights path. This brief does not assert that any named instrument is necessary or sufficient.
3. **A dependency license audit** once the C1 dependency set is known (the G6.1 lane already exists to run it).
4. **Confirmation of the GPLv2-compatibility characterization** of Apache-2.0 vs MIT. `[UNVERIFIED]` — it is the load-bearing reason for preferring the dual form over Apache-2.0 alone, and it should be confirmed rather than inherited from convention.

## Blast radius if wrong

| Failure | Consequence | Reversibility |
|---|---|---|
| Contribution rights do not support a later licensing change | A desired future distribution or commercial-license path may require additional permissions, replacement of affected contributions, or abandonment of the change. | Path-dependent and counsel-bound; do not claim irreversibility or ease without the actual grants. |
| Chosen license reduces adoption or contribution | Corpus and compatibility-evidence acquisition may be thinner than planned. | Adoption effect is `[UNVERIFIED]`; later license changes cannot restore elapsed participation. |
| A needed express patent term is absent | Distribution or contribution risk may remain under the intended use. Whether such exposure exists and how it can be remediated are `[UNVERIFIED]`. | Counsel-bound; do not promise that adding another license later repairs prior grants or exposure. |
| License and `FieldDefinitionId` decided incoherently | MonkeyBee may fall outside the committed field rule, or the field rule may appear tuned to MonkeyBee after the fact. The supportable Q2 scope then degrades under the committed protocol. | Before commitment, reconcile the rules. After commitment, any change follows the fresh-identifier and confirmatory-evidence law in §33.4. |

## Human ratification

This brief proposes; it does not decide. Rev 7 §29.9 reserves legal interpretation and product/claim boundaries to humans.

- [ ] **Ratify** MIT OR Apache-2.0 dual, after counsel review (recommended proposal)
- [ ] **Ratify** MPL-2.0 / Apache-2.0-only / copyleft-with-commercial-dual (record which, and the business rationale)
- [ ] **Contribution instrument (before outside contributions):** [ ] DCO  ·  [ ] CLA  ·  [ ] other counsel-approved path; attach the verified rights analysis
- [ ] **Route GAP-2 separately** — runtime dependency license policy and cryptographic-crate selection are not ratified by this brief
- [ ] **Defer** — recording that no outside contribution may be accepted until the contribution-rights path is defined

Ratifier: ______________________ Date: ____________ Counsel consulted: [ ] yes [ ] no
