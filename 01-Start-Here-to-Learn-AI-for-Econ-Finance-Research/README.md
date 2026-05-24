# Start Here: Learn AI for Economics and Finance Research

This is the **one README version** of the learning handbook. Read this page first. Do not click through every subfolder unless you need detail.

> [!IMPORTANT]
> AI can make research tasks faster. It does not make claims true, citations real, identification credible, code correct, or confidential data safe.

## What This Page Replaces

This README now combines the guidance that used to be spread across many overview files. The detailed pages can remain as reference material, but ordinary readers should not need to open every folder just to understand the workflow.

## The Whole Handbook In One Page

| Part | What to learn | Direct action |
| --- | --- | --- |
| 1. Foundations | LLMs are assistants, not databases or referees | Split tasks into search, reasoning, writing, and coding before asking AI |
| 2. Responsibility | The scholar remains responsible for claims, citations, data, code, and disclosure | Decide data sensitivity before uploading anything |
| 3. Skills | Repeated tasks should become reusable procedures | Convert anything used twice into a project instruction, checklist, or skill |
| 4. Tools | Prompts, projects, skills, agents, MCPs, and GitHub solve different problems | Pick the smallest object that safely solves the workflow |
| 5. Research workflow | AI compresses execution, not judgment | Use AI to accelerate tasks, not to choose claims for you |
| 6. Empirical work | Code, data, tables, and figures need version control and validation | Use Git, data lineage notes, and runnable checks |
| 7. Writing and presenting | AI can improve structure and clarity | Preserve claims, citations, caveats, and meaning |
| 8. Automation | Agents can edit files and run commands | Use branches or worktrees, inspect diffs, and log changes |

## First Rule

AI output is not evidence. It is a draft, explanation, checklist, critique, or coding aid that must be checked against sources, data, code, or theory.

## Minimum Setup For Scholars

Before serious AI-assisted research, set up:

1. ChatGPT, Claude, Codex, Claude Code, Cursor, Copilot, or another AI workspace.
2. A GitHub repository or Git repo for each research project.
3. VS Code or another editor that can work with code, LaTeX, Git, and terminal commands.
4. Zotero or another reference manager.
5. One research coding language: Stata, R, Python, MATLAB, or Julia.
6. A project folder with `data/`, `code/`, `paper/`, `output/`, and `docs/`.
7. An AI-use log.
8. A rule for confidential, restricted, licensed, or referee materials.

## Safe Beginner Workflow

1. Pick one narrow research task.
2. Give AI only the context needed for that task.
3. Ask for structured output with uncertainty flags.
4. Verify every factual claim, citation, coefficient, equation, and institutional detail.
5. Record what AI helped with and what you accepted.
6. Keep original files under version control.

## AI Research Workflow Formula

```text
Task + Context + Rules + Output format + Verification = usable AI workflow
```

## Tool Choice: Prompt, Project, Skill, Agent, MCP, Or GitHub?

| Use | When |
| --- | --- |
| Prompt | One-off task, low risk, no reusable process needed |
| Project | Ongoing paper, dataset, course, talk, or revision |
| Skill | Repeated task with stable steps, inputs, outputs, and checks |
| Agent | Multi-step work that reads files, edits files, runs commands, or uses tools |
| MCP | AI needs a controlled connection to an external app, database, file system, or service |
| GitHub repo | Any workflow where AI can change files, code, paper text, tables, slides, or outputs |
| Worktree or branch | Any risky restructuring or agent-driven editing task |

MCPs are connection infrastructure. Skills are task procedures. A good research workflow may use both: MCP for safe access, skill for how to behave once access exists.

## Research Taste In The AI Age

AI compresses the research pipeline. It does not make a project important.

| AI can speed up | The scholar still decides |
| --- | --- |
| literature search and summaries | whether the question matters |
| code generation and translation | whether the design identifies the estimand |
| table and figure production | whether the result is true and meaningful |
| prose and slides | whether the claim is honest |
| referee-response drafting | what to concede, rerun, or defend |

The scarce skill is not producing more text. The scarce skill is producing research that is true, important, credible, and worth reading.

## Copy-And-Use: Research Project Triage Prompt

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

## Copy-And-Use: Clean Up A Research Project With An Agent

Use this only on a copy, branch, or worktree.

```text
I want your help cleaning up this research project and setting up a safe Git workflow.

Rules:
- First inspect the folder tree.
- Do not delete files without listing them first.
- Copy the full project to a backup directory before restructuring.
- Create or suggest a `.gitignore` before the first commit.
- Identify private, raw, restricted, generated, and cache files.
- Create a `DATA.md` or data-lineage note.
- Put code, data documentation, paper, slides, and outputs into a clear structure.
- Keep raw data read-only.
- Make all changes on a new branch or worktree.
- After restructuring, run the existing code or tests and compare outputs to prior results.
- Report commands run, files changed, outputs changed, and remaining uncertainty.

Desired structure:
project/
  README.md
  data/
    raw/          # not committed if restricted or too large
    processed/
    DATA.md
  code/
  paper/
  slides/
  output/
  docs/
  logs/
    ai-use-log.md
```

## Copy-And-Use: Tough Referee Prompt

```text
Act as a tough but fair economics/finance referee.

Paper or project summary:
[PASTE SUMMARY]

Evidence available:
[DATA, DESIGN, MAIN RESULTS]

Your task:
1. State the paper's claimed contribution.
2. Identify the strongest version of the paper.
3. List the top threats to identification, measurement, theory, and interpretation.
4. Separate fatal concerns from fixable concerns.
5. Suggest robustness checks only if they directly test a stated threat.
6. Identify overclaiming in the abstract, introduction, and conclusion.
7. List what must be verified in the original paper, data, or code.

Rules:
- Do not invent citations.
- Do not ask for generic robustness checks.
- Do not rewrite the contribution beyond the evidence.
```

## Copy-And-Use: Paper Summarizer Prompt

```text
Summarize this economics/finance paper for research use, not for casual reading.

Output format:
1. Research question
2. Setting and data
3. Identification strategy or model
4. Main result
5. Mechanism
6. Contribution relative to literature
7. What I must verify in the PDF
8. Possible relation to my project
9. Questions for seminar discussion
10. Claims that should not be repeated without checking

Rules:
- Use only the attached paper or provided text.
- Mark missing information as missing.
- Do not invent citations, data details, or results.
```

## Copy-And-Use: Code Review Prompt

```text
Review this research code as if it will affect a paper submission.

Focus on:
1. What each block does.
2. Inputs and outputs.
3. Data assumptions.
4. Possible merge, filter, missing-value, timing, or clustering errors.
5. Whether the code can be rerun from a clean checkout.
6. Whether tables and figures match the paper claims.
7. Tests or diagnostics I should run before accepting changes.

Rules:
- Explain before editing.
- Make small changes.
- Use Git diff.
- Do not change results silently.
```

## Verification Checklist

Before accepting AI output, check:

- Are all citations real and relevant?
- Are claims supported by the cited source or actual result?
- Did any code change affect sample size, filters, merges, clustering, or standard errors?
- Are confidential, restricted, licensed, or referee materials protected?
- Are planned tests separated from exploratory tests?
- Is the AI-use log updated?
- Can the project be restored from Git?

## Stop Signs

Pause before using AI if the task involves:

- unpublished coauthor drafts without team agreement
- referee reports or confidential seminar materials
- WRDS, CRSP, Compustat, transaction-level, household, firm, student, or administrative microdata
- licensed data whose terms prohibit upload or external processing
- causal claims, policy recommendations, or investment implications
- agents that can edit files, run code, push commits, send email, or access external tools

## Where To Go Next

- Need copyable tools: [Copy and Use AI Research Instructions and Templates](../02-Copy-and-Use-AI-Research-Instructions-and-Templates/README.md)
- Need a project setup: [How to Set Up Your AI Research Workflow](../03-How-to-Set-Up-Your-AI-Research-Workflow/README.md)
- Need examples: [See Examples Diagrams and Failure Cases](../04-See-Examples-Diagrams-and-Failure-Cases/README.md)
- Need official docs and builder sources: [Check Builders Official Docs and Resources](../05-Check-Builders-Official-Docs-and-Resources/README.md)

## Optional Reference Pages

These detailed pages are now optional. Use them when you need depth, not as required reading.

- [Concept Index and Glossary](00-concept-index-and-glossary.md)
- [Knowledge Links for Further Reading](00-knowledge-links.md)
- [Prompts, Projects, Skills, Agents, MCPs, and GitHub Repos](tools-and-features/01-prompts-projects-skills-agents-mcps.md)
- [Research Taste in the AI Age](econ-finance-research-workflow/00-research-taste-in-the-ai-age.md)
- [Data Sensitivity Matrix](responsible-use-and-risks/07-data-sensitivity-matrix.md)
- [Checking AI Outputs](core-ai-skills-for-research/06-checking-ai-outputs.md)

## Sources and Workflow Influences

Draws on economics and finance research workflow practice; Paul Goldsmith-Pinkham's AI writing, coding, VS Code/Copilot, paper-packaging, and research-in-the-time-of-AI discussions; official AI tool documentation; Git/GitHub workflow practices; and builder-oriented advice to follow durable workflows rather than influencer hype.

Last checked: 2026-05-24
