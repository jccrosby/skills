---
name: crosby-skill-review
description: Review an AI skill for precise triggering, narrow scope, usable instructions, repository consistency, and conflicts with neighboring skills. Use before publishing a new or substantially revised SKILL.md; produces findings without editing unless requested.
---

# Review an AI skill

Evaluate whether another agent can discover and apply the skill reliably without unnecessary context or permissions.

## Establish local rules

1. Read the repository's contributor instructions and the complete target `SKILL.md`.
2. Read directly referenced resources and the nearest comparable skills.
3. Inspect indexes, metadata, or validation commands that the repository expects for skills.

## Review criteria

- **Discovery:** the name is valid and the description states both capability and trigger without attracting unrelated work.
- **Scope:** the skill solves one repeatable task and has clear boundaries with adjacent skills.
- **Instructions:** guidance changes agent decisions, preserves user intent, and avoids restating generic capabilities.
- **Inputs and outputs:** required context, artifact, evidence, and stopping condition are clear.
- **Safety and authority:** read-only requests do not imply writes; external or destructive actions retain appropriate authorization boundaries.
- **Portability:** examples and assumptions are reusable or explicitly identified as local conventions.
- **Progressive disclosure:** the entrypoint stays focused, and conditional detail is routed to discoverable references.
- **Consistency:** frontmatter, links, terminology, and indexes agree with the repository.
- **Testability:** observable behavior or invariants can validate the workflow; tests do not merely match prose.

## Findings

Report findings in priority order with the file location, issue, consequence, and smallest useful correction. Separate blocking problems from recommended improvements. End with **Ready to publish** or **Needs revision** and the reason.

Do not rewrite the skill during a review-only request. Do not require extra files, examples, scripts, or metadata unless they provide a concrete benefit or the repository requires them.
