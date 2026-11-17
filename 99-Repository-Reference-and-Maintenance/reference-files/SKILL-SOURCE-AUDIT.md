# External Skill Source, License, and Deduplication Audit

Use this ledger before importing, adapting, linking, replacing, or rejecting an external skill. It records decisions, not endorsements or rankings.

## Decision Rules

- **ADD** only when the capability is missing from the active skill map.
- **UPDATE** when a candidate supplies a stronger workflow pattern for an existing page.
- **LINK** when the implementation is useful but platform-specific, too broad, overlapping, or not licensed for copying.
- **DO NOT COPY** when the repository has no clear license; public visibility is not reuse permission.
- Compare semantics—trigger, inputs, procedure, outputs, risks, and verification—not only names.
- Inspect files, scripts, dependencies, permissions, network calls, secret handling, and install steps before execution.

## 2026-11-17 Incremental Methods Audit

Clean worktree; fetched origin/main `2e1f2a1b2a22b7ab97da4c26af22650ef952ac3e`; new dated branch directly from main. Source-history window starts 2026-11-16 21:46:45 UTC (30-minute overlap before last successful completion). Pending #4–11 remain open drafts and were deduplicated, not imported. All checks dated 2026-11-17. Bounded source scan, not exhaustive literature/release coverage.

### Adopted Source, Rights and Semantic Comparison

Sebastian Calonico, Matias D. Cattaneo, Max H. Farrell and Rocio Titiunik / rdpackages, maintainer Calonico verified in [pinned R DESCRIPTION](https://github.com/rdpackages/rdrobust/blob/ddf48c41871cb44913a45aa540c761d5c5472118/R/rdrobust/DESCRIPTION); contributor GitHub account `soodoku`: [rdrobust PR #28](https://github.com/rdpackages/rdrobust/pull/28), merged 2026-11-17 04:07:16 UTC, revision `ddf48c41871cb44913a45aa540c761d5c5472118`; [pinned changelog](https://github.com/rdpackages/rdrobust/blob/ddf48c41871cb44913a45aa540c761d5c5472118/CHANGELOG.md). Checked 2026-11-17: all four final changed files inspected, with surrounding selector/estimator code and complete invariance test file. DESCRIPTION declares GPL-3. **UPDATE + LINK**, no ADD: original workflow for paired input permutations, distinct-support floors, selection/estimation decomposition and interpretation stop rules. No upstream code, tests, datasets, prose or extended structure copied or executed. Upstream test assertions inspected, not independently reproduced; merged source is not certification of a released package. The repository MIT license does not relicense the linked source.

Existing 03 and packaged reference 05 already accept design/code/output inputs and return methods/inference checks. Pending #4 adds general RD version checks; #8–9 address RDFlex asymmetric windows, weights and input shape. None specifies paired row permutations across all auxiliary inputs, distinct-support bandwidth floors and selected-versus-fixed estimation/bias bandwidth decomposition. Same trigger family and output ledger: **UPDATE**, no ADD. Procedure gains a concrete verification contract and a stop boundary for unexplained order dependence; page and package attribution supplied. Navigation, routes, sources, standards and changelog synchronized.

Security/maintenance: active official project, merged patch; read-only source inspection only. No external code, fixtures, dependencies or datasets executed/installed/imported. AI-assistance disclosure in the PR is not correctness evidence. New upstream tests directly cover hc1/hc3 with masspoints off and explicit bwcheck; do not claim exhaustive option-grid verification or local upstream suite success.

### Other Screened Sources and Decisions

| Primary source | Date, rights and observed scope | Decision / reason |
| --- | --- | --- |
| Manish Jha, Georgia State University, [AI for Finance Research](https://mjha91.github.io/pdf/AIFinanceResearch.pdf) and [Text Data in Finance](https://mjha91.github.io/pdf/TextDataFinance.pdf), linked by [author site](https://mjha91.github.io/) | Homepage and both PDFs byte-identical to last run; Last-Modified November 2. AI cover October 30; text lecture undated. No explicit reuse permission established. | **LINK + DO NOT COPY**; requested plan/review/execute, independent review, diff/sample/merge, batch ledger, agent instructions, eight-area LLM audit, leakage/memorization, construct validation and text-analysis boundaries already in pending #4. No slides, wording, prompts, figures, templates or extended structure copied; no new page/update. |
| [DoubleML Python #462](https://github.com/DoubleML/doubleml-for-py/pull/462) | Merged November 17; one-file final patch inspected, zero-signal policy-tree labels. Prior project BSD-3-Clause record not freshly license-pinned for this candidate. | **LINK**, no adoption; broader policy-value/evaluation and zero-weight semantics require deeper audit; no source copied/executed. |
| [DoubleML R #238](https://github.com/DoubleML/doubleml-for-r/pull/238), history also names #221 | November 17; final two-file #238 patch inspected: SSM fold-specific parameters, learner task type and formerly skipped test. #221 PR API returned 404 despite commit message. Prior MIT record not freshly pinned. | **LINK**, no adoption; fold/learner delivery overlaps #6–7; scope and merge/history discrepancy require follow-up before specialized guidance. No full applied-validation claim. |
| [QuantEcon Kesten-process commit](https://github.com/QuantEcon/lecture-python.myst/commit/f3d1a4ad4638f66e9d7d567789688d8eacf7bdc7) | November 17; full one-file patch changes installation to avoid upgrading jax. Prior lecture CC BY-SA 4.0, not a blanket MIT license. | **LINK + DO NOT COPY**; existing environment-preservation gate covers it; no new method. Nothing installed/copied. |
| [AEA policy](https://www.aeaweb.org/journals/data/data-code-policy) | Visible policy remains February 2026; no substantive dated change established. Copyright retained, not blanket reuse. | **LINK + DO NOT COPY**; existing/pending replication intake covers scope. |
| [NBER papers](https://www.nber.org/papers), [econ.EM](https://arxiv.org/list/econ.EM/recent?show=100), [stat.ME](https://arxiv.org/list/stat.ME/recent?show=100) | NBER web 403, direct HTTP succeeds but listing dynamic; arXiv bounded first pages. Listing dates may differ from submission dates. Paper-specific rights required. | **LINK + DO NOT COPY** screening only; no method adopted from titles/abstracts. NBER discovery incomplete. |
| [Farahat, AI-labeled treatments](https://arxiv.org/abs/2611.21207), [D’Haultfœuille, Hazard and Ketz, Never too LATE](https://arxiv.org/abs/2611.21496) | Official v1 times November 16 15:01 and 17:59:49 UTC, before cutoff; abstracts/history only. No full author/proof/rights audit performed. | **LINK + DO NOT COPY** watchlist, not newly published since last run despite newer daily listing. No adoption or replication claim. |

Official default-branch histories: DoubleML Python 1, R 2, rdrobust 1, fixest 0, QuantEcon 1, no next pages. Only adopted rdrobust underwent full scoped rights/context audit; other candidates remain bounded screening. No popularity/aggregator evidence used. Original report/metadata can be archived; no upstream lecture/code assets uploaded.

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
