> Copyright (c) 2026 SuperJayLiu (Chaojie Liu). Licensed under the repository MIT License.

# Survey, Experiment, and Preregistration Skills

Use these skills before collecting original data or before making a confirmatory claim from a planned study. They connect the research question to the unit of assignment, measurement instrument, power, analysis plan, and design-based inference.

> [!WARNING]
> AI can help expose design choices; it cannot approve research ethics, consent language, deception, participant compensation, data protection, or field operations. Follow the applicable IRB/ethics, institution, funder, registry, platform, and local-law rules.

> [!NOTE]
> Import/use-as-skill protocol for any block on this page: `Start by collecting only the missing inputs needed for the task. Ask up to five clarifying questions when required inputs, data rules, method details, permissions, audience, or output format are unclear. For long outputs or file-producing tasks, first return "Proposed structure and assumptions" and ask the user to confirm. Before finalizing, double-check for unsupported claims, invented citations or results, privacy risks, and mismatch with the requested format. End with "What I produced", "What I did not change", "What you must verify", and "Questions for you".`

## Choose a Skill

| Research task | Use |
| --- | --- |
| turn a causal question into a randomized field/lab/online experiment | Skill 1 |
| design or adapt a survey instrument and sampling plan | Skill 2 |
| write a pre-analysis plan or preregistration without pretending outcomes are unseen | Skill 3 |
| audit randomization, power, compliance, attrition, and implementation | Skill 4 |
| analyze a weighted, stratified, or clustered survey correctly | Skill 5 |

## Boundary With Existing Skills

- Use [Research Question, Taste, and Positioning](18-research-question-taste-and-positioning-skills.md) before this page if the question is still vague.
- Use [Causal Inference and Econometrics](11-causal-inference-econometrics-and-time-series-skills.md) for observational DiD/IV/RD/SCM designs.
- Use [Data Cleaning and Output](14-data-cleaning-merging-analysis-and-output-skills.md) after the design is fixed to build the data pipeline.
- Use this page when the researcher controls assignment, creates a survey/instrument, needs a prospective analysis plan, or must honor a complex sampling design.

## Skill 1: Randomized Experiment Design Gate

```text
Act as a skeptical economics/finance experiment-design assistant.

Inputs:
- Research question and mechanism: ask if missing
- Target population and setting: ask if missing
- Intervention/treatment arms and control condition: ask if missing
- Unit of assignment and unit of outcome measurement: ask if missing
- Outcome timing and implementation window: ask if missing
- Spillover/interference risk: ask if missing
- Operational, ethical, legal, and platform constraints: ask if missing
- Budget, expected take-up, attrition, and feasible sample: ask if missing

Before proposing an analysis, produce a design gate that:
1. defines the causal estimand, treatment versions, comparator, and target population;
2. distinguishes the unit of assignment, treatment delivery, observation, and analysis;
3. chooses individual, cluster, pair-matched, stratified, factorial, encouragement, or phased assignment only after explaining the trade-off;
4. lists blocking/stratification variables known before assignment;
5. identifies interference, contamination, noncompliance, differential attrition, and implementation risks;
6. specifies primary and secondary outcomes, measurement timing, and treatment-independent data collection;
7. states the analysis implied by the design, including clustering and randomization inference where relevant;
8. creates a seeded, reproducible allocation plan and a protected allocation file plan;
9. marks every ethics/consent/data-protection issue that requires human or institutional approval.

Return:
- design decision table;
- estimand and unit map;
- randomization and implementation plan;
- failure-mode pre-mortem;
- analysis skeleton;
- preregistration fields still missing.

Rules:
- Do not treat repeated observations as independent assignment units.
- Do not optimize treatment balance by inspecting future outcomes.
- Do not claim that baseline balance tests validate randomization.
- Do not invent a sample size before effect size, ICC, take-up, attrition, assignment ratio, and design are stated.
- Do not generate consent/deception language as approved legal or ethics text.
```

## Skill 2: Survey Instrument and Sampling Plan

```text
Design or audit an economics/finance survey as a measurement system, not a list of questions.

Inputs:
- Constructs and intended estimands: ask if missing
- Target population and sampling frame: ask if missing
- Survey mode and languages: ask if missing
- Existing validated instruments and permission to reuse them: ask if missing
- Sensitive topics or identifiers: ask if missing
- Intended analysis and subgroup comparisons: ask if missing
- Length, device, accessibility, and field constraints: ask if missing

Workflow:
1. Map each construct to dimensions, observable indicators, and planned analysis.
2. Check whether a validated instrument exists and whether adaptation/reuse is licensed.
3. Build a sampling-frame and coverage-error table before drafting items.
4. Draft one concept per item with a specific reference period and exhaustive, non-overlapping response options.
5. Mark leading, loaded, double-barreled, ambiguous, hypothetical, sensitive, and recall-heavy items.
6. Plan ordering, skip logic, randomization, device layout, translations, and paradata.
7. Plan expert review, cognitive interviews, a pilot, and revision decisions.
8. Plan reliability and validity evidence appropriate to the construct; do not equate one alpha threshold with validity.
9. Define consent, minimization, retention, access, and disclosure rules for respondent data.

Return:
- construct-to-item matrix;
- sampling and coverage plan;
- draft instrument with annotations;
- cognitive-interview and pilot protocol;
- measurement-validation plan;
- privacy and fieldwork checklist;
- items that should be removed or need author approval.

Rules:
- Do not report a convenience sample as representative.
- Do not use attention checks or exclusions without prespecifying their role and possible bias.
- Do not collect an identifier merely because the platform allows it.
- Do not assume literal translation establishes cross-language measurement equivalence.
```

## Skill 3: Pre-Analysis Plan and Preregistration Builder

```text
Build a transparent pre-analysis plan for an economics/finance study.

First establish the timing status:
- PROSPECTIVE: target outcome data have not been observed;
- BLINDED: data exist but the analyst is demonstrably blinded to treatment/outcomes;
- RETROSPECTIVE: relevant outcomes or results have already been observed.

Never label a retrospective plan as prospective preregistration.

Inputs:
- Registry/journal/funder requirements: ask if missing
- Research questions and theory: ask if missing
- Design and assignment mechanism: ask if missing
- Sample, stopping rule, and exclusions: ask if missing
- Outcomes, construction, timing, and hierarchy: ask if missing
- Estimands, models, fixed effects, standard errors, and weights: ask if missing
- Missing-data, attrition, noncompliance, and multiple-testing rules: ask if missing
- Planned heterogeneity and robustness analyses: ask if missing

Create:
1. study status and timestamp statement;
2. confirmatory hypotheses linked one-to-one to outcomes and estimands;
3. exact sample, exclusion, treatment, outcome, and variable-construction rules;
4. primary specification and prespecified alternatives with a decision rule;
5. inference, multiplicity, missing-data, attrition, noncompliance, and stopping plans;
6. planned tables/figures and a results-blind mock output shell;
7. exploratory-analysis section that remains explicitly exploratory;
8. deviation log template: original plan, change, date, reason, outcome knowledge, and consequence for interpretation.

Return:
- registry-ready plan outline;
- unresolved decision table;
- confirmatory/exploratory boundary;
- machine-readable analysis-spec table;
- verification checklist.

Rules:
- Do not choose specifications based on which result is significant.
- Do not hide deviations; preserve the registered analysis and label additions.
- Preregistration increases transparency but does not certify identification, measurement, ethics, or code correctness.
```

## Skill 4: Randomization, Power, and Implementation Audit

```text
Audit this planned or completed randomized study before results are interpreted.

Inputs:
- Allocation code/schedule and seed handling: ask if missing
- Assignment unit, strata/blocks/clusters, and arm ratios: ask if missing
- Power calculation assumptions: ask if missing
- Enrollment, take-up, compliance, attrition, and timing data: ask if missing
- Primary estimand and inference plan: ask if missing

Check:
1. allocation reproducibility and protection from manual reassignment;
2. whether block/stratum/cluster variables appear in the analysis;
3. whether the MDE/power calculation matches the actual assignment unit, ICC, treatment share, take-up, attrition, and multiple outcomes;
4. whether power is reported as a design trade-off, not a post-hoc explanation of significance;
5. intention-to-treat, treatment-on-treated/IV, and per-protocol distinctions;
6. differential attrition, missing outcomes, treatment contamination, and spillovers;
7. manipulation or implementation deviations after randomization;
8. randomization inference or few-cluster methods when conventional asymptotics are weak;
9. consistency among registry, field records, code, sample flow, tables, and prose.

Return:
- severity-ranked audit;
- recalculation inputs that must be corrected;
- sample-flow and compliance table shell;
- confirmatory-versus-exploratory classification;
- safe interpretation language.
```

## Skill 5: Complex-Survey Design and Analysis Gate

```text
Audit or plan analysis of a probability survey with weights, strata, clusters/PSUs, replicate weights, or finite-population corrections.

Inputs:
- Survey documentation and release/version: ask if missing
- Target population and sample design: ask if missing
- Weight variables and weight type: ask if missing
- Strata, PSU/cluster, FPC, and replicate-weight fields: ask if missing
- Domain/subpopulation estimates and models: ask if missing

Before quoting any population estimate:
1. declare the design object: weights, strata, PSU, FPC, and nesting;
2. distinguish base/design, nonresponse, post-stratification/calibration, and replicate weights;
3. preserve the full design when estimating domains/subpopulations;
4. use Taylor linearization or the provider-specified replicate-weight method;
5. report unweighted N separately from weighted population estimates;
6. report design effects or effective sample size for key estimates;
7. use design-adjusted regression/inference and explain the target population;
8. check singleton strata, zero/extreme weights, trimming/calibration decisions, and missing design fields.

Return:
- design declaration;
- software plan in R/Stata/Python;
- weighted estimate/table shell with correct uncertainty;
- diagnostics and stop conditions;
- disclosure text for methods and notes.

Rules:
- Do not run an unweighted analysis merely because point estimates look similar.
- Do not filter the raw data first and then pretend the original design remains intact.
- Do not infer causality from survey weighting alone.
```

## Sources and Workflow Influences

The copy-ready blocks above are original adaptations for economics and finance research. The following sources informed specific workflow patterns; none was copied wholesale.

- [World Bank DIME Analytics, *Development Research in Practice: The DIME Analytics Data Handbook*](https://worldbank.github.io/dime-data-handbook/) — research-design variables in a master dataset, reproducible randomization, power/MDE trade-offs, survey acquisition, and pre-analysis-plan discipline.
- [K-Dense Inc., `scientific-agent-skills` (MIT), `experimental-design` and `hypothesis-generation`](https://github.com/K-Dense-AI/scientific-agent-skills) — explicit unit-of-assignment, blocking, seeded allocation, rival predictions, evidence boundaries, and preregistration artifacts. Adapted here to social-science field experiments and economics estimands.
- [AlterLab, `AlterLab-Academic-Skills` (MIT), `alterlab-survey-design`, `alterlab-survey-analysis`, and `alterlab-preregistration-discipline`](https://github.com/AlterLab-IEU/AlterLab-Academic-Skills) — construct-first survey design, cognitive interviews/pilots, design-object-first survey inference, and plan/deviation gates. The present page replaces absolute rules with a timing-status distinction suitable for observational and secondary-data economics.
- [Center for Open Science, Preregistration](https://www.cos.io/initiatives/prereg) — confirmatory/exploratory separation and transparent deviations.
- [EGAP, Lula Chen and Chris Grady, “10 Things to Know About Pre-Analysis Plans”](https://egap.org/resource/10-things-to-know-about-pre-analysis-plans/) — social-science preregistration orientation.
- [AEA RCT Registry](https://www.socialscienceregistry.org/) — economics and social-science trial registration destination; verify current fields and policies on the registry before submission.

Last checked: 2026-08-24
