# One Paper, One Repo, One AI Project

This workflow sets up a durable research system for one paper.

> [!NOTE]
> Default add-on for this workflow: `If any required input, file permission, data rule, Git term, agent permission, or output format is unclear, ask me up to five clarifying questions before acting. Define unfamiliar technical terms in plain language and end with "Questions for you" if anything remains uncertain.`

## Principle

```text
One paper = one GitHub repo + one ChatGPT/Claude Project + one AI-use log + one data rule.
```

> [!IMPORTANT]
> This is the default workflow for serious research. Do not start with multiple agents, MCP connectors, or automation until this basic system is working.

## Project Setup Instructions

```text
Help me set up an AI-assisted research workspace for one economics/finance paper.

Paper/project:
- Title: [title]
- Field: [field]
- Coauthors: [yes/no]
- Data sensitivity: [public/licensed/restricted/private]
- Current stage: [idea/data/methods/results/draft/revision]
- Tools: [ChatGPT/Claude/Codex/Claude Code/Cursor/GitHub/etc.]

Create:
1. A project purpose statement.
2. A safe folder structure.
3. Project instructions for ChatGPT/Claude.
4. AGENTS.md instructions for coding agents.
5. AI-USE-LOG.md template.
6. DATA.md template.
7. A first-week task plan.
8. A verification checklist.

Rules:
- Do not upload restricted data.
- Do not invent citations or results.
- Keep human approval points before code edits, paper rewrites, and public sharing.
- Ask up to five clarifying questions before building the workspace if data sensitivity, coauthor rules, target output, or tool permissions are unclear.
- Define technical terms such as repo, project instructions, AGENTS.md, AI-use log, branch, and `.gitignore` in plain language.
```

## ChatGPT/Claude Project Instructions

```text
You are my AI research workspace for this paper.

Purpose:
Help organize, critique, draft, and verify research work. Do not replace scholarly judgment.

Rules:
- Never invent citations, data, results, robustness checks, institutional facts, or theoretical derivations.
- Separate facts, interpretation, suggestions, and uncertainty.
- Always state what I must verify manually.
- Preserve cautious causal language.
- Do not treat uploaded drafts as public.
- Do not summarize confidential or restricted material unless I confirm it is allowed.
- Ask for approval before editing code, rewriting paper text, changing file structure, or preparing public materials.
- Ask clarifying questions when project facts, data permissions, output expectations, or terminology are unclear.
- Explain technical terms briefly for non-CS economics/finance researchers.

Default output format:
1. Short answer.
2. Evidence or reasoning.
3. Risks/uncertainty.
4. Questions for you.
5. What I should do next.
```

## Quality Gate Before Accepting AI Output

```text
Before I accept this AI-assisted output, audit it.

Output:
[paste output]

Project facts:
[paste known facts]

Check:
1. Does it invent citations, facts, variables, data, results, or robustness checks?
2. Does it change causal language or contribution claims?
3. Does it match the code, tables, figures, or source documents?
4. Does it expose private, licensed, or restricted material?
5. Does it need coauthor, PI, journal, or data-provider approval?
6. What should be recorded in the AI-use log?

Return:
- accept / revise / reject
- required edits
- manual checks
- AI-use log entry
```

## Good Project Roles

- Literature Cartographer
- Tough Referee
- Empirical Design Critic
- Code Auditor
- Theory Intuition Checker
- Writing Coach
- Seminar Q&A Opponent
- Revision Strategy Assistant

## First Week Checklist

```text
Day 1: create repo, README, DATA.md, AI-USE-LOG.md, AGENTS.md.
Day 2: write project instructions for ChatGPT/Claude.
Day 3: run one small literature or code task with AI.
Day 4: verify output and record AI-use log.
Day 5: turn one repeated task into a skill.
```

Sources and workflow influences: ChatGPT/Claude Projects, Paul Goldsmith-Pinkham's one-research-pipeline framing, and PaperSpine-style stage separation.
