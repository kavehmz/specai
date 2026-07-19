# Blind re-verification round 2 — lens 1: consistency/contract (verbatim report)

*Preserved verbatim per `verification_core.md` §6 rule 4 (received via agent relay; the run lead
performed no edits beyond this header). Dispatcher: the operator by standing order ("go"); lead as
mechanical proxy. Package: the full tree minus `verdicts/` and `.git`.*

---

All 23 in-scope files read in full; nothing outside scope was opened (verdicts/ was listed for existence only, never read; .git untouched).

# Lens verdict — consistency/contract: **FAIL** (1 blocker, 7 majors, 8 minors)

**DISCLOSURE of ambient context beyond the prompt and listed files:** my session carries harness-injected context: a system-reminder with a user email and today's date; a listing of available skills (slack, dataviz, deep-research, etc.) and MCP tool inventories; environment info (cwd, platform). No CLAUDE.md, no memory files, and no project-specific context about specai were injected. None of it informed the findings below.

**What held up (checked, not padded):** tier thresholds (0–3/4–7/8–10), verifier counts (S=1/M=2/L≥3), gate schedule (Definition always, Architecture M/L, Contracts L, seal always), spot-verify schedule, working-file names (inventory/notes-seed/consumer-ledger/journal/slices×3/gaps/taxonomy/change-request/inventory-delta), verification-mode value set, identity/revisitable marks, the DRIFT lifecycle across its eight homes, the pre-seal no-bump allowance triangle (contracts ↔ delta), and the testing-floor stub triangle (architecture step 9 ↔ contracts outputs ↔ emission output 7) are all mutually consistent. Terms tempo, spot-verify schedule, seal, close, focused pass, top tier, IOU, fresh context, experience-led each have exactly one defining home and are used consistently — with the single exception of "dispatcher" (finding 6).

## BLOCKER

**1. {where: reference/exemplars.md preamble + grammar.md §1/§3.2 + 4 templates + phases/emission.md}** — The eval-integrity invariant ("this file is the only home of the answer key") is factually false about this tree; the eval protocol's enforceability claim is contradicted by the binding documents themselves.

- **Evidence, the claim:** exemplars.md: "This file is the **only** home of the exemplars' identifying calibration facts — names, tiers, sizes, dial breakdowns, decomposition shapes, signature principles. Binding documents cite this file and never carry those facts inline (that is what makes §3's target-exclusion rule enforceable: excluding this file removes the answer key)." And grammar.md §1: "names, tiers, sizes, and imitation notes live there and only there."
- **Evidence, the contradictions (all in documents an eval run must read):**
  - grammar.md §3 rule 2: "feedler's export ↔ api_contract split is the pattern" (name + decomposition shape).
  - templates/contract_standard.md: "Reference instances: feedler's `api_contract.md` (tier S, one seam) and the trading platform's versioned platform contract (tier L)" (names + tiers + decomposition).
  - templates/component_spec.md: "feedler's `export_spec.md`" (name + component identity).
  - templates/start.md: "a tier-S manual runs ~180 lines; tier L ~280 plus satellite standards" (the exemplars' sizes — exemplars.md §1/§2 present these same numbers as feedler's and the platform's).
  - templates/notes.md: "Reference instance: the trading platform's NOTES.md."
  - phases/emission.md procedure 2: "the discipline lives inline in start.md §4, **feedler-style**."
  - (weak) SKILL.md §2: "`evaluate feedler`" as the routing example.
- **Why blocker:** an L1 eval run conforming to the written protocol (exclude the target repo + exemplars.md) still learns from its own process docs that feedler is tier S, has one seam named `api_contract.md`, has an `export_spec.md`, and a ~180-line start.md — material answer-key leakage while exemplars.md asserts the exclusion "removes the answer key". The protocol's validity claim and the tree contradict each other outright; an eval would be contaminated yet certifiable as clean. (NOTES' fix-loop entry claims these facts were "quarantined to reference/exemplars.md" — the residue above shows the quarantine is incomplete, which also makes that ledger claim inaccurate.)
- **Fix:** genericize every inline mention to the anonymous pattern already used by templates/engineering_standard.md ("Reference instance: the tier-S exemplar's engineering standard (`reference/exemplars.md`)"): grammar §3.2 → "the tier-S exemplar's export↔contract split" → better, describe the pattern without the exemplar; contract/component/notes templates → "the tier-S exemplar's single-seam contract", "the tier-S exemplar's strongest component spec (see exemplars.md)"; start.md template sizes → move to exemplars.md and cite; emission.md → "tier-S-exemplar style" or drop; SKILL §2 → "`evaluate <exemplar>`".

## MAJOR

**2. {where: phases/definition.md (REG-n, step 4) vs phases/architecture.md step 8 / templates/architecture.md §7b / grammar.md §4.2 vs dial.md §2}** — The money/compliance machinery's trigger condition is pinned three different ways; at tier L with regulatory/money scoring 0–1 the documents give contradictory instructions and REG-lines have no mapping home.

- **Evidence:** definition.md: "**REG-n the regulatory register** (**at tier L, or** whenever regulatory/money scores 2 — `dial.md` §1) … phase 2 maps every REG-line to an enforcing component or principle in architecture's Money & compliance section" and step 4: "at tier L — or whenever regulatory/money scores 2 … — add the money/compliance round". But phases/architecture.md step 8: "Money & compliance section (**only when regulatory/money scores 2**…)"; templates/architecture.md §7b: "*(only when regulatory/money scores 2…)*"; grammar §4.2: "whenever regulatory/money scores 2". Meanwhile dial.md §2's L cells list "an explicit money/compliance round" and "money section" by tier, with the note "Money/compliance items in these rows apply whenever regulatory/money scores 2, regardless of tier" — which resolves the reg-2-at-low-tier direction but leaves the L-without-reg-2 direction ambiguous.
- **Consequence:** a tier-L, reg≤1 run (e.g. 3+2+2+0+1=8) must produce a REG register and money round per definition.md, then map REG-lines "to architecture's Money & compliance section" — a section three documents forbid emitting. Guaranteed drift or an improvised section.
- **Fix:** dial.md §1 rule 2 is titled "keys to the dimension, not the tier" — make it the sole owner. Rewrite definition.md's two conditions to "whenever regulatory/money scores 2" (dropping "at tier L, or"), or, if a register-at-L-always is intended, give sub-2 REG-lines an explicit non-money home (e.g. the coverage matrix) and say the money section itself remains reg-2-only. Reword dial §2's L cells to cite §1 rule 2 rather than sit in a tier column.

**3. {where: templates/architecture.md §7 vs standards/style.md §1 + templates/engineering_standard.md header (and grammar.md §4.7)}** — The licensed-HOW enumeration has two claimed owners, and the two candidate lists already differ.

- **Evidence:** style.md §1: "exactly the concerns `grammar.md` §4.7 names as owned; **§4.7 owns that enumeration** and it is not repeated here." templates/engineering_standard.md: "The licensed-HOW enumeration is **owned by `grammar.md` §4.7**; this template instantiates it." But templates/architecture.md §7: "every section of `templates/engineering_standard.md` still applies, just relocated **(that template owns the enumeration)**."
- **The lists diverge:** grammar §4.7 "Owns: build & deploy …, configuration …, persistence rules, security posture, HTTP conventions, whole-product Risk & Audit + Deployment & Retirement …, testing floor, Deliverables checklist" — no Glossary, no separate Deployment shape, Stack only in prose; the template has 12 sections including "§3 Deployment shape (binding)" and "§7 Conventions" (broader than "HTTP conventions"). A verifier checking an inlined tier-S engineering section against "every section still applies" gets a different pass/fail than one checking against §4.7's Owns list.
- **Fix:** one owner, one list. Either grammar §4.7 defers to the template's section list ("the enumeration is the template's §1–§12") and architecture-template §7 stands, or the template/architecture-template both point at §4.7 and §4.7's list is completed to match the template's sections. Update style.md §1 to cite whichever wins.

**4. {where: standards/change_rule.md §5 rules 1–2}** — The self-change gates overlap with no precedence rule: every rule-2 surface is also swept by rule 1's broader classes at a weaker gate.

- **Evidence:** rule 1: "Any substantive change to **`standards/*`**, **`SKILL.md` (any section)**, `templates/*` …, or `reference/exemplars.md` takes **one fresh verifier** before it lands." Rule 2: "Changes to the self-governing surfaces — **`verification_core.md`**, this document's §4–§5, or **`SKILL.md` §4's** contamination/degraded-floor clauses — take a full fresh-context **panel** (≥3 distinct lenses)." verification_core.md ∈ standards/*; SKILL §4 ⊂ "SKILL.md (any section)". §5 has no "first match wins"/"stricter wins" clause (§2's first-match rule belongs to the router, not §5).
- **Consequence:** an editor can satisfy rule 1's letter with one verifier on a verification_core.md change and claim conformance — the exact under-gating the panel review was fixing.
- **Fix:** one sentence in rule 1: "…except the self-governing surfaces, which rule 2 escalates" (or "where both rules match, the stricter gate binds").

**5. {where: standards/verification_core.md §2 rule 4 vs §4 S-row + §7 + phases/verification.md pass 2 + reference/exemplars.md §3 rule 3}** — The "conforming brief" definition makes the judgment-gate dispatch (mandatory at every seal) and the eval comparison-panel brief nonconforming by construction.

- **Evidence:** §2 rule 4: "A conforming brief is exactly: **the §5 lens row verbatim** + the §6 finding shape and PASS rule + the file package — **nothing else**." But §4 (S row): "1 fresh verifier running all applicable lenses (**carrying the judgment-gate brief** as its own verdict section)"; phases/verification.md: "at tier S the judgment-gate brief **folds into the single verifier's dispatch**"; at M/L the gate "is an **additional fresh context**". The judgment gate has no §5 lens row — its content lives in §7. Likewise exemplars §3's comparison panel judges on "rule 5" axes, not a §5 row.
- **Consequence:** every seal dispatch either violates the exactly/nothing-else rule or omits the judgment gate; a verifier auditing dispatch legitimacy must fail one of two binding rules.
- **Fix:** amend rule 4 to "the applicable §5 lens row(s), the §7 judgment-gate brief where the tier requires it, or the eval-comparison brief (exemplars.md §3) — verbatim from their owning sections — plus the §6 finding shape and PASS rule and the file package; nothing else."

**6. {where: standards/verification_core.md §3 (fix loop) vs §2 rules 1 and 4}** — "Curated by the dispatcher" contradicts the taxonomy's own handling rules and the zero-discretion dispatch rule; "lens seeds" is an undefined term.

- **Evidence:** §3: "prior learnings travel only as distilled patterns (taxonomy/**lens seeds, curated by the dispatcher** per §2 rule 1)". §2 rule 1: taxonomy is "distilled **mechanically** from prior verdict records … passed **unchanged — never selected or edited per review**, and never written by the artifact's author." §2 rule 4: "the run lead may dispatch mechanically, with **zero discretion over what the verifier sees**."
- **Consequence:** §3 licenses exactly the per-review selection §2 forbids, in the hands of the party rule 4 strips of discretion. "Lens seeds" appears nowhere else in the tree.
- **Fix:** replace with "(the taxonomy, distilled mechanically per §2 rule 1 — never the author's fix claims)"; delete or define "lens seeds".

**7. {where: standards/grammar.md §4.11 + phases/emission.md vs grammar.md §5 Design row vs standards/dial.md §2 L cell}** — The condition for emitting `studio.md` is pinned three different ways.

- **Evidence:** grammar §4.11: "**`studio.md`** (L, **experience-led**)"; emission.md: "`studio.md` (L, experience-led — shape: `grammar.md` §4.11)". But grammar §5 Design row (whose S cell keys the row to "if UI"): L = "+ design-studio track (`studio.md`) with storyboards" — condition L∧UI. And dial §2 Emitted-process-docs L cell: "+ verification with taxonomy/lenses/verdicts, **`studio.md`**, ops standards" — condition L, unconditional.
- **Consequence:** a tier-L UI product that is not experience-led: dial §2 says emit studio.md, grammar §4.11/emission say don't. A whole document appears or not depending on which table the run reads.
- **Fix:** §4.11 owns the condition (L ∧ experience-led); grammar §5's cell and dial §2's cell each gain "(experience-led — §4.11)" or drop the item and cite.

**8. {where: SKILL.md §0 + NOTES.md vs reference/exemplars.md §3 rule 2}** — Eval runs are simultaneously directed into and barred from specai's own NOTES.md, which carries target answer-key facts.

- **Evidence:** SKILL §0: "(Lineage and rationale: `NOTES.md`; …)" — every run's front door points at the ledger. NOTES' L1 entry carries feedler's answer key: "dial scored 2 → tier S, matching the calibration anchor exactly. **Six isolated component authors** … **4,113 spec lines from a 27-line ideation**" plus capability deltas. exemplars §3 rule 2 excludes "its repo, specs, **any derived notes**, and this file" — without stating whether specai's own mixed-content ledger is in the "derived notes" set, and with no way to exclude half a file.
- **Consequence:** an L1 eval run lead following SKILL §0 reads a richer answer key than exemplars.md itself; a run lead following rule 2 strictly must skip the file SKILL calls its decision ledger. Contradictory directives, unresolved by any precedence.
- **Fix:** exemplars §3 rule 2 names `NOTES.md` explicitly among the excluded inputs for eval runs (the neutral-directory rule already keeps it out of spawned contexts — extend it to the run lead), or target-derived run facts move out of NOTES into the (already excluded) verdict records with NOTES keeping only pointers.

## MINOR

**9. {where: phases/verification.md pass 2}** — "Dispatch per tier …: S = 1 verifier, all lenses; M = 2, split, **verdict record**; L = panel ≥3 + adversarial re-verify + **verdict record**" attaches the verdict record to M/L only, while verification_core.md §4 says "**Every** seal writes a verdict record (§6)" and §6 rule 4 pins "Minimum content **at every tier**". Fix: add ", verdict record" to the S clause or drop it from all three (VC owns it).

**10. {where: phases/contracts.md Outputs}** — Restates the engineering standard's content list ("Content: stack …, one-command acceptance gate, binding env-var table, persistence rules, security posture, whole-product risk/audit + deploy/retire") — already diverged from the template's sections (omits Deployment shape, Conventions, Deliverables checklist). Fix: replace the list with "every section of `templates/engineering_standard.md`".

**11. {where: standards/dial.md §1 note, standards/grammar.md header, phases/emission.md inputs}** — Three lossy summaries say "the eval **target** is off-limits during an eval" while exemplars §3 rule 2 excludes "**this file**" entirely; a reader of dial.md could open exemplars.md mid-eval for the other exemplar's anchors and see the target's breakdown. Fix: each summary becomes "exemplars.md is off-limits to an eval run (its §3)".

**12. {where: standards/dial.md §2, Component authoring L cell}** — "(design-first ordering: `phases/component_specs.md`)" sits in the L column; component_specs.md Ordering rule 1 mandates "Design first for UI products (experience-led or not…)" at every tier. Fix: move the parenthetical out of the tier cells or mark it "(UI products, any tier)".

**13. {where: README.md, "shape in five sentences"}** — "authored in parallel by isolated authors who see **only the contracts and their own scope**" contradicts phases/component_specs.md's closed list (vision + architecture **in full** + contracts + slice + design spec + style + template). README is gated binding text (change_rule §5 rule 3). Fix: "…who see only the vision, the architecture, the contracts, and their own slice".

**14. {where: templates/component_spec.md header vs phases/component_specs.md inputs}** — The template hands authors load-bearing references to grammar §4.5/§4.6 ("the intent-vs-binding split (grammar §4.6)") but grammar.md is not in any author's closed input package — the design author cannot resolve the split's definition. Fix: state the split in one sentence in the template (it owns the author-facing shape) and keep the grammar citation as provenance only.

**15. {where: standards/change_rule.md §3}** — "it comes from the citation graph (… the **mechanical machinery of `grammar.md` §6 check 2**)": check 2 only verifies that citations resolve; no named machinery derives a reverse citation graph. Fix: "the citation graph check 2 already walks" or name the derivation explicitly.

**16. {where: reference/exemplars.md §3 rule 2}** — "The **other** exemplar remains readable, as in a normal run" conflicts with excluding "this file": exemplars.md is the only home of the other exemplar's read paths and imitation notes, so it cannot be used "as in a normal run". Fix: either carve out the other exemplar's section, or say "the other exemplar's repo remains readable, though without this file's imitation notes".

---

**Summary for the caller:** FAIL on the consistency/contract lens. The pinned numeric values, term definitions, and gate schedules are in good shape — the founding consistency debts the panel flagged were largely paid. What remains broken clusters in two places: (1) the eval-integrity story contradicts itself — the "only home of the answer key" invariant is violated by six binding documents and by NOTES, so the tree's central self-test is currently invalid as written (the blocker plus majors 2 and 8's cousins); (2) the verification machinery's newest self-binding rules (exact-brief, taxonomy handling, self-gate tiers, money trigger, studio condition, enumeration ownership) each have one leftover restatement or overlap that contradicts the rule they were written to enforce.
