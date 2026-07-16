---
generated-by: Claude G5 owner (claude-opus-4-8)
date: 2026-07-14
inputs:
  - MONKEYBEE_CAMPAIGN_CHARTER_v1.md §3.1, §3.2, §10
  - CYCLE_0_WORK_ORDER.md §5.1, §5.2, §6
  - AUDIT_FINDINGS_LEDGER.md C-9
  - MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md §33.1, §33.4, §28.4, §35 (evaluation precommitment substrate; open decision 4)
  - opentimestamps.org; docs.sigstore.dev (see "External facts", below)
status: DRAFT
evidence-status: provisional-pending-substrate
package-id: P3
human-bound: yes
execution-status: NOT EXECUTED — no timestamp submitted, no log entry made, no ledger opened, no hash broadcast
---

# P3 — Commitment substrate and production-ledger opening

## What this is

The choice, setup, and first use of the **tamper-evident commitment substrate**: the channel that turns this campaign's precommitments into evidence. Plus the opening ceremony of the production ledger, whose first entry is the committed Charter hash.

Everything in this repository currently carries `evidence-status: provisional-pending-substrate`. **This package is what removes that qualifier.** Until it executes, the campaign has plans, not evidence.

## Why a human must do this

- **Committing is an external, outward-facing act, and must be assumed irreversible.** Submitting a hash to a timestamping calendar or a public transparency log broadcasts it. Whether such an entry can ever be removed is `[UNVERIFIED]` for the mechanisms surveyed below — which is precisely why it must be treated as unrecallable: an entry may permanently disclose that *something* was committed on that date. Agents in this campaign are forbidden every one of those acts.
- **The independence property is the whole point.** A commitment the project's own agents made, on infrastructure the project controls, on a clock the project controls, proves nothing about the project. Rev 7 §33.4 requires the commitment be held by an independent steward, a witnessed/timestamped append-only log, or an equivalent mechanism — *before* results.
- **Charter §10 and audit finding C-9 are explicit: a git commit alone is decoration.** Git timestamps are attacker-controlled (any committer can set any date), and a repository the project owns cannot witness the project.
- **Open decision 4 (Rev 7 §35) is unresolved and is the human's to resolve**: self-hosted versus existing transparency ecosystem, with a threat model that includes split-view/equivocation resistance, privacy, and *potentially irreversible membership disclosure*. That last one is why an agent must not "just try it."

## Prerequisites

- A human authorized to ratify the substrate choice and accept the selected provider terms. No agent can supply that authority.
- The exact P4, P5, and P8 drafts that will enter the opening batch, plus the canonical inputs named below, present on disk and freshly hashed at ceremony time.
- A current human review of the selected TSA and OpenTimestamps client instructions. Their provider/command details remain `[UNVERIFIED]` in this closure.
- P1 Role B (commitment custodian) if available. Its absence is not blocking when the human ratifies a qualifying witnessed/timestamped mechanism, but the gap must be logged.
- No implementation start and no campaign-artifact broadcast before the human completes the checks above.

## What the substrate must do (requirements, from §33.4 and §24.16)

1. **Bind bytes to a time the project does not control.** Reveal must prove the *exact* committed bytes.
2. **Be append-only and non-equivocating** — no ability to show one history to one party and a different history to another.
3. **Precede the activity it governs.** Discovery commitment before search; discovery report before measurement design; evaluation protocol before measurement (§24.16's three irreversible stages). One late omnibus document cannot retroactively satisfy all three boundaries (§33.4).
4. **Support amendment without laundering:** a material change creates a *new* ID and requires fresh confirmatory data; the changed run is exploratory until then.
5. **Not leak what must stay sealed.** Held-out corpus manifests and confidential material get salted or access-controlled commitments — Rev 7 §28.4 forbids publishing unsalted hashes of confidential or low-entropy material, because a hash of a guessable thing is not a secret.

## Options considered

### Recorded external evidence and unverified candidate (2026-07-14)

- **OpenTimestamps** (`https://opentimestamps.org/`) **[ROOT-VERIFIED at the mechanism scope]**: a format for blockchain timestamping. The client hashes the file locally and submits the digest to free public calendar servers, which aggregate and anchor it to the Bitcoin blockchain and pay the transaction fee. No registration, no API key, no cost. Verification is against Bitcoin, not against the operators — the trust assumption is Bitcoin's integrity and availability, not OpenTimestamps' honesty. Only the client-computed digest is submitted; confidential or low-entropy material still requires the salting rule in §28.4.
- **Sigstore Rekor** (`https://docs.sigstore.dev/logging/overview/`) **[ROOT-VERIFIED at the recorded scope]**: an append-only, tamper-resistant transparency log for signed supply-chain metadata, with inclusion proofs and signed tree heads, auditable for append-only consistency. A public instance runs at `rekor.sigstore.dev` with a stated 99.5% availability SLO. **Retention and privacy guarantees are `[UNVERIFIED]`** — neither this owner nor root found them stated, and root recorded that absence as provisional rather than as proof that no policy exists. An earlier draft of this package asserted that entries are "public and permanent"; that overstated the evidence. **Treat publication as irreversible by conservative assumption, not as an established property** — the safe assumption and the verified fact are different things, and only one of them is available here.
- **RFC 3161 Time-Stamp Protocol**: cited by stable identifier as a candidate TSA mechanism. No RFC body or vendor terms were fetched during this run; its fit, current implementations, trust chain, jurisdiction, and cost are `[UNVERIFIED]` pending human review.

| Option | Proves time | Non-equivocating | Discloses existence publicly | Trust assumption | Cost |
|---|---|---|---|---|---|
| **A. Independent steward custody** (P1 Role B) | Only as well as the human attests | Human integrity | No | One person | Their time |
| **B. RFC 3161 TSA token** | `[UNVERIFIED]` pending selection and review of a TSA | `[UNVERIFIED]` pending selected TSA | `[UNVERIFIED]` pending selected TSA | Selected TSA and its verifier chain | `[UNVERIFIED]` |
| **C. OpenTimestamps** | Yes, by the eventual Bitcoin anchor | Bitcoin | Only a client-computed digest is submitted; salt confidential or low-entropy manifests (§28.4) | Bitcoin's continued integrity | Free |
| **D. Sigstore Rekor** | Yes, with inclusion proofs | Yes — auditable append-only log | **Yes; treat as irreversible.** Retention/removal policy `[UNVERIFIED]` | Log operators + auditors/monitors | Free |
| **E. Git commit alone** | **No** — committer sets the date | No | — | The project itself | — |

Option E is listed only to name it as prohibited (Charter §10; C-9).

## Recommendation — `PROPOSED, awaiting human ratification`

**Use B + C + A together, and hold D in reserve.** Concretely, for each commitment:

1. Compute the digest of the exact bytes (with a salt where the content is confidential or low-entropy — §28.4).
2. After human review of the mechanism and provider, get an **RFC 3161 token** from the selected TSA. The provider's terms, chain, jurisdiction, and cost remain `[UNVERIFIED]` until that review.
3. **OpenTimestamp** the same digest (anchors it to a mechanism nobody in this project controls, at zero cost, submitting only the digest; apply §28.4 salting where required).
4. Send the digest, the token, and the `.ots` proof to the **independent custodian** (P1 Role B), who records receipt independently of the project's infrastructure.

Why the combination rather than one: the mechanisms and custodian produce distinct records, so the failure or discontinuation of one does not silently erase every commitment path. The actual marginal cost is `[UNVERIFIED]` until the human selects and tests the providers.

**Why Rekor is held in reserve rather than adopted now.** It offers public, auditable append-only properties that may fit later release-artifact verification. But its entries are public, its retention and removal guarantees are unestablished, and open decision 4 flags irreversible membership disclosure as an unresolved threat-model question. The privacy effect of committing the *existence* of either a discovery protocol or a held-out corpus seal has not been established here. When you cannot verify whether publication is reversible, assume it is not. Decide this deliberately, not by default.

**Note on the OpenTimestamps boundary:** the externally checkable time bound comes from the eventual Bitcoin anchor, not from an unverified local submission timestamp. Current client syntax, confirmation latency, and upgrade procedure are `[UNVERIFIED]` in this closure; the human must confirm them against the current official client instructions, retain the initial receipt if one exists, and file the upgraded proof before relying on it.

## Exact steps

### First: choose (30 min)

Ratify or amend the recommendation above. Record the choice, the rationale, and the date as a §34.5-style decision row. If the human picks a different mechanism, that is a ratification, not a deviation — the requirement is §33.4's properties, not a specific vendor.

### Then: set up (1–2 h)

1. Install an OpenTimestamps client (human machine, not an agent's), following the current official instructions. Verify the current command surface against a throwaway file first — *never* a campaign artifact — so that the first real commitment is not also the first test.
2. Select a TSA and confirm its terms and its certificate chain. `[UNVERIFIED]`: no specific TSA is recommended here; the human should pick one whose terms and jurisdiction they are comfortable with.
3. Confirm the custodian (P1 Role B) is engaged, or record that they are not and proceed with B + C alone, logging the gap.
4. Write down the **reveal procedure** before you need it: which bytes, which salt, where the salt is kept, who can perform a reveal, and how a third party verifies. A commitment whose reveal procedure was never written down is a commitment nobody can check.

### Then: the opening ceremony (30 min)

Commit, in **one batch** (Work Order §6), and record the batch hash as **ledger entry #1**:

- `MONKEYBEE_CAMPAIGN_CHARTER_v1.md` — the Charter is its own first committed artifact (Charter §3.2)
- `CYCLE_0_WORK_ORDER.md`
- `AUDIT_FINDINGS_LEDGER.md`
- `CAMPAIGN_CHARTER_REASONING.md`
- The discovery-protocol commitment texts (**P4**) and the challenge-window durations (**P5**)
- The Q3 claim-family precommitment (**P4**, §2)
- The baseline-budget reservation (**P8**)
- The held-out seal manifests **when they exist** (**P7**) — these come later, and they come *before any implementation agent runs*

The exact file digests to commit are maintained by the orchestrator in `ledger/CANONICAL_HASHES.md`. **Recompute them at ceremony time from the actual files** — do not trust a table an agent wrote, including that one. Recomputation takes seconds and is the entire point.

### Then: open the production ledger (30 min, then forever)

Rev 7 §33.1: the production ledger begins **before candidate generation**, not after a successful artifact appears. Entries are append-only or correction-linked, and cryptographically committed under a versioned protocol with independently witnessed checkpoints where practical.

First entries: the batch hash above; the campaign's model/harness/tool manifest; the human participants and roles; the known unknowns (start with: the four `SOURCE-UNAVAILABLE` and `[UNVERIFIED]` items this repository already carries).

Everything the agent swarm has produced *before* this ceremony — including the entire overnight run that produced this package — is labeled **`retrospective`** and may explain history but cannot by itself support a prospective foundry claim (§33.1). That labeling is not a formality to be finessed later; write it into ledger entry #2 now, while it is unambiguous.

## Expected time

2–4 human hours to first commitment. Then minutes per commitment thereafter, plus the OpenTimestamps upgrade step hours later.

## Evidence returned to the repo

- The chosen substrate, recorded as a ratified decision with rationale and date.
- Ledger entry #1: the batch hash, its TSA token, its `.ots` proof, and the custodian's receipt.
- The written reveal procedure.
- A ledger row for every subsequent commitment: what, when, by which mechanism, and where the proof lives.

## Failure and downgrade path

| Failure | Consequence | Honest response |
|---|---|---|
| No custodian (P1 Role B declines) | Commitments rest on TSA + OpenTimestamps | Acceptable. Log the gap. §33.4 permits a witnessed/timestamped log *or* a steward |
| Substrate not established before implementation starts | **The campaign's central evidentiary premise fails.** Everything after becomes retrospective | Stop. Do not start implementation. This is the one item where proceeding without it is worse than delay — a retrospectively "committed" protocol is exactly the FrankenSim failure this campaign was designed against |
| Substrate established late, mid-campaign | Everything before is `retrospective`; everything after is prospective | Label the boundary date explicitly and never blur it. A mixed ledger with an honest boundary is evidence; a mixed ledger without one is not |
| Bitcoin/OTS or the TSA becomes unavailable years later | Existing proof bytes may remain checkable only while their verifier dependencies and trust roots remain available; continuity is not assumed | Preserve the proofs and verifier requirements, then version the commitment protocol (§33.4 anticipates this: material change ⇒ new ID) |

## Draft ceremony command outline (for the human, not for an agent)

This is **not** a repository file and must not be committed as code (the campaign is plan-space only). It is a draft of what the human types. The `ots` command surface is `[UNVERIFIED]` in this closure; confirm it against the current official client instructions before using any campaign artifact.

```
# 1. Recompute the digests yourself; don't trust the table.
sha256sum MONKEYBEE_CAMPAIGN_CHARTER_v1.md CYCLE_0_WORK_ORDER.md \
          AUDIT_FINDINGS_LEDGER.md CAMPAIGN_CHARTER_REASONING.md \
          human_actions/P4_DISCOVERY_PROTOCOL_COMMITMENTS.md \
          human_actions/P5_CHALLENGE_WINDOW_PROPOSAL.md \
          human_actions/P8_BASELINE_BUDGET_RESERVATION.md > batch-c0.txt

# 2. The batch manifest is itself the committed artifact.
sha256sum batch-c0.txt

# 3. Timestamp it (Bitcoin anchor; free; discloses only the hash).
ots stamp batch-c0.txt

# 4. Hours later, once a block confirms, finish the proof.
ots upgrade batch-c0.txt.ots
ots verify batch-c0.txt.ots

# 5. Get an RFC 3161 token for the same digest from your chosen TSA.
# 6. Send batch-c0.txt, the .ots proof, and the token to the custodian.
# 7. Record all of it as ledger entry #1.
```

Note that step 3 is a network broadcast. That is why it is in this package and not in any agent's hands.

## Open items requiring human verification

| Item | Status | Verification step |
|---|---|---|
| Open decision 4 (receipt/log trust substrate) | **Unresolved** in Rev 7 §35; this package proposes a resolution for the *evaluation-commitment* use only | Human ratifies; note that Bet 23's public receipt log is a *separate* question this does not settle |
| RFC 3161 fit; choice of TSA and its terms | `[UNVERIFIED]` — no RFC body or provider terms were fetched; none recommended | Human reads the current RFC/provider material, selects a TSA, and records mechanism fit, terms, trust chain, jurisdiction, and cost |
| OpenTimestamps client syntax, upgrade procedure, and latency | `[UNVERIFIED]` in this closure | Human follows the current official client instructions and validates the commands on a throwaway file before any campaign artifact |
| Rekor retention, removal, and privacy guarantees | `[UNVERIFIED]`; absence from this run's retrieved page is not proof that no policy exists | Human checks the current official service policy before any entry; absent an affirmative guarantee, treat publication as irreversible and do not expose confidential membership |
| Whether to use Rekor's public log | Held in reserve | Requires a deliberate decision on irreversible public disclosure (§28.4, open decision 4) |
| `ledger/CANONICAL_HASHES.md` accuracy | Orchestrator-owned; **provisional** | Recompute at ceremony time. A mismatch is a stop-and-dispute event, not a rounding error |
