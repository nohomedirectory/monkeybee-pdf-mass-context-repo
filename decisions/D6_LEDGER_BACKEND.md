---
generated-by: Claude G2 owner (claude-opus-4-8, effort xhigh)
date: 2026-07-14
revised-by: Codex G2 owner
revised-date: 2026-07-16
inputs:
  - CYCLE_0_WORK_ORDER.md §4 resolve-now item 6, §5 (day-zero checklist), §6
  - MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md §29.5, §29.8, §30.1, §33.1, §33.3, §33.4, §34.9, §35
  - MONKEYBEE_CAMPAIGN_CHARTER_v1.md §3 (day-zero track), §10 (commitment mechanics)
  - AGENTS.md rules 5, 12, and the G0 extension (rules 15, 18, 20)
  - ledger/owners/G3_STATE.md accepted R01-A07 disposition (operational disposition evidence only)
  - ledger/owners/G6_STATE.md dispositions R21-A02 and R21-A07 (operational disposition evidence only)
  - CYCLE_0_WORK_ORDER_v1.1.md proposed commitment/schema repairs (not governing canon)
status: PROPOSED
evidence-status: provisional-pending-substrate
decision-id: D6
ratification: PROPOSED — awaiting human ratification
---

# D6 — Persistent ledger backend

## The distinction that must come first

Two different things are called "the ledger," and confusing them would be a serious error:

| | **The production ledger (this decision)** | **The tamper-evident commitment substrate (not this decision)** |
|---|---|---|
| What it is | The project's own durable, append-oriented record of what happened | An independently held, witnessed, timestamped commitment channel |
| Holds | Models, harness versions, attempts, failed branches, discarded candidates, cost, human hours, selection decisions, sealed cycle trial records | Hashes of committed artifacts, held by a party who is not us |
| Governed by | Rev 7 §33.1, §33.3, §34.9; Charter §3.1 | Rev 7 §33.4; Charter §3.2, §10 |
| Trust property | Durable event representation and integrity checks. **A backend cannot prove event completeness or provide tamper-evidence against its writers.** | Tamper-evidence within the independently witnessed scope |
| Who resolves it | **G2 — this brief** | Human-bound; packaged by G5; a day-zero not-done item |

Rev 7 §35 lists them as separate rows ("Persistent ledger backend" and "Evaluation precommitment substrate"), and the Charter is blunt that "a bare git timestamp is insufficient" and "a git commit alone is decoration."

**The consequence for this brief:** no backend choice can make the production ledger tamper-evident. A hash chain detects *accidental* corruption and *casual* editing; it does not defend against an adversary — or an over-eager agent — with write access to the repository, who can simply recompute the chain. Tamper-evidence comes only from the external substrate. Any claim otherwise would be an overclaim of exactly the kind the campaign exists to avoid, and it is stated here so that no later reader mistakes the hash chain below for the substrate.

## Cross-artifact disposition boundary

The C1 plan owner accepted R01-A07: prospective event capture needs a low-dependency append path before candidate work and a later seal that binds final roots. This brief preserves that lifecycle; a final cycle record cannot serve as the producer of its own earlier events.

G6 also qualified R21-A02 and R21-A07. The proposed Charter-set v1.1 files make commitment entry #1 a canonical batch record/root and propose one versioned `CycleTrialRecordSchemaId`. Those successors remain `PROPOSED — awaiting human ratification`. D6 therefore requires a versioned record/preimage interface and a shard-head manifest, but it does not silently ratify the batch ordinal or the proposed trial schema. Both remain in the human queue.

## The question

What stores the production ledger?

## What the ledger has to be good at

- **Append-oriented, from many concurrent writers.** This run alone has a root orchestrator, five owners, and a stream of fresh reviewers writing at once — and AGENTS.md rule 5 forbids any agent from overwriting another's work.
- **Crash-safe.** An agent dying mid-write must not corrupt the record. This run has already logged compaction events and pane restarts.
- **Independently decodable and verifiable.** The ledger's purpose includes outside review (§33). The schema, canonical preimage grammar, shard manifest, and verifier procedure therefore travel with it; no adjudicator should need a MonkeyBee binary or trust a generated index.
- **Hashable and committable.** A canonical manifest root covering every admitted shard head goes into the external substrate.
- **Diffable and reviewable.** It lives alongside the campaign in git; a reviewer should see what changed.

## Options

### Option A — Append-only JSONL files, hash-chained

One record per line; each record carries the digest of the previous record.

- **For:** Textual and diff-friendly; a fixed schema can be decoded without a MonkeyBee binary. The claims "zero dependencies," "any tool," and indefinite future readability are not supportable and are not used.
- **Against:** No query engine — answering "what did model X cost across cycles 1–4?" means writing a script. Concurrent appends from many agents to *one* file can interleave and corrupt lines. Large volumes get unwieldy.

### Option B — SQLite (or a SQLite-class embedded database)

- **For:** Transaction and query facilities are candidate benefits. Exact durability, concurrency, binding, and version properties are `[UNVERIFIED]` until an implementation is selected and tested.
- **Against:** Binary storage is not line-diffable and requires a compatible database reader. That does not make independent reading impossible, but it adds a tool and export surface to the evidence handoff. Any binding and license choice remains subject to the unresolved dependency policy; no implementation is selected here.

### Option C — Hash-chained JSONL as the source of truth, with a derived, regenerable index — **recommended**

- Durable truth: append-only, hash-chained JSONL shards, with a canonical manifest of every shard head committed through the external substrate.
- Convenience: an optional SQLite (or in-memory) index **built from** the JSONL for querying. The index is *derived*, never authoritative, and is regenerable from the files at any time.

This is the shape canon already prefers, in two places:

- §29.5, "Generated knowledge must remain derivable" — a derived index that can be rebuilt from the source of truth is exactly this pattern.
- AGENTS.md G0 extension rule 15: "Generated or operational state never silently upgrades or supersedes canon," and rule 20: "Generated prose cannot strengthen a claim."

**Concurrency, bounded structurally:** each writer owns its own shard — `ledger/events/<writer-id>.jsonl` — so concurrent writers do not append to the same file. Each record carries a monotone shard sequence number and predecessor digest. Timestamps are observations, not an authoritative global clock. A derived view may sort by a declared deterministic key for navigation, but it cannot manufacture causal or wall-clock order. Cross-shard order exists only where an explicit causal link or witnessed commitment batch records it.

**Crash safety candidate:** append with platform-appropriate append and durability semantics, verified by a kill test. A torn suffix is not admitted as a record; its raw bytes are retained for diagnosis, and recovery emits a new linked diagnostic rather than silently rewriting history. Exact operating-system guarantees are `[UNVERIFIED]` until the test and implementation contract exist.

## Recommendation

**PROPOSED — awaiting human ratification. Adopt Option C.**

1. **Source of truth:** hash-chained, append-only JSONL, one shard per writer, under `ledger/`. Every shard has a stable writer identity, schema version, monotone sequence, and predecessor digest.
2. **Record schema and hash preimage are versioned.** Every record carries: declared timestamp plus clock provenance, writer identity and sequence, event class, payload, predecessor digest, schema/preimage IDs, and `evidence-status`. The chain digest is computed over the D2 canonical encoding of the typed record under a distinct ledger-record domain; it is not computed over an unspecified JSON parse. The JSONL representation and canonical typed record must round-trip or verification fails.
3. **`retrospective` is a first-class flag on every record** (§33.3: retrospective entries "are labeled `retrospective` and never support prospective claims"). A record written after the fact and not marked is a blocking integrity defect under the human-ratified review protocol; this brief does not self-assign its grade. The schema must make the flag structurally impossible to omit.
4. **A canonical shard-head manifest is what gets committed to the external substrate.** It binds every writer/shard ID, head digest, last admitted sequence, record-schema/preimage versions, and the prior manifest root. There is no singular global chain head unless the manifest itself supplies it. Adding or omitting a shard changes the manifest root.
5. **Derived indexes are regenerable and never authoritative.** Any query tool rebuilds from the JSONL; the index is never the thing that is hashed, committed, or cited.
6. **Honest scope statement, to be carried in the ledger's own header:** this backend represents admitted events durably and detects divergence from a previously witnessed shard-head manifest. It does not prove that every real event was recorded, and before an external commitment a writer with repository access can rewrite records and recompute local chains. §33.4's independently held substrate is human-bound and currently not-done.

## Rationale

The ledger is an evidentiary artifact before it is a query store. Text shards keep review and diff surfaces visible, while the derived index remains explicitly non-authoritative. Verification is not a shell one-liner: it requires the versioned schema, D2 preimage grammar, shard-chain check, and manifest-root check. The recommendation prefers that disclosed verifier surface to a binary-only source of truth; no global readability or query-performance claim is made.

Per-writer sharding is more than an implementation detail. A multi-agent swarm appending to one file creates an interleaving risk. Unique writer admission, shard ownership, and per-shard sequence checks reduce that risk; sharding alone does not prove that two writers never received the same identity.

## Reversibility and migration path

**High at the storage-format layer; low for missing prospective history.**

- JSONL → SQLite and SQLite → JSONL are plausible migrations only with a tested, lossless mapping of schema versions, record identities, predecessor links, shard membership, and manifest roots. Neither direction is called trivial here.
- Changing the record schema: versioned records; old records remain readable under their version.

The one thing that does *not* migrate cleanly is a **gap in the record.** Whatever backend is chosen, the ledger's value depends on its completeness from day zero, and a period during which nothing was written cannot be reconstructed later except as `retrospective` entries, which by §33.3 support no prospective claim. **The cost of choosing the backend slowly is higher than the cost of choosing it wrong**, because the ledger is supposed to be recording from the first implementation agent onward (Charter §3.1: "Production ledger opens before any implementation agent runs").

That is the real risk here, and it is a scheduling risk rather than a technical one.

## Dependencies

- **Consumes:** D1 (shard and manifest digests) and D2 (typed record and manifest preimages). D1/D2 ratification must precede the first evidence-bearing external commitment; no local hash chain substitutes for that ratification.
- **Consumed by:** the day-zero production ledger (Charter §3.1); every sealed cycle trial record (§34.9's close gate); the Q3 package's provenance column (Charter §7).
- **Feeds:** the external commitment substrate (§33.4) — the canonical shard-head manifest root is what gets committed. The substrate itself is *not* this decision.
- **Constrains:** nothing in the engine. The ledger is tooling, not runtime (§30.1 package roles).

## Evidence still needed before ratification

1. **A volume and throughput estimate.** The write path and manifest cadence require a project-workload check. `[UNVERIFIED — not measured in this phase.]`
2. **The record schema itself**, which G3's C1 plan and the close-gate definition (§34.9's sealed trial record: "attempts, failures, retries, cost, human interventions, median and best outcomes") both depend on.
3. **Crash and concurrency tests** — kill a writer mid-record; retain and diagnose a torn suffix; run concurrent shards with skewed/equal timestamps; prove per-shard sequence integrity, manifest inclusion, deterministic derived-view behavior, and the absence of an inferred authoritative global order.
4. **A decision on where token/cost telemetry comes from.** This run's ledger already records honestly that "provider token and monetary telemetry are not yet available" and that absence "will be labeled rather than estimated" — the schema must make that labeling structural.

## Blast radius if wrong

| Failure | Consequence | Severity |
|---|---|---|
| Binary-only backend chosen without an independent handoff format | Outside review requires a database reader and a separately verified export path; git diff no longer exposes record-level changes. | Moderate and evidentiary. Recoverable only if the export is bound to the same committed roots. |
| Ledger opens late, or has gaps | Missing periods can only be reconstructed as `retrospective` entries, which support no prospective claim (§33.3). The foundry-distribution evidence (§34.9) is permanently thinner. | **High, and unrecoverable.** The real risk. |
| Concurrent writers corrupt a shared file | Lost or interleaved records; the chain breaks; recovery is manual. | Moderate — and structurally prevented by per-writer sharding. |
| Shards are merged by timestamp as if that proved chronology | Clock skew or equal timestamps manufacture a false global order; selection/attempt chronology may be misstated. | High for foundry evidence. Prevented by per-shard sequence, explicit causal links, and witnessed batch manifests. |
| A shard is omitted from the committed manifest | The apparent ledger can exclude a writer's events while every included shard verifies. | High and potentially silent. Prevented only if writer/shard admission and manifest membership are themselves controlled and audited. |
| Hash chain mistaken for tamper-evidence | The project believes it has a §33.4 substrate when it has a detection mechanism. A reviewer discovers this and discounts the provenance claim — correctly. | **High, and it is an integrity failure rather than a technical one.** Prevented by stating the limit in the ledger's own header, which recommendation item 6 requires. |

## Human ratification

This brief proposes; it does not decide (Rev 7 §29.9).

- [ ] **Ratify Option C** — hash-chained JSONL source of truth + derived regenerable index, per-writer shards (recommended)
- [ ] **Ratify Option A** — plain hash-chained JSONL, no index
- [ ] **Ratify Option B** — SQLite-class backend (recording the independent-readability cost)
- [ ] **Amend** (record the variant and rationale)

Ratifier: ______________________ Date: ____________
