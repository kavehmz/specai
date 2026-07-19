# Blind re-verification round 4 — lens 1: consistency/contract (verbatim report)

*Preserved verbatim per `verification_core.md` §6 rule 4. Dispatcher: the operator by standing
order; lead as mechanical proxy. Package: the full tree minus `verdicts/` and `.git`.*

---

**Disclosure of ambient context beyond this prompt and the listed files:** a system-reminder carrying a user email and today's date; a system prompt with environment info including git status and recent commit titles ("verdicts and review", "adding the concept of drift"); tool/skill listings. None of it informed the findings below; I read nothing outside the 21 listed files.

# Lens verdict: **FAIL** — 1 blocker, 4 majors, 10 minors

## BLOCKER

**B1 — Eval runs cannot satisfy both the phase-6 seal rules and the eval hygiene rules; the NOTES.md exclusion contradicts the seal package and the IOU collector.**
- **where:** phases/verification.md §Pass 2 + §The seal; reference/exemplars.md §3 rule 2; standards/change_rule.md §5 rule 4
- **issue:** An eval run is "a normal `new product` run plus a comparison verdict", so it ends in a phase-6 seal. Phase 6 mandates specai's NOTES.md in the verifier package and an IOU sweep at the seal presentation — but eval hygiene makes NOTES.md off-limits to the run, and the IOUs live in NOTES.md. A conforming eval is impossible: follow verification.md and the eval "proves nothing"; follow exemplars.md and the seal package/collector rules are violated. The exclusion "overrides only SKILL §0, not verification.md's package". The tier-L taxonomy got exactly the needed carve-out, proving the pattern was known and this item was missed.
- **fix:** Condition the package item and the seal-time sweep: at eval runs the IOU/exempted-edit sweep is the operator's at the eval preamble and specai's NOTES.md is excluded from the package, disclosed in the verdict record. Mirror one line in exemplars §3 rule 2.

## MAJORS

**M1 — The conforming brief forbids the content the attestation rule requires.** Rule 4 defines the brief as a closed list ending "nothing else", then mandates that every verifier report open with a verbatim attestation — never delivered through the only licensed channel. Same gap for the default-accepted weighting (definition step 5), which appears in no §5 lens row. Fix: add the attestation/conduct clauses ("§2 rules 2–4 verbatim") to the brief enumeration; move the default-accepted weighting into the §5 coverage row.

**M2 — delta.md step 1 erases the identity/revisitable split**: "non-goals are the firewall — a request that violates one stops here" vs change_rule §2.1's "a request against a non-goal marked revisitable … is not a stop". Precisely in the engagement whose job is operator-ordered reshaping. Fix: identity non-goals stop; revisitable cuts route as operator-confirmed vision edits.

**M3 — The delta engagement drops the tamper-evidence and collector chain**: steps 1/3 never copy gate approvals to gates/; step 6's package omits gate copies, spot-verify records, and the NOTES/IOU sweep — baseline diff and record-count checks impossible at a delta re-seal. Fix: add the gate-copy acts and extend step 6's package/seal duties (or cite phases/verification.md's).

**M4 — SKILL §4's degraded-seal IOU waives the anchor §5.4 makes mandatory** and parks the IOU in the emitted NOTES, which the collector never sweeps. Fix: use §5.4's operator-re-anchored form in specai's NOTES.

## MINORS

m1 — residual fuzzy echoes: dial preamble "an eight-component tree" (matches the L exemplar's "8 platform components"); definition inputs "a page of informal brain-dump … multi-thousand-line suite" (echoes the §1 fixture description). **Otherwise the invariant holds in every binding document, README.md included.**
m2 — verification-mode triple spelled verbatim in three files; one should own.
m3 — dial §2 puts the money round only in the L column while the note keys it to the dimension; footnote the cell.
m4 — phases/verification.md judgment-gate restates §7's failure classes; emission output 1 restates the S command list grammar §4.3 assigns to the template.
m5 — restated pinned values, all currently agreeing (tier ranges; ≤3 threshold; consumers-appendix pin; stable-ID ladder; "seven document skeletons").
m6 — README five-sentences "see only…" understates the closed list.
m7 — SKILL §2 eval row drops "any candidate repos it names" from the exclusion summary.
m8 — "checkpoint" residual overload (vc §2.6 "human checkpoint"; dial §2 row header "per phase").
m9 — taxonomy assembly counts findings from seed and source records twice; dedupe by source.
m10 — templates/vision §2 "Why now" dial-gate exists only in the template; grammar's (dial) legend points at dial.md which never mentions it.

## Clean categories
Citation resolution: every citation checked resolves; the say-what-the-citer-claims failures are exactly B1/M1/M2/M4. Canonical terms otherwise single-meaning (tempo, spot-verify schedule, seal, close, dispatcher, registrar, fresh context, focused pass, top tier). Gate/tempo/spot-verify schedules agree exactly across all homes. NOTES.md honesty: every claimed fix verifiably present except the dial-preamble echo (m1).
