---
name: adr-revise
description: 'Revise an existing ADR from review feedback by creating a change plan, letting the user review and edit it, and then applying the approved updates to the ADR.'
argument-hint: '<adr path> [--feedback "<review notes>"]'
---

# SKILL: adr-revise

## When to Use

- There is an existing ADR that requires changes after review, discussion, or stakeholder feedback.
- Feedback raises issues around clarity, missing trade-offs, weak rationale, outdated context, or incomplete next steps.
- The user wants a structured plan before editing the ADR itself.
- The user says "revise the ADR", "update this ADR", or "address reviewer feedback".

## When NOT to Use

- Creating a new ADR from scratch; use `adr-create` instead.
- Rewriting large sections without a clear source of review feedback.
- Making implementation changes outside the ADR document itself.
- Changing the decision outcome without explicit approval from the user.

## Inputs to Gather

Before proposing edits, collect:

1. **ADR path** — the exact ADR file to update.
2. **Feedback source** — review comments, issue threads, notes, or a pasted summary of concerns.
3. **Decision context** — whether the ADR is still the same decision or should be re-scoped.
4. **Edit boundaries** — whether the user wants only the ADR text updated, or also references / next steps / consequences.

If the feedback is vague, ask for a concise list of problems and the intended outcome.

## Procedure

1. **Read the ADR in full** and identify the relevant sections affected by the feedback.
2. **Classify the feedback** into one or more buckets:
   - clarification / wording
   - missing context
   - missing trade-offs or consequences
   - weak rationale or unsupported claims
   - stale references or next steps
   - decision / status changes
3. **Draft a concrete revision plan** with the smallest change set that addresses the feedback.
   - For each item, state the issue, the section to update, and the proposed change.
   - Keep the plan action-oriented and reviewable.
4. **Pause for human review** before editing the ADR.
   - Present the plan to the user and ask for edits or approval.
   - The user may remove items, refine wording, add scope, or request a different sequencing.
5. **Apply only the agreed plan**.
   - Update the ADR in place.
   - Preserve the existing ADR structure unless the user explicitly wants a broader rewrite.
   - Keep the content factual and evidence-based.
6. **Check the final ADR** for consistency with the decision and reviewer feedback.
   - Ensure the ADR still explains the context, decision, rationale, trade-offs, and next steps clearly.
7. **Report back** with a short summary of what changed and any unresolved questions.

## Required Output

The skill should always do the following in order:

1. Summarize the ADR issues and the likely affected sections.
2. Propose a revision plan in a format the user can review and edit.
3. Wait for user feedback on the plan.
4. After approval, update the ADR directly.
5. Provide a brief final summary showing what changed.

## Suggested Plan Format

Use a reviewable structure like this:

```markdown
## ADR Revision Plan

### Goal

Summarize the intended outcome of the change in one sentence.

### Planned Changes

1. **Issue:** Clarify the context around X.
   **Section:** Context
   **Action:** Add a short explanation of Y and remove unsupported claims.

2. **Issue:** Strengthen the rationale for the decision.
   **Section:** Rationale
   **Action:** Add evidence from Z and explain why Option A is preferred.

3. **Issue:** Update consequences and next steps.
   **Section:** Consequences / Next Steps
   **Action:** Add the expected cost and assign ownership for follow-up work.

### Out of Scope

- Items not addressed by the current feedback.

### Review Notes

- Any assumptions or open questions needing user input.
```

## Decision Rules

- Prefer the smallest change set that resolves the feedback.
- Do not silently broaden scope beyond the ADR or the review comments.
- Do not invent references, tickets, or dates unless the user supplies them.
- If the feedback contradicts the current ADR decision, call that out explicitly and ask for direction before changing the decision itself.
- If the ADR has become stale or inconsistent, note the risk and propose a targeted update rather than a full rewrite.

## Quality Checklist

Before finalizing the ADR revision, verify:

- [ ] The plan clearly maps feedback to specific ADR sections.
- [ ] The user had a chance to review and edit the plan before any ADR changes were made.
- [ ] The changes are limited to the agreed scope.
- [ ] The ADR still reads as a coherent decision record.
- [ ] Rationale, consequences, and next steps are updated consistently.
- [ ] The final text contains no unsupported claims or invented references.
- [ ] The summary explains the change clearly and calls out any unresolved questions.

## Output Format

After reading the ADR and feedback, present:

### 🧭 Revision Plan

- The plan as a reviewable markdown block.

### ✅ Review Instructions

- Ask the user to approve, revise, or expand the plan.

Then, after approval:

### ✏️ ADR Updated

- Brief summary of the exact sections changed.
- Mention the ADR file path.
- Note any remaining items for follow-up.

---

**Constraint:** Do not change the ADR until the user has reviewed and approved the revision plan. The plan is the checkpoint; the ADR update is only the execution step after approval.
