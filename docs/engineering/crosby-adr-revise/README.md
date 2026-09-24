# Revise ADR

## Purpose

Use this skill to revise an existing ADR from review comments, stakeholder feedback, or new context. Keep the decision and local format intact.

## When to use it

Use it when:

- an ADR has been reviewed and needs clarification or corrections,
- feedback exposes missing rationale, consequences, or next steps,
- the decision is still valid but the wording or evidence needs tightening,
- or the user wants a structured plan before making changes to the ADR.

## When not to use it

Do not use it for:

- creating a brand-new ADR; use the `crosby-adr-create` skill instead,
- making implementation work outside the ADR document,
- broad rewriting without a clear source of feedback,
- or changing the decision itself without explicit user approval.

## Workflow

1. Read the existing ADR and gather the review feedback.
2. Identify the relevant sections and classify the issues.
3. Draft a concrete revision plan tied to the feedback and ADR sections.
4. Ask for direction if the feedback changes the decision or leaves scope unclear.
5. Apply the requested revision. Return a plan without editing when the user asked only for a plan.
6. Verify the ADR remains coherent, evidence-based, and consistent with the decision.
7. Summarize what changed and any remaining follow-up items.

## Required outputs

A strong ADR revision workflow includes:

- a summary of the concerns raised,
- a reviewable plan that maps feedback to sections,
- a question only when a material decision remains unresolved,
- a final ADR update with a brief summary of changes.

## Good practice

- Keep the scope tight: fix only what the feedback actually requires.
- Separate wording fixes from substantive decision changes.
- Preserve the ADR structure unless a broader change is explicitly requested.
- Capture assumptions and unresolved questions instead of inventing details.

## Common pitfalls

- Changing the ADR's decision without approval.
- Broadening the scope beyond reviewer feedback.
- Changing the decision outcome without approval.
- Inventing references, dates, or tickets that were not provided.
- Leaving the ADR internally inconsistent after the update.
