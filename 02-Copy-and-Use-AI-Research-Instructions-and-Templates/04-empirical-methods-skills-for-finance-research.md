> Copyright (c) 2026 SuperJayLiu (Chaojie Liu). Licensed under the repository MIT License.

# Empirical Methods Skills for Finance Research

These skills are tailored for asset pricing, corporate finance, banking, household finance, market microstructure, fintech, and accounting-adjacent finance work.

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

Rules:
- Do not invent data filters or risk factors.
- Do not confuse predictability with causal effect.
- Do not ignore look-ahead, survivorship, delisting, liquidity, and transaction cost concerns.
- Distinguish statistical significance from economic magnitude.
- If the design is associational, say so.
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

Sources and workflow influences: Paul Goldsmith-Pinkham's AI-era research caution about p-hacking and replication, plus finance-specific concerns around factor mining, backtest overfitting, and empirical transparency.

