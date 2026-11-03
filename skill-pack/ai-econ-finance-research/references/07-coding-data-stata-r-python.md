# Coding, Data, Stata, R, Python, Tables, And Figures

Use this for code help, debugging, data cleaning, merges, EDA, tables, and figures.

## Required Inputs

Ask for:

1. software: Stata, R, Python, Matlab, SQL, or other;
2. task and expected output;
3. code or error message;
4. data schema, not confidential raw data;
5. unit, time, keys, and merge rules;
6. expected table/figure;
7. whether code may be edited or only reviewed.

## Safe Coding Workflow

1. Diagnose before editing.
2. Propose minimal change.
3. Build toy-data known-answer test.
4. Run or explain checks.
5. Compare output to research design.
6. Record changes in AI-use log.

## Copy-Ready Instruction

```text
Act as a Stata/R/Python research coding assistant for economics and finance.

First ask for the software, research goal, expected output, code/error, data schema, unit, time, keys, and data sensitivity if I have not provided them.

Do not request restricted raw data. Work from metadata, toy rows, synthetic data, code, logs, or public examples when needed.

Before changing code, explain the likely issue, propose a minimal plan, and ask for confirmation.

Produce corrected code or a patch plan, a toy-data known-answer test, and a checklist for sample, timing, variables, merges, and output interpretation.
```

## Batch Measurement

For bulk LLM labeling, require an input-ID manifest, a hand-checked pilot, bounded retries/spending, and a resumable item ledger. Reconcile missing, duplicate, refused, malformed, and validated responses before accepting completion. A failed response is not a substantive zero. Keep licensed text and credentials out of public logs. For the detailed contract, use the handbook's [batch acceptance gate](https://github.com/SuperJayLiu/AI-for-Economics-and-Finance-Research/blob/main/02-Copy-and-Use-AI-Research-Instructions-and-Templates/skills/08-coding-data-analysis-and-debugging-skills.md#batch-measurement-acceptance).

An accounted-for failure remains unusable for analysis until resolved or covered by a documented, researcher-approved exclusion rule with reported coverage/sample effects.

## Language Notes

- Stata: check `merge`, duplicates, `xtset`, `reghdfe`, `esttab`, clustering, and missing values.
- R: check `dplyr`, `fixest`, `did`, `rdrobust`, date handling, joins, and reproducible scripts.
- Python: check `pandas`, `statsmodels`, `linearmodels`, merge keys, index types, and environment reproducibility.

## Sources and Workflow Influences

Manish Jha, Georgia State University, [AI for Finance Research](https://mjha91.github.io/pdf/AIFinanceResearch.pdf), cover 2026-10-30; checked 2026-11-03. Influence: scripted item-level accountability in bulk measurement. No explicit reuse license found on author page/PDF; original high-level adaptation only, with no lecture text, prompts, templates, code, figures, or slide structure copied. Lecture remains outside the repository MIT license.
