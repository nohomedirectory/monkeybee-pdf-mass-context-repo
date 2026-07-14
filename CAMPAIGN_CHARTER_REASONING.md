# Campaign Charter Reasoning

**Version:** 1.0
**Date:** 2026-07-14
**Companion to:** MONKEYBEE_CAMPAIGN_CHARTER_v1.md
**Purpose:** Every structural choice in the Charter, justified. Per the planning methodology's own law — a plan without *why* forces future agents to guess, and guessing is where coherence dies. This document is the *why*. It is reference material for delta-plan authors and review rounds; it is never converted to beads.

---

## 1. Why restructure Rev 7 at all (Constitution / Charter / delta plans)

Three forcing facts:

**Context economics.** Rev 7 is ~75,000 words. The planning methodology's ceiling — a plan a fresh agent can hold and act on — is strained at that size, and every addendum makes it worse. A campaign of seven cycles against one monolithic, growing plan means every cycle pays the full context cost and every polish round defends the full surface. Splitting means each cycle holds: kernel (stable, memorized by reference), Charter (short), one delta plan (~2–4k lines). Nothing else.

**Drift mechanics.** Both Grade-A defects found in three audit rounds were *duplication drift*: Appendix B falling out of sync with §10.6, and ALIEN_ARTIFACT.md falling out of sync with its own re-audit. Rev 7 hand-restates its central laws in four to six places each (idempotency ~25 mentions, nonce ~23). Every addendum cycle multiplies restatement sites. The split assigns each law exactly one normative home (the Constitution), makes everything else a generated echo or a reference, and gives the drift auditor a tractable target.

**Kernel stability is the addendum enabler.** The entire economics of "plan against the repo, bead the delta, swarm, repeat" collapses if an addendum can change the identity grammar — every receipt, cache key, and claim downstream invalidates. Declaring the kernel and forbidding casual touch converts "hopefully nothing breaks" into a checkable per-cycle declaration. The kernel freezes *laws*, not *inventory*: the crate atlas stays provisional (per Rev 7 §30 itself) because P19 merges and boundary-budget splits are normal evolution, while layer direction and the budget rules are law.

## 2. Why seven cycles, and why each boundary sits where it does

The decomposition rule: a cycle boundary belongs wherever (a) a claim envelope can ship, (b) the beads graph would otherwise exceed what polish rounds hold at steady state, or (c) an evidence checkpoint needs a stable artifact. Applying it:

- **C0 separate from C1** because plan-space work and swarm work have different failure modes; mixing them is how restructuring errors ship into code.
- **C1 = kernel + immune system + R0** because (i) R0 is independently sellable — the wedge exists before anything renders; (ii) the immune system must predate growth — drift appeared in this ecology at documentation stage, so building six cycles of code before the drift auditor exists is knowingly repeating FrankenSim F-09..F-12; (iii) the kernel beads exactly once, so it must be first. Read-side standard-handler decryption lands here — not later — because the R0 exclusion clause makes credentialed decryption R0-scope, and the C3 wild-tail gate hits encrypted files immediately (this was Charter correction C-1; the first campaign draft misplaced it in C5).
- **C2/C3 split (rendering before text)** because fonts are the single largest domain in the project — five formats, CMaps, glyph execution sandboxing, text semantics. One beads graph holding VM + raster + fonts + ICC is precisely the graph the polish protocol cannot hold; and the plan's page-local refusal law makes a text-less renderer *honest*, not embarrassing — refusal receipts are the product working as designed.
- **C4 = writer + Q3 checkpoint** because Q3 is achievable at R2: the ladder's artifact-candidate rung needs substance-that-works plus provenance plus disproportion, none of which require R4 fidelity. Checkpointing here rather than at campaign end means the verdict clock (external, uncontrollable) starts six days earlier, and a negative review arrives while there is still campaign left to respond with. WASM lands here because Bet 21's Observatory playground runs on it; release engineering lands here because a wedge you cannot install is not a wedge.
- **C5 = transforms/security** because redaction, sanitization, and signature *trust* validation complete the commercial CDR story, and because the agent/EditSession surface needs a writer to mutate through — it cannot come earlier.
- **C6 = two tracks** because fidelity (codecs, transparency, profiles) and authoring (layout engine, UAX ownership, tagged generation) are disjoint domains that only share the R4 label; running them as tracks keeps each beads graph coherent. The performance-hardening slice lives here — not earlier as a dedicated cycle, not later as a scramble — because D-class determinism discipline is kernel (C1) and benchmark *tracking* starts C2, so by C6 the perf work is targeted optimization against six cycles of telemetry rather than blind tuning. The coverage *scorer* is built here, but the *tagging* it reads began at C1 — retro-tagging five cycles of features at C6 would itself be a drift factory.
- **C7 = pure measurement** because mixing building and measuring in one cycle invites exactly the evaluator-optimization the protocol forbids. By C7, nothing new is built; the field freezes per commitments made at day 0, before any code existed to bias them.

Seven, not five, by default: the compressed variant is real but earns its use only from C1 telemetry. Seven, not ten: the remaining plausible splits (C1 into kernel/R0, C6 tracks into cycles) buy graph size relief at the cost of two more archaeology+delta+gate overheads, and the graphs at seven are already inside the polish protocol's demonstrated range.

## 3. Why the day-zero track exists: what compute cannot compress

Unlimited compute compresses: implementation, tests, fuzz-hours, baselines, ablations, the coverage matrix, documentation. It compresses **none** of: steward and reviewer recruitment (humans), two-person SpecCard meaning review (humans, and on *every* cycle's critical path), challenge windows (calendar objects whose credibility is proportional to their duration — a 48-hour window on a "leads the field" claim reads as theater to exactly the adversarial reviewer who matters), held-out corpus sealing (must precede implementation or nothing is held out), and external verdict latency.

Therefore every uncompressible item moves off the build's critical path and onto a parallel track that starts at hour zero. This is the single largest structural difference between this campaign and the FrankenSim trajectory, whose tempo it otherwise shares: evidence apparatus at swarm tempo, from the start, or the two-week pace produces a two-week FrankenSim — temporal concentration 4.5, grounding 2.0, verdict underdetermined.

## 4. Theory of victory: Q3

The §33.15 artifact-candidate rung decomposes into six conditions; the Charter's evidence-thread table maps each to its producing cycles. The design insights worth stating:

- **Substance is deliberately sized down.** R0–R2 with closed provenance beats R0–R4 with open questions; a smaller artifact whose causal account closes is *more* alien-eligible than a bigger one that impresses. This is why the checkpoint is C4, not C7.
- **The loop is the foundry evidence.** Each cycle's sealed trial record (attempts, failures, cost, median outcomes, drift results, probe results) is one point in the output distribution §33.8 demands. Seven instrumented cycles are a foundry evaluation *as a byproduct of shipping*. FrankenSim ran the identical loop and got zero credit because nothing was committed prospectively — this campaign's entire evidentiary advantage over its mentor-project is instrumentation, not skill, and the reasoning document says so plainly because the Charter's credibility depends on not overclaiming.
- **The red team is continuous, not a phase.** The F-01 lesson: the killer failure is a false certificate the whole ecology agrees on — source, tests, contract, and campaign prose sharing one wrong premise. Countermeasures that share the ecology (same model family writing checker and checked) are structurally weak; hence the different-model-family requirement and seeded-defect detection-rate trials, which measure the falsifiers instead of trusting them.
- **Honest degradation beats silent pretending.** Every independence element that cannot be obtained is logged, and the affected claims cap at self-attested tiers. A campaign that says "we could not get an external adjudicator; this claim is therefore internal-only" is *more* credible on its remaining claims, not less.

## 5. Theory of victory: Q2

Q2 is two claims wearing one sentence: an alienness claim (inherited from Q3's machinery — incumbents are the definition's high-substance/low-disproportion quadrant, so any earned candidate label leads them on that axis) and a **completion measurement**, which is the real mountain. Its requirements:

- **The instrument before the claim.** "Complete" is unmeasurable without the clause-by-clause matrix (Rev 7 §0.2 concedes it doesn't exist). Tagging from C1 + scorer at C6 produces it as a side effect of disciplined building rather than a retrofit.
- **The denominator is friendlier than folk intuition.** Strict ISO 32000-2 scoring drops XFA (deprecated), Movie/Sound (deprecated), PostScript XObjects (deprecated) from the field — Acrobat's most famous exclusives largely exit the denominator — and specifies ECMAScript *actions*, not Acrobat's full JS API. What remains genuinely in-spec and excluded from MonkeyBee's envelope: 3D artwork and rich media. The campaign's honest options are implement-to-a-declared-tier or score them parse-and-preserve and out-cover elsewhere — the second is viable because no incumbent, Adobe included, demonstrably implements all of 32000-2, and the open engines carry enormous evidenced gaps in tagged structure, transparency corners, and color.
- **The field is frozen by commitments that predate the code.** Discovery protocol, inclusion criteria, and window durations committed at day 0 are what make a C7 `leading` outcome an *observed_field_lead* instead of a curated victory lap. The claim-scope vocabulary exists precisely so that the campaign cannot say "best" where the evidence says "led the named set."

## 6. FrankenSim lessons → campaign countermeasures

| Re-audit finding | Campaign countermeasure |
|---|---|
| F-01 false certificate survived source+tests+contract+campaign | Different-model-family red team; seeded-defect trials; external oracles the generator cannot redefine |
| F-02 contract described a removed, unsound API | Contract-truth checks: named-API existence, dependency agreement, claim-registry linkage — in C1, before growth |
| F-04 checker verified headings, not truth | Same; plus the explicit rule that heading checks never count as verification |
| F-05/F-06 license metadata and toolchain instructions wrong | Day-zero license decision; generated quick-start from pinned toolchain |
| F-08/F-09/F-10/F-11/F-12 five stale truth surfaces | Single normative home per law; generated echoes; blocking per-cycle drift audit |
| F-13 orphaned scaffolds as sediment | Quarantine-with-tombstone rule in the repository constitution |
| F-14 no head-specific public execution proof | Sealed per-cycle trial records with logs, inventory, host identity |
| F-15 counts mistaken for depth | Counts are inventory facts; only Gauntlet-tier evidence supports claims |
| §8.10 selection effects unknown | The ledger records the distribution, not the winning trajectory |
| §11.3 no construction ledger, unrecoverable | Ledger opens at day 0 — the one advantage that cannot be retrofitted |

## 7. Timeline reconciliation (the 6–18-month and 15-day estimates are both real)

Two duration estimates were given in this project's planning conversation, and they differ by an order of magnitude because they price different things. The 6–18-month figure assumed normal compute, serial cycles, and human latency (recruitment, review, windows) *inside* the critical path, and measured to *verdict*. The 15-day figure assumes effectively unlimited parallel compute, every human-bound item moved to the day-zero concurrent track, and measures to *package submission* — with verdicts explicitly external. The Charter adopts the second frame and the tempo-independence rule so that the structure survives either reality: same seven plans, same gates, whether two weeks or six months. What is *not* claimed anywhere: that verdicts arrive in two weeks. They arrive when independent people finish reading, and the campaign's credibility rests on that being someone else's decision.

## 8. The graceful-degradation design

The campaign serves two goals that fail in opposite directions: the verdict goals die by under-instrumenting (skip baselines → FrankenSim outcome), the survival goal dies by over-instrumenting (evidence apparatus starves the sellable product). The resolution is architectural, not motivational: **no G1 deliverable ever depends on G2/G3 machinery.** The wedge ships from C1 with zero stewards, zero windows, zero baselines; the checkpoint (C4's package) and the measurement cycle (C7) are the only §33-gated elements, and both detach cleanly. This clause exists in writing because mid-campaign resource pressure will test it, and the failure mode it prevents — quietly cannibalizing the evidence budget while still talking like the verdicts are coming — is worse than either honest outcome.

## 9. Honest limits: how this campaign can fail, and what it cannot claim

- **The gauntlet can fail on the merits.** Baselines A–D might not lose — vanilla agents at equal budget might reproduce the integration, in which case the disproportion claim is dead and the honest publication is exactly that. This outcome is *allowed*; a campaign that cannot fail proves nothing.
- **The artifact can grow its own F-01.** A false certificate the whole ecology agrees on, surviving the red team. The seeded-defect trials estimate the probability; they do not zero it.
- **Reviewers can say no**, or say nothing for months. Submission ≠ verdict.
- **The moat is narrower than it sounds.** What FrankenSim permanently lacks is the *construction-era* ledger — attempts, search, selection, cost — so its foundry/provenance claims stay underdetermined. Its *artifact-level* assurance (sealed verification bundles, external audits, adversarial certificate hunts) can be earned late, any time its author chooses. MonkeyBee's structural advantage is specifically on provenance and disproportion axes, not a general and permanent superiority. Stated here because the Charter's earlier drafting history contained the overclaim ("permanently capped, forever") and this document is where the correction lives.
- **A yes on Q2/Q3 is not a proof of superior skill.** It is proof of a decidable claim — the first of its kind if it lands, which is historic on its own terms. The method being executed is inherited; instrumenting an inherited method is a different achievement from inventing it, and the campaign's public claims must keep that distinction or forfeit exactly the credibility they exist to earn.

## 10. Corrections incorporated (drafting provenance)

Charter v1.0 already contains the round-3 audit fixes to its own first draft: C-1 (read decryption moved to C1), C-2 (SpecCard pipeline on the day-zero track with per-cycle coverage gates), C-3 (CLI C1, WASM C4, C-ABI preview C5, freeze post-R4), C-4 (D-classes C1, benchmarks C2, hardening slice C6), C-5 (authoring track added to C6), C-6 (corpus sealing day 0, release engineering C4–5), C-7 (kernel freezes layer law, not the crate atlas; kernel beads exactly once), C-8 (tagging C1, scorer C6), C-9 (Charter through the commitment substrate), C-10 (Evolution Trial formalized at C4; probes at every boundary; Flagships G/H named at C7), C-11 (day-15 arithmetic), C-12 (baseline-cost risk promoted to #1; Baseline E acknowledged). Strategic corrections S-1 through S-4 are reflected in §7 and §9 above. Future audits should verify against this list; the AUDIT_FINDINGS_LEDGER carries the full history.

---

*End of Reasoning v1.0.*
