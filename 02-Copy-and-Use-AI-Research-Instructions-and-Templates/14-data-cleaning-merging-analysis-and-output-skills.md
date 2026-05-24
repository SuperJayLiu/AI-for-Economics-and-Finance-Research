> Copyright (c) 2026 SuperJayLiu (Chaojie Liu). Licensed under the repository MIT License.

# Data Cleaning, Merging, Analysis, and Output Skills

Use these skills when AI is helping you produce research objects: cleaned data, merge scripts, variable dictionaries, exploratory analysis, tables, figures, and testable code.

> [!IMPORTANT]
> This page is about safe execution. AI can draft code and plans, but it cannot certify that your data construction is correct. Run the code, inspect intermediate files, test toy examples, and compare outputs against the paper's design.

Questions or suggestions for this part: email [jay.liu@bristol.ac.uk](mailto:jay.liu@bristol.ac.uk) with subject `[AI Econ Finance Data Skill] Suggestion`.

## Choose a Skill

| Research task | Use |
| --- | --- |
| turn a messy data task into a reproducible pipeline | Skill 1 |
| plan a WRDS/CRSP/Compustat-style merge | Skill 2 |
| define and audit constructed variables | Skill 3 |
| implement Fama-MacBeth or portfolio sorts safely | Skill 4 |
| create EDA, tables, and figures without hidden hand edits | Skill 5 |
| test AI-written code on toy data before using real data | Skill 6 |

## Skill 1: Reproducible Research Data Pipeline Builder

```text
Act as an economics/finance research data-pipeline assistant.

Project:
- Research question: [question]
- Data sources: [sources]
- Software: [Stata/R/Python/SAS/MATLAB]
- Raw files available: [list files, do not paste restricted data]
- Unit of observation: [unit]
- Time frequency: [daily/monthly/quarterly/annual/etc.]
- Target outputs: [analysis-ready dataset/tables/figures]
- Data restrictions: [public/licensed/restricted/confidential]

Design a reproducible pipeline with these stages:
1. raw data intake;
2. raw data inventory;
3. cleaning and standardization;
4. merging and link rules;
5. variable construction;
6. analysis-ready dataset;
7. tables and figures;
8. logs and validation checks.

For each stage, return:
- input files;
- output files;
- script name;
- checks to run;
- failure modes;
- what should never be modified.

Rules:
- Do not ask me to upload restricted or licensed data.
- Do not overwrite raw data.
- Use relative paths.
- Separate raw, derived, output, and logs.
- Include a toy-data test before real-data execution.
- If project facts are missing, mark [NEEDS AUTHOR INPUT].

Output:
1. proposed folder structure;
2. run order;
3. script skeleton names;
4. validation checklist;
5. AI-use log entry template for this pipeline.
```

## Skill 2: WRDS, CRSP, Compustat, and CCM Merge Plan

Use this before writing merge code for finance data.

Resource note: external WRDS-oriented agent toolkits show a useful pattern: separate specialist agents for CRSP, Compustat, OptionMetrics, TAQ, and a query orchestrator; preload schema information before writing queries; and keep psql/SSH/SAS execution rules explicit. Do not copy permissions or connection settings blindly. WRDS credentials, SSH keys, scratch paths, licensed extracts, and downloaded files must follow WRDS and institutional rules.

```text
Act as a finance data-construction auditor.

I need a merge plan for:
- Data sources: [CRSP/Compustat/CCM/IBES/13F/TRACE/Dealscan/other]
- Unit of observation: [firm-year/firm-quarter/stock-month/stock-day/etc.]
- Sample period: [period]
- Required identifiers: [permno/permco/gvkey/cusip/cik/ticker/isin/etc.]
- Return frequency, if relevant: [daily/monthly]
- Accounting timing rule: [fiscal year/month, reporting lag, public availability assumption]
- Link table, if relevant: [CCM linktable rules known/unknown]
- Outcome variables: [outcomes]
- Predictor/treatment variables: [predictors]
- Sample screens: [exchange/share code/industry/price filters/etc.]

Create a data merge plan that specifies:
1. identifier priority and why;
2. CRSP/Compustat/CCM linking logic;
3. link-date validity checks;
4. linktype/linkprim assumptions to verify;
5. fiscal-year and calendar-time alignment;
6. reporting-lag rule to avoid look-ahead bias;
7. delisting return treatment, if returns are used;
8. duplicate checks;
9. survivorship and selection risks;
10. audit tables to print after each merge.

Return:
- step-by-step merge algorithm;
- code skeleton in [Stata/R/Python];
- checks after each merge;
- red flags that should stop the analysis;
- exact assumptions I must verify in WRDS/data documentation.

Rules:
- Do not invent WRDS variable names if I have not supplied them.
- Do not assume ticker/CUSIP matching is sufficient.
- Do not ignore link-date validity.
- Do not use future accounting information for past returns.
- Do not treat a successful merge rate as proof of correctness.
```

## Skill 3: Variable Construction Dictionary and Audit

```text
Create a variable construction dictionary for this economics/finance project.

Project facts:
- Research question: [question]
- Data sources: [sources]
- Unit/time: [unit/time]
- Variables to construct: [list]
- Existing code or formulas: [paste or describe]
- Intended table/figure use: [where each variable appears]

For each variable, produce:
1. final variable name;
2. plain-language definition;
3. source fields used;
4. formula;
5. timing rule;
6. winsorization/trimming/imputation rule;
7. missing-value rule;
8. unit and scale;
9. expected range or sign;
10. code file where it is created;
11. table/figure where it is used;
12. validation check.

Also flag:
- post-treatment controls;
- look-ahead variables;
- variables that mix annual and monthly timing;
- transformations that change interpretation;
- labels that may mislead readers.

Return:
- variable dictionary table;
- audit checklist;
- suggested code comments;
- questions for the researcher.
```

## Skill 4: Fama-MacBeth and Portfolio Sort Implementation Plan

Use this for asset pricing, return predictability, fund performance, and cross-sectional finance tests.

```text
Act as an asset-pricing implementation assistant.

Research task:
- Signal/predictor: [signal]
- Returns: [raw/excess/abnormal], frequency [daily/monthly/etc.]
- Universe: [stocks/funds/bonds/options/etc.]
- Sample period: [period]
- Sorting rule or regression design: [portfolio sorts/Fama-MacBeth/panel regression]
- Controls or characteristics: [list]
- Risk model or benchmark: [CAPM/FF3/FF5/q-factor/characteristics/etc.]
- Transaction cost/liquidity treatment: [details]
- Inference: [Newey-West/Fama-MacBeth SE/clustering/bootstrap/etc.]

Create an implementation plan with:
1. timing diagram: when signal is measured and when returns are realized;
2. sample screens and exclusion rules;
3. portfolio breakpoints, weighting, and rebalancing frequency;
4. Fama-MacBeth first-stage and second-stage steps, if used;
5. risk-adjustment procedure;
6. standard error and lag choices;
7. delisting return and survivorship checks;
8. multiple-testing and out-of-sample discipline;
9. output table shells;
10. code test using toy data.

Return:
- pseudo-code;
- code skeleton in [Stata/R/Python];
- expected intermediate outputs;
- table notes draft;
- checks that would catch look-ahead bias.

Rules:
- Do not use information unavailable at portfolio formation.
- Do not turn predictability into causal language.
- Do not hide transaction costs or liquidity limits when relevant.
- Do not claim a new factor without multiple-testing and out-of-sample discussion.
```

## Skill 5: EDA, Table, and Figure Production Workflow

```text
Design a reproducible EDA/table/figure workflow for this paper.

Inputs:
- Research question: [question]
- Analysis-ready dataset: [file or description]
- Main variables: [variables]
- Main tables/figures needed: [list]
- Software: [Stata/R/Python/LaTeX]
- Target output format: [CSV/LaTeX/HTML/PDF/PNG/SVG]

Create:
1. EDA checklist;
2. summary statistics plan;
3. balance or pre-period comparison plan, if relevant;
4. main regression/table plan;
5. figure plan with captions and units;
6. output folder structure;
7. reproducible export rules;
8. consistency checks between code, tables, figures, and prose.

Every table/figure must include:
- source dataset;
- script that generated it;
- sample used;
- variable definitions;
- date generated;
- known limitations.

Return:
- run order;
- code skeleton;
- table/figure inventory;
- verification checklist.

Rules:
- Do not manually copy values from console output into the paper.
- Do not change table labels to sound stronger than the estimate.
- Do not omit uncertainty intervals when they matter.
```

## Skill 6: Toy Data Test Harness for AI-Written Code

Use this before running AI-written code on real data.

```text
Create a toy-data test for this research code.

Code or task:
[paste code or describe task]

Expected behavior:
[what the code should do]

Research context:
- Unit/time: [unit/time]
- Variables: [variables]
- Method: [merge/variable construction/regression/event study/etc.]
- Software: [Stata/R/Python]

Build a small toy dataset where the correct answer is known by inspection.

Return:
1. toy data table;
2. code to create the toy data;
3. expected output;
4. why the expected output is correct;
5. failure cases the test should catch;
6. how to adapt the test before running on real data.

Rules:
- Keep the toy data tiny.
- Include at least one edge case: duplicate, missing value, boundary date, or unmatched merge key.
- Do not say the real code is correct just because the toy test passes.
```

## Sources and Workflow Influences

This page draws on applied empirical implementation norms, Paul Goldsmith-Pinkham's emphasis on AI lowering the cost of data assembly and analysis, finance replication concerns, and common WRDS/CRSP/Compustat workflow risks.

Last checked: 2026-05-24
