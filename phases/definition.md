# Phase 1 — Definition (ideation → vision + requirements inventory + dial)

**One brain, one pass.** Requirements, domain concepts, and user stories share a single information
context — the idea — so they are produced together, coherently, by one author. (Why the merge:
`NOTES.md`, founding decision 2.)

## Inputs (all this phase may read)
- The **ideation**: the operator's raw product description, verbatim, however informal — typos,
  mixed asks, and implied conventions included. Never ask the operator to clean it up.
- Any **attachments** the ideation cites (sample files, existing systems to imitate, data).
- The operator's **engineering defaults** if provided (preferred stack, deployment constraints —
  an invented example: "Rust, everything dockerized, no local installs"). If absent, they become
  checkpoint questions.
- `standards/dial.md`, `standards/style.md`, `standards/grammar.md` §4.1, `templates/vision.md`.

## Outputs
1. `<repo>/reference/ideation.md` — the ideation preserved verbatim; attachments preserved beside
   it (`<repo>/reference/<file>`) and cited from it.
2. `<repo>/specs/vision.md` — repo-grade, per `templates/vision.md`.
3. **The requirements inventory** — a factory working artifact (`<run-dir>/inventory.md`), consumed
   by phases 2–4 and the phase-6 coverage lens. Enumerated, one line each, source-tagged:
   - **R-n requirements** (functional + non-functional), each traced to an ideation line or a
     checkpoint answer;
   - **U-n user types** (personas and anti-personas) and **S-n user stories** (atomic: as/wants/why,
     with edge cases and admin/operator flows — the areas ideations always under-specify);
   - **D-n domain concepts** (candidate glossary terms with one-line meanings);
   - **C-n constraints** (stack, deployment, compliance, non-goals candidates);
   - **X-n explicit exclusions** (what the operator said or implied NOT to build);
   - **REG-n the regulatory register** (when and only when regulatory/money scores 2 —
     `dial.md` §1 rule 2): each regulatory/compliance obligation, its source (law, scheme rule,
     checkpoint answer), one line each — phase 2 maps every REG-line to an enforcing component or
     principle in architecture's Money & compliance section (`grammar.md` §4.2).
4. **The dial score** (`standards/dial.md`): five dimensions, one-line justifications, tier. The
   score + tier bind in `vision.md` §Dial; the justifications go to the NOTES seed.
5. **The NOTES seed** — `<run-dir>/notes-seed.md`: checkpoint answers, dial justifications, gate
   approvals, decisions made where the ideation was ambiguous (phase 5 instantiates it into the
   repo's `NOTES.md`).

## Procedure
1. Read the ideation twice: once for what it says, once for what it assumes — a product category
   implies conventional features its ideation never states (an invented example: "a to-do app"
   implies due dates, reordering, completion states); enumerate the implied set explicitly as
   R-lines marked *implied*, so the operator sees them.
2. Draft the inventory. Hunt omissions harder than contradictions: full user journey (first run →
   daily use → failure states → reset/retirement), operator/admin needs, the boring parts.
3. Score the dial.
4. **Checkpoint (the one operator interruption of this phase):** one batched set of questions —
   only what the ideation doesn't answer and a default would be presumptuous for. Always ≤10, each
   with a proposed default so the operator can answer "defaults fine". Include engineering defaults
   if not provided. **A contradiction inside the ideation is always a checkpoint question** — never
   silently resolved. At tier M and above add a risk-focused round; whenever regulatory/money scores 2
   (`dial.md` §1 rule 2 — the dimension, never the tier), add the money/compliance round
   (`dial.md` §2). Present the dial score for confirmation in the same message.
5. Fold answers into the inventory (source-tagged `checkpoint`); record them in the NOTES seed
   (`<run-dir>/notes-seed.md`), **each answer marked chosen or default-accepted** — the coverage
   and judgment lenses weigh default-accepted answers as factory assumptions — along with the
   confirmed dial justifications.
6. Write `vision.md`: the problem and vision in the operator's own terms sharpened, pillars that
   can carry later judgment calls, honest audience/anti-audience, measurable success criteria,
   **non-goals promoted from X-lines** (numbered, each marked **identity** — the change-request
   firewall — or **revisitable** — a scope cut a rebuild must not restore; `grammar.md` §4.1), and
   the binding **Dial line** (score + tier + any override).
7. **Self-review** (quality cell): re-enter as a skeptic — does every inventory line trace to
   ideation or checkpoint? Would a stranger reading only `vision.md` know what to refuse to build?
   Is anything in vision.md HOW? Fix. Per the spot-verify schedule (`dial.md` §2), also dispatch
   the fresh spot-verify (lenses: ideation coverage + altitude/style, scoped to vision/inventory;
   the package is this phase's input list plus `<run-dir>/notes-seed.md` — a verifier-only
   addition, the default-accepted marks live there) before the operator gate.

## Gate
Operator approves `vision.md` + the inventory + the dial (whether this gate fires at the run's
tier is the tempo rule's to say — `dial.md` §3, cited, not restated). Approval is recorded in the NOTES seed, and **every approved
artifact** — `vision.md`, the inventory, the seed — is copied to `<run-dir>/gates/definition/`,
the baseline the seal diffs against. Do not proceed without it.
