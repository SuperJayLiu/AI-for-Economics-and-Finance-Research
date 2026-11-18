> Copyright (c) 2026 SuperJayLiu (Chaojie Liu). Licensed under the repository MIT License.

# Empirical Methods Skills for Economics Research

These skills are tailored for applied economics: labor, public, development, health, education, macro, IO, urban, political economy, and related fields.

> [!IMPORTANT]
> These skills help draft and audit methods prose. They do not choose identification for you. You must verify design assumptions, code, tables, and data provenance.

> [!NOTE]
> Import/use-as-skill protocol for any block on this page: `Start by collecting only the missing inputs needed for the task. Ask up to five clarifying questions when required inputs, data rules, method details, permissions, audience, or output format are unclear. For long outputs, file-producing tasks, slides, code, methods sections, literature reviews, referee responses, or agentic workflows, first return "Proposed structure and assumptions" and ask the user to confirm before producing the full output. Before finalizing, double-check for unsupported claims, invented citations or results, privacy risks, and mismatch with the requested format. End with "What I produced", "What I did not change", "What you must verify", and "Questions for you".`

## Choose the Right Skill

| Need | Use |
| --- | --- |
| write a first methods draft from verified facts | Skill 1 |
| audit an existing methods section | Skill 2 |
| compare methods prose to scripts/tables | Skill 3 |
| check whether the design is credible before writing | Skill 4 |
| create a reviewer-facing limitations paragraph | Skill 5 |

For execution, pair this page with [Data Cleaning, Merging, Analysis, and Output Skills](14-data-cleaning-merging-analysis-and-output-skills.md). For method-specific checks, use [Causal Inference, Econometrics, and Time-Series Skills](11-causal-inference-econometrics-and-time-series-skills.md).

## Filled Mini Example

```text
Research question:
Do expanded bus routes affect employment among low-income workers?

Design:
Staggered rollout across neighborhoods, monthly employment outcomes, neighborhood and month fixed effects, event-study graph.

Good AI output should:
- ask whether treatment timing is staggered and whether effects may be heterogeneous;
- ask which DiD/event-study estimator is used;
- describe the identifying variation and comparison group;
- flag pre-trend power, clustering, spillovers, and neighborhood selection;
- mark missing information as NEEDS AUTHOR INPUT.

Bad AI output to reject:
"Because the regression includes fixed effects, the coefficient identifies the causal effect."
Reject because fixed effects alone do not establish identification.
```

## Skill 1: Draft Empirical Methods Section for Economics

```text
Draft an empirical methods section for an applied economics paper.

Inputs:
- Research question: If I have not provided it, ask me to specify: question
- Setting/institutional background: If I have not provided it, ask me to specify: setting
- Unit of observation: If I have not provided it, ask me to specify: unit
- Sample period: If I have not provided it, ask me to specify: period
- Data sources: If I have not provided it, ask me to specify: sources
- Outcome variables: If I have not provided it, ask me to specify: outcomes
- Treatment/exposure/shock: If I have not provided it, ask me to specify: treatment
- Control variables: If I have not provided it, ask me to specify: controls
- Empirical design: If I have not provided it, ask me to specify: DiD/event study/RD/IV/RCT/panel FE/synthetic control/other
- Main estimating equation, if any: If I have not provided it, ask me to specify: equation
- Identification assumption: If I have not provided it, ask me to specify: assumption
- Threats to validity: If I have not provided it, ask me to specify: threats
- Inference plan: If I have not provided it, ask me to specify: standard errors/clustering/randomization inference/etc.
- Current estimator or package, if known: If I have not provided it, ask me to specify: e.g., fixest/reghdfe/csdid/eventstudyinteract/did_imputation/rdrobust/etc.

Write:
1. Data and sample paragraph.
2. Variable construction paragraph.
3. Empirical specification with equation.
4. Identification argument.
5. Inference paragraph.
6. Threats to validity and planned robustness checks.
7. Interpretation paragraph explaining what the coefficient means.
8. A short "what this design can and cannot establish" paragraph.
9. A paragraph explaining why the chosen estimator is appropriate for timing, heterogeneity, and inference.

Rules:
- Do not claim causality unless the design and assumptions support it.
- Do not invent controls, sample restrictions, or robustness checks.
- State the identifying variation clearly.
- Explain economic magnitude, not only statistical significance.
- If the design is DiD/event study, discuss staggered timing and heterogeneous treatment effects where relevant.
- If the design is IV, discuss weak-instrument diagnostics and weak-IV robust inference where relevant.
- If the design is RD, discuss bandwidth, manipulation, and local interpretation.
- Use cautious applied economics prose.
- If information is missing, write NEEDS AUTHOR INPUT rather than filling it in.

Output format:
- Draft methods section.
- Missing inputs table.
- Verification checklist for code/tables.
```

## Skill 2: Check Empirical Methods Section for Economics

```text
Audit this empirical methods section as an applied econometrician.

Text:
If I have not provided this, ask me to provide: paste methods section

Known project facts:
- Research question: If I have not provided it, ask me to specify: question
- Data: If I have not provided it, ask me to specify: data
- Design: If I have not provided it, ask me to specify: design
- Main outcome/treatment: If I have not provided it, ask me to specify: variables

Check:
1. Is the unit of observation clear?
2. Is the treatment/exposure/shock clearly defined?
3. Is the comparison group credible?
4. Is the identifying variation stated?
5. Are fixed effects and controls justified?
6. Is inference/clustering appropriate?
7. Are pre-trends, balance, manipulation, exclusion, or monotonicity issues addressed where relevant?
8. Are robustness checks real or merely promised?
9. Does the prose overclaim causality?
10. Are coefficient interpretations correct?
11. Does the estimator match current applied standards for the design?
12. Is inference justified rather than mechanically chosen?

Return:
- Major issues.
- Minor issues.
- Suggested rewrite for the weakest paragraph.
- Checklist of analyses to verify in code.
- One paragraph explaining the strongest version of the design and the main reason it may fail.
```

## Skill 3: Methods-to-Code Consistency Check

```text
Compare the methods description to the code/table plan.

Methods text:
If I have not provided this, ask me to provide: paste

Code summary or script:
If I have not provided this, ask me to provide: paste or describe

Table/figure plan:
If I have not provided this, ask me to provide: paste

Identify mismatches:
- variables named in text but absent in code
- sample restrictions in code but not text
- controls/fixed effects in text but not code
- standard errors or clustering mismatch
- table labels that misstate coefficients
- robustness checks described but not run
- results interpreted beyond design

Return a table with: issue, evidence, severity, required fix.
```

## Skill 4: Identification Design Pre-Mortem

Use before writing or presenting the empirical strategy.

```text
Act as a skeptical applied microeconomist reviewing my proposed design before I write the methods section.

Project facts:
- Research question: If I have not provided it, ask me to specify: question
- Setting: If I have not provided it, ask me to specify: institutional background
- Data: If I have not provided it, ask me to specify: sources, unit, period
- Outcome: If I have not provided it, ask me to specify: outcome
- Treatment/exposure/shock: If I have not provided it, ask me to specify: treatment
- Proposed design: If I have not provided it, ask me to specify: DiD/event study/RD/IV/RCT/panel FE/synthetic control/etc.
- Comparison group or identifying variation: If I have not provided it, ask me to specify: describe
- Timing: If I have not provided it, ask me to specify: what happens when
- Main concern: If I have not provided it, ask me to specify: concern
- Estimator currently planned: If I have not provided it, ask me to specify: if known

Assess:
1. What is the implied experiment or quasi-experiment?
2. What variation identifies the coefficient?
3. What would make the design credible?
4. What would make it fail?
5. What balance, pre-trend, manipulation, placebo, or falsification checks are relevant?
6. What data or institutional facts must be documented?
7. What language should I avoid in the paper?
8. Which estimator or diagnostic would a good referee expect for this design?

Return:
- one-sentence design summary
- identifying variation
- identifying assumption
- top five threats
- estimator and inference concerns
- minimum evidence needed before writing causal language
- suggested methods paragraph outline
```

## Skill 5: Limitations Paragraph That Does Not Undermine the Paper

Use when you need honest limitations without vague defensiveness.

```text
Draft a limitations paragraph for an applied economics empirical paper.

Inputs:
- Research question: If I have not provided it, ask me to specify: question
- Design: If I have not provided it, ask me to specify: design
- Main result: If I have not provided it, ask me to specify: result
- Data limitations: If I have not provided it, ask me to specify: limitations
- Identification limitations: If I have not provided it, ask me to specify: limitations
- External validity limits: If I have not provided it, ask me to specify: limits
- What the paper still contributes: If I have not provided it, ask me to specify: contribution

Write a concise limitations paragraph that:
1. states what the design cannot prove;
2. explains which threats remain;
3. avoids overstating weakness;
4. preserves the paper's real contribution;
5. does not add new robustness checks or citations.

Also return a checklist of claims in the paper that should be softened.
```

Sources and workflow influences: Paul Goldsmith-Pinkham's Applied Empirical Methods course emphasis on practical implementation, research design intuition, communication, and disentangling the experiment behind causal claims.

## Group Encoding and GATE Verification

Use inside the existing empirical-method/code audit when estimating group average treatment effects with DoubleML scalar PLR or IRM. Request exact installed revision/API, score, fitted-model evidence, analytic row IDs/order, group definitions, group table and dtypes, missing-value policy, sample splits, repetitions and covariance options. Missing inputs remain **UNVERIFIED**.

```text
1. State the group estimand and freeze its definition before outcome-driven specification search. Confirm that the chosen score supports the requested effect; in the inspected IRM scalar implementation CATE/GATE requires score='ATE'. A working dtype does not establish identification or justify selecting favorable subgroups.
2. Match every group row to the fitted analytic observation, including order and exclusions. Inspect actual membership values, missingness, group counts and intended coverage. For a complete partition require exactly one active 0/1 indicator per row; document any deliberate incomplete coverage. Arbitrary integer labels are not a one-hot matrix. Never cast a multi-category numeric column to bool to bypass an error.
3. Record whether input is one string-label column or an explicit indicator matrix, including the resulting column-to-group map. In the audited revision NumPy bool, signed integer and unsigned integer dtypes enter the indicator path; multi-column floats and pandas nullable Int64 are rejected. Acceptance does not verify binary values or mutual exclusivity. Do not silently coerce nullable columns or missing labels into nonmembership; resolve missingness and recheck membership first.
4. On the SAME fitted object, sample, splits, score and covariance settings, encode the SAME valid indicator matrix as bool and supported NumPy integer dtypes. Compare group names/order, coefficients and standard errors within declared tolerances; check reported intervals separately. Do not refit nuisance learners between comparisons. If comparing a single string column, explicitly reconcile generated group columns and reference conventions before comparing outputs.
5. Distinguish upstream assertions from checks actually run locally. Archive revision, group map/counts, dtype comparisons, output differences and affected tables. The November 18 correction concerns an unreleased scalar API, not every DoubleML interface or installed release. Preserve archived environments and verify source revision before any deliberate upgrade.
6. Stop interpretation if membership, alignment, score support or encoding equivalence is unresolved. Small-group warnings do not certify overlap or reliable inference; review support, treatment overlap and multiple subgroup comparisons separately. Passing this computational check does not validate causal assumptions or economic significance.

Return a ledger: revision/API/score, analytic IDs, group definitions and coverage, dtypes/missingness, matched-fit comparisons/tolerances, upstream-versus-local evidence, affected outputs, unresolved issues and next action.
```

### Sources and Workflow Influences for GATE Encoding

DoubleML project / Philipp Bach, Victor Chernozhukov, Sven Klaassen, Malte S. Kurz and Martin Spindler (copyright holders in the [pinned BSD-3-Clause license](https://github.com/DoubleML/doubleml-for-py/blob/6dd568a85df45cd668301891e1a1ed57c68554b0/LICENSE)); contributor GitHub account `vrjdev`: [scalar PLR/IRM GATE input fix, PR #466](https://github.com/DoubleML/doubleml-for-py/pull/466), merged 2026-11-18 17:34:02 UTC, revision `6dd568a85df45cd668301891e1a1ed57c68554b0`. Checked 2026-11-18: all four final changed files, complete GATE functions and associated test files inspected. **UPDATE + LINK**, no ADD: original adaptation of encoding-invariance and schema verification to the existing methods audit. No upstream code, tests, fixtures, prose or extended structure copied or executed. The final patch uses NumPy dtype-kind checks, beyond the PR body's initial parentheses description. Tests compare bool/int64/int32/uint8 coefficients and standard errors and reject multi-column float/nullable Int64; these are inspected assertions, not local execution. The PR explicitly limits the bug to the unreleased scalar API; do not claim a released-package defect or a verified installed fix. Linked BSD terms remain applicable to upstream assets.
