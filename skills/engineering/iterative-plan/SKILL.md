---
name: iterative-plan
description: 'Break a complex task into 3-5 simple, testable development steps. Focuses on KISS and avoiding premature abstraction.'
argument-hint: '<task description>'
---

# SKILL: iterative-plan

## When to Use

- Before starting a new feature or complex refactor.
- When a task feels "too big" or architectural drift is likely.
- To enforce the "Iterative Dev" mandate from `global-standards.md`.

## Procedure

1. Analyze the target requirement.
2. Identify the "Minimal Viable Logic" required to achieve the goal.
3. Deconstruct the implementation into 3-5 distinct, sequential steps.
4. For each step, define a **Success Criteria** (e.g., a test pass or specific behavior).

## Output Format

### 🎯 The Iterative Roadmap

1. **Step 1: [Name]**
   - **Action:** (Concise technical implementation detail)
   - **KISS Check:** Why this is the simplest path.
   - **Success:** How to verify.

2. **Step 2: [Name]**
   - ... (repeat for max 5 steps)

---

**Constraint:** No over-engineering. Do not suggest abstractions (interfaces, wrappers) unless they are required for Step 1.
