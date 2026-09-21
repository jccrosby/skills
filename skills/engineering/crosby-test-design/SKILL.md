---
name: crosby-test-design
description: Design a risk-based test plan for a feature, defect, refactor, or migration. Use when deciding what behavior to test, which test level to use, or what regression evidence a change needs; does not implement tests unless requested.
---

# Design a test plan

Choose the smallest set of tests that provides credible evidence for the change. Prefer tests at the lowest level that can observe the required behavior, while preserving integration or end-to-end coverage for risks that lower levels cannot detect.

## Analyze the change

1. Read the requirement, acceptance criteria, diff, and nearby tests that are available.
2. Identify changed behavior, invariants that must remain true, system boundaries, state transitions, and failure paths.
3. Rank risks by impact and likelihood. Give extra attention to data loss, authorization, compatibility, concurrency, money, and irreversible effects when relevant.
4. Map each material risk or acceptance criterion to observable evidence.

## Select coverage

For each proposed test, state:

- behavior or risk covered,
- test level: unit, component, integration, contract, end-to-end, or manual,
- setup and important input,
- expected observable result,
- why a lower-cost test would not be sufficient, when applicable.

Include normal behavior, meaningful boundaries, failures, and regressions. Exclude permutations that do not change risk or behavior. Avoid tests that only repeat implementation details or assert incidental structure.

## Output

Return:

1. **Risk summary**
2. **Required automated tests**, ordered by value
3. **Manual or environment-dependent checks**, only when automation is impractical
4. **Existing coverage to retain or update**
5. **Explicit exclusions**, with reasons
6. **Completion evidence**

Do not claim coverage without inspecting the tests or execution results. If asked to implement the plan, preserve the project's existing test conventions and run the narrowest relevant test command before broader suites.
