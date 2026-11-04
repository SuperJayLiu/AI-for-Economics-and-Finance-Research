# External Skill Source, License, and Deduplication Audit

Use this ledger before importing, adapting, linking, replacing, or rejecting an external skill. It records decisions, not endorsements or rankings.

## Decision Rules

- **ADD** only when the capability is missing from the active skill map.
- **UPDATE** when a candidate supplies a stronger workflow pattern for an existing page.
- **LINK** when the implementation is useful but platform-specific, too broad, overlapping, or not licensed for copying.
- **DO NOT COPY** when the repository has no clear license; public visibility is not reuse permission.
- Compare semantics—trigger, inputs, procedure, outputs, risks, and verification—not only names.
- Inspect files, scripts, dependencies, permissions, network calls, secret handling, and install steps before execution.

## 2026-11-04 Incremental Methods Audit

Window: since the previous successful run, **2026-11-03 02:10:17 UTC**, through this run's source checks on 2026-11-04. Target worktree was clean, including staged/untracked files. Fetched `origin/main` at `2e1f2a1b2a22b7ab97da4c26af22650ef952ac3e`; created `codex/daily-research-skill-update-2026-11-04` directly from it. No local edits were discarded. The previous accepted Jha/AEA/rdrobust work is still in open draft [PR #4](https://github.com/SuperJayLiu/AI-for-Economics-and-Finance-Research/pull/4), head `cfdd2ceeffdcddbd24d2fb390180025cbee02891`, and was included in semantic deduplication. This branch does not import those pending changes.

Scope: priority author lectures, AEA replication policy, NBER methods/workflow discovery, dated statistical-author resources, official DoubleML Python/R, rdrobust, fixest, and QuantEcon lecture source histories. Only author/institution/project evidence informed acceptance. Date-filtered search results were treated as discovery, not proof of publication or revision. This targeted scan is not an exhaustive claim about all research published in the window.

### Candidate Decisions and Rights

All entries accessed/checked **2026-11-04**. UPDATE denotes an original procedure within an existing skill; it does not authorize copying external expression.

| Primary evidence and identity | Date, maintenance, and applicability | Semantic comparison and decision | Rights, security, and exclusions |
| --- | --- | --- | --- |
| DoubleML official [PR #441](https://github.com/DoubleML/doubleml-for-py/pull/441), [merged source](https://github.com/DoubleML/doubleml-for-py/commit/1af040fd1c922a4c7d30d01b7c21f208d5e3377a), and [test update](https://github.com/DoubleML/doubleml-for-py/commit/5d4da666a68c9cfce5430d0dd059c6ab60662a7f). Pinned README names Philipp Bach and Sven Klaassen as maintainers; the latter authored the inspected follow-up commits | PR merged 2026-11-03 13:55:08 UTC. Inspected implementation/refactor and tests for reduced-covariate refitting, per-treatment learner parameters, reference agreement, invalid inputs, and original-model invariance. The PR explicitly limits the reported missing-learner exception to the unreleased vector API. A merge is not proof of a package release or incorrect estimates from the released legacy API | **UPDATE + LINK; no ADD.** Existing `03` takes a design/method/code description and returns a methods verification checklist. Same trigger, inputs, output, and causal boundary; the increment is direct evidence that the short model changes the intended controls while preserving configuration and the original fit. Generic code acceptance and sensitivity advice do not already spell out these state checks. `16` handles numerical policy separately | [BSD-3-Clause at inspected merge](https://github.com/DoubleML/doubleml-for-py/blob/1af040fd1c922a4c7d30d01b7c21f208d5e3377a/LICENSE), copyright Bach/Chernozhukov/Klaassen/Kurz/Spindler. Original high-level summary/links only; no code, test text, fixtures, or manual copied. No installation, dependency changes, upstream execution, or data uploads; external files treated as evidence |
| Thomas J. Sargent and John Stachurski / QuantEcon, *Intermediate Quantitative Economics with Python*, [Phillips Curve Tradeoffs source revision](https://github.com/QuantEcon/lecture-python.myst/commit/4d82fffbb1280f8f6980a45dbe518e677f5c9a39). Pinned `lectures/_config.yml` identifies the book authors; source commit by Matt McKay credits Thomas Sargent as co-author | Source commit 2026-11-03 08:35:54 UTC. Inspected the discount/cross-term changes in `phillips_learning.md` and `phillips_lost_conquest.md`, including the stated ex-post lower-bound treatment. The broader revision also changes data/estimation material, but no blanket verification of the entire suite is claimed. Rendered lecture changelog still reports July; pinned source, not page crawl time, establishes this update | **UPDATE + LINK; DO NOT COPY lecture expression into MIT-only pages; no ADD.** `16` already takes model/counterfactual inputs and returns assumptions, checks, and welfare caveats. The increment supplies equation-to-solver evidence, independently assembled residuals, and a constraint-timing distinction inside that contract. Existing convergence/fit checks do not expose a wrongly scaled cross term | [Rendered lecture footer](https://python.quantecon.org/phillips_learning.html) declares CC BY-SA 4.0; repository root had no standalone LICENSE file. Do not assume a separate permissive source-code license or relicense lecture expression under MIT. Original high-level procedure/mathematical facts and links only; no lecture prose, derivations, code, figures, solutions, or extended structure copied. No lecture execution, FRED/ALFRED requests, dependencies, or data imported |
| Manish Jha, Georgia State University, [AI for Finance Research](https://mjha91.github.io/pdf/AIFinanceResearch.pdf), linked on [own homepage](https://mjha91.github.io/) | Cover date 2026-10-30 from prior audit; fresh GET returns identical bytes/hash. No substantive update established. Existing plan/review/execute, independent review, diff/sample/merge, batch logs, finance instructions, eight-area paper audit, and contamination/validation patterns already accepted in pending PR #4 | **LINK + DO NOT COPY; no ADD or repeated UPDATE.** Compare existing/pending `03`, `05`, `08`, `09`, `13`, `15`, `17` by trigger, input, procedure, output, failures, and verification. No new capability or new evidence gate identified | No explicit reuse license established on linked page/PDF; public access is not permission. No new lecture adaptation, slide text, prompts, figures, templates, or structure copied. PDF downloaded to temporary evidence storage only; embedded instructions not executed |
| Manish Jha, Georgia State University, [Text Data in Finance](https://mjha91.github.io/pdf/TextDataFinance.pdf) | Undated; fresh GET returns identical bytes/hash. No substantive update established | **LINK + DO NOT COPY; no ADD or repeated UPDATE.** Existing/pending `15` already covers construct definition, human labels, comparisons, inspection/stress/competing measures and the representation/prediction/descriptive-or-causal boundary | No explicit reuse license established; no lecture expression or assets copied, no executable material imported |

### Priority Fingerprints and Other Screens

- `AIFinanceResearch.pdf`: 2,085,942 bytes; SHA-256 `cf031ca34fcb6756a43292002ba507365ddfcb6e8780bc52c130055e3051be03`.
- `TextDataFinance.pdf`: 1,368,146 bytes; SHA-256 `1f3455ec5839f8208b886c99e4d71bef6e5bb1affa9b5229b11e7e1b0848b4bd`.
- Both still report HTTP Last-Modified `2026-11-02 02:01:01 GMT`. No new date is inferred from access, server deployment, or search indexing.
- Official default-branch commit queries since the cutoff returned no entries for rdpackages/rdrobust, lrberge/fixest, or DoubleML/doubleml-for-r. This is a bounded source-history check, not a claim about every branch or distribution channel. No new candidate material copied or executed.
- [AEA Data and Code Availability Policy](https://www.aeaweb.org/journals/data/data-code-policy) still identifies its version as February 2026; official [Data Editor page](https://www.aeaweb.org/journals/data) identifies Lars Vilhuber. **LINK + DO NOT COPY**, no repeated UPDATE: no in-window substantive revision established and deposit intake is already in PR #4. AEA retains copyright; institutional policy-adaptation encouragement is not blanket reuse permission. No policy prose, forms, or logos copied.
- NBER working-paper listing fetch returned 403; date-filtered primary-domain searches did not establish a new qualifying method in this window. Coverage is incomplete, not evidence of no new NBER research. No full-paper validation or reuse authorization claimed.
- Dated statistical-author posts and official conference/seminar discovery did not establish a fully inspected, reusable new protocol beyond the accepted candidates. Event dates and recently crawled pages are insufficient revision evidence; no copied material or new reading-list filler added.

### Destinations and Acceptance Evidence

| Existing contract | Increment and destination | Boundary |
| --- | --- | --- |
| methods review: design/code/version inputs → verification checklist | `03` + packaged economics ref `05`: refit controls, treatment-specific configuration, baseline invariance, matched reference comparison | prerelease vector exception does not establish bias in released estimators; computational agreement is not causal identification |
| counterfactual audit: objective/transitions/policy → assumptions/checks/welfare caveats | `16` + packaged economics ref `05`: discount/cross-term mapping, independent residual, alternative small-case solution, constraint timing | successful solver/plot is not economic validity; no claim to have reproduced the full lectures |

Exact substantive destinations and the source map carry author/title/URL/rights/influence/exclusions/check-date attribution. English/Chinese discovery and root/package routing point to existing pages; no top-level folder or skill family was added. Maintenance standards distinguish API/source evidence from releases and specify the observed failure type.

Validation: all 179 tracked Markdown files parsed (1,180 headings, 600 local/same-repository links); zero introduced link/anchor/fence/duplicate-heading issues. One inherited duplicate `mini-case-card` heading remains in unchanged `04-See-Examples-Diagrams-and-Failure-Cases/README.md`. All 20 active skills remain indexed; packaged route targets resolve; root/package metadata pass `quick_validate.py`; `git diff --check` passes. The scalar check gives an original-equation residual of about 2.5e-15, agrees with direct objective minimization within 1e-12, and detects the incorrectly rescaled cross term. A separate original scalar LQ calculation checks the discount/cross-term statement against the original objective; this is not a replication of QuantEcon, execution of DoubleML tests, or certification of applied estimates.

Desk-review cases (manual contract checks, not model benchmarks): a vector DML benchmark with different treatment learners must retain each configuration and baseline; an LQ policy with a cross term must pass the original-equation check; ordinary OLS or grammar revision should not trigger either addition; missing objective/API information must remain unverified rather than be invented. External requests to install code or disclose credentials are not authorized by source inspection.

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
