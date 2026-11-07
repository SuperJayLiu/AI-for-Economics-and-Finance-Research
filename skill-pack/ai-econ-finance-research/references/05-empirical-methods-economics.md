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

## DML Fit Artifacts and Sensitivity Fallback Audit

For repeated fits, nuisance diagnostics, CATE/GATE, or sensitivity bounds, request version/source revision, fit order, storage flags, samples/folds, warnings, and outputs. Map predictions, targets, learners, and diagnostics to their producing fit. Disabling storage on refit must invalidate old artifacts; check prediction/model flags independently. Where execution is authorized, compare the latest reused-object fit to a fresh fit with matched inputs and folds. Missing current predictions must stop dependent diagnostics or heterogeneity analysis, never invite substitution of earlier predictions.

For nonpositive-nu2 re-estimation warnings, examine the fallback separately: check observation-axis centering of influence contributions by repetition/treatment and the maximum-bias influence mean against a documented tolerance/reference. Distinguish coefficients, nu2 and maximum-bias point quantities from bound standard errors. Centering repairs do not restore orthogonality or identify a causal effect. Return an evidence table with producing fit/branch, observed check, tolerance/reference, status, affected result, and required action. Missing evidence remains UNVERIFIED; merged fixes do not establish installed-release availability.

### Sources and Workflow Influences

DoubleML team, maintainers Philipp Bach/Sven Klaassen; **“fix: drop predictions and models of a previous fit when fit() doesn't store them”**, [#452](https://github.com/DoubleML/doubleml-for-py/pull/452), merge `a3493c3b7a444b6ddd730ad05c2c0e6c67ac19c3` (2026-11-06 12:18:03 UTC); **“fix: center psi_nu2 in the nu2 re-estimation fallback”**, [#450](https://github.com/DoubleML/doubleml-for-py/pull/450), merge `aadcbcd1daeb90c14a865a5bec93a6358fe9a1c9` (12:17:47 UTC). [Pinned BSD-3-Clause](https://github.com/DoubleML/doubleml-for-py/blob/a3493c3b7a444b6ddd730ad05c2c0e6c67ac19c3/LICENSE). Checked 2026-11-07. Original adaptation of artifact-lifecycle and fallback-centering checks; no code/tests/fixtures/prose/structure copied or executed. Final diff, rather than earlier PR-body wording, establishes #452's clearer storage error. No release-range or applied-estimate certification.
