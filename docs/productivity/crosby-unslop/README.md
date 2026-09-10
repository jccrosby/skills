# Unslop

## What it does

This skill edits writing to remove recognizable AI-generated patterns while preserving the meaning and intended tone. It checks wording, punctuation, structure, and filler, then rewrites the text in plain, direct language.

It works on existing text rather than generating a new message from scratch. The skill preserves the writer's point and fixes the patterns that make the text feel machine-written.

## When to use it

You invoke this skill by typing `/crosby-unslop`, and the agent will not reach for it on its own.

Reach for it when a draft sounds generic, over-polished, repetitive, or recognizably AI-generated. For a prompt that needs clearer requirements or narrower scope, use [crosby-prompt-create](../crosby-prompt-create/README.md) instead.

## What it checks

The skill looks for patterns such as vague attributions, inflated vocabulary, forced lists, synonym cycling, em dash overuse, decorative formatting, chatbot phrases, filler, hedging, jargon, and passive or mannered prose.

It also checks whether each sentence gives the reader a concrete fact, instruction, or number. That check keeps the rewrite focused on what the text says rather than how it feels.

## It's working if

- The draft keeps its original meaning and intended tone.
- The prose uses specific, ordinary words instead of stock AI vocabulary.
- Sentences state facts or instructions without filler, vague attribution, or unnecessary hedging.
- Formatting and punctuation support the text instead of drawing attention to themselves.

## Where it fits

This skill is a standalone cleanup step that you can apply after drafting and before sharing or publishing text. Use [crosby-language-simplify](../crosby-language-simplify/README.md) when the main problem is a difficult or overlong prompt, rather than AI writing patterns.
