> Copyright (c) 2026 SuperJayLiu (Chaojie Liu). Licensed under the repository MIT License.

# Text-as-Data and LLM Measurement Skills

Use these skills when text becomes data: filings, earnings calls, central-bank speeches, news, analyst reports, patents, job postings, social media, survey responses, or policy documents.

> [!WARNING]
> If an LLM produces a variable used in regressions, the LLM is part of the measurement instrument. Record the model, prompt, date, settings, input text, output schema, validation sample, and sensitivity checks.

Questions or suggestions for this part: email [jay.liu@bristol.ac.uk](mailto:jay.liu@bristol.ac.uk) with subject `[AI Econ Finance Text-as-Data Skill] Suggestion`.

> [!NOTE]
> Default add-on for any block on this page: `If any required input, term, method detail, data rule, or output format is unclear, ask me up to five clarifying questions before giving the final output. Define unfamiliar technical terms in plain language. After producing output, state what changed, what did not change, and what the researcher must verify. End with "Questions for you" if anything remains uncertain.`

## Choose a Skill

| Need | Use |
| --- | --- |
| turn text into an empirical variable | Skill 1 |
| build a human validation sample | Skill 2 |
| test prompt/model sensitivity | Skill 3 |
| prevent look-ahead and leakage in text measures | Skill 4 |
| document an LLM-generated variable for a paper | Skill 5 |

## Skill 1: LLM-as-Measurement Protocol

```text
Act as a text-as-data measurement designer for economics/finance research.

Project:
- Research question: [question]
- Text corpus: [10-Ks/earnings calls/news/speeches/job postings/etc.]
- Unit of analysis: [firm-year/document/paragraph/sentence/event/etc.]
- Outcome or downstream use: [regression/table/figure]
- Construct to measure: [sentiment/risk/disclosure tone/policy stance/attention/etc.]
- Time period: [period]
- Intended model/tool: [ChatGPT/Claude/local model/API/etc.]
- Confidentiality status: [public/licensed/restricted/confidential]

Design a measurement protocol with:
1. construct definition;
2. unit of text;
3. inclusion/exclusion rules;
4. label schema;
5. prompt template;
6. output JSON schema;
7. deterministic settings if available;
8. validation set;
9. human review procedure;
10. prompt/model sensitivity checks;
11. storage format for prompts, inputs, outputs, and model metadata.

Return:
- measurement protocol;
- copy-ready prompt;
- JSON output schema;
- validation checklist;
- disclosure paragraph skeleton.

Rules:
- Do not treat LLM labels as ground truth.
- Do not use future text to label past observations.
- Do not change the prompt after seeing regression results without logging it.
- Do not compare labels across model versions unless you test drift.
- If the corpus is licensed or confidential, recommend local or approved workflows.
```

## Skill 2: Human Validation Set Builder

```text
Help me design a human validation sample for an LLM-generated text measure.

Inputs:
- Construct: [construct]
- Corpus: [corpus]
- Unit of text: [document/paragraph/sentence/etc.]
- Number of observations: [N]
- Subgroups/time periods that matter: [groups]
- LLM label schema: [schema]
- Research use: [regression/descriptive measure/prediction/etc.]

Create:
1. sampling plan for validation examples;
2. coding guide for human labels;
3. disagreement resolution rule;
4. metrics to compare human and LLM labels;
5. minimum performance threshold before using the measure;
6. failure-mode list.

Return:
- validation-sample plan;
- human coder instructions;
- comparison table template;
- decision rule: use, revise, or reject the LLM measure.

Rules:
- Include difficult, borderline, and subgroup cases.
- Do not validate only on easy examples.
- Check whether error rates differ by firm type, industry, period, source, language, or document length.
```

## Skill 3: Prompt and Model Sensitivity Check

```text
Design a sensitivity analysis for an LLM-generated text variable.

Current setup:
- Model/tool: [model/tool]
- Prompt: [paste]
- Output variable: [variable]
- Corpus/sample: [sample]
- Downstream analysis: [regression/table/figure]

Create sensitivity tests for:
1. prompt wording;
2. label definitions;
3. output scale;
4. temperature or randomness settings, if controllable;
5. model version or provider;
6. text chunking or retrieval order;
7. repeated runs on the same text;
8. subgroup-specific error.

Return:
- test matrix;
- expected output comparison table;
- decision rule for acceptable stability;
- how to report instability in a paper;
- code/data fields to archive for reproducibility.

Rules:
- Do not choose the prompt based on which version gives the desired coefficient.
- Report meaningful sensitivity, not only the best-performing variant.
- Keep the original prompt and all tested variants in the AI-use log.
```

## Skill 4: Text-Measure Leakage and Look-Ahead Audit

```text
Audit this text-as-data design for leakage and look-ahead bias.

Project facts:
- Text source: [source]
- Text timestamp: [timestamp rule]
- Outcome timing: [timing]
- Predictor/treatment timing: [timing]
- LLM/model used: [model]
- Training/pretraining concern: [known/unknown]
- Regression design: [design]

Check:
1. whether text was available before the outcome period;
2. whether document timestamps reflect publication, filing, revision, or download date;
3. whether the LLM may use knowledge unavailable at the historical prediction time;
4. whether chunking includes future sections or later revisions;
5. whether labels are created after inspecting outcomes;
6. whether the prompt embeds outcome information;
7. whether repeated prompt tuning created p-hacking risk;
8. whether model-version drift affects comparability.

Return:
- leakage risks by severity;
- safer timing rule;
- audit fields to store;
- reporting language;
- checks to run before using the measure.
```

## Skill 5: Paper Methods Paragraph for LLM-Based Measurement

```text
Draft a methods paragraph for an LLM-generated text variable.

Inputs:
- Construct measured: [construct]
- Corpus and sample: [corpus/sample]
- Unit of text: [unit]
- Model/tool and version/date: [model/version/date]
- Prompt family: [summary]
- Output schema: [schema]
- Validation set: [details]
- Human validation results: [results]
- Sensitivity checks: [results]
- Limitations: [limitations]

Write:
1. a methods paragraph explaining how the variable was generated;
2. a validation paragraph;
3. a limitations paragraph;
4. a reproducibility note.

Rules:
- Do not imply the LLM directly observes the latent construct.
- Do not hide prompt/model sensitivity.
- Do not overclaim causal interpretation from a text measure.
- Mark missing information as [NEEDS AUTHOR INPUT].

Also return:
- data appendix checklist;
- AI-use log fields;
- disclosure sentence for the paper or appendix.
```

## Minimal Archive Fields for LLM-Generated Variables

```text
variable_name:
construct:
corpus_source:
document_id:
text_span_or_hash:
prompt_id:
prompt_text:
model_provider:
model_name:
model_version_or_snapshot:
run_date:
temperature_or_randomness_setting:
seed_if_available:
output_schema:
raw_output:
parsed_value:
human_validation_status:
notes:
commit_hash:
```

## Sources and Workflow Influences

This page draws on economics text-as-data practice, LLM measurement and reproducibility concerns, finance text sources such as filings and earnings calls, and the general principle that AI-generated variables must be validated like measurement instruments.

Last checked: 2026-05-24
