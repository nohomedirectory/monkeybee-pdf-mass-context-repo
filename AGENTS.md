# AGENTS.md — MonkeyBee Campaign Repository

**Status:** Seed version 1.0 (2026-07-14). The overnight run's G0 subgoal extends this file; preserve every rule below when extending.
**What this repo is:** The planning and evidence substrate for the MonkeyBee campaign — a clean-room, memory-safe PDF engine in Rust, built through instrumented plan→beads→swarm cycles, aiming to answer two precommitted questions (Q3: artifact-alien candidate verdict; Q2: field-leading completion measurement) by independent adjudication. Right now this repo contains **documents only**. That is deliberate.

---

## Rule 0 and the core rules

0. **The human's instructions override everything below.**
1. **No file deletion**, ever, without explicit human permission.
2. **No destructive git commands** (`git reset --hard`, `git clean -fd`, `rm -rf`, force-push without lease).
3. **All work on `main`.** No branches, no worktrees.
4. **No file proliferation** — no `_v2`/`_improved` variants. Versioned successors follow the explicit convention below (`*_v1.1.md` with changelog) and nothing else.
5. **Multi-agent awareness:** never stash, revert, or overwrite another agent's changes; treat them as your own work you don't remember making.
6. **After any context compaction: reread this file.** Then continue.

## Campaign-specific golden rules

7. **Plan space only, until the human says otherwise.** No beads (`br` creation), no pseudo-bead markdown inventories, no source code, no build scaffolding. The current phase produces planning substrate.
8. **Clean-room law is absolute** (Rev 7 §4): never clone/fetch/read/cite existing PDF processor source or docs (pdf.js, PDFBox, MuPDF, Poppler, PDFium, iText, QPDF, Ghostscript, lopdf, pdf-rs, hayro, krilla, and the rest of the prohibited list). **No SpecCard semantic bodies** from model memory — registry and slots only, `PENDING-LICENSED-SOURCE`.
9. **No measurements** of or comparisons against other PDF libraries before the discovery protocols are committed through the substrate. Premature measurement permanently poisons the Q2 evidence chain.
10. **No external actions** — nothing sent, published, purchased, or posted. Drafts only.
11. **Canonical inputs are read-only** (list below). All new work = new files with a provenance header (`generated-by`, `date`, `inputs`, `status: DRAFT | PROPOSED`). Findings against a canonical doc go to `DISPUTES.md` or a versioned successor — never silent edits.
12. **Log to the run ledger** (`ledger/`): sub-agent spawns, review rounds, findings counts, fetches, failures, disputes. Everything is `provisional-pending-substrate` until the human establishes the tamper-evident commitment channel.
13. **Claim vocabulary is law:** no "best," "complete," "fastest," "mogged," or any supremacy phrasing anywhere in repo documents outside properly scoped claim structures (Rev 7 §10.3/§24). When in doubt, understate.

## Truth hierarchy (when documents disagree)

1. **The human**, live.
2. **MONKEYBEE_CAMPAIGN_CHARTER_v1.md** (+ CYCLE_0_WORK_ORDER.md, AUDIT_FINDINGS_LEDGER.md, CAMPAIGN_CHARTER_REASONING.md) — governs the campaign: cycles, goals, gates, constraints.
3. **Constitution v8** (once extracted; until then, Rev 7's kernel sections §§4/6/9/10/11/33/34) — governs the product's laws.
4. **MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md** — the source plan; authoritative for domain content until superseded section-by-section by the extraction.
5. **Definitions** (pre_claude_code_alien_artifact.md, post_agent_alien_artifact.md) — govern what alienness claims mean.
6. **frankensim_alienartifactness_reaudit.md** (+ ALIEN_ARTIFACT.md if present — note: partially superseded by the re-audit) — cautionary reference; the failure catalog this campaign is designed against.

Conflicts between levels: higher wins; log the conflict in `DISPUTES.md`. Conflicts within a level: stop and log; do not resolve silently.

## Reading order for a fresh agent

1. This file. 2. INDEX.md (if it exists yet). 3. MONKEYBEE_CAMPAIGN_CHARTER_v1.md. 4. Your current goal file (e.g., OVERNIGHT_GOAL.md). 5. CYCLE_0_WORK_ORDER.md + AUDIT_FINDINGS_LEDGER.md. 6. Whatever your task's authority chain names next. Read Rev 7 sections on demand, not linearly — it is 75k words; the Charter tells you which sections own what.

## File inventory (seed; INDEX.md supersedes when generated)

| File | Role |
|---|---|
| MONKEYBEE_PDF_PLAN_REVISION_7_ALIEN_AUDIT.md | Source plan (read-only canon) |
| MONKEYBEE_CAMPAIGN_CHARTER_v1.md | Campaign law: 7 cycles, goals, gates |
| CAMPAIGN_CHARTER_REASONING.md | Why the Charter is shaped this way |
| CYCLE_0_WORK_ORDER.md | First executable step (this phase) |
| AUDIT_FINDINGS_LEDGER.md | All known defects + fix status |
| OVERNIGHT_GOAL.md | Active goal for the overnight run |
| pre_claude_code_alien_artifact.md / post_agent_alien_artifact.md | Governing definitions (read-only canon) |
| frankensim_alienartifactness_reaudit.md | Cautionary case study (read-only canon) |
| PROJECT_OVERVIEW.md / ALIEN_ARTIFACT.md (if present) | Background context (read-only; ALIEN_ARTIFACT.md partially superseded — see ledger R2-N7) |

## Process reference

Methodology intuition (planning, fresh-eyes review, convergence, blunder hunts, de-slopification): **https://agent-flywheel.com/complete-guide**. All installed Flywheel skills/tools are available; rules 7–10 above constrain which are appropriate in this phase.

## The spirit of this repo

Every document here exists to make one thing true: that when this project claims something, the claim carries its own reasons for trust. The FrankenSim re-audit in this repo shows what happens to extraordinary work without that property. Prefer verified-and-small over impressive-and-unaccounted, in every task, at every scale.

---

## G0 extension — navigation and evidence hygiene

**Extension provenance:** `generated-by: Codex G0 owner`; `date: 2026-07-14`; `inputs: AGENTS.md, OVERNIGHT_GOAL.md, INDEX.md, reports/INGEST_REPORT.md`; `status: PROPOSED`; `evidence-status: provisional-pending-substrate`.

Every seed rule above remains unchanged and governs this extension.

14. **`INDEX.md` is navigation, not authority.** It records where things are and how they are classified. If it disagrees with the truth hierarchy above, follow the hierarchy and record the mismatch in `DISPUTES.md`.
15. **Classify before relying.** Distinguish read-only canon, generated campaign artifacts, owner checkpoints, orchestration ledgers, and local control-plane state. Generated or operational state never silently upgrades or supersedes canon.
16. **Do not reconstruct unavailable inputs.** If a named input is absent, record `SOURCE-UNAVAILABLE`, identify the dependent finding or task, and wait for the exact artifact. A related document is context, not a substitute.
17. **Make verification reproducible.** Prefer stable section identifiers. Local line numbers are supporting coordinates, not durable IDs. An absence finding records the searched file, bounded region when applicable, and search vocabulary.
18. **Keep shared state disk-first.** Owner phase and unresolved evidence live in the owner's checkpoint and partial artifact. Orchestration state routes work; an owner checkpoint records the owner's current progress. Any meaningful mismatch is surfaced rather than silently reconciled.
19. **Treat `.ntm/` as local control-plane state.** It is non-normative, may change during a run, and must not be cited as campaign evidence. Its existence and classification belong in the run ledger and repository inventory.
20. **Generated prose cannot strengthen a claim.** Reports and summaries preserve the scope, uncertainty, provenance, and no-claim boundary of their source evidence.

For a handoff, a fresh agent should be able to state four things after the reading order above: the active goal, its authority chain, the files it may change, and every unavailable input that affects its work. If any answer is unclear, stop at orientation and record the ambiguity.
