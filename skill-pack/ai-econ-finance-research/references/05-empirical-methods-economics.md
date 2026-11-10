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

## RDFlex Final-Bandwidth Reporting Audit

Use with the existing methods/code audit when a regression-discontinuity table, sample description, or replication log relies on DoubleML RDFlex bandwidths. This supplements the RD design checks; it does not establish identification or choose a bandwidth for the author.

Required inputs: exact DoubleML and rdrobust versions/source revisions, iteration and repetition counts, sample/fold identities, supplied bandwidth arguments, selection options, warnings, and the final estimation outputs for each repetition. Missing inputs remain **UNVERIFIED**.

```text
1. Separate the initial nuisance-stage bandwidth, any iterative updates, and the bandwidth actually used in the final rdrobust estimation. Check both automatic selection and explicit user bandwidths; a missing reported value after one iteration does not prove that estimation used no bandwidth.
2. Reconcile RDFlex.h with each repetition's final estimation record. In the inspected implementation h is a per-repetition maximum of the left/right final estimation bandwidths. Retain both sides separately, and distinguish estimation bandwidth h from bias bandwidth b. Do not infer symmetry, both-side sample counts, or a common window from a finite maximum.
3. Where execution is authorized, compare one-iteration and multi-iteration runs to their own final estimation records under documented samples, folds, learners, options, and numerical tolerances. Include an asymmetric user-bandwidth case. This is a reporting-consistency check; it does not require equal bandwidths or coefficients across different iteration settings.
4. Inspect the installed implementation before claiming a fix is available. Separate metadata-only changes from coefficient, standard-error, confidence-interval, and sample changes. The inspected patch repairs bandwidth storage/documentation while leaving extraction of coefficients and uncertainty unchanged; it does not establish that earlier estimates were numerically wrong. If final records are absent or inconsistent, stop publication of the bandwidth claim until reconstructed or rerun.

Return a reconciliation table: repetition, fit/sample identity, iteration count, supplied/selected bandwidth, final left/right h and b, reported h, tolerance, status, and required action. State which quantities were inspected versus rerun and which installed version was verified.
```

### Sources and Workflow Influences for the Bandwidth Audit

DoubleML team; maintainers Philipp Bach and Sven Klaassen; contributor `vrjdev`, **“fix: report the final bandwidth in RDFlex.h for n_iterations=1”**, [PR #456](https://github.com/DoubleML/doubleml-for-py/pull/456), merged 2026-11-10 07:56:43 UTC, revision `a8ef43d39abb386c12c8d687f85288f36f467db7`. [Pinned BSD-3-Clause license](https://github.com/DoubleML/doubleml-for-py/blob/a8ef43d39abb386c12c8d687f85288f36f467db7/LICENSE); maintainer identities verified in the pinned project README. Checked 2026-11-10. Original adaptation: reconcile reported and realized final RD bandwidths by repetition, retain asymmetric bandwidths, and distinguish metadata repair from estimator changes. No upstream code, tests, fixtures, prose, or document structure copied, installed, or executed. The merged source does not establish installed-release availability or certify applied estimates.
