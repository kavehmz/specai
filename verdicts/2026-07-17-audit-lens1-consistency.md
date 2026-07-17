# Post-seal audit — lens 1: consistency/contract (verbatim report)

*Preserved verbatim per `verification_core.md` §6 rule 4. Post-seal audit round, dispatched at the
operator's invitation over the sealed tree (d86eec3). Package: the tree minus `verdicts/`/.git.*

---

**DISCLOSURE — ambient context beyond this prompt and the listed files:** the harness system prompt (env/git status, tool and skill listings) and a system-reminder carrying the user's email and today's date. Nothing else was read.

# VERDICT: FAIL — 0 blockers · 4 majors · 4 minors

**MAJOR 1 — Comms-matrix arrival tier contradicts across grammar §4.2 / grammar §5 / dial §2; grammar §5's L cell is a garbled enumeration.** grammar §4.2 and dial §2 put the comms matrix at M/L; grammar §5's cumulative Coverage row omits it at M and introduces it at L ("+ matrices and comms matrix, maintained"). Fix: M cell "+ explicit coverage matrix + comms matrix in architecture"; L "+ both matrices, maintained".

**MAJOR 2 — Design-spec binding enumeration restated by the template disagrees with its owner (drops "motion intent"), and the template is the author's only source.** grammar §4.6 lists five binding items; templates/component_spec.md restates four. The design author's closed input list never includes grammar.md — rework by construction. Fix: add motion intent to the template (or make the template the owner).

**MAJOR 3 — phases/architecture.md's procedure cites reference/exemplars.md, but its closed Inputs list doesn't declare it** (steps 3 and 5 vs Inputs; SKILL §0's "each phase file names all it may read"). Fix: declare it as optional calibration with the eval carve-out, as emission does.

**MAJOR 4 — Delta spot-verifies assign change-request coverage but never hand the verifier the change request.** The lens's sources are dual (change request + delta inventory); step 1 names only the delta inventory, step 2's substitutions never map in `<run-dir>/change-request.md` (the step-6 seal substitution shows the mapping exists and was omitted here). A request line dropped before the delta inventory is exactly the laundering the dual-source lens exists to catch. Fix: add change-request.md to both spot packages.

**MINOR 1** SKILL §3's delta parenthetical omits `gates/*-delta/` and the delta slices. **MINOR 2** delta's relocation claim for change-request.md exceeds §6.4's named set. **MINOR 3** §2 rule 1's "sees only" list doesn't license the phase-6 package's extras — defer to rule 4's declared package. **MINOR 4** SKILL §0's second "gate" sense re-seeds the corrected letter ("whose verdict must return" — §5.4 requires *closing*).

**Clean:** canonical terms; pinned values (incl. M-split totality); ownership seams; the three seal paths mutually consistent at seal level; IOU letter + collectors; quarantine (no identifying facts outside exemplars.md; README generic); maps match the tree; no other malformed sentences.
