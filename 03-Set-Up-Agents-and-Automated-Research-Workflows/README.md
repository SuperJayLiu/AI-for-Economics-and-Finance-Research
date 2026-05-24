# Set Up Agents and Automated Research Workflows

This folder is for multi-step workflows where AI may plan, edit files, run code, inspect outputs, or monitor updates.

Use these only after reading the [handbook](../01-Start-Here-to-Learn-AI-for-Econ-Finance-Research/README.md) and setting up Git.

## Files

| File | Use it for |
| --- | --- |
| [01 Clean Existing Research Project and Set Up Git](01-clean-existing-research-project-and-set-up-git.md) | turn a messy folder into a safe repo |
| [02 One Paper, One Repo, One AI Project](02-one-paper-one-repo-one-ai-project.md) | set up a durable AI workspace for a paper |
| [03 Replication Package Agent Workflow](03-replication-package-agent-workflow.md) | inspect, run, and document replication packages |
| [04 AI Research Update Digest Workflow](04-ai-research-update-digest-workflow.md) | build a low-noise update system from official docs and builders |

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
