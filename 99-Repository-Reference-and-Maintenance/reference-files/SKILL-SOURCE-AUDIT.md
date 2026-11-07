# External Skill Source, License, and Deduplication Audit

Use this ledger before importing, adapting, linking, replacing, or rejecting an external skill. It records decisions, not endorsements or rankings.

## Decision Rules

See the latest [2026-11-07 incremental audit](#2026-11-07-incremental-methods-audit).


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

## 2026-11-07 Incremental Methods Audit

Checked 2026-11-07, Europe/London (UTC). Last successful recorded run: 2026-11-05 07:43:12 UTC; source history queries overlap by 30 minutes. The scheduler's November 6 execution timestamp has no corresponding successful-run record, so it is not used to skip evidence. Clean worktree, fetched `origin/main` at `2e1f2a1b2a22b7ab97da4c26af22650ef952ac3e`. This branch starts directly from that baseline; open draft PRs [#4](https://github.com/SuperJayLiu/AI-for-Economics-and-Finance-Research/pull/4), [#5](https://github.com/SuperJayLiu/AI-for-Economics-and-Finance-Research/pull/5), [#6](https://github.com/SuperJayLiu/AI-for-Economics-and-Finance-Research/pull/6) were inspected for semantic deduplication, not imported.

### Decisions, Evidence, and Rights

| Candidate and primary evidence | Date / maintenance | Semantic comparison and decision | Rights and safety |
| --- | --- | --- | --- |
| DoubleML team, Philipp Bach/Sven Klaassen maintainers; [#452, fit storage lifecycle](https://github.com/DoubleML/doubleml-for-py/pull/452), merge `a3493c3b7a444b6ddd730ad05c2c0e6c67ac19c3` | Merged 2026-11-06 12:18:03 UTC; official active project, identity confirmed in pinned README; final production/test diff inspected | **UPDATE + LINK; no ADD.** Existing 03 Skill 3 and packaged ref 05 already take code/method/output evidence and return mismatch tables. Add artifact-to-fit identity, independent storage flags, and explicit failure of dependent diagnostics when current predictions are absent. PR #6 covers tuning state; this is the separate lifecycle of persisted predictions/targets/models after refit | [Pinned BSD-3-Clause](https://github.com/DoubleML/doubleml-for-py/blob/a3493c3b7a444b6ddd730ad05c2c0e6c67ac19c3/LICENSE). Original checks only; no upstream prose/code/tests/fixtures/structure copied, installed, or executed. Final diff adds clearer missing-storage error despite earlier body wording; no affected release range or installed-release guarantee asserted |
| Same team; [#450, sensitivity fallback centering](https://github.com/DoubleML/doubleml-for-py/pull/450), merge `aadcbcd1daeb90c14a865a5bec93a6358fe9a1c9` | Merged 2026-11-06 12:17:47 UTC; final production/test diff inspected | **UPDATE + LINK; no ADD.** Same trigger/input/output contract in 03/ref 05; adds fallback-specific influence centering by repetition/treatment and separates bound uncertainty from coefficient/nu2/maximum-bias point quantities. Prior reduced-control benchmark and tuning audits do not cover this inference branch | Same BSD license verified at inspected revision. Original adaptation; no expression/code/tests/assets copied or executed. Non-orthogonal fallback is not repaired identification; bound-SE change is not a coefficient correction. Applied results not certified |
| Manish Jha, Georgia State University; [author homepage](https://mjha91.github.io/), [AI for Finance Research](https://mjha91.github.io/pdf/AIFinanceResearch.pdf), [Text Data in Finance](https://mjha91.github.io/pdf/TextDataFinance.pdf) | Fresh downloads on 2026-11-07; identical SHA-256 to successful November 3–5 records: AI `cf031ca34fcb6756a43292002ba507365ddfcb6e8780bc52c130055e3051be03`; text `1f3455ec5839f8208b886c99e4d71bef6e5bb1affa9b5229b11e7e1b0848b4bd`. Both HTTP Last-Modified November 2; no new revision established | **LINK + DO NOT COPY; no repeated UPDATE.** PR #4 already covers plan/review/execute/verify, independent review, diff/sample/merge checks, item logs, finance agent instructions, eight-area LLM paper audit, look-ahead/memorization, human-label/benchmark/stress validation, and prediction/description/causality boundaries across 03/05/08/09/13/15/17 | No explicit reuse license established. No slide words, figures, templates, assets, or substantial structure copied, committed, or uploaded. This run only rechecks and links; prior page-level attribution remains in PR #4 |
| DoubleML [#435, DID sensitivity benchmark](https://github.com/DoubleML/doubleml-for-py/pull/435), merge `ab24f4da3e5b77649c15fa953ee8255269839970`; [#443, vector covariate flag](https://github.com/DoubleML/doubleml-for-py/pull/443), merge `b7d4a03474d8da295972443c08fe38f2297c7c3e` | Merged November 5 at 19:37:49 / 19:45:49 UTC; official PR bodies and file patches screened | **LINK; no separate UPDATE.** #435 overlaps PR #5's intended reduced-control refit/reference verification. #443 concerns a different requested-control-set realization and explicitly only the unreleased vector API; existing code/specification and control-list checks suffice | Same project BSD license; no source material copied/executed. No claim that released legacy estimates have this vector issue |

### Other Discovery and Coverage Limits

- Official default-branch histories since 2026-11-05 07:13:12 UTC: DoubleML Python seven commits (no next page); DoubleML R, rdrobust, fixest, QuantEcon Python lectures zero. This bounds the monitored channels, not all research or release channels. **LINK/no repeated UPDATE** for unchanged projects; no copied material or new rights inferred.
- [AEA policy](https://www.aeaweb.org/journals/data/data-code-policy) still identifies its policy version as February 2026; no in-window substantive update established. **LINK + DO NOT COPY**, no new adaptation or copied policy content. Existing replication intake in PR #4 covers it.
- [NBER papers](https://www.nber.org/papers) was reachable through direct HTTP but did not establish an in-window reusable methods candidate; browser retrieval returned 403. [November 13 AI/finance conference announcement](https://www.nber.org/calls-papers-and-proposals/big-data-artificial-intelligence-and-financial-economics) is an event, not evidence of a newly released method. **LINK + DO NOT COPY**, discovery only; coverage incomplete, no claim of no new NBER methods.
- Primary arXiv econ.EM/stat.ME recent listings screened for discovery, not quality or reuse evidence. Bhattacharya/Makiranta [Discrete Choice under Congestion](https://arxiv.org/abs/2611.07787v1), submitted November 5 10:27:17 UTC, and Bhattacharya/Martin [Unobserved Consideration and Consumer Welfare](https://arxiv.org/abs/2611.07774v1), submitted 10:12:26 UTC, remain **LINK + DO NOT COPY/watchlist** pending full assumption, author-identity, rights, and implementation review. Abstract screening is insufficient to adopt a welfare recipe. Habibnia/Maasoumi/Shah [Panel DML](https://arxiv.org/abs/2611.07249v1), submitted November 4 23:57:32 UTC, precedes cutoff; **LINK + DO NOT COPY**, no in-window update established. No paper material copied or method imported; unverified rights are not treated as permission.

### Acceptance and Boundaries

No new page, trigger family, project dependencies, or candidate-source installation/execution. Existing 03/ref 05 now specify required evidence, steps, an evidence-table output, missing-input/failure boundaries, and matched verification. English/Chinese discovery, root/package routers, sources, standards, and changelog synchronized. Exact destination pages include full author/title/URL/rights/influence/exclusion/date attribution.

Manual contract cases: (1) stored fit then nonstored refit must invalidate old artifacts; (2) predictions on/models off must be checked independently; (3) fallback warning requires per-repetition/treatment centering and separate bound-SE review; (4) an ordinary regression without DML history is a near-miss, so no forced fallback audit; (5) missing fit/fold/version evidence remains unverified; (6) a request to reuse old diagnostics or treat narrower bounds as identification must be rejected. These are desk checks, not model benchmarks or upstream software replication. Structural Markdown/index/router checks and diff checks are recorded in the run report.
