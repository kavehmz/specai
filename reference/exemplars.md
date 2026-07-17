# exemplars.md — The Ground Truth (what to imitate, what is product-specific)

Two hand-grown spec repos predate this skill and define its output class. They are **optional
calibration**: the grammar and templates stand alone (grammar's tiebreaker is the templates), and
where an exemplar is available it sharpens judgment — except during an eval, where the **target
exemplar is off-limits** (§3). They are also the eval fixtures (§3).

This file is the only home **in binding documents** of the calibration facts that characterize a
**specific named exemplar** — names, dial breakdowns, decomposition shapes, domains, sizes,
signature principles (`NOTES.md`, a record, also carries run history about them — which is why
eval runs exclude both). Binding documents cite this file and never carry those facts inline
(that is what makes §3's target-exclusion rule enforceable: excluding this file removes the
answer key). **Tier-role references** in binding documents ("the tier-S exemplar", "the
tier-matched exemplar" — tier labels allowed, nothing else) are licensed: that one exemplar is
tier S and one is tier L identifies nothing — a target's tier is derivable from its ideation by
the dial, by design.

## 1. feedler — tier S exemplar (github.com/kavehmz/feedler)

Self-hosted single-user RSS reader; ~4.1K spec lines; one deployable with seven spec areas.
**Dial: 2 → S** (technical 1, users 0, integrations 1 [feed origins], reg 0, scale 0).
Signature domain principle: "politeness to origins". Its `start.md` is the ~180-line tier-S
operating-manual reference; its `engineering_standard.md` and `develop_loop.md` are the tier-S
reference instances those templates cite.
- **Ideation:** `old/prompt.md` — 27 informal lines. The input class: typos, mixed asks, implied
  conventions ("like Reeder"), stack preferences inline.
- **Imitate:** `specs/start.md` (a complete tier-S operating manual in 180 lines);
  `specs/components/export_spec.md` (the component-spec form at its best — scope/not-this-spec,
  binding worked examples incl. the timezone law, invariants, open questions, acceptance +
  deliverables; its export ↔ api_contract split is the shared-surface-deferral instance
  `grammar.md` §3 rule 2 cites); `specs/standards/engineering_standard.md` (whole-app risk
  carried once);
  `specs/standards/develop_loop.md` (the Builder/Gate auto-convergence standard — reference text
  for any emitted repo that wants the loop); `specs/architecture.md` §2/§3 (glossary-as-domain-model,
  data model with numbered invariants).
- **Product-specific (do not generalize):** the export format itself, feed semantics, the
  no-auth/single-user stance (that is feedler's vision, not a grammar rule).

## 2. The trading platform — tier L exemplar (private)

A real-money trading platform; ~6.9K spec lines; 8 platform components plus a product family.
**Dial: 10 → L** (3/2/2/2/1). Signature domain principle: "products never call the platform
back". Its `start.md` (~280 lines + satellite standards) is the tier-L operating-manual
reference.
- **Imitate:** its `specs/start.md` + design-track manual (operating manual + decoupled studio);
  its verification standard (the full practice: judge/judging separation, tiers, lenses, taxonomy,
  verdict records — `standards/verification_core.md` here is its product-agnostic core); its
  versioned platform contract (version bumps with migration notes + a conformance suite — the
  tier-L contract form); its product-family authoring template (the pattern when a tier-L repo
  hosts sibling products); its `NOTES.md` (the ledger discipline).
- **Product-specific (do not generalize):** money/custody semantics, the agent-operations layer
  (generalize only for AI-operated products), the product mechanics.

## 3. As eval fixtures (the reproduction test)

Both repos preserve their founding ideation, so the factory can be tested against ground truth.
An eval run is a normal `new product` run plus a comparison verdict; findings feed `improve specai`.

**Eval hygiene (binding — an eval that violates these proves nothing):**
1. **Neutral working directory.** The run launches where no ambient context (CLAUDE.md, memory,
   the exemplar checkout) can leak the target (`SKILL.md` §4).
2. **The target exemplar is off-limits to the run** — its repo, specs, any derived notes, **this
   file** (the calibration facts above are the answer key), **specai's own `NOTES.md` plus any
   candidate repos it names** (the ledger carries run history about the fixtures; the eval run
   needs no factory history, and this exclusion overrides `SKILL.md` §0's lineage pointer for the
   run's duration), **and `verdicts/`** (relocated records and raw verifier reports quote
   identifying facts). The run gets only the preserved ideation + attachments — **staged by the
   operator** into the run's input location, since the run may not enter the target repo to fetch
   them — like any real customer. At tier-L evals the taxonomy is **staged by the operator**
   (from `verdicts/taxonomy-seed.md` after scrubbing fixture-derived lines) or starts empty.
   The *other* exemplar's repo remains readable where available (the operator stages its pointer;
   this file stays excluded, so its imitation notes are unavailable during an eval).
3. **The comparison panel — ≥2 fresh contexts — is dispatched by the operator**, never by the
   run being evaluated (`verification_core.md` §2 rule 4). The panel receives both repos; the
   run never does. The comparison verdict lands at `<run-dir>/verdict-comparison-<target>.md`.
4. **No PASS without the integration proof**: the **operator launches** a fresh builder context
   to `develop` the emitted repo end-to-end through its own `start.md`, and **separately
   dispatches** the proof's verification pass to another fresh
   context (the same legitimacy rule as rule 3), regardless of the emitted repo's tier; that
   fresh context — never the builder — signs the DoD's independent-verification line, and the
   evidence attaches to the comparison verdict. Until that step runs, the honest verdict is at
   most "comparison passed; build-proof pending."
5. Judge on ideation coverage, decision quality, and buildability first; grammar conformance is
   the **weakest axis** for a target the grammar was derived from (circular) — weight it last.
   **Never** byte similarity (different good decisions are fine; missing asks and grammar
   violations are not).
6. **The eval preamble sweeps specai's open IOUs and enumerates the exempted-edit bundle**
   (`change_rule.md` §5 rules 3–4), recording the sweep's result in the comparison verdict
   record: an IOU past its anchor blocks the eval until paid or operator-re-anchored.

7. **The eval run's own dispatch is templated and preserved.** The operator (or a non-run
   orchestrator that never leads the run) launches the run with the fenced prompt below —
   preserved verbatim in the run dir like a verifier dispatch prompt — and stages or verifies a
   run environment where the excluded paths are absent or unreadable. Evals never run in
   degraded (no-spawn) mode.

**Eval dispatch prompt (verbatim):**

```
Run `new product <name>` from the staged ideation + attachments at <path>, target <dir>.
This is an eval: do not read, fetch, or reconstruct — the target exemplar's repo or any
candidate repo, reference/exemplars.md, specai's NOTES.md, or verdicts/. Ambient context you
receive anyway must be disclosed in your run journal and the verdict record.
```

**Comparison brief (verbatim — the §2-rule-4 conforming brief for the comparison panel):**

```
You compare a candidate spec repo against a reference repo for the same ideation. Judge on:
ideation coverage, decision quality, and buildability first; grammar conformance last (it is
circular for a target the grammar was derived from). Never byte similarity — different good
decisions are fine; missing asks and grammar violations are not. Finding shape and PASS rule
per verification_core.md §6. Verdict: does the candidate reach the reference's class?
```

The fixtures:
- **L1 — reproduce feedler:** run `new product` on the operator-staged founding ideation
  (feedler's `old/prompt.md` + its `Feeds.opml`) into a scratch directory; compare per rule 5;
  then the integration proof. *(Run history: `NOTES.md`, the L1 entry.)*
- **L4 — reproduce the trading platform:** same, against its preserved founding vision note
  (private). Expect divergence in decisions; require parity in class: an architecture of numbered
  principles with rejection force, versioned contracts, an instantiated verification practice,
  self-operability.
