---
generated-by: Claude G2 owner (claude-opus-4-8, effort xhigh)
date: 2026-07-14
inputs:
  - CYCLE_0_WORK_ORDER.md §4 resolve-now item 6, §5 (day-zero checklist), §6
  - MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md §29.5, §29.8, §30.1, §33.1, §33.3, §33.4, §34.9, §35
  - MONKEYBEE_CAMPAIGN_CHARTER_v1.md §3 (day-zero track), §10 (commitment mechanics)
  - AGENTS.md rules 5, 12, and the G0 extension (rules 15, 18, 20)
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
| Trust property | Durability and completeness. **It is not tamper-evident against us.** | Tamper-evidence, *because custody is independent* |
| Who resolves it | **G2 — this brief** | Human-bound; packaged by G5; a day-zero not-done item |

Rev 7 §35 lists them as separate rows ("Persistent ledger backend" and "Evaluation precommitment substrate"), and the Charter is blunt that "a bare git timestamp is insufficient" and "a git commit alone is decoration."

**The consequence for this brief:** no backend choice can make the production ledger tamper-evident. A hash chain detects *accidental* corruption and *casual* editing; it does not defend against an adversary — or an over-eager agent — with write access to the repository, who can simply recompute the chain. Tamper-evidence comes only from the external substrate. Any claim otherwise would be an overclaim of exactly the kind the campaign exists to avoid, and it is stated here so that no later reader mistakes the hash chain below for the substrate.

## The question

What stores the production ledger?

## What the ledger has to be good at

- **Append-oriented, from many concurrent writers.** This run alone has a root orchestrator, five owners, and a stream of fresh reviewers writing at once — and AGENTS.md rule 5 forbids any agent from overwriting another's work.
- **Crash-safe.** An agent dying mid-write must not corrupt the record. This run has already logged compaction events and pane restarts.
- **Independently readable.** This is the property that outranks the others. The ledger's *purpose* is to be read by an external adjudicator deciding whether MonkeyBee's foundry claims are grounded (§33). A record that requires our tooling to read is a record the adjudicator must take on trust — which defeats the point of having it.
- **Hashable and committable.** Its head digest goes into the external substrate.
- **Diffable and reviewable.** It lives alongside the campaign in git; a reviewer should see what changed.

## Options

### Option A — Append-only JSONL files, hash-chained

One record per line; each record carries the digest of the previous record.

- **For:** Zero dependencies. Trivially readable by any human, any tool, any language, forever. Diff-friendly. Already what this run does (`ledger/RUN_LEDGER.md` in prose; the structured form is the upgrade). Hashing the head is trivial. Survives every tooling change the project will ever make.
- **Against:** No query engine — answering "what did model X cost across cycles 1–4?" means writing a script. Concurrent appends from many agents to *one* file can interleave and corrupt lines. Large volumes get unwieldy.

### Option B — SQLite (or a SQLite-class embedded database)

- **For:** Transactional, WAL-based crash safety; real concurrency handling; queryable.
- **Against:** **Binary.** An external adjudicator cannot read it without our tooling or theirs, which cuts directly against the ledger's reason for existing. It diffs as an opaque blob, so a reviewer cannot see what changed and git cannot merge it. And a C-backed SQLite binding sits awkwardly with Rev 7 §35's pure-Rust dependency preference — though note §30.1's package-role distinction genuinely does admit it: the ledger tooling is a `lab-tool` or `build-tool`, not the shipped `runtime`, so a C dependency there is not the violation it would be in the engine. The disqualifying objection is evidentiary, not technical.

### Option C — Hash-chained JSONL as the source of truth, with a derived, regenerable index — **recommended**

- Durable truth: append-only, hash-chained JSONL files, committed to git and hashed into the substrate.
- Convenience: an optional SQLite (or in-memory) index **built from** the JSONL for querying. The index is *derived*, never authoritative, and is regenerable from the files at any time.

This is the shape canon already prefers, in two places:

- §29.5, "Generated knowledge must remain derivable" — a derived index that can be rebuilt from the source of truth is exactly this pattern.
- AGENTS.md G0 extension rule 15: "Generated or operational state never silently upgrades or supersedes canon," and rule 20: "Generated prose cannot strengthen a claim."

**Concurrency, solved structurally:** each writer owns its own shard — `ledger/events/<agent-id>.jsonl` — so concurrent agents never append to the same file and cannot interleave. A merge step composes the total order from timestamps and the per-shard hash chains. This directly discharges AGENTS.md rule 5 (never overwrite another agent's work) at the storage layer instead of by convention, which is where multi-agent safety should live.

**Crash safety:** append with `O_APPEND`, fsync per record or per explicitly declared batch. A torn final line is detected by the chain and is **dropped with a recorded diagnostic** — never silently repaired, and never silently kept.

## Recommendation

**PROPOSED — awaiting human ratification. Adopt Option C.**

1. **Source of truth:** hash-chained, append-only JSONL, one shard per writer, under `ledger/`.
2. **Record schema is versioned**, and every record carries: timestamp, writer identity (agent + model family + effort, exactly as this run already records), event class, payload, the previous record's digest, and an `evidence-status` field.
3. **`retrospective` is a first-class flag on every record** (§33.3: retrospective entries "are labeled `retrospective` and never support prospective claims"). A record written after the fact and not marked is a Grade-A finding — the flag must be structurally impossible to omit, not merely required by policy.
4. **The chain's head digest is what gets committed to the external substrate.** Cheap, and it is the only thing that makes the ledger's integrity externally checkable.
5. **Derived indexes are regenerable and never authoritative.** Any query tool rebuilds from the JSONL; the index is never the thing that is hashed, committed, or cited.
6. **Honest scope statement, to be carried in the ledger's own header:** this backend provides durability, completeness, and *tamper-detection*. It does not provide tamper-*evidence* against a party with repository write access. That property comes only from §33.4's independently held substrate, which is human-bound and currently not-done.

## Rationale

The ledger is an evidentiary artifact before it is a data store, and its consumer is a skeptical outsider. That single observation settles the choice: the format that a stranger can read with no tools, verify with a shell one-liner, and diff in a pull request beats the format with better query ergonomics, because query ergonomics are our convenience and readability is their trust. The derived index recovers our convenience at no evidentiary cost, which is why the hybrid dominates rather than compromises.

Per-writer sharding is worth calling out as more than an implementation detail. A multi-agent swarm appending to a shared file is a data race dressed as a logging strategy; solving it at the storage layer means no future agent can violate rule 5 by accident.

## Reversibility and migration path

**High — this is the most reversible decision in the resolve-now set, and it should be ratified with correspondingly less agonizing.**

- JSONL → SQLite: trivial import.
- SQLite → JSONL: straightforward export.
- Changing the record schema: versioned records; old records remain readable under their version.

The one thing that does *not* migrate cleanly is a **gap in the record.** Whatever backend is chosen, the ledger's value depends on its completeness from day zero, and a period during which nothing was written cannot be reconstructed later except as `retrospective` entries, which by §33.3 support no prospective claim. **The cost of choosing the backend slowly is higher than the cost of choosing it wrong**, because the ledger is supposed to be recording from the first implementation agent onward (Charter §3.1: "Production ledger opens before any implementation agent runs").

That is the real risk here, and it is a scheduling risk rather than a technical one.

## Dependencies

- **Consumes:** D1 (the chain's hash function) and D2 (records are canonically encoded before hashing — otherwise the chain commits to an ambiguous preimage, and D2's ambiguity analysis applies to the ledger exactly as it applies to identities).
- **Consumed by:** the day-zero production ledger (Charter §3.1); every sealed cycle trial record (§34.9's close gate); the Q3 package's provenance column (Charter §7).
- **Feeds:** the external commitment substrate (§33.4) — the chain head is what gets committed. The substrate itself is *not* this decision.
- **Constrains:** nothing in the engine. The ledger is tooling, not runtime (§30.1 package roles).

## Evidence still needed before ratification

1. **A volume and throughput estimate.** If a swarm generates ledger records at a rate where plain-file append becomes a bottleneck, the derived-index side of the hybrid absorbs the read load, but the write path should be sanity-checked. `[UNVERIFIED — not measured; measurement of our own tooling is permitted, but has not been done this phase.]`
2. **The record schema itself**, which G3's C1 plan and the close-gate definition (§34.9's sealed trial record: "attempts, failures, retries, cost, human interventions, median and best outcomes") both depend on.
3. **A crash-safety test** — kill a writer mid-record; confirm the chain detects the torn line, drops it, and records the diagnostic.
4. **A decision on where token/cost telemetry comes from.** This run's ledger already records honestly that "provider token and monetary telemetry are not yet available" and that absence "will be labeled rather than estimated" — the schema must make that labeling structural.

## Blast radius if wrong

| Failure | Consequence | Severity |
|---|---|---|
| Binary-only backend chosen | The production ledger — the core of the Q3 provenance claim — becomes an artifact an external adjudicator cannot independently read or verify. The claim it exists to support is weakened by the way it is stored. | Moderate, and **evidentiary rather than technical**. Recoverable by export, but a reviewer who was handed a database and asked to trust it has already formed an impression. |
| Ledger opens late, or has gaps | Missing periods can only be reconstructed as `retrospective` entries, which support no prospective claim (§33.3). The foundry-distribution evidence (§34.9) is permanently thinner. | **High, and unrecoverable.** The real risk. |
| Concurrent writers corrupt a shared file | Lost or interleaved records; the chain breaks; recovery is manual. | Moderate — and structurally prevented by per-writer sharding. |
| Hash chain mistaken for tamper-evidence | The project believes it has a §33.4 substrate when it has a detection mechanism. A reviewer discovers this and discounts the provenance claim — correctly. | **High, and it is an integrity failure rather than a technical one.** Prevented by stating the limit in the ledger's own header, which recommendation item 6 requires. |

## Human ratification

This brief proposes; it does not decide (Rev 7 §29.9).

- [ ] **Ratify Option C** — hash-chained JSONL source of truth + derived regenerable index, per-writer shards (recommended)
- [ ] **Ratify Option A** — plain hash-chained JSONL, no index
- [ ] **Ratify Option B** — SQLite-class backend (recording the independent-readability cost)
- [ ] **Amend** (record the variant and rationale)

Ratifier: ______________________ Date: ____________
