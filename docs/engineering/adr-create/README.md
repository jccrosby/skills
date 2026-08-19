# Create ADR

## Purpose

Use this skill to draft an architectural decision record when a project needs to capture a decision that affects more than one team, process, or long-term direction.

## When to use it

Use it when:

- a decision changes architecture or long-term direction,
- a new pattern or technology is being adopted,
- a prior ADR is being superseded,
- or the change needs documentation before broader rollout.

## When not to use it

Do not use it for:

- local or narrow implementation decisions,
- short-lived experiments,
- routine bug fixes,
- or decisions with no cross-team impact.

## Workflow

1. Confirm the decision topic and status.
2. Gather contributors, references, and any superseded ADRs.
3. Draft the ADR in the project’s required structure.
4. Include context, decision, rationale, considered options, consequences, and next steps.
5. Save the draft in a docs/adrs folder and stop after drafting.

## Required ADR sections

A strong ADR includes:

- title and date,
- status,
- contributors,
- context,
- decision,
- rationale,
- options considered,
- consequences,
- next steps,
- references.

## Good practice

- Separate the problem from the proposed solution.
- List trade-offs instead of only benefits.
- Use concrete next steps and owners when possible.
- Leave placeholders explicit instead of inventing details.

## Common pitfalls

- Writing a solution description before explaining the problem.
- Omitting alternatives or trade-offs.
- Inventing contributors, dates, or ticket references.
- Marking an ADR as accepted without review.
