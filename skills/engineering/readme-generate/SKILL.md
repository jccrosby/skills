---
name: generate-readme
description: 'Generates a comprehensive project README.md based on the local .ai brain and codebase analysis.'
---
SKILL: generate-readme

PROCEDURE

Analyze Context: Read ./.ai/project-context.md and ./.ai/global-standards.md to understand the project's purpose and tech stack.

Scan Codebase: Use ls -R or directory_tree MCP to identify key directories and entry points.

Structure Output: Create a README.md with the following sections:

Project Title: Clear and descriptive.

Overview: High-level value proposition.

Architecture: Mention the ./.ai brain and aisync workflow.

Tech Stack: Languages, frameworks, and tools.

Getting Started: Installation and run instructions.

Agent Interaction: Instructions on using AGENTS.md for AI collaboration.

KISS Check: Ensure the README is readable, concise, and lacks fluff.

CONSTRAINT

Do not include personal contact info.

Do not over-explain obvious setup steps (npm install, etc.) unless specialized.