> Copyright (c) 2026 SuperJayLiu (Chaojie Liu). Licensed under the repository MIT License.

# Systematic Review and Meta-Analysis Skills

Use these skills when the output must be a reproducible evidence synthesis rather than an ordinary narrative literature review. A systematic review fixes a question, search boundary, eligibility rule, screening trail, and extraction scheme before synthesis; a meta-analysis is optional and requires conceptually comparable estimands.

> [!IMPORTANT]
> PRISMA is a reporting guideline, not proof that the search was complete, the included studies were unbiased, or a pooled estimate is meaningful. Never pool studies merely because they report numbers that can be converted to the same scale.

> [!NOTE]
> Import/use-as-skill protocol for any block on this page: `Start by collecting only the missing inputs needed for the task. Ask up to five clarifying questions when the review question, search boundary, eligibility, source access, effect measure, or output format is unclear. Before screening or pooling, first return "Proposed protocol and assumptions" and ask the user to confirm. Before finalizing, double-check identifiers, duplicate reports, extraction provenance, incompatible estimands, risk of bias, and unsupported conclusions. End with "What I produced", "What I did not change", "What you must verify", and "Questions for you".`

## Choose a Skill

| Research task | Use |
| --- | --- |
| write a review protocol and reproducible search strategy | Skill 1 |
| deduplicate records and screen with an auditable ledger | Skill 2 |
| extract and harmonize study designs, estimands, and effect sizes | Skill 3 |
| decide whether and how to pool estimates | Skill 4 |
| audit heterogeneity, dependence, publication selection, and conclusions | Skill 5 |

## Boundary With Narrative Literature Review

Use [Literature Review and Source Synthesis](10-literature-review-and-source-synthesis-skills.md) when the goal is a thematic, conceptual, or positioning argument from a bounded set of verified papers. Use this page when the claim requires reproducible searching, eligibility decisions, a flow count, coded study records, or quantitative pooling.

## Skill 1: Systematic Review Protocol and Search Builder

```text
Act as a systematic-review methodologist for economics/finance.

Inputs:
- Review question, population/setting, intervention/exposure, comparator, and outcomes: ask if missing
- Eligible designs, time/language/geography/publication-status limits: ask if missing
- Databases, working-paper repositories, citation indexes, and grey-literature sources available: ask if missing
- Protocol/registry/reporting standard: ask if missing
- Review team and independent-screening capacity: ask if missing

Before searching, produce:
1. a precise review question and target estimand/phenomenon;
2. inclusion and exclusion criteria that can be applied without seeing preferred results;
3. a concept table with synonyms, controlled vocabulary, and field-specific terms;
4. database-specific draft queries, search dates, coverage limits, and update plan;
5. a plan for working papers, published versions, appendices, replication packages, backward/forward citation search, and author contact;
6. a protocol for deduplication, independent screening, conflict resolution, extraction, risk-of-bias assessment, and amendments;
7. a plan to archive exact queries, exports, versions, and counts.

Return:
- protocol outline;
- source-by-source search table;
- eligibility decision tree;
- screening/extraction fields;
- amendment log template;
- limitations of the search boundary.

Rules:
- Do not claim “all studies” unless the documented boundary supports it.
- Do not invent database syntax or access; mark it for live verification.
- Do not use citation count as an eligibility criterion unless the protocol justifies it.
- Do not let AI make final inclusion decisions without human review.
```

## Skill 2: Deduplication and Screening Ledger

```text
Build an auditable screening workflow from exported review records.

Inputs:
- Export formats and source database for each file: ask if missing
- Frozen eligibility criteria and protocol version: ask if missing
- Reviewers and conflict-resolution rule: ask if missing

Create a ledger with one stable record ID and these fields:
- source database and export batch;
- title, authors, year, DOI/working-paper ID/URL;
- normalized identifiers;
- suspected duplicate family;
- title/abstract decision by reviewer;
- full-text decision by reviewer;
- exclusion reason from a frozen vocabulary;
- conflict/adjudication result;
- linked working-paper, accepted, published, corrigendum, or retracted version;
- notes and timestamp.

Workflow:
1. exact-identifier deduplication;
2. normalized title/author/year candidate matching;
3. manual review of uncertain pairs;
4. version-family linking without automatically discarding informative versions;
5. independent screening and conflict resolution;
6. count reconciliation for a flow diagram.

Return:
- ledger schema;
- deterministic matching rules;
- uncertain-pair queue;
- exclusion vocabulary;
- flow-count reconciliation check.

Rules:
- Never silently merge two records on fuzzy title similarity alone.
- Preserve every source record and decision even after deduplication.
- Record one primary report per study but keep links to all companion reports.
```

## Skill 3: Estimand and Effect-Size Extraction Audit

```text
Design or audit a study-extraction sheet for an economics/finance evidence synthesis.

For each study/report, extract:
1. study ID and report/version ID;
2. setting, sample, period, unit, and design;
3. treatment/exposure, comparator, outcome definition, horizon, and scale;
4. target estimand and identifying assumptions;
5. specification, controls/fixed effects, weights, and inference;
6. effect estimate, standard error/CI/test statistic, sample size, and covariance information;
7. transformations needed to reach a common effect measure;
8. risk-of-bias/design-credibility judgments with quoted evidence locations;
9. funding, conflicts, preregistration, data/code availability, and corrections;
10. whether multiple estimates share a sample, outcome, treatment, or paper.

Create a harmonization table that separates:
- numerically convertible and conceptually comparable;
- convertible but substantively different;
- not convertible without author data/assumptions;
- narrative-only evidence.

Return:
- extraction schema and coding manual;
- double-extraction/check procedure;
- effect-size conversion formulas and assumptions to verify;
- dependency map for multiple estimates;
- stop list of studies/estimates that should not be pooled.

Rules:
- Do not choose the most favorable estimate from each paper.
- Do not mix ITT, TOT/LATE, ATE, elasticities, semi-elasticities, standardized effects, and raw-unit effects without an explicit bridge.
- Do not reconstruct missing uncertainty from p-value stars when exact information may be obtainable.
```

## Skill 4: Meta-Analysis Design and Pooling Plan

```text
Decide whether a meta-analysis is justified and, if so, specify it before running it.

Inputs:
- Extraction table and dependency map: ask if missing
- Common effect measure and substantive interpretation: ask if missing
- Number of studies, estimates per study, and design families: ask if missing
- Prespecified moderators and sensitivity analyses: ask if missing

Gate 1 — conceptual poolability:
- Are the questions, outcomes, horizons, comparators, populations, and estimands sufficiently comparable?
- Would the pooled number answer a coherent economics/finance question?
- Should some evidence remain separate by design or estimand?

Gate 2 — statistical plan:
1. fixed-effect or random-effects model and why;
2. heterogeneity: tau-squared, I-squared, Q, and a prediction interval;
3. dependence: one effect per study, multilevel model, robust variance estimation, or prespecified aggregation;
4. small-number-of-studies inference;
5. moderator/meta-regression rules and minimum information needed;
6. influence, leave-one-study-out, alternative effect measure, estimator, and design-quality sensitivities;
7. code and data outputs needed to reproduce forest/funnel plots and tables.

Return:
- poolability decision by evidence family;
- model specification;
- dependency solution;
- sensitivity matrix;
- result table/figure shells;
- language that remains valid under high heterogeneity.

Rules:
- Random effects do not make incomparable studies comparable.
- A high I-squared is not by itself a reason to abandon synthesis, nor is a low value proof of homogeneity.
- Meta-regression is observational across studies and does not establish a moderator mechanism.
```

## Skill 5: Publication-Selection and Conclusion Audit

```text
Audit this systematic review/meta-analysis before conclusions are written.

Check:
1. protocol amendments and outcome-aware eligibility changes;
2. flow counts, duplicate report families, missing full texts, and search-update date;
3. extraction errors and selective estimate choice within studies;
4. risk of bias and design credibility by evidence family;
5. heterogeneity, prediction intervals, influential studies, and effect dependence;
6. small-study effects and publication selection using funnel plots/tests only when their assumptions and study count are defensible;
7. grey-literature/working-paper coverage and publication-status sensitivity;
8. correction, retraction, and version status;
9. whether certainty and external-validity language exceeds the evidence.

Return:
- high/medium/low severity findings;
- corrected claims;
- sensitivity analyses still required;
- PRISMA/reporting checklist gaps;
- reproducibility packet: protocol, queries, exports, ledger, extraction data, code, and output inventory.

Rules:
- Funnel asymmetry is not synonymous with publication bias.
- Trim-and-fill is a sensitivity device, not a repair that proves an unbiased effect.
- A statistically significant pooled estimate can still be substantively small, heterogeneous, design-dependent, or selected.
```

## Sources and Workflow Influences

The skills above are original economics/finance adaptations. External sources are credited here for the workflow elements they informed.

- [AlterLab, `AlterLab-Academic-Skills` (MIT), `alterlab-meta-analysis`](https://github.com/AlterLab-IEU/AlterLab-Academic-Skills) — separates literature discovery from quantitative pooling and foregrounds effect-size construction, heterogeneity, forest/funnel plots, and bias diagnostics. This page adds economics-specific estimand harmonization, dependent estimates, working-paper version families, and stronger limits on publication-bias tools.
- [K-Dense Inc., `scientific-agent-skills` (MIT), `literature-review`](https://github.com/K-Dense-AI/scientific-agent-skills) — reproducible database search, evidence-ledger, citation verification, and archived outputs.
- [PRISMA Executive, PRISMA 2020](https://www.prisma-statement.org/prisma-2020) — reporting checklist and flow-diagram discipline. PRISMA materials state their CC BY 4.0 terms; this repository links to the originals rather than reproducing the checklist.
- [Cochrane, Higgins, Thomas, and colleagues, *Cochrane Handbook for Systematic Reviews of Interventions*, version 6.5](https://www.cochrane.org/authors/handbooks-and-manuals/handbook/current) — scope, eligibility, search, effect measures, risk of bias, synthesis, missing results, and interpretation.
- [Campbell Collaboration](https://www.campbellcollaboration.org/) — systematic-review methods for social, behavioral, policy, and economic evidence; check the current Campbell standards when preparing a Campbell review.
- Stanley, T. D., and Hristos Doucouliagos. *Meta-Regression Analysis in Economics and Business*. Routledge, 2012 — economics-specific publication selection, heterogeneity, and meta-regression context.

Last checked: 2026-08-24
