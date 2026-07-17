# change_rule.md — Change, Cascade, and the Router

**Status:** Binding — for specai's own evolution, for the factory while a repo is being authored,
and (via `templates/start.md`) instantiated into every emitted repo.

## 1. The change rule

> **"If a better AI rebuilt this from the specs alone, would this change be lost?"**
> Yes → the spec must change **first** (with the operator's confirmation). No → code-only fix.

A defect the spec already implies the correct behavior for is a code fix; anything that changes
WHAT — a contract, a data model, a user-relied-on behavior, a config key — is a spec change and
lands in the spec before any implementation moves. **A decision that must survive regeneration
lives in a spec; `NOTES.md` keeps history and rationale; `DRIFT.md` keeps current divergence
(`grammar.md` §4.10); nothing else stores truth.**

A code-only fix that cannot land in the same session is parked in the repo's `DRIFT.md`
(`grammar.md` §4.10) — non-binding, dated, deleted when fixed — never written into a spec and never
left only in conversation.

## 2. The router — one front door

Every request enters through the entrypoint (`SKILL.md` for specai; the emitted `start.md` for a
product) and is **classified to the owning artifact** before anything is edited. No exceptions for
urgency: a security issue is classified by *where the fix lives*, not by how loud it is.

Classification order (first match wins):
1. Violates an **identity** non-goal or an architecture principle → **stop and say so**; propose
   the closest conformant alternative. (The identity non-goals are a firewall, not a suggestion.
   A request against a non-goal marked **revisitable** — a recorded scope cut, `grammar.md` §4.1 —
   is not a stop: it routes as a vision edit, rule 2.)
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
edit is announced loudly with its migration story. **The cascade set is derived, never asserted:**
it is walked **bidirectionally** from the citation graph (the emitted `start.md` §5 concrete
graph) — the documents the artifact cites, the documents citing it, and the owners of every
canonical term the diff touches — and the verdict of any gated change names the derived set. An
author's "cascades nowhere" claim is not an input, and an omitted citation does not shrink the
set (the term-owner leg catches contradictions the author never linked).

## 4. Verification gating of changes

Per the emitted repo's tier (`dial.md`, `verification_core.md` §4): standards/architecture and
money-path spec changes verify at the **top tier** — the phase-6 seal depth of the repo's tier in
`verification_core.md` §4 (money-path changes at this depth whenever regulatory/money scores 2,
regardless of tier — `dial.md` §1) — before landing; other substantive spec edits get a **focused
pass** — one fresh verifier receiving the **whole spec tree** (spec trees are small), whose first
task is to **re-derive the cascade set independently** from the citation graph — a mismatch with
the dispatcher's named set is itself a finding — then verify the changed artifact plus that set,
applicable lenses only; typo/clarity edits are exempt (a "substantive" edit is any edit that
changes what a conforming reader would do; when in doubt, it is substantive). A **money-path**
change is any edit to a clause cited by architecture's Money & compliance section. **Committing is the operator's act and the
countersign** — specai never commits, ever; emitted-repo builders never commit except under an
explicit, gated standard (the develop-loop Gate class), never by default.

## 5. specai's own change process

The skill obeys its own rule. Verification weight keys to the **target document**, never to the
edit's claimed size:

1. Any substantive change to `standards/*`, `SKILL.md` (any section), `templates/*` (they are the
   grammar's tiebreaker — standards-class carriers), or `reference/exemplars.md` takes **one fresh
   verifier before it lands** (the §4 focused pass, run against this tree; for specai
   self-changes the verifier's package includes the full `standards/` set + `SKILL.md` as
   context — the tree is small and cross-document contradictions are the common defect).
   Template changes additionally cascade to a re-read of `grammar.md` for consistency. **Where
   rule 2 also matches, the stricter gate binds.**
2. Changes to the **self-governing surfaces** — `verification_core.md`, this document's §4–§5,
   `SKILL.md` §4's contamination/degraded-floor clauses, `reference/exemplars.md` §3 (the eval
   hygiene rules — the highest-leverage self-serving edit surface), or the **seal-operating
   text** (`phases/verification.md`'s verifier package + fenced checks, `phases/delta.md`
   step 6 — functionally equivalent to the rules they execute) — take a full fresh-context
   **panel** (≥3 distinct lenses) before landing. **No typo/clarity exemption on these
   surfaces**: any diff takes at least the focused pass.
3. Phase-file changes are focused; any other binding text in this tree (`README.md` included)
   gets the §4 focused pass; typo/clarity edits are exempt — and every exempted edit is logged
   one-line (date, file, one-phrase description) under the standing **"Exempted edits"** heading
   in `NOTES.md`, the bundle enumerated at the next seal/eval preamble alongside the IOU sweep,
   so the "clarity only" claim gets one eventual reader.
4. **Deferral is a named state, never a silent skip.** A gate **has run only when its verdict is
   returned** — dispatching a verifier is not paying the gate. If the verdict cannot return
   before landing, the operator records an IOU in `NOTES.md` naming the change, the owed gate,
   and the payoff anchor ("before the next seal/eval" at latest; a degraded-mode seal's owed
   independent verification — `SKILL.md` §4 — is an admitted IOU of this rule, though no specai
   change drove it). **An IOU is paid only by the
   owed gate closing** over the tree that contains the change — a PASS verdict, or a FAIL whose
   blockers/majors are fixed-and-reconfirmed or operator-accepted with recorded reason
   (`verification_core.md` §6). A returned FAIL converts the IOU into an open fix loop; it never
   clears it. **IOUs have a collector:** every phase-6 seal presentation, every **delta re-seal**,
   and every eval preamble enumerates specai's open IOUs (`phases/verification.md`,
   `phases/delta.md` step 6, `reference/exemplars.md` §3); an IOU past its anchor blocks the
   seal/eval until paid or operator-re-anchored with a recorded reason.
5. Dispatch per `verification_core.md` §2 rule 4: reviews of specai itself are the operator's to
   order; the run lead may relay briefs as mechanical proxy.

After any change: update `SKILL.md`'s map **and** `README.md`'s layout if files were added, moved,
or removed, and record the decision in `NOTES.md`. The maps staying true is part of the change, not
an afterthought.
