# verification_core.md — The Verification Practice (generic core)

**Status:** Binding for specai's phase-6 seal and for what `phases/emission.md` instantiates into
emitted repos. This is the product-agnostic core of the the trading platform verification standard (v1.1),
carrying ai-it's draft→self-review→verify→judge cell inside it.

## 1. The structural idea

**Separate the judge from the judging.** A builder's blind spots are correlated — the same
misreading produces both the defect and the test that passes it. So every substantive artifact gets
an **independent second pass** by a **fresh-context** agent, and the author never dispatches or
grades their own verification.

## 2. The independence rules (binding)

1. **Fresh context.** A verifier sees only: the relevant specs/inputs, the artifact under review,
   its lens brief, and (tier L) the defect taxonomy. Never the author's conversation, journal,
   reasoning, or a prior run's report.
2. **Spec-first derivation.** The verifier derives expected behavior from the inputs *before*
   reading the artifact, then tests the artifact against its own expectations. The artifact must
   never teach the verifier what "correct" means.
3. **Adversarial posture.** The job is to refute "done", not confirm it. Findings name exact
   locations, evidence, and a concrete fix; praise is not a deliverable.
4. **Independent dispatch.** The author never orchestrates their own verifiers; the dispatcher is
   the orchestrating session or the operator. Self-dispatched verification satisfies no gate.
5. **Observed behavior over reading** (runtime targets). Anything a user sees or does is judged by
   driving the running artifact; "looks right in the source" is not a PASS, and an undriven surface
   is UNVERIFIED — say so. (For spec trees — specai's usual target — the analog is rule 2 plus the
   executability lens: *walk* every mandated behavior through the surfaces the spec provides.)
6. **Proceed on defaults; ask only when truly blocked.** A run executes its full scope without
   asking the operator to confirm what the inputs settle. The human checkpoint is the verdict
   countersign, not the setup.

## 3. The quality cell (the per-artifact pipeline — defined once, used by every phase)

```
draft  →  self-review  →  [fresh verify]  →  fix loop  →  seal
```

- **Draft** from declared inputs only (each phase file names them — the information boundary).
- **Self-review:** the author re-enters their own output in *update mode* — gap-analyze against the
  inputs and the grammar/style as if someone else wrote it; fix what's found. (ai-it's
  same-role-re-run, kept because it's cheap and catches the sloppy third.)
- **Fresh verify:** per the dial's tempo (`dial.md` §2) — every phase output gets at least
  self-review; dial-designated checkpoints and the phase-6 seal get fresh-context verification.
- **Fix loop:** the author fixes; re-verification uses **fresh verifiers who never see the prior
  report** — prior learnings travel only as distilled patterns (taxonomy/lens seeds), never as the
  author's fix claims.
- **Seal:** operator countersign. No PASS, no done.

## 4. Tiers (bound to the dial)

| Tier | Phase-6 seal of an emitted repo | Mid-run spot-verifies |
|---|---|---|
| **S** | mechanical pass (`grammar.md` §6) + **1** fresh verifier running all applicable lenses | none (self-review only) |
| **M** | mechanical pass + **2** fresh verifiers with split lenses | after Architecture |
| **L** | mechanical pass + panel of **≥3** distinct-lens verifiers + adversarial re-verify of fixes + a written verdict record | after Definition, Architecture, Contracts |

Change-time gating after emission follows the emitted repo's own standard (instantiated per tier by
`phases/emission.md`).

## 5. The lens set (for verifying spec trees)

| Lens | Hunts for |
|---|---|
| **Ideation coverage** | every ask in `reference/ideation.md` + checkpoint answers traces to a binding clause **or** a recorded deliberate cut in NOTES.md; nothing the human asked for silently vanished |
| **Consistency/contract** | citations resolve; glossary terms single-defined and used verbatim; pinned values agree across documents; contract shapes match everywhere they're cited |
| **Outcomes** | independently recompute every binding worked example; re-derive formulas and boundary math from the prose |
| **Adversarial-user** | abuse paths, edge inputs, failure modes, idempotency and money-safety holes the specs are silent on |
| **Lifecycle/time** | first-run, restart, retirement stories hold end-to-end; state survival and re-entry are specified, not assumed |
| **Altitude/style** | `style.md` violations both directions — transcribed HOW, and binding claims too vague to build |
| **Executability** | walk every mandated behavior end-to-end through the surfaces the specs provide: no rule depending on a lookup that doesn't exist, no harness told to verify what no surface exposes, a builder never forced to guess |
| **Buildability (the rebuild test)** | the whole-tree question: could a fresh AI build this product from this repo alone — are the boot table, acceptance gates, and DoD sufficient to start and to know when to stop |

(For runtime artifacts the emitted repos add the visual/interaction lens — driving the running UI
over time — per their instantiated standard; that lens is about built products, not spec trees.)

## 6. Findings and verdicts

Finding shape (binding): `{where, severity: blocker|major|minor, issue, evidence, fix}`.
**Blocker** = would produce a wrong or contradictory product · **major** = will cause drift or
rework · **minor** = polish. **PASS requires zero open blockers and zero open majors** — each fixed
(confirmed by a fresh re-run of the lens that caught it) or explicitly accepted by the operator with
a recorded reason. Minors may ride, listed — where they land depends on the target: at a spec-tree
seal they fold into the emitted `NOTES.md` open topics; on a **built** product, findings that name
a spec divergence — including operator-accepted ones, carrying the acceptance reason and date —
land in `DRIFT.md` (`grammar.md` §4.10; an emitted repo's own instantiated standard cites its
`start.md` §3 definition instead, never this grammar), while §-less polish minors fold into
`NOTES.md` open topics. At tier M/L the verdict is written as a record
(`verdict-<target>-<date>.md` in the factory run's working dir; the emitted repo's future verdicts
follow its own standard) — findings, resolutions, the final PASS/FAIL, the dispatcher.

## 7. The judgment gate (ai-it's roo-man, preserved)

Verification asks *"does it satisfy the inputs?"*; the seal also asks *"is it good?"* — one
fresh-context review at phase 6 explicitly licensed to fail a conforming tree: incoherent component
boundaries, a grammar-perfect spec for the wrong product (vision drift), an operating manual that
routes but doesn't teach. This is the taste gate; its findings are argued to the operator, who
decides.

## 8. Automation note — the develop-loop pattern

For *built* products, the Builder/Gate auto-convergence loop (fresh builder reconciles code to
specs; independent gate commits only clause-grounded diffs; stops on spec defects) is the proven
automated form of this practice — feedler's `standards/develop_loop.md` is the reference
instantiation, and `phases/emission.md` offers it to every emitted repo at tier S+. The loop never
edits specs and never commits a spec change; those always return to the human.
