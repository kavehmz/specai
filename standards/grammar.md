# grammar.md — The Spec-Tree Grammar (what specai emits)

**Status:** Binding for every emitted repository. This is the definition of "done" for the factory:
an emitted repo conforms to this grammar or the run has not finished.
**Derived from:** two ground-truth exemplar repos hand-grown before this grammar was written
(`reference/exemplars.md` — names, tiers, sizes, and imitation notes live there and only there).
When this document is ambiguous, the **templates are the tiebreaker** — this tree stands alone;
the exemplars are optional calibration where available (exemplars.md is off-limits to an eval run
entirely — its §3).

---

## 1. What an emitted repository IS

A **self-operable spec repository**: a git-ready directory that contains everything a future AI
needs to build, verify, change, and operate the product — with **no dependence on specai, on the
authoring conversation, or on any harness**. The test is the change rule inverted: *a better AI,
given only this repo, rebuilds the product completely and correctly, and knows how to take a change
request.* The two appreciating assets are the `specs/` tree and its operating manual
(`specs/start.md`); everything under `workspace/` is disposable.

specai's job ends when this repo is sealed (verified + operator countersign). `develop`, `design`,
`verify`, and change requests thereafter belong to the repo's own `start.md`, not to specai.

## 2. Root layout (binding)

```
<product>/
├── specs/                      ← the source of truth (this grammar's subject)
│   ├── start.md                ← the operating manual / AI entrypoint (§4.3)
│   ├── vision.md               ← the WHY (§4.1)
│   ├── architecture.md         ← the shape: glossary, data model, components, principles (§4.2)
│   ├── README.md               ← the map: what this repo is, how to invoke it, the file tree (§4.8)
│   ├── standards/              ← binding cross-component contracts & process standards (§4.4, §4.7)
│   ├── components/             ← one spec per component: the WHAT (§4.5)
│   └── design/                 ← the visual & interaction language, when the product has a UI (§4.6)
├── workspace/                  ← the implementation mirror of specs/ — disposable, rebuildable
│   └── README.md               ← workspace conventions (mirror rule, ports, harness) — seeded at emission
├── reference/
│   └── ideation.md             ← the founding human ideation, preserved verbatim (non-normative)
├── NOTES.md                    ← the decision ledger: founding decisions, dial score, session history (§4.9)
├── DRIFT.md                    ← the divergence ledger: where the implementation currently departs
│                                 from specs/ (§4.10) — absent until code exists and diverges
└── verdicts/                   ← durable home of relocated verdict records (`verification_core.md`
                                  §6 rule 4) — absent until the first record relocates
```

Naming bends with the dial (§5): a tier-L product family may use `products/` beside `platform/`
instead of a flat `components/`; tier S keeps the flat layout above.
The **mirror rule** is invariant: `specs/<path>` is the WHAT, `workspace/<path>` is the HOW.

## 3. The four load-bearing relationships

1. **Everything cites `architecture.md`; `architecture.md` cites `vision.md`.** The glossary and
   principles live in exactly one place and are reused verbatim — a term defined twice is a defect.
2. **Contracts are the narrow waist.** Component specs talk to each other *only* through
   `standards/` contracts and the shared glossary — never by citing each other's internals. (One
   deliberate exception class: a component may cite a sibling for a *shared surface* it explicitly
   defers to, named in its "Not this spec" header — the pattern instance lives in
   `reference/exemplars.md` §1.)
3. **`start.md` routes everything.** Every spec file (§6 check 1's two exemptions aside) is
   reachable from its boot table; a spec no command path reads is dead weight (defect), and a
   target with no reading list is unbuildable (defect).
4. **Specs absorb their intermediates.** There is no PRD, domain-model, or user-story document in
   the emitted repo: requirements land as binding clauses in component specs; the domain model
   becomes the glossary + data model; user stories become `architecture.md`'s **lifecycle stories**
   and the components' behavior sections. (The factory's requirements inventory is a working
   artifact — `phases/definition.md` — whose full absorption is what phase-6 verification checks.)

## 4. Document grammar (per kind)

Section names below are grammar; exact numbering may vary. **(dial)** marks parts gated by
`dial.md` — by tier (§5) or by dimension (its §1 rule 2). All documents obey `standards/style.md`.

### 4.1 `vision.md` — the WHY
Opens with "what this document is" (WHY here / HOW elsewhere). Then:
**The problem** · **Why now** (dial) · **Vision** (one indented, quotable statement) ·
**Value proposition** (numbered) · **Product pillars** (the load-bearing beliefs; every later
judgment call traces to one) · **Experience philosophy** · **Audience** (personas *and*
anti-personas) · **Success criteria** · **Non-goals** (numbered, binding, each marked **identity**
— permanent, the change-request firewall — or **revisitable** — a recorded scope cut a rebuild
must not "restore", reversible only as a vision edit) · **Dial** (one binding line: score + tier +
any operator override; per-dimension justifications live in `NOTES.md`).

### 4.2 `architecture.md` — the shape
Header: "Status: Authoritative. Every spec must be consistent with this document." Then:
**The system in one picture** (an ASCII/diagram a builder can hold in their head) ·
**Glossary** (canonical terms, used verbatim suite-wide — the absorbed domain model) ·
**The data model** (binding, with numbered invariants) — when the product owns durable state ·
**The components** (a table: area → what it owns → its spec file; this is the coverage anchor) ·
**The principles** (numbered, non-negotiable; "any change violating one is rejected or escalated") ·
**Lifecycle stories** (the absorbed user stories, written as acceptance narratives: first run,
primary flows, reset/retirement) · **Engineering standards** (inline at tier S if small, else cites
`standards/engineering_standard.md`) · **What this architecture deliberately does not have**
(the anti-scope — as binding as the scope) · **(dial)** inter-component communication matrix and
explicit requirements-coverage matrix at tier M/L · **(dial)** a **Money & compliance** section
whenever regulatory/money scores 2 (`dial.md` §1): the money flows and custody/settlement rules,
each REG-line of the regulatory register (`phases/definition.md`) mapped to its enforcing
component or principle, and the audit surfaces — money-path changes gate at top tier
(`change_rule.md` §4).
Declares the requirement-language convention (MUST/SHOULD per RFC 2119) once, for the whole suite.

### 4.3 `start.md` — the operating manual
The most exactly-shaped document (template: `templates/start.md`):
**§0 Philosophy** (specs-are-the-asset; WHAT/HOW both directions — transcribed HOW *and* omitted
WHAT are defects; the change rule verbatim; never guess / never fail silently; symptom-first) ·
**§1 Boot sequence** with the **boot table** (target → ordered reading list) ·
**§2 Command grammar** (per `templates/start.md` §2 — the template owns the command list and its
dial conditions; not restated here) ·
**§3 The three cases** (A fresh build · B spec changed, spec wins, reconciliation list —
unapplied reconciliation items parked in `DRIFT.md` (§4.10) · C change
request: vision-first → change rule → spec-first → conformant-alternative on principle violation →
reshape-scale requests handed back to the operator for a delta engagement) ·
**§4 Working discipline** (journaling, delegation with bounded excerpts, the QA layers tailored to
the product's acceptance gate, honesty rule, independent verification) ·
**§5 Spec editing rules** (vision-first; propose-before-edit; the **cascade graph** for this repo;
the binding style list; contract changes need version bump + migration note, said loudly) ·
**§6 Definition of Done** (checklist; always includes: every Deliverables item met, the acceptance
gate green, evidence shown, **independent verification per §4 returned PASS for the target**, no
spec contradicted or spec-first honored, `DRIFT.md` reflecting reality, and **process friction
flagged with proposed improvements to this manual** — the self-improvement loop).

### 4.4 `standards/` — contract standards (the hardened waist)
At least one **wire/interface contract** whenever ≥2 sides must agree (frontend↔backend counts):
object shapes → conventions (error shape, status codes, auth posture) → every endpoint/message
verbatim. Header carries **Version**; any change to a shape, endpoint, parameter, or status code
requires a **version bump + migration note in the document itself**. Contracts are born
consumer-driven (`phases/contracts.md`) and keep a consumers appendix (who needs which endpoint,
why — mandatory at M/L, recommended at S). Plus `engineering_standard.md` (§4.7) when not
inlined, and process standards per dial (§5): `verification_standard.md`, `develop_loop.md`.

### 4.5 `components/<name>_spec.md` — the WHAT of one component
(Template: `templates/component_spec.md`.) Title states scope in one line. Header: Status +
"read first" list (its declared inputs) + **Scope of this spec / Not this spec** (names which
sibling/standard owns each adjacent concern). Then: **why it exists** (traced to vision pillars) ·
**glossary additions only** (canonical terms reused verbatim) · numbered behavior sections with
**(binding)** markers and **worked examples labeled as binding test cases** wherever a
transformation has a right answer · **behavioral invariants** · **risk & failure considerations** ·
**open questions** (flagged, never silently resolved) · **Acceptance Criteria** (checklist) ·
**Deliverables checklist**. UI-bearing components enumerate surfaces + controls + key interactions
as binding behavior (no pixels/colors/timings — those are design's).

### 4.6 `design/design_spec.md` — the look & feel (UI products)
Component-spec shape (§4.5) with one extra discipline: it separates **intent** (the current visual
identity — replaceable) from **binding behavior** (layout shape, theming behavior, interaction
patterns, accessibility floor, motion intent). Behavior lives in feature specs; appearance here.

### 4.7 `standards/engineering_standard.md` — the chosen HOW-level
The one deliberate WHAT/HOW exception: the document that binds HOW-level choices, starting with
the stack **named and binding at the category level** ("Rust backend, Postgres via a pooled
driver, Svelte frontend" — an invented example) — changing any of it is a spec change. It MAY
inline as architecture's engineering-standards section at tier S with a **small surface** (small
= the whole standard fits as one architecture section with no template section dropped). **Its
section enumeration is owned by `templates/engineering_standard.md`** (glossary through
Deliverables checklist); every section applies whether the document stands alone or is inlined
as architecture's engineering-standards section. It exists so whole-product risk/audit and
deployment/retirement concerns are carried once, never restated per component.

### 4.8 `specs/README.md` — the map
What the product is (one paragraph) · how to invoke the repo (literal example commands against
`start.md`) · the annotated file tree · "the shape of the product in five sentences".

### 4.9 `NOTES.md` — the decision ledger
A **record, not a spec** (says so at the top; specs win — nothing binding lives here). Seeded at
emission with: the dial justifications (the score + tier themselves bind in `vision.md` §Dial),
checkpoint answers (each marked chosen or default-accepted), founding decisions with rationale, the
rationale behind the vision's revisitable cuts (the cuts themselves bind in `vision.md`
§Non-goals), open topics. Appended per working session; its seal lines carry the verification mode
(`templates/notes.md`). Durable decisions that must survive regeneration belong in specs (the
change rule); NOTES is history and context.

### 4.10 `DRIFT.md` — the divergence ledger
A **record, not a spec** — the current-state complement to NOTES' history: a non-binding, dated
ledger of where the implementation currently departs from `specs/`. Its rules:

1. **Contents.** Known code defects the specs already imply the answer to; reconciliation items a
   session could not finish; verification findings accepted with a recorded reason.
2. **Item shape.** Each item dated, grouped under a per-component heading, naming the divergence,
   the owning spec §, and the fix owed.
3. **Never a build input.** A rebuild builds from `specs/` alone — this file is never an input to
   what gets built (it may be read as context; a regeneration deletes the items it superseded).
   That is its purpose: specs stay clean of bug diaries (`style.md` §2 rule 4) without the
   knowledge living only in conversation.
4. **Acceptance defers, never dissolves.** A divergence meant to be permanent is a spec change,
   not a DRIFT item.
5. **Lifecycle.** Never emitted at a seal: the file appears the first time an implementation
   diverges and the fix cannot land in-session; an item is **deleted when fixed**; the file is
   deleted when empty — its absence asserts conformance.
6. **Spec-ahead-of-code is drift.** An `edit specs` session that knowingly moves the spec ahead of
   the code records the divergence here before it ends (the repo's develop, case B, clears it).

Three tenses, one rule: specs say what is true, `NOTES.md` says why decisions were made, `DRIFT.md`
says where reality has not caught up.

### 4.11 Process standards — `develop_loop.md` and `studio.md` (dial-gated shapes)
Neither has a full template; these category shapes are their grammar, self-sufficient without any
exemplar.
- **`develop_loop.md`** (offered S+; `verification_core.md` §8 is the normative pattern): names the
  two roles (a fresh **Builder** that reconciles code to specs; an independent **Gate** that
  commits only clause-grounded diffs), the loop steps, the stop conditions (spec defect → stop and
  return to the human; N clean passes → done), and the two laws verbatim: *the loop never edits
  specs* and *never commits a spec change*.
- **`studio.md`** (L **and** experience-led — this clause owns the condition): the design-track
  manual — how design sessions run decoupled from builds: their inputs (vision's experience
  philosophy and audience, the design spec, the UI-touching lifecycle stories — all durable
  emitted documents), the storyboard form (titled interaction sequences: state → user act →
  response, citing the design spec), and the handoff (storyboards feed feature specs' behavior
  sections; the studio is never a build gate).
- **Conformance-suite spec** (tier L, alongside versioned contracts; the operator may waive it,
  recorded in NOTES): names, per contract surface, the checks an implementation must pass to
  claim conformance — each check citing the contract § it tests, each versioned with the
  contract; the suite is the contract's acceptance criteria made executable.
- **Ops / infra standards** (tier L): the operating envelope as binding rules — environments and
  their differences, capacity/limit envelopes, backup/restore drill, incident posture (what
  degrades, what pages the operator), each rule testable like any invariant.
- **Agent standards** (tier L, only when the product is AI-operated): the operating agents'
  briefs as specs — each agent's declared inputs, authority boundary (what it may never do), and
  escalation rule, mirroring this factory's own dispatch discipline.

## 5. How the dial bends the grammar

Tier per `standards/dial.md`. Higher tiers add; they never remove.

| Grammar element | S | M | L |
|---|---|---|---|
| Layout | flat `components/` | flat, more of them | `platform/` + `products/` split allowed |
| Contract standards | one `api_contract.md` | one per boundary | versioned platform-standard class, conformance suite |
| Engineering standard | separate or inlined in architecture | separate | separate + infra/ops specs |
| Verification | fresh-eyes discipline inline in `start.md` §4 | separate standard, focused passes per `change_rule.md` §4 | full standard: QA-officer pattern, lens panel, taxonomy, verdict records |
| `develop_loop.md` (Builder/Gate auto-convergence) | optional | recommended | recommended |
| Design | `design/design_spec.md` if UI | same | + design-studio track when experience-led (`studio.md` — §4.11 owns the condition) |
| Coverage | component table + phase-6 traceability check | + explicit coverage matrix in architecture | + matrices and comms matrix, maintained |
| Stable requirement IDs | no (named sections suffice) | optional | yes, if the tree is large enough that citations strain |
| Divergence ledger | one root `DRIFT.md`, per-component headings | same | may split per component when the one file strains (length, edit contention, ownership): split files at `drift/<component>.md`, the root file becomes the index (deleted when the last split file goes); per-file absence asserts that component's conformance |
| Agent operations | no | no | agent standards when the product is AI-operated |

## 6. Mechanical conformance (the speclint class)

Phase-6 verification checks these mechanically before any judgment lens runs:

1. Every file in §2's required set exists (`DRIFT.md`, the root `verdicts/` dir, and `specs/design/`
   are conditional — absent until their first need or when no UI exists, per §2); every `specs/`
   file — except `start.md`
   (the table's host) and `specs/README.md` (the map, routed by invocation) — is reachable from
   `start.md` §1's boot table; every boot-table entry resolves to a real file.
2. Every cross-document citation (file or §section) resolves.
3. Glossary discipline: canonical terms defined once in `architecture.md`; component specs add
   terms only in "glossary additions".
4. Every component spec ends with Acceptance Criteria + Deliverables checklist; risk/audit and
   deployment concerns are carried per §4.5/§4.7 (component-local or engineering-standard, stated).
5. Every contract standard carries a Version header; the requirement-language convention is
   declared in `architecture.md`.
6. *(semi-mechanical)* Worked examples labeled **binding** exist for every transformation the
   specs define with a right answer — presence is checked here; sufficiency belongs to the
   outcomes lens.
7. `reference/ideation.md` present; `vision.md` carries the binding Dial line (§4.1); `NOTES.md`
   seeded with dial justifications and founding decisions, and any recorded seal line carries its
   verification mode (§4.9). At a **first** seal, no `DRIFT.md` (nothing has been built yet —
   §4.10); at a delta re-seal a present `DRIFT.md` conforms to §4.10 (or, at tier L, to §5's split
   form). (`DRIFT.md` is outside checks 1–2's required set, and references to it are conditional —
   they resolve vacuously while the file is legitimately absent.)
8. No template scaffolding survives: no `<placeholder>` angle-bracket text and no authoring
   blockquotes anywhere in `specs/`, outside fenced examples.
