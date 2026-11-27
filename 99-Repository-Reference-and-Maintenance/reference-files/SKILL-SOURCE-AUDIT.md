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

## 2026-11-27 Incremental Methods Audit

Clean preflight; fresh origin/main `2e1f2a1b2a22b7ab97da4c26af22650ef952ac3e`. Window begins 2026-11-26 21:46 UTC (prior scan start minus 30 minutes). Pending draft PRs #4–16 included through memory, saved diffs and refreshed PR metadata; no earlier branch imported. Checks dated 2026-11-27. Bounded audit, not a publication census.

### Accepted Source and Semantic Decision

DoubleML official Python project, maintained by Philipp Bach and Sven Klaassen ([pinned README](https://github.com/DoubleML/doubleml-for-py/blob/baf9b87260e46f3d078dd187812ef797439d40ad/README.md)); contributor `vrjdev`, merged by Sven Klaassen: [PR #468, multi-way cluster fold comparison in scalar fit](https://github.com/DoubleML/doubleml-for-py/pull/468), merged 2026-11-27 13:01:44 UTC at `baf9b87260e46f3d078dd187812ef797439d40ad`. [Pinned BSD-3-Clause license](https://github.com/DoubleML/doubleml-for-py/blob/baf9b87260e46f3d078dd187812ef797439d40ad/LICENSE). Checked 2026-11-27: both final patches, scalar fit/draw/set splitting paths, reset hooks and four parametrized cluster test cases. **UPDATE + LINK**: original adaptation of split-preservation and refit acceptance checks. No upstream code, tests, fixtures, wording, figures, templates or extended structure copied; no upstream code installed or executed. This patch concerns the unreleased scalar API; it does not establish a released-package defect, valid cluster assignment, identification or confidence-interval coverage.

Existing 03/08/11/17 cover methods, split-aware verification and reproducibility. Pending #5 covers fit/refit artifacts; #10 concerns covariance under clustered framework arithmetic, not fold units; #16 concerns treatment scaling. They do not specify per-cluster versus product fold counts or repetition-only redraw acceptance. Same review trigger, input family and ledger output, with a stronger failure boundary: **UPDATE**, no ADD. Destination 03 and packaged reference 05; page-level attribution paired with this ledger. Source and tests inspected, no empirical coverage or package execution certified. Actively maintained official repository, merged revision and BSD-3-Clause verified; no external scripts, dependencies or models installed or executed.

### Other Candidates and Rights Decisions

| Source | Verification and decision | Semantic comparison / limits |
| --- | --- | --- |
| Manish Jha, Georgia State University: [author site](https://mjha91.github.io/), [AI for Finance Research](https://mjha91.github.io/pdf/AIFinanceResearch.pdf), [Text Data in Finance](https://mjha91.github.io/pdf/TextDataFinance.pdf) | Identity on author site and PDF bytes checked; SHA-256 AI `cf031ca34fcb6756a43292002ba507365ddfcb6e8780bc52c130055e3051be03`, Text `1f3455ec5839f8208b886c99e4d71bef6e5bb1affa9b5229b11e7e1b0848b4bd`, unchanged. Last-Modified November 20 is not a new substantive revision. No explicit reuse license established: **LINK + DO NOT COPY**. | Pending #4 already addresses plan/review/execute/verify, fresh independent review, diff/sample/merge checks, scripted item logs, finance agent instructions, eight-part LLM audit, look-ahead/memorization, measurement validation and representation/prediction/description/causal boundaries in 03/05/08/09/13/15/17 and measurement references. No new adaptation; no lecture text, figures, templates or extended structure copied. |
| DoubleML [#474](https://github.com/DoubleML/doubleml-for-py/pull/474), RDD/SSM array validation | Merged November 27; all three final patches read; project BSD-3-Clause, no execution. **LINK**. | Existing row alignment, role-specific finite-input and failure-state validation overlap; not a missing skill. Full constructor path not separately certified. |
| DoubleML [#475](https://github.com/DoubleML/doubleml-for-py/pull/475), policy-tree prediction feature order | Merged November 27; both final patches read; project BSD-3-Clause, no execution. **LINK**. | Fitted-schema versus incoming column order is useful concrete evidence, but existing data/code schema and prediction validation cover the capability; no second protocol adopted. |
| DoubleML [#476](https://github.com/DoubleML/doubleml-for-py/pull/476), sensitivity parameter name; [#418](https://github.com/DoubleML/doubleml-for-py/pull/418), metadata | November 27 merge metadata/body inspected; no item-specific full-file audit. **LINK + DO NOT COPY**. | Documentation/metadata updates do not establish a new operational research method. |
| [DoubleML R](https://github.com/DoubleML/doubleml-for-r), [rdrobust](https://github.com/rdpackages/rdrobust), [fixest](https://github.com/lrberge/fixest), [QuantEcon](https://github.com/QuantEcon/lecture-python.myst) | No default-branch commits returned in bounded window, no next-page headers. **LINK**. | No established new increment; not a statement about every branch or release channel. |
| AEA [Data and Code Availability Policy](https://www.aeaweb.org/journals/data/data-code-policy) and [FAQ](https://www.aeaweb.org/journals/data/faq) | Current official pages checked; policy version February 2026. No blanket asset reuse license inferred; **LINK + DO NOT COPY**. | Existing 05/17 replication and disclosure workflow covers the policy; depositor-specific licenses still govern assets. |
| NBER [w36044](https://www.nber.org/papers/w36044), Hoces de la Guardia, Miguel et al., missing results; [w36017](https://www.nber.org/papers/w36017), Schmieder, fereg | Official listing title/author discovery; item browser requests returned 403, exact in-window revision and full method/rights unverified. **LINK + DO NOT COPY**, watchlist. | Existing 20 preregistration/selection reporting and 08/11 estimator choice overlap at topic level; specific methods not declared redundant without full text. |
| Carlson/Dell [unstructured-data inference v4](https://arxiv.org/abs/2505.00282v4), and current [econ](https://arxiv.org/list/econ/new)/[stat.ME](https://arxiv.org/list/stat.ME/new) listings | v4 record last revised November 25, before window; prior audit recorded CC BY 4.0. Lists byte-identical to prior run, no new full-paper census. **LINK**, no copying. | MAR-S remains a potentially substantive earlier-window supplement; full version comparison and estimator assumptions pending. Do not infer causal validity from prediction accuracy. |

No source assets or credentials redistributed. Only original adaptation and source metadata included.
