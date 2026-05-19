# Codex Idea Development Framework

A reusable Markdown-first framework for turning raw business or actionable ideas into researched directions, principles, strategy, MVP or experiment options, decisions, next actions, and review loops.

The framework is built for Codex. It keeps the project memory in files so work can continue across sessions without depending on chat history.

## When To Use It

Use this framework for software ideas, businesses, services, internal initiatives, workshops, content projects, physical products, or personal projects.

It works best when an idea is still uncertain and needs structured development before execution.

## Start A New Idea Project

1. Copy `templates/project/` into a new project folder.
2. Open the new project with Codex.
3. Ask Codex to use `.agents/skills/idea-orchestrator/SKILL.md`.
4. Start with `01-idea/idea-brief.md` and `01-idea/raw-notes.md`.
5. Let Codex suggest a depth level, then accept or override it.

Suggested depth levels:

- `Light`: personal, internal, or low-risk idea.
- `Standard`: most business, software, service, or content ideas.
- `Deep`: high-cost, high-risk, regulated, or strategically important idea.

## Continue An Existing Idea Project

Ask Codex to:

1. Read `00-control/current-state.md`.
2. Read `00-control/open-questions.md`.
3. Identify the current phase and blocked items.
4. Continue the next recommended phase unless you request a manual jump.

## Run One Phase

Ask Codex to run a specific phase, for example:

> Run the research evidence phase for this idea.

Codex should:

1. Read `00-control/current-state.md`.
2. Use the matching skill from `.agents/skills/`.
3. Read the phase input files.
4. Ask only the necessary questions.
5. Update the phase output files.
6. Log decisions and risks.
7. Update `00-control/current-state.md`.

## Skip With Risk Logging

You may skip a phase, question, or artifact. Codex must log:

- What was skipped
- Why it was skipped
- The risk created
- Who accepted the risk
- When to revisit it

Use `framework/rules/blocking-and-skipping.md` for the required format.

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
- `templates/project/`: files to copy for a new idea project.
- `.agents/skills/`: Codex skills for orchestrating and running phases.
- `examples/cozyinn-demo/`: a short fictional example project.

