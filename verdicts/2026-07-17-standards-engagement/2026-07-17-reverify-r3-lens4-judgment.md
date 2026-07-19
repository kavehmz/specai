# Blind re-verification round 3 — lens 4: judgment gate + adversarial (verbatim report)

*Preserved verbatim per `verification_core.md` §6 rule 4. Dispatcher: the operator by standing
order; lead as mechanical proxy. Package: the full tree minus `verdicts/` and `.git`.*

---

## DISCLOSURE — ambient context injected into this session

- A harness system-reminder carrying a user email and today's date (2026-07-17).
- Environment preamble: cwd, platform, and a **git status block naming the current branch and five recent commit subjects**. This leaks a sliver of authoring history despite my no-history mandate; I did not act on it, but per the tree's own contamination rule (SKILL.md §4) it must be disclosed.
- A harness skills/tools listing — irrelevant, not used.
- No CLAUDE.md and no memory files were injected.

## VERDICT: **FAIL** — 2 blockers, 9 majors, 3 minors

### Blockers

**B1 — IOU "payment" is defined as verdict *return*, not verdict *PASS*: a FAIL verdict pays the IOU and unblocks seals and evals.**
- **where:** change_rule.md §5 rule 4 (and the live IOU in NOTES.md, final entry)
- **issue:** "An IOU is paid by the owed gate's verdict returning over the tree that contains the change" — a returned FAIL satisfies the letter. Nothing requires the FAIL's findings to be fixed or operator-accepted before the IOU is cleared. This directly contradicts verification_core §3 ("No PASS, no done"). Not hypothetical: the tree's own last two confirmation rounds returned FAIL ×4, and the open IOU is written in exactly this letter.
- **fix:** Redefine payment: "An IOU is paid by the owed gate **closing** over the tree containing the change — a PASS verdict, or a FAIL whose blockers/majors are fixed-and-reconfirmed or operator-accepted with recorded reason. A returned FAIL converts the IOU into an open fix loop; it never clears it."

**B2 — The eval answer-key quarantine is still incomplete: README.md carries an exemplar name, violating the "only home" invariant.**
- **where:** README.md §Invoke; contradicts exemplars.md header and grammar.md header
- **issue:** README — binding text per change_rule §5 rule 3 and **not** on the eval exclusion list — names the tier-S fixture twice; combined with the clone URL, an eval run with web access reconstructs the reference tree in one guess. NOTES' claim "the quarantine completed" is falsified.
- **fix:** README examples become placeholder-form; grep the tree for both fixture names before the next eval; add README.md explicitly to the quarantine sweep list.

### Majors

**M1 — Gate copies are not tamper-evident: the lead writes them, the lead can rewrite them, and nothing commits them at gate time.** Concrete cheat: after gate approval, delete an inconvenient checkpoint-sourced R-line from inventory, seed, **and** both gate copies — the phase-6 diff shows nothing (checkpoint-sourced lines exist only in lead-writable files). A copy the suspect can rewrite is not tamper-evident. **Fix:** the gate approval act includes the operator committing `<run-dir>/gates/<phase>/` (or recording content hashes in the operator's own approval); a gate is approved only when its baseline is operator-fixed.

**M2 — The definition gate copies omit vision.md, the most load-bearing gate-approved artifact.** Concrete cheat: post-gate, edit the binding Dial line from M to S — the seal runs with 1 verifier instead of 2 + judgment context, and no surface records the difference. Same hole for demoting an identity non-goal to revisitable. **Fix:** every gate copies **every artifact it approved**; the phase-6 diff covers all baselined artifacts.

**M3 — The verifier's actual package and brief are lead-asserted, never verifier-attested.** Concrete cheat: dispatch a verifier omitting the one file carrying the contradiction, then write the full declared package into the verdict record; "any deviation is disclosed in the verdict" — disclosed by the deviator. **Fix:** (a) every verifier report MUST open by echoing verbatim the brief and file list it received; (b) each dispatch prompt is preserved verbatim beside the raw report it produced.

**M4 — Eval contamination via verdicts/:** the L4 eval's taxonomy assembly reads committed verdict records whose verbatim raw reports quote exemplar answer-key facts; verdicts/ is not on the eval exclusion list. **Fix:** exemplars §3 rule 2 adds verdicts/ to the exclusion; an eval run's taxonomy is staged by the operator from taxonomy-seed.md after a names/facts scrub, or starts empty.

**M5 — The eval's integration proof has no independent dispatcher, and at tier S its exit criterion is self-graded by construction.** The tier-S independent-verification line *is* the builder verifying with its own fresh eyes; no one but the builder is required to exist, and no rule names who dispatches the build proof. **Fix:** the proof's verification pass is **operator-dispatched to a fresh context**, regardless of the emitted repo's tier; the fresh context, not the builder, signs the DoD's independent-verification line.

**M6 — The exempted-edit bundle has no durable home: it can only rot.** Any session boundary silently empties the bundle; nothing could ever detect the loss. **Fix:** each exempted edit gets a one-line entry in NOTES.md under a standing "Exempted edits" heading (or a committed ledger); the preamble enumerates from that file.

**M7 — The cascade set is "derived, never asserted" — but derived by the interested party, and the focused-pass verifier structurally cannot detect under-derivation.** Concrete cheat: change a contract, "miss" one consuming component spec, dispatch the focused pass without it. **Fix:** the focused-pass verifier receives the whole spec tree and its **first task is to re-derive the cascade set independently**; a mismatch with the dispatcher's named set is itself a finding.

**M8 — Scheduled spot-verify records and the IOU sweep are enumerated only by the lead — the collectors are fed by the party whose omissions they exist to catch.** Concrete cheat: at tier L, skip the contracts spot-verify; enumerate two records at the seal. **Fix:** add the spot-verify records plus dial.md §2 to the seal verifier's package with an explicit expected-count check; the seal verifier receives NOTES.md (factory seals) and checks recent binding-file changes against recorded gates/IOUs.

**M9 — Tier-S single-context sequential authoring is licensed while claiming an impossibility, with no disclosure duty.** One context that has just authored component A cannot honor an input list excluding A's spec while authoring B. **Fix:** sequential single-context authoring is a named degraded mode; the NOTES seed and verdict record MUST carry an "authoring isolation: degraded" line; the phase-6 consistency lens weights cross-component anchoring accordingly.

### Minors

**m1 — dial.md §2's table is structurally broken** by the interposed parenthetical; the spot-verify schedule definition depends on table integrity. Fix: move it.
**m2 — The taxonomy transform's "leaves no discretion" claim is false:** the `pattern` field is authored free text. Fix: define the pattern as a verbatim copy of the source finding's `issue` field, truncated, never paraphrased.
**m3 — The eval protocol is not a panel-gated self-governing surface:** a weakening edit to eval hygiene is the highest-leverage self-serving change available and gets the lightest gate. Fix: add exemplars.md §3 to change_rule §5 rule 2's enumerated surfaces.

### Judgment summary

The tree genuinely teaches, the phase cuts are coherent, and the ledger is unusually honest — it discloses its own FAILs, self-dispatch history, and an operator-accepted style debt. But the round-3 thesis recorded in NOTES — "the correct fixes are operator-visible tamper-evident surfaces… rather than more lead-maintained rules" — is not yet true of the tree as built: every surface it added is still produced, held, or enumerated by the lead. The two blockers are letter-level: one lets a FAIL verdict discharge the debt that exists to prevent exactly that, and one leaves an exemplar name in a non-excluded binding file after the ledger declared the quarantine complete. FAIL.
