# TEMPLATE — architecture.md (grammar §4.2 · style.md applies)

> Authoring notes in blockquotes; delete them. This is the most-cited document in the repo —
> everything must stay consistent with it, and it must stay consistent with `vision.md`.

# <Product> — System Architecture

**Status:** Authoritative. Every spec in this suite must be consistent with this document.
**Audience:** the AI that builds <product> from these specs, and the human who directs it.
> State the WHAT/HOW posture in two lines, and declare the requirement-language convention once:
> "The key words MUST, SHOULD, MAY follow RFC 2119."

## 1. The system in one picture
> An ASCII diagram a builder can hold in their head: the deployable(s), the client(s), the
> datastore(s), every network egress/ingress. Close with the counting sentence — "One process. One
> port. One file." class — and what there is exactly none of.

## 2. Glossary (canonical terms — used verbatim across all specs)
> A table: Term → Meaning (with identity rules and cross-refs to owning specs). This is the
> absorbed domain model. Every later document reuses these words exactly and adds terms only in
> its own "glossary additions".

## 3. The data model (binding) *(when the product owns durable state)*
> The schema verbatim (this document owns it; the wire truth is the contract standard's — say so).
> Then **numbered binding invariants**: identity/dedup rules, cascade behavior, units/timezone law,
> ordering law, health semantics. Every invariant is testable.

## 4. The components
> Prose: how the product decomposes and what "component" means here (spec areas vs deployables).
> Then **the table**: | Area | Owns | Spec |. This table is the coverage anchor, the phase-4 work
> order, and the source of `start.md`'s boot table. State the mirror rule (workspace/ mirrors
> specs/, disposable).
> *(dial M/L)*: the inter-component communication matrix (consumer → provider → needed capability →
> pattern) and the explicit requirements-coverage matrix.

## 5. The principles (non-negotiable)
> Numbered. "Any proposed change that violates one of these must be rejected or escalated to the
> operator." Each principle is one bolded rule + 1–3 sentences of enforcement meaning. Derived
> from: vision pillars, data invariants, the deployment stance, plus the universal WHAT/HOW
> principle. 6–15 of them; each must have teeth (could reject a real request).

## 6. Lifecycle stories
> "These stories are the architecture's acceptance tests. Every relevant spec must keep them true."
> One titled paragraph each: **First run** · each primary flow · failure/recovery ·
> **Reset / rebuild** (including the doctrine sentence: deleting the code and rebuilding from this
> suite yields the same system). Cite the owning component spec at the end of each story.

## 7. Engineering standards
> Tier S with a small surface: the stack, build, config, and security posture inline here.
> Otherwise: one line citing `standards/engineering_standard.md`.

## 8. What this architecture deliberately does not have
> Bulleted negatives with teeth: no second datastore, no auth layer, no telemetry, no separately
> deployed frontend… Each traces to a vision non-goal or a principle. As binding as the scope.
