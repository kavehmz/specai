# Phase 3 — Contracts (consumer-driven derivation → hardened standards)

The narrow waist is built here. This phase carries ai-it's most distinctive mechanism —
**consumers write their requirements into provider contracts** — fused with the 2026 discipline
that a finished contract is a **versioned, binding standard**.

## Inputs
- `specs/architecture.md` (component map, glossary, data model, comms sketch), the inventory slices
  per component, the dial.
- `standards/grammar.md` §4.4/§4.7, `standards/style.md`, `templates/contract_standard.md`,
  `templates/engineering_standard.md`.

## Outputs
- `<repo>/specs/standards/<contract>.md` — one per boundary where ≥2 sides must agree. The
  frontend↔backend seam **always** counts (feedler's whole waist is one `api_contract.md`); a
  platform↔plugins seam gets its own; tier L may add a conformance-suite spec.
- `<repo>/specs/standards/engineering_standard.md` (unless inlined at tier S): stack (from
  engineering defaults), one-command acceptance gate, **binding env-var table**, persistence rules,
  security posture, whole-product risk/audit + deploy/retire, testing floor.
- The **consumer ledger** — a working artifact recording which consumer demanded which surface and
  why (may survive as a "Consumers" appendix in the standard).

## Procedure — the consumer-driven walk
1. **Order the walk top-down by dependency**: user-facing surfaces first (their needs are known —
   they come straight from lifecycle stories and component inventory slices), then each consumer
   level down, providers last. (ai-it's Level-0→core hierarchy, kept verbatim in spirit.)
2. **Each consumer states demands against each provider**: operation, data in/out, error cases it
   must distinguish, idempotency/ordering needs — annotated `(consumer: <component> — <purpose>)`.
   Demands are *accumulated into the provider's draft contract*, never invented by the provider.
   **No speculation:** a provider surface no consumer demanded does not exist. At tier S with one
   deployable, run the same walk with the SPA/UI as the consumer and the backend as the provider —
   the mechanism is identical, just one round.
3. **Harmonize**: near-duplicate demands (same method+resource+purpose, ~80% overlap) merge into
   one surface serving all consumers; genuinely different needs stay distinct. Record merges in the
   ledger.
4. **Harden into the standard**: object shapes first (from the data model — cite, don't restate),
   then conventions (error shape, status codes, auth posture, content types), then every
   endpoint/message verbatim with request/response shapes and status codes. Stamp **Version: 1.0**.
   Write the versioning law into the document: *any schema change bumps the version and carries a
   migration note here.*
5. **Close the loop against the inventory**: every R/S-line that needs the wire can be satisfied
   through some contracted surface — walk each one (this is executability, run early). A line that
   can't reach the wire means a missing demand: add it via its consumer, not ad hoc.
6. **Self-review**, then per tempo: tier L fresh spot-verify (consistency + executability +
   adversarial-user on the contract: abuse paths, idempotency, error honesty).

## Gate
Tier L: operator approves the contract set before component authoring fans out (tempo rule).
S/M: proceed.
