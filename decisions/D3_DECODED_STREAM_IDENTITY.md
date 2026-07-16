---
generated-by: Claude G2 owner (claude-opus-4-8, effort xhigh)
date: 2026-07-14
revised-by: Codex G2 owner
revised-date: 2026-07-16
inputs:
  - CYCLE_0_WORK_ORDER.md §4 resolve-now item 3 ("DecodedStreamId cost/availability model")
  - MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md §9.1.1, §9.2, §9.5, §9.6, §11.2, §11.2.2, §11.9, §12.1, §12.9, §26.4, §26.6, Appendix A.6
  - AUDIT_FINDINGS_LEDGER.md R2-N2, R2-N3
status: PROPOSED
evidence-status: provisional-pending-substrate
decision-id: D3
ratification: PROPOSED — awaiting human ratification
---

# D3 — Decoded-stream identity: cost and availability model

## Naming: a drift that must be settled before the decision is stated

The Work Order §4 item 3, the Charter, the Overnight Goal, and the Owner Marching Orders all name **`DecodedStreamId`**. That identifier occurs **zero times** in Rev 7. Rev 7 §9.2's identity table names **`DecodedContainerId`** — "one decoded container under a source/object/security/filter/algorithm identity" — which is the only decoded-artifact identity in the domain canon.

- Evidence: over `MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md`, `grep -c "DecodedStreamId"` = 0; `grep -c "DecodedContainerId"` = 2.
- This is campaign-layer-to-domain-canon name drift, the same class as audit rows R1-1 and R2-N7 — both of which are duplication drift, and both of which are Grade A.
- **Disposition:** this brief treats `DecodedContainerId` (Rev 7 §9.2) as the canonical name and `DecodedStreamId` as a campaign-layer alias for it. Nothing in the substance of the decision turns on the name. Recorded as finding **F-G2-1** in `ledger/owners/G2_STATE.md` and routed to root for a `DISPUTES.md` entry — `DISPUTES.md` is orchestrator-owned and G2 does not edit another owner's paths. The correct fix is a naming reconciliation, not a new identity.

"Container" is also the more accurate word, and canon chose it deliberately: the identity covers object streams and any decoded artifact, not only content streams. The alias should be retired rather than blessed.

## The question

When does a decoded container acquire an identity, what does that identity commit to, and what does it cost to have one?

## Why this is a real decision and not a naming exercise

Rev 7 §9.5 defines the provenance chain and states that every virtual span carries, among other things, a **"decoded artifact hash"**:

```text
file byte span
  -> filter/decryption derivation
  -> decoded-container artifact
  -> virtual decoded span
  -> parsed object or program node
```

Read literally, that requires hashing the decoded bytes of every stream. That collides with three other laws, and the collision is the decision:

1. **§9.6 / §26.4 lazy, demand-driven derivation.** "A page thumbnail does not require complete text extraction, full structure validation, or unrelated attachment decoding." Bet 13 is demand-driven parsing. A content hash of a decoded artifact requires *fully decoding* it — so a literal reading makes every identity eager and defeats laziness.
2. **§11.2 budgets and the decode-bomb limits.** If naming a container requires decoding it, then an attacker can force expensive decode work merely by causing the container to be *referenced*. Naming becomes an attack surface.
3. **§12.1 progressive/streaming sources and §9.1.1 `Ephemeral` identities.** For a source whose bytes are not all available, a whole-artifact content hash may never be computable at all. §9.1.1 is explicit that `Ephemeral` supports only `ObservedBytes`, never durable whole-source `ByteExact` evidence.

So the question is not cosmetic. It is: *is a decoded container named by what it is, or by how it was made?*

## Options

### Option A — Content identity (eager): `DecodedContainerId` = hash of the full decoded bytes

- **For:** A content-derived identity directly commits to the decoded bytes; two identical decoded artifacts can share one identity regardless of how they were produced.
- **Against:** The identity is unavailable until the artifact is fully decoded, which makes it unavailable for deciding whether to decode. It forces full materialization when a consumer requests only a bounded range. It converts naming into decode work, so it amplifies decode-bomb pressure rather than bounding it. It is unavailable as a whole-artifact content identity for incomplete streaming and `Ephemeral` sources. **Rejected on those stated constraints.**

### Option B — Derivational identity (recipe): `DecodedContainerId` = hash of how it is made

The identity is the canonical encoding (D2) of the derivation tuple, which §9.2 already spells out — "under a source/object/security/filter/algorithm identity":

`(SourceRootId, ObjectVersionId, source byte span, filter chain + decode params, cryptographic context, decoder algorithm + version, outcome-sensitive limits, profile)`

- **For:** Available *before* decoding, at metadata cost. Enables lazy decode, partial reads, streaming, and cheap budget decisions. Qualifies virtual spans (§9.5 needs to say *which container* an offset is inside, and a recipe identity does that perfectly well). Costs no decode work to mint.
- **Against:** It names the recipe, not the bytes. Two different recipes that happen to produce identical bytes get different identities — no false equality, but a missed sharing opportunity. The dangerous direction is real: **the same recipe under a buggy, nondeterministic, or silently-updated decoder can name different bytes.** A durable cross-run cache keyed on recipe alone could therefore serve the wrong bytes under a valid-looking identity. That is a severe, silent evidence-corruption failure.

### Option C — Hybrid: two typed, distinct identities — **recommended**

Keep both, and never let either impersonate the other.

| | `DecodedContainerId` (recipe) | `DecodedArtifactDigest` (content) |
|---|---|---|
| What it is | Canonical hash (D2/D1) of the derivation tuple above | Content digest of the committed decoded bytes |
| Available | Before decoding, at metadata cost | Only after a **successful commit** (Appendix A.6) |
| Used for | Cache candidate lookup, budget decisions, diagnostics, qualifying virtual spans, addressing a container that has not been (and may never be) decoded | Evidence; verification on cache reuse; any byte-exactness claim over decoded bytes |
| Lives in | The identity grammar (§9.2) | The `DecodeCommitReceipt` (Appendix A.6) and the §9.5 virtual-span record |

This reading is not an invention; it is what canon already implies once the pieces are laid side by side. §9.5 lists *both* "filter chain and decode parameters" *and* "decoded artifact hash" as things a virtual span carries — i.e. recipe and content, together. Appendix A.6 already mints a `DecodeCommitReceipt` at commit and already enforces the terminal-state law: "a byte-filter stage is not visible as a completed decoded artifact until commit succeeds." The content digest is a *post-commit evidence field*; the recipe identity is a *pre-decode address*. The hybrid simply names that split and makes the availability states explicit.

## Recommendation

**PROPOSED — awaiting human ratification. Adopt Option C.**

### The availability model

A decoded container is always in exactly one of these states, and the state is a typed value, never an inference:

| State | Meaning | What may be claimed |
|---|---|---|
| `Planned` | Recipe known; not decoded | Addressing, budgeting, diagnostics. **No claim about content.** |
| `Materialized { digest }` | Decode committed; content digest known | Byte-exactness over the decoded artifact; durable cross-run reuse (subject to §9.6 manifest validation) |
| `Materialized { digest: NotComputed }` | Decode committed under an explicit transient profile that skipped hashing | Operation-local use only. **No durable reuse, no byte-exact claim.** |
| `Refused { cause }` | Budget exhausted, limit fired, cancellation, or decoder refusal | Nothing about content. The refusal itself is evidence (§10, P17: no unsupported success). |

A claim that needs a content digest and finds one absent **degrades or refuses; it never invents one.** This is the §9.1.1 pattern applied one level down — that section already refuses to let prose promote a partial `Ephemeral` range into durable whole-source exactness, and the same discipline applies here.

### The cost model

1. **Minting a `DecodedContainerId` is classified as metadata work** — one canonical encoding and one hash of the bounded recipe tuple. The exact cost is `[UNVERIFIED]`, but the operation performs no decoded-byte production.
2. **The content digest is computed incrementally, in-line with the decode**, as bytes flow through `DecodeWriteTxn::write` (Appendix A.6). The hash adds bounded state and does not itself require buffering the whole artifact or a second decoded-byte pass. Its measured overhead remains evidence-needed item 2. This narrows Option A's cost objection while keeping its evidentiary value — the objection to eager content identity was the forced *decode*.
3. **Charging follows §11.2.2 exactly:** the physical decode (and its hash) is charged once, to the operation that produced it; logical consumers get attribution without re-charging the physical counter. Cache hits still charge bounded lookup and materialization work and cannot reset global allowances.
4. **Hashing is mandatory whenever the artifact is retained, cached, or referenced by evidence.** It is skippable only under an explicit transient profile, which lands the container in `Materialized { digest: NotComputed }` and forfeits every durable claim. The default is to hash; skipping is opt-in and costs capability, not correctness.
5. **Reuse is validated, never assumed.** §9.6's two-stage law governs: the recipe identity may locate a *candidate* cache entry, but it never authorizes reuse. Reuse requires validating canon's dependency-and-selection manifest and, under this recommendation, **verifying the content digest of the reused artifact**. A recipe match is a hypothesis; the digest supplies a byte-integrity check rather than authority or semantic equivalence.
6. **`Ephemeral` sources (§9.1.1) never produce durably reusable containers.** Their decoded containers are operation-local by inheritance. This falls out of canon and is restated so no implementer re-derives it wrongly.

### One security law worth stating explicitly

The recipe tuple includes a **non-secret cryptographic-context identity**. It never contains a credential, raw key, password, or decrypted content. Two containers decoded from the same source occurrence under different authorized contexts must not share a recipe identity, and a decoded container derived from an encrypted stream must never be cached into a context authorized to see only the encrypted form. §9.6 partitions the candidate index "by tenant, security context, sensitivity/disclosure class, and cache-isolation domain"; this decision inherits that partitioning. The exact non-secret context fields and their disclosure properties require the threat model named below.

The post-commit content digest also inherits the decoded artifact's sensitivity. It is not public metadata by default: exporting it across a tenant, disclosure class, or cache-isolation boundary requires explicit authority because a digest can act as a confirmation oracle for guessed content. This control does not change the digest algorithm or the recipe identity; it constrains storage and disclosure.

Related, from R2-N2 (the hasher law): the cache index keyed by these identities is an **attacker-keyed map**. It requires DoS-resistant hashing or ordered structures. That is a distinct concern from the content-hash choice (D1) — the identity digest is cryptographic; the *hash-map hasher* over those digests is a separate mechanism, and a performance-motivated swap of it requires an explicit contract note. Naming this here because a cache index is exactly where the R2-N2 defect would land.

## Rationale

The key distinction is that a recipe identity and a content identity answer different questions at different times. "Which container is this span inside?" must be answerable before decoding — a content identity cannot answer it. "Are these bytes the bytes I think they are?" must be answerable before durable reuse — a recipe identity cannot answer it, because it assumes decoder determinism rather than proving it.

Collapsing the two, in either direction, produces a specific and predictable bug. Content-only (A) makes naming expensive and defeats laziness. Recipe-only (B) makes durable cache reuse rest on an *assumption* of decoder determinism, and assumptions of determinism are exactly what the D-class discipline (§11.9) exists to convert into verified claims. The hybrid costs one 32-byte field per container and one streaming hash pass, and it converts that assumption into a check.

## Reversibility and migration path

**High, subject to the exception below.**

Adding a content digest later to a recipe-only design is straightforward: it is a new field in the receipt and a new precondition on durable reuse. Removing it later is likewise easy. The identity grammar is versioned (§9.2), and decoded containers are derived artifacts, not committed evidence roots — they can be recomputed from their recipe.

The path-dependent case is shipping recipe-only durable cross-run caching in C1 and discovering a nondeterministic decoder in C2 or later. At that point every artifact reused from cache under the old law is suspect, and every receipt that depended on one has to be re-derived. Landing the hybrid before durable caching exists avoids that retrospective invalidation; its actual runtime cost remains evidence-needed item 2.

## Dependencies

- **Consumes:** D1 (hash algorithm) and D2 (the recipe tuple is a canonically encoded structured value). Cannot be implemented before those are ratified, though it can be *planned* against them.
- **Consumed by:** the C1 filter/decoder stack (Flate + predictors, ASCIIHex, ASCII85, RunLength, LZW), object streams (§12.9), the cache hierarchy (§26.6, whose "decoded streams" tier this *is*), and every virtual span (§9.5).
- **Interacts with:** §11.2's decode budgets and the decode-bomb limits; §9.6's validated-manifest reuse law; R2-N2's hasher law at the cache index.
- **Gates:** C1's decoded-artifact provenance and any byte-exactness claim over decoded content.

## Evidence still needed before ratification

1. **A decoder-determinism audit.** The hybrid's value depends on decoders being deterministic (D0). Each C1 decoder needs its determinism class declared and tested — this is a C1 acceptance criterion, and it is the thing the content digest is there to *catch* if it is ever untrue.
2. **A measurement of incremental-hash cost as a fraction of decode cost**, taken in C1 when benchmarking is legal. The claim that streaming hashing is cheap relative to inflate is highly plausible and is `[UNVERIFIED]` until measured. If it proved false, the transient-profile escape hatch is the mitigation, not a redesign.
3. **A cache-isolation and digest-disclosure threat model** covering the security-context partitioning above — specifically, whether the recipe tuple carries enough non-secret context to prevent cross-tenant or cross-key reuse, and when a decoded-content digest may be stored or disclosed without becoming a confirmation oracle.
4. **Confirmation of the naming reconciliation** (`DecodedContainerId` vs `DecodedStreamId`) once root routes F-G2-1 into `DISPUTES.md`.

## Blast radius if wrong

| Failure | Consequence | Severity |
|---|---|---|
| Content-only identity adopted (Option A) | Naming requires decoding. Decode-bomb amplification: referencing a container forces its full decode. Lazy rendering (§26.4, Bet 13) is defeated. Streaming and `Ephemeral` sources cannot be addressed at all. | High, but **loud** — it would surface immediately as a performance and DoS failure, not silently. |
| Recipe-only identity with durable cross-run caching (Option B) | A nondeterministic or silently-updated decoder serves wrong bytes under a valid-looking identity. Every downstream claim — text extraction, security inventory, redaction evidence — inherits the corruption with a clean receipt attached. | **Catastrophic and silent.** The failure this recommendation exists to prevent. |
| Content digest present but not verified on reuse | Same as above; the digest is decoration if reuse does not check it. | Catastrophic and silent. Hence recommendation item 5. |
| Hybrid adopted; incremental hashing proves expensive | Performance cost on the decode path. | Low. Bounded by the transient profile; measurable; fixable at a cycle boundary. |

The asymmetry is the point: the recommendation's failure mode is *slow*, and the alternative's failure mode is *wrong and quiet*.

## Human ratification

This brief proposes; it does not decide (Rev 7 §29.9).

- [ ] **Ratify Option C** — hybrid recipe identity + post-commit content digest, with the availability states and cost model above (recommended)
- [ ] **Ratify Option B** — recipe-only (and accept that durable reuse rests on assumed decoder determinism)
- [ ] **Ratify Option A** — content-only (and accept eager decode)
- [ ] **Amend** (record the variant and rationale)
- [ ] Separately: **confirm the naming reconciliation** — `DecodedContainerId` is canonical; `DecodedStreamId` is a campaign-layer alias to retire

Ratifier: ______________________ Date: ____________
