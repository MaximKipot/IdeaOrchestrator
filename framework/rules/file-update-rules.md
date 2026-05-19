# File Update Rules

Markdown files are the project memory. Keep them useful, short, and current.

## Progressive Creation

- Create only the project folder before work starts.
- Do not create the full folder tree in advance.
- Do not copy all files from `templates/project/` into a new project.
- Create `00-control/current-state.md`, `00-control/open-questions.md`, and `00-control/decision-log.md` when initializing the project.
- If importing existing material, create `00-import/source-material.md` and `00-import/import-summary.md` only for that import.
- Create phase folders and files only when entering that phase or when the file is needed for a real decision, risk, note, or output.
- If a phase is skipped, log the skip in control files. Do not create the skipped phase folder only to record that it was skipped.
- Use `templates/project/` as reference content for files created just in time.

## General Rules

- Prefer dated bullets and compact tables.
- Keep raw notes separate from synthesized direction.
- Preserve rejected alternatives.
- Move stale information to an archive section instead of deleting it.
- Link related files when a decision depends on research or assumptions.

## Required Updates

Every phase must update:

- The phase output files.
- `00-control/current-state.md`.
- `00-control/decision-log.md` when a decision was made.
- `00-control/open-questions.md` when a question remains unresolved.

For imports from existing material:

- Preserve source material or a faithful summary in `00-import/source-material.md`.
- Put extracted structure in `00-import/import-summary.md`.
- Put confirmed decisions in `00-control/decision-log.md`.
- Put unconfirmed implied decisions in `00-control/open-questions.md` or the candidate decisions section of `00-import/import-summary.md`.

## File Style

- Use plain Markdown.
- Keep headings stable.
- Avoid long narrative unless context requires it.
- Label claims as `Fact`, `Assumption`, `Guess`, `Opinion`, `Preference`, or `Decision`.
