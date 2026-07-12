# dial.md — The Complexity Dial

**Status:** Binding. Scored once in `phases/definition.md`, confirmed by the operator, recorded in
the emitted `NOTES.md`. The dial sizes **both** the emitted spec tree (`grammar.md` §5) **and** the
factory process itself — it is the governor that stops specai from producing an eight-component
platform for an RSS reader, or a one-pager for a real-money exchange.

*(Inherited from ai-it's complexity assessment — the scoring held up across a year of use; the
consequences table is modernized.)*

## 1. Scoring (0–10)

| Dimension | Range | Anchors |
|---|---|---|
| **Technical** | 0–3 | 0 = single process, simple logic · 1 = several concerns in one deployable · 2 = multiple services / real-time / nontrivial algorithms · 3 = distributed system, advanced correctness demands |
| **Users** | 0–2 | 0 = single user, no auth · 1 = multiple user types OR auth · 2 = roles/permissions AND auth |
| **Integrations** | 0–2 | 0 = standalone · 1 = 1–2 external systems · 2 = many, or third parties integrate with *us* |
| **Regulatory / money** | 0–2 | 0 = none · 1 = privacy/data care · 2 = real money, financial/health compliance |
| **Scale / performance** | 0–1 | 0 = personal/team scale · 1 = high scale or hard latency targets |

**Tiers:** S = 0–3 · M = 4–7 · L = 8–10.

Rules: score each dimension with one sentence of justification (recorded in NOTES). When in doubt
between tiers, **money and regulatory always round up**; everything else rounds down (ai-it's
"score conservatively" flipped where it must be). The operator may override the tier; the override
and reason are recorded. The dial can be re-scored later only through the emitted repo's change
process (it is a founding decision, not a mood).

Calibration anchors: **feedler = 2** (technical 1, users 0, integrations 1 [feed origins], reg 0,
scale 0) → S. **the trading platform = 10** (3/2/2/2/1) → L.

## 2. What the dial bends

| Concern | S | M | L |
|---|---|---|---|
| Definition depth | vision + a lean requirements inventory | + explicit user-type breakdown, edge-case sweep | + full inventory with stable IDs, regulatory register |
| Checkpoint questions (per phase) | 1 batched set, only what the ideation doesn't answer | same, plus a risk-focused round | same, plus an explicit money/compliance round |
| Architecture | components table + principles | + comms matrix + coverage matrix | + matrices, money section, agent layer if AI-operated |
| Contracts phase | one pass, single contract | consumer-driven walk per boundary | full hierarchy walk, versioned standards, conformance suite spec |
| Component authoring | may run sequentially in one context if tiny | parallel, isolated authors | parallel, isolated authors, design track first |
| Emitted process docs | `start.md` (verification inline) | + `verification_standard.md` | + verification with taxonomy/lenses/verdicts, `studio.md`, ops standards |
| Phase-6 verification | 1 fresh verifier, all lenses in one run + mechanical pass | 2 verifiers, split lenses | panel ≥3 distinct lenses + adversarial re-verify, verdict record |
| specai spot-verifies mid-run | none (self-review only) | after Architecture | after Definition, Architecture, and Contracts |

## 3. The tempo rule

The dial also sets how often the operator is pulled in during a run: at S, the operator approves
**Definition** and the final seal; at M, also **Architecture**; at L, also **Contracts**. Between
those checkpoints specai proceeds autonomously — it never asks what the ideation, the dial, or the
grammar already answer.
