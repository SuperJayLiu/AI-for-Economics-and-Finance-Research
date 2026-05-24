# Parallel Agents and Git Worktrees

Use this when you want several AI agents to work on different parts of a project without stepping on each other.

> [!WARNING]
> Parallel agents are useful only if each agent has a narrow task, its own branch or worktree, and a clear merge/review gate.

> [!NOTE]
> Default add-on for this workflow: `If any required input, file permission, data rule, Git term, agent permission, or output format is unclear, ask me up to five clarifying questions before acting. Define unfamiliar technical terms in plain language and end with "Questions for you" if anything remains uncertain.`

## When To Use

Good uses:

- one agent reviews methods prose while another checks code
- one agent builds slides while another audits citations
- one agent tests replication while another writes documentation
- one agent creates figures while another checks table labels

Bad uses:

- multiple agents editing the same manuscript section
- multiple agents changing the same data-cleaning pipeline
- agents touching restricted data without approval
- agents pushing directly to `main`

## Copy-Paste Workflow

```text
Help me set up parallel AI work safely using Git branches or worktrees.

Project:
[project description]

Tasks to split:
1. [task A]
2. [task B]
3. [task C]

Rules:
- Each agent gets one narrow task.
- Each agent works on a separate branch or worktree.
- No agent edits raw data.
- No agent pushes to main.
- Each agent must report files changed, commands run, outputs checked, and uncertainty.
- I will review diffs before merging.

First, propose:
1. branch/worktree names
2. task assignment
3. files each agent may edit
4. files each agent must not edit
5. validation command for each task
6. merge order and conflict risks
```

## Suggested Worktree Pattern

```text
main repo: project/

worktrees:
../project-methods-review
../project-code-audit
../project-slides
../project-replication-check
```

## Review Gate

Before merging any agent output:

```text
For this branch/worktree, summarize:
1. What changed?
2. Why was it changed?
3. What files were touched?
4. What commands were run?
5. What outputs changed?
6. What remains uncertain?
7. What should I inspect before merge?
```

Sources and workflow influences: Git worktree documentation, Claude Code parallel-agent/worktree patterns, and research project safety practices.
