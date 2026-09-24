---
name: crosby-plan-execute
description: Implement the next part of an existing plan with focused changes and verification. Use when the user asks to execute a plan or a named step.
---

# Execute an implementation plan

Use the plan as the source of scope. Complete the work the user authorized, including later steps when requested.

## Procedure

1. Locate the plan and identify the requested step or remaining work. Check earlier results and relevant repository instructions.
2. Implement the smallest coherent change for each step. Add tests when they provide useful evidence for behavior or risk.
3. Run focused verification, inspect the diff, and fix failures caused by the change.
4. Update plan status when the plan tracks it. Keep status consistent with work actually completed.
5. Report the changes, verification, and remaining risks. Continue through the authorized scope unless a material decision needs user input.

## Boundaries

- Keep unrelated bugs and refactors outside the plan unless they block its completion.
- Pause for a decision only when the plan leaves a material choice unresolved or the user asked for a checkpoint.
- Commit only when requested or required by repository instructions. Keep each commit coherent and use the repository's message convention.
- Run repository-specific sync tools only when they exist and the changed files require them.
