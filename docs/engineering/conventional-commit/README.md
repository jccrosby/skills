# Conventional commit

## Purpose

This skill helps produce a commit message that is clear, machine-readable, and consistent with conventional commit conventions.

## When to use it

Use it:

- after staging changes,
- before committing,
- when you want a clean, parseable history.

## Workflow

1. Review the git diff or staged changes.
2. Choose the most appropriate type: feat, fix, docs, style, refactor, perf, test, chore, build, or ci.
3. Write a short imperative subject line.
4. Add a brief body that explains the motivation and impact.
5. Keep the message atomic and avoid filler.

## Commit structure

```text
<type>(<scope>): <subject>

<body>

[Footer: e.g., JIRA-123]
```

## Guidance

- Prefer imperative verbs such as “add”, “fix”, or “refactor”.
- Keep the subject short and specific.
- Explain the “what” and “why”, not the implementation details.
- If the diff covers multiple unrelated concerns, flag that the commit should be split.

## Common pitfalls

- Writing vague subjects like “update stuff”.
- Mixing unrelated logic in a single commit.
- Adding filler phrases such as “In this commit...” or “I have updated...”.

## Output expectations

Return the final commit message in a single copy-paste block, ready to use in git.
