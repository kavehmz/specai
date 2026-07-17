# kimik3_notes2.md — Follow-up: review of the triage + seed regeneration (second pass)

**What this is:** the second external note (Kimi), following `kimik3_notes.md`. It records (a) my
verdict on the author session's triage of the first note, (b) one finding that turned out worse
than first reported, and (c) the change I applied myself at the operator's explicit instruction —
left **uncommitted** for the operator to review with the author before anything lands.
**Date:** 2026-07-17 · **Basis:** full re-read of the author session's diff (NOTES.md + 5 audit
records + the new `verdicts/taxonomy-seed.md`), the panel record's close section, and every raw
verifier report r2–r6 + the post-seal audit.

---

## 1. Verdict on the triage: approved, with two of my own errors conceded

The author session's handling was textbook `change_rule.md §5`: zero-gate bookkeeping applied
immediately (SHA fix, seed creation), everything panel-gated recorded as **queued** and kept out
of the tree (git status confirms no standards/SKILL/templates/phases files were touched), the
batching question deferred to the panel's own brief. The execution order (IOU panel → build-proof
→ tier-S delta drill → speclint) respects the IOU's letter.

The author's two corrections to my first review both verified against the record, and I concede
both (an erratum is appended to `kimik3_notes.md`):

1. **Round 6's five majors were fixed, not accepted.** The acceptance was: landing those fixes
   without a seventh blind round, plus standing accepted classes and one recorded edge (panel
   record, "Engagement close" items 1–3; NOTES round-6 entry: "All round-6 findings are fixed").
   My obs-2 framing was wrong. What survives of it: closure still ran on acceptance of
   *unreconfirmed* fixes — and the recorded reason ("blind reconfirmation has each round seeded
   equivalent new letter defects") is itself the ratchet evidence from obs 3.
2. **S3's anchor-relaxation is redundant.** `change_rule.md §5.4`'s "operator-re-anchored with a
   recorded reason" has been the legal deferral path since D1; the three deferrals I cited
   predated it. Brake-only adoption was the right call.

## 2. The seed finding, restated — and worse than first reported

The first note flagged `taxonomy-seed.md`'s patterns as paraphrased/compressed against
`verification_core.md §2` rule 1's "verbatim … never paraphrased … nothing else" (5 of 5 sampled
raw-report lines deviated). Regeneration revealed a second, objective defect class beyond
paraphrase: **four source records were mis-cited** —

- Three lines citing `reverify-r2-lens2-executability.md` carried findings that file does not
  contain (mid-run spot-verify dispatch legality; exempted-edit bundle durability; the
  definition-gate baseline omission). The findings are `reverify-r3-lens2-executability.md`'s
  M1/M3/M4 — r2-lens2's majors are M-1…M-5, none of them these.
- One line citing `reverify-r3-lens2` carried an r4-lens2 finding (phase-6 package embedding
  duties no conforming brief can deliver), plus an annotation ("as r4; first surfaced r3/r4
  boundary") that the format's "nothing else" does not license.

Why this matters beyond tidiness: the transform is exempt from the author ban *because* it
leaves no discretion; a paraphrased, mis-cited seed is a lead-curated artifact — the exact class
rounds 2–3 hardened against ("the lead's dedup cites, never replaces").

## 3. What I changed (uncommitted — review before landing)

At the operator's instruction I first **committed the author session's change set** as
`a77d382` ("external review triage: …"), so authorship boundaries are clean in history. On top
of that, uncommitted:

**`verdicts/taxonomy-seed.md` regenerated verbatim.** Every one of the 113 pattern lines
re-copied from its cited record under this stated convention (now in the file header): the
finding's bold issue statement — or the `**Issue:**` field's first sentence for locator-style
headers, or the panel record's consolidated finding text — completed from the running text when
the statement ends open (colon/em-dash); finding IDs, {where}/{severity} locators, markdown
emphasis, and the sentence-final period stripped; wraps rejoined; resolution text excluded.
Specific changes:

- All patterns verbatim (previously: paraphrases, truncations, and at least one meaning-altering
  generalization — the r6 lens-split line had dropped "tier-M" and "buildability").
- The four mis-citations corrected by moving the lines to the records that carry the findings
  (r2→r3 ×3, r3→r4 ×1); the "nothing else"-violating annotation dropped.
- Round-1 section: raw r1 reports were never preserved (disclosed limitation in the panel
  record), so patterns are the consolidated findings' **verbatim titles**, and findings the
  consolidation merged appear once (16 lines → 13).

**Self-verification, mechanical:** a ~20-line script normalized whitespace/emphasis and
substring-checked every pattern against its cited record: **113/113 verbatim**. The checker is
trivial to re-run (method: collapse whitespace, strip `*`, substring-test each pattern against
the cited file). This is worth pausing on — the verification the seed needed was a 20-line
script, which is the factory-mode speclint argument made concrete. Suggest the seed's
verbatim-ness become a permanent mechanical check (speclint factory mode, or a line in the
seal/eval preamble sweeps) rather than a one-time event.

**Deliberately not touched:** the author's coverage/dedup set, lens assignments, † flags, and
section structure. Two coverage gaps noticed but **not** fixed (adding findings is curation,
i.e. discretion — the panel's call, not a mechanical regeneration's): r2-lens2 M-3 (REG-lines
dangling at tier L with reg ≤ 1) and r6-lens2 finding 4 (the delta architecture spot-verify
package naming the absent full inventory) have no seed lines.

## 4. Nothing else outstanding from me

The queued standards batch (S2 accepted-majors fold-in, the normative-sentence brake, the S8
floor line) is correctly parked behind the IOU-payment panel; the IOU payment, the tier-S
build-proof, the delta drill, and speclint are operator-ordered dispatches/builds, all pending.
I have no further change requests.

## 5. For the reviewing author — what to check

1. Re-run the verbatim check (§3) — 113/113 should hold; the two files to spot-check by eye if
   you sample: `reverify-r3-lens2-executability.md` (the three moved lines) and
   `reverify-r4-lens2-executability.md` finding 2 (the fourth).
2. Confirm the round-1 collapses against the panel record's round-1 section (the consolidation
   merged what the first seed listed as separate lines; raw reports gone, verbatim titles are
   the only honest pattern source).
3. Decide the two coverage questions in §3 (strictly, rule 1 says "one line per closed
   blocker/major" — the seed is a deduped set, not a complete one; that was true of the first
   seed too and is recorded as a choice, not smuggled).
4. Consider adopting the permanent verbatim-guard suggestion (§3) into the speclint work order.

## 6. Disclosure

- `a77d382` = the author session's change set, committed by me at the operator's explicit
  instruction ("first commit the current change"). Its content is the author's.
- Uncommitted on top: the seed regeneration (this note's §3).
- Files I own, untracked, operator's to keep or discard: `kimik3_notes.md` (+ erratum),
  `kimik3_notes2.md`. (`specai.html`, the visualization from the first session, is no longer in
  the working tree — removed while untracked; it carried no skill content.)
