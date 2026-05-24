> Copyright (c) 2026 SuperJayLiu (Chaojie Liu). Licensed under the repository MIT License.

# Coding, Data Analysis, and Debugging Skills

Use these when AI is helping with Stata, R, Python, MATLAB, SAS, LaTeX, tables, figures, or replication code.

> [!WARNING]
> AI-generated code is not evidence. Run it, inspect outputs, test small examples, and compare against the empirical design.

For full data-production workflows, use [Data Cleaning, Merging, Analysis, and Output Skills](14-data-cleaning-merging-analysis-and-output-skills.md). This page is for debugging, review, and consistency checks.

## Skill 1: Debug Stata/R/Python Research Code

```text
Act as a research coding assistant for economics/finance.

Code:
[paste code or error]

Context:
- Language/software: [Stata/R/Python/Matlab/SAS]
- Research task: [task]
- Data structure: [unit, time, panel/cross-section/time-series]
- Expected output: [table/figure/data file]
- Error or problem: [error message or wrong output]

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
[paste code]

Paper/method description:
[paste short description]

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
- Table/figure: [paste or describe]
- Results paragraph: [paste]
- Code snippet or table notes: [paste]
- Empirical design: [brief description]

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
[paste table or describe]

Audience:
[MBA/PhD seminar/conference/public/policy]

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
- File tree: [paste]
- Main scripts: [paste names or content]
- Software: [Stata/R/Python/Matlab/SAS/LaTeX]
- Target output: [tables/figures/paper]

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
[paste]

Research task:
[task]

Expected output:
[table/figure/dataset/model result]

Project facts:
- Data: [data]
- Unit/time: [unit/time]
- Method: [method]
- Existing baseline output, if any: [describe]
- Software: [Stata/R/Python/MATLAB/SAS]

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

Sources and workflow influences: Paul Goldsmith-Pinkham's VS Code/Git/data workflow examples, applied methods implementation norms, and recent concerns about dependency gaps in AI-generated code.
