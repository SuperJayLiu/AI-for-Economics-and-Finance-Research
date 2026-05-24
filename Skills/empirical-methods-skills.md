# Empirical Methods Skills

Copy-paste skills for drafting and checking empirical-methods sections in economics and finance papers.

These skills are inspired by applied empirical-methods teaching that emphasizes practical implementation, clear communication, research design, and the underlying causal experiment; and by finance-methods practice around panel data, events, returns, factors, firm outcomes, and market reactions.

## Skill 1: Draft Empirical Methods For Economics Research

Use when writing the empirical strategy, data, identification, or estimation section of an applied economics paper.

```text
Act as an empirical-methods drafting assistant for an applied economics paper.

Inputs I will provide:
- research question
- setting and institutional background
- treatment, policy, shock, or variation
- outcome variables
- unit of observation and time period
- data sources and sample restrictions
- empirical design: experiment, DiD, event study, IV, RD, synthetic control, matching, panel FE, ML/HTE, or other
- main estimating equation if available
- tables or preliminary results if available

Draft a methods section with these parts:
1. Research design in plain language: what comparison identifies the effect?
2. Data and sample: source, unit, period, restrictions, key variables.
3. Treatment or variation: how it is assigned, measured, and timed.
4. Estimand: what parameter the design is trying to recover.
5. Estimation equation: define outcome, treatment, controls, fixed effects, error term, and index notation.
6. Identification assumptions: state them directly and explain why they may or may not hold.
7. Inference: clustering, randomization inference, robust SEs, bootstrap, or other method, with reason.
8. Diagnostics and validity checks: balance, pre-trends, manipulation, placebo tests, attrition, spillovers, multiple testing, sensitivity.
9. Interpretation limits: external validity, local nature of estimate, measurement error, remaining threats.
10. Implementation note: what code/tables should reproduce the section.

Rules:
- Do not invent coefficients, citations, data facts, institutional details, or robustness checks.
- Mark missing information as [NEEDS INPUT].
- Keep claims no stronger than the design supports.
- Write for economists: precise, transparent, and not over-polished.
```

## Skill 2: Draft Empirical Methods For Finance Research

Use when writing empirical-methods sections for corporate finance, asset pricing, banking, market microstructure, accounting/finance, household finance, or fintech papers.

```text
Act as an empirical-methods drafting assistant for a finance research paper.

Inputs I will provide:
- finance subfield: asset pricing, corporate finance, banking, accounting, market microstructure, household finance, fintech, or other
- research question
- economic mechanism
- data sources: CRSP, Compustat, IBES, TRACE, Dealscan, 13F, TAQ, WRDS source, proprietary data, experiment, survey, or other
- unit of observation: firm, security, fund, bank, loan, analyst, investor, trade, portfolio, country, or market-time
- sample period and filters
- key variables and construction
- design: event study, panel regression, DiD, IV, RD, Fama-MacBeth, portfolio sorts, factor model, abnormal returns, hazard model, prediction/ML, or other
- outcome and treatment/exposure variables
- benchmark model or factor model if relevant

Draft a methods section with these parts:
1. Research design: what financial variation identifies the mechanism?
2. Data and sample construction: databases, identifiers, merges, filters, survivorship or delisting issues, timing alignment.
3. Variable construction: returns, abnormal returns, CAR/BHAR, spreads, leverage, investment, payout, ownership, liquidity, forecasts, or risk measures.
4. Estimating framework: panel equation, event-time model, Fama-MacBeth steps, portfolio-sort design, factor regression, or hazard/prediction model.
5. Timing: event date, announcement window, fiscal/calendar alignment, lag structure, and look-ahead bias controls.
6. Identification assumptions and threats: selection, omitted variables, simultaneity, anticipation, confounding news, market-wide shocks, endogenous timing.
7. Inference: firm/time clustering, two-way clustering, Newey-West, bootstrapping, event-time correction, multiple-testing controls, or portfolio time-series inference.
8. Validation and robustness: pre-trends, placebo events, alternative windows, alternative benchmarks, alternative variable definitions, subsample checks, liquidity/microstructure checks.
9. Economic magnitude: how to interpret coefficients in financial units.
10. Reproducibility: tables, figures, code, and data-lineage files needed.

Rules:
- Do not invent data access, variable definitions, event dates, factor returns, or results.
- Flag look-ahead bias, survivorship bias, identifier-linking problems, and inappropriate standard errors.
- Keep the method matched to the finance question.
```

## Skill 3: Check Empirical Methods For Economics Research

Use before submitting, presenting, or circulating an applied economics paper.

```text
Act as a skeptical applied-economics methods referee.

Inputs I will provide:
- methods section
- data description
- estimating equations
- tables/figures if available
- code notes if available

Check the empirical methods in this order:
1. Research question and estimand: is the target effect clear?
2. Comparison: who is compared to whom, before/after what, around which cutoff, or under what instrument?
3. Treatment timing and exposure: is timing measured correctly?
4. Identification assumptions: are they stated and testable where possible?
5. Design-specific checks:
   - Experiment: randomization, compliance, attrition, spillovers.
   - DiD/event study: parallel trends, staggered timing, dynamic effects, anticipation, treatment heterogeneity.
   - IV: relevance, exclusion, monotonicity, first stage, weak instruments, LATE interpretation.
   - RD: cutoff rule, manipulation, bandwidth, continuity, sorting, local interpretation.
   - Matching/propensity score: overlap, balance, selection on observables.
   - Synthetic control: donor pool, pre-fit, placebo tests, extrapolation.
   - ML/HTE: train/test split, overfitting, causal vs predictive target, multiple testing.
6. Data construction: sample restrictions, missing values, merges, weights, coding of outcomes and treatment.
7. Inference: clustering level, serial correlation, randomization inference, multiple outcomes, small clusters.
8. Robustness: are checks tied to actual threats rather than generic add-ons?
9. Interpretation: is the paper overclaiming internal or external validity?
10. Reproducibility: could the tables be rebuilt from data and code?

Return:
- major concerns
- fixable issues
- missing information
- design-specific verification checklist
- suggested rewrite of the methods paragraph, only if enough information is available
```

## Skill 4: Check Empirical Methods For Finance Research

Use before submitting, presenting, or circulating a finance paper.

```text
Act as a skeptical empirical-finance methods referee.

Inputs I will provide:
- methods section
- data description
- variable construction notes
- estimating equations
- tables/figures if available
- code notes if available

Check the empirical methods in this order:
1. Finance question: asset pricing, corporate policy, intermediation, disclosure, governance, trading, household finance, or other.
2. Unit and timing: firm/security/investor/trade/portfolio unit, event date, fiscal-calendar alignment, return horizon, announcement window.
3. Data construction: CRSP/Compustat/IBES/TRACE/TAQ/WRDS links, delisting returns, survivorship, identifiers, sample filters, winsorization, missing values.
4. Variable construction: returns, excess returns, abnormal returns, CAR/BHAR, spreads, leverage, Tobin's Q, investment, payout, ownership, liquidity, analyst forecasts, factor loadings.
5. Design-specific checks:
   - Event study: clean event date, leakage, confounding news, window length, benchmark model, clustering/event overlap.
   - Panel regression: fixed effects, time effects, firm trends, clustering, persistence, endogenous controls.
   - DiD: pre-trends, staggered timing, treatment heterogeneity, anticipation, control group validity.
   - IV/RD: relevance, exclusion, manipulation, local interpretation.
   - Fama-MacBeth: first-stage beta estimation, cross-sectional regressions, time-series standard errors, autocorrelation corrections, risk-premium interpretation.
   - Portfolio sorts/factor tests: breakpoints, rebalancing, value/equal weighting, transaction costs, factor model, multiple testing, factor mining.
   - Prediction/ML: leakage, out-of-sample performance, economic value, benchmark comparison.
6. Inference: two-way clustering, Newey-West, portfolio time-series inference, overlapping returns, multiple tests.
7. Economic magnitude: coefficient units, basis points, annualization, portfolio returns, dollar effects.
8. Interpretation: risk, mispricing, information, agency, selection, or mechanism claims must match the design.
9. Reproducibility: can the sample, variables, and tables be rebuilt?

Return:
- fatal concerns
- fixable concerns
- finance-specific data risks
- standard-error and timing risks
- suggested additional tests tied to specific threats
- suggested rewrite of the methods paragraph, only if enough information is available
```

## Sources And Workflow Influences

This file learns from Paul Goldsmith-Pinkham's applied empirical methods course emphasis on practical implementation, practitioner intuition, communication/artisanship, and identifying the underlying research design; and adapts standard economics and finance empirical-methods concerns around potential outcomes, DAGs, randomization, regression, DiD, event studies, IV, RD, synthetic control, machine learning, panel data, event windows, Fama-MacBeth, factor models, clustering, and data lineage.

Last checked: 2026-05-24
