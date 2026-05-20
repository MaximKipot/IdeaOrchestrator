# Framework Index

Read this only when routing, starting, or resuming an idea project.

## Default Read Order

1. `00-control/current-state.md`
2. `00-control/open-questions.md` only if status is blocked, skipped, or unclear
3. The current skill's listed input files only

Do not read `examples/`, `templates/project/`, future phase files, or all rules by default.

## Context Modes

| Mode | Use When |
| --- | --- |
| `Inline` | Small projects or quick updates. |
| `Clean Handoff` | Each phase should start fresh from files, possibly with another agent/model. |
| `Parallel Support` | Independent research or option-generation subtasks can run separately. |

For Clean Handoff Mode, use `framework/rules/clean-handoff.md`.

## Skill Route

| Situation | Skill |
| --- | --- |
| Existing chat, doc, transcript, or notes dump | `idea-import` |
| Fresh raw idea | `idea-intake` |
| Problem/user unclear | `problem-definition` |
| Evidence needed | `research-evidence` |
| Uncertainty needs sorting | `assumptions-risks` |
| Direction unclear | `vision-direction` |
| Tradeoff rules needed | `principles-constraints` |
| Target, value, model, channel, metrics needed | `strategy` |
| Experiment options needed | `mvp-experiments` |
| Path and roadmap needed | `decision-roadmap` |
| Actions/progress needed | `execution-tracking` |
| Evidence review or pivot needed | `review-pivot` |

## Sequential Flow

Optional: `idea-import`

Normal flow:

`idea-intake` -> `problem-definition` -> `research-evidence` -> `assumptions-risks` -> `vision-direction` -> `principles-constraints` -> `strategy` -> `mvp-experiments` -> `decision-roadmap` -> `execution-tracking` -> `review-pivot`

Manual jumps are allowed only when requested by the user and logged with risk.
