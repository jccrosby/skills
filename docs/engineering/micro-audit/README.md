# Micro audit

## Purpose

This skill is a focused logic review for a single file. It is meant to catch simplification opportunities, missing edge cases, and unintended side effects.

## When to use it

Use it when:

- a file needs a correctness review,
- the code looks more complex than needed,
- or you want to check for logic gaps before approving a change.

## Review checklist

Review the file for:

- KISS violations and over-engineering,
- missing edge cases,
- DRY/YAGNI issues,
- and side effects that are not clearly contained.

## Output format

Provide a short list with only findings:

- Fixes needed: logic bugs and correctness issues
- KISS refactors: simpler alternative designs or stripped-back code

## Good practice

- Be specific about the actual issue.
- Prefer a clear recommendation over vague criticism.
- Focus on what needs to change now.

## Common pitfalls

- Suggesting broad redesigns instead of the smallest valid fix.
- Listing style preferences as if they were correctness problems.
- Missing edge cases and safety boundaries.
