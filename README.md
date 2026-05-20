# Codex Idea Development Framework

A reusable Markdown-first framework for turning raw business or actionable ideas into researched directions, principles, strategy, MVP or experiment options, decisions, next actions, and review loops.

The framework is built for Codex. It keeps the project memory in files so work can continue across sessions without depending on chat history.

It is also context-efficient by default: Codex should read the current state first, then only the files needed for the current phase.

## When To Use It

Use this framework for software ideas, businesses, services, internal initiatives, workshops, content projects, physical products, or personal projects.

It works best when an idea is still uncertain and needs structured development before execution.

## Start A New Idea Project

1. Create only one empty project folder for the idea.
2. Open that folder with Codex.
3. Ask Codex to use `.agents/skills/idea-orchestrator/SKILL.md`.
4. Codex creates only the control files needed to start:
   - `00-control/current-state.md`
   - `00-control/open-questions.md`
   - `00-control/decision-log.md`
5. Codex creates phase folders and files only when that phase starts or when a file is actually needed.
6. Let Codex suggest a depth level, then accept or override it.

Do not copy `templates/project/` into the new project. The templates are reference patterns, not an up-front scaffold.

Suggested depth levels:

- `Light`: personal, internal, or low-risk idea.
- `Standard`: most business, software, service, or content ideas.
- `Deep`: high-cost, high-risk, regulated, or strategically important idea.

## Start From Existing Material

Use `idea-import` before normal intake when you already have a long chat, document, transcript, research dump, strategy note, or mixed notes.

Ask Codex:

> Import this existing material and turn it into an idea project.

Codex should:

1. Create the control files if they do not exist.
2. Create only the import files:
   - `00-import/source-material.md`
   - `00-import/import-summary.md`
3. Preserve the original material or a faithful summary of it.
4. Extract candidate ideas, facts, assumptions, guesses, opinions, preferences, rejected alternatives, open questions, and candidate decisions.
5. Ask you to confirm the main idea and any candidate decisions.
6. Route into `idea-intake` or `problem-definition`.

Old chat conclusions are not automatically decisions. They become decisions only after you confirm them.

## Continue An Existing Idea Project

Ask Codex to:

1. Read `00-control/current-state.md`.
2. Read `00-control/open-questions.md` only when blocked, skipped, or unclear.
3. Identify the current phase and blocked items.
4. Continue the next recommended phase unless you request a manual jump.

Codex should not read examples, templates, future phase folders, or every rule file unless the current task needs them.

## Clean Handoff Mode

Use Clean Handoff Mode when you want each phase to start with fresh context, possibly on a different agent or model.

The pattern is:

`Skill/Agent 1 -> writes Markdown files and handoff -> context clears -> Skill/Agent 2 reads the handoff and minimum files -> continues`

Ask Codex:

> Use Clean Handoff Mode for this project.

Codex should then create or update `00-control/handoff.md` after each phase.

Best use cases for Clean Handoff Mode:

- `idea-import`: when the source chat or document is long.
- `research-evidence`: when evidence quality matters or research is broad.
- `strategy`: when target, positioning, distribution, or model choices are strategic.
- `mvp-experiments`: when comparing several experiment paths.
- `review-pivot`: when deciding whether to continue, pivot, pause, or stop.

Less useful for Clean Handoff Mode:

- `idea-intake`: usually small enough to run inline.
- `execution-tracking`: often better as quick incremental updates.
- Tiny personal projects or low-risk internal notes.

Model assignment idea:

| Skill | Suggested Model Type |
| --- | --- |
| `idea-orchestrator` | Fast general model |
| `idea-import` | Strong summarization model for long source material |
| `idea-intake` | Fast general model |
| `problem-definition` | General or stronger reasoning model |
| `research-evidence` | Strong research/reasoning model |
| `assumptions-risks` | Strong reasoning model |
| `vision-direction` | Strong reasoning model |
| `principles-constraints` | General reasoning model |
| `strategy` | Strong strategy/reasoning model |
| `mvp-experiments` | Strong reasoning and option-generation model |
| `decision-roadmap` | General reasoning model |
| `execution-tracking` | Fast general model |
| `review-pivot` | Strong reasoning model |

Use `Parallel Support` only for independent research branches, competitor scans, or option generation. One agent should integrate the results into the project files.

## Run One Phase

Ask Codex to run a specific phase, for example:

> Run the research evidence phase for this idea.

Codex should:

1. Read `00-control/current-state.md`.
2. Use the matching skill from `.agents/skills/`.
3. Create only that phase's required folder and files if they are missing.
4. Read the phase input files that exist.
5. Ask only the necessary questions.
6. Update the phase output files.
7. Log decisions and risks.
8. Update `00-control/current-state.md`.

## Skip With Risk Logging

You may skip a phase, question, or artifact. Codex must log:

- What was skipped
- Why it was skipped
- The risk created
- Who accepted the risk
- When to revisit it

Use `framework/rules/blocking-and-skipping.md` for the required format.

Skipping does not require creating the skipped phase folder. Record the risk in `00-control/current-state.md` and `00-control/open-questions.md` unless a more specific file already exists.

## Review Or Pivot

Use phase `11-review-pivot` when:

- New evidence contradicts the current direction.
- An experiment finishes.
- Progress stalls.
- Strategy, MVP, or target user needs to change.

Pivots are decisions. Record them in both `11-review/pivot-decisions.md` and `00-control/decision-log.md`.

## Repository Contents

- `framework/phases/`: phase-by-phase process guidance.
- `framework/rules/`: cross-phase rules for evidence, decisions, files, transitions, blocking, and skipping.
- `framework/index.md`: compact routing index for context-efficient navigation.
- `templates/project/`: reference file patterns for progressive creation; do not copy all files up front.
- `.agents/skills/`: Codex skills for orchestrating and running phases.
- `examples/cozyinn-demo/`: a short fictional example project.
