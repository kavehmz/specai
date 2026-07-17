# dial.md — The Complexity Dial

**Status:** Binding. Scored once in `phases/definition.md`, confirmed by the operator, recorded in
the emitted `NOTES.md`. The dial sizes **both** the emitted spec tree (`grammar.md` §5) **and** the
factory process itself — it is the governor that stops specai from producing a many-component
platform tree for a personal utility, or a one-pager for a compliance-bound product.

*(Lineage: `NOTES.md`.)*

## 1. Scoring (0–10)

| Dimension | Range | Anchors |
|---|---|---|
| **Technical** | 0–3 | 0 = single process, simple logic · 1 = several concerns in one deployable · 2 = multiple services / real-time / nontrivial algorithms · 3 = distributed system, advanced correctness demands |
| **Users** | 0–2 | 0 = single user, no auth · 1 = multiple user types OR auth · 2 = roles/permissions AND auth |
| **Integrations** | 0–2 | 0 = standalone · 1 = 1–2 external systems · 2 = many, or third parties integrate with *us* |
| **Regulatory / money** | 0–2 | 0 = none · 1 = privacy/data care · 2 = real money, financial/health compliance |
| **Scale / performance** | 0–1 | 0 = personal/team scale · 1 = high scale or hard latency targets |

**Tiers:** S = 0–3 · M = 4–7 · L = 8–10.

Rules:

1. Score each dimension with one sentence of justification (recorded in NOTES; the score + tier
   bind in the emitted `vision.md` — `grammar.md` §4.1). When a dimension's score is uncertain
   between two values, **money and regulatory resolve up**; everything else resolves down. The
   operator may override the tier; the override and reason are recorded.
2. **The money trigger keys to the dimension, not the tier.** Whenever regulatory/money scores
   **2**, the money/compliance machinery applies regardless of the total: the money/compliance
   checkpoint round (§2), architecture's money section, and top-tier verification of money-path
   changes (`change_rule.md` §4). Simple never means low-stakes.
3. **Mid-run re-score.** A phase that discovers scope changing *any* dimension score (invented
   examples: "these gift credits are redeemable for cash"; "operators are a second user class")
   routes back to a
   re-score — operator confirm, then downstream phases re-size to the new tier (`SKILL.md` §3
   mid-run feedback). Carrying on under a stale score launders the discovery. After the seal, the
   dial changes only through the emitted repo's change process (it is a founding decision, not a
   mood).

Calibration anchors: the two ground-truth exemplars' scored breakdowns live in
`reference/exemplars.md` §1–2 (that file is off-limits to an eval run entirely — its §3).

## 2. What the dial bends

| Concern | S | M | L |
|---|---|---|---|
| Definition depth | vision + a lean requirements inventory | + explicit user-type breakdown, edge-case sweep | + full inventory (emitted-tree ID apparatus per `grammar.md` §5), regulatory register (reg/money = 2 — §1 rule 2) |
| Checkpoint questions (per phase) | 1 batched set, only what the ideation doesn't answer | same, plus a risk-focused round | same as M, plus the money/compliance round (reg/money = 2 — §1 rule 2) |
| Architecture | components table + principles | + comms matrix + coverage matrix | + matrices, money section (reg/money = 2 — §1 rule 2), agent layer if AI-operated |
| Contracts phase | one pass, single contract | consumer-driven walk per boundary | full hierarchy walk, versioned standards, conformance suite spec |
| Component authoring | may run sequentially in one context if tiny (a named degraded mode — `phases/component_specs.md` owns the threshold) | parallel, isolated authors | parallel, isolated authors |
| Emitted process docs | `start.md` (verification inline) | + `verification_standard.md` | + verification with taxonomy/lenses/verdicts, `studio.md` (experience-led — `grammar.md` §4.11), ops standards (§4.11) |
| Phase-6 verification | per `verification_core.md` §4 (owns the counts) | per §4 | per §4 |
| specai spot-verifies mid-run | none (self-review only) | after Architecture | after Definition, Architecture, and Contracts |

The last row is the **spot-verify schedule** — the term other documents cite for it. Design-first
ordering applies to UI products at **any** tier (`phases/component_specs.md`). Money/
compliance items in these rows (the money round, the money section, the REG register) apply
**when and only when** regulatory/money scores 2 — the dimension, never the tier, is the trigger
(§1 rule 2). The M/L extra checkpoint rounds are run inside `phases/definition.md` step 4.

## 3. The tempo rule

The dial also sets how often the operator is pulled in during a run ("tempo" names exactly this —
the operator-gate cadence; the mid-run verification cadence is §2's spot-verify schedule): at S,
the operator approves **Definition** and the final seal; at M, also **Architecture**; at L, also
**Contracts**. Between those gates specai proceeds autonomously — it never asks what the
ideation, the dial, or the grammar already answer.
