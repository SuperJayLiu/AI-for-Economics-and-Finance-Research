# Verification, Reproducibility, And Disclosure

Use this whenever an AI output might enter research notes, code, slides, papers, or replies.

## Verification Methods

| Output | Check |
| --- | --- |
| citation | DOI, journal page, author/year/title, source supports claim |
| literature claim | claim-source bank and closest-paper check |
| code | toy-data known-answer test and real-output audit |
| coefficient | sign, unit, magnitude, sample, timing, denominator |
| method prose | compare to code, data construction, estimand, inference |
| proof/model | algebra, limiting cases, equilibrium logic, assumptions |
| data access | provider terms, institution rules, confidentiality |
| slides | claim-to-evidence mapping and public-sharing permission |

## Text Measurement and LLM Paper Review

Distinguish representation, score prediction, and subsequent economic analysis. Require a construct rubric, adjudicated human labels, a held-out evaluation sample, distribution/subgroup diagnostics, sensitivity checks, and competing measures. Separate future information in inputs from memorized training targets; document unknown cutoffs and the information lost through anonymization. Model release dates and open weights do not establish a training cutoff or causal validity.

For a paper audit, return `claim | evidence location | finding | missing check | researcher responsible` across model, prompt, information boundary, human validation, benchmarks, construct, reproducibility, and economic magnitude. Do not certify unobserved checks. Use the handbook's [text measurement workflows](https://github.com/SuperJayLiu/AI-for-Economics-and-Finance-Research/blob/main/02-Copy-and-Use-AI-Research-Instructions-and-Templates/skills/15-text-as-data-and-llm-measurement-skills.md) and [LLM paper audit](https://github.com/SuperJayLiu/AI-for-Economics-and-Finance-Research/blob/main/02-Copy-and-Use-AI-Research-Instructions-and-Templates/skills/17-verification-reproducibility-and-disclosure-skills.md#llm-paper-evidence-audit) for full contracts. For batch execution, load `07-coding-data-stata-r-python.md`.

## Copy-Ready Instruction

```text
Act as a verification and AI-use disclosure assistant for economics and finance research.

First ask what output needs verification, how it will be used, and what original sources, code, data, tables, policies, or materials are available.

Classify the output type. Identify the main risks. Give the minimum verification method. State acceptance, revision, or rejection criteria. Draft an AI-use log entry and disclosure note if needed.

Do not claim something is verified unless the relevant source, code, data, or policy has been checked.
```

## AI-Use Log Fields

- date;
- tool/model if known;
- task;
- inputs used;
- output accepted;
- human edits;
- files changed;
- checks run;
- remaining uncertainty;
- commit hash if relevant.

## Sources and Workflow Influences

Manish Jha, Georgia State University, [AI for Finance Research](https://mjha91.github.io/pdf/AIFinanceResearch.pdf), cover 2026-10-30, and [Text Data in Finance](https://mjha91.github.io/pdf/TextDataFinance.pdf), undated; accessed 2026-11-03. Influences: LLM audit scope, construct diagnostics, contamination risks, and prediction/analysis boundaries. No explicit reuse license found on author page/PDFs. Original high-level adaptations and links only; no lecture text, prompts, templates, figures, or extended slide structure copied. Sources remain outside the repository MIT license.
