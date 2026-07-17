# Phase 6 — Verification & Seal

The factory's exit gate. Two passes — mechanical, then judgment — followed by the operator's
countersign. Everything here follows `standards/verification_core.md`; this file only binds it to
the emitted-repo target.

## Inputs
- The complete emitted repo; the factory artifacts: `<run-dir>/inventory.md`,
  `consumer-ledger.md`, `taxonomy.md` (tier L), `notes-seed.md`, `<run-dir>/gates/` and the
  spot-verify records; specai's `NOTES.md` (non-eval — the sweeps); `standards/grammar.md`,
  `standards/style.md`, `standards/verification_core.md`, `standards/dial.md` §2, `templates/`
  (the grammar's tiebreaker; `notes.md` for the seal-line shape), `phases/emission.md` (the
  develop-loop offer rule).

## Pass 1 — mechanical (grammar conformance)
Run every check of the `grammar.md` §6 checklist literally, including their stated exemptions;
this file does not restate or count them. Fix mechanically; these findings never reach the
judgment pass; the verdict record carries one line of trace ("mechanical pass: N checks run, M
findings fixed"). By script where one exists, else by hand.

## Pass 2 — judgment (fresh-context lenses)
Dispatch per the tier row of `verification_core.md` §4 (verdict records at every tier — its §6).
**The phase-6 dispatch is the operator's to order** (`verification_core.md` §2 rule 4); the run
lead relays the templated briefs and declared packages as mechanical proxy, and the verdict
record names both.

Verifier package (independence rules apply): the emitted repo, `reference/ideation.md`, the
inventory + consumer ledger + NOTES seed and the gate copies (`<run-dir>/gates/`), the
spot-verify records plus `standards/dial.md` §2–§3, specai's `NOTES.md`, the lens briefs and conduct
rules (`standards/verification_core.md`), `standards/style.md`, `standards/grammar.md`,
`templates/` (the grammar's tiebreaker), and at tier L `<run-dir>/taxonomy.md`. **Eval
exception:** during an eval, specai's `NOTES.md` is excluded from this package
(`reference/exemplars.md` §3 rule 2), the IOU sweep lives at the operator's eval preamble (its
rule 6), and the exclusion is disclosed in the verdict record. **Never**: factory conversation,
phase working notes, prior seal-round reports (the spot-verify records above are the deliberate
exception).

**Verifier checks (verbatim — travels in the brief per `verification_core.md` §2 rule 4):**

```
1. Derive the fired-gate set from the tempo rule (dial.md §3; delta gates per delta.md steps
   1-3), then diff EVERY artifact under <run-dir>/gates/** against its sealed counterpart —
   unexplained post-gate changes are findings, and an absent or empty gates/<phase>/ for a
   fired gate blocks like an unpaid IOU. (Delta engagements: baselines live under
   gates/*-delta/; the inventory's counterpart is inventory-delta.md, the NOTES seed's is the
   appended repo-NOTES entry.)
2. Derive the expected spot-verify record count — from the tier's schedule (dial.md §2) for a
   full run, or for a delta from the re-run phases the appended repo-NOTES entry MUST
   enumerate — and count the records (verdict-spot-<phase>-<date>.md). A mismatch is a finding.
3. (non-eval seals) Sweep specai's NOTES.md for open IOUs and the exempted-edit bundle — a
   past-anchor IOU is a finding.
```

The two lenses that decide most seals — **ideation coverage** and **buildability** — live in
`verification_core.md` §5, cited whole, not restated. ("Nice UI, great UX" must land somewhere
real — a design spec with binding interaction behavior, not adjectives.)

Plus the **judgment gate** (`verification_core.md` §7 — its failure classes live there, cited
whole). This paragraph owns the dispatch shape (§4's rows cite it): at tier S the judgment-gate
brief **folds into the single verifier's dispatch** (one dispatch, reported as its own verdict
section); at M/L it is an **additional fresh context** beyond the lens verifiers.

## Fix loop
Route each finding to the phase that owns it (a coverage miss → phase 1/2; a contract hole →
phase 3, via its consumer; a component defect → a fresh context with that component's same closed
input list; a manual defect → phase 5). A fix that edits a **gate-approved artifact** re-triggers
the owning gate (`verification_core.md` §3). Re-verify with fresh verifiers who never see the
prior report. PASS = zero open blockers/majors (fixed or operator-accepted with recorded reason).

## The seal
Present to the operator: the verdict (findings + resolutions), the coverage summary (inventory →
tree), notable open questions living in the specs, NOTES, the **spot-verify records**
(`verification_core.md` §4 — an absent scheduled record blocks like an unpaid IOU), **specai's
open IOUs and exempted-edit bundle** (`change_rule.md` §5 rules 3–4 — an IOU past its anchor
blocks this seal until paid or operator-re-anchored with a recorded reason; at an eval's internal
seal this sweep is the operator's, at the eval preamble — `exemplars.md` §3), and — at S+ where
not already decided — the `develop_loop.md` offer (`phases/emission.md`; acceptance routes
through the sealed repo's own change process). **The operator's approval — and commit, which is
always the operator's act — is the countersign.** Record the seal in NOTES **with its
verification mode** (independent panel / single fresh verifier / degraded self-review —
`templates/notes.md`); the verdict record persists per `verification_core.md` §6 rule 4.

After the seal, specai's authority over the repo **ends**. `develop`, `design`, `verify`, and every
change request belong to the emitted `start.md`. A specai re-entry (re-running phases against a
sealed repo) is a new, operator-requested engagement that respects the repo's own change process
and NOTES history — never a silent regeneration.
