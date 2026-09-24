---
name: crosby-audit-micro
description: Review one source file for correctness, unnecessary complexity, and unintended effects. Use for a focused code review rather than a feature-wide audit.
---

# SKILL: crosby-audit-micro

## When to Use

- Auditing a single file for logic correctness
- Checking for KISS violations or over-engineering
- Reviewing for missing edge cases or unintended side effects

## Checklist

1. **KISS Violations** — Is there a simpler approach in the file's language and framework? Does the code solve an unsupported future requirement?
2. **Logic Gaps** — Check meaningful edge cases, error handling, and data validation.
3. **DRY/YAGNI** — Is this file solving a problem that doesn't exist yet?
4. **Side Effects** — Are functions as pure as possible? Are side effects clearly isolated?

## Output Format

Provide a concise, unornamented list:

- **Fixes Needed** — Logic bugs and correctness issues.
- **KISS Refactors** — Simpler alternatives for over-complex code.

No praise. Findings only.
Include a location, evidence, and the smallest useful fix for each finding. If none are supported, say so.
