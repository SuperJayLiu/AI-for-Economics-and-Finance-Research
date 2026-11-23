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

## IV Prediction Verification

Use in the existing empirical-method/code audit when a fixest second-stage IV result feeds predictions, scenario calculations or prediction uncertainty. Request version/source revision, formula and stage, retained coefficient names, newdata with row IDs, endogenous/exogenous variables, fixed effects, offsets, and covariance/small-sample settings. Missing evidence remains **UNVERIFIED**.

```text
1. State the target: a structural linear predictor using observed or explicitly supplied endogenous values, a first-stage projection, or a forecast. These are different quantities. A numerical structural predictor is not automatically a conditional expectation, policy effect or feasible forecast when future endogenous inputs are unavailable.
2. Build a retained-column ledger matching design columns, coefficients and both covariance axes by identity and order. Rename only the fitted endogenous coefficient entries when mapping to original variables; an exogenous variable legitimately called fit_income must keep its name. Stop on missing, duplicate or unmatched retained columns rather than silently dropping them. Document intentional collinearity exclusions.
3. Include the endogenous contribution even with an intercept-only exogenous formula or no exogenous regressors. For a small, supported no-fixed-effect linear case, compare explicit newdata predictions with a manual structural design-times-coefficient calculation. Include a legitimate fit_ exogenous name, multiple endogenous variables if used, and missing required inputs. Keep sample IDs, exclusions and missingness aligned.
4. Treat predict(object), predict(object, newdata=...) and requests for se.fit/interval as distinct paths. At the inspected revision the ordinary no-newdata call can return stored fitted values early; inspecting the newdata repair does not establish equivalence. Compare the actual paths used, document their target, and investigate unexplained differences before updating tables or archived results.
5. For supported prediction standard errors, independently check the diagonal of X V X' after the SAME name/order mapping, with the requested vcov and small-sample settings. Distinguish uncertainty of the fitted linear combination from a prediction interval for a future outcome. Source-level covariance-name repair alone establishes neither IV coverage nor valid forecast-error assumptions. Fixed-effect and nonlinear-in-parameter prediction-SE requests remain unsupported in the inspected function; do not fabricate intervals.
6. Return a revision/specification record, prediction-target statement, row/column/covariance ledger, numerical discrepancies and tolerances, warnings, affected outputs and unresolved items. Preserve archived values before deliberate environment changes. Separate inspected upstream behavior from locally executed checks; halt interpretation on missing mappings or unexplained discrepancies. Prediction agreement does not validate instrument exclusion, exogeneity or causal interpretation.
```

### Sources and Workflow Influences for IV Prediction

Laurent Berge / official fixest project; contributor Kyle Butts (both identified in the [pinned DESCRIPTION](https://github.com/lrberge/fixest/blob/6371909a0249b19373f5923af44ce75792346e36/DESCRIPTION)): [fix predict() for IV models, PR #714](https://github.com/lrberge/fixest/pull/714), merged 2026-11-22 16:19:10 UTC at `6371909a0249b19373f5923af44ce75792346e36`. GPL-3 applies to upstream assets. Checked 2026-11-23: the complete single-file final patch, full pinned `predict.fixest` function and [prediction documentation](https://github.com/lrberge/fixest/blob/6371909a0249b19373f5923af44ce75792346e36/man/predict.fixest.Rd). **UPDATE + LINK**: original adaptation of input, coefficient-name and covariance-alignment verification. No upstream code, tests, wording, figures, templates or extended structure copied or executed. This PR adds no tests; inspection is not numerical certification or evidence of availability in an installed release. Existing no-newdata fast paths and restrictions on prediction uncertainty still require separate checks.
