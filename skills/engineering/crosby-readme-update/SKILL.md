---
name: crosby-readme-update
description: Update an existing README.md for a requested change using repository evidence. Use when setup, usage, features, or architecture documentation has become stale.
---

# Update an existing README

## Procedure

1. Read the request and the current README. Inspect the relevant code, configuration, or documentation that establishes the change. Use commits or project context files when they add evidence.
2. Find the affected sections. Check examples and commands against the repository before changing them.
3. Update only the sections affected by the change. Preserve the README's tone and structure.
4. Review the diff for unsupported claims, broken links, and unrelated edits. Report what changed and any facts that remain unverified.

When the user requests an update, apply it and present the resulting diff or summary. For a review-only request, return proposed changes without editing the file.
