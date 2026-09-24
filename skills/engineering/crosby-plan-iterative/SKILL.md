---
name: crosby-plan-iterative
description: Break a complex implementation task into a small sequence of testable steps. Use when the work needs an execution plan before coding.
---

# SKILL: crosby-plan-iterative

## When to Use

- Before starting a new feature or complex refactor.
- When a task feels "too big" or architectural drift is likely.

## Procedure

1. Analyze the target requirement and relevant repository constraints.
2. Identify the "Minimal Viable Logic" required to achieve the goal.
3. Divide the work into the fewest coherent steps that can be implemented and checked in sequence.
4. For each step, define a **Success Criteria** (e.g., a test pass or specific behavior).

## Output Format

### 🎯 The Iterative Roadmap

1. **Step 1: [Name]**
   - **Action:** (Concise technical implementation detail)
   - **KISS Check:** Why this is the simplest path.
   - **Success:** How to verify.

2. **Step 2: [Name]**
   - ... (repeat as needed)

---

**Constraint:** Avoid speculative abstractions. Add one when the current work requires it.
