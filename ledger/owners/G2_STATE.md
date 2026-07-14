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
status: DRAFT
evidence-status: provisional-pending-substrate
owner: G2
owner-fsm: SUBMIT-FOR-REVIEW
---

# G2 Owner Checkpoint — Decisions

## Transition record

| Phase | Timestamp | Checkpoint |
|---|---|---|
| `INGEST` | 2026-07-14T16:33:09+02:00 | Governing instructions read in full; authority, scope, and deliverables recorded before any broader work |
| `DRAFT` | 2026-07-14T16:40:48+02:00 | Decision-bearing canon read at stable section IDs; three primary-standards fetches logged; option space grounded; `decisions/` authoring begun |
| `SELF-CHECK` | 2026-07-14T16:52:00+02:00 | Nine artifacts on disk; scope, canonical-integrity, claim-vocabulary, clean-room, provenance, citation, and de-slopification checks run; two self-found defects repaired |
| `SUBMIT-FOR-REVIEW` | 2026-07-14T16:56:16+02:00 | G2 stops here. Root routes fresh reviewers. No commit, no push, no `REVISE` without a reviewer packet. |

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
