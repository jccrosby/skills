---
name: crosby-adr-review
description: 'Review an existing Architectural Decision Record (ADR) for comprehensiveness, completeness, clarity, simple language, and correct organization of supporting assets. Use when checking a PROPOSED ADR before circulation, evaluating an ADR before acceptance, or auditing an existing ADR. Produces a structured report only — does not modify the ADR.'
argument-hint: '<adr path>'
---

# SKILL: crosby-adr-review

## When to Use

- Reviewing a PROPOSED ADR before it is circulated for approval.
- Evaluating an ADR before it is moved to ACCEPTED.
- Auditing an existing ADR that may be stale, incomplete, or unclear.
- User says "review the ADR", "check this ADR", or "audit this decision record".

## When NOT to Use

- Drafting a new ADR — use `crosby-adr-create`.
- Applying changes to an ADR based on feedback — use `crosby-adr-revise`.
- Reviewing implementation code that follows from an ADR — use `crosby-pr-review` or `crosby-audit-repo`.
- General doc review that is not a decision record — use `crosby-documentation-create`.

## Inputs to Gather

Before reviewing, confirm with the user:

1. **ADR path** — the exact file to review (typically under `docs/adrs/`).
2. **Review focus** — full review, or scoped to specific sections (e.g. only Rationale and Options Considered).
3. **Audience** — reviewers, adjacent teams, or a wider audience. Affects how strict the "simple language" bar is.
4. **Related ADRs** — any ADR this one supersedes, extends, or depends on.

If the file cannot be located or is not a decision record, stop and ask the user for the correct path.

## Source of Truth

The ADR template, section list, status values, and file-naming convention are owned by `crosby-adr-create`. Treat that skill as the single source of truth. Do not restate the template here; check the ADR against it.

## Procedure

1. **Read the ADR in full.** Do not skim. Note the intended decision before evaluating structure.
2. **Read supporting assets.** Open every referenced ADR, ticket, image, and external link that is reachable. Flag any that are missing or broken.
3. **Check location and filename.** The file should live in `docs/adrs/` and match `YYYYMMDD-descriptive-title.md`.
4. **Compare against the template** defined by `crosby-adr-create`. Confirm all required sections are present, in the right order, and non-empty.
5. **Apply the Review Criteria below** section by section.
6. **Group findings by severity** and emit the report in the Output Format below.
7. **Recommend the next action** — usually a hand-off to `crosby-adr-revise` when changes are required.

Do not edit the ADR. This skill is read-only.

## Review Criteria

### 1. Structural Completeness

- Title matches `YYYYMMDD - Descriptive Title` and the date is real.
- Metadata table is present with Status, Contributors, Due Date (optional), and References.
- Status is one of `PROPOSED 🟡`, `ACCEPTED 🟢`, `REJECTED 🔴`.
- All required sections are present: Context, Decision (with Rationale and Options Considered), Consequences (Pros and Cons), Next Steps, References.
- No extra top-level sections are added without cause.

### 2. Comprehensiveness

- **Context** explains **why** the decision is needed, not what the solution is. Includes measurements, screenshots, or reproductions where they exist.
- **Decision** covers both **what** is changing and **how** it will be applied.
- **Rationale** is evidence-based, not opinion. Each reason cites data, prior art, or a concrete constraint.
- **Options Considered** lists real alternatives with pros and cons, and clearly identifies the Recommended option.
- **Consequences** includes both pros **and** cons. An empty cons section is a finding — every decision has trade-offs.
- **Next Steps** are concrete: each item is actionable, and where possible, owned by a person or team and linked to a ticket.
- **References** resolve to real URLs, ADRs, and ticket IDs. No invented links.

### 3. Clarity and Simple Language

- The reader can identify the decision within the first screen.
- Plain language. Domain jargon is defined the first time it appears.
- Active voice. Short, direct sentences.
- No marketing, hedging, or corporate speak.
- Terminology is consistent throughout — the same concept is not named three different ways.
- Lists are used where prose adds no value.
- Diagrams, tables, and code blocks earn their space; if they are not clearer than prose, they are noise.

### 4. Supporting Assets and Organization

- The ADR is in `docs/adrs/` alongside its peers.
- Filename slug matches the title and is URL-safe.
- Superseded or related ADRs are linked with a working relative path.
- Images and screenshots use relative paths and live in a predictable location next to the ADR (for example, `docs/adrs/assets/YYYYMMDD-slug/`). Inline base64 or absolute local paths are a finding.
- Every image has meaningful alt text.
- External links are stable — no localhost URLs, private previews, or dead endpoints.
- No fabricated contributors, dates, ticket IDs, or citations.
- Placeholders (`_TBD_`, `TODO`) are either resolved or explicitly flagged as open questions.

## Quality Checklist

Before finalizing the review, verify:

- [ ] Every finding names the exact section, line, or asset it applies to.
- [ ] Every finding is actionable — the author can fix it without asking follow-up questions.
- [ ] Findings are grouped by severity, not by section.
- [ ] The report distinguishes structural gaps (missing sections) from content gaps (thin reasoning).
- [ ] The ADR itself is not modified.
- [ ] The final recommendation names the next skill or human step (usually `crosby-adr-revise`).

## Output Format

Emit the report in this exact structure. Keep prose tight and use lower-case, copy-pasteable bullets where possible.

### 🧭 Review Summary

- **ADR:** `docs/adrs/YYYYMMDD-slug.md`
- **Status observed:** PROPOSED 🟡 / ACCEPTED 🟢 / REJECTED 🔴
- **Overall verdict:** _one sentence — approve, revise, or reject with reason_.

### 🔴 Critical — Must Fix Before Circulation or Acceptance

- **[Section]** — Issue. Suggested action.

### 🟡 Recommended — Improves Quality, Not Merge-Blocking

- **[Section]** — Issue. Suggested action.

### 🟢 Minor — Nits and Future Polish

- **[Section]** — Issue. Suggested action.

### ❓ Open Questions for the Author

- Bulleted list of unresolved `_TBD_`s, missing owners, or assumptions the author must confirm.

### ➡️ Next Action

- If any Critical or Recommended items exist, hand off to `crosby-adr-revise` with the findings above as the feedback source.
- If the ADR is clean, state that it is ready for circulation (`PROPOSED`) or acceptance review.

---

**Constraint:** This skill is read-only. Do not edit the ADR, change its status, or create follow-up tickets. The output is a structured review; any changes are executed through `crosby-adr-revise` after the author reviews the findings.
