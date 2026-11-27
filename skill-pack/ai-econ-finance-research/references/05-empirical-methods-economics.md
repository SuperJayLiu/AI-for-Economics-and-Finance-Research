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

## Multiway Cluster Split and Refit Audit

Use within the existing methods/code review when a clustered DML analysis draws or supplies cross-fitting partitions and later refits or changes repetitions. Require the installed revision/API, cluster dimensions and IDs, requested fold count per dimension, total fold count, repetition count, observation and cluster partitions, and split-dependent nuisance artifacts. Missing records remain **UNVERIFIED**.

1. Record the meaning of each count before fitting. In the audited scalar API, k folds per cluster variable across d dimensions produce k**d cross-fitting folds per repetition. For two dimensions and k=2, the total is 4, not a request for 4 folds in each dimension. Check actual partitions as well as counts; a count alone cannot establish cluster separation or prevent leakage.
2. Snapshot supplied or drawn partitions before refitting. With unchanged k and repetitions, require unchanged observation/cluster memberships and no unexpected redraw warning. Include the set-sample-splitting path when partitions are supplied externally; a fixed seed alone is insufficient evidence of partition preservation.
3. Change one setting at a time. Increasing repetitions while retaining k=2 must retain 4 folds per repetition in the two-way example; changing k to 3 must produce 9. An intentional redraw discards fit state. Rebuild or revalidate nuisance predictions, tuning artifacts and all split-dependent inputs against the new memberships and repetition dimension; compatible array shapes alone do not establish correct provenance.
4. Stop comparisons that silently change split semantics. Do not reinterpret a total fold count as the per-dimension input or suppress warnings to make estimates agree. Separate deliberately redrawn repetitions from estimates computed with fixed partitions. Confirm behavior in the exact installed revision before applying a workaround; source review is not package execution.

Return a split/refit ledger: revision, dimensions, per-dimension and total counts, repetitions, before/after membership evidence, warnings/state changes, dependent-artifact disposition, affected estimates/tables and unresolved checks. Controls should include unchanged settings, repetition-only change, fold-only change and externally supplied partitions. One-way and nonclustered cases are comparison controls; this upstream fix does not change their fold-count semantics. None of these checks validates the empirical dependence assumptions or inference coverage.

### Sources and Workflow Influences for Cluster Split Semantics

DoubleML official Python project, maintained by Philipp Bach and Sven Klaassen ([pinned README](https://github.com/DoubleML/doubleml-for-py/blob/baf9b87260e46f3d078dd187812ef797439d40ad/README.md)); contributor `vrjdev`, merged by Sven Klaassen: [PR #468, multi-way cluster fold comparison in scalar fit](https://github.com/DoubleML/doubleml-for-py/pull/468), merged 2026-11-27 13:01:44 UTC at `baf9b87260e46f3d078dd187812ef797439d40ad`. [Pinned BSD-3-Clause license](https://github.com/DoubleML/doubleml-for-py/blob/baf9b87260e46f3d078dd187812ef797439d40ad/LICENSE). Checked 2026-11-27: both final patches, scalar fit/draw/set splitting paths, reset hooks and four parametrized cluster test cases. **UPDATE + LINK**: original adaptation of split-preservation and refit acceptance checks. No upstream code, tests, fixtures, wording, figures, templates or extended structure copied; no upstream code installed or executed. This patch concerns the unreleased scalar API; it does not establish a released-package defect, valid cluster assignment, identification or confidence-interval coverage.
