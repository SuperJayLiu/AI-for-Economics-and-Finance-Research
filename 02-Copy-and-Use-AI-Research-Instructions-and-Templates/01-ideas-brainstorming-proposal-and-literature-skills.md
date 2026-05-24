> Copyright (c) 2026 SuperJayLiu (Chaojie Liu). Licensed under the repository MIT License.

# Research Ideas, Brainstorming, and Proposal Skills

Copy the relevant block and paste it into your AI tool.

For full literature review workflows, use [Literature Review and Source Synthesis Skills](10-literature-review-and-source-synthesis-skills.md). This file keeps only the early-stage idea, proposal, and paper-orientation blocks.

## Skill 1: Research Idea Stress Test

Use for early-stage ideas before you invest weeks.

```text
Act as a skeptical but constructive economics/finance research advisor.

Project area: [field/subfield]
Initial idea: [one paragraph]
Possible data: [data sources, access status, frequency, unit of observation]
Possible mechanism: [mechanism or theory]
Target audience: [seminar, PhD field paper, journal, policy audience]

Your task:
1. Restate the research question in one precise sentence.
2. Identify the outcome, treatment/exposure/shock, unit of observation, and time dimension.
3. Explain the economic or financial mechanism that would make the question matter.
4. List three ways the idea could be important.
5. List five reasons the idea may fail.
6. Identify the biggest identification, measurement, data-access, and novelty risks.
7. Suggest two narrower versions and two more ambitious versions.
8. Tell me what I must verify before proceeding.

Rules:
- Do not invent papers or citations.
- Do not claim novelty without verification.
- Separate "promising", "uncertain", and "must verify".
- Be direct. I want research judgment, not encouragement.
```

## Skill 2: Proposal Builder for Econ/Finance

Use when turning an idea into a structured proposal.

```text
Help me turn the following idea into a serious economics/finance research proposal.

Inputs:
- Working title: [title]
- Research question: [question]
- Motivation: [why it matters]
- Data: [sources, access, sample, frequency, unit]
- Empirical strategy or model: [current plan]
- Main concern: [what worries me]
- Target format: [PhD proposal / grant / seminar / pre-analysis memo]

Produce:
1. One-paragraph nontechnical motivation.
2. Research question and contribution in economist/finance language.
3. Conceptual framework or mechanism.
4. Data and measurement plan.
5. Identification or research design plan.
6. Expected empirical tables/figures.
7. Threats to validity and how to address them.
8. Feasibility checklist.
9. A 10-item "next week" task list.

Guardrails:
- Do not fabricate literature.
- Do not decide the identification strategy for me; critique options.
- State what evidence would change the proposal.
- Mark any claim that requires citation.
```

## Skill 3: Literature Map Without Fake Citations

Use this for a quick first-pass map after you have real papers, PDFs, BibTeX, or notes. For a fuller literature review, use the separate literature review file.

```text
Build a literature map from the materials I provide. Use only the papers, notes, and citations I give you unless I explicitly ask for search.

Research question: [question]
My project's intended contribution: [current contribution]
Materials provided: [PDFs/notes/BibTeX/list]

For each paper, extract:
- research question
- setting and data
- model or empirical design
- identification or theoretical mechanism
- main result
- limitation
- relation to my project
- what I should verify in the original paper

Then create:
1. A literature map grouped by mechanism, method, and setting.
2. A contribution table comparing my project to the literature.
3. A list of possible missing literatures, clearly labeled as hypotheses.
4. A "fake novelty risk" section explaining where my project may be less novel than I think.

Rules:
- Never invent a citation.
- If a citation is incomplete, flag it.
- Use "I cannot verify from the supplied materials" when needed.
```

## Skill 4: LLM-Friendly Paper Orientation File

Use for your own paper so future AI tools read it correctly.

```text
Create an llms.txt-style orientation file for my paper.

Inputs:
- Paper title: [title]
- Authors: [authors]
- Status: [draft/working paper/submitted/published]
- Abstract or intro: [paste]
- Data and methods summary: [paste]
- Key results: [paste]
- Limitations: [paste]

Output a plain Markdown file with:
1. What this paper is about.
2. What this paper does not show.
3. Important context and definitions.
4. Data and methods fingerprint.
5. Key results with scope conditions.
6. Limitations and boundary conditions.
7. Navigation guide for readers and AI tools.
8. Citation and publication status.

Rules:
- Be more specific about limitations than abstracts usually are.
- Do not overgeneralize.
- Do not add results not supplied.
```

Sources and workflow influences: Paul Goldsmith-Pinkham's research pipeline and LLM-friendly paper proposal; PaperSpine's artifact-trail logic.
