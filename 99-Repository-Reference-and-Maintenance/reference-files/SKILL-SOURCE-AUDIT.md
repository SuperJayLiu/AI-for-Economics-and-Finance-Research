# External Skill Source, License, and Deduplication Audit

Use this ledger before importing, adapting, linking, replacing, or rejecting an external skill. It records decisions, not endorsements or rankings.

## Decision Rules

- **ADD** only when the capability is missing from the active skill map.
- **UPDATE** when a candidate supplies a stronger workflow pattern for an existing page.
- **LINK** when the implementation is useful but platform-specific, too broad, overlapping, or not licensed for copying.
- **DO NOT COPY** when the repository has no clear license; public visibility is not reuse permission.
- Compare semantics—trigger, inputs, procedure, outputs, risks, and verification—not only names.
- Inspect files, scripts, dependencies, permissions, network calls, secret handling, and install steps before execution.

## 2026-11-25 Incremental Methods Audit

Clean preflight and fresh origin/main baseline `2e1f2a1b2a22b7ab97da4c26af22650ef952ac3e`. Run began November 24 and completed November 25 Europe/London; no schedule change. Window starts 2026-11-24 06:27:04 UTC (30-minute overlap). Pending draft PRs #4–15 and prior memory included in semantic deduplication, not imported. All following checks dated 2026-11-25 unless stated. Bounded audit, not a comprehensive publication census.

### Accepted Source and Semantic Decision

DoubleML official Python project, maintained by Philipp Bach and Sven Klaassen ([pinned README](https://github.com/DoubleML/doubleml-for-py/blob/50663c993d8056d3e75ca4c226fcdcdb555133c6/README.md)); contributor `vrjdev`, merged by Sven Klaassen: [scalar score scale checks, PR #467](https://github.com/DoubleML/doubleml-for-py/pull/467), merged 2026-11-24 15:30:18 UTC, revision `50663c993d8056d3e75ca4c226fcdcdb555133c6`. [BSD-3-Clause license](https://github.com/DoubleML/doubleml-for-py/blob/50663c993d8056d3e75ca4c226fcdcdb555133c6/LICENSE). Checked 2026-11-25: all five final patches, the full pinned linear-score estimator, scalar-PLR residual/score implementations and fit/tuning call sites, and added test cases. **UPDATE + LINK**: original adaptation of unit-rescaling, cancellation and treatment-residual verification. No upstream code, test fixtures, wording, figures, templates or extended structure copied; no upstream installation or tests executed. The PR explicitly concerns the unreleased scalar API, not a newly established bug in a released package. Source inspection and local score arithmetic do not certify package execution, identification or interval coverage.

Existing 03/08/11/17 cover method selection, debugging, DML assumptions and reproducibility. Pending #5 covers benchmark fit/refit artifacts; #10 rescales framework arithmetic and clustered uncertainty, not treatment-input units; #13 covers GATE group encoding. None specifies the generic signed-derivative guard versus PLR residual-to-treatment second-moment check, or the earlier IV-type initial-estimate/tuning divisions. Same trigger family and empirical audit output, stronger numerical failure boundaries: **UPDATE**, no ADD. Update 03 and packaged reference 05 plus navigation, routes and acceptance standards. Do not bypass numerical errors or claim adequate identifying variation from threshold passage. Official actively maintained repository, merged SHA, maintainer identity and BSD-3-Clause verified. No external agents, scripts, installs or datasets executed; upstream code/tests remain linked assets.

### Other Candidates and Rights Decisions

| Source | Evidence, rights and limits | Decision and semantic comparison |
| --- | --- | --- |
| Manish Jha, Georgia State University: [author site](https://mjha91.github.io/), [AI for Finance Research](https://mjha91.github.io/pdf/AIFinanceResearch.pdf), [Text Data in Finance](https://mjha91.github.io/pdf/TextDataFinance.pdf) | Own-site affiliation and original PDF bytes checked November 24. AI SHA-256 `cf031ca34fcb6756a43292002ba507365ddfcb6e8780bc52c130055e3051be03`, Text `1f3455ec5839f8208b886c99e4d71bef6e5bb1affa9b5229b11e7e1b0848b4bd`, unchanged. Last-Modified November 20 17:10:58 GMT is not a substantive revision date; AI cover October 30, Text undated. No explicit reuse license established. | **LINK + DO NOT COPY**. Pending #4 already covers plan-review-execute-verify, independent review, diff/sample/merge checks, scripted item logs, finance agent instructions, eight-part LLM audit, look-ahead/memorization, measurement validation and representation/prediction/description/causal boundaries in 03/05/08/09/13/15/17 and measurement references. No lecture text, figures, templates or extended structure copied; no new Jha adaptation in this change. |
| DoubleML [from-arrays treatment finite-check #472](https://github.com/DoubleML/doubleml-for-py/pull/472) | Two final patches read; merged commit `692499f5b9823fa14121faed1986e4c4b5874d11` November 24. Separate treatment versus covariate finite-input flags, constructor equivalence test. BSD-3-Clause project; full input path not audited/executed. | **LINK**, existing role-specific missingness/data validation overlaps; no second operational protocol adopted. |
| QuantEcon [environment channel correction #1142](https://github.com/QuantEcon/lecture-python.myst/pull/1142) | Official history records November 25 `eb065995c24253382613b4e3e45ff3ee97a3dcf3`; metadata only. Channel-name correction, not a new research method. No item-specific license audit. | **LINK + DO NOT COPY**, existing environment reproducibility covers capability; no code or installation imported. |
| [DoubleML R](https://github.com/DoubleML/doubleml-for-r), [rdrobust](https://github.com/rdpackages/rdrobust), [fixest](https://github.com/lrberge/fixest) | Official default-branch commit queries returned zero in bounded window, no next-page headers. No claim about every release/branch channel. | **LINK**, no established increment; prior changes already pending. |
| AEA [Data and Code Availability Policy](https://www.aeaweb.org/journals/data/data-code-policy) | Still explicitly February 2026. Copyright retained; policy adaptation allowance is not a blanket license to assets. | **LINK + DO NOT COPY**, replication/disclosure protocol already covered; no new policy adopted. |
| Graham, Harvey and Jha, NBER [CFOs Meet LLMs w36057](https://www.nber.org/papers/w36057); Galiani, López and Sosa, [AI Agents and Prompt Engineering in Econometric Coding w35588](https://www.nber.org/papers/w35588) | Official NBER listing/search author/title evidence; w35588 direct HTML obtained, revision month November but precise in-window day unverified. Browser item retrieval returned 403. Full methods, revision delta and reuse rights unverified. | **LINK + DO NOT COPY** watchlist. Synthetic survey measurement and agent validation overlap existing capabilities; abstracts do not establish a new procedure. No aggregate-source evidence adopted. |
| arXiv [econ new](https://arxiv.org/list/econ/new), [stat.ME new](https://arxiv.org/list/stat.ME/new) | Current listings fetched; title discovery only. Full papers, author identity, exact revision delta and item-specific licenses not comprehensively audited. | **LINK + DO NOT COPY**, no operational method adoption. |

Only #467 passed the complete adoption gate. General licenses are not inferred for other sources; no restricted data, source PDFs, source code or credentials redistributed. Original prose and source metadata only.

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
