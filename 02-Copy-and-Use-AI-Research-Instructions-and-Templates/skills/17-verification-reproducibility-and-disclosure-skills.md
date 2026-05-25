> Copyright (c) 2026 SuperJayLiu (Chaojie Liu). Licensed under the repository MIT License.

# Verification, Reproducibility, and Disclosure Skills

Use these skills when you need to check AI-assisted work rather than merely warn yourself to "verify." Verification is a method, not a slogan.

> [!IMPORTANT]
> The right verification method depends on the object: citation, code, coefficient, proof, data merge, text measure, slide, or disclosure statement.

Questions or suggestions for this part: email [jay.liu@bristol.ac.uk](mailto:jay.liu@bristol.ac.uk) with subject `[AI Econ Finance Verification Skill] Suggestion`.

> [!NOTE]
> Default add-on for any block on this page: `If any required input, term, method detail, data rule, or output format is unclear, ask me up to five clarifying questions before giving the final output. Define unfamiliar technical terms in plain language and end with "Questions for you" if anything remains uncertain.`

## Choose a Skill

| Object to verify | Use |
| --- | --- |
| any AI output | Skill 1 |
| citation or literature claim | Skill 2 |
| code or data operation | Skill 3 |
| coefficient/result interpretation | Skill 4 |
| equation/proof/model claim | Skill 5 |
| AI-use reproducibility/disclosure | Skill 6 |

## Filled Mini Example

```text
AI output:
"The coefficient of 0.08 means treated firms increase investment by 8%."

Verification:
1. Check whether the dependent variable is log investment, investment/assets, or a percentage point measure.
2. Check the baseline mean.
3. Check whether the standard error and confidence interval support a precise estimate.
4. Check whether the design supports causal wording.
5. Compare the sentence to the table note and code.

Safer wording if dependent variable is log investment:
"The estimate implies an approximately 8 percent increase in investment under the maintained identification assumptions."

Bad output to reject:
"This proves the policy increased investment by 8%."
```

## Skill 1: Verification Method Selector

```text
Select the right verification method for this AI-assisted research output.

Output to verify:
[paste or describe]

Object type:
[citation/literature claim/code/data merge/table/figure/coefficient/equation/proof/slide/policy claim/LLM measure/other]

Project context:
- Field: [economics/finance subfield]
- Stakes: [notes/draft/submission/public talk/published paper]
- Data sensitivity: [public/licensed/restricted/confidential]
- What AI did: [summarized/wrote/edited/coded/measured/planned]

Return:
1. verification method;
2. exact evidence needed;
3. fastest low-cost check;
4. stronger check for submission quality;
5. stop conditions;
6. AI-use log entry.

Rules:
- Do not accept "looks plausible" as verification.
- If original sources, code, or data are needed, say exactly which ones.
- Separate low-stakes note checks from paper-submission checks.
```

## Skill 2: 30-Second Citation and Claim Check

```text
Check this citation or literature claim.

Claim:
[paste sentence]

Citation:
[citation, DOI, URL, BibTeX, or paper title]

Available evidence:
[abstract/notes/PDF excerpt/link]

Verify:
1. Does the source exist?
2. Are authors, year, title, journal/working-paper status, and DOI correct?
3. Does the source directly support the sentence?
4. Is the claim broader than the source?
5. Is there a correction, retraction, newer version, or relevant limitation?

Return:
- status: supported / partially supported / unsupported / cannot verify;
- safer wording;
- missing source information;
- what I should check manually.

Rules:
- Do not invent bibliographic fields.
- If you cannot access the original source, say so.
- Do not use a famous paper as support unless it supports this exact claim.
```

## Skill 3: Toy-Input Code Verification

```text
Verify this AI-written research code using a toy input with a known answer.

Code:
[paste]

Task:
[merge/variable construction/regression/table/figure/etc.]

Expected behavior:
[describe]

Software:
[Stata/R/Python/Matlab/SAS]

Create:
1. a minimal toy dataset;
2. expected output calculated by hand;
3. code to run the function/script on the toy data;
4. pass/fail criteria;
5. edge cases to test.

Return:
- toy data;
- expected output;
- test code;
- explanation of what the test catches;
- remaining risks after the test.

Rules:
- Include at least one edge case.
- Keep the toy data small enough to inspect by eye.
- Do not say the real analysis is verified unless the real pipeline also runs and outputs match expectations.
```

## Skill 4: Back-of-Envelope Coefficient and Magnitude Check

```text
Check whether this coefficient interpretation is numerically and economically plausible.

Result:
- Coefficient: [value]
- Standard error or CI: [value]
- Outcome unit: [unit]
- Treatment/regressor unit: [unit]
- Variable transformations: [logs/percent/z-score/standardized/etc.]
- Sample mean or baseline: [value]
- Claimed interpretation: [paste]

Verify:
1. correct unit interpretation;
2. correct log/percent/semi-elasticity interpretation;
3. economic magnitude relative to baseline;
4. whether standard error/CI supports the language;
5. whether causal language is supported by design;
6. whether result is policy/investment relevant or overstated.

Return:
- correct plain-language interpretation;
- magnitude calculation;
- overclaiming risks;
- safer sentence;
- checks needed in table/code.
```

## Skill 5: Proof, Equation, and Model Verification

```text
Verify this equation, proof step, or model claim.

Text/equation/proof:
[paste]

Model context:
- Objective or proposition: [goal]
- Variables and parameters: [definitions]
- Assumptions: [assumptions]
- Equilibrium or solution concept: [if relevant]

Check:
1. notation consistency;
2. algebraic step validity;
3. boundary or limiting cases;
4. units/dimensions;
5. missing assumptions;
6. hidden inequality or regularity condition;
7. whether conclusion follows from premises.

Return:
- valid steps;
- questionable steps;
- missing assumptions;
- counterexample or edge case if any;
- corrected proof outline if possible.

Rules:
- Do not pretend a derivation is correct because it is elegant.
- If a step cannot be verified from supplied assumptions, mark it.
```

## Skill 6: AI Reproducibility Packet and Disclosure Draft

```text
Create an AI-use reproducibility packet and disclosure draft for this project.

Project:
- Paper/project title: [title]
- AI tools used: [ChatGPT/Claude/Codex/Claude Code/Copilot/etc.]
- Tasks AI helped with: [writing/code/lit review/text measurement/slides/etc.]
- Materials given to AI: [public/private/licensed/restricted?]
- Files touched: [files]
- Checks run: [checks]
- Human edits and decisions: [summary]
- Journal/conference/university policy: [known/unknown]

Produce:
1. AI-use log entry;
2. reproducibility fields to archive;
3. disclosure paragraph for paper/appendix if required;
4. coauthor note;
5. risks or missing policy checks.

Disclosure paragraph should state only true facts:
- tool/model used, if known;
- date or period of use;
- task categories;
- human responsibility and verification;
- no confidential data uploaded, if true;
- no AI authorship claim.

Rules:
- Do not over-disclose private details.
- Do not claim compliance with a policy unless supplied.
- If policy is unknown, write [CHECK POLICY].
```

## Minimal AI-Use Log Row

```text
Date:
Tool/model:
Task:
Input materials:
Files touched:
Output accepted:
Human edits:
Verification performed:
Remaining uncertainty:
Disclosure needed?:
Commit hash:
```

## Sources and Workflow Influences

This page draws on reproducible research norms, journal disclosure practice, AI-use logs, citation-audit workflows, toy-data testing, and model/proof verification habits in economics and finance.

Last checked: 2026-05-24
