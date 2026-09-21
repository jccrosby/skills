---
name: crosby-audit-repo
description: Audit a feature or directory for correctness, architecture, maintainability, performance, and compliance with repository conventions. Use for a broad code review that spans multiple files; use a focused review for a single file.
---

# Audit a repository area

## When to Use

- Auditing a feature, package, service, or directory across multiple files.
- Identifying architectural, correctness, maintainability, or performance risks.
- Verifying compliance with repository-specific instructions and established patterns.

## Procedure

1. Read the repository instructions and relevant architecture or project-context documents when they exist.
2. Establish the target area's purpose, public boundaries, callers, dependencies, tests, and operational constraints.
3. Trace important data, control, error, and resource-lifecycle paths across the files in scope.
4. Identify issues supported by concrete code evidence. Consider correctness, integration, architecture, security boundaries, performance, resource cleanup, maintainability, and test gaps when relevant.
5. Check repository conventions using the actual language and framework in the target, not assumptions from another stack.
6. Avoid reporting style preferences as defects unless the repository defines them as requirements.

## Output Format

Markdown table of findings:

| File / location | Issue | Evidence | Severity | Smallest useful correction |
| --- | --- | --- | --- | --- |
| `path/to/file` | ... | ... | Critical / Major / Moderate / Minor | ... |

Order findings by severity. Include file and line references when available. If no actionable finding is supported, say so and identify any verification limits. Do not modify code during an audit-only request.
