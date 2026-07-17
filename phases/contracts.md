# Phase 3 — Contracts (consumer-driven derivation → hardened standards)

The narrow waist is built here. The mechanism: **consumers write their requirements into provider
contracts**, fused with the discipline that a finished contract is a **versioned, binding
standard**. (Lineage: `NOTES.md`.)

## Inputs
- `specs/architecture.md` (component map, glossary, data model, comms sketch), the inventory
  slices (`<run-dir>/slices/<component>.md` and `slices/product.md` — operator defaults and
  cross-cutting constraints), the dial.
- `standards/grammar.md` §4.4/§4.7/§4.11, `standards/style.md`, `templates/contract_standard.md`,
  `templates/engineering_standard.md`.

## Outputs
- `<repo>/specs/standards/<contract>.md` — one per boundary where ≥2 sides must agree. The
  frontend↔backend seam **always** counts (a tier-S product's whole waist is often a single
  `api_contract.md`); a platform↔plugins seam gets its own; tier L may add a conformance-suite
  spec.
- **The engineering standard — this phase writes it in every case**, from
  `templates/engineering_standard.md`: as `standards/engineering_standard.md`, or at tier S with a
  small surface delivered as `architecture.md`'s engineering-standards section — **every section
  of the template applies** either way (the template owns the list; it is not repeated here),
  sourced from the engineering defaults in `slices/product.md`. The **testing floor** (template
  §11) is left as a marked stub — phase 5 completes it once component specs exist and the binding
  worked examples are known.
- At tier L: the **conformance-suite spec** (`grammar.md` §4.11; the operator may waive it,
  recorded in NOTES).
- The **consumer ledger** — `<run-dir>/consumer-ledger.md`, recording which consumer demanded
  which surface and why (merges included); it survives as the standard's "Consumers" appendix
  (**mandatory at M/L**, recommended at S).

## Procedure — the consumer-driven walk
1. **Order the walk top-down by dependency**: user-facing surfaces first (their needs are known —
   they come straight from lifecycle stories and component inventory slices), then each consumer
   level down, providers last.
2. **Each consumer states demands against each provider**: operation, data in/out, error cases it
   must distinguish, idempotency/ordering needs — annotated `(consumer: <component> — <purpose>)`.
   Demands are *accumulated into the provider's draft contract*, never invented by the provider.
   **No speculation:** a provider surface no consumer demanded does not exist. At tier S with one
   deployable, run the same walk with the SPA/UI as the consumer and the backend as the provider —
   the mechanism is identical, just one round.
3. **Harmonize**: near-duplicate demands (same method + resource + purpose) merge into
   one surface serving all consumers; genuinely different needs stay distinct. Record merges in the
   ledger.
4. **Harden into the standard**: object shapes first (from the data model — cite, don't restate),
   then conventions (error shape, status codes, auth posture, content types), then every
   endpoint/message verbatim with request/response shapes and status codes. Stamp **Version: 1.0**.
   Write the versioning law into the document: *any change to a shape, endpoint, parameter, or
   status code bumps the version and carries a migration note here.* **The pre-seal no-bump
   allowance:** until the repo's first seal, drafts iterate freely at Version 1.0 with no bumps —
   there are no consumers yet; from the seal on (and always in a delta engagement,
   `phases/delta.md`), every such change bumps.
5. **Close the loop against the inventory**: every R/S-line that needs the wire can be satisfied
   through some contracted surface — walk each one (this is executability, run early). A line that
   can't reach the wire means a missing demand: add it via its consumer, not ad hoc.
6. **Self-review**, then per the spot-verify schedule (`dial.md` §2): fresh spot-verify
   (consistency/contract + executability + adversarial-user on the contract: abuse paths,
   idempotency, error honesty — scoped to this phase's artifacts).

## Gate
Per the tempo rule (`dial.md` §3 — cited, not restated): where the gate fires, the operator
approves the contract set before component authoring fans out; approval is recorded in the NOTES
seed and the approved standards are copied to `<run-dir>/gates/contracts/`. Otherwise proceed.
