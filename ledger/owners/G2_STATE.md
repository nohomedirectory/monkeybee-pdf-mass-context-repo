---
generated-by: Claude G2 owner (claude-opus-4-8, effort xhigh)
date: 2026-07-14
inputs:
  - AGENTS.md
  - INDEX.md
  - MONKEYBEE_CAMPAIGN_CHARTER_v1.md
  - OVERNIGHT_GOAL.md
  - CYCLE_0_WORK_ORDER.md
  - AUDIT_FINDINGS_LEDGER.md
  - ledger/prompts/OWNER_MARCHING_ORDERS.md
  - DISPUTES.md
  - ledger/ORCHESTRATION_STATE.md
  - ledger/RUN_LEDGER.md
  - ledger/owners/G0_STATE.md
  - gauntlet/ROUND_LOG.md (read-only review-intake snapshot at REVISE entry)
  - live human override, 2026-07-16 (review-budget reduction and mandatory closure pass)
status: DRAFT
evidence-status: provisional-pending-substrate
owner: G2
owner-fsm: DONE/HANDOFF
---

# G2 Owner Checkpoint — Decisions

## Transition record

| Phase | Timestamp | Checkpoint |
|---|---|---|
| `INGEST` | 2026-07-14T16:33:09+02:00 | Governing instructions read in full; authority, scope, and deliverables recorded before any broader work |
| `DRAFT` | 2026-07-14T16:40:48+02:00 | Decision-bearing canon read at stable section IDs; three primary-standards fetches logged; option space grounded; `decisions/` authoring begun |
| `SELF-CHECK` | 2026-07-14T16:52:00+02:00 | Nine artifacts on disk; scope, canonical-integrity, claim-vocabulary, clean-room, provenance, citation, and de-slopification checks run; two self-found defects repaired |
| `SUBMIT-FOR-REVIEW` | 2026-07-14T16:56:16+02:00 | G2 stops here. Root routes fresh reviewers. No commit, no push, no `REVISE` without a reviewer packet. |
| `REVISE` | 2026-07-16T02:03:44+02:00 | Live human authority cuts R27/R28 and requires a fresh mandatory hardening pass despite the prior packet-only transition condition; R27/R28 remain explicit zero-evidence omissions. No decision artifact changed before this transition was persisted. |
| `DONE/HANDOFF` | 2026-07-16T02:17:25+02:00 | Mandatory hardening repaired locally established owner-contract defects; exact nine-artifact manifest and all supportable gates reproduced; R27/R28 remain unrun and receive no credit. Closure is authorized only by the live scope reduction, not by review evidence that does not exist. |

## Self-check evidence

| Check | Result |
|---|---|
| Scope | `git status` shows exactly `decisions/` and `ledger/owners/G2_STATE.md` under G2. No other owner's path touched. |
| Canonical integrity | All 9 canonical inputs re-hashed against `ledger/CANONICAL_HASHES.md`: **9/9 byte-identical**. No canonical file modified. |
| Claim vocabulary | Supremacy-phrasing scan clean. Four hits triaged: three are verbatim canon quotes (§34.9 "median and best outcomes"; §9.6 "complete text extraction"; §9.6 "complete dependency-and-selection manifest"), one is the idiom "best-effort" used to *forbid* best-effort encoding. No supremacy claim about MonkeyBee anywhere. |
| Clean-room | Zero occurrences of any prohibited processor name (`pdf.js`, PDFBox, MuPDF, Poppler, PDFium, iText, QPDF, Ghostscript, lopdf, pdf-rs, hayro, krilla) across all nine files. No processor source or documentation was read or cited. No competitor material. |
| Measurement | None performed. Every performance claim is either absent or marked `[UNVERIFIED]` and routed to a C1 measurement step. |
| SpecCards | No card authored; no semantic body written. D4 references SpecCards only as an *input class* to the checker author. |
| Beads / code / scaffolding | None. Markdown only; zero non-`.md` files; no bead or pseudo-bead inventory; no crate named as a committed choice. |
| Provenance | All 9 files carry frontmatter with `generated-by`, `date`, `inputs`, `status`, and (where applicable) `evidence-status`. |
| Mandated brief elements | All 7 resolve-now briefs carry Options, Recommendation, Rationale, Reversibility/migration, Dependencies, Blast radius, and a Human ratification block. |
| Human authority | Every brief states `PROPOSED — awaiting human ratification` and carries an unticked ratification block. No brief reads as a decision. |
| De-slopification | Manual pass; slop-pattern scan clean. |

### Defects found in my own work during SELF-CHECK, and repaired

1. **Misattributed quotation (would have been a Grade-A honesty defect).** D4 attributed the phrase *"Correlation is recorded; 'external' does not imply independence"* to Rev 7 §10.2.1. That wording is from the §35 table row, not §10.2.1's body. Caught by reading §10.2.1's actual text rather than trusting my own section index (in which I had also misread the line number, 1737 as 2737). **Repaired:** D4 now quotes §10.2.1 verbatim — and the real text is materially stronger for the argument, because it names *model family* outright as a correlation axis and states that "unknown lineage is explicit uncertainty, not assumed independence." The argument for authorship isolation now rests on canon's own words instead of a paraphrase.
2. **Non-standard heading.** D5's reversibility section was titled "The reversibility asymmetry", so a reviewer scanning for the mandated element would have scored it missing. Renamed to "Reversibility and migration path — the asymmetry that makes this urgent". Content unchanged.

## Current checkpoint

- Timestamp: `2026-07-14T16:56:16+02:00`
- Phase: `SUBMIT-FOR-REVIEW`
- Owner: Claude G2 owner, sole owner of the decisions subgoal.
- Active goal: author one PROPOSED decision brief per Work Order §4 resolve-now item, plus `decisions/DEFERRED_REGISTER.md` and a compact decision index for G3; stop this turn at `SUBMIT-FOR-REVIEW`.
- Exclusive writable paths: `decisions/**` and `ledger/owners/G2_STATE.md`. Nothing else.
- Partial outputs at this checkpoint: this checkpoint only; `decisions/` did not exist at INGEST entry.
- Branch: `main`, tracking `origin/main`. No commit, push, branch, worktree, or stash will be performed by G2.
- Concurrency: G1 (`INGEST`, Constitution/shell paths) and G3 (`INGEST`, C1 delta plan path) are live in non-overlapping paths. `ledger/RUN_LEDGER.md` carries an unrelated concurrent modification and is orchestrator-owned; G2 will not touch it.
- Owner fetches: none at this checkpoint. Any permitted fetch will be recorded in the fetch table below with exact URL and purpose for transfer to the root ledger.
- Sub-agent activity: none. G2 does not route its own review; root routes fresh reviewers after `SUBMIT-FOR-REVIEW`.

## Files read in the required order before this checkpoint

1. `AGENTS.md` — full file, seed rules 0–13, truth hierarchy, reading order, and the G0 navigation/evidence-hygiene extension (rules 14–20).
2. `INDEX.md` — full file; treated as navigation, never as authority.
3. `MONKEYBEE_CAMPAIGN_CHARTER_v1.md` — full file.
4. `OVERNIGHT_GOAL.md` — full file.
5. `CYCLE_0_WORK_ORDER.md` — full file.
6. `AUDIT_FINDINGS_LEDGER.md` — full file.
7. `ledger/prompts/OWNER_MARCHING_ORDERS.md` — full shared contract and the G2 section.
8. Shared state read for orientation, not owned: `DISPUTES.md`, `ledger/ORCHESTRATION_STATE.md`, `ledger/RUN_LEDGER.md`, `ledger/owners/G0_STATE.md`, and the INGEST checkpoints of G1 and G3.

## Authority chain for this subgoal

1. The human's live instruction.
2. `MONKEYBEE_CAMPAIGN_CHARTER_v1.md` (with `CYCLE_0_WORK_ORDER.md`, `AUDIT_FINDINGS_LEDGER.md`, `CAMPAIGN_CHARTER_REASONING.md`).
3. `CYCLE_0_WORK_ORDER.md` §4 — the resolve-now and defer lists that define my deliverable set.
4. `MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md` §35 (open decisions), plus the sections each decision touches (§§4, 9, 10, 11, 22, 26, 29.9, 33, 34.5) read on demand by stable section ID.
5. `AUDIT_FINDINGS_LEDGER.md` rows that bind a decision — R1-9 (checker isolation), R2-N2 (hasher law), R1-4/R1-8/R2-N3 (canonicalization scope and cost).

## Scope law I am operating under

- Plan space only. No beads, no pseudo-bead inventories, no source, no build or CI scaffolding.
- No canonical edits. Every output is a new file under `decisions/` with a provenance header.
- Clean-room law is absolute: no PDF-processor source or documentation is read or cited, for any reason, including "just the README". No SpecCard semantic bodies; slots only, `PENDING-LICENSED-SOURCE`.
- No measurements, no competitor comparisons, no benchmark generation.
- No external action: nothing sent, purchased, published, or posted.
- Recommendations are proposed defaults only. The human ratifies (Rev 7 §29.9 human-authority law). Nothing I write is a ratification, and no brief may read as one.
- Anything I cannot verify from local canon or a first-party primary source is marked `[UNVERIFIED]`.
- Claim vocabulary is law: no supremacy phrasing anywhere in my outputs.

## Deliverables I own

Seven resolve-now briefs (Work Order §4):

1. Content-hash algorithm and digest widths.
2. Canonical serialization grammar for hashing.
3. DecodedStreamId cost/availability model.
4. Evidence-checker isolation (per audit row R1-9).
5. Project license.
6. Persistent ledger backend default.
7. Rust toolchain pin.

Plus `decisions/DEFERRED_REGISTER.md` for the five deferred items (raster/GPU backend → C6; PDF/A-1 vs 1.7/2.0 writer conflict → C6; C-ABI freeze point → post-R4; base-font fallback licensing → C3; S6 performance-per-fidelity metric → C7), each with owner cycle, trigger, evidence needed, and the harm of premature resolution.

Plus a compact decision index for G3, so the C1 delta plan can build against proposed defaults and label each dependency as awaiting ratification.

Every brief carries: options, recommendation (`PROPOSED — awaiting human ratification`), rationale, reversibility and migration path, dependencies, evidence still needed, and blast radius if wrong.

## Open risks recorded at INGEST

- Legal and library facts (license terms, crate/toolchain versions, algorithm availability) are the highest contamination and staleness risk in this subgoal. Local canon is the default source; any current-fact claim without first-party evidence will be marked `[UNVERIFIED]` and routed to a human verification step rather than asserted.
- The hash-algorithm and canonical-serialization briefs are the deepest-blast-radius items: every identity in the kernel consumes them. A wrong default is recoverable only by re-hashing every receipt, so reversibility analysis is load-bearing, not decorative.
- G1 owns the Constitution that will consume my proposed defaults, and G3 builds the C1 plan against them. Both are drafting concurrently. My briefs must be self-contained and must not assume a Constitution section number that does not exist yet; I cite Rev 7 stable IDs.

## Owner fetch record

Three fetches, all first-party primary standards pages at NIST CSRC. Purpose: the content-hash and canonical-serialization briefs gate every identity in the kernel, and asserting a standard number or status from recall is the exact "invented versions or clause numbers" failure the honesty rule forbids. No PDF-processor source or documentation was contacted; no competitor material; no measurement. Root should transfer these rows to `ledger/RUN_LEDGER.md`.

| Time | URL | Purpose | Result | Classification |
|---|---|---|---|---|
| 2026-07-14T~16:37 | `https://csrc.nist.gov/pubs/fips/180-4/upd1/final` | Confirm FIPS 180-4 (Secure Hash Standard) identity and status before recommending SHA-256 as the identity algorithm | Title and number confirmed. Page records that NIST decided to revise FIPS 180-4 (announced 2023-03-07). The SHA-2 algorithms are not withdrawn; the standard document is under revision. Recorded honestly rather than as "current and unrevised". | Permitted primary technical reference; no PDF-domain or prohibited-processor contact |
| 2026-07-14T~16:37 | `https://csrc.nist.gov/pubs/sp/800/185/final` | Confirm SP 800-185 and whether TupleHash is what Rev 7 §9.2's length-framing/domain-separation law needs | Confirmed: "SHA-3 Derived Functions: cSHAKE, KMAC, TupleHash, and ParallelHash", final, Dec 2016. TupleHash is "designed to hash tuples of input strings unambiguously" — the standardized form of the §9.2 requirement. | Permitted primary technical reference |
| 2026-07-14T~16:38 | `https://csrc.nist.gov/pubs/fips/202/final` | Confirm FIPS 202 (SHA-3) identity, status, and function list before offering it as a coherent alternative package | Confirmed: final, Aug 2015; specifies SHA3-224/256/384/512 and SHAKE128/256. Page carries a 2025-03-13 planning note that NIST has decided to update the publication. | Permitted primary technical reference |

Honest reading of the two revision notices: both FIPS 180-4 and FIPS 202 have announced document revisions and neither algorithm family is withdrawn. Whether a revised document has since published is `[UNVERIFIED]` here and is a named human/counsel verification step in `decisions/D1_CONTENT_HASH.md`.

## Findings raised during ingest (for root routing; G2 does not own the affected files)

- **F-G2-1 (Grade A, name drift).** `DecodedStreamId` — named in `CYCLE_0_WORK_ORDER.md` §4.3, `MONKEYBEE_CAMPAIGN_CHARTER_v1.md`, `OVERNIGHT_GOAL.md`, and `ledger/prompts/OWNER_MARCHING_ORDERS.md` — occurs **zero** times in Rev 7. Rev 7 §9.2's identity table names `DecodedContainerId` ("one decoded container under a source/object/security/filter/algorithm identity"), which is the only decoded-artifact identity in the domain canon. Evidence: `grep -c "DecodedStreamId"` = 0 and `grep -c "DecodedContainerId"` = 2 over `MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md`. This is campaign-layer-to-domain-canon drift of the same class as audit rows R1-1 and R2-N7 (both duplication drift). G2 resolves the reference inside its own brief and names `DecodedContainerId` as canonical, but `DISPUTES.md` is orchestrator-owned and G2 does not edit another owner's paths. Routed to root for a `DISPUTES.md` entry.
- **F-G2-2 (gap, judgment).** The runtime dependency allowlist and the cryptographic-crate selection (Rev 7 §35 rows "Runtime dependency allowlist" and "Cryptographic crates"; §15.9 codec dependency policy) gate Cycle 1 code — C1 lands Flate/LZW decoders and the RC4/AES/MD5/SHA standard-security-handler stack — yet they appear in neither the Work Order §4 resolve-now list nor its defer list. G2 does not silently expand its mandate: the gap is recorded in `decisions/DEFERRED_REGISTER.md` under identified gaps, with an option space and a recommended disposition, for the human to route.
- **F-G2-3 (sequencing, Grade B).** Charter §10 makes the Charter the first artifact committed through the tamper-evident substrate, and its hash "the campaign's first ledger entry". A digest committed to an external substrate cannot later be re-hashed without destroying the timestamp semantics that give it value. The content-hash algorithm therefore has to be ratified **before** the first substrate commitment, or the campaign's founding evidence entry stands under an unratified algorithm. Recorded in `decisions/D1_CONTENT_HASH.md` and raised to the ratification queue as an ordering constraint.

## Delivered artifacts

All under `decisions/`, all `PROPOSED — awaiting human ratification`, 1,265 lines total.

| File | Decision | Proposed default |
|---|---|---|
| `D1_CONTENT_HASH.md` | Content-hash algorithm and digest widths | SHA-256, full 256-bit; algorithm-versioned registry; legacy MD5/RC4/SHA-1 fenced to PDF semantics, never project identity |
| `D2_CANONICAL_SERIALIZATION.md` | Canonical serialization grammar for hashing | Deterministic-CBOR profile + mandatory domain separation and length framing; floats forbidden; refuse rather than guess; encoder dual-implemented |
| `D3_DECODED_STREAM_IDENTITY.md` | Decoded-container identity: cost and availability | Hybrid — recipe identity pre-decode + content digest post-commit, verified on reuse; four typed availability states |
| `D4_EVIDENCE_CHECKER_ISOLATION.md` | Evidence-checker isolation (audit row R1-9) | Code + authorship (different model family) + specification isolation + measured seeded-defect detection rate from C1; human adversarial review by C4 |
| `D5_PROJECT_LICENSE.md` | Project license | MIT OR Apache-2.0 dual + dependency-license allowlist; **DCO vs CLA must be decided now** |
| `D6_LEDGER_BACKEND.md` | Persistent ledger backend | Hash-chained append-only JSONL, per-writer shards, as source of truth + derived regenerable index |
| `D7_RUST_TOOLCHAIN_PIN.md` | Rust toolchain pin | Two pinned toolchains by package role: exact stable (runtime/release) + date-pinned nightly (assurance lanes only); toolchain is a determinism input |
| `DEFERRED_REGISTER.md` | The five deferrals + two identified gaps | Owner cycle, trigger, evidence needed, harm of early resolution, and a **guard** for each |
| `DECISION_INDEX.md` | Compact index for G3 and the ratification queue | Couplings, what C1 must assume and how to label it, do-not-build-on list, priority-ordered ratification queue |

## Decisions taken as owner (recorded for review)

- **D1 and D2 are presented as coupled packages, not independent knobs.** The hash family and the framing grammar are what make each package sound; offering them as free-standing choices would invite an incoherent mix (a SHA-2 core with TupleHash framing, or a hand-waved framing with any hash).
- **The decisive criterion for D1 is independent verifiability, not throughput.** The checker (Appendix A.13) and the external adjudicator (§33) are adversarial or independent by construction, and an identity algorithm they cannot cheaply reimplement or recompute taxes exactly the parties whose independence carries the Q3 verdict. This inverts the usual ranking and is stated explicitly in the brief so a reviewer can attack it.
- **`DecodedContainerId` (Rev 7 §9.2) is treated as the canonical name**; `DecodedStreamId` is a campaign-layer alias. See F-G2-1.
- **No crate is named as a committed choice anywhere**, because a "which crate" answer sourced from recall is an unverifiable ecosystem claim in a phase that forbids measurement. GAP-2 routes the dependency-policy question to the human instead.
- **No version number is invented.** D7 deliberately leaves the stable pin blank for a human or CI to fill at C1 start rather than fabricating a plausible-looking version.
- **The three standards fetches were judged genuinely necessary** and are logged above. Both FIPS revision notices are reported honestly rather than smoothed into "current".

## Open risks at submission

- **Ordering risk (F-G2-3), the sharpest item in the queue.** Charter §10 makes the Charter the first artifact committed to the tamper-evident substrate and its hash the first ledger entry. A committed digest cannot be re-hashed without destroying the timestamp semantics that give it value. D1 therefore needs ratification *before* the first substrate commitment, not merely before C1 code. If the substrate is established before D1 is ratified, the campaign's founding evidence entry stands under an unratified algorithm.
- **D5's contribution instrument has a deadline that passes by inattention.** Permissive → copyleft is effectively one-way once outside contributions land without a licensing grant. The DCO/CLA choice is a day-zero decision that expires quietly with no event to mark it.
- **D2's CBOR determinism rule set is not yet quoted against a first-party specification.** Marked `[UNVERIFIED]` in the brief. It is the loose end in the recommended package and must be closed at C1, not inherited from a library's defaults.
- **All legal content in D5 is `[UNVERIFIED]` and requires counsel.** G2 is not qualified to give legal advice and §29.9 reserves legal interpretation to humans.
- **Single-model-family limitation.** These briefs were authored by one model (claude-opus-4-8). Per the goal's own §4 note, correlated blind spots are a known limitation of same-family authorship; the fresh reviewers root routes should include a different family, and rounds 27–28 of the precommitted allocation already assign the decision briefs to `Sol` and `Opus` respectively.

## Not done, by law or by scope

- No decision is ratified. Every brief awaits the human.
- No `DISPUTES.md` entry for F-G2-1 — that file is orchestrator-owned, and G2 does not edit another owner's paths. Routed to root.
- No commit, no push, no branch, no worktree, no stash.
- No beads, no code, no scaffolding, no measurement, no external action, no SpecCard bodies.
- No `REVISE` transition. Per the shared contract, a fresh reviewer must file a finding packet first.

## Next transition condition

`REVISE`, and only on receipt of a fresh-context reviewer's finding packet routed by root. G2 stops here.

## REVISE entry — live review-budget override and intake boundary

The preceding next-transition condition was correct when written at submission. It is superseded prospectively by the live human instruction received on 2026-07-16. Human authority requires G2 to perform the mandatory `REVISE` hardening pass and close under a reduced overnight review scope; it does not manufacture a reviewer packet or turn an omission into validation.

### Controlling scope change

- The overnight target is now approximately twenty accepted reviews; root's bounded landing is 22 accepted reviews while preserving a floor of twelve accepted C1 reviews.
- R27 (`reversibility and dependency blast radius`) and R28 (`security/DoS`) are cut from overnight execution. Neither may be replaced here, inferred from another lens, or counted as review, coverage, a finding, a grade, a disposition, or convergence evidence.
- The cut is a scheduling authorization only. It supplies no substantive evidence about any decision artifact.
- The live instruction authorizes G2's mandatory owner hardening pass without the G2-specific fresh packet that the original shared contract expected. All decision recommendations remain proposals awaiting human ratification.

### Review-intake evidence reproduced before REVISE work

- Read-only Round Log identity at intake: `gauntlet/ROUND_LOG.md`, 7,913 lines, 1,348,963 bytes, SHA-256 `d6a7b9f96ed4fcd67a89d2b4f161d9a6f33d030a46318ab18521693bfe977965`.
- Round Log allocation row R27 is at local line 112: artifact `Decision briefs`; sole allocated lens `reversibility and dependency blast radius`; model `Sol`; artifact hash `PENDING`; status `PRECOMMITTED`; finding counts, marginal result, and owner disposition all empty.
- Round Log allocation row R28 is at local line 113: artifact `Decision briefs`; sole allocated lens `security/DoS`; model `Opus`; artifact hash `PENDING`; status `PRECOMMITTED`; finding counts, marginal result, and owner disposition all empty.
- No R27 or R28 packet exists in the Round Log. No G2-specific reviewer finding or owner review disposition exists on disk.
- The live 22-review landing is a human-set root boundary. G2 does not alter or certify the shared allocation, accepted-review arithmetic, convergence record, or C1 floor; those remain root/G7/G8 responsibilities.

### State boundary and next condition

- Writable scope remains exactly `decisions/**` and `ledger/owners/G2_STATE.md`.
- Shared Round, Convergence, root-ledger, orchestration, other-owner, canonical, source, code, Beads, task-inventory, and external-system state remain untouched.
- No fetch, measurement, comparison, spawn, message, staging, commit, push, publication, purchase, or contact occurred during intake.
- REVISE will freshly inspect all nine submitted artifacts against the admitted on-disk dispositions that can bind their contracts, then reproduce the exact manifest and the dependency, reversibility, security, no-action, no-claim, and no-prohibited-source gates supportable from local evidence.
- If that pass finds no evidence-backed artifact defect, the preferred closure is state-only. Any unresolved proposal, verification need, legal question, or human ratification boundary remains unresolved rather than being silently promoted.

## REVISE result

State-only closure was evaluated and rejected because the fresh pass found evidence-backed defects in the submitted G2 artifacts. The repairs stayed within the nine existing `decisions/*.md` files; no successor or extra file was created.

### Admitted dispositions and owner contracts applied

These are later owner dispositions over other reviewed artifacts. They constrain G2 handoff consistency but do not become fresh G2 reviewer findings, do not promote the reviewers' grades, and do not ratify any proposal.

| Input | Bounded effect on G2 hardening |
|---|---|
| G3 accepted R01-B02 | D4 now separates pre-run isolation admission, seeded-trial execution, and post-trial assessment; no pre-run state consumes its own later result. |
| G3 accepted R01-A07 | D6 preserves a low-dependency prospective append path before candidate work and a later seal that binds final roots. |
| G3 accepted R41-A03 | D7 separates pre-source toolchain-policy admission from later candidate-build evidence and makes nightly conditional on locally demonstrated tool need. |
| G6 `QUALIFIES` R21-A03 | D4 distinguishes checker-backed evidence admission from the unconditional G1 product wedge; proposed v1.1 text remains unratified. |
| G6 `QUALIFIES` R21-A02/R21-A07 | D6 preserves the proposed commitment-batch/schema interfaces without ratifying the batch ordinal or `CycleTrialRecordSchemaId`. |
| G6 `QUALIFIES` R19-A04/R21-A08 | `DECISION_INDEX.md` and `DEFERRED_REGISTER.md` now disclose that Work Order v1.0 routes 12 of 83 Rev 7 §35 rows and that the proposed v1.1 83-row overlay remains awaiting human ratification. |

### Corrections made in the mandatory pass

- D1/D2 no longer describe TupleHash as a separable wrapper around SHA-3, SHAKE, or SHA-256. It is treated as an alternative hash construction that still needs a separately specified structured-value encoding and exact first-party parameter evidence.
- Current ecosystem, hardware, tooling, adoption, and performance assertions were removed, narrowed to local evidence, or marked `[UNVERIFIED]`. No comparison or benchmark was run.
- D3 now forbids secrets in the recipe preimage and treats the decoded-content digest as sensitive metadata that can become a confirmation oracle across disclosure boundaries.
- D4 now carries the admitted lifecycle split, a human-accepted model-family classification gate, `PENDING-LICENSED-SOURCE` discipline, and a row-scoped failure boundary that does not silently block G1.
- D5 no longer asserts a universal relicensing direction, no longer folds GAP-2 into the project-license ratification, and leaves every legal effect to counsel and the human.
- D6 now commits a canonical manifest of every admitted shard head, not a fictitious singular head; timestamps do not manufacture total order; backend integrity does not claim event completeness; typed D2 preimages and JSONL must round-trip; omitted-shard and chronology failures are explicit.
- D7 no longer treats an unverified nightly premise as an established gate fact or claims that a pinned nightly inherently prevents reproducibility. The exact stable version, components, and any nightly need remain human/local-evidence inputs.
- The index and deferral register preserve the unresolved proposed v1.1 routing overlay and both branches of the unpromoted S6 timing premise.

## DONE/HANDOFF evidence

### Exact decision-artifact manifest

All identities below were reproduced after the final artifact edit. Counts are physical UTF-8 file line and byte counts from local disk; hashes are SHA-256 over the exact bytes.

| Path | Lines | Bytes | SHA-256 |
|---|---:|---:|---|
| `decisions/D1_CONTENT_HASH.md` | 146 | 17,681 | `78cfe82c444e7e7f521d506dc8c7f38d3b2fb60c8a0c3b472ae5a63588578f0a` |
| `decisions/D2_CANONICAL_SERIALIZATION.md` | 176 | 18,262 | `4f636d19b7879c53c7ee1a9003b13336c28c45ea9b0dd596df71c969a55a9d81` |
| `decisions/D3_DECODED_STREAM_IDENTITY.md` | 164 | 17,664 | `bb940e9843a5c4dd58d85e04a917d5a2a443b647fef25540452af9a384dede6d` |
| `decisions/D4_EVIDENCE_CHECKER_ISOLATION.md` | 195 | 19,542 | `bb9cd9796abb55b34f93d9034ded4f7cec462e99a7cd78f1d48abe01f6ef05da` |
| `decisions/D5_PROJECT_LICENSE.md` | 132 | 12,350 | `5ec471cc37d389202ec86051253337f9d6db26ca6c8f4b74142aa36030a225d2` |
| `decisions/D6_LEDGER_BACKEND.md` | 146 | 15,392 | `bdcf92c01be055e53d43bd2261376e1bcfb3e153914312d2cbb1e71ef75c9967` |
| `decisions/D7_RUST_TOOLCHAIN_PIN.md` | 138 | 12,222 | `28d6f8d147674d842252d570d4224a0a8a7f3241016e709cf5e4fd67cd6941f2` |
| `decisions/DECISION_INDEX.md` | 100 | 11,032 | `33f28afffbc1b6aba69d340a6a93682a8f0cda6244f5b1b6c9781a3b97af8a0e` |
| `decisions/DEFERRED_REGISTER.md` | 126 | 14,783 | `7279a80c0d6c3bb5c418d91ba127f044f2dadd398f7904212df452f7781288ed` |
| **Total** | **1,323** | **138,928** | nine-file set; no aggregate digest is substituted for the per-file identities |

### Structure and scope gates

- Exactly nine regular files exist directly under `decisions/`; all nine are Markdown. No file was added or deleted.
- All nine have `status: PROPOSED`, `evidence-status: provisional-pending-substrate`, and the 2026-07-16 revision provenance. The seven briefs each reproduce exactly one Options, Recommendation, Rationale, Reversibility/migration, Dependencies, Evidence-needed, Blast-radius, and Human-ratification section.
- Eight documents carry `ratification: PROPOSED — awaiting human ratification`; the compact index has no ratification frontmatter and states the same boundary in its body. Checked ratification boxes: zero.
- `git diff --check -- decisions ledger/owners/G2_STATE.md` passed. Immediately before this transition, the G2 state was 212 lines / 23,469 bytes / SHA-256 `40db85982912460e1b456164b69e195fb1ce266cde8c374ddc43b9fb0b3624c2`.
- The G2 changed-path set is exactly the nine manifest paths plus `ledger/owners/G2_STATE.md`. Concurrent changes in Round, Convergence, human-action, root-ledger, orchestration, and other-owner paths were neither edited, staged, reverted, nor reconciled by G2.
- Branch is `main`, tracking `origin/main`. The staged-path query returned no paths.

### Dependency and reversibility gates

| Artifact | Dependency boundary reproduced | Reversibility boundary reproduced |
|---|---|---|
| D1 | Root decision; consumed by D2/D3/D4/D6 and every content identity; first external commitment waits for D1/D2 ratification. | Algorithm-versioned migration is prospective; an already witnessed timestamped commitment is not retroactively reissued as the same evidence. |
| D2 | Consumes D1; consumed by D3/D4/D6 and identity/evidence records; exact CBOR and alternative TupleHash profiles remain evidence-gated. | Version change re-identifies every value; an ambiguous historical preimage cannot be safely reconstructed by assertion. |
| D3 | Consumes D1/D2; gates decoded-container provenance, virtual spans, cache reuse, and decoded-byte claims. | Recipe/content fields can evolve prospectively; prior recipe-only durable reuse leaves affected downstream evidence requiring re-derivation. |
| D4 | Consumes D1/D2; its post-trial assessment gates only checker-backed evidence/Q3 scope, not unconditional G1 admission. | Checker code can change; affected historical checker-backed evidence requires re-verification and claim-lapse handling. |
| D5 | Consumes no technical decision; coordinates with the independently fixed field rule; GAP-2 stays separately routed. | Rights history is path-dependent and counsel-bound; no licensing direction is asserted as easy or irreversible without actual grants. |
| D6 | Consumes D1/D2; prospective append precedes candidate work; later seal and canonical shard-head manifest feed the external substrate. | Storage migration requires a proved lossless mapping; missing prospective events cannot be upgraded from retrospective entries. |
| D7 | Root decision; exact pin precedes source work and determinism-bearing receipts; nightly exists only if a selected assurance lane proves it necessary. | Pins can move through a versioned event; receipts lacking a recorded compiler identity remain unreplayable. |

### Security, no-action, no-claim, and clean-room gates

- Prohibited-processor-name scan across the nine decision artifacts: zero hits for the locally enumerated prohibited list in AGENTS rule 8. No processor source or documentation was opened, fetched, or cited.
- SpecCard-semantic-body scan: zero `MB-SC-*` normative-body patterns. The one new card boundary says `PENDING-LICENSED-SOURCE`; no unavailable semantics were reconstructed.
- URL scan across the nine artifacts: zero. This continuation performed no fetch. The three historical NIST fetches remain only the submission-era evidence already recorded above.
- Measurement/comparison: none performed. Performance, adoption, implementation availability, current tool behavior, and legal effects without local evidence are marked `[UNVERIFIED]` or left as future evidence steps.
- Guarded claim-word scan found exactly three occurrences: D6 carries the exact §34.9 field-list quote containing `best`; D3 carries the exact Rev 7 laziness quote containing `complete`; D2 forbids `best-effort` encoding. No `fastest` or `mogged` occurrence exists. These are scoped quotation/no-claim uses, not MonkeyBee predicates.
- Supremacy-vocabulary scan found exactly three occurrences: one exact §34.5.1 rationale and two explicit negative/no-claim guards in `DEFERRED_REGISTER.md`/`DECISION_INDEX.md`. None reports a result or adds evidence.
- Security controls reproduced locally include D1 collision quarantine and legacy namespace fencing; D2 injective/versioned/refuse-on-ambiguity encoding plus separate implementations; D3 DoS-resistant cache indexing, non-secret context identity, and digest-disclosure authority; D4 known-correlation lineage and separated assessment; D5 counsel gate; D6 shard inclusion, explicit chronology, and external-manifest limits; D7 exact tool identity and rerun-on-bump law.
- Canonical integrity: all nine paths in `ledger/CANONICAL_HASHES.md` reproduce their recorded SHA-256 values, 9/9. No canonical path was edited.
- No spawn, send, message, stage, commit, push, branch, worktree, stash, deletion, source/code/scaffold, Beads/task inventory, publication, purchase, contact, or external-system mutation occurred. All commands were local reads/checks; all edits used structured patches in G2's exclusive paths.

### Review evidence that exists and does not exist

- Closing read-only review snapshot: `gauntlet/ROUND_LOG.md`, 7,987 lines, 1,360,985 bytes, SHA-256 `8b47bc3d83bd81ef3abbf131286f45342120e0abdbe30e91f7aaa01b1ba4793f`; `gauntlet/CONVERGENCE_REPORT.md`, 1,192 lines, 176,087 bytes, SHA-256 `cad9f6eb996251b9d71205a2021b1d2b6614e3233534852254a6557e636c854c`. These are read-only snapshots and may continue changing under their owners.
- R27 remains at Round Log local line 112 with artifact hash `PENDING`, status `PRECOMMITTED`, and empty finding-count, marginal, and disposition cells. No R27 packet exists. Therefore no reversibility/dependency-blast-radius review evidence, finding, grade, coverage, owner disposition, curve point, or convergence credit exists for G2.
- R28 remains at local line 113 with artifact hash `PENDING`, status `PRECOMMITTED`, and empty finding-count, marginal, and disposition cells. No R28 packet exists. Therefore no security/DoS review evidence, finding, grade, coverage, owner disposition, curve point, or convergence credit exists for G2.
- The allocation-table snapshot contains 18 rows with a filed validated or chain-qualified status. That is a physical snapshot fact, not G2's certification of the overnight accepted-review total. The live human sets root's bounded landing at 22 accepted reviews with a twelve-accepted-C1 floor; root/G7/G8 own that eventual accounting. G2 neither changes nor infers it.
- The R27/R28 cut is not used anywhere as substantive validation. The only G2 content assurance added in REVISE is the owner hardening and local gate evidence listed above.

### Unresolved proposals and human decisions preserved

- D1–D7 remain proposed. No algorithm, serialization profile, decoded-identity model, checker-independence claim, project license, ledger backend, toolchain version, nightly need, dependency provider, contribution instrument, or legal interpretation is human-ratified here.
- D2's exact first-party CBOR profile and the TupleHash alternative parameters remain `[UNVERIFIED]`; D5 remains counsel-bound; D7's exact stable version/components and any nightly need remain unfilled human/local-evidence inputs.
- GAP-1, GAP-2, DEF-1 through DEF-5, and the proposed Work Order v1.1 83-row routing overlay remain unresolved at their stated boundaries. The S6 timing branches are preserved rather than silently selected.
- `ALIEN_ARTIFACT.md` and `PROJECT_OVERVIEW.md` remain `SOURCE-UNAVAILABLE` under INDEX/DISPUTES handling. Neither is an input to a G2 decision correction, so no missing G2 semantic claim was reconstructed from them.
- No decision-specific fresh-context review exists because R27/R28 were cut by the live human. The single-model-family authorship limitation therefore remains and must appear in MORNING_REPORT's omission/risk disclosure.

### Why G2 may close

The live human explicitly reduced the overnight review scope, fixed root's bounded landing at 22 accepted reviews with the C1 floor preserved, cut R27/R28, and ordered G2 through a mandatory REVISE pass to closure. That higher authority supersedes the original packet-only transition precondition. G2 may close because the required owner hardening and local gates are now on disk, not because R27/R28 passed or because their lenses can be inferred. The missing lenses remain named omissions for MORNING_REPORT ratification/omission disclosure.

### State-file identity convention

`FINAL-SELF-LINES: 000323`

`FINAL-SELF-BYTES: 00038214`

`FINAL-SELF-SHA256-NORMALIZED: edeb5d2d1b1e6a9cf3d52553f2a5799656fd8a9102224ef0cab89ff8d9f58d83`

To reproduce the state identity after this transition, replace exactly the 64 hexadecimal characters in the unique field above with 64 ASCII zeroes, preserve every other byte, and compute SHA-256 over the resulting UTF-8 file. Line and byte counts are over the final on-disk file without normalization. This convention avoids an impossible raw self-hash while making the persisted state identity deterministic.

## Root post-handoff editorial receipt — `2026-07-16T09:24:35+02:00`

- **Authority and boundary:** root performed the mandatory final manual de-slopification and claim-vocabulary pass after G2's terminal handoff. No proposal, recommendation, option, dependency, evidence status, human-ratification boundary, or `[UNVERIFIED]` classification changed. The edits removed rhetorical rankings, unsupported cost adjectives, and conversational filler; they did not add an external fact or decision.
- **FSM preservation:** G2's six-state owner sequence remains the substantive closure. This is a root integrity receipt, not a silent owner restart. The pre-receipt state identity is 323 lines / 38,214 bytes / `cce5a66c0c25ea140537c4cd0a0407bf0b0d482323ab3c59e38ec37baf1ec9b5`; the earlier normalized-self convention describes that terminal owner boundary, not bytes appended by root.
- **Review-target correction:** the earlier G2 closure narrative recorded a then-live target of 22 accepted reviews / 12 C1. The human later reduced the target to approximately 20 accepted rounds. Final review accounting belongs only to G7/G8; neither number supplies G2 content-review credit. R27/R28 remain unexecuted, and G2 still infers no missing review.
- **Current decision identities:** D1 146 / 17,396 / `063bc746a51286efccce3a2137f9141fbd5c2f2861bdc0f7ea8020f648de052b`; D2 176 / 18,237 / `9987c35caffbcda50e1bcdc63bdd69e6dae8d347e8a3150b846d6664666241a6`; D3 164 / 17,589 / `93ebe9c6ae81837da42f4eccc6176bc017e643f5381d3998d9d2757b7c9fb9ee`; D4 195 / 19,460 / `02009420fc0f6bb10025ab08e9df7393bf08e0a61ada5acb4120ac231fed579e`; D5 132 / 12,350 / `5ec471cc37d389202ec86051253337f9d6db26ca6c8f4b74142aa36030a225d2`; D6 146 / 15,392 / `bdcf92c01be055e53d43bd2261376e1bcfb3e153914312d2cbb1e71ef75c9967`; D7 138 / 12,222 / `28d6f8d147674d842252d570d4224a0a8a7f3241016e709cf5e4fd67cd6941f2`; index 100 / 11,040 / `c8c78cc4dd908902aa82ff380d24868deb12a4ad9a118a2679605053114caa26`; deferred register 126 / 14,783 / `7279a80c0d6c3bb5c418d91ba127f044f2dadd398f7904212df452f7781288ed`.
- **Gate:** all nine files retain the required provenance/status boundary; scoped `git diff --check` is clean. Exact residual controlled-word uses remain the canon quotation, the explicit no-approximation prohibition, and scoped negative claim structures already dispositioned by G2.
