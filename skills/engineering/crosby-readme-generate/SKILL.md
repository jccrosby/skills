---
name: crosby-readme-generate
description: Generate a project README from repository evidence. Use when a repository lacks an adequate README and needs accurate purpose, setup, usage, architecture, and contribution guidance.
---

# Generate a project README

Write for someone encountering the repository for the first time. Every command and factual claim must come from repository evidence or be marked as unresolved.

## Inspect the repository

1. Read contributor instructions, manifests, existing documentation, configuration, entry points, tests, and example environment files.
2. Read repository-specific context directories such as `.ai/` only when they exist.
3. Determine the project's purpose, intended users, supported environments, installation path, common tasks, and verification commands.
4. Run safe help or verification commands when they materially improve accuracy.

## Draft the README

Follow an established local documentation style when present. Include only applicable sections, usually:

- project name and purpose,
- prerequisites,
- installation or setup,
- primary usage with verified examples,
- configuration,
- architecture or repository layout when it helps contributors,
- development, testing, and contribution guidance,
- links to deeper documentation.

Document agent-specific workflows only when the repository actually uses them and they matter to contributors. Link to the source of truth rather than duplicating large policy documents.

## Constraints

- Do not invent commands, supported versions, environment variables, URLs, or project capabilities.
- Do not include secrets or personal contact information.
- Do not present generic setup steps as repository-specific instructions without confirming them.
- Keep the README as an entrypoint. Move deep reference material to existing documentation or recommend a focused companion document.

Write `README.md` only when the user asked for a file change. Otherwise return a draft for review and list any unresolved facts.
