# Set Up Agents and Automated Research Workflows

This folder is for multi-step workflows where AI may plan, edit files, run code, inspect outputs, or monitor updates.

Use these only after reading the [handbook](../01-Start-Here-to-Learn-AI-for-Econ-Finance-Research/README.md) and setting up Git.

Questions or suggestions for this part: email [jay.liu@bristol.ac.uk](mailto:jay.liu@bristol.ac.uk) with subject `[AI Econ Finance Automation] Workflow question`.

## Files

| File | Use it for |
| --- | --- |
| [01 Clean Existing Research Project and Set Up Git](01-clean-existing-research-project-and-set-up-git.md) | turn a messy folder into a safe repo |
| [02 One Paper, One Repo, One AI Project](02-one-paper-one-repo-one-ai-project.md) | set up a durable AI workspace for a paper |
| [03 Replication Package Agent Workflow](03-replication-package-agent-workflow.md) | inspect, run, and document replication packages |
| [04 AI Research Update Digest Workflow](04-ai-research-update-digest-workflow.md) | build a low-noise update system from official docs and builders |
| [05 Parallel Agents and Git Worktrees](05-parallel-agents-and-git-worktrees.md) | run multiple AI tasks safely without corrupting the main project |
| [06 GitHub Review Feedback and Publish Workflow](06-github-review-feedback-and-publish-workflow.md) | handle PR comments, stage changes intentionally, commit, push, and open PRs safely |

## Pick the Right Workflow

| Situation | Best workflow | Be careful about |
| --- | --- | --- |
| messy old folder | clean project and Git setup | never delete files or commit restricted data |
| one active paper | one paper, one repo, one AI project | define project instructions before file edits |
| replication package | replication package agent workflow | do not claim success until code runs and outputs match |
| staying updated | research update digest | dated claims, official docs, and low-noise sources |
| multiple AI tasks | branches/worktrees | agents editing same file or raw data |
| GitHub feedback | review feedback and publish workflow | never reply, resolve, or push without approval |

## Agent Rule

For any agentic workflow:

```text
Plan first. Ask before changing files. Use Git. Run checks. Report uncertainty.
```

## Automation Levels

| Level | Name | Example |
| --- | --- | --- |
| 0 | manual | scholar reads and writes alone |
| 1 | guided chat | AI explains a method or critiques a paragraph |
| 2 | project workspace | ChatGPT/Claude Project for one paper |
| 3 | repo-aware assistant | Codex/Claude Code works inside a Git repo |
| 4 | semi-automation | AI runs scripts, checks outputs, drafts logs |
| 5 | human-in-the-loop agent | AI plans and executes, scholar approves gates |

Do not use level 4 or 5 for confidential or restricted data unless the environment is approved.

## Required Safety Gates

Every automation workflow should have these gates.

```text
Gate 1: Plan
- What will the agent do?
- Which files may it touch?
- Which files are forbidden?
- What checks will prove it worked?

Gate 2: Approval
- Human approves before file edits, data movement, public sharing, or GitHub writes.

Gate 3: Verification
- Run code, compile paper/slides, inspect diffs, compare outputs, or verify sources.

Gate 4: Trace
- Record files changed, commands run, outputs checked, uncertainty, and commit hash.
```

## Tool Concepts

| Tool concept | Use in research | Risk |
| --- | --- | --- |
| `AGENTS.md` | repo-level instructions for Codex and other coding agents | vague rules lead to unsafe edits |
| `CLAUDE.md` | Claude Code project memory/instructions | stale or overly broad instructions |
| Skills | repeatable procedures for common tasks | weak skills can automate mistakes |
| MCPs | connect AI tools to apps, files, databases, or services | permissions, tokens, privacy, accidental actions |
| Git branches | isolate experiments | branch drift and merge conflicts |
| Worktrees | run parallel branches in separate folders | confusion if outputs are mixed |
| GitHub PRs | review and discuss changes | public/private boundary and accidental disclosure |

## University and Institution Rules

Before using automation, check your university, employer, funder, data provider, journal, conference, and coauthor policies. If a policy says a task cannot use external AI tools, do not use external AI tools for that task. When in doubt, use synthetic examples, local approved environments, or ask the relevant authority.
