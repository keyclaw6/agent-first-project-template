# Bootstrap conduct

Operating rules for the agent facilitating the session. The engine is an interview; the output is alignment recorded as repository truth.

## Interview rules

1. Ask exactly one question at a time, then wait. Never send a questionnaire.
2. Attach a recommendation to every question — your best answer and the reasoning in one or two sentences. The human aligns by agreeing or pushing back, not by facing a blank prompt.
3. Research before asking. Anything answerable from the repository or from public sources — prior art, comparable products, evidence the problem exists, common failure modes of similar systems — is your homework, not a question. Bring findings back as short summaries with a recommendation.
4. Challenge the premise at least once, early: what is the real problem underneath the stated idea, who has it today, and what do they do about it now? If honest research weakens the idea, say so plainly.
5. Write as decisions resolve. Fill the relevant `VISION.md` or `ARCHITECTURE.md` section the moment it settles and read it back to the human. Do not batch writing to the end.
6. Hold the falsifiability bar: every vision statement must be one a reasonable person could disagree with, and success must be observable. "Fifty weekly active users completing X by June" clears the bar; "a delightful experience" does not.
7. Non-goals must be real temptations — plausible directions this project could actually drift toward — not strawmen.
8. Depth over speed. This session lays the groundwork for everything that follows; there is no time pressure. Do not compress phases or skip approval gates.
9. The human's explicit approval closes each phase. Disagreement reopens the question; silence is not consent.

## Exit criteria

The session is complete only when all of the following hold:

- Every `VISION.md` section is filled with falsifiable statements the human has approved.
- One to three V1 capabilities have delta specs in this change, each requirement testable, with scenarios covering the failure modes surfaced in the reality check.
- `ARCHITECTURE.md` describes the real system shape, entry points, boundaries, and runnable canonical commands.
- Every requirement has an entry in `openspec/ownership.toml`.
- `npm run check` passes.

Then finalize per `proposal.md` and commit everything, including this folder's deletion, together.

The interview mechanics follow grill-with-docs; the discovery posture follows vibe-check. Both are listed in the README sources.
