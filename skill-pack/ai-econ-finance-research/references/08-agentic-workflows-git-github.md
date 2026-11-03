# Agentic Workflows, Git, GitHub, And Collaboration

Use this before AI edits files, runs code, or collaborates with coauthors/RAs.

## Zero-To-Agentic Setup

Guide the user through:

1. create GitHub account;
2. create private research repo;
3. add `.gitignore`;
4. add `README.md`, `DATA.md`, `AGENTS.md` or `CLAUDE.md`, and `AI-USE-LOG.md`;
5. create a branch;
6. ask AI for a plan;
7. approve or revise plan;
8. let AI edit files only after approval;
9. review diff;
10. run code/checks;
11. commit;
12. push;
13. open pull request for coauthor or RA review if collaborating.

## Collaboration Rules

Distinguish a fresh execution session from an independent review. When authorized and useful, give a read-only reviewer the plan/artifact, research contract, and safe validation inputs without the implementation conversation or preferred verdict. Record findings with evidence. Acceptance also requires reconciling the diff, filter counts, keys, merges, and final estimation sample; agreement between agents is insufficient. A human or separate chat can perform the review.

Ask who is responsible for:

- uploading data;
- approving AI-generated code;
- checking claims and citations;
- reviewing pull requests;
- merging changes;
- recording AI use;
- deciding whether confidential materials can be used.

## Copy-Ready Instruction

```text
Act as a Git, GitHub, and agentic workflow assistant for an economics/finance research project.

First ask what project stage I am in, whether a Git repo exists, what files are sensitive, who is collaborating, and what commands/checks are available.

Before editing files, inspect the project structure, propose a plan, identify files that must not be touched, and wait for approval.

After changes, summarize the diff, run or specify checks, update the AI-use log, and state what I must verify before commit or pull request.
```

## Required Guardrails

- never use destructive Git commands unless explicitly approved;
- never expose raw/restricted/licensed data;
- use branches for experiments;
- use pull requests for coauthor/RA review;
- use worktrees only when the user understands multiple working directories.

## Sources and Workflow Influences

Manish Jha, Georgia State University, [AI for Finance Research](https://mjha91.github.io/pdf/AIFinanceResearch.pdf), cover 2026-10-30; accessed 2026-11-03. Influence: independent review and sample/diff evidence in the existing plan workflow. No explicit reuse license found on author page/PDF; original high-level adaptation only. No lecture wording, prompts, templates, figures, or presentation structure copied; lecture is outside the repository MIT license.
