> Copyright (c) 2026 SuperJayLiu (Chaojie Liu). Licensed under the repository MIT License.

# Empirical Methods Skills for Finance Research

These skills are tailored for asset pricing, corporate finance, banking, household finance, market microstructure, fintech, and accounting-adjacent finance work.

> [!IMPORTANT]
> Finance AI outputs are especially vulnerable to clean narratives around noisy patterns. Use these skills to document timing, benchmarks, sample construction, risk adjustment, and limits. Do not use them to manufacture a story after searching many specifications.

> [!NOTE]
> Import/use-as-skill protocol for any block on this page: `Start by collecting only the missing inputs needed for the task. Ask up to five clarifying questions when required inputs, data rules, method details, permissions, audience, or output format are unclear. For long outputs, file-producing tasks, slides, code, methods sections, literature reviews, referee responses, or agentic workflows, first return "Proposed structure and assumptions" and ask the user to confirm before producing the full output. Before finalizing, double-check for unsupported claims, invented citations or results, privacy risks, and mismatch with the requested format. End with "What I produced", "What I did not change", "What you must verify", and "Questions for you".`

## Choose the Right Skill

| Need | Use |
| --- | --- |
| write a first finance methods draft | Skill 1 |
| audit a methods section | Skill 2 |
| guard against overclaiming results | Skill 3 |
| check asset-pricing/factor-mining risk | Skill 4 |
| check corporate/banking panel design | Skill 5 |
| check event-study design | Skill 6 |

For code, data construction, WRDS/CRSP/Compustat merges, portfolio sorts, and Fama-MacBeth implementation, pair this page with [Data Cleaning, Merging, Analysis, and Output Skills](14-data-cleaning-merging-analysis-and-output-skills.md).

## Filled Mini Example

```text
Research question:
Does a firm-level governance measure predict future stock returns?

Data:
CRSP monthly returns, Compustat annual fundamentals, governance data, 1995-2024.

Good AI output should:
- ask for CRSP/Compustat link rules and fiscal-year reporting lag;
- ask whether delisting returns are included;
- distinguish predictability from causality;
- require risk adjustment, transaction cost discussion, and multiple-testing caution;
- state how portfolios or Fama-MacBeth regressions are formed.

Bad AI output to reject:
"This proves that governance causes higher returns."
Reject because return predictability does not by itself establish a causal mechanism.
```

## Skill 1: Draft Empirical Methods Section for Finance

```text
Draft an empirical methods section for a finance research paper.

Inputs:
- Field: If I have not provided it, ask me to specify: asset pricing/corporate finance/banking/household finance/etc.
- Research question: If I have not provided it, ask me to specify: question
- Data sources: If I have not provided it, ask me to specify: CRSP/Compustat/WRDS/TRACE/Dealscan/13F/EDGAR/proprietary/etc.
- Unit of observation: If I have not provided it, ask me to specify: firm-month/stock-day/loan-quarter/fund-month/etc.
- Sample period and filters: If I have not provided it, ask me to specify: period, exchanges, industries, screens
- Key variables: If I have not provided it, ask me to specify: outcomes, predictors, treatment, controls
- Empirical design: If I have not provided it, ask me to specify: panel regression/event study/portfolio sorts/Fama-MacBeth/DiD/IV/RD/structural/etc.
- Main equation or portfolio construction: If I have not provided it, ask me to specify: details
- Return measurement, if relevant: If I have not provided it, ask me to specify: raw/excess/abnormal/risk-adjusted
- Risk adjustment, if relevant: If I have not provided it, ask me to specify: CAPM/FF3/FF5/q-factor/characteristic controls/etc.
- Inference: If I have not provided it, ask me to specify: cluster, Newey-West, double clustering, bootstrap
- Data merge and timing rules: If I have not provided it, ask me to specify: CRSP/Compustat/CCM link rules, reporting lag, return window, availability timing
- Finance-specific concerns: If I have not provided it, ask me to specify: look-ahead, survivorship, delisting returns, microstructure, transaction costs, multiple testing

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
10. Data lineage from raw source to final table/figure.

Rules:
- Do not invent data filters or risk factors.
- Do not confuse predictability with causal effect.
- Do not ignore look-ahead, survivorship, delisting, liquidity, and transaction cost concerns.
- Do not assume ticker/CUSIP merges or accounting timing are valid without documentation.
- Do not interpret a successful backtest as evidence of economic mechanism.
- Distinguish statistical significance from economic magnitude.
- If the design is associational, say so.
- If information is missing, write NEEDS AUTHOR INPUT rather than filling it in.

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
If I have not provided this, ask me to provide: paste methods section

Known project facts:
- Field: If I have not provided it, ask me to specify: field
- Data: If I have not provided it, ask me to specify: data
- Unit/time: If I have not provided it, ask me to specify: unit and frequency
- Design: If I have not provided it, ask me to specify: design
- Main variables: If I have not provided it, ask me to specify: variables

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
11. Does the methods section explain data lineage from raw sources to analysis-ready sample?
12. Would a replicator know exactly how to rebuild the sample and outputs?

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
If I have not provided this, ask me to provide: paste

Design and data:
If I have not provided this, ask me to provide: describe

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
- Predictor/signal: If I have not provided it, ask me to specify: signal
- Return horizon: If I have not provided it, ask me to specify: horizon
- Sample period: If I have not provided it, ask me to specify: period
- Universe: If I have not provided it, ask me to specify: stocks/bonds/funds/options/etc.
- Portfolio construction or regression: If I have not provided it, ask me to specify: method
- Benchmark/risk model: If I have not provided it, ask me to specify: CAPM/FF3/FF5/q-factor/characteristics/etc.
- Transaction cost or liquidity treatment: If I have not provided it, ask me to specify: details
- Number of signals/specifications tried: If I have not provided it, ask me to specify: if known
- Out-of-sample or validation plan: If I have not provided it, ask me to specify: plan

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
- Research question: If I have not provided it, ask me to specify: question
- Unit of observation: If I have not provided it, ask me to specify: firm-year/bank-quarter/loan-month/etc.
- Data sources: If I have not provided it, ask me to specify: Compustat/CRSP/Dealscan/Call Reports/13F/EDGAR/proprietary/etc.
- Treatment/exposure: If I have not provided it, ask me to specify: treatment
- Outcome: If I have not provided it, ask me to specify: outcome
- Controls and fixed effects: If I have not provided it, ask me to specify: controls/FE
- Timing: If I have not provided it, ask me to specify: when variables are measured
- Inference: If I have not provided it, ask me to specify: clustering
- Merge/link rules: If I have not provided it, ask me to specify: identifier rules, link-date rules, reporting lag

Check:
1. whether treatment timing precedes outcomes;
2. whether controls are bad controls or post-treatment variables;
3. whether fixed effects absorb the intended variation;
4. whether standard errors match the dependence structure;
5. whether sample selection or missing data could drive results;
6. whether merges create survivorship or selection bias;
7. whether the text overstates causality;
8. whether economic magnitude is reported clearly.
9. whether data linkage and timing assumptions are documented enough for replication.

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
- Event: If I have not provided it, ask me to specify: event
- Event date definition: If I have not provided it, ask me to specify: date rule
- Unit: If I have not provided it, ask me to specify: firm/security/fund/bank/etc.
- Return or outcome: If I have not provided it, ask me to specify: outcome
- Event window: If I have not provided it, ask me to specify: window
- Estimation window: If I have not provided it, ask me to specify: window
- Benchmark model: If I have not provided it, ask me to specify: market/CAPM/FF/q-factor/matched firms/etc.
- Sample filters: If I have not provided it, ask me to specify: filters
- Clustering/inference: If I have not provided it, ask me to specify: method
- Overlapping events: If I have not provided it, ask me to specify: yes/no/unknown
- Long-horizon or volatile-period design: If I have not provided it, ask me to specify: yes/no

Check:
1. whether the event date is clearly defined and not chosen using outcomes;
2. whether events overlap or cluster in calendar time;
3. whether the benchmark model matches the claim;
4. whether estimation and event windows are appropriate;
5. whether long-horizon interpretation is credible;
6. whether confounding events are addressed;
7. whether abnormal returns are interpreted as causal effects too strongly;
8. whether graph labels, cumulative windows, and standard errors are clear.
9. whether the design follows causal event-study logic rather than only abnormal-return convention;
10. whether long-horizon results are vulnerable to confounding, model misspecification, or overlapping events.

Return:
- design summary
- event-date risks
- benchmark/model risks
- inference risks
- safer methods paragraph
- table/figure checks to run
```

Sources and workflow influences: Paul Goldsmith-Pinkham's AI-era research caution about p-hacking and replication, his work on credibility and financial event-study interpretation, plus finance-specific concerns around factor mining, backtest overfitting, and empirical transparency.
