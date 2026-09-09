# Language-simplify

## What it does

This skill rewrites a user prompt in clear, direct language. It keeps the task, requirements, examples, and technical details intact.

The skill simplifies wording without reducing the prompt's scope. It also flags unclear instructions that could change the result.

## When to use it

You invoke this skill by typing `/language-simplify`, and the agent will not reach for it on its own.

Reach for it when a prompt feels long, vague, repetitive, technical, or difficult to scan. For a new workflow, use [plan-iterative](../../engineering/jccrosby-plan-iterative/README.md) instead.

## What it preserves

The skill keeps code, commands, paths, URLs, identifiers, placeholders, quoted text, formats, and literal values unchanged. It removes filler and repetition only when they add no meaning.

It follows plain-language rules based on ASD-STE100 and Federal Plain Language Guidelines. The result targets an 8th-grade reading level, short sentences, active voice, and concrete words.

## It's working if

- The prompt keeps its original goal and required actions.
- The wording feels shorter, clearer, and easier to scan.
- Technical terms remain accurate or receive a useful definition.
- Code, commands, paths, URLs, and placeholders remain unchanged.
- The skill flags ambiguity instead of guessing.

## Where it fits

This skill works as a standalone rewrite step before another prompt-driven task.
