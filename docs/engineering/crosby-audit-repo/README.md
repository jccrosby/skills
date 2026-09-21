# Audit repository

## Purpose

Use this skill when you need a high-level review of a feature, directory, service, or package across multiple files.

It is designed to surface:

- architectural anti-patterns,
- correctness, performance, or resource-lifecycle concerns,
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
3. Trace important data, control, error, and resource-lifecycle paths.
4. Check whether the implementation aligns with the actual language, framework, project context, and repository rules.
5. Present evidence-backed findings with severity and the smallest useful correction.

## Output format

Use a table like this:

| File / location | Issue | Evidence | Severity | Smallest useful correction |
| --- | --- | --- | --- | --- |
| path/to/file | Example: unnecessary coupling or hot path | Relevant code path or behavior | Critical / Major / Moderate / Minor | Example: simplify the flow or isolate side effects |

## Good practice

- Focus on the actual impact, not just style.
- Separate a real bug from a design concern.
- Be explicit about risk level and why the issue matters.

## Common pitfalls

- Reviewing only the surface area without checking surrounding context.
- Reporting style concerns as architecture issues without evidence.
- Recommending a broad refactor when a small local fix is sufficient.
