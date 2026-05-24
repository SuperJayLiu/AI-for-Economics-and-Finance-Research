> Copyright (c) 2026 SuperJayLiu (Chaojie Liu). Licensed under the repository MIT License.

# Git, Data, Replication, and Research Safety Templates

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

## Template 4: AI-USE-LOG.md

```markdown
# AI Use Log

| Date | Tool/model | Task | Files touched | Output accepted | Human checks | Remaining uncertainty | Commit |
| --- | --- | --- | --- | --- | --- | --- | --- |
| YYYY-MM-DD | [tool] | [task] | [files] | [what was used] | [checks] | [uncertainty] | [hash] |
```

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
```

Sources and workflow influences: Paul Goldsmith-Pinkham's emphasis on replication package infrastructure and AI-assisted code/data workflows; Git and GitHub documentation.

