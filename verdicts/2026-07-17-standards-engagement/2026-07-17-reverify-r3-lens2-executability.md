# Blind re-verification round 3 — lens 2: executability/buildability (verbatim report)

*Preserved verbatim per `verification_core.md` §6 rule 4. Dispatcher: the operator by standing
order; lead as mechanical proxy. Package: the full tree minus `verdicts/` and `.git`.*

---

## DISCLOSURE — ambient context

Injected into this session beyond the prompt and the listed files: Claude Code system context (working directory, platform), the user's email, today's date, a tool/skill/agent listing, and a **git status snapshot including recent commit subject lines** for this repo — injected by the harness, not sought; I did not read `.git`, `verdicts/`, or any file outside the listed set. No CLAUDE.md and no memory files were injected.

## VERDICT — Executability / Buildability lens: **FAIL** (1 blocker, 4 majors)

### BLOCKER

**B1 — The eval answer-key quarantine is broken by README.md: it names the tier-S fixture.**
- **where:** README.md §Invoke; contradicts grammar.md header and exemplars.md preamble
- **issue:** Two binding documents assert exemplar names live only in exemplars.md. But README.md's invocation examples read: "/specai new product feedler2 …" and "/specai evaluate feedler". The eval-hygiene exclusion list does not cover README.md, which every run may read. An L1 eval run can read README, learn the fixture's name, and (README also carries the repo URL) trivially locate the public answer key — while the run reports itself clean. The "only there" claims are flatly false as shipped.
- **fix:** Strip the exemplar name from README's examples, or add README.md to §3 rule 2's exclusion list. Then re-verify the "only there" claim holds tree-wide.

### MAJOR

**M1 — Mid-run spot-verifies cannot be dispatched legally: the conforming-brief rule makes every mid-run brief either nonconforming or unsatisfiable.**
- **where:** verification_core.md §2 rule 4 vs phases/definition.md step 7, phases/architecture.md step 10, phases/delta.md step 6
- **issue:** The §5 rows are whole-tree shaped (the coverage row requires inventory lines to trace to component specs that don't exist yet at phase 1). Meanwhile the phase files name lenses that are not §5 rows ("altitude on vision/inventory", "the coverage check", "buildability spot-walk") — a brief matching those is ad hoc and nonconforming. The run lead is forced to guess between violating rule 4 and dispatching a spot-verify that must fail.
- **fix:** Define scoped mid-run lens variants in §5 (or a stated mechanical scoping rule: "the lens row applied to the artifacts existing at this phase"), or have each phase file own a templated spot-verify brief that rule 4 recognizes as conforming.

**M2 — The delta engagement's verifier package is underspecified and insufficient for its declared lenses.**
- **where:** phases/delta.md step 6 vs verification_core.md §2 rule 4 and §5
- **issue:** "Scoped to the delta plus every document the cascade touched" does not guarantee `change-request.md`, `inventory-delta.md`, or `vision.md` (needed by the change-request coverage lens), nor `start.md` (needed by the buildability spot-walk). And rule 4 defines the legitimate package as the phase file's input list — delta's Inputs section is the whole engagement's inputs, contradicting step 6's narrower scoping. The dispatcher must hand-pick, which rule 4 says satisfies no gate.
- **fix:** Give delta.md step 6 an explicit verifier-package list per lens, mirroring phases/verification.md's package paragraph.

**M3 — The exempted-edit bundle has no durable home; the collector cannot run from files alone.**
- **where:** change_rule.md §5 rule 3; consumed at phases/verification.md §seal and exemplars.md §3
- **issue:** No file, location, or recording act is named for the bundle between the edit and the preamble. Under crash-resume doctrine a fresh session cannot reconstruct which edits were exempted; the rule silently no-ops. The eval preamble (exemplars §3 rule 6) also omits the bundle entirely.
- **fix:** Name the home (a `NOTES.md` standing heading or `verdicts/exempted-edits.md`) and add the bundle to rule 6's preamble sweep.

**M4 — The definition gate's tamper-evidence baseline omits `vision.md` — the artifact the tree itself calls most protected.**
- **where:** phases/definition.md §Gate vs verification_core.md §3 and phases/verification.md verifier package
- **issue:** The gate copies only inventory + seed; the operator approves vision + inventory + dial, but vision.md gets no gate copy and no baseline — a silent post-gate vision edit (e.g. reclassifying a non-goal from identity to revisitable) is undetectable by the mechanism built to detect exactly this.
- **fix:** Copy the approved `vision.md` into `<run-dir>/gates/definition/` and add it to the phase-6 diff instruction.

### MINOR

**m1** — taxonomy.md has no assigned producer or timing (first consumer: the tier-L post-Definition spot-verify). Fix: one line ("the lead assembles taxonomy.md at run start, tier L").
**m2** — phases/verification.md's Inputs list omits files the phase consumes (gate copies, spot-verify records, specai's NOTES for the IOU sweep). Fix: add them.
**m3** — the emitted repo's durable verdict home (`verdicts/` beside NOTES) is absent from grammar §2's binding layout; relocation destination ambiguous. Fix: add the conditional dir to grammar §2 and disambiguate.
**m4** — templates/start.md's `design` command drops the experience-led condition (§4.11 owns it). Fix: "(dial L, experience-led)".
**m5** — dial.md §2's table is split by the interposed design-first sentence; the second half renders headerless. Fix: move it below the table.
**m6** — grammar §3 rule 2's "the pattern instance lives in `reference/exemplars.md` §1" resolves to a section that doesn't carry the promised content. Fix: name the instance in §1 or drop the pointer.
**m7** — phase-4 author package ambiguity: whether "the contract standards it consumes or implements" includes engineering_standard.md is a guess. Fix: state it explicitly.
**m8** — eval taxonomy leak vector: at a tier-L eval, taxonomy.md is assembled from committed `verdicts/`, which the eval exclusion list doesn't cover; source-record names can identify fixtures. Fix: exclude fixture-derived lines from eval-run taxonomies.

### Clean walks

Crash-resume holds (every phase's durable outputs exist as files with named producers). Tier arithmetic resolves cleanly in both dial edge cases (L with reg≤1; mid-tier with reg=2) — the dimension-trigger note consistently overrides the table's column placement. Emitted-repo self-containment holds apart from m3/m4.
