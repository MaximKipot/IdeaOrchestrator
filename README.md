# Codex Idea Development Framework

A reusable Markdown-first framework for turning raw business or actionable ideas into researched directions, principles, strategy, MVP or experiment options, decisions, next actions, and review loops.

The framework is built for Codex. It keeps the project memory in files so work can continue across sessions without depending on chat history.

It is also context-efficient by default: Codex should read the current state first, then only the files needed for the current phase.

## Skill Sequence

Use `idea-o` as the router. The numbered skills show the normal order in slash search:

| Order | Skill | Purpose |
| --- | --- | --- |
| Optional | `idea-o-00-import` | Import an existing chat, document, transcript, or notes dump. |
| 01 | `idea-o-01-intake` | Capture or sharpen the raw idea. |
| 02 | `idea-o-02-problem` | Define problem, user, context, and current alternatives. |
| 03 | `idea-o-03-research` | Gather and classify evidence, with a founder-assumption, end-user-questionnaire, or mixed research mode. |
| 04 | `idea-o-04-risks` | Sort assumptions, risks, unknowns, and tests. |
| 05 | `idea-o-05-vision` | Define vision, direction, and anti-vision. |
| 06 | `idea-o-06-principles` | Set principles, constraints, and tradeoff rules. |
| 07 | `idea-o-07-strategy` | Define target, value, positioning, model, distribution, and metrics. |
| 08 | `idea-o-08-mvp` | Generate MVP and experiment options. |
| 09 | `idea-o-09-roadmap` | Select a path, preserve rejected options, and plan the roadmap. |
| 10 | `idea-o-10-execution` | Track focus, progress, blockers, and next actions. |
| 11 | `idea-o-11-review` | Review evidence and decide whether to continue, adjust, pivot, pause, or stop. |

## When To Use It

Use this framework for software ideas, businesses, services, internal initiatives, workshops, content projects, physical products, or personal projects.

It works best when an idea is still uncertain and needs structured development before execution.

## Start A New Idea Project

1. Create only one empty project folder for the idea.
2. Open that folder with Codex.
3. Ask Codex to use `.agents/skills/idea-o/SKILL.md`.
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

Use `idea-o-00-import` before normal intake when you already have a long chat, document, transcript, research dump, strategy note, or mixed notes.

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
6. Route into `idea-o-01-intake` or `idea-o-02-problem`.

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

- `idea-o-00-import`: when the source chat or document is long.
- `idea-o-03-research`: when evidence quality matters or research is broad.
- `idea-o-07-strategy`: when target, positioning, distribution, or model choices are strategic.
- `idea-o-08-mvp`: when comparing several experiment paths.
- `idea-o-11-review`: when deciding whether to continue, pivot, pause, or stop.

Less useful for Clean Handoff Mode:

- `idea-o-01-intake`: usually small enough to run inline.
- `idea-o-10-execution`: often better as quick incremental updates.
- Tiny personal projects or low-risk internal notes.

Model assignment idea:

| Skill | Suggested Model Type |
| --- | --- |
| `idea-o` | Fast general model |
| `idea-o-00-import` | Strong summarization model for long source material |
| `idea-o-01-intake` | Fast general model |
| `idea-o-02-problem` | General or stronger reasoning model |
| `idea-o-03-research` | Strong research/reasoning model |
| `idea-o-04-risks` | Strong reasoning model |
| `idea-o-05-vision` | Strong reasoning model |
| `idea-o-06-principles` | General reasoning model |
| `idea-o-07-strategy` | Strong strategy/reasoning model |
| `idea-o-08-mvp` | Strong reasoning and option-generation model |
| `idea-o-09-roadmap` | General reasoning model |
| `idea-o-10-execution` | Fast general model |
| `idea-o-11-review` | Strong reasoning model |

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
8. Apply `framework/rules/phase-quality-gates.md`.
9. Update `00-control/current-state.md`.

In `idea-o-03-research`, Codex should choose or ask for a research mode:

- `Founder Assumption Audit`: test what the founder currently believes.
- `End-User Questionnaire`: create interview or survey questions for target users.
- `Mixed`: use both, usually for product, service, business, and market-facing ideas.

Every research mode must include a market scan for present solutions, substitutes, workarounds, and comparable alternatives.

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
