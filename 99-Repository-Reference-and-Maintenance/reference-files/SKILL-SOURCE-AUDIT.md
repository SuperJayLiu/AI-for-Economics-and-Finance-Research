# External Skill Source, License, and Deduplication Audit

Use this ledger before importing, adapting, linking, replacing, or rejecting an external skill. It records decisions, not endorsements or rankings.

## Decision Rules

- **ADD** only when the capability is missing from the active skill map.
- **UPDATE** when a candidate supplies a stronger workflow pattern for an existing page.
- **LINK** when the implementation is useful but platform-specific, too broad, overlapping, or not licensed for copying.
- **DO NOT COPY** when the repository has no clear license; public visibility is not reuse permission.
- Compare semantics—trigger, inputs, procedure, outputs, risks, and verification—not only names.
- Inspect files, scripts, dependencies, permissions, network calls, secret handling, and install steps before execution.

## 2026-08-24 Audit

GitHub repository search and exact-file review were performed on 2026-08-24. Star counts and marketplace claims were treated only as discovery signals, never as quality evidence.

| Source | Maintainer / license at check | Distinct pattern found | Existing overlap | Decision and destination |
| --- | --- | --- | --- | --- |
| [OpenAI “Build skills”](https://developers.openai.com/codex/skills) | OpenAI / official documentation | focused jobs, progressive disclosure, concise trigger descriptions, optional scripts/references/assets, trigger tests | repo already uses skill blocks but lacked an intake/eval gate | **UPDATE** `09` Skill 7 and review standards |
| [`AlterLab-Academic-Skills`](https://github.com/AlterLab-IEU/AlterLab-Academic-Skills) | AlterLab / MIT | survey design, design-object-first survey analysis, preregistration/deviation gates, meta-analysis, positive and near-miss evals | ordinary literature review and econometrics existed; these four workflows did not | **ADD** `19` and `20`; **UPDATE** `09` eval pattern |
| [`scientific-agent-skills`](https://github.com/K-Dense-AI/scientific-agent-skills) | K-Dense Inc. / MIT | seeded experimental design, assignment/measurement boundaries, rival predictions, evidence ledgers, local deterministic validators | general research-question and literature skills existed; original-data design did not | **ADD/ADAPT** `19`; **LINK** scripts rather than copying domain-specific implementation |
| [`finai-research`](https://github.com/csmar432/finai-research) | CSMAR Data Center maintainers / MIT | data-source preflight, explicit fallback checkpoint, no silent simulated-data substitution, provenance log | `14` already had cleaning/merging but not acquisition governance | **UPDATE** `14` Skill 7; source-specific endpoints and credentials not copied |
| [`awesome-academic-skills`](https://github.com/O0000-code/awesome-academic-skills) | O0000-code / CC0-1.0 | research-lifecycle catalog with license and execution notes | resource database existed but lacked semantic dedup and trust gates | **UPDATE** `09` Skill 7 and this ledger |
| [`econometrics-skill`](https://github.com/xiaomihu1992/econometrics-skill) | xiaomihu1992 / MIT | estimator routing and applied code workflow | active `11`, `08`, and `14` already cover the same estimator families with stronger identification/verification boundaries | **LINK/NO ADD**; no duplicate estimator page |
| [`Awesome-Scientific-Skills`](https://github.com/InternScience/Awesome-Scientific-Skills) | InternScience / MIT | curated scientific-skill discovery | source index, not a unique economics workflow | **LINK/NO ADD**; useful for future discovery only |
| [`Auto-Empirical-Research-Skills`](https://github.com/brycewang-stanford/Auto-Empirical-Research-Skills) | CoPaper.AI / GitHub API returned `NOASSERTION` | very large empirical-social-science catalog | broad overlap with nearly every active family | **DO NOT COPY** without license clarification; discovery-only |
| [`EconAgentSkills`](https://github.com/JonasWeinert/EconAgentSkills) | Jonas Weinert / GitHub API returned `NOASSERTION` | DIME-oriented econometric workflow packaging | overlaps `08`, `11`, and `14` | **DO NOT COPY** without license clarification; existing pages cite DIME directly |
| [`stata-skill`](https://github.com/dylantmoore/stata-skill) | Dylan Moore / GitHub API returned `NOASSERTION` | broad Stata syntax/package coverage | overlaps the Stata assistant in `08` | **DO NOT COPY** without license clarification; possible external link after manual testing |
| [`Awesome-Journal-Skills`](https://github.com/brycewang-stanford/Awesome-Journal-Skills) | CoPaper.AI / MIT | journal-specific routing | overlaps writing, methods, referee, and disclosure skills; journal policies are time-sensitive | **TEST LATER**; do not add “fast track publication” claims without policy-by-policy verification |

## Accepted Change Map

| Active destination | What changed | Corresponding attribution |
| --- | --- | --- |
| `skills/09-tool-selection-updates-and-skill-improvement.md` | external-skill provenance, semantic dedup, trust inspection, license gate, trigger/non-trigger evals | OpenAI, O0000-code, AlterLab, K-Dense |
| `skills/11-causal-inference-econometrics-and-time-series-skills.md` | real-time vintages, forecast origins, pseudo-out-of-sample evaluation, benchmarks, leakage | ALFRED, Hyndman & Athanasopoulos, K-Dense, AlterLab |
| `skills/14-data-cleaning-merging-analysis-and-output-skills.md` | acquisition preflight, explicit fallback checkpoint, immutable raw data, provenance record | `finai-research`, DIME, SEC/FRED official docs |
| `skills/19-survey-experiment-and-preregistration-skills.md` | new original-data study-design family | DIME, K-Dense, AlterLab, COS, EGAP, AEA RCT Registry |
| `skills/20-systematic-review-and-meta-analysis-skills.md` | new systematic evidence-synthesis family | AlterLab, K-Dense, PRISMA, Cochrane, Campbell, Stanley & Doucouliagos |

## Next Audit Rule

For every future candidate, add one row here and add attribution in the exact skill page that changes. A central row without page-level attribution is incomplete; page-level attribution without a dedup decision is also incomplete.

## 2026-11-11 Incremental Methods Audit

Clean preflight; fetched origin/main `2e1f2a1b2a22b7ab97da4c26af22650ef952ac3e`; date branch created directly from it. Window starts at prior success 2026-11-10 22:16:13 UTC with 30-minute overlap. Pending draft PRs #4–8 were read for semantic deduplication, not imported. All sources accessed 2026-11-11. This is a bounded audit, not a systematic review.

### Accepted UPDATE + LINK

DoubleML team; maintainers Philipp Bach and Sven Klaassen; contributor `vrjdev`: [sample-weight routing PR #457](https://github.com/DoubleML/doubleml-for-py/pull/457), merged 2026-11-11 06:17:06 UTC, `09cd5d51dd8f06a54a9896e1b36a5f16a6d874a0`; [RD score-column validation PR #458](https://github.com/DoubleML/doubleml-for-py/pull/458), merged 2026-11-11 06:17:31 UTC, `919c09c01fc4a131ac93ae51ec6d1135cdb2dffb`. Titles: “fix: reject a Pipeline in the sample weight check unless metadata routing is enabled” and “fix: validate score_col when constructing DoubleMLRDDData.” [Pinned BSD-3-Clause license](https://github.com/DoubleML/doubleml-for-py/blob/919c09c01fc4a131ac93ae51ec6d1135cdb2dffb/LICENSE); identities checked in the pinned README. Checked 2026-11-11. Original workflow adaptation: trace nested weight delivery and configuration timing; verify loaded RD column identity and disjointness. No upstream code, tests, fixtures, prose, or structure copied or executed. Final patches and tests, rather than initial PR descriptions, ground this guidance. Merged source does not establish installed-release availability, complete wrapper coverage, or valid applied estimates.

Dedup: 03, 08, 11, 14 and packaged economics ref already cover methods, code, RD inputs and data checks. They do not explicitly require nested sample-weight request/delivery evidence, fit-time configuration rechecks, or revalidated loaded/mutable score-column identity and disjointness. Trigger and output remain methods review and its validation ledger, so UPDATE existing 03 and reference 05; no ADD. This differs from pending #8 final-bandwidth reporting and #5–7 fit/inference checks. Final #457 includes recursive wrapper checks and a pre-fit recheck despite its initial description's unresolved-wrapper note; final #458 includes setter disjointness despite its initial constructor-focused description. No complete wrapper coverage or transactional setter rollback is claimed.

### Other Candidate Decisions

| Source and identity | Date/maintenance and semantic decision | Rights, safety, and next action |
| --- | --- | --- |
| Manish Jha, Georgia State University, [AI for Finance Research](https://mjha91.github.io/pdf/AIFinanceResearch.pdf), [Text Data in Finance](https://mjha91.github.io/pdf/TextDataFinance.pdf), [author identity](https://mjha91.github.io/) | LINK + DO NOT COPY, no UPDATE. Fresh PDF hashes unchanged: AI `cf031ca34fcb6756a43292002ba507365ddfcb6e8780bc52c130055e3051be03`, text `1f3455ec5839f8208b886c99e4d71bef6e5bb1affa9b5229b11e7e1b0848b4bd`; Last-Modified November 2. AI cover October 30; text undated. Requested plan/review/execute/verify, independent review, diff/sample/merge evidence, batch logs, finance agent instructions, eight-area LLM audit, look-ahead/memorization, variable validation, and text-as-data boundaries already in pending #4 across 03/05/08/09/13/15/17 and packaged refs | No explicit reuse license established. Only original summaries and references; no slide wording, charts, templates, prompts, extended structure or lecture assets copied/uploaded. No new substantive update established |
| AEA [Data and Code Availability Policy](https://www.aeaweb.org/journals/data/data-code-policy) | LINK + DO NOT COPY; visible policy unchanged, still February 2026. Replication intake already in #4 | Copyright retained; no blanket reuse license. No policy text/forms copied |
| QuantEcon official lecture project, commits [f6d51df](https://github.com/QuantEcon/lecture-python.myst/commit/f6d51df8cca856e4978d6ca353efe90e84f6ed63), [82b7437](https://github.com/QuantEcon/lecture-python.myst/commit/82b74376f5b9d90793f74bd4ce81d9facb253c50), November 11 | LINK, no UPDATE: build/static-path and figure-caption/dependency maintenance, no verified new research method | No assets/code copied or executed; no new license clearance inferred from past lecture audits |
| Du/Escanciano/Pei, [Backtesting High-Dimensional Expected Shortfall](https://arxiv.org/abs/2611.13882v1); Chen/Ma/Yu, [Semiparametric Inference in Panel Data with Interactive and High-dimensional Confounding](https://arxiv.org/abs/2611.14385v1); Sargent/Sun/Zhang/Liu, [Prediction-Powered LLM Ranking with Adaptively Collected Human Feedback](https://arxiv.org/abs/2611.13186v1) | LINK + DO NOT COPY / queue. Primary version records: November 10 10:40:04, November 10 17:37:38, November 9 20:06:11 UTC respectively; all predate cutoff despite appearing on today's category list. No subsequent revision established. Existing 03/11/15 already route backtesting/panel inference/measurement validation; not accepted recipes | Abstract/version records only; full assumptions, author qualification and reuse rights not certified. No general reuse permission assumed, no paper expression/assets copied. Full audit required before adoption |
| [NBER papers](https://www.nber.org/papers) | LINK + DO NOT COPY, no accepted increment. Direct HTTP listing reached, browser 403; raw HTML changed only in script metadata; visible listing unchanged | No NBER full-text rights verified or expression redistributed; coverage incomplete |

Official default-branch histories: DoubleML Python two commits (above), QuantEcon two, DoubleML R/rdrobust/fixest zero, no next pages. arXiv econ.EM recent 39 entries and first stat.ME page (50 of 145) screened; not a full revision scan. No aggregator or popularity measure used as evidence.

Desk acceptance cases: disabled Pipeline routing must fail; enabled routing with unset requests remains unverified; a nested unsupported recipient cannot be inferred safe from **kwargs; intentional unweighted preprocessing must be recorded; configuration changed before fit must be rechecked; nonexistent or covariate-overlapping score columns must stop; ordinary RD without these objects routes to general design review. Manual contract checks only, no model benchmark or upstream test execution. Structural checks and final publication evidence are recorded in the run report.

Validation: 179 tracked Markdown files, 1,173 headings and 599 local links checked; zero introduced link/anchor/fence/duplicate issues. All 20 active skills indexed; git diff --check passed. The inherited Mini Case Card duplicate in unchanged examples README remains. No candidate installation, upstream execution, or applied-estimate certification.
