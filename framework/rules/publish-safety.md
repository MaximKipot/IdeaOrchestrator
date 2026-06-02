# Publish Safety

Use this checklist before branching, staging, committing, pushing, or opening a pull request for idea artifacts.

## Confirm Before Git Writes

- Target idea folder and absolute path.
- Repository root and current branch.
- Base branch for the publish branch.
- Branch naming convention, usually `codex/<idea-or-track-name>`.
- Exact files to stage.
- Whether generated, source, private, or unrelated files must be excluded.
- Whether the publish is a branch only, commit, push, or pull request.

## Wrong-Folder Prevention

Before staging, run checks equivalent to:

- `pwd`
- `git status --short --branch`
- `git diff --name-only`
- `git ls-files --others --exclude-standard`

Confirm staged paths are inside the intended idea folder or explicitly approved shared framework files. Do not stage unrelated dirty worktree changes.

## Control-File Record

Record the publish decision in control files before or as part of the publish:

- `00-control/decision-log.md`: branch or publish decision, base branch, scope, and tradeoffs.
- `00-control/current-state.md`: recently changed files, publish status, and next action.
- `00-control/open-questions.md`: unresolved publishing blockers, if any.

If the user asks only for a safety review, do not stage, commit, push, or create a PR.
