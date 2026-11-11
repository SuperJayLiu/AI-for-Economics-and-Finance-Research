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

## RDFlex Learner-Weight and Running-Variable Audit

Use within the existing methods/code review when RDFlex uses a Pipeline or nested learner, or when constructing or changing DoubleMLRDDData. Ordinary RD design review still requires its own identification, cutoff, manipulation, and bandwidth evidence.

Required inputs: exact DoubleML/scikit-learn revisions, learner/wrapper tree, metadata-routing configuration at construction and fit, step-level fit/score weight requests, data schema, intended running variable, cutoff, covariate list, and sample/row identifiers. Missing evidence remains **UNVERIFIED**.

```text
1. Trace sample weights through the complete learner tree. A **kwargs fit signature alone does not prove delivery to a wrapped estimator. Inspect Pipeline, search/stacking/target-transform wrappers, and each intended recipient. Record explicit weight acceptance, forwarding, and declared requests; distinguish unsupported, unset, intentionally ignored, and consumed weights.
2. Check routing configuration both when assigning learners and immediately before fit. A Pipeline accepted inside an enabled configuration context can become invalid after that context ends. Enabling routing alone is insufficient when child requests are unset. Document intentionally unweighted preprocessing separately from a weighted final learner; do not silently route only to the final step as an equivalent repair.
3. Where execution is authorized, pilot the exact installed learner tree and configuration with a small representative sample and nonconstant weights. Seek evidence of intended delivery, not only finite output. Include disabled routing, unset requests, a nested unsupported learner, and configuration changed before fit as negative controls. Static acceptance is not proof that every wrapper implements the intended weighted procedure.
4. After data load, verify that score_col names an actual column, that the extracted score matches the intended running-variable values and row order, and that it is excluded from x_cols. Repeat existence, disjointness, and extracted-value checks after a setter change; preserve the design's cutoff/units. A successful object construction alone is insufficient evidence. After a failed mutation, re-establish a valid object and recheck all fields before fitting; do not assume rollback.
5. Preserve the original environment and compare matched samples, learners, weights, and options before attributing numerical changes to software. These patches strengthen validation and earlier failure reporting; they do not by themselves establish bias in previously completed estimates or select a new RD design.

Return a validation ledger: revision/configuration timing, learner path, weight intent/request/delivery evidence, schema/score/covariate checks, negative-control result, inspected versus executed status, and unresolved action. Stop fitting or reporting a weighted/RD claim if its required contract cannot be established.
```

### Sources and Workflow Influences for the Learner and Data Audit

DoubleML team; maintainers Philipp Bach and Sven Klaassen; contributor `vrjdev`: [sample-weight routing PR #457](https://github.com/DoubleML/doubleml-for-py/pull/457), merged 2026-11-11 06:17:06 UTC, `09cd5d51dd8f06a54a9896e1b36a5f16a6d874a0`; [RD score-column validation PR #458](https://github.com/DoubleML/doubleml-for-py/pull/458), merged 2026-11-11 06:17:31 UTC, `919c09c01fc4a131ac93ae51ec6d1135cdb2dffb`. Titles: “fix: reject a Pipeline in the sample weight check unless metadata routing is enabled” and “fix: validate score_col when constructing DoubleMLRDDData.” [Pinned BSD-3-Clause license](https://github.com/DoubleML/doubleml-for-py/blob/919c09c01fc4a131ac93ae51ec6d1135cdb2dffb/LICENSE); identities checked in the pinned README. Checked 2026-11-11. Original workflow adaptation: trace nested weight delivery and configuration timing; verify loaded RD column identity and disjointness. No upstream code, tests, fixtures, prose, or structure copied or executed. Final patches and tests, rather than initial PR descriptions, ground this guidance. Merged source does not establish installed-release availability, complete wrapper coverage, or valid applied estimates.
