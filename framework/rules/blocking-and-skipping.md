# Blocking And Skipping Rules

The framework should move sequentially, but it should not pretend missing information is resolved.

## Blocking

Block progress when a missing answer could materially change the next phase.

Log blockers in `00-control/open-questions.md`:

| Date | Question | Why It Blocks | Owner | Needed By | Status |
| --- | --- | --- | --- | --- | --- |

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
