# Phase 4 — Component Specs (bounded parallel authoring)

Each component's WHAT, written in **authoring isolation**: an author sees the contracts + its own
scope, nothing else. This is the narrow-waist law applied to the factory itself — it prevents
anchoring, keeps every spec provably derivable from its declared inputs, and makes the components
independently re-authorable forever.

## Inputs — per component author (the whole point: this list is closed)
- `specs/vision.md` (the WHY it must serve), `specs/architecture.md` (glossary, data model,
  principles, **its own row** of the component table).
- The contract standards it consumes or implements (`specs/standards/*`).
- **Its inventory slice only** (the R/S/U/C lines assigned to it in phase 2).
- `specs/design/design_spec.md` when it has UI (see ordering below).
- `standards/style.md`, `templates/component_spec.md`.
- **Not**: other components' specs, the raw ideation, other components' inventory slices, or any
  factory conversation. A term it needs that isn't in the glossary, or a surface that isn't in a
  contract, is a **gap filed back to phase 2/3** — never invented locally.

## Outputs
- `<repo>/specs/components/<name>_spec.md` per `templates/component_spec.md` — behavior sections
  with (binding) markers, worked examples as binding test cases, invariants, risk, open questions,
  Acceptance Criteria, Deliverables checklist.
- `<repo>/specs/design/design_spec.md` for UI products (see below).
- Gap reports back to earlier phases, if any.

## Ordering
1. **Design first when experience-led:** `design_spec.md` (component-spec shape; intent vs binding
   split per `grammar.md` §4.6) is authored before UI-bearing feature specs, which then cite it for
   appearance and own their behavior. Its author gets: vision (experience philosophy), architecture,
   the U-lines, and the UI-relevant lifecycle stories.
2. Then all remaining components **in parallel** (isolated authors — subagents per the harness
   binding in `SKILL.md`; sequentially in one context only at tier S when the set is tiny, still
   honoring each spec's closed input list).

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
mapping still complete. Fix by routing to the owning author-context, not by patching centrally —
central patches reintroduce the leakage this phase exists to prevent.
