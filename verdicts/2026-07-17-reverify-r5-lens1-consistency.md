# Blind re-verification round 5 — lens 1: consistency/contract (verbatim report)

*Preserved verbatim per `verification_core.md` §6 rule 4. Dispatcher: the operator by standing
order; lead as mechanical proxy. Package: the full tree minus `verdicts/` and `.git`.*

---

**DISCLOSE:** Ambient context injected beyond this prompt and the listed files: a system-reminder carrying a user email and today's date, an environment block (cwd, platform, git status/log lines), and the harness tool/skill listings. None influenced findings. I read exactly the scoped files; nothing in `verdicts/`, `.git`, or outside the repo.

# VERDICT: FAIL — 1 blocker, 4 majors, 8 minors

## BLOCKER

**1. The delta seal's declared verifier package contradicts the verifier checks and taxonomy rule it imports.** delta step 6 says the phase-6 machinery applies in full ("the seal-presentation sweeps, and its fenced Verifier checks all apply") then declares a package omitting `standards/dial.md` §2 (check 2 needs it), specai's `NOTES.md` (check 3), `templates/`, and the tier-L taxonomy (§2 rule 1) — a delta-seal verifier either fails its mandatory checks or receives undeclared files; both horns break a binding rule. And check 2's derivation is wrong for deltas: the schedule keys to full-run phases while delta runs "affected phases only" — the expected count over-counts and manufactures a false finding. Fix: declare the delta package as the phase-6 package plus/minus named delta substitutions; add a delta derivation rule for check 2 (expected records = phases actually run).

## MAJOR

**2. Verifier check 1 names artifacts that do not exist on the delta path** (sealed vision/inventory/NOTES seed vs delta's inventory-delta.md, no seed, gates/*-delta/). Fix: a delta mapping line.
**3. The architecture delta's operator gate has no gate-copy** — step 2 ends "Operator gate at M/L." with no copy instruction while steps 1/3 and the main path all name theirs; check 1 has no baseline to diff. Fix: add gates/architecture-delta/.
**4. The tier-L taxonomy assembly rule directs an eval run into `verdicts/`**, and the staging override lives only in exemplars.md, which the run may not read — two contradictory readable instructions, no readable resolution. Fix: eval carve-out in §2 rule 1 itself.
**5. `phases/emission.md` mis-scopes the eval exclusion** ("the eval target is off-limits" vs rule 2's whole-file + NOTES + verdicts/ exclusion) — a mid-eval lead reading emission is licensed to open exemplars.md so long as it avoids the target. Fix: rephrase to whole-file exclusion.

## MINOR

6 unclosed parenthesis + "—," artifact in phases/verification.md's package sentence. 7 exemplars preamble overstates "only home" (NOTES also carries fixture facts) — say "only home in binding documents". 8 SKILL §3's "neither this file nor the phase files restate it" is false (verification.md restates the fix-loop clause and PASS rule) — soften. 9 delta hard-codes the gate cadence dial §3 owns — cite. 10 contracts declares inputs §4.4/§4.7 but owes a §4.11 duty — add. 11 grammar §6 check 1 gives DRIFT a carve-out but not the conditional verdicts/ dir — add. 12 grammar §4.3's command summary omits `new` — align. 13 the spot-record naming convention exists only in the fenced check — move to §4.

## CLEAN

Eval-exclusion invariant across binding docs: **holds** — only licensed tier-neutral role references; the exclusion list identical in rule 2, SKILL §2, and the fenced prompt. Canonical terms all single-meaning. Pinned values agree everywhere with a named owner. Ownership seams clean (engineering-standard enumeration, command list, boot-table exemptions, §6 counts, verifier counts vs schedule). Identity/revisitable consistent across six homes. DRIFT lifecycle consistent across all homes. IOU letter: pay-by-closing + three collectors agree; degraded-seal IOU matches; "evals never run degraded" identical in both homes. Money trigger dimension-keyed consistently everywhere.
