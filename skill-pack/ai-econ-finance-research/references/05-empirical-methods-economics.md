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

## DML Treatment Scale and Residual Verification

Use within the existing empirical-method/code audit when scalar PLR reports a near-zero score denominator, treatment units change, or fitted/external treatment predictions nearly reproduce the treatment. Request the exact API/revision, score, treatment units and origin, sample IDs, cross-fitting splits, learner settings, predictions and per-repetition score elements. Missing artifacts remain **UNVERIFIED**.

```text
1. Separate small physical units, cancellation of signed score derivatives, and negligible residual treatment variation. Preserve the original environment and outputs; do not fix an error by silently changing units, deleting observations or relaxing numerical tolerances.
2. For each repetition record the mean score derivative and mean absolute derivative. The inspected generic guard compares abs(mean(psi_a)) with 1e-12 times mean(abs(psi_a)); a small absolute mean alone need not imply a numerical failure. For the partialling-out PLR score's nonpositive squared-residual derivative, cancellation is absent: this generic guard cannot by itself detect nearly perfect treatment prediction.
3. Separately record mean((d - m_hat)^2) and mean(d^2), including fitted and external predictions and the initial-estimate paths used in fitting/tuning. The inspected PLR check stops at a ratio no greater than 1e-12 in any repetition; all-zero treatment also stops. This numerical rule depends on the treatment's origin through its uncentered second moment. Passing it is not proof of adequate identifying variation, overlap or reliable inference; do not interpret it as a universal weak-identification test.
4. With a continuous-treatment linear PLR specification and equivalent nuisance predictions, hold rows, folds and settings fixed and change d to c*d for a finite nonzero c. Check theta_new*c against theta_old and se_new*abs(c) against se_old, per repetition, using explicit tolerances. Use small and large positive c. Learner regularization or tuning can break prediction equivalence; diagnose that before attributing a discrepancy to score arithmetic. These checks do not automatically apply to binary-treatment recoding or other estimands.
5. Include zero residuals, near-exact treatment prediction and signed-derivative cancellation as separate failure cases. For IV-type PLR inspect the residual check before the initial coefficient as well as final post-fit checks; a final guard alone does not establish safety of earlier divisions. Keep nonfinite-input handling separate. Stop on unexplained failures and mark affected outputs for review.
6. Return a revision/API record, treatment-scale and residual ledger, fixed-split comparison, tolerances, observed exceptions, affected results and unresolved questions. Distinguish source-inspected tests, independently executed arithmetic and actual package execution. Rescaling agreement does not establish causal assumptions or valid confidence intervals.
```

### Sources and Workflow Influences for DML Treatment Scale

DoubleML official Python project, maintained by Philipp Bach and Sven Klaassen ([pinned README](https://github.com/DoubleML/doubleml-for-py/blob/50663c993d8056d3e75ca4c226fcdcdb555133c6/README.md)); contributor `vrjdev`, merged by Sven Klaassen: [scalar score scale checks, PR #467](https://github.com/DoubleML/doubleml-for-py/pull/467), merged 2026-11-24 15:30:18 UTC, revision `50663c993d8056d3e75ca4c226fcdcdb555133c6`. [BSD-3-Clause license](https://github.com/DoubleML/doubleml-for-py/blob/50663c993d8056d3e75ca4c226fcdcdb555133c6/LICENSE). Checked 2026-11-25: all five final patches, the full pinned linear-score estimator, scalar-PLR residual/score implementations and fit/tuning call sites, and added test cases. **UPDATE + LINK**: original adaptation of unit-rescaling, cancellation and treatment-residual verification. No upstream code, test fixtures, wording, figures, templates or extended structure copied; no upstream installation or tests executed. The PR explicitly concerns the unreleased scalar API, not a newly established bug in a released package. Source inspection and local score arithmetic do not certify package execution, identification or interval coverage.
