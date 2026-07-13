# Architecture

This is the concise structure map used by humans and agents making code changes. Keep it current and useful; do not turn it into an implementation manual.

## Repository layout

- `src/` — production code.
- `tests/` — automated tests and test support code.
- `openspec/specs/` — baseline behavioral contract.
- `openspec/changes/` — active, temporary behavior-change proposals.
- `scripts/` — repository lifecycle and validation automation.

Do not add a `docs/` tree by default. Add durable documentation only when code, tests, specs, configuration, or generated state cannot express the necessary truth.

## System shape

Describe the major runtime components and their responsibilities once the project has them.

## Entry points

List the main application, worker, CLI, API, or deployment entry points.

## Boundaries and dependency direction

Describe the important module or domain boundaries and the allowed dependency direction. Once a boundary matters, enforce it mechanically where practical rather than relying only on prose.

## Data and external systems

Describe persistent data, queues, third-party services, and the trust boundaries around them.

## Run and verify

List the canonical commands for starting the system, running focused tests, and running the full verification suite.
