# Framework Index

Read this only when routing, starting, or resuming an idea project.

## Default Read Order

1. `00-control/current-state.md`
2. `00-control/open-questions.md` only if status is blocked, skipped, or unclear
3. The current skill's listed input files only

Do not read `examples/`, `templates/project/`, future phase files, or all rules by default.

Resolve `framework/rules/...` from the project workspace first, then from the installed IDEA-O skill/framework location. Missing project-local rules are not a failure.

Before advancing, confirm required outputs are written or consciously skipped with accepted risk. Use `framework/rules/persistence-and-completion.md` when this is unclear.

When the user asks a direct reasoning, process, or product question, answer first. Update Markdown only if the answer changes durable project memory: a decision, risk, evidence item, assumption, open question, rejected alternative, artifact index, current focus, or next action. If no durable update is needed, say so and do not force a phase run.

Keep `00-control/current-state.md` as a compact dashboard: active decisions, blocking questions, recently changed files, next recommended skill, and next action. Keep long history in phase files or `00-control/project-history.md` only when needed.

## Context Modes

| Mode | Use When |
| --- | --- |
| `Inline` | Small projects or quick updates. |
| `Clean Handoff` | Each phase should start fresh from files, possibly with another agent/model. |
| `Parallel Support` | Independent research or option-generation subtasks can run separately. |

For Clean Handoff Mode, use `framework/rules/clean-handoff.md`.

Before marking a phase complete, use `framework/rules/phase-quality-gates.md`.

Use `framework/rules/challenge-pass.md` in phases 03, 04, 08, 09, and 11.

## Depth And Research Shortcuts

`Assumption-led` is a research depth/mode for narrowing work around the riskiest decision-relevant assumptions. It preserves the mandatory market scan, evidence labels, deferred research risk, and smallest validation step.

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
| Implementation-ready spec needed before execution | `idea-o-10-implementation-spec` |
| Agent execution boundaries needed before execution | `idea-o-10-execution-rules` |
| Actions/progress needed | `idea-o-10-execution` |
| Build/test/debug/user-feedback evidence needs capture without full review | `idea-o-10-execution-evidence` |
| Evidence review or pivot needed | `idea-o-11-review` |
| Idea artifacts need branching, staging, commit, push, or PR safety | `idea-o-publish` |
| Focused child idea track needed | Use `framework/rules/sub-idea-tracks.md`, then route the child project through `idea-o` |

## Sequential Flow

Optional: `idea-o-00-import`

Normal flow:

`idea-o-01-intake` -> `idea-o-02-problem` -> `idea-o-03-research` -> `idea-o-04-risks` -> `idea-o-05-vision` -> `idea-o-06-principles` -> `idea-o-07-strategy` -> `idea-o-08-mvp` -> `idea-o-09-roadmap` -> `idea-o-10-execution` -> `idea-o-11-review`

Optional Phase 10 prep:

`idea-o-09-roadmap` -> `idea-o-10-implementation-spec` -> `idea-o-10-execution-rules` -> `idea-o-10-execution`

Use prep only when implementation work is concrete enough to delegate or execution boundaries matter. The implementation spec should cover non-goals, forbidden assumptions, acceptance criteria, verification expectations, and Spec Kit compatible prompt output when applicable. Ask the user before resolving decision forks in specs, permissions, execution mode, or verification.

Phase 10 evidence capture may run inside execution without forcing Phase 11:

`idea-o-10-execution` -> `idea-o-10-execution-evidence` -> `idea-o-10-execution`

Move to `idea-o-11-review` only when execution evidence changes direction, finishes an experiment, creates a pivot/stop/pause decision, or requires broader tradeoff review.

Manual jumps are allowed only when requested by the user and logged with risk.

## Optional Escape Hatches

- Direct-answer persistence: use `framework/rules/persistence-and-completion.md` for reasoning questions that may or may not update files.
- Import fidelity: use `framework/rules/import-fidelity.md` when importing existing material.
- Sub-idea tracks: use `framework/rules/sub-idea-tracks.md` and create only `00-control/track-context.md` plus needed control files.
- Publishing: use `idea-o-publish` and `framework/rules/publish-safety.md`.
- Research decision packets: use `framework/rules/research-decision-packets.md` from Phase 03 when evidence supports a decision.
- Optional UX artifacts: use `framework/rules/optional-ux-artifacts.md`; create `screen-map.md`, `copy-decisions.md`, `interaction-rules.md`, or `permission-experience.md` only when needed and index them in current state.
