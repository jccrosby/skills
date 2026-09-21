---
name: crosby-debug-root-cause
description: Diagnose a reproducible software defect and identify its root cause using evidence. Use for incorrect behavior, regressions, intermittent failures, or error reports when the cause is not yet established; do not use for general code review.
---

# Diagnose a software defect

Establish why the failure occurs before proposing a fix. Treat logs, tests, traces, code paths, and observed behavior as evidence. Label inference as inference.

## Investigation

1. Restate the symptom, expected behavior, affected environment, and known reproduction conditions.
2. Reproduce the failure when safe and feasible. Record the exact command, input, and observed result.
3. Trace the failing path from the visible symptom toward the earliest incorrect state or decision.
4. Form a small set of plausible hypotheses. For each, identify evidence that would confirm or reject it.
5. Run the narrowest useful checks. Change one variable at a time and preserve relevant output.
6. Identify the root cause only when evidence distinguishes it from downstream symptoms.
7. Determine affected scope and whether the same condition can occur elsewhere.

If the failure cannot be reproduced, report what was checked, the remaining hypotheses, and the evidence needed next. Do not present the most likely hypothesis as confirmed.

## Report

Return:

- **Symptom and reproduction**
- **Evidence**
- **Root cause**, with the causal chain from defect to symptom
- **Affected scope**
- **Fix direction**, limited to the smallest change that addresses the cause
- **Regression checks**
- **Confidence and unresolved questions**

## Boundaries

- Do not modify code when the user asked only for diagnosis.
- Avoid broad refactors during investigation.
- Do not erase logs, caches, data, or other diagnostic evidence without explicit authorization.
- Do not use successful retries as proof that an intermittent defect is resolved.
