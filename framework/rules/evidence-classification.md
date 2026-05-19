# Evidence Classification Rules

Use classification labels every time the project records a claim that affects direction, risk, strategy, or execution.

## Labels

| Label | Meaning | Example |
| --- | --- | --- |
| `Fact` | Verified source, direct observation, or explicit user statement. | Three interviewees said onboarding is confusing. |
| `Assumption` | Planning belief accepted temporarily. | Hosts will reply to guest feedback requests. |
| `Guess` | Weak belief with little support. | Families may prefer SMS over email. |
| `Opinion` | Subjective judgment. | The concept feels more credible as a service than an app. |
| `Preference` | Chosen taste, constraint, or working style. | Prefer no-code tools for the first experiment. |
| `Decision` | Explicit choice that changes direction. | Start with concierge testing before software. |

## Rules

- Use the weakest honest label.
- Do not upgrade assumptions into facts without evidence.
- Link facts to `03-research/source-list.md`, interview notes, or user-provided statements.
- Convert important assumptions into tests in `08-mvp-experiments/experiment-design.md`.
- Record decisions in `00-control/decision-log.md`.

