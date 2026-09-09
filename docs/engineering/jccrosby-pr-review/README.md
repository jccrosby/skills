# PR review

## Purpose

This skill generates a structured review of a pull request, with attention to scope, simplicity, context alignment, and risk.

## When to use it

Use it when:

- you need to review a branch before merge,
- you want a structured framework for feedback,
- or you want to flag risk without posting direct PR comments.

## Workflow

1. Identify source and target branches.
2. Diff the changes.
3. Review scope, simplicity, project alignment, and evidence of safety.
4. Sort findings by severity and priority.
5. Return the review in a readable report format.

## Review criteria

Check for:

- limit of scope,
- KISS and over-engineering issues,
- alignment with repo or project context,
- missing evidence or tests around risky code,
- and standard maintainability concerns.

## Output structure

Return a report with:

1. High-level summary
2. Action required: high priority
3. Recommended: medium priority
4. Minor suggestions: low priority

## Good practice

- Prefer concrete findings with file paths and suggested improvements.
- Focus on risk and correctness first.
- Separate blocking issues from optional improvements.

## Common pitfalls

- Reviewing style instead of behavior.
- Missing test gaps in sensitive areas.
- Treating every suggestion as equal priority.
