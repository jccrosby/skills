---
name: crosby-pr-description
description: Draft a GitHub pull request title and body from a branch, commit range, or diff using the target repository's template and conventions. Use when preparing or opening a pull request; do not create or push it unless requested.
---

# Draft a pull request description

Describe the change that reviewers will actually see. Base every claim on the diff, commit history, repository context, or verification output.

## Gather context

1. Identify the source and base branches. Prefer the repository's configured default branch when the user did not name a base.
2. Inspect working-tree status, commits in the range, and the full merge-base diff.
3. Locate the repository's pull request template under `.github/`, `docs/`, or the configured template directory. Use it when present.
4. Read relevant issues, plans, or ADRs that are locally available or supplied by the user.
5. Record verification actually run and its result.

Fetch remote state only when it is needed for accuracy and authorized. If uncommitted work is not part of the pull request diff, do not describe it as included.

## Write the description

Preserve the repository template's headings, checklist items, and instructions. Remove placeholder comments only when the template expects a clean final body. When no template exists, use the smallest useful structure:

```markdown
## Summary

[Purpose and user or operator impact]

## Changes

- [Material change]

## Verification

- [Command or check and result]
```

Add risk, rollout, screenshots, breaking changes, migrations, or related work only when relevant. Derive ticket identifiers from the branch or supplied context only when the repository documents the pattern; otherwise omit them or leave a clear placeholder.

Check checklist items only when evidence supports them. Never claim tests pass, builds succeed, warnings are absent, or documentation is complete unless those checks were run or confirmed.

## Output and actions

Return a copy-ready title and body. Note mixed or unrelated changes that may warrant separate pull requests.

Do not push a branch, create a pull request, edit remote metadata, or request reviewers unless the user explicitly asks. Before opening a pull request, show or confirm the final title, body, base, and source unless the user requested immediate creation with those values already clear.
