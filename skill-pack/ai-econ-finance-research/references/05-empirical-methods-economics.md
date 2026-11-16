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

## Clustered DoubleML Framework Arithmetic Audit

Use within the existing methods/code audit when a reported sum or contrast is formed by adding or subtracting clustered DoubleMLFramework objects. This extends the existing clustering and table/code verification contract; it does not introduce a new estimator or skill.

Required inputs: installed revision, exact operation expression, component estimates/frameworks, sample and row identifiers, cluster IDs and dimensions, split/repetition records, and the intended joint covariance calculation. Missing evidence remains **UNVERIFIED**.

```text
1. Trace the reported quantity back to the framework operation. Component estimates with cluster-robust standard errors do not establish valid inference for their sum or difference. Preserve sample alignment, cluster structure, and cross-estimate dependence; do not combine standard errors as if estimates were independent without justification.
2. At the audited upstream revision, addition and subtraction of clustered frameworks explicitly fail with NotImplementedError. Earlier arithmetic could return standard errors computed without the cluster structure. Do not catch that exception and substitute unclustered inference, strip cluster metadata, or manually report the point contrast with the returned standard error.
3. Preserve the replication environment. Where execution is authorized, compare the exact installed behavior on a small representative one-way or two-way clustered design. Use scalar rescaling and sign reversal as limited consistency controls: a fixed scalar scales standard errors by its absolute value, while sign reversal preserves them. These controls do not validate framework addition/subtraction or the empirical design.
4. For the requested contrast, require a separately justified joint cluster-robust covariance procedure that accounts for dependence and the actual cluster design. If unavailable, stop the contrast's uncertainty/significance claim and record the unresolved method. Do not claim that this patch implements clustered contrast inference or invalidates every clustered DoubleML result.

Return an operation ledger: revision, expression, component/sample/cluster alignment, inspected versus executed behavior, covariance justification, affected outputs, controls, and unresolved action. Reconcile any corrected inference with tables and methods prose before acceptance.
```

### Sources and Workflow Influences for Clustered Arithmetic

DoubleML team; maintainers Philipp Bach and Sven Klaassen (pinned README); contributor `vrjdev`: [PR #460, “fix: raise NotImplementedError for adding or subtracting clustered DoubleMLFramework objects”](https://github.com/DoubleML/doubleml-for-py/pull/460), merged 2026-11-15 06:05:22 UTC at `6a92b231214dc977b76b9ca27e2a8e2d2a9860e1`. [Pinned BSD-3-Clause license](https://github.com/DoubleML/doubleml-for-py/blob/6a92b231214dc977b76b9ca27e2a8e2d2a9860e1/LICENSE). Checked 2026-11-16 against all three final changed files, including one-/two-way cluster tests. **UPDATE + LINK**: original workflow adaptation for operation-specific inference acceptance; no source code, tests, fixtures, prose, or extended structure copied or executed. Merged source is not evidence of installed-release availability or valid applied estimates.
