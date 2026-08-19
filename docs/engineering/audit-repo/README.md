# Audit repository

## Purpose

Use this skill when you need a high-level review of a feature, directory, or code area in a JavaScript or TypeScript project.

It is designed to surface:

- architectural anti-patterns,
- performance or memory concerns,
- logic gaps,
- and compliance issues with the repo’s project context guidance.

## When to use it

Choose this skill when:

- a feature or directory needs a structural review,
- you suspect the solution is over-engineered,
- a bug may come from deeper architectural drift,
- or you need to verify adherence to project-level standards.

## Workflow

1. Identify the feature or directory to audit.
2. Review the relevant code and surrounding context.
3. Look for architectural misuse, performance bottlenecks, and memory-risk patterns.
4. Check whether the implementation aligns with the project context and repo rules.
5. Present findings as a concise markdown table with severity and recommended fixes.

## Output format

Use a table like this:

| File / Location | Issue | Severity | Proposed Fix |
| --- | --- | --- | --- |
| path/to/file | Example: unnecessary coupling or hot path | Critical / Major / Moderate / Minor | Example: simplify the flow or isolate side effects |

## Good practice

- Focus on the actual impact, not just style.
- Separate a real bug from a design concern.
- Be explicit about risk level and why the issue matters.

## Common pitfalls

- Reviewing only the surface area without checking surrounding context.
- Reporting style concerns as architecture issues without evidence.
- Recommending a broad refactor when a small local fix is sufficient.
