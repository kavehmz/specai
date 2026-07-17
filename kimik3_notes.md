# kimik3_notes.md — External review of the specai tree (observations + suggestions)

**What this is:** an outside AI's (Kimi) read of the specai skill tree, written for the operator to
review **with another AI before acting**. Nothing here is binding; nothing here has been applied to
the tree. Treat every claim as a hypothesis to check against the files cited.
**Date:** 2026-07-17 · **Basis:** full read of `SKILL.md`, `README.md`, `NOTES.md`, all of
`standards/`, `phases/`, `templates/`, `reference/exemplars.md`, plus a delegated full read of all
27 files in `verdicts/`. Git history inspected for one specific check (observation 7).
**Tree state reviewed:** HEAD = `c3ea19a` (post-seal audit + fixes), one open IOU.

---

## 0. One-paragraph context (for the reviewing AI)

specai is a harness-agnostic agent skill: a human ideation enters a six-phase factory (definition →
architecture → contracts → parallel isolated component authoring → emission → verification/seal)
and exits as a **sealed, self-operable spec repository** a future AI can build/verify/change from
using only the repo's own `start.md`. It obeys its own change rule; its own verification history
(six blind re-verification rounds against a founding panel, sealed 2026-07-17, then a post-seal
audit) is in `NOTES.md` + `verdicts/`. One IOU is open: focused pass + panel over the post-seal
fixes, anchored **before the next seal or eval — named: the tier-S build-proof or L4, whichever
first** (`NOTES.md`, post-seal entry).

## 0.1 Verified vs. inferred

- **Verified by direct read/git:** all finding counts below (from `NOTES.md` entries + the verdict
  subagent's cross-check); the orphaned SHA (obs 7); the absence of `verdicts/taxonomy-seed.md`
  (no file, no git history); the delta engagement's unexercised status (`NOTES.md` 2026-07-12);
  the deferred speclint (`NOTES.md` founding + L1 entries); the local checkout of the emitted
  tier-S repo at `../specai-feedler`.
- **Inference/judgment (the reviewing AI should attack these hardest):** the "complexity ratchet"
  reading of the round counts (obs 3); "convergence runs on operator acceptance" (obs 2); the
  proportionality suggestion (S3) — the most contestable item here, see §3 note.

---

## 1. Observations (problems), ranked

### 1. The core empirical claim is still unproven — and it is the IOU's anchor
The factory's load-bearing promise: *a better AI, given only the emitted repo, rebuilds the
product.* As of 2026-07-17 no emitted repo has been built end-to-end by a fresh AI through its own
`start.md` under the hardened protocol (`exemplars.md §3` rule 4). The L1 build-proof has been owed
since 2026-07-11; the 2026-07-12 "GPT builder obeyed it" note is anecdote, not proof. The open IOU
is anchored on this very event. Everything else achieved so far (grammar conformance, comparison
parity) is secondary evidence for the central claim.

### 2. Convergence happened by operator acceptance, not by PASS — and acceptances have no collector
Every round of the 2026-07-17 engagement FAILed (panel: 0 blockers/~24 majors; r1: 1/~29 raw
(~20 deduped); r2: 1/~18; r3: 3/~21; r4: 1/~10; r5: 1/~9; r6: **0 blockers**, 5 majors). The
engagement closed via the operator's standing triage-and-close; round 6's five majors were
**accepted**, not fixed. (Contrast: the 2026-07-11 tier-S product seal did reach zero majors — the
no-clean-PASS pattern holds for the skill tree, not universally.) For *built* products,
operator-accepted findings land in `DRIFT.md` (`verification_core.md §6` rule 2). For **spec-tree
seals there is no equivalent fold-in**: accepted majors live only in the verdict record, and no
collector ever re-surfaces them — unlike IOUs, which block seals past their anchor. Operator
acceptance is the real convergence mechanism; fatigue risk is structural.

### 3. A complexity ratchet is visible in the engagement's own data *(inference — attack this)*
Majors went 24 → 29 → 18 → **21** → 10 → 9 → 5: the count *rose* twice mid-loop because each
hardening added new normative letter, and letter-level enumeration misses were the dominant defect
class (sibling paths: eval-internal seals, delta seals, spot-verify briefs — round 4's named
disease; the README fixture-name leak; fenced-check drift). Each fix was individually correct, but
the normative surface monotonically grows, and every added rule is a future cross-document
inconsistency (map rot was itself a finding class). Meanwhile the self-governance weight
(panel per self-governing-surface edit) is calibrated for a blast radius the skill does not yet
have: exactly one emitted repo exists, and zero external consumers depend on this tree.

### 4. The mechanical pass is run by hand — the cheapest high-ROI gap
Phase 6 pass 1 (`phases/verification.md`: "run every check literally, fix mechanically") has been
hand-executed since founding; `speclint` is a deferred founding item. The L1 run materialized a
`speclint.py` unprompted (NOTES, L1 entry, learning 8) and it was never harvested. The defect class
that dominated rounds 1–5 — letter-level enumeration misses — is precisely the class a script
catches deterministically and humans miss.

### 5. The delta engagement is unexercised and is the most substitution-wired file in the tree
`phases/delta.md` (designed 2026-07-12, "Unexercised — first real exercise expected at L4") is ~100
lines of named substitutions (ideation→change-request, inventory→inventory-delta,
gates→`gates/*-delta/`, consumer-ledger conditional, NOTES-seed→appended entry…). Round 5's blocker
was exactly a delta-package contradiction. Current plan = first live fire at maximum stakes (L4).

### 6. `verdicts/taxonomy-seed.md` does not exist
Referenced by `SKILL.md` §1/§5 and `verification_core.md §2` rule 1 as the cross-run accumulation
point; never created (no product run has sealed since the rule exists). Mitigating fact the
reviewing AI should weigh: the assembly rule reads the seed **plus post-seed records**, so the next
tier-L run's taxonomy would still see the panel's patterns via the raw records — the seed is a
dedup/efficiency device, not a correctness hole. Still: ~60 closed blocker/major findings with
source records sit in `verdicts/` and the transform is mechanical.

### 7. A stale commit reference survived the honesty machinery (verified)
`NOTES.md` (post-seal entry) and `verdicts/2026-07-17-postseal-audit.md` cite the seal as
`d86eec3`. `git cat-file` shows it exists but is **unreachable from any branch**: the seal commit
was amended into `630ac46` (same message, reachable). HEAD is `c3ea19a`. This is the *second*
instance of the class (`ec501fb` "drop stale commit reference"), and it passed the round-6
ledger↔tree truthfulness check — suggesting that check does not cover SHA references in prose.

### 8. Two design questions (not defects)
- **No floor:** tiers add, never remove; nothing in routing says "this ideation is under the
  factory's worth." A 27-line ideation → 4,113 spec lines is the demonstrated class; below roughly
  dial 2 the factory likely over-emits, and the honest answer should be sayable at the definition
  checkpoint.
- **Brittle numbered citations:** the factory tree cross-cites by number (`§4.10`, `§5 rule 4`)
  while its own style rule 9 prefers named-section citations. Insertions renumber silently; map rot
  was already a finding class. (Do **not** mass-renumber — churn without behavior change.)

---

## 2. Suggestions (solutions), mapped to the observations

Each entry: the fix · where it lands · the gate specai's own `change_rule.md §5` puts on it.

### S1 (obs 1) — Pay the IOU, then run the build-proof. In that order.
The IOU's letter fixes the sequence (anchor = before the next seal or eval, build-proof named).
1. **IOU payment:** operator orders a focused pass + panel (≥3 fresh lenses) over the post-seal
   *fix* diff in `c3ea19a` (standards/templates changes, excluding the audit record files); run
   lead relays templated briefs as mechanical proxy (`verification_core.md §2` rule 4). Verdicts
   must return **and close** (`change_rule.md §5.4` — a returned FAIL does not pay).
2. **Build-proof** (`exemplars.md §3` rule 4) against the local `../specai-feedler` checkout:
   operator stages a copy into a **neutral working directory**; operator orders two dispatches —
   (a) a fresh builder told only `develop feedler` through the repo's own `specs/start.md`;
   (b) a separate fresh verifier that drives the running product and signs the DoD's
   independent-verification line (never the builder). Run manifest attaches to
   `verdict-comparison-L1.md`; verdict upgrades from "comparison passed; build-proof pending."
3. If the proof fails: findings route to `improve specai` — the loop working as designed, and the
   most informative failure available.

### S2 (obs 2) — Fold accepted majors into the existing collector (no new machinery)
- `verification_core.md §6` rule 1: extend "riding minors fold into the emitted NOTES open topics"
  to **"riding minors and operator-accepted majors (each with acceptance reason, date, and a
  revisit anchor)"**.
- specai's own `NOTES.md` gains the same standing heading; round 6's five accepted majors are
  retro-entered (they are already named in the panel record's close section).
- **Gate:** §6 is a self-governing surface → panel. Batch with S3 + S8 (see S8 note).

### S3 (obs 3) — Make the practiced proportionality legal + a ratchet brake *(most contestable)*
- `change_rule.md §5` gains one sentence: *"Where a change cannot invalidate any sealed emitted
  repo — none exist that cite the changed surface — the owed gate's anchor may be set to the next
  seal or eval that does have downstream consumers; the reasoning is recorded."* This converts the
  thrice-repeated deferral exception (founding tree, delta, DRIFT) into a rule.
- Ratchet brake, one line in the same section: **no new normative sentence lands without naming
  the finding it answers** (the resolution-log discipline, applied prospectively).
- **CAUTION for the reviewing AI:** this weakens a gate that demonstrably caught real defects. The
  alternative reading of obs 3 is "the machinery worked — six rounds is what convergence costs."
  Argue both sides before adopting. **Gate:** §5 self-governing → the same batched panel.

### S4 (obs 4 + 8b) — Build `speclint.py` (two modes)
- **Emitted-repo mode:** grammar §6 checks 1–5, 7, 8 fully mechanical (required file set;
  boot-table reachability of every `specs/` file minus the two exemptions; cross-document citation
  resolution; glossary single-definition + additions-only discipline; Acceptance Criteria +
  Deliverables presence; contract Version headers + RFC 2119 declaration; ideation/Dial-line/
  NOTES-seed presence; no `DRIFT.md` at first seal; no template scaffolding). Check 6 as
  report-only (binding sections lacking labeled worked examples).
- **Factory mode:** check 2's citation resolution against the specai tree itself — every numbered
  `§`-citation becomes machine-verified; map rot becomes a caught error.
- Recover the L1 seed (`speclint.py` + factory-id guard) from the feedler run dir if present;
  test against `../specai-feedler`.
- **Gate:** none (code, not binding text); `SKILL.md` map + `README` layout + NOTES entry when
  kept, per the files-added rule.

### S5 (obs 5) — Tier-S delta drill before L4
After the build-proof, on `../specai-feedler`: one real, small, reshaping request (one new
component or one contract surface — big enough to re-run phases 1–4 in update mode, small enough
to stay tier S). Full delta path: `change-request.md` → definition delta (gate) → architecture
delta → contracts delta (**mandatory version bump** — the pre-seal no-bump allowance must not
fire) → changed-component re-authoring (own-spec addition + delta slice substitution) → emission
reconcile (incl. DRIFT adoption note: feedler predates DRIFT/case-C hand-back) → delta seal with
the substituted package. Explicitly exercises round 5's fixed surfaces: delta seal package,
`gates/*-delta/` baselines, delta readings of the fenced checks. Cost: one tier-S run.

### S6 (obs 6) — Seed `verdicts/taxonomy-seed.md` now
Apply the `§2`-rule-1 transform verbatim to existing records: one line per closed blocker/major —
`lens · first sentence of the issue line, verbatim · source record` — from the panel record, the
r2–r6 raw reports, and the post-seal audit; dedup by source record. The transform is exempt from
the author ban (zero discretion), so this is registrar bookkeeping; operator commits. Keep it free
of exemplar-identifying facts so the eval-staging scrub stays trivial.

### S7 (obs 7) — One-line ledger fix + a citation habit
- `NOTES.md`: `d86eec3` → `630ac46`; log the fix as the first entry under the standing "Exempted
  edits" heading.
- Record the habit once: cite commits as message + date + SHA — amends orphan SHAs.

### S8 (obs 8) — Floor line + citation style, minimal diffs
- **Floor:** one line in `SKILL.md` §2 routing inputs: below roughly dial 2, the definition
  checkpoint includes the honest option "under the factory's floor — propose a lighter path,"
  recorded in the NOTES seed. **Gate:** one fresh verifier (§5 rule 1).
- **Citations:** no renumbering pass. New/edited factory text cites by section name going forward;
  existing numbered citations become safe once S4's factory mode exists.

---

## 3. Execution order (respecting the IOU's letter) and cost map

```
0. bookkeeping (zero-discretion, now):  S6 taxonomy seed · S7 SHA fix          — operator commits
1. S1a IOU payment:                     focused pass + panel on c3ea19a fixes  — operator orders
2. S1b build-proof:                     staged fresh builder + fresh verifier  — operator orders both
3. S5  tier-S delta drill on feedler                                        — one run's dispatches
4. S4  speclint.py build + test                                           — no gate (code)
5. standards batch: S2 + S3 + S8        ONE change set → ONE panel          — see batching note
```

**Batching note for the reviewing AI:** S2/S3/S8 are deliberately one change set so the
self-governing panel reviews one diff once. Check `change_rule.md §5` rule 2's letter ("Changes to
the self-governing surfaces … take a full fresh-context panel (≥3 distinct lenses) before
landing") and decide whether batching is within the letter (one landing = one panel) or an
end-run around it (one change = one panel). Also weigh whether a mixed diff dilutes lens focus.

## 4. What the reviewing AI should specifically scrutinize

1. **Obs 3 / S3** — is "ratchet" the right model, or did the machinery simply work as intended?
   Would S3 have changed any outcome in the six rounds, or only lowered their cost?
2. **Obs 2** — is the missing fold-in real? Check `verification_core.md §6` rules 1–4 and
   `templates/notes.md` for any existing home for accepted majors at spec-tree seals.
3. **S1 sequencing** — does the build-proof count as a "seal or eval" under the IOU's anchor, or
   is it the eval's final step (making "IOU first" still correct but for a different reason)?
4. **S5 scope** — is a synthetic drill a valid exercise of the delta path, or does an artificial
   request fail to stress what a real reshape stresses?
5. **Obs 1 framing** — the buildability lens + the L1 comparison already exist; is "unproven"
   fair, or is the claim better stated as "proven on paper, integration proof owed" (the tree's
   own wording)?
6. Anything in these notes that misreads the tree — every claim cites its file; check them.

## 5. Disclosure

This session also produced `specai.html` (an untracked visualization of the process at the
operator's request; it uses tier-role references instead of fixture names per the eval quarantine,
and its seal-SHA was corrected per obs 7). No other files in the tree were created or modified.

---

## Erratum — 2026-07-17 (after the author session's triage of this review)

1. **Obs 2 corrected.** Round 6's five majors were **fixed**, not accepted — what the operator
   accepted was landing those fixes without a seventh blind round, plus the standing accepted
   classes and one recorded edge (panel record, "Engagement close"; NOTES round-6 entry). My
   "accepted, not fixed" framing was wrong. What survives of obs 2: the engagement still closed
   without a returning clean blind PASS, and the recorded reason — blind reconfirmation kept
   seeding new letter defects — is itself the ratchet evidence from obs 3. S2 as adopted
   (fold future accepted majors + the standing classes into open topics with revisit anchors)
   addresses the durable-visibility point.
2. **S3 half-withdrawn.** The anchor-relaxation half is redundant: `change_rule.md §5.4`'s
   "operator-re-anchored with a recorded reason" has been the legal deferral path since D1
   landed it. The brake half (no new normative sentence without naming its finding) stands and
   was adopted.
3. **New finding (taxonomy seed).** The seed's structure, coverage, dedup, and †-flagging are
   right, but its pattern fields for raw-report-sourced lines are paraphrased/compressed rather
   than verbatim copies of the source findings' issue lines (`verification_core.md §2` rule 1:
   "verbatim … never paraphrased … nothing else"). Sampled 5 raw-report lines, all 5 deviate
   (ranging from truncation to meaning-altering generalization, e.g. the r6 lens-split line drops
   "tier-M" and "buildability"); panel-record-sourced lines verified verbatim on sample. One line
   also carries an annotation the format's "nothing else" doesn't license. The zero-discretion
   exemption is the transform's whole point — the seed should be regenerated with verbatim copies
   before its first consumer; cheap now, ungated bookkeeping.
