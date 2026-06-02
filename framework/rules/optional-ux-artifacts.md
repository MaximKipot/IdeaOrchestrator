# Optional UX Artifacts

Create UX artifacts just in time when product, MVP, onboarding, permission, copy, or interaction choices need durable detail. They are optional and phase-local; do not create a separate UX track or all UX files up front.

## Optional Files

- `screen-map.md`: screens, states, entry points, exits, and unresolved screen questions.
- `copy-decisions.md`: confirmed copy, rejected copy, tone rules, and copy risks.
- `interaction-rules.md`: mode behavior, allowed actions, blocked actions, feedback, and edge cases.
- `permission-experience.md`: permission prompts, user benefit, fallback behavior, privacy concerns, and recovery paths.

Create the file in the phase folder where the decision is being made, such as `05-vision-direction/`, `07-strategy/`, `08-mvp-experiments/`, or `10-execution/`.

## When To Create

- A user-visible flow cannot be understood from strategy or MVP files alone.
- Copy wording changes the product promise, trust, safety, or conversion risk.
- Modes, states, permissions, or fallbacks need behavior rules before implementation.
- A custom UX file would prevent implementation agents from inventing user-visible decisions.

## Indexing

When creating any optional UX or custom artifact, add it to the `00-control/current-state.md` custom artifact index with purpose, status, owner, and next use.

If a UX artifact creates or changes a decision, update `00-control/decision-log.md`. If it creates a blocker, update `00-control/open-questions.md`.
