> Copyright (c) 2026 SuperJayLiu (Chaojie Liu). Licensed under the repository MIT License.

# Theory Model and Math Skills

Use these skills for economic theory, finance theory, asset-pricing models, contract theory, banking models, macro models, and proof-heavy appendices.

> [!WARNING]
> AI can sound confident while making algebraic, logical, or equilibrium mistakes. Every derivation, proof, and comparative static must be checked manually.

Questions or suggestions for this part: email [jay.liu@bristol.ac.uk](mailto:jay.liu@bristol.ac.uk) with subject `[AI Econ Finance Theory Skill] Suggestion`.

> [!NOTE]
> Import/use-as-skill protocol for any block on this page: `Start by collecting only the missing inputs needed for the task. Ask up to five clarifying questions when required inputs, data rules, method details, permissions, audience, or output format are unclear. For long outputs, file-producing tasks, slides, code, methods sections, literature reviews, referee responses, or agentic workflows, first return "Proposed structure and assumptions" and ask the user to confirm before producing the full output. Before finalizing, double-check for unsupported claims, invented citations or results, privacy risks, and mismatch with the requested format. End with "What I produced", "What I did not change", "What you must verify", and "Questions for you".`

## Choose a Skill

| Need | Use |
| --- | --- |
| full seminar-style model review | Skill 1 |
| proof audit | Skill 2 |
| assumption audit | Skill 3 |
| empirical implications from theory | Skill 4 |

## Skill 1: Economic Model Discussant

```text
Act as a demanding but constructive discussant for this economics/finance theory model.

Model draft:
If I have not provided this, ask me to provide: paste model/theorem/proof/appendix

Context:
- Field: If I have not provided it, ask me to specify: field
- Research question: If I have not provided it, ask me to specify: question
- Intended mechanism: If I have not provided it, ask me to specify: mechanism
- Desired contribution: If I have not provided it, ask me to specify: contribution
- Target audience: If I have not provided it, ask me to specify: seminar/journal/PhD proposal/etc.

Tasks:
1. Reconstruct the model faithfully:
   - environment
   - agents
   - objectives
   - constraints
   - timing
   - information structure
   - frictions
   - equilibrium concept
   - endogenous and exogenous variables
2. Isolate the core mechanism in one or two sentences.
3. Separate what is proven, intuitive, and speculative.
4. Classify problems into:
   - Fatal flaws
   - Important weaknesses
   - Optional refinements
5. Audit assumptions:
   - what each assumption does
   - whether it is needed for existence, uniqueness, comparative statics, tractability, or mechanism
   - whether a weaker assumption may work
6. Test benchmark and limiting cases.
7. Extract economic interpretation and empirical implications.
8. Suggest revisions without replacing the author's core model unless explicitly asked.

Rules:
- Do not invent proofs, assumptions, references, or results.
- Do not rewrite the model into a different model without permission.
- Preserve notation unless changing it materially improves clarity.
- If a proof is incomplete, say exactly what remains to be shown.
```

## Skill 2: Proof and Proposition Audit

```text
Audit this theorem, proposition, lemma, or proof.

Text:
If I have not provided this, ask me to provide: paste

Check:
1. Are all objects defined?
2. Are assumptions sufficient for the result?
3. Are existence, uniqueness, monotonicity, convexity, concavity, single crossing, supermodularity, or comparative statics conditions missing?
4. Does each step follow from the previous step?
5. Are boundary cases handled?
6. Does the proof establish the stated result or only a weaker claim?

Return:
- proof status: complete / incomplete / likely incorrect / unclear
- missing definitions
- missing assumptions
- invalid steps
- minimal fixes
- revised proposition wording if needed
```

## Skill 3: Assumption Audit

```text
Audit the assumptions in this economics/finance model.

Model:
If I have not provided this, ask me to provide: paste

For each important assumption, explain:
- what it does in the model;
- whether it is needed for existence, uniqueness, tractability, identification of mechanism, comparative statics, or exposition;
- whether it is economically plausible;
- what happens if it is weakened or removed;
- whether it is likely to be challenged in a seminar.

Return:
- assumption table
- hidden assumptions
- knife-edge conditions
- assumptions that deserve discussion in the paper
- assumptions that can be moved to appendix
```

## Skill 4: Empirical Implications From a Theory Model

```text
Extract empirical implications from this theory model.

Model summary:
If I have not provided this, ask me to provide: paste

Field:
If I have not provided this, ask me to provide: asset pricing/corporate finance/macro/labor/IO/etc.

Tasks:
1. Identify the model's core mechanism.
2. State what variables should move, for whom, in what direction, and under what conditions.
3. Distinguish sharp predictions from qualitative predictions.
4. Identify competing explanations the model is meant to rule out.
5. Suggest data requirements and empirical tests.
6. State what evidence would not distinguish the model from alternatives.

Rules:
- Do not claim the model is empirically validated.
- Do not invent data or results.
- Keep welfare, policy, or asset-pricing implications conditional on the model.
```

Sources and workflow influences: the repository author's `economic-model-discussant` skill, seminar discussant practice, and theory-proof guardrails for economics and finance.
