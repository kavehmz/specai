# taxonomy-seed.md — cross-run defect-pattern accumulation point

*Format per `verification_core.md` §2 rule 1: one line per closed blocker/major —
`lens · pattern · source record`, the pattern a **verbatim copy of the source finding's issue
line's first sentence, never paraphrased** — nothing else. Applied here as: the finding's bold
issue statement (for locator-style headers, the `**Issue:**` field's first sentence; for the
panel record's consolidated findings, the finding text after its ID/where prefix), completed
from the running text when the statement ends open (colon/em-dash); finding IDs, {where}/
{severity} locators, markdown emphasis, and the sentence-final period stripped; wraps rejoined;
resolution text ("→ fixed:", "Fix:") excluded. Lens assignments and the dedup set (a convergent
finding — same defect, multiple lenses — appears once, citing one record) carry over from the
initial seed. Scrub note for eval staging: no line names an exemplar; lines referencing "the
tier-S fixture" are flagged (†) for removal when staging an eval taxonomy.*

*Third pass (2026-07-17, author session): the second note's two disclosed coverage gaps completed
— r2-lens2's REG-dangling major and r6-lens2's delta-spot-verify major, +2 lines, patterns
verbatim per the stated convention; the full set mechanically re-verified 115/115 after the
addition. Completing the transform over closed majors is zero-discretion; the deduped-set choice
(convergent findings appear once) stands as recorded.*

*Second pass (2026-07-17, at the operator's instruction; uncommitted pending operator review):
the initial seed's patterns were paraphrased/compressed against rule 1's "verbatim" letter, and
four source records were mis-cited. Corrected here: every pattern re-copied verbatim from the
cited record; three lines moved from the r2 section to r3 (their findings are r3-lens2's —
r2-lens2 carries none of them); one line moved from r3 to r4 (r4-lens2's finding 2), its
"nothing else"-violating annotation dropped. Round-1 patterns are the consolidated findings'
verbatim titles — raw round-1 reports were not preserved (disclosed in the panel record), and
findings the consolidation merged appear once.*

## From 2026-07-17-standards-panel.md (founding panel, deduped majors)

- consistency · the top-tier pre-landing gate for standards changes is not livable as written; three consecutive changes deferred it (recorded in NOTES) · 2026-07-17-standards-panel.md
- consistency · "author never dispatches" is unsatisfiable (every mid-run spot-verify is author-dispatched by design) or hollow · 2026-07-17-standards-panel.md
- judgment · fresh contexts are contaminated on the primary harness (CLAUDE.md/memory injection); the neutral-directory rule exists only as a NOTES "binding note for L4" · 2026-07-17-standards-panel.md
- judgment · the degraded-independence disclosure has no durable home; add a verification-mode field (independent panel / single fresh verifier / degraded self-review) to the NOTES seal line; mechanical pass checks it exists · 2026-07-17-standards-panel.md
- judgment · the eval protocol is contaminated by design (target exemplar is assigned reading), self-graded, and its integration-proof criterion was waived at first use · 2026-07-17-standards-panel.md
- consistency · "(Run: PASS 2026-07-11)" is unqualified while NOTES records the integration proof still owed · 2026-07-17-standards-panel.md
- consistency · verdict-record requirement contradicts at tier M (§4/dial: L-only; §6: M/L) · 2026-07-17-standards-panel.md
- consistency · "top tier" / "focused pass" for change-time verification undefined; define by reference to verification_core §4 rows · 2026-07-17-standards-panel.md
- consistency · the tier-L factory "defect taxonomy" is a declared verifier input no document produces; also seed/taxonomy curation is unowned (name the dispatcher as curator, not the author) · 2026-07-17-standards-panel.md
- altitude · "seal" carries two meanings (per-artifact cell terminal vs phase-6 event); the cell read literally demands an operator countersign per artifact, contradicting the tempo rule; SKILL's summary restates the cell differently while forbidding restatement · 2026-07-17-standards-panel.md
- altitude · "tempo" overloaded (operator-gate cadence vs spot-verify schedule); name the §2 referent "spot-verify schedule"; fix the §3-vs-§2 citation · 2026-07-17-standards-panel.md
- executability · the judgment gate: unstated whether it is an additional fresh context or a brief folded into a tier's verifier count (at S: one dispatch or two?) · 2026-07-17-standards-panel.md
- executability · the NOTES seed has no file path; name it (e.g. `<run-dir>/notes-seed.md`) in Definition's Outputs and SKILL §3's working-dir inventory · 2026-07-17-standards-panel.md
- executability · "paths, not summaries" collides with "its inventory slice only"; emit per-component slice files (`<run-dir>/slices/<component>.md`) and cite those paths · 2026-07-17-standards-panel.md
- executability · gap reports have no file home (`<run-dir>/gaps/<component>.md`); the crash-resume story breaks exactly there · 2026-07-17-standards-panel.md
- consistency · engineering_standard.md ownership contradicted ("phase 4/5 to fill" vs phase-3 output), and its §11 testing floor cannot be written before component specs exist; assign to phase 3, add the phase-5 (or phase-4 fan-in) completion step · 2026-07-17-standards-panel.md
- consistency · README omits phases/delta.md (map rot); also [1] SKILL's map omits README.md itself · 2026-07-17-standards-panel.md
- executability · the ambiguity tiebreaker and tier-L calibration inputs are external, one private; the develop_loop "reference text" is external · 2026-07-17-standards-panel.md
- executability · tier-L machinery (QA-officer pattern, taxonomy seed, studio.md, storyboards) is name-dropped but defined nowhere in this repo; give category-level definitions or explicitly mark "per the tier-L exemplar, where available" · 2026-07-17-standards-panel.md
- judgment · money/regulatory machinery keys to tier, not the reg dimension; the round-up rule can't reach a simple real-money product (scores M) · 2026-07-17-standards-panel.md
- judgment · no mid-run dial re-score path; hidden regulatory scope is laundered · 2026-07-17-standards-panel.md
- judgment · NOTES declared non-normative yet holds three normative tenants (the tier; deliberate cuts as "binding context"; delta reads it as binding) · 2026-07-17-standards-panel.md
- altitude · the "one licensed HOW" is claimed narrower than what the template binds · 2026-07-17-standards-panel.md
- altitude · systemic rule-11 violation: ai-it lineage and dated authoring status inside binding docs (worst: delta.md's "Designed 2026-07-12; not yet exercised") · 2026-07-17-standards-panel.md
- altitude · normative rules stored only in the record (neutral-dir rule → SKILL §4 per A3; registrar/orchestrator-stamp precedent → verification_core or SKILL §5) · 2026-07-17-standards-panel.md

## From the round-1 section of 2026-07-17-standards-panel.md (raw reports not preserved — patterns are the consolidated findings' verbatim titles; findings the consolidation merged appear once)

- judgment · ledger lags tree (NOTES's last entry claimed the fix loop still owed while the tree carried the fixes) · 2026-07-17-standards-panel.md
- judgment · Eval answer key embedded in binding docs · 2026-07-17-standards-panel.md
- judgment · Self-change gate holes · 2026-07-17-standards-panel.md
- judgment · IOUs have no collector · 2026-07-17-standards-panel.md
- judgment · Tier-S verdict records / disclosure durability · 2026-07-17-standards-panel.md
- judgment · Degraded floor discloses but never owes · 2026-07-17-standards-panel.md
- judgment · Coverage-lens cut cheat · 2026-07-17-standards-panel.md
- judgment · Cascade sets author-asserted · 2026-07-17-standards-panel.md
- executability · Working-file gaps · 2026-07-17-standards-panel.md
- executability · Engineering standard inline path · 2026-07-17-standards-panel.md
- executability · Money machinery undefined · 2026-07-17-standards-panel.md
- executability · studio.md / develop_loop.md shapeless · 2026-07-17-standards-panel.md
- executability · develop-loop accepted at seal lands unverified · 2026-07-17-standards-panel.md

## From 2026-07-17-reverify-r2-*.md

- altitude † · Exemplar answer-key facts sit inline in binding documents, falsifying the quarantine declaration that makes the eval protocol enforceable · 2026-07-17-reverify-r2-lens3-altitude.md
- judgment · The eval run is not barred from `NOTES.md`, which carries the dial answer key and the L1 grading rubric · 2026-07-17-reverify-r2-lens4-judgment.md
- judgment · Checkpoint answers and inventory lines have no integrity anchor: the phase-6 coverage lens verifies against artifacts the run itself can silently curate after the gate · 2026-07-17-reverify-r2-lens4-judgment.md
- judgment · Coverage misses can be laundered into `vision.md` as fix-loop "revisitable" non-goals: no reverse-provenance check, and no explicit re-gate · 2026-07-17-reverify-r2-lens4-judgment.md
- judgment · Mid-run spot-verifies have no enforcement surface: nothing records that they ran, so skipping them is invisible at the seal · 2026-07-17-reverify-r2-lens4-judgment.md
- judgment · The derived cascade set can be shrunk by omitting citations: the focused pass never sees the document a change contradicts · 2026-07-17-reverify-r2-lens4-judgment.md
- judgment · Taxonomy mechanics are incoherent twice: the sourcing loop is broken, and mid-loop curation collides with the author-exclusion rule · 2026-07-17-reverify-r2-lens4-judgment.md
- judgment · Injection disclosures and independence facts can quietly vanish: "committed" verdict records live inside a directory the run is licensed to delete · 2026-07-17-reverify-r2-lens4-judgment.md
- judgment · The typo/clarity exemption is an author-adjudicated bypass of the self-change gates, including on the self-governing surfaces · 2026-07-17-reverify-r2-lens4-judgment.md
- judgment · The tree is currently living inside an un-IOU'd deferral: round-2 fixes are landed with the confirming gate pending, and rule 4's trigger is too ambiguous to catch it · 2026-07-17-reverify-r2-lens4-judgment.md
- judgment · Verdict-record authorship is unspecified and raw verifier reports need not be preserved: everything the operator countersigns is filtered through the party under judgment · 2026-07-17-reverify-r2-lens4-judgment.md
- consistency · The money/compliance machinery's trigger condition is pinned three different ways; at tier L with regulatory/money scoring 0–1 the documents give contradictory instructions and REG-lines have no mapping home · 2026-07-17-reverify-r2-lens1-consistency.md
- consistency · The licensed-HOW enumeration has two claimed owners, and the two candidate lists already differ · 2026-07-17-reverify-r2-lens1-consistency.md
- consistency · The self-change gates overlap with no precedence rule: every rule-2 surface is also swept by rule 1's broader classes at a weaker gate · 2026-07-17-reverify-r2-lens1-consistency.md
- consistency · The "conforming brief" definition makes the judgment-gate dispatch (mandatory at every seal) and the eval comparison-panel brief nonconforming by construction · 2026-07-17-reverify-r2-lens1-consistency.md
- consistency · "Curated by the dispatcher" contradicts the taxonomy's own handling rules and the zero-discretion dispatch rule; "lens seeds" is an undefined term · 2026-07-17-reverify-r2-lens1-consistency.md
- consistency · The condition for emitting `studio.md` is pinned three different ways · 2026-07-17-reverify-r2-lens1-consistency.md
- executability · delta verification declares no verifier input package, but dispatch legitimacy requires the package to be "the phase file's input list" and forbids lead discretion — so a delta seal cannot be legitimately dispatched as written · 2026-07-17-reverify-r2-lens2-executability.md
- executability · at tier L with regulatory/money scoring 0 or 1 (e.g., 3+2+2+1+1 = 9 → L), the regulatory register is mandatorily produced but its only named consumer never exists, and the assignment step skips it — REG-lines dangle · 2026-07-17-reverify-r2-lens2-executability.md
- altitude · Commit doctrine has two strengths for the same actor · 2026-07-17-reverify-r2-lens3-altitude.md
- altitude · The spot-verify/tempo enumeration is owned by dial.md but restated verbatim in two other binding documents · 2026-07-17-reverify-r2-lens3-altitude.md

## From 2026-07-17-reverify-r3-*.md

- consistency † · Exemplar decomposition shapes — facts `reference/exemplars.md` declares live only in itself — are carried inline in a binding phase file that every eval run must read · 2026-07-17-reverify-r3-lens1-consistency.md
- consistency · Pinned check count contradicts the owning checklist · 2026-07-17-reverify-r3-lens1-consistency.md
- consistency † · An exemplar name — first item on exemplars.md's identifying-facts list — appears inline in binding text (change_rule §5 rule 3 counts README as binding), and README is not on the eval exclusion list · 2026-07-17-reverify-r3-lens1-consistency.md
- consistency · The eval integration-proof exit criterion cites a DoD line that neither the template nor the grammar puts in §6 · 2026-07-17-reverify-r3-lens1-consistency.md
- judgment · IOU "payment" is defined as verdict return, not verdict PASS: a FAIL verdict pays the IOU and unblocks seals and evals · 2026-07-17-reverify-r3-lens4-judgment.md
- judgment · Gate copies are not tamper-evident: the lead writes them, the lead can rewrite them, and nothing commits them at gate time · 2026-07-17-reverify-r3-lens4-judgment.md
- judgment · The verifier's actual package and brief are lead-asserted, never verifier-attested · 2026-07-17-reverify-r3-lens4-judgment.md
- judgment · Eval contamination via verdicts/: the L4 eval's taxonomy assembly reads committed verdict records whose verbatim raw reports quote exemplar answer-key facts; verdicts/ is not on the eval exclusion list · 2026-07-17-reverify-r3-lens4-judgment.md
- judgment · The eval's integration proof has no independent dispatcher, and at tier S its exit criterion is self-graded by construction · 2026-07-17-reverify-r3-lens4-judgment.md
- judgment · Scheduled spot-verify records and the IOU sweep are enumerated only by the lead — the collectors are fed by the party whose omissions they exist to catch · 2026-07-17-reverify-r3-lens4-judgment.md
- judgment · Tier-S single-context sequential authoring is licensed while claiming an impossibility, with no disclosure duty · 2026-07-17-reverify-r3-lens4-judgment.md
- executability · Mid-run spot-verifies cannot be dispatched legally: the conforming-brief rule makes every mid-run brief either nonconforming or unsatisfiable · 2026-07-17-reverify-r3-lens2-executability.md
- executability · The exempted-edit bundle has no durable home; the collector cannot run from files alone · 2026-07-17-reverify-r3-lens2-executability.md
- executability · The definition gate's tamper-evidence baseline omits `vision.md` — the artifact the tree itself calls most protected · 2026-07-17-reverify-r3-lens2-executability.md
- altitude · Carries both exemplars' decomposition shapes inline, lightly fuzzed ("eight-plus components hosting a product family" ≈ the L exemplar) · 2026-07-17-reverify-r3-lens3-altitude.md

## From 2026-07-17-reverify-r4-*.md

- consistency · Eval runs cannot satisfy both the phase-6 seal rules and the eval hygiene rules; the NOTES.md exclusion contradicts the seal package and the IOU collector · 2026-07-17-reverify-r4-lens1-consistency.md
- consistency · The conforming brief forbids the content the attestation rule requires · 2026-07-17-reverify-r4-lens1-consistency.md
- consistency · delta.md step 1 erases the identity/revisitable split · 2026-07-17-reverify-r4-lens1-consistency.md
- consistency · The delta engagement drops the tamper-evidence and collector chain · 2026-07-17-reverify-r4-lens1-consistency.md
- consistency · SKILL §4's degraded-seal IOU waives the anchor §5.4 makes mandatory · 2026-07-17-reverify-r4-lens1-consistency.md
- executability · Phase-6 verifier package embeds duties no conforming brief can deliver, and hands specai's NOTES.md to product-seal verifiers against §2 rule 1 · 2026-07-17-reverify-r4-lens2-executability.md
- executability · The delta seal (step 6) is underdetermined: verifier count, judgment gate, dispatch authority, IOU sweep · 2026-07-17-reverify-r4-lens2-executability.md
- executability · The eval route both mandates and forbids its own protocol file; the preamble sweep's agent is unassigned · 2026-07-17-reverify-r4-lens2-executability.md
- altitude † · Exemplar tier designators inline in binding documents — six files · 2026-07-17-reverify-r4-lens3-altitude.md
- altitude · grammar.md §4.11 makes the emitted studio.md depend on "U-lines" · 2026-07-17-reverify-r4-lens3-altitude.md
- altitude · phases/emission.md restates the command list its declared owner holds — and the restatement drifted · 2026-07-17-reverify-r4-lens3-altitude.md
- altitude · Gate and spot-verify tier values restated in three phase files against the declared single owner · 2026-07-17-reverify-r4-lens3-altitude.md
- judgment · eval-run dispatch: the eval run itself has no templated brief, no preserved dispatch prompt, and no defined way to learn it is under eval; the exclusion list lives chiefly in the excluded file; binding docs invite the read (emission's optional-calibration pointer) · 2026-07-17-reverify-r4-lens4-judgment.md

## From 2026-07-17-reverify-r5-*.md

- consistency · The delta seal's declared verifier package contradicts the verifier checks and taxonomy rule it imports · 2026-07-17-reverify-r5-lens1-consistency.md
- consistency · Verifier check 1 names artifacts that do not exist on the delta path · 2026-07-17-reverify-r5-lens1-consistency.md
- consistency · The architecture delta's operator gate has no gate-copy · 2026-07-17-reverify-r5-lens1-consistency.md
- consistency · The tier-L taxonomy assembly rule directs an eval run into `verdicts/` · 2026-07-17-reverify-r5-lens1-consistency.md
- consistency · `phases/emission.md` mis-scopes the eval exclusion · 2026-07-17-reverify-r5-lens1-consistency.md
- executability · Architecture spot-verify cannot be dispatched legally with its own mandated lens: step 10 names ideation coverage, whose briefed procedure requires the ideation file, but phase 2's input list explicitly excludes the raw ideation and rule 4 forbids adding to the package · 2026-07-17-reverify-r5-lens2-executability.md
- executability · Delta step 6 imports phase-6 duties its declared package and procedure cannot pay: no specai NOTES.md (check 3 + §5.4's delta collector), no taxonomy at L (§2 rule 1), no NOTES seed / non-delta baselines (check 1's named artifacts), no templates/; and the package names "spot-verify records" no delta step produces — step 2 omits the spot-verify, so check 2's expected count has no derivable answer for a delta · 2026-07-17-reverify-r5-lens2-executability.md
- executability · The emitted-repo commit discipline has no emitted home: change_rule §4 binds "emitted-repo builders never commit except under an explicit, gated standard … never by default" and claims instantiation "via `templates/start.md`" — but the template contains no occurrence of "commit" · 2026-07-17-reverify-r5-lens2-executability.md
- altitude · Unclosed parenthetical garbles the seal verifier-package enumeration · 2026-07-17-reverify-r5-lens3-altitude.md
- judgment · eval path: SKILL §5's run-closing duties are unsatisfiable under eval hygiene; no carve-out exists · 2026-07-17-reverify-r5-lens4-judgment.md
- judgment · M/L gate baselines are collected but never inspected: fenced check 1 names only the definition artifacts; no check diffs the sealed architecture.md or contract standards against gates/architecture/ and gates/contracts/ · 2026-07-17-reverify-r5-lens4-judgment.md
- judgment · gate-weight asymmetry: the seal-operating text (phase-6 package, fenced checks, delta step 6) is functionally equivalent to the paneled surfaces but gated at a single focused pass with the typo/clarity exemption intact — a one-verifier or "clarity" edit could drop the eval carve-out or a check · 2026-07-17-reverify-r5-lens4-judgment.md

## From 2026-07-17-reverify-r6-*.md

- consistency · verification_core.md §4 (M row) vs phases/verification.md: the tier-M default lens split omits buildability, a lens phase 6 calls decisive · 2026-07-17-reverify-r6-lens1-consistency.md
- consistency · phases/delta.md step 6's lens enumeration conflicts with the phase-6 lens apparatus it imports "in every duty" · 2026-07-17-reverify-r6-lens1-consistency.md
- executability · verification_core.md §4 L row: no templated lens allocation and no rule that the panel's union must cover all applicable lenses — the dispatcher is forced to invent the split, exactly the discretion rule 4 forbids · 2026-07-17-reverify-r6-lens2-executability.md
- executability · phases/delta.md step 1 vs fenced check 2: the definition delta mandates no spot-verify, but the check derives an expected record for every re-run phase — at a tier-L delta, a guaranteed false finding or an undeclared duty · 2026-07-17-reverify-r6-lens2-executability.md
- executability · the delta architecture spot-verify cannot be dispatched as written · 2026-07-17-reverify-r6-lens2-executability.md
- judgment · the tier-L per-run taxonomy has no enforcement surface, and the cheat is invisible even in the commit-time diff (escapes the recorded acceptance) · 2026-07-17-reverify-r6-lens4-judgment.md

## From 2026-07-17-audit-*.md (post-seal)

- consistency · Comms-matrix arrival tier contradicts across grammar §4.2 / grammar §5 / dial §2; grammar §5's L cell is a garbled enumeration · 2026-07-17-audit-lens1-consistency.md
- consistency · Design-spec binding enumeration restated by the template disagrees with its owner (drops "motion intent"), and the template is the author's only source · 2026-07-17-audit-lens1-consistency.md
- consistency · phases/architecture.md's procedure cites reference/exemplars.md, but its closed Inputs list doesn't declare it · 2026-07-17-audit-lens1-consistency.md
- consistency · Delta spot-verifies assign change-request coverage but never hand the verifier the change request · 2026-07-17-audit-lens1-consistency.md
- executability · The architecture-delta spot-verify mandates the change-request coverage lens but its zero-discretion package cannot contain the lens's primary source · 2026-07-17-audit-lens2-executability.md
- altitude · The emitted-world money gate hangs on terms defined only in a factory file the authoring phase may not read and the emitted repo never receives · 2026-07-17-audit-lens3-altitude.md
- altitude · Canonical-term collision: README's layout line calls SKILL.md "the dispatcher", colliding with the tree-canonical dispatcher (verifier-launching) on a trust seam; style rule 1 classes a two-meaning term blocker-class · 2026-07-17-audit-lens3-altitude.md
- judgment · Eval close-out text is outside the panel gate its own class rule demands · 2026-07-17-audit-lens4-judgment.md
- judgment · Gate-copy tamper evidence fails open on absence · 2026-07-17-audit-lens4-judgment.md
- judgment · The delta coverage lens lacks the main path's anti-laundering hardenings: no reverse-provenance leg, and any-mark non-goal accepted as a sink (the main row requires revisitable) · 2026-07-17-audit-lens4-judgment.md
