# specai — the ideation→spec factory

A harness-agnostic AI skill that turns a human product ideation — however informal — into a
**sealed, self-operable spec repository**: vision, architecture, versioned contracts, component
specs, and an operating manual (`start.md`) that lets any future AI build, verify, and change the
product from the repo alone. specai writes specs; it never builds software — the emitted repo owns
its own `develop`.

**Lineage.** A modernization of an earlier idea→code pipeline under the spec-first doctrine of
two hand-grown exemplar repos (`reference/exemplars.md`). What was kept, changed, and dropped is
recorded in `NOTES.md`.

## Invoke

specai is an [agent skill](https://code.claude.com/docs/en/skills): `SKILL.md` carries the
`name`/`description` frontmatter a harness discovers it by. Install it on a skills path — for
Claude Code:

```
git clone https://github.com/kavehmz/specai ~/.claude/skills/specai
```

then invoke it by name from any working directory:

```
/specai new product <name> — ideation at ./my-idea.md, target ../<name>/
/specai evaluate <exemplar>
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
SKILL.md          the front door: doctrine, routing, the run, harness bindings
standards/        grammar (what an emitted repo is) · dial · style · change_rule · verification_core
phases/           definition · architecture · contracts · component_specs · emission · verification
                  · delta (product-reshaping change on a sealed repo)
templates/        the seven document skeletons (start.md, the operating manual, chief among them)
reference/        exemplars.md — the two ground-truth repos + the eval protocol
verdicts/         verification verdict records for the skill itself
NOTES.md          decision ledger (founding decisions, sessions)
```

## The shape of specai, in five sentences

An ideation enters phase 1 and becomes a vision plus a source-tagged requirements inventory and a
0–10 complexity score that sizes everything downstream. Architecture turns the inventory into a
glossary, data model, component map, and non-negotiable principles; contracts are then derived
consumer-first and hardened into versioned standards — the narrow waist. Component specs are
authored in parallel by isolated authors working from a closed input list
(`phases/component_specs.md` owns it), mirroring the product's own information architecture. Emission instantiates the operating manual and
process standards, making the repo self-operable; verification seals it with a mechanical grammar
pass, fresh-context lens verifiers (ideation coverage and buildability above all), and the
operator's countersign. After the seal, specai steps aside: the repo's own `start.md` owns
building, verifying, and change — forever.

An emitted repo keeps three tenses apart: `specs/` say what is **true**, `NOTES.md` records **why**
decisions were made, and `DRIFT.md` — appearing only once an implementation diverges — tracks where
reality has **not caught up**, item-by-item, deleted as fixed (`standards/grammar.md` §4.10).
