# OVERNIGHT GOAL — Cycle 0 Document-Space Execution

**Status:** Active goal for the overnight run
**Date issued:** 2026-07-14
**Governing documents:** MONKEYBEE_CAMPAIGN_CHARTER_v1.md · CYCLE_0_WORK_ORDER.md · AUDIT_FINDINGS_LEDGER.md
**Process reference:** https://agent-flywheel.com/complete-guide — consult it for any needed intuition on the planning methodology (plan space vs. bead space, fresh-eyes review, convergence detection, blunder-hunt repetition, de-slopification). All Flywheel skills and tools available to this instance may be used, **except as restricted in §1**.
**Mode:** PLAN SPACE ONLY, for the entire run. You are producing the campaign's planning and navigation substrate, not its implementation.

---

## 0. Parent goal

Execute the document-space portion of Cycle 0 so that when the human wakes (~8 hours):

1. The **Cycle 1 delta plan is complete** and has survived a heavy fresh-context review gauntlet (§7) — this is the single non-negotiable deliverable.
2. The **campaign document architecture is in place**: Constitution v8 extracted from Rev 7 with the ledgered fixes applied, shell corpus organized, cycle briefs and the Q2/Q3 traceability matrix written.
3. Every **human-bound action is packaged** and ready to execute in the first waking hour.
4. The **entire repo is navigable by any fresh agent** after one read of AGENTS.md.
5. A **run ledger and morning report** account honestly for everything done, not done, and disputed.

**Wake-up test:** a fresh agent, given only AGENTS.md, can find the C1 delta plan, understand its authority chain, and state what happens next — and the human can ratify decisions, send outreach packages, and start the beads conversion without reconstructing anything from memory.

## 1. Hard operating rules (violations invalidate the run)

1. **No beads, no code.** Do not invoke `br` or `bv` for creation. Do not write pseudo-bead inventories in markdown (the guide's anti-pattern — beads happen later, with the human, via the real tool). Do not create source files, Cargo manifests, CI configs, or repo scaffolding beyond documents. Trait/type sketches *inside* plan documents are permitted, matching Rev 7 Appendix A style.
2. **No SpecCard bodies.** The clean-room law (Rev 7 §4) makes rights-vetted SpecCards the only legal channel for ISO semantics, and the licensed source does not exist in this repo. You may build the card **registry**: card IDs, the R0-surface coverage map, the extraction protocol document, review templates. Every card slot is marked `PENDING-LICENSED-SOURCE`. Generating card semantic content from model memory is clean-room contamination and is forbidden — this is the #1 predicted failure mode of this run. Plan documents may discuss PDF semantics at Rev 7's own level of description; normative cards may not exist yet.
3. **No prohibited-source contact.** Never clone, fetch, read, or cite the source or documentation of existing PDF processors (pdf.js, PDFBox, MuPDF, Poppler, PDFium, iText, QPDF, Ghostscript, lopdf, pdf-rs, hayro, krilla, or anything on Rev 7 §4's prohibited list). Not "for reference," not "just the README." Contamination cannot be undone.
4. **No measurements.** No benchmarks, no competitor comparisons, no coverage scoring against other libraries, no downloading their artifacts. Measurement before the committed discovery protocols poisons the Q2 evidence chain permanently. Reading the register text already inside Rev 7 is fine; generating new comparative data is not.
5. **No external actions.** No emails, purchases, publishing, visibility changes, or postings. Draft everything; send nothing. Read-only web access is permitted for the process guide above and for public technical references needed by decision briefs (e.g., hash-function literature) — log every fetch in the run ledger. Rule 3 overrides this permission everywhere it applies.
6. **Canonical inputs are read-only.** Rev 7, the definitions, the FrankenSim re-audit, and the four v1.0 Charter-set documents are never edited in place. All outputs are new files with a provenance header (`generated-by`, `date`, `inputs`, `status: DRAFT | PROPOSED`). Improvements to v1.0 documents become `*_v1.1.md` files with a changelog section — never silent edits.
7. **Run ledger from minute one.** Create `ledger/` and log: session start, model/harness identity, every sub-agent spawn and death, every gauntlet round (lens, findings count, grades), disputes, fetches, failures, and token/cost telemetry where available. Label everything `provisional-pending-substrate` (the tamper-evident commitment channel is a human-bound day-zero item).
8. **Honesty rules.** No invented versions, ISO clause numbers, or competitor facts — mark anything unverifiable `[UNVERIFIED]`. If you disagree with an AUDIT_FINDINGS_LEDGER entry, write it up in `DISPUTES.md` with evidence; never silently skip a fix.
9. **Sub-agent hygiene.** One owner per subgoal; reviewers are always fresh-context (that is what makes them reviewers); no ringleader holds load-bearing state — state lives in files on disk, written incrementally so a crash loses minutes, not hours; stagger spawns.
10. **After any compaction: reread AGENTS.md.** Non-negotiable.
11. **De-slopify** every human-facing document as a final pass (per the guide's pattern list), manually, line by line.

## 2. Deliverables tree

```
/AGENTS.md                      (extend the seed; keep general rules)
/INDEX.md                       (full repo manifest: every file, its authority, its status)
/constitution/                  (G1: kernel v8 documents)
/shell/                         (G1: reference corpus, reorganized from Rev 7)
/reports/INGEST_REPORT.md       (G0)
/reports/FIX_APPLICATION.md     (G1: ledger-ID → change mapping)
/decisions/                     (G2: one brief per resolve-now item + DEFERRED_REGISTER.md)
/plans/CYCLE_1_DELTA_PLAN.md    (G3: the flagship)
/plans/cycle_briefs/C2..C7.md   (G4)
/reports/TRACEABILITY_MATRIX.md (G4: Q2/Q3 requirement → cycle → artifact → gate)
/human_actions/                 (G5: sign-and-send packages)
/gauntlet/ROUND_LOG.md          (G7 process: per-round lens, findings, grades)
/gauntlet/CONVERGENCE_REPORT.md
/ledger/                        (run ledger entries)
/DISPUTES.md                    (if any)
/MORNING_REPORT.md              (G8: the first thing the human reads)
```

## 3. Subgoal DAG

**G0 — Orient and verify (first).** Read every file in the repo. Extend AGENTS.md (preserve its general rules; add anything this run learns). Build INDEX.md. Then an ingest-verification pass: spot-check every Grade-A finding in AUDIT_FINDINGS_LEDGER against Rev 7's actual text before trusting it. Output: `reports/INGEST_REPORT.md` — confirmations, discrepancies, disputes.

**G1 — Constitution v8 + fixes.** Execute Work Order §1 (kernel extraction: §§4, 6, 9, 10, 11, layer law + boundary-budget rules — *not* the concrete crate atlas — canonical hashing grammars, §33, §34 + new §34.9) and Work Order §2 (apply every OPEN-C0 fix). Single normative home per law; restatements become citations or `generated-echo` marks. Appendix B is regenerated from the schemas, never hand-patched. Output: `constitution/`, `shell/`, `reports/FIX_APPLICATION.md` mapping every ledger ID to its change location.

**G2 — Decision briefs.** For each Work Order §4 resolve-now item (hash algorithm, canonical serialization grammar, DecodedStreamId cost model, evidence-checker isolation, license, ledger backend, toolchain pin): options, recommendation, rationale, reversibility analysis, blast radius if wrong. Status: `PROPOSED — awaiting human ratification`. You propose; the human ratifies (Rev 7 §29.9 human-authority law). Deferred items go to `DEFERRED_REGISTER.md` with owner cycles. The C1 delta plan builds against the proposed defaults and flags the dependency.

**G3 — The Cycle 1 delta plan (flagship deliverable).** Per Work Order §7 and Charter §5/C1, covering: L0–L2 capability surface with consequence contracts (bytes/lexer/COS/xref/revisions/object streams; Flate+predictors, ASCIIHex, ASCII85, RunLength, LZW; recovery-as-bounded-hypothesis-search v1; encryption inventory **plus standard-handler read decryption with credentials** — RC4/AESV2/AESV3, password preparation); the immune system as first-class capabilities with their own contracts and falsifiers (generated schemas, claim registry, contract-truth checks, drift auditor); the CLI surface; fuzz-target inventory and the zero-reachable-panics gate; SpecCard *slot* citations throughout (per Rule 2); the C1 close-gate definition; explicit exclusions (no rendering, no fonts, no public-key handlers, no writer). Style: self-contained per the Flywheel standard — a fresh agent implements from it without asking; dependency-aware in prose (what blocks what); every non-obvious choice justified. Target 2,500–4,000 lines. If G1 is unfinished when you start, cite Rev 7 stable section IDs directly and upgrade citations later — do not block the flagship on the extraction.

**G4 — Cycle briefs + traceability.** For C2–C7: a 1–3 page brief each (scope boundary, expected consequence-contract families, dependencies on decisions, known risks, evidence emissions, close-gate sketch). **Do not write full delta plans for C2–C7** — the §34.9 archaeology-first law requires them to be authored against repo reality that does not exist yet; full plans now would be plans against imagined code. Then `TRACEABILITY_MATRIX.md`: every Q3 requirement (Charter §7, §33.15 ladder) and every Q2 requirement mapped to producing cycle → artifact → gate, with a zero-orphan rule in both directions, closing with a written answer to the reality-check question: *"If every cycle completes as briefed, do Q2 and Q3 actually get answered? Why or why not?"* If the answer is no, say what is missing — do not paper over it.

**G5 — Human-action packages.** Sign-and-send drafts for every human-bound day-zero item (Work Order §5): steward/reviewer/red-team outreach emails with role descriptions and independence requirements; ISO license acquisition steps under current AI-use terms; commitment-substrate options with setup instructions; discovery-protocol commitment texts ready to commit verbatim; challenge-window duration proposal with justification; vulnerability-disclosure policy draft; corpus acquisition and sealing procedure. Each package: what it is, why it cannot be automated, exactly what the human does, expected time.

**G6 — Charter-set v1.1 proposals (conditional).** Only if gauntlet rounds surface genuine defects in the four v1.0 documents: produce v1.1 files with changelogs. Do not restyle or "improve" absent defects.

**G7 — The review gauntlet.** See §4. Runs throughout, concentrated after G3.

**G8 — Final integrity gate + morning report.** Cross-document drift scan (term consistency, single-normative-home check, claim-vocabulary legality — no "best/complete/mogged" leakage anywhere); regenerate INDEX.md; seal the run ledger with the night's telemetry; de-slopify pass; write `MORNING_REPORT.md` per §6.

## 4. The review gauntlet (~30 fresh-context rounds)

**Allocation:** C1 delta plan **12** · Constitution extraction + fix application **6** · Charter-set cross-consistency **4** · traceability matrix + cycle briefs **4** · decision briefs **2** · final whole-repo coherence **2**. If an artifact converges early (two consecutive marginal-only rounds), reallocate its remaining rounds to the C1 plan.

**Per-round protocol:** a fresh-context sub-agent (no memory of authoring) receives the artifact + its authority chain + **one declared lens**, hunts, and files graded findings (A = confirmed defect, B = probable, C = judgment) into `gauntlet/ROUND_LOG.md`. The owner agent triages, fixes, and logs dispositions before the next round.

**Lens rotation** (each round declares one): envelope-dependency (the §34.4 bug class — found twice in this project already) · identity-law consistency (§9/§10 grammar) · PDF-normative-fact check · security/DoS · clean-room contamination scan · self-containment (paste the most obscure section alone into fresh context: implementable as written?) · dependency-soundness (draw the DAG; cycles and orphans are bugs) · duplication/drift · claim-vocabulary legality · Q2/Q3 traceability · kernel-touch audit · oversimplification hunt (**DO NOT LOSE FEATURES** — flag anything a fix deleted) · de-slopification (final rounds only).

**Techniques from the guide, mandatory:** repeat the *exact same* blunder-hunt prompt 5× consecutively after each major artifact lands (each pass finds what the last one missed); use the overshoot technique on cross-reference passes ("I am positive you missed at least 80 elements"); track convergence per the guide's phase model (rounds 1–3 structural, 4–7 architecture, 8–12 refinement, 13+ polish) and report the findings-per-round curve honestly in `CONVERGENCE_REPORT.md`. If the harness can run a genuinely different model family for some rounds, do so and log which; if not, log that all rounds share one model family — that is a known correlated-blind-spot limitation, state it, don't hide it.

## 5. Priority ladder (if time or budget runs short, cut from the bottom)

1. G3 — C1 delta plan
2. Gauntlet rounds on G3
3. G1 — Constitution + fixes
4. G4 — traceability matrix (the matrix outranks the briefs)
5. G2 — decision briefs
6. G4 — cycle briefs
7. G5 — human-action packages
8. G6, remaining gauntlet, extended G8 polish

G0, the ledger, and MORNING_REPORT.md are never cut.

## 6. Morning report spec

`MORNING_REPORT.md` contains, in order: (1) one-paragraph outcome vs. the wake-up test; (2) per-subgoal status with file links; (3) convergence curves per gauntleted artifact and total findings by grade; (4) the **ratification queue** — every PROPOSED decision awaiting the human, one line each; (5) human-action packages ready to send, with a recommended first-three-actions list; (6) disputes; (7) **not-done list with reasons** (expected entries: commitment substrate, ISO license, steward recruitment, SpecCard bodies, C2–C7 full plans, all beads — these are human-bound or law-bound, not failures); (8) known risks introduced overnight; (9) the explicit next step: **beads conversion of the C1 delta plan happens with the human present** — flag the plan-bead gap from the guide so it cannot be forgotten.

## 7. Spirit clause

When in doubt, choose the interpretation that maximizes the campaign's evidentiary integrity over the one that maximizes visible output volume. A smaller, verified, honestly-accounted substrate beats an impressive pile — the FrankenSim re-audit in this repo is the case study, and this campaign's entire premise is not repeating it. Go hard on volume *of review*, not volume of assertion.
