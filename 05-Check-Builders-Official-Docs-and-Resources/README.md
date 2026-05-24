# Check Builders, Official Docs, and Resources

This folder is not a link dump. It explains which external resources influenced the repo and what we extract from them.

## Source Use Policy

We cite briefly and adapt only relevant workflow ideas. We do not copy external skills wholesale unless the license permits it.

## Source-to-Repo Map

| Source | What this repo extracts |
| --- | --- |
| [Paul Goldsmith-Pinkham: Applied Methods PhD](https://github.com/paulgp/applied-methods-phd) | practical empirical implementation, research design intuition, communication and artisanship |
| [Paul Goldsmith-Pinkham: Using AI in Research and Teaching](https://paulgp.com/2024/06/24/llm_talk.html) | VS Code/Git mindset, code explanation, scraping, Makefile/project help, local models for sensitive contexts |
| [Paul Goldsmith-Pinkham: Research in the Time of AI](https://paulgp.com/2026/03/16/research-in-time-of-ai.html) | research pipeline thinking, AI lowering execution costs, p-hacking and slop risks |
| [Paul Goldsmith-Pinkham: LLM-Friendly Academic Papers](https://paulgp.com/2026/03/10/llms-txt-for-academic-papers.html) | llms.txt-style paper orientation files, paper bundles, limitations-first AI reading |
| [Paul Goldsmith-Pinkham: Things I Want to Build](https://paulgp.com/2026/04/08/incomplete-list-things-i-want-to-build.html) | citation networks, knowledge databases, replication package metadata, better econometric tooling |
| [Zara Zhang: AI Learning Library](https://zara.faces.site/ai) | curated learning paths and low-noise AI learning |
| [Zara Zhang: Follow Builders](https://github.com/zarazhangrui/follow-builders) | builder-focused digest, daily/weekly updates, bilingual summaries, public-source tracking |
| [PaperSpine](https://github.com/WUBING2023/PaperSpine) | staged academic writing skills, branch skills, citation support bank, writing rationale matrix, audit trail |
| [Nature Skills](https://github.com/Yuan1z0825/nature-skills) | source-grounded skill design, directly usable artifacts, journal-style rules |
| [OpenAI Codex Skills](https://developers.openai.com/codex/skills) | skills as reusable instruction packages |
| [OpenAI AGENTS.md](https://developers.openai.com/codex/guides/agents-md) | repo-level AI agent instructions |
| [Claude Skills](https://docs.claude.com/en/docs/claude-code/skills) | skill format and Claude Code workflow concept |
| [Model Context Protocol](https://modelcontextprotocol.io/docs/getting-started/intro) | connectors between AI tools and external systems |
| [GitHub ignoring files](https://docs.github.com/en/get-started/git-basics/ignoring-files) | `.gitignore` safety for data and secrets |
| [Git worktree docs](https://git-scm.com/docs/git-worktree) | isolated branches/worktrees for AI experiments |

## Resource Inclusion Criteria

Add a resource only if it does at least one of these:

- teaches a reusable workflow
- gives official tool behavior
- is directly relevant to economics/finance research
- provides working code or a reproducible example
- explains risks, limitations, or failures
- helps scholars build skills rather than chase tools

Exclude or mark cautiously:

- generic tool rankings
- "write a paper in one hour" claims
- unsupported model comparisons
- advice that ignores privacy, Git, or verification

## Tool Claims Must Be Dated

Use this format for any tool comparison:

```text
Last checked:
Tool versions/plans checked:
Task tested:
Author's judgment:
Known uncertainty:
```

Do not write timeless claims such as "Codex is best" or "Claude is best." Write task-specific, dated claims.

## Learning From Builders

Extract:

- what they built
- what workflow problem it solves
- what inputs it needs
- what output artifact it produces
- what risks remain
- what must be adapted for economics/finance

Do not simply collect personalities.
