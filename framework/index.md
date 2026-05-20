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

Before marking a phase complete, use `framework/rules/phase-quality-gates.md`.

## Skill Route

| Situation | Skill |
| --- | --- |
| Existing chat, doc, transcript, or notes dump | `idea-o-import` |
| Fresh raw idea | `idea-o-intake` |
| Problem/user unclear | `idea-o-problem` |
| Evidence needed | `idea-o-research` |
| Uncertainty needs sorting | `idea-o-assumptions` |
| Direction unclear | `idea-o-vision` |
| Tradeoff rules needed | `idea-o-principles` |
| Target, value, model, channel, metrics needed | `idea-o-strategy` |
| Experiment options needed | `idea-o-mvp` |
| Path and roadmap needed | `idea-o-roadmap` |
| Actions/progress needed | `idea-o-execution` |
| Evidence review or pivot needed | `idea-o-review` |

## Sequential Flow

Optional: `idea-o-import`

Normal flow:

`idea-o-intake` -> `idea-o-problem` -> `idea-o-research` -> `idea-o-assumptions` -> `idea-o-vision` -> `idea-o-principles` -> `idea-o-strategy` -> `idea-o-mvp` -> `idea-o-roadmap` -> `idea-o-execution` -> `idea-o-review`

Manual jumps are allowed only when requested by the user and logged with risk.
