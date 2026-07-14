---
generated-by: Codex G0 owner (NTM session `monkeybee-pdf-mass-context-repo--g0`)
date: 2026-07-14
inputs:
  - AGENTS.md
  - MONKEYBEE_CAMPAIGN_CHARTER_v1.md
  - CAMPAIGN_CHARTER_REASONING.md
  - CYCLE_0_WORK_ORDER.md
  - AUDIT_FINDINGS_LEDGER.md
  - OVERNIGHT_GOAL.md
  - MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md
  - pre_claude_code_alien_artifact.md
  - post_agent_alien_artifact.md
  - frankensim_alienartifactness_reaudit.md
  - DISPUTES.md
  - ledger/CANONICAL_HASHES.md
  - ledger/ORCHESTRATION_STATE.md
  - ledger/RUN_LEDGER.md
  - ledger/prompts/OWNER_MARCHING_ORDERS.md
  - ledger/prompts/G0_REVIEW.md
  - ledger/reviews/G0_REVIEW.md
status: PROPOSED
evidence-status: provisional-pending-substrate
owner-fsm: DONE
---

# G0 Ingest Report

## 1. Scope and method

G0 inventories the checkout, reads every tracked seed document, maps authority and mutation policy, and checks every Grade-A audit row against the evidence available in this checkout. It does not apply audit fixes assigned to G1 or alter canonical inputs.

The read proceeds in authority order, followed by a sequential read of each long-form document. Verification cites stable section identifiers and line-numbered local evidence. Absence claims use bounded searches over the named artifact and record the searched terms. Dynamic `.ntm/**` instances are excluded from stable per-file coverage and classified as local control-plane state; orchestration ledgers are operational state, not campaign authority.

## 2. Ingest baseline

At the initial checkpoint, `main` tracked `origin/main`. The ten tracked seed files were unchanged; only the orchestrator's `.ntm/` and `ledger/` artifacts were untracked. `INDEX.md`, `ALIEN_ARTIFACT.md`, and `PROJECT_OVERVIEW.md` were absent. During ingest, the shared orchestrator added `DISPUTES.md` and `ledger/CANONICAL_HASHES.md`; G0 read and classified both without changing them.

| File | Role and authority | Mutation policy | Read state |
|---|---|---|---|
| `AGENTS.md` | Repository operating law; live human instruction layer | G0 may extend while preserving every seed rule | READ |
| `MONKEYBEE_CAMPAIGN_CHARTER_v1.md` | Highest campaign document in the repository truth hierarchy | Read-only v1.0 canon | READ |
| `CYCLE_0_WORK_ORDER.md` | Cycle 0 execution authority and fix routing | Read-only v1.0 canon | READ |
| `AUDIT_FINDINGS_LEDGER.md` | Finding provenance and fix status | Read-only v1.0 canon | READ |
| `CAMPAIGN_CHARTER_REASONING.md` | Rationale companion to the Charter | Read-only v1.0 canon | READ |
| `OVERNIGHT_GOAL.md` | Active overnight assignment and deliverable law | Read-only run authority | READ |
| `MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md` | Domain source plan, below the Charter set | Read-only canon | READ |
| `pre_claude_code_alien_artifact.md` | Governing pre-agent definition | Read-only canon | READ |
| `post_agent_alien_artifact.md` | Governing post-agent definition | Read-only canon | READ |
| `frankensim_alienartifactness_reaudit.md` | Cautionary re-audit and failure catalog | Read-only canon | READ |

## 3. Authority map

The live human and `AGENTS.md` govern repository conduct. The Charter, Work Order, Audit Findings Ledger, and Charter Reasoning govern campaign staging and Cycle 0. Rev 7 governs domain content until the v8 extraction supersedes it section by section. The two alien-artifact definitions govern claim meaning. The FrankenSim re-audit is cautionary evidence and outranks any older `ALIEN_ARTIFACT.md` summary if that file later appears.

No `INDEX.md` existed at ingest, so this report began from the seed inventory and truth hierarchy in `AGENTS.md`. The ten-file tracked seed corpus and all current operational files have now been read. G0 created `INDEX.md` as a non-authoritative map; it does not alter the hierarchy.

## 4. Grade-A verification register

Disposition terms in this register mean:

- `CORROBORATED`: the named text or absence was reproduced in the artifact available here.
- `CORROBORATED-WITH-COUNT-NOTE`: the substance was reproduced and the ledger's approximate count needs a local counting convention.
- `SOURCE-UNAVAILABLE`: the finding's named source is absent, so the claim was not tested.

| ID | Disposition | Reproduced evidence |
|---|---|---|
| R1-1 | `CORROBORATED` | Rev 7 §10.6 requires exact `DocumentViewId`, `RevisionGraphId`, and `DerivationId` bindings across the relevant report families, plus an expected-state binding for each document input to a `TransformReceipt`. A search bounded from Appendix B.1 through B.4 returned zero occurrences of `DocumentViewId`, `RevisionGraphId`, `DerivationId`, and `ExpectedStateId`. B.3 role-labels roots but supplies neither the selected view nor expected state. The finding's second conjunct also reproduces: §0.6 check 8 says the integrated document audit covered stale identifiers, broken internal references, and contradictions; the Appendix B/§10.6 contradiction survived that audit, falsifying the stated coverage for the integrated whole. |
| R1-3 | `CORROBORATED` | Flagship D has adjacent bullets: “run an independent forensic tool” and “run an independently sourced forensic path whose shared parser/model/data lineage is disclosed” (local lines 6391–6392). The text does not state whether these are one path described twice or two distinct paths. |
| R1-4 | `CORROBORATED` | Rev 7 §9.1 says there is no unqualified universal semantic identity and makes meaning contingent on `SemanticScopeId`. Section 22.4 nevertheless promises byte identity from identical `SemanticStateId`, assets, versions, and profile. Neither §22.4 nor the document-wide `serialization-total` search supplies the missing scope-totality condition. |
| R1-5 | `CORROBORATED` | The plan contains 25 `steward` tokens on 23 lines, nine `scout` tokens, and one `two-person` token; the ledger's “stewards ×23” is the line count. Section 35.1 lists assumptions about representation, parsing, dependencies, testing, evidence cost, crates, corpora, and processor access, but no staffing, cost, recruitment, or honest-degradation assumption for the human independence ecology. |
| R1-6 | `CORROBORATED` | Document-wide case-insensitive searches returned zero for `CVE`, `embargo`, `coordinated disclosure`, `vulnerability disclosure`, and `security response`. Generic incident and advisory mentions exist, but they do not define intake, triage, embargo, disclosure, or claim-withdrawal policy. |
| R1-7 | `CORROBORATED` | Searches returned zero for `encrypted payload`, `unencrypted wrapper`, `PhoneticAlphabet`, `Phoneme`, `Prop_Build`, `UTF-8 text string`, and `PDF/VT`. Section 25.4 does contain the near-match “explicit UTF-8 and byte-string distinctions” for the C ABI (local line 5230), but it never names or inventories the PDF 2.0 UTF-8 text-string feature, so it does not satisfy that conjunct. The enumerations in §§16.8 and 23.12 omit encrypted-payload/unencrypted-wrapper documents, and §21.1 omits the named structure vocabulary. Separate searches also reproduce the Grade-C `/Tabs` and `NeedsRendering` omissions, but those are not counted as Grade-A evidence here. |
| R1-10 | `CORROBORATED-WITH-COUNT-NOTE` | `idempoten*` appears on 25 lines (30 tokens); `nonce*` appears on 24 lines (38 tokens). Thus the ledger's “~25/~23” is reproducible as an approximate line count, not as a raw token count. Rev 7 §29.5 rejects authoritative hand-maintained duplicates, while R1-1 supplies a concrete drift instance. The qualitative “4–6× each” characterization was not treated as a separate exact metric. |
| R2-N1 | `CORROBORATED` | The R0 Revision Autopsy required-consequence cell omits signature/`ByteRange` discovery while Workflow B Document Autopsy promises “signatures and byte ranges.” R2 promises source-preserving incremental writes, and §23.3 requires `DocMDP`/`FieldMDP`/field-lock classification before publication, yet the envelope table first assigns signature analysis to R3. This is the excluded-capability dependency prohibited by §34.4. |
| R2-N2 | `CORROBORATED` | Searches returned zero for `SipHash`, hash-flooding language, attacker-keyed hashing, and any `hasher` rule. The one generic DoS-resistant hit concerns regular expressions, and the ordered-structure hits concern semantic graph canonicalization. Section 26.7 discusses locality without a security condition on map/hash substitutions. |
| R2-N3 | `CORROBORATED` | The §11.2 limits table names bytes, graph size/depth, decoding, rendering, scripts, recovery, time, CPU, output, and diagnostics, but no canonicalization/symmetry work dimension. Section 22.3 uses SCC condensation and symmetry classes; §32 has a correctness/nondeterminism symmetry risk, not a work-budget dimension. |
| R2-N4 | `CORROBORATED` | Appendix A.2 stores `limits: &'a Limits`; `child` accepts `local: &'b Limits` and returns `WorkContext<'b>` while only a comment promises intersection. The sketch supplies no storage for a computed intersection or min-at-check rule. It also shares `&DiagnosticCollector`; §10.4 calls its mutation surface non-re-entrant but states no `Sync`/interior-mutability contract for parallel children. |
| R2-N7 | `SOURCE-UNAVAILABLE` | The finding is explicitly about statements in `ALIEN_ARTIFACT.md`, which is absent. The re-audit does establish its own supersession and the later F-01/F-02/F-04 evidence, but it cannot prove the exact absent file's wording. Shared dispute D-002 already records the gap and forbids reconstruction. |

Summary: 11 of 12 Grade-A rows are corroborated from available artifacts; one is source-unavailable; none is contradicted. This is a verification of the audit ledger, not application of its fixes.

## 5. Discrepancies and limits

- `AUDIT_FINDINGS_LEDGER.md` says its Round 2 scope included `ALIEN_ARTIFACT.md` and `PROJECT_OVERVIEW.md`, but neither file exists in this checkout. G0 verified the absence and relied on shared dispute D-002; it did not reconstruct or silently substitute either artifact.
- R1-10's approximate counts match line-bearing hits (25 and 24), while raw token counts are 30 and 38. This is a counting-convention clarification, not a contradiction of the duplication finding.
- The reviewer observed that the earlier `ledger/ORCHESTRATION_STATE.md` snapshot both lagged G0's phase and omitted `ledger/owners/G0_STATE.md` from the G0 files-owned cell. Root subsequently updated that shared file to list the checkpoint and route G0 to `REVISE`, bringing the records into agreement at revision intake. G0 then advanced its owned checkpoint to `DONE`; root retains ownership of any later orchestration update. G0 did not edit either orchestrator-owned ledger.
- The exact seconds of the first two owner transitions were not retained in their original checkpoints. `ledger/owners/G0_STATE.md` now records bounded times from the append-oriented run ledger instead of inventing precision; `SELF-CHECK` and later transitions use exact timestamps.
- Exact hosted model point-version evidence comes from the orchestrator ledger. The owner does not independently receive a model point-version API and therefore does not strengthen that claim.
- The G0 owner made no network fetch and contacted no prohibited source. The shared run ledger separately records one orchestrator process-methodology fetch. No comparator measurement, bead creation, or source-code generation occurred during G0.

## 6. Self-check and G0 handoff

Self-check results:

| Check | Result |
|---|---|
| Canonical byte baseline | 9 of 9 SHA-256 values match `ledger/CANONICAL_HASHES.md` |
| Repository manifest | 20 of 20 current non-`.git`, non-`.ntm` files represented; `.ntm/**` classified once and excluded from the stable count |
| AGENTS seed preservation | Original 5,816-byte prefix matches `HEAD:AGENTS.md`; extension is append-only |
| Scope | Current orchestration, marching-order, and owner-state records all name `ledger/owners/G0_STATE.md` within G0 scope; revision patches target only the four human-authorized paths |
| Formatting | `git diff --check` passes |
| Claim vocabulary | Zero hits for the four forbidden tokens named in AGENTS Rule 13 within G0 additions |
| Clean room | Zero prohibited-processor-name hits in G0 additions; no network or prohibited source was used by the G0 owner |
| Provenance | Both new campaign artifacts and the owner checkpoint carry required metadata; the AGENTS extension carries its inline provenance block |
| Git diff | Canonical hashes match 9 of 9; `AGENTS.md` is the sole tracked diff and remains append-only |
| De-slopification | Manual pass performed; no flagged formulaic pattern remains |

Revised owned artifacts:

- `AGENTS.md`: seed preserved; proposed navigation/evidence-hygiene extension appended.
- `INDEX.md`: every current non-`.git`, non-`.ntm` file classified; `.ntm/**` recorded once as an excluded local class.
- `reports/INGEST_REPORT.md`: authority map and all Grade-A dispositions.
- `ledger/owners/G0_STATE.md`: disk-first owner checkpoint with all five review dispositions.

No canonical input was edited, no Cycle 0 fix was applied, and no additional dispute file was created.

## 7. Fresh-review dispositions

| Finding | Triage | Warranted repair | Revision status |
|---|---|---|---|
| A-1 | Accepted | Expanded R1-1 to test and cite the §0.6 check-8 audit-coverage conjunct | `RESOLVED` |
| B-1 | Accepted | Replaced individual `.ntm/` rows and the unstable all-file count with a `.ntm/**` class exclusion and stable non-`.ntm` manifest | `RESOLVED` |
| C-1 | Accepted | Reconciled `steward` as 25 tokens on 23 lines and identified the ledger's ×23 convention | `RESOLVED` |
| C-2 | Accepted | Recorded the §25.4 UTF-8 near-match and explained why it is not the PDF 2.0 text-string feature | `RESOLVED` |
| C-3 | Accepted | Named the earlier routing ownership/phase gap and root's later shared-ledger correction; no shared file edited by G0 | `RESOLVED` |
