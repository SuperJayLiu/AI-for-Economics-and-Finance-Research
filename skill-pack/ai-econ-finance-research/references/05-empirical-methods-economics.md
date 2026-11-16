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

## Weighted IV Diagnostic Reconciliation

Use within the existing methods/code audit when weighted IV output includes second-stage R-squared or a Sargan overidentification test. This extends the existing IV and table verification contract.

Required inputs: exact installed revision, formula and stage, estimation rows in order, outcome, controls/instruments, fixed-effect treatment, weights and their interpretation, relevant residual definitions, diagnostic type and reported outputs. Missing inputs remain **UNVERIFIED**.

```text
1. Preserve the replication environment and identify the exact statistic. Distinguish structural IV residuals used for a reported fit measure from residuals in the overidentification auxiliary regression. Trace weights and row removals through every calculation; align rows before comparing diagnostics.
2. For second-stage IV R-squared, verify the package's residual definition and use the same weights in residual and centered-outcome sums of squares. For Sargan, independently reconstruct the specified weighted auxiliary regression using the intended instruments and included exogenous controls; check that its residual and centered structural-residual sums of squares use the same weights and weighted centering. Record the auxiliary sample size and degrees of freedom. Do not treat these two R-squared calculations as interchangeable.
3. Where execution is authorized, reconcile package output with a small transparent independent calculation on the identical sample/specification. Use common positive weight rescaling and constant-weight versus unweighted fits as diagnostic consistency controls for these calculations. A changed definition of weights or sample size may change the estimand/reference distribution; these controls do not validate survey or frequency-weight inference generally.
4. The audited fixest changes affect diagnostic weight handling: #703 weights the IV residual sum of squares; #708 weights the Sargan total sum of squares. Do not infer coefficient changes or a complete affected-release range from these patches. Do not silently replace an old replication result; isolate revision, sample and specification effects, then reconcile diagnostic tables and prose.
5. Do not reject a structural IV R-squared merely because it is negative, or interpret fit as identification. Sargan requires its own error and weight assumptions; it is not automatically a heteroskedasticity- or cluster-robust Hansen test because coefficient standard errors are robust. A non-rejection does not establish exclusion or instrument validity. If the appropriate diagnostic/reference distribution is unresolved, stop that inferential claim.

Return a diagnostic ledger: revision, statistic/stage, residual definitions, rows/weights, centering, auxiliary specification and degrees of freedom, inspected versus executed evidence, controlled comparisons, affected table cells, assumptions and unresolved action.
```

### Sources and Workflow Influences for Weighted IV Diagnostics

fixest project; maintainer Laurent Berge, verified in [pinned DESCRIPTION](https://github.com/lrberge/fixest/blob/76adcc876acda767bc749303c6c4e5758778add9/DESCRIPTION); contributor GitHub account `soodoku`: [PR #703, weighted second-stage IV R-squared](https://github.com/lrberge/fixest/pull/703), merged 2026-11-16 17:09:34 UTC at `8b9fd7af9951b330f0144a332695bceeeab6be57`; [PR #708, weighted Sargan total sum of squares](https://github.com/lrberge/fixest/pull/708), merged 17:54:42 UTC at `271b7e8b8a166f3e879d7cdf837fd87736a3a1fb`. Checked 2026-11-16 against both final two-file patches, including tests; DESCRIPTION declares GPL-3. **UPDATE + LINK**, no ADD: original diagnostic-reconciliation procedure only; no upstream code, tests, data, prose or extended structure copied or executed. These are merged-source checks, not a claim that a particular installed/CRAN release includes them or that overidentification tests prove instrument validity.
