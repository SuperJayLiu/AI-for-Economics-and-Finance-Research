# Check Builders, Official Docs, and Resources

This folder is not a link dump. It explains which external resources influenced the repo and what we extract from them.

> [!IMPORTANT]
> This page is for learning what to extract from outside sources. It is not a recommendation to copy another person's skill, code, or writing without checking license, attribution, and fit.

## Source Use Policy

We cite briefly and adapt only relevant workflow ideas. We do not copy external skills wholesale unless the license permits it.

Use this extraction rule:

```text
Source -> workflow pattern -> econ/finance adaptation -> copy-ready asset -> verification rule
```

## Source-to-Repo Map

| Source | What this repo extracts |
| --- | --- |
| [Paul Goldsmith-Pinkham: Applied Methods PhD](https://github.com/paulgp/applied-methods-phd) | practical empirical implementation, research design intuition, communication and artisanship |
| [Paul Goldsmith-Pinkham: Using AI in Research and Teaching](https://paulgp.com/2024/06/24/llm_talk.html) | VS Code/Git mindset, code explanation, scraping, Makefile/project help, local models for sensitive contexts |
| [Paul Goldsmith-Pinkham: Research in the Time of AI](https://paulgp.com/2026/03/16/research-in-time-of-ai.html) | research pipeline thinking, AI lowering execution costs, p-hacking and slop risks |
| [Paul Goldsmith-Pinkham: LLM-Friendly Academic Papers](https://paulgp.com/2026/03/10/llms-txt-for-academic-papers.html) | llms.txt-style paper orientation files, paper bundles, limitations-first AI reading |
| [Paul Goldsmith-Pinkham: Things I Want to Build](https://paulgp.com/2026/04/08/incomplete-list-things-i-want-to-build.html) | citation networks, knowledge databases, replication package metadata, better econometric tooling |
| [Paul Goldsmith-Pinkham: AI writing roundup](https://paulgp.com/2026/04/27/ai-writing-roundup.html) | writing help should preserve thinking, voice, evidence, and field-specific caution |
| [Paul Goldsmith-Pinkham: Tracking the Credibility Revolution across Fields](https://www.nber.org/papers/w35051) | field differences in empirical design language, especially applied micro vs finance/macroeconomics |
| [Paul Goldsmith-Pinkham: Causal Inference in Financial Event Studies](https://paulgp.com/papers/financial_event_studies_dec282025.pdf) | event-study caution, especially long horizons, confounding, and design-vs-model interpretation |
| [Pedro Sant'Anna: Claude Code academic workflow](https://psantanna.com/claude-code-my-workflow/) | plan-first contractor workflow, specialized agents, quality checks, reusable commands |
| [Chris Blattman / Claude Blattman](https://claudeblattman.com/) | non-coder academic workflows, project folders, reusable skills, council-of-critics style review |
| [Anton Korinek: AI agents for economic research](https://www.nber.org/papers/w34202) | economist-facing explanation of agents for literature, code, data, and workflow coordination |
| [Mihail Velikov: AI in Business and Economic Research](https://velikov-mihail.github.io/ai-econ-wiki/) | curated source index, summaries, categories, and knowledge-base maintenance |
| [Novy-Marx and Velikov: AI-powered finance scholarship](https://www.aeaweb.org/articles?id=10.1257/jel.20251821) | caution about industrialized finance paper production, HARKing, and factor-mining incentives |
| [Joshua Gans](https://joshuagans.substack.com/) | AI's effect on research and teaching production, course-specific AI assistants |
| [Luis Garicano](https://sites.google.com/site/luisgaricano/) | AI, knowledge work, task bundling, and the changing value of human judgment |
| [Aniket Panjwani](https://aniketpanjwani.com/) | practical economist-facing agent onboarding and dated tool-comparison discipline |
| [Zara Zhang: AI Learning Library](https://zara.faces.site/ai) | curated learning paths and low-noise AI learning |
| [Zara Zhang: Follow Builders](https://github.com/zarazhangrui/follow-builders) | builder-focused digest, daily/weekly updates, bilingual summaries, public-source tracking |
| [Zara Zhang: frontend-slides](https://github.com/zarazhangrui/frontend-slides) | web-native slide skills, visual exploration, single-file HTML artifacts, avoiding generic AI aesthetics |
| [Maverick Gao: slide-craft-skill](https://github.com/maverickgao8848/slide-craft-skill) | structured slide workflow, style choices, overflow handling, bilingual slide-skill design |
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

## Builder Extraction Card

Use this card when adding a new source.

```markdown
## Source: [name]

Link:
Type: official docs / economist workflow / skill repo / course / blog / paper
Level: beginner / intermediate / advanced

What they built or taught:

Reusable workflow pattern:

How this changes economics/finance research practice:

What to adapt into this repo:

What not to copy blindly:

License or attribution notes:

Last checked:
```

## Missing Topics To Keep Watching

These are not fully settled and should be updated carefully:

| Topic | Why it matters | What to watch |
| --- | --- | --- |
| AI disclosure policies | journal, conference, funder, and university rules differ | official policy pages and publisher updates |
| local/private models | sensitive data may require local or approved tools | institutional guidance, model quality, security rules |
| AI coding agents | capabilities and costs change quickly | official docs, hands-on tests, GitHub issue patterns |
| MCP security | connectors increase permissions and data exposure | official MCP docs and security advisories |
| AI-generated finance research | paper production may scale faster than review standards | finance methodology, replication, and p-hacking discussions |
| AI for teaching | course assistants and study tools are improving | student privacy, academic integrity, instructor controls |
