# Evaluate an idea with Proven-Better-New

Use this skill to evaluate an app, tool, or project before investing in implementation.
It researches alternatives, examines proposed improvements, and identifies assumptions worth testing.

The [skill instructions](../../../skills/productivity/crosby-proven-better-new/SKILL.md) define the workflow.
The framework adapts Mark Pincus's [Proven-Better-New approach](https://www.lifeatthespeedofplay.com/).
It provides a way to organize evidence, not a formula for predicting success.

## When to use it

Choose this skill when you want to assess an idea's value, differentiation, feasibility, or unresolved assumptions.
It supports personal tools, internal projects, open-source projects, and commercial apps.
It does not produce an implementation roadmap.

## Supply useful context

Describe the idea, intended user, current workaround, desired outcome, and main constraints.
Include existing research or usage evidence when available.
An incomplete idea still works.
The skill states assumptions and asks only a question that could change the evaluation.

Web access enables current research.
Without it, the skill returns a provisional assessment and identifies claims that remain unverified.

## Example invocations

### Personal tool

```text
Use crosby-proven-better-new to evaluate a tool that combines my household maintenance reminders.
I currently use a spreadsheet and calendar.
My goal is less weekly administration, with minimal maintenance and no paid hosting.
```

### Internal project

```text
Use crosby-proven-better-new to evaluate a release checklist tool for our web team.
We currently coordinate through issue comments and chat.
Evaluate adoption, integration, and ongoing ownership before suggesting any build work.
```

### Commercial app

```text
Use crosby-proven-better-new to evaluate an app that helps independent tutors manage cancellations.
Compare existing products and manual workarounds.
Give a conditional recommendation and identify the smallest useful demand test.
```

## Read the evaluation

The report explains the intended benefit and compares the idea with relevant alternatives.
It groups findings under Proven, Better, and New while keeping evidence strength separate.

- Proven identifies existing patterns and checks evidence that they work in a comparable setting.
- Better examines a proposed improvement, including tradeoffs and switching effort.
- New identifies unsupported assumptions and explains what depends on them.

The report also covers practical constraints, failed alternatives where documented, and tests for important unknowns.
It prioritizes reasons to pursue or reconsider the idea.
Ask for a recommendation when you want explicit advice.

Market research does not prove that people will use your solution.
Treat proposed tests as ways to gather evidence, with limits on what each result establishes.
The skill suggests experiments; it does not authorize outreach, purchases, or execution.

## Choose a related skill

Use [crosby-prompt-create](../crosby-prompt-create/README.md) when you need to improve a prompt rather than evaluate a project.
After choosing to build, use [crosby-plan-iterative](../../engineering/crosby-plan-iterative/README.md) to plan implementation.
