# exemplars.md — The Ground Truth (what to imitate, what is product-specific)

Two hand-grown spec repos predate this skill and define its output class. When the grammar or a
template is ambiguous, **read the exemplar**. They are also the eval fixtures (§3).

## 1. feedler — tier S exemplar (github.com/kavehmz/feedler)

Self-hosted single-user RSS reader; ~4.1K spec lines; one deployable.
- **Ideation:** `old/prompt.md` — 27 informal lines. The input class: typos, mixed asks, implied
  conventions ("like Reeder"), stack preferences inline.
- **Imitate:** `specs/start.md` (a complete tier-S operating manual in 180 lines);
  `specs/components/export_spec.md` (the component-spec form at its best — scope/not-this-spec,
  binding worked examples incl. the timezone law, invariants, open questions, acceptance +
  deliverables); `specs/standards/engineering_standard.md` (whole-app risk carried once);
  `specs/standards/develop_loop.md` (the Builder/Gate auto-convergence standard — reference text
  for any emitted repo that wants the loop); `specs/architecture.md` §2/§3 (glossary-as-domain-model,
  data model with numbered invariants).
- **Product-specific (do not generalize):** the export format itself, feed semantics, the
  no-auth/single-user stance (that is feedler's vision, not a grammar rule).

## 2. The trading platform — tier L exemplar (private)

A real-money trading platform; ~6.9K spec lines; 8 platform components plus a product family.
- **Imitate:** its `specs/start.md` + design-track manual (operating manual + decoupled studio);
  its verification standard (the full practice: judge/judging separation, tiers, lenses, taxonomy,
  verdict records — `standards/verification_core.md` here is its product-agnostic core); its
  versioned platform contract (version bumps with migration notes + a conformance suite — the
  tier-L contract form); its product-family authoring template (the pattern when a tier-L repo
  hosts sibling products); its `NOTES.md` (the ledger discipline).
- **Product-specific (do not generalize):** money/custody semantics, the agent-operations layer
  (generalize only for AI-operated products), the product mechanics.

## 3. As eval fixtures (the reproduction test)

Both repos preserve their founding ideation, so the factory can be tested against ground truth:
- **L1 — reproduce feedler:** run `new product` on feedler's `old/prompt.md` (+ its `Feeds.opml`)
  into a scratch directory; panel-compare the emitted repo against real feedler on grammar
  conformance, ideation coverage, decision quality, buildability — **never** byte similarity
  (different good decisions are fine; missing asks and grammar violations are not). Then `develop`
  the emitted repo end-to-end as the integration proof. *(Run: PASS 2026-07-11 — see `NOTES.md`;
  public at github.com/kavehmz/specai-feedler.)*
- **L4 — reproduce the trading platform:** same, against its preserved founding vision note
  (private). Expect divergence in decisions; require parity in class: constitution-grade
  architecture, versioned contracts, verification practice, self-operability.

An eval run is a normal `new product` run plus a comparison verdict; findings feed `improve specai`.
