# TEMPLATE — components/<name>_spec.md (grammar §4.5 · style.md applies)

> Authoring notes in blockquotes; delete them. Reference instance for the **run lead's**
> calibration only: the tier-S exemplar's strongest component spec (named in
> `reference/exemplars.md` §1) — it is NOT part of a phase-4 author's closed input list. Authors
> work from this template and their declared inputs alone.
> The design spec uses this same shape with the intent-vs-binding split: **appearance (the
> current visual identity) is replaceable intent; layout shape, theming behavior, interaction
> patterns, the accessibility floor, and motion intent are binding behavior** (grammar §4.6 is
> the provenance).

# <Product> — <Component> — <one-line scope: the surfaces/behaviors this spec owns>

**Status:** Authoritative for <component>. **Read first:** <architecture.md §§, the contract
standard §§ it implements/consumes, the design spec if UI, vision §pillar it serves>.

**Scope of this spec.** <What it owns, in one paragraph — the behaviors, surfaces, and rules.>
**Not this spec.** <Each adjacent concern → the sibling/standard that owns it. Resolve every
boundary here, in the header. E.g. "the wire shape is `<contract>.md` §n — referenced, never
restated here.">

## 1. Why this exists
> 1–2 paragraphs tracing to vision pillars; name the load-bearing consequences every rule below
> serves. If a component can't say why it exists, phase 2 made a mistake — file it back.

## 2. Glossary additions
> Reuse `architecture.md` §2 terms verbatim (name the ones you lean on). Add ONLY genuinely new
> terms, in a table. Most components add ≤3.

## 3..n Behavior sections
> The body: numbered sections, one per behavior area, ordered by the component's own logic
> (data-in → transformation → surfaces → dialogs, or whatever fits). Discipline:
> - Mark contractual sections **(binding)** in the heading.
> - **Worked examples as binding test cases** wherever a transformation has a right answer —
>   fenced input→output, labeled binding.
> - UI surfaces: enumerate controls + interactions + states as behavior tables ("Control →
>   Behavior"), including empty/loading/error states, keyboard access, and dismissal rules.
>   No pixels/colors/timings — cite the design spec.
> - Cite contracts and the data model; never restate them.

## n+1. Behavioral invariants
> Numbered rules the component must uphold across all states — the always-true sentences a
> verifier can attack (invented examples: "the draft view equals the published output",
> "reading a report mutates nothing").

## n+2. Risk & failure considerations
> Component-local risks: untrusted input on this path, degradation choices (what fails soft and
> what fails loud), size/rate bounds. Whole-product risk lives in the engineering standard — don't
> restate it.

## n+3. Open questions
> Genuinely unresolved product choices, stated as questions with the alternatives — flagged for
> the operator, never silently decided (style.md rule 7).

## Acceptance Criteria
> Checklist — each item phrased so a skeptical verifier can refute it against the running
> product/spec, citing the section it tests. Cover every binding section and invariant.

## Deliverables checklist
> Checklist — what must exist when this component is built (engines, surfaces, dialogs, tests for
> the binding examples). Phase-4 authors write it; `develop` builders live by it; the DoD reads it.
