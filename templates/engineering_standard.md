# TEMPLATE — standards/engineering_standard.md (grammar §4.7 · the chosen HOW-level)

> Authoring notes in blockquotes; delete them. Reference instance: feedler's
> `engineering_standard.md`. Tier S with a tiny surface MAY inline this as `architecture.md` §7;
> everything below still applies, just relocated.

# <Product> — Engineering Standard

**Status:** Binding for every build. **Read `architecture.md` first.**
**Scope:** the stack, the deployment shape, the build, configuration, persistence, security
posture, conventions, and the testing floor. This document carries the **whole-product Risk &
Audit and Deployment & Retirement** concerns, so component specs do not each restate them.

## 1. Glossary
> Additions only (the binary, the data dir, …).

## 2. Stack (the chosen HOW — binding at this level)
> The one licensed WHAT/HOW exception (style.md §1): name the categories and chosen technologies —
> backend language, persistence + driver class, frontend framework class, key library classes —
> from the operator's engineering defaults. "The dependency set is replaceable per-library as long
> as required behavior is preserved; the categories are binding; changing them is a spec change."

## 3. Deployment shape (binding)
> The product's equivalent of "one binary, one port, one command": what serves what, what is
> embedded vs separate, what is *never* exposed. Numbered rules with teeth.

## 4. Configuration (binding env-var contract)
> The table: | Variable | Default | Meaning |. **Names and defaults are binding** — the operator's
> compose file and README depend on them. State what configuration surfaces deliberately don't
> exist.

## 5. Persistence rules (binding)
> Where durable state lives, journal/consistency mode, writer discipline, idempotent schema
> creation, migration posture ("additive and forgiving; a destructive migration is a loud spec
> change"), backup story.

## 6. Security posture (binding)
> The honest surface for THIS product: untrusted-input handling, outbound limits
> (timeouts/size caps/user-agent), secrets stance, PII/telemetry stance. What the operator is
> responsible for (e.g. not exposing an auth-less port) — stated, not papered over.

## 7. Conventions
> HTTP/error/status conventions if not already the contract's; logging posture; graceful shutdown.

## 8. Build & deployment (binding)
> The build stages, the **one-command acceptance gate** verbatim (e.g.
> `docker compose up --build`), the healthcheck, the clean-reset path (`down -v` class), upgrade
> story.

## 9. Risk & Audit (whole product)
> The largest risks, each with its named mitigation and how to verify it. How the system is
> audited (what's inspectable, what's queryable).

## 10. Deployment & Retirement
> Deploy, back up, retire — each one paragraph, each ending in a clean state.

## 11. Testing floor
> The acceptance gate + which spec'd worked examples are the highest-value unit tests (name the
> component specs that carry them) + what a smoke run must cover.

## 12. Deliverables checklist
> What must exist infrastructure-wise when `develop <product>` completes.
