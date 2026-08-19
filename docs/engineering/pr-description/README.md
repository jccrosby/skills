# Pull request description

## Purpose

This skill creates a pull request description from the current branch by reading the diff and matching the repo’s template.

## When to use it

Use it when:

- you need a PR summary,
- you are preparing a GitHub PR body,
- or you want to draft a release-ready description from the local branch.

## Workflow

1. Inspect the current branch and working state.
2. Compare against the default base branch.
3. Read the git log and diff for scope and likely user-visible changes.
4. Fill in the repo template with accurate overview, change type, related tickets, and checklist items.
5. Return a markdown body ready to paste into GitHub or pass to the CLI.

## What makes a good PR description

A strong PR description should:

- explain why the change exists,
- describe the user or operator impact,
- list the relevant type of change,
- include any related tickets,
- and only check checklist items that are genuinely supported.

## Good practice

- Do not invent behavior or test results.
- Keep the overview focused on motivation and impact.
- Preserve the exact template headings and structure.
- Call out if the diff mixes unrelated concerns.

## Common pitfalls

- Checking “tests pass” or “build works” without evidence.
- Listing file names instead of user impact.
- Inventing tickets or assumptions.
- Overstating certainty about changes that are not verified.
