---
name: crosby-ci-triage
description: Triage a failed continuous-integration run and distinguish code failures, flaky tests, environment faults, and pipeline configuration problems. Use when a build, check, or deployment pipeline fails and the responsible layer is unclear.
---

# Triage a CI failure

Find the first actionable failure, identify its likely owner, and recommend the smallest next action. A later cancellation or cascade failure is not the root failure.

## Collect context

1. Identify the repository, commit, branch, workflow, job, attempt, and runner environment.
2. Read the failed step and enough preceding output to understand setup and dependencies.
3. Compare with the same job on a recent successful commit when available.
4. Check whether the failure reproduces locally or in an equivalent isolated environment when doing so is safe and practical.

## Classify the failure

Use evidence to classify it as one or more of:

- **Change-caused:** the proposed code or tests violate expected behavior.
- **Flaky:** repeated identical conditions produce inconsistent results and there is evidence of nondeterminism.
- **Environment or infrastructure:** runner, network, service, resource, credential, or platform failure independent of the change.
- **Pipeline configuration:** incorrect workflow syntax, permissions, dependencies, caching, artifacts, or job ordering.
- **Unknown:** evidence is insufficient to distinguish the above.

Do not label a failure flaky merely because retrying might make it pass.

## Report

Return the first actionable failure, classification, supporting evidence, affected scope, likely owning area, and the next diagnostic or repair action. Note downstream jobs that can be ignored until the first failure is resolved.

Do not rerun, cancel, approve, or modify a remote workflow unless the user asks. When a rerun is authorized, preserve the original run and compare attempts before drawing a conclusion.
