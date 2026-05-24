# Prompts Projects Skills Agents MCPs And GitHub Repos

## What Problem This Solves

Scholars often confuse one-time prompts, persistent projects, reusable skills, agents, connectors, and GitHub repositories. The result is either too much chatting and no reusable workflow, or too much automation before the project is safe.

## Fast Distinction

| Concept | Meaning for scholars | Use it when |
| --- | --- | --- |
| Prompt | One-time instruction | the task is small and will not repeat |
| Project | Persistent workspace for a paper, dataset, talk, course, or recurring task | context and rules should stay stable |
| Skill | Reusable procedure for a repeated task | the same task happens more than twice |
| Agent | AI system that plans and uses tools | the task needs file edits, commands, search, or multi-step execution |
| MCP | Connector between AI and external apps or data | AI needs controlled access to tools, databases, calendars, files, or services |
| GitHub repo | Version-controlled research workspace | files, code, paper, data documentation, and AI changes must be traceable |
| Project instruction file | Instructions for AI working inside the repo | coding agents need project-specific rules |
| Worktree | Separate checkout of the same repo | an agent should edit in isolation without disturbing your main working copy |

## Practical Rule

Use prompts for one-off tasks, projects for ongoing context, skills for repeated workflows, agents for tool-using execution, MCPs for connections, and GitHub for traceability.

## MCPs vs Skills

MCPs and skills solve different problems.

| Question | Prefer MCP | Prefer skill |
| --- | --- | --- |
| Does AI need to connect to another app or database? | yes | no |
| Does AI need a reusable procedure or checklist? | no | yes |
| Is the risk mainly permission and data exposure? | yes | sometimes |
| Is the risk mainly vague instructions or inconsistent output? | sometimes | yes |
| Does the workflow need small, copyable instructions? | sometimes | yes |
| Can long connector context waste tokens? | yes | no |

MCPs are connection infrastructure. Skills are task procedures. A good research workflow can use both: MCP for controlled access, skill for how to behave once access exists.

## Copy-And-Use: Decide What To Build

```text
I need to turn this research task into the right AI workflow object.

Task:
[DESCRIBE TASK]

Frequency:
[ONE-OFF / WEEKLY / EVERY PAPER / EVERY COURSE]

Inputs:
[FILES, DATA, PAPERS, CODE, EMAILS, CALENDAR, WEB]

Risk level:
[PUBLIC / INTERNAL / CONFIDENTIAL / RESTRICTED]

Needed actions:
[READ / WRITE / RUN CODE / SEARCH WEB / CONNECT TO APP / CREATE FILES]

Please decide whether this should be a prompt, project instruction, reusable skill, agent task, MCP-enabled workflow, GitHub repo rule, or combination.

For each recommendation, give:
- why this object fits,
- what the copyable instruction should contain,
- what permissions are needed,
- what a human must verify,
- what should be logged.
```

## Default Project Roles For Research

| Role | Use for | Main warning |
| --- | --- | --- |
| Prompt engineering assistant | turning vague requests into reusable workflows | do not optimize for cleverness over verification |
| Tough referee | finding weaknesses in identification, theory, contribution, and writing | do not accept invented citations or generic criticism |
| Paper summarizer | controlled paper notes and literature maps | verify against the PDF |
| Idea verification assistant | feasibility, novelty, data, and mechanism checks | search does not prove novelty |
| Code reviewer | explaining, testing, and refactoring code | require Git diff and runnable checks |
| Data steward | writing data lineage notes and privacy rules | never upload restricted data without approval |
| Presentation coach | slide outline, Q&A, and talk practice | avoid overclaiming results |

## GitHub Rule

If AI can edit files, the project should use Git. If AI can restructure a project, use a new branch or worktree. If AI can run code, it must report commands, outputs, and differences from prior results.

## Sources and Workflow Influences

Draws on official OpenAI, Anthropic, MCP, GitHub, and Git documentation; builder workflows emphasizing skills, plans, worktrees, and repo-specific instructions; and Paul Goldsmith-Pinkham's VS Code/Copilot-oriented examples for research and teaching workflows.

Last checked: 2026-05-24
