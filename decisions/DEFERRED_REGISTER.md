---
generated-by: Claude G2 owner (claude-opus-4-8, effort xhigh)
date: 2026-07-14
inputs:
  - CYCLE_0_WORK_ORDER.md §4 (defer list), §8
  - MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md §3.2, §7 (Bets 25, 16), §15.9, §16.1, §20.12, §24.15, §26.2–26.3, §30.1, §34.5.1, §35
  - MONKEYBEE_CAMPAIGN_CHARTER_v1.md §4 (cycle map), §5
status: PROPOSED
evidence-status: provisional-pending-substrate
ratification: PROPOSED — awaiting human ratification
---

# Deferred Decision Register

The five decisions the Work Order §4 defers, each with an owner cycle, a trigger, the evidence required, and the harm of resolving early. Plus a **guard** for each — see immediately below, because the guard is the part that makes a deferral safe.

## Why every deferral carries a guard

A deferred decision does not stay open by itself. It stays open only if nothing built in the meantime quietly assumes an answer. The realistic failure is not that someone decides early and writes it down; it is that C1 code accretes around an unstated assumption, and by C6 the "open" decision has been made by default, by accident, and by no one — with the cost of reversing it now paid in rewrites.

So each entry below names what may **not** be assumed while the decision is open. The guards are the enforceable part of the deferral, and they are proposed as reviewable conditions, not aspirations. Rev 7's §34.9 archaeology-first law is the backstop: each delta plan is written against repository reality, so a violated guard should surface at the next cycle boundary rather than at C7.

---

## DEF-1 — Raster backend and GPU path

- **Owner cycle:** C6 (the performance-hardening slice).
- **Current disposition (Rev 7 §35 decision 7, §34.5.1 row 7):** open; **default outside all declared envelopes.**
- **Trigger:** a bounded CPU-equivalence probe with stable certificate semantics, run inside the C6 perf slice.
- **Evidence needed:** cross-target determinism results; fixed-point and blend feasibility on the GPU path; independence of the equivalence-certificate checker; demonstrated performance value large enough to justify the assurance cost.
- **Why premature resolution is harmful:** admitting a GPU lane before CPU-equivalence certificates exist would make a nondeterministic path a hidden prerequisite for ordinary rendering. That directly attacks D2 (same-target pixel determinism, §11.9), which is a *declared class* other claims depend on. Canon is explicit that CPU-equivalence "cannot become a hidden prerequisite for common rendering."
- **Guard — what may not be assumed before C6:** no rendering API, trait, or report schema may be shaped around the existence of a GPU path. No public type may carry a GPU-specific parameter. The CPU raster path is the reference path, and Bet 25 remains a research bet outside every envelope until its probe passes.

---

## DEF-2 — PDF/A-1 versus the 1.7/2.0 writer scope (the S4 conflict)

- **Owner cycle:** C6 (validation profiles; Track A).
- **Current disposition (Rev 7 §35 decision 8, §34.5.1 row 8):** open — scope parity to PDF/A-2+ and PDF/UA-1, **or** widen §3.2 with a PDF/A-1-sufficient PDF 1.4 writer profile.
- **Trigger:** writer maturity plus profile-validation evidence, at the C6 boundary.
- **Evidence needed:** product demand for PDF/A-1 specifically; standards/profile validation with an independent validator; writer complexity cost of a PDF 1.4 profile; interoperability evidence.
- **Why premature resolution is harmful:** the conflict is between S4's parity target and the declared writer-version envelope. Canon's own rationale is worth quoting because it is the whole point: "**matching a competitor is not sufficient reason to widen product scope**" (§34.5.1 row 8). Resolving early — in the direction of widening — would let a supremacy-lane target drive product scope, which inverts the intended dependency and is precisely the distortion §24.15's precommitment discipline exists to prevent.
- **Guard — what may not be assumed before C6:** no C1–C5 work may assume a PDF 1.4 writer profile exists or will exist. The writer's target-version/profile contract (§22.3) stays parameterized rather than specialized. No claim, roadmap line, or release-envelope table may list PDF/A-1 as in-scope.

---

## DEF-3 — C-ABI freeze point

- **Owner cycle:** post-R4 for the freeze; **preview at C5** (Workflow M), per Charter §5/C5 and Rev 7 §35's C-ABI row.
- **Current disposition:** open. "Preview ABI may ship earlier; first compatibility commitment only through the explicit public-compatibility freeze after the advanced capability envelope stabilizes."
- **Trigger:** the public-compatibility freeze, once the advanced envelope (R4) has stabilized.
- **Evidence needed:** API/ABI review; a migration rehearsal; evidence that the semantic core has stopped moving.
- **Why premature resolution is harmful:** freezing an ABI before the semantic core stabilizes locks in a boundary drawn around an immature model. Every subsequent kernel or semantic change then pays compatibility rent forever, and the kernel-touch protocol (§34.9 item 2) makes that cost explicit rather than absorbing it — meaning an early freeze converts ordinary evolution into a version-bump-plus-migration-plus-claim-lapse event, repeatedly.
- **Guard — what may not be assumed before the freeze:** the C5 preview ABI is explicitly **not** a compatibility commitment and must be documented as such at its surface, not only in a plan. No public Rust type may be shaped for FFI convenience ahead of the freeze — §25.4's C ABI is an adapter over the core, and the core does not bend to it. No external consumer may be told the preview is stable.

---

## DEF-4 — Base-font fallback pack and its licensing

- **Owner cycle:** C3 (the text and font stack).
- **Current disposition (Rev 7 §20.12, §35):** open. "**No silent default; resolver profile required.**"
- **Trigger:** the C3 font stack landing and needing a substitution path.
- **Evidence needed:** font licensing terms for any candidate pack (redistribution rights, embedding rights, modification rights); a metric study of substitution fidelity.
- **Why premature resolution is harmful:** two distinct harms. Legally, a fallback pack is redistributed *with* the product, so its licensing binds the whole distribution — an early, casual choice can encumber the G1 wedge. Epistemically, a silent fallback changes what text extraction and rendering *mean*: substituted glyphs with substituted metrics produce output that looks authoritative and is not. §20.12's "no silent default" is a claim-integrity rule before it is a licensing one.
- **Guard — what may not be assumed before C3:** no font resolution path may silently substitute. Absent an admitted resolver profile, the correct behaviour is an explicit substitution-or-refusal receipt under the page-local refusal law (Charter §5/C2 already requires exactly this for C2's text handling). No fallback font may be vendored into the repository before its license is reviewed.

---

## DEF-5 — S6 performance-per-fidelity metric

- **Owner cycle:** C7 protocol finalization — and the metric must be **committed before C7 begins**, not defined during it.
- **Current disposition (Rev 7 §35 decision 9, §34.5.1 row 9):** open; current §26.3 competitive posture retained. "Parity alone is not a supremacy claim."
- **Trigger:** the C7 measurement-design step, which precedes measurement.
- **Evidence needed:** profile-aligned benchmark evidence; the overhead of determinism and evidence machinery, quantified; proof that the safety contracts are not bypassed to obtain the number.
- **Why premature resolution is harmful, and this is the sharpest one in the register:** a performance metric defined *after* seeing performance data is a post-hoc metric, and §33.4 forbids precisely that — "the evaluation commitment predates measurement," and "post hoc discoveries are hypotheses until replicated under a new committed protocol." Defining S6 early is equally harmful for the opposite reason: canon warns that "superiority may distort safety/evidence architecture," meaning a metric adopted before the architecture is stable will bend the architecture toward the metric. The decision must land in a narrow window: after the architecture stabilizes, before any measurement.
- **Guard — what may not be assumed before C7:** no optimization may bypass a safety contract, a budget, or an evidence obligation in pursuit of an unspecified future metric. No performance claim of any kind is published before the metric is committed. Benchmark *tracking* begins at C2 (Charter §4) and is for regression detection — it is **not** a supremacy measurement and must never be reported as one.

---

## Additional deferrals and gaps identified by G2

These are **not** in the Work Order's five. They are recorded because they fall between the resolve-now list and the defer list, and an unlisted decision is the kind that gets made by accident. G2 does not expand its own mandate: each is flagged for the human to route, with a recommended disposition and no action taken.

### GAP-1 — Minimum supported Rust version (MSRV)

- **Status:** deferred by Rev 7 §35 ("deferred until the dependency set stabilizes"), but **absent from both** of the Work Order §4 lists.
- **Recommended disposition:** deferred, owner cycle **C1-close** (when the C1 dependency set is known). See `D7_RUST_TOOLCHAIN_PIN.md` recommendation item 7.
- **Trigger:** dependency-set stabilization at the C1 close gate.
- **Guard:** no MSRV is advertised until it is declared. Once the public API stability is claimed (post-R4, §25.7), the declared MSRV becomes a semver-relevant contract and cannot be raised casually.

### GAP-2 — Runtime dependency allowlist and cryptographic-crate selection

- **Status:** Rev 7 §35 carries rows for "Runtime dependency allowlist" and "Cryptographic crates"; §15.9 sets the codec-dependency admissibility conditions. **Neither the Work Order's resolve-now list nor its defer list names them.**
- **Why this matters now, and why it is a genuine gap rather than a pedantic one:** the Work Order's resolve-now criterion is "they gate Cycle 1 code." These gate C1 code. C1 lands the lossless filter set (Flate + predictors, LZW, and the rest) and the standard-security-handler read-decryption stack (RC4, AESV2, AESV3, MD5 and SHA-2 key derivation, per Charter §5/C1). Every one of those is a dependency decision governed by §15.9's admissibility conditions and §16.1's "audited, permissively licensed, pure-Rust" rule. G3's C1 delta plan cannot specify its capability surface without knowing the dependency policy it is specifying against.
- **Recommended disposition — for the human to route, not for G2 to assume:** ratify the **policy** now (it is already largely written in §15.9 and §16.1: memory-safe Rust in the default build; permissive license per D5's allowlist rider; controllable input limits; narrow semantic boundary; pinned version; independent fuzzing story; MonkeyBee retains PDF-specific validation and provenance), and defer the **specific crate selections** to C1 archaeology, where they can be reviewed against a real dependency graph rather than a remembered one. That split resolves the gate without inviting anyone to name crates from memory — which would also risk the clean-room boundary, since a "which crate" answer sourced from recall is a claim about the ecosystem that this phase cannot verify.
- **Guard, if the human accepts the split:** no crate is named in a plan document as a committed choice before its §15.9 review exists. A crate named as an *illustration* is marked as such. No cryptographic primitive is implemented in-house (§16.1: "MonkeyBee does not invent modern cryptographic primitives").

---

## Standing law for this register

1. **A deferral is not a silent default.** If C1–C5 work makes a deferred decision moot by assuming an answer, that is a Grade-A finding at the next cycle-close drift audit, not a fait accompli.
2. **Every deferral has an owner cycle and a trigger.** An item with neither is not deferred; it is forgotten.
3. **Deferred items are re-read at each cycle boundary** as part of the §34.9 archaeology step, and their guards are checked against repository reality.
4. **Resolving a deferred item early is permitted** — but only through the same ratification path as a resolve-now item: a brief with options, recommendation, rationale, reversibility, dependencies, and blast radius, ratified by a human. Not by an implementer's convenience.

## Human ratification

- [ ] **Ratify** the five deferrals with their owner cycles, triggers, and guards as stated
- [ ] **Route GAP-1** (MSRV) — [ ] accept as deferred to C1-close  ·  [ ] other
- [ ] **Route GAP-2** (dependency allowlist / crypto crates) — [ ] ratify the policy now and defer crate selection to C1  ·  [ ] add to the resolve-now set  ·  [ ] other
- [ ] **Amend** (record the variant and rationale)

Ratifier: ______________________ Date: ____________
