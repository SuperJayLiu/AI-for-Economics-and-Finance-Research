> Copyright (c) 2026 SuperJayLiu (Chaojie Liu). Licensed under the repository MIT License.

# Git, Data, Replication, and Research Safety Templates

> [!IMPORTANT]
> Follow university, employer, data-provider, journal, conference, funder, and coauthor policies on AI use. These templates are not permission to upload confidential or restricted material.

> [!NOTE]
> Default add-on for any block on this page: `If any required input, term, method detail, data rule, or output format is unclear, ask me up to five clarifying questions before giving the final output. Define unfamiliar technical terms in plain language and end with "Questions for you" if anything remains uncertain.`

## Template 1: Clean Up Existing Project and Start Git Safely

```text
I want help cleaning up this research project and setting up a safe Git workflow.

Before changing anything:
1. Inspect the current folder structure.
2. Identify likely raw data, derived data, code, paper files, figures, tables, logs, and temporary files.
3. Propose a backup plan.
4. Propose a `.gitignore`.
5. Propose a clean folder structure.
6. Ask me to approve the plan before moving files.

After approval:
1. Create or update README.md, DATA.md, AGENTS.md, and AI-USE-LOG.md.
2. Move files into a structure like:
   data/raw, data/derived, code, output/tables, output/figures, paper, slides.
3. Initialize Git if needed.
4. Commit the starting point.
5. Create a new branch for restructuring.
6. Run any code that was moved or modified.
7. Compare outputs to prior results where possible.

Rules:
- Do not delete files.
- Do not edit raw data.
- Do not commit restricted/private data.
- Do not push to public GitHub unless I explicitly approve.
- Ask clarifying questions before acting if data sensitivity, target folder structure, GitHub privacy, or software environment is unclear.
- Define Git and software terms in plain language the first time they appear.
```

## Template 2: Minimal `.gitignore` for Econ/Finance Research

```gitignore
# Raw, restricted, and licensed data
data/raw/
data/restricted/
data/private/

# Common data formats
*.dta
*.sas7bdat
*.rds
*.parquet
*.feather
*.csv
*.xlsx
*.zip

# Secrets and local config
.env
*.key
*.pem

# Logs and caches
*.log
__pycache__/
.Rhistory
.RData
.DS_Store

# Generated outputs that can be rebuilt
output/temp/
tmp/
```

## Template 3: AGENTS.md for Research Repo

```markdown
# AGENTS.md

## Project Purpose
[One paragraph describing the research project.]

## Rules For AI Agents
- Never edit files in `data/raw/` or `data/restricted/`.
- Never commit or expose private, restricted, licensed, or identifiable data.
- Ask for approval before restructuring folders.
- Before editing code, explain the plan.
- After editing code, run the smallest relevant test or script.
- After editing paper text, preserve citations, numbers, notation, and hedging.
- Do not invent results, citations, robustness checks, or institutional facts.
- Ask clarifying questions if the task, data sensitivity, validation command, or permission boundary is unclear.
- Define technical terms briefly for non-CS economics/finance researchers.

## Folder Structure
- `data/raw/`: original data, do not edit
- `data/derived/`: cleaned data
- `code/`: scripts
- `output/tables/`: generated tables
- `output/figures/`: generated figures
- `paper/`: manuscript
- `slides/`: presentations

## Validation
Before reporting completion, state:
- files changed
- commands run
- outputs checked
- remaining uncertainty
```

## Template 3B: CLAUDE.md for Research Repo

Use this when working with Claude Code or another tool that reads project memory/instructions.

```markdown
# CLAUDE.md

## Project Purpose
[One paragraph describing the research project.]

## Current Research Stage
[idea / data cleaning / empirical analysis / theory / writing / revision / replication]

## Non-Negotiable Rules
- Do not edit `data/raw/`, `data/restricted/`, or `data/private/`.
- Do not upload, expose, summarize, or commit private, restricted, licensed, identifiable, or confidential material.
- Ask before changing file structure, running destructive commands, rewriting paper text, or preparing public output.
- Preserve citations, numbers, notation, table labels, variable definitions, sample definitions, and hedging.
- Do not invent results, citations, data sources, robustness checks, institutional facts, or theory claims.
- If policy or data sensitivity is uncertain, stop and ask.
- If the task, data rule, validation command, or expected output is unclear, ask clarifying questions before acting.
- Define technical terms briefly for non-CS economics/finance researchers.

## Preferred Workflow
1. Restate the task.
2. Propose a plan.
3. Identify files to read/edit.
4. Identify risks.
5. Wait for approval when edits or public actions are involved.
6. Implement narrowly.
7. Run checks.
8. Report files changed, commands run, outputs checked, and uncertainty.

## Validation Commands
[add commands such as `make`, `Rscript code/main.R`, `python code/build.py`, `latexmk paper/main.tex`]

## AI-Use Logging
After any accepted AI-assisted change, suggest an AI-USE-LOG entry.
```

## Template 3C: Institutional AI Policy Check

```text
Before using AI on this task, help me check the policy risk.

Task:
[describe]

Materials:
[public paper / coauthor draft / referee report / restricted data / licensed data / student data / code / public data]

Policies I must consider:
- university or employer policy: [known/unknown]
- journal or conference policy: [known/unknown]
- data-provider license: [known/unknown]
- funder or IRB/research ethics rule: [known/unknown]
- coauthor agreement: [known/unknown]

Return:
1. likely risk level;
2. policies I must check before proceeding;
3. safer alternatives, such as synthetic examples, metadata only, local approved tools, or manual review;
4. exact questions to ask my institution, coauthors, editor, or data provider.

Rule:
If permission is unclear, recommend not uploading or exposing the material.
If policy language is ambiguous, list the exact questions I should ask and who should answer them.
```

## Template 4: AI-USE-LOG.md

```markdown
# AI Use Log

| Date | Tool/model/version | Task | Input materials | Files touched | Output accepted | Human checks | Remaining uncertainty | Disclosure needed? | Commit |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| YYYY-MM-DD | [tool/model/version if known] | [task] | [public/private/licensed/restricted?] | [files] | [what was used] | [checks] | [uncertainty] | [yes/no/check policy] | [hash] |
```

For a fuller reproducibility packet or disclosure paragraph, use [Verification, Reproducibility, and Disclosure Skills](17-verification-reproducibility-and-disclosure-skills.md).

## Template 5: Replication Package Intake

```text
Analyze this replication package as a research assistant.

Inputs:
- Package folder: [path or file list]
- Paper: [title/link/PDF]
- Target table/figure: [if any]

Tasks:
1. Identify the main entry scripts.
2. Map scripts to tables and figures.
3. Identify raw data, derived data, and generated outputs.
4. Find software dependencies.
5. Find hard-coded paths and local assumptions.
6. Identify missing files or unclear instructions.
7. Propose a run order.
8. Explain what can be replicated and what cannot.

Rules:
- Do not alter files yet.
- Do not claim replication success unless code runs and outputs match.
- Create a checklist before running anything.
- Ask clarifying questions if the paper, target output, software environment, or data permission is unclear.
```

Sources and workflow influences: Paul Goldsmith-Pinkham's emphasis on replication package infrastructure and AI-assisted code/data workflows; Git and GitHub documentation.
