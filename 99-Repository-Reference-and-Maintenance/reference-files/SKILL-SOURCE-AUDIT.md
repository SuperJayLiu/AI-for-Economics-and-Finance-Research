# External Skill Source, License, and Deduplication Audit

Use this ledger before importing, adapting, linking, replacing, or rejecting an external skill. It records decisions, not endorsements or rankings.

## Decision Rules

- **ADD** only when the capability is missing from the active skill map.
- **UPDATE** when a candidate supplies a stronger workflow pattern for an existing page.
- **LINK** when the implementation is useful but platform-specific, too broad, overlapping, or not licensed for copying.
- **DO NOT COPY** when the repository has no clear license; public visibility is not reuse permission.
- Compare semantics—trigger, inputs, procedure, outputs, risks, and verification—not only names.
- Inspect files, scripts, dependencies, permissions, network calls, secret handling, and install steps before execution.

## 2026-11-20 Incremental Methods Audit

Clean preflight; fetched origin/main `2e1f2a1b2a22b7ab97da4c26af22650ef952ac3e`; dated branch directly from main. Actual execution November 20 morning Europe/London, not a claim of November 19 22:05 execution. Source window starts November 18 21:44:29 UTC (30-minute overlap before last successful completion). Pending #4–13 remain open and are included in semantic deduplication, not imported. All checks dated 2026-11-20; bounded audit, not an exhaustive literature review.

### Adopted Source and Deduplication

Laurent Berge / official fixest project; contributor GitHub account `Don-Yin`: [Fix clustered Kleibergen-Paap test when scores and coefficients differ in size, PR #709](https://github.com/lrberge/fixest/pull/709), merged 2026-11-20 02:18:09 UTC at `a4fa1af45b984a1a23f660c0200dff353e957a50`. Author/maintainer and GPL-3 verified in [pinned DESCRIPTION](https://github.com/lrberge/fixest/blob/a4fa1af45b984a1a23f660c0200dff353e957a50/DESCRIPTION). Checked 2026-11-20: all six final file patches, full `kp_stat`/`proj_on_U`, clustered covariance context and the relevant test block inspected. **UPDATE + LINK**: original workflow adaptation of diagnostic normalization, dimension, weight and covariance checks; no upstream code, test fixtures, prose, figures or extended structure copied or executed. GPL-3 governs upstream assets; linking does not relicense them. The API/final merge revision is authoritative here; cached web PR text still shows the earlier open state. Upstream tests contain selected robust/clustered statistic comparisons and a singularity case; comments reporting Stata verification are not our independent execution. Weighted/IID/p-value changes were inspected in code, not independently numerically certified. No installed-release availability or universal numerical validity claimed.

Existing 03 requests weak-IV diagnostics and 11 routes IV identification/inference. Pending #11 concerns weighted IV R-squared/Sargan; #10 concerns DoubleML cluster arithmetic. Their triggers/inputs overlap this candidate, but none prescribes KP score/coefficient dimension checks, first-stage correction provenance or the divided-statistic/undivided-quadratic p-value distinction. Same output family: **UPDATE**, no ADD. Added an evidence ledger and stop boundaries in 03 and packaged reference 05, with page-level attribution and synchronized discovery/maintenance. No generic weak-IV threshold or new inference theorem imported.

Maintenance/security: active official project, merged source verified through live GitHub API and pinned raw files; no external code, dependencies, agents, data or install instructions executed. Cached web PR state was stale; live API merged_at/SHA and raw final code used. Upstream assertions are not our test run; no applied replication or installed-version guarantee.

### Other Candidates and Rights Decisions

| Source | Review and rights at 2026-11-20 | Decision and semantic reason |
| --- | --- | --- |
| Manish Jha, Georgia State University: [author site](https://mjha91.github.io/), [AI for Finance Research](https://mjha91.github.io/pdf/AIFinanceResearch.pdf), [Text Data in Finance](https://mjha91.github.io/pdf/TextDataFinance.pdf) | Site updates conference/news and paper links; both lecture bytes remain identical to first/prior audit. HTTP Last-Modified November 20 is deployment evidence, not lecture revision. AI cover previously verified October 30; text lecture undated. No explicit lecture reuse license established. | **LINK + DO NOT COPY**. Requested plan/review/execute/verify, fresh review, diff/sample/merge, scripted item ledgers, finance agent instructions, eight-area LLM audit, look-ahead/memorization, construct validation and text-analysis boundaries already in pending #4 for 03/05/08/09/13/15/17 and text/LLM workflows. No lecture wording, figures, templates or extended structure copied/uploaded. |
| John R. Graham, Campbell R. Harvey, Manish Jha, [CFOs Meet LLMs](https://arxiv.org/abs/2606.13812); new author-site [NBER link w36057](https://www.nber.org/papers/w36057) | Author-site link is new; arXiv v3 last revised November 15, before cutoff. Abstract/history inspected, not full paper or assets. NBER web retrieval unavailable; no fresh substantive revision established. Item-specific arXiv license link exists; not used as permission to copy and not freshly resolved. | **LINK + DO NOT COPY** monitoring. No new method adopted merely from a new link or abstract; pending measurement/look-ahead checks already apply. |
| Laurent Berge / fixest [logical model matrix #710](https://github.com/lrberge/fixest/pull/710) | Merged November 20 03:15:35 UTC; one final patch inspected, GPL-3 package. Converts logical alongside integer matrices; no test added in this diff. | **LINK**, no ADD: general encoding verification exists, pending #13 already targets dtype equivalence (different package). No fixest-specific result claim without tests. Other model.matrix commit screened by title and related #709 context only. |
| [DoubleML Python](https://github.com/DoubleML/doubleml-for-py), [DoubleML R](https://github.com/DoubleML/doubleml-for-r), [rdrobust](https://github.com/rdpackages/rdrobust) | Official default-branch history returns zero commits in window, no pagination. Previously verified BSD/GPL provenance not a fresh license audit of every asset. | **LINK** monitoring; no newly verified increment or adoption. |
| QuantEcon / [lecture build stack #1135](https://github.com/QuantEcon/lecture-python.myst/commit/6071051dfe42e75bbecb0682bfc65daf4dc8f60d), font cache #1134 | November 19; history/title screening only. Build/version pinning overlaps existing reproducibility. Item-specific reuse not freshly verified; lecture rights must not be conflated with code rights. | **LINK + DO NOT COPY**; no substantive method increment established. Information-geometry full-method audit from prior run remains pending. |
| [AEA Data and Code Availability Policy](https://www.aeaweb.org/journals/data/data-code-policy) | Visible text identical to prior run; prior version February 2026, institutional copyright retained. | **LINK + DO NOT COPY**; existing/pending replication intake covers it. |
| [NBER papers](https://www.nber.org/papers), [econ.EM recent](https://arxiv.org/list/econ.EM/recent?show=100), [stat.ME recent](https://arxiv.org/list/stat.ME/recent?show=100) | NBER direct visible page unchanged, web 403/dynamic discovery incomplete. Direct arXiv pages current through November 20: 42 economics, first 100 of 156 statistics entries available; title screen only, remaining 56 not inspected. Web cached economics listing stale, not used for freshness. No item-specific rights/full-proof audit of screened papers. | **LINK + DO NOT COPY** discovery only. Prioritize second-order orthogonality, fuzzy DiD and coding-agent selective inference for full source/assumption audits; titles do not justify recipes. |
| BIS, [MaRCo@BIS: AI-agentic econometric analysis for central bankers](https://www.bis.org/publications/working-paper-1395-marcobis-ai-agentic-econometric-analysis-central-bankers) | Official landing page discovery, dated November 12 (outside window); full paper/authorship/asset rights not audited in this run. | **LINK + DO NOT COPY** watchlist; no adoption from search excerpt. |

No popularity or aggregator evidence used. No upstream assets included in repository or Drive deliverables. Reuse restrictions above concern copying; all adopted prose is original adaptation.

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
