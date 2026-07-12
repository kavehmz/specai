# NOTES — specai decision ledger (founded 2026-07-11)

The operator's record of what was decided and why. A record, not a spec — the `standards/` and
`phases/` files win. (specai eats its own dog food: this is the `templates/notes.md` discipline
applied to the factory itself.)

## Founding (2026-07-11) — Kaveh + Fable

**What this is.** The modernization of `../ai-it` (2025, Roo-based, 48 prompts / ~13.8K lines,
idea→code) into a harness-agnostic skill that emits **self-operable spec repos** of the
feedler / trading-platform class. Full source study preceded this: all of ai-it's `all.md` (16,692 lines)
plus `.roomodes`/README/Makefile/history posts; feedler read in full; the trading platform's process docs read in full (its content already
deeply known).

**Founding decisions (each with its live home):**

1. **Emit the genome, not the organism.** specai ends at a sealed spec repo; `develop` belongs to
   the emitted `start.md`. Kills ai-it's spec+code co-evolution cascade. → `SKILL.md` §0, §2.
2. **Phases cut by information boundary, not token budget.** Requirements+domain+stories merge
   into one Definition pass (the 2025 split was a 200K-context artifact); architecture, contracts,
   component authoring, and verification stay separate because isolation is the point, not because
   context is small. → `phases/*`, each with a closed input list.
3. **Specs absorb their intermediates.** No PRD/domain/stories docs in emitted repos — vision +
   architecture (glossary, lifecycle stories) + component specs carry them, as both exemplars
   already do. The factory-side requirements inventory is working material; phase 6 verifies its
   full absorption. → `grammar.md` §3.4, `phases/definition.md`.
4. **Consumer-driven contracts, hardened.** ai-it's consumer_expand kept whole (top-down walk,
   annotated demands, ~80% harmonization, no speculation) and fused with the 2026 rule that a
   finished contract is a versioned standard with migration notes. → `phases/contracts.md`,
   `templates/contract_standard.md`.
5. **The dial sizes product AND process.** ai-it's 0–10 scoring kept (money/regulatory round up);
   bends the grammar (`grammar.md` §5), the emitted process docs, verification depth, and operator
   tempo. Calibration: feedler=2/S, the trading platform=10/L. → `standards/dial.md`.
6. **Quality cell defined once.** draft → self-review-in-update-mode (ai-it's trick, kept) →
   fresh verify → fix loop → seal; phase files never restate it. Roughly half of ai-it's line count
   was this cell restated eleven times — dropped. → `verification_core.md` §3.
7. **Verification = the trading platform's practice, genericized.** Judge/judging separation, fresh
   contexts, spec-first derivation, tiers, lens set (+ two factory-specific lenses: ideation
   coverage, buildability/rebuild test), zero-open-blockers/majors PASS, operator countersign.
   ai-it's roo-man survives as the judgment gate ("is it good?" may fail conforming work).
   ai-it's completeness checklists demoted to the mechanical pass. → `verification_core.md`,
   `phases/verification.md`.
8. **Preferences dissolve into the change rule.** Durable decisions live in specs; NOTES keeps
   history; operator engineering defaults arrive with the ideation or via checkpoint (recorded in
   the emitted NOTES). No parallel directive store. ai-it's current-state-not-history rule survives
   inside NOTES discipline. → `change_rule.md` §1, `templates/notes.md`.
9. **Harness-agnostic by files-as-interface.** Roles are briefs, not Roo modes; every phase I/O is
   a file; delegation isolated in one section with a stated degraded floor (single-context runs
   must disclose degraded verification independence). → `SKILL.md` §4.
10. **User-input checkpoints kept** (one batched set, proposed defaults, first run) and given a
    tempo: operator gates at Definition + seal (always), + Architecture (M/L), + Contracts (L).
    → `phases/definition.md`, `dial.md` §3.
11. **Router kept as the single front door** — including for the skill itself; security classified
    by where the fix lives; ai-it's Level 1–11 table replaced by classify-to-owning-artifact +
    the repo's concrete cascade graph. → `change_rule.md` §2–3.
12. **Both exemplars preserved their ideations → they are the eval fixtures.** L1 = reproduce
    feedler; L4 = reproduce the trading platform; judged on grammar conformance, ideation coverage, decision
    quality, buildability — never byte similarity. → `reference/exemplars.md` §3.
13. **Operator commits; specai never runs git mutation.** The commit is the countersign
    (Kaveh's standing rule, made doctrine). Automated commits exist only as an explicit emitted
    standard (develop_loop class), never a factory default. → `SKILL.md` §0.

**Deliberately dropped from ai-it** (recorded so no future "restoration"): per-phase orchestration
boilerplate; prescriptive code-structure/framework tables in guidelines (WHAT/HOW violation —
engineering defaults are the operator's, named once in the emitted engineering standard);
`PREFIX-XX-3CHAR` IDs as a default (tier-L-only option; named-section citations proved sufficient
at 7K lines); Roo mode mechanics; the standalone visual/post/present tooling (out of scope for the
factory).

**Deferred (open):**
- **speclint-for-emitted-repos**: a mechanical script for `grammar.md` §6 (a seed speclint
  already exists in the trading platform's private repo; generalize when the first
  emitted repo exists to test against). Until then phase 6 pass 1 runs by hand.
- **L1 eval run** (reproduce feedler) — the next milestone; then L4.
- Whether emitted tier-M/L repos should also get a `develop_loop.md` by default (currently
  "offered"); decide after L1.
- Skill packaging polish (frontmatter metadata beyond name/description) once the first
  harness-installed use happens.

**Verification status of this founding tree:** self-review pass done (lead); independent
fresh-context verification **pending** — per our own doctrine this founding batch should get a
panel review before heavy use; the L1 eval run doubles as its live-fire test. Operator countersign
= Kaveh's first commit of this repo.

## 2026-07-11 — L1 eval: reproduce feedler — PASS (class parity, locally exceeded)

**The run** (same day as founding — the skill's first full engagement): dial scored 2 → tier S,
matching the calibration anchor exactly. Six isolated component authors, four blind verification
rounds (majors 4 → 1 → 1 → 0; zero blockers ever; every binding worked example independently
recomputed at least twice), operator-sealed, countersigned as `eb54c20` in the
specai-feedler repo (github.com/kavehmz/specai-feedler) (4,113 spec lines from a 27-line ideation; the hand-built
reference is ~4.1K). Full audit trail in that repo's `.specai-run/`.

**Comparison verdict** (`.specai-run/verdict-comparison-L1.md`): headline **YES**. Grammar
conformance: candidate EXCEEDS (it hits the written grammar more exactly than the hand-built
exemplar the grammar was extracted from). Ideation coverage: PARITY, zero silent losses either
direction (the two capability deltas — full-text, search — are recorded checkpoint answers,
input-attributable). Decision quality: parity leaning exceeds (candidate stronger on security
posture, contract discipline, identity/dedup rules, cold deep-links, bound mobile behavior;
reference richer on export surface and carries build-proven maturity). Buildability:
parity-to-exceeds on paper — **the integration proof (actually building the emitted tree via its
own start.md) is still owed** per exemplars.md §3.

**Process learnings — to apply via `improve specai`:**
1. Rationale-placement rule → `style.md`: binding specs trace rationale to `vision.md`, never to
   the non-normative ideation (one instance emitted).
2. Benchmark-behavior checkpoint → `phases/definition.md`: when an ideation names a benchmark
   ("like Reeder on iOS"), surface the benchmark's signature behaviors as checkpoint questions.
3. Fixture-math discipline held (attached artifacts → verified binding fixtures) — name it
   explicitly in `phases/definition.md`.
4. Riding-minors seal policy → `verification_core.md` §6: minors riding a PASS fold into the
   emitted NOTES open topics at seal (done this run by judgment; make it the rule).
5. Tier-S traceability stub → `phases/emission.md`: a one-table "ask → owning §" appendix in
   emitted NOTES makes phase-6 and eval tracing cheap.
6. `exemplars.md`: name the emitted shell's placement/semantics/appearance three-way split as an
   imitation pattern (it out-performed the reference's decomposition).
7. Harness learnings → `SKILL.md` §4: (a) sub-agent→parent reply channels proved unroutable in
   Claude Code — the orchestrator relays; files stay the truth (held up across ~10 relays);
   (b) background-agent transcripts do not survive a conversation branch — disk-state resume is
   the recovery (validated twice more, incl. a mid-phase usage-limit kill); (c) **the harness
   injects the cwd project's CLAUDE.md into every subagent** — verifiers disclosed it unprompted;
   benign here, FATAL for the L4 trading-platform eval: **eval runs must launch from a neutral working
   directory** (binding note for L4).
8. speclint materialized unprompted: the run lead built `speclint.py` (+ a factory-id guard) to
   run grammar §6 — harvest it as specai's own deferred tool.

**Next:** the integration proof (`develop feedler` through the emitted repo's own start.md);
an `improve specai` pass applying items 1–8; then the L4 trading-platform reproduction (neutral-dir
rule binding). Seal bookkeeping precedent recorded: when the run lead is unreachable at seal time, the
orchestrator performs the NOTES stamp from verdict records — registrar work, disclosed in the
run journal.

## 2026-07-12 — Operator review: the large-change path

Kaveh's question while reviewing the blog draft: in ai-it, one front door took "I need this large
change" and re-entered the pipeline at the right phase (router → e.g. architecture → cascade →
code). Where does that live after the split?

**As designed, relocated into the emitted repo:** `templates/start.md` §3 case C + §5 give every
emitted repo the router (classify to the owning artifact, `change_rule.md` §2) and the concrete
cascade graph; code follows via case B reconciliation ("spec changed, spec wins"). Verified in the
field: the emitted feedler `start.md` carries it, and the GPT builder obeyed it.

**Gap he exposed, closed same day:** the factory-side re-entry for product-reshaping changes was
a placeholder row. Now designed as `phases/delta.md` — the **delta engagement**: affected phases
re-run in update mode against the sealed tree (definition delta with operator gate → architecture
delta → contracts delta with **mandatory** version bumps → isolated authors, changed components'
authors additionally receiving their own existing spec → emission reconcile → delta verification →
operator seal). Never regenerates untouched specs; honors NOTES deliberate cuts; code follows via
the repo's own case-B develop. ai-it's update-mode, ported to the factory. **Unexercised** — first
real exercise expected at L4. `SKILL.md` map + routing updated. Top-tier verification of this
standard change rides the founding tree's pending panel review.

Naming note: the emitted entrypoint stays the **operating manual** — ai-it's "orchestrator"
describes only the routing half of what it does (it also teaches: philosophy, QA layers, DoD).

Follow-up same day: `templates/start.md` case C gained the hand-back clause — an emitted repo
recognizes reshape-scale requests, stops, and returns them to the operator for a delta engagement
(soft reference to "the factory that emitted this repo, or its successor"; no path or tool
dependency — absent any factory, the repo can still reshape itself via its own `edit specs` /
`new component` sessions). feedler, emitted before this clause existed, can adopt it through its
own change process.
