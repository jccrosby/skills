# Engineering Skills Index

This folder groups the repository's engineering-focused operational skills. Each skill is designed to solve a specific kind of work: planning, review, documentation, commit hygiene, PR drafting, and architecture-level assessment.

Use these skills when a task matches the trigger described in the relevant `SKILL.md`. In practice, the best invocation is direct and specific: name the skill, describe the target, and state the artifact or decision you want produced.

## How to invoke a skill

For a human or model, the pattern should look like this:

- "Use the `audit-repo` skill to review the auth service directory."
- "Run the `iterative-plan` skill for the migration work and break it into 3-5 steps."
- "Use the `conventional-commit` skill for this git diff before I commit."

Good invocations are narrow, task-based, and output-oriented. They tell the skill:

1. what the task is,
2. what object is in scope,
3. what kind of output is expected.

Avoid broad prompts like "fix the project"; prefer prompts that name the task and the skill.

## Skill catalog

### Architecture and quality

- `audit-repo` — Audits a feature or directory for architectural drift, anti-patterns, performance risk, and compliance with repo context. Use when reviewing a large area rather than a single file.
  - Typical invocation: "Use the `audit-repo` skill on the payments feature and flag any risks or rule violations."
  - Expected output: A prioritized findings table with file locations, issue types, severity, and recommended fixes.

- `micro-audit` — Performs a high-density review of a single file or small unit. Use when looking for KISS problems, missing edge cases, DRY/YAGNI issues, or unintended side effects.
  - Typical invocation: "Use the `micro-audit` skill on `src/handlers/user.ts` and focus on correctness and simplicity."
  - Expected output: A concise list of logic issues, refactor opportunities, and necessary fixes.

### Planning and execution

- `iterative-plan` — Breaks a large task into a short execution roadmap of 3-5 sequential, testable steps. Use before implementation starts.
  - Typical invocation: "Use the `iterative-plan` skill to break this API migration into a safe step-by-step roadmap."
  - Expected output: A short implementation plan with success criteria for each step.

- `execute-plan` — Carries out the current step of an implementation plan while keeping scope tight and requiring human approval before moving on.
  - Typical invocation: "Use the `execute-plan` skill for step 2 of the migration plan and keep the change scoped."
  - Expected output: A small implementation change, verification notes, and a request for review before the next step.

### Documentation and decision-making

- `documentation-create` — Helps turn subject-matter knowledge into clear, maintainable documentation. Use when writing a single article or planning a full documentation set.
  - Typical invocation: "Use the `documentation-create` skill to draft a setup guide for the new deployment flow."
  - Expected output: A structured document draft, with audience, headings, and clear task-oriented guidance.

- `adr-create` — Drafts an ADR when a decision affects multiple teams, introduces a new standard, or supersedes a previous decision.
  - Typical invocation: "Use the `adr-create` skill to draft an ADR for moving the service to async processing."
  - Expected output: A markdown ADR draft with context, decision rationale, options, consequences, and open questions.

- `readme-generate` — Produces a project README from repository context, project goals, and codebase structure.
  - Typical invocation: "Use the `readme-generate` skill to draft a README for this service."
  - Expected output: A new project README with overview, architecture, setup instructions, and agent workflow guidance.

- `readme-update` — Refreshes an existing README in place with only the changes needed.
  - Typical invocation: "Use the `readme-update` skill to add the new environment variables and setup steps to the README."
  - Expected output: A minimal, targeted documentation update that preserves existing tone and structure.

### Review and delivery workflow

- `pr-review` — Produces a structured review of a branch or PR against quality and project standards. Use before approval or when checking a change for correctness and scope.
  - Typical invocation: "Use the `pr-review` skill to review this branch for scope, correctness, and any KISS violations."
  - Expected output: A review summary with findings and recommendation.

- `pr-description` — Writes a GitHub PR body based on the current branch and relevant diff. Use when preparing a pull request for review or `gh pr create`.
  - Typical invocation: "Use the `pr-description` skill to draft the PR body for the current branch."
  - Expected output: A markdown PR body aligned with the repo template.

- `conventional-commit` — Creates a conventional commit message based on a git diff. Use before a commit when the change is ready to be captured clearly.
  - Typical invocation: "Use the `conventional-commit` skill for this staged diff and generate the commit message."
  - Expected output: A copy-ready conventional commit message in a single code block.

## Recommended usage pattern

When choosing a skill, start with the task, not the folder:

- If the work is architectural or broad: use `audit-repo`.
- If the work is a one-file review: use `micro-audit`.
- If the work is large and ambiguous: use `iterative-plan`.
- If the work is implementation-focused: use `execute-plan`.
- If the work is documentation or decision records: use `documentation-create` or `adr-create`.
- If the work is review or delivery: use `pr-review`, `pr-description`, or `conventional-commit`.

This folder is intended to be a practical index, not a replacement for the individual skill instructions. For the exact trigger conditions, output format, and constraints, read the matching `SKILL.md` in each subfolder.
