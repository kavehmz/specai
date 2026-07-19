# The Delta Engagement — re-entering a sealed repo for a product-reshaping change

**Status:** Binding. This is the factory-side path for changes too large for an emitted repo's own
change process; it is that process's biggest case, not a bypass of it. (Lineage: `NOTES.md`.)

## 0. Route check (before anything)

A delta engagement runs only when **both** hold:
1. The operator explicitly asked specai to take the change (the emitted repo's `start.md` is the
   default front door, and its case C + cascade graph handle vision, architecture, contract, and
   component edits).
2. The change reshapes the product: new components, a new user class or boundary, a re-tiered dial,
   a decomposition change — anything whose blast radius spans multiple phases' outputs.

If (2) fails, hand the request back to the emitted repo's `start.md` and stop. Classify first via
`change_rule.md` §2, as always.

## Inputs

The sealed repo **including** its specs (`vision.md`'s non-goals and Dial line bind — the
revisitable cuts live there), `NOTES.md` (checkpoint answers, founding decisions, cut rationale —
history and context, not binding), `DRIFT.md` when present (current known divergence is reshaping
context — a landed delta must not silently orphan or duplicate its items), and
`reference/ideation.md`; the change request verbatim — preserved as
`<run-dir>/change-request.md` (relocating with the verdict records at run-dir deletion —
`verification_core.md` §6 rule 4; the run dir's location, files, and freshness rule are
`SKILL.md` §3's); the dial (re-scored only if the change
plausibly moves it — an operator gate either way, `dial.md` §1). Unlike eval runs, a delta
engagement reads the existing tree: it is maintenance, not reproduction.

## Procedure — affected phases only, in update mode

Update-mode discipline throughout: read what exists first; gap-analyze
against the change; touch only what the change requires; **never regenerate an untouched spec**;
preserve every conforming decision; honor the vision's revisitable cuts (a cut is reversed only by
the operator, explicitly, as a vision edit — `change_rule.md` §2).

1. **Definition delta.** Judge the request against `vision.md` (**identity** non-goals are the
   firewall — a request violating one stops here with a conformant alternative; a request against
   a **revisitable** cut routes as an explicit operator-confirmed vision edit — `change_rule.md`
   §2). Amend vision if the WHY itself changes (rare, loud). Produce a **delta inventory**
   (`<run-dir>/inventory-delta.md`): new/changed/retired requirement lines, source-tagged to the
   request. Checkpoint questions only for what the request leaves open. Spot-verify where the
   schedule fires (`dial.md` §2), in its delta reading (change-request coverage;
   `<run-dir>/change-request.md` **and** the delta inventory as the sources — both join the
   package). **Operator gate**
   (delta gates mirror the tempo rule, `dial.md` §3: this one always) — approved artifacts
   copied to `<run-dir>/gates/definition-delta/` (SKILL §3).
2. **Architecture delta.** Re-enter `phases/architecture.md` in update mode (its spot-verify
   step included where the schedule fires, with the delta substitutions: the full inventory →
   `inventory-delta.md` + the delta slices; ideation coverage → change-request coverage, and
   `<run-dir>/change-request.md` joins the spot-verify package; the
   ideation itself stays — it lives in the sealed repo): glossary additions, data-model changes (with
   migration implications named loudly), component-map changes, principle changes (top-tier
   scrutiny), coverage re-check of the delta inventory — assigning its lines to owning components
   and **writing their delta slice files** (`<run-dir>/slices/<component>.md`, phase-2
   conventions). Operator gate at M/L — the approved `architecture.md` copied to
   `<run-dir>/gates/architecture-delta/`.
3. **Contracts delta.** Consumer-driven walk for new or changed boundaries only
   (`phases/contracts.md` §procedure, scoped to the delta). A sealed contract is presumed to have
   consumers: **every schema change bumps the version and carries a migration note** — the
   pre-seal no-bump allowance (`phases/contracts.md` step 4) never applies here. (Where
   `phases/contracts.md`'s inputs name `slices/product.md`, the delta substitute is the sealed
   engineering standard.) Operator gate at L — approved standards copied to
   `<run-dir>/gates/contracts-delta/`.
4. **Component deltas.** New components: full isolated authoring per `phases/component_specs.md`.
   Changed components: the same isolation, with the author's closed input list changed by one
   addition (the component's own existing spec) and one substitution (its delta slice replaces
   its original phase-2 slice). Unchanged components are not opened.
5. **Emission delta.** Reconcile the operating manual: boot-table rows, cascade graph, README map,
   command grammar if surfaces changed. **If the dial re-tiered, instantiate the process standards
   and verification cadence the new tier requires** (`phases/emission.md` output 2, `grammar.md`
   §5) — a re-tier never leaves the repo running the old tier's process. Reconcile `DRIFT.md` when
   present (re-point owning-§ citations the delta moved; delete items it resolved or made moot),
   and in every case record the delta's own spec-ahead-of-code divergence per `grammar.md` §4.10
   rule 6 — one dated entry naming the engagement, code reconciliation deferred to the repo's
   `develop` (case B); create the file if absent. Append the engagement to the
   repo's `NOTES.md` (what changed, why, decisions, any reversed cuts with the operator's say-so,
   **and the phases re-run** — fenced check 2's source).
6. **Delta verification & seal — a phase-6 seal in every duty** (`phases/verification.md`'s
   dispatch authority, verifier counts per `verification_core.md` §4's tier row, the judgment
   gate, the seal-presentation sweeps, and its fenced Verifier checks all apply; this step adds
   only the delta specifics). Mechanical pass over the whole tree (grammar §6 — cheap, always
   full). Fresh-context verifiers with this declared package: **the phase-6 package
   (`phases/verification.md` — dial §2, specai's NOTES, templates/, tier-L taxonomy and all),
   with these delta substitutions**: `reference/ideation.md` → `<run-dir>/change-request.md`;
   the inventory → `<run-dir>/inventory-delta.md` + the delta slices; the consumer ledger →
   included only where step 3 ran; the NOTES seed → the
   appended repo-NOTES entry; the gate copies → `<run-dir>/gates/*-delta/`; plus the derived
   cascade set named in the dispatch (derived per `change_rule.md` §3, never asserted). The
   fenced Verifier checks apply in their delta readings (stated inside the checks). **All
   applicable `verification_core.md` §5 lenses apply** (the §4 totality rule), scoped to the
   changed set plus the derived cascade seam — outcomes over new/changed binding examples,
   adversarial-user over new/changed surfaces — with these delta readings: change-request
   coverage replaces ideation coverage; consistency runs across the old/new seam; executability
   over changed paths; buildability as a spot-walk via the repo's own `start.md` boot table.
   Fix loops per `verification_core.md`.
   **Operator seal, as ever — commit is the countersign.**

## Outputs

The updated sealed repo (specs + manual + NOTES + `DRIFT.md` carrying the delta's
spec-ahead-of-code entry — reconciled when it existed, created when it did not), the delta
inventory and verdicts in
`<run-dir>/`, and version-bumped contracts with migration notes. Code is untouched — the emitted
repo's own `develop` (case B: spec changed, spec wins) reconciles implementations afterward.
