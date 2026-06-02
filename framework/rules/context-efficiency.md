# Context Efficiency Rules

The framework should protect context and avoid unnecessary file loading.

## Read Budget

Always read:

- `00-control/current-state.md`

Read only when needed:

- `00-control/open-questions.md` when blocked, skipped, unclear, or making a phase transition
- `00-control/decision-log.md` when making or revisiting a decision
- `00-control/track-context.md` when working in a sub-idea track
- Current phase input files listed by the active skill
- `framework/index.md` when routing is unclear

Do not read by default:

- `examples/`
- `templates/project/`
- Future phase folders
- All phase files
- All rules files
- Long imported source material after it has been summarized

## Framework Rule Lookup

When a skill references `framework/rules/...`, resolve the path in this order:

1. Project workspace: `<project>/framework/rules/...`
2. Installed IDEA-O framework or skill-relative location
3. Bundled reference from the current IdeaZone checkout, if available

Missing project-local rule files are not a failure. Use the installed or framework-relative copy and continue. Only block if no copy of a required rule can be found anywhere available to the agent.

## Write Budget

- Create only files needed for the current action.
- Do not create future phase folders.
- Use templates only as patterns when creating a missing file.
- Record the import fidelity choice in `00-import/import-summary.md`. Create `00-import/source-material.md` only for verbatim/local source preservation or useful source pointers, then work from `00-import/import-summary.md` afterward.
- Create optional UX or custom artifacts only when they are needed for the current phase, then index them in `00-control/current-state.md`.

## Summarization Rules

- Summarize long material before using it repeatedly.
- Preserve facts, assumptions, guesses, opinions, preferences, decisions, rejected alternatives, and open questions.
- Treat old chat conclusions as candidate decisions until confirmed.
- Prefer compact tables and bullets over narrative.

## Current-State Compaction

Keep `00-control/current-state.md` as a compact dashboard. It should include only:

- project, owner, current phase, status, last updated date
- current focus
- active decisions that affect the next action
- blocking questions for the next action
- recently changed files
- next recommended skill and next action
- active skip or jump risks
- custom or optional artifact index with purpose, status, owner, and next use

Move long history, transcripts, detailed phase summaries, and stale notes into the relevant phase file or `00-control/project-history.md` when a separate history file is actually needed. Link to those files from the dashboard instead of copying the history back in.

## Skill Rules

- A skill should be a runner, not a manual.
- Shared rules belong in `framework/rules/`.
- Routing belongs in `framework/index.md`.
- Each skill should name the minimum files to read and write.
- Ask only questions that block the next useful file update.
- When Clean Handoff Mode is active, write `00-control/handoff.md` and let the next agent/model read from files instead of chat.
- Before marking a phase complete, run the lightweight checks in `framework/rules/phase-quality-gates.md`.
