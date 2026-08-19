---
name: micro-audit
description: 'High-density logic audit on a single file. Use when checking for KISS violations, logic gaps, DRY/YAGNI issues, or unintended side effects. Standards sourced from global-identity.md.'
argument-hint: '<file to audit>'
---

# SKILL: micro-audit

## When to Use

- Auditing a single file for logic correctness
- Checking for KISS violations or over-engineering
- Reviewing for missing edge cases or unintended side effects

## Checklist

1. **KISS Violations** — Is there a simpler native JS/TS solution? Is this change 'over-solving' for a future requirement? If so, recommend stripping the logic back to the immediate use case.
2. **Logic Gaps** — Check for edge cases, missing error boundaries, or improper type guards.
3. **DRY/YAGNI** — Is this file solving a problem that doesn't exist yet?
4. **Side Effects** — Are functions as pure as possible? Are side effects clearly isolated?

## Output Format

Provide a concise, unornamented list:

- **Fixes Needed** — Logic bugs and correctness issues.
- **KISS Refactors** — Simpler alternatives for over-complex code.

No praise. Findings only.
