# Context Efficiency Rules

The framework should protect context and avoid unnecessary file loading.

## Read Budget

Always read:

- `00-control/current-state.md`

Read only when needed:

- `00-control/open-questions.md` when blocked, skipped, unclear, or making a phase transition
- `00-control/decision-log.md` when making or revisiting a decision
- Current phase input files listed by the active skill
- `framework/index.md` when routing is unclear

Do not read by default:

- `examples/`
- `templates/project/`
- Future phase folders
- All phase files
- All rules files
- Long imported source material after it has been summarized

## Write Budget

- Create only files needed for the current action.
- Do not create future phase folders.
- Use templates only as patterns when creating a missing file.
- Keep source material in `00-import/source-material.md`; work from `00-import/import-summary.md` afterward.

## Summarization Rules

- Summarize long material before using it repeatedly.
- Preserve facts, assumptions, guesses, opinions, preferences, decisions, rejected alternatives, and open questions.
- Treat old chat conclusions as candidate decisions until confirmed.
- Prefer compact tables and bullets over narrative.

## Skill Rules

- A skill should be a runner, not a manual.
- Shared rules belong in `framework/rules/`.
- Routing belongs in `framework/index.md`.
- Each skill should name the minimum files to read and write.
- Ask only questions that block the next useful file update.
- When Clean Handoff Mode is active, write `00-control/handoff.md` and let the next agent/model read from files instead of chat.
