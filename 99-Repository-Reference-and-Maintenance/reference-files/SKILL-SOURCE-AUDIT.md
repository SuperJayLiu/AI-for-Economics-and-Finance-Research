# External Skill Source, License, and Deduplication Audit

Use this ledger before importing, adapting, linking, replacing, or rejecting an external skill. It records decisions, not endorsements or rankings.

## Decision Rules

- **ADD** only when the capability is missing from the active skill map.
- **UPDATE** when a candidate supplies a stronger workflow pattern for an existing page.
- **LINK** when the implementation is useful but platform-specific, too broad, overlapping, or not licensed for copying.
- **DO NOT COPY** when the repository has no clear license; public visibility is not reuse permission.
- Compare semantics—trigger, inputs, procedure, outputs, risks, and verification—not only names.
- Inspect files, scripts, dependencies, permissions, network calls, secret handling, and install steps before execution.

## 2026-11-18 Incremental Methods Audit

Clean preflight; fetched origin/main `2e1f2a1b2a22b7ab97da4c26af22650ef952ac3e`; dated branch created directly from main. Source-history window starts 2026-11-17 21:45:39 UTC (30-minute overlap before last successful completion). Pending #4–12 are still open drafts: deduplicated, not imported. All checks dated 2026-11-18; bounded source scan, not an exhaustive literature audit.

### Adopted Source, Rights and Semantic Comparison

DoubleML project / Philipp Bach, Victor Chernozhukov, Sven Klaassen, Malte S. Kurz and Martin Spindler (copyright holders in the [pinned BSD-3-Clause license](https://github.com/DoubleML/doubleml-for-py/blob/6dd568a85df45cd668301891e1a1ed57c68554b0/LICENSE)); contributor GitHub account `vrjdev`: [scalar PLR/IRM GATE input fix, PR #466](https://github.com/DoubleML/doubleml-for-py/pull/466), merged 2026-11-18 17:34:02 UTC, revision `6dd568a85df45cd668301891e1a1ed57c68554b0`. Checked 2026-11-18: all four final changed files, complete GATE functions and associated test files inspected. **UPDATE + LINK**, no ADD: original adaptation of encoding-invariance and schema verification to the existing methods audit. No upstream code, tests, fixtures, prose or extended structure copied or executed. The final patch uses NumPy dtype-kind checks, beyond the PR body's initial parentheses description. Tests compare bool/int64/int32/uint8 coefficients and standard errors and reject multi-column float/nullable Int64; these are inspected assertions, not local execution. The PR explicitly limits the bug to the unreleased scalar API; do not claim a released-package defect or a verified installed fix. Linked BSD terms remain applicable to upstream assets.

Existing 03 and packaged reference 05 already trigger on research design/code/output and return verification issues. Existing 11 covers causal identification; pending #6–7 concern tuning and fit artifacts, #10 clustered arithmetic/contrasts, #12 RD permutations. None specifies GATE group-table schema, nullable-versus-NumPy dtypes, category-versus-indicator semantics or identical-fit encoding invariance. Same input/output family: **UPDATE**, no ADD. Added concrete steps and stop boundaries within existing pages, with page-level attribution and synchronized routes/indexes/standards. A missing type check does not establish the source caused biased published estimates.

Maintenance/security: active official project and merged patch; authorship separated from contributor account. Read-only source inspection; no candidate code/dependencies/data installed or executed, no instructions from external files followed. No benchmark, upstream suite or applied-estimate replication claimed.

### Other Screened Sources and Decisions

| Source | Dates, rights and review scope | Decision / reason |
| --- | --- | --- |
| Manish Jha, Georgia State University, [AI for Finance Research](https://mjha91.github.io/pdf/AIFinanceResearch.pdf), [Text Data in Finance](https://mjha91.github.io/pdf/TextDataFinance.pdf), [author site](https://mjha91.github.io/) | Homepage/two PDFs byte-identical to prior run; HTTP Last-Modified November 2; AI cover October 30, text lecture undated. No explicit reuse license established. | **LINK + DO NOT COPY**: requested plan/review/execute/verify, independent review, diff/sample/merge, batch ledger, agent instructions, eight-area LLM audit, leakage/memorization, construct validation and text-analysis boundaries already covered by pending #4. No slides, wording, figures, prompts, templates or extended structure copied/uploaded. |
| Thomas J. Sargent / QuantEcon, [information-geometry lectures commit](https://github.com/QuantEcon/lecture-python.myst/commit/0d5c6873873de21f824fae15d157980e68267fba) | November 17 22:54:47 UTC, five files; commit metadata/file list and topic headings screened, not full proofs/exercises. Existing project lecture CC BY-SA 4.0 record; rendered new pages unavailable in web tool and item-specific rights not freshly verified. | **LINK + DO NOT COPY** watchlist: substantial new exposition, but no fully audited incremental workflow adopted. General theory/math checks already exist; defer theorem/support/KL-direction audit before adding specialized guidance. No code/derivations/exercises copied. |
| [DoubleML Python history](https://github.com/DoubleML/doubleml-for-py/commits/main/) | Eight commits; #466 adopted above, remaining #469 formatting/config/backend/docs changes screened by titles only. | **LINK**: no separately established research-method increment; not a full audit of formatting diff. |
| [DoubleML R](https://github.com/DoubleML/doubleml-for-r), [rdrobust](https://github.com/rdpackages/rdrobust), [fixest](https://github.com/lrberge/fixest) | Official default-branch histories return zero new commits within window, no pagination. | **LINK** monitoring; not proof of no updates on other branches/distribution channels. |
| [AEA Data and Code Availability Policy](https://www.aeaweb.org/journals/data/data-code-policy) | Visible version remains February 2026; no dated substantive update established. Copyright retained; not a blanket reuse license. | **LINK + DO NOT COPY**, existing/pending replication intake covers it. |
| [NBER papers](https://www.nber.org/papers), [econ.EM recent](https://arxiv.org/list/econ.EM/recent?show=100), [stat.ME recent](https://arxiv.org/list/stat.ME/recent?show=100) | NBER browser 403; direct page available but dynamic discovery incomplete. arXiv first pages contain 45 economics and 100 statistics entries; today’s 7 economics and 21 statistics titles screened, not full paper review. Item-specific rights required. | **LINK + DO NOT COPY** screening; no theorem or recipe adopted from titles/abstracts. |
| Florian Gunsilius, David Van Dijcke and Kaspar Wüthrich, [Inference after coding agents](https://arxiv.org/abs/2611.23174) | Official v1 November 17 18:22:01 UTC predates cutoff despite November 18 listing; abstract/author/history and nonexclusive distribution license inspected; no independent affiliation/full-proof/code audit. | **LINK + DO NOT COPY** priority watchlist: selective-inference replay correction requires stability/selection assumptions; do not equate independent agent review or a fresh run with statistical correction. No empirical rates or universal validity claim imported. |

No popularity or aggregator evidence used. Only original report and review metadata may be archived; no upstream assets uploaded.

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
