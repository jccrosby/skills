---
name: execute-plan
description: 'Step-by-step implementation of an iterative plan. Enforces atomic commits, state tracking, and mandatory human-in-the-loop checkpoints.'
argument-hint: '<link to plan or current step description>'
---

# SKILL: execute-plan

## 🎯 OBJECTIVE
Execute the current step of an implementation plan while maintaining high-density communication and system integrity. Focus on the smallest possible unit of work that provides value or testability.

## 🛠 PROCEDURE

### Phase 1: Context Alignment
1. **Locate the Plan:** Identify the source of truth for the implementation (e.g., `PLAN.md` or a specific section in `project-context.md`).
2. **State Check:** Mark the current step as "IN PROGRESS." Ensure all previous steps are "COMPLETED."

### Phase 2: Atomic Implementation
1. **Small Batching:** Implement the minimum logic required for the current step.
2. **Prioritize TDD:** Create tests that prove the desired behavior before writing the implementation code.
3. **KISS Audit:** Before showing code, perform a mental `micro-audit`. Is this over-engineered?
4. **Drafting:** Apply the changes to the codebase.

### Phase 3: The Human Loop (MANDATORY)
1. **Summarize:** Explain exactly what was changed and *why* it satisfies the current step.
2. **Verification:** Run relevant tests or linters if available.
3. **STOP:** Do not proceed to the next step. Prompt the user: "⚠️ Step [X] implemented. Please review the changes. Ready to commit?"

### Phase 4: Persistence
1. **Commit:** Upon approval, invoke the `conventional-commit` skill logic to generate a message for the diff.
2. **Update State:** Move the step to "COMPLETED" in the plan.
3. **Sync:** If any architectural rules or context were modified, run `aisync`.

## 🚫 CRITICAL CONSTRAINTS
- **No Scope Creep:** Do not fix "nearby" bugs or refactor unrelated code unless explicitly part of the step.
- **Max Diff Size:** If a single step produces >200 lines of change, pause and suggest breaking the step into sub-tasks.
- **Atomic Commits:** One step = One commit. No exceptions.