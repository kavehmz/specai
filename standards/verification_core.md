# verification_core.md — The Verification Practice (generic core)

**Status:** Binding for specai's phase-6 seal and for what `phases/emission.md` instantiates into
emitted repos. (Lineage: `NOTES.md`.)

## 1. The structural idea

**Separate the judge from the judging.** A builder's blind spots are correlated — the same
misreading produces both the defect and the test that passes it. So every substantive artifact gets
an **independent second pass** by a **fresh-context** agent, and the author never grades their own
verification (dispatch legitimacy: §2 rule 4).

## 2. The independence rules (binding)

1. **Fresh context.** A verifier sees only: the relevant specs/inputs (exactly rule 4's declared
   package — never more), the artifact under review,
   its lens brief, and (tier L) the defect taxonomy. The taxonomy is a standing defect-pattern
   list at `<run-dir>/taxonomy.md`, part of the declared package and passed unchanged — never
   selected or edited per review. Its assembly is a **stated mechanical transform**, exempt from
   the author ban because it leaves no discretion: one line per closed blocker/major in a prior
   verdict record — `lens · pattern · source record`, where the pattern is a **verbatim copy of
   the source finding's issue line's first sentence, never paraphrased** — nothing else (factory
   runs: assembled by the lead at run start, tier L, from `verdicts/taxonomy-seed.md` plus
   post-seed records, deduped by source record; a first run starts empty; **eval runs never
   assemble it** — the operator stages a scrubbed taxonomy or it starts empty,
   `reference/exemplars.md` §3 rule 2; emitted repos per their instantiated standard). Never the author's conversation,
   journal, reasoning, or a prior run's report.
2. **Spec-first derivation.** The verifier derives expected behavior from the inputs *before*
   reading the artifact, then tests the artifact against its own expectations. The artifact must
   never teach the verifier what "correct" means.
3. **Adversarial posture.** The job is to refute "done", not confirm it. Findings name exact
   locations, evidence, and a concrete fix; praise is not a deliverable.
4. **Dispatch legitimacy.** Independence is a property of the **channel**, not the button-presser:
   a review is independent when the verifier starts fresh (rule 1), receives the **declared input
   package** (the phase file's input list — never a hand-picked subset), and a **templated lens
   brief** (§5 / the instantiated standard — never a brief authored ad hoc for this review). Under
   those conditions the run lead may dispatch mechanically, with **zero discretion** over what the
   verifier sees; the verdict record names the dispatcher and the package, and any deviation is
   disclosed in the verdict. A conforming brief is exactly: the applicable §5 lens row(s), plus
   the §7 judgment-gate brief where the tier requires it, or the eval-comparison brief
   (`reference/exemplars.md` §3's fenced brief) — each verbatim from its owning section — plus
   **§2 rules 2–4 verbatim** (so every verifier receives its conduct and attestation duties in
   the brief itself), the §6 finding shape and PASS rule, the file package, and — where the
   dispatching phase file carries a fenced **"Verifier checks (verbatim)"** block — that block;
   nothing else. For **mid-run spot-verifies** the scoping is mechanical, not discretion: the
   phase file's named lens rows apply to the artifacts existing at that phase — unbuilt artifacts
   are out of scope, not failures. **Attestation:** every verifier report MUST open by echoing
   verbatim the brief and file list it received (the record's package claim is verifier-attested,
   never only dispatcher-asserted), and each dispatch prompt is preserved verbatim beside the raw
   report it produced. The **operator personally
   orders** the phase-6 seal review and any review of specai itself (the lead may relay briefs as
   mechanical proxy). What satisfies no gate: a verifier fed the author's conversation, fix
   claims, or a hand-picked package — however dispatched.
5. **Observed behavior over reading** (runtime targets). Anything a user sees or does is judged by
   driving the running artifact; "looks right in the source" is not a PASS, and an undriven surface
   is UNVERIFIED — say so. (For spec trees — specai's usual target — the analog is rule 2 plus the
   executability lens: *walk* every mandated behavior through the surfaces the spec provides.)
6. **Proceed on defaults; ask only when truly blocked.** A run executes its full scope without
   asking the operator to confirm what the inputs settle. The human's moment is the verdict
   countersign, not the setup.

## 3. The quality cell (the per-artifact pipeline — defined once, used by every phase)

```
draft  →  self-review  →  [fresh verify]  →  fix loop  →  close
```

- **Draft** from declared inputs only (each phase file names them — the information boundary).
- **Self-review:** the author re-enters their own output in *update mode* — gap-analyze against the
  inputs and the grammar/style as if someone else wrote it; fix what's found.
- **Fresh verify:** per the dial's spot-verify schedule (`dial.md` §2) — every phase output gets at
  least self-review; schedule-designated checkpoints and the phase-6 seal get fresh-context
  verification.
- **Fix loop:** the author fixes; re-verification uses **fresh verifiers who never see the prior
  report** — prior learnings travel only as the taxonomy (§2 rule 1: mechanically distilled,
  passed unchanged), never as the author's fix claims. A fix that edits a **gate-approved
  artifact** (vision.md above all) re-triggers the owning phase's operator gate before
  re-verification.
- **Close:** the artifact is closed by its **owning gate** — for the whole tree, the phase-6
  **seal** with the operator countersign ("seal" names only that event); a mid-run artifact closes
  when its phase's gate passes (the operator is pulled in per the tempo rule, `dial.md` §3, not
  per artifact). No PASS, no done.

## 4. Tiers (bound to the dial)

This table owns the **emitted-repo seal** verifier counts (specai's own self-change gate weights
are `change_rule.md` §5's); the mid-run cadence is owned by the spot-verify schedule — cite
`dial.md` §2 for it, never this table.

| Tier | Phase-6 seal of an emitted repo | Mid-run spot-verifies |
|---|---|---|
| **S** | mechanical pass (`grammar.md` §6) + **1** fresh verifier running all applicable lenses (carrying the judgment-gate brief as its own verdict section — `phases/verification.md`) | per `dial.md` §2 |
| **M** | mechanical pass + **2** fresh verifiers with split lenses (the templated dispatch names the split; default: coverage + outcomes + lifecycle + **buildability** / consistency + altitude + executability + adversarial-user) + the judgment gate (dispatch shape per `phases/verification.md`) | per `dial.md` §2 |
| **L** | mechanical pass + panel of **≥3** distinct-lens verifiers (the partition is named in the operator's seal order) + the judgment gate (dispatch shape per `phases/verification.md`) + adversarial re-verify of fixes | per `dial.md` §2 |

**Lens totality (every tier):** the union of the dispatched lens briefs MUST equal the applicable
§5 set — a lens with no dispatched carrier blocks the seal.

Every seal writes a **verdict record** (§6). Every **spot-verify** writes a one-page verdict
record in the run dir, named `verdict-spot-<phase>-<date>.md`; the seal presentation enumerates
them, an absent record blocks like an unpaid IOU, and a spot-verify FAIL enters the fix loop
before the next phase begins.

Change-time gating after emission follows the emitted repo's own standard (instantiated per tier by
`phases/emission.md`).

## 5. The lens set (for verifying spec trees)

| Lens | Hunts for |
|---|---|
| **Ideation coverage** | procedure: read the ideation *first*, derive your own expectation of the product, then hunt the tree for each expectation. Every ask in `reference/ideation.md`, every checkpoint answer, **and every requirements-inventory line** traces to a binding clause **or** a revisitable non-goal in `vision.md` (a cut recorded only in NOTES is a coverage FAIL — NOTES holds rationale, never the cut); **and the reverse**: every non-goal (identity or revisitable) traces back to an X-line or a recorded checkpoint answer — an unprovenanced entry is a coverage FAIL (a cut may launder a miss; an identity entry injects unprovenanced firewall scope); checkpoint answers marked default-accepted weigh as factory assumptions, not operator choices; nothing the human asked for silently vanished |
| **Change-request coverage** *(delta engagements)* | the delta analog of ideation coverage, both legs: every line of the change request + delta inventory traces to a binding clause or a **revisitable** non-goal in `vision.md` (a cut recorded only in NOTES is a FAIL); **and the reverse**: every non-goal the delta adds or changes traces to a change-request line or a recorded checkpoint answer — an unprovenanced addition is a FAIL; nothing the request asked for silently vanished |
| **Consistency/contract** | citations resolve; glossary terms single-defined and used verbatim; pinned values agree across documents; contract shapes match everywhere they're cited |
| **Outcomes** | independently recompute every binding worked example; re-derive formulas and boundary math from the prose |
| **Adversarial-user** | abuse paths, edge inputs, failure modes, idempotency and money-safety holes the specs are silent on |
| **Lifecycle/time** | first-run, restart, retirement stories hold end-to-end; state survival and re-entry are specified, not assumed |
| **Altitude/style** | `style.md` violations: transcribed HOW, and binding claims too vague to build (the clause-level form of omitted WHAT) |
| **Executability** | walk every mandated behavior end-to-end through the surfaces the specs provide: no rule depending on a lookup that doesn't exist, no harness told to verify what no surface exposes, a builder never forced to guess |
| **Buildability (the rebuild test)** | the whole-tree question: could a fresh AI build this product from this repo alone — are the boot table, acceptance gates, and DoD sufficient to start and to know when to stop |

(For runtime artifacts the emitted repos add the visual/interaction lens — driving the running UI
over time — per their instantiated standard; that lens is about built products, not spec trees.)

## 6. Findings and verdicts

Finding shape (binding): `{where, severity: blocker|major|minor, issue, evidence, fix}`.
**Blocker** = would produce a wrong or contradictory product · **major** = will cause drift or
rework · **minor** = polish. **PASS requires zero open blockers and zero open majors** — each fixed
(confirmed by a fresh re-run of the lens that caught it) or explicitly accepted by the operator with
a recorded reason. Minors may ride, listed. Where findings land:

1. At a **spec-tree** seal, riding minors fold into the emitted `NOTES.md` open topics.
2. On a **built** product, a finding that names a spec divergence — including operator-accepted
   ones, carrying the acceptance reason and date — lands in `DRIFT.md` (`grammar.md` §4.10; an
   emitted repo's own instantiated standard cites its `start.md` §3 definition instead, never this
   grammar).
3. On a built product, §-less polish minors fold into `NOTES.md` open topics.
4. **Every seal writes a verdict record** (`verdict-<target>-<date>.md` in the factory run's
   working dir; the emitted repo's future verdicts follow its own standard). Minimum content at
   every tier: findings, resolutions, the final PASS/FAIL, **the dispatcher and each verifier's
   input package** (§2 rule 4), the verification mode (independent panel / single fresh verifier /
   degraded self-review — mirrored in the NOTES seal line, `templates/notes.md`), ambient-context
   injection disclosures, and any operator-accepted findings with their reasons. M/L add the full
   form (per-lens verdicts, re-verify trail). **Each verifier's report is preserved verbatim** as
   a run-dir file named in the record; the compiler's dedup/resolution log cites the raw reports,
   never replaces them. Records outlive the run dir: **before a run dir is deleted, its verdict
   records (raw reports included) relocate to a durable committed home** — the factory's
   `verdicts/`, or for an emitted repo a committed `verdicts/` beside `NOTES.md` — and the NOTES
   seal line cites the final path; `<run-dir>/taxonomy.md`, the preserved dispatch prompts, the
   gate copies (`gates/**`), and a delta's `change-request.md`
   relocate with the records (so the diff backstop sees them); the run's **new** defect patterns
   reach the cross-run seed via the run-closing distillation `SKILL.md` §5 owns (this rule does
   not specify a second append).
   If the operator discards a record instead, its dispatcher/package/injection facts survive
   verbatim in the NOTES seal line.

## 7. The judgment gate

Verification asks *"does it satisfy the inputs?"*; the seal also asks *"is it good?"* — one
fresh-context review at phase 6 explicitly licensed to fail a conforming tree: incoherent component
boundaries, a grammar-perfect spec for the wrong product (vision drift), an operating manual that
routes but doesn't teach, a tree that covers every ask while inverting the ideation's *emphasis*
(what the human weighted most must weigh most in the tree). This is the taste gate; its findings
are argued to the operator, who decides.

## 8. Automation note — the develop-loop pattern

For *built* products, the Builder/Gate auto-convergence loop (fresh builder reconciles code to
specs; independent gate commits only clause-grounded diffs; stops on spec defects) is the automated
form of this practice. The pattern as stated here and shaped in `grammar.md` §4.11 is normative;
the tier-S exemplar carries a reference instantiation where available (`reference/exemplars.md`
§1). `phases/emission.md` offers the loop to every emitted repo at tier S+. The loop never edits
specs and never commits a spec change; those always return to the human.
