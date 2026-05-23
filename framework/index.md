# Framework Index

Read this only when routing, starting, or resuming an idea project.

## Default Read Order

1. `00-control/current-state.md`
2. `00-control/open-questions.md` only if status is blocked, skipped, or unclear
3. The current skill's listed input files only

Do not read `examples/`, `templates/project/`, future phase files, or all rules by default.

Before advancing, confirm required outputs are written or consciously skipped with accepted risk. Use `framework/rules/persistence-and-completion.md` when this is unclear.

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
| Existing chat, doc, transcript, or notes dump | `idea-o-00-import` |
| Fresh raw idea | `idea-o-01-intake` |
| Problem/user unclear | `idea-o-02-problem` |
| Evidence needed | `idea-o-03-research` |
| Uncertainty needs sorting | `idea-o-04-risks` |
| Direction unclear | `idea-o-05-vision` |
| Tradeoff rules needed | `idea-o-06-principles` |
| Target, value, model, channel, metrics needed | `idea-o-07-strategy` |
| Experiment options needed | `idea-o-08-mvp` |
| Path and roadmap needed | `idea-o-09-roadmap` |
| Actions/progress needed | `idea-o-10-execution` |
| Evidence review or pivot needed | `idea-o-11-review` |

## Sequential Flow

Optional: `idea-o-00-import`

Normal flow:

`idea-o-01-intake` -> `idea-o-02-problem` -> `idea-o-03-research` -> `idea-o-04-risks` -> `idea-o-05-vision` -> `idea-o-06-principles` -> `idea-o-07-strategy` -> `idea-o-08-mvp` -> `idea-o-09-roadmap` -> `idea-o-10-execution` -> `idea-o-11-review`

Manual jumps are allowed only when requested by the user and logged with risk.
