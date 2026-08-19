# Skills Repository

This repository is a curated library of reusable AI-assisted workflows, operating patterns, and documentation playbooks. It is designed for work that benefits from clear prompts, disciplined task structure, and repeatable execution patterns rather than application code.

## Overview

The project holds a collection of skills grouped by purpose. Each skill is intentionally narrow and task-oriented so it can be reused across different repos and teams without becoming a monolithic automation layer.

The repository is organized around a simple rule: keep the unit of work small, explicit, and easy to invoke.

## What is in this repo

- `skills/engineering/` contains engineering-focused skills for planning, review, documentation, architecture assessment, and delivery workflow.
- `skills/productivity/` holds broader productivity-oriented patterns and supporting materials.
- `docs/` provides human-readable summaries of the skills and their intended usage.
- `AGENTS.md` defines the repository conventions and expectations for AI-assisted contributors.
- `package.json` tracks the project metadata and tooling used by the repo.

## Main skill areas

### Engineering operations

The engineering skills cover common workflows such as:

- architecture reviews and quality audits,
- iterative planning and execution,
- ADR creation,
- documentation drafting,
- PR preparation and review,
- conventional commit hygiene.

Examples include:

- `audit-repo`
- `micro-audit`
- `iterative-plan`
- `execute-plan`
- `documentation-create`
- `adr-create`
- `readme-generate`
- `readme-update`
- `pr-review`
- `pr-description`
- `conventional-commit`

### Documentation and knowledge capture

This repo treats documentation as a product in its own right. Skills help turn domain knowledge into useful guidance for humans and AI co-workers by emphasizing clear structure, user intent, maintainability, and findability.

## Repository conventions

This repo follows a few core principles:

- keep each skill focused on one task or workflow,
- prefer practical, reusable instructions over broad abstractions,
- give each skill a clear trigger, output, and scope,
- preserve lightweight, human-readable structure and minimal duplication.

## How to use the repository

1. Find the skill that matches the task.
2. Read the corresponding `SKILL.md` file in the relevant skill directory.
3. Invoke the skill with a specific prompt that names the task, scope, and desired output.
4. Keep the work narrow and reviewable.

A typical invocation looks like this:

- "Use the `documentation-create` skill to draft a setup guide for the deployment flow."
- "Use the `iterative-plan` skill to break this migration into safe milestones."
- "Use the `conventional-commit` skill for this git diff and generate the commit message."

## Contribution approach

When adding or updating skills, keep the repo easy to navigate and easy to reuse. Favor:

- small, single-purpose skill directories,
- clear naming and descriptions,
- practical examples,
- a tight focus on workflow and output.
