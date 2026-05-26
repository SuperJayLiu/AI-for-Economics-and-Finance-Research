> Copyright (c) 2026 SuperJayLiu (Chaojie Liu). Licensed under the repository MIT License.

# Coding, Data Analysis, and Debugging Skills

Use these when AI is helping with Stata, R, Python, MATLAB, SAS, LaTeX, tables, figures, or replication code.

> [!WARNING]
> AI-generated code is not evidence. Run it, inspect outputs, test small examples, and compare against the empirical design.

For full data-production workflows, use [Data Cleaning, Merging, Analysis, and Output Skills](14-data-cleaning-merging-analysis-and-output-skills.md). This page is for debugging, review, and consistency checks.

> [!NOTE]
> Import/use-as-skill protocol for any block on this page: `Start by collecting only the missing inputs needed for the task. Ask up to five clarifying questions when required inputs, data rules, method details, permissions, audience, or output format are unclear. For long outputs, file-producing tasks, slides, code, methods sections, literature reviews, referee responses, or agentic workflows, first return "Proposed structure and assumptions" and ask the user to confirm before producing the full output. Before finalizing, double-check for unsupported claims, invented citations or results, privacy risks, and mismatch with the requested format. End with "What I produced", "What I did not change", "What you must verify", and "Questions for you".`

## Skill 1: Debug Stata/R/Python Research Code

```text
Act as a research coding assistant for economics/finance.

Code:
If I have not provided this, ask me to provide: paste code or error

Context:
- Language/software: If I have not provided it, ask me to specify: Stata/R/Python/Matlab/SAS
- Research task: If I have not provided it, ask me to specify: task
- Data structure: If I have not provided it, ask me to specify: unit, time, panel/cross-section/time-series
- Expected output: If I have not provided it, ask me to specify: table/figure/data file
- Error or problem: If I have not provided it, ask me to specify: error message or wrong output

Tasks:
1. Explain what the code is trying to do.
2. Identify the most likely source of the error.
3. Suggest the smallest safe fix.
4. Explain whether the fix changes the empirical design.
5. Provide a test on a toy example if possible.
6. Tell me what output I should inspect after running.

Rules:
- Do not rewrite the whole script unless necessary.
- Do not change variable definitions silently.
- Do not change sample restrictions silently.
- Do not claim the result is correct until the code is run.
- If the code touches research data, propose a toy-data test before real-data execution.
```

## Skill 2: Code Review for Empirical Research

```text
Review this empirical research code for hidden mistakes.

Code:
If I have not provided this, ask me to provide: paste code

Paper/method description:
If I have not provided this, ask me to provide: paste short description

Check for:
- sample restrictions not documented in paper
- treatment/control timing errors
- merge problems
- duplicate observations
- missing value handling
- fixed effects or clustering mismatch
- generated variables that do not match definitions
- graph/table labels inconsistent with code
- look-ahead bias or survivorship bias if finance data
- hard-coded paths and non-reproducible assumptions
- AI-generated code that is too complex for the task
- output files created manually rather than from scripts

Return:
1. Severity-ranked issues.
2. Exact code lines or patterns to inspect.
3. Why each issue matters for the research claim.
4. Safer code or pseudo-code.
5. Tests I should run.
6. Whether a toy-data test, snapshot test, or output comparison is needed.
```

## Skill 3: Table and Figure Consistency Check

```text
Check whether this table/figure is consistent with the paper's text and code.

Inputs:
- Table/figure: If I have not provided it, ask me to specify: paste or describe
- Results paragraph: If I have not provided it, ask me to specify: paste
- Code snippet or table notes: If I have not provided it, ask me to specify: paste
- Empirical design: If I have not provided it, ask me to specify: brief description

Check:
1. Are coefficient signs, units, and magnitudes described correctly?
2. Are standard errors, stars, and p-values interpreted correctly?
3. Are fixed effects, controls, and sample restrictions reflected in notes?
4. Does the text overstate causal interpretation?
5. Are all panels/columns explained?
6. Are figure axes, labels, legends, and windows accurate?

Return a correction table with:
- issue
- location
- why it matters
- suggested revision
- verification needed
```

## Skill 4: Convert a Regression Table Into a Figure Plan

```text
Help me convert this regression table into a figure plan for teaching or presentation.

Table:
If I have not provided this, ask me to provide: paste table or describe

Audience:
If I have not provided this, ask me to provide: MBA/PhD seminar/conference/public/policy

Produce:
1. What the table shows in one sentence.
2. Which result is visually worth plotting.
3. Recommended chart type.
4. Axis labels and units.
5. What uncertainty to show.
6. What caveat must appear on the slide.
7. A draft caption.

Rules:
- Do not change numerical values.
- Do not turn non-causal estimates into causal claims.
- Do not hide standard errors or confidence intervals when they matter.
```

## Skill 5: Dependency and Reproducibility Check

```text
Audit this project for reproducibility gaps.

Inputs:
- File tree: If I have not provided it, ask me to specify: paste
- Main scripts: If I have not provided it, ask me to specify: paste names or content
- Software: If I have not provided it, ask me to specify: Stata/R/Python/Matlab/SAS/LaTeX
- Target output: If I have not provided it, ask me to specify: tables/figures/paper

Check:
1. Is there a single entry point to rebuild outputs?
2. Are package dependencies declared?
3. Are software versions recorded?
4. Are paths relative rather than local machine-specific?
5. Are raw and derived data separated?
6. Are outputs generated from code rather than manually copied?
7. Are random seeds set where needed?
8. Is there a README/DATA/AI-use log?

Return:
- reproducibility score from 0 to 5
- missing files
- needed fixes
- minimal Makefile or run order
```

## Skill 6: AI-Written Code Acceptance Gate

Use this before accepting code written by ChatGPT, Claude, Codex, Claude Code, Cursor, Copilot, or another agent.

```text
Decide whether I should accept this AI-written research code.

Code or diff:
If I have not provided this, ask me to provide: paste

Research task:
If I have not provided this, ask me to provide: task

Expected output:
If I have not provided this, ask me to provide: table/figure/dataset/model result

Project facts:
- Data: If I have not provided it, ask me to specify: data
- Unit/time: If I have not provided it, ask me to specify: unit/time
- Method: If I have not provided it, ask me to specify: method
- Existing baseline output, if any: If I have not provided it, ask me to specify: describe
- Software: If I have not provided it, ask me to specify: Stata/R/Python/MATLAB/SAS

Check:
1. Does the code implement the stated research design?
2. Does it change sample restrictions, variables, timing, or inference?
3. Does it touch raw or restricted data?
4. Are paths, dependencies, seeds, and outputs reproducible?
5. Is the code simpler than the problem requires, or unnecessarily clever?
6. What toy-data test should pass?
7. What real-data output should be compared to the previous version?

Return:
- accept / revise / reject;
- required edits before acceptance;
- tests to run;
- outputs to inspect;
- AI-use log entry.

Rules:
- Do not accept code because it merely runs.
- Do not accept code that changes the empirical design without explicit human approval.
- Do not accept code that cannot be explained to a coauthor or referee.
```

## Skill 7: Python Empirical Analysis Assistant

Use this when the analysis is in Python, especially with `pandas`, `numpy`, `statsmodels`, `linearmodels`, `pyfixest`, `scikit-learn`, `matplotlib`, or `seaborn`.

```text
Act as a Python empirical research assistant for economics/finance.

Before giving final code, ask clarifying questions if the data structure, variable timing, sample definition, method, output format, or data-safety rule is unclear.

Research task:
If I have not provided this, ask me to provide: describe task

Python context:
- Current packages: If I have not provided it, ask me to specify: pandas/numpy/statsmodels/linearmodels/pyfixest/scikit-learn/other
- Data structure: If I have not provided it, ask me to specify: cross-section/panel/time series/event-level/text data
- Unit of observation: If I have not provided it, ask me to specify: firm-year/person-month/security-day/etc.
- Time variable: If I have not provided it, ask me to specify: name and frequency
- Outcome: If I have not provided it, ask me to specify: variable
- Treatment/exposure/key regressor: If I have not provided it, ask me to specify: variable
- Fixed effects/clustering/inference: If I have not provided it, ask me to specify: if known
- Desired output: If I have not provided it, ask me to specify: clean data/table/figure/model output

Code or error:
If I have not provided this, ask me to provide: paste code, traceback, or current plan

Tasks:
1. Explain the current code or proposed analysis in plain language.
2. Identify the smallest safe change needed.
3. State whether the change affects sample, timing, variables, fixed effects, or inference.
4. Provide Python code using clear, boring, reproducible patterns.
5. Create a toy-data test with a known expected result.
6. List outputs I should inspect after running.
7. End with "Questions for you" if anything remains uncertain.

Python-specific guardrails:
- Use relative paths, not local machine paths.
- Never overwrite raw data.
- Prefer explicit column lists and documented merges.
- Use assertions for unique keys, missingness, duplicates, and merge rates.
- Report package imports and any package assumptions.
- For panel regressions, make the index, fixed effects, clustering, and dropped observations explicit.
- For finance data, check look-ahead bias, survivorship bias, delisting returns, event windows, and identifier changes when relevant.
```

Mini example:

```text
Task:
Build a firm-year panel and estimate a regression with firm and year fixed effects.

Good AI output should include:
- `merge(validate="one_to_one")` or another explicit merge validation where appropriate;
- duplicate-key and missingness assertions;
- a small synthetic firm-year panel that proves the fixed-effect code runs;
- a warning if the requested package cannot cluster standard errors as needed;
- a note that code running successfully does not validate identification.

Reject output if:
- it silently drops unmatched observations;
- it uses calendar-year outcomes with future accounting variables without a reporting-lag rule;
- it reports coefficients without units, sample size, and fixed-effect/clustering details.
```

## Skill 8: R Econometrics Workflow Assistant

Use this when the analysis is in R, especially with `tidyverse`, `data.table`, `fixest`, `did`, `rdrobust`, `plm`, `modelsummary`, `ggplot2`, or `targets`.

```text
Act as an R econometrics workflow assistant for economics/finance.

Before giving final code, ask clarifying questions if the empirical design, data structure, variable timing, package choice, or output target is unclear.

Research task:
If I have not provided this, ask me to provide: describe task

R context:
- Packages used or preferred: If I have not provided it, ask me to specify: tidyverse/data.table/fixest/did/rdrobust/plm/modelsummary/ggplot2/targets/other
- Data structure: If I have not provided it, ask me to specify: cross-section/panel/time series/event study/text data
- Unit of observation: If I have not provided it, ask me to specify: firm-year/county-month/security-day/etc.
- Outcome: If I have not provided it, ask me to specify: variable
- Treatment/exposure/key regressor: If I have not provided it, ask me to specify: variable
- Fixed effects: If I have not provided it, ask me to specify: if any
- Clustering/inference: If I have not provided it, ask me to specify: if any
- Output target: If I have not provided it, ask me to specify: table/figure/cleaned data/report

Current code or problem:
If I have not provided this, ask me to provide: paste code, error, warning, or plan

Tasks:
1. Explain what the current R code is trying to do.
2. Identify design-relevant risks before editing code.
3. Suggest the minimal code change or clean workflow.
4. Include checks for joins, missingness, duplicate keys, timing, and sample loss.
5. If estimating a model, state the estimand, fixed effects, clustering, and diagnostic outputs.
6. Provide a toy-data test or small simulated example where possible.
7. End with "Questions for you" if any research choice is unresolved.

R-specific guardrails:
- Do not silently change factor/reference categories, sample filters, winsorization, or clustering.
- Use explicit `join_by()`/key checks or `data.table` keys when merging.
- For `fixest`, write the formula so fixed effects and clustered SEs are visible.
- For DiD, do not default to TWFE when treatment timing is staggered without discussing heterogeneity and estimator choice.
- For RD, report bandwidth, running variable, cutoff, polynomial order, and manipulation/density checks.
- For output tables, ensure labels match the paper's variable definitions and model notes.
```

Mini example:

```text
Task:
Estimate a staggered-adoption DiD and create a coefficient plot.

Good AI output should include:
- a warning that plain TWFE event-study coefficients may be misleading under heterogeneous treatment effects;
- a suggested estimator workflow such as group-time or imputation-style estimates when appropriate;
- checks for treatment timing, never-treated or not-yet-treated comparison groups, and event-time support;
- code that prints dropped observations and sample counts by cohort/event time;
- a plot caption that does not treat insignificant pre-trends as proof of validity.

Reject output if:
- it defaults to `lm(y ~ treat + factor(id) + factor(year))` without discussing timing;
- it calls a pre-trend test "passed" without power or confidence-band discussion;
- it changes clustering without explaining the design reason.
```

## Skill 9: Stata Research Workflow Assistant

Use this when the analysis is in Stata, including do-file debugging, panel setup, event studies, regression tables, or data cleaning.

```text
Act as a Stata research workflow assistant for economics/finance.

Before giving final code, ask clarifying questions if variable names, panel keys, time variables, sample restrictions, installed packages, or output expectations are unclear.

Research task:
If I have not provided this, ask me to provide: describe task

Stata context:
- Stata version, if known: If I have not provided it, ask me to specify: version
- Data structure: If I have not provided it, ask me to specify: cross-section/panel/time series/event-level
- Unit of observation: If I have not provided it, ask me to specify: firm-year/person-month/security-day/etc.
- ID variable(s): If I have not provided it, ask me to specify: id vars
- Time variable: If I have not provided it, ask me to specify: time var and frequency
- Outcome: If I have not provided it, ask me to specify: variable
- Treatment/exposure/key regressor: If I have not provided it, ask me to specify: variable
- Fixed effects/clustering: If I have not provided it, ask me to specify: if known
- Packages used: If I have not provided it, ask me to specify: reghdfe/ivreghdfe/eventstudyinteract/csdid/estout/asdoc/other
- Desired output: If I have not provided it, ask me to specify: clean data/table/figure/log

Current do-file, command, or error:
If I have not provided this, ask me to provide: paste code/error/log excerpt

Tasks:
1. Explain the do-file or command in plain language.
2. Identify likely Stata-specific problems: sorting, duplicates, panel declaration, merge status, missing values, globals/locals, paths, package availability.
3. Suggest the smallest safe fix.
4. Show revised Stata code with comments.
5. Add diagnostic commands before and after the main operation.
6. State whether the fix affects the empirical design.
7. End with "Questions for you" if any research choice is unresolved.

Stata-specific guardrails:
- Never overwrite raw `.dta` files.
- Use `preserve`/`restore` carefully and explain why.
- After `merge`, report `_merge` counts and check unmatched observations before dropping anything.
- Before panel work, check `isid`, `duplicates report`, `xtset`, and time gaps.
- For high-dimensional fixed effects, make absorbed fixed effects and clustered standard errors explicit.
- For finance data, check PERMNO/GVKEY/link-table timing, delisting returns, event windows, and share/exchange-code filters when relevant.
- Use logs and relative paths so the workflow is reproducible.
```

Mini example:

```text
Task:
Merge CRSP monthly returns with Compustat annual fundamentals and run a portfolio-sort or panel regression.

Good AI output should include:
- `isid` or `duplicates report` checks before and after merges;
- `_merge` tabulations and an explanation before dropping unmatched rows;
- CCM link-date logic, not only GVKEY/PERMNO matching;
- an explicit lag/availability rule for accounting variables;
- diagnostics for share codes, exchange codes, delisting returns, and sample screens;
- output notes that match the paper's sample and variable definitions.

Reject output if:
- it drops `_merge != 3` without inspection;
- it overwrites the original `.dta`;
- it uses future accounting information for return prediction;
- it reports a table without documenting fixed effects and clustered standard errors.
```

Sources and workflow influences: Paul Goldsmith-Pinkham's VS Code/Git/data workflow examples, applied methods implementation norms, Aniket Panjwani's agentic coding exercise and Git/skills/planning warnings, Antonio Mele's economics skill catalog, Frank Lee's academic research skills catalog, Han Lulong's economics writing and AI-for-economists resource lists, and recent concerns about dependency gaps in AI-generated code.
