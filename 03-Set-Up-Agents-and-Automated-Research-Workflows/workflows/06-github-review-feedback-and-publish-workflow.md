# GitHub Review Feedback and Publish Workflow

Use this when a research repo, code package, paper repository, or handbook contribution has review comments to address or changes to publish.

> [!WARNING]
> GitHub writes are public or team-visible in many repositories. Do not reply, resolve threads, push, or open a PR until you understand scope, branch, repository visibility, and data sensitivity.

Questions or suggestions for this part: email [jay.liu@bristol.ac.uk](mailto:jay.liu@bristol.ac.uk) with subject `[AI Econ Finance GitHub Workflow] Question`.

> [!NOTE]
> Default add-on for this workflow: `If any required input, repository visibility, branch, PR status, file permission, data rule, or output format is unclear, ask me up to five clarifying questions before acting. Define unfamiliar technical terms in plain language and end with "Questions for you" if anything remains uncertain.`

## Workflow 1: Address Review Comments Safely

```text
Help me address GitHub review comments on this research project.

Context:
- Repository: [repo]
- PR or branch: [PR/branch]
- Review comments: [paste or summarize]
- Data sensitivity: [public/private/restricted]
- What I want changed: [scope]

First, do not edit files. Triage comments:
1. Group comments by file, paper section, or behavior area.
2. Separate actionable requests from informational comments, duplicates, and already-resolved issues.
3. Identify conflicts between comments.
4. Identify comments that need code, text, documentation, data, or reply-only action.
5. Ask for approval before editing.

After approval:
1. Implement only selected fixes.
2. Keep each change traceable to a comment cluster.
3. Run relevant checks.
4. Summarize comments addressed, comments left open, files changed, checks run, and uncertainty.

Rules:
- Do not reply publicly unless I ask.
- Do not resolve threads unless I ask.
- Do not stage unrelated changes.
- Do not push until I approve.
```

## Workflow 2: Publish Local Changes Intentionally

```text
Help me publish local research-repo changes to GitHub safely.

Before doing anything:
1. Show git status.
2. Summarize changed files.
3. Identify unrelated or risky changes.
4. Ask which files belong in the commit if scope is mixed.

Then:
1. Stage only intended files.
2. Commit with a terse message.
3. Run the relevant checks if not already run.
4. Push the branch.
5. Open a draft PR unless I explicitly ask to push directly to main.

PR body should include:
- what changed
- why it changed
- research/user impact
- checks run
- remaining risks

Rules:
- Never stage unrelated changes silently.
- Never push private, restricted, licensed, or identifiable data.
- Default to draft PR for collaborative review.
```

## Workflow 3: Research Repo PR Checklist

```text
Before opening a research PR, check:

- Does `.gitignore` exclude raw, restricted, licensed, private, and large data?
- Do files changed match the intended task?
- Can the main script still run?
- Do generated tables/figures match the paper text?
- Are AI-assisted changes logged?
- Did AI alter citations, coefficients, notation, claims, or limitations?
- Are coauthors aware if shared manuscript text changed?
- Does the PR description explain research impact, not only file changes?
```

Sources and workflow influences: the repository author's GitHub review-comment and publishing skills, GitHub PR review practice, and research reproducibility norms.
