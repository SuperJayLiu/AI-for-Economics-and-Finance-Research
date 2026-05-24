> Copyright (c) 2026 SuperJayLiu (Chaojie Liu). Licensed under the repository MIT License.

# Empirical Methods Skills for Finance Research

These skills are tailored for asset pricing, corporate finance, banking, household finance, market microstructure, fintech, and accounting-adjacent finance work.

> [!IMPORTANT]
> Finance AI outputs are especially vulnerable to clean narratives around noisy patterns. Use these skills to document timing, benchmarks, sample construction, risk adjustment, and limits. Do not use them to manufacture a story after searching many specifications.

## Choose the Right Skill

| Need | Use |
| --- | --- |
| write a first finance methods draft | Skill 1 |
| audit a methods section | Skill 2 |
| guard against overclaiming results | Skill 3 |
| check asset-pricing/factor-mining risk | Skill 4 |
| check corporate/banking panel design | Skill 5 |
| check event-study design | Skill 6 |

## Skill 1: Draft Empirical Methods Section for Finance

```text
Draft an empirical methods section for a finance research paper.

Inputs:
- Field: [asset pricing/corporate finance/banking/household finance/etc.]
- Research question: [question]
- Data sources: [CRSP/Compustat/WRDS/TRACE/Dealscan/13F/EDGAR/proprietary/etc.]
- Unit of observation: [firm-month/stock-day/loan-quarter/fund-month/etc.]
- Sample period and filters: [period, exchanges, industries, screens]
- Key variables: [outcomes, predictors, treatment, controls]
- Empirical design: [panel regression/event study/portfolio sorts/Fama-MacBeth/DiD/IV/RD/structural/etc.]
- Main equation or portfolio construction: [details]
- Return measurement, if relevant: [raw/excess/abnormal/risk-adjusted]
- Risk adjustment, if relevant: [CAPM/FF3/FF5/q-factor/characteristic controls/etc.]
- Inference: [cluster, Newey-West, double clustering, bootstrap]
- Finance-specific concerns: [look-ahead, survivorship, delisting returns, microstructure, transaction costs, multiple testing]

Write:
1. Data construction and sample screens.
2. Variable definitions.
3. Main empirical specification or portfolio procedure.
4. Identification or interpretation limits.
5. Risk adjustment or benchmark model.
6. Inference and standard error approach.
7. Robustness and economic magnitude.
8. Finance-specific caveats.
9. Replication details needed for another researcher to rebuild the sample.

Rules:
- Do not invent data filters or risk factors.
- Do not confuse predictability with causal effect.
- Do not ignore look-ahead, survivorship, delisting, liquidity, and transaction cost concerns.
- Distinguish statistical significance from economic magnitude.
- If the design is associational, say so.
- If information is missing, write [NEEDS AUTHOR INPUT] rather than filling it in.

Output format:
- Draft methods section.
- Missing replication details.
- Timing and data-leakage checklist.
- Claims that require softer wording.
```

## Skill 2: Check Empirical Methods Section for Finance

```text
Audit this finance empirical methods section.

Text:
[paste methods section]

Known project facts:
- Field: [field]
- Data: [data]
- Unit/time: [unit and frequency]
- Design: [design]
- Main variables: [variables]

Check:
1. Are sample screens and data sources clear enough to replicate?
2. Are CRSP/Compustat/WRDS-style merge assumptions stated?
3. Is the timing of variables clear enough to prevent look-ahead bias?
4. Are delisting returns, survivorship, microstructure, or liquidity issues relevant?
5. Are event windows and estimation windows defined?
6. Are portfolio sorts or Fama-MacBeth procedures fully specified?
7. Is risk adjustment appropriate for the claim?
8. Are standard errors appropriate for panel/time-series dependence?
9. Are multiple-testing or factor-mining risks acknowledged?
10. Does the text overstate causal interpretation or investment implications?

Return:
- Fatal problems.
- Important revisions.
- Replication details missing.
- Suggested rewrite.
- Code/table checks to run.
- Whether the design supports prediction, association, causal interpretation, or only descriptive evidence.
```

## Skill 3: Finance Result Interpretation Guardrail

```text
Review this results paragraph for finance overclaiming.

Paragraph:
[paste]

Design and data:
[describe]

Check for:
- correlation described as causality
- statistical significance without economic magnitude
- omitted risk adjustment caveats
- ignored transaction costs or limits to arbitrage
- investment advice language
- look-ahead or multiple-testing concerns
- claims beyond sample period or asset class

Return:
1. Sentences that overclaim.
2. Safer replacement sentences.
3. Missing caveats.
4. What must be verified in tables/code.
```

## Skill 4: Asset Pricing and Factor-Mining Risk Check

```text
Audit this asset-pricing or return-predictability design for factor-mining and backtest risk.

Project facts:
- Predictor/signal: [signal]
- Return horizon: [horizon]
- Sample period: [period]
- Universe: [stocks/bonds/funds/options/etc.]
- Portfolio construction or regression: [method]
- Benchmark/risk model: [CAPM/FF3/FF5/q-factor/characteristics/etc.]
- Transaction cost or liquidity treatment: [details]
- Number of signals/specifications tried: [if known]
- Out-of-sample or validation plan: [plan]

Check:
1. look-ahead bias
2. survivorship bias
3. delisting return treatment
4. microstructure and liquidity
5. multiple testing and p-hacking
6. benchmark/risk-model sensitivity
7. transaction costs and capacity
8. sample-period dependence
9. economic mechanism
10. investment-advice overclaiming

Return:
- red flags
- minimum robustness checks
- safer interpretation language
- replication details missing
- what evidence would make the signal more credible
```

## Skill 5: Corporate Finance or Banking Panel Design Check

```text
Audit this corporate finance, banking, household finance, or accounting-style panel design.

Project facts:
- Research question: [question]
- Unit of observation: [firm-year/bank-quarter/loan-month/etc.]
- Data sources: [Compustat/CRSP/Dealscan/Call Reports/13F/EDGAR/proprietary/etc.]
- Treatment/exposure: [treatment]
- Outcome: [outcome]
- Controls and fixed effects: [controls/FE]
- Timing: [when variables are measured]
- Inference: [clustering]

Check:
1. whether treatment timing precedes outcomes;
2. whether controls are bad controls or post-treatment variables;
3. whether fixed effects absorb the intended variation;
4. whether standard errors match the dependence structure;
5. whether sample selection or missing data could drive results;
6. whether merges create survivorship or selection bias;
7. whether the text overstates causality;
8. whether economic magnitude is reported clearly.

Return:
- fatal issues
- important fixes
- suggested methods rewrite
- table/code checks to run
- cautious interpretation paragraph
```

## Skill 6: Finance Event Study Design Check

Use before trusting an event-study graph or writing event-study methods.

```text
Audit this finance event-study design.

Project facts:
- Event: [event]
- Event date definition: [date rule]
- Unit: [firm/security/fund/bank/etc.]
- Return or outcome: [outcome]
- Event window: [window]
- Estimation window: [window]
- Benchmark model: [market/CAPM/FF/q-factor/matched firms/etc.]
- Sample filters: [filters]
- Clustering/inference: [method]
- Overlapping events: [yes/no/unknown]
- Long-horizon or volatile-period design: [yes/no]

Check:
1. whether the event date is clearly defined and not chosen using outcomes;
2. whether events overlap or cluster in calendar time;
3. whether the benchmark model matches the claim;
4. whether estimation and event windows are appropriate;
5. whether long-horizon interpretation is credible;
6. whether confounding events are addressed;
7. whether abnormal returns are interpreted as causal effects too strongly;
8. whether graph labels, cumulative windows, and standard errors are clear.

Return:
- design summary
- event-date risks
- benchmark/model risks
- inference risks
- safer methods paragraph
- table/figure checks to run
```

Sources and workflow influences: Paul Goldsmith-Pinkham's AI-era research caution about p-hacking and replication, his work on credibility and financial event-study interpretation, plus finance-specific concerns around factor mining, backtest overfitting, and empirical transparency.
