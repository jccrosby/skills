---
name: crosby-adr-review
description: Review an Architecture Decision Record (ADR) for structural completeness, evidence, trade-offs, clarity, and consistency with repository conventions. Use before circulation or acceptance; produces findings without editing the record.
---

# Review an Architecture Decision Record

Assess whether the record explains a consequential decision well enough for its intended reviewers and future maintainers.

## Establish the convention

1. Read the ADR in full and identify its intended decision and status.
2. Read repository instructions, the local ADR template, neighboring records, and any ADR index.
3. When no local convention exists, use the fallback structure in `crosby-adr-create`.
4. Open reachable supporting ADRs, tickets, images, and links. Note anything that cannot be verified.

Do not impose the fallback filename, status values, or section order when the repository has a different established convention.

## Review criteria

### Structure and organization

- The location, filename, metadata, and section structure follow the established convention.
- The decision, status, and relationship to earlier records are easy to identify.
- Supporting assets use portable paths, meaningful labels or alt text, and predictable locations.
- Placeholders and unresolved questions are explicit.

### Decision quality

- Context explains the problem, constraints, and reason a decision is needed.
- The decision says what will change and enough about how it applies to prevent conflicting interpretations.
- Rationale uses evidence or concrete constraints rather than preference alone.
- Credible alternatives and the option to do nothing are considered when relevant.
- Consequences include benefits, costs, risks, and limitations.
- Follow-up work is concrete and owned when ownership information exists.

### Clarity and integrity

- A reader can identify the decision without reconstructing it from background material.
- Terms remain consistent and domain language is defined for the intended audience.
- Claims, dates, contributors, tickets, and citations are supported rather than invented.
- Related and superseded records link correctly and do not leave conflicting active guidance unexplained.

## Findings

Group findings by severity:

- **Critical:** the decision is ambiguous, unsupported, internally inconsistent, or unsafe to circulate or accept.
- **Recommended:** the record is understandable but materially incomplete or difficult to maintain.
- **Minor:** a localized clarity or organization issue with little effect on the decision.

For each finding, cite the section, line, or asset; explain the consequence; and give the smallest useful correction. Distinguish structural gaps from reasoning gaps.

End with the ADR path, observed status, overall verdict, open questions, and next action. Recommend `crosby-adr-revise` when changes are needed. Otherwise state the next step required by the repository's actual decision process.

This skill is read-only. Do not edit the ADR, change its status, or create follow-up work during a review-only request.
