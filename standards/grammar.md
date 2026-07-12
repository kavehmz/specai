# grammar.md — The Spec-Tree Grammar (what specai emits)

**Status:** Binding for every emitted repository. This is the definition of "done" for the factory:
an emitted repo conforms to this grammar or the run has not finished.
**Derived from:** two ground-truth exemplars that were hand-grown before this grammar was written —
**feedler** (github.com/kavehmz/feedler, ~4.1K spec lines, tier S) and **a real-money trading
platform** (private, ~6.9K spec lines, tier L). When this document is
ambiguous, the exemplars are the tiebreaker (`reference/exemplars.md`).

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
└── NOTES.md                    ← the decision ledger: founding decisions, dial score, session history (§4.9)
```

Naming bends with the dial (§5): a tier-L product family may use `products/` beside `platform/`
instead of a flat `components/` (the trading platform does); tier S keeps the flat layout above (feedler does).
The **mirror rule** is invariant: `specs/<path>` is the WHAT, `workspace/<path>` is the HOW.

## 3. The four load-bearing relationships

1. **Everything cites `architecture.md`; `architecture.md` cites `vision.md`.** The glossary and
   principles live in exactly one place and are reused verbatim — a term defined twice is a defect.
2. **Contracts are the narrow waist.** Component specs talk to each other *only* through
   `standards/` contracts and the shared glossary — never by citing each other's internals. (One
   deliberate exception class: a component may cite a sibling for a *shared surface* it explicitly
   defers to, named in its "Not this spec" header — feedler's export ↔ api_contract split is the
   pattern.)
3. **`start.md` routes everything.** Every spec file is reachable from its boot table; a spec no
   command path reads is dead weight (defect), and a target with no reading list is unbuildable
   (defect).
4. **Specs absorb their intermediates.** There is no PRD, domain-model, or user-story document in
   the emitted repo: requirements land as binding clauses in component specs; the domain model
   becomes the glossary + data model; user stories become `architecture.md`'s **lifecycle stories**
   and the components' behavior sections. (The factory's requirements inventory is a working
   artifact — `phases/definition.md` — whose full absorption is what phase-6 verification checks.)

## 4. Document grammar (per kind)

Section names below are grammar; exact numbering may vary. **(dial)** marks parts that appear only
at higher tiers (§5). All documents obey `standards/style.md`.

### 4.1 `vision.md` — the WHY
Opens with "what this document is" (WHY here / HOW elsewhere). Then:
**The problem** · **Why now** (dial) · **Vision** (one indented, quotable statement) ·
**Value proposition** (numbered) · **Product pillars** (the load-bearing beliefs; every later
judgment call traces to one) · **Experience philosophy** · **Audience** (personas *and*
anti-personas) · **Success criteria** · **Non-goals** (numbered, binding — the change-request
firewall).

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
explicit requirements-coverage matrix at tier M/L.
Declares the requirement-language convention (MUST/SHOULD per RFC 2119) once, for the whole suite.

### 4.3 `start.md` — the operating manual
The most exactly-shaped document (template: `templates/start.md`):
**§0 Philosophy** (specs-are-the-asset; WHAT/HOW both directions — transcribed HOW *and* omitted
WHAT are defects; the change rule verbatim; never guess / never fail silently; symptom-first) ·
**§1 Boot sequence** with the **boot table** (target → ordered reading list) ·
**§2 Command grammar** (`develop <target>`, plain-language change requests, `edit specs:`,
`new <component>`, `verify <target>`; dial adds `design`, `develop-loop`, `archive`) ·
**§3 The three cases** (A fresh build · B spec changed, spec wins, reconciliation list · C change
request: vision-first → change rule → spec-first → conformant-alternative on principle violation) ·
**§4 Working discipline** (journaling, delegation with bounded excerpts, the QA layers tailored to
the product's acceptance gate, honesty rule, independent verification) ·
**§5 Spec editing rules** (vision-first; propose-before-edit; the **cascade graph** for this repo;
the binding style list; contract changes need version bump + migration note, said loudly) ·
**§6 Definition of Done** (checklist; always includes: every Deliverables item met, the acceptance
gate green, evidence shown, no spec contradicted or spec-first honored, and **process friction
flagged with proposed improvements to this manual** — the self-improvement loop).

### 4.4 `standards/` — contract standards (the hardened waist)
At least one **wire/interface contract** whenever ≥2 sides must agree (frontend↔backend counts):
object shapes → conventions (error shape, status codes, auth posture) → every endpoint/message
verbatim. Header carries **Version**; any schema change requires a **version bump + migration note
in the document itself**. Contracts are born consumer-driven (`phases/contracts.md`) and MAY keep a
consumers appendix (who needs which endpoint, why). Plus `engineering_standard.md` (§4.7) when not
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
The one deliberate WHAT/HOW exception: the stack is **named and binding at the category level**
("Go backend, SQLite via CGO-free driver, React/Vite frontend") — changing it is a spec change.
Owns: build & deploy (the one-command acceptance gate, e.g. `docker compose up --build`),
configuration (**binding env-var names + defaults table**), persistence rules, security posture,
HTTP conventions, whole-product Risk & Audit + Deployment & Retirement (so component specs don't
restate them), testing floor, Deliverables checklist.

### 4.8 `specs/README.md` — the map
What the product is (one paragraph) · how to invoke the repo (literal example commands against
`start.md`) · the annotated file tree · "the shape of the product in five sentences".

### 4.9 `NOTES.md` — the decision ledger
A **record, not a spec** (says so at the top; specs win). Seeded at emission with: the dial score +
reasoning, checkpoint answers, founding decisions with rationale, deliberate scope cuts (so a future
rebuild doesn't "restore" them as omitted-WHAT defects), open topics. Appended per working session.
Durable decisions that must survive regeneration belong in specs (the change rule); NOTES is history
and context.

## 5. How the dial bends the grammar

Tier per `standards/dial.md`. Higher tiers add; they never remove.

| Grammar element | S (0–3) | M (4–7) | L (8–10) |
|---|---|---|---|
| Layout | flat `components/` | flat, more of them | `platform/` + `products/` split allowed |
| Contract standards | one `api_contract.md` | one per boundary | versioned platform-standard class, conformance suite |
| Engineering standard | separate or inlined in architecture | separate | separate + infra/ops specs |
| Verification | fresh-eyes discipline inline in `start.md` §4 | separate standard, 1–2 verifier focused runs | full standard: QA-officer pattern, lens panel, taxonomy, verdict records |
| `develop_loop.md` (Builder/Gate auto-convergence) | optional | recommended | recommended |
| Design | `design/design_spec.md` if UI | same | + design-studio track (`studio.md`), storyboards |
| Coverage | component table + phase-6 traceability check | + explicit coverage matrix in architecture | + matrices and comms matrix, maintained |
| Stable requirement IDs | no (named sections suffice) | optional | yes, if the tree is large enough that citations strain |
| Agent operations | no | no | agent standards when the product is AI-operated |

## 6. Mechanical conformance (the speclint class)

Phase-6 verification checks these mechanically before any judgment lens runs:

1. Every file in §2's required set exists; every `specs/` file is reachable from `start.md` §1's
   boot table; every boot-table entry resolves to a real file.
2. Every cross-document citation (file or §section) resolves.
3. Glossary discipline: canonical terms defined once in `architecture.md`; component specs add
   terms only in "glossary additions".
4. Every component spec ends with Acceptance Criteria + Deliverables checklist; risk/audit and
   deployment concerns are carried per §4.5/§4.7 (component-local or engineering-standard, stated).
5. Every contract standard carries a Version header; the requirement-language convention is
   declared in `architecture.md`.
6. Worked examples labeled **binding** exist for every transformation the specs define with a right
   answer.
7. `reference/ideation.md` present; `NOTES.md` seeded with dial score and founding decisions.
