> Copyright (c) 2026 SuperJayLiu (Chaojie Liu). Licensed under the repository MIT License.

# Empirical Methods Skills for Economics Research

These skills are tailored for applied economics: labor, public, development, health, education, macro, IO, urban, political economy, and related fields.

## Skill 1: Draft Empirical Methods Section for Economics

```text
Draft an empirical methods section for an applied economics paper.

Inputs:
- Research question: [question]
- Setting/institutional background: [setting]
- Unit of observation: [unit]
- Sample period: [period]
- Data sources: [sources]
- Outcome variables: [outcomes]
- Treatment/exposure/shock: [treatment]
- Control variables: [controls]
- Empirical design: [DiD/event study/RD/IV/RCT/panel FE/synthetic control/other]
- Main estimating equation, if any: [equation]
- Identification assumption: [assumption]
- Threats to validity: [threats]
- Inference plan: [standard errors/clustering/randomization inference/etc.]

Write:
1. Data and sample paragraph.
2. Variable construction paragraph.
3. Empirical specification with equation.
4. Identification argument.
5. Inference paragraph.
6. Threats to validity and planned robustness checks.
7. Interpretation paragraph explaining what the coefficient means.

Rules:
- Do not claim causality unless the design and assumptions support it.
- Do not invent controls, sample restrictions, or robustness checks.
- State the identifying variation clearly.
- Explain economic magnitude, not only statistical significance.
- Use cautious applied economics prose.
```

## Skill 2: Check Empirical Methods Section for Economics

```text
Audit this empirical methods section as an applied econometrician.

Text:
[paste methods section]

Known project facts:
- Research question: [question]
- Data: [data]
- Design: [design]
- Main outcome/treatment: [variables]

Check:
1. Is the unit of observation clear?
2. Is the treatment/exposure/shock clearly defined?
3. Is the comparison group credible?
4. Is the identifying variation stated?
5. Are fixed effects and controls justified?
6. Is inference/clustering appropriate?
7. Are pre-trends, balance, manipulation, exclusion, or monotonicity issues addressed where relevant?
8. Are robustness checks real or merely promised?
9. Does the prose overclaim causality?
10. Are coefficient interpretations correct?

Return:
- Major issues.
- Minor issues.
- Suggested rewrite for the weakest paragraph.
- Checklist of analyses to verify in code.
```

## Skill 3: Methods-to-Code Consistency Check

```text
Compare the methods description to the code/table plan.

Methods text:
[paste]

Code summary or script:
[paste or describe]

Table/figure plan:
[paste]

Identify mismatches:
- variables named in text but absent in code
- sample restrictions in code but not text
- controls/fixed effects in text but not code
- standard errors or clustering mismatch
- table labels that misstate coefficients
- robustness checks described but not run
- results interpreted beyond design

Return a table with: issue, evidence, severity, required fix.
```

Sources and workflow influences: Paul Goldsmith-Pinkham's Applied Empirical Methods course emphasis on practical implementation, research design intuition, communication, and disentangling the experiment behind causal claims.

