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

### DML Sensitivity Benchmarks

For a reduced-control refit, record the estimator/API and source version, dropped controls, treatment-specific learners, sample, and splits. Verify that the controls actually change, the intended learners survive reconstruction, and the original coefficients/covariates remain unchanged. Compare a separately specified reference implementation under matched settings where feasible; return discrepancies and unverified conditions. DoubleML PR #441, merged 2026-11-03, reports a refit exception in the unreleased vector API, not a demonstrated error in estimates from the released legacy API. Do not infer release availability or silently upgrade a replication environment.

### Numerical Policy Rules

For structural counterfactuals using discounted LQ control, obtain the objective, transitions, solver convention, constraints, and code version. Check discounting, cross-term signs, and transposes against the original equations. With a time-invariant period loss, scaling transition/control matrices by `sqrt(beta)` does not also scale the period-loss cross term. Evaluate an independently assembled Riccati/Bellman residual and compare a small alternative solution where feasible, with stated tolerances and existence/stability conditions. Distinguish optimization with constraints from clipping an unconstrained rule afterward. Report evidence and limitations before interpreting policy or welfare results.

## Sources and Workflow Influences

- DoubleML team, maintainers Philipp Bach and Sven Klaassen, [PR #441](https://github.com/DoubleML/doubleml-for-py/pull/441) and [configuration/invariance test update](https://github.com/DoubleML/doubleml-for-py/commit/5d4da666a68c9cfce5430d0dd059c6ab60662a7f), merged/committed 2026-11-03; checked 2026-11-04. Influence: reduced-model configuration, baseline invariance, and reference comparisons. [BSD-3-Clause](https://github.com/DoubleML/doubleml-for-py/blob/1af040fd1c922a4c7d30d01b7c21f208d5e3377a/LICENSE); original summary/links only, no source, tests, fixtures, or documentation text copied. No upstream execution or release certification.
- Thomas J. Sargent and John Stachurski / QuantEcon, *Intermediate Quantitative Economics with Python*, [Phillips Curve Tradeoffs revision](https://github.com/QuantEcon/lecture-python.myst/commit/4d82fffbb1280f8f6980a45dbe518e677f5c9a39), 2026-11-03; checked 2026-11-04. Influence: discount/cross-term checks and policy-constraint interpretation. [Lecture footer](https://python.quantecon.org/phillips_learning.html): CC BY-SA 4.0, not an MIT relicense. Original high-level procedure and mathematical facts only; no lecture prose, derivations, code, figures, solutions, or extended structure copied. Full lecture execution not performed.
