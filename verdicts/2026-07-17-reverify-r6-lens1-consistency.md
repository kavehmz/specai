# Blind re-verification round 6 — lens 1: consistency/contract (verbatim report)

*Preserved verbatim per `verification_core.md` §6 rule 4. Dispatcher: the operator by standing
order; lead as mechanical proxy. Package: the full tree minus `verdicts/` and `.git`.*

---

**DISCLOSURE — ambient context beyond this prompt and the listed files:** harness-injected environment metadata (working directory, git status snapshot listing recent commit titles, platform, date, user email) and a tool/skills listing. I did not open `verdicts/`, `.git`, or anything outside the listed files.

# VERDICT: FAIL — 0 blockers, 2 majors, 10 minors

## MAJOR

**M1 — verification_core.md §4 (M row) vs phases/verification.md: the tier-M default lens split omits buildability, a lens phase 6 calls decisive.** The M-row default covers 7 of §5's lenses; buildability is assigned to neither verifier. A tier-M seal executed exactly as written never runs the rebuild-test lens; only the tier with a pinned enumeration has the hole. Fix: add buildability to one side of the M default split.

**M2 — phases/delta.md step 6's lens enumeration conflicts with the phase-6 lens apparatus it imports "in every duty".** Two readings execute two different seals: exhaustive (contradicts "in every duty"; a money-path delta never runs adversarial-user or outcomes) or scoping (contradicted by the narrower enumeration). Fix: one sentence declaring the §4/§5 apparatus applies in full with these delta scopings.

## MINOR

m1 verification.md Inputs vs its own package pin different values (notes.md vs templates/; package items unnamed in Inputs). m2 dial §2 L "stable IDs" undefined vs definition.md's unconditional ID'd inventory. m3 exemplars label "tier-neutral" contradicts its instances ("the tier-S exemplar" names a tier) — rename the class. m4 grammar §6 check 1's conditional list omits specs/design/. m5 delta step 4 "exactly two items" arithmetic (one is a substitution). m6 "gate" carries two senses, absent from the terms block. m7 SKILL §4 applies §5.4's IOU outside its stated scope (degraded emitted-repo seal) — admit the case in §5.4. m8 the delta package can name a nonexistent consumer-ledger.md when no contracts phase ran — add "where produced". m9 the pre-seal no-bump allowance lives only factory-side; the emitted contract header is unconditional. m10 SKILL §1 map's verdicts/ line omits taxonomy-seed.md.

## CLEAN

Eval exclusions/carve-outs mutually consistent end-to-end across all seven homes. IOU letter + three collectors agree everywhere. Canonical terms single-defined ("gate" excepted). Ownership seams: one owner each, deferrers cite. Citation resolution: everything traced resolves and (M2/m7 aside) says what the citer claims. Pinned values agree at every occurrence. NOTES round-6 claims all hold against the tree.
