# Phase 1 — Definition (ideation → vision + requirements inventory + dial)

**One brain, one pass.** Requirements, domain concepts, and user stories share a single information
context — the idea — so they are produced together, coherently, by one author. (The 2025 three-phase
split was a context-window artifact; the merge is deliberate.)

## Inputs (all this phase may read)
- The **ideation**: the operator's raw product description, verbatim, however informal. (Reference
  class: feedler's 27-line brain-dump with typos → a 4.1K-line suite. Never ask the operator to
  clean it up.)
- Any **attachments** the ideation cites (sample files, existing systems to imitate, data).
- The operator's **engineering defaults** if provided (preferred stack, deployment constraints —
  e.g. "Go, everything dockerized, no local installs"). If absent, they become checkpoint questions.
- `standards/dial.md`, `standards/style.md`, `templates/vision.md`.

## Outputs
1. `<repo>/reference/ideation.md` — the ideation preserved verbatim (plus attachments referenced).
2. `<repo>/specs/vision.md` — repo-grade, per `templates/vision.md`.
3. **The requirements inventory** — a factory working artifact (`<run-dir>/inventory.md`), consumed
   by phases 2–4 and the phase-6 coverage lens. Enumerated, one line each, source-tagged:
   - **R-n requirements** (functional + non-functional), each traced to an ideation line or a
     checkpoint answer;
   - **U-n user types** (personas and anti-personas) and **S-n user stories** (atomic: as/wants/why,
     with edge cases and admin/operator flows — the areas ideations always under-specify);
   - **D-n domain concepts** (candidate glossary terms with one-line meanings);
   - **C-n constraints** (stack, deployment, compliance, non-goals candidates);
   - **X-n explicit exclusions** (what the operator said or implied NOT to build).
4. **The dial score** (`standards/dial.md`): five dimensions, one-line justifications, tier.

## Procedure
1. Read the ideation twice: once for what it says, once for what it assumes (the unstated
   conventional features — "a feed reader" implies unread counts, folders, keyboard nav; enumerate
   the implied set explicitly as R-lines marked *implied*, so the operator sees them).
2. Draft the inventory. Hunt omissions harder than contradictions: full user journey (first run →
   daily use → failure states → reset/retirement), operator/admin needs, the boring parts.
3. Score the dial.
4. **Checkpoint (the one operator interruption of this phase):** one batched set of questions —
   only what the ideation doesn't answer and a default would be presumptuous for. Always ≤10, each
   with a proposed default so the operator can answer "defaults fine". Include engineering defaults
   if not provided. Present the dial score for confirmation in the same message.
5. Fold answers into the inventory (source-tagged `checkpoint`); record them and the confirmed dial
   in what will become the repo's `NOTES.md` seed.
6. Write `vision.md`: the problem and vision in the operator's own terms sharpened, pillars that
   can carry later judgment calls, honest audience/anti-audience, measurable success criteria, and
   **non-goals promoted from X-lines** (numbered — this is the future change-request firewall).
7. **Self-review** (quality cell): re-enter as a skeptic — does every inventory line trace to
   ideation or checkpoint? Would a stranger reading only `vision.md` know what to refuse to build?
   Is anything in vision.md HOW? Fix. At tier L, also dispatch the fresh spot-verify (`dial.md` §2:
   lenses = ideation coverage + altitude on vision/inventory) before the operator gate.

## Gate
Operator approves `vision.md` + the inventory + the dial (the tempo rule, `dial.md` §3 — this
checkpoint happens at every tier). Approval is recorded in the NOTES seed. Do not proceed without it.
