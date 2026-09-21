---
name: crosby-release-readiness
description: Assess whether a change or release is ready to ship using evidence for compatibility, operations, rollout, rollback, and verification. Use before deployment, publication, or merge when release risk needs an explicit go/no-go decision.
---

# Assess release readiness

Evaluate the actual change and its operating context. Do not treat a completed checklist as evidence when the underlying result is unavailable.

## Review areas

Check the areas that apply:

- intended scope and approved requirements,
- automated and manual verification results,
- backward and forward compatibility,
- data or schema migrations, including partial failure and recovery,
- configuration, secrets, feature flags, and environment differences,
- observability needed to detect success or harm,
- rollout sequence, dependencies, and ownership,
- rollback or mitigation path and its limits,
- user, operator, support, and documentation changes,
- known risks, deferred work, and active incidents.

Mark an area **Not applicable** only with a short reason. Mark evidence **Missing** when it was not supplied or cannot be verified; do not infer success from absence of failure.

## Decision

Return one of:

- **Ready:** required evidence exists and no release-blocking risk remains.
- **Ready with conditions:** named actions must occur during rollout, but do not require another code change or approval decision.
- **Not ready:** a specific missing control, failed check, or unresolved risk should block release.

Include blockers, non-blocking risks, rollout checks, rollback triggers, and the evidence reviewed. Distinguish a rollback that restores code from one that can also restore data or external state.

This skill assesses readiness only. Do not merge, publish, deploy, toggle production flags, or execute rollback unless the user explicitly requests that action.
