# Blind re-verification round 2 — lens 3: altitude/style (verbatim report)

*Preserved verbatim per `verification_core.md` §6 rule 4 (received via agent relay; the run lead
performed no edits beyond this header). Dispatcher: the operator by standing order ("go"); lead as
mechanical proxy. Package: the full tree minus `verdicts/` and `.git`.*

---

# Lens verdict: altitude / style — **FAIL**

**Disclosure of ambient context:** my session carried a system prompt with environment info (cwd, platform), a git-status snapshot including recent commit titles ("verdicts and review", "adding the concept of drift", …), the user's email, today's date, and harness tool/skill listings (Slack, artifacts, MCP instructions). No CLAUDE.md or memory-file content was injected. I did not open verdicts/, .git, or anything outside the listed files; the commit titles were visible to me but are not used as evidence below.

Expectations were derived from `standards/style.md` (the altitude law, the eleven working rules, the tone rule).

## Blocker

**B1 — Exemplar answer-key facts sit inline in binding documents, falsifying the quarantine declaration that makes the eval protocol enforceable.**
- **where:** `standards/grammar.md` §3; `templates/contract_standard.md` header note; `templates/component_spec.md` header note; `phases/emission.md` procedure step 2
- **severity:** blocker
- **issue:** `reference/exemplars.md` declares, bindingly: *"This file is the **only** home of the exemplars' identifying calibration facts — names, tiers, sizes, dial breakdowns, decomposition shapes, signature principles. Binding documents cite this file and never carry those facts inline (that is what makes §3's target-exclusion rule enforceable: excluding this file removes the answer key)."* Four binding files carry exactly such facts inline:
  - `grammar.md` §3: *"feedler's export ↔ api_contract split is the pattern"* — name + decomposition shape, in the one document read on **every** run.
  - `templates/contract_standard.md`: *"Reference instances: feedler's `api_contract.md` (tier S, one seam)"* — name + tier + seam count.
  - `templates/component_spec.md`: *"feedler's `export_spec.md` (`reference/exemplars.md`) — it is NOT part of a phase-4 author's closed input list"* — the caveat does not unload the fact; this template **is** in every phase-4 author's declared inputs (`phases/component_specs.md` §Inputs), so every L1-eval component author reads a target component name.
  - `phases/emission.md`: *"the discipline lives inline in start.md §4, feedler-style"*.
  An L1 eval ("reproduce feedler") excludes exemplars.md per its §3 rule 2, yet grammar.md, the templates, and the phase files are necessarily in the run's read set — so the answer key leaks anyway. exemplars.md §3 states *"an eval that violates these proves nothing"*: as written, every L1 eval run per protocol is simultaneously required-clean and necessarily-contaminated. Two binding documents directly contradict each other about a load-bearing enforcement mechanism — the definition of a contradictory outcome.
- **fix:** scrub exemplar names and identifying facts from all four locations; replace with role language plus a citation (e.g. grammar §3: "a component may cite a sibling for a shared surface it explicitly defers to, named in its 'Not this spec' header — the pattern instance lives in `reference/exemplars.md` §1"; templates: "Reference instances: `reference/exemplars.md`", the form `templates/start.md` and `templates/engineering_standard.md` already use). Same treatment for emission.md ("inline in start.md §4, per the tier-S reference in `reference/exemplars.md`").

## Major

**M1 — The conforming-brief definition excludes the judgment-gate brief that tier S is required to include.**
- **where:** `standards/verification_core.md` §2 rule 4 vs §4 (S row) and `phases/verification.md` §Pass 2
- **issue:** §2 rule 4 binds: *"A conforming brief is exactly: the §5 lens row verbatim + the §6 finding shape and PASS rule + the file package — nothing else."* The judgment gate (§7) is not a §5 lens row. Yet §4's S row mandates *"**1** fresh verifier running all applicable lenses (carrying the judgment-gate brief as its own verdict section)"* and phases/verification.md mandates *"at tier S the judgment-gate brief **folds into the single verifier's dispatch**"*. A tier-S seal dispatch cannot satisfy both clauses; more broadly, no tier's judgment-gate dispatch has a conforming-brief definition at all — dispatch legitimacy, the mechanism these rules exist to harden, is undefined for it.
- **fix:** amend §2 rule 4 to enumerate the judgment-gate brief as a second templated form ("the §5 lens row verbatim, **or** §7 verbatim for the judgment gate") and state that at tier S the two concatenate.

**M2 — §3 licenses per-review "curation" that §2 rule 1 forbids.**
- **where:** `standards/verification_core.md` §3 (fix loop) vs §2 rule 1
- **issue:** §3 says re-verification learnings travel as *"distilled patterns (taxonomy/lens seeds, curated by the dispatcher per §2 rule 1)"*. But §2 rule 1 defines the taxonomy as *"distilled **mechanically** from prior verdict records … passed unchanged — never selected or edited per review"*. "Curated by the dispatcher" is precisely selection/editing, and it cites the rule that forbids it. A dispatcher reading §3 alone gains license to shape what re-verifiers see — the contamination channel the whole section exists to close. ("Lens seeds" is also used nowhere else and never defined.)
- **fix:** reword §3: "prior learnings travel only as the taxonomy (§2 rule 1 — mechanically distilled, passed unchanged), never as the author's fix claims"; delete "curated by the dispatcher" and "lens seeds".

**M3 — Commit doctrine has two strengths for the same actor.**
- **where:** `standards/change_rule.md` §4 vs `SKILL.md` §0
- **issue:** SKILL.md §0 is absolute: *"**The operator commits; you never run git mutation.** The commit is the countersign."* change_rule.md §4 weakens it: *"specai and emitted-repo builders never commit **unasked**"* — which licenses committing when asked, contradicting the absolute and voiding the countersign logic (a countersign executed by the countersigned party certifies nothing). A reader of change_rule.md alone (the document that governs every modification) gets the weaker rule.
- **fix:** in §4, split the actors: "specai never commits — the operator does; emitted-repo builders never commit except under an explicit, gated standard (develop-loop Gate class)."

**M4 — The spot-verify/tempo enumeration is owned by dial.md but restated verbatim in two other binding documents.**
- **where:** `standards/verification_core.md` §4 (third table column); `SKILL.md` §3 (run diagram) — vs `standards/dial.md` §2–3
- **issue:** dial.md §2 declares ownership: *"The last row is the **spot-verify schedule** — the term other documents cite for it."* verification_core §4 then reproduces the values anyway — *"none (self-review only) / after Architecture / after Definition, Architecture, Contracts"* — excusing itself with *"cited here for completeness"*, the exact restate-with-drift-risk pattern style.md rule 2 bans ("every other document *cites* the owner, never restates"). SKILL.md §3's diagram likewise restates the tempo values dial.md §3 owns (*"[operator gate: vision + inventory + dial] (always) … [operator gate at tier M/L] … [operator gate at tier L]"*). The asymmetry proves it's avoidable: dial.md §2's own phase-6 row correctly says *"per `verification_core.md` §4 (owns the counts)"* with no values.
- **fix:** in verification_core §4, replace the column's values with "per `dial.md` §2"; in SKILL.md §3, annotate gates as "(tempo: `dial.md` §3)" without the per-tier values.

**M5 — Two documents claim ownership of the licensed-HOW enumeration.**
- **where:** `templates/architecture.md` §7 vs `standards/style.md` §1 and `templates/engineering_standard.md` header
- **issue:** style.md §1: *"§4.7 owns that enumeration and it is not repeated here."* templates/engineering_standard.md concurs: *"The licensed-HOW enumeration is owned by `grammar.md` §4.7; this template instantiates it."* But templates/architecture.md §7 asserts: *"every section of `templates/engineering_standard.md` still applies, just relocated **(that template owns the enumeration)**."* Two owners for what a reader will treat as one enumeration — and the two lists already diverge (the template adds §1 Glossary and §2 Stack as sections; grammar §4.7's owns-list says "HTTP conventions" where the template has §7 "Conventions"). One-owner-per-enumeration is the drift control; asserting a second owner defeats it.
- **fix:** in templates/architecture.md §7, replace "(that template owns the enumeration)" with "(the enumeration is `grammar.md` §4.7's; that template instantiates it)".

## Minor

**m1 — The "verbatim" change-rule quote has already drifted.** `templates/start.md` §0 renders the rule as *"Yes → the spec must change first. No → code-only fix."* while the owner (`change_rule.md` §1) reads *"Yes → the spec must change **first** (with the operator's confirmation)."* — the confirmation clause is dropped, in the very document grammar §4.3 requires to carry *"the change rule verbatim"*. Fix: restore the parenthetical or amend grammar §4.3 to "the change-rule question verbatim".

**m2 — Dated authoring history in binding text (style rule 11).** `README.md` §Lineage and `grammar.md` header. Fix: compress both to "Lineage: `NOTES.md`."

**m3 — Verification weight gates on an undefined boundary.** `change_rule.md` §4–5: "substantive" vs "clarity" never defined, and the classifier is the party who wants the cheaper path. Fix: "substantive = any edit that changes what a conforming reader would do; when in doubt, it's substantive."

**m4 — The rounding rule names a mechanism the scoring doesn't have.** `dial.md` §1 rule 1: scores are integer sums with fixed tier cut lines; nothing rounds. State the intended rule as uncertain-dimension resolution.

**m5 — Unmeasurable number in a binding step.** `phases/contracts.md` step 3: "~80% overlap" — measured how? Drop or define.

**m6 — Evaluative adjective gating an eval requirement.** `reference/exemplars.md` §3: "constitution-grade architecture". Fix: name the observable properties.

**m7 — Lens rules paraphrased where they are also cited.** `phases/verification.md` Pass 2 restates the ideation-coverage rule beside its citation. Fix: keep only the phase-specific procedure and cite the rule.

**m8 — Anonymized exemplar-shape echoes in binding standards.** `dial.md` §Status ("an eight-component platform for an RSS reader"), `phases/architecture.md` step 3 ("eight-plus components"), `phases/definition.md` inputs ("~30-line informal brain-dump"). Same drift class as B1; scrub to role language.

**m9 — One-meaning-per-sentence strain.** Worst instance: `phases/emission.md` output 2 — a single ~9-line sentence with four nested asides carrying distinct binding rules. Split it. (NOTES records this class as operator-accepted style debt — the ledger is honest about it; the debt is still real.)

**Summary:** 1 blocker, 5 majors, 9 minors → **FAIL** under the zero-blockers-and-zero-majors PASS rule. What held up under this lens: SKILL.md's terms block (glossary-first done properly), the templates' pattern-over-instance discipline everywhere except the exemplar-name notes, dial.md's phase-6 row as the model citation form, and the tree's tone — with the exceptions quoted, binding text is plain, numbered, and unpromotional.
