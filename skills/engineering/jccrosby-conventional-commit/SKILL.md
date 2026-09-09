---
name: conventional-commit
description: Generate a Conventional Commit message based on a git diff. Ensures messages are atomic, descriptive, and follow project-specific standards.
argument-hint: '<git diff output or staged files>'
---

# SKILL: conventional-commit

## When to Use

- After staging changes (`git add`) and before committing.
- To maintain a clean, parseable project history.

## Procedure

1. Analyze the provided `git diff`.
2. Categorize the change type: `feat`, `fix`, `docs`, `style`, `refactor`, `perf`, `test`, `chore`.
3. Draft a subject line (max 50 chars) in the imperative mood (e.g., "add", not "added").
4. Provide a body explaining the "What" and "Why" (the motivation), not the "How" (the code speaks for itself).

## Constraints

- **KISS:** If the diff contains multiple unrelated logic changes, warn the user and suggest splitting the commit.
- **No Filler:** Skip phrases like "In this commit..." or "I have updated...".

## Output Format

Provide the commit message in a single code block for easy copying:

```text
<type>(<scope>): <subject>

<body>

[Footer: e.g., <JIRA_BOARD>-<ISSUE_NUMBER>]
```
