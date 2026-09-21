# Engineering Skills Index

This folder groups the repository's engineering-focused operational skills. Each skill is designed to solve a specific kind of work: planning, review, documentation, commit hygiene, PR drafting, and architecture-level assessment.

Use these skills when a task matches the trigger described in the relevant `SKILL.md`. In practice, the best invocation is direct and specific: name the skill, describe the target, and state the artifact or decision you want produced.

## How to invoke a skill

For a human or model, the pattern should look like this:

- "Use the `crosby-audit-repo` skill to review the auth service directory."
- "Run the `crosby-plan-iterative` skill for the migration work and break it into 3-5 steps."
- "Use the `crosby-conventional-commit` skill for this git diff before I commit."

Good invocations are narrow, task-based, and output-oriented. They tell the skill:

1. what the task is,
2. what object is in scope,
3. what kind of output is expected.

Avoid broad prompts like "fix the project"; prefer prompts that name the task and the skill.

## Skill catalog

### Architecture and quality

- `crosby-audit-repo` — Audits a feature or directory for architectural drift, anti-patterns, performance risk, and compliance with repo context. Use when reviewing a large area rather than a single file.
  - Typical invocation: "Use the `crosby-audit-repo` skill on the payments feature and flag any risks or rule violations."
  - Expected output: A prioritized findings table with file locations, issue types, severity, and recommended fixes.

- `crosby-audit-micro` — Performs a high-density review of a single file or small unit. Use when looking for KISS problems, missing edge cases, DRY/YAGNI issues, or unintended side effects.
  - Typical invocation: "Use the `crosby-audit-micro` skill on `src/handlers/user.ts` and focus on correctness and simplicity."
  - Expected output: A concise list of logic issues, refactor opportunities, and necessary fixes.

### Planning and execution

- `crosby-issue-refine` — Turns an ambiguous request or ticket into a build-ready brief with scope, acceptance criteria, unknowns, and verification.
  - Typical invocation: "Use `crosby-issue-refine` to make this bug report ready for implementation planning."
  - Expected output: A scoped issue brief and a readiness decision.

- `crosby-plan-iterative` — Breaks a large task into a short execution roadmap of 3-5 sequential, testable steps. Use before implementation starts.
  - Typical invocation: "Use the `crosby-plan-iterative` skill to break this API migration into a safe step-by-step roadmap."
  - Expected output: A short implementation plan with success criteria for each step.

- `crosby-plan-execute` — Carries out the current step of an implementation plan while keeping scope tight and requiring human approval before moving on.
  - Typical invocation: "Use the `crosby-plan-execute` skill for step 2 of the migration plan and keep the change scoped."
  - Expected output: A small implementation change, verification notes, and a request for review before the next step.

### Diagnosis and verification

- `crosby-debug-root-cause` — Investigates incorrect or intermittent behavior and distinguishes a confirmed root cause from symptoms and hypotheses.
  - Typical invocation: "Use `crosby-debug-root-cause` to explain why this request intermittently times out."
  - Expected output: Reproduction evidence, causal chain, affected scope, and fix direction.

- `crosby-test-design` — Designs a risk-based test plan for a feature, defect, refactor, or migration.
  - Typical invocation: "Use `crosby-test-design` to define regression coverage for this change."
  - Expected output: Prioritized automated and manual checks mapped to behaviors and risks.

- `crosby-ci-triage` — Finds the first actionable CI failure and classifies the responsible layer.
  - Typical invocation: "Use `crosby-ci-triage` on this failed workflow run."
  - Expected output: Failure classification, evidence, affected scope, and next action.

### Documentation and decision-making

- `crosby-documentation-create` — Helps turn subject-matter knowledge into clear, maintainable documentation. Use when writing a single article or planning a full documentation set.
  - Typical invocation: "Use the `crosby-documentation-create` skill to draft a setup guide for the new deployment flow."
  - Expected output: A structured document draft, with audience, headings, and clear task-oriented guidance.

- `crosby-adr-create` — Drafts an ADR when a decision affects multiple teams, introduces a new standard, or supersedes a previous decision.
  - Typical invocation: "Use the `crosby-adr-create` skill to draft an ADR for moving the service to async processing."
  - Expected output: A markdown ADR draft with context, decision rationale, options, consequences, and open questions.

- `crosby-adr-revise` — Revises an existing ADR from reviewer feedback by creating a small, reviewable plan, waiting for user approval, and then updating the ADR in place.
  - Typical invocation: "Use the `crosby-adr-revise` skill to address the comments on docs/adrs/20260820-foo.md and update the ADR only after I review the plan."
  - Expected output: A concrete revision plan, user approval checkpoint, and the final ADR update with any remaining follow-up notes.

- `crosby-adr-review` — Reviews an existing ADR for comprehensiveness, completeness, clarity, simple language, and correct organization of supporting assets. Read-only — produces a structured report only.
  - Typical invocation: "Use the `crosby-adr-review` skill on docs/adrs/20260820-foo.md before I circulate it for approval."
  - Expected output: A tiered findings report (Critical / Recommended / Minor) with a recommended next action, usually a hand-off to `crosby-adr-revise`.

- `crosby-readme-generate` — Produces a project README from repository context, project goals, and codebase structure.
  - Typical invocation: "Use the `crosby-readme-generate` skill to draft a README for this service."
  - Expected output: A new project README with overview, architecture, setup instructions, and agent workflow guidance.

- `crosby-readme-update` — Refreshes an existing README in place with only the changes needed.
  - Typical invocation: "Use the `crosby-readme-update` skill to add the new environment variables and setup steps to the README."
  - Expected output: A minimal, targeted documentation update that preserves existing tone and structure.

### Review and delivery workflow

- `crosby-pr-review` — Produces a structured review of a branch or PR against quality and project standards. Use before approval or when checking a change for correctness and scope.
  - Typical invocation: "Use the `crosby-pr-review` skill to review this branch for scope, correctness, and any KISS violations."
  - Expected output: A review summary with findings and recommendation.

- `crosby-pr-description` — Writes a GitHub PR body based on the current branch and relevant diff. Use when preparing a pull request for review or `gh pr create`.
  - Typical invocation: "Use the `crosby-pr-description` skill to draft the PR body for the current branch."
  - Expected output: A markdown PR body aligned with the repo template.

- `crosby-conventional-commit` — Creates a conventional commit message based on a git diff. Use before a commit when the change is ready to be captured clearly.
  - Typical invocation: "Use the `crosby-conventional-commit` skill for this staged diff and generate the commit message."
  - Expected output: A copy-ready conventional commit message in a single code block.

- `crosby-release-readiness` — Assesses whether a change has enough compatibility, rollout, rollback, and verification evidence to ship.
  - Typical invocation: "Use `crosby-release-readiness` on version 2.4 before deployment."
  - Expected output: A ready, ready-with-conditions, or not-ready decision with blockers and release checks.

- `crosby-dependency-upgrade` — Researches compatibility and creates an evidence-backed upgrade plan for a dependency or runtime.
  - Typical invocation: "Use `crosby-dependency-upgrade` to plan the upgrade from framework v4 to v5."
  - Expected output: Compatibility findings, ordered migration steps, verification, and rollback limits.

- `crosby-postmortem-create` — Creates a factual, blameless incident postmortem from operational evidence.
  - Typical invocation: "Use `crosby-postmortem-create` with these incident notes and logs."
  - Expected output: Impact, timeline, causal analysis, and owned corrective actions.

- `crosby-skill-review` — Reviews a skill's discovery metadata, scope, instructions, portability, safety boundaries, and repository consistency.
  - Typical invocation: "Use `crosby-skill-review` before publishing this new skill."
  - Expected output: Prioritized findings and a publish-readiness decision.

## Recommended usage pattern

When choosing a skill, start with the task, not the folder:

- If the work is architectural or broad: use `crosby-audit-repo`.
- If the work is a one-file review: use `crosby-audit-micro`.
- If the work is large and ambiguous: use `crosby-plan-iterative`.
- If the requirement itself is ambiguous: use `crosby-issue-refine`.
- If the work is implementation-focused: use `crosby-plan-execute`.
- If a failure's cause is unknown: use `crosby-debug-root-cause` or `crosby-ci-triage` for a pipeline failure.
- If verification coverage is unclear: use `crosby-test-design`.
- If the work is documentation or decision records: use `crosby-documentation-create` or `crosby-adr-create`.
- If the work is reviewing a decision record: use `crosby-adr-review`.
- If the work is review or delivery: use `crosby-pr-review`, `crosby-pr-description`, or `crosby-conventional-commit`.
- If the work is about shipping or operational learning: use `crosby-release-readiness` or `crosby-postmortem-create`.

This folder is intended to be a practical index, not a replacement for the individual skill instructions. For the exact trigger conditions, output format, and constraints, read the matching `SKILL.md` in each subfolder.
