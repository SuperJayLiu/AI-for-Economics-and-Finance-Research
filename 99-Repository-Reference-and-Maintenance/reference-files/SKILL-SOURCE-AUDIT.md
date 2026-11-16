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

## 2026-11-16 Incremental Methods Audit

Clean preflight; fetched origin/main `2e1f2a1b2a22b7ab97da4c26af22650ef952ac3e`; dated branch created directly from main. Prior successful completion: 2026-11-12 22:13:51 UTC, search overlap from 21:43:51 UTC. Pending drafts #4–9 were deduplicated, not imported. All sources accessed 2026-11-16. Bounded audit, not an exhaustive literature or revision search.

### Adopted Update and Deduplication

DoubleML team; maintainers Philipp Bach and Sven Klaassen (pinned README); contributor `vrjdev`: [PR #460, “fix: raise NotImplementedError for adding or subtracting clustered DoubleMLFramework objects”](https://github.com/DoubleML/doubleml-for-py/pull/460), merged 2026-11-15 06:05:22 UTC at `6a92b231214dc977b76b9ca27e2a8e2d2a9860e1`. [Pinned BSD-3-Clause license](https://github.com/DoubleML/doubleml-for-py/blob/6a92b231214dc977b76b9ca27e2a8e2d2a9860e1/LICENSE). Checked 2026-11-16 against all three final changed files, including one-/two-way cluster tests. **UPDATE + LINK**: original workflow adaptation for operation-specific inference acceptance; no source code, tests, fixtures, prose, or extended structure copied or executed. Merged source is not evidence of installed-release availability or valid applied estimates.

Existing 03 and packaged reference 05 already accept design/code/inference inputs and return methods/table verification. Pending #5–9 cover DML benchmarking, tuning, fit artifacts, sensitivity fallback, RD bandwidths, weights and running-variable validation. They do not specify the clustered framework arithmetic failure boundary. **UPDATE**, no ADD: preserve that existing contract while requiring exact operations, cluster/sample alignment, joint covariance evidence and explicit stop on unsupported uncertainty claims. English/Chinese discovery, routers, source page, review standards and changelog carry corresponding routes; both substantive pages carry the full source record.

Security: read source and final tests only; no external code installed/executed, no credentials or research data requested, no automatic fallback to unclustered inference. Upstream tests cover one-/two-way PLIV operations; they do not certify all wrappers, estimators or applied results. No release-version guarantee inferred.

### Other Source Decisions

| Source | Decision and reason | Rights and exclusions |
| --- | --- | --- |
| Manish Jha, Georgia State University; [AI for Finance Research](https://mjha91.github.io/pdf/AIFinanceResearch.pdf), [Text Data in Finance](https://mjha91.github.io/pdf/TextDataFinance.pdf), [author homepage](https://mjha91.github.io/) | **LINK + DO NOT COPY**, no new UPDATE. Fresh bytes match prior hashes (AI `cf031ca34fcb6756a43292002ba507365ddfcb6e8780bc52c130055e3051be03`; text `1f3455ec5839f8208b886c99e4d71bef6e5bb1affa9b5229b11e7e1b0848b4bd`), Last-Modified November 2. All requested review/execution, diff/sample, batch logging, instruction, eight-area LLM, contamination, construct-validation and text-as-data patterns already in pending #4 across 03/05/08/09/13/15/17 and packaged refs | No explicit reuse license established. AI cover October 30; text undated. Only original attribution/linking here; no lecture wording, charts, templates, prompts, extended structure or assets copied or uploaded |
| AEA [Data and Code Availability Policy](https://www.aeaweb.org/journals/data/data-code-policy) | **LINK**, visible version February 2026; no substantive in-window policy update established; existing replication skills cover the contract | AEA permits policy-language adaptation but reserves name/logo rights; none copied |
| NBER [working papers](https://www.nber.org/papers), checked [w35962](https://www.nber.org/papers/w35962) | **LINK + DO NOT COPY**, no adoption. Direct primary record identifies Avdjiev/Forbes/Nenova/Santos, global imbalances, issue November 2; search preview associated the number with an unrelated LLM benchmark. Primary record overrides preview; no in-window method increment established | No general reuse permission established; no paper content copied. Browser 403/direct HTTP reachable; listing discovery incomplete |
| Ramesh Johari/Anushka Murthy [2611.16406](https://arxiv.org/abs/2611.16406); Boyarsky/Egami/Namkoong [2611.16242](https://arxiv.org/abs/2611.16242) | **LINK**, date-screened only, no adoption: primary histories v1 November 12 at 07:15:30 and 03:40:32 UTC, respectively, before cutoff; November 13 list appearance is not a revision | First record arXiv nonexclusive distribution, **DO NOT COPY**; second CC BY 4.0. No text/code adapted; full identity/proof/implementation audit not certified |

Official default-branch histories since overlap: DoubleML Python 1 commit (adopted above); DoubleML R, rdrobust, fixest, QuantEcon 0, no next pages. arXiv econ.EM 42 entries and stat.ME first page screened for discovery; new records remain a review queue unless version, identity, assumptions, rights and distinct workflow benefit are established. No popularity evidence used. No central or page-level attribution is added for an unadopted workflow beyond this screening ledger.
