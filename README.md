# specai — the ideation→spec factory

A harness-agnostic AI skill that turns a human product ideation — however informal — into a
**sealed, self-operable spec repository**: vision, architecture, versioned contracts, component
specs, and an operating manual (`start.md`) that lets any future AI build, verify, and change the
product from the repo alone. specai writes specs; it never builds software — the emitted repo owns
its own `develop`.

**Lineage.** The ai-it pipeline (2025: idea → PRD → domain → stories → architecture → APIs →
services → code, as ~13.8K lines of Roo prompts) modernized under the 2026 spec-first doctrine of
two hand-grown exemplars — **feedler** (tier S) and a real-money trading platform (tier L). What
was kept, changed, and dropped is recorded in `NOTES.md`.

## Invoke

specai is an [agent skill](https://code.claude.com/docs/en/skills): `SKILL.md` carries the
`name`/`description` frontmatter a harness discovers it by. Install it on a skills path — for
Claude Code:

```
git clone https://github.com/kavehmz/specai ~/.claude/skills/specai
```

then invoke it by name from any working directory:

```
/specai new product feedler2 — ideation at ./my-idea.md, target ../feedler2/
/specai evaluate feedler
/specai improve specai: <request>
```

or just describe the task ("turn ./my-idea.md into a spec repo") — the agent matches on the
skill's description and loads it itself. On a harness with no skill system, the fallback is the
file: start a session in this directory and open with "Read SKILL.md." followed by the same
commands.

For a product that already has a sealed repo, don't come here — use that repo's own
`specs/start.md`.

## Layout

```
SKILL.md          the dispatcher: doctrine, routing, the run, harness bindings
standards/        grammar (what an emitted repo is) · dial · style · change_rule · verification_core
phases/           definition · architecture · contracts · component_specs · emission · verification
templates/        the seven document skeletons (start.md is the crown)
reference/        exemplars.md — the two ground-truth repos + the eval protocol
NOTES.md          decision ledger (founding decisions, sessions)
```

## The shape of specai, in five sentences

An ideation enters phase 1 and becomes a vision plus a source-tagged requirements inventory and a
0–10 complexity score that sizes everything downstream. Architecture turns the inventory into a
glossary, data model, component map, and non-negotiable principles; contracts are then derived
consumer-first and hardened into versioned standards — the narrow waist. Component specs are
authored in parallel by isolated authors who see only the contracts and their own scope, mirroring
the product's own information architecture. Emission instantiates the operating manual and
process standards, making the repo self-operable; verification seals it with a mechanical grammar
pass, fresh-context lens verifiers (ideation coverage and buildability above all), and the
operator's countersign. After the seal, specai steps aside: the repo's own `start.md` owns
building, verifying, and change — forever.

An emitted repo keeps three tenses apart: `specs/` say what is **true**, `NOTES.md` records **why**
decisions were made, and `DRIFT.md` — appearing only once an implementation diverges — tracks where
reality has **not caught up**, item-by-item, deleted as fixed (`standards/grammar.md` §4.10).
