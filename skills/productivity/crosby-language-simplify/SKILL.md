---
name: crosby-language-simplify
description: 'Simplify the language of a user-provided prompt while preserving its intent, requirements, technical accuracy, and important details.'
argument-hint: '<prompt to simplify>'
---

# SKILL: crosby-language-simplify

## When to Use

Use this skill when a prompt needs clearer, shorter, or more direct language.

Use it for prompts that contain:

- long or difficult sentences,
- vague or abstract wording,
- passive voice or unnecessary jargon,
- repeated ideas or filler, or
- instructions that users may misread.

Do not use it to change the task, add requirements, summarize the prompt, or rewrite code.

## Procedure

1. Read the complete prompt and identify its goal, audience, constraints, inputs, outputs, and success criteria.
2. Separate instructions from examples, quoted text, code, commands, file paths, URLs, identifiers, and literal values.
3. Rewrite the instructions with plain, direct language.
4. Keep the original order when it helps the reader follow the task.
5. Use headings and bullets when they improve scanning.
6. Remove repetition, filler, hype, idioms, and vague wording.
7. Keep technical terms when they carry exact meaning. Define terms that the intended reader may not know.
8. Preserve every requirement, condition, exception, example, and output format unless the user asks to remove it.
9. Check the result against the quality checks below.
10. Return the simplified prompt. Add a short note only when the original prompt contains an ambiguity that could change the result.

## Simple Language Rules

Apply the rules in `./simple-language-rules.md`. The core rules are:

- Target an 8th-grade reading level.
- Follow ASD-STE100 Simplified Technical English and Federal Plain Language Guidelines.
- Keep each sentence to 20 words or fewer.
- Keep each paragraph to three sentences or fewer.
- Keep noun groups to three consecutive nouns or fewer.
- Use active voice when the actor remains known.
- Minimize forms of "to be".
- Use concrete nouns and strong verbs.
- Avoid flowery language, filler, hype, and abstract wording.
- Avoid these cliches: `delve`, `tapestry`, `multifaceted`, `testament`, `dynamic`, `leverage`, `paramount`, `non-trivial`, `holistic`, `seamless`, `foster`, `overarching`, `synergy`, `landscape`, `pivotal`, `intricate`, and `robust`.

## Preservation Rules

- Keep code, commands, paths, URLs, identifiers, placeholders, and quoted text unchanged unless the user asks otherwise.
- Keep required output formats, schemas, headings, and field names unchanged.
- Keep the prompt's scope and level of detail. Make wording simpler, not the task smaller.
- Do not invent context, definitions, requirements, or examples.
- Do not remove a detail only because it seems repetitive. Remove it only when it repeats the same instruction without adding meaning.
- Flag conflicts or unclear references. Do not resolve them by guessing.

## Output Format

Return the rewritten prompt in a code block when the prompt includes formatting that the user must copy. Otherwise, return the rewritten prompt as plain Markdown.

If you need to flag an ambiguity, append:

`Note: [brief description of the ambiguity and the decision it may affect.]`

## Quality Checks

- The rewritten prompt keeps the original goal and all required actions.
- The rewritten prompt contains no unsupported facts or new requirements.
- The sentences use plain words and direct verbs.
- The prompt scans quickly through useful headings or bullets.
- Code, commands, paths, URLs, identifiers, placeholders, and quoted text remain unchanged.
- The result reads more clearly than the input without losing technical precision.
