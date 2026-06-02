# Sub-Idea Tracks

Use a sub-idea track for a focused child question that is substantial enough to need its own idea files but should stay connected to a parent project.

## Progressive Setup

Create only the child project folder, control files, and `00-control/track-context.md`. Do not copy the full template tree or create future phase folders up front.

## Track Context

`00-control/track-context.md` must include:

- Parent project name and path.
- Track purpose.
- Why this is separate from the parent.
- Parent context files the child agent must read.
- Parent decisions that constrain this track.
- Decisions that may stay local.
- Decisions that must be promoted to the parent.
- Naming and publishing expectations.

## Decision Promotion

Keep decisions local when they only affect the child artifact, exploration method, local UX variant, or validation plan.

Promote decisions to the parent when they affect product direction, target user, positioning, principles, roadmap priority, implementation requirements, launch scope, risk posture, or any assumption the parent depends on.

Promoted decisions must be added or linked in the parent `00-control/decision-log.md`. The child track should also note the promotion in its own decision log and current state.

## Naming And Publishing

Use names that preserve the parent relationship, such as `<parent>-idea-<track>` or `<parent>/idea-<track>`, unless the user gives a different convention. Publishing a child track follows `framework/rules/publish-safety.md`.
