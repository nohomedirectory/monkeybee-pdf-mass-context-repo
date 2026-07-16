---
generated-by: Claude G5 owner (claude-opus-4-8)
date: 2026-07-14
inputs:
  - MONKEYBEE_CAMPAIGN_CHARTER_v1.md §3.4, §2, §8
  - CYCLE_0_WORK_ORDER.md §5.4
  - AUDIT_FINDINGS_LEDGER.md R1-5, R1-9
  - MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md §28.3, §33.4, §33.5, §33.7, §33.10, §33.15
status: DRAFT
evidence-status: provisional-pending-substrate
package-id: P1
human-bound: yes
execution-status: NOT EXECUTED — nothing sent, no one contacted, no one recruited
---

# P1 — Independence-layer outreach

## What this is

Four role charters and four ready-to-send outreach drafts, for the people whose independence is the load-bearing element of the Q3 (and, downstream, Q2) verdict: a **corpus steward**, a **commitment custodian**, a **red team**, and **external reviewers/adjudicators**.

Audit finding R1-5 is the reason this package exists: the evidence machinery in Rev 7 assumes a human ecology — stewards, scouts, adjudicators, two-person reviewers — that was never provisioned, costed, or given a degradation path. Charter §3.4 answers it with a day-zero engagement track and an honest-logging rule. This package is the executable form of that track.

(The two-person SpecCard *meaning reviewers* are a fifth human role. They are staffed in **P2**, not here, because their qualification is standards competence under a licence, and their independence requirement is different.)

## Why a human must do this

Recruitment is a relationship, not a task. An agent cannot contact a person, make a commitment on the project's behalf, assess a conflict of interest, negotiate compensation, or **supply the required independence from this project's agents.** Rev 7 §29.9 reserves this authority to the human; §33.15 forbids the repository from self-awarding any candidate label.

## Prerequisites

- **P3 (commitment substrate)** should exist first, so that role acceptances, conflict declarations, and the held-out seal can be committed as they arrive rather than reconstructed later.
- A decision on compensation. Independence is cheaper to *claim* than to *have*; unpaid reviewers churn, and churn silently degrades the verdict. Budget is the human's call; the drafts below leave a placeholder rather than inventing a number.
- Nothing else. This package can be dispatched on day 0 with no other campaign artifact finished.

## The four roles

### Role A — Corpus steward (custody + sealing)

**Holds:** the wild-tail corpus, the stratification, and — the part that cannot be delegated to any agent — the **held-out splits, sealed before any implementation exists** (Charter §3.6; Rev 7 §28.3).

**Does:** acquires and stratifies sources per P7; selects held-out splits; computes and commits the seal manifest through the substrate; administers the held-out evaluation protocol (`EvaluationProtocolId`: who may submit, how many submissions, what feedback is returned, reveal and replacement rules); keeps access logs; performs the one derivation step agents may never perform — deriving rights-cleared canonical fixtures from public conformance suites whose surrounding repositories are prohibited clean-room sources (Rev 7 §24.15.1 denominator rule, §4.1).

**Independence requirements:** not a MonkeyBee implementer; no access to implementation prompts or repositories beyond what the protocol grants; compensation not contingent on any result; able to refuse a submission and to record a failed probe.

**Failure mode this role prevents:** held-out sets that quietly become development data (Rev 7 §28.3 — "repeated adaptive tuning against a hidden set makes it development data even if bytes were never revealed"). Without a steward, *every* strong held-out claim in the campaign collapses to self-attested.

### Role B — Commitment custodian

**Holds:** the protocol commitments — Charter hash, discovery protocols, evaluation protocols, seal manifests — under independent custody, so that a reveal proves the exact committed bytes (Rev 7 §33.4).

**Does:** receives each commitment root, records receipt independently of the project's own infrastructure, and can later attest that the bytes revealed are the bytes committed, on a date the project did not control.

**Independence requirements:** no financial interest in the outcome; not the author of any committed protocol; distinct from the corpus steward where possible (splitting custody from sealing removes a single point of both failure and suspicion).

**Note on scope:** if P3 is executed with a witnessed append-only log (timestamping plus a public transparency log), the custodian's role narrows to attestation of the *reveal* rather than custody of the *bytes*. Both mechanisms are permitted by Rev 7 §33.4; a defense-in-depth configuration uses both so the mechanism and the custodian provide distinct records.

### Role C — Red team

**Does:** attacks the artifact, the evidence, and the claims — continuously from day 0, **not** as a Cycle-4 event (Charter §3.4). Seeded-defect trials; independent falsifiers; attempts to make the immune system certify something false.

**Independence requirements — the sharp one:** *a different model family* from the implementation swarm, plus humans. Audit finding R1-9 and Rev 7 §33.7 are explicit that shared training, tools, and provider routing are **correlation, not independent replication**. The F-01 pattern (Charter risk #7) is an entire ecology agreeing on a wrong certificate; a red team drawn from the same model family reproduces that failure at higher cost and with a false sense of coverage.

**What the red team must be able to do:** publish an adverse finding that the project cannot suppress, and be paid the same either way.

### Role D — External reviewers / adjudicators

**Does:** receives the Q3 package at the Cycle-4 checkpoint (~day 9) and the Q2 package at C7 (~day 15), and renders a verdict on their own calendar. Rev 7 §33.15: the repository self-awards none of the candidate labels. Charter §8 risk #6 accepts verdict latency as a design property, not a defect — the value of the verdict comes precisely from not controlling it.

**Independence requirements:** no participation in construction; no financial interest; disclosed conflicts; competence in at least one of (a) PDF/document-format engineering, (b) software-assurance methodology, (c) evaluation/measurement design. A panel drawn from all three covers more distinct competence areas than three reviewers from one.

**Adjudicator vs reviewer:** an adjudicator additionally rules on contested comparator outcomes (Rev 7 §24.12 rule 12 — `incomparable` and `indeterminate` are real outcomes, and someone who is not the maker must be able to declare them).

## Exact steps

1. **Decide compensation and disclosure posture** (30 min). Two questions only: is there a budget per role, and may reviewers publish their findings independently of the project? Recommended: yes and yes. A reviewer who cannot publish adversely is a consultant.
2. **Build the candidate list** (60–90 min). For each role, name 3–5 candidates. Screen each against the independence criteria above *before* contacting them; a conflict discovered after acceptance is expensive to unwind.
3. **Send the four drafts below**, one per role, personalized. Do not batch-send; these are individual asks.
4. **Record every dispatch and every reply — including refusals and silences — in `OUTREACH_TRACKER.md`.** Charter §3.4: what cannot be obtained is logged honestly, and the affected claim degrades to its self-attested tier. The tracker is the evidence that the degradation was honest rather than convenient.
5. **On acceptance**, capture: the signed role charter, the conflict-of-interest declaration, the model family and version (Role C), and the date — and commit each through the substrate (P3).
6. **After 10 business days**, convert every non-reply to a recorded miss and re-dispatch or degrade. Do not leave a role "pending" indefinitely; an indefinitely-pending steward is an unsealed corpus.

## Expected time

Human: 2–4 hours to dispatch all four roles. Calendar: **weeks**, and this is the campaign's binding constraint on Q3. Charter §8 risk #3 (independence-layer non-materialization) is mitigated only by starting on day 0 and logging honestly, never by waiting.

## Evidence returned to the repo

- `OUTREACH_TRACKER.md` — one row per candidate per role: dispatched, replied, accepted, declined, silent, conflicted.
- Signed role charters and conflict declarations (stored under the human's control; their hashes committed through P3).
- For Role C: the exact model family, version, and harness, recorded before the first attack — because a red team's lineage is itself evidence (Rev 7 §33.7).

## Failure and downgrade path

| Role not obtained | Immediate consequence | Claim degradation (honest, recorded — never silent) |
|---|---|---|
| A — corpus steward | No sealed held-out splits; the C3 wild-tail gate has no independently stewarded sample | Every held-out and wild-tail claim degrades to self-attested. S2 cannot be published as a stewarded ledger. Q3's "grounding that survives attack" row loses its independently stewarded held-out input |
| B — commitment custodian | Commitments rest on the timestamping/log mechanism alone | Q3 provenance degrades from independently-custodied to witnessed-log-only. Acceptable if P3's log configuration is in place; **not** acceptable if the only artifact is a git commit (Charter §10 — git alone is decoration) |
| C — red team | No adversarial grounding from outside the ecology | "Grounding that survives attack" (Charter §7) has no evidence. The F-01 failure mode is unmitigated. Q3 artifact claims cap below `Artifact-alien candidate`, which requires independent judgment |
| D — reviewers/adjudicators | **No Q3 verdict exists at all** | G2 is dropped under the graceful-degradation law (Charter §2). The campaign terminates as G1 — a shipped, evidenced, sellable product — with no stranded work. This is a designed outcome, not a failure |

The graceful-degradation law is what makes this table safe to publish: **no G1 deliverable is gated on any row of it.**

## Ready-to-send drafts

Placeholders in `[BRACKETS]` are the human's to fill. Nothing below has been sent.

### Draft A — Corpus steward

```
Subject: Independent corpus steward for a PDF-engine evaluation (paid, ~[N] h/month)

Hello [NAME],

I'm building MonkeyBee, a clean-room PDF engine in Rust. I want its claims to
be checkable by someone who has no stake in them being true, which requires
people who are independent of the project by construction.

I'd like to ask you to be the corpus steward.

Concretely, you would: acquire and stratify a wild-tail PDF corpus from public
sources; select the held-out evaluation splits; and seal them **before any
implementation code exists** — which is the point, because after code exists,
nothing new can honestly become held-out. You would then administer access to
those splits: how many submissions the project gets, what feedback comes back,
when they are revealed, and what replaces them.

The one thing I cannot do myself, and cannot let an AI agent do, is hold the
evaluation set I am being measured against. That is the whole role.

Requirements are independence, not availability: you would not be an
implementer, your compensation would not depend on any result, and you would
be free to record a failed probe or refuse a submission. Estimated commitment:
[N] hours/month for [DURATION]. Compensation: [AMOUNT/TERMS].

If you're interested, I'll send the steward charter (roughly two pages: custody,
sealing procedure, submission budgets, reveal rules) before you commit to
anything.

Either way, thank you for reading.

[NAME]
[CONTACT]
```

### Draft B — Commitment custodian

```
Subject: Independent commitment custodian — small, occasional, consequential

Hello [NAME],

I'm running a build-and-evaluate campaign on a Rust PDF engine (MonkeyBee)
where the central discipline is that every claim is precommitted before the
measurement that could confirm it. Protocols, comparator-discovery methods,
and held-out corpus seals all get committed up front, and revealed afterwards.

For that to be worth anything, someone who isn't me has to hold the
commitments, so that when the bytes are revealed later, a third party can say:
those are the bytes, and that was the date.

The ask is small and occasional: receive a commitment root (a hash, plus a
sealed copy where appropriate), record it independently of my infrastructure,
and later attest that what was revealed matches what was committed. Perhaps
[N] events over [DURATION], minutes each.

What makes it valuable is exactly what makes it unautomatable: you have no
financial interest in the outcome, you did not author the protocols, and the
dates are not mine to control.

The human-ratified timestamping/log mechanism will run alongside you. Its
proof and your independently recorded receipt/reveal provide distinct records.

Compensation: [AMOUNT/TERMS]. Happy to send the one-page custodian charter.

[NAME]
[CONTACT]
```

### Draft C — Red team

```
Subject: Red team engagement — break a PDF engine's *evidence*, not just its parser (paid)

Hello [NAME/TEAM],

I'm looking for a red team for MonkeyBee, a clean-room memory-safe PDF engine
in Rust. The engagement runs continuously from day zero rather than as a
pre-release event, and the target is unusual, so I'll be precise about it.

The parser is a target, of course: hostile files, resource exhaustion,
recovery ambiguity, decryption edge cases. But the *primary* target is the
evidence machinery. The project generates claims about what it did and did not
prove, and checks them with its own machinery. I want you to make that
machinery certify something false. If a whole ecology of agents can agree on a
wrong certificate — and I have watched it happen in a predecessor project —
then everything downstream is theatre.

There is a hard requirement I want to state up front: **you must not be running
the same model family as the implementation swarm.** Shared training data and
shared tooling produce correlated blind spots, and a red team with the same
blind spots as the builder is a very expensive way to feel safe. Humans in the
loop, plus a different model family, is the requirement.

Terms: you publish what you find, including if what you find is embarrassing;
compensation does not depend on what you find; seeded-defect trials are part of
the scope (I want your detection rate measured, not asserted).

Scope, cadence, and rate: [TERMS]. Interested?

[NAME]
[CONTACT]
```

### Draft D — External reviewer / adjudicator

```
Subject: Independent reviewer for an agent-built PDF engine's evidence package

Hello [NAME],

I'd like to ask you to serve as an independent reviewer on a project whose
central premise is that it doesn't get to grade itself.

MonkeyBee is a clean-room PDF engine in Rust, built by an instrumented
multi-agent process. Two questions are precommitted, and the project is
forbidden from answering either one itself:

  1. Is the artifact an extreme outlier in integrated consequence, given a
     bounded and authenticated record of exactly what produced it?
  2. On a predeclared measurement of PDF specification coverage, against a
     comparator field frozen by a discovery protocol committed before the
     search, where does it actually land?

Your role: receive the evidence package — production ledger, protocol
commitments and reveals, equal-resource baselines, ablations, red-team results,
held-out probes, known unknowns — and render a verdict on your own calendar.
Not mine. The project's timeline stops at submission by design.

Requirements: no participation in construction, no financial interest,
disclosed conflicts, and freedom to conclude "underdetermined," "no," or
"this evidence doesn't support that claim." Those are real outcomes here, and
the protocol has names for them.

Estimated: [N] hours at the first checkpoint (~[DATE]), [N] at the second.
Compensation: [AMOUNT/TERMS], not contingent on the verdict.

If it's useful, I can send the evaluation protocol in advance — it is
precommitted, so you would be reading the same bytes the adjudication will
later be checked against.

[NAME]
[CONTACT]
```

## Open items requiring human verification

| Item | Status | Verification step |
|---|---|---|
| Compensation levels for each role | Not set — deliberately left blank | Human decision; record in the ledger as a committed line item alongside P8 |
| Candidate names | **None proposed.** No agent has contacted, screened, or shortlisted anyone | Human builds the list; agents may not |
| Red-team model family availability | `[UNVERIFIED]` | Confirm at engagement; record exact family, version, harness before the first attack (Rev 7 §33.7) |
