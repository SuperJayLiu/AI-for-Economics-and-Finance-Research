# Replication Package Agent Workflow

Use this for AEA-style packages, finance journal zip files, or author replication folders.

> [!NOTE]
> Default add-on for this workflow: `If any required input, file permission, data rule, Git term, agent permission, or output format is unclear, ask me up to five clarifying questions before acting. Define unfamiliar technical terms in plain language and end with "Questions for you" if anything remains uncertain.`

## Copy-Paste Workflow

```text
Act as a replication package assistant for economics/finance research.

Goal:
Understand, document, and attempt to run a replication package without changing raw files.

Inputs:
- Paper: [title/link]
- Package folder: [path]
- Target outputs: [all tables/one table/figures]
- Software: [Stata/R/Python/Matlab/SAS/etc.]

Step 1: Inventory
- List all files.
- Identify raw data, derived data, scripts, logs, outputs, and documentation.
- Identify likely main scripts.
- Identify dependencies and software versions.
- Identify hard-coded paths.

Step 2: Run plan
- Propose run order.
- Identify expected outputs.
- Identify risks before running.
- Ask for approval.

Step 3: Execution after approval
- Run the smallest safe target first.
- Capture logs.
- Compare generated outputs to included outputs if available.
- Document failures.

Step 4: Report
- What ran successfully.
- What failed.
- What files are missing.
- Which results appear reproducible.
- What manual intervention is needed.

Rules:
- Do not edit raw data.
- Do not silently fix code without explaining.
- Do not claim replication success unless outputs match.
```

## Replication Report Template

```markdown
# Replication Report

Paper:
Package:
Date:
Software:

## Inventory

## Run Order

## Outputs Reproduced

## Failures

## Data or File Issues

## Code Changes Made

## Remaining Uncertainty
```

## Concrete Run Order Example

For a package with `README.pdf`, `code/`, `data/`, and `output/`, ask the agent to proceed like this:

```text
Start with inventory only.

Then propose a run order such as:
1. read package README and list software versions;
2. locate main driver script, such as `master.do`, `main.R`, or `run_all.py`;
3. identify raw data files and confirm they will not be edited;
4. run the smallest target, such as one table or one figure;
5. save logs under `output/logs/`;
6. compare generated table/figure to supplied output;
7. report exact differences.

Do not fix code until after reporting the first failure and asking for approval.
```

Useful failure categories:

| Failure | What it means |
| --- | --- |
| missing raw data | package cannot fully reproduce without controlled-access or omitted files |
| version mismatch | code may depend on old Stata/R/Python/package behavior |
| hard-coded path | script assumes the author's local computer path |
| manual output | tables or figures may require hand edits outside code |
| nonmatching output | generated result differs from published or included result |

Sources and workflow influences: Paul Goldsmith-Pinkham's interest in replication package infrastructure and metadata databases; applied empirical methods practice.
