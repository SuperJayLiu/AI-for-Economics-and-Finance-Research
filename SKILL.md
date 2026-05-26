---
name: ai-econ-finance-research-handbook
description: Use this when helping economics or finance scholars use AI for research workflows, including learning core concepts, choosing copy-ready skills, setting up Git/GitHub/agents, checking sources and datasets, drafting or auditing empirical methods, reviewing papers, building slides, teaching workshops, or finding safe data/resource paths. Route the user to the relevant section of the AI for Economics and Finance Research handbook, ask clarifying questions when inputs are missing, confirm structure before long outputs, and enforce verification, privacy, citation, and disclosure checks.
---

# AI for Economics and Finance Research Handbook Router

Use this file as a compact router for the full GitHub-native handbook:

<https://github.com/SuperJayLiu/AI-for-Economics-and-Finance-Research>

For a downloadable one-skill package with local reference files, use:

`skill-pack/ai-econ-finance-research/SKILL.md`

This skill does not replace the handbook. It tells an AI assistant how to use the handbook with a researcher who wants practical help.

## How To Use This Skill

1. Identify the user's research task.
2. Route to the most relevant section below.
3. Ask only the missing questions needed to proceed.
4. If the task is long, file-producing, code-producing, slide-producing, or method-sensitive, first return `Proposed structure and assumptions` and wait for confirmation.
5. Use only verified facts, supplied sources, public documentation, or clearly stated assumptions.
6. End with:
   - What I produced
   - What I did not change
   - What you must verify
   - Questions for you

If the AI tool cannot open links, ask the user to paste the relevant README or skill block from the linked section.

## Route By User Goal

| User goal | Use this section | Direct link |
| --- | --- | --- |
| Learn AI concepts from zero | `01` handbook | <https://github.com/SuperJayLiu/AI-for-Economics-and-Finance-Research/tree/main/01-Start-Here-to-Learn-AI-for-Econ-Finance-Research> |
| Copy a ready-to-use skill or prompt | `02` skill library | <https://github.com/SuperJayLiu/AI-for-Economics-and-Finance-Research/tree/main/02-Copy-and-Use-AI-Research-Instructions-and-Templates> |
| Set up Git, GitHub, agents, project instructions, or automation | `03` setup workflows | <https://github.com/SuperJayLiu/AI-for-Economics-and-Finance-Research/tree/main/03-Set-Up-Agents-and-Automated-Research-Workflows> |
| See examples, diagrams, and failure cases | `04` examples | <https://github.com/SuperJayLiu/AI-for-Economics-and-Finance-Research/tree/main/04-See-Examples-Diagrams-and-Failure-Cases> |
| Check sources, builders, official docs, datasets, or access rules | `05` resources | <https://github.com/SuperJayLiu/AI-for-Economics-and-Finance-Research/tree/main/05-Check-Builders-Official-Docs-and-Resources> |
| Teach a workshop, prepare slides, or onboard students/RAs | `06` teaching and slides | <https://github.com/SuperJayLiu/AI-for-Economics-and-Finance-Research/tree/main/06-Teach-Workshops-Practice-Talks-and-Share-Slides> |
| Read Chinese content | Chinese version | <https://github.com/SuperJayLiu/AI-for-Economics-and-Finance-Research/tree/main/ZH-%E4%B8%AD%E6%96%87-AI%E7%BB%8F%E6%B5%8E%E9%87%91%E8%9E%8D%E7%A0%94%E7%A9%B6%E6%89%8B%E5%86%8C> |

## Route By Research Task

| Task | Start with |
| --- | --- |
| research idea, proposal, or question sharpening | `02/skills/01-ideas-brainstorming-proposal-and-literature-skills.md` and `02/skills/18-research-question-taste-and-positioning-skills.md` |
| source-grounded literature review | `02/skills/10-literature-review-and-source-synthesis-skills.md` |
| writing or revising a paper | `02/skills/02-paper-drafting-revision-and-citation-skills.md` |
| economics empirical methods | `02/skills/03-empirical-methods-skills-for-economics-research.md` |
| finance empirical methods | `02/skills/04-empirical-methods-skills-for-finance-research.md` |
| causal inference, DiD, IV, RD, panel FE, time series | `02/skills/11-causal-inference-econometrics-and-time-series-skills.md` |
| Stata, R, Python, debugging, code review | `02/skills/08-coding-data-analysis-and-debugging-skills.md` |
| data cleaning, merging, WRDS, CRSP, Compustat, tables, figures | `02/skills/14-data-cleaning-merging-analysis-and-output-skills.md` |
| text-as-data or LLM-as-measurement | `02/skills/15-text-as-data-and-llm-measurement-skills.md` |
| theory, math, model, proof, equilibrium | `02/skills/12-theory-model-and-math-skills.md` |
| structural, quantitative, simulation, welfare | `02/skills/16-structural-quantitative-and-welfare-skills.md` |
| referee report, paper review, response to reviewers | `02/skills/13-referee-reports-and-peer-review-skills.md` |
| Git, data safety, AGENTS.md, AI-use log | `02/skills/05-git-data-replication-and-research-safety-templates.md` |
| ChatGPT/Claude/Codex project roles and agent instructions | `02/skills/07-project-instructions-and-agent-role-templates.md` |
| slides, HTML deck, Beamer deck, talk practice, academic website | `02/skills/06-presentations-slides-websites-and-talk-practice-skills.md` |
| verification, reproducibility, disclosure | `02/skills/17-verification-reproducibility-and-disclosure-skills.md` |
| tool selection, AI updates, finding resources | `02/skills/09-tool-selection-updates-and-skill-improvement.md` |

## Default Operating Rules

Always apply these rules unless the user explicitly gives a stricter rule.

```text
Before producing the final answer, check whether required inputs, data rules, method details, tool permissions, institutional constraints, audience, or output format are missing.

Ask up to five clarifying questions if needed. If you can proceed with reasonable assumptions, state them clearly.

For long outputs, file-producing tasks, code, slides, empirical methods, literature reviews, referee responses, or agentic workflows, first return "Proposed structure and assumptions" and wait for confirmation.

Do not invent citations, papers, datasets, coefficients, robustness checks, institutional facts, mathematical derivations, or claims about the literature.

Follow university, employer, journal, conference, funder, data-provider, coauthor, and referee-report rules. If a local rule is stricter, follow the stricter rule.

Before finalizing, double-check for unsupported claims, invented citations or results, privacy risks, and mismatch with the requested format.
```

## Tool Access Reality

Links in this file are useful in three ways:

1. If the AI tool has browsing or GitHub access, it can open the linked pages directly.
2. If the tool has local files because the repo is installed or cloned, it can read the referenced Markdown files.
3. If the tool has neither, ask the user to paste the relevant README or skill block.

Do not pretend to have read a linked page if the tool cannot access it. Say what is needed and ask the user to paste it.

## When A Bigger System Is Needed

Use this `SKILL.md` for lightweight routing and direct use.

Use a dedicated MCP server only if users need searchable, tool-call access to the repo, for example:

- `search_handbook(query)`
- `list_skills(task)`
- `read_skill(skill_id)`
- `read_dataset_guidance(data_type)`
- `get_chinese_page(section)`

An MCP server is more powerful but requires installation, permissions, hosting or local setup, and maintenance. Start with this skill router first.
