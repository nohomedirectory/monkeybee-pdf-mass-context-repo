---
generated-by: Claude G2 owner (claude-opus-4-8, effort xhigh)
date: 2026-07-14
inputs:
  - CYCLE_0_WORK_ORDER.md §4 resolve-now item 4
  - MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md §10.2.1, §10.10, §33.5, §33.6, §33.15, §35 (checker-isolation row), Appendix A.13, P13
  - AUDIT_FINDINGS_LEDGER.md R1-9, and the F-01 pattern in frankensim_alienartifactness_reaudit.md
  - MONKEYBEE_CAMPAIGN_CHARTER_v1.md §7, §8 (risk 7)
status: PROPOSED
evidence-status: provisional-pending-substrate
decision-id: D4
ratification: PROPOSED — awaiting human ratification
---

# D4 — Evidence-checker isolation

## The question

What exactly makes `mb-checker` independent of the producer, and how is that independence *measured* rather than asserted?

## The finding this decision answers

Rev 7 §35's current default is code isolation:

> Separate `mb-checker` with independently implemented package parser/canonical-root verification; only narrow crypto/schema constants may be shared.

Audit row **R1-9** says that is not enough, and it is the most conceptually important finding in the ledger:

> mb-checker "independence" is intra-ecology; shared premise (the F-01 killer) not countered by shared-code prohibition alone.

The argument is short and it is correct. Two components can share *zero lines of code* and still share a *misunderstanding*. If the same model family, working from the same materials, authors both the producer and the checker, then a wrong reading of the specification produces a producer that emits the wrong thing and a checker that blesses it. The two agree. Both are wrong. Nothing in the codebase is duplicated, and nothing catches it.

This is not hypothetical. It is F-01 in this repository's own cautionary canon: the FrankenSim re-audit documents an entire ecology agreeing on a wrong certificate, and the Charter names it as risk #7 — "the whole ecology can agree on a wrong certificate."

Rev 7 already states the principle, and states it more precisely than the checker's own §35 row does. §10.2.1:

> "**'External' is not synonymous with independent.** Two validators may share the same rule data, parser library, **model family**, corpus, or standards interpretation. […] Reports summarize evidence diversity and known correlation; they do not count ten correlated wrappers as ten independent falsifiers. **Unknown lineage is explicit uncertainty, not assumed independence.**"

That paragraph names *model family* outright as a correlation axis, and P13 makes independent oracles mandatory. The law is already on the books. R1-9's contribution is to notice that the checker, **as specified in §35, does not satisfy Rev 7's own §10.2.1** — the §35 row buys the "parser library" axis and leaves "model family" and "standards interpretation" open. That is not a gap in the principle; it is a gap between the principle and the one component whose independence the Q3 claim rests on.

**So the real question is not "is the checker separate?" but "what is the checker's correlation with the producer, and what is the residual detection rate after that correlation is accounted for?"**

## The axes of independence

Independence is not one property. It is at least five, and they can be bought separately at very different prices.

| # | Axis | What it prevents | Cost |
|---|---|---|---|
| 1 | **Code isolation** — separate crate, independently implemented parser, canonical-root verification, coverage accounting | Shared *implementation* bugs | Low. Already Rev 7's default. |
| 2 | **Authorship isolation** — the checker is authored by a different model family than the producer | Shared *model-family* blind spots and idiom | Low-to-moderate. Mostly a harness/routing decision. |
| 3 | **Specification isolation** — the checker's author receives only the normative spec (SpecCards, package-format protocol) and never the producer's source or its authored rationale prose | Shared *premise* — the F-01 killer. A checker author who reads the producer's rationale inherits its misreading. | Moderate. Requires real discipline about what enters the checker author's context. |
| 4 | **Human adversarial review** — humans, not only models, review the checker against the spec | Correlated failure across *all* model families | High. Human-bound, and slow — Charter risk #2's shape. |
| 5 | **Measured detection rate** — seeded-defect trials quantify what the checker actually catches | Everything above being *asserted rather than true* | Moderate, and it is the only axis that produces evidence. |

Axis 5 is the one that converts this decision from a claim into a lane that emits evidence. It deserves emphasis: **every other axis is an input; only axis 5 is an observation.** A project can do 1–4 perfectly and still not know whether the checker works. A project that does 5 finds out.

## Options

### Option A — Code isolation only (Rev 7's current default)

- Separate crate; independent package parser; only narrow crypto/schema constants shared.
- **Verdict:** necessary, and demonstrably insufficient. This is precisely what R1-9 rejects. It is recorded here so that ratifying anything stronger is a conscious upgrade of Rev 7's default and not an unlogged drift.

### Option B — Code + authorship isolation

- Axes 1–2. The checker is authored by a different model family, with no access to producer source.
- **For:** Cheap; decorrelates model-family idiom and some blind spots.
- **Against:** A different model family reading *the producer's rationale document* still inherits the producer's premise. Authorship isolation without specification isolation leaks the very thing that needs isolating.

### Option C — Code + authorship + specification isolation

- Axes 1–3. The checker author's entire input is the normative specification: the package-format protocol, the canonical-encoding grammar (D2), and the relevant SpecCards. No producer source. No producer rationale. No producer test fixtures.
- **For:** Directly attacks the shared-premise mechanism. This is the strongest *structural* answer available without human cost.
- **Against:** Still an assertion. Nobody has measured whether the resulting checker catches anything.

### Option D — C + measured detection rate + hostile corpus + human adversarial review — **recommended, staged**

- Axes 1–5, with the human-bound axis (4) phased in where it is affordable.

## Recommendation

**PROPOSED — awaiting human ratification. Adopt Option D, staged as follows.**

### C1 floor (mandatory, blocking the C1 close gate)

1. **Code isolation** (axis 1) — as Rev 7 already requires: separate `mb-checker`; its own package parser, structural walk, canonical-root verification, availability/materialization checks, and coverage accounting. Per Appendix A.13, it accepts **raw hostile package bytes** and "never receives a producer-parsed `EvidencePackage` as trusted input."
2. **Authorship isolation** (axis 2) — the checker is authored by a **different model family** than the producer, and the model identities of both are recorded in the production ledger. The campaign already demonstrates this is operationally feasible: this run routes `gpt-5.6-sol` and `claude-opus-4-8` as distinct families and records which produced what.
3. **Specification isolation** (axis 3) — the checker author's context contains the normative package-format specification, the D2 canonical-encoding grammar, and SpecCards. It does **not** contain producer source, producer rationale prose, or producer-authored fixtures. This is a hard constraint on the authoring harness, and it should be enforced by the task's allowed-source manifest (§4.2.2 already provides "task-local allowed-source manifests" as the mechanism).
4. **The seeded-defect detection-rate trial** (axis 5) — the checker's own falsifier, run at **every cycle close gate**, not once. See the trial design below.
5. **Lineage recording** (§10.2.1) — the checker carries an `OracleLineage` record exactly as §10.2.1 requires of any corroborating observation: producer, implementation family, shared dependencies and data where known, protocol author, environment, and adjudication relationship. Its correlation with the producer is recorded as *data*. Per that same section, **"unknown lineage is explicit uncertainty, not assumed independence"** — so an unrecorded axis degrades the claim rather than defaulting to independent. The checker's independence is a measured, disclosed quantity with an honest degradation path, never a badge.

### Scale-up by C4 (the Q3 checkpoint)

6. **Hostile package corpus** authored by the red team (different model family + humans, running continuously from day 0 per Charter §3.4), targeting the checker rather than the engine.
7. **Human adversarial review** (axis 4) of the checker against the specification — at minimum for the canonical-root verification and coverage-accounting paths, which are the two places a subtle blessing-of-garbage bug would hide.

### The one admitted code-sharing exception, and its limit

Only two things may be shared with the producer, and the boundary should be machine-checked, not honoured by convention:

- **The audited cryptographic primitive** (the SHA-256 implementation, D1). Rationale, stated honestly because it cuts against the grain of this brief: reimplementing a hash function is *more* dangerous than sharing an audited one, and a hash implementation bug is detectable by published standard test vectors in a way that a semantic misunderstanding is not. The shared primitive is therefore a controlled risk with an external oracle. If the human prefers, the checker may instead take a *different* audited SHA-256 crate, which strictly dominates and costs little; this is offered as evidence-needed item 4 in D1.
- **Generated schema constants and identity class IDs** — allowlisted, machine-checked, containing no logic.

**What may explicitly NOT be shared: the canonical encoder (D2).** This is the most important line in this brief, and it follows directly from D2's analysis: if the producer and checker share one canonical-encoding implementation, an ambiguity bug in that encoder is *invisible to the checker* — it encodes the attacker's value the same wrong way, computes the same digest, and confirms the claim. The encoder is dual-implemented, and the differential test between the two implementations, over an adversarial encoding corpus, is a C1 acceptance criterion. Sharing the encoder would reintroduce the exact shared-premise failure this decision exists to prevent, at the one place where it does the most damage.

### The seeded-defect trial (this is the evidence-producing part)

Independence becomes a *measurement* by injecting known producer-side defects and recording what the checker catches. Defect classes to seed, at minimum:

- a wrong identity digest;
- a canonical-encoding ambiguity (two distinct values, one encoding);
- truncated or overstated coverage accounting;
- a forged availability class (an `IdentityOnly` artifact presented as materialized — A.13 explicitly requires the checker to distinguish identity verification from evidence availability);
- a stale or incomplete dependency-and-selection manifest (§9.6);
- a replayed or transplanted receipt (right digest, wrong binding);
- an equivocating identity (same ID, different content — §9.2's quarantine trigger);
- a package that is internally consistent but whose root does not bind what it claims to bind.

**A miss is a Grade-A finding.** The detection rate, per class, is recorded in the cycle trial record and travels into the Q3 package as evidence about the checker itself. Note what this buys beyond assurance: §33 asks for grounding that survives attack, and a checker with a *published, measured* detection rate against seeded defects is a far stronger artifact to hand an adjudicator than a checker with an architecture diagram.

## Rationale

Everything above follows from one observation: **the checker is not a test, it is a witness.** Its output is the thing an external adjudicator relies on when deciding whether MonkeyBee's claims are grounded. A witness whose reasoning is correlated with the defendant's is not a witness, and the correlation is invisible from inside the ecology — which is exactly why FrankenSim's ecology never noticed.

The staging reflects cost honestly. Axes 1–3 and 5 are affordable in C1 and are therefore mandatory in C1. Axis 4 is human-bound and slow, so it phases in by C4 where the Q3 package needs it — and if it cannot be obtained, the Charter's graceful-degradation law applies: the claim degrades to its self-attested tier and the miss is logged honestly (Charter §3.4, §8 risk 3). It is not quietly skipped.

## Reversibility and migration path

**Structurally reversible. Evidentially, largely not — this is the least reversible decision in the set, and the reason is worth being precise about.**

A checker can be rewritten at any time; that is easy. What cannot be undone is the *evidence produced under a compromised checker*. If the checker is later found to have shared the producer's premise:

- every receipt it verified must be re-verified by the corrected checker;
- every claim published on the strength of those receipts **lapses** and must be withdrawn or re-grounded — this is precisely the "claim-withdrawal linkage" that audit row R1-6 requires the disclosure policy to define;
- the Q3 package's grounding column (Charter §7: "Grounding that survives attack") is retroactively weakened for every cycle that ran under the compromised checker, because the cycle trial records were sealed with its verdicts inside them.

Sealed cycle trial records are the campaign's foundry evidence (§34.9: "a cycle without a sealed record contributes nothing to any §33 claim"). A sealed record containing a compromised checker's verdicts cannot be quietly amended — amending it is exactly the tamper the substrate exists to detect.

**Therefore this must be right from C1.** Not "right eventually." The cost of getting it right in C1 is a harness routing constraint and a seeded-defect corpus. The cost of getting it wrong is the campaign's central claim.

## Dependencies

- **Consumes:** D1 (the shared crypto primitive is the single admitted sharing exception) and D2 (the canonical encoder is the thing that must *not* be shared, and must be dual-implemented).
- **Consumed by:** every evidence claim in the campaign; the C1 close gate; the Q3 package at C4 (Charter §5/C4).
- **Depends on a harness capability:** the ability to route an authoring task to a *named, verifiable* model family and record which one ran. This run's ledger shows the capability exists and that model identity is verified from process arguments and TUI, not from an alias — that discipline must carry into checker authoring.
- **Interacts with:** §10.2.1 oracle lineage and correlation; Charter risk #7; the red-team window that runs continuously from day 0.

## Evidence still needed before ratification

1. **A written threat model for the checker** — Rev 7 §35's own row demands "threat model, dual-implementation prototype, and adversarial package corpus." None exists yet.
2. **The seeded-defect taxonomy**, expanded and reviewed. The eight classes above are a starting set proposed by G2, not a validated taxonomy; a red-team review should attack the *list* before it attacks the checker.
3. **Confirmation that specification isolation is enforceable in the authoring harness** — that a checker-authoring task can be given an allowed-source manifest that provably excludes producer source and rationale. If it cannot be enforced, say so and downgrade the claim rather than asserting isolation that the harness does not deliver.
4. **A decision on whether the shared SHA-256 primitive becomes a second independent implementation** (see D1, evidence item 4). Cheap; strictly stronger; offered rather than assumed.

## Blast radius if wrong

| Failure | Consequence | Detectability |
|---|---|---|
| Checker shares the producer's premise (the F-01 pattern) | Every "verified" receipt is worthless to an external adjudicator. Q3's grounding column collapses. Worse: **the project does not know**, and continues generating confident evidence on a rotten foundation. | **From inside: near zero.** This is the defining property of the failure — it is invisible to the ecology that contains it. Only axis 5 (seeded defects) or an external party detects it. |
| Checker shares the canonical encoder | An encoding ambiguity is confirmed rather than caught. Manufactured identity equality passes verification with a clean receipt. | Near zero from inside. Hence the dual-implementation law. |
| Checker is independent but never measured | Independence is an assertion. An adjudicator is entitled to discount it entirely, and should. | Detectable, in the sense that the *absence* of a detection-rate number is visible in the Q3 package — to the reviewer, if not to us. |
| Human adversarial review unobtainable | Correlated-blind-spot risk across model families remains. | Known. Handled by the degradation law: log the miss, cap the claim at its self-attested tier, do not pretend. |

## What would change this recommendation

- The harness cannot enforce specification isolation → keep axes 1, 2, 5; **log the axis-3 gap honestly** and cap the independence claim accordingly. Do not describe the checker as premise-isolated when it is not.
- A second model family becomes unavailable → axis 2 fails; the seeded-defect trial (axis 5) becomes the *only* remaining independence evidence, and the claim degrades. This is survivable and must be stated, not hidden.
- The seeded-defect trial shows a high detection rate across all classes → the independence claim strengthens on evidence rather than architecture, which is the outcome this design is aiming for.

## Human ratification

This brief proposes; it does not decide. Rev 7 §29.9 reserves "selection of genuinely independent evidence" to humans — which is, precisely and by name, this decision.

- [ ] **Ratify Option D staged** — C1 floor (axes 1, 2, 3, 5 + lineage recording); scale-up to axis 4 by C4 (recommended)
- [ ] **Ratify Option C** — structural isolation without the measured detection-rate trial
- [ ] **Ratify Option B** or **Option A** (recording that this knowingly leaves audit row R1-9 unaddressed)
- [ ] **Amend** (record the variant and rationale)

Ratifier: ______________________ Date: ____________
