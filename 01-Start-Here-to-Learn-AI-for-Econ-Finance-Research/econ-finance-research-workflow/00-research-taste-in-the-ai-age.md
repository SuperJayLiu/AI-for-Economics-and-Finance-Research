# Research Taste In The AI Age

## What Problem This Solves

AI makes execution cheaper. It can draft prose, write code, assemble data, build figures, summarize papers, and produce plausible paper narratives quickly.

That does not make scholarship easier in the most important sense. It shifts value toward judgment.

## Core Message

Everyone can produce more text, code, and tables. The scarce skill is producing research that is true, important, credible, and worth reading.

AI compresses the research timeline. It does not remove the need to ask whether the project should exist.

## The Research Pipeline AI Compresses

| Stage | What AI can help with | What still belongs to the scholar |
| --- | --- | --- |
| Ideation | surface literatures, examples, mechanisms, counterarguments | decide whether the question matters |
| Design and feasibility | map possible data, proxies, identification threats, implementation steps | judge credibility and institutional fit |
| Data assembly | write scrapers, parse files, document data lineage, create validation checks | decide what data is appropriate and legal to use |
| Core analysis | implement estimators, reproduce tables, translate code, explain output | choose the estimand and assess assumptions |
| Robustness and extensions | generate checklists, run planned variants, organize outputs | separate planned checks from exploratory search |
| Writing | restructure arguments, clarify contributions, improve prose | preserve claims, caveats, citations, and intellectual honesty |
| Submission and review | organize referee reports, build response matrices, draft replies | decide what to concede, rerun, or defend |
| Publication and dissemination | make slides, websites, replication packages, LLM-friendly bundles | represent findings honestly and reproducibly |

## Two Failure Modes

### 1. Low-Care Output

AI lowers the cost of producing drafts. That increases the risk of weak papers, careless claims, and fake polish.

Rule: every AI-assisted artifact needs a verification trail: sources, data checks, code diff, or theory check.

### 2. Specification Search At Machine Speed

AI can run many regressions, variants, and robustness checks quickly. That can be useful for replication and diagnostics, but it can also hide researcher degrees of freedom.

Rule: separate planned tests, exploratory tests, and post-search holdout checks. Do not let an agent choose a result merely because it looks impressive.

## What Becomes More Important

- asking important questions
- choosing credible identification
- finding high-quality, proprietary, or experimental data
- understanding institutions
- building real theory
- exercising taste in what not to do
- knowing when a result is not worth pursuing
- writing claims that match evidence
- documenting uncertainty instead of hiding it

## Copy-And-Use: Project Triage Prompt

```text
You are my research taste and feasibility critic for an economics/finance project.

Project idea:
[PASTE 1-3 PARAGRAPHS]

Known data:
[DATA SOURCES, SAMPLE, ACCESS LIMITS]

Possible design:
[IDENTIFICATION STRATEGY OR MODEL]

Your task:
1. State the strongest version of the research question.
2. Explain why the question might matter economically.
3. Identify the main identification, data, theory, and interpretation risks.
4. List what would make the project not worth doing.
5. Separate tasks AI can help execute from judgments I must make.
6. Give a 30-day feasibility plan with checkpoints.
7. List what evidence would change your mind.

Rules:
- Do not invent citations.
- Flag specification-search risks.
- Use cautious language when the data or design is unclear.
```

## What The Scholar Must Verify

- whether the question matters
- whether the mechanism is real
- whether the empirical design is credible
- whether the result survives serious scrutiny
- whether the contribution is honest
- whether AI-generated code and text preserve the intended claim

## Sources and Workflow Influences

Influenced by Paul Goldsmith-Pinkham's discussion of AI compressing the economics/finance research pipeline while making research taste, institutional knowledge, identification, and careful iteration more valuable; his warning that fast AI-assisted analysis can increase low-care output and specification-search risk; and the broader repo rule that AI output is not evidence.

Last checked: 2026-05-24
