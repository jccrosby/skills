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
4. Use the repository's pull request template when one exists; otherwise use a small summary, changes, and verification structure.
5. Return a title and markdown body ready to paste into GitHub or pass to the CLI.

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
- Preserve the repository template's headings and structure when one exists.
- Call out if the diff mixes unrelated concerns.

## Common pitfalls

- Checking “tests pass” or “build works” without evidence.
- Listing file names instead of user impact.
- Inventing tickets or assumptions.
- Overstating certainty about changes that are not verified.
