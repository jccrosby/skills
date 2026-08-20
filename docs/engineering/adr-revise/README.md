# Revise ADR

## Purpose

Use this skill when an existing ADR needs to be adjusted in response to review comments, stakeholder feedback, or newly discovered context. The goal is to turn feedback into a focused, reviewable change plan and then apply only the approved updates to the ADR.

## When to use it

Use it when:

- an ADR has been reviewed and needs clarification or corrections,
- feedback exposes missing rationale, consequences, or next steps,
- the decision is still valid but the wording or evidence needs tightening,
- or the user wants a structured plan before making changes to the ADR.

## When not to use it

Do not use it for:

- creating a brand-new ADR; use the `adr-create` skill instead,
- making implementation work outside the ADR document,
- broad rewriting without a clear source of feedback,
- or changing the decision itself without explicit user approval.

## Workflow

1. Read the existing ADR and gather the review feedback.
2. Identify the relevant sections and classify the issues.
3. Draft a concrete revision plan tied to the feedback and ADR sections.
4. Present the plan for user review and editing.
5. Apply only the approved changes to the ADR.
6. Verify the ADR remains coherent, evidence-based, and consistent with the decision.
7. Summarize what changed and any remaining follow-up items.

## Required outputs

A strong ADR revision workflow includes:

- a summary of the concerns raised,
- a reviewable plan that maps feedback to sections,
- a human approval checkpoint before editing,
- a final ADR update with a brief summary of changes.

## Good practice

- Keep the scope tight: fix only what the feedback actually requires.
- Separate wording fixes from substantive decision changes.
- Preserve the ADR structure unless a broader change is explicitly requested.
- Capture assumptions and unresolved questions instead of inventing details.

## Common pitfalls

- Editing the ADR before the user has reviewed the plan.
- Broadening the scope beyond reviewer feedback.
- Changing the decision outcome without approval.
- Inventing references, dates, or tickets that were not provided.
- Leaving the ADR internally inconsistent after the update.
