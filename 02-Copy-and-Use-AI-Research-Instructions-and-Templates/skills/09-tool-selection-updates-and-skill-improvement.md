> Copyright (c) 2026 SuperJayLiu (Chaojie Liu). Licensed under the repository MIT License.

# Tool Selection, Updates, and Skill Improvement

Use these when deciding what to learn, which tool to use, and whether a new AI update matters.

> [!NOTE]
> Default add-on for any block on this page: `If any required input, term, method detail, data rule, or output format is unclear, ask me up to five clarifying questions before giving the final output. Define unfamiliar technical terms in plain language. After producing output, state what changed, what did not change, and what the researcher must verify. End with "Questions for you" if anything remains uncertain.`

## Skill 1: Dated Tool Choice for a Research Task

```text
Help me choose an AI tool for this economics/finance research task.

Task:
[describe task]

Constraints:
- Data sensitivity: [public/licensed/restricted/private]
- Files involved: [PDF/code/data/LaTeX/slides]
- Need code execution? [yes/no]
- Need web search? [yes/no]
- Need GitHub/file editing? [yes/no]
- Budget or subscription constraints: [constraints]
- My technical level: [beginner/intermediate/advanced]

Compare only tools you can evaluate for this task. Use dated claims.

Return:
1. Recommended tool/workflow.
2. Why it fits the task.
3. Tools not recommended and why.
4. Privacy/security concerns.
5. Verification burden.
6. Last checked date.
7. What could make this recommendation outdated.

Rules:
- Do not say one tool is universally best.
- Do not use model rankings without task-specific reasoning.
- If current information is needed, ask to search official docs.
```

## Skill 2: AI Information Diet

```text
Design a low-noise AI information diet for an economics/finance scholar.

My goals:
[goals]

Fields:
[fields]

Tools I use:
[tools]

Time budget per week:
[minutes]

Create:
1. Official docs to follow.
2. Academic AI workflow builders to follow.
3. Economics/finance AI sources to follow.
4. GitHub repos to watch.
5. Things to ignore.
6. A weekly review ritual.
7. A template for deciding whether to adopt a new tool or skill.

Principle:
Follow builders and official docs. Extract workflows, not opinions.
```

## Skill 3: Continuous Skill Improvement Loop

```text
Help me improve one of my AI research skills.

Current skill:
[paste skill]

Evidence from use:
- What worked: [notes]
- What failed: [notes]
- Repeated edits I made manually: [notes]
- Missing inputs: [notes]
- Bad outputs: [notes]

Improve the skill by:
1. Clarifying trigger/use case.
2. Adding required inputs.
3. Adding step-by-step procedure.
4. Tightening output contract.
5. Adding failure modes.
6. Adding verification checklist.
7. Removing vague language.

Return:
- revised skill
- change log
- test case to try next
```

## Skill 4: Bad AI Advice Filter

```text
Evaluate this AI advice for economics/finance researchers.

Advice/source:
[paste]

Check:
1. Is it for research, coding, business, marketing, or general productivity?
2. Does it include a real workflow?
3. Does it protect privacy and reproducibility?
4. Does it require paid tools or hidden infrastructure?
5. Does it increase verification burden?
6. Does it make unsupported tool claims?
7. Does it apply to economics/finance research?
8. Is it current and dated?

Return:
- useful parts to extract
- risky parts to ignore
- how to adapt it safely
- whether it should be added to my workflow
```

## Skill 5: Build a Low-Noise AI Research Resource Database

Use this when you want to keep up with AI tools, skills, papers, builders, and official docs without turning your reading list into a noisy link dump.

```text
Act as an AI research-workflow librarian for economics and finance scholars.

Goal:
Build a small resource database for my AI research workflow.

My field:
[economics/finance/subfield]

My current AI tools:
[ChatGPT/Claude/Codex/Claude Code/Cursor/VS Code/Zotero/GitHub/other]

My skill level:
[beginner/intermediate/advanced]

My weekly time budget:
[minutes]

Resource candidates:
[paste links, names, or descriptions]

Create a resource database with these fields:
1. Name
2. URL
3. Author or maintainer
4. Category: Learning material / Application tool / Setup / Official docs / Dataset / Methods reference
5. Topic: Workflow / Stata / R / Python / WRDS / Skills & MCP / Writing / Slides / Data / Methods / General
6. Level: Beginner / Intermediate / Advanced
7. Language
8. Direct-use value: copy skill / install tool / follow workflow / read background / cite method / verify docs
9. Data or confidentiality risk
10. License or attribution note
11. Last checked date
12. Where it belongs in my research workflow
13. Keep / test later / ignore

Then create these views:
- Start Here: maximum 8 beginner-friendly resources
- Application Tools: resources I can actually use, install, copy, or test
- Official Docs: product behavior and security rules
- Econ/Finance Research: field-specific workflows only
- Chinese Resources: Chinese or bilingual materials
- Needs Testing: promising resources that should not be recommended yet

Rules:
- Do not rank tools as universally best.
- Do not include generic AI hype.
- Flag resources that lack real examples, verification steps, data-safety warnings, or dates.
- Prefer resources that produce a reusable workflow, skill, template, dataset note, or code artifact.

Return:
1. the resource table;
2. the recommended views;
3. the top 5 resources to test this week;
4. what to ignore;
5. a 30-minute weekly review ritual.
```

## Skill 6: Find More Resources For One Econ/Finance Research Task

Use this when you need more tools, examples, papers, datasets, or skills for a specific task, but you do not want a random list.

```text
Act as a resource scout for economics and finance research workflows.

Task I need help with:
[example: Stata event-study code / finance text-as-data / Python panel data / R DiD / literature map / paper review / presentation slides]

My field/subfield:
[field]

My constraints:
- Data sensitivity: [public/licensed/restricted/private/unknown]
- Software: [Stata/R/Python/LaTeX/GitHub/Zotero/other]
- Skill level: [beginner/intermediate/advanced]
- Time budget: [minutes/hours]
- Need: [tutorial/tool/skill/code example/dataset/reference/official docs]

Search and evaluate resources using this standard:
1. direct relevance to economics/finance research;
2. whether it gives a working example, skill, code, dataset, or documented workflow;
3. whether it discusses privacy, licenses, reproducibility, or verification;
4. whether it is maintained or dated;
5. whether it is official documentation, canonical method reference, or builder-tested material;
6. what I should not copy blindly.

Return:
1. Top 10 resources in a table.
2. For each: URL, type, level, why useful, risk note, and how I should use it.
3. A "test this first" shortlist of 3 resources.
4. A "do not use yet" list with reasons.
5. Questions for you: what I need to clarify before adopting any resource.

Rules:
- Do not include generic AI hype.
- Do not rank tools universally.
- Prefer official docs, field-specific resources, working code, and reusable skills.
- If a resource requires licensed data, MCP access, or cloud upload, flag the permission risk.
```

Sources and workflow influences: Zara Zhang's curated AI learning library and follow-builders digest, Claude Blattman's continuous-improvement loop, Mihail Velikov's curated AI-in-econ wiki, Frank Lee's academic research skills taxonomy, Antonio Mele's Awesome Econ AI Stuff, Han Lulong's Awesome AI for Economists and Econ Writing Skill, and official documentation-first tool evaluation.
