# Phase 4 — Component Specs (bounded parallel authoring)

Each component's WHAT, written in **authoring isolation**: an author sees the contracts + its own
scope, nothing else. This is the narrow-waist law applied to the factory itself — it prevents
anchoring, keeps every spec provably derivable from its declared inputs, and makes the components
independently re-authorable forever.

## Inputs — per component author (the whole point: this list is closed)
- `specs/vision.md` (the WHY it must serve), `specs/architecture.md` **in full** (glossary, data
  model, principles, the component table — knowing every sibling's boundary is required for the
  "Not this spec" header; what is excluded is the siblings' *specs and slices*, not the map).
- The contract standards it consumes or implements (`specs/standards/*`), **including the
  engineering standard** (its config/build surfaces bind every component).
- **Its inventory slice only** — `<run-dir>/slices/<component>.md` (written in phase 2 step 4),
  passed as a path.
- `specs/design/design_spec.md` when it has UI (see ordering below).
- `standards/style.md`, `templates/component_spec.md`.
- **Not**: other components' specs, other components' slice files, the raw ideation, or any
  factory conversation. A term it needs that isn't in the glossary, or a surface that isn't in a
  contract, is a **gap filed back to phase 2/3** — never invented locally.

## Outputs
- `<repo>/specs/components/<name>_spec.md` per `templates/component_spec.md` — behavior sections
  with (binding) markers, worked examples as binding test cases, invariants, risk, open questions,
  Acceptance Criteria, Deliverables checklist.
- `<repo>/specs/design/design_spec.md` for UI products (see below).
- Gap reports back to earlier phases, if any — filed as `<run-dir>/gaps/<component>.md` (a file,
  not a message: the crash-resume story depends on it). An in-flight spec carries
  `Status: DRAFT` in its header until the integration step clears it.

## Ordering
1. **Design first for UI products** (experience-led or not — UI-bearing feature specs cite it, so
   the dependency forces the order): `design_spec.md` (component-spec shape; intent vs binding
   split per `grammar.md` §4.6) is authored before UI-bearing feature specs, which then cite it
   for appearance and own their behavior. Its author gets: `specs/vision.md`,
   `specs/architecture.md`, the engineering standard (its config/build surfaces bind the design
   too), its slice — `<run-dir>/slices/design.md` (written in phase 2 step 4),
   `standards/style.md`, and `templates/component_spec.md`.
2. Then all remaining components **in parallel** (isolated authors — subagents per the harness
   binding in `SKILL.md`). Sequential authoring in one context is permitted only at tier S with a
   tiny set (≤3 components) and is a **named degraded mode**: true isolation is impossible once
   one context has authored a sibling, so the closed input lists are honored by discipline only,
   the NOTES seed and the verdict record MUST carry "authoring isolation: degraded (sequential
   single context)", and the phase-6 consistency lens weights cross-component anchoring
   accordingly.

## Per-author procedure
1. Derive the component's obligations from its inventory slice + the lifecycle stories that touch
   it + the contract surfaces it owns or consumes. Enumerate before writing.
2. Write scope/not-this-spec first (what it owns; which sibling or standard owns each adjacent
   concern — resolve boundaries in the header, from the architecture table, not by peeking).
3. Behavior sections: every obligation as observable behavior; **worked examples (binding)**
   wherever there's a right answer; UI surfaces as enumerated controls + interactions + states.
4. Invariants; risk & failure (component-local only — whole-product risk is the engineering
   standard's); **open questions** for anything genuinely unresolved (never silently decide a
   product question — flag it).
5. Acceptance Criteria (how to refute "done") + Deliverables checklist (what must exist).
6. **Self-review** in update mode against the closed input list: every inventory line covered?
   anything cited that isn't in the inputs? any HOW? any restated contract (cite instead)?

## Integration step (the lead, after fan-in)
Read the full set **once, as reviewer, not author**: boundary seams consistent with the headers;
no term drift; gaps filed during authoring resolved (loop phases 2/3 if needed); the coverage
mapping still complete. Fix by dispatching a **fresh context with that component's same closed
input list** (author contexts do not persist), not by patching centrally — central patches
reintroduce the leakage this phase exists to prevent.
