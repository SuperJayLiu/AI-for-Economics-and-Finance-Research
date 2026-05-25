> Copyright (c) 2026 SuperJayLiu (Chaojie Liu). Licensed under the repository MIT License.

# Causal Inference, Econometrics, and Time-Series Skills

Use these skills to check methods before writing confident prose. They are designed for economists and finance researchers who need method-specific review, not generic AI explanation.

> [!WARNING]
> These skills do not certify identification. They help you identify assumptions, failure modes, diagnostics, and wording that must be checked by the researcher.

Questions or suggestions for this part: email [jay.liu@bristol.ac.uk](mailto:jay.liu@bristol.ac.uk) with subject `[AI Econ Finance Methods Skill] Suggestion`.

> [!NOTE]
> Import/use-as-skill protocol for any block on this page: `Start by collecting only the missing inputs needed for the task. Ask up to five clarifying questions when required inputs, data rules, method details, permissions, audience, or output format are unclear. For long outputs, file-producing tasks, slides, code, methods sections, literature reviews, referee responses, or agentic workflows, first return "Proposed structure and assumptions" and ask the user to confirm before producing the full output. Before finalizing, double-check for unsupported claims, invented citations or results, privacy risks, and mismatch with the requested format. End with "What I produced", "What I did not change", "What you must verify", and "Questions for you".`

## Choose a Skill

| Method/problem | Use |
| --- | --- |
| causal design overall | Skill 1 |
| OLS or cross-sectional regression | Skill 2 |
| panel fixed effects | Skill 3 |
| DiD or event study | Skill 4 |
| IV | Skill 5 |
| RD | Skill 6 |
| synthetic control | Skill 7 |
| time-series AR/MA/ARMA/VAR | Skill 8 |
| clustering and few-cluster inference | Skill 9 |

## Skill 1: Causal Design Diagnostic

```text
Diagnose this economics/finance causal design.

Project facts:
- Research question: [question]
- Treatment/exposure/shock: [treatment]
- Outcome: [outcome]
- Unit and time: [unit/time]
- Data: [data]
- Proposed design: [design]
- Comparison group: [comparison]
- Main concern: [concern]

Check:
1. What is the implied counterfactual?
2. What variation identifies the effect?
3. What assumptions are required?
4. What would violate those assumptions?
5. What diagnostics or falsification checks are relevant?
6. What claims are supported: descriptive, predictive, associational, or causal?
7. What language should be avoided?

Return:
- design summary
- assumptions table
- main threats
- minimum diagnostics
- safe interpretation paragraph
```

## Skill 2: OLS and Cross-Sectional Regression Check

```text
Audit this OLS or cross-sectional regression.

Specification:
[paste equation or table]

Context:
- Outcome: [outcome]
- Key regressor: [regressor]
- Controls: [controls]
- Sample: [sample]
- Intended interpretation: [interpretation]

Check:
- omitted variables
- reverse causality
- bad controls
- functional form
- measurement error
- sample selection
- heteroskedasticity and clustering
- units and economic magnitude

Return:
- what the coefficient means
- what it does not mean
- main threats
- robustness checks
- safer wording
```

## Skill 3: Panel Fixed Effects Check

```text
Audit this panel fixed-effects design.

Specification:
[paste]

Project facts:
- Unit: [unit]
- Time: [time]
- Outcome: [outcome]
- Treatment/regressor: [regressor]
- Fixed effects: [FE]
- Controls: [controls]
- Clustering: [cluster]

Check:
1. What variation remains after fixed effects?
2. Are controls post-treatment or bad controls?
3. Are fixed effects absorbing the treatment variation?
4. Is there serial correlation or within-cluster dependence?
5. Are staggered timing or heterogeneous effects relevant?
6. Does the text overclaim causality?
7. Is the clustering level tied to treatment assignment, sampling, or residual correlation rather than habit?

Return:
- identifying variation explanation
- risks
- code/table checks
- safer methods wording
```

## Skill 4: Difference-in-Differences and Event Study Check

```text
Audit this DiD/event-study design.

Project facts:
- Treatment: [treatment]
- Treated group: [treated]
- Control group: [control]
- Treatment timing: [timing]
- Outcome: [outcome]
- Unit/time: [unit/time]
- Specification/event window: [specification]

Check:
1. parallel trends or identifying assumption;
2. treatment timing and staggered adoption;
3. anticipation effects;
4. dynamic treatment effects;
5. composition changes;
6. event-time binning and omitted category;
7. clustering and inference;
8. graph labels and interpretation.
9. whether conventional TWFE is appropriate with staggered timing and heterogeneous effects;
10. whether the design should consider Callaway-Sant'Anna, Sun-Abraham, Borusyak-Jaravel-Spiess imputation, de Chaisemartin-D'Haultfoeuille, or a Goodman-Bacon decomposition;
11. whether pre-trend tests are underpowered and should be supplemented with sensitivity analysis.

Return:
- required diagnostics
- estimator-choice recommendation with assumptions
- event-study plot checklist
- threats to validity
- safer interpretation language

Rules:
- Do not say "parallel trends passed" only because pre-treatment coefficients are insignificant.
- Do not use a TWFE event-study coefficient as the target estimand without checking treatment timing and heterogeneity.
- If treatment timing is staggered, state what group-time comparisons identify the estimate.
```

## Skill 5: Instrumental Variables Check

```text
Audit this IV design.

Project facts:
- Endogenous variable: [variable]
- Instrument: [instrument]
- Outcome: [outcome]
- Unit/time: [unit/time]
- First stage: [summary]
- Exclusion restriction argument: [argument]

Check:
- relevance
- exclusion restriction
- monotonicity/LATE interpretation
- weak instruments
- direct effects
- instrument timing
- plausible defiers or heterogeneous effects
- whether an effective F-statistic, Kleibergen-Paap-style diagnostic, Anderson-Rubin/weak-IV robust confidence set, or other weak-instrument robust inference is needed

Return:
- strongest IV argument
- weakest assumption
- tests and diagnostics
- what the coefficient estimates
- cautious interpretation paragraph

Rules:
- Do not rely mechanically on "first-stage F > 10" when the design is clustered, heteroskedastic, or otherwise nonstandard.
- If instruments may be weak, ask for weak-IV robust inference before writing strong conclusions.
```

## Skill 6: Regression Discontinuity Check

```text
Audit this regression discontinuity design.

Project facts:
- Running variable: [running variable]
- Cutoff: [cutoff]
- Outcome: [outcome]
- Treatment rule: [rule]
- Bandwidth: [bandwidth]
- Unit/time: [unit/time]

Check:
- continuity assumption
- manipulation or sorting around cutoff
- bandwidth sensitivity
- polynomial/order choices
- covariate balance
- donut RD need
- local interpretation
- rdrobust-style robust bias-corrected inference, MSE-optimal bandwidth choices, and density/manipulation tests such as McCrary where relevant

Return:
- RD assumption summary
- diagnostic checklist
- graph/table checks
- safe wording for methods and results

Rules:
- Do not choose bandwidths after seeing the desired result.
- Do not treat global high-order polynomials as a substitute for local design credibility.
- Report local interpretation and manipulation checks clearly.
```

## Skill 7: Synthetic Control Check

```text
Audit this synthetic control design.

Project facts:
- Treated unit: [unit]
- Treatment date: [date]
- Donor pool: [pool]
- Outcomes: [outcomes]
- Predictors: [predictors]
- Pre-period: [period]
- Post-period: [period]

Check:
- donor pool credibility
- pre-treatment fit
- predictor choice
- spillovers
- placebo tests
- sensitivity to donor pool
- interpretation of post-treatment gap

Return:
- design strengths
- design weaknesses
- required figures/tables
- safe interpretation language
```

## Skill 8: Time-Series AR/MA/ARMA/VAR Check

```text
Audit this time-series model for economics/finance.

Project facts:
- Series: [series]
- Frequency: [daily/monthly/quarterly/etc.]
- Sample period: [period]
- Model: [AR/MA/ARMA/ARIMA/VAR/etc.]
- Purpose: [forecasting/description/policy/asset pricing/etc.]
- Transformations: [levels/logs/differences/returns]

Check:
1. stationarity and transformations;
2. lag selection;
3. autocorrelation and residual diagnostics;
4. structural breaks;
5. seasonality;
6. out-of-sample validation;
7. forecast evaluation;
8. whether causal language is inappropriate.

Return:
- model-purpose fit
- diagnostics to run
- interpretation limits
- safer results wording
```

## Skill 9: Clustering and Inference Check

```text
Audit the standard error and inference plan for this economics/finance design.

Project facts:
- Research question: [question]
- Unit of observation: [unit]
- Treatment/exposure level: [level]
- Sampling or assignment level: [level]
- Time dimension: [time]
- Main specification: [equation/table]
- Current standard errors: [robust/clustered/two-way/Newey-West/bootstrap/etc.]
- Number of clusters: [number]
- Cluster size balance: [balanced/unbalanced/unknown]

Check:
1. what dependence structure is plausible;
2. whether treatment varies at a cluster level;
3. whether clustering follows sampling, assignment, geography, firm, individual, time, or market structure;
4. whether two-way clustering is needed;
5. whether there are too few clusters for conventional cluster-robust inference;
6. whether wild-cluster bootstrap, randomization inference, or design-based inference is needed;
7. whether standard errors in the paper match the code and table notes.

Return:
- recommended inference approach;
- assumptions behind it;
- minimum table-note language;
- code/table checks;
- risks if the current inference is kept.

Rules:
- Do not choose clustering because it gives preferred significance.
- Do not cluster mechanically without explaining why.
- If clusters are few or highly unbalanced, require sensitivity checks.
```

Sources and workflow influences: applied econometrics teaching, credibility-revolution design language, modern DiD/event-study guidance, weak-IV inference, RD practice, clustering guidance, finance event-study cautions, and AI-assisted methods-review workflows.
