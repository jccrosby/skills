# Productivity Skills Index

This category is reserved for productivity-oriented workflows: planning, execution support, personal operations, communication, and lightweight coordination tasks that help a person or agent work more effectively.

This folder includes skills for prompt writing, editing, and idea evaluation.

## How to use this category

A good productivity skill invocation should be:

- specific about the task,
- narrow about the scope,
- explicit about the output expected.

Examples:

- "Use the `planning` skill to break this week into focused execution blocks."
- "Use the `triage` skill to sort this backlog by urgency and payoff."
- "Use the `communication` skill to draft a concise status update for stakeholders."

The key rule is simple: a skill should be used for a repeatable work pattern, not as a generic catch-all for every task.

## Expected skill structure

Each future productivity skill in this folder should include:

- a clear purpose,
- when to use it,
- how to invoke it,
- the form of output it produces,
- any constraints or guardrails.

The most effective pattern is:

1. name the skill,
2. define the subject or task,
3. say what the result should look like,
4. keep the scope narrow and practical.

## Current status

The productivity folder now includes the following skills:

- [crosby-proven-better-new](crosby-proven-better-new/SKILL.md) evaluates app, tool, and project ideas before implementation. It returns researched findings and proposed tests.
- `crosby-prompt-create` — Reviews and refines rough requests into focused, reusable model prompts, including clarification, persona, and scope guidance.
- `crosby-language-simplify` — Simplify a user-provided prompt while preserving its intent, requirements, and technical details.
- `crosby-unslop` — Removes recognizable AI writing patterns while preserving the meaning and intended tone of existing text.

For idea evaluation, use: "Use crosby-proven-better-new to evaluate this tool idea against my current workaround."
See the [usage guide](../../docs/productivity/crosby-proven-better-new/README.md) for examples and expected output.

When a skill is added, it should be summarized here with:

- skill name,
- purpose,
- trigger situations,
- invocation examples,
- expected artifact.

## Recommended invocation pattern

Use the following pattern for future entries:

- "Use the `[skill-name]` skill to [do a specific task]."
- "Apply the `[skill-name]` skill to [project, issue, file, day plan, report, list]."
- "Return a [summary / draft / plan / checklist / brief] for review."

This keeps the workflow predictable for both humans and AI agents and makes the category easier to grow without accidental overlap between skills.
