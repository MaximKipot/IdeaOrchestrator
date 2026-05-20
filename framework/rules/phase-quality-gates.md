# Phase Quality Gates

Run this before marking any phase complete.

## Required Checks

- Required files for the current phase were created or intentionally skipped.
- `00-control/current-state.md` was updated.
- Decisions were logged in `00-control/decision-log.md`.
- Open questions were logged in `00-control/open-questions.md`.
- Skipped work includes reason, risk, owner, date, and revisit trigger.
- Facts, assumptions, guesses, opinions, preferences, and decisions are not mixed.
- Rejected or deferred alternatives are preserved.
- Research gaps are explicit when research was narrowed or deferred.
- `00-control/handoff.md` was updated if Clean Handoff Mode is active.

## Completion Rule

If a required check fails, do not mark the phase complete.

Instead:

- Update the missing file.
- Ask the one blocking question.
- Or log the skip and accepted risk.

Keep the gate lightweight. It should prevent false completion, not create process overhead.

