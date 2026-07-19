# Blind re-verification round 2 — lens 4: judgment gate + adversarial (verbatim report)

*Preserved verbatim per `verification_core.md` §6 rule 4 (received via agent relay; the run lead
performed no edits beyond this header). Dispatcher: the operator by standing order ("go"); lead as
mechanical proxy. Package: the full tree minus `verdicts/` and `.git`.*

---

**DISCLOSURE — ambient context beyond this prompt and the listed files:** my session carries harness-injected context: the working directory path, a git status block naming the current branch and five recent commit subjects (e.g. "verdicts and review", "adding the concept of drift"), a scratchpad path, a user email, today's date, and a list of unrelated installed skills/tools. No CLAUDE.md or memory-file content was injected. I read nothing outside the listed files; the commit subjects gave me no finding I did not derive from the files themselves.

**Dog-food checks requested:** the ledger and the binding docs agree — I traced all six D1–D6 resolutions in NOTES to landed text (D1→`change_rule.md` §5.1–2, D2→`dial.md` §1.2, D3→`verification_core.md` §2.4, D4→`templates/vision.md` §9–10/`grammar.md` §4.1, D5→`reference/exemplars.md` §3, D6→`style.md` §1/`grammar.md` §4.7). Nothing binding lives only in a record, with two exceptions found below (the eval answer key leaking *out of* records into binding docs is the blocker; the round-2 deferral is the IOU major). The ledger's honesty itself holds up.

# LENS VERDICT: **FAIL** — 1 blocker, 10 majors, 3 minors

## BLOCKER

**B1 — The eval answer-key quarantine is false: binding, mandatory-read documents carry the exemplars' identifying facts inline, directly contradicting the quarantine claim.**
- **where:** `reference/exemplars.md` (preamble) vs `standards/grammar.md` §3 + header, `templates/contract_standard.md`, `templates/component_spec.md`, `templates/notes.md`
- **issue:** The eval protocol's enforceability rests on one claim: exemplars.md is the only home of identifying calibration facts. That claim is false four times over, in files an eval run **must** read: grammar.md §3 rule 2 ("feedler's export ↔ api_contract split is the pattern"); grammar.md's own header asserting the opposite of its §3; templates/contract_standard.md ("feedler's `api_contract.md` (tier S, one seam)"); templates/component_spec.md ("feedler's `export_spec.md`" — the caveat governs *reading the file*, not the fact printed in the template itself).
  **Constructed attack:** run `evaluate feedler` fully conformantly — never open the feedler repo, never open exemplars.md. From mandatory reads alone the run learns: target is tier S, one API contract seam, has an export component that defers a shared surface to the api_contract. The comparison verdict is then contaminated while certified clean — a wrong outcome produced by following the rules exactly.
- **fix:** Strip every exemplar name/tier/shape from `grammar.md` §3, `templates/contract_standard.md`, `templates/component_spec.md`, and `templates/notes.md` (cite `reference/exemplars.md §1/§2` anonymously, as `templates/engineering_standard.md` and `verification_core.md` §8 already correctly do). Then grammar's header claim becomes true.

## MAJOR

**M1 — The eval run is not barred from `NOTES.md`, which carries the dial answer key and the L1 grading rubric.**
- **where:** `reference/exemplars.md` §3 rule 2; `NOTES.md` founding decision 5 and the L1 entry
- **issue:** Rule 2 excludes the target's repo/specs/notes and exemplars.md — not specai's own ledger. But an eval run is "a normal `new product` run", and SKILL.md §0 routes every run to NOTES. NOTES carries "Calibration: feedler=2/S, the trading platform=10/L" (the exact dial answers for **both** eval fixtures) and the L1 entry's component count, capability deltas, and the exact axes a prior comparison panel rewarded. **Attack:** the eval run reads the L1 entry and optimizes for the rewarded axes — the operator-dispatched panel then scores EXCEEDS.
- **fix:** Rule 2 adds specai's `NOTES.md` (and any prior emitted candidate repo named in it) to the eval run's excluded set; the eval run needs no factory history.

**M2 — Checkpoint answers and inventory lines have no integrity anchor: the phase-6 coverage lens verifies against artifacts the run itself can silently curate after the gate.**
- **where:** `phases/verification.md` §Pass 2 (package); `verification_core.md` §5; `phases/definition.md` §Gate
- **issue:** The lens checks coverage against the inventory and checkpoint answers, but the verifier package omits `notes-seed.md`, and no snapshot of the gate-approved inventory exists. **Attack:** the operator answers a checkpoint question; the tree fails to honor it; the lead deletes that line from `inventory.md` and the seed before phase 6 — coverage passes on the curated inventory.
- **fix:** Add `notes-seed.md` to the phase-6 verifier package (it is a gate artifact, not "phase working notes"), and freeze the gate-approved inventory + seed at the phase-1 gate (a copy or hash recorded in the journal) so post-gate curation is diffable at the seal.

**M3 — Coverage misses can be laundered into `vision.md` as fix-loop "revisitable" non-goals: no reverse-provenance check, and no explicit re-gate.**
- **where:** `verification_core.md` §5; `phases/verification.md` §Fix loop; `templates/vision.md` §9
- **issue:** The lens passes any line tracing to a revisitable non-goal, but nothing checks the reverse direction, and nothing states that a fix-loop edit to vision.md re-triggers phase 1's operator gate. **Attack:** the coverage lens FAILs on a missed ask; the lead appends a revisitable non-goal to vision.md; a fresh verifier (blind to the prior report) sees a legitimately recorded cut.
- **fix:** (a) The coverage lens gains the reverse check: every **revisitable** non-goal traces to an X-line or a recorded checkpoint answer, else FAIL. (b) Fix-loop edits to gated artifacts re-trigger the owning phase's operator gate, or at minimum are presented as a diff at the seal.

**M4 — Mid-run spot-verifies have no enforcement surface: nothing records that they ran, so skipping them is invisible at the seal.**
- **where:** `dial.md` §2 (last row); `verification_core.md` §3, §6
- **issue:** The schedule mandates fresh verification mid-run at M/L, but verdict records exist only per seal. A tier-L run that skips all three spot-verifies is indistinguishable at seal time from one that ran them — a rule "violations nothing would ever catch."
- **fix:** Each spot-verify writes a one-page verdict record in the run dir; the seal presentation enumerates them — an absent record blocks like an unpaid IOU. State what a spot-verify FAIL does.

**M5 — The derived cascade set can be shrunk by omitting citations: the focused pass never sees the document a change contradicts.**
- **where:** `change_rule.md` §3–§5; `grammar.md` §6 check 2
- **issue:** The citation graph is authored by the same author: check 2 verifies citations **resolve**, never that necessary citations **exist**. **Attack:** edit doc A to contradict doc B; A cites B nowhere; the derived set excludes B; the focused verifier cannot see the contradiction.
- **fix:** For specai self-changes the focused-pass package includes the full `standards/` + `SKILL.md` set as context; generally, derive the set bidirectionally — documents the artifact cites, documents citing it, and documents defining any term the diff touches.

**M6 — Taxonomy mechanics are incoherent twice: the sourcing loop is broken, and mid-loop curation collides with the author-exclusion rule.**
- **where:** `verification_core.md` §2 rule 1, §3, §6 rule 4; SKILL.md §1 map
- **issue:** (a) The factory taxonomy is seeded from `verdicts/` — which holds only skill-review records; product-run verdicts live in other repos and never reach it, so the taxonomy can never learn product-run defect patterns. No distillation procedure is defined. (b) §3's "curated by the dispatcher" collides with rule 1's "never selected or edited per review" while rule 4 makes the lead (the author) the normal dispatcher.
- **fix:** Define distillation as a mechanical transform (one line per closed blocker/major: lens · pattern · source record); route each product run's distilled patterns into a committed factory-side file at run close; when dispatcher = author, restrict additions to verbatim finding-category lines or require operator sign-off.

**M7 — Injection disclosures and independence facts can quietly vanish: "committed" verdict records live inside a directory the run is licensed to delete.**
- **where:** SKILL.md §3; `verification_core.md` §6 rule 4; `templates/notes.md` §Seal
- **issue:** Records live in the run dir; SKILL.md §3 says the dir "is deletable after the seal" while records "default to committed." The commit-then-delete path — both explicitly permitted — leaves the working tree recordless and the ambient-injection disclosures surviving only in git history. A disclosure that requires archaeology is a vanished disclosure.
- **fix:** Before run-dir deletion, verdict records relocate to a durable committed path; the NOTES seal line cites the final path; §6 rule 4 states the relocation rule.

**M8 — The typo/clarity exemption is an author-adjudicated bypass of the self-change gates, including on the self-governing surfaces.**
- **where:** `change_rule.md` §4, §5 rule 3
- **issue:** §5 keys weight to the target document, then rule 3 keys an exemption to the edit's claimed **nature**, adjudicated by the author, checked by no one. **Attack:** reword `verification_core.md` §6's PASS rule "for clarity" in a way that shifts meaning; no gate fires.
- **fix:** On §5 rule 2's self-governing surfaces, no exemption — any diff takes the focused pass. Elsewhere, exempted edits accumulate in a bundle enumerated at the next seal/eval preamble.

**M9 — The tree is currently living inside an un-IOU'd deferral: round-2 fixes are landed with the confirming gate pending, and rule 4's trigger is too ambiguous to catch it.**
- **where:** `change_rule.md` §5 rule 4; `NOTES.md` final entry
- **issue:** The final ledger entry lands round-2 fixes with the confirmation "dispatched and pending" and no rule-4-form IOU. Either this violates rule 4, or "cannot run before landing" doesn't cover dispatched-but-unreturned gates — in which case any change can land the moment its verifier is *launched*, gutting the pre-landing gate.
- **fix:** Define "the gate has run" as "the verdict is returned"; whenever landing precedes the verdict, an IOU is mandatory (this very state should carry one).

**M10 — Verdict-record authorship is unspecified and raw verifier reports need not be preserved: everything the operator countersigns is filtered through the party under judgment.**
- **where:** `verification_core.md` §6 rule 4; `phases/verification.md` §Pass 2, §The seal
- **issue:** §6 rule 4 lists minimum content but never who writes the record; the lead dispatches, receives, dedupes, compiles, and presents. Nothing requires the verifiers' reports verbatim anywhere. **Attack:** downgrade a repeat major to a "new minor" in the dedup; no artifact exists to contradict the compilation.
- **fix:** Each verifier's report is preserved verbatim as a run-dir file named in the verdict record; the lead's dedup/resolution log cites, never replaces, them; the seal presentation links the raw set.

## MINOR

**m1 — `grammar.md` §6 has no check for leftover template scaffolding.** Fix: add check 8 (no angle-bracket placeholders, no template authoring notes, outside fenced examples).

**m2 — The eval integration proof names no grader.** Fix: the proof's exit is the emitted repo's own §6 DoD **including its independent-verification line**, with evidence attached to the comparison verdict.

**m3 — Phase 5's input list doesn't cover what its own procedure cites.** `templates/engineering_standard.md` absent from emission's declared inputs while output 7 completes its §11. Fix: add it.

**Judgment summary (the half that isn't findings):** the core design is genuinely good and would be lived by — the phase cuts by information boundary, the quality cell defined once, the dial's proportionality, the DRIFT three-tenses split, and templates that teach rather than route are the strongest parts; the ledger is honest to a fault. The systemic weakness is concentrated, not diffuse: nearly every major above is the same disease — **the run lead is author, dispatcher, relay, dedupe judge, record-writer, and run-dir custodian, and the tree keeps answering this with more lead-maintained paperwork instead of operator-visible, tamper-evident surfaces** (snapshots at gates, verbatim reports, durable records, enumerable collectors). D3 chose lead-dispatch deliberately; these findings are the residue that choice must now pay for. The eval protocol, hardened twice, is still contaminated by its own history files — B1/M1 must land before L4, or the L4 verdict will be unusable.
