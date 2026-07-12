# TEMPLATE — standards/<contract>.md (grammar §4.4 · the hardened waist)

> Authoring notes in blockquotes; delete them. Reference instances: feedler's `api_contract.md`
> (tier S, one seam) and the trading platform's versioned platform contract (tier L).
> Born in phase 3 from accumulated consumer demands; hardened here into verbatim wire truth.

# <Product> — <Contract Name>

**Version:** 1.0 · **Status:** Binding wire truth. Both sides implement this document; nothing
else couples them.
**Versioning law:** any change to a shape, endpoint, parameter, or status code in this document
requires a **version bump and a migration note added at the top of this file**. Announce such
changes loudly (start.md §5).
> *(dial M/L)*: version-negotiation window, conformance-suite hook.

## 1. Object shapes
> Every JSON/message object verbatim, once: fenced, field-per-line, with per-field comments
> (type, nullability, meaning). These reflect the data model (`architecture.md` §3) — cite it;
> storage truth and wire truth are specified once each.

## 2. Conventions
> Content types · the **error shape** verbatim (e.g. `{ "error": "<message>" }`) · status-code
> table (200/201/202/400/404/5xx — what each means here) · auth posture (or its deliberate
> absence, cited to the principle) · idempotency and timeout conventions.

## 3..n Endpoints / messages (grouped by resource or flow)
> Per endpoint:
> ### `<METHOD> <path>`
> Purpose (one line) · parameters (table: name, type, default, meaning — **names and defaults are
> binding**) · request/response shapes (cite §1 objects; show deltas only) · status codes ·
> one worked example where the shape is nontrivial (binding).
> *(from phase 3, optional but recommended)*: a **Consumers** note per endpoint — who demanded it
> and why — kept from the consumer ledger; invaluable when a future change asks "who breaks?".

## n+1. Consumers appendix *(optional, from the consumer ledger)*
> Consumer → the surfaces it depends on → purpose. The future cascade map for this contract.
