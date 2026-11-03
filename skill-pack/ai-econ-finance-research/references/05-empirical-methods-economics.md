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

For RD software changes, preserve the original environment and record package version/options. The official `rdrobust` 2026-10-01 entry identifies result-affecting fixes, including sharp covariate-adjusted derivative estimates with order at least two. Establish whether the specification is affected and compare fixed versus selected bandwidth results before interpreting a change. Do not silently upgrade a replication environment.

## Sources and Workflow Influences

Sebastian Calonico, Matias D. Cattaneo, Max H. Farrell, Rocio Titiunik / rdpackages, [rdrobust changelog](https://github.com/rdpackages/rdrobust/blob/main/CHANGELOG.md) and [R metadata](https://raw.githubusercontent.com/rdpackages/rdrobust/main/R/rdrobust/DESCRIPTION), 2026-10-01; checked 2026-11-03. Influence: specification-specific version checks. GPL-3 is declared; no implementation, tests, or documentation text copied, only an original summary and links. Package-channel availability was not independently checked.
