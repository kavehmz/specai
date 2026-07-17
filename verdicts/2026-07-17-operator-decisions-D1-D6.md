# Operator decision packet — D1–D6 (from the 2026-07-17 standards panel)

Six design decisions the panel surfaced that belong to the operator, in plain language.
Each is: *the problem found → what is proposed → what it means for you.* The full findings
behind them are in `verdicts/2026-07-17-standards-panel.md`. Decide each (yes / no / adjust),
then run the fix loop.

---

**D1 — How much review does changing specai's own rulebook need?**
Today the rule says: any edit to `standards/` needs a 3+ verifier panel *before* it lands. That's
so heavy that you've never actually done it — three changes shipped with "review pending" notes
instead. A rule everyone skips is a bad rule.
**Proposal:** small edits to the rulebook need just **one** fresh reviewer before landing. Only
edits to the verification rules themselves need the full panel. And the 2026-07-17 panel counts as
paying off the three old IOUs.
*For you: less ceremony, and the rule finally matches what's doable.*

**D2 — Money projects can slip past the money checks.**
The skill scores each product 0–10 and sizes everything by the total. Problem: a *simple* app that
moves real money scores maybe 5/10 — mid-tier — and mid-tier gets **none** of the extra
money/compliance checks. Those only switch on at 8+. Simple doesn't mean low-stakes.
**Proposal:** the money/compliance checks switch on whenever the *money score itself* is high —
regardless of the total. And if a run discovers hidden money scope halfway through ("oh, these
gift credits are redeemable for cash"), it must go back and re-score instead of carrying on.
*For you: a small real-money product still gets the real-money treatment.*

**D3 — Who is allowed to order a review?**
Current rule: "the author never dispatches their own verifiers." Sounds right, but in practice the
AI running the whole show *wrote* most of the documents — so read strictly, no run can ever review
itself legitimately, and read loosely the rule means nothing. It's the ambiguity that created your
three IOUs.
**Proposal:** say plainly what actually makes a review independent — the reviewer starts *fresh*,
sees *only* the files and a fixed brief, never the author's chat. The run lead may press the
"launch reviewers" button; **you** personally order only the final seal review and reviews of
specai itself.
*For you: the rule finally describes what we actually do (and what the panel did).*

**D4 — Two important things live in the wrong file.**
NOTES.md is declared "just history, never binding." But two binding things live *only* there: the
product's tier score (which controls how much process it gets forever), and the "deliberate cuts"
("we chose no search in v1" — recorded so a rebuild doesn't re-add it). If a rebuild reads only
the specs, as the doctrine demands, those get lost.
**Proposal:** the tier gets written into a spec; deliberate cuts move into the vision's non-goals
list (marked "revisitable" when they're just for-now); NOTES keeps only the *why*.
*For you: nothing binding hides in the history file.*

**D5 — The self-test can cheat.**
specai's quality test is "rebuild feedler from its original idea and compare." But during that
test, the run is *allowed to read the real feedler* (a template literally says "read feedler's
export spec first") — the answer key is on the desk. And the one run so far declared PASS while
skipping the test's own final step, and graded itself.
**Proposal:** during an eval, the target product's repo is off-limits; the comparison is judged by
reviewers *you* dispatch, not the run itself; no PASS until the final step (actually building from
the emitted specs) runs. The old "PASS" gets relabeled "comparison passed; build-proof pending."
*For you: when specai claims it reproduced feedler, that claim is real.*

**D6 — One sentence understates its own exception.**
The doctrine is "specs say WHAT, never HOW" with one licensed exception, described as: the
engineering standard may name the stack ("Go backend, React frontend"). But that document
actually — and correctly — also pins deploy commands, database rules, build steps. So the
exception as written is narrower than the reality, and a strict reviewer would have to fail every
conforming project.
**Proposal:** reword the exception to match: *that one document* is licensed to bind the how-level
choices; everything else stays WHAT-only.
*For you: one sentence, honesty fix, no behavior change.*

---

None of these changes what specai fundamentally is — D2, D4, D5 close real holes; D1, D3, D6 make
rules match reality. The session lead's recommendation was yes to all six.
