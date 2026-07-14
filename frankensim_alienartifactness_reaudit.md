# FrankenSim’s “Alien-Artifact-Ness,” Re-Audited

## A fresh-eyes, adversarial review of `Dicklesworthstone/frankensim`

**Assessment date:** 2026-07-14  
**Repository snapshot:** [`main@e7ebbab`](https://github.com/Dicklesworthstone/frankensim/commit/e7ebbab3fffff065021208979bf92efd990426e6)  
**Supersedes:** the earlier `frankensim_alienartifactness.md` assessment  
**Primary standard:** the supplied *Post-Agent Alien Software Artifact* definition  
**Contrast standard:** the supplied *Pre–Claude Code Alien Software Artifact* definition  
**Inspection mode:** static repository, source, contract, documentation, and Git-history review  
**Not performed:** a clean bootstrap of the seven-repository constellation, compilation of the full workspace, execution of DSR, real-x86 runtime verification, reproduction of performance results, or independent scientific validation

---

## Executive judgment

The previous assessment was **too generous**.

FrankenSim remains an extraordinary repository-scale engineering effort. It contains a large amount of real Rust code, unusually explicit architecture, sophisticated numerical and provenance concepts, numerous integration surfaces, and a striking attempt to turn agent-generated work into cumulative institutional structure rather than a pile of patches.

However, under the canonical post-agent definition, the correct present conclusion is:

> **FrankenSim is a high-substance and architecturally unusual post-agent artifact candidate, but its alienness is not established. On the public evidence currently available, the strict judgment is underdetermined—not “strongly maker-relative,” not “plausibly public-frontier,” and certainly not global-frontier.**

The reasons are not merely missing paperwork. A deeper re-audit found confirmed defects and contradictions in precisely the mechanisms that the repository presents as safeguards against self-consistent overclaiming:

1. **A public “certified” neural Lipschitz mechanism is mathematically unsound for admissible inputs.** The fixed-start power iteration in `fs-rep-neural` can return a spectral norm of zero for a nonzero matrix. The resulting network can publish a zero “certified” Lipschitz constant and an infinite “provably safe” sphere-tracing radius for a field that actually changes sign.
2. **The contract checker checks headings, not contract truth.** It cannot detect the neural defect, stale API claims, dependency contradictions, or code/contract semantic drift.
3. **`fs-sos` demonstrates actual contract drift.** Its source explicitly says a former tolerance-based API forged global certificates and was replaced, while its current `CONTRACT.md` still describes the old API and “zero false certificates.” The contract also says “no dependencies” while the manifest has two runtime dependencies.
4. **Repository-wide truth artifacts disagree.** The license metadata conflicts with the actual license, reproducibility instructions bypass the pinned toolchain, a cross-ISA guide describes the wrong sibling constellation, the CI status table describes already-landed crates as future work, the README says neural representations do not exist while `fs-rep-neural` does, and `AGENTS.md` still calls the project “plan-first.”
5. **No independently inspectable green proof accompanies the current head.** The project intentionally uses DSR rather than GitHub Actions, but no head-specific, externally checkable DSR proof bundle was found in the repository, and GitHub exposes no workflow run or combined status for the inspected commit.
6. **The strict causal comparison is absent.** There is no authenticated production ledger, matched equal-resource baseline, ablation, attempt distribution, held-out foundry trial, or independent clean-room reproduction.
7. **Empirical maturity is necessarily minimal.** The repository is roughly eight days old, has no packaged product, no stable public API, no release, no demonstrated user population, and no long operational history.

The strongest surviving positive claim is narrower:

> **FrankenSim exhibits exceptional architectural ambition and substantial integration work at remarkable speed. Its most unusual property is not raw size but the attempt to impose one cross-cutting protocol of units, identity, cancellation, evidence, provenance, budgets, and refusal across a very broad scientific-computing workspace.**

That is impressive. It is not yet sufficient for strict alien-artifact status.

### Revised labels

| Claim | Revised assessment | Confidence |
|---|---|---:|
| Substantive software artifact | **Yes, at source-workspace level** | High |
| Packaged end-user simulator | **No** | High |
| Scientifically validated simulation platform | **Not established** | High |
| Strong maker-relative alien artifact | **Not established; provenance is insufficient** | High |
| Maker-relative alien candidate | **Yes** | Moderate |
| Public-frontier alien artifact | **Unsupported / indeterminate** | High |
| Global-frontier alien artifact | **Unsupported** | Very high |
| Alien foundry | **Not demonstrated** | High |
| Proto-foundry / foundry research program | **Yes** | Moderate-high |
| Alien lineage | **Too early; early semantic drift is already visible** | High |

---

## 1. What the governing definition actually requires

The supplied post-agent definition is deliberately stricter than “a lot of impressive software made quickly.” It requires a functioning computational object whose integrated consequences are a **robust extreme outlier** relative to:

- a specified date;
- an explicit reference class;
- an authenticated, bounded production account;
- the available models and harnesses;
- compute, tools, search, retries, and parallelism;
- human expertise and attention;
- inherited code, data, and services; and
- the operational substrate that continues to make the object work.

Alienness is the **explanatory surplus left after all of that leverage is credited**.

The supplied pre-agent definition used a different impossible conjunction: civilization-scale scope with single-mind coherence, maturity suggesting centuries, and cleanliness suggesting a system born whole. That is useful as an aesthetic contrast, but it cannot be applied directly after repository-scale coding agents become ordinary production infrastructure.

For FrankenSim, therefore, none of the following establishes alienness by itself:

- 127 crate directories;
- 263 test files;
- approximately 1,400 commits after inception;
- broad specialist vocabulary;
- rapid development;
- agent co-author trailers;
- long contracts and documentation;
- many named algorithms;
- or even internally green tests.

Those facts may establish unusual productivity. The strict question is whether the **working, grounded, durable integration** is a robust outlier after the complete human-agent production ecology is admitted.

### 1.1 Evidence grades used in this report

To avoid repeating the repository’s own mistake of treating every attractive claim as equally grounded, this review uses four evidence grades:

| Grade | Meaning |
|---|---|
| **A — source-confirmed** | Directly visible in code, manifest, lockfile, or mutually contradictory repository artifacts; no runtime execution is required to establish it |
| **B — repository-attested** | Claimed by contracts, tests, commit messages, or documentation, but not independently executed in this review |
| **C — analytical inference** | Reasonable consequence of A/B evidence, clearly identified as inference |
| **D — unknown** | Requires execution, external data, provenance, or expertise not available in this review |

The most serious findings below are Grade A.

### 1.2 Artifact boundary

The practical artifact is not just the `frankensim` Git tree. Its minimum operational closure includes:

- the root workspace;
- the nested `fs-wasm` workspace;
- seven pinned sibling repositories in `constellation.lock`;
- their full transitive dependency closure;
- the pinned Rust nightly;
- DSR configuration outside this repository;
- real x86 hosts for runtime cross-ISA claims;
- performance-authority policy and retained receipts;
- FrankenSQLite ledger files and promoted baselines; and
- human procedures for admission, promotion, release, and re-freezing.

Construction-time agents belong to provenance. External systems needed to reproduce and sustain claimed behavior belong to operational closure.

---

## 2. Corrections to the previous report

The earlier report did include caveats, but several judgments were still too favorable. The following corrections are substantive.

### 2.1 “Strong maker-relative candidate” was too strong

Maker-relative alienness still requires an authenticated account of the maker’s resources, attempts, costs, models, parallelism, inherited work, and selection process. The public repository does not provide that account.

A better phrase is:

> **Maker-relative alien candidate under an incomplete production account.**

The difference matters. “Strong candidate” implied that most of the causal comparison was already available. It is not.

### 2.2 “Plausible public-frontier candidate” was not justified

No matched public baseline was presented. There is no equal-budget comparison against:

- direct use of the same models;
- a strong general agent harness;
- the same process without contracts;
- the same process without Beads/identity memory;
- the same process without the evidence layer; or
- another expert operator with equivalent compute and model access.

Without that comparison, “public-frontier” is not a supported classification. The correct status is **indeterminate**.

### 2.3 Commit velocity was over-weighted

The inception-to-head history is remarkable, but commit count is a weak unit of organized consequence. Fine-grained agent commits, bookkeeping commits, generated documentation, issue-ledger exports, and iterative repair can inflate the count without proportionally increasing validated capability.

Velocity remains contextual evidence. It should not carry the alienness argument.

### 2.4 Contract presence was mistaken for contract verification

The old report said contracts were “normative and machine-checked.” That was imprecise.

What `xtask check-contracts` actually checks is:

- whether `CONTRACT.md` exists; and
- whether ten required section headings occur as substrings.

It does **not** check:

- that named public APIs exist;
- that the contract matches the current source;
- that dependencies match the contract;
- that a conformance test file exists;
- that the stated tests ran;
- that mathematical guarantees are sound;
- that no-claim boundaries cover every public path; or
- that source changes update the contract.

The later findings in `fs-sos` and `fs-rep-neural` demonstrate that this distinction is load-bearing.

### 2.5 The old report underweighted correlated evaluation error

The repository frequently uses one human-agent ecology to produce:

- the architecture;
- the implementation;
- the tests;
- the contracts;
- the README;
- the issue status;
- the golden rationale; and
- the review narrative.

That can be disciplined and valuable. It is still a correlated evidence loop. The neural certificate defect survived source, contract, tests, an end-to-end campaign, README discussion, and claim-state policy because all of those artifacts shared the same mistaken premise.

This is exactly the failure mode the post-agent definition warns about.

### 2.6 Operational incompleteness was understated

The previous report called FrankenSim a promising proto-foundry. That remains a fair research-program description, but the operational gap is wider than the wording suggested:

- no packaged simulator;
- no stable API;
- no release;
- no public production validation corpus;
- no head-specific public proof bundle;
- external DSR configuration;
- external authority files for positive performance gates;
- local sibling repositories;
- ignored mid/full flagship lanes; and
- no demonstrated external user workflow.

### 2.7 The previous review did not adversarially test “certificate” implementations

This was the largest methodological omission. A repository centered on “certificates over vibes” must be reviewed by trying to construct false certificates, not only by reading the intended invariants.

Doing that immediately exposed a deterministic counterexample in `fs-rep-neural`.

### 2.8 The previous review missed truth-source drift

It did not identify:

- the root license metadata conflict;
- floating-nightly instructions that bypass the pinned toolchain;
- the stale sibling count in the x86 playbook;
- stale Decalogue gate statuses;
- stale README claims about neural representations;
- stale “plan-first” language in `AGENTS.md`;
- the stale changelog endpoint; or
- orphaned, deliberately uncompilable scaffold files retained under the no-deletion rule.

These are not cosmetic in a project whose central claim is unusually low semantic decay.

---

## 3. What is real and substantial today

A strict re-audit should not collapse into the opposite error of dismissing the entire repository because defects exist.

### 3.1 It is a real source workspace, not merely a plan

The root README accurately states that FrankenSim is a working Rust source workspace and library substrate, not a packaged application. The workspace manifest lists 126 native `fs-*` members, while `fs-wasm` is a nested standalone workspace. The tree has 127 contract files and hundreds of Rust test files.

The manifest, crate source, tests, policy tooling, lockfile, and bootstrap machinery are concrete.

### 3.2 Several core mechanisms have substantial implementations

A non-exhaustive sample:

- **Representation routing:** `fs-geom::router` contains a bounded multi-objective label-correcting planner, explicit error-composition rules, deterministic tie-breaking, execution receipts, and a cost-oracle abstraction.
- **Evidence algebra:** `fs-evidence` has typed numerical, statistical, and model-form evidence, validity-domain handling, conservative color composition, model cards, falsifier pairing, and structured refusal paths.
- **Execution:** `fs-exec` defines logical stream identity, cancellation gates, fixed-shape reductions, tile pools, leases, resumable solver state, race behavior, and tuning identities.
- **Ledger:** `fs-ledger` has a large, versioned FrankenSQLite schema with content-addressed artifacts, operations, lineage, time travel, session claims, integrity checks, and bounded reads.
- **Geometric algebra:** `fs-ga` includes compile-time Clifford tables, PGA/CGA multivectors, motors, constructions, façade types, and extensive stated conformance batteries.
- **Planning:** `fs-plan` contains cost/error models, attribution ledgers, routing integration, a budget allocator, value-of-information features, and feature-gated moonshot planning.
- **Flagship composition:** e2e crates connect lower-level components into deterministic smoke-tier studies with frozen metric identities and explicit no-claim boundaries.

These are not just crate names.

### 3.3 The repository often displays unusually good scientific honesty

Positive examples include:

- commits that downgrade overclaimed theorems to conditional or no-claim language;
- explicit distinctions between integrity and external authority;
- refusal to treat signatures as authenticated without a verifier;
- distinction among Verified, Validated, and Estimated evidence;
- preservation of golden-change explanations;
- source comments documenting build-mode and ISA divergences;
- bounds on parsing, allocation, and work; and
- acknowledgement that smoke-tier campaigns are not production-scale physics validation.

That culture is a genuine strength.

### 3.4 The architectural constitution is unusually coherent

Across many crates, the same conceptual carriers recur:

- dimensions and quantity kinds;
- logical identities and content roots;
- explicit execution contexts;
- cancellation ownership;
- validity domains;
- evidence strength;
- bounded work;
- structured refusals;
- deterministic serialization;
- exact machine/build identities; and
- explicit no-claim boundaries.

This is the strongest basis for calling FrankenSim unusual.

---

## 4. Vision versus reality

This section compares the project’s stated constitutional vision with the inspected snapshot. “Partial” is not a criticism by itself; the project is very young. The purpose is to prevent plan language from being read as implemented fact.

### 4.1 The Decalogue

| Principle | Vision | Reality at `e7ebbab` | Status |
|---|---|---|---|
| **P1 — Pure memory-safe Rust, Franken-only dependencies** | No BLAS/LAPACK/C/C++/FFI; runtime dependency set limited to `std` and the Franken constellation; unsafe only in small audited capsules | Workspace crates enforce direct dependency names and deny unsafe by default. However, `check-deps` examines direct manifest edges only; `Cargo.lock` shows the sibling constellation brings a large crates.io and platform/FFI closure. `fs-wasm` directly uses `wasm-bindgen` and `getrandom`. The public phrase “zero other runtime dependencies” is therefore true only under a narrow boundary that treats constellation internals as externalized substrate. | **Partially realized; boundary overstated** |
| **P2 — Determinism as a feature** | Bit-identical results across runs, thread counts, and best-effort across ISAs | Many local deterministic mechanisms are real: fixed reductions, logical RNG keys, deterministic math, golden identities, and x86 procedures. The repository’s own CI mapping still describes the global G5 audit as deferred, and no head-specific public proof bundle was found. | **Substantial local realization; global claim unproven** |
| **P3 — Differentiable or certifiable** | Every operator exposes an adjoint or rigorous enclosure | AD, adjoints, intervals, DWR, evidence wrappers, and gradient checks exist. Numerous no-claim boundaries remain. The generic neural Lipschitz “certificate” is unsound, demonstrating that the global principle is not yet reliably enforced. | **Mixed; serious counterexample** |
| **P4 — Budgets first** | Accuracy, time, memory, and capability budgets are explicit and compose end to end | Execution leases, ledger fields, planner budgets, work caps, and bounded APIs are substantial. Not every synchronous helper or public algorithm is budget/cancellation aware, and end-to-end budget composition is not demonstrated for the entire stack. | **Substantial but incomplete** |
| **P5 — Structure preservation** | Exact sequences, variational structure, and power-conserving coupling eliminate defect classes | FEEC, incidence, Hodge machinery, coupling abstractions, and explicit caveats exist. The project correctly notes that exact incidence alone is not a no-spurious-mode theorem and that passivity requires additional obligations. A universal flagship-level proof is not present. | **Meaningful partial realization** |
| **P6 — Matrix-free and roofline-honest** | Every kernel has measurable arithmetic-intensity context and machine-specific performance evidence | Matrix-free operators, roofline code, tune rows, machine fingerprints, and authority-gated performance paths exist. Positive gates require external policy/receipt/ledger inputs and quiet reference machines. Public head-level attainment evidence is not bundled with the source snapshot. | **Infrastructure substantial; claims externally contingent** |
| **P7 — Cancellation-correct compute** | Every unit of work runs in explicit scopes, polls at bounded tile boundaries, and drains correctly | `fs-exec` is one of the strongest realized areas. Yet many small/synchronous crates explicitly have no `Cx`, and the repository’s gate table still labels executor-wide storm coverage as future/partial. System-wide bounded cancellation has not been independently demonstrated. | **Strong core, incomplete universality** |
| **P8 — One data model** | Complexes/cochains and chart representations form one shared substrate | Chart/Region and cochain abstractions are real; representation-aware conversion is a major strength. The 127-crate workspace still contains many specialized local models and adapters, and the “one canonical in-memory layout for each” vision is not established across all domains. | **Architectural direction, not complete fact** |
| **P9 — Provenance-complete** | Every artifact is content-addressed; every operation is replayable and explainable from the ledger | The ledger implementation is substantial. But project-construction provenance is not complete, DSR/performance evidence is partly external, many public examples are in-process fixtures, and no current public run bundle closes source-to-result provenance for the whole workspace. | **Strong subsystem; artifact-level closure missing** |
| **P10 — Agent-first ergonomics** | Units, seeds, budgets, versions, and capabilities are always explicit; errors teach | This principle is visible throughout the code. However, stale docs, stale contracts, license drift, toolchain drift, and the neural false certificate show that agent-readable governance does not yet maintain one reliable truth surface. | **Strong design, imperfect institutional execution** |

#### 4.1.1 Important nuance on P1

The project may intentionally define “Franken-only” as “workspace crates may directly depend only on sibling Franken projects.” That is a coherent governance rule.

It is not the same as:

> the operational artifact has no third-party runtime code, native interfaces, or crates.io dependencies.

The current `xtask` implementation checks the former. Some plan and README language can be read as the latter. The artifact-boundary analysis must use the full transitive closure.

### 4.2 The Twelve Big Bets

| Bet | Vision | Inspected reality | Status |
|---|---|---|---|
| **1. Representation router** | Certified-error Pareto routing over geometry charts | A substantial router exists with bounded labels, cost/error objectives, deterministic winner rules, execution receipts, and cost-oracle integration. Converter certificate availability is partly declared, and opaque admitted converter authority remains a no-claim. | **One of the strongest realized bets** |
| **2. Geometric algebra core** | PGA/CGA replace fragmented coordinate representations | `fs-ga` contains meaningful PGA/CGA implementation, compile-time tables, motors, constructions, façade types, tests, and explicit performance/no-claim boundaries. Broader adoption as the universal kinematics core is not yet shown. | **Substantial implementation; adoption partial** |
| **3. FEEC + CutFEM + variational/coupled physics** | Structure-preserving, mesh-optional multiphysics | FEEC, CutFEM, solids, coupling, time, and several fixtures exist. The full conjunction—production-grade multiphysics, validated accuracy, passivity across partitioned time integration, and flagship-scale use—is not established. | **Many ingredients; conjunction incomplete** |
| **4. Adjoint-native, goal-driven everything** | Every solver designed around IFT/transposed solves and DWR | Adjoint machinery and verification surfaces are extensive. Contracts retain many limits: sampled residuals, 1-D reference estimators, Estimated explanations, caller-declared objective identity, and unverified external authority. | **Substantial research infrastructure; not universal** |
| **5. Anytime-valid stochastic layer** | E-processes and conformal logic govern all stochastic decisions | E-process, race, UQ, BO, robust, and campaign pieces exist. “All stochastic estimation” is broader than the demonstrated pathways, and no independent optional-stopping audit of the whole system was performed here. | **Meaningful partial realization** |
| **6. Optimization as geometry** | Riemannian/information/shape/OT geometry unifies optimizers | Multiple optimizer crates and algorithms exist. Some earlier `fs-opt` geometry files are explicitly orphaned noncompiled scaffolds, while live implementations are distributed across `fs-ascent`, `fs-dfo`, `fs-opt`, and related crates. The grand unification remains incomplete. | **Broad implementation; architecture still settling** |
| **7. Certificates everywhere** | Rigorous proofs for geometry, numerics, stability, and optimization | Many serious certificate mechanisms exist, and some earlier false-certification paths were corrected. The neural counterexample and stale SOS contract show that “certificate” is not yet a reliably enforced semantic category. | **Mixed; strongest vision–reality fault line** |
| **8. Cancellation as numerical primitive** | Statistical decisions kill losing simulation work with deterministic replay | Cancellation, racing, e-process decisions, and kill registries exist. End-to-end examples are mostly smoke/fixture scale, and global bounded-latency/drain behavior has not been externally reproduced. | **Promising partial realization** |
| **9. Learned accelerators with guarantees** | Neural operators/DeepONet/DeepSDF/POD-DEIM at 100–10,000× speed inside certified bands | `fs-rep-neural` is a small inference-only v0; it does not train. Its generic Lipschitz certificate is unsound. Surrogate and reduced-order pieces exist, but the stated speedups and guarantee envelope are not established as a unified production path. | **Early and currently compromised** |
| **10. Design Ledger** | Content-addressed, replayable, queryable study history | `fs-ledger` is unusually extensive for the project’s age and implements many of the intended concepts. The remaining gap is adoption and public run evidence across the whole artifact, not absence of code. | **Probably the strongest realized bet** |
| **11. Sheaf-theoretic consistency** | H⁰/H¹ as the language of gluing and obstruction | `fs-geom::sheaf` implements sampled interface complexes, exact incidence, watertightness evidence, repair-related features, and falsifiers. Guarantees are scoped to the represented/sampled construction and explicit clips; this is not a general theorem for arbitrary industrial geometry. | **Substantial specialized implementation** |
| **12. Self-optimizing pipeline** | HELM co-optimizes error and time across the full workflow using learned cost models and tropical critical paths | Cost/error ledgers, a router oracle, allocator, VoI, tropical tools, and feature-gated planners exist. A continuously self-optimizing full pipeline with demonstrated end-to-end superiority is not shown. | **Components present; headline conjunction unproven** |

### 4.3 Product vision versus delivered product

| Vision-level impression | Reality |
|---|---|
| A complete simulation/design system | A broad source workspace and research substrate |
| A ready solver platform | Numerous kernels, fixtures, and smoke-tier compositions; full multiphysics suite incomplete |
| Evidence-backed scientific output | Evidence types and package machinery exist; no independently validated production corpus was inspected |
| Browser-facing flagships | WASM wiring and reduced pipelines exist; this review did not run them, and they are not equivalent to full-fidelity production campaigns |
| Mature operational system | No packaged app, stable API, release, broad users, or long incident history |
| One source of truth | Multiple stale or contradictory truth artifacts exist |

---

## 5. Confirmed defects, contradictions, and governance failures

The following are not generic concerns. They are specific findings in the inspected snapshot.

### F-01 — Unsound “certified” spectral norm and Lipschitz bound in `fs-rep-neural`

**Severity:** High for scientific assurance; localized in direct code impact  
**Evidence grade:** A — source-confirmed  
**Files:** [`crates/fs-rep-neural/src/lib.rs`](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/crates/fs-rep-neural/src/lib.rs), [`CONTRACT.md`](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/crates/fs-rep-neural/CONTRACT.md), [`tests/neural.rs`](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/crates/fs-rep-neural/tests/neural.rs)

#### Claimed behavior

The source and contract say:

- `spectral_norm` computes the largest singular value;
- each layer is normalized to the requested bound;
- the product of these values is a certified global Lipschitz constant;
- `|f(x)|/L` is a provably safe sphere-tracing radius; and
- the interval and gradient tests form a certificate battery.

#### Actual algorithm

`spectral_norm`:

1. uses one fixed initial vector, `v[i] = 1 + 0.1i`;
2. applies 200 iterations of power iteration to `WᵀW`; and
3. returns zero immediately if the first/any iterate has norm below `1e-30`.

Power iteration is an estimator. Without a certified residual bound, spectral gap analysis, multiple starts, or a separate upper bound, it is not a rigorous upper bound on the largest singular value.

#### Deterministic exact counterexample

For a two-input layer, the implementation’s normalized start is:

```text
v0 = 1 / sqrt(1 + 1.1²)  = 0.6726727939963124...
v1 = 1.1 / sqrt(1 + 1.1²) = 0.7399400733959437...
```

Choose the nonzero one-row matrix:

```text
W = [v1, -v0]
```

Then the first matrix-vector product is exactly:

```text
W v = v1*v0 - v0*v1 = 0
```

The two products are bit-identical and cancel. The implementation returns `0.0` as the spectral norm.

But the true spectral norm of a one-row matrix is its Euclidean row norm:

```text
||W||₂ = sqrt(v1² + v0²) ≈ 1
```

Therefore:

- `spectral_normalize` sees an estimated norm of zero and does not scale the nonzero layer;
- `MlpSdf::new` records a Lipschitz constant of zero for a nonconstant linear function; and
- `safe_step_radius(value, 0)` returns positive infinity.

A nonconstant linear function has a zero plane, so an infinite no-sign-change ball is false.

A regression test can be expressed directly:

```rust
#[test]
fn fixed_start_nullspace_cannot_mint_zero_lipschitz() {
    let n = (1.0_f64 + 1.1_f64 * 1.1_f64).sqrt();
    let v0 = 1.0 / n;
    let v1 = 1.1 / n;
    let layer = Layer::new(vec![vec![v1, -v0]], vec![0.0]);

    // Current implementation returns zero, although the row norm is ~1.
    assert!(spectral_norm(&layer.weights) > 0.99);

    let net = MlpSdf::new(vec![layer], 1.0);
    assert!(net.lipschitz() > 0.99);
    assert!(safe_step_radius(net.eval(&[1.0, 0.0]), net.lipschitz()).is_finite());
}
```

#### Why existing tests miss it

The tests use:

- two friendly matrices for spectral norm;
- sampled pairs for a Lipschitz check;
- sampled points for interval containment;
- sampled gradients; and
- 64 sampled ray directions.

Sampling cannot prove a global upper bound, and none of the tests attacks the fixed-start nullspace.

#### Blast radius

The generic public `MlpSdf` guarantee is false. `fs-neuroshape-e2e` relies on `MlpSdf` and describes a “PROVEN neural implicit shape.” Its particular demo matrices may happen to produce the intended norm, but `run_campaign` accepts arbitrary `MlpSdf` values and reports the purported certified radius. The generic trust boundary is therefore unsound.

#### Required correction

At minimum:

- stop calling power iteration a certificate;
- return an Estimated norm unless a rigorous upper bound is computed;
- use a guaranteed upper bound such as a carefully overflow-checked Frobenius norm as a conservative fallback;
- or implement a verified eigen/singular-value enclosure with residual bounds and outward rounding;
- make `MlpSdf::new` fallible and reject nonfinite/invalid bounds;
- demote dependent `Verified` claims until the corrected bound is used; and
- add adversarial nullspace, clustered-spectrum, zero-matrix, nonfinite, and extreme-scale tests.

### F-02 — `fs-sos` contract describes a certificate API the source says was unsound and removed

**Severity:** High for contract trust  
**Evidence grade:** A  
**Files:** [`crates/fs-sos/CONTRACT.md`](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/crates/fs-sos/CONTRACT.md), [`src/lib.rs`](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/crates/fs-sos/src/lib.rs), [`Cargo.toml`](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/crates/fs-sos/Cargo.toml)

The current contract says:

- `certified_bound(p, tol)` returns a global bound when a tolerance-based coefficient check passes;
- the crate has “zero false certificates”; and
- it has no dependencies.

The current source says the opposite about the old API:

- a small coefficient residual can be arbitrarily negative for large `x`;
- the old tolerance-based `certified_bound(tol)` **forged certificates**; and
- callers must use newer exact/global or radius-scoped methods.

The manifest also depends on `fs-ivl` and `fs-math`.

This is decisive evidence that:

- contract text can be stale after a major semantic repair;
- `check-contracts` does not verify API or dependency truth; and
- “127 contracts” cannot be used as evidence that 127 crate specifications are current.

### F-03 — `fs-sos::is_psd` can panic on public malformed input despite a “total/no panics” contract

**Severity:** Medium  
**Evidence grade:** A  
**File:** [`crates/fs-sos/src/lib.rs`](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/crates/fs-sos/src/lib.rs)

`is_psd` accepts `&[Vec<f64>]` and forwards it to `min_eigenvalue`. The implementation sets `n = a.len()` and indexes both `a[i][j]` and `a[j][i]` for every `i,j < n` without checking that every row has length `n`.

A ragged or rectangular matrix can therefore panic by out-of-bounds indexing. The contract’s error model says “Total functions” and “No panics.”

The fix is straightforward: validate nonempty/square/finite input and return a typed result or a conservative false/refusal.

### F-04 — Contract enforcement is syntactic, not semantic

**Severity:** High as a governance misconception  
**Evidence grade:** A  
**File:** [`xtask/src/main.rs`](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/xtask/src/main.rs)

`check_contracts` performs substring checks for ten headings. It does not even require a referenced conformance file.

This is not itself a bug if described accurately. The problem is that repository prose often treats contract count as if it represented implemented, current, checked semantics.

A more accurate name would be `check-contract-shape` unless deeper checks are added.

### F-05 — License metadata conflicts with the actual license

**Severity:** Medium-high operational/legal metadata issue  
**Evidence grade:** A  
**Files:** [`Cargo.toml`](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/Cargo.toml), [`LICENSE`](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/LICENSE)

The workspace manifest declares:

```toml
license = "MIT OR Apache-2.0"
```

The actual file is an MIT-form license with a substantial OpenAI/Anthropic exclusion rider. There is no Apache-2.0 license in the inspected material, and the rider makes the license nonstandard.

This can mislead Cargo metadata consumers and automated compliance tools. The manifest should use an accurate `license-file` declaration and should not advertise `MIT OR Apache-2.0` unless that is genuinely the governing grant.

This review is not a legal opinion; it is a repository metadata consistency finding.

### F-06 — Quick-start and troubleshooting instructions bypass the exact pinned toolchain

**Severity:** Medium reproducibility defect  
**Evidence grade:** A  
**Files:** [`README.md`](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/README.md), [`rust-toolchain.toml`](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/rust-toolchain.toml)

The toolchain file pins:

```text
nightly-2026-07-06
```

The README tells users to run:

```bash
rustup toolchain install nightly
rustup component add rustfmt clippy --toolchain nightly
```

and later:

```bash
cargo +nightly test --workspace
```

`+nightly` explicitly selects the floating nightly and bypasses the repository pin. Components can also be installed for the wrong toolchain.

The instructions should use the exact channel, or simply let `rustup` honor `rust-toolchain.toml` and run:

```bash
rustup toolchain install nightly-2026-07-06 --component rustfmt --component clippy
cargo test --workspace
```

### F-07 — “Franken-only dependency” enforcement does not inspect transitive operational closure

**Severity:** Medium policy/claim-boundary issue  
**Evidence grade:** A  
**Files:** [`xtask/src/main.rs`](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/xtask/src/main.rs), [`Cargo.lock`](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/Cargo.lock), [`fs-wasm/Cargo.toml`](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/crates/fs-wasm/Cargo.toml)

The checker accepts any direct dependency whose name is:

- another workspace crate; or
- prefixed as a constellation dependency.

It does not recursively audit what constellation crates depend on. The lockfile contains many registry packages and platform crates, and `asupersync`’s closure includes native/platform-facing dependencies. `fs-wasm` directly admits `wasm-bindgen` and `getrandom` under its target section.

The policy is therefore a **direct-edge ownership policy**, not a proof of a pure-Rust, no-FFI, zero-third-party operational closure.

The docs should state that distinction explicitly.

### F-08 — Cross-ISA guide describes a stale/wrong constellation

**Severity:** Medium reproducibility/documentation issue  
**Evidence grade:** A  
**Files:** [`docs/CROSS_ISA_VERIFICATION.md`](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/docs/CROSS_ISA_VERIFICATION.md), [`constellation.lock`](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/constellation.lock)

The cross-ISA guide says FrankenSim has “8 sibling path-deps” and lists `franken_engine`. The current lock contains seven libraries and no `franken_engine`.

The same paragraph’s arithmetic is internally confusing: it says `frankensim + its 8 sibling path-deps` but lists eight repositories total.

A supposedly authoritative reproduction playbook should derive its inventory from `constellation.lock` rather than duplicate it manually.

### F-09 — Decalogue CI status table is stale relative to the tree

**Severity:** Medium governance drift  
**Evidence grade:** A  
**File:** [`docs/CI_GATES.md`](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/docs/CI_GATES.md)

The mapping says, among other things:

- P3 wiring arrives when `fs-ad` and the first solver land;
- P5 suites land with `fs-feec`;
- P7 executor-wide storms land with `fs-exec`;
- P8 lands with `fs-geom`/`fs-feec`;
- P9 replay lands with ledger time travel; and
- P10 catalog no-drift lands with `fs-ir`.

Those crates and several described mechanisms are already in the workspace. The remaining global gate may still be partial or deferred, but the stated reason/status is stale.

This table should be generated from machine-readable gate ownership and current evidence, not maintained as free prose.

### F-10 — README says neural representations are absent while the crate and campaign exist

**Severity:** Medium claim-state drift  
**Evidence grade:** A  
**Files:** [`README.md`](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/README.md), [`fs-rep-neural`](https://github.com/Dicklesworthstone/frankensim/tree/e7ebbab3fffff065021208979bf92efd990426e6/crates/fs-rep-neural), [`fs-neuroshape-e2e`](https://github.com/Dicklesworthstone/frankensim/tree/e7ebbab3fffff065021208979bf92efd990426e6/crates/fs-neuroshape-e2e)

The README limitation table says neural representations are not implemented as a first-class representation crate. Yet `fs-rep-neural` is a workspace member, has source/tests/contract, and is used by an e2e campaign and WASM surface.

A precise replacement would be:

> A minimal inference/certificate-oriented neural representation crate exists; training, analytic/autograd gradients, stronger bound propagation, and source-chart agreement certification remain staged.

### F-11 — `AGENTS.md` still describes the repository as “currently plan-first”

**Severity:** Low-medium truth-source drift  
**Evidence grade:** A  
**File:** [`AGENTS.md`](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/AGENTS.md)

The repository has a large working workspace, but its primary agent operating contract still says the project is “currently plan-first.” In a fast-moving agent project, stale orientation text can cause agents to privilege aspirational plan language over implemented reality.

The truth hierarchy should be updated to distinguish:

1. current source and tests;
2. current crate contracts;
3. current machine-generated status manifests; and
4. long-range plan documents.

### F-12 — Changelog endpoint is materially stale

**Severity:** Medium for lineage/audit claims  
**Evidence grade:** A  
**File:** [`CHANGELOG.md`](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/CHANGELOG.md)

The changelog is scoped through July 10 and a 999-commit checkpoint, while the inspected head is July 14 and roughly 1,400 commits beyond inception.

Periodic changelogs need not update every commit. But a repository that cites the changelog as durable agent-facing history should mark its staleness conspicuously or generate a current delta summary.

### F-13 — Orphaned, deliberately uncompilable scaffolds remain in the source tree

**Severity:** Medium semantic-sediment issue  
**Evidence grade:** A  
**Files:** `crates/fs-opt/src/{riemann,manifold,sexpr,expr,graph}.rs`

At least five `fs-opt` files are labeled:

```text
ORPHANED SCAFFOLD — NOT COMPILED
```

and include an inert `compile_error!` sentinel if reconnected.

This is an understandable consequence of the project’s categorical no-file-deletion rule. It is also visible historical sediment that:

- inflates source volume;
- complicates code search;
- can confuse agents and external reviewers;
- requires special explanation; and
- weakens claims of unusually clean, low-decay evolution.

A no-deletion policy should support a clearly segregated archive/quarantine with machine-excluded status rather than leaving dead implementation candidates beside live modules.

### F-14 — Current head lacks a publicly inspectable green execution proof

**Severity:** High evidentiary gap, not proof of failure  
**Evidence grade:** A/D  
**Sources:** current commit status, repository CI documentation, recent commits

GitHub reports no workflow run and no combined status for `e7ebbab`. That is expected in part because the project declares DSR—not GitHub Actions—the source of truth.

The problem is that the repository also documents limitations in the external DSR aggregate and does not include a head-specific sealed proof bundle containing:

- exact HEAD and constellation snapshot;
- commands;
- complete logs;
- terminal proof seals;
- test inventory;
- host/toolchain identities; and
- artifact hashes.

Recent commits include a small import fix described as unblocking the workspace build after earlier geometry/dimension errors. That does not imply the current head fails. It means a static reviewer cannot cite a public green result.

The correct status is **unknown**, not “passing.”

### F-15 — Inventory counts are mechanically accurate but weak evidence of depth

**Severity:** Methodological  
**Evidence grade:** A/C

The claim-state checker derives crate, contract, and test-file counts, which is good anti-drift hygiene.

But it does not distinguish:

- a 50-line smoke fixture from a mature solver;
- a live module from orphaned source;
- a sampled check from a theorem;
- an ignored perf lane from a required gate;
- a contract heading from a current specification; or
- an internally generated oracle from independent grounding.

Counts should remain inventory facts, not quality evidence.

---

## 6. Confirmed strengths that survive the re-audit

The defects above materially change the verdict, but several features remain genuinely unusual and valuable.

### 6.1 The representation router is more than architecture prose

The router has:

- explicit chart-kind nodes and converter edges;
- cost, error, and certification attributes;
- bounded Pareto search;
- deterministic tie-breaking;
- structured refusal reasons;
- execution through registered runners;
- evidence-bearing observations; and
- machine-specific cost learning behind a layer-clean interface.

That is a concrete realization of a deep project idea.

### 6.2 The ledger is an unusually serious subsystem for such a young project

The `fs-ledger` contract and source surface show sustained attention to:

- schema attestation;
- transactional migration;
- content addressing;
- bounded reads;
- artifact chunking;
- lineage;
- replay identity;
- time travel;
- session mutation authority;
- corruption refusal; and
- semantic versus envelope identity.

Even without independent execution, the design depth is real.

### 6.3 Failure history is often metabolized into code

Examples include:

- eliminating build-mode-dependent `powi` paths;
- recording exact reasons for golden changes;
- fixing signature/authentication self-authorization;
- distinguishing candidate performance baselines from authority-admitted gates;
- downgrading unconditional physical claims;
- adding schema/version/domain separation; and
- retaining explicit no-claim boundaries.

This is the strongest evidence for a potentially powerful lineage mechanism.

### 6.4 The project understands many epistemic hazards correctly

The code and contracts repeatedly recognize that:

- numerical verification is not model validation;
- a content hash is integrity, not authority;
- a signature string is not authentication;
- a sampled residual is not a global theorem;
- a validated model is regional;
- a weaker evidence ingredient must limit composition;
- a performance number needs a machine and denominator; and
- stochastic stopping requires appropriate inference.

The neural flaw is especially important because it does not erase that understanding; it demonstrates how difficult it is to enforce consistently.

### 6.5 The repository’s no-claim culture is better than typical generated software

Many crates explicitly state what they do not prove. This lowers the risk of reading every named algorithm as production capability.

The right conclusion is not “the contracts are worthless.” It is:

> **Contracts are valuable human-agent coordination artifacts whose truth still requires adversarial semantic verification.**

---

## 7. Alienness dimensions, scored conservatively

Scores are on a 0–5 scale and refer to evidence available at the inspected snapshot, not potential.

| Dimension | Score | Confidence | Rationale |
|---|---:|---:|---|
| **Absolute software substance** | 3.5 | Moderate-high | Large real source workspace with substantial mechanisms; depth uneven and not independently built |
| **Architectural breadth** | 4.5 | High | Exceptionally broad domain map and many concrete crates |
| **Nonlocal conceptual coherence** | 3.5 | Moderate | Strong recurring laws, but stale truth artifacts and semantic defects show meaningful coordination loss |
| **Behavioral integration** | 2.5 | Moderate-low | Smoke/e2e paths exist; full stack not independently executed |
| **Grounding surplus** | 2.0 | Moderate | Sophisticated grounding architecture, but mostly self-generated and at least one false certificate survived it |
| **Compression/generativity** | 2.5 | Low-moderate | Shared carriers and contracts plausibly reduce integration cost; no matched construction trial demonstrates the delta |
| **Temporal concentration** | 4.5 | High | Extraordinary source/history growth in roughly eight days |
| **Temporal maturity** | 1.0 | High | Structural maturity in places; almost no empirical maturity possible yet |
| **Operational closure** | 1.5 | High | Source substrate only; distributed external closure, no packaged app/release/public run bundle |
| **Production provenance** | 1.0 | High | Git history rich, but model/search/human/attempt ledger absent |
| **Independent assurance** | 1.0 | High | No clean-room reproduction or external validation inspected |
| **Foundry reliability** | 0.5 | High | No output distribution, held-out tasks, or matched baseline |
| **Evolution/lineage evidence** | 1.5 | Moderate-high | Intense short-horizon repair, but too young and already showing documentation/contract drift |
| **Causal disproportion** | 2.0 | Low | Plausible, but cannot be estimated without reference class and resource accounting |

### 7.1 What the score does and does not mean

This is not a scientific measurement. It is a disciplined way to expose which parts of the alienness claim are supported and which are being supplied by aesthetic impression.

The repository scores highest on:

- breadth;
- temporal concentration;
- architectural ambition; and
- explicit epistemic/governance design.

It scores lowest on the dimensions most essential to the strict post-agent definition:

- authenticated production provenance;
- independent assurance;
- operational maturity;
- foundry reliability; and
- matched causal comparison.

That asymmetry is why “alienness not established” is the correct verdict.

---

## 8. Alternative explanations that must be fully credited

A strict alienness analysis must explain why ordinary post-agent mechanisms may account for much of the apparent anomaly.

### 8.1 A very detailed master plan supplies global coherence

Much of the repeated architecture is specified centrally in advance. Agents following one long constitution will naturally produce more uniform semantics than independent teams inventing locally.

That is excellent process design. It reduces the unexplained residue.

### 8.2 Shared model priors produce correlated specialist fluency

Multiple agent identities do not imply independent expertise. They may share:

- training corpora;
- stylistic patterns;
- favored abstractions;
- scientific misconceptions;
- and reward-induced confidence habits.

The same error can therefore appear coherently in code, tests, contracts, and explanation.

### 8.3 Parallel generation explains breadth and speed

Repository-scale models can generate implementations, tests, contracts, documentation, and repair commits at a rate unavailable to a pre-agent team.

The resulting volume is historically striking but causally ordinary relative to strong agents and heavy iteration.

### 8.4 The sibling constellation externalizes capability

FrankenSim inherits:

- structured concurrency;
- storage;
- dataframe/graph/numerical support;
- ML components;
- and a large transitive ecosystem.

The full artifact is much larger than one repository.

### 8.5 Fine-grained commits amplify the apparent history

The history includes:

- implementation commits;
- contract updates;
- issue-ledger exports;
- narrow hardening passes;
- formatting/build fixes;
- and documentation refreshes.

Commit count is not comparable to conventional team commit count without normalization.

### 8.6 Internal test generation can create impressive but correlated coverage

A test suite written from the same mistaken model as the implementation may pass comprehensively. `fs-rep-neural` is a concrete example: the test battery was broad enough to look convincing but did not challenge the estimator’s fixed-start failure mode.

### 8.7 Smoke-tier vertical slices compress scope

A crate can correctly compose several APIs while operating on a deliberately narrow, small, manufactured fixture. That proves interface compatibility, not production fidelity across a whole scientific domain.

### 8.8 Named algorithms can overstate delivered depth

The repository often does a good job distinguishing scaffolds and no-claims, but top-level architecture prose contains full research-program names. A reader can easily infer more than the code implements.

The vision-versus-reality table is necessary to counter this effect.

### 8.9 The no-deletion rule preserves visible volume and sediment

Retaining all obsolete files protects against destructive agent behavior, but it also means source-tree size includes intentionally dead code.

### 8.10 Selection effects are unknown

The public tree is the surviving trajectory. We do not know:

- how many alternatives were generated;
- how much code was discarded before commit;
- how many agent-hours failed;
- how much human filtering occurred; or
- whether comparable projects under the same process usually succeed.

The best output shows reachability. It does not show production reliability.

---

## 9. Artifact, foundry, and lineage—revised separately

### 9.1 Artifact alienness

A functioning artifact can be alien even if its production process is not repeatable.

For FrankenSim, source-level substance is clear. Functioning at the full claimed envelope is not. The repository is best classified as:

> **A substantial, unusually integrated research-software artifact with unresolved assurance and operational closure.**

Alien artifact status remains open.

### 9.2 Foundry alienness

A foundry claim requires repeated transformation of new intentions into coherent artifacts under bounded resources, with:

- attempt distributions;
- success probability;
- equal-resource baselines;
- held-out tasks;
- ablations;
- model swaps; and
- inherited semantics in each extension.

FrankenSim has infrastructure suggestive of a foundry:

- Beads;
- agent operating rules;
- contracts;
- policy gates;
- identity registries;
- golden couplings;
- a design ledger; and
- a very rapid repair loop.

But one repository trajectory is not a foundry evaluation.

The correct term is:

> **Proto-foundry or foundry research program, not demonstrated alien foundry.**

### 9.3 Lineage alienness

Lineage alienness requires sustained coherent evolution through changing requirements, failures, and environments.

Positive evidence:

- rapid schema migrations;
- cross-cutting unit migration from five to six dimensions;
- content-identity versioning;
- golden rationale;
- hardening passes; and
- explicit repair history.

Negative evidence:

- stale contracts;
- stale README claims;
- stale CI status;
- stale agent orientation;
- stale changelog;
- dead scaffolds;
- and at least one false certificate crossing source, tests, contract, and e2e prose.

At eight days, the only defensible conclusion is:

> **Lineage potential is visible; lineage alienness is not. Early semantic decay is already measurable.**

---

## 10. The strongest residual explanatory surplus

After fully crediting agents, plans, tools, reuse, parallelism, selection, and sibling repositories, what remains unusual?

### 10.1 The breadth of attempted semantic integration

Most generated repositories optimize for local feature completion. FrankenSim repeatedly attempts to carry the same deeper obligations through unrelated domains:

- identity;
- dimensions;
- cancellation;
- bounded work;
- evidence rank;
- provenance;
- replay;
- deterministic serialization;
- no-claim behavior; and
- machine context.

### 10.2 The speed of institutionalization

Failures often become:

- named beads;
- source comments;
- domain/version identities;
- regression tests;
- policy checks;
- contract amendments; and
- explicit historical explanations.

That is more interesting than the raw code count.

### 10.3 The human operator’s architectural discipline

The repository strongly suggests a central operator who:

- insists on explicit invariants;
- preserves failures;
- demands adversarial evidence;
- uses agents as a coordinated production ecology; and
- repeatedly pushes local fixes into cross-repository law.

This may itself explain much of the coherence. It is still an unusually effective post-agent engineering practice.

### 10.4 Why the residue is not yet alienness

The residue has not been shown to be:

- a robust extreme outlier;
- typical of the process rather than selected;
- superior to equal-resource baselines;
- independently grounded;
- operationally mature; or
- causally disproportionate after full resource accounting.

Thus the residue is **an anomaly worth studying**, not a closed alien-artifact proof.

---

## 11. What would establish—or falsify—the stronger claim

The next work should prioritize epistemic closure over new breadth.

### 11.1 Fix and publicly disclose the confirmed certificate defects

Before promoting alienness, the project should:

- add the `fs-rep-neural` adversarial regression;
- replace/demote the spectral certificate;
- review every dependent `Verified` path;
- update `fs-sos` contract and tests;
- validate `is_psd` input shape; and
- audit other “certified,” “exact,” “sound,” “proof,” and `Verified` constructors with adversarial counterexample generation.

A public defect-and-repair record would strengthen rather than weaken trust.

### 11.2 Publish a sealed head-specific verification bundle

For one frozen commit, retain:

- exact root and sibling commits;
- source-tree content identity;
- toolchain identity;
- every command;
- full untruncated logs;
- test/target inventory;
- per-lane result rows;
- terminal proof seals;
- x86/aarch64 host identity;
- performance authority inputs where applicable; and
- a standalone verifier.

The bundle must be downloadable and independently checked without trusting DSR’s summary.

### 11.3 Produce an authenticated construction ledger

For a future fixed evaluation window, record:

- model and harness versions;
- number of agents and concurrent contexts;
- token/inference/tool usage;
- wall-clock and monetary cost;
- prompts or reproducible task descriptions;
- failed branches and retries;
- discarded candidates;
- human edits and review time;
- sibling-repository work attributable to FrankenSim;
- imported code/data; and
- best, median, and failed outcomes.

### 11.4 Run matched equal-resource baselines

At least:

1. direct agent use with the same master task;
2. a strong off-the-shelf repository agent;
3. FrankenSim process without contracts;
4. without Beads/identity memory;
5. without evidence/color machinery;
6. without custom policy gates; and
7. the full process.

Use the same models, total budget, human attention, and elapsed time.

### 11.5 Run held-out foundry challenges

Outside evaluators should choose unfamiliar tasks only after the system is frozen. Examples:

- add a seventh base dimension with wire migration;
- add a new chart representation and conversion route;
- introduce a new PDE operator plus adjoint;
- rotate an evidence schema without laundering old claims;
- recover from a deliberately corrupted ledger;
- port a flagship to a new ISA; and
- add a requirement that cuts across units, runtime, evidence, ledger, package, and WASM surfaces.

Measure:

- completion rate;
- correctness;
- inherited semantics;
- human review burden;
- regression count;
- duplicated concepts;
- and time to a sealed proof.

### 11.6 Audit a stratified source sample externally

Select at least 15–20 crates across:

- deterministic math;
- intervals/exact predicates;
- sparse/dense numerics;
- geometry;
- meshing;
- FEEC/CutFEM;
- solvers;
- adjoints;
- stochastic inference;
- optimization;
- evidence;
- ledger;
- packaging/checker; and
- e2e campaigns.

Independent experts should attempt to falsify the strongest public invariant in each.

### 11.7 Separate integrity, theorem, validation, and authority gates mechanically

The code already distinguishes these concepts in many places. The repository needs a generated claim registry that records, for every public strong claim:

- claim text;
- owner;
- source symbol;
- contract clause;
- evidence type;
- theorem assumptions;
- independent falsifier;
- required execution lane;
- current status;
- last verified commit; and
- no-claim boundary.

A README sentence should be generated from this registry or fail a gate.

### 11.8 Test long-horizon evolution

After freezing a baseline, run repeated externally chosen changes for months. Track:

- contract drift;
- doc drift;
- dead code;
- API duplication;
- dependency creep;
- test oracle independence;
- migration failures;
- and mean change-propagation cost.

Only then can lineage claims become meaningful.

### 11.9 Accumulate empirical maturity

Synthetic tests cannot fully replace:

- external users;
- real malformed data;
- long-running studies;
- hardware turnover;
- operational incidents;
- disputed scientific models;
- and adversarial misuse.

The project needs time in reality.

---

## 12. Prioritized remediation plan

### P0 — Scientific trust boundary

1. **Demote or repair `fs-rep-neural` certification immediately.**
2. **Audit `fs-neuroshape-e2e` and WASM claims that depend on it.**
3. **Update `fs-sos` contract to the current exact/scoped APIs.**
4. **Make `is_psd` fallible and shape/finite checked.**
5. **Search all public uses of `Verified`, `Certified`, “proof,” “sound,” “exact,” and “cannot” for constructor authority and adversarial tests.**

### P0 — Truth-source consistency

6. **Fix root license metadata.**
7. **Fix exact toolchain instructions.**
8. **Regenerate the constellation inventory in every document.**
9. **Update or generate the Decalogue gate-status table.**
10. **Update README neural-representation status.**
11. **Update `AGENTS.md` truth-source hierarchy.**
12. **Mark changelog staleness or auto-generate a current delta.**

### P1 — Contract governance

13. Replace `check-contracts` with a layered set of checks:

- contract shape;
- named API existence;
- manifest dependency agreement;
- conformance file existence;
- source/contract version stamp;
- compiled documentation examples;
- no stale symbol references;
- claim registry linkage; and
- current verification receipt.

14. Rename the existing check to make its limited semantics explicit.

15. Add adversarial “certifier certification” suites that are designed by a different model/operator or externally reviewed.

### P1 — Public verification

16. Publish sealed, head-specific result bundles.
17. Add a small standalone verifier for source snapshot, result rows, and seals.
18. Avoid claims that a private or external DSR summary alone establishes repository health.

### P2 — Source hygiene

19. Move orphaned scaffolds into a clearly excluded archive with a machine-readable tombstone.
20. Add a gate that live source directories cannot contain unreferenced implementation modules unless explicitly quarantined.
21. Track semantic-debt metrics separately from raw file counts.

### P2 — Alienness evaluation

22. Freeze a future evaluation window.
23. Capture the production ledger.
24. Run equal-resource baselines and ablations.
25. Commission held-out construction tasks.
26. Report distributions, not only the best repository.

---

## 13. Revised final formulation

FrankenSim is not merely a giant generated repository. The source contains too much real structure, too many cross-cutting mechanisms, and too much deliberate failure handling for that dismissal to be fair.

It is also not yet a defensible post-agent alien artifact.

The project’s central aspiration is to make claims carry their own reasons for trust. The re-audit found that one of its public certificate paths can produce a false global bound through a deterministic, simple adversarial input, while the surrounding contract and sampling tests call the result certified. A separate proof-oriented crate has a contract that still describes an API its own source says forged certificates. Several repository-wide truth sources disagree about basic operational facts.

Those findings do not make FrankenSim ordinary. They make the current evidence more honest:

- the **architecture** is exceptional;
- the **implementation breadth** is remarkable;
- the **integration effort** is substantial;
- the **governance design** is unusually ambitious;
- the **operational maturity** is low;
- the **independent grounding** is weak;
- the **production provenance** is insufficient; and
- the **strict causal outlier claim** is untested.

The most accurate present conclusion is:

> **FrankenSim is an extraordinary rapid research-software construction and a serious candidate experiment in post-agent software coordination. Its alien-looking feature is the amount of shared architectural law attempted across a huge technical surface in very little time. But its “alienartifact-ness” remains unproven because the causal comparison is missing, the full artifact is not independently reproduced or operationally mature, and the project’s own assurance machinery has already admitted at least one false certificate and multiple truth-source drifts.**

A compact formulation:

> **FrankenSim currently demonstrates unusual concentration of architectural intent—not yet causally disproportionate, independently grounded, durable functioning consequence.**

And the most useful forward-looking formulation:

> **The next frontier is not adding more crates. It is proving that the existing shared law is true, externally checkable, causally attributable, and stable under adversarial extension.**

---

## 14. Evidence map

All repository links below are pinned to the inspected commit.

### Governing definitions supplied by the user

- `post_agent_alien_artifact(1).md` — canonical post-agent definition
- `pre_claude_code_alien_artifact(1).md` — pre-agent contrast definition

### Snapshot and public scope

- [Inspected head](https://github.com/Dicklesworthstone/frankensim/commit/e7ebbab3fffff065021208979bf92efd990426e6)
- [Initial plan commit](https://github.com/Dicklesworthstone/frankensim/commit/8e4c0a5c4f18aa7d0bd0add47e407b835c7a3b86)
- [Inception-to-head comparison](https://github.com/Dicklesworthstone/frankensim/compare/8e4c0a5c4f18aa7d0bd0add47e407b835c7a3b86...e7ebbab3fffff065021208979bf92efd990426e6)
- [README](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/README.md)
- [Root Cargo manifest](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/Cargo.toml)
- [Pinned toolchain](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/rust-toolchain.toml)
- [Constellation lock](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/constellation.lock)
- [Cargo lock](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/Cargo.lock)
- [Actual license](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/LICENSE)

### Vision and governance

- [Comprehensive plan](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/COMPREHENSIVE_PLAN_FOR_FRANKENSIM.md)
- [Agent operating contract](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/AGENTS.md)
- [Workspace conventions](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/docs/CONVENTIONS.md)
- [CI gates](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/docs/CI_GATES.md)
- [Cross-ISA playbook](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/docs/CROSS_ISA_VERIFICATION.md)
- [Bootstrap guide](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/docs/BOOTSTRAP.md)
- [`xtask` policy implementation](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/xtask/src/main.rs)
- [`xtask` claim-state implementation](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/xtask/src/claims.rs)
- [Changelog](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/CHANGELOG.md)

### Confirmed defect sources

- [`fs-rep-neural` source](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/crates/fs-rep-neural/src/lib.rs)
- [`fs-rep-neural` contract](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/crates/fs-rep-neural/CONTRACT.md)
- [`fs-rep-neural` tests](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/crates/fs-rep-neural/tests/neural.rs)
- [`fs-neuroshape-e2e` source](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/crates/fs-neuroshape-e2e/src/lib.rs)
- [`fs-neuroshape-e2e` contract](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/crates/fs-neuroshape-e2e/CONTRACT.md)
- [`fs-sos` source](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/crates/fs-sos/src/lib.rs)
- [`fs-sos` contract](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/crates/fs-sos/CONTRACT.md)
- [`fs-sos` manifest](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/crates/fs-sos/Cargo.toml)
- [Orphaned `fs-opt` scaffold example](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/crates/fs-opt/src/riemann.rs)

### Representative substantial implementations

- [`fs-geom` representation router](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/crates/fs-geom/src/router.rs)
- [`fs-geom` contract](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/crates/fs-geom/CONTRACT.md)
- [`fs-evidence` contract](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/crates/fs-evidence/CONTRACT.md)
- [`fs-exec` contract](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/crates/fs-exec/CONTRACT.md)
- [`fs-ledger` contract](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/crates/fs-ledger/CONTRACT.md)
- [`fs-ga` contract](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/crates/fs-ga/CONTRACT.md)
- [`fs-plan` contract](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/crates/fs-plan/CONTRACT.md)
- [`fs-adjoint` contract](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/crates/fs-adjoint/CONTRACT.md)
- [`fs-flagship-e2e` contract](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/crates/fs-flagship-e2e/CONTRACT.md)
- [`fs-flagship-e2e` tests](https://github.com/Dicklesworthstone/frankensim/blob/e7ebbab3fffff065021208979bf92efd990426e6/crates/fs-flagship-e2e/tests/e2e_battery.rs)

---

## Appendix A — Minimal adversarial reasoning for the neural certificate

This appendix restates the source-level failure in compact mathematical form.

The algorithm chooses a fixed nonzero starting vector and normalizes it:

```text
s = normalize([1, 1.1]) = [a, b]
```

Define:

```text
W = [b, -a]
```

Then:

```text
W s = ba - ab = 0
```

The implementation returns zero before discovering any other singular direction.

Yet:

```text
W Wᵀ = b² + a² = 1
```

so the sole nonzero singular value is one.

The failure does not depend on stochastic bad luck, a difficult matrix, or insufficient samples. It is constructed directly from the algorithm’s public fixed start.

Any certificate based on this estimate is invalid for the generic input domain.

---

## Appendix B — Claims that should be demoted pending external evidence

The following wording classes should be treated conservatively wherever they occur:

- “certified” when backed only by sampled tests;
- “exact” when floating construction or platform arithmetic participates;
- “bit-stable across ISAs” without a current two-ISA retained row;
- “zero false certificates” without adversarial certifier trials;
- “working” when the referenced lane is ignored, feature-gated, smoke-tier, or not publicly executed at the current head;
- “Franken-only” when discussing full transitive closure;
- “proven” when the source supplies integrity but not external authority;
- “validated” without authenticated external anchors;
- “production” when the implementation is a fixture or reduced campaign; and
- “current” in hand-maintained status documents without a generated freshness marker.

---

## Appendix C — A compact future re-audit checklist

A future reviewer should be able to answer all of these with retained evidence:

1. What exact source and sibling snapshot was run?
2. Can a clean machine reproduce the workspace using only documented steps?
3. Does the exact pinned toolchain run every required target?
4. Where is the sealed full-log result bundle?
5. Which strong claims have independent falsifiers?
6. Which certificate constructors have adversarial counterexample tests?
7. Do contracts match current public APIs and dependencies?
8. Are README and gate statuses generated from current claim state?
9. What models, agents, tools, cost, attempts, and human hours produced the evaluated window?
10. What do equal-resource baselines produce?
11. What disappears under ablation?
12. What is the median result across held-out tasks?
13. Which parts are smoke-tier, ignored, estimated, or externally contingent?
14. Has an independent party reproduced the flagship evidence?
15. What empirical failures have been converted into structure over at least several months?

Until those questions have strong answers, FrankenSim should be described as an exceptional candidate and research program—not as a demonstrated alien artifact.
