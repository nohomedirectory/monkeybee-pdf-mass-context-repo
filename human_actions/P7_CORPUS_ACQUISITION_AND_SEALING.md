---
generated-by: Claude G5 owner (claude-opus-4-8)
date: 2026-07-14
inputs:
  - MONKEYBEE_CAMPAIGN_CHARTER_v1.md §3.6, §5 (C3 gate)
  - CYCLE_0_WORK_ORDER.md §5.6
  - MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md §4.1, §4.7, §24.15.1, §24.15.2, §28.1–28.4, §33.4
  - ledger/RUN_LEDGER.md fetch record (root-verified corpus URLs)
status: DRAFT
evidence-status: provisional-pending-substrate
package-id: P7
human-bound: yes
execution-status: NOT EXECUTED — no corpus downloaded, nothing acquired, nothing sealed, no steward engaged
---

# P7 — Corpus acquisition and sealing

## What this is

The procedure for acquiring the wild-tail PDF corpus, stratifying it, and — the part with a one-way deadline — having an independent steward **seal the held-out splits before any implementation exists.**

Charter §3.6 defines a hard evidence boundary: *after code exists, nothing new can become held-out.* Once an implementation has been shaped, however indirectly, by knowledge of a document, that document cannot later establish held-out generalization. A later procedure cannot restore that independence. **This package must finish before the C1 swarm runs.**

## Why a human must do this

- **Acquisition is downloading**, at scale, from third parties, under terms someone must read and accept. An agent may not acquire anything, and I have downloaded nothing.
- **The held-out split must be selected by someone the implementation cannot reach.** If an agent chose the split, the split would be known to the system it is meant to test. That is not a policy — it is the definition of the thing being purchased (Rev 7 §28.3).
- **One acquisition step is forbidden to agents for clean-room reasons, permanently.** The S1 denominator (Rev 7 §24.15.1) is built from public conformance fixtures whose surrounding repositories are prohibited processor sources. Rev 7 requires **a corpus steward who does not expose that surrounding source to implementation contexts.** A human can walk into that repository, take the rights-cleared fixture files, and walk out. **An agent cannot: reading the repository to fetch the fixtures is exactly the contamination the clean-room law forbids, and contamination cannot be undone** (OVERNIGHT_GOAL §1.3).
- **Privacy and legal classification are judgments** (Rev 7 §28.4; §4.7). Wild PDFs contain personal data.

## Prerequisites

- **P1 Role A (corpus steward)** engaged. Without a steward, sealing does not exist — a project that seals its own held-out set has performed a ceremony, not a control.
- **P3 (substrate)**, to commit the seal manifests.
- Storage that is access-controlled, encrypted at rest, and **isolated** — see the malware warning below, which is not hypothetical.
- Counsel availability for the Common Crawl AI/ML indemnification question (below).

## Sources, evidence classes, and constraints

**[ROOT-VERIFIED]** — root opened these exact pages and recorded the findings in `ledger/RUN_LEDGER.md`. **Nothing was downloaded by any agent, and nothing may be.**

| Source | Exact URL | What it is | The condition that actually matters |
|---|---|---|---|
| **Govdocs1** | `https://digitalcorpora.org/corpora/file-corpora/files/` | ~1M files harvested from `.gov` servers; stated freely redistributable | **It contains known malware, disclosed explicitly by the publisher.** This is a feature for a hostile-input engine and a hazard for the machine holding it. Isolated storage, no execution, and AV quarantine will fight you — plan for it |
| **SafeDocs PDF corpus** | `https://digitalcorpora.org/corpora/file-corpora/cc-main-2021-31-pdf-untruncated/` | PDFs extracted from Common Crawl; the wild-tail workhorse | **The publisher warns it is a convenience sample and not representative.** This constrains what S2 may claim: a wild-tail ledger over a non-representative sample is a ledger over that sample, and the selection bias must be a declared stratum, not a footnote (Rev 7 §24.15.2 requires exactly this — strata record known selection bias) |
| **Common Crawl** | `https://commoncrawl.org/terms-of-use` | The upstream crawl | Limited, non-exclusive, non-transferable licence; no separate PII harvesting; third-party copyright is the *user's* responsibility; discretionary takedown. **And an indemnification clause that expressly covers use of crawled content with AI/ML** — which this project does, structurally. **Counsel decision, not an agent's** |
| **Public conformance suites** | *(not listed here by URL, deliberately)* | The S1 denominator's fixture source | **Steward-only.** The fixture files may be rights-cleared; the repositories around them are prohibited clean-room sources (Rev 7 §4.1). A human extracts the fixtures. No agent goes near the repository — not for the fixtures, not for the README, not "just to check the licence" |
| **Project-generated fixtures** | — | Grammar/mutation generators (Rev 7 §28.5, §28.6) | The only class agents may freely produce. They are not wild-tail evidence and cannot substitute for it |

## Exact steps

### Phase 1 — Rights and privacy review, *before* any download (2–3 h + counsel)

1. Read each source's terms **as they stand on the acquisition date**, and file them. Terms change; the project's rights are the terms it accepted.
2. Take the **Common Crawl AI/ML indemnification** question to counsel explicitly. The relevant question is narrow and worth phrasing precisely: *the corpus is processed by the software under development, and its documents may also appear in agent-visible debugging contexts.* Those are two different exposures, and the second is the one people forget.
3. Classify every source per Rev 7 §4.7: source · licence or use basis · redistribution policy · privacy classification · committable or hash-only · partition (train/dev/validation/**held-out**).

### Phase 2 — Acquisition (steward-executed; hours to days of transfer)

4. The steward downloads to **isolated, access-controlled, encrypted-at-rest storage.** Not a laptop. Not a shared drive. Govdocs1 contains live malware, and the storage must be built on that assumption.
5. Record, per Rev 7 §28.2, a manifest for every item: internal content identity · provenance · licence · source date · personal-data status · expected claims · expected **no-claims** · profile applicability · partition.
6. **No agent may be given a path to this storage.** Not read-only, not "just the sanitized subset." The access boundary is the control.

### Phase 3 — Stratification (steward + human, 2–4 h)

7. Stratify per Rev 7 §24.15.2: producer · version/dialect · encryption · malformedness · fonts · codecs · transparency · signatures · page count — **and known selection bias**, which for the SafeDocs corpus is a publisher-stated fact and must appear as a stratum rather than a disclaimer.
8. Reserve a **replacement pool** now (Rev 7 §28.3 requires a fresh reserve set sufficient for replication). A held-out set that gets burned — and one will — must be replaceable without a new acquisition project.

### Phase 4 — The seal (steward-only; the one-way step; 1–2 h)

9. **The steward selects the held-out splits.** Not the human running the campaign, and emphatically not an agent.
10. The steward computes **salted** commitments over the split manifests. Rev 7 §28.4 is explicit: do not publish unsalted hashes of confidential or low-entropy material — a hash of a guessable thing is not a secret. The salt lives with the steward.
11. The steward commits the seal manifest through the substrate (**P3**), with its date.
12. The steward records the `EvaluationProtocolId` (Rev 7 §28.3): who may submit · submission/query budget and whether failed runs consume it · what aggregate feedback returns before final freeze · whether per-case diagnostics, labels, or breakdowns are withheld · access logs · the reveal rule · the replacement reserve.
13. **Then, and only then, may implementation begin.**

### Phase 5 — Standing discipline (forever)

14. The evaluation service prevents leakage through bytes, summaries, embeddings, caches, dashboards, scorer diagnostics, model-provider retention, and **human side channels** (Rev 7 §28.3). Provider behaviour that cannot be verified is a known unknown and disqualifies the affected set from strong held-out claims; record that limit before evaluation begins.
15. **When a held-out set is burned, say so.** Repeated adaptive tuning against a hidden set makes it development data even if the bytes were never revealed. The set is then retired to a regression fixture, the strong claim is withdrawn, and the reserve replaces it. P4 (DC-2 §5) precommits this treatment so it is not renegotiated after exposure.

## Expected time

4–8 human hours of decision and procedure, plus transfer time (sizes are `[UNVERIFIED]` — read them off the source pages at acquisition; the SafeDocs corpus is large and the storage must be provisioned before the download, not during it). Calendar: days, and gated on the steward's availability.

## Evidence returned to the repo

- The rights/privacy classification table (one row per source).
- The stratification design, including the declared selection-bias strata.
- The **committed seal manifest hash** and its commitment proof (bytes stay with the steward; only the commitment enters the repository).
- The `EvaluationProtocolId` text.
- **Not** the corpus. Not a sample of it. Not a summary of the held-out split. Nothing that would let a reader — or a model — infer its contents.

## Failure and downgrade path

| Failure | Consequence | Honest response |
|---|---|---|
| **Implementation starts before the seal** | **Irreversible.** No held-out claim is available for the whole campaign; the C3 wild-tail gate has no independently stewarded sample | Do not start. Held-out independence cannot be restored after implementation begins |
| No steward (P1 Role A fails) | The project can still acquire and stratify, but its "held-out" set is self-sealed | Every held-out and wild-tail claim degrades to **self-attested**, explicitly and in public. S2 is published as a ledger over a self-selected sample — which is still useful, and must not be described as anything more |
| Common Crawl terms unacceptable to counsel | The SafeDocs/CC lineage is unavailable | Fall back to Govdocs1 plus project-generated and conformance corpora, and **declare the coverage loss** — the intended wild-tail stratum is then absent |
| Malware handling defeats the storage plan | Acquisition stalls | Expected. Plan isolation before downloading, not after the first quarantine event |
| Held-out set burned by adaptive tuning | The strong claim is void | Retire the set, withdraw the claim, deploy the reserve, record it. §33.10: a system that never demotes a claim is epistemically suspect — the demotion is evidence *for* the project's grounding, not against it |

## Ready-to-send draft — steward sealing brief

Send with the P1 Role A charter, once the steward accepts.

```
Subject: Sealing brief — what I need you to do before I write a line of code

[NAME],

Thank you for taking the steward role. The sealing step is the one with a
deadline that cannot be moved, so here it is in full, up front.

Before any implementation exists, you select the held-out evaluation splits and
seal them. After code exists, nothing new can honestly become held-out — not
because of a rule I made up, but because an implementation shaped by knowledge
of a document can no longer be tested by it. There is no way to undo that, so
the ordering is: you seal, then I build.

Concretely:

  1. Acquire and stratify the corpus (procedure attached). Isolated storage,
     please — Govdocs1 ships with real malware, which is exactly why we want it
     and exactly why it doesn't go on your laptop.
  2. Note that the SafeDocs PDF corpus is published as a convenience sample and
     is not representative. Please carry that as an explicit stratum, not a
     footnote. Any claim I make later has to inherit that limitation honestly.
  3. YOU choose the held-out splits. Not me. I would like to be very clear that
     I do not want to know which documents are in them, and that if you tell me,
     you will have destroyed the thing I asked you to make.
  4. Salt and commit the split manifest, and keep the salt.
  5. Write the access protocol: how many submissions I get, what feedback comes
     back, when the set is revealed, and what replaces it when it is used up.

One more thing, and it is the part people find strange: if I ever start tuning
against your held-out set — even indirectly, even without seeing the bytes —
that set has become development data and I need you to tell me so. Retiring a
set is a normal, expected event, not a failure. Please have the reserve ready.

Nothing here has been downloaded yet. The first acquisition is yours.

[NAME]
```

## Open items requiring human verification

| Item | Status | Verification step |
|---|---|---|
| Corpus sizes and current terms | `[UNVERIFIED]` — deliberately not fetched in bulk; **nothing downloaded** | Steward reads the two Digital Corpora pages and the Common Crawl terms at acquisition |
| Common Crawl AI/ML indemnification exposure | **[ROOT-VERIFIED]** that the clause exists; its consequences for this project are a legal judgment | Counsel |
| SafeDocs non-representativeness | **[ROOT-VERIFIED]** — publisher-stated | Must appear in the stratification and in every claim that rests on the corpus |
| Which conformance suites are rights-cleared for fixture extraction | Not researched — **and not researchable by an agent** | Steward, by hand, without exposing surrounding processor source to any agent context |
| Storage provisioning | Not sized | Provision before download |
