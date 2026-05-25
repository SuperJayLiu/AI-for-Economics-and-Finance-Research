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

## Concrete Split Example

Suppose a paper needs a revision package.

| Agent | Branch/worktree | Allowed files | Forbidden files | Check |
| --- | --- | --- | --- | --- |
| methods reviewer | `revise-methods` | `paper/methods.tex`, `paper/appendix.tex` | `data/`, `code/` | compare prose to equation and table shell |
| code auditor | `audit-table2-code` | `code/table2.*`, `output/logs/` | `data/raw/`, `paper/` | run Table 2 script and toy test |
| slide builder | `seminar-slides` | `slides/`, `output/figures/` copies only | `data/`, `code/` | check each slide claim against paper |

Merge order:

1. code auditor first, because methods and slides should reflect code;
2. methods reviewer second;
3. slide builder last.

Conflict risk:

- methods and slides may both refer to Table 2;
- no two agents should edit the same manuscript file at the same time;
- no agent should edit raw or licensed data.

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
