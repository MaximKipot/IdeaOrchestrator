# Codex Idea Development Framework

This repository is a Codex-first framework for developing an idea from a raw note into a researched direction, principles, strategy, MVP or experiment options, decisions, execution tracking, and review loops.

The framework is intentionally Markdown-based. Chat is useful for discussion, but Markdown files are the durable project memory.

## Source of Truth

- The source of truth is the project Markdown files, not chat memory.
- New idea projects use progressive file creation by default.
- Do not copy or create the full project folder tree up front.
- At startup, create only the project folder and the control files needed to begin.
- Phase folders and files are created just in time when their phase starts or when a file is actually needed.
- If the user starts from an existing chat, document, transcript, or notes dump, use `idea-import` before normal intake.
- Import work may create `00-import/source-material.md` and `00-import/import-summary.md`, but only when source material exists.
- Every important decision must be written to `00-control/decision-log.md`.
- Every phase must begin by reading `00-control/current-state.md`.
- Every phase must end by updating `00-control/current-state.md`.
- Important unresolved questions must be written to `00-control/open-questions.md`.
- Rejected ideas, rejected MVPs, and abandoned alternatives must be preserved in `09-roadmap/rejected-options.md` or the most relevant phase file.
- Do not delete rejected alternatives. Mark them as rejected, superseded, paused, or archived.
- Keep Markdown concise but complete. Prefer clear bullets, dated entries, and tables over long essays.

## Evidence Language

Use explicit labels whenever recording claims:

- `Fact`: verified from a reliable source or direct user statement.
- `Assumption`: treated as true for planning, but not yet verified.
- `Guess`: weak belief based on limited information.
- `Opinion`: subjective judgment from the AI, user, or stakeholder.
- `Preference`: chosen taste, constraint, or working style.
- `Decision`: explicit choice that changes the project direction.

Do not blur these labels. If a claim is uncertain, label it as uncertain.

## Mandatory Skill Usage

Codex must use the relevant skill from `.agents/skills/` for each phase.

- Use `idea-orchestrator` to choose the current phase and maintain process flow.
- Use `idea-import` before `idea-intake` when the user provides substantial existing material to organize.
- Use one phase skill at a time for normal work.
- Do not jump phases unless the user explicitly requests it.
- If the user requests a jump, record the jump and its risk in `00-control/current-state.md`.
- Before starting any phase, read `00-control/current-state.md`.
- After finishing any phase, update `00-control/current-state.md`.
- When starting a phase, create only the folders and files required by that phase if they are missing.

## Blocking And Skipping

- A phase may be blocked when key information is missing.
- Blocking questions go in `00-control/open-questions.md`.
- Skipping is allowed only when the user accepts the risk.
- Every skip must log the skipped item, reason, risk, owner, date, and revisit trigger.
- Skipping research does not remove the research requirement; it only defers or narrows it.
- Skipping a phase does not require creating that phase's folder. Log the skip in control files unless the phase file already exists.

## Decisions

Log decisions immediately when they become meaningful.

Imported conclusions from prior chats or documents are not decisions until the user confirms them. Record them as candidate decisions in `00-import/import-summary.md` or as open questions.

Each decision must include:

- Date
- Decision
- Classification: `Decision`
- Context
- Options considered
- Evidence used
- Tradeoffs
- Consequences
- Revisit trigger

## Research

Research is mandatory for every idea project, but depth depends on the idea.

- Lightweight personal project: basic desk research and comparable examples.
- Business, product, or service: user, market, competitor, distribution, and risk research.
- Regulated, financial, medical, legal, or safety-sensitive idea: deeper research and explicit uncertainty.

## Execution

Execution means tracking progress and next actions. It does not always mean building software.

The framework should always look for the smallest useful next experiment before committing to a large plan.
