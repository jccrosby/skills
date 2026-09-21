---
name: crosby-postmortem-create
description: Create a blameless incident postmortem from logs, timelines, impact data, and participant notes. Use after a service disruption, production defect, or operational incident to document causes, recovery, and owned follow-up work.
---

# Create an incident postmortem

Produce a factual account that helps prevent recurrence. Describe system conditions and decisions without assigning personal blame.

## Gather evidence

Read the incident timeline, alerts, logs, tickets, chat notes, deployment history, and existing incident template when available. Separate observed facts, participant reports, and later inference. Preserve source timestamps and time zones; normalize them only when the chosen format states the conversion.

Do not invent impact, duration, causes, owners, or action dates. Mark missing facts explicitly and ask only for information that materially changes the analysis.

## Analyze the incident

Distinguish:

- **Trigger:** the event that initiated the failure.
- **Root cause:** the underlying condition that made the failure possible.
- **Contributing conditions:** factors that increased likelihood, impact, or recovery time.
- **Detection and response:** how the incident was noticed, diagnosed, mitigated, and resolved.
- **Recovery:** what restored service and whether latent effects remain.

Avoid stopping at operator error. Examine the system conditions that allowed an action to cause or prolong harm.

## Document

Follow an existing repository template when present. Otherwise include:

1. summary and status,
2. user or business impact,
3. timeline,
4. trigger, root cause, and contributing conditions,
5. detection and response analysis,
6. what reduced or increased impact,
7. corrective actions with owner, priority, and completion evidence,
8. unresolved questions and follow-up review date.

Corrective actions should address prevention, detection, or recovery. Do not use vague actions such as "be more careful." Do not create tickets, notify stakeholders, or publish the postmortem unless explicitly requested.
