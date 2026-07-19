# Blind re-verification round 2 — lens 2: executability/buildability (verbatim report)

*Preserved verbatim per `verification_core.md` §6 rule 4 (received via agent relay; the run lead
performed no edits beyond this header). Dispatcher: the operator by standing order ("go"); lead as
mechanical proxy. Package: the full tree minus `verdicts/` and `.git`.*

---

**DISCLOSURE — ambient context beyond the prompt and the listed files:** the harness system prompt injected: working directory + platform info, a git status snapshot including recent commit subjects ("verdicts and review", "adding the concept of drift", "specai: initial release" — mild history leakage), the user's email, today's date (2026-07-17), a scratchpad path, and tool/skill listings. No CLAUDE.md or memory-file content was injected. I read exactly the 21 scoped files; I did not open `verdicts/`, `.git`, or anything outside the repo.

# Lens verdict: **FAIL** (0 blockers, 5 majors, 9 minors)

Walk results in one line each:
1. Full `new product`, tier S: executes end-to-end; every S-tier working file has a producer before its consumer (inventory→P1, slices/gaps→P2/P4, consumer-ledger→P3, notes-seed→P1, verdicts→P6). Checkpoint answers reach component authors via inventory fold→slices, and reach seal verifiers via emitted NOTES — clean.
2. Full `new product`, tier L: blocked by M-1 (taxonomy has no legitimate producer) and M-5 (required tier-L artifact classes with no defined shape).
3. Regulatory/money = 2 at mid tier: the machinery is reachable (checkpoint round, REG register, architecture §7b, top-tier change gating all fire off the dimension) — but the adjacent case, tier L with reg/money ≤ 1, produces a register with no consumer (M-3).
4. Crash-resume: holds — every phase output is a file, DRAFT status marks in-flight specs, gate approvals land in the notes-seed (weakly, see m-8).
5. Delta engagement: walks cleanly except the verifier package is undeclared (M-4). Eval route: walks cleanly except m-6.
6. Emitted-repo operability: an instantiated start.md routes every §2 command through the boot table; the emitted tree is self-contained (DRIFT rules inline in §3B, notes template cites start.md §3 not grammar, all blockquoted specai-tree citations are deleted at instantiation) — modulo m-4/m-5.

## MAJOR findings

**M-1 · verification_core.md §2 rule 1 + §3 + SKILL.md §3 · major**
**Issue:** `<run-dir>/taxonomy.md` (tier L, part of the declared verifier package) has no legitimate producer, no defined entry shape, and two contradictory handling rules.
**Evidence:** §2 rule 1: "a standing defect-pattern list distilled **mechanically from prior verdict records** … kept at `<run-dir>/taxonomy.md` … passed unchanged — never selected or edited per review, and **never written by the artifact's author**". But SKILL.md §3 makes it one of the run dir's "named working files" the run (i.e., the lead — who authored vision/inventory/architecture, artifacts under seal review) creates. And §3 of the same file says the opposite of "passed unchanged": "prior learnings travel only as distilled patterns (taxonomy/lens seeds, **curated by the dispatcher** per §2 rule 1)". No document defines the "mechanical" distillation procedure or what a taxonomy entry looks like.
**Fix:** name the producer explicitly (e.g., "the operator, or the lead running a stated mechanical procedure exempt from the author ban"), define the entry shape (pattern → source verdict → lens it arms), and reconcile "curated by the dispatcher" with "never selected or edited per review".

**M-2 · verification_core.md §2 rule 4 vs §4/§7 and phases/verification.md · major**
**Issue:** the conforming-brief definition makes every judgment-gate dispatch non-conforming — the rule is unsatisfiable exactly as written, at every tier.
**Evidence:** rule 4: "A conforming brief is exactly: the **§5 lens row verbatim** + the §6 finding shape and PASS rule + the file package — **nothing else**." Yet §4 (tier S): "**1** fresh verifier running all applicable lenses (**carrying the judgment-gate brief** as its own verdict section)", and phases/verification.md: "at tier S the judgment-gate brief **folds into the single verifier's dispatch**". The judgment gate (§7) is not a §5 lens row and has no templated brief home, so the S dispatch violates "nothing else" and the M/L judgment context receives a brief rule 4 doesn't license.
**Fix:** either add the judgment gate as a §5 row (its §7 text as the templated brief) or amend rule 4 to "the §5 lens row(s) and/or the §7 judgment brief verbatim".

**M-3 · phases/definition.md output 3 + phases/architecture.md steps 4/8 + grammar.md §4.2 · major**
**Issue:** at tier L with regulatory/money scoring 0 or 1 (e.g., 3+2+2+1+1 = 9 → L), the regulatory register is mandatorily produced but its only named consumer never exists, and the assignment step skips it — REG-lines dangle.
**Evidence:** definition.md: "**REG-n the regulatory register (at tier L, or whenever regulatory/money scores 2** …): … phase 2 maps every REG-line to an enforcing component or principle in architecture's Money & compliance section". But that section exists "**only when regulatory/money scores 2**" (architecture.md step 8; grammar §4.2 "whenever regulatory/money scores 2"), and architecture.md step 4 assigns only "**every inventory line (R/S/U/C/X)**" — REG is not in the list. The coverage lens ("every requirements-inventory line traces to a binding clause") would then FAIL the seal for lines the process gave no landing home.
**Fix:** either emit REG-lines only when reg/money = 2, or add REG to step 4's assignment list with a non-money home (mapped to enforcing components/principles even without a §7b).

**M-4 · phases/delta.md step 6 vs verification_core.md §2 rule 4 · major**
**Issue:** delta verification declares no verifier input package, but dispatch legitimacy requires the package to be "the phase file's input list" and forbids lead discretion — so a delta seal cannot be legitimately dispatched as written.
**Evidence:** delta.md step 6 says only "Fresh-context verifiers scoped to the delta plus every document the cascade touched … lenses per `verification_core.md` §5: change-request coverage…" — no package (does the verifier get `change-request.md`? `inventory-delta.md`? NOTES? the ideation? the full tree?). Rule 4: "receives the **declared input package** (the phase file's input list — **never a hand-picked subset**)" and grants the lead "**zero discretion** over what the verifier sees". The change-request-coverage lens needs "every line of the change request + delta inventory" — files no declared package delivers.
**Fix:** add an explicit verifier-package list to delta.md step 6 (updated repo + `change-request.md` + `inventory-delta.md` + delta slices + cascade-set documents + lens briefs + style/grammar), mirroring phases/verification.md's package paragraph.

**M-5 · dial.md §2 + grammar.md §5 vs contracts.md and grammar §4.11 · major**
**Issue:** tier L mandates artifact classes whose shape exists nowhere in the tree — a tier-L run lead (and especially the L4 eval, which excludes `reference/exemplars.md`) must invent them; modality also conflicts across documents.
**Evidence:** dial.md §2 L contracts row: "full hierarchy walk, versioned standards, **conformance suite spec**" (unqualified) vs contracts.md: "tier L **may** add a conformance-suite spec"; dial.md §2 L process-docs row adds "**ops standards**"; grammar §5: "separate + **infra/ops specs**" and "**agent standards** when the product is AI-operated". None has a template or a §4.11-style category shape — contrast grammar §4.11's deliberate fix for develop_loop/studio: "Neither has a full template; these category shapes are their grammar, **self-sufficient without any exemplar**." The only instances live in the private exemplar, off-limits during the very L4 eval meant to exercise tier L.
**Fix:** give conformance-suite / ops-infra / agent standards the §4.11 treatment (a paragraph-length category shape each), and align contracts.md's "may" with dial §2's unqualified listing.

## MINOR findings

**m-1 · SKILL.md §3 + §5 · minor** — `journal.md` is a named working file with no producer, content rule, or cadence anywhere in the phases; its only defined use is registrar disclosure ("disclosed in `<run-dir>/journal.md`"). Fix: one sentence in SKILL.md §3 stating who writes it (the run lead, per phase transition/gate/dispatch) and what it minimally records.

**m-2 · verification_core.md §6 rule 4 · minor** — the discard branch names a destination that doesn't exist: "`taxonomy.md`'s distilled patterns are absorbed into **a committed record**" — which record, if the run's verdict record was just discarded? And "for the skill itself" is `verdicts/`' declared scope (SKILL.md §1), leaving product-run records without a named durable home once the run dir is deleted. Fix: name the destination (e.g., the emitted repo's committed `.specai-run/verdicts/`, archived not deleted).

**m-3 · phases/architecture.md step 9 · minor** — "(its testing floor is completed at phase 5 — `phases/contracts.md` outputs)" points the "phase 5" claim at the phase-3 file; a fast reader maps contracts=phase 5. Also phase 2 must write "one line citing whichever home applies" before phase 3 has decided inline-vs-separate. Fix: cite `phases/emission.md` output 7 for the completion, and let phase 3 own writing/correcting the citation line.

**m-4 · templates/start.md §1 step 3 · minor** — "diff it against the spec — that tells you whether you are in case A, B, or C (§3)": the diff distinguishes A from B; case C is determined by the command, not the diff. Fix: "case A or B; a plain-language request is case C regardless".

**m-5 · templates/start.md §6 · minor** — "run manifest for verifiers (M/L)" is an undefined term nowhere else in the tree; the emitter must guess what to instantiate. Fix: define it in the blockquote (what ran, versions, how to reproduce — the verifier's §2-rule-5 input).

**m-6 · reference/exemplars.md §3 rule 2 · minor** — "The *other* exemplar remains readable, as in a normal run" is unactionable: this file is "the **only** home of the exemplars' identifying calibration facts" and is excluded whole, so the run cannot know what/where the other exemplar is. Fix: let the operator stage the other exemplar's pointer alongside the ideation, or drop the sentence.

**m-7 · phases/verification.md fix loop + phases/component_specs.md integration step · minor** — "route… to its isolated author-context" assumes a persistent context; subagent transcripts don't survive (SKILL.md §4 acknowledges this). The intended meaning — a fresh context with that component's same closed input list — is never stated. Fix: say exactly that.

**m-8 · phases/architecture.md / contracts.md gates · minor** — neither M/L gate says where its approval is recorded; only phase 1's notes-seed description ("checkpoint answers, dial justifications, **gate approvals**") implies the home. Crash-resume of gate state hangs on that implication. Fix: one clause per gate: "approval recorded in the NOTES seed".

**m-9 · phases/verification.md pass 2 vs verification_core.md §6 rule 4 · minor** — "S = 1 verifier, all lenses; M = 2, split, **verdict record**; L = panel ≥3 … + **verdict record**" reads as if tier S writes none, contradicting "**Every** seal writes a verdict record". Fix: drop "verdict record" from the M/L items (it's universal) or add it to S.

**What held up under attack:** the producer-before-consumer chain for every S/M working file; checkpoint-answer plumbing (ideation → inventory → slices → specs, and → NOTES → seal verifiers); the crash-resume claim; emitted-repo self-containment (no emitted document depends on a specai-only file after blockquote deletion); the DRIFT lifecycle; and the eval route's target-exclusion mechanics.
