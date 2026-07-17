# Phase 5 — Process Emission (make the repo self-operable)

The step with no 2025 equivalent: instantiate the operating manual and process standards so the
repo can build, verify, and change itself **without specai**. After this phase, the factory's only
remaining job is the seal.

## Inputs
- The full emitted `specs/` tree so far, the dial, the NOTES seed (checkpoint answers, decisions).
- `standards/grammar.md`, `standards/change_rule.md`, `standards/verification_core.md`,
  `templates/start.md`, `templates/notes.md`.
- The exemplars for calibration (`reference/exemplars.md`): feedler's `start.md` at tier S,
  the trading platform's at tier L.

## Outputs
1. `<repo>/specs/start.md` — instantiated from `templates/start.md`:
   - §1 **boot table generated from the architecture component table**: one row per target
     (whole product · each component · each standard · design · spec work), each with its ordered
     reading list (contracts before consumers; design spec for UI surfaces). Every spec file must
     appear in some row (grammar §6 checks this mechanically).
   - §2 command grammar per the dial (S: develop / change / edit specs / new / verify [+
     develop-loop]; L adds design/studio and lifecycle commands the product needs).
   - §4 QA layers **tailored to this product's acceptance gate** (from the engineering standard —
     e.g. compose-up → drive primary flows → data/contract truth → time/restart) and the
     verification discipline per tier.
   - §5 the **cascade graph made concrete** (this repo's actual files, from
     `change_rule.md` §3's generic graph) + the binding style list.
   - §6 DoD, always ending with the process-friction improvement loop.
2. Per the dial (`dial.md` §2): `<repo>/specs/standards/verification_standard.md` (M/L —
   instantiated from `verification_core.md` with the product's runtime lenses; L adds
   QA-officer pattern, taxonomy seed, verdict-record rules) · `develop_loop.md` (offered S+;
   feedler's is the reference text) · `studio.md` (L, experience-led).
3. `<repo>/specs/README.md` — the map (grammar §4.8), with literal invocation examples.
4. `<repo>/workspace/README.md` — mirror rule, bring-up command, port/layout conventions.
5. `<repo>/NOTES.md` — from `templates/notes.md`: dial score + reasoning, checkpoint answers,
   founding decisions with rationale, **deliberate cuts** (from X-lines — so a future rebuild
   doesn't "restore" them as omitted-WHAT), open topics.
6. `reference/ideation.md` confirmed in place (phase 1 put it there).

No `DRIFT.md` is emitted — the divergence ledger (`grammar.md` §4.10) appears only once an
implementation exists and diverges; the instantiated `start.md` (§1 boot, §3 case B, §4
verification, §5 spec-editing, §6 DoD) carries its discipline.

## Procedure
1. Generate the boot table from the component map; walk every command through it as a dry run —
   each command must resolve to a readable, ordered, *sufficient* list (the future builder's first
   experience of the repo is this table; it must not lie).
2. Instantiate the tier's process standards; strip everything the tier doesn't need (a tier-S repo
   gets no QA-officer machinery — the discipline lives inline in start.md §4, feedler-style).
3. Wire citations: start.md ↔ standards ↔ architecture cross-references all resolve.
4. Write README and NOTES. NOTES is seeded honestly — including what specai found ambiguous and
   decided, so the operator can overrule with full context.
5. **Self-review as the rebuilding AI:** cold-read the repo top-to-bottom as if handed only this
   directory. Can you route every §2 command? Do you know when you'd be done? What would you have
   to guess? Fix what you'd guess.
