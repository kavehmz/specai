# NOTES — specai decision ledger (founded 2026-07-11)

The operator's record of what was decided and why. A record, not a spec — the `standards/` and
`phases/` files win. (specai eats its own dog food: this is the `templates/notes.md` discipline
applied to the factory itself.)

## Open state (read first — the live items)

- **Open IOU** (`change_rule.md` §5.4, from the 2026-07-17 postseal audit): change = the audit
  fixes (`c3ea19a`) · owed gate = focused pass + panel per §5, verdicts returned **and closed** ·
  anchor = before the next seal or eval.
- **Queued for that panel batch (operator-decided, NOT landed):** S2 — operator-accepted majors
  fold into NOTES open topics with reason/date/revisit anchor · S3-brake — no new normative
  sentence lands without naming the finding it answers · S8 — definition checkpoint gains an
  honest-floor option below ~dial 2 (one-verifier gate). Batching question (one landing = one
  panel) is put to that panel's brief.
- **Adopted execution order:** IOU payment → tier-S delta drill on the emitted feedler repo →
  speclint.py (emitted + factory modes, with the seed verbatim-guard; recover the L1 run's seed
  script if present).
- **Unexercised:** the delta engagement (`phases/delta.md`) — first real exercise was expected
  at L4; the tier-S delta drill above now precedes it.
- **Deferred from founding:** whether tier-M/L repos get `develop_loop.md` by default (decide
  after the delta drill) · skill packaging polish (frontmatter beyond name/description).

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

*(The founding tree's verification was deferred at founding and paid by the 2026-07-17 panel —
see the standards-engagement entry. Operator countersign of the founding = Kaveh's first commit.)*

## 2026-07-11 — L1 eval: reproduce feedler — comparison PASS (relabeled 2026-07-17)

specai's first full run, same day as founding: dial 2 → tier S (matching the calibration anchor),
six isolated component authors, four blind verification rounds (majors 4→1→1→0), sealed as
**specai-feedler** (github.com/kavehmz/specai-feedler) — 4,113 spec lines from a 27-line ideation.
Comparison vs the hand-built reference: grammar conformance EXCEEDS, ideation coverage PARITY,
decision quality parity-leaning-exceeds, buildability parity on paper. **Relabeled 2026-07-17**
when eval hygiene hardened (`exemplars.md` §3): the run pre-dated the protocol (target exemplar
was readable; comparison self-dispatched), so the honest verdict was "comparison passed;
build-proof pending" — the build-proof is now done per the operator (see the 2026-07-19
build-proofs entry). Eight process learnings from this run were applied via `improve specai`
(rationale placement, benchmark checkpoint, riding-minors seal policy, tier-S traceability stub,
neutral-dir eval rule, orchestrator-relays pattern, disk-state resume, the speclint seed).
Full audit trail: the specai-feedler repo's `.specai-run/`.

## 2026-07-12 — The delta engagement designed

Gap exposed by operator review: the factory-side re-entry for product-reshaping change was a
placeholder. Closed as `phases/delta.md` — affected phases re-run in update mode against the
sealed tree (definition delta with operator gate → architecture delta → contracts delta with
mandatory version bumps → isolated authors → emission reconcile → delta verification → operator
seal). Never regenerates untouched specs; honors revisitable cuts; code follows via the repo's own
case-B develop. Same day: `templates/start.md` case C gained the hand-back clause (reshape-scale
requests return to the operator for a delta engagement; the repo can still reshape itself via
`edit specs` if no factory is available). **Unexercised** — see Open state.

## 2026-07-17 — DRIFT.md joins the grammar

Gap from a week of operating a production spec-first monorepo: no home for durable code-vs-spec
divergence. Decision: emitted repos gain `DRIFT.md` — non-binding, dated, per-component, each item
naming divergence + owning spec § + fix owed; deleted item-by-item when fixed, deleted entirely
when empty (absence asserts conformance); never a build input; spec-ahead-of-code **is** drift.
Three tenses: specs = what is true · NOTES = why decided · DRIFT = where reality lags.
Homes: `grammar.md` §4.10 and the files its entry lists. Two self-dispatched pre-commit review
rounds ran (self-QA, not the gate); the gate rode the panel below.

## 2026-07-17 — The standards engagement: panel FAIL → six rounds → sealed

The operator dispatched the full standards panel over the whole skill at `1af9e4e`, paying the
gates deferred by the founding tree, the delta engagement, and the DRIFT change. **Panel: FAIL ×4
— 0 blockers, ~24 deduped majors.** The operator resolved six design decisions (D1–D6: review
weight keyed to target doc; money machinery keyed to the dimension; independence = channel with
zero-discretion dispatch; tier binds in vision.md; eval excludes the target exemplar + no PASS
without build-proof; licensed-HOW exception scoped). The fix loop then ran **six blind
re-verification rounds** — trajectory: blockers 1→3→3→1→0, majors ~24→~9→5 (structural →
letter-level). The ledger caught and corrected **two false claims of its own** mid-engagement;
the **IOU mechanism** (`change_rule.md` §5.4, payment = the gate *closing*) was born here; the
trust-root class (lead-held baselines, lead-assembled packages) was **operator-accepted with
reason** (the countersign commit is the operator-fixing act; per-gate commits declined as
ceremony). Closed by operator triage-and-close + countersign at `630ac46`. Standing practices
left behind: verbatim raw verifier reports · the taxonomy seed · the exempted-edits ledger ·
tamper-evident gate copies · "a gate has run only when its verdict is returned."
Full record (panel + D1–D6 packet + raw r2–r6 reports + per-round resolution logs):
`verdicts/2026-07-17-standards-engagement/`.

## 2026-07-17 — Postseal audit: 0 blockers, ~9 majors fixed; IOU left open

After the seal (`630ac46`) the operator invited one more four-lens audit (information, not a
gate): FAIL ×4 with zero blockers. The two catches that justified it: the **money-path definition
never reached the emitted world** (emitted repos gated on a term only a factory file defined) and
**gate-copy tamper evidence failed open on absence** (absence now blocks like an unpaid IOU).
All findings fixed in `c3ea19a`. The engagement left the **open IOU** recorded in Open state
above. Record: `verdicts/2026-07-17-postseal-audit/`.

## 2026-07-17 — External review (Kimi) triaged; taxonomy seed created and re-verified

An outside AI's review of the tree was assessed: high quality — its checkable claims verified
(orphaned seal SHA, missing taxonomy seed, unexercised delta, deferred speclint), with two
substantive corrections (round 6's majors were *fixed*, not accepted; the IOU was already the
legal deferral path). Zero-gate bookkeeping: the orphaned seal SHA corrected (`d86eec3` →
`630ac46`) across this ledger and five audit records; `verdicts/taxonomy-seed.md` created by the
§2-rule-1 mechanical transform. A follow-up regenerated the seed (the first version paraphrased
against the verbatim letter and mis-cited four source records — caught by exactly the review
symmetry the rules exist for); this session independently re-verified **115/115 verbatim**, and
the **seed verbatim-guard** joined the speclint work order. Operator decisions S2/S3/S8 queued —
see Open state. Commits: `a77d382`, `3d15333`.

## 2026-07-19 — Records housekeeping: verdicts/ regrouped by engagement

Zero-gate bookkeeping. The 27 flat records under `verdicts/` moved into two engagement
subdirectories (`2026-07-17-standards-engagement/`, `2026-07-17-postseal-audit/`) with
`taxonomy-seed.md` and a one-page index (`verdicts/README.md`) at top level; basenames unchanged;
raw reports untouched; full-path citations re-pointed. Commit: `bf93176`.

## 2026-07-19 — Build-proofs exist (operator report)

The operator reports **two working build-proofs**: (1) **feedler** — public, built and working
from the specai-emitted spec repo (the L1 integration proof owed since 2026-07-11); (2) the
**trading platform** — private, the doctrine running at tier-L scale in production (the hand-grown
exemplar tree, not a specai emission). Records live in their own repos. The operator may later
rebuild a **public tier-L product from scratch** with specai — that run would double as the L4
eval. *(Ledger note: whether the feedler build ran the full eval-grade ceremony of `exemplars.md`
§3 rule 4 — operator-dispatched builder + independent DoD-signing verifier — is to be confirmed
by the operator; if it ran informally, this line should say so honestly.)*

## 2026-07-19 — Ledger compression

Housekeeping, on external review feedback (Kimi): closed engagements compressed to summaries with
pointers (all detail preserved verbatim in `verdicts/`); the founding entry kept in full; the new
**Open state** section collects the live items (IOU, queued decisions, execution order, deferred
questions) so compression can't bury them. No decision content changed; no gated file touched.
Operator countersign = the commit.

## Exempted edits
- 2026-07-17 · NOTES.md + 5 verdicts/ records · orphaned seal SHA corrected (record fix, ungated
  by nature; logged here for the one-reader guarantee).
- 2026-07-19 · verdicts/ (27 records → two engagement subdirs + index README) · NOTES.md + panel
  record + D1–D6 packet full-path citations re-pointed (record bookkeeping, ungated by nature).
- 2026-07-19 · NOTES.md · stale "Currently empty." dropped from this heading's parenthetical.

*(standing heading per `change_rule.md` §5 rule 3 — one line per typo/clarity-exempted edit;
enumerated at every seal/eval preamble.)*
