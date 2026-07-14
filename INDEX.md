---
generated-by: Codex G0 owner (NTM session `monkeybee-pdf-mass-context-repo--g0`)
date: 2026-07-14
inputs:
  - AGENTS.md
  - OVERNIGHT_GOAL.md
  - repository file inventory excluding .ntm/** at 2026-07-14T16:23:35+02:00
  - DISPUTES.md
  - ledger/ORCHESTRATION_STATE.md
  - ledger/RUN_LEDGER.md
  - ledger/prompts/OWNER_MARCHING_ORDERS.md
  - ledger/prompts/G0_REVIEW.md
  - ledger/reviews/G0_REVIEW.md
status: PROPOSED
evidence-status: provisional-pending-substrate
owner-fsm: DONE
---

# MonkeyBee Campaign Repository Index

This is a navigation aid, not a new authority layer. Resolve disagreements through the hierarchy in `AGENTS.md` and preserve them in `DISPUTES.md`. The manifest enumerates every regular file outside `.git/**` and `.ntm/**` present at the snapshot above. The `.ntm/**` class is recorded separately because live control-plane instances change as panes start and stop.

## Start here

1. Read `AGENTS.md` for repository law and the authority hierarchy.
2. Read the active goal, currently `OVERNIGHT_GOAL.md`.
3. Read `MONKEYBEE_CAMPAIGN_CHARTER_v1.md`, then the goal-specific authority chain.
4. Read `DISPUTES.md` before acting on absent inputs or conflicting instructions.
5. Read the relevant owner checkpoint under `ledger/owners/` before changing an owned artifact.

## Classification key

| Class | Meaning |
|---|---|
| Operating law | Governs agent conduct and the active run. |
| Campaign canon | Governs campaign stages, gates, findings, or rationale; read-only at v1.0. |
| Domain canon | Governs PDF-engine planning content until superseded through the authorized extraction. |
| Definition canon | Governs the meaning and evidence burden of alienness claims. |
| Cautionary canon | Supplies a failure catalog; it does not govern MonkeyBee domain semantics. |
| Generated campaign artifact | New, provisional work subject to review and its stated owner scope. |
| Operational ledger | Provisional routing, provenance, or run-state evidence; not domain law. |
| Local control plane | Ephemeral runtime support; not campaign substrate. |

## Repository manifest

| Path | Class and role | Status / authority | Mutation and owner |
|---|---|---|---|
| `AGENTS.md` | Operating law; conduct, hierarchy, reading order | Seed v1.0 plus proposed G0 extension | Preserve seed rules; G0 extension permitted |
| `INDEX.md` | Generated campaign artifact; repository navigation | PROPOSED; non-authoritative map | G0-owned now; G8 regenerates at final gate |
| `OVERNIGHT_GOAL.md` | Operating law; active document-space assignment | Read-only run authority | Human-owned |
| `MONKEYBEE_CAMPAIGN_CHARTER_v1.md` | Campaign canon; cycles, goals, gates, constraints | v1.0 read-only canon | Human/change-control successor only |
| `CYCLE_0_WORK_ORDER.md` | Campaign canon; Cycle 0 routing and acceptance law | v1.0 read-only canon | Human/change-control successor only |
| `AUDIT_FINDINGS_LEDGER.md` | Campaign canon; finding provenance, grade, status, fix path | v1.0 read-only canon | Append only in a separately authorized audit round |
| `CAMPAIGN_CHARTER_REASONING.md` | Campaign canon; rationale and strategic corrections | v1.0 read-only canon | Human/change-control successor only |
| `MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md` | Domain canon; source plan | Read-only; below the Charter set | New v8/shell artifacts may supersede it section by section |
| `pre_claude_code_alien_artifact.md` | Definition canon; pre-agent contrast | Read-only canon | Human-owned |
| `post_agent_alien_artifact.md` | Definition canon; post-agent standard | Read-only canon | Human-owned |
| `frankensim_alienartifactness_reaudit.md` | Cautionary canon; adversarial failure catalog | Read-only canon | Human-owned |
| `DISPUTES.md` | Generated campaign artifact; authority conflicts and unavailable evidence | DRAFT; resolutions await ratification | Shared orchestrator-owned artifact; do not silently rewrite |
| `reports/INGEST_REPORT.md` | Generated campaign artifact; G0 read/verification record | PROPOSED; review findings resolved | G0-owned |
| `ledger/CANONICAL_HASHES.md` | Operational ledger; canonical byte baseline | DRAFT and provisional | Orchestrator-owned; mismatch is stop-and-dispute |
| `ledger/ORCHESTRATION_STATE.md` | Operational ledger; owner scopes and routing snapshot | DRAFT and dynamic | Orchestrator-owned |
| `ledger/RUN_LEDGER.md` | Operational ledger; append-oriented run events and telemetry | DRAFT and provisional | Orchestrator-owned; corrections identify prior entries |
| `ledger/prompts/OWNER_MARCHING_ORDERS.md` | Operational ledger; shared owner execution contract | DRAFT and provisional | Orchestrator-owned instruction artifact |
| `ledger/prompts/G0_REVIEW.md` | Operational ledger; fresh-review lens and writable review path | DRAFT; review filed | Orchestrator-owned instruction artifact |
| `ledger/reviews/G0_REVIEW.md` | Operational ledger; fresh-context G0 findings packet | DRAFT; reviewer terminated after filing | Reviewer-owned; G0 reads and dispositions only |
| `ledger/owners/G0_STATE.md` | Operational ledger; G0 owner checkpoint | PROPOSED; `DONE` | G0-owned |

## Non-normative local control-plane class

These files exist in the working directory but are locally excluded from campaign versioning and per-file manifest coverage. Their instance count may change without changing campaign truth.

| Path class | Runtime role | Status |
|---|---|---|
| `.ntm/**` | Pane logs, process records, provider backoff state, spawn metadata, and related local runtime support | Ephemeral and non-normative; excluded from stable per-file count |

## Named inputs unavailable in this checkout

| Expected path | Why it matters | Handling |
|---|---|---|
| `ALIEN_ARTIFACT.md` | Named evidence for audit row R2-N7 | `SOURCE-UNAVAILABLE`; see `DISPUTES.md` D-002 |
| `PROJECT_OVERVIEW.md` | Named evidence for audit row R2-N8 | `SOURCE-UNAVAILABLE`; see `DISPUTES.md` D-002 |

Neither path may be reconstructed from related material or model memory. If restored, read and hash the exact artifact before using it.

## G0 handoff route

G0's owned evidence is `reports/INGEST_REPORT.md`, with phase in `ledger/owners/G0_STATE.md`. The fresh packet is `ledger/reviews/G0_REVIEW.md`; all five findings are resolved and G0 is `DONE`.
