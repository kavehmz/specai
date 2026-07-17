# Verdict record — full standards panel over specai @ `1af9e4e` · 2026-07-17

**Scope:** the entire skill (SKILL.md, README.md, standards/*, phases/*, templates/*,
reference/exemplars.md, NOTES.md) at commit `1af9e4e`.
**Tier:** top (panel). **Dispatcher:** the operator (Kaveh), by recorded instruction; the session
lead relayed briefs as mechanical proxy. This panel pays the pre-landing gate owed by the founding
tree (2026-07-11), the delta engagement (2026-07-12), and the DRIFT change (2026-07-17).
**Panel:** four fresh-context verifiers, distinct lenses, blind to the authoring conversation and
to each other: (1) consistency/contract · (2) executability/buildability · (3) altitude/style ·
(4) judgment gate + adversarial.

**Per-lens verdicts:** FAIL · FAIL · FAIL · FAIL — zero blockers anywhere; majors below.
**Panel verdict: FAIL** (the repo's own bar: zero open majors). **Fix loop: PENDING** — deferred
by the operator to a fresh session, together with the six operator decisions in
`verdicts/2026-07-17-operator-decisions-D1-D6.md`.

Convergence note: findings marked ×2/×3/×4 were found independently by that many lenses.

---

## Consolidated MAJOR findings (deduped; lens in brackets)

Grouped; each is fixable with localized edits unless marked (design → D-packet).

### A. The practice failing to bind itself
- **A1 ×4 | change_rule.md §5** — the top-tier pre-landing gate for standards changes is not
  livable as written; three consecutive changes deferred it (recorded in NOTES). → D1.
- **A2 ×3 | verification_core.md §2 rule 4 (+ dial §2/§3, definition step 7, SKILL §4)** —
  "author never dispatches" is unsatisfiable (every mid-run spot-verify is author-dispatched by
  design) or hollow. Define dispatch legitimacy: independence = fresh context + closed package +
  fixed lens brief; lead as mechanical dispatcher; operator dispatch for the seal and
  `improve specai`. → D3.
- **A3 [4] | SKILL.md §4 + verification_core §2 rule 1** — fresh contexts are contaminated on the
  primary harness (CLAUDE.md/memory injection); the neutral-directory rule exists only as a NOTES
  "binding note for L4". Bind it in SKILL §4 for all fresh-context roles, with disclosure in the
  verdict when injection is unavoidable.
- **A4 [4] | SKILL.md §4 degraded floor + templates/notes.md seal line** — the degraded-independence
  disclosure has no durable home; add a verification-mode field (independent panel / single fresh
  verifier / degraded self-review) to the NOTES seal line; mechanical pass checks it exists.
- **A5 [4] | reference/exemplars.md §3 + templates/component_spec.md + grammar header** — the eval
  protocol is contaminated by design (target exemplar is assigned reading), self-graded, and its
  integration-proof criterion was waived at first use. → D5.
- **A6 ×2 | exemplars.md §3 L1 annotation vs NOTES** — "(Run: PASS 2026-07-11)" is unqualified
  while NOTES records the integration proof still owed. Re-scope the stamp. → D5.

### B. Verification/process mechanics
- **B1 [1] | verification_core §4 vs §6 vs dial §2** — verdict-record requirement contradicts at
  tier M (§4/dial: L-only; §6: M/L). Align (presumably to M/L).
- **B2 ×3 | change_rule §4** — "top tier" / "focused pass" for change-time verification undefined;
  define by reference to verification_core §4 rows.
- **B3 ×3 | verification_core §2 rule 1 / §3** — the tier-L factory "defect taxonomy" is a declared
  verifier input no document produces; also seed/taxonomy curation is unowned (name the dispatcher
  as curator, not the author).
- **B4 [3] | verification_core §3 + SKILL §3** — "seal" carries two meanings (per-artifact cell
  terminal vs phase-6 event); the cell read literally demands an operator countersign per artifact,
  contradicting the tempo rule; SKILL's summary restates the cell differently while forbidding
  restatement. Qualify the cell's terminal step; make SKILL cite, not restate.
- **B5 ×2 | dial §3 vs verification_core §3, SKILL §3, architecture step 9, contracts step 6** —
  "tempo" overloaded (operator-gate cadence vs spot-verify schedule); name the §2 referent
  "spot-verify schedule"; fix the §3-vs-§2 citation.
- **B6 [2] | phases/verification.md pass 2** — the judgment gate: unstated whether it is an
  additional fresh context or a brief folded into a tier's verifier count (at S: one dispatch or
  two?). State it.

### C. Run mechanics / files-as-interface
- **C1 ×2 | phases/definition.md outputs + emission inputs + SKILL §3** — the NOTES seed has no
  file path; name it (e.g. `<run-dir>/notes-seed.md`) in Definition's Outputs and SKILL §3's
  working-dir inventory.
- **C2 ×2 | SKILL §4 vs component_specs inputs** — "paths, not summaries" collides with "its
  inventory slice only"; emit per-component slice files (`<run-dir>/slices/<component>.md`) and
  cite those paths. Also [4]: "its own row of the component table" is unimplementable literally —
  authors get whole architecture.md; excluded items are sibling specs and sibling slices; say so.
- **C3 [4] | component_specs outputs** — gap reports have no file home (`<run-dir>/gaps/<component>.md`);
  the crash-resume story breaks exactly there. Optionally a draft-status convention for in-flight
  specs.
- **C4 ×2 | architecture step 8 vs contracts outputs (+ template §11)** — engineering_standard.md
  ownership contradicted ("phase 4/5 to fill" vs phase-3 output), and its §11 testing floor cannot
  be written before component specs exist; assign to phase 3, add the phase-5 (or phase-4 fan-in)
  completion step.
- **C5 [3] | README.md layout vs SKILL map** — README omits phases/delta.md (map rot); also [1]
  SKILL's map omits README.md itself. Fix both; amend change_rule §5 to cover both maps (or make
  README cite the SKILL map).

### D. External dependencies
- **D-ext ×3 | grammar header, emission inputs, exemplars §2, verification_core §8** — the ambiguity
  tiebreaker and tier-L calibration inputs are external, one private; the develop_loop "reference
  text" is external. Vendor sanitized excerpts into reference/ or demote exemplars to optional
  calibration with grammar/templates self-sufficient; state the fallback.
- **D-L ×2 | emission output 2, grammar §5, verification_core §2** — tier-L machinery (QA-officer
  pattern, taxonomy seed, studio.md, storyboards) is name-dropped but defined nowhere in this repo;
  give category-level definitions or explicitly mark "per the tier-L exemplar, where available".

### E. Dial and records (design → D-packet)
- **E1 [4] | dial §1–2 + grammar §5** — money/regulatory machinery keys to tier, not the reg
  dimension; the round-up rule can't reach a simple real-money product (scores M). → D2.
- **E2 [4] | dial §1 + phases/*** — no mid-run dial re-score path; hidden regulatory scope is
  laundered. → D2.
- **E3 [4] | grammar §4.9, templates/notes.md, dial, delta** — NOTES declared non-normative yet
  holds three normative tenants (the tier; deliberate cuts as "binding context"; delta reads it as
  binding). Missing record kind: "deliberately not yet". → D4.
- **E4 [3] | style §1 vs engineering template §§5/8 + grammar §4.7** — the "one licensed HOW" is
  claimed narrower than what the template binds. → D6.

### F. Style/altitude
- **F1 [3] | dial, verification_core, change_rule, definition, contracts, emission, delta headers** —
  systemic rule-11 violation: ai-it lineage and dated authoring status inside binding docs (worst:
  delta.md's "*Designed 2026-07-12; not yet exercised*"). Strip to NOTES pointers; NOTES already
  holds all of it.
- **F2 ×2 | style rule 9 vs grammar §5** — stable-requirement-ID rule conflicts (L-only vs
  M-optional) and cites dial.md which has no such rule; align to grammar §5, re-point the citation.
- **F3 [3] | NOTES 2026-07-11 item 7c + registrar precedent** — normative rules stored only in the
  record (neutral-dir rule → SKILL §4 per A3; registrar/orchestrator-stamp precedent →
  verification_core or SKILL §5).

## Consolidated MINOR findings (one line each)

1. delta step 3 cites a "pre-seal no-bump allowance" defined nowhere (×3) — state it in
   phases/contracts.md.
2. component_spec template orders an out-of-list exemplar read, breaking phase-4 isolation (×3) —
   make it lead-level advice or a licensed input.
3. grammar §6 check 6 is judgment, not mechanics (×3) — mark semi-mechanical; completeness belongs
   to the outcomes lens.
4. grammar §6 checks 1/6 vs boot table — README.md/start.md unreachable-from-boot-table false
   positives [2]; exempt/route them.
5. emission's `develop_loop.md` "offered S+" — no step owns the offer; no S-tier touchpoint to make
   it [2]; fold into the phase-1 checkpoint or seal presentation.
6. SKILL §3 ".specai-run absorption is what phase 6 checks" overclaims — enumerate the absorption
   checklist; state the dir's commit/delete disposition [2].
7. delta: `<run-dir>` undefined for deltas; change-request verbatim has no durable home [2].
8. architecture step 8 "inline a §6" vs template §7 numbering [2].
9. dial §2's M/L extra checkpoint rounds are carried by no phase file (×2) — anchor them to the
   M/L gates.
10. grammar §4.4 "schema change" vs contract template's broader bump trigger (shape/endpoint/
    parameter/status code) [1] — pick one breadth, repeat verbatim.
11. grammar §4.3's case-C summary omits the mandatory reshape hand-back clause [1].
12. emission's inputs omit style.md though it writes prose [1].
13. verification_core §3 "per the dial's tempo (`dial.md` §2)" mis-cite [1] (folded into B5).
14. contracts phase: product-wide constraints (operator defaults, C-lines) have no named input
    slice [4].
15. definition step 4: contradictions in the ideation are excluded from the checkpoint license
    [4] — one clause: a contradiction is always a checkpoint question.
16. consumer ledger "invaluable" yet optional and in a deletable dir [4] — make the consumers
    appendix mandatory at M/L.
17. templates/start §4 QA-layer names hard-coded; blockquote as tailorable default [3].
18. templates/start §0 "the signature formats" — exemplar ghost in a placeholder [3].
19. exemplars §3 dated run-history line duplicates NOTES [3] — keep only the pointer.
20. grammar §4.10 / verification_core §6 / start §3B — the DRIFT additions are rule-dense
    unnumbered prose [3]; number them.
21. "experience-led" gates an ordering rule but is undefined [3].
22. Tone nits: "crown", "invaluable", "proven", "catches the sloppy third" [3]; typo "the the
    trading platform" (verification_core header) [1,3].
23. Skill-wide: no canonical-terms block and no declared MUST/SHOULD/MAY convention for the
    skill's own tree [3] — add a short block in SKILL.md.

## JUDGMENT items (operator reading; no fix mandated)

- J-emphasis [4]: the coverage lens checks every ask lands, not that the ideation's *emphasis*
  survived — add "does the tree weight what the ideation weighted?" to the judgment-gate brief.
- J-M-anchor [4]: tier M has no calibration exemplar; expect M-tier judgment calls to be the least
  reproducible until one exists.
- J-defaults [4]: checkpoint-default laundering — record per answer whether chosen or
  default-accepted; coverage/judgment lenses weigh default-accepted as factory assumptions.
- J-neglect [4]: at M/L, untouched components' drift is invisible indefinitely; a scheduled
  full-tree `verify` in the instantiated verification standard would close it cheaply.
- J-S-proportionality [4]: tier-S independent verification triggers on self-judged "substantial" —
  the builder certifies its own DoD below that line; "all QA layers every time" invites checkbox
  theater on trivial fixes.

## CLEAN (all four lenses)

Phase cuts and gate schedule; the DRIFT lifecycle end-to-end (every lens walked it; the emitted
repo is self-sufficient without grammar.md); pinned values and tier arithmetic; template↔grammar
section pairings; citation sweep (~70 refs, two mis-targets reported); gates fail closed;
files-as-interface resume (except C1/C3); record/spec separation mechanics; rule-10 calibration
discipline; templates' blockquote hygiene; NOTES' honesty.

## Resolution log

*(to be completed by the fix-loop session: per finding — fixed (evidence) | accepted (operator,
reason); then blind re-verification per §3 by fresh verifiers who have not seen this record's
findings-as-fixed claims; then PASS/FAIL and the operator countersign.)*
