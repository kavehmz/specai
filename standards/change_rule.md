# change_rule.md — Change, Cascade, and the Router

**Status:** Binding — for specai's own evolution, for the factory while a repo is being authored,
and (via `templates/start.md`) instantiated into every emitted repo.

## 1. The change rule

> **"If a better AI rebuilt this from the specs alone, would this change be lost?"**
> Yes → the spec must change **first** (with the operator's confirmation). No → code-only fix.

This one test replaces ai-it's bug-vs-modification taxonomy: a defect the spec already implies the
correct behavior for is a code fix; anything that changes WHAT — a contract, a data model, a
user-relied-on behavior, a config key — is a spec change and lands in the spec before any
implementation moves. It also replaces the directive/preferences system: **a decision that must
survive regeneration lives in a spec; NOTES.md keeps the history and rationale; nothing else is a
truth store.**

## 2. The router — one front door

Every request enters through the entrypoint (`SKILL.md` for specai; the emitted `start.md` for a
product) and is **classified to the owning artifact** before anything is edited. No exceptions for
urgency: a security issue is classified by *where the fix lives*, not by how loud it is.

Classification order (first match wins):
1. Violates the vision's non-goals or an architecture principle → **stop and say so**; propose the
   closest conformant alternative. (The non-goals list is a firewall, not a suggestion.)
2. Changes the WHY (audience, pillars, non-goals) → `vision.md` — the rarest, loudest edit.
3. Changes the shape (glossary, data model, components, principles, lifecycle) → `architecture.md`.
4. Changes a cross-component contract (wire shape, config key, schema) → the owning standard, with
   **version bump + migration note in the document itself**.
5. Changes one component's WHAT → that component spec (cascades nowhere by default).
6. Changes appearance/interaction language → the design spec.
7. Changes process (how building/verifying works) → `start.md` or the process standard.
8. None of the above (the spec already implies the right behavior) → code-only fix.

## 3. The cascade graph

The generic graph every emitted repo instantiates concretely in its `start.md` §5:

- `vision.md` → judged against by everything; an edit re-opens `architecture.md`'s principles and
  every non-goal-adjacent spec.
- `architecture.md` (glossary, data model, principles) and `standards/*` → cascade to **every**
  document that cites them; re-read the citing set in the same session.
- A contract standard → cascades to every component spec using the changed surface **and** to both
  sides of the implementation.
- A single component spec → cascades nowhere, unless it touches a shared term (fix the glossary)
  or a contract surface (fix the standard — which then cascades).
- The design spec → cascades to visual surfaces of feature specs, never to contracts or data.
- `start.md` / process standards → cascade to working practice only; no product spec changes.

**Discipline:** propose before editing (affected files + sections + the cascade, then the
operator's go-ahead); after editing, re-read every cascade target in the same session; a wire/schema
edit is announced loudly with its migration story.

## 4. Verification gating of changes

Per the emitted repo's tier (`dial.md`, `verification_core.md` §4): standards/architecture and
money-path spec changes verify at the top tier before landing; other substantive spec edits get a
focused pass; typo/clarity edits are exempt. **Committing is the operator's act and the
countersign** — specai and emitted-repo builders never commit unasked (an automated exception must
be an explicit, gated standard like a develop-loop, never a default).

## 5. specai's own change process

The skill obeys its own rule. Changes to `standards/*` here are top-tier (fresh-context
verification before they land); phase-file changes are focused; template changes cascade to a
re-read of `grammar.md` for consistency. After any change: update `SKILL.md`'s map if files were
added/moved/removed, and record the decision in `NOTES.md`. The map staying true is part of the
change, not an afterthought.
