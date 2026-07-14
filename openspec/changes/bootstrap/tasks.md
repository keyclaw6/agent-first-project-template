# Bootstrap tasks

Follow the conduct rules in `design.md`. Phases run in order; each ends with explicit human approval.

## 1. Orient

- [ ] 1.1 Read `VISION.md`, `ARCHITECTURE.md`, `README.md`, and this change in full.
- [ ] 1.2 Confirm the human wants to run the bootstrap now, and ask for the raw idea in their own words — unpolished is fine.

## 2. Vision

- [ ] 2.1 Interview toward each `VISION.md` section in order: North Star, Who it serves, What success looks like, Non-negotiables, Not optimizing for.
- [ ] 2.2 Research prior art and evidence for the problem; present findings with a recommendation before locking the North Star.
- [ ] 2.3 Fill each section as it resolves and read it back.
- [ ] 2.4 Obtain explicit approval of the completed `VISION.md`.

## 3. Reality check

- [ ] 3.1 Walk the core experience end to end with the human: happy path, failure paths, edge cases.
- [ ] 3.2 Identify the riskiest assumption — the thing that, if false, kills the idea — and how V1 tests it cheaply.
- [ ] 3.3 Split scope: the smallest V1 that produces the vision's outcome. Everything else is explicitly later.

## 4. First specs

- [ ] 4.1 Agree on one to three V1 capabilities and their kebab-case names.
- [ ] 4.2 Write delta specs in this change under `specs/<capability>/spec.md` using `## ADDED Requirements`, `### Requirement:` headings, and `#### Scenario:` blocks.
- [ ] 4.3 Cover the failure modes from the reality check as scenarios, not only the happy path.
- [ ] 4.4 Validate: `npx openspec validate bootstrap --strict`.

## 5. Architecture

- [ ] 5.1 Research candidate stacks and structures; present two or three options with trade-offs and one recommendation. The human picks.
- [ ] 5.2 Replace every stub section in `ARCHITECTURE.md`: system shape, entry points, boundaries and dependency direction, data and external systems, run and verify commands.
- [ ] 5.3 Ensure the canonical commands are real and runnable, not aspirational.

## 6. Ownership and verification

- [ ] 6.1 Add an `openspec/ownership.toml` entry for every new requirement.
- [ ] 6.2 Run `npm run check` and resolve every error.

## 7. Finalize and remove

- [ ] 7.1 Present the full diff for human review: `VISION.md`, `ARCHITECTURE.md`, this change, ownership.
- [ ] 7.2 After approval, run: `npm run spec:finalize -- bootstrap --human-approved`.
- [ ] 7.3 Commit the baseline specs, `VISION.md`, `ARCHITECTURE.md`, ownership, and this folder's deletion together.
