# External Skill Source, License, and Deduplication Audit

Use this ledger before importing, adapting, linking, replacing, or rejecting an external skill. It records decisions, not endorsements or rankings.

## Decision Rules

- **ADD** only when the capability is missing from the active skill map.
- **UPDATE** when a candidate supplies a stronger workflow pattern for an existing page.
- **LINK** when the implementation is useful but platform-specific, too broad, overlapping, or not licensed for copying.
- **DO NOT COPY** when the repository has no clear license; public visibility is not reuse permission.
- Compare semantics—trigger, inputs, procedure, outputs, risks, and verification—not only names.
- Inspect files, scripts, dependencies, permissions, network calls, secret handling, and install steps before execution.

## 2026-11-23 Incremental Methods Audit

Clean preflight; fetched origin/main `2e1f2a1b2a22b7ab97da4c26af22650ef952ac3e`; dated branch directly from main. Actual run November 23 afternoon Europe/London; not a claim of 22:05 execution. Window starts November 20 08:42:08 UTC (30-minute overlap before last successful completion). Pending #4–14 diff additions and previous audit memory included in deduplication, not imported. Bounded source audit, not an exhaustive literature review. All checks dated 2026-11-23.

### Adopted Source and Semantic Comparison

Laurent Berge / official fixest project; contributor Kyle Butts (both identified in the [pinned DESCRIPTION](https://github.com/lrberge/fixest/blob/6371909a0249b19373f5923af44ce75792346e36/DESCRIPTION)): [fix predict() for IV models, PR #714](https://github.com/lrberge/fixest/pull/714), merged 2026-11-22 16:19:10 UTC at `6371909a0249b19373f5923af44ce75792346e36`. GPL-3 applies to upstream assets. Checked 2026-11-23: the complete single-file final patch, full pinned `predict.fixest` function and [prediction documentation](https://github.com/lrberge/fixest/blob/6371909a0249b19373f5923af44ce75792346e36/man/predict.fixest.Rd). **UPDATE + LINK**: original adaptation of input, coefficient-name and covariance-alignment verification. No upstream code, tests, wording, figures, templates or extended structure copied or executed. This PR adds no tests; inspection is not numerical certification or evidence of availability in an installed release. Existing no-newdata fast paths and restrictions on prediction uncertainty still require separate checks.

Existing 03/08/11/17 already route empirical methods, code debugging, IV assumptions and reproducibility. Pending #11 addresses weighted R-squared/Sargan, #14 KP normalization; #4 addresses general independent review/diff/sample checks. Same trigger family, inputs and output artifact; none specifies endogenous-only rename versus legitimate fit_ exogenous names, covariance-axis mapping, intercept-only prediction or the no-newdata fast-path distinction. **UPDATE**, no ADD. Strengthened 03 and packaged reference 05; synchronized discovery, routers and standards with page-level attribution. Stop on missing inputs/columns or unsupported uncertainty. Active official maintainer repository; final merged SHA and full function verified. No source code, agents, dependencies or data executed; no guarantee of release availability, universal numerical correctness or valid IV interval coverage.

### Other Candidates and Rights Decisions

| Source | Evidence and limits | Decision and deduplication |
| --- | --- | --- |
| Manish Jha, Georgia State University: [author site](https://mjha91.github.io/), [AI for Finance Research](https://mjha91.github.io/pdf/AIFinanceResearch.pdf), [Text Data in Finance](https://mjha91.github.io/pdf/TextDataFinance.pdf) | Author affiliation confirmed on site. Direct PDF bytes match prior audit: AI SHA-256 `cf031ca34fcb6756a43292002ba507365ddfcb6e8780bc52c130055e3051be03`; Text `1f3455ec5839f8208b886c99e4d71bef6e5bb1affa9b5229b11e7e1b0848b4bd`. Both Last-Modified November 20 17:10:58 GMT are deployment metadata, not content revisions. AI lecture cover previously dated October 30; Text undated. No explicit reuse license established. | **LINK + DO NOT COPY**. All requested plan/review/execute/verify, independent review, diff/sample/merge, scripted item logging, finance agent instructions, eight-part LLM audit, look-ahead/memorization, measurement validation and text-analysis boundaries already addressed in pending #4's 03/05/08/09/13/15/17 and packaged workflows. No lecture text, figures, templates or extended structure copied/uploaded. |
| Laurent Berge / Kyle Butts, fixest [Cook's distance and hatvalues #711](https://github.com/lrberge/fixest/pull/711) | Merged November 20 17:12:16 UTC, `7163096ac0661a26adc0c2019ba8eaebb9367abc`; all six patches read, including weighted leverage, quasi-family dispersion and reference tests. GPL-3 package. Full hatvalues/covariance call chain and numerical replication not audited. | **LINK** pending deeper review, no adoption. Existing diagnostic verification overlaps; leverage/HC2/HC3 implications merit a separate, bounded source audit. No upstream tests run or copied. |
| [DoubleML Python](https://github.com/DoubleML/doubleml-for-py), [DoubleML R](https://github.com/DoubleML/doubleml-for-r), [rdrobust](https://github.com/rdpackages/rdrobust) | Official default-branch history: zero commits in window, no next-page headers. No new item-specific license audit or change claim. | **LINK** monitoring; prior pending changes already cover latest verified increments. |
| QuantEcon / [information-projection lectures #1138](https://github.com/QuantEcon/lecture-python.myst/pull/1138) and follow-ups #1144/#1147 | Six history entries; #1138 metadata/body inspected (merged November 22), follow-ups title screening only. New time-series misspecification/specification-test/indirect-inference teaching candidate. Full derivations, numerical claims and item-specific rights not freshly verified. | **LINK + DO NOT COPY** until full methods/rights review. Existing time-series/verification routes overlap; no theorem, exercise, code or lecture structure imported. |
| AEA [Data and Code Availability Policy](https://www.aeaweb.org/journals/data/data-code-policy) | Official current policy page found; no in-window substantive update established. Policy is not a content reuse license. | **LINK + DO NOT COPY**; existing replication/disclosure coverage, no new rule adopted. |
| NBER [working papers](https://www.nber.org/papers), [Shrink Responsibly w36053](https://www.nber.org/papers/w36053), [missing research results w36044](https://www.nber.org/papers/w36044) | Official search/listing discovery and w36053 landing metadata only. Browser item retrieval failed; direct official w36053 HTML succeeded and confirms Peter Hull / Michal Kolesár, DOI 10.3386/w36053, publication November 23, 2026. Full methods and rights remain unverified; w36044 item not read. No abstract-level inference accepted as a method audit. | **LINK + DO NOT COPY**, deeper review deferred. Empirical Bayes and hypothesis-level reporting are watchlist topics, not adopted capabilities. |
| arXiv [econ new](https://arxiv.org/list/econ/new), [stat.ME recent](https://arxiv.org/list/stat.ME/recent) | November 23 econ 19 entries and first 50/147 recent stat.ME entries title-screened; author metadata visible. Not all papers read, identities independently checked or rights resolved; not an exhaustive window census. | **LINK + DO NOT COPY** discovery only; no high-confidence nonduplicative workflow adopted from these listings. |

No ADD decision passed. Repository changes concern only the fully inspected #714 source; unverified candidates remain outside operational instructions. External material was treated as evidence, not as executable instructions. No credentials, restricted data or upstream assets redistributed.

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
