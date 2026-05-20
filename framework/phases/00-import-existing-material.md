# Optional Pre-Phase: Import Existing Material

## Purpose

Turn a long chat, document, transcript, research dump, or mixed notes into structured project memory before normal idea intake.

This is optional. Use it only when source material already exists.

## Read

- User-provided source material
- `00-control/current-state.md` if it exists
- `00-control/open-questions.md` if it exists
- `00-control/decision-log.md` if it exists

## Write

- `00-control/current-state.md`
- `00-control/open-questions.md`
- `00-control/decision-log.md` for confirmed decisions only
- `00-import/source-material.md`
- `00-import/import-summary.md`

## Questions

- What material should be treated as the source?
- Should the source be preserved verbatim, summarized, or referenced by filename?
- Which extracted idea should be treated as the main idea?
- Are any candidate decisions confirmed?

## Blocking Conditions

- No source material is available.
- The material contains several unrelated ideas and the user will not choose one to start with.
- A prior conclusion is being treated as a decision without user confirmation.

## Skip Behavior

If import is skipped despite existing material, log the risk that important context, rejected alternatives, or assumptions may be lost.

## Done When

- Source material is preserved or faithfully summarized.
- Extracted claims are classified.
- Candidate decisions are separated from confirmed decisions.
- Open questions are logged.
- The next recommended skill is `idea-o-intake` or `idea-o-problem`.
