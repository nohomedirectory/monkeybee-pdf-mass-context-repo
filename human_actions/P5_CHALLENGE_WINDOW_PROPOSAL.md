---
generated-by: Claude G5 owner (claude-opus-4-8)
date: 2026-07-14
inputs:
  - MONKEYBEE_CAMPAIGN_CHARTER_v1.md §3.3, §4 (C7), §9, §11
  - CYCLE_0_WORK_ORDER.md §5.3
  - MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md §24.12, §24.15, §24.16
status: DRAFT
evidence-status: provisional-pending-substrate
package-id: P5
human-bound: yes
execution-status: NOT EXECUTED — no window opened, nothing published, no nomination solicited
---

# P5 — Challenge-window proposal

## What this is

A proposed set of **predeclared challenge-window durations**, with justification, to be committed verbatim alongside DC-1 (P4) on day 0.

Charter §3.3 requires the durations be predeclared *now* and the windows open *immediately*, running concurrent with the build — "so no one can later claim they were rigged short." That requirement is sound and this package honours it. It also surfaces a conflict between the window durations that requirement implies and the Charter's own 15-day timeline. **The conflict is real, it is not resolvable by drafting, and it is stated here rather than smoothed over.**

## Why a human must do this

Opening a window is publication: the commitment text has to reach the people who might nominate a challenger, or the window is a window nobody can see through. Publication is an external action, forbidden to every agent in this campaign. Choosing the duration is a judgment about credibility that trades directly against the campaign's schedule, and that trade is the human's to make (Rev 7 §29.9).

## What a challenge window is for

Two distinct jobs, often conflated:

1. **Nomination.** Third parties propose comparators the scouts missed. This is what converts "we searched and found these" into "we searched, published our method, and invited the world to tell us what we missed." Without it, discovery coverage rests entirely on the searchers' diligence — and the searchers work for the claimant.
2. **Maintainer/vendor challenge.** The people who built a measured artifact get to contest its *configuration* and *eligibility* before the result is published (§24.12 rule 8). This is the mechanism that prevents a lead manufactured out of a competitor's badly-wired defaults, which is the most common way honest people produce dishonest benchmarks.

A window that is open but unannounced does neither job.

## Proposal — `PROPOSED, awaiting human ratification`

| Window | Proposed duration | Opens | Closes |
|---|---|---|---|
| **W1 — Initial nomination window** | **21 days** | The day DC-1 is committed and published (day 0) | Day 21. Gates the *first* discovery-report freeze |
| **W2 — Standing nomination window** | **Continuous** | Day 0 | Never closes while any current-facing field claim stands. Nominations after W1 do not reopen a frozen historical report; they lapse *current-facing* claims until characterized (§24.16) |
| **W3 — Maintainer/vendor challenge** | **30 days** from notification, per measured artifact | When a maintainer is notified their artifact is in a comparator set | Before the result binding that artifact is published |
| **W4 — Pre-publication challenge on the discovery report** | **14 days** | When the frozen `CompetitorDiscoveryReportId` is published | Before the measurement protocol (stage 3) is committed against it |

**Minimum floor, committed:** no field claim is published on a discovery report whose nomination window ran **less than 21 days**, and no comparator result is published against a maintainer who had **less than 30 days** to contest configuration. These floors are precommitted so that a schedule crunch cannot later shorten them — which is the exact abuse Charter §3.3 anticipates.

### Why 21 days for nomination

Short enough to fit a fast campaign; long enough that a maintainer who reads a mailing list weekly, or a researcher on holiday for a fortnight, still has a real chance to respond. Below about two weeks, the window is decorative: it excludes anyone not already watching, which is precisely the population whose challengers the scouts most likely missed. Above roughly a month, the marginal nomination rate does not plausibly justify the schedule cost — this is a judgment, not a measurement, and it is offered as one.

### Why 30 days for maintainer challenge

A vendor or maintainer must be able to reply, reproduce the harness, and object to a configuration — and unlike the project, they have no stake in the campaign's timeline and no reason to prioritize it. Thirty days is the shortest interval that is not effectively a demand for immediate compliance.

### Why W2 never closes

§24.16 is unambiguous: a newly discovered or released material challenger **preserves historical reports but lapses current-facing registered/observed field leads until characterized.** A field claim is a perishable good. Declaring W2 permanent at day 0 means the project never has to decide, later and inconveniently, whether to notice a challenger it would rather not have noticed.

---

## The conflict this package must not hide

**Charter §4 schedules the Q2 package at C7, ~day 15, with "challenge windows close on their predeclared schedule."** A 21-day nomination window opened on day 0 **has not closed by day 15.**

This is not a drafting error to be papered over by shortening the window. Shortening it to fit the calendar is precisely what §24.16 and Charter §3.3 exist to prevent, and a 14-day window chosen because the campaign is 15 days long would be a window whose duration was set by the claimant's convenience — the definition of rigged-short.

**Three honest resolutions. The human picks one.**

| Option | What happens at day 15 | Cost | Assessment |
|---|---|---|---|
| **A. Submit at day 15 with scope capped** | The Q2 package is submitted on schedule, but every field result is stated as **`named_set_lead`** (and equivalence/non-inferiority gate results, which do not depend on field completeness). The `registered_open_field_lead` upgrade is submitted as an **addendum** when W1 and W4 have closed and the report is frozen | The strongest Q2 claim arrives ~2–4 weeks after the campaign "ends" | **Recommended.** It preserves the campaign's tempo *and* the claim's integrity, and it is honest at every moment. The campaign was always going to wait on external calendars for the *verdict* (Charter §8 risk #6); waiting on one for the *field freeze* is the same kind of patience |
| **B. Extend C7 until the windows close** | Q2 submission moves to ~day 30–35 | The 15-day headline goes | Perfectly legitimate. Charter §9's tempo-independence rule already says the structure is identical whether the campaign takes two weeks or six. Choose this if the day-15 date matters to nobody |
| **C. Shorten the windows to fit day 15** | Q2 submits on schedule with a "closed" window | **The field claim's credibility** | **Not recommended, and arguably not permitted.** It converts the challenge window into theatre, and an adjudicator who notices — and this is exactly what an adjudicator is for — will discount the field claim entirely. Charter §3.3's own words condemn it |

**A note on why this was worth surfacing rather than resolving quietly:** the campaign's premise is that its claims carry their own reasons for trust. A window sized to the schedule instead of to the challengers is a small, plausible, easily-defended decision that would quietly void the strongest thing Q2 could say. It is the kind of decision the FrankenSim re-audit in this repository catalogues.

### Proposed dispute entry (for the orchestrator to file — G5 does not own `DISPUTES.md`)

`D-006` is proposed on the basis that `D-004` and `D-005` were taken by G2 at 16:43 (`ledger/RUN_LEDGER.md`). **The orchestrator assigns the final ID**; the text below is the finding, not the numbering.

```
## D-006 — Challenge-window duration versus the day-15 Q2 submission

- conflict: Charter §3.3 requires predeclared challenge windows that open at day 0 and
  cannot be "claimed rigged short"; Charter §4 schedules the Q2 package at ~day 15 with
  windows closed. Any window credible enough to satisfy §3.3 (P5 proposes 21 days
  nomination, 30 days maintainer challenge) is still open on day 15.
- evidence: Rev 7 §24.16 — `registered_open_field_lead` requires the challenge window to
  have run; incomplete or uncommitted discovery cannot exceed `named_set_lead` scope.
- proposed resolution: Option A (P5) — submit at day 15 with field results capped at
  `named_set_lead`; upgrade to `registered_open_field_lead` by addendum after the windows
  close and the discovery report is frozen. Shortening the windows to fit the schedule is
  rejected.
- status: PROPOSED — awaiting human ratification. Affects Charter §4 (C7 gate wording) and
  may warrant a Charter v1.1 `sequence`-class amendment under §11.
```

---

## Exact steps

1. **Ratify the durations** (or amend them) — 30 minutes with P4 open.
2. **Resolve the day-15 conflict** by picking A, B, or C above. Record the choice, its rationale, and its date; if it changes a Charter gate, it is a `sequence`-class change-control entry under Charter §11.
3. **Commit the durations verbatim** with DC-1, in the day-0 batch (P3).
4. **Publish the nomination invitation** — the draft below — wherever the relevant maintainers actually are. `[VENUE — the human's call; the point is that people who might nominate a challenger can see it.]` Publication is a human act, and no agent may perform it.
5. **Log every nomination and its disposition**, including the ones the project would rather not have received. A nomination log with no rejected nominations is a log nobody used.

## Expected time

30–60 minutes to ratify. Minutes to commit. The windows then run on their own clock, which is the entire point of them.

## Evidence returned to the repo

The committed durations; the publication record (where, when); and the nomination log with a disposition for every entry.

## Failure and downgrade path

| Failure | Consequence |
|---|---|
| Window opened but never published | It did not happen. Discovery coverage rests on the scouts alone, and the report must say so |
| Window shortened after a challenger appears | Fatal to the field claim. §24.16: eligibility may not be relaxed or tightened after seeing results |
| A material challenger is discovered after freeze | **Not a failure — the designed behaviour.** The historical report stands; current-facing field claims lapse until the challenger is characterized (§24.16). Say so in public, on the day it happens |
| No nominations at all | A real, publishable result: `uncontested` — a *dated field-status result of this search*, and not superiority, not proof of absence (§24.12 rule 13) |

## Ready-to-send draft — nomination invitation

```
Subject: Open call — nominate a PDF implementation for a comparator field (window closes [DATE])

We are running a measurement of PDF specification coverage and rendering/generation
behaviour across the open field, and we have committed the discovery protocol before
running the search, so that the field we measure is not the field we happened to
remember.

The commitment is published at [LINK], with its timestamp proof. It fixes the field
definitions, the eligibility criteria, the search surfaces and terms, and the
exclusions — all before any searching.

Two asks:

1. **Nominate anything we will miss.** If you maintain, use, or know of a PDF
   implementation eligible for any field defined in the protocol, tell us. Our search
   will be imperfect; "documentation silence" is not evidence of absence, and we would
   rather be corrected now than be right-sounding later. The nomination window closes
   [DATE, ≥21 days out]. Every nomination receives a recorded disposition, published
   with the report.

2. **If your project ends up in a comparator set, you get to argue with us about it.**
   Before any result involving your artifact is published, you will be notified and
   have 30 days to contest its configuration and eligibility. We want your strongest
   documented production configuration, not the one we guessed. A benchmark that
   measures a competitor's badly-wired defaults measures nothing.

Nominations and challenges: [CONTACT].

[NAME], [PROJECT]
```

## Open items requiring human verification

| Item | Status | Verification step |
|---|---|---|
| The day-15 conflict | **Unresolved; three options above** | Human picks. Option A recommended. This is the item to read first in this package |
| Publication venue | `[VENUE]` — not selected | Human's call. It must be somewhere the relevant maintainers actually look |
| Durations (21/30/14 days) | Proposed, with reasoning given as judgment | Human ratifies or amends. They are not measurements and are not presented as any |
