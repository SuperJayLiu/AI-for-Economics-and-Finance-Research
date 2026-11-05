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

### Tuned DML and Generated Controls

For tuned DML, collect API/version, learners, preset/tuned parameters, treatment/repetition/fold maps, splits, scorer, and predictions. Verify fold-specific fit isolation and unchanged untuned parameters. Compare a fresh direct-parameter reference under matched settings; recompute the actual inner tuning objective separately from outer-fold loss. Return evidence, tolerances, discrepancies, and unverified conditions. Use the [full DML audit](https://github.com/SuperJayLiu/AI-for-Economics-and-Finance-Research/blob/main/02-Copy-and-Use-AI-Research-Instructions-and-Templates/skills/03-empirical-methods-skills-for-economics-research.md#dml-tuning-audit-for-skills-2-and-3).

For many generated proxies used to control confounding, use the [measurement page's role and identification check](https://github.com/SuperJayLiu/AI-for-Economics-and-Finance-Research/blob/main/02-Copy-and-Use-AI-Research-Instructions-and-Templates/skills/15-text-as-data-and-llm-measurement-skills.md#generated-controls-role-and-identification-check). Retain unresolved assumptions and inference requirements.

## Sources and Workflow Influences

- DoubleML team, Philipp Bach/Sven Klaassen maintainers: [leave untuned learners unchanged, #447](https://github.com/DoubleML/doubleml-for-py/pull/447), [treatment/repetition indexing, #438](https://github.com/DoubleML/doubleml-for-py/pull/438), [validate LPLR tuning against its CV objective, #446](https://github.com/DoubleML/doubleml-for-py/pull/446), merged 2026-11-04; checked 2026-11-05. [BSD-3-Clause at #447 merge](https://github.com/DoubleML/doubleml-for-py/blob/ddf496e7c17cb81e5be19d553558b0eb8c0d1b56/LICENSE), copyright Bach/Chernozhukov/Klaassen/Kurz/Spindler. Original tuning-verification summary and links only; no code, tests, fixtures, or documentation copied/executed. Inspect final diffs: #446 also changes production routing of outer-fold parameters to inner models despite its test-only description. Fixed-release availability is unverified.
- Timothy Christensen/Daniel Vebman, Yale University, [Regression with Many Generated Controls, arXiv:2611.06855v1](https://arxiv.org/abs/2611.06855v1), submitted 2026-11-04; checked 2026-11-05. Influence: route generated-control users to a role/assumption check. ArXiv perpetual non-exclusive distribution license does not grant general reuse. No paper prose, equations, proofs, examples, figures, code, or structure copied; no implementation executed. Conditional consistency is not certified inference.
