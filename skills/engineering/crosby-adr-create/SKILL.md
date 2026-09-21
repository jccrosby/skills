---
name: crosby-adr-create
description: Draft an Architecture Decision Record (ADR) using the repository's established convention or a portable fallback structure. Use for consequential technical decisions, shared standards, or decisions that supersede earlier records.
---

# SKILL: crosby-adr-create

## When to Use

- The change affects multiple teams or processes.
- Introducing a technology or pattern that may be adopted across projects or teams.
- Superseding or overriding a previously accepted ADR.
- User says "ADR" or "decision record"

## When NOT to Use

- Localized changes inside a single team's project with no cross-team impact.
- Reversible experiments — prototype first, then ADR if it graduates.
- Routine bug fixes or straightforward implementation choices covered by existing ADRs.

## Inputs to Gather

Reuse supplied context and inspect existing ADRs before asking for missing information. Gather:

1. **Topic** — one-line description of the decision.
2. **Status** — use the repository's initial status, or `Proposed` when no convention exists.
3. **Contributors** — who is authoring or reviewing, when the local format requires it.
4. **Superseded ADRs** — any prior ADR this replaces or amends.
5. **Options considered** — even if the recommendation is clear, list credible alternatives.

Do not fabricate contributors, dates, or ticket IDs. If unknown, use a placeholder like `_TBD_` and flag it in the summary.

## Procedure

1. Locate existing ADRs, templates, indexes, and repository instructions. Follow their directory, filename, status, and section conventions when they are consistent.
2. If no convention exists, use the fallback below and save under `docs/adrs/YYYYMMDD-descriptive-title.md`.
3. Keep the record concise. Link evidence and related decisions instead of copying large source material.
4. Stop after the draft is written. Do not attempt to publish, sync, or upload the file anywhere — the skill's output is markdown on disk, nothing else.

## Required Sections

Use this fallback only when the repository has no established ADR format. Add or omit optional metadata to match the decision context.

```markdown
# YYYYMMDD - [Descriptive Title]

|                  |                                         |
| ---------------- | --------------------------------------- |
| **Status**       | Proposed                                |
| **Contributors** | - @Name 1<br>- @Name 2                  |
| **Due Date**     | _optional review-period end date_       |
| **References**   | _Superseded or overridden ADRs_         |

## Context

_Describe the current situation and **why** this decision is necessary._
_State the problem plainly. Include measurements, screenshots, or links to reproductions where they exist. Do not editorialize._

## Decision

_Describe the **what** and **how** of the change._

### Rationale

1. Reason 1 — evidence, not opinion.
2. Reason 2.

### Options Considered

1. **Option A** — brief description. Pros / cons.
2. **Option B** — brief description. Pros / cons.
3. **Recommended:** which option and why.

## Consequences

### Pros

1. …

### Cons

1. …

## Next Steps

1. Concrete action with owner (person or team).
2. Ticket to be created / created (`PROJ-123`).
3. Docs / configs to update.
4. Communication or rollout work when needed.

## References

- Links to external docs, RFCs, benchmarks.
- Ticket IDs.
- Prior ADRs.
```

## Quality Checklist

Before handing the draft to the user, verify:

- [ ] Title and filename follow the repository convention, or the dated fallback when no convention exists.
- [ ] Status follows the repository convention, or is `Proposed` when using the fallback.
- [ ] Context explains **why**, not what — no solutioning leaks in.
- [ ] Decision covers **what** and **how**, and names a recommended option when alternatives exist.
- [ ] Consequences lists both pros **and** cons. If the cons section is empty, push back — every decision has trade-offs.
- [ ] Next Steps are concrete: each item is actionable and, where possible, owned.
- [ ] All `_placeholders_` are either filled in or explicitly flagged for the user.
- [ ] Referenced ADRs, tickets, and links resolve — never invent URLs or ticket IDs.

## Output Format

After drafting, print a short summary to the user:

### Draft saved

- **Path:** `[saved ADR path]`
- **Status:** `[initial status]`

### Open questions

- Bulleted list of every `_TBD_`, unresolved option, or assumption the user must resolve before circulating the draft.

---

**Constraint:** Do not mark an ADR accepted on the user's behalf. The skill's job ends with a well-formed proposed record unless the user provides evidence that the repository's decision process already accepted it.
