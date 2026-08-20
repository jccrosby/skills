# Prompt Create

## Purpose

This skill turns a rough request or incomplete prompt into a focused, reusable model prompt. It reviews the request, identifies gaps, recommends a useful persona when appropriate, narrows the scope, and produces a copy-ready draft.

## When to use it

Choose it when:

- a prompt is vague, over-scoped, or internally inconsistent,
- the desired audience or output is unclear,
- you want targeted clarifying questions before drafting,
- or you need help deciding whether a persona adds value.

## Workflow

1. Identify the intended outcome, audience, context, constraints, and output.
2. Review the prompt for ambiguity, conflicts, missing information, and unnecessary scope.
3. Ask only questions that could materially change the result.
4. Recommend a specific persona when it improves the work; otherwise omit it.
5. Reduce the request to one primary outcome and defer optional work.
6. Draft and check a prompt that can be used without the review notes.

## Output

The skill returns a prompt review, clarifying questions when needed, a copy-ready draft prompt, assumptions, and useful follow-up prompts for deferred work.

## Example invocation

"Use the `prompt-create` skill to improve this rough request into a prompt for a senior technical reviewer. Ask only blocking questions, narrow the scope to one outcome, and return a copy-ready draft."
