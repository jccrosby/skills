---
name: crosby-issue-refine
description: Refine a rough engineering request or ticket into a build-ready brief with scope, acceptance criteria, constraints, unknowns, and verification. Use before implementation planning when the requested outcome is still ambiguous.
---

# Refine an engineering issue

Turn incomplete requests into a precise agreement about what should change. Do not design the implementation unless technical constraints affect scope or acceptance.

## Gather evidence

1. Read the supplied request and linked context.
2. Inspect the relevant product behavior, code, documentation, or existing issue when available.
3. Separate facts from assumptions. Ask only about missing information that would materially change scope or expected behavior.
4. Identify the user or operator affected, the current behavior, the desired behavior, and why the change matters.

## Define the issue

Produce a brief containing:

- **Problem:** observable current behavior and its impact.
- **Desired outcome:** the result, without prescribing an unnecessary implementation.
- **In scope:** the smallest coherent change that produces the outcome.
- **Out of scope:** adjacent work that should not enter the change accidentally.
- **Acceptance criteria:** independently verifiable behavior, including important failure and boundary cases.
- **Constraints and dependencies:** compatibility, policy, data, timing, or system limitations supported by evidence.
- **Unknowns:** unresolved questions, each paired with its effect on the work.
- **Verification:** how a reviewer can prove the acceptance criteria were met.

Use Given/When/Then only when it makes behavioral criteria clearer. Do not turn implementation details into acceptance criteria unless the implementation itself is a requirement.

## Boundaries

- Do not invent product decisions, deadlines, owners, metrics, or ticket identifiers.
- Do not estimate effort without repository context and an explicit request.
- Do not implement the issue or update an external tracker unless the user asks.
- If evidence shows the request combines unrelated outcomes, propose separate issues and explain the dependency between them.

End with a readiness decision: **Ready for planning** or **Needs input**, followed by the specific reason.
