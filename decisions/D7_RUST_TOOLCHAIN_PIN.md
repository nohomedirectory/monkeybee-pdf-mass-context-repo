---
generated-by: Claude G2 owner (claude-opus-4-8, effort xhigh)
date: 2026-07-14
inputs:
  - CYCLE_0_WORK_ORDER.md §4 resolve-now item 7
  - MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md §11.6, §11.7, §11.9, §25.7, §26.9, §26.10, §27 (G5, G6.1), §30.1, §35
  - MONKEYBEE_CAMPAIGN_CHARTER_v1.md §5 (C1 gate: zero reachable panics under the fuzz corpus; C4 release engineering)
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

## The wrinkle: C1's own gate requires nightly

Charter §5/C1 and the Work Order both make **coverage-guided fuzzing operate from hour one**, with a C1 close gate of "**zero reachable panics under the fuzz corpus**." Rev 7's G5 lane requires fuzzing, and G6.1 requires "Miri or equivalent interpreter checks" and "sanitizers."

The standard Rust tooling for those lanes — `cargo-fuzz`/libFuzzer, Miri, and the sanitizers — requires a **nightly** toolchain `[UNVERIFIED as of 2026-07; this has been true historically and should be confirmed against current tooling at C1 rather than assumed]`. Meanwhile, §26.9/§26.10's determinism classes and G6.1's "reproducible-build comparison" require a **pinned, stable, reproducible** build for anything the project ships or makes determinism claims about.

A single-toolchain answer cannot satisfy both. Reading §35's "pinned stable **or** dated nightly" as an exclusive choice would force either giving up reproducible release builds or giving up the C1 fuzz gate — and both are non-negotiable. The resolution is that these are **two different toolchains for two different package roles**, which §30.1's role taxonomy already gives us the vocabulary to express.

## Options

### Option A — Pinned stable for everything

- **Against:** Cannot run the C1 fuzz gate, Miri, or the sanitizers. Fails Charter §5/C1 on its face. Rejected.

### Option B — Nightly for everything

- **For:** All tooling available.
- **Against:** Destroys reproducible builds and semver stability; makes the shipped wedge depend on an unstable compiler; §35 explicitly permits nightly "only if essential." Rejected.

### Option C — Track latest stable, unpinned

- **Against:** Build identity varies silently. §11.9's D0, D1, and D2 classes *all* condition on pinned dependencies and "deterministic build identity" — an unpinned compiler means a receipt cannot be replayed, and the reproducible-build comparison lane cannot pass. This is not a style preference; it directly voids determinism claims. Rejected.

### Option D — Two pinned toolchains, split by package role — **recommended**

| | Toolchain | Applies to | Why |
|---|---|---|---|
| **Release/build** | Pinned **stable**, exact version, via `rust-toolchain.toml`; edition 2024 (§30.1); `Cargo.lock` committed | `runtime`, `adapter`, `release-tool` — everything shipped, and everything making a D-class claim | Reproducibility, determinism receipts, semver stability, enterprise adoption of the G1 wedge |
| **Assurance** | Pinned **nightly, by date**, recorded in the assurance manifest | `lab-tool` — the fuzz, Miri, and sanitizer lanes only | These lanes need nightly features; they never produce a shipped artifact or a determinism claim |

Both are *pinned*. Neither floats. The nightly is confined to lanes whose output is a *finding*, never a binary or a receipt.

## Recommendation

**PROPOSED — awaiting human ratification. Adopt Option D.**

1. **`rust-toolchain.toml` pins an exact stable version**, with `rustfmt`, `clippy`, and `rust-src` components. **This brief deliberately does not name the version number.** G2 cannot verify which stable release is current on 2026-07-14 without a fetch that would not improve the decision, and inventing a plausible-looking version number is exactly the "no invented versions" failure the honesty rules forbid. The pin is set to the then-current stable at C1 start, by a human or by CI, and recorded. `[UNVERIFIED — version to be filled at C1 start.]`
2. **Edition 2024** (§30.1, already canon).
3. **`Cargo.lock` committed** (§30.1, already canon).
4. **A separate, date-pinned nightly** for the fuzz / Miri / sanitizer lanes, recorded in the assurance manifest alongside the lane results. Nightly output is findings only — never a shipped artifact, never a determinism receipt.
5. **Workspace lints deny unsafe** (§30.1/§11.7); unsafe capsules follow §11.7's protocol and the machine-checked capsule registry.
6. **The toolchain version is part of the determinism contract, and a bump is a versioned event.** This is the substantive addition and it is easy to overlook:

> §11.9 defines **D1 Serialized** as "byte-identical under a declared mode **and pinned dependencies**," and **D2 Same-target pixels** as requiring a "**deterministic build identity**." The compiler is a dependency and it is part of the build identity. A toolchain bump can change codegen, and a codegen change can change floating-point evaluation, iteration order in optimized code, and therefore raster output. **A toolchain bump can silently break a D1 or D2 claim.**

Therefore: the toolchain identity is recorded in every determinism-bearing receipt; a toolchain bump triggers a re-run of the determinism lanes (D1 byte-identity, D2 pixel-identity, reproducible-build comparison) before the bump lands; and a bump that changes any D-class output is a finding to be dispositioned, not a diff to be accepted. Toolchain bumps are never silent, and never "just a version bump."

7. **MSRV stays deferred**, per Rev 7 §35 ("deferred until the dependency set stabilizes"). Registered in `DEFERRED_REGISTER.md` with owner cycle C1-close and a stated guard, because it is *not* among the Work Order's five named deferrals and would otherwise fall between the two lists.

## Rationale

The one-line canon row ("pinned stable or dated nightly only if essential") reads as a choice and is actually a role split. Once you notice that the C1 fuzz gate *requires* nightly and the C1 determinism claims *require* pinned stable, the exclusive reading is impossible, and the inclusive reading is not a compromise — it is the correct decomposition, and §30.1's package-role taxonomy already exists to express it. Nightly is admitted precisely where it cannot contaminate a claim: in lanes that emit findings rather than artifacts.

The determinism coupling (item 6) is the part most likely to be lost in implementation, because a toolchain bump looks like maintenance. It is not: it is a change to an input of every D1 and D2 receipt the project has issued.

## Reversibility and migration path

**Technically high. Evidentially, one-way in a specific and limited sense.**

Re-pinning to a different stable version, or bumping the nightly date, is a config change. Nothing is architecturally locked.

The asymmetry is in the receipts, not the code:

- Determinism receipts issued **before** a pin exists cannot be replayed, because the build identity they depended on was never recorded. Those receipts are not retroactively repairable — you cannot go back and learn which compiler produced them.
- Determinism receipts issued **after** a pin, and superseded by a bump, remain replayable *if* the old toolchain is still obtainable. This is a real constraint on toolchain retention: the project must be able to reconstruct the exact toolchain for any receipt it still stands behind.

So the decision is cheap to change and expensive to have delayed. Pinning early costs nothing; pinning late costs every receipt issued in the interim.

## Dependencies

- **Consumes:** nothing. Ratifiable independently.
- **Consumed by:** every D-class claim (§11.9); the reproducible-build comparison lane (G6.1); the C1 fuzz gate and the zero-reachable-panics criterion; the C4 release-engineering slice (Charter §5/C4).
- **Interacts with:** D5's dependency-license allowlist (the same G6.1 lane audits both); the MSRV deferral.
- **Blocks:** nothing outright, but any determinism claim made before the pin is unreplayable, so it effectively blocks the first receipt.

## Evidence still needed before ratification

1. **Confirmation that the fuzz/Miri/sanitizer lanes still require nightly** with current tooling. `[UNVERIFIED]` — historically true; check at C1 rather than assume. If some lane has stabilized, the nightly surface shrinks, which is strictly good.
2. **The current stable version number**, to be filled at C1 start. Deliberately not guessed here.
3. **A toolchain-retention policy** — how the project reconstructs an old toolchain to replay an old receipt. This falls out of the reversibility analysis and does not exist yet.
4. **A determinism-lane baseline** so that the first toolchain bump has something to compare against. Without a baseline, "the bump changed nothing" is an assertion.

## Blast radius if wrong

| Failure | Consequence | Severity |
|---|---|---|
| Unpinned or floating toolchain | D0/D1/D2 claims are unreplayable; the reproducible-build lane cannot pass; the C4 release-engineering gate fails; Q3's provenance column weakens because receipts cannot be reproduced. | **High, and it silently degrades evidence** rather than breaking the build — which is what makes it dangerous. |
| Nightly in the shipped runtime | The wedge depends on an unstable compiler; enterprise adoption stalls; reproducibility is fragile. | High, and loud. |
| Stable-only, no nightly lane | The C1 fuzz gate cannot run; "zero reachable panics under the fuzz corpus" is unverifiable; a Charter §5/C1 gate fails. | High, and loud. |
| Toolchain bumped without re-running determinism lanes | A D1 or D2 claim silently becomes false. Receipts assert byte- or pixel-identity that no longer holds. | **High and silent.** The failure mode item 6 exists to prevent. |
| Pin set late | Receipts issued before the pin are unreplayable, permanently. | Moderate, unrecoverable, and entirely avoidable by pinning on day one. |

## Human ratification

This brief proposes; it does not decide (Rev 7 §29.9).

- [ ] **Ratify Option D** — pinned stable (release/runtime) + date-pinned nightly (assurance lanes only), with the toolchain-as-determinism-input law (recommended)
- [ ] **Ratify** a single-toolchain variant (recording which Charter gate is thereby given up)
- [ ] **Amend** (record the variant and rationale)
- [ ] **Confirm** that MSRV remains deferred to C1-close per Rev 7 §35

Ratifier: ______________________ Date: ____________ Stable version pinned: ____________
