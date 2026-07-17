# Post-seal audit — lens 3: altitude/style (verbatim report)

*Preserved verbatim per `verification_core.md` §6 rule 4. Post-seal audit round over the sealed
tree (630ac46). Package: the tree minus `verdicts/`/.git.*

---

**Disclosure — ambient context beyond this prompt and the listed files:** the harness injected a context block (user email, current date), a git status snapshot (branch, recent commit subjects), and system listings of available agents/skills/tools. I read none of `verdicts/`, `.git`, or any file outside the scope list.

# Verdict: FAIL — 0 blockers, 2 majors, 6 minors

**MAJOR 1 — The emitted-world money gate hangs on terms defined only in a factory file the authoring phase may not read and the emitted repo never receives.** templates/architecture.md §7b instructs "Money-path changes gate at top tier — say so here" and templates/start.md §4 keys the fresh-context duty to "products with regulatory/money = 2" — but the sole definition of "money-path" is change_rule.md §4's, outside phase 2's closed inputs and outside the emitted tree entirely (grammar §1: no dependence on specai); the reg/money dimension score also binds nowhere in the emitted tree (vision §10 binds only the total). Undefined terms gating a binding rule; omitted WHAT on the highest-stakes surface. Fix: emit the definition verbatim in §7b ("a money-path change is any edit to a clause cited by this section"); key start §4's clause to the section's presence; put the definition line inside phase 2's declared inputs.

**MAJOR 2 — Canonical-term collision: README's layout line calls SKILL.md "the dispatcher"**, colliding with the tree-canonical dispatcher (verifier-launching) on a trust seam; style rule 1 classes a two-meaning term blocker-class. Fix: one word ("the front door").

**MINORS:** 3 SKILL §0 declares "gate" with two senses — against rule 1's letter (context-partitioned, hence minor). 4 The judgment-gate dispatch shape has two unmarked owners (§4 rows vs phase 6). 5 Agreeing verbatim restatements without a declared owner: the versioning-law enumeration (three files) and SKILL §3's autonomy sentence. 6 Two divergent, unlabeled invariant-class example enumerations (phase step 2 vs template §3; "health semantics" template-only). 7 delta step 6's "the consumer ledger → only where step 3 ran" puts a condition where a target should be. 8 grammar §6 checks 1 and 7 characterize DRIFT's set membership two ways.

**Not counted (operator-accepted):** nested-parenthetical density.

**What held:** the exemplar quarantine as written (all references are licensed tier-role forms; dial's archetypes name no exemplar), invented-example labeling elsewhere, lineage pointers, RFC 2119 usage, the template-owns-enumeration device where applied, and tone.
