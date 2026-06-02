# Phase Quality Gates

Run this before marking any phase complete.

## Required Checks

- Required files for the current phase were created or intentionally skipped.
- Existing phase files and control files were checked for what the user already completed, skipped, or left blocked.
- Required phase outputs are written, or each missing output has a conscious skip with accepted risk.
- `00-control/current-state.md` was updated.
- `00-control/current-state.md` remains a compact dashboard with active decisions, blocking questions, recently changed files, next recommended skill, and next action.
- Optional UX or custom artifacts created in the phase are indexed in `00-control/current-state.md` with purpose, status, owner, and next use.
- Decisions were logged in `00-control/decision-log.md`.
- Decision lifecycle status is explicit: Active, Superseded, Rejected, Deferred, or Archived. Superseded decisions link to replacements, and active decisions appear in the top summary.
- Open questions were logged in `00-control/open-questions.md`.
- Open questions are triaged as Blocking Next Action, Decision Needed Soon, Research Later, Parking Lot, or Resolved, with owner, phase/status, and revisit trigger.
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
