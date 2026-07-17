# NOTES — specai decision ledger (founded 2026-07-11)

The operator's record of what was decided and why. A record, not a spec — the `standards/` and
`phases/` files win. (specai eats its own dog food: this is the `templates/notes.md` discipline
applied to the factory itself.)

## Founding (2026-07-11) — Kaveh + Fable

**What this is.** The modernization of `../ai-it` (2025, Roo-based, 48 prompts / ~13.8K lines,
idea→code) into a harness-agnostic skill that emits **self-operable spec repos** of the
feedler / trading-platform class. Full source study preceded this: all of ai-it's `all.md` (16,692 lines)
plus `.roomodes`/README/Makefile/history posts; feedler read in full; the trading platform's process docs read in full (its content already
deeply known).

**Founding decisions (each with its live home):**

1. **Emit the genome, not the organism.** specai ends at a sealed spec repo; `develop` belongs to
   the emitted `start.md`. Kills ai-it's spec+code co-evolution cascade. → `SKILL.md` §0, §2.
2. **Phases cut by information boundary, not token budget.** Requirements+domain+stories merge
   into one Definition pass (the 2025 split was a 200K-context artifact); architecture, contracts,
   component authoring, and verification stay separate because isolation is the point, not because
   context is small. → `phases/*`, each with a closed input list.
3. **Specs absorb their intermediates.** No PRD/domain/stories docs in emitted repos — vision +
   architecture (glossary, lifecycle stories) + component specs carry them, as both exemplars
   already do. The factory-side requirements inventory is working material; phase 6 verifies its
   full absorption. → `grammar.md` §3.4, `phases/definition.md`.
4. **Consumer-driven contracts, hardened.** ai-it's consumer_expand kept whole (top-down walk,
   annotated demands, ~80% harmonization, no speculation) and fused with the 2026 rule that a
   finished contract is a versioned standard with migration notes. → `phases/contracts.md`,
   `templates/contract_standard.md`.
5. **The dial sizes product AND process.** ai-it's 0–10 scoring kept (money/regulatory round up);
   bends the grammar (`grammar.md` §5), the emitted process docs, verification depth, and operator
   tempo. Calibration: feedler=2/S, the trading platform=10/L. → `standards/dial.md`.
6. **Quality cell defined once.** draft → self-review-in-update-mode (ai-it's trick, kept) →
   fresh verify → fix loop → seal; phase files never restate it. Roughly half of ai-it's line count
   was this cell restated eleven times — dropped. → `verification_core.md` §3.
7. **Verification = the trading platform's practice, genericized.** Judge/judging separation, fresh
   contexts, spec-first derivation, tiers, lens set (+ two factory-specific lenses: ideation
   coverage, buildability/rebuild test), zero-open-blockers/majors PASS, operator countersign.
   ai-it's roo-man survives as the judgment gate ("is it good?" may fail conforming work).
   ai-it's completeness checklists demoted to the mechanical pass. → `verification_core.md`,
   `phases/verification.md`.
8. **Preferences dissolve into the change rule.** Durable decisions live in specs; NOTES keeps
   history; operator engineering defaults arrive with the ideation or via checkpoint (recorded in
   the emitted NOTES). No parallel directive store. ai-it's current-state-not-history rule survives
   inside NOTES discipline. → `change_rule.md` §1, `templates/notes.md`.
9. **Harness-agnostic by files-as-interface.** Roles are briefs, not Roo modes; every phase I/O is
   a file; delegation isolated in one section with a stated degraded floor (single-context runs
   must disclose degraded verification independence). → `SKILL.md` §4.
10. **User-input checkpoints kept** (one batched set, proposed defaults, first run) and given a
    tempo: operator gates at Definition + seal (always), + Architecture (M/L), + Contracts (L).
    → `phases/definition.md`, `dial.md` §3.
11. **Router kept as the single front door** — including for the skill itself; security classified
    by where the fix lives; ai-it's Level 1–11 table replaced by classify-to-owning-artifact +
    the repo's concrete cascade graph. → `change_rule.md` §2–3.
12. **Both exemplars preserved their ideations → they are the eval fixtures.** L1 = reproduce
    feedler; L4 = reproduce the trading platform; judged on grammar conformance, ideation coverage, decision
    quality, buildability — never byte similarity. → `reference/exemplars.md` §3.
13. **Operator commits; specai never runs git mutation.** The commit is the countersign
    (Kaveh's standing rule, made doctrine). Automated commits exist only as an explicit emitted
    standard (develop_loop class), never a factory default. → `SKILL.md` §0.

**Deliberately dropped from ai-it** (recorded so no future "restoration"): per-phase orchestration
boilerplate; prescriptive code-structure/framework tables in guidelines (WHAT/HOW violation —
engineering defaults are the operator's, named once in the emitted engineering standard);
`PREFIX-XX-3CHAR` IDs as a default (tier-L-only option; named-section citations proved sufficient
at 7K lines); Roo mode mechanics; the standalone visual/post/present tooling (out of scope for the
factory).

**Deferred (open):**
- **speclint-for-emitted-repos**: a mechanical script for `grammar.md` §6 (a seed speclint
  already exists in the trading platform's private repo; generalize when the first
  emitted repo exists to test against). Until then phase 6 pass 1 runs by hand.
- **L1 eval run** (reproduce feedler) — the next milestone; then L4.
- Whether emitted tier-M/L repos should also get a `develop_loop.md` by default (currently
  "offered"); decide after L1.
- Skill packaging polish (frontmatter metadata beyond name/description) once the first
  harness-installed use happens.

**Verification status of this founding tree:** self-review pass done (lead); independent
fresh-context verification **pending** — per our own doctrine this founding batch should get a
panel review before heavy use; the L1 eval run doubles as its live-fire test. Operator countersign
= Kaveh's first commit of this repo.

## 2026-07-11 — L1 eval: reproduce feedler — PASS (class parity, locally exceeded)

*(Superseded 2026-07-17: relabeled per the hardened eval protocol — the honest verdict is
"comparison passed; build-proof pending"; the run pre-dated eval hygiene: the target exemplar was
readable and the comparison was self-dispatched. `reference/exemplars.md` §3.)*

**The run** (same day as founding — the skill's first full engagement): dial scored 2 → tier S,
matching the calibration anchor exactly. Six isolated component authors, four blind verification
rounds (majors 4 → 1 → 1 → 0; zero blockers ever; every binding worked example independently
recomputed at least twice), operator-sealed and countersigned in the
specai-feedler repo (github.com/kavehmz/specai-feedler) (4,113 spec lines from a 27-line ideation; the hand-built
reference is ~4.1K). Full audit trail in that repo's `.specai-run/`.

**Comparison verdict** (`.specai-run/verdict-comparison-L1.md`): headline **YES**. Grammar
conformance: candidate EXCEEDS (it hits the written grammar more exactly than the hand-built
exemplar the grammar was extracted from). Ideation coverage: PARITY, zero silent losses either
direction (the two capability deltas — full-text, search — are recorded checkpoint answers,
input-attributable). Decision quality: parity leaning exceeds (candidate stronger on security
posture, contract discipline, identity/dedup rules, cold deep-links, bound mobile behavior;
reference richer on export surface and carries build-proven maturity). Buildability:
parity-to-exceeds on paper — **the integration proof (actually building the emitted tree via its
own start.md) is still owed** per exemplars.md §3.

**Process learnings — to apply via `improve specai`:**
1. Rationale-placement rule → `style.md`: binding specs trace rationale to `vision.md`, never to
   the non-normative ideation (one instance emitted).
2. Benchmark-behavior checkpoint → `phases/definition.md`: when an ideation names a benchmark
   ("like Reeder on iOS"), surface the benchmark's signature behaviors as checkpoint questions.
3. Fixture-math discipline held (attached artifacts → verified binding fixtures) — name it
   explicitly in `phases/definition.md`.
4. Riding-minors seal policy → `verification_core.md` §6: minors riding a PASS fold into the
   emitted NOTES open topics at seal (done this run by judgment; make it the rule).
5. Tier-S traceability stub → `phases/emission.md`: a one-table "ask → owning §" appendix in
   emitted NOTES makes phase-6 and eval tracing cheap.
6. `exemplars.md`: name the emitted shell's placement/semantics/appearance three-way split as an
   imitation pattern (it out-performed the reference's decomposition).
7. Harness learnings → `SKILL.md` §4: (a) sub-agent→parent reply channels proved unroutable in
   Claude Code — the orchestrator relays; files stay the truth (held up across ~10 relays);
   (b) background-agent transcripts do not survive a conversation branch — disk-state resume is
   the recovery (validated twice more, incl. a mid-phase usage-limit kill); (c) **the harness
   injects the cwd project's CLAUDE.md into every subagent** — verifiers disclosed it unprompted;
   benign here, FATAL for the L4 trading-platform eval: **eval runs must launch from a neutral working
   directory** (binding note for L4).
8. speclint materialized unprompted: the run lead built `speclint.py` (+ a factory-id guard) to
   run grammar §6 — harvest it as specai's own deferred tool.

**Next:** the integration proof (`develop feedler` through the emitted repo's own start.md);
an `improve specai` pass applying items 1–8; then the L4 trading-platform reproduction (neutral-dir
rule binding). Seal bookkeeping precedent recorded: when the run lead is unreachable at seal time, the
orchestrator performs the NOTES stamp from verdict records — registrar work, disclosed in the
run journal.

## 2026-07-12 — Operator review: the large-change path

Kaveh's question while reviewing the blog draft: in ai-it, one front door took "I need this large
change" and re-entered the pipeline at the right phase (router → e.g. architecture → cascade →
code). Where does that live after the split?

**As designed, relocated into the emitted repo:** `templates/start.md` §3 case C + §5 give every
emitted repo the router (classify to the owning artifact, `change_rule.md` §2) and the concrete
cascade graph; code follows via case B reconciliation ("spec changed, spec wins"). Verified in the
field: the emitted feedler `start.md` carries it, and the GPT builder obeyed it.

**Gap he exposed, closed same day:** the factory-side re-entry for product-reshaping changes was
a placeholder row. Now designed as `phases/delta.md` — the **delta engagement**: affected phases
re-run in update mode against the sealed tree (definition delta with operator gate → architecture
delta → contracts delta with **mandatory** version bumps → isolated authors, changed components'
authors additionally receiving their own existing spec → emission reconcile → delta verification →
operator seal). Never regenerates untouched specs; honors NOTES deliberate cuts; code follows via
the repo's own case-B develop. ai-it's update-mode, ported to the factory. **Unexercised** — first
real exercise expected at L4. `SKILL.md` map + routing updated. Top-tier verification of this
standard change rides the founding tree's pending panel review.

Naming note: the emitted entrypoint stays the **operating manual** — ai-it's "orchestrator"
describes only the routing half of what it does (it also teaches: philosophy, QA layers, DoD).

Follow-up same day: `templates/start.md` case C gained the hand-back clause — an emitted repo
recognizes reshape-scale requests, stops, and returns them to the operator for a delta engagement
(soft reference to "the factory that emitted this repo, or its successor"; no path or tool
dependency — absent any factory, the repo can still reshape itself via its own `edit specs` /
`new component` sessions). feedler, emitted before this clause existed, can adopt it through its
own change process.

## 2026-07-17 — The divergence ledger (DRIFT.md) joins the grammar

**Gap, exposed by a week of operating a production spec-first monorepo** (the operator's CS-AI
platform, which practices this doctrine at team scale): the factory had no home for
**code-vs-spec divergence as durable state**. `style.md` banned bug diaries from specs (correctly)
but named no destination; `start.md` case B's reconciliation list was session-scoped; NOTES is
append-only history. In live team use divergence is persistent state — dev-owed fixes, cross-team
decisions pending, verification findings accepted with reason — and conversation history is not a
truth store. That production repo's per-service `DRIFT.md` convention ("SPEC says what *should*
be; DRIFT says what currently *isn't*") is the direct source.

**Decision:** emitted repos gain `DRIFT.md`, the divergence ledger — a record, not a spec:
non-binding, dated, grouped per component, each item naming the divergence + owning spec § + fix
owed; **deleted item-by-item when fixed, deleted entirely when empty** (absence asserts
conformance); **never built from by a rebuild**. Dial-sized like everything else: one root file at S/M
(per-component headings), may split per component at L when the one file strains (length, edit
contention, ownership). Never emitted at seal — no code exists; born at the first divergence a
session cannot resolve. Three tenses: specs = what is true · NOTES = why decided · DRIFT = where
reality lags.

**Homes:** `grammar.md` §2 layout / new §4.10 / §4.3 summary / §5 dial row / §6 check 7 ·
`change_rule.md` §1 · `style.md` §2 rules 4 + 7 · `verification_core.md` §6 ·
`templates/start.md` §1.3, §3B, §4, §5, §6 · `templates/notes.md` header · `phases/delta.md`
inputs, step 5, outputs · `phases/emission.md` outputs note · `phases/verification.md` pass-1
paraphrase · README (three-tenses line). No files added to the skill itself → `SKILL.md` map
unchanged.

**Decision added in review (was a gap):** a spec change awaiting implementation **is** drift — an
`edit specs` session that knowingly moves the spec ahead of the code records the divergence in
`DRIFT.md` before it ends; spec edits also re-point/moot DRIFT items whose owning §s they move
(the in-repo mirror of the delta engagement's step-5 duty).

*(Superseded same day: the full standards panel below ran after this change landed — see the
2026-07-17 panel entry.)*

**Verification status:** two same-day fresh-context review rounds ran pre-commit, both dispatched
by the author — self-QA per `verification_core.md` §2 rule 4, **not** the gate. Round 1 (one
verifier, all lenses): FAIL — 2 majors (the §6 seal check contradicted delta re-seals; emitted
repos, which never receive `grammar.md`, weren't handed DRIFT's full shape/non-binding status) +
9 minors; fixes applied. Round 2 (two fresh verifiers, split lenses, blind to round 1 per §3):
FAIL — 2 new majors (verification_core §6's built-product routing was incompatible with §4.10's
owning-§ item shape for §-less polish minors; the emitted repo's everyday `edit specs` path had no
DRIFT re-pointing duty, only the rare delta path did) + minors and the spec-ahead-of-code gap
above; fixes applied. **Round-2 fixes are themselves unconfirmed by a fresh re-run** (§3's own
rule); the pending independent top-tier verification is the confirming gate — it rides the
founding tree's pending panel review alongside the delta engagement. Round-2 judgment note for the
operator: this is the third consecutive standards change to defer the pre-landing gate to the
panel review — either exercise the panel or amend `change_rule.md` §5 to name the deferral path.
feedler, sealed before this existed, can adopt it through its own change process. Operator
countersign = Kaveh's commit of this change.

## 2026-07-17 — The founding panel review ran: unanimous FAIL, fix loop deferred

The operator dispatched the full standards panel over the whole skill at `1af9e4e` — paying the
pre-landing gate deferred by the founding tree, the delta engagement, and the DRIFT change. Four
fresh-context verifiers, distinct lenses (consistency/contract · executability · altitude/style ·
judgment+adversarial), blind to the authoring sessions and to each other.

**Verdict: FAIL on all four lenses — zero blockers, ~24 deduped majors, ~23 minors.** The full
record: `verdicts/2026-07-17-standards-panel.md`. The majors cluster: the practice not binding
itself (dispatch legitimacy, the §5 gate, degraded-disclosure durability, harness contamination,
the eval protocol); founding consistency debts (engineering-standard ownership, seal/tempo term
overloads, verdict-record tier contradiction, unnamed working files, map rot, private-exemplar
tiebreaker); and two design findings (money/reg machinery keyed to tier not dimension; no mid-run
dial re-score). What held up everywhere: the phase cuts, the DRIFT lifecycle, gates fail closed,
template discipline, this ledger's honesty.

Six findings need operator design decisions before the fix loop:
`verdicts/2026-07-17-operator-decisions-D1-D6.md` (plain-language packet). **Fix loop deferred by
the operator to a fresh session** — resume by reading the two verdicts/ files; the resolution log
in the verdict record is the work list; blind re-verification per `verification_core.md` §3
follows the fixes; the operator's countersign closes.

Map updated (`SKILL.md` §1: verdicts/ added). Operator countersign of this record = the commit.

## 2026-07-17 — D1–D6 decided; fix loop unblocked

The operator resolved all six panel design decisions in a fresh session (independent of the
authoring sessions and the panel; it concurred with the session lead's yes-to-all-six and adjusted
four). All six accepted in adjusted form — full resolutions with fix homes appended to
`verdicts/2026-07-17-operator-decisions-D1-D6.md` (now the binding work order alongside the panel
record's resolution log). In one line each: **D1** review weight keyed to target doc (1 verifier
for standards edits; panel for the self-governing surfaces; deferral becomes a named IOU; this
panel pays the three old ones) · **D2** money machinery keyed to the reg/money dimension scoring 2,
re-score generic to any dimension · **D3** independence = channel (fresh context + declared package
+ templated brief); lead dispatches with zero discretion; operator dispatches seal + specai reviews
· **D4** tier binds in `vision.md`; non-goals split into identity vs revisitable-cut classes ·
**D5** eval excludes the target exemplar only; operator-dispatched comparison; no PASS without
build-proof; L1 relabeled honestly · **D6** licensed-HOW exception scoped by the template's
sections, cited not restated.

Remaining: the fix loop over the panel's ~24 majors (+ minors), then blind re-verification per
`verification_core.md` §3, then the operator countersign. Operator countersign of these
resolutions = the commit.

## 2026-07-17 — The fix loop ran: panel findings fixed, round-1 blind re-verification FAILed, round-2 fixes applied

Same session as the D1–D6 resolutions, operator-ordered ("go"), run lead as mechanical proxy.

**Round 1 (the panel's findings):** every major (~24), all 23 minors, and three judgment items
(J-emphasis, J-defaults, J-neglect) fixed per the D1–D6 work order; per-finding evidence in the
panel record's resolution log (`verdicts/2026-07-17-standards-panel.md`). J-M-anchor and
J-S-proportionality accepted (recorded there).

**Blind re-verification, round 1** (four fresh verifiers, panel lens split, `verdicts/` excluded
from packages; first dispatch was killed by a harness usage limit and relaunched clean —
disk-state resume held): **FAIL ×4 — 1 blocker, ~29 majors (deduping to ~20), ~27 minors.** The
blocker was this ledger lagging the fixed tree mid-session (entry owed before re-dispatch — the
lesson: **the NOTES entry lands with the fixes, not after their verification**; adopted as
practice, this entry is its first instance). The majors clustered: eval answer-key facts embedded
in binding docs (quarantined to `reference/exemplars.md`, which eval runs now exclude); tier-S
verdict-record/disclosure gaps (records now written at every seal, committed by default);
engineering-standard inline-path incoherence (phase 3 now writes it in every case); the money
section and regulatory register invoked but undefined (now defined: grammar §4.2/§4.11,
architecture template §7b, definition REG-lines); self-change gate holes (templates,
SKILL §4–§5, exemplars.md now gated; IOUs got a collector at seals/evals; degraded seals now owe
an IOU); a coverage-lens cheat via NOTES-only cuts (cuts now count only in vision.md);
author-asserted cascade sets (now derived from the citation graph); working-file gaps
(consumer-ledger.md, journal.md, slices/design.md named). All round-1 findings and resolutions:
the verdict record's round-1 section.

**State at this entry:** round-2 fixes are applied; round-2 blind confirmation (four fresh
lenses) is dispatched and pending. Accepted without fix (operator, via the session's standing
order): lens-4 minor "nested-parenthetical prose density" — style debt for a future altitude
pass, does not change behavior. The engagement closes with the round-2 verdict and the operator's
countersign; this entry is truthful as of dispatch, and the round-2 outcome gets its own entry.

## 2026-07-17 — Round 2 returned FAIL ×4; round-3 fixes applied; **IOU recorded**

Round-2 blind confirmation returned FAIL on all four lenses — 1 blocker (the eval answer-key
quarantine was incomplete: identifying facts survived in six binding files; found independently
by three lenses), ~18 deduped majors, ~29 minors. The raw verifier reports are preserved verbatim
(new rule, adopted and practiced this round): `verdicts/2026-07-17-reverify-r2-lens*.md`; the
findings→resolutions map is the panel record's round-2 section. Round-3 fixes are applied across
the tree — the quarantine completed (grammar, four templates, emission, SKILL routing, echoes),
evals now also exclude specai's own NOTES.md (this file carries fixture answer keys), the
judgment-gate/eval briefs joined the conforming-brief rule, the taxonomy got a defined mechanical
transform + cross-run seed file, gates got tamper-evident copies (`<run-dir>/gates/`), the
coverage lens got the reverse-provenance check, spot-verifies now write records, cascade
derivation went bidirectional, "a gate has run only when its verdict is returned," and specai
never commits, ever.

Two structural learnings, recorded as practice: (1) verifier reports are preserved verbatim as
files from now on — the lead's dedup cites, never replaces them; (2) per lens 4's judgment
summary, the remaining risk class is concentrated: the run lead wears every hat, so the correct
fixes are operator-visible tamper-evident surfaces (gate copies, raw reports, durable records,
enumerated collectors) rather than more lead-maintained rules — this round added exactly those.

**IOU (change_rule.md §5 rule 4):** change = the round-3 fixes (this entry's tree) · owed gate =
blind confirmation, four fresh lenses, verdicts returned · anchor = before this engagement's
countersign (no seal or eval may run before it is paid). Round-3 confirmation is dispatched; its
returned verdicts pay this IOU and get their own entry.

## 2026-07-17 — Round 3 returned FAIL ×4; two ledger corrections; operator triage requested

Round-3 blind confirmation: FAIL on all four lenses — 3 deduped blockers, ~21 deduped majors
(raw reports verbatim at `verdicts/2026-07-17-reverify-r3-lens*.md`; findings map in the panel
record's round-3 section).

**Two corrections to this ledger's own prior entries (the verifiers caught both):**
1. The previous entry's claim "the quarantine completed" was **false** — `README.md`'s invocation
   examples still name the tier-S fixture (missed by the sweep), and four fuzzy echoes survive
   (architecture's decomposition shapes, definition's product-category example, the vision
   template's pillar example, dial's preamble). The quarantine is incomplete until those land.
2. The IOU above is written in a defective letter: §5 rule 4 says an IOU is paid "by the owed
   gate's verdict **returning**" — under which a returned FAIL pays the debt. The intended and
   correct reading, binding for this IOU: **payment = the gate closing** (PASS, or FAIL resolved
   per verification_core §6). This IOU therefore remains **open**: three FAIL verdicts have
   returned and none has closed.

**State:** the letter/quarantine/enumeration finding classes are objective and lead-fixable. The
trust-root class (gate baselines the lead can rewrite, packages lead-asserted, collectors
lead-fed, the integration proof self-graded at S) is fixable only by adding **operator duties**
(gate-time commits of baselines, eval input staging, operator-dispatched build proofs) or by
operator-accepting the residual trust with recorded reason — a design decision the operator must
make (D1's lesson: a rule the operator won't live by is a bad rule). Triage requested; the fix
loop resumes on the operator's decision.

## 2026-07-17 — Operator triage: two eval duties adopted, gate-commit ceremony declined; round-4 fixes landed

The operator chose **triage & close**. Adopted into the standards: **eval staging** (operator
stages eval inputs and a scrubbed taxonomy; `verdicts/` joins the eval exclusion — exemplars §3
rule 2) and **eval build-proof dispatch** (operator dispatches the proof's verifier, which signs
the DoD line — exemplars §3 rule 4). Declined: gate-time operator commits of baselines —
**accepted with reason**: gate copies remain lead-held; the operator reviews diffs at commit
time, and the countersign commit is the operator-fixing act; per-gate commits would be ceremony
not lived by. All other round-3 findings (3 blockers, remaining majors, minors) are fixed —
per-finding map in the panel record's triage section; raw round-3 reports at
`verdicts/2026-07-17-reverify-r3-lens*.md`.

The **IOU above remains open** under the corrected payment rule (a gate closes by PASS or
resolved FAIL — `change_rule.md` §5.4). Round-4 blind confirmation is dispatched as the closing
gate; per the triage decision, judgment-class residue inside the accepted trust-root class does
not reopen the loop. Its outcome and the operator countersign close this engagement.

## 2026-07-17 — Round 4 FAILed on sibling-path enumeration; round-5 fixes landed; letter refinement disclosed

Round-4 blind confirmation: FAIL ×4 — 1 deduped blocker (my round-4 NOTES-in-package edit
colliding with eval hygiene, found independently by two lenses), ~10 deduped majors, all in one
named class: every hardening rode the main path and missed a sibling path (eval-internal seals,
delta seals, spot-verify briefs). The trust-root class **held as accepted** — the judgment lens
honored the recorded acceptance and confirmed ledger↔tree agreement. Raw reports:
`verdicts/2026-07-17-reverify-r4-lens*.md`; the findings→resolutions map is the panel record's
round-4 section.

Round-5 fixes are applied (the eval carve-out; attestation travels in the brief; fenced verifier-
checks blocks; the delta path joined every mitigation; the eval route operationalized with a
preserved templated dispatch prompt; no degraded-mode evals; the remaining echoes de-numbered).
**One disclosed design call:** the quarantine letter was refined — it now covers facts
characterizing a *specific named* exemplar and licenses tier-neutral role references, since a
target's tier is ideation-derivable by design; the round-5 confirmation verifies the refinement.
The **IOU above remains open**; round-5 confirmation is dispatched as its closing gate — its
verdicts, this ledger's final entry, and the operator countersign end the engagement.

## 2026-07-17 — Round 5 FAILed on the last mile; round-6 fixes landed; two ledger claims corrected

Round-5 blind confirmation: FAIL ×4 — 1 blocker (the delta seal's package contradicting the
checks it imports; three-lens convergence), ~9 deduped majors. **Two of the previous entry's
claims were partially false and are corrected here:** "the eval carve-out" had not reached
SKILL §5's run-closing acts, and "the delta path joined every mitigation" missed step 2's gate
copy and the check mapping. What verified clean: the refined quarantine letter (two lenses), the
eval-exclusion invariant, all canonical terms, pinned values, ownership seams, DRIFT, the IOU
letter, and the money trigger. Raw reports: `verdicts/2026-07-17-reverify-r5-lens*.md`;
resolutions in the panel record's round-5 section.

Round-6 fixes are applied — the delta seal now runs the phase-6 machinery by named substitution,
check 1 diffs everything under `gates/**`, the eval path is complete end-to-end (close-out is the
operator/registrar's; the taxonomy carve-out is in readable text), the emitted start template
carries the commit rule it had somehow never received, and the seal-operating text joined the
panel-gated class. The **IOU above remains open**; round-6 confirmation is dispatched as its
closing gate.

## 2026-07-17 — Round 6: zero blockers ×4; closing fixes applied; engagement presented for countersign

The closing round: FAIL ×4 on majors but **zero blockers on all four lenses** — first time in
the engagement. Five deduped majors, maximally convergent (the M-split buildability omission — a
round-6 edit's own defect — found by all four lenses independently). The judgment lens verified
every prior NOTES claim true against the tree; the quarantine, eval path, IOU letter, and both
ledger self-corrections all held under attack. Raw reports:
`verdicts/2026-07-17-reverify-r6-lens*.md`.

All round-6 findings are fixed (the lens-totality rule chief among them: at every tier the union
of dispatched briefs MUST equal the applicable lens set). Per the operator's standing
triage-and-close decision and their explicit in-session confirmation that round 6 is the last
round: **no seventh blind round.** The closing acceptance packet — the fixes landing on direct
diff review, the standing accepted classes, and one recorded edge — is in the panel record's
"Engagement close" section. **The operator's commit is the acceptance, the IOU's payment, and
the countersign.** Trajectory for the record: blockers 1→3→3→1→0; majors ~24→~9→5, structural →
letter-level. What this engagement leaves behind besides the hardened tree: verbatim verifier
reports as standing practice, the taxonomy seed, the exempted-edits ledger, tamper-evident gate
copies, and a process that caught and recorded its own false claims twice.

## 2026-07-17 — Post-seal audit (operator-invited): 0 blockers, ~9 majors found and fixed; IOU recorded

After the seal (`d86eec3`), the operator invited one more four-lens audit — information, not a
gate. **FAIL ×4 with zero blockers**; ~9 deduped majors, half final-wave residue, half
multi-round survivors. The two catches that justified the round: the **money-path definition
never reached the emitted world** (emitted repos gated on a term only a factory file defined —
now emitted verbatim by the architecture template §7b), and **gate-copy tamper evidence failed
open on absence** (check 1 diffed only what existed — absence now blocks like an unpaid IOU, and
gate copies join the relocation set so the diff backstop durably sees them). Everything else
held, including full ledger↔tree agreement on this engagement's closing claims. Full record:
`verdicts/2026-07-17-postseal-audit.md`; raw reports `verdicts/2026-07-17-audit-lens*.md`.

All findings fixed in this change set. **IOU (§5.4):** the fixes touch rule-1/rule-2 surfaces ·
owed gate = focused pass + panel per §5, verdicts returned and closed · anchor = before the next
seal or eval (the feedler build-proof or L4, whichever first). Operator countersign of this
audit + fixes = the commit.

## Exempted edits

*(standing heading per `change_rule.md` §5 rule 3 — one line per typo/clarity-exempted edit;
enumerated at every seal/eval preamble. Currently empty.)*
