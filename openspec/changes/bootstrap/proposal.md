# Bootstrap: establish vision, first specs, and architecture

## Why

A project created from this template starts with placeholder truth: `VISION.md` has no intent, `openspec/specs/` has no behavior, `ARCHITECTURE.md` has no structure. Implementation is cheap; alignment is the scarce input. The riskiest moment in an agent-built project is the fluffy start — code written before human and agent agree on what is worth building.

This change turns project setup into a deliberate working session: a deep, collaborative interview that produces the vision, the first behavioral contract, and the initial architecture before any code exists.

## What changes

- `VISION.md` is completed and explicitly approved by the human.
- One to three V1 capabilities are specified as OpenSpec deltas under this change's `specs/`.
- `ARCHITECTURE.md`'s stub sections are replaced with the initial system shape and canonical commands.
- `openspec/ownership.toml` gains an owner for every new requirement.

## Division of labor

The agent contributes what models are good at: information access and research, prior art, option generation, and a recommendation for every question it asks. The human contributes what humans are good at: judgment about what is worth wanting, what is acceptable, and what is out of scope. The agent recommends; the human decides.

## Self-removal

Finalizing applies the first specs to the baseline and deletes this folder:

```sh
npm run spec:finalize -- bootstrap --human-approved
```

A project bootstraps once. Git history is the archive.

## Non-goals

- No code, prototypes, or locked-in dependency choices during the session beyond what `ARCHITECTURE.md` needs.
- No roadmap beyond V1. Later capabilities become ordinary OpenSpec changes.
- No new documentation artifacts such as glossaries or ADR trees. Settled vocabulary belongs in the specs' own language; hard-to-reverse decisions belong in this change and its Git history.
