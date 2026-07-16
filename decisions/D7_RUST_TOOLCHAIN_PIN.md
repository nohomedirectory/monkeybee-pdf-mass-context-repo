---
generated-by: Claude G2 owner (claude-opus-4-8, effort xhigh)
date: 2026-07-14
revised-by: Codex G2 owner
revised-date: 2026-07-16
inputs:
  - CYCLE_0_WORK_ORDER.md §4 resolve-now item 7
  - MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md §11.6, §11.7, §11.9, §25.7, §26.9, §26.10, §27 (G5, G6.1), §30.1, §35
  - MONKEYBEE_CAMPAIGN_CHARTER_v1.md §5 (C1 gate: zero reachable panics under the fuzz corpus; C4 release engineering)
  - ledger/owners/G3_STATE.md accepted R41-A03 disposition (operational disposition evidence only)
status: PROPOSED
evidence-status: provisional-pending-substrate
decision-id: D7
ratification: PROPOSED — awaiting human ratification
---

# D7 — Rust toolchain pin

## The question

Which Rust toolchain builds MonkeyBee, how is it pinned, and what happens when it moves?

## What canon already fixes

Rev 7 §30.1 settles more of this than the open-decision row suggests:

- "**Rust 2024 edition or later** pinned toolchain selected before implementation."
- "Workspace lints **deny unsafe code** by default." (With §11.7's capsule protocol as the only escape, and "PDF semantics never justify unsafe code.")
- "**`Cargo.lock` committed** for reproducibility."
- Each crate declares an architectural layer and a **package role** (`runtime`, `adapter`, `lab-tool`, `build-tool`, `release-tool`).

Rev 7 §35 adds: "Rust toolchain — Pinned stable or dated nightly only if essential." And separately: "Minimum supported Rust version — Deferred until dependency set stabilizes."

So the shape is given. The decision is the part canon leaves open, and it turns out to have a wrinkle that the one-line row hides.

## The wrinkle: some C1 assurance tools may require nightly

Charter §5/C1 and the Work Order both make **coverage-guided fuzzing operate from hour one**, with a C1 close gate of "**zero reachable panics under the fuzz corpus**." Rev 7's G5 lane requires fuzzing, and G6.1 requires "Miri or equivalent interpreter checks" and "sanitizers."

Whether the selected `cargo-fuzz`/libFuzzer, Miri, and sanitizer lanes require **nightly** is `[UNVERIFIED as of 2026-07]` and must be checked locally at C1 before a nightly is admitted. Separately, project policy can require a pinned stable toolchain for release artifacts and determinism-bearing product receipts. A stable pin is an input to reproducibility; it does not prove a reproducible build by itself.

The proposal therefore separates the release-build toolchain from any assurance-only nightly that current tool evidence proves necessary. This is an output/invocation boundary, not a claim that only `lab-tool` packages are compiled under nightly: Miri, fuzzing, or sanitizer invocations may compile runtime code for analysis, but they do not produce the admitted release binary.

## Options

### Option A — Pinned stable, with no nightly admitted

- **For:** Keeps one toolchain identity if all selected assurance lanes support it.
- **Against:** Insufficient if a required selected lane is locally proven to require nightly. The current brief does not establish that premise, so this option is conditional rather than rejected.

### Option B — Nightly for everything

- **For:** May support assurance tools that require nightly, subject to local verification.
- **Against:** Expands the release surface exposed to an unstable compiler channel without evidence that release artifacts need it. A pinned nightly can still be a recorded build input; no claim that nightly inherently prevents reproducibility is made. Not proposed for release artifacts.

### Option C — Track latest stable, unpinned

- **Against:** Build identity varies silently. §11.9's D0, D1, and D2 classes *all* condition on pinned dependencies and "deterministic build identity" — an unpinned compiler means a receipt cannot be replayed, and the reproducible-build comparison lane cannot pass. This is not a style preference; it directly voids determinism claims. Rejected.

### Option D — Pinned stable release toolchain plus a conditional pinned assurance nightly — **recommended**

| | Toolchain | Applies to | Why |
|---|---|---|---|
| **Release/build** | Pinned **stable**, exact version, via `rust-toolchain.toml`; edition 2024 (§30.1); `Cargo.lock` committed | `runtime`, `adapter`, `release-tool` — everything shipped, and everything making a D-class claim | Recorded build identity, replay inputs, and release-policy stability |
| **Assurance** | Pinned **nightly, by date**, only for a locally verified lane that requires it; recorded in the assurance manifest | Assurance invocations, which may compile runtime code but never supply the admitted release binary | Preserve exact tool identity while confining unneeded nightly exposure |

Every admitted toolchain is pinned. The assurance nightly may emit assurance evidence and findings, but it never supplies the shipped binary or a product-output determinism receipt. Its own evidence records the exact nightly identity.

## Recommendation

**PROPOSED — awaiting human ratification. Adopt Option D.**

1. **`rust-toolchain.toml` pins an exact stable version.** Required components are selected from locally admitted tool evidence; `rustfmt`, `clippy`, and `rust-src` are candidates, not preverified availability claims. **This brief deliberately does not name the version number.** G2 cannot verify which stable release is current on 2026-07-14 without a fetch, and inventing a plausible-looking version number would violate the honesty rule. The human fills and records the exact pin before C1 source work. `[UNVERIFIED — version and components remain human inputs.]`
2. **Edition 2024** (§30.1, already canon).
3. **`Cargo.lock` committed** (§30.1, already canon).
4. **A separate, date-pinned nightly only where a required lane is locally shown to need it**, recorded in the assurance manifest alongside the lane results. If every selected lane works under the stable pin, no nightly is admitted merely because this brief lists one.
5. **Workspace lints deny unsafe** (§30.1/§11.7); unsafe capsules follow §11.7's protocol and the machine-checked capsule registry.
6. **The toolchain version is part of the determinism contract, and a bump is a versioned event.** This is the substantive addition and it is easy to overlook:

> §11.9 defines **D1 Serialized** as "byte-identical under a declared mode **and pinned dependencies**," and **D2 Same-target pixels** as requiring a "**deterministic build identity**." The compiler is a dependency and part of the build identity. A toolchain bump changes that declared input; whether output changes is unknown until the relevant lanes rerun. **A toolchain bump can invalidate an unretested determinism-class D1 or D2 claim.**

Therefore: the toolchain identity is recorded in every determinism-bearing receipt; a toolchain bump triggers a re-run of the determinism lanes (D1 byte-identity, D2 pixel-identity, reproducible-build comparison) before the bump lands; and a changed D-class output is routed under the governing review protocol rather than silently accepted. Toolchain bumps are never silent.

7. **MSRV stays deferred**, per Rev 7 §35 ("deferred until the dependency set stabilizes"). Registered in `DEFERRED_REGISTER.md` with owner cycle C1-close and a stated guard, because it is *not* among the Work Order's five named deferrals and would otherwise fall between the two lists.

## Rationale

The one-line canon row ("pinned stable or dated nightly only if essential") permits a conditional split. The release path uses the exact stable pin proposed here; an assurance nightly is admitted only after a selected lane proves it necessary. §30.1's package-role taxonomy helps record why a tool exists, but the controlling boundary is which invocation produced the release artifact or assurance evidence.

The determinism coupling (item 6) is easy to lose in implementation because a toolchain bump looks like maintenance. It is instead a change to an input of every D1 and D2 receipt the project has issued.

## Reversibility and migration path

**Technically high. Evidentially, one-way in a specific and limited sense.**

Re-pinning to a different stable version, or bumping the nightly date, is a config change. Nothing is architecturally locked.

The asymmetry is in the receipts, not the code:

- Determinism receipts issued **before** a pin exists cannot be replayed, because the build identity they depended on was never recorded. Those receipts are not retroactively repairable — you cannot go back and learn which compiler produced them.
- Determinism receipts issued **after** a pin, and superseded by a bump, remain replayable *if* the old toolchain is still obtainable. This is a real constraint on toolchain retention: the project must be able to reconstruct the exact toolchain for any receipt it still stands behind.

The configuration is straightforward to change, but delaying the pin leaves intervening receipts without a reproducible compiler identity. Exact migration and retention costs remain `[UNVERIFIED]` until the toolchain policy is exercised.

## Dependencies

- **Consumes:** nothing. Ratifiable independently.
- **Consumed by:** every D-class claim (§11.9); the reproducible-build comparison lane (G6.1); the C1 fuzz gate and the zero-reachable-panics criterion; the C4 release-engineering slice (Charter §5/C4).
- **Interacts with:** D5's dependency-license allowlist (the same G6.1 lane audits both); the MSRV deferral.
- **Blocks:** nothing outright, but any determinism claim made before the pin is unreplayable, so it effectively blocks the first receipt.

## Evidence still needed before ratification

1. **Confirmation of which selected fuzz/Miri/sanitizer lanes require nightly** with the locally admitted tool versions. `[UNVERIFIED]` — check at C1 rather than assume. Admit no nightly for a lane that does not require it.
2. **The current stable version number**, to be filled at C1 start. Deliberately not guessed here.
3. **A toolchain-retention policy** — how the project reconstructs an old toolchain to replay an old receipt. This falls out of the reversibility analysis and does not exist yet.
4. **A determinism-lane baseline** so that the first toolchain bump has something to compare against. Without a baseline, "the bump changed nothing" is an assertion.

## Blast radius if wrong

| Failure | Consequence | Severity |
|---|---|---|
| Unpinned or floating toolchain | D0/D1/D2 claims are unreplayable; the reproducible-build lane cannot pass; the C4 release-engineering gate fails; Q3's provenance column weakens because receipts cannot be reproduced. | **High, and it silently degrades evidence** rather than breaking the build — which is what makes it dangerous. |
| Nightly produces the shipped release without a ratified need | The release build uses a broader compiler channel than the proposed policy permits; replay and support expectations may diverge. Adoption effects are `[UNVERIFIED]`. | High and visible in the build identity. |
| A required assurance lane is proven nightly-only but no pinned nightly is available | That lane cannot emit its required result; the affected C1 gate is unavailable rather than silently passed. | High and visible. |
| Toolchain bumped without re-running determinism lanes | A D1 or D2 claim silently becomes false. Receipts assert byte- or pixel-identity that no longer holds. | **High and silent.** The failure mode item 6 exists to prevent. |
| Pin set late | Receipts issued before the pin are unreplayable, permanently. | Moderate, unrecoverable, and entirely avoidable by pinning on day one. |

## Human ratification

This brief proposes; it does not decide (Rev 7 §29.9).

- [ ] **Ratify Option D** — pinned stable for release artifacts + date-pinned nightly only for locally verified assurance needs, with the toolchain-as-determinism-input law (recommended)
- [ ] **Ratify** a single-toolchain variant (recording the local tool evidence and any affected Charter gate)
- [ ] **Amend** (record the variant and rationale)
- [ ] **Confirm** that MSRV remains deferred to C1-close per Rev 7 §35

Ratifier: ______________________ Date: ____________ Stable version pinned: ____________
