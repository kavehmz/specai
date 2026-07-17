# style.md — The Spec Style (binding for every document specai writes)

**Status:** Binding. This is the working form of the WHAT/HOW doctrine; `grammar.md` defines what
documents exist, this defines how every one of them is written. Verifiers judge against it
(the altitude/style lens).

## 1. The altitude law — defects in both directions

- **Specs define WHAT; the implementer decides HOW.** Wire contracts, data models, invariants,
  formulas, state machines, named config keys, named copy, and behaviors a user relies on are
  **verbatim and binding**. File layout, function decomposition, library calls, CSS classes,
  variable names are the builder's — a spec that transcribes them is defective.
- **Omitted WHAT is a defect, equal to transcribed HOW.** If rebuilding from the spec alone would
  lose a feature, surface, interaction, state, or behavior the product is meant to have, the spec is
  incomplete. **Conciseness is never the goal; completeness of the WHAT is.** For **experience-led**
  products (the ideation's value hinges on interaction feel — it names UX benchmarks or look-and-feel
  as a primary ask), interaction design (surfaces, controls, key interactions, states) is binding
  WHAT, described as behavior — never a single impressionistic paragraph, and never pixels.
- **The one licensed HOW-document:** the engineering standard (`grammar.md` §4.7) is the sole
  document licensed to bind HOW-level choices — exactly the sections
  `templates/engineering_standard.md` defines; the template owns that enumeration (§4.7 defers to
  it) and it is not repeated here. Changing any of it is a spec change. Every other document
  stays WHAT-only.

## 2. The eleven working rules

1. **Glossary-first.** Canonical terms are defined once (`architecture.md` §glossary) and reused
   verbatim everywhere. A component spec adds terms only under "glossary additions". A term used
   with two meanings is a blocker-class defect.
2. **Contracts verbatim, implementation descriptive.** Endpoints, JSON shapes, schema columns,
   config keys, and literal output formats are quoted exactly, once, in the document that owns them;
   every other document *cites* the owner, never restates. (An invented example of the pattern:
   "The billing request contract is `wire_contract.md` §6 — do not duplicate it here.")
3. **Worked examples as binding test cases.** Wherever a transformation has a right answer (a
   payout formula, a timezone boundary, a format), give a concrete input→output example, fence it,
   and label it **binding**. These become the highest-value unit tests and the outcomes lens's
   anchors.
4. **Behavioral invariants, not bug diaries.** State the rule the system must uphold, numbered;
   never the history of a fix. Known code-vs-spec divergence lives in the repo's `DRIFT.md`
   (`grammar.md` §4.10), never in a spec.
5. **Scope / Not-this-spec headers.** Every component spec opens by naming what it owns and which
   sibling or standard owns each adjacent concern. Overlap is resolved in the header, not
   discovered in the body.
6. **Requirement language is declared and meant.** MUST/SHOULD/MAY per RFC 2119, declared once in
   `architecture.md`. "(binding)" marks sections where every sentence is contractual.
7. **Open questions are flagged, never silently resolved.** The test is whether the spec already
   answers it: an unresolved product *choice* (between two specs, or between the spec and desired
   behavior) gets an "Open questions" entry with the alternatives stated — never a quiet decision
   buried in prose; an established divergence the spec already answers belongs in `DRIFT.md`
   (rule 4).
8. **Every component spec ends with Acceptance Criteria + Deliverables checklist.** Acceptance =
   how you'd refute "done"; Deliverables = what must exist. Risk & failure considerations appear
   component-local; whole-product risk/audit/deployment live in the engineering standard (stated,
   not assumed).
9. **Traceability by name, not apparatus.** Cite `file.md §section` — precise named citations are
   the default. Stable requirement IDs per `grammar.md` §5's requirement-ID row.
10. **Patterns over instances in process docs.** Process documents (start.md, standards) speak in
    roles — "a component", "the contract", "the operator" — never in borrowed domain examples that
    a builder might mistake for requirements. (Product specs, by contrast, are maximally concrete.)
11. **Write for the rebuilding AI.** The reader has the whole repo and no conversation history.
    No "as discussed", no "for now", no reference to the authoring process. Present tense, active
    voice, one meaning per sentence.

## 3. Tone

Plain, precise, unpromotional. Numbers over adjectives. A spec never says a feature is "elegant" or
"powerful"; it says exactly what the feature does and how you'd know it's broken. Honest about
state: known gaps, deliberate cuts, and open questions are written down where a reader will hit
them.
