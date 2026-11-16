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

## 2026-11-16 Evening Incremental Methods Audit

Clean preflight; fetched origin/main `2e1f2a1b2a22b7ab97da4c26af22650ef952ac3e`. Search since previous successful completion 09:54:26 UTC, with overlap from 09:24:26. Existing same-date branch/PR #10 preserved; new `codex/daily-research-skill-update-2026-11-16-evening` created directly from origin/main. Pending #4–10 deduplicated, not imported. All sources accessed 2026-11-16. Bounded audit, not exhaustive literature or release-channel coverage.

### Adopted Update, Rights and Deduplication

fixest project; maintainer Laurent Berge, verified in [pinned DESCRIPTION](https://github.com/lrberge/fixest/blob/76adcc876acda767bc749303c6c4e5758778add9/DESCRIPTION); contributor GitHub account `soodoku`: [PR #703, weighted second-stage IV R-squared](https://github.com/lrberge/fixest/pull/703), merged 2026-11-16 17:09:34 UTC at `8b9fd7af9951b330f0144a332695bceeeab6be57`; [PR #708, weighted Sargan total sum of squares](https://github.com/lrberge/fixest/pull/708), merged 17:54:42 UTC at `271b7e8b8a166f3e879d7cdf837fd87736a3a1fb`. Checked 2026-11-16 against both final two-file patches, including tests; DESCRIPTION declares GPL-3. **UPDATE + LINK**, no ADD: original diagnostic-reconciliation procedure only; no upstream code, tests, data, prose or extended structure copied or executed. These are merged-source checks, not a claim that a particular installed/CRAN release includes them or that overidentification tests prove instrument validity.

Existing 03 and packaged reference 05 take design/code/inference inputs and return methods/table checks. Their generic IV relevance, exclusion and inference checks do not specify weighted diagnostic reconstruction. Pending #4–10 address review/measurement, versioning, DML/RD or numerical-policy contracts; they do not distinguish these two residual/centering chains. **UPDATE**, not ADD: same trigger family, inputs and output ledger; add statistic-specific weight consistency, controlled reconstruction and failure boundaries. Both substantive pages carry exact attribution; navigation/routes/sources/standards/changelog are synchronized.

Maintenance: final two-file patch of each adopted PR inspected, including weighted-formula and constant-weight controls. DESCRIPTION at pinned current source identifies maintainer and GPL-3; root LICENSE URL returned 404, not evidence of missing package permission. No GPL implementation/test expression imported into this MIT repository. PR body AI-assistance disclosures are not correctness evidence; final diffs independently read. Security: read-only external inspection; no packages/dependencies installed or upstream code/tests/data executed; no credentials or restricted research data used. Original local synthetic calculation is limited arithmetic verification, not upstream or applied-estimate certification.

### Other Decisions

| Primary source | Date/identity and incremental evidence | Decision, rights and boundary |
| --- | --- | --- |
| Manish Jha, Georgia State University; [homepage](https://mjha91.github.io/), [AI for Finance Research](https://mjha91.github.io/pdf/AIFinanceResearch.pdf), [Text Data in Finance](https://mjha91.github.io/pdf/TextDataFinance.pdf) | Own-site affiliation verified. Homepage and both PDFs byte-identical to morning; PDF hashes `cf031ca34fcb6756a43292002ba507365ddfcb6e8780bc52c130055e3051be03` and `1f3455ec5839f8208b886c99e4d71bef6e5bb1affa9b5229b11e7e1b0848b4bd`; Last-Modified November 2 is deployment evidence, not revision | **LINK + DO NOT COPY**, no UPDATE. No reuse license established; AI cover October 30, text undated. All requested plan/review/execute, independent review, diff/sample, batch ledger, agent instructions, eight-area LLM, look-ahead/memorization, construct validation and text-as-data boundaries already pending #4. No slides, prompts, figures, templates, structure or assets copied |
| AEA [Data and Code Availability Policy](https://www.aeaweb.org/journals/data/data-code-policy) | Visible version remains February 2026; change since morning is an administrative telephone banner, not replication policy | **LINK**, no UPDATE. Institutional adaptation encouragement is not blanket asset permission; no policy prose/forms/logos copied |
| [NBER working papers](https://www.nber.org/papers), [arXiv econ.EM recent](https://arxiv.org/list/econ.EM/recent), [stat.ME recent](https://arxiv.org/list/stat.ME/recent) | NBER visible text and both arXiv page bytes unchanged since morning; arXiv 42 econ entries and first 50 stat entries only | **LINK + DO NOT COPY** screening, no adoption. No general reuse license inferred for listings/papers. NBER browser 403 but direct HTTP works; dynamic listing/search coverage incomplete. No claim that no new NBER papers exist; no full paper/identity/proof audit inferred |
| fixest [#682](https://github.com/lrberge/fixest/pull/682), [#684](https://github.com/lrberge/fixest/pull/684) | Merged November 16; demeaning budget and sparse matrix changes. Final patches read as candidate screening | **LINK**, GPL-3 declared by package; no copied code/tests. Existing numerical convergence and sample/matrix checks overlap; detailed numerical/representation coverage audit deferred, not silently adopted |

Official default-branch histories since overlap: fixest 22 commits, DoubleML Python/R, rdrobust and QuantEcon zero; no next pages. Other fixest commits screened by title only, not all fully audited. No popularity evidence used. Original reports/metadata only may be archived, no restricted assets.
