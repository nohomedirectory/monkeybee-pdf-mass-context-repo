---
generated-by: Claude G2 owner (claude-opus-4-8, effort xhigh)
date: 2026-07-14
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

1. **The reversibility asymmetry** (below). This is the one decision in the set that gets *harder* with every day of external contribution.
2. **It touches the Q2 measurement.** See the `FieldDefinitionId` coupling below — a non-obvious interaction that a license discussion would normally miss entirely.

## Two couplings that are easy to miss

### Coupling 1 — the license is part of the Q2 comparator field's eligibility boundary

Rev 7 §9.2 defines `FieldDefinitionId` as:

> One versioned canonical eligibility boundary for a comparative field: atomic capability/output contract, **openness/channel/license**, implementation-language/runtime restrictions if any, platform/jurisdiction, and other inclusion rules.

The license is therefore *inside* the definition of the field MonkeyBee will be measured against at C7. This has a consequence nobody would look for in a licensing discussion:

> **A strongly copyleft MonkeyBee could fail to qualify for a field it defines by openness criteria** — or, worse, could force the field definition to be drawn around MonkeyBee's own license, which is exactly the kind of self-serving denominator that §33.4's pre-search discovery commitment exists to prevent, and that an adjudicator would be right to reject.

This does not decide the question. It means the license and the day-zero discovery-protocol commitment (Charter §3.3, which is human-bound and being packaged by G5) must be decided *coherently*, and the license should be settled first because the discovery protocol has to be committed before the search begins.

### Coupling 2 — patent exposure is unusually relevant in this domain

PDF's codec heritage (JBIG2, JPX/JPEG 2000) and its cryptographic surface carry a patent history. Whether any relevant patents remain in force is `[UNVERIFIED]` and is a counsel question, not one G2 can answer. But the *structural* point stands regardless of the answer: a license with an **explicit patent grant and defensive-termination clause** (Apache-2.0) is worth materially more in this domain than in a typical Rust library, and a bare MIT license grants no patent rights expressly.

## Options

### Option A — MIT OR Apache-2.0, dual (the Rust ecosystem convention) — **recommended**

- **For:** Maximum adoption and zero legal friction for downstream users, whose counsel have already approved this pair a thousand times. The Apache-2.0 arm supplies the express patent grant and defensive termination that this domain warrants (coupling 2). The MIT arm preserves compatibility for GPLv2-only downstreams, which Apache-2.0 alone does not have — this is the actual reason the Rust ecosystem settled on the dual form, and it is a real property, not a convention. Compatible with essentially the entire crate ecosystem, so §15.9's "licensing permits the project's distribution goals" is satisfied with no per-dependency analysis burden. Keeps the G1 wedge sellable (support, hosted service, proprietary integrations) and keeps MonkeyBee eligible under the widest plausible `FieldDefinitionId`.
- **Against:** No copyleft protection. A competitor may fork, embed, and ship without contributing anything back — including, pointedly, a competitor who takes the clean-room engine and does not inherit the evidence discipline that makes it trustworthy. The license does not itself monetize anything.

### Option B — Apache-2.0 only

- **For:** Single license; patent grant; trademark clause; NOTICE requirements give some attribution leverage.
- **Against:** `[UNVERIFIED]` but widely held: Apache-2.0 is incompatible with GPLv2-only downstreams. Gives up the one property the dual form exists to preserve, in exchange for simplicity that few downstream users actually want.

### Option C — MPL-2.0 (file-level weak copyleft)

- **For:** A genuine middle path, and the strongest option if the human wants *any* copyleft. Modifications to MPL'd files must be published, but the code can still be linked into proprietary products — so commercial adoption survives. It protects the specific thing worth protecting here (improvements to the engine) without the adoption collapse of strong copyleft.
- **Against:** Less conventional in Rust; more corporate legal reviews will stall on it than on MIT/Apache-2.0. File-level scope is subtle and is a recurring source of downstream confusion.

### Option D — AGPL/GPL with a commercial dual license (open-core / sell exceptions)

- **For:** The only option that creates a real license-based monetization lever: SaaS and proprietary-embedding users must buy a commercial license. If the business plan depends on license revenue rather than services, this is the mechanism.
- **Against:** Suppresses adoption and ecosystem contribution — and adoption is what generates the wild-tail corpus and the compatibility evidence the campaign depends on. Requires a **CLA with a licensing grant from every contributor** to be able to dual-license at all, which adds contributor friction and legal overhead from the first outside patch. Interacts badly with the `FieldDefinitionId` coupling above.

## Recommendation

**PROPOSED — awaiting human ratification.**

1. **License: MIT OR Apache-2.0 (dual).** It is Rev 7 §35's own default direction ("permissive adoption-oriented"), it supplies the patent grant this domain warrants, it preserves GPLv2-downstream compatibility, it imposes zero dependency-compatibility burden, and it keeps both the G1 wedge and the Q2 field eligibility unencumbered.

2. **Contribution instrument: adopt a DCO (Developer Certificate of Origin) rather than a CLA — *unless* the human wants to preserve the option to relicense later, in which case a CLA must be adopted now.** This is the sharp edge of this brief and it is the reason the decision cannot be deferred; see below.

3. **Rider — runtime dependency license allowlist.** Distinct from the project's own license and worth ratifying alongside it: runtime dependencies are restricted to an allowlist (MIT, Apache-2.0, BSD-2/3-Clause, ISC, Zlib, Unicode-DFS or equivalent), with copyleft runtime dependencies denied by default and admitted only by explicit review. Rev 7 §15.9 already conditions codec dependencies on "licensing permits the project's distribution goals," and G6.1 already runs "dependency advisory, **license**, provenance, and duplicate-version audits." This rider just names the policy the audit enforces. Note the §30.1 package-role distinction: a `lab-tool` or `build-tool` package is not the shipped runtime, and a dependency admissible there is not thereby admissible in `runtime`.

4. **Corpus licensing is a separate regime and is not resolved here.** Rev 7 §4.7 governs it, and it is human-bound day-zero work (Charter §3.6, packaged by G5). A permissive *code* license says nothing about whether a corpus item may be redistributed. Recorded so the two are never conflated.

## Reversibility and migration path — the asymmetry that makes this urgent

**Permissive → copyleft is effectively one-way. Copyleft → permissive is easy.**

- Relicensing *away* from permissive requires the agreement of every copyright holder whose code is in the tree. Once outside contributions land under MIT/Apache-2.0 without a licensing grant, that agreement becomes practically unobtainable — you would have to identify, contact, and get consent from every contributor, or rip out and rewrite their work.
- Relicensing *from* copyleft to permissive is easy for whoever holds the rights, because loosening a license needs no one's permission but the owner's.

Therefore:

> **If there is any chance the human wants license-based monetization or copyleft protection later, the instrument to preserve that option — a CLA with a licensing/relicensing grant — must be adopted on day zero.** Not at C4 when the wedge has customers. Not at C7. The option expires quietly, without an event, the first time an external contribution lands under a bare permissive license.

A DCO (which certifies provenance but grants no relicensing right) is the lower-friction, more community-friendly instrument and is the right default *if* the human is content to stay permissive forever. A CLA is the insurance policy. The decision between them is a business decision, it is genuinely the human's, and its deadline is *now* rather than later — which is exactly the kind of quiet expiry the Charter's change-control clause (§11) exists to prevent for goals, and which nothing currently protects for this.

## Rationale

The recommendation follows canon's stated default and adds the two things canon's one-line row does not surface: the patent grant is worth more here than in a typical Rust project, and the license is silently part of the Q2 field definition. Neither changes the answer; both change what the human is agreeing to, and both should be visible at ratification.

The DCO/CLA point is the one place where this brief argues for urgency rather than a specific outcome. G2 has no view on whether MonkeyBee should monetize by license — that is a business judgment with no technical answer. G2 has a strong view that the *option* should not be lost by inattention.

## Dependencies

- **Consumes:** nothing technical. Ratifiable independently of D1–D4, D6, D7.
- **Consumed by:** the C4 release-engineering slice (packaging, distribution, NOTICE files — Charter §5/C4); the Q2 `FieldDefinitionId` and hence the day-zero discovery-protocol commitment (Charter §3.3); the dependency allowlist that C1's decoder and crypto crates must satisfy.
- **Blocks (softly):** the day-zero discovery-protocol commitment, which should not be committed while the license — an input to the field's eligibility boundary — is unsettled.
- **Human-bound:** requires counsel. G5's human-action packages carry the outreach; this brief carries the engineering consequences.

## Evidence still needed before ratification

1. **Counsel review** of the license choice, the patent-grant question in the PDF codec domain, and the DCO-versus-CLA instrument. `[UNVERIFIED]` throughout this brief by construction.
2. **A business decision on monetization model** — services/support (compatible with A), or license-based (requires C or D, and requires the CLA now).
3. **A dependency license audit** once the C1 dependency set is known (the G6.1 lane already exists to run it).
4. **Confirmation of the GPLv2-compatibility characterization** of Apache-2.0 vs MIT. `[UNVERIFIED]` — it is the load-bearing reason for preferring the dual form over Apache-2.0 alone, and it should be confirmed rather than inherited from convention.

## Blast radius if wrong

| Failure | Consequence | Reversibility |
|---|---|---|
| Permissive chosen; human later wants copyleft or license revenue | The option is gone unless a CLA was adopted on day zero. Recovering it means contacting every contributor or rewriting their work. | **Effectively irreversible.** The core risk of this decision, and the reason the CLA question is raised now. |
| Copyleft chosen; adoption suppressed | Fewer users, thinner wild-tail corpus, weaker compatibility evidence, harder `FieldDefinitionId` eligibility. Relicensing to permissive later is easy, but the lost years of adoption and corpus are not recoverable. | Legally easy; practically costly. |
| Patent exposure unaddressed (bare MIT) | No express patent grant, in a domain with a codec-patent history. Downstream enterprise adoption may stall on it. | Reversible by adding the Apache-2.0 arm later, though downstream users on the old terms keep the old terms. |
| License and `FieldDefinitionId` decided incoherently | The Q2 field is drawn around MonkeyBee's own license, or MonkeyBee fails its own field's openness criterion. Either way an adjudicator discounts the result. | Reversible only *before* the discovery protocol is committed. After commitment, changing the field definition requires a new `EvaluationProtocolId` and fresh confirmatory data (§33.4). |

That last row is the one to watch: it is the only failure here that can contaminate the Q2 evidence chain rather than merely cost money.

## Human ratification

This brief proposes; it does not decide. Rev 7 §29.9 reserves legal interpretation and product/claim boundaries to humans.

- [ ] **Ratify** MIT OR Apache-2.0 dual + dependency allowlist rider (recommended)
- [ ] **Ratify** MPL-2.0 / Apache-2.0-only / copyleft-with-commercial-dual (record which, and the business rationale)
- [ ] **Contribution instrument (decide now, not later):** [ ] DCO — accepting that relicensing later is effectively foreclosed  ·  [ ] CLA with licensing grant — preserving the relicensing option
- [ ] **Defer** — recording explicitly that every day of deferral under an unsettled instrument narrows the CLA option

Ratifier: ______________________ Date: ____________ Counsel consulted: [ ] yes [ ] no
