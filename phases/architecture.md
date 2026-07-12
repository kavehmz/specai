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
   state + behavior and interacts with siblings only through contracts. Right-size to the dial —
   feedler is one deployable with seven *spec areas*; the trading platform is eight platform components plus
   products. Components ≠ deployables; the engineering standard decides deployment shape.
4. **Assign every inventory line** (R/S/U/C/X) to exactly one owning component (or to a standard /
   vision non-goal). Unassignable lines mean the decomposition is wrong — iterate. This assignment
   IS the coverage matrix (explicit table at M/L; the component table's "owns" column at S).
5. **Derive the principles**: from vision pillars (each load-bearing belief gets its enforcing
   principle), from invariant-class C-lines, and from the universal set that has earned its place —
   WHAT/HOW (always); identity→idempotency and untrusted-input rules (when state/input exists);
   one-command bring-up (when deployable); plus the product's own (feedler's "politeness to
   origins"; the trading platform's "products never call the platform back"). Number them; each is a rejection rule, not
   a vibe.
6. **Write the lifecycle stories**: the absorbed user stories, condensed into acceptance
   narratives — first run, each primary flow, failure/recovery, reset/retirement. Every S-line must
   be recognizable inside one story or a component's behavior obligations.
7. **"What this architecture deliberately does not have"**: promote the X-lines and the
   architectural negatives (no second datastore, no auth layer, …). As binding as the scope.
8. Engineering standards: inline a §6 at tier S if it fits; otherwise leave the section citing
   `standards/engineering_standard.md` for phase 4/5 to fill.
9. **Self-review**, then per the dial's tempo: fresh spot-verify (M/L) — lenses: consistency
   (glossary/inventory), altitude, and the coverage check.

## Gate
Tier M/L: operator approves the component map + principles before contracts begin (tempo rule).
Tier S: proceed; the operator sees architecture at the seal.
