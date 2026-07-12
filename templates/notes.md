# TEMPLATE — NOTES.md (grammar §4.9 · the decision ledger)

> Authoring notes in blockquotes; delete them. Seeded by phase 5; appended by every later working
> session in the emitted repo. Reference instance: the trading platform's NOTES.md.

# NOTES — <product> decision ledger (<founding date>)

The operator's record of what was decided, where it landed, and what's still open. This file is a
**record, not a spec** — nothing here is normative; the specs win. A decision that must survive
regeneration lives in a spec (the change rule); this file keeps the history and the why.

## Founding (specai run, <date>)

- **Ideation:** preserved at `reference/ideation.md`.
- **Dial:** <score> → tier <S/M/L> — <one line per dimension>. <Operator override + reason, if any.>
- **Checkpoint answers:** <each question → the operator's answer, one line each.>
- **Founding decisions:** <each with one-line rationale — the calls specai made where the ideation
  was ambiguous, so the operator can overrule with context.>
- **Deliberate cuts (binding context for future rebuilds):** <each X-line exclusion with reason —
  recorded so a future rebuild does NOT "restore" it as an omitted-WHAT defect.>
- **Open topics:** <unresolved product questions, also flagged in the owning specs' Open questions.>
- **Seal:** verification verdict <PASS, date, tier> · operator countersign <date/commit>.

## <Session date> — <topic>
> One entry per working session that decides anything: what was decided, where it landed
> (spec §refs), what remains open. Current-state style — a superseded decision is corrected in
> place in the spec; here you may note the supersession in one line.
