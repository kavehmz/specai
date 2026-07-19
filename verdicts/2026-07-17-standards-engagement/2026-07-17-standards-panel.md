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
`verdicts/2026-07-17-standards-engagement/2026-07-17-operator-decisions-D1-D6.md`.

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

## Resolution log (fix-loop session, 2026-07-17)

Design-flagged findings resolved per the operator's D1–D6 decisions
(`verdicts/2026-07-17-standards-engagement/2026-07-17-operator-decisions-D1-D6.md`, Operator resolutions section). Evidence =
where the fix landed.

### Majors — all fixed

- **A1** fixed (D1): `change_rule.md` §5 rewritten — weight keyed to target document; panel only
  for the self-governing surfaces; deferral is a named NOTES IOU with a payoff anchor.
- **A2** fixed (D3): `verification_core.md` §2 rule 4 — independence as channel (fresh context +
  declared package + templated brief); lead as zero-discretion mechanical dispatcher; operator
  orders the seal + specai reviews; §1 aligned; `phases/verification.md` pass 2 states the
  phase-6 dispatch; `change_rule.md` §5 rule 5 cites it.
- **A3** fixed: `SKILL.md` §4 contamination bullet — neutral working directory binding for every
  fresh-context role, disclosure in the verdict when injection is unavoidable;
  `reference/exemplars.md` §3 hygiene rule 1.
- **A4** fixed: verification-mode field added — `templates/notes.md` seal line,
  `verification_core.md` §6 rule 4, `SKILL.md` §4 degraded floor, `grammar.md` §6 check 7,
  `phases/verification.md` seal.
- **A5** fixed (D5): `reference/exemplars.md` §3 rewritten with binding eval hygiene (target
  exemplar off-limits — the other remains readable; operator-dispatched comparison; no PASS
  without the integration proof); `templates/component_spec.md` header exemplar read demoted to
  lead-level calibration and excluded from author packages; `grammar.md` header tiebreaker moved
  to the templates.
- **A6** fixed (D5): L1 stamp relabeled in `exemplars.md` §3 — "comparison verdict passed
  2026-07-11; build-proof pending; pre-dates the hygiene rules (target readable, comparison
  self-dispatched)."
- **B1** fixed: verdict record required at M and L everywhere — `verification_core.md` §4 table,
  `dial.md` §2 row, `phases/verification.md` pass 2 (aligned to §6).
- **B2** fixed: `change_rule.md` §4 defines **top tier** (the tier's phase-6 seal depth,
  `verification_core.md` §4) and **focused pass** (one fresh verifier over the artifact + cascade
  set).
- **B3** fixed: taxonomy defined and owned — `verification_core.md` §2 rule 1 (dispatcher curates,
  never the author; `<run-dir>/taxonomy.md` for factory runs) and §3 fix-loop bullet.
- **B4** fixed: `verification_core.md` §3 seal step names the owning gate (operator per the tempo
  rule, not per artifact); `SKILL.md` §3 now cites the cell without restating it.
- **B5** fixed: `dial.md` §2 names the **spot-verify schedule**; §3 disambiguates **tempo**;
  citations corrected in `verification_core.md` §3, `phases/architecture.md` step 9,
  `phases/contracts.md` step 6; both terms in `SKILL.md`'s terms block.
- **B6** fixed: `phases/verification.md` pass 2 — at S the judgment-gate brief folds into the
  single verifier's dispatch (own verdict section); at M/L an additional fresh context.
- **C1** fixed: `<run-dir>/notes-seed.md` named — `phases/definition.md` output 5 + step 5,
  `phases/emission.md` inputs, `SKILL.md` §3 working-file inventory.
- **C2** fixed: `phases/architecture.md` step 4 writes `<run-dir>/slices/<component>.md` +
  `slices/product.md`; `phases/component_specs.md` inputs clarify full-architecture reading (the
  excluded items are sibling specs and slices) and cite slice paths; `SKILL.md` §4 notes the file
  mechanism.
- **C3** fixed: gap reports at `<run-dir>/gaps/<component>.md`; `Status: DRAFT` convention for
  in-flight specs (`phases/component_specs.md` outputs).
- **C4** fixed: engineering standard owned by phase 3 (`phases/architecture.md` step 8,
  `phases/contracts.md` outputs — testing floor stubbed) and completed at phase 5
  (`phases/emission.md` procedure 7).
- **C5** fixed: `README.md` layout adds `delta` + `verdicts/`; `SKILL.md` map adds `README.md`;
  `change_rule.md` §5 now covers both maps.
- **D-ext** fixed: self-sufficiency stated — `grammar.md` header (templates tiebreak; exemplars
  optional), `reference/exemplars.md` header, `phases/emission.md` inputs,
  `verification_core.md` §8 (the loop pattern is normative; feedler's file a reference where
  available).
- **D-L** fixed: category-level definitions — `phases/emission.md` output 2 (QA-officer pattern,
  taxonomy seed, verdict-record rules, studio.md), `grammar.md` §5 design row (storyboards).
- **E1** fixed (D2): `dial.md` §1 rule 2 — money machinery keys to regulatory/money = 2 regardless
  of tier; §2 note; `change_rule.md` §4 money-path clause; `phases/definition.md` step 4.
- **E2** fixed (D2): `dial.md` §1 rule 3 — generic mid-run re-score on any dimension discovery,
  operator confirm, downstream re-size.
- **E3** fixed (D4): the tier binds in `vision.md` §Dial (`grammar.md` §4.1,
  `templates/vision.md` §10, `phases/definition.md` steps 3/6, `grammar.md` §6 check 7); non-goals
  carry identity/revisitable marks (`templates/vision.md` §9, `change_rule.md` §2 rule 1,
  `templates/start.md` case C, `phases/delta.md`); NOTES holds nothing binding (`grammar.md` §4.9,
  `templates/notes.md`).
- **E4** fixed (D6): `style.md` §1 — the engineering standard licensed to bind exactly its
  template's HOW-level surfaces; everything else WHAT-only.
- **F1** fixed: lineage/dated-status stripped to NOTES pointers in `dial.md`,
  `verification_core.md` (header, §3, §7), `change_rule.md` §1, `phases/definition.md` header,
  `phases/contracts.md` (header, step 1), `phases/emission.md` header, `phases/delta.md` header.
- **F2** fixed: `style.md` rule 9 aligned to `grammar.md` §5 (none/optional/L-when-strained),
  citation re-pointed.
- **F3** fixed: neutral-dir rule → `SKILL.md` §4 (with A3); registrar seal-bookkeeping precedent →
  `SKILL.md` §5.

### Minors — all fixed

1 `phases/contracts.md` step 4 defines the pre-seal no-bump allowance; `phases/delta.md` cites it ·
2 `templates/component_spec.md` header (lead-level, eval-excluded) · 3 `grammar.md` §6 check 6
semi-mechanical · 4 §6 check 1 exempts `start.md`/`README.md` · 5 develop_loop offer owned by the
seal presentation (`phases/emission.md`, `phases/verification.md`) · 6 `SKILL.md` §3 absorption
checklist + run-dir disposition · 7 `phases/delta.md` defines its `<run-dir>` +
`change-request.md` home · 8 `phases/architecture.md` step 8 → template §7 · 9 M/L checkpoint
rounds anchored in `phases/definition.md` step 4 · 10 bump-trigger breadth unified (template
wording, verbatim in `grammar.md` §4.4 + `phases/contracts.md` step 4) · 11 `grammar.md` §4.3
case-C summary carries the hand-back · 12 `phases/emission.md` inputs add `style.md` · 13 folded
into B5 · 14 `slices/product.md` named (`phases/architecture.md` step 4, `phases/contracts.md`
inputs) · 15 ideation contradictions always checkpoint questions (`phases/definition.md` step 4) ·
16 consumers appendix mandatory at M/L (`grammar.md` §4.4, `phases/contracts.md`,
`templates/contract_standard.md`) · 17 QA-layer names tailorable (`templates/start.md` §4) ·
18 "signature formats" ghost → "named output formats" · 19 exemplars run-history line relabeled +
NOTES pointer · 20 DRIFT prose numbered (`grammar.md` §4.10 rules 1–6, `verification_core.md` §6
rules 1–4, `templates/start.md` §3B rules 1–4) · 21 "experience-led" defined (`style.md` §1,
`SKILL.md` terms) · 22 tone nits + typo fixed ("crown" ×2, "invaluable", "proven", "sloppy third",
"the the") · 23 `SKILL.md` terms block + RFC 2119 declaration added.

### Judgment items

- **J-emphasis** applied: emphasis survival added to the judgment gate (`verification_core.md` §7,
  `phases/verification.md`).
- **J-defaults** applied: checkpoint answers marked chosen/default-accepted
  (`phases/definition.md` step 5, `templates/notes.md`, `grammar.md` §4.9).
- **J-neglect** applied: M/L verification standards include a scheduled full-tree verify
  (`phases/emission.md` output 2).
- **J-M-anchor** accepted (operator): no tier-M exemplar exists; remains an open topic until one
  does.
- **J-S-proportionality** accepted (operator): tier-S self-judged "substantial" stands for now;
  revisit if S-tier seals show checkbox theater.

### Status

Fixes complete; **blind re-verification pending** per `verification_core.md` §3 — fresh verifiers,
same four-lens split, who have not seen this record. PASS/FAIL and the operator countersign follow
it.

---

## Blind re-verification — round 1 (2026-07-17)

**Dispatch:** operator-ordered ("go", recorded in-session); run lead as mechanical proxy. Four
fresh verifiers, panel lens split. Package: the full tree **minus `verdicts/`** (this record and
all fix claims excluded) and minus `.git`; NOTES.md included as content-under-review. Templated
briefs (lens row + finding shape + PASS rule + package). First dispatch was killed by a harness
usage limit before any verifier produced findings; relaunched clean — no contamination.
**Injection disclosure (all four verifiers, unprompted):** harness ambient context included the
repo's git-status snapshot with recent commit subjects ("verdicts and review", …) — authoring-
history-adjacent; none reported using it as evidence. No CLAUDE.md or memory files injected.

**Verdicts: FAIL · FAIL · FAIL · FAIL** — 1 blocker, ~29 majors (deduped ~20), ~27 minors.
Convergence: the tier-S verdict-record gap, the engineering-standard inline path, and the
self-change gate holes were each found independently by 2–3 lenses. All four verifiers
independently corroborated NOTES.md's honesty.

### Round-1 findings → round-2 resolutions (all fixed unless marked accepted)

- **BLOCKER [judgment] ledger lags tree** (NOTES's last entry claimed the fix loop still owed
  while the tree carried the fixes) → fixed: fix-loop session entry appended to NOTES; practice
  adopted: the NOTES entry lands **with** the fixes.
- **Eval answer key embedded in binding docs** [judgment] → fixed: identifying calibration facts
  (names, tiers, sizes, dial breakdowns, decomposition shapes, signature principles, manual line
  counts) quarantined into `reference/exemplars.md` (now itself excluded for eval runs — its §3
  rule 2); genericized in `grammar.md` (header, §2), `dial.md` §1, `SKILL.md` header, `README.md`,
  `phases/definition.md`, `phases/architecture.md` steps 3/5, `phases/contracts.md`,
  `phases/emission.md`, `templates/start.md` header, `templates/engineering_standard.md` header,
  `verification_core.md` §8. Comparison axes re-weighted (grammar conformance last — circular);
  operator stages eval inputs; verdict home named.
- **Tier-S verdict records / disclosure durability** [exec 7, judgment 6, altitude 5] → fixed:
  every seal writes a verdict record (minimal S form; committed by default; discard rule preserves
  dispatcher/package/injection facts in the NOTES seal line; taxonomy absorbed before run-dir
  deletion) — `verification_core.md` §4+§6.4, `templates/notes.md`, `SKILL.md` §3.
- **Engineering standard inline path** [exec 2, altitude 2+3, consistency 1] → fixed: phase 3
  writes it in every case (separate, or delivered as architecture §7 at S);
  `templates/architecture.md` §7 cites the engineering template; style.md §1 cites grammar §4.7
  as the single enumeration owner; emission output 7 names both homes.
- **Money machinery undefined** [exec 4, consistency 2] → fixed: `grammar.md` §4.2 Money &
  compliance section; `templates/architecture.md` §7b; regulatory register as REG-lines
  (`phases/definition.md`); authoring step (`phases/architecture.md` step 8).
- **studio.md / develop_loop.md shapeless** [exec 5] → fixed: `grammar.md` §4.11 category shapes,
  self-sufficient without exemplars.
- **develop-loop accepted at seal lands unverified** [exec 6] → fixed: acceptance routes through
  the sealed repo's own change process (`phases/emission.md`, `phases/verification.md`).
- **Self-change gate holes** [judgment 3+7, altitude 6] → fixed: `change_rule.md` §5 —
  templates + all of SKILL.md + exemplars.md gated at one-verifier weight; SKILL §4's
  contamination/degraded clauses join the panel class; catch-all row for any other binding text.
- **IOUs have no collector** [judgment 5] → fixed: seal presentations and eval preambles
  enumerate open IOUs; past-anchor blocks (`change_rule.md` §5.4, `phases/verification.md`,
  `exemplars.md` §3.6).
- **Degraded floor discloses but never owes** [judgment 9] → fixed: degraded seal records an IOU
  (`SKILL.md` §4).
- **Coverage-lens cut cheat** [judgment 2, consistency 14] → fixed: a cut counts only as a
  `vision.md` revisitable non-goal; NOTES-only cuts FAIL; inventory lines added to the lens
  (`verification_core.md` §5, `phases/verification.md`).
- **Cascade sets author-asserted** [judgment 8] → fixed: derived from the citation graph, named
  in the verdict (`change_rule.md` §3, `phases/delta.md` step 6).
- **Working-file gaps** [exec 1+3, consistency 3] → fixed: `consumer-ledger.md`, `journal.md`,
  `slices/design.md`, delta filenames — named in `SKILL.md` §3 and their producing/consuming
  phases; phase-6 package + inputs reconciled (taxonomy included).
- **Dispatcher-curation vs zero-discretion** [consistency 4] → fixed: taxonomy is mechanical
  distillation from committed verdict records, part of the declared package, passed unchanged.
- **Table restatement dial§2/core§4** [consistency 5] → fixed: §4 owns counts; dial cites.
- **Boot-table exemptions ×3 + grammar §3.3** [consistency 6, altitude 4] → fixed: all sites cite
  or carry §6 check 1's exemptions.
- **"Seal" overload** [consistency 7, altitude 9] → fixed: quality-cell stage renamed **close**;
  "seal" reserved for phase 6.
- **DRIFT permanence guard missing from template** [altitude 7] → fixed: `templates/start.md`
  §3B rule 4.
- **grammar §6 paraphrase drift** [altitude 4] → fixed: pass 1 cites the checklist whole.
- Minors: judgment-gate dispatch in §4 table · conforming-brief definition · delta lens row ·
  delta slices producer + two-item wording · closed-input list violations (definition, phase 6) ·
  L1 NOTES supersession line · registrar/run-lead circularity · UI design-first trigger ·
  new-component shape guidance · attachments home · taxonomy bootstrap · start §5 style-list
  drift · RFC-2119 extension · rule-11 residue (exemplars history → pointer, speclint aside,
  delta lineage) — all fixed at the named homes.
- **Accepted (operator):** nested-parenthetical prose density [judgment 13] — style debt for a
  future altitude pass; behavior unchanged.

**Round-2 blind confirmation:** dispatched over the round-2 tree (same lens split, fresh
verifiers, `verdicts/` excluded); its verdict + the operator countersign close this engagement.

---

## Blind re-verification — round 2 (2026-07-17)

**Dispatch:** as round 1 (operator standing order; lead as mechanical proxy; templated briefs;
tree minus `verdicts/`). All four verifiers disclosed the same ambient injection (git-status
commit subjects; no CLAUDE.md/memory) unprompted; none used it as evidence.

**Verdicts: FAIL ×4 — 1 blocker (found independently by 3 lenses), ~27 raw majors (deduped ~18),
~29 minors.** Raw reports preserved verbatim (per the new §6 rule 4, adopted mid-engagement):
`2026-07-17-reverify-r2-lens{1,2,3,4}-*.md`. Round-1 raw reports predate the rule and survive
only as round 1's consolidated section — disclosed limitation. Positive findings: pinned values,
term discipline, S-tier walks, crash-resume, emitted-repo self-containment, and the D1–D6
ledger↔tree trace all held; lens 4 judged the core design "genuinely good and would be lived by."

### Round-2 findings → round-3 resolutions (all fixed unless marked accepted)

- **BLOCKER: quarantine residue** [altitude B1, judgment B1, consistency 1] → fixed: exemplar
  names/tiers/shapes/sizes scrubbed from `grammar.md` (header claim now true, §3 rule 2, §4.7 —
  stack example replaced with an invented one), `templates/contract_standard.md`,
  `templates/component_spec.md`, `templates/notes.md`, `templates/start.md` header,
  `phases/emission.md` ("feedler-style"), `SKILL.md` §2 (`evaluate <exemplar>`), plus the
  anonymized echoes (dial status line, architecture step 3, definition reference-class line).
- **Eval reads NOTES** [judgment M1, consistency 8] → fixed: `exemplars.md` §3 rule 2 excludes
  specai's `NOTES.md` + named candidate repos, overriding SKILL §0's pointer for the run.
- **Judgment-gate brief nonconforming** [×3] → fixed: `verification_core.md` §2 rule 4 licenses
  the §5 row(s), the §7 brief, and the eval-comparison brief, each verbatim from its owner.
- **Taxonomy producer/curation/sourcing** [×3 + judgment M6] → fixed: §2 rule 1 defines the
  mechanical transform (one line per closed blocker/major: lens · pattern · source record),
  entry shape, author-ban exemption, and the cross-run accumulation point
  (`verdicts/taxonomy-seed.md`, appended at run close — `SKILL.md` §5); §3's "curated" clause
  replaced.
- **Money trigger pinned three ways** [exec M-3, consistency 2] → fixed: the dimension is the
  sole trigger everywhere ("when and only when reg/money = 2") — `phases/definition.md` ×2,
  `dial.md` §2 note.
- **Licensed-HOW two owners** [alt M5, consistency 3] → fixed: the template owns the section
  enumeration; `grammar.md` §4.7, `style.md` §1, and both template headers defer to it.
- **Gate overlap precedence** [consistency 4] → fixed: "where rule 2 also matches, the stricter
  gate binds" (`change_rule.md` §5.1).
- **Delta verifier package undeclared** [exec M-4] → fixed below with the delta package list.
- **Tier-L artifact classes shapeless** [exec M-5] → fixed: `grammar.md` §4.11 gains category
  shapes for the conformance-suite spec, ops/infra standards, and agent standards;
  `phases/contracts.md` aligns modality (L adds the suite; operator may waive, recorded).
- **studio.md condition pinned three ways** [consistency 7] → fixed: §4.11 owns (L ∧
  experience-led); `grammar.md` §5 and `dial.md` §2 cite it.
- **Gate tamper-evidence** [judgment M2] → fixed: gate-approved copies at `<run-dir>/gates/<phase>/`
  (definition/architecture/contracts gates); `notes-seed.md` + gate copies join the phase-6
  package; verifiers diff sealed artifacts against baselines.
- **Cut laundering** [judgment M3] → fixed: coverage lens gains the reverse-provenance check;
  fix-loop edits to gate-approved artifacts re-trigger the owning gate (`verification_core.md`
  §3+§5, `phases/verification.md`).
- **Spot-verifies unenforced** [judgment M4] → fixed: every spot-verify writes a one-page record;
  the seal enumerates them; absence blocks (`verification_core.md` §4, `phases/verification.md`).
- **Cascade shrinkable** [judgment M5, consistency 15] → fixed: bidirectional derivation incl.
  term-owners (`change_rule.md` §3); specai focused passes carry full standards/+SKILL context
  (§5.1).
- **Records can vanish** [judgment M7, exec m-2] → fixed: relocation-before-deletion rule +
  verbatim per-verifier reports named in the record (`verification_core.md` §6 rule 4) —
  practiced immediately (the four r2 report files).
- **Typo exemption bypass** [judgment M8] → fixed: no exemption on self-governing surfaces;
  elsewhere exempted edits join a seal/eval-enumerated bundle (`change_rule.md` §5.2–5.3).
- **Un-IOU'd deferral / "gate has run"** [judgment M9] → fixed: a gate has run only when its
  verdict returns (`change_rule.md` §5.4); the current pending round-3 confirmation is recorded
  as a formal IOU in NOTES.
- **Commit doctrine two strengths** [alt M3] → fixed: `change_rule.md` §4 splits the actors
  (specai never commits, ever).
- **Restatements** [alt M4, consistency 5-cousins] → fixed: `verification_core.md` §4 spot column
  cites dial §2; `SKILL.md` §3 diagram drops per-tier gate values and cites the tempo rule.
- **Minors** (all four lenses) → fixed at the named homes: grammar §6 check 8 (scaffolding),
  eval proof grader + staging + other-exemplar wording, REG-trigger wording, verdict-record
  tier-line in phases/verification.md, contracts content-list citation, engineering-standard
  provenance pointers, journal producer/content, run-manifest definition, start.md case-A/B/C
  wording + change-rule verbatim restore + §5 style-list wording, component template's
  intent-vs-binding sentence, README five-sentences package fix, dial resolution-not-rounding
  wording, "~80%" dropped, "constitution-grade" replaced with observables, design-first
  any-tier note, emission mega-sentence split + template input added, verification pass-1/pass-2
  paraphrases replaced with citations.
- **Accepted (operator, standing):** residual nested-parenthetical prose density [alt m9
  re-flag] — carried style debt, unchanged behavior.

**Round-3 blind confirmation:** dispatched over the round-3 tree (same lens split, fresh
verifiers, `verdicts/` excluded). Its verdict + the operator countersign close this engagement;
the owed gate is recorded as an IOU in NOTES until that verdict returns.

---

## Blind re-verification — round 3 (2026-07-17)

**Dispatch:** as rounds 1–2. All four verifiers disclosed the same harness injection (git-status
commit subjects; no CLAUDE.md/memory) unprompted.

**Verdicts: FAIL ×4 — 3 deduped blockers, ~21 deduped majors, ~25 minors.** Raw reports verbatim:
`2026-07-17-reverify-r3-lens{1,2,3,4}-*.md`. Convergence: the README fixture-name leak was found
independently by three lenses; the architecture decomposition echo by two; the exempted-bundle
homelessness by three.

**The three blockers:** (1) `README.md`'s invocation examples name the tier-S fixture — the one
file the round-3 quarantine sweep missed, falsifying NOTES' "quarantine completed" claim;
(2) `change_rule.md` §5 rule 4 defines IOU payment as the verdict *returning* — a returned FAIL
pays the debt (letter bug; the live IOU is written in exactly this letter); (3) the round-3
"genericization" of `phases/architecture.md` step 3 still carries both exemplars' decomposition
shapes, lightly fuzzed.

**The major clusters:** residual quarantine echoes (definition's feed-reader example, the vision
template's "single-user by design" pillar, dial's preamble, component template's export-flavored
invariants, `verdicts/` itself now leaking into eval taxonomies); enumeration/letter residue
("all seven checks" written while adding check 8; command-grammar with three variant owners;
verifier counts restated; the coverage-lens paraphrase carrying additions its own brief rule
forbids; the exempted bundle promised a reader but given no file); mid-run spot-verify briefs
unsatisfiable as templated; the delta verifier package still underdeclared; and the trust-root
class — gate copies lead-rewritable, vision.md unbaselined, packages lead-asserted rather than
verifier-attested, collectors fed by the collected-upon, the integration proof self-graded at S,
tier-S sequential authoring undisclosed degraded isolation.

**Resolution status: PENDING — operator triage requested.** The letter/quarantine/enumeration
classes are objective and lead-fixable. The trust-root class requires **new operator duties**
(gate-time baseline commits, eval staging, operator-dispatched build proofs) — adopting those is
a design decision the tree's own D1 history warns against making unilaterally (a rule the
operator won't live by is a bad rule). The round-3 IOU remains open under the corrected reading
of payment (gate must *close*, not merely return).

### Operator triage (2026-07-17) and round-4 resolutions

**Operator decisions:** triage & close. Adopted duties: **eval staging** (operator stages eval
inputs + a scrubbed taxonomy; `verdicts/` joins the eval exclusion) and **eval build-proof
dispatch** (operator dispatches the integration proof's verifier, which signs the DoD line).
**Declined:** gate-time operator commits of baselines. **Accepted with reason** [covers r3
judgment M1 and the residual of M8]: gate baselines and collectors remain lead-held files; *"the
operator reviews diffs at commit time — the countersign commit is the operator-fixing act;
per-gate commits declined as ceremony that would not be lived by."*

**All other round-3 findings fixed:** README examples neutralized + lineage trimmed; IOU payment
redefined as gate-closing (`change_rule.md` §5.4); architecture step 3 reduced to role statement;
definition's category/stack examples replaced with labeled invented ones; vision-template pillar
example invented; component-template invariants invented; dial preamble neutralized; dial table
repaired + tiny/small/money-path defined (dial §2, grammar §4.7, change_rule §4); "all seven
checks" → count-free; command-grammar enumeration → template owns (grammar §4.3); verifier-count
restatement → citation; coverage-lens procedure moved into its §5 row + §2 rules 2–3 join the
conforming brief + spot-verify scoping made mechanical + verifier attestation echoes and
dispatch-prompt preservation (`verification_core.md` §2.4); exempted-edit bundle homed in NOTES
("Exempted edits" heading) + swept at evals (exemplars §3.6); DoD gains the
independent-verification line (start template §6, grammar §4.3); delta step 6 got its declared
package; vision.md joined the gate baselines + phase-6 diff; seal-verifier package gained
spot-records + dial §2 + NOTES with an expected-count check; cascade re-derivation by the
focused-pass verifier over the whole tree; tier-S sequential authoring named a degraded mode with
disclosure; taxonomy pattern = verbatim issue copy; taxonomy-seed append single-owned (SKILL §5);
exemplars §3 joined the panel-gated surfaces; comparison brief fenced verbatim; grammar §2 gained
the conditional `verdicts/` dir; the shared-surface pattern instance named in exemplars §1;
"checkpoint"/"gate" disambiguated; remaining minors at their named homes.

**Round-4 blind confirmation dispatched** (same lens split, fresh verifiers, `verdicts/`
excluded) — the closing gate for the open IOU under the corrected payment rule. Its verdict + the
operator countersign close this engagement; per the operator's triage decision, judgment-class
residue in the accepted trust-root class does not reopen the loop.

---

## Blind re-verification — round 4 (2026-07-17) and round-5 resolutions

**Verdicts: FAIL ×4 — 1 deduped blocker (×2 convergence), ~10 deduped majors, ~24 minors.** Raw
reports verbatim: `2026-07-17-reverify-r4-lens{1,2,3,4}-*.md`. The trust-root class held as
accepted (judgment lens honored the recorded acceptance; its brief carried the acceptance —
disclosed in its report header). The named disease: each hardening rode the main path only; the
fix class is "enumerate every path the rule must ride."

**Round-5 resolutions (all fixed):** the blocker — phase-6's NOTES package item and seal sweep
got the eval carve-out (operator's preamble owns the sweep at evals; exclusion disclosed in the
record). Attestation + conduct rules now travel **in** the conforming brief (§2 rules 2–4
verbatim), and phase files may carry fenced "Verifier checks (verbatim)" blocks the brief
licenses — phases/verification.md's checks (gate diff, record count with the
`verdict-spot-<phase>-<date>.md` convention, non-eval IOU sweep) are now such a block. The delta
path joined every mitigation: identity/revisitable honored at step 1, gate copies at delta gates,
step 6 declared a phase-6 seal in every duty (counts, judgment gate, operator dispatch, sweeps,
delta gate copies + records in the package), delta re-seals joined §5.4's collector list. The
eval route was operationalized: the operator executes §3's protocol (SKILL §2 row), a fenced
**eval dispatch prompt** is templated + preserved, degraded-mode evals are prohibited, the
default-accepted weighting moved into the §5 coverage row. The studio's inputs became durable
emitted documents. Emission cites the template-owned command list. Phase gates and spot-verify
steps now cite dial §2–3 instead of restating tier letters. SKILL §4's degraded IOU uses §5.4's
re-anchored form in specai's NOTES; the registrar act is named in the NOTES stamp itself. Minors
fixed at their homes (echo de-numbering, seed-append transform + first-sentence truncation +
source-record dedupe, mechanical-pass trace line, RFC case, update-mode term, README/SKILL claim
scoping, design author's engineering standard, agent-standards producer, vision "Why now"
ownership, dial money-cell footnotes).

**Resolved by invariant refinement (disclosed design call under the triage mandate):** altitude
M1's tier-designator class — `exemplars.md`'s preamble now scopes the quarantine to facts
characterizing a **specific named exemplar** and licenses tier-neutral role references ("the
tier-S exemplar"), since a target's tier is ideation-derivable by the dial by design. This edit
to a rule-1-gated surface (the preamble, not §3) is verified by the round-5 confirmation itself.

**Accepted (operator, standing):** m5-class restated-but-agreeing pinned values (table headers);
the verification-mode triple's three verbatim homes; residual "checkpoint" echoes in row headers;
prose density. Logged, unchanged behavior.

**Round-5 blind confirmation dispatched** — the closing gate. Zero blockers/majors on the
objective lenses (accepted-class residue excepted) pays the IOU and sends the engagement to the
operator's countersign.

---

## Blind re-verification — round 5 (2026-07-17) and round-6 resolutions

**Verdicts: FAIL ×4 — 1 blocker (delta package contradiction, ×3 convergence), ~9 deduped
majors, ~25 minors.** Raw reports verbatim: `2026-07-17-reverify-r5-lens{1,2,3,4}-*.md`. The
refined quarantine letter **verified clean** on two lenses ("only licensed tier-neutral role
references"); the trust-root acceptance held; the consistency lens's CLEAN list covered the eval
invariant, every canonical term, every pinned value, every ownership seam, DRIFT, the IOU letter,
and the money trigger. Two round-5 ledger claims caught as partially overstated (the eval
carve-out missed SKILL §5; the delta path missed step 2 + the check mapping) — recorded honestly.

**Round-6 resolutions (all fixed):** the blocker — delta step 6's package is now the **phase-6
package with named delta substitutions** (dial §2, specai NOTES, templates/, tier-L taxonomy ride
along); check 1 generalized to **every artifact under `gates/**`** with delta readings inside the
fenced text; check 2 gained the delta derivation (phases actually re-run); delta step 2 got its
gate copy + spot-verify; the package sentence's unclosed parenthesis restructured into a clean
eval-exception sentence. The eval path completed: SKILL §5's run-closing acts got the eval
carve-out (operator/registrar, from preserved records), §2 rule 1's taxonomy assembly got the
eval carve-out in readable text, emission's exclusion parenthetical corrected to whole-file
scope, the eval prompt discloses to journal **and** verdict record, the build-proof's builder
launch assigned to the operator. The architecture spot-verify got a declared package (+ideation,
verifier-only). The **emitted commit rule** joined the start template §0 (operator commits;
develop-loop Gate the only exception) with an S-tier money-path fresh-dispatch line in §4. The
seal-operating text (phase-6 package + fenced checks, delta step 6) joined `change_rule.md`
§5.2's panel class. Minors fixed: spot-record naming in §4, seed-append transform stated in
SKILL §5, §4 count-ownership scoped + M-split default named, exemplars preamble "only home in
binding documents", SKILL §3 meta-claim softened, delta gate cadence cites tempo, contracts
inputs +§4.11, grammar §6 check 1 conditional carve-outs, grammar §4.3 command line cite-only,
grammar §5 headers de-ranged, dial ≤3 threshold single-owned, style rule 9 truncated + rule 2
example invented-and-labeled, architecture/vision examples labeled invented, README five-sentences
collapsed to the owner citation, delta change-request relocation duty. **Accepted (operator,
standing):** dial §2's money items marked in tier cells rather than pulled out (the §1-rule-2
markers + corrective note make the trigger unambiguous); restated-but-agreeing table values
previously logged.

**Round-6 blind confirmation dispatched** — the closing gate under the same terms.

---

## Blind re-verification — round 6 (2026-07-17) — the closing round

**Verdicts: FAIL ×4 — 0 blockers (first time in the engagement), 5 deduped majors, ~20 minors.**
Raw reports verbatim: `2026-07-17-reverify-r6-lens{1,2,3,4}-*.md`. Convergence at maximum: the
M-split buildability omission (a round-6 edit's own defect) was found independently by **all
four lenses**; the delta lens-set ambiguity by three. The judgment lens's ledger↔tree audit
verified every round-6 NOTES claim true; the quarantine held under grep on two lenses; the eval
path, IOU letter, cascade re-derivation, and both ledger self-corrections all "held under
attack."

**Round-7 fixes (applied; blind reconfirmation waived by operator decision — see below):**
buildability into the M split + the **lens-totality rule** (every tier: the union of dispatched
briefs MUST equal the applicable §5 set; an uncarried lens blocks the seal) + the L partition
named in the templated dispatch; delta step 6's lens sentence disambiguated (all §5 lenses apply,
scoped, with the four delta readings); delta step 1 gained its scheduled spot-verify, step 2 its
spot-verify substitutions, the package its conditional consumer-ledger; `taxonomy.md` + preserved
dispatch prompts relocate with the verdict records (closing the last invisible-in-diff channel);
the registrar definition widened to the eval carve-out; "gate" joined the terms block;
phases/verification.md's Inputs completed + "prior seal-round reports" disambiguated; the
"tier-role references" license relabeled; grammar §6 check 1's conditional set completed
(design/); §5.4 admits the degraded-seal IOU; the contract template carries the pre-seal no-bump
parenthetical; the comparison panel got its ≥2 floor; the eval preamble sweep records into the
comparison verdict; SKILL's map/eval-row citations corrected; the remaining unlabeled examples
labeled invented; the altitude-lens gloss, style rule 9's owner phrase, dial's L-row ID phrase,
and the speclint aside made timeless.

### Engagement close (presented for the operator's countersign)

Six blind verification rounds over five fix waves: blockers 0→1→3→3→1→0·0·0·0; majors
~24 → ~20 → ~18 → ~21 → ~10 → ~9 → 5 — from structural (undefined money machinery, a
self-defeating eval protocol) to a single missing lens name in a table written the same day. The
final round found zero blockers on all four lenses, verified the ledger fully truthful, and its
"held" lists cover the entire system.

**Presented for operator acceptance with recorded reasons (the IOU's closing act, per
`change_rule.md` §5.4's acceptance arm):**
1. The round-6/7 fixes above land **without a seventh blind round**. Reason: six rounds of
   monotone convergence; the remaining fix class is one-line letter repairs whose blind
   reconfirmation has each round seeded equivalent new letter defects; the operator reviews this
   round's diff directly at the countersign.
2. Standing accepted classes (unchanged): lead-held trust root with commit-diff backstop; dial §2
   money items marked in tier cells; restated-but-agreeing table values; prose density.
3. Judgment-lens accepted-class edge noted for the record: gate copies do not relocate at run-dir
   deletion (post-hoc baseline audit ends with the run dir; at-seal diff + gate-time reading are
   the coverage).

**The operator's commit of this tree is: the acceptance of items 1–3 with these reasons, the
payment of the open IOU, the countersign of the 2026-07-17 panel engagement, and its close.**
