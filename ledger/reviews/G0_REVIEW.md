---
generated-by: G0 fresh-context reviewer (Claude Code pane `monkeybee-pdf-mass-context-repo--g0review`)
date: 2026-07-14
inputs:
  - AGENTS.md
  - OVERNIGHT_GOAL.md
  - INDEX.md
  - reports/INGEST_REPORT.md
  - ledger/owners/G0_STATE.md
  - AUDIT_FINDINGS_LEDGER.md
  - ledger/prompts/G0_REVIEW.md
  - ledger/prompts/OWNER_MARCHING_ORDERS.md
  - ledger/ORCHESTRATION_STATE.md
  - ledger/CANONICAL_HASHES.md
  - ledger/RUN_LEDGER.md
  - DISPUTES.md
  - MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md (cited regions only)
status: DRAFT
evidence-status: provisional-pending-substrate
---

# G0 Fresh-Context Review Packet

**Model identity (observed, not asserted):** `claude-opus-4-8`, effort `xhigh`. Verified in this pane's own process arguments — `/home/joseph/.local/bin/claude --dangerously-skip-permissions --model claude-opus-4-8 --effort xhigh` — and in the TUI, which reports Opus 4.8. This independently corroborates the `ledger/RUN_LEDGER.md` agent-lifecycle row for `YellowSpring`.

**Declared lens:** `evidentiary-reproducibility` — can a fresh agent reproduce every G0 read-state, authority classification, absence claim, and Grade-A disposition from the cited local inputs without trusting the author?

**Final FSM state:** `FILE-GRADED-FINDINGS -> TERMINATED`.

**Findings:** Grade A — 1. Grade B — 1. Grade C — 3.

**Reviewer scope:** No artifact under review was edited. No web, Beads, comparator tool, measurement, prohibited-processor material, source work, commit, or push was used. The only file written is this packet.

---

## 1. What reproduced

Every check below was re-run from scratch against the local artifacts. Unless noted, results are byte- or count-exact against what `reports/INGEST_REPORT.md` claims.

| Claim under test | Result |
|---|---|
| Canonical byte baseline, 9 of 9 | Reproduced. All nine SHA-256 values recomputed and matched `ledger/CANONICAL_HASHES.md` exactly. |
| AGENTS seed preserved, append-only | Reproduced. `git show HEAD:AGENTS.md` is 5,816 bytes; the working file's first 5,816 bytes hash identically (`31763f96…3606b`). `git diff --numstat` reports `18 0 AGENTS.md` — eighteen insertions, zero deletions. Every seed rule 0–13, the truth hierarchy, the reading order, and the file inventory survive verbatim. |
| Canonical inputs unmodified | Reproduced. `AGENTS.md` is the only tracked file modified, and it is the one file the goal authorizes G0 to extend. |
| Ten tracked seed files | Reproduced. `git ls-tree HEAD` returns exactly ten Markdown files. |
| Absent inputs not reconstructed | Reproduced. `ALIEN_ARTIFACT.md` and `PROJECT_OVERVIEW.md` are absent; no G0 artifact contains substitute content for either, and both are handled as `SOURCE-UNAVAILABLE` under `DISPUTES.md` D-002. |
| Grade-A row coverage | Reproduced. The Grade-A set in `AUDIT_FINDINGS_LEDGER.md` is exactly {R1-1, R1-3, R1-4, R1-5, R1-6, R1-7, R1-10, R2-N1, R2-N2, R2-N3, R2-N4, R2-N7} = 12 rows. The register carries all 12. Nothing was silently dropped. |
| `.ntm/` classification | Reproduced. Treated as non-normative local control-plane state in `INDEX.md`, the run ledger, and AGENTS rule 19. Not cited as campaign evidence anywhere. |
| Claim-vocabulary legality | Reproduced. Zero whole-word hits for `best`, `complete`, `fastest`, `mogged` across `INDEX.md`, `reports/INGEST_REPORT.md`, `ledger/owners/G0_STATE.md`, and the AGENTS extension. |
| Clean-room hygiene | Reproduced. Zero mentions of any processor on the prohibited list, as that list is enumerated in AGENTS rule 8, across every G0 output. |
| `git diff --check`, upstream tracking | Reproduced. Formatting passes; `origin/main` exists and is the tracked upstream. |

Eleven of the twelve Grade-A rows were re-derived independently against Rev 7. Ten reproduce in full; R1-1 reproduces in part (Finding A-1). R2-N7 is genuinely untestable here, and the report says so rather than guessing.

The numeric claims are exact, not approximate. `idempoten*` occurs on 25 lines / 30 tokens and `nonce*` on 24 lines / 38 tokens, precisely as R1-10's disposition states. `steward` = 25 tokens, `scout` = 9, `two-person` = 1, as R1-5 states. The bounded Appendix B search (local lines 7585–7712, B.1 through B.4) returns zero occurrences of `DocumentViewId`, `RevisionGraphId`, `DerivationId`, and `ExpectedStateId`, while those identifiers occur on 41, 27, 17, and 24 lines respectively elsewhere in Rev 7 — the drift is real and the bound is honest. The R2-N4 sketch analysis is not merely restated but correct: `WorkContext<'a>` stores `limits: &'a Limits`, and `child<'b>` returns `WorkContext<'b>` with no storage parameter and no arena, so the `// intersects limits` comment at local line 7259 cannot describe what the signature permits; `interior mutability` occurs zero times document-wide, so the shared `&DiagnosticCollector` against §10.4's non-re-entrancy claim (local line 1811) is likewise unaddressed.

I also attacked the absence claims with vocabulary the report did not use, because a single missed synonym would flip a Grade-A row. R2-N2 survives: `HashMap`, `hash map`, `keyed hash`, and `randomized hash` all return zero, and the lone `DoS-resistant` hit is `ReDoS-resistant`, about regular expressions, exactly as characterized. R1-6 survives: `responsible disclosure`, `security.txt`, `bug bounty`, and whole-word `CERT` all return zero, and the 29 `disclosure` hits are all data/privacy-disclosure vocabulary, never a security-response policy.

This is careful work. The findings below are narrow.

---

## 2. Grade A — confirmed defect (1)

### A-1. R1-1 is dispositioned `CORROBORATED`, but only one of its two conjuncts was tested

**Evidence.** `AUDIT_FINDINGS_LEDGER.md` R1-1 (Round 1 table) is a compound finding with two clauses joined by `; also`:

1. Appendix B report examples violate §10.6 identity laws — zero occurrences of the four identity IDs across B.1–B.4;
2. *"also falsifies §0.6 check-8's audit-coverage claim."*

The register cell in `reports/INGEST_REPORT.md` §4 for R1-1 addresses clause 1 in full and never mentions §0.6, check-8, or the audit-coverage claim. A search of the whole report for `0.6`, `check-8`, and `audit coverage` returns zero hits. The row is nonetheless marked `CORROBORATED`, and §4's summary counts it among the "11 of 12 Grade-A rows … corroborated."

The report defines `CORROBORATED` as "the named text or absence was reproduced in the artifact available here." For a compound finding, that has to mean both conjuncts. It does not here.

The second conjunct is testable and, as it happens, corroborable. Rev 7 §0.6 (local line 125) asserts "Revision seven applies eight classes of check to the integrated whole," and check-8 (local line 134) is a **Document audit** covering "broken internal references, stale identifiers … and contradictions." Appendix B's total omission of four identity fields that §10.6 requires is precisely such a contradiction, and the claimed audit did not catch it. So the defect is not a wrong conclusion — it is an asserted verification that was never performed.

**Why this matters under the lens.** This is the one place in G0's evidence chain where the report claims more coverage than it did. It is a small instance of exactly the failure class the campaign exists to prevent: a claim that does not carry its own reasons for trust. Left as-is, G1 inherits R1-1 believing both halves were checked, and the §0.6 self-audit falsification — which is the meta-finding, the one that says the plan's own review process missed this — silently drops out of the fix scope.

**Minimal repair.** In the R1-1 evidence cell, append the second conjunct's evidence: Rev 7 §0.6 check-8 (local line 134) claims a document audit covering stale identifiers, broken internal references, and contradictions; the reproduced Appendix B absence falsifies that coverage claim for the integrated whole. If the G0 owner prefers not to adjudicate the falsification, re-grade the row `CORROBORATED-IN-PART`, name the untested conjunct explicitly, and adjust §4's summary sentence. Either repair is a few lines and touches only G0-owned text.

---

## 3. Grade B — probable defect (1)

### B-1. The `INDEX.md` manifest enumerates ephemeral `.ntm/` files individually, so its coverage claim and the "23 of 23" self-check are already unreproducible

**Evidence.** `INDEX.md` states: "The manifest covers every regular file outside `.git/**` present at the snapshot above," snapshot `2026-07-14T16:08:15+02:00`. `reports/INGEST_REPORT.md` §6 records the matching self-check: "Repository manifest | 23 of 23 current non-`.git` files represented in `INDEX.md`."

Both were true when written. Neither reproduces now. A fresh `find . -path ./.git -prune -o -type f -print` returns **25** files. The two not in the manifest are `.ntm/logs/cm-monkeybee-pdf-mass-context-repo--g0review.log` and `.ntm/pids/cm-monkeybee-pdf-mass-context-repo--g0review.pid` — created at 16:09 by the spawn of *this reviewer*, one minute after the snapshot.

The G0 owner did nothing wrong at its timestamp, and the snapshot is honestly declared. The defect is in the method: enumerating ephemeral control-plane state file-by-file inside a manifest that also asserts total coverage guarantees the manifest is wrong for every subsequent reader, and guarantees it drifts further with every pane the run spawns. Under AGENTS rule 17 ("make verification reproducible"), a coverage claim that no later agent can re-derive is a claim that has to be trusted rather than checked. The next reader who runs the count sees a 2-file gap and cannot distinguish "stale manifest" from "an owner wrote outside its scope" without reconstructing the spawn history.

**Minimal repair.** In `INDEX.md`, replace the four per-file `.ntm/` rows with a single glob row (`.ntm/**` — local control-plane state, ephemeral, non-normative, count varies with live panes), and scope the coverage sentence to campaign substrate: every non-`.git`, non-`.ntm` file is enumerated; `.ntm/**` is classified as a class, not a list. The self-check then becomes a claim a fresh agent can reproduce at any time. Rule 19 is still satisfied — `.ntm/`'s existence and classification remain recorded here and in the run ledger.

---

## 4. Grade C — judgment (3)

### C-1. R1-5's evidence cell reports a token count against a ledger row that is only reproducible as a line count, without the convention note it applied to R1-10

`AUDIT_FINDINGS_LEDGER.md` R1-5 claims "stewards ×23." The register cell reports "25 `steward` tokens." Both numbers are correct — `steward` occurs 25 times across 23 lines — but the report reconciles them nowhere. This is the same counting-convention ambiguity the report carefully surfaces for R1-10 ("the ledger's '~25/~23' is reproducible as an approximate line count, not as a raw token count"), applied inconsistently one row earlier. A verifier who greps `-c` gets 23 and thinks the report is wrong; one who greps `-o | wc -l` gets 25 and thinks the ledger is wrong. The underlying finding — §35.1's seven assumptions contain zero staffing, recruitment, cost, or degradation entries — is solid and I reproduced it exactly.

**Minimal repair.** Add the same parenthetical to R1-5: `steward` = 25 tokens on 23 lines; the ledger's "×23" is the line count.

### C-2. R1-7's UTF-8 conjunct rests on one phrase search that has an unacknowledged near-miss

The register reports zero hits for `UTF-8 text string`, which is literally true. But Rev 7 local line 5230 says "explicit UTF-8 and byte-string distinctions" — the concept is not wholly absent from the plan, only the PDF 2.0 normative feature. A fresh verifier who searches the broader term finds a hit and cannot tell from the register whether R1-7's UTF-8 conjunct survives it. AGENTS rule 16's requirement to record search vocabulary is met; the issue is that a single-vocabulary absence search over a synonym-rich concept is the weakest link in an otherwise strong evidence chain.

**Minimal repair.** Note the line-5230 hit in R1-7's cell and state why it does not satisfy the finding — the plan distinguishes UTF-8 from byte strings generally but never names the PDF 2.0 UTF-8 text-string feature.

### C-3. The self-check's "declared owned paths" claim is not reproducible against the routing table it appears to reference

`reports/INGEST_REPORT.md` §6 asserts "G0 additions are confined to declared owned paths." `ledger/ORCHESTRATION_STATE.md`'s owner table lists G0's owned files as `INDEX.md`, `reports/INGEST_REPORT.md`, and the permitted AGENTS extension — it does **not** list `ledger/owners/G0_STATE.md`, which G0 wrote. The path *is* legitimately declared: `ledger/prompts/OWNER_MARCHING_ORDERS.md` mandates persisting the FSM in `ledger/owners/GN_STATE.md`, and the `RUN_LEDGER.md` lifecycle row includes it in G0's scope. So there is no actual scope violation — but a reviewer checking scope against the orchestration table alone finds a file outside it, and has to consult two more artifacts to clear it.

`ORCHESTRATION_STATE.md` is orchestrator-owned, so G0 cannot repair it, and G0 *did* surface the related staleness (its §5 notes the file "remained at its earlier G0 `INGEST` routing snapshot"). It did not surface this specific ownership-column gap.

**Minimal repair.** Orchestrator: add `ledger/owners/G0_STATE.md` to G0's "Files owned" cell and advance the phase to `SUBMIT-FOR-REVIEW`. G0: extend the §5 mismatch bullet to name the ownership-column gap as well as the phase gap.

---

## 5. Assessment against the review order's five questions

- **AGENTS extension preserves every seed rule** — yes, byte-verified. The extension is purely additive (rules 14–20 plus a handoff paragraph), carries its own provenance block, and its rule 14 explicitly subordinates `INDEX.md` to the seed truth hierarchy rather than competing with it.
- **Dynamic files are classified** — yes. `.ntm/` is non-normative in AGENTS rule 19, `INDEX.md`, and the run ledger. See B-1 for the enumeration method, not the classification.
- **Canonical inputs remain unmodified** — yes, all nine hashes match; only the authorized `AGENTS.md` extension exists among tracked files.
- **Absent inputs are not reconstructed** — yes. This is handled well: `SOURCE-UNAVAILABLE`, dependent row named, no substitute sourced from the re-audit or from model memory, and D-002 carried forward to the ratification queue.
- **All Grade-A rows have an honest disposition** — 11 of 12, and the 12th (`R2-N7`) is honestly untestable. R1-1's disposition overstates its coverage; that is Finding A-1.
- **Wake-up navigation route is usable** — yes. `AGENTS.md` → `INDEX.md` → Charter → `OVERNIGHT_GOAL.md` → Work Order + Audit Ledger resolves, and `INDEX.md`'s "Start here" adds `DISPUTES.md` and the owner checkpoints. A fresh agent can state the active goal, the authority chain, the files it may change, and both unavailable inputs after one pass. The C1 delta plan is not yet findable because G3 has not run — that is a run-state fact, not a G0 defect.

## 6. Termination

Findings filed: A = 1, B = 1, C = 3. No packet repair attempted; no artifact under review edited. The G0 owner triages these before entering `REVISE`.

`TERMINATED`.
