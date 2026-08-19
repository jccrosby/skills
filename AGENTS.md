# AGENTS.md

This repository is a home for reusable AI skills and supporting documentation. It is not a product application, and the main unit of work is a skill, not an app feature or service.

## Repository purpose

- Keep each skill in its own directory under `skills/`.
- Prefer a focused, single-purpose skill over a broad, multi-topic one.
- Store reusable instructions, task workflows, and examples that can be applied across projects.
- Use this repo as a living collection of prompts, conventions, and operational playbooks for day-to-day AI-assisted work.

## Layout and conventions

- Skill directories live under `skills/{skill-name}/` or `skills/{category}/{skill-name}/`.
- Each skill usually includes a `SKILL.md` file as the primary entrypoint.
- Supporting documents can live alongside the skill when they clarify process, templates, or style guidance.
- Keep supporting files tightly scoped to the skill; do not duplicate large amounts of documentation that already exists elsewhere.
- Prefer linking to existing docs rather than copying them into a new skill.

## Skill authoring guidance

When creating or updating a skill:

1. Read the nearest existing skill examples before writing anything new.
2. Keep the skill narrowly scoped and action-oriented.
3. Give the skill a clear `name` and a precise `description` in the frontmatter.
4. Write in plain, practical language that tells an agent what to do and when to do it.
5. Include only the context that would be hard to infer from the repo itself.
6. Prefer reusable workflows over one-off instructions.
7. Keep the skill easy to extend without turning it into a monolith.

## Repo-specific operational rules

- This repo is a knowledge repo, so prefer docs, prompts, and workflows over production code.
- Do not add application scaffolding, framework boilerplate, or unrelated tooling unless the repo explicitly becomes more than a skills library.
- Keep changes small and easy to review.
- Follow conventional commit standards for any repository changes.
- Favor examples that are easy to adapt to another codebase rather than deeply local implementation details.

## Typical workflow for a new skill

- Create a directory named for the skill (for example, `skills/my-skill/`).
- Add a `SKILL.md` file with clear frontmatter and instructions.
- Add any necessary companion docs only if the skill depends on them.
- Keep examples and commands realistic, copy-paste-ready, and minimal.
- If the skill references external tooling such as GitHub CLI, Jira, or other services, document the exact trigger and expected behavior.

## References

Good examples in this repo:

- [skills/engineering/documentation-create/SKILL.md](skills/engineering/documentation-create/SKILL.md)
- [skills/engineering/pr-description/SKILL.md](skills/engineering/pr-description/SKILL.md)
- [skills/engineering/execute-plan/SKILL.md](skills/engineering/execute-plan/SKILL.md)

## Working style for agents

- Do not rewrite large sections of the repo without a clear reason.
- Preserve the style and intent of the existing skills when editing them.
- When adding new skills, make the repo easier for future agents to navigate, not harder.
- Favor consistency, discoverability, and minimal duplication.

This repository is most useful when it remains a clean, well-structured library of reusable operational patterns.
