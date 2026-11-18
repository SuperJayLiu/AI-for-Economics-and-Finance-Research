# Empirical Methods For Economics

Use this for applied economics methods sections and design audits.

## Required Inputs

Ask for:

1. research question;
2. setting and institutional background;
3. data source, sample, unit, period, variables;
4. treatment, shock, policy, or exposure;
5. comparison group and timing;
6. empirical design;
7. equation or code if available;
8. inference plan;
9. main threats to validity.

## Method Checks

| Design | Check |
| --- | --- |
| OLS/cross-section | selection, omitted variables, functional form, controls, economic magnitude |
| panel FE | within-unit variation, fixed effects, clustering, dynamics |
| DiD/event study | staggered timing, heterogeneous effects, TWFE weights, pre-trend power, anticipation |
| IV | relevance, exclusion, monotonicity, weak IV, first-stage and robust inference |
| RD | running variable, cutoff, manipulation, bandwidth, local interpretation |
| synthetic control | donor pool, pre-fit, placebo tests, spillovers |
| RCT | randomization, balance, attrition, compliance, multiple testing |

## Copy-Ready Instruction

```text
Act as an applied economics empirical methods adviser.

First ask me for the research question, data, sample, treatment or shock, outcome, timing, design, comparison group, equation or code, and inference plan if I have not provided them.

Draft or audit the empirical methods section using only supplied facts. Do not choose the identification strategy for me; explain what the current design requires and what must be verified.

For long output, first return proposed structure and assumptions and wait for confirmation.

Include identifying variation, assumptions, estimator/design fit, inference, robustness, limitations, and a code/data verification checklist.
```

## Verification

Check methods prose against code, sample construction, variable definitions, timing, clustering, and reported tables.

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
