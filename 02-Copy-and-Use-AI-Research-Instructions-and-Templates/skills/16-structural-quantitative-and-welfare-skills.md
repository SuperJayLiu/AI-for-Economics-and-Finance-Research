> Copyright (c) 2026 SuperJayLiu (Chaojie Liu). Licensed under the repository MIT License.

# Structural, Quantitative, and Welfare Skills

Use these skills for structural economics, quantitative macro, IO, trade, labor, public finance, banking, asset pricing, corporate finance, and contract-theory projects where the empirical object is not just a regression coefficient.

> [!IMPORTANT]
> AI can help organize equations, estimation plans, simulations, and counterfactual logic. It cannot certify identification, convergence, equilibrium existence, welfare interpretation, or model fit.

Questions or suggestions for this part: email [jay.liu@bristol.ac.uk](mailto:jay.liu@bristol.ac.uk) with subject `[AI Econ Finance Structural Skill] Suggestion`.

> [!NOTE]
> Import/use-as-skill protocol for any block on this page: `Start by collecting only the missing inputs needed for the task. Ask up to five clarifying questions when required inputs, data rules, method details, permissions, audience, or output format are unclear. For long outputs, file-producing tasks, slides, code, methods sections, literature reviews, referee responses, or agentic workflows, first return "Proposed structure and assumptions" and ask the user to confirm before producing the full output. Before finalizing, double-check for unsupported claims, invented citations or results, privacy risks, and mismatch with the requested format. End with "What I produced", "What I did not change", "What you must verify", and "Questions for you".`

## Choose a Skill

| Need | Use |
| --- | --- |
| map a structural model into objects and assumptions | Skill 1 |
| connect moments to parameters | Skill 2 |
| plan GMM/SMM/MLE/calibration | Skill 3 |
| audit simulations and counterfactuals | Skill 4 |
| check welfare claims | Skill 5 |

## Skill 1: Structural Model Map

```text
Act as a structural economics/finance model assistant.

Model context:
- Field: If I have not provided it, ask me to specify: IO/macro/trade/labor/public/asset pricing/corporate finance/etc.
- Research question: If I have not provided it, ask me to specify: question
- Agents: If I have not provided it, ask me to specify: households/firms/banks/investors/government/etc.
- State variables: If I have not provided it, ask me to specify: states
- Choices: If I have not provided it, ask me to specify: choices
- Shocks: If I have not provided it, ask me to specify: shocks
- Constraints: If I have not provided it, ask me to specify: constraints
- Equilibrium concept: If I have not provided it, ask me to specify: equilibrium
- Data/moments available: If I have not provided it, ask me to specify: moments/data
- Counterfactual of interest: If I have not provided it, ask me to specify: counterfactual

Create a model map:
1. agents;
2. timing;
3. state variables;
4. choice variables;
5. objective functions;
6. constraints;
7. equilibrium conditions;
8. parameters;
9. moments or targets;
10. counterfactuals;
11. welfare object.

Return:
- model-object table;
- timing diagram in text;
- assumptions that drive identification;
- parameters not disciplined by data;
- missing equations or definitions;
- risks to interpretation.

Rules:
- Do not add equations not supplied unless clearly labeled as suggestions.
- Preserve the author's intended mechanism.
- Separate model mechanics from empirical discipline.
```

## Skill 2: Moments-to-Parameters Audit

```text
Audit how this model maps data moments to structural parameters.

Inputs:
- Model summary: If I have not provided it, ask me to specify: paste
- Parameters: If I have not provided it, ask me to specify: list
- Moments or target statistics: If I have not provided it, ask me to specify: list
- Estimation method: If I have not provided it, ask me to specify: GMM/SMM/MLE/calibration/Bayesian/other
- Data sources: If I have not provided it, ask me to specify: sources
- Identification claim: If I have not provided it, ask me to specify: claim

For each parameter, answer:
1. Which moment identifies or disciplines it?
2. Is the mapping direct, indirect, or weak?
3. What other parameter could explain the same moment?
4. What normalization or exclusion restriction is being used?
5. What sensitivity check should be reported?

Return:
- parameter-moment table;
- underidentified or weakly disciplined parameters;
- overidentifying moments;
- suggested sensitivity analysis;
- cautious methods language.

Rules:
- Do not say a parameter is identified just because the model estimates it.
- Flag moments that are outcomes of the counterfactual rather than valid targets.
- Distinguish fit from identification.
```

## Skill 3: GMM, SMM, MLE, or Calibration Plan

```text
Design an estimation and validation plan for this quantitative model.

Project facts:
- Model: If I have not provided it, ask me to specify: summary
- Estimation method: If I have not provided it, ask me to specify: GMM/SMM/MLE/calibration/Bayesian
- Parameters: If I have not provided it, ask me to specify: list
- Data moments: If I have not provided it, ask me to specify: moments
- Objective function: If I have not provided it, ask me to specify: known/unknown
- Simulation requirements: If I have not provided it, ask me to specify: if any
- Software: If I have not provided it, ask me to specify: R/Python/Julia/Matlab/Stata/etc.
- Existing code: If I have not provided it, ask me to specify: describe

Create a plan covering:
1. data preparation;
2. moment construction;
3. objective function;
4. weighting matrix or likelihood;
5. numerical optimization;
6. starting values and bounds;
7. convergence diagnostics;
8. standard errors or uncertainty;
9. model fit table;
10. sensitivity analysis;
11. reproducibility checks.

Return:
- step-by-step estimation plan;
- code skeleton or pseudo-code;
- diagnostic checklist;
- table shells for paper;
- failure modes.

Rules:
- Do not hide convergence failures.
- Do not let a good fit table substitute for external validity.
- Do not claim welfare implications without checking the welfare object.
```

## Skill 4: Counterfactual Validity Check

```text
Audit this structural or quantitative counterfactual.

Counterfactual:
- Policy/shock/change: If I have not provided it, ask me to specify: counterfactual
- Baseline model: If I have not provided it, ask me to specify: summary
- Parameters held fixed: If I have not provided it, ask me to specify: parameters
- Equilibrium objects recomputed: If I have not provided it, ask me to specify: objects
- Outcome of interest: If I have not provided it, ask me to specify: outcomes
- Welfare metric: If I have not provided it, ask me to specify: metric

Check:
1. What exactly changes in the counterfactual?
2. Which agents reoptimize?
3. Which prices, constraints, or aggregates adjust?
4. Which parameters are assumed invariant?
5. Does the counterfactual isolate the intended mechanism?
6. Are there equilibrium existence or multiplicity concerns?
7. Is the welfare comparison well-defined?
8. What reduced-form moments support or challenge the mechanism?

Return:
- counterfactual logic map;
- assumptions that matter most;
- robustness/counterfactual variants;
- welfare caveats;
- safe interpretation paragraph.
```

## Skill 5: Welfare Interpretation Guardrail

```text
Review this welfare or policy interpretation from a structural/quantitative paper.

Text:
If I have not provided this, ask me to provide: paste

Model facts:
- Agents: If I have not provided it, ask me to specify: agents
- Welfare object: If I have not provided it, ask me to specify: consumer surplus/social welfare/utility/value function/etc.
- Counterfactual: If I have not provided it, ask me to specify: counterfactual
- Distributional dimensions: If I have not provided it, ask me to specify: groups
- Key assumptions: If I have not provided it, ask me to specify: assumptions

Check for:
- welfare object unclear;
- partial-equilibrium result stated as general equilibrium;
- distributional effects hidden by averages;
- policy recommendation stronger than model supports;
- ignored external validity limits;
- missing uncertainty around estimated parameters;
- mechanism not isolated.

Return:
1. overclaiming sentences;
2. safer replacement language;
3. assumptions that must be disclosed;
4. robustness or sensitivity checks;
5. one paragraph explaining what the welfare result does and does not establish.
```

## Sources and Workflow Influences

This page adapts theory-model audit logic, structural-estimation workflow norms, and AI-assisted code/debugging patterns into direct-use prompts for quantitative economics and finance.

Last checked: 2026-05-24
