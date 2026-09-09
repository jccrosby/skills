---
name: adr-create
description: 'Draft an Architectural Decision Record (ADR). Use when proposing a technology change, capturing a decision that affects multiple teams/processes, superseding a prior decision, or when the user asks for a ADR / decision record. Produces a markdown draft file only.'
argument-hint: '<decision topic> [--supersedes <MV title>]'
---

# SKILL: adr-create

## When to Use

- The change affects multiple teams or processes.
- Introducing a new technology or pattern the Web Stream group may adopt across projects.
- Superseding or overriding a previously accepted ADR.
- User says "ADR" or "decision record"

## When NOT to Use

- Localized changes inside a single team's project with no cross-team impact.
- Reversible experiments — prototype first, then ADR if it graduates.
- Routine bug fixes or straightforward implementation choices covered by existing ADRs.

## Inputs to Gather

Before drafting, confirm with the user:

1. **Topic** — one-line description of the decision.
2. **Status** — start as `PROPOSED` unless retro-documenting an accepted decision.
3. **Contributors** — who is authoring / reviewing.

- **Superseded ADRs** — any prior ADR this replaces or amends.

5. **Options considered** — even if the recommendation is clear, list the alternatives.

Do not fabricate contributors, dates, or ticket IDs. If unknown, use a placeholder like `_TBD_` and flag it in the summary.

## Procedure

1. Compute the title prefix: today's date as `YYYYMMDD`. Combine with a short, descriptive title in Title Case.
2. Draft the sections in the order below. Keep each section tight — prose, bullets, and small tables only.
3. Save the draft as `docs/adrs/YYYYMMDD-descriptive-title.md` in the current repo. Create the folder if missing.
4. Stop after the draft is written. Do not attempt to publish, sync, or upload the file anywhere — the skill's output is markdown on disk, nothing else.

## Required Sections

Follow the "Web Stream ADR" template exactly. Do not add or remove top-level sections without cause.

```markdown
# YYYYMMDD - [Descriptive Title]

|                  |                                         |
| ---------------- | --------------------------------------- |
| **Status**       | PROPOSED 🟡 / ACCEPTED 🟢 / REJECTED 🔴 |
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
4. Communication plan (Slack channel, standup, all-hands).

## References

- Links to external docs, RFCs, benchmarks.
- Ticket IDs.
- Prior ADRs.
```

## Quality Checklist

Before handing the draft to the user, verify:

- [ ] Title matches `YYYYMMDD - Descriptive Title` and today's date is correct.
- [ ] Status is one of the three allowed values, styled with the matching color emoji.
- [ ] Context explains **why**, not what — no solutioning leaks in.
- [ ] Decision covers **what** and **how**, and names a recommended option when alternatives exist.
- [ ] Consequences lists both pros **and** cons. If the cons section is empty, push back — every decision has trade-offs.
- [ ] Next Steps are concrete: each item is actionable and, where possible, owned.
- [ ] All `_placeholders_` are either filled in or explicitly flagged for the user.
- [ ] Referenced MVs, tickets, and links resolve — never invent URLs or ticket IDs.

## Output Format

After drafting, print a short summary to the user:

### 📝 Draft Saved

- **Path:** `docs/adrs/YYYYMMDD-slug.md`
- **Status:** PROPOSED 🟡

### ❓ Open Questions

- Bulleted list of every `_TBD_`, unresolved option, or assumption the user must resolve before circulating the draft.

---

**Constraint:** Do not mark an ADR `ACCEPTED` on the user's behalf. Acceptance follows an asynchronous review; the skill's job ends at a well-formed `PROPOSED` markdown draft on disk.
