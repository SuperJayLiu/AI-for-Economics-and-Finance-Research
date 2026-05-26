# Copy and Use AI Research Instructions and Templates

This folder is the direct-use toolbox for the repository. Use this README as the index, then open the detailed skill pages inside [`skills/`](skills/) when you want a copy-ready block for a specific research task.

Open a skill page, copy the block you need, paste it into ChatGPT, Claude, Codex, Claude Code, Cursor, GitHub Copilot, or another AI tool, and add the project facts you already know. If the task, data, method, permission rule, or output format is unclear, the skill should ask you clarifying questions before producing the full answer. The goal is not to read every file; the goal is to find one usable instruction, run it on a small task, verify it, and save what changed.

> Copyright (c) 2026 SuperJayLiu (Chaojie Liu). Licensed under the repository MIT License. These instructions/workflows are original to this repository unless otherwise noted. External inspirations are cited in relevant files.

This is not the reading book. For concepts and risks, start with [the handbook](../01-Start-Here-to-Learn-AI-for-Econ-Finance-Research/README.md).

> [!TIP]
> Start with one narrow task. Copy one block. Add your project facts. Ask for a plan. Then verify.

> [!IMPORTANT]
> Beginners should not try to use every skill. Pick the page that matches the research object in front of you: idea, literature, data, code, methods, paper text, slides, verification, or revision.

Questions or suggestions for this part: email [jay.liu@bristol.ac.uk](mailto:jay.liu@bristol.ac.uk) with subject `[AI Econ Finance Skills] Suggest a skill or prompt`.

## Start With A Task Card

Use these as the fastest entry points. Each card points to one copy-ready block and one verification habit.

| I want to... | Copy first | Then verify by... |
| --- | --- | --- |
| test whether a research idea is worth pursuing | [Research Idea Stress Test](skills/01-ideas-brainstorming-proposal-and-literature-skills.md#skill-1-research-idea-stress-test) | naming the closest papers, data obstacle, and identification/model obstacle |
| build a literature review without fake citations | [Source-Grounded Literature Review Builder](skills/10-literature-review-and-source-synthesis-skills.md#skill-1-source-grounded-literature-review-builder) | checking every claim against supplied sources or verified search results |
| write or revise an introduction | [Introduction Spine Builder](skills/02-paper-drafting-revision-and-citation-skills.md#skill-1-introduction-spine-builder) | confirming the question, contribution, data/design, and strongest result are accurate |
| draft empirical methods for applied economics | [Draft Empirical Methods Section for Economics](skills/03-empirical-methods-skills-for-economics-research.md#skill-1-draft-empirical-methods-section-for-economics) | comparing prose with code, sample, timing, estimand, and inference |
| draft empirical methods for finance | [Draft Empirical Methods Section for Finance](skills/04-empirical-methods-skills-for-finance-research.md#skill-1-draft-empirical-methods-section-for-finance) | checking timing, link tables, survivorship, delisting, event windows, and factor-mining risk |
| debug code in Python, R, or Stata | [Coding, Data Analysis, and Debugging Skills](skills/08-coding-data-analysis-and-debugging-skills.md) | running a toy-data test before trusting real-data output |
| use agents on files safely | [AGENTS.md for Research Repo](skills/05-git-data-replication-and-research-safety-templates.md#template-3-agentsmd-for-research-repo) | inspecting `git diff`, running checks, and logging AI use |
| prepare slides or practice a seminar | [Full-Materials Presentation Intake and Structure Confirmation](skills/06-presentations-slides-websites-and-talk-practice-skills.md#skill-0-full-materials-presentation-intake-and-structure-confirmation) | matching every slide claim to the paper, table, figure, or model |
| decide whether an AI answer can be accepted | [Verification Method Selector](skills/17-verification-reproducibility-and-disclosure-skills.md#skill-1-verification-method-selector) | choosing source, code, data, math, policy, or disclosure checks |
| find more tools/resources for one task | [Find More Resources For One Econ/Finance Research Task](skills/09-tool-selection-updates-and-skill-improvement.md#skill-6-find-more-resources-for-one-econfinance-research-task) | rejecting generic hype and testing at most three resources first |

## Default Clarification Rule

Paste this before any skill when the task is serious, the inputs are incomplete, or the audience may not know technical terms:

```text
Before producing the final answer, check whether any required input, term, data rule, method detail, institutional detail, policy constraint, or output format is unclear.

If something is unclear, ask up to five numbered clarifying questions first. If you can proceed with reasonable assumptions, state those assumptions clearly and ask me to confirm or correct them.

When you use technical terms, define them in plain language and give one economics or finance research example.

At the end, include a short section called "Questions for you" listing anything I should decide, check, or clarify next.
```

Use this rule especially for Git, `.gitignore`, branches, worktrees, MCPs, agent permissions, data licenses, identification assumptions, variable construction, and disclosure policies.

## Skill Import Mode

Use this when you want to import a skill into ChatGPT, Claude, Codex, Claude Code, Cursor, or another AI tool and type less later. Paste the relevant skill block once, then add this operating rule:

```text
Use the pasted block as an imported skill for this task.

Start by collecting only the missing inputs needed to do the work. Ask up to five clarifying questions if required inputs, data rules, method details, permissions, audience, or output format are unclear.

For long outputs, file-producing tasks, slides, code, empirical methods, literature reviews, referee responses, or agentic workflows, first return a section titled "Proposed structure and assumptions" and wait for my confirmation before producing the full output.

Before finalizing, double-check for unsupported claims, invented citations or results, privacy risks, and mismatch with the requested format.

End with four sections:
1. What I produced.
2. What I did not change.
3. What you must verify.
4. Questions for you.
```

This makes the skill behave less like a one-off prompt and more like a step-by-step research assistant. It is especially useful when you upload a full paper, code folder, slide deck, referee letter, or replication package.

## What Is Here

### How A Copy-Ready Skill Should Work

Every usable skill should move through the same visible chain.

```mermaid
flowchart LR
  I["Inputs you provide"] --> A["AI asks clarifying questions"]
  A --> P["Proposed structure and assumptions"]
  P --> C["You confirm or correct"]
  C --> O["Output you can use"]
  O --> D["AI double-checks before reply"]
  D --> V["Verification checklist"]
  V --> L["AI-use log entry"]
```

| Part | What the reader should see | Bad sign |
| --- | --- | --- |
| inputs | exactly what to paste or attach | "give me everything" |
| clarifying questions | what the AI should ask before acting | AI guesses missing data rules |
| proposed structure | files, assumptions, steps, risks, and output format | AI jumps straight to final prose/code |
| confirmation | a chance to correct structure before the long answer | AI creates a full deck/paper/code change without approval |
| output | draft text, code, table, checklist, or slide plan | vague advice only |
| double-check | final scan for unsupported claims, privacy issues, and format mismatch | polished output with hidden errors |
| verification | concrete source/code/data/math/policy check | "verify manually" with no method |
| log | what to record after using the output | no trace of AI involvement |

### Skill Selection Map

Use the artifact you need, not the tool name, to choose a skill.

```mermaid
flowchart TD
  T["What artifact do you need?"] --> I["Idea, proposal, or question"]
  T --> L["Literature map or source synthesis"]
  T --> D["Data, code, table, or figure"]
  T --> M["Empirical method or design check"]
  T --> W["Paper prose, revision, or response"]
  T --> S["Slides, talk, website, or teaching material"]
  T --> G["Git, agent rules, disclosure, verification"]
  I --> F1["01 or 18"]
  L --> F2["10"]
  D --> F3["08 or 14"]
  M --> F4["03, 04, 11, 16"]
  W --> F5["02 or 13"]
  S --> F6["06"]
  G --> F7["05, 07, 09, 17"]
  click F1 "01-ideas-brainstorming-proposal-and-literature-skills.md" "Open idea/proposal skills"
  click F2 "10-literature-review-and-source-synthesis-skills.md" "Open literature skills"
  click F3 "14-data-cleaning-merging-analysis-and-output-skills.md" "Open data/output skills"
  click F4 "11-causal-inference-econometrics-and-time-series-skills.md" "Open econometrics skills"
  click F5 "02-paper-drafting-revision-and-citation-skills.md" "Open writing skills"
  click F6 "06-presentations-slides-websites-and-talk-practice-skills.md" "Open presentation skills"
  click F7 "05-git-data-replication-and-research-safety-templates.md" "Open safety templates"
```

### Search By Function

If you are using GitHub search, search these words inside this folder. If you are reading manually, use the links.

| Function / keyword | First place to look | Typical output |
| --- | --- | --- |
| `write`, `revise`, `introduction`, `abstract` | [Paper Drafting, Revision, and Citation Skills](skills/02-paper-drafting-revision-and-citation-skills.md) | section draft, revision plan, citation-safe prose |
| `review`, `referee`, `response`, `R&R` | [Referee Reports and Peer Review Skills](skills/13-referee-reports-and-peer-review-skills.md) | self-review, referee report, response table |
| `literature`, `matrix`, `source`, `citation` | [Literature Review and Source Synthesis Skills](skills/10-literature-review-and-source-synthesis-skills.md) | paper matrix, synthesis outline, claim-source bank |
| `idea`, `proposal`, `brainstorm`, `research question` | [Ideas, Brainstorming, Proposal, and Literature Skills](skills/01-ideas-brainstorming-proposal-and-literature-skills.md) | idea stress test, proposal frame, question refinement |
| `economics methods`, `identification`, `design` | [Empirical Methods Skills for Economics Research](skills/03-empirical-methods-skills-for-economics-research.md) | methods section, design audit, pre-mortem |
| `finance methods`, `asset pricing`, `corporate finance`, `banking` | [Empirical Methods Skills for Finance Research](skills/04-empirical-methods-skills-for-finance-research.md) | finance methods draft, return/window/survivorship checks |
| `Python`, `R`, `Stata`, `debug`, `code review` | [Coding, Data Analysis, and Debugging Skills](skills/08-coding-data-analysis-and-debugging-skills.md) | language-specific code plan, diagnosis, toy test |
| `WRDS`, `CRSP`, `Compustat`, `merge`, `table`, `figure` | [Data Cleaning, Merging, Analysis, and Output Skills](skills/14-data-cleaning-merging-analysis-and-output-skills.md) | pipeline, merge plan, output audit |
| `DiD`, `IV`, `RD`, `panel`, `time series` | [Causal Inference, Econometrics, and Time-Series Skills](skills/11-causal-inference-econometrics-and-time-series-skills.md) | method diagnostic, estimator checklist |
| `text-as-data`, `LLM measurement`, `filings` | [Text-as-Data and LLM Measurement Skills](skills/15-text-as-data-and-llm-measurement-skills.md) | labeling protocol, validation plan |
| `Git`, `DATA.md`, `AGENTS.md`, `AI-use log` | [Git, Data, Replication, and Research Safety Templates](skills/05-git-data-replication-and-research-safety-templates.md) | project safety files and logging templates |
| `slides`, `Beamer`, `HTML`, `website`, `practice talk` | [Presentations, Slides, Websites, and Talk Practice Skills](skills/06-presentations-slides-websites-and-talk-practice-skills.md) | slide workflow, talk drill, website prompt |
| `find resources`, `resource scout`, `follow builders`, `tool updates` | [Tool Selection, Updates, and Skill Improvement](skills/09-tool-selection-updates-and-skill-improvement.md) | dated comparison, update filter, resource shortlist |

### Search By Software

| Software or tool | Use first | What to ask AI to produce |
| --- | --- | --- |
| Stata | [Stata Research Workflow Assistant](skills/08-coding-data-analysis-and-debugging-skills.md#skill-9-stata-research-workflow-assistant) | do-file plan, merge/check diagnostics, table command review |
| R | [R Econometrics Workflow Assistant](skills/08-coding-data-analysis-and-debugging-skills.md#skill-8-r-econometrics-workflow-assistant) | `fixest`/`did`/`rdrobust`/`tidyverse` plan with tests |
| Python | [Python Empirical Analysis Assistant](skills/08-coding-data-analysis-and-debugging-skills.md#skill-7-python-empirical-analysis-assistant) | pandas/statsmodels/linearmodels plan with toy-data tests |
| LaTeX/Beamer | [Presentations, Slides, Websites, and Talk Practice Skills](skills/06-presentations-slides-websites-and-talk-practice-skills.md) | paper section, Beamer deck, table/figure formatting |
| Codex/Claude Code/Cursor | [Project Instructions and Agent Role Templates](skills/07-project-instructions-and-agent-role-templates.md) | project instructions, agent role, approval gates |

### Tagged Skill Index

Use this table when you know the artifact you need but not the file name. Levels mean the expected reader setup: beginner = browser AI and public material; intermediate = project context and source checks; advanced = Git, code, data, or agent workflow.

| Skill page | Field | Level | Required input | Output | Verification | Best tool mode |
| --- | --- | --- | --- | --- | --- | --- |
| [01 Ideas, brainstorming, proposal](skills/01-ideas-brainstorming-proposal-and-literature-skills.md) | both | beginner | topic, setting, possible data, audience | idea stress test, proposal frame, paper orientation | closest papers, data obstacle, identification/model obstacle | chat or project |
| [02 Paper drafting, revision, citation](skills/02-paper-drafting-revision-and-citation-skills.md) | both | intermediate | verified claims, paper stage, target audience | introduction spine, revision, response plan | citations, claims, hedging, author voice | project |
| [03 Economics empirical methods](skills/03-empirical-methods-skills-for-economics-research.md) | economics | intermediate | design, data, sample, equation, timing | methods prose or design audit | code, estimand, sample, timing, inference | project or agent |
| [04 Finance empirical methods](skills/04-empirical-methods-skills-for-finance-research.md) | finance | intermediate | data source, security/firms, timing, model, benchmark | finance methods prose or audit | look-ahead, survivorship, delisting, link tables, multiple testing | project or agent |
| [05 Git, data, replication safety](skills/05-git-data-replication-and-research-safety-templates.md) | both | beginner-intermediate | project folder, data rules, desired structure | `.gitignore`, `DATA.md`, `AGENTS.md`, AI-use log | Git diff, ignored files, data permissions | GitHub workflow |
| [06 Presentations, slides, websites](skills/06-presentations-slides-websites-and-talk-practice-skills.md) | both | beginner-intermediate | paper/materials, audience, time, figures, format | confirmed talk structure, HTML slides, Beamer deck, talk drill, website plan | claim-to-evidence match, privacy, public-sharing permission | chat, project, or agent |
| [07 Project instructions and roles](skills/07-project-instructions-and-agent-role-templates.md) | both | beginner-intermediate | research purpose, role, files, rules | project instructions, role prompts, agent rules | missing-input questions, permissions, output scope | project or agent |
| [08 Coding, data analysis, debugging](skills/08-coding-data-analysis-and-debugging-skills.md) | both | intermediate | code, error, expected output, data schema | diagnosis, patch plan, toy test, code review | run code, inspect output, compare to design | coding agent |
| [09 Tool selection and updates](skills/09-tool-selection-updates-and-skill-improvement.md) | both | beginner | task, budget, tool access, risk tolerance | dated tool choice, update digest, resource shortlist | date, official docs, small-task test | chat |
| [10 Literature review](skills/10-literature-review-and-source-synthesis-skills.md) | both | beginner-intermediate | supplied papers, notes, BibTeX, verified links | literature matrix, synthesis, claim-source bank | source match, DOI/journal page, no invented citations | project or search-grounded chat |
| [11 Causal inference/econometrics/time series](skills/11-causal-inference-econometrics-and-time-series-skills.md) | both | intermediate-advanced | design, timing, panel, outcome, treatment, code/table | estimator diagnostic and inference checklist | estimator assumptions, clustering, robustness, timing | project or agent |
| [12 Theory/model/math](skills/12-theory-model-and-math-skills.md) | both | advanced | model, assumptions, proposition, proof sketch | model audit, proof gaps, implications | algebra, limiting cases, equilibrium logic | project |
| [13 Referee and peer review](skills/13-referee-reports-and-peer-review-skills.md) | both | intermediate | manuscript, review policy, comments, target journal | self-review, report aid, response plan | confidentiality policy, claim support, tone | project |
| [14 Data cleaning/merging/output](skills/14-data-cleaning-merging-analysis-and-output-skills.md) | both | advanced | schema, merge keys, timing, code, desired outputs | pipeline, merge plan, toy data, tables/figures | toy-data answer, audit tables, lineage | coding agent |
| [15 Text-as-data/LLM measurement](skills/15-text-as-data-and-llm-measurement-skills.md) | both | advanced | corpus, labels, construct, validation sample | measurement protocol, prompt sensitivity, methods paragraph | validation, model version, leakage, sensitivity | project or agent |
| [16 Structural/quantitative/welfare](skills/16-structural-quantitative-and-welfare-skills.md) | both | advanced | model, moments, parameters, estimation, counterfactual | structural map, estimation plan, welfare guardrail | fit, convergence, identification, counterfactual interpretation | project or coding agent |
| [17 Verification/disclosure](skills/17-verification-reproducibility-and-disclosure-skills.md) | both | beginner-intermediate | AI output, source/code/data object, target use | verification method, disclosure, reproducibility packet | source/code/data/math/policy check | chat, project, or agent |
| [18 Research question/taste/positioning](skills/18-research-question-taste-and-positioning-skills.md) | both | beginner-intermediate | topic, mechanism, closest papers, data idea | sharper question, mechanism tension, so-what test | importance, novelty, feasibility, contribution | chat or project |

| File | Use it when you need... |
| --- | --- |
| [01 Research Ideas, Brainstorming, and Proposal Skills](skills/01-ideas-brainstorming-proposal-and-literature-skills.md) | quick idea stress tests, proposal framing, LLM-friendly paper orientation |
| [02 Paper Drafting, Revision, and Citation Skills](skills/02-paper-drafting-revision-and-citation-skills.md) | introduction, paper drafting, revision, citation support, referee response |
| [03 Empirical Methods Skills for Economics Research](skills/03-empirical-methods-skills-for-economics-research.md) | drafting or checking empirical methods in applied economics |
| [04 Empirical Methods Skills for Finance Research](skills/04-empirical-methods-skills-for-finance-research.md) | drafting or checking empirical methods in asset pricing, corporate finance, banking, household finance |
| [05 Git, Data, Replication, and Research Safety Templates](skills/05-git-data-replication-and-research-safety-templates.md) | project cleanup, `.gitignore`, AGENTS.md, DATA.md, AI-use log, replication checks |
| [06 Presentations, Slides, Websites, and Talk Practice Skills](skills/06-presentations-slides-websites-and-talk-practice-skills.md) | HTML slides, Beamer slides, presentation practice, personal academic websites |
| [07 Project Instructions and Agent Role Templates](skills/07-project-instructions-and-agent-role-templates.md) | ChatGPT/Claude Projects, tough referee, paper summarizer, idea verifier, conference tracker |
| [08 Coding, Data Analysis, and Debugging Skills](skills/08-coding-data-analysis-and-debugging-skills.md) | Stata/R/Python debugging, code review, table/figure checks, reproducibility |
| [09 Tool Selection, Updates, and Skill Improvement](skills/09-tool-selection-updates-and-skill-improvement.md) | dated tool comparison, update digest, resource scouting, continuous improvement, bad-advice filter |
| [10 Literature Review and Source Synthesis Skills](skills/10-literature-review-and-source-synthesis-skills.md) | source-grounded literature review, paper matrices, research gaps, citation-safe synthesis |
| [11 Causal Inference, Econometrics, and Time-Series Skills](skills/11-causal-inference-econometrics-and-time-series-skills.md) | OLS, panel FE, DiD, IV, RD, event studies, synthetic control, AR/MA/ARMA/VAR checks |
| [12 Theory Model and Math Skills](skills/12-theory-model-and-math-skills.md) | theory-model reconstruction, assumption audit, proof gaps, economic interpretation |
| [13 Referee Reports and Peer Review Skills](skills/13-referee-reports-and-peer-review-skills.md) | referee reports, journal response planning, revision triage, GitHub-style feedback handling |
| [14 Data Cleaning, Merging, Analysis, and Output Skills](skills/14-data-cleaning-merging-analysis-and-output-skills.md) | data pipelines, WRDS/CRSP/Compustat merges, Fama-MacBeth, portfolio sorts, EDA, tables, figures |
| [15 Text-as-Data and LLM Measurement Skills](skills/15-text-as-data-and-llm-measurement-skills.md) | filings, earnings calls, speeches, news, LLM-generated variables, validation, prompt sensitivity |
| [16 Structural, Quantitative, and Welfare Skills](skills/16-structural-quantitative-and-welfare-skills.md) | GMM, SMM, MLE, calibration, counterfactuals, welfare, model fit |
| [17 Verification, Reproducibility, and Disclosure Skills](skills/17-verification-reproducibility-and-disclosure-skills.md) | citation checks, toy-data tests, coefficient checks, proof checks, AI-use disclosure |
| [18 Research Question, Taste, and Positioning Skills](skills/18-research-question-taste-and-positioning-skills.md) | topic-to-question sharpening, mechanisms, closest-paper positioning, so-what test, AI cost-benefit |

## Why These Skill Families Exist

| Skill family | Why a new scholar needs it |
| --- | --- |
| idea and taste | AI can make weak ideas sound polished; this helps you test whether the question is worth pursuing. |
| literature review | AI can hallucinate citations; this forces source-grounded maps and contribution checks. |
| empirical methods | AI can draft clean prose that misstates identification; this keeps design, data, and inference explicit. |
| data and coding execution | AI saves time here, but only if merges, timing, variables, and outputs are testable. |
| text-as-data | LLM labels are measurements, not magic; they need validation, versioning, and sensitivity checks. |
| theory and structural work | AI can explain and code models, but assumptions, identification, equilibrium, and welfare need scrutiny. |
| writing and slides | AI can improve clarity, but it can also overclaim or flatten the paper's voice. |
| agents and project rules | file-editing AI needs boundaries: what to touch, what not to touch, what to verify. |
| verification and disclosure | "Check it" is too vague; this gives concrete checks and AI-use records. |

## Why Some Topics Have Separate Files

Most topics should stay in one README-style file. Separate files are useful only when readers will repeatedly search for that skill family:

| Separate file | Why it is separate |
| --- | --- |
| literature review | large enough to need source matrices, synthesis workflows, and fake-citation guardrails |
| causal inference/econometrics/time series | method-specific checks are easier to find in one place |
| data cleaning/merging/output | execution workflows need code, toy tests, and data lineage in one place |
| text-as-data/LLM measurement | AI-generated variables create distinct validation and reproducibility issues |
| structural/quantitative/welfare | estimation, simulation, counterfactuals, and welfare use different checks from reduced-form methods |
| theory and math | proof, equilibrium, and model-audit workflows require different guardrails |
| verification/reproducibility/disclosure | every other skill depends on concrete verification methods |
| referee/review | reviewer comments, journal responses, and PR-style feedback need a different workflow |

## Research Pipeline: Which Skill Feeds Which

Use this when you are not sure where to begin.

```mermaid
flowchart LR
  A["Idea and taste"] --> B["Literature map"]
  B --> C["Design pre-mortem"]
  C --> D["Data pipeline and variable dictionary"]
  D --> E["Code, EDA, tables, figures"]
  E --> F["Methods prose"]
  F --> G["Result interpretation"]
  G --> H["Paper revision and presentation"]
  H --> I["Referee response or public communication"]
  V["Verification and AI-use log"] -. "runs across every stage" .-> A
  V -.-> D
  V -.-> F
  V -.-> I
```

| Stage | First skill to copy |
| --- | --- |
| idea | [Topic-to-Tension Research Question Builder](skills/18-research-question-taste-and-positioning-skills.md#skill-1-topic-to-tension-research-question-builder) |
| literature | [Source-Grounded Literature Review Builder](skills/10-literature-review-and-source-synthesis-skills.md#skill-1-source-grounded-literature-review-builder) |
| design | [Identification Design Pre-Mortem](skills/03-empirical-methods-skills-for-economics-research.md#skill-4-identification-design-pre-mortem) |
| data execution | [Reproducible Research Data Pipeline Builder](skills/14-data-cleaning-merging-analysis-and-output-skills.md#skill-1-reproducible-research-data-pipeline-builder) |
| code | [Debug Stata/R/Python Research Code](skills/08-coding-data-analysis-and-debugging-skills.md#skill-1-debug-statarpython-research-code) |
| methods | [Economics Methods](skills/03-empirical-methods-skills-for-economics-research.md#skill-1-draft-empirical-methods-section-for-economics) or [Finance Methods](skills/04-empirical-methods-skills-for-finance-research.md#skill-1-draft-empirical-methods-section-for-finance) |
| verification | [Verification Method Selector](skills/17-verification-reproducibility-and-disclosure-skills.md#skill-1-verification-method-selector) |
| presentation | [Full-Materials Presentation Intake and Structure Confirmation](skills/06-presentations-slides-websites-and-talk-practice-skills.md#skill-0-full-materials-presentation-intake-and-structure-confirmation) |

## Most-Used Blocks

| Task | Copy this first |
| --- | --- |
| early idea | [Research Idea Stress Test](skills/01-ideas-brainstorming-proposal-and-literature-skills.md#skill-1-research-idea-stress-test) |
| proposal | [Proposal Builder](skills/01-ideas-brainstorming-proposal-and-literature-skills.md#skill-2-proposal-builder-for-econfinance) |
| literature review | [Source-Grounded Literature Review Builder](skills/10-literature-review-and-source-synthesis-skills.md#skill-1-source-grounded-literature-review-builder) |
| intro | [Introduction Spine Builder](skills/02-paper-drafting-revision-and-citation-skills.md#skill-1-introduction-spine-builder) |
| econ methods | [Draft Empirical Methods Section for Economics](skills/03-empirical-methods-skills-for-economics-research.md#skill-1-draft-empirical-methods-section-for-economics) |
| finance methods | [Draft Empirical Methods Section for Finance](skills/04-empirical-methods-skills-for-finance-research.md#skill-1-draft-empirical-methods-section-for-finance) |
| causal inference | [Causal Design Diagnostic](skills/11-causal-inference-econometrics-and-time-series-skills.md#skill-1-causal-design-diagnostic) |
| data pipeline | [Reproducible Research Data Pipeline Builder](skills/14-data-cleaning-merging-analysis-and-output-skills.md#skill-1-reproducible-research-data-pipeline-builder) |
| WRDS/CRSP/Compustat merge | [WRDS, CRSP, Compustat, and CCM Merge Plan](skills/14-data-cleaning-merging-analysis-and-output-skills.md#skill-2-wrds-crsp-compustat-and-ccm-merge-plan) |
| text-as-data | [LLM-as-Measurement Protocol](skills/15-text-as-data-and-llm-measurement-skills.md#skill-1-llm-as-measurement-protocol) |
| structural/quantitative model | [Moments-to-Parameters Audit](skills/16-structural-quantitative-and-welfare-skills.md#skill-2-moments-to-parameters-audit) |
| verification/disclosure | [AI Reproducibility Packet and Disclosure Draft](skills/17-verification-reproducibility-and-disclosure-skills.md#skill-6-ai-reproducibility-packet-and-disclosure-draft) |
| theory model | [Economic Model Discussant](skills/12-theory-model-and-math-skills.md#skill-1-economic-model-discussant) |
| messy repo | [Clean Up Existing Project and Start Git Safely](skills/05-git-data-replication-and-research-safety-templates.md#template-1-clean-up-existing-project-and-start-git-safely) |
| slides | [Full-Materials Presentation Intake and Structure Confirmation](skills/06-presentations-slides-websites-and-talk-practice-skills.md#skill-0-full-materials-presentation-intake-and-structure-confirmation) |
| coding | [Debug Stata/R/Python Research Code](skills/08-coding-data-analysis-and-debugging-skills.md#skill-1-debug-statarpython-research-code) |
| referee response | [Journal Referee Response Planner](skills/13-referee-reports-and-peer-review-skills.md#skill-2-journal-referee-response-planner) |

## How To Use These Blocks

1. Copy one block.
2. Add the paper title, data source, target journal, or other project facts you already know. If you do not know them, leave them out and require the AI to ask clarifying questions first.
3. Add your actual materials.
4. Ask the AI to clarify missing inputs before it writes, edits, or codes.
5. For long outputs, ask for "Proposed structure and assumptions" before the full answer.
6. Confirm or correct the structure.
7. Let AI produce the usable output.
8. Require a final double-check.
9. Verify everything.
10. Save the accepted output and checks in your AI-use log.

## Universal Safety Instruction

Add this to any skill when working on serious research:

```text
Do not invent citations, data sources, coefficients, robustness checks, institutional details, mathematical derivations, or claims about the literature. If information is missing, say exactly what is missing and what I must verify manually. Separate verified facts, interpretation, suggestions, and uncertainty.

Follow all university, employer, journal, conference, funder, data-provider, and coauthor policies on AI use. If the relevant rule is stricter than this instruction, follow the stricter rule.

If any input, term, policy, method, data rule, or output format is unclear, ask up to five clarifying questions before giving the final answer. If you proceed with assumptions, state them explicitly. End with "Questions for you" if anything remains uncertain.

For long outputs, file-producing tasks, slides, code, empirical methods, literature reviews, referee responses, or agentic workflows, first return "Proposed structure and assumptions" and wait for my confirmation before producing the full output.

Before finishing, double-check for unsupported claims, invented citations or results, privacy risks, and mismatch with the requested format. State what you changed or produced, what you did not change, and what I must verify manually.
```

## Universal Output Contract

Add this when you want a cleaner answer:

```text
Return your answer in seven sections:
1. Proposed structure and assumptions, if this is a long or file-producing task.
2. Direct output I can use.
3. Assumptions you made.
4. Items I must verify manually.
5. Risks or failure modes.
6. What you produced, what you did not change, and what I must verify.
7. Questions for you and next action checklist.
```

## Source Use Rule

Some skills are inspired by public workflow ideas from Paul Goldsmith-Pinkham, Zara Zhang, PaperSpine, Nature-style skill repositories, and official tool documentation. Do not copy external skills wholesale unless the license permits it. This repo adapts workflow ideas into economics and finance research instructions.

## Suggest a New Skill

```text
Email subject: If I have not provided it, ask me to specify: AI Econ Finance Skills Suggest a new skill

Suggested skill name:
Research task:
Who would use it:
Required inputs:
Expected output:
Risks/failure modes:
Verification checklist:
External inspiration or source, if any:
```
