---
name: audit-repo
description: 'Perform a Principal-level audit of a feature or directory. Use when identifying architectural anti-patterns, memory leaks, or performance bottlenecks in a JS/TS codebase, or verifying compliance with project-context.md.'
argument-hint: '<feature or directory to audit>'
---

# SKILL: audit-repo

## When to Use

- Auditing a specific feature or directory in a JS/TS codebase
- Identifying architectural anti-patterns or performance issues
- Verifying compliance with `project-context.md` rules

## Procedure

Using the full context of this repository, perform a Principal-level audit of **[Feature/Directory]**:

1. Identify architectural anti-patterns.
2. Flag potential memory leaks or performance bottlenecks in the JS/TS code.
3. Verify compliance with the Project Context (`project-context.md`).

## Output Format

Markdown table of findings:

| File / Location | Issue | Severity                            | Proposed Fix |
| --------------- | ----- | ----------------------------------- | ------------ |
| `path/to/file`  | ...   | Critical / Major / Moderate / Minor | ...          |
