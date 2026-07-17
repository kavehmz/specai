# Blind re-verification round 3 — lens 1: consistency/contract (verbatim report)

*Preserved verbatim per `verification_core.md` §6 rule 4. Dispatcher: the operator by standing
order; lead as mechanical proxy. Package: the full tree minus `verdicts/` and `.git`.*

---

**DISCLOSURE — ambient context beyond the prompt and listed files:** my session carries the Claude Code system prompt for this repo, which injected: the working directory path, a git status snapshot including recent commit subjects (`verdicts and review`, `adding the concept of drift`, `readme: real skill installation...`, `specai: initial release`), the user's email and today's date (2026-07-17), and a harness skill/tool listing. No CLAUDE.md and no memory files were injected. I read nothing outside the 20 listed files (verdicts/ and .git untouched). The commit subjects are a mild authoring-history hint; they did not inform any finding below.

# Lens verdict: **FAIL** (1 blocker, 3 majors)

## BLOCKER

**B1 — {where: phases/architecture.md §Procedure step 3, severity: blocker}**
**Issue:** Exemplar decomposition shapes — facts `reference/exemplars.md` declares live only in itself — are carried inline in a binding phase file that every eval run must read. The eval-exclusion invariant does not hold.
**Evidence:** exemplars.md header: "This file is the **only** home of the exemplars' identifying calibration facts — names, tiers, sizes, dial breakdowns, **decomposition shapes**, signature principles…" Versus phases/architecture.md step 3: "a tier-S product may be one deployable with a handful of *spec areas*; a tier-L platform may be **eight-plus components hosting a product family** (scored instances: `reference/exemplars.md`)." Compare exemplars.md §2: "~6.9K spec lines; **8 platform components plus a product family**" and §1: "one deployable with seven spec areas." An L4 eval run reads phases/architecture.md and receives the target's decomposition shape near-verbatim.
**Fix:** Delete both shape illustrations from step 3; keep only "Right-size to the dial (scored decomposition instances: `reference/exemplars.md` — cited, never carried here)."

## MAJOR

**M1 — {where: phases/verification.md §Pass 1, severity: major}**
**Issue:** Pinned check count contradicts the owning checklist. grammar.md §6 contains **eight** numbered checks; verification.md pins seven — in the same sentence that forbids restating.
**Evidence:** verification.md: "Run the `grammar.md` §6 checklist literally — **all seven checks**, including their stated exemptions; this file does not restate them." grammar.md §6 ends with check "8. No template scaffolding survives…".
**Fix:** Replace "all seven checks" with count-free wording ("every check in the list") so the number cannot rot again.

**M2 — {where: README.md §Invoke, severity: major}**
**Issue:** An exemplar **name** — first item on exemplars.md's identifying-facts list — appears inline in binding text (change_rule §5 rule 3 counts README as binding), and README is not on the eval exclusion list. "feedler" resolves to a public GitHub repo — the L1 answer key.
**Evidence:** README.md: "/specai new product **feedler2** — ideation at ./my-idea.md, target ../**feedler2**/" and "/specai evaluate **feedler**". SKILL.md §2 already shows the clean form: "`evaluate <exemplar>`".
**Fix:** Neutralize the README examples: `/specai new product <name>` and `/specai evaluate <exemplar>`.

**M3 — {where: reference/exemplars.md §3 rule 4, severity: major}**
**Issue:** The eval integration-proof exit criterion cites a DoD line that neither the template nor the grammar puts in §6. Independent verification lives in start.md §4; §6 imports only "the QA layers (§4)", and grammar §4.3's "always includes" list for §6 has no independent-verification item. An emitted repo built exactly from the template has no such line, so rule 4's exit is unsatisfiable as written.
**Evidence:** exemplars.md §3 rule 4: "The proof's exit is the emitted repo's own §6 Definition of Done **including its independent-verification line**…" Versus templates/start.md §6 and grammar §4.3's always-includes list — neither carries one.
**Fix:** Add an explicit §6 DoD item to templates/start.md ("independent verification per §4 returned PASS for this target") and mirror it in grammar §4.3's always-includes list.

## MINOR

**m1 — grammar.md §5 Verification row:** "1–2 verifier focused runs" disagrees with change_rule §4's "one fresh verifier" focused pass. Fix: "focused passes per `change_rule.md` §4".
**m2 — phases/definition.md step 4:** "At tier M add a risk-focused round" reads M-only; dial §2's cumulative L cell inherits it. Fix: "At tier M/L".
**m3 — verification_core §6 rule 4 vs SKILL.md §5:** two owners for the taxonomy-seed append with different content (absorbing taxonomy lines back duplicates prior entries). Fix: SKILL §5's distill-from-this-run's-records is the sole append; VC §6.4 cites it.
**m4 — grammar.md §4 legend vs §4.2:** "(dial) marks parts that appear only at higher tiers (§5)" contradicts the dimension-keyed money section. Fix: "(dial) marks parts gated by `dial.md` — by tier (§5) or by dimension (§1 rule 2)".
**m5 — "checkpoint" carries two meanings** (the phase-1 question round vs operator gates in definition.md §Gate and dial §3). Fix: reserve "checkpoint" for the question round; say "gate(s)" elsewhere.
**m6 — SKILL.md §2 evaluate row:** the hygiene summary omits the headline exclusion (the target exemplar repo itself). Fix: add "target exemplar off-limits".
**m7 — exemplars.md §3 rule 6:** the eval preamble sweeps only IOUs; change_rule §5 rule 3 mandates the exempted-edit bundle there too. Fix: add the bundle to rule 6.
**m8 — dial.md §2:** the interposed "(Design-first ordering…)" parenthetical splits the table; rows from "| Emitted process docs |" render headerless. Fix: move it below the table.
**m9 — phases/definition.md Inputs + step 1:** fixture-domain echoes ("a feed reader implies unread counts, folders, keyboard nav"; the brain-dump reference class). Fix: swap to a non-fixture domain ("a to-do app implies due dates, reordering, completion states") and generalize.
**m10 — verification_core §2 rule 4:** "the eval-comparison brief (`reference/exemplars.md` §3) — verbatim from its owning section" — exemplars §3 never delimits a brief; extraction requires discretion. Fix: add a fenced "Comparison brief (verbatim)" block to exemplars.md §3.
**m11 — phases/delta.md §Inputs vs SKILL.md §3:** run-dir freshness pinned twice, differently; the uncommitted-old-dir case is unspecified. Fix: one owner — delta cites SKILL §3; SKILL §3 covers the uncommitted case.

## Categories with nothing found (checked, not padded)

Tier thresholds; verifier counts per seal tier (cross-cited both ways); gate schedule (tempo) and spot-verify schedule (all match); canonical terms from SKILL §0's list (each single-defined; the only overloaded term found is "checkpoint", not on the canonical list); engineering-standard ownership chain (grammar §4.7 ↔ style §1 ↔ template all defer to the template; "phase 3 writes it in every case" agrees across three files); DRIFT.md dual-home (deliberate, documented, currently in sync); NOTES.md honesty — every checkable recent claim resolved against the tree **except** its round-3 claim that "the quarantine completed", which B1/M2/m9 refute; the open round-3 IOU is recorded, consistent with change_rule §5 rule 4.
