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

## RD Row-Order and Bandwidth-Floor Verification

Use within the existing methods/code audit for R `rdrobust()` or `rdbwselect()` when bandwidth selection uses an explicit `bwcheck`, especially with `masspoints = "off"` and variance estimation other than nearest-neighbor. Required inputs: exact installed revision, complete options, cutoff, running variable, outcome, stable row IDs, sample exclusions, covariates, weights, clusters and fuzzy-treatment inputs where used. Missing evidence remains **UNVERIFIED**.

```text
1. Preserve the replication environment and original result. Record selected estimation/bias bandwidths, effective samples, coefficients, standard errors and intervals. A package version string alone may not identify the source revision containing a fix.
2. Hold the analytic sample, row identities and all options fixed. Apply the SAME permutation to every row-aligned input, then compare original, running-variable-sorted and several reproducibly shuffled orders within a justified numerical tolerance. Check both the bandwidth selector and the estimator; never shuffle x separately from y, covariates, weights, clusters or treatment status.
3. Trace the bandwidth floor to distances of distinct running-variable values from the cutoff on each side. Verify nearest-value ordering and the available distinct support when the requested count exceeds it. Duplicating rows does not create new support. A misplaced pilot floor can change a final selected bandwidth even when the final bandwidth exceeds that floor.
4. If selected-bandwidth fits differ, compare genuinely identical explicit estimation AND bias bandwidths to help separate selection from estimation; preserve all other inputs/options. This is a diagnostic decomposition, not proof of correctness. Record remaining differences and reconcile affected tables before interpreting them economically.
5. The audited R source correction explicitly sorts right-side distinct values before reading the floor. The upstream changelog identifies R 4.0.0–4.1.1 for this option path and labels the correction Unreleased. Confirm the actual installed code; do not generalize to all RD specifications, Python/Stata, or an available CRAN fix. Do not silently upgrade an archived replication environment or treat sorting as a substitute for a verified correction.
6. Stop interpretation of unexplained order-dependent results. Passing these checks verifies a computational contract; it does not establish RD continuity, absence of manipulation, adequate support, or valid causal inference. Separate inspected upstream tests from tests actually executed locally.

Return a ledger: revision/options, IDs and sample alignment, distinct support and floor checks, permutation/sorted comparisons and tolerances, fixed-bandwidth diagnostic, affected outputs, unresolved discrepancies and next action.
```

### Sources and Workflow Influences for RD Row Order

Sebastian Calonico, Matias D. Cattaneo, Max H. Farrell and Rocio Titiunik / rdpackages, maintainer Calonico verified in [pinned R DESCRIPTION](https://github.com/rdpackages/rdrobust/blob/ddf48c41871cb44913a45aa540c761d5c5472118/R/rdrobust/DESCRIPTION); contributor GitHub account `soodoku`: [rdrobust PR #28](https://github.com/rdpackages/rdrobust/pull/28), merged 2026-11-17 04:07:16 UTC, revision `ddf48c41871cb44913a45aa540c761d5c5472118`; [pinned changelog](https://github.com/rdpackages/rdrobust/blob/ddf48c41871cb44913a45aa540c761d5c5472118/CHANGELOG.md). Checked 2026-11-17: all four final changed files inspected, with surrounding selector/estimator code and complete invariance test file. DESCRIPTION declares GPL-3. **UPDATE + LINK**, no ADD: original workflow for paired input permutations, distinct-support floors, selection/estimation decomposition and interpretation stop rules. No upstream code, tests, datasets, prose or extended structure copied or executed. Upstream test assertions inspected, not independently reproduced; merged source is not certification of a released package. The repository MIT license does not relicense the linked source.
