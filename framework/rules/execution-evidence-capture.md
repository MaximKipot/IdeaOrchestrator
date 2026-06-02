# Execution Evidence Capture

Use this routine when build, test, debug, launch, user feedback, or other execution work teaches the idea something worth preserving, but the project does not need a full Phase 11 review yet.

## Capture Questions

Record the answers in `10-execution/execution-evidence.md` or `10-execution/progress-log.md`:

- What new evidence did execution create?
- What command, test, artifact, user observation, or debug finding produced it?
- Did a decision change or need confirmation?
- Was an assumption invalidated, weakened, or strengthened?
- Did user-visible behavior, scope, constraints, or success criteria change?
- What files or control logs must be updated now?

## Update Rules

- Update `10-execution/progress-log.md` for ordinary progress and evidence.
- Create or update `10-execution/execution-evidence.md` when evidence needs more explanation than one progress-log row.
- Update `00-control/current-state.md` with changed focus, blockers, recently changed files, and next action.
- Update `00-control/decision-log.md` when execution confirms, changes, supersedes, rejects, or defers a decision.
- Update `00-control/open-questions.md` when execution creates a question that blocks the next action or should be answered soon.
- Update the relevant phase file when execution changes product, UX, research, risk, MVP, roadmap, or implementation-spec content.

Small evidence captures may stay in Phase 10. Move to `idea-o-11-review` only when evidence changes direction, finishes an experiment, creates a pivot/stop/pause decision, or requires broader tradeoff review.
