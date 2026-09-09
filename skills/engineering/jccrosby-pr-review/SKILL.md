---
name: pr-review
description: 'Generate a structured PR review outline comparing two branches. Use when reviewing a pull request for KISS compliance, context alignment, evidence of safety, and standard code quality metrics. Does not write PR comments — produces a structured report for the human reviewer.'
argument-hint: '<source-branch> vs <target-branch>'
---

# SKILL: pr-review

## When to Use

- Reviewing a pull request before merging
- Generating structured, tiered feedback across risk levels
- Checking compliance with `project-context.md` rules if the file exists

## Procedure

1. Identify `<SOURCE_BRANCH>` and `<TARGET_BRANCH>`.
   1. If branches are not provided, run git branch --show-current to identify the source and assume main or develop as the target.
2. Diff the branches and load the changed files.
3. Apply the review criteria below.
4. Output the report in the format below. Do **not** write PR comments directly.

## Review Criteria

1. **Limit Scope** - Only focus on the changes and affected code and tests.
2. **The KISS Check** — Is this the simplest possible solution? Flag premature abstractions or over-engineering.
3. **Context Alignment** — Does the change follow the rules in `project-context.md`?
4. **Evidence Over Explanation** — Flag high-risk areas (Auth, State, Data) that lack tests or safety evidence.
5. **Standard Metrics** — DRY, SOLID, YAGNI, and performance bottlenecks.

## Output Format

**CRITICAL:** Format output in a way that is easy to identify where/which file and copy/paste the feedback into the existing PR in github.

### 1. High-Level Summary

1. 2–3 sentences on the intent and overall risk of the changes.
2. For each issue raised provide file paths and line numbers and suggestions to improve or questions to ask

### 2. Action Required — High Priority

- **[Severity: Critical/Major]** Security, correctness, or architectural violations that should block merge.

### 3. Recommended — Medium Priority

- **[Severity: Moderate]** Improvements for maintainability or performance that are not merge-blocking.

### 4. Minor Suggestions — Low Priority

- Nits, future refactors, and "if you touch this again" items.
