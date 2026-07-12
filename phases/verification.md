# Phase 6 — Verification & Seal

The factory's exit gate. Two passes — mechanical, then judgment — followed by the operator's
countersign. Everything here follows `standards/verification_core.md`; this file only binds it to
the emitted-repo target.

## Inputs
- The complete emitted repo; the requirements inventory + consumer ledger (factory artifacts);
  `standards/grammar.md` §6, `standards/verification_core.md`, `standards/dial.md` §2.

## Pass 1 — mechanical (grammar conformance)
Run the `grammar.md` §6 checklist literally: required files, boot-table completeness both
directions, citation resolution, glossary discipline, Acceptance+Deliverables endings, contract
Version headers, requirement-language declaration, binding worked examples present, ideation
preserved, NOTES seeded. Fix mechanically; these findings never reach the judgment pass.
*(Automation: a speclint-class script is the intended form — `NOTES.md` tracks it as deferred
tooling; until it exists, the checklist is run by hand.)*

## Pass 2 — judgment (fresh-context lenses)
Dispatch per tier (`verification_core.md` §4): S = 1 verifier, all lenses; M = 2, split;
L = panel ≥3 + adversarial re-verify + verdict record.

Verifier package (independence rules apply): the emitted repo, `reference/ideation.md`, the
inventory + consumer ledger, the lens briefs (`verification_core.md` §5), `standards/style.md`,
`standards/grammar.md`. **Never**: factory conversation, phase working notes, prior reports.

The two lenses that decide most seals:
- **Ideation coverage:** every ideation ask and checkpoint answer → a binding clause, or a
  deliberate cut recorded in NOTES. The verifier reads the ideation *first*, builds their own
  expectation of the product, then hunts the tree for each expectation. ("Nice UI, great UX" must
  land somewhere real — a design spec with binding interaction behavior, not adjectives.)
- **Buildability (the rebuild test):** could a fresh AI, handed only this repo, build the product
  and know when it's done? Walk `develop <product>` mentally end-to-end through the boot table:
  every reading list sufficient, every acceptance gate concrete, every mandated behavior reachable
  (executability), nothing left to guess.

Plus the **judgment gate** (`verification_core.md` §7): one review licensed to fail a conforming
tree — wrong product, incoherent boundaries, a manual that routes but doesn't teach.

## Fix loop
Route each finding to the phase that owns it (a coverage miss → phase 1/2; a contract hole →
phase 3, via its consumer; a component defect → its isolated author-context; a manual defect →
phase 5). Re-verify with fresh verifiers who never see the prior report. PASS = zero open
blockers/majors (fixed or operator-accepted with recorded reason).

## The seal
Present to the operator: the verdict (findings + resolutions), the coverage summary (inventory →
tree), notable open questions living in the specs, and NOTES. **The operator's approval — and
commit, which is always the operator's act — is the countersign.** Record the seal in NOTES.

After the seal, specai's authority over the repo **ends**. `develop`, `design`, `verify`, and every
change request belong to the emitted `start.md`. A specai re-entry (re-running phases against a
sealed repo) is a new, operator-requested engagement that respects the repo's own change process
and NOTES history — never a silent regeneration.
