# Blocking And Skipping Rules

The framework should move sequentially, but it should not pretend missing information is resolved.

## Blocking

Block progress when a missing answer could materially change the next phase.

Log unresolved questions in `00-control/open-questions.md` under one of these triage sections:

- `Blocking Next Action`: must be answered before the next useful file update or phase advance.
- `Decision Needed Soon`: does not block the immediate edit, but will block an upcoming decision.
- `Research Later`: evidence should be gathered later; do not let it silently become an assumption.
- `Parking Lot`: useful but not tied to the current sequence.
- `Resolved`: answered, closed, or superseded questions preserved for traceability.

Each question row must include:

| Date | Question | Classification | Owner | Phase/Status | Revisit Trigger |
| --- | --- | --- | --- | --- | --- |

Use `Blocking Next Action` sparingly. The first unanswered row in that section is the question to ask the user next.

## Skipping

Skipping is allowed only when the user consciously accepts the risk.

Do not infer skip acceptance from silence, impatience, or a vague request to continue. If the risk is material, state it briefly and record explicit acceptance before advancing.

Log skips in the current phase file and `00-control/current-state.md`:

| Date | Skipped Item | Reason | Risk | Accepted By | Revisit Trigger |
| --- | --- | --- | --- | --- | --- |

## Non-Skippable Behavior

- Do not delete skipped items.
- Do not hide skipped research.
- Do not treat a skipped decision as made.
- Do not advance when a blocking question remains unresolved unless the user explicitly accepts the risk.
- Do not mix blocking questions with parking-lot questions; triage them so the next answer needed is obvious.
