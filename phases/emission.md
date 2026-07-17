# Phase 5 — Process Emission (make the repo self-operable)

Instantiate the operating manual and process standards so the repo can build, verify, and change
itself **without specai**. After this phase, the factory's only remaining job is the seal.

## Inputs
- The full emitted `specs/` tree so far, the dial, the NOTES seed (`<run-dir>/notes-seed.md`:
  checkpoint answers, decisions, dial justifications).
- `standards/grammar.md`, `standards/change_rule.md`, `standards/verification_core.md`,
  `standards/style.md`, `templates/start.md`, `templates/notes.md`,
  `templates/engineering_standard.md` (output 7 completes its §11).
- Optional calibration, where available: the tier-matched exemplar's `start.md`
  (`reference/exemplars.md` — the templates are self-sufficient; during an eval that file is
  off-limits **entirely**, its §3, and only an operator-staged pointer to the non-target
  exemplar may be read).

## Outputs
1. `<repo>/specs/start.md` — instantiated from `templates/start.md`:
   - §1 **boot table generated from the architecture component table**: one row per target
     (whole product · each component · each standard · design · spec work), each with its ordered
     reading list (contracts before consumers; design spec for UI surfaces). Reachability per
     grammar §6 check 1 — its two exemptions apply — checked mechanically at phase 6.
   - §2 command grammar per `templates/start.md` §2 — the template owns the command list and its
     dial conditions; this file does not restate them.
   - §4 QA layers **tailored to this product's acceptance gate** (from the engineering standard —
     e.g. compose-up → drive primary flows → data/contract truth → time/restart) and the
     verification discipline per tier.
   - §5 the **cascade graph made concrete** (this repo's actual files, from
     `change_rule.md` §3's generic graph) + the binding style list.
   - §6 DoD, always ending with the process-friction improvement loop.
2. Per the dial (`dial.md` §2), the process standards:
   - `verification_standard.md` (M/L) — instantiated from `verification_core.md` with the
     product's runtime lenses. It includes a scheduled full-tree `verify` cadence, so untouched
     components' drift surfaces. At L it adds: the QA-officer pattern (a standing
     independent-verification role the repo's sessions dispatch, never the builder), a taxonomy
     seed (the defect-pattern list verifiers load, grown from verdict records), and
     verdict-record rules per `verification_core.md` §6.
   - `develop_loop.md` — the Builder/Gate auto-convergence standard (shape: `grammar.md` §4.11;
     pattern: `verification_core.md` §8). At S+ the offer is made at the seal presentation
     (`phases/verification.md`); on acceptance the standard is instantiated **through the sealed
     repo's own change process with its verification gating** — never landed unverified by the
     factory.
   - `studio.md` (L and experience-led — `grammar.md` §4.11 owns the condition and shape) and,
     at L, the ops/infra standards and — when the product is AI-operated — the agent standards
     (both §4.11).
3. `<repo>/specs/README.md` — the map (grammar §4.8), with literal invocation examples.
4. `<repo>/workspace/README.md` — mirror rule, bring-up command, port/layout conventions.
5. `<repo>/NOTES.md` — from `templates/notes.md` and the NOTES seed: dial justifications (the
   score + tier bind in `vision.md` §Dial), checkpoint answers (marked chosen / default-accepted),
   founding decisions with rationale, the rationale behind the vision's revisitable cuts (the cuts
   themselves bind in `vision.md` §Non-goals), open topics.
6. `reference/ideation.md` confirmed in place (phase 1 put it there).
7. **Complete the engineering standard's testing floor** (template §11, stubbed by phase 3 —
   in `standards/engineering_standard.md` or, at tier S, in the inlined architecture section):
   name the component specs carrying the binding worked examples and what a smoke run must cover.

No `DRIFT.md` is emitted — the divergence ledger (`grammar.md` §4.10) appears only once an
implementation exists and diverges; the instantiated `start.md` (§1 boot, §3 case B, §4
verification, §5 spec-editing, §6 DoD) carries its discipline.

## Procedure
1. Generate the boot table from the component map; walk every command through it as a dry run —
   each command must resolve to a readable, ordered, *sufficient* list (the future builder's first
   experience of the repo is this table; it must not lie).
2. Instantiate the tier's process standards; strip everything the tier doesn't need (a tier-S repo
   gets no QA-officer machinery — the discipline lives inline in start.md §4, per the tier-S
   reference instance).
3. Wire citations: start.md ↔ standards ↔ architecture cross-references all resolve.
4. Write README and NOTES. NOTES is seeded honestly — including what specai found ambiguous and
   decided, so the operator can overrule with full context.
5. **Self-review as the rebuilding AI:** cold-read the repo top-to-bottom as if handed only this
   directory. Can you route every §2 command? Do you know when you'd be done? What would you have
   to guess? Fix what you'd guess.
