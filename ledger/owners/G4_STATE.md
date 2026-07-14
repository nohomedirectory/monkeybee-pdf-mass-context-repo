---
generated-by: Claude G4 owner (NTM session `monkeybee-pdf-mass-context-repo--g4`, `claude-opus-4-8`)
date: 2026-07-14
inputs:
  - AGENTS.md
  - INDEX.md
  - MONKEYBEE_CAMPAIGN_CHARTER_v1.md
  - OVERNIGHT_GOAL.md
  - CYCLE_0_WORK_ORDER.md
  - AUDIT_FINDINGS_LEDGER.md
  - ledger/prompts/OWNER_MARCHING_ORDERS.md
  - ledger/ORCHESTRATION_STATE.md
  - ledger/RUN_LEDGER.md
  - ledger/owners/G0_STATE.md
  - DISPUTES.md
  - MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md (§0.2, §3, §4.6–4.7, §10.10, §11.9, §13.9–13.10, §24.12–24.16, §26.2–26.3, §27–27.4, §28.3, §30.5–30.10, §31.4–31.10, §33, §35)
status: PROPOSED
evidence-status: provisional-pending-substrate
---

# G4 Owner State

- owner: G4 — traceability matrix and C2–C7 cycle briefs
- phase: `SUBMIT-FOR-REVIEW`
- exclusive paths: `reports/TRACEABILITY_MATRIX.md`, `plans/cycle_briefs/**`, `ledger/owners/G4_STATE.md`
- **this file is the single normative home of the G4 owner phase.** No owned artifact's front matter states owner phase; artifact headers carry artifact-local status only (AGENTS rule 18; Rev 7 §29.5 single-source principle).
- terminal phase for this turn: `SUBMIT-FOR-REVIEW`. A fresh reviewer must file a finding packet before `REVISE`.

## Transition record

| Phase | Time (Europe/Berlin) | Checkpoint |
|---|---|---|
| `INGEST` | 2026-07-14T16:36+02:00 | Required reading order completed; authority chain fixed; checkpoint persisted before any owned-artifact drafting |
| `DRAFT` | 2026-07-14T16:44+02:00 | On-demand Rev 7 sections read; nine candidate gaps confirmed by grep against the Charter; matrix drafted first per the priority ladder (OVERNIGHT_GOAL §5.4 places the matrix above the briefs), then C2–C7 |
| `SELF-CHECK` | 2026-07-14T17:02+02:00 | Scope, provenance, clean-room, claim-vocabulary, cross-reference, and zero-orphan checks run; two root corrections received and applied; four unscoped Rule-13 sites repaired; matrix reverse-coverage closed |
| `SUBMIT-FOR-REVIEW` | 2026-07-14T17:08+02:00 | All seven artifacts on disk and internally consistent; findings ready for fresh-context review |

## Declared outputs

| Artifact | Status | Size |
|---|---|---|
| `reports/TRACEABILITY_MATRIX.md` | PROPOSED | 50 requirement IDs, bidirectional, 9 graded findings, reality-check answered |
| `plans/cycle_briefs/C2.md` … `C7.md` | PROPOSED | Six briefs, 1–3 pages each |
| `ledger/owners/G4_STATE.md` | this file | — |

No other path was created, edited, or read-for-write. `git status --short` shows other owners' paths (`constitution/`, `decisions/`, `human_actions/`, `shell/`, `reports/FIX_APPLICATION.md`, `plans/CYCLE_1_DELTA_PLAN.md`, sibling `ledger/owners/*`) as theirs and untouched by G4.

## Root corrections received mid-turn, and their disposition

| # | Correction | Disposition |
|---|---|---|
| 1 | `reports/TRACEABILITY_MATRIX.md` declared `owner-fsm: SUBMIT-FOR-REVIEW` while this checkpoint said `DRAFT` and the briefs did not exist — a disk-state inconsistency | `ACCEPTED — RESOLVED`. The header now carries `artifact-status` only and names this file as the normative home of owner phase. The finished matrix was not weakened; only the header changed |
| 2 | `plans/cycle_briefs/C5.md` carried the unscoped Rule-13 token in "CDR product complete"; disposition every `best\|complete\|fastest\|mogged\|supremacy` hit across all G4 Markdown and record the scan | `ACCEPTED — RESOLVED`. My first vocabulary scan omitted `complete` from the regex — the scan was the defect, not just the phrase. Full scan run and dispositioned below; the G1 survival-wedge requirement is preserved by citation to Charter §5/C5 rather than by restating the claim adjective |

## Claim-vocabulary scan (AGENTS rule 13) — full disposition

Scan: `grep -nioE "\b(best[a-z-]*|complet[a-z]+|fastest|mogged|supremac[a-z]+)\b"` over all eight G4-owned Markdown files. 56 hits, every one dispositioned.

**REPAIRED — unscoped claim vocabulary in G4's own prose (4 sites):**

| Site | Was | Now |
|---|---|---|
| `C5.md` title | "the CDR product completes" | "the CDR wedge reaches its Charter endpoint" |
| `C5.md` §1 lede | "content disarm and reconstruction, complete" | "reaches the content-disarm-and-reconstruction deliverable boundary that Charter §5/C5 defines," plus an explicit no-claim sentence bounding it to the R3 envelope |
| `C5.md` evidence table | "**CDR product complete**" | "**CDR deliverable boundary reached** (Charter §5/C5)" |
| `C5.md` §1 scope | "Decryption-matrix completion" | "The remaining decryption matrix: the public-key security handlers that C1's standard-handler read path left open" |
| `C6.md` §1 / §2 | "JPX, JBIG2, and CCITT completion"; "the complete blend set" | "JPX, JBIG2, and CCITT land here"; "every blend mode the R4 profile admits" |

Rationale: the Charter itself uses "complete" for the CDR deliverable (§2, §5/C5), but AGENTS rule 20 forbids generated prose from strengthening a source claim, and rule 13's tie-breaker is to understate. Citing the Charter's deliverable boundary preserves the G1 requirement without G4 asserting product completeness in its own voice.

**KEEP — with recorded rationale (5 classes):**

| Class | Instances | Why it is not a rule-13 violation |
|---|---|---|
| `PDF-completion FieldDefinitionId`, "completion field / denominator / measurement" | 29 | The name of the comparative field **Q2 asks about**, verbatim from Charter §0 and §2/G3. Rule 13 carves out "properly scoped claim structures (Rev 7 §10.3/§24)" and `FieldDefinitionId` is that structure. The matrix's argument is that this field is undefined and may not be leadable — the opposite of a supremacy claim |
| "supremacy doctrine / lanes / headline / -lane results" | 14 | Names of Rev 7 §24.12–24.16 constructs and of Charter §0's own Q2 wording. Citations to canonical section content, not claims |
| "median and best outcomes", "best-of-N" | 4 | Required production-ledger field names from Rev 7 §33.8 and the §34.9 close-gate law. Deleting them would misquote the obligation |
| "provenance completeness" | 1 | §33.9's own metric name |
| "if every cycle completes as briefed"; "Completed a clause-by-clause standards coverage matrix" | 5 | Verbatim quotes: the first is OVERNIGHT_GOAL §3/G4's reality-check question, the second is Rev 7 §0.2's statement of what the plan has **not** done |

## Self-check evidence

- **Scope:** only the three owned paths written. No canonical file, no other owner's path, no `DISPUTES.md`, no ledger file outside `ledger/owners/G4_STATE.md`.
- **Clean-room (AGENTS rule 8):** `grep -nioE "pdf\.js|pdfbox|mupdf|poppler|pdfium|itext|qpdf|ghostscript|lopdf|pdf-rs|hayro|krilla|stet|pdfpurr|oxidize|pdfluent|pdf_oxide|printpdf"` over all G4 artifacts → **zero hits**. No processor is named anywhere in G4's output; competitor material stays a citation to Rev 7 §24.13. No prohibited source was fetched, read, or cited.
- **No measurements, no beads, no code, no external action, no SpecCard bodies.** Briefs name consequence-contract *families* in prose; contract IDs are authored in the delta plans under §10.10, never here.
- **Provenance headers:** present on all seven owned artifacts (`generated-by`, `date`, `inputs`, `status`, `evidence-status`).
- **Cross-reference:** 50 requirement IDs defined in the matrix; 18 cited across the briefs; **zero cited-but-undefined**. Nine finding IDs defined; all nine now cited by at least one brief.
- **Zero-orphan (both directions):** 50 defined → 40 discharged by a named producer in the reverse table + 14 forward orphans + 1 discharged by reference (overlapping counts resolve to 50). **Unaccounted: zero.** All IDs are written out in full so the audit is reproducible by grep rather than by reading prose. Two self-inflicted defects were caught here and fixed: a `Q2-CMP-1…6` range notation that defeated mechanical checking, and five IDs missing from the reverse table.
- **De-slopification:** manual line-by-line pass. Five superlatives that were G4's own editorializing about G4's own artifacts ("soundest lane", "strongest grounding artifact", "highest-leverage item") were replaced with factual statements ("the only lane whose prerequisites all exist"). Superlatives that are canonical quotes ("strongest ordinary replacement", §33.6) were kept.

## Findings produced (for root's routing, not for G4 to file)

Nine graded findings against the **campaign layer**, not against Rev 7's domain content. G4 owns none of the implicated documents and has written to no shared dispute channel.

| ID | Grade | One line |
|---|---|---|
| F-1 | A | Flagship G is scheduled at C7; its capability surface (Bet 16 metered form actions, static XFA projection) is built by no cycle and is placed outside R0–R4 by Rev 7 §3.5. Charter grep for `xfa\|bet 16\|form.action\|javascript\|postscript` → zero hits |
| F-2 | A | Q2's "plus supremacy-lane results" names lanes S1/S3/S4/S6; no cycle executes them, while C6 calls its perf slice "the S6/S1 prerequisite" — the §34.4 envelope-dependency pattern, one layer up from R2-N1 |
| F-3 | A | The Q2 completion field has no lane in §24.15, no denominator, and no field-side instrument. §0.2 lists the clause-by-clause coverage matrix among what Rev 7 has **not** done. C6's scorer reads MonkeyBee's own tagging; nothing scores the field, and §24.12 rule 4 forbids inferring coverage from competitor documentation |
| F-4 | B | §24.16's discovery stage 2 (execute search, characterize, run the challenge window, freeze a `CompetitorDiscoveryReportId`) is unscheduled and its scouts are unstaffed. Without it, §24.16 caps Q2 at `named_set_lead` |
| F-5 | B | Four §33 obligations that constitute the Artifact rung — §33.3 boundary, §33.9 integration surplus, §33.12 consequence-compression audit, §33.13 maturity taxonomy — have no producer. Charter greps → zero |
| F-6 | C | Operational closure (§33.11) has a producer (C4 release engineering) but no gate tests its metric set |
| F-7 | B | Precommitment covers discovery but not evaluation (`EvaluationProtocolId`, §33.4); six of thirteen §33.16 bundle contents have no upstream producer; §35's reference-class row is routed nowhere |
| F-8 | B | Seeded-defect detection-rate trials are cited by Charter §7 as Q3 grounding evidence and gated nowhere; claim demotions are never required to be reported |
| F-9 | C | Object hygiene: the C7 foundry distribution is Foundry-rung evidence and the C4 Evolution Trial is Lineage-rung evidence, for rungs the campaign does not claim (§33.17 forbids borrowing). And nobody owns the post-submission claim refresh (§33.2 contemporaneous vintage; §24.16 lapse law) |

**Reality-check answer (matrix §7), stated honestly:** Q3 is answerable, conditionally — the package as specified is missing instruments its own protocol requires (F-5), and those gaps are closable inside the existing cycle structure. **Q2, as worded in Charter §0, is not answerable by the campaign as briefed** — not because a cycle is expected to fail, but because the question names an instrument, a field, and a set of lanes that no cycle builds (F-1, F-2, F-3, F-4). What Q2 *can* honestly yield is Flagship H, the wild-tail ledger, which is fully provisioned and publishable whether MonkeyBee leads or trails. The remedy is a human decision at C0 about what Q2 is actually asking — and §24.16 makes it irreversible once the discovery protocol is committed, because a field definition authored after the search begins is not a predeclared field.

## Open risks

- Findings F-1 through F-4 implicate `MONKEYBEE_CAMPAIGN_CHARTER_v1.md`, which is read-only v1.0 canon (D-003). G4 wrote no successor and edited nothing. If a fresh reviewer sustains them, root should open dispute entries (D-004+) and consider whether G6's conditional Charter-successor path is triggered. **G4 does not self-route this.**
- All nine findings are one owner's judgment from one model family. They are falsifiable by exhibiting the missing producer, and they should be reviewed by a fresh context under the `Q2/Q3 zero-orphan audit` lens (`ledger/ORCHESTRATION_STATE.md` round 23) before the human acts on them.
- Two named inputs remain `SOURCE-UNAVAILABLE` (D-002). Neither is load-bearing for any G4 row.

## Next transition condition

`SUBMIT-FOR-REVIEW → REVISE` on receipt of a fresh-context finding packet. G4 stops here and returns control to root; no commit, no push, no reviewer spawned by this owner.
