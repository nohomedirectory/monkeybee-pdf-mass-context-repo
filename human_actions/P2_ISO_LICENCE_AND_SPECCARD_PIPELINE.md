---
generated-by: Claude G5 owner (claude-opus-4-8)
date: 2026-07-14
inputs:
  - MONKEYBEE_CAMPAIGN_CHARTER_v1.md §3.5, §8 (risk 2)
  - CYCLE_0_WORK_ORDER.md §5.5
  - OVERNIGHT_GOAL.md §1.2 (no SpecCard bodies)
  - MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md §4.2, §4.2.1, §4.3, §4.4, §35 (ISO access and quotation policy)
  - iso.org licence terms (see "External facts", below)
  - pdfa.org sponsored-standards programme (see "External facts", below)
status: DRAFT
evidence-status: provisional-pending-substrate
package-id: P2
human-bound: yes
execution-status: NOT EXECUTED — no copy obtained, nothing purchased, no permission requested, no reviewer engaged
---

# P2 — ISO 32000-2 licence acquisition and SpecCard pipeline standup

## What this is

The steps to lawfully obtain ISO 32000-2 (and its errata) **under ISO's current AI-use terms**, to classify the resulting rights, and to stand up the human pipeline that converts a licensed specification into agent-consumable `SpecCard`s without contaminating the clean room.

This is the campaign's **critical path**. Rev 7 §4.2.1 makes rights-vetted SpecCards the *only* legal channel for ISO semantics into implementation. Charter §3.5 makes card coverage a gate on every cycle's swarm start, and Charter §8 ranks SpecCard human latency as risk #2 — the slowest step in a compute-unlimited campaign. Nothing about this can be compressed by adding agents; adding agents to it is precisely the contamination failure.

## The gate, stated plainly

**Three different facts, routinely conflated (Rev 7 §4.2): available at no cost · legally obtained · permitted to place in an AI prompt.**

### External facts (2026-07-14), with their evidence class marked

Two evidence classes appear below and are **not** interchangeable. **Root-verified** means the root orchestrator opened the official page and recorded the finding in `ledger/RUN_LEDGER.md`. **Search-derived** means this owner's direct fetches were refused (iso.org and pdfa.org return HTTP 403 to automated requests) and the detail exists only in a search result served from the official domain — which is *not* primary-page verification and carries no stronger claim than `[UNVERIFIED]`.

**1. ISO's terms require a separate licence for a model-visible workflow. [ROOT-VERIFIED]** Root opened `https://www.iso.org/terms-conditions-licence-agreement.html` and `https://www.iso.org/copyright.html` and recorded that they establish **a separate licence is required for the contemplated model-visible workflow** — that is, placing ISO publication text where an AI model can see it is not covered by ordinary access.

> Additional detail is **`[UNVERIFIED]`**: search results from the iso.org domain further indicated that the prohibition expressly names embedding, prompting, and querying (not only training), and that ISO opts out of the EU DSM Article 4 text-and-data-mining exception, with audit rights reserved and permissions handled at `copyright@iso.org`. **None of that wording was read on the page by this owner.** It is recorded as a search-level signal for the human to confirm, not as an established fact, and nothing in this package depends on it — the root-verified headline alone is sufficient to set the policy.

**2. ISO 32000-2 catalogue metadata. [ROOT-VERIFIED]** Root opened `https://www.iso.org/standard/75839.html`: **Edition 2, published/current status, CHF 227 list price.**

**3. A no-cost route exists; its AI-use rights do not. [ROOT-VERIFIED, with the decisive gap open]** Root opened `https://pdfa.org/sponsored-standards/` and confirmed **no-cost public access** to ISO 32000-2. Root also recorded that **rights for this campaign's AI workflow remain unestablished.** The licence terms attached to the no-cost copy are therefore still the single most important thing for the human to read — no-cost access is a fact about price, not about permission (Rev 7 §4.2 makes exactly this distinction).

**4. Rev 7 §4.4's errata baseline remains a project-internal claim. `[UNVERIFIED]`** Rev 7 asserts the planning baseline is ISO 32000-2:2020 plus the PDF Association's June 2026 Errata Collection 3. The edition line is now consistent with root's catalogue read (Edition 2), but **the errata collection's identity, version, and publishing authority were not verified by anyone this run.** Confirm at acquisition, and keep ISO amendments/corrigenda distinct from PDF Association errata collections — Rev 7 §4.4 insists they are different authorities and must not both be called "formal ISO errata."

**The conclusion that follows.** A lawfully obtained copy — purchased or no-cost — gives *humans* reading rights. It does not give *agents* anything. **This does not break the campaign.** Rev 7 §4.2.1's default policy is already **deny model access to standards text**, and the SpecCard pipeline is built so agents never see the specification at all. Being denied AI-use permission costs the project nothing it planned to use. What this package must actually deliver is (a) a lawfully obtained copy humans may read, (b) a written record of what the licence does and does not permit, and (c) two humans to review the cards.

## Why a human must do this

1. **Purchase and licence acceptance are legal acts.** An agent cannot enter a licence agreement, and I am prohibited from purchasing anything.
2. **The AI-use gate is definitionally not delegable to the AI.** If an agent fetched the specification to determine whether agents may fetch the specification, the question would already be answered the wrong way — irreversibly. Contamination cannot be undone (OVERNIGHT_GOAL §1.3).
3. **Two-person meaning review is a human epistemic act** (Rev 7 §4.2.1(3)): a card is authoritative because two humans checked it against the controlling source, not because a model wrote it fluently.
4. **Rights classification requires judgment about legal instruments**, and the registry records "not reviewed" rather than treating an absent restriction as clearance (Rev 7 §4.2.1).

## Prerequisites

- P3 (substrate), so the rights determination and each card's provenance can be committed as they land. Not strictly blocking — obtain the copy first if P3 slips.
- Counsel or a designated source-rights owner (Rev 7 §35: "Standards AI-use rights → Counsel/source-rights owner and per-source terms matrix").
- Two people with PDF/standards competence for meaning review. They may be part-time. They may not be the same person twice, and neither may be an implementation agent.

## Exact steps

1. **Read the terms before acquiring anything** (30 min). Open `https://www.iso.org/terms-conditions-licence-agreement.html` and the PDF Association sponsored-standards page. Confirm, in the human's own reading: (a) the AI/ML prohibition's exact scope; (b) what the no-cost copy's licence actually says; (c) whether ISO 32000-2:2020 is the current edition; (d) what the current errata collection is and who publishes it (ISO amendment/corrigendum vs PDF Association errata collection — Rev 7 §4.4 insists these are different authorities and must not both be called "formal ISO errata").
2. **Acquire the copy** (30 min). Either the no-cost sponsored copy or a purchased ISO copy — whichever's terms the human prefers after step 1. **Capture the licence text as it stood on the acquisition date** and file it with the copy; licence terms change, and the project's rights are the terms at acquisition. If purchasing: this is a purchase, and no agent may make it.
3. **File the rights matrix** (60 min, with counsel). For ISO 32000-2, the errata collection, and every other normative source (ETSI/PAdES, ICC, Unicode, font, and cryptographic specs — Rev 7 §4.2.1 applies the same gate to all of them), record the ten independent flags from §4.2.1: human reading · machine parsing by non-generative tools · inclusion in model prompts/retrieval · training/fine-tuning · test/corpus execution · quotation in project artifacts · redistribution · black-box experimental use · patent/SEP/trademark/export encumbrance review status · approved jurisdictions. Record **"not reviewed"** where it is not reviewed. Absence of a known restriction is not clearance.
4. **Decide whether to request AI-use permission at all** (15 min). The recommendation is: **do not**, at least not initially. The pipeline is designed to not need it; requesting it invites an audit relationship and a negotiation the project does not require, and a *denial on the record* is worse than a *policy of not asking*. If the human wants the option preserved for a later, narrower purpose (for example, a non-generative extraction tool that parses clause structure without a model), the draft enquiry below is ready — and it deliberately asks about *non-generative machine parsing*, which is a different flag from prompting.
5. **Staff the two-person meaning review** (60 min to identify and ask). Two humans. Neither authored the card under review. Both have access to the licensed source. Their names and the review dates become each card's rights and technical provenance (Rev 7 §4.3).
6. **Declare the agent-visible boundary in writing** (30 min) — the table below — and hand it to every human who touches the specification.
7. **Begin card production for the R0 surface** (ongoing; cards run one cycle ahead of implementation, Charter §3.5). The card *registry, slot map, extraction protocol, and review template* are being produced in-repo by the G1 owner with every slot marked `PENDING-LICENSED-SOURCE`; this package supplies the licensed source and the humans that fill them.

## The agent-visible boundary (hand this to every human on the pipeline)

| Artifact | May an implementation agent see it? | Why |
|---|---|---|
| ISO 32000-2 text, in any form — file, screenshot, paste, quote, retrieval index, chat log, CI artifact | **Never**, absent a recorded counsel permission basis | Rev 7 §4.2.1(1). ISO's licence bars prompting/embedding without separate authorization |
| A project-authored SpecCard that has passed two-person review | Yes | §4.2.1(4) — this is the only legal channel |
| Public errata material whose terms permit use | Yes, once its terms are recorded | §4.2.1(4); terms are per-source, never inherited |
| Machine-readable standards models with compatible licences | Yes, once classified | §4.2 |
| A model's *memory* of the PDF specification | **Never as a card body** | OVERNIGHT_GOAL §1.2: generating card semantics from model memory is clean-room contamination, and is the #1 predicted failure mode of the agent run. Plan documents may discuss PDF semantics at Rev 7's level; normative cards may not exist until a licensed human writes them |

The last row is the one that will be violated by accident. It looks like helpfulness.

## Expected time

| Step | Human time | Calendar |
|---|---|---|
| Read terms, acquire copy | 1 h | Same day |
| Rights matrix with counsel | 1–2 h (+ counsel's own time) | Days |
| Staff two-person review | 1 h to ask | Days–weeks |
| Optional ISO written enquiry (step 4) | 30 min to send | **Weeks, `[UNVERIFIED]`** — ISO's response time is unknown to this project |
| Card production, R0 surface | Ongoing, and it is the campaign's rate limit | One cycle ahead of implementation, forever |

## Evidence returned to the repo

- The rights matrix (one row per source, ten flags, with "not reviewed" where true).
- The licence text as captured at acquisition, with its date and hash committed through P3.
- The two reviewers' names and qualifications (in the ledger; card-level provenance references them).
- The signed agent-visible boundary declaration.
- **Not** the specification itself, and not any excerpt of it, anywhere in this repository.

## Failure and downgrade path

| Failure | Consequence | Honest response |
|---|---|---|
| AI-use permission not obtained | **None.** The pipeline never planned to use it | Record the flag as denied/not-granted and proceed. The default was already deny |
| No lawful copy obtained at all | Fatal to the SpecCard channel: no cards, so every cycle's coverage gate blocks | The campaign cannot proceed to implementation on ISO semantics. It may not substitute model memory. Escalate to the human; this is a stop-the-line condition |
| Two-person review cannot be staffed | Cards exist but are not authoritative (§4.3: a card is not authoritative because an agent wrote it) | Cards ship marked single-reviewed; every claim resting on them carries that provenance. Coverage gates report the deficit rather than hiding it. This is a real degradation and must be logged, not smoothed |
| Errata authority misattributed | Corpus contradicts itself about what is normative | Rev 7 §4.4's rule stands: an ISO amendment/corrigendum and a PDF Association errata collection are different authorities with different status. Record which is which, per resolution |

## Ready-to-send drafts

Nothing below has been sent.

### Draft A — Optional enquiry to ISO (only if step 4 says yes)

```
To: copyright@iso.org
Subject: Licence enquiry — permitted processing of ISO 32000-2 for standards-conformance engineering

Hello,

I am acquiring ISO 32000-2 for use in a software engineering project and want
to confirm my obligations before doing anything with it, rather than after.

My intended workflow is deliberately conservative. Named individuals read the
publication and hand-author short, project-authored requirement summaries in
our own words, each citing a clause reference. Those summaries — not the ISO
text — are what our engineering process consumes. The publication itself would
not be placed in any AI system, any prompt, any retrieval index, or any
automated pipeline.

Two questions:

  1. Does that workflow sit inside the standard single-user licence as you
     understand it?

  2. Separately, and I ask because I understand it is a different permission:
     would non-generative machine parsing of the publication — extracting
     clause structure and numbering for an internal index, with no AI/ML model
     involved and no reproduction of text — require a separate licence? If so,
     what is the route to request one?

I am not asking for permission to use the publication with AI or machine
learning systems, and our process is designed not to require it.

Thank you,
[NAME]
[ORGANIZATION]
```

*Why this draft is worded this way:* it does not ask for AI-use permission (the project does not need it, and asking creates a record and a relationship it does not want), it distinguishes non-generative parsing from model access — which ISO's own terms treat as separate — and it states the conservative workflow up front so the answer is about the actual practice rather than a hypothetical.

### Draft B — Two-person meaning reviewer ask

```
Subject: Two-person spec review for a PDF engine (paid, ~[N] h/week)

Hello [NAME],

I'm building a PDF engine under a clean-room protocol, and I need something
specific that I cannot get from an AI agent: two people who can read ISO
32000-2 and confirm that a short summary of a clause actually means what the
clause says.

The workflow: a licensed human reads the clause and writes a "SpecCard" — a
paraphrase in our own words, with the clause reference, the normative level
(shall/should/informative), preconditions, required behaviour, failure
behaviour, and test obligations. Then a second person, who did not write it,
checks it against the source. Only then may our engineering process use it.

The reason for the second person is not bureaucracy. The cards are the *only*
channel through which specification meaning reaches the implementation, by
design and for legal reasons. A wrong card is a wrong engine, silently, and
nothing downstream will catch it.

You would need access to the licensed copy (I provide it), PDF or
standards-engineering background, and a tolerance for pedantry — the job is
almost entirely pedantry.

[N] hours/week, [DURATION], [COMPENSATION]. Interested?

[NAME]
[CONTACT]
```

## Open items requiring human verification

| Item | Status | Verification step |
|---|---|---|
| ISO terms require a separate licence for model-visible use | **[ROOT-VERIFIED]** — root opened the ISO terms and copyright pages | None needed for the policy. The boundary table below already assumes the strictest reading |
| Exact clause wording (embedding/prompting/querying; EU Art. 4 TDM opt-out; audit rights) | **`[UNVERIFIED]`** — search-derived only; this owner's fetches were refused (403) | Human opens `https://www.iso.org/terms-conditions-licence-agreement.html` and reads it. **Nothing in this package depends on this detail** |
| Licence terms of the no-cost PDF Association copy | **`[UNVERIFIED]` — the decisive unknown.** Root confirmed the route exists; the rights did not follow | Human obtains the copy via `https://pdfa.org/sponsored-standards/` and reads the licence attached to it. No agent may download it |
| ISO 32000-2 edition, status, price | **[ROOT-VERIFIED]** — Edition 2, published/current, CHF 227 | Confirm at purchase if buying |
| Current errata collection identity and publisher | `[UNVERIFIED]`; Rev 7 §4.4 asserts PDF Association Errata Collection 3, June 2026 | Human confirms at acquisition; record publisher and status **separately** from ISO's (§4.4) |
| ISO response latency to Draft A | `[UNVERIFIED]` | Only knowable by sending — and step 4 recommends not sending |
