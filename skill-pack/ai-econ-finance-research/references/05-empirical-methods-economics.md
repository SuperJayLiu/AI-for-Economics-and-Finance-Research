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

## IV Rank Diagnostic Verification

Use within the existing empirical-method/code audit when a fixest IV analysis reports a Kleibergen-Paap rank diagnostic, changes weights/covariance, or revisits archived first-stage results. Request the installed version and source revision, formula, analytic row IDs, excluded instruments, endogenous regressors, exogenous controls/fixed effects, weights, cluster IDs, covariance and small-sample settings. Missing evidence remains **UNVERIFIED**.

```text
1. Freeze the analytic sample and specification. Record k endogenous regressors and l retained excluded instruments after collinearity removal; check column identities, not only formula counts. The inspected routine presumes l >= k. Distinguish coefficient dimensions from first-stage score dimensions; a crash disappearing does not establish correct inference.
2. Trace weighting through residualization, fixed-effect removal, instrument projection, cross-products and covariance scores. Check first-stage residual degrees of freedom and cluster corrections against the SAME estimation sample and requested covariance. Do not add a second correction already applied inside the covariance routine or substitute second-stage regressor counts.
3. Record the exact statistic, normalization and reference distribution separately. At the audited revision the displayed kpr statistic is a rank Wald quadratic divided by l; its returned p-value uses the UNDIVIDED quadratic with chi-square degrees of freedom l-k+1. Reconstruct that mapping where supported and record tolerance and numerical provenance. Never pass the displayed divided statistic directly to that chi-square tail, or treat the returned p-value as a weak-instrument strength certificate.
4. Benchmark against a trusted implementation only after matching observations, instruments, endogenous variables, weights, covariance and finite-sample conventions. Cover the actually used case: IID, heteroskedastic or clustered; exactly or overidentified; one or multiple endogenous regressors. With one endogenous regressor, a matched first-stage joint Wald F is a useful check; do not generalize that equality to multiple endogenous regressors. Preserve archived outputs before a deliberate environment change.
5. Inspect covariance rank, warnings and missing diagnostics. The new projected-covariance solve has a warning/NA path, but earlier Cholesky/linear solves can still fail. Never turn missing diagnostics into zeros, successful identification, or evidence against weak instruments. Limited cluster support needs its own inference assessment.
6. Return revision and specification, sample/column/weight/covariance ledger, statistic-to-p-value mapping, matched benchmark differences, warnings, affected tables and unresolved issues. Separate upstream assertions, code inspection and local execution. Halt interpretation on unexplained discrepancies; choose design-appropriate weak-IV robust inference separately. Rank-test rejection does not establish exclusion restrictions, instrument exogeneity or economic importance.
```

### Sources and Workflow Influences for IV Rank Diagnostics

Laurent Berge / official fixest project; contributor GitHub account `Don-Yin`: [Fix clustered Kleibergen-Paap test when scores and coefficients differ in size, PR #709](https://github.com/lrberge/fixest/pull/709), merged 2026-11-20 02:18:09 UTC at `a4fa1af45b984a1a23f660c0200dff353e957a50`. Author/maintainer and GPL-3 verified in [pinned DESCRIPTION](https://github.com/lrberge/fixest/blob/a4fa1af45b984a1a23f660c0200dff353e957a50/DESCRIPTION). Checked 2026-11-20: all six final file patches, full `kp_stat`/`proj_on_U`, clustered covariance context and the relevant test block inspected. **UPDATE + LINK**: original workflow adaptation of diagnostic normalization, dimension, weight and covariance checks; no upstream code, test fixtures, prose, figures or extended structure copied or executed. GPL-3 governs upstream assets; linking does not relicense them. The API/final merge revision is authoritative here; cached web PR text still shows the earlier open state. Upstream tests contain selected robust/clustered statistic comparisons and a singularity case; comments reporting Stata verification are not our independent execution. Weighted/IID/p-value changes were inspected in code, not independently numerically certified. No installed-release availability or universal numerical validity claimed.
