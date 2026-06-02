# Phase 10: Execution Tracking

## Purpose

Track progress, next actions, current focus, and evidence produced by execution.

Optional prep in this phase can produce an implementation spec and agent execution rules before tracking begins.

Use `idea-o-10-implementation-spec` for implementation-ready requirements, non-goals, forbidden assumptions, acceptance criteria, verification expectations, and Spec Kit compatible prompt output. Use `idea-o-10-execution-rules` for allowed/protected files, permissions, stop conditions, verification commands, and handoff evidence.

Use `idea-o-10-execution-evidence` when build, test, debug, launch, user feedback, or implementation work creates evidence that should update project memory without forcing a full review phase.

## Read

- `00-control/current-state.md`
- `09-roadmap/selected-path.md`
- `09-roadmap/roadmap.md`
- `10-execution/implementation-spec.md` when implementation-ready requirements exist
- `10-execution/agent-execution-rules.md` when AI agents will execute the work
- `10-execution/next-actions.md`
- `10-execution/progress-log.md`
- `10-execution/execution-evidence.md` when evidence needs detail

## Write

- `10-execution/implementation-spec.md` when build-ready requirements are needed
- `10-execution/agent-execution-rules.md` when AI agent boundaries are needed
- `10-execution/next-actions.md`
- `10-execution/progress-log.md`
- `10-execution/execution-evidence.md` when evidence needs detail
- `10-execution/current-focus.md`
- `00-control/current-state.md`
- `00-control/open-questions.md`
- `00-control/decision-log.md` when execution confirms, changes, supersedes, rejects, or defers a decision

## Questions

- What is the current focus?
- What is the next action?
- What progress happened?
- What evidence did execution create?
- Did that evidence change a decision, invalidate an assumption, or alter user-visible behavior?
- What files or control logs must be updated?
- Does this execution need an implementation spec before work starts?
- Does this execution need agent execution rules before work starts?
- What decision forks must be resolved by the user rather than assumed by agents?
- What non-goals, forbidden assumptions, or verification expectations must be explicit before execution continues?

## Blocking Conditions

- No owner or next action exists.
- Execution reveals a decision that has not been logged.
- Execution evidence changes user-visible behavior, scope, success criteria, or implementation assumptions without updating the relevant files.
- Implementation agents would need to invent requirements, acceptance criteria, permissions, execution mode, or verification rules.

## Done When

- Next actions are clear.
- Progress is logged.
- Execution evidence is captured in `progress-log.md` or `execution-evidence.md`.
- Any needed implementation spec or execution rules exist, or skipped prep is logged with accepted risk.
- The next recommended skill is `idea-o-11-review` only after evidence changes direction, finishes an experiment, creates a pivot/stop/pause decision, or requires broader tradeoff review.
