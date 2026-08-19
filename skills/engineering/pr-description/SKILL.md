---
name: pr-description
description: Drafts GitHub pull request bodies from the current branch using this repo's PULL_REQUEST_TEMPLATE.md. Use when the user asks for a PR description, PR body, opening a pull request, or running gh pr create for paywall-contentful-migrations.
---

# Pull request description

Produce a PR body that matches [.github/PULL_REQUEST_TEMPLATE.md](./.github/PULL_REQUEST_TEMPLATE.md). Base analysis on the **current working branch** unless the user names another branch or base.

## Gather context

Run these in parallel (use `all` permissions if `gh` or network is needed later):

1. `git branch --show-current`
2. `git status`
3. `git log <base>..HEAD --oneline` (default `<base>`: `main`; use `origin/main` if local `main` is missing)
4. `git diff <base>...HEAD` — full diff for scope, changelog, and checklist inference

If the user will open the PR immediately, also run `git rev-parse --abbrev-ref @{upstream}` and `git fetch origin <base>` when needed so the summary matches what GitHub will show.

**Ticket ID:** If the branch name matches `PAID-\d+`, use it in Related Tickets. Otherwise ask once or leave the placeholder.

## Write each section

| Section             | Guidance                                                                                                                                                                                                                                                                                                                                                                                               |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Overview**        | Purpose, scope, and motivation in 2–4 sentences. Lead with _why_, not file lists.                                                                                                                                                                                                                                                                                                                      |
| **Type of change**  | Check every box that applies; delete none of the option lines. Prefer **Tooling change** for `tools/`, scripts, and migration tooling; **New feature** for new product-facing capability; **Bug fix** / **Breaking change** only when accurate.                                                                                                                                                        |
| **Changelog**       | Bullet list of user-visible or operator-visible changes derived from commits and diff. Group related commits; use imperative or past tense consistently.                                                                                                                                                                                                                                               |
| **Related Tickets** | `- [PAID-NNN](https://baseball.atlassian.net/browse/PAID-NNN)` — replace `NNN` from branch or user input.                                                                                                                                                                                                                                                                                              |
| **Checklist**       | Check items only when the diff supports them; leave others unchecked. Infer: **Includes tests** if `*.test.ts` or test dirs changed; **documentation** if `README.md` or `*.md` docs changed; **style guidelines** when TypeScript follows existing `tools/` patterns. Never check **Base branch**, **tests pass**, **build**, or **no warnings** unless the user confirmed or you ran those commands. |

## Optional sections

Include only when relevant; omit the HTML comment wrappers from the template file.

- **Screenshots** — UI or CSV/output samples worth visual review.
- **Documentation** — Link new or updated README paths (not bare repo root).
- **Related** — Other PRs, ADRs under `plans/`, or follow-up work.

## Output rules

1. Return the PR body as a single markdown document the user can paste into GitHub or pass to `gh pr create --body`.
2. Preserve template headings and emoji labels exactly (`### Overview`, `:receipt:`, etc.).
3. Do not invent tickets, behavior, or test results.
4. If the diff mixes unrelated concerns, say so in Overview and suggest splitting the PR.

## Body template

Fill placeholders; keep structure identical to the repo template:

```markdown
### Overview

[Purpose, scope, motivation]

### Type of change :receipt:

- [ ] Bug fix (non-breaking change which fixes an issue)
- [ ] Tooling change (non-breaking change which adds functionality to the tooling)
- [ ] New feature (non-breaking change which adds functionality)
- [ ] Breaking change (fix or feature that would cause existing functionality to not work as expected)
- [ ] This change requires a documentation update
- [ ] Styling update

### Related Tickets :ticket:

- [PAID-TICKET_NUMBER](https://baseball.atlassian.net/browse/PAID-TICKET_NUMBER)

### Checklist :memo:

- [ ] Base branch is correct
- [ ] Includes tests
- [ ] My code follows the style guidelines of this project
- [ ] I have made corresponding changes to the documentation
- [ ] My changes generate no new warnings
- [ ] New and existing unit tests pass locally with my changes
- [ ] The build step works
```

## Opening the PR (only when asked)

After the body is approved or on explicit request:

1. Push with `git push -u origin HEAD` if no upstream.
2. `gh pr create --title "..." --body "$(cat <<'EOF'
[filled body]
EOF
)"`

Title: short imperative summary; include `PAID-NNN` when a ticket exists.
