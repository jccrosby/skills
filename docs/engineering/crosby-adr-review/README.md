# Review ADR

## Purpose

Use this skill to review an existing architectural decision record for comprehensiveness, completeness, clarity, simple language, and correct organization of supporting assets. The skill is read-only and produces a structured report; it does not edit the ADR.

## When to use it

Use it when:

- a PROPOSED ADR is about to be circulated for approval,
- an ADR is being considered for acceptance,
- an existing ADR may be stale, incomplete, or unclear,
- or you want a structured critique before handing feedback to the author.

## When not to use it

Do not use it for:

- drafting a new ADR; use the `crosby-adr-create` skill instead,
- applying changes to an ADR; use the `crosby-adr-revise` skill instead,
- reviewing implementation code that follows from an ADR,
- or general documentation review that is not a decision record.

## Workflow

1. Confirm the ADR path, review focus, audience, and any related ADRs.
2. Read the ADR in full and open every referenced ADR, ticket, image, and link.
3. Check the file location and filename against the project convention.
4. Compare the ADR against the template owned by `crosby-adr-create`.
5. Apply the four review criteria: structural completeness, comprehensiveness, clarity, and supporting assets.
6. Group findings by severity and return the report.
7. Recommend the next action, usually a hand-off to `crosby-adr-revise`.

## Review criteria

Check for:

- structural completeness against the required ADR template,
- comprehensiveness of context, rationale, options considered, consequences, and next steps,
- clarity and simple language, including active voice and consistent terminology,
- and correct organization of supporting assets such as filenames, image paths, and references.

## Output structure

Return a report with:

1. Review summary with ADR path, observed status, and overall verdict
2. Critical findings that must be fixed before circulation or acceptance
3. Recommended findings that improve quality but do not block
4. Minor findings and nits
5. Open questions for the author
6. A next action, typically a hand-off to `crosby-adr-revise`

## Good practice

- Point every finding at a specific section, line, or asset.
- Separate structural gaps from content gaps.
- Prefer actionable suggestions the author can apply without follow-up questions.
- Keep the ADR untouched; hand changes off to the revise skill.

## Common pitfalls

- Editing the ADR instead of reporting on it.
- Restating the ADR template rather than checking against it.
- Mixing structural issues with wording nits at the same severity.
- Missing supporting assets, such as broken image paths or dead links.
- Approving an ADR that has an empty cons section or invented references.
