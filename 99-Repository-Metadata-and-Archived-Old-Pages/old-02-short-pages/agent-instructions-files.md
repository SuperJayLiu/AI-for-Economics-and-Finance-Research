> Copyright (c) 2026 SuperJayLiu (Chaojie Liu). Licensed under the repository MIT License.
> This instruction/workflow is original to this repository unless otherwise noted. External inspirations are cited in “Sources and workflow influences.”

# Agent Instruction Files

## What Problem This Solves

AI agents need project-specific rules. Without them, they may edit the wrong files, mishandle data, or skip verification.

## Recommended Files

| File | Purpose |
| --- | --- |
| `AGENTS.md` | Instructions for coding agents working in the repo |
| `CLAUDE.md` | Claude-specific project rules if using Claude Code |
| `PROJECT.md` | Human-readable project purpose, folder structure, and workflow |
| `RESEARCH_LOG.md` | Research decisions and AI-use notes |
| `DATA.md` | Data sources, access rules, restrictions, and construction notes |

## Minimum `AGENTS.md` Content

- project purpose
- folder structure
- commands to run
- files never to edit
- data privacy rules
- validation steps
- commit and logging expectations

## Sources and Workflow Influences

Draws on official Codex custom instruction guidance, AGENTS.md documentation, GitHub repository custom instruction docs, and academic AI workflow practices.

Last checked: 2026-05-24
