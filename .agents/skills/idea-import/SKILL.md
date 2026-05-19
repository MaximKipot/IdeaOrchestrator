---
name: idea-import
description: Use when starting or continuing an idea project from existing source material such as a long chat, document, transcript, research dump, strategy note, or mixed notes that need to be organized before normal idea intake.
---

# Idea Import

## Quick Start

1. Read or receive the source material.
2. Create only the control files and `00-import` files if they are missing; do not create later-phase folders.
3. Preserve the source material verbatim when practical, or write a faithful summary with a reference to the original location.
4. Extract candidate ideas, claims, preferences, rejected alternatives, open questions, and candidate decisions.
5. Classify claims as `Fact`, `Assumption`, `Guess`, `Opinion`, `Preference`, or `Decision` only when confirmed.
6. Ask the user to confirm the main idea and any candidate decisions.
7. Update `00-control/current-state.md` and recommend `idea-intake` or `problem-definition`.

## Ease Of Use Rules

- Do not make the user clean up the material before importing it.
- Preserve messy context in `00-import/source-material.md`; put structure in `00-import/import-summary.md`.
- Treat prior chat conclusions as candidate decisions, not confirmed decisions.
- Prefer one recommended next step over a broad menu.
- If the source contains several unrelated ideas, recommend one project focus and ask the user to confirm.
- Do not create folders for future phases during import.

## When To Use

Use before normal idea intake when the user already has substantial source material.

Good triggers:

- Long AI chat about an idea
- Existing strategy doc
- Meeting notes or transcript
- Research dump
- Mixed notes with several possible ideas
- User asks to continue from previous discussion

Do not use when the user is starting from a fresh short idea. Use `idea-intake` instead.

## Inputs

- Existing chat, document, transcript, notes, or pasted material
- Existing project files, if any
- User preference for preserving source verbatim or summarized

## Files To Read

- User-provided source material
- `00-control/current-state.md` if it exists
- `00-control/open-questions.md` if it exists
- `00-control/decision-log.md` if it exists

## Files To Write

- `00-control/current-state.md`
- `00-control/open-questions.md`
- `00-control/decision-log.md` for confirmed decisions only
- `00-import/source-material.md`
- `00-import/import-summary.md`

## Questions To Ask

Ask at most one question at a time. Prefer these only when needed:

- Should I preserve the source verbatim or summarize it with a reference?
- Which candidate idea should become the main project?
- Are these candidate decisions confirmed, or should they stay open?

## Blocking Conditions

- No source material is available.
- The source contains several unrelated ideas and the user will not choose one project focus.
- A prior conclusion is being treated as a confirmed decision without user confirmation.
- The source material is too large to preserve and no summary/reference approach is accepted.

## Skip Behavior

If import is skipped despite existing material, log the risk that important context, rejected alternatives, assumptions, or implied decisions may be lost.

## Outputs

- Source material preserved or faithfully summarized
- Import summary with candidate ideas and classified claims
- Candidate decisions separated from confirmed decisions
- Open questions logged
- Recommended next skill named

## Next Recommended Skill

Primary: `idea-intake` when the main idea needs confirmation or sharpening.

Alternative: `problem-definition` when the main idea is already clear and the imported material contains enough context to describe the problem.

Fallback: `idea-orchestrator` if the source material suggests multiple possible projects or a manual phase jump.
