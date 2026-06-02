# Codex Idea Development Framework

This repository is a Codex-first framework for developing an idea from a raw note into a researched direction, principles, strategy, MVP or experiment options, decisions, execution tracking, and review loops.

The framework is intentionally Markdown-based. Chat is useful for discussion, but Markdown files are the durable project memory.

## Source of Truth

- The source of truth is the project Markdown files, not chat memory.
- New idea projects use progressive file creation by default.
- Do not copy or create the full project folder tree up front.
- At startup, create only the project folder and the control files needed to begin.
- Phase folders and files are created just in time when their phase starts or when a file is actually needed.
- If the user starts from an existing chat, document, transcript, or notes dump, use `idea-o-00-import` before normal intake.
- Import work uses `00-import/import-summary.md` as the fidelity and summary record.
- Create `00-import/source-material.md` only for verbatim/local preservation or useful source pointers.
- Import work must choose and record one fidelity mode: `Verbatim Preservation`, `Structured Faithful Summary`, or `Decision-Focused Summary`, including why it was chosen, what was preserved, what was omitted, remaining risk, and source pointer when exact wording may matter.
- Protect context: follow `framework/rules/context-efficiency.md`.
- Persist until phase outputs are written or consciously skipped: follow `framework/rules/persistence-and-completion.md`.
- Use `framework/rules/challenge-pass.md` in research, assumptions/risks, MVP, roadmap, and review phases.
- Use Clean Handoff Mode from `framework/rules/clean-handoff.md` when the user requests separate agents/models, clean context, or phase handoffs.
- Resolve framework rule paths from the project workspace first. If a project-local `framework/rules/...` file is missing, use the installed IDEA-O skill/framework copy instead; missing project-local rules are not a phase failure.
- Use `framework/index.md` for routing when the next skill is unclear.
- Every important decision must be written to `00-control/decision-log.md`.
- Every phase must begin by reading `00-control/current-state.md`.
- Every phase must end by updating `00-control/current-state.md` as a compact dashboard, not a long history file.
- `current-state.md` must show current phase/status, active decisions, blocking questions, recently changed files, next recommended skill, and next action. Move long narrative history into phase files or `00-control/project-history.md` only when needed.
- Optional UX and other custom artifacts must be indexed in `current-state.md` with purpose, status, owner, and next use so they do not become invisible.
- Important unresolved questions must be written to `00-control/open-questions.md` under the right triage section.
- Rejected ideas, rejected MVPs, and abandoned alternatives must be preserved in `09-roadmap/rejected-options.md` or the most relevant phase file.
- Do not delete rejected alternatives. Mark them as rejected, superseded, paused, or archived.
- Keep Markdown concise but complete. Prefer clear bullets, dated entries, and tables over long essays.
- When the user asks a direct reasoning, process, or product question, answer first. Update Markdown only if the answer changes a decision, risk, evidence item, assumption, open question, rejected alternative, artifact index, current focus, or next action. If no durable update is needed, say no file update was required.

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

- Use `idea-o` to choose the current phase and maintain process flow.
- Normal sequence: `idea-o-01-intake` -> `idea-o-02-problem` -> `idea-o-03-research` -> `idea-o-04-risks` -> `idea-o-05-vision` -> `idea-o-06-principles` -> `idea-o-07-strategy` -> `idea-o-08-mvp` -> `idea-o-09-roadmap` -> `idea-o-10-execution` -> `idea-o-11-review`.
- Optional Phase 10 prep sequence: `idea-o-10-implementation-spec` -> `idea-o-10-execution-rules` -> `idea-o-10-execution`.
- Use `idea-o-10-implementation-spec` when execution needs implementation-ready requirements, acceptance criteria, or verification before build work starts.
- Use `idea-o-10-execution-rules` when AI agents will execute implementation work and need boundaries, permissions, checkpoints, stop conditions, or handoff rules.
- Use `idea-o-10-execution-evidence` when build, test, debug, launch, user feedback, or implementation work creates evidence that should update project memory without forcing a full review phase.
- Use `idea-o-publish` when an idea project or sub-idea track is ready to be branched, staged, committed, pushed, or opened as a pull request.
- Phase 10 implementation specs must include non-goals, forbidden assumptions, verification expectations, and Spec Kit compatible prompt output when a Spec Kit handoff is intended.
- Do not let implementation agents assume product, architecture, permission, execution-mode, or verification decisions. Ask the user and log unresolved forks.
- Use `idea-o-00-import` before `idea-o-01-intake` when the user provides substantial existing material to organize.
- During import, use `framework/rules/import-fidelity.md`; old chat conclusions remain candidate decisions until confirmed.
- Use one phase skill at a time for normal work.
- Do not jump phases unless the user explicitly requests it.
- If the user requests a jump, record the jump and its risk in `00-control/current-state.md`.
- Before starting any phase, read `00-control/current-state.md`.
- For sub-idea tracks, create only control files and `00-control/track-context.md`; record parent project, track purpose, parent context files, local decisions, promoted decisions, and naming/publishing expectations.
- Before working, identify what the user already completed, skipped, or left blocked.
- After finishing any phase, update `00-control/current-state.md`.
- Do not mark a phase complete until required outputs are written or the user consciously accepts logged skip risk.
- When starting a phase, create only the folders and files required by that phase if they are missing.
- Do not load examples, templates, future phase files, or all rules unless needed.
- If Clean Handoff Mode is active, every skill must update `00-control/handoff.md` before the next skill starts.
- Before marking a phase complete, apply `framework/rules/phase-quality-gates.md`.

## Blocking And Skipping

- A phase may be blocked when key information is missing.
- Blocking questions go in `00-control/open-questions.md`.
- Skipping is allowed only when the user accepts the risk.
- Every skip must log the skipped item, reason, risk, owner, date, and revisit trigger.
- Skipping research does not remove the research requirement; it only defers or narrows it.
- Assumption-led research narrows research to high-risk, decision-relevant assumptions; it does not delete the mandatory market scan or evidence labeling.
- Skipping a phase does not require creating that phase's folder. Log the skip in control files unless the phase file already exists.

## Decisions

Log decisions immediately when they become meaningful.

Imported conclusions from prior chats or documents are not decisions until the user confirms them. Record them as candidate decisions in `00-import/import-summary.md` or as open questions.

Each decision must include:

- Date
- Status: Active | Superseded | Rejected | Deferred | Archived
- Decision
- Classification: `Decision`
- Context
- Options considered
- Evidence used
- Tradeoffs
- Consequences
- Supersedes / Superseded by, when relevant
- Revisit trigger

Keep an active-decision summary near the top of `00-control/decision-log.md`. Superseded decisions must link to their replacement instead of being deleted.

## Research

Research is mandatory for every idea project, but depth depends on the idea.

- Lightweight personal project: basic desk research and comparable examples.
- Business, product, or service: user, market, competitor, distribution, and risk research.
- Regulated, financial, medical, legal, or safety-sensitive idea: deeper research and explicit uncertainty.
- Assumption-led mode: choose high-risk assumptions, do decision-relevant research, log deferred research risk, and define the smallest validation step while still completing a market scan.

## Execution

Execution means tracking progress and next actions. It does not always mean building software.

The framework should always look for the smallest useful next experiment before committing to a large plan.
