# Post-seal audit — lens 2: executability/buildability (verbatim report)

*Preserved verbatim per `verification_core.md` §6 rule 4. Post-seal audit round over the sealed
tree (630ac46). Package: the tree minus `verdicts/`/.git.*

---

**DISCLOSURE:** Ambient context injected beyond this prompt and the listed files: a system-reminder carrying the user's email and today's date; environment metadata (cwd, platform, git status snapshot with recent commit subjects); the harness's tool/skill listings. None used as review input.

## VERDICT: FAIL — 1 major, 4 minors

**1. MAJOR — The architecture-delta spot-verify mandates the change-request coverage lens but its zero-discretion package cannot contain the lens's primary source.** delta step 2's substitutions are exhaustive and none maps in `<run-dir>/change-request.md`; the delta-inventory lines are only "source-tagged to the request", not the request text; the step-6 seal substitution shows the mapping exists and was omitted here. Fix: the change request joins the spot-verify package — the same declared-verifier-addition device phase 2 already uses.

**2. MINOR** — definition step 7 and architecture step 10 spot packages omit `notes-seed.md`, so the lens's default-accepted weighing leg is unexecutable mid-run (the marks live only in the seed). Declare the seed a verifier-only addition in both. **3. MINOR** — the L row names no partition and no one who may choose it ("zero discretion"); give L a default or assign the partition to the operator's seal order. **4. MINOR** — fenced check 2's delta reading names no authoritative source for which phases re-ran. **5. MINOR** — the comparison verdict record has an unassigned compiler (panel ≥2, run barred, §6.4 compiler duties seal-scoped); assign the operator.

**Clean walks (verified end-to-end):** S-run producer/consumer chain; L-run with reg/money=2 (the dimension trigger consistent everywhere, reg-2-at-S coherent); all named working files have producers; spot-verify schedule coherence (0/1/3 for full runs); phase-6 seal dispatch legality (conforming-brief fully sourced, checks 1–3 executable, NOTES sweep correctly non-eval-scoped); **lens totality holds** (M's split covers exactly the 8 applicable lenses; S single-carrier and delta swap preserve it); judgment-gate shapes; delta seal substitution package (all seven substitutions resolve; sweeps reach delta re-seals); **eval route end-to-end** (staging → fenced prompt → severable exclusions → internal seal with disclosed NOTES-exclusion → operator comparison ≥2 → operator-launched build proof with separately dispatched verifier → operator/registrar close-out); crash-resume (in-flight dispatches safely re-dispatchable under "gate has run only when verdict returned"); emitted-repo operability from templates alone (start.md carries the full §4.3 surface incl. the commit rule; §4.11 shapes exemplar-free); no other forced guessing (defaults exist for target dir, sequential threshold, pre-seal no-bump, degraded floor, mid-run re-score).

PASS requires zero blockers and zero majors; finding 1 is a major. Fixes for all five findings are one-to-two-line edits.
