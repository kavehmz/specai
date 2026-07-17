# TEMPLATE — vision.md (grammar §4.1 · style.md applies)

> Authoring notes are in blockquotes; delete them. Sections marked *(dial)* per `standards/dial.md`.

# <Product> — Vision

**What this document is:** the WHY. Every product judgment call traces back here. If a question is
"what should this feel like / who is it for / is this worth building", this document answers; if it
is "how is the system shaped / what is the contract", `architecture.md` answers.

## 1. The problem
> 2–4 paragraphs, concrete. What's broken or missing in the world, in the operator's own terms
> (sharpened, not replaced). Name the wrong bets competitors/alternatives make.

## 2. Why now *(this template owns the condition: tier M/L, or when the ideation implies timing)*
> What changed to make this buildable/valuable now.

## 3. Vision
> **One indented, quotable statement** — the product in a single sentence a builder can test
> decisions against. Then ≤2 paragraphs: the deliberately conventional parts, and the one or two
> opinionated ideas (every good product has few).

## 4. Value proposition
> Numbered, 3–5 items, each a user-felt outcome (not a feature name).

## 5. Product pillars
> The load-bearing beliefs, one subsection each (### 5.n <pillar>). Each pillar must be strong
> enough to *reject a future feature request* — that's its job. Include the scope-defining ones
> (the pillar that fixes who this is for and at what scale — an invented example: "offline-first
> by design"), the experience ones, and the doctrine ones (e.g. disposable code / durable specs,
> when the operator runs that doctrine).

## 6. Experience philosophy
> Bulleted stances on how it should feel: what's conventional on purpose, what's fast, what's
> honest (state, errors, counts), theming/accessibility posture. Behavior-level, never pixels.

## 7. Audience
> **Primary persona(s)** — who, concretely, and what they do with it.
> **Anti-persona(s)** — who this is deliberately not for. As binding as the personas.

## 8. Success criteria
> Measurable or observable: "time to X", "zero-friction Y", "one command up, one command away".
> These become acceptance narratives in architecture's lifecycle stories.

## 9. Non-goals
> **Numbered, binding.** Promoted from the definition inventory's X-lines, each with its one-line
> reason and one of two marks:
> - **(identity)** — permanent; part of what the product *is*. The change-request firewall:
>   `start.md` case C stops requests violating one and proposes a conformant alternative.
> - **(revisitable)** — a deliberate scope cut (an invented example: "no offline mode in v1").
>   Binding on every rebuild — a
>   regeneration must NOT restore it as an omitted-WHAT defect — but reversible by the operator as
>   a normal vision edit. The *why* behind each cut lives in `NOTES.md`.

## 10. Dial
> **One binding line:** `Dial: <n>/10 → tier <S|M|L>` plus any operator override and its reason.
> This line sizes the repo's process forever (verification depth, change gating — the repo's own
> standards read it). Per-dimension justifications are history and live in `NOTES.md`.
