# The Delta Engagement — re-entering a sealed repo for a product-reshaping change

**Status:** Binding. This is the factory-side path for changes too large for an emitted repo's own
change process; it is that process's biggest case, not a bypass of it. Lineage: ai-it's update
mode, ported to the factory. *(Designed 2026-07-12; not yet exercised — first exercise expected at
L4 scale.)*

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

The sealed repo **including** its specs, `NOTES.md` (checkpoint answers, founding decisions,
deliberate cuts — binding context), `DRIFT.md` when present (current known divergence is reshaping
context — a landed delta must not silently orphan or duplicate its items), and
`reference/ideation.md`; the change request verbatim; the
dial (re-scored only if the change plausibly moves it — an operator gate either way). Unlike eval
runs, a delta engagement reads the existing tree: it is maintenance, not reproduction.

## Procedure — affected phases only, in update mode

Update-mode discipline throughout (the ai-it inheritance): read what exists first; gap-analyze
against the change; touch only what the change requires; **never regenerate an untouched spec**;
preserve every conforming decision; honor NOTES' deliberate cuts (a cut is reversed only by the
operator, explicitly).

1. **Definition delta.** Judge the request against `vision.md` (non-goals are the firewall — a
   request that violates one stops here with a conformant alternative). Amend vision if the WHY
   itself changes (rare, loud). Produce a **delta inventory** (`<run-dir>/inventory-delta.md`):
   new/changed/retired requirement lines, source-tagged to the request. Checkpoint questions only
   for what the request leaves open. **Operator gate: always.**
2. **Architecture delta.** Re-enter `phases/architecture.md` in update mode: glossary additions,
   data-model changes (with migration implications named loudly), component-map changes, principle
   changes (top-tier scrutiny), coverage re-check of the delta inventory. Operator gate at M/L.
3. **Contracts delta.** Consumer-driven walk for new or changed boundaries only
   (`phases/contracts.md` §procedure, scoped to the delta). A sealed contract is presumed to have
   consumers: **every schema change bumps the version and carries a migration note** — the
   pre-seal no-bump allowance never applies here. Operator gate at L.
4. **Component deltas.** New components: full isolated authoring per `phases/component_specs.md`.
   Changed components: the same isolation, with the author's closed input list extended by exactly
   one item — the component's own existing spec — plus the delta inventory slice. Unchanged
   components are not opened.
5. **Emission delta.** Reconcile the operating manual: boot-table rows, cascade graph, README map,
   command grammar if surfaces changed. Reconcile `DRIFT.md` when present (re-point owning-§
   citations the delta moved; delete items it resolved or made moot). Append the engagement to the
   repo's `NOTES.md` (what changed, why, decisions, any reversed cuts with the operator's say-so).
6. **Delta verification & seal.** Mechanical pass over the whole tree (grammar §6 — cheap, always
   full). Fresh-context verifiers scoped to the delta plus every document the cascade touched;
   lenses: change-request coverage (the delta analog of ideation coverage), consistency across the
   old/new seam, executability of changed paths, buildability spot-walk. Fix loops per
   `verification_core.md`. **Operator seal, as ever — commit is the countersign.**

## Outputs

The updated sealed repo (specs + manual + NOTES + a reconciled `DRIFT.md` when present), the delta
inventory and verdicts in
`<run-dir>/`, and version-bumped contracts with migration notes. Code is untouched — the emitted
repo's own `develop` (case B: spec changed, spec wins) reconciles implementations afterward.
