---
name: idea-o-publish
description: Use when an idea project or sub-idea track is ready to be branched, staged, committed, pushed, or opened as a pull request.
---

# Publish Idea Artifacts

## Quick Start

1. Read `00-control/current-state.md` and `framework/rules/publish-safety.md`.
2. Confirm target folder, repository root, base branch, branch name, and exact files to stage.
3. Check the worktree for unrelated changes before any git write.
4. Record the publish decision in control files.
5. Perform only the git actions the user explicitly requested.

## Context Budget

Always read:

- `00-control/current-state.md`

Read only if needed:

- `00-control/decision-log.md`
- `00-control/open-questions.md`
- `00-control/track-context.md` for sub-idea tracks
- `framework/rules/publish-safety.md`

Do not read:

- every phase file
- templates
- unrelated repository files

Resolve `framework/rules/...` from the project workspace first, then from the installed IDEA-O skill/framework location. Missing project-local rules are not a failure.

## Files To Write

- `00-control/decision-log.md` for the publish decision
- `00-control/current-state.md` for publish status, recently changed files, and next action
- `00-control/open-questions.md` for publish blockers
- `00-control/handoff.md` when Clean Handoff Mode is active

## Confirmations

Confirm these before staging, committing, pushing, or opening a PR:

- Target idea folder and absolute path.
- Repository root.
- Base branch.
- Publish branch name, usually `codex/<idea-or-track-name>`.
- Exact files to stage.
- Files to exclude.
- Requested git actions: branch only, commit, push, PR, or some subset.

## Wrong-Folder Checks

Run checks equivalent to:

- `pwd`
- `git status --short --branch`
- `git diff --name-only`
- `git ls-files --others --exclude-standard`

Do not stage unrelated dirty worktree changes. Stop if intended files are outside the confirmed folder unless the user explicitly approves shared framework files.

## Blocking Conditions

- Target folder, base branch, branch name, or files to stage are unclear.
- Unrelated dirty changes would be staged.
- The user has not explicitly requested the git write action.
- Publish would omit required control-file updates.

## Outputs

- Publish checklist result
- Control-file publish decision
- Git actions completed, if explicitly requested
- Remaining blockers or next action
