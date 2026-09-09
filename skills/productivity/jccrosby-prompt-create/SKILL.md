---
name: prompt-create
description: 'Create or improve a model prompt from a rough user request. Use when a prompt needs critique, clarifying questions, persona selection, scope reduction, or a structured final draft.'
argument-hint: '<rough prompt or task description>'
---

# Prompt Create

Turn an incomplete or loosely written request into a clear, effective model prompt.
Optimize for a prompt that is specific enough to guide reliable work while remaining small enough to fit the actual task.

## When to Use

- A user has an idea but not a usable prompt.
- An existing prompt is vague, over-scoped, contradictory, or missing constraints.
- The task needs a better-defined audience, role, output, or success criteria.
- The user wants help choosing a persona or deciding whether a persona is useful.

## Procedure

1. **Read the request.** Identify the desired outcome, subject, audience, available context, constraints, and expected output.
2. **Review the prompt.** Point out ambiguity, missing information, unnecessary instructions, conflicting requirements, and assumptions that could cause poor results.
3. **Decide whether clarification is needed.** Ask only questions that could materially change the prompt or its output. Prefer no more than five questions. If the gaps are low-risk, state reasonable assumptions and continue.
4. **Suggest a persona when useful.** Recommend one specific role only when it improves judgment, domain framing, or communication. Explain the role in terms of the task. Do not add decorative or inflated personas.
5. **Narrow the scope.** Split unrelated outcomes, remove optional work, and define boundaries. If the request is too broad, propose a smallest useful version and identify sensible follow-up prompts.
6. **Draft the prompt.** Use direct instructions, concrete inputs, explicit output requirements, and relevant constraints. Preserve the user's intent and terminology.
7. **Check the draft.** Confirm that the prompt has a clear objective, enough context, a defined output, appropriate scope, and no invented facts.
8. **Deliver the result.** Provide the final prompt and briefly note the key decisions, assumptions, and any unresolved questions.

## Clarification Rules

- Ask questions before drafting when the answer would change the task, audience, safety boundary, or output format.
- Do not ask for information that can be safely represented with a placeholder.
- Do not use questions to outsource ordinary prompt-writing judgment to the user.
- When the user asks for an immediate draft, provide a provisional draft if clarification is not blocking and label assumptions clearly.
- Never invent project facts, user preferences, source material, or success measures.

## Persona Guidance

Choose a persona based on the work, not status or theatrics.
Useful personas describe relevant expertise and communication behavior, such as:

- a requirements analyst for ambiguous product requests,
- a senior reviewer for risk and correctness checks,
- a technical writer for audience-focused documentation,
- a teaching assistant for explanations and exercises.

Avoid personas that merely say "expert," "world-class," or "industry-leading" without changing the work.
A prompt can omit a persona when the task is already clear or when a role would add bias without useful guidance.

## Scope Guidance

A good prompt normally has one primary outcome.
When a request contains several outcomes:

1. Identify the primary outcome.
2. Move optional outcomes to a short follow-up list.
3. Separate analysis from execution when mixing them would create uncertainty.
4. Define what is out of scope when that prevents scope creep.

Prefer a smaller prompt that can be evaluated over a comprehensive prompt that tries to solve every adjacent problem.

## Output Format

### Prompt Review

- **Intent:** The outcome the prompt should produce.
- **Issues:** Ambiguities, conflicts, missing context, or unnecessary scope.
- **Persona:** Recommended role, or why no persona is needed.
- **Scope:** What is included and what is deferred.
- **Assumptions:** Facts or decisions made to draft provisionally.

### Clarifying Questions

Include this section only when answers are needed before finalizing the prompt.
Ask concise, decision-oriented questions.

### Draft Prompt

```text
[The complete prompt, ready to copy and use]
```

### Follow-up Prompts

Include only useful deferred work that does not belong in the primary prompt.

## Quality Checks

Before delivering the prompt, verify:

- The primary outcome is stated as an observable result.
- The prompt identifies the relevant audience or user when that affects the response.
- Inputs and source-of-truth material are named or represented with placeholders.
- Output format and level of detail are explicit.
- Constraints are relevant, non-conflicting, and testable.
- The scope fits one coherent task.
- The persona is justified or intentionally omitted.
- Assumptions and unanswered questions are visible.
- No facts, sources, requirements, or capabilities were invented.
- The prompt can be used without reading the review notes first.

## Constraints

- Do not silently change the user's objective.
- Do not add generic prompt boilerplate that does not guide behavior.
- Do not over-specify implementation details when the user only needs an outcome.
- Do not finalize a materially ambiguous prompt without either asking questions or marking it provisional.
- Keep the final prompt concise enough to maintain and reuse.
