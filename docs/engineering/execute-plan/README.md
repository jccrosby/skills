# Execute plan

## Purpose

Use this skill to carry out a single step from an implementation plan while keeping the work narrow, testable, and reviewable.

## When to use it

Use it when:

- you have a plan with defined steps,
- the task is large enough to need sequencing,
- or you need to maintain a disciplined human-review loop.

## Core workflow

1. Locate the plan and confirm the current step.
2. Ensure previous steps are marked complete.
3. Implement only the minimum logic for the current step.
4. Prefer tests and a small change set.
5. Summarize the work and ask for review.
6. Only continue after approval.

## Mandatory review gate

This skill explicitly requires a human review checkpoint before moving to the next step. The agent should stop and ask the user to review the implementation before proceeding.

## Good practice

- Keep changes atomic.
- Avoid unrelated fixes or refactors.
- Keep each step small enough to reason about quickly.
- Use the commit message workflow when the step is approved.

## Common pitfalls

- Scope creep into nearby issues.
- Making a single step too large.
- Skipping the user review loop.
- Over-engineering before the minimum viable path is proven.
