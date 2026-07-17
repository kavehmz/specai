# Phase 2 — Architecture (the shape: glossary, data, components, principles)

Consumes the definition; emits the one document everything else will cite. This phase decides the
**information architecture of the product** — and therefore of the remaining factory run, since
component authors will see only what this document and the contracts expose.

## Inputs
- `specs/vision.md`, the requirements inventory, the dial (from phase 1).
- `standards/grammar.md` §4.2, `standards/style.md`, `templates/architecture.md`.
- **Not** the raw ideation (definition absorbed it; if architecture keeps needing the ideation,
  definition failed — go back).

## Outputs
- `<repo>/specs/architecture.md` per `templates/architecture.md`.
- The **component map** (the table: area → owns → spec file) — the work order for phases 3–4.
- At tier M/L: the inter-component communication sketch (who needs whom — the input hierarchy for
  the contracts phase) and the explicit coverage matrix.

## Procedure
1. **Glossary first.** Promote D-lines into canonical terms; resolve synonyms now (one term, one
   meaning, forever). This is the absorbed domain model.
2. **Data model** (if the product owns durable state): entities, identity rules, and **numbered
   binding invariants** (identity → dedup/idempotency; cascade rules; timezone/units law; ordering).
   Invariants are where inventory edge-cases become architecture.
3. **Decompose into components** by information boundary: a component owns a coherent slice of
   state + behavior and interacts with siblings only through contracts. Right-size the component
   count to the dial (scored decomposition instances: `reference/exemplars.md` — cited, never
   carried here). Components ≠ deployables; the engineering standard decides deployment shape.
4. **Assign every inventory line** (R/S/U/C/X) to exactly one owning component (or to a standard /
   vision non-goal). Unassignable lines mean the decomposition is wrong — iterate. This assignment
   IS the coverage matrix (explicit table at M/L; the component table's "owns" column at S).
   **Write the slice files**: `<run-dir>/slices/<component>.md` (each component's assigned lines,
   verbatim), `<run-dir>/slices/product.md` (operator engineering defaults + cross-cutting
   C-lines no single component owns), and for UI products `<run-dir>/slices/design.md` (the
   U-lines + the S-lines that touch a UI surface, verbatim — the design author's slice) —
   phases 3–4 hand these paths to isolated contexts.
5. **Derive the principles**: from vision pillars (each load-bearing belief gets its enforcing
   principle), from invariant-class C-lines, and from the universal set that has earned its place —
   WHAT/HOW (always); identity→idempotency and untrusted-input rules (when state/input exists);
   one-command bring-up (when deployable); plus the product's own domain principles (every real
   product grows one or two — calibration instances in `reference/exemplars.md`). Number them;
   each is a rejection rule, not a vibe.
6. **Write the lifecycle stories**: the absorbed user stories, condensed into acceptance
   narratives — first run, each primary flow, failure/recovery, reset/retirement. Every S-line must
   be recognizable inside one story or a component's behavior obligations.
7. **"What this architecture deliberately does not have"**: promote the X-lines and the
   architectural negatives (invented examples: no second datastore, no telemetry). As binding as
   the scope.
8. **Money & compliance section** (only when regulatory/money scores 2 — `dial.md` §1,
   `grammar.md` §4.2): money flows and custody/settlement rules; every REG-line of the register
   mapped to its enforcing component or principle; the audit surfaces.
9. Engineering standards: **phase 3 writes the engineering standard in every case** — as
   `standards/engineering_standard.md`, or at tier S with a small surface delivered as this
   document's engineering-standards section (template §7). This phase leaves the section as a
   one-line placeholder; phase 3 sets the final citation when it writes the standard (the testing
   floor completes at phase 5 — `phases/emission.md` output 7).
10. **Self-review**, then per the spot-verify schedule (`dial.md` §2): fresh spot-verify —
   lenses: consistency/contract (glossary/inventory), altitude/style, and ideation coverage.
   The spot-verify package is this phase's input list **plus `reference/ideation.md` and the
   full inventory** (a verifier-only addition, declared here — the coverage lens needs the
   source; the author ban on the raw ideation stands).

## Gate
Per the tempo rule (`dial.md` §3 — cited, not restated): where the gate fires, the operator
approves the component map + principles before contracts begin; approval is recorded in the
NOTES seed and the approved `architecture.md` is copied to `<run-dir>/gates/architecture/`.
Otherwise proceed; the operator sees architecture at the seal.
