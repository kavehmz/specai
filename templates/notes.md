# TEMPLATE — NOTES.md (grammar §4.9 · the decision ledger)

> Authoring notes in blockquotes; delete them. Seeded by phase 5; appended by every later working
> session in the emitted repo. Reference instance: the tier-L exemplar's ledger
> (`reference/exemplars.md` §2).

# NOTES — <product> decision ledger (<founding date>)

The operator's record of what was decided, where it landed, and what's still open. This file is a
**record, not a spec** — nothing here is normative; the specs win. A decision that must survive
regeneration lives in a spec (the change rule); this file keeps the history and the why. Where the
*implementation* currently departs from the specs is not history — that lives in `DRIFT.md`
(`start.md` §3), deleted item-by-item as fixed.

## Founding (specai run, <date>)

- **Ideation:** preserved at `reference/ideation.md`.
- **Dial justifications:** <one line per dimension — the score + tier themselves bind in
  `vision.md` §Dial, not here.> <Operator override reasoning, if any.>
- **Checkpoint answers:** <each question → the operator's answer, one line each, marked **chosen**
  or **default-accepted** — verifiers weigh default-accepted answers as factory assumptions.>
- **Founding decisions:** <each with one-line rationale — the calls specai made where the ideation
  was ambiguous, so the operator can overrule with context.>
- **Cut rationale:** <the why behind each revisitable non-goal in `vision.md` §Non-goals — the cuts
  themselves bind there, not here.>
- **Open topics:** <unresolved product questions, also flagged in the owning specs' Open questions.>
- **Seal:** verification verdict <PASS, date, tier> · verification mode <independent panel /
  single fresh verifier / degraded self-review> · verdict record <committed path — or, if the
  operator discarded it, its dispatcher/package/injection facts restated here verbatim> ·
  operator countersign <date/commit>.

## <Session date> — <topic>
> One entry per working session that decides anything: what was decided, where it landed
> (spec §refs), what remains open. Current-state style — a superseded decision is corrected in
> place in the spec; here you may note the supersession in one line.
