# External Skill Source, License, and Deduplication Audit

Use this ledger before importing, adapting, linking, replacing, or rejecting an external skill. It records decisions, not endorsements or rankings.

## Decision Rules

- **ADD** only when the capability is missing from the active skill map.
- **UPDATE** when a candidate supplies a stronger workflow pattern for an existing page.
- **LINK** when the implementation is useful but platform-specific, too broad, overlapping, or not licensed for copying.
- **DO NOT COPY** when the repository has no clear license; public visibility is not reuse permission.
- Compare semantics—trigger, inputs, procedure, outputs, risks, and verification—not only names.
- Inspect files, scripts, dependencies, permissions, network calls, secret handling, and install steps before execution.

## 2026-11-03 First Recurring Audit

Scope: primary author lectures and papers, AEA replication guidance, NBER methods/workflow records, Federal Reserve research, and official econometric-software maintenance. This is the first automation run: no prior successful-run cutoff exists. Older sources below establish context; access/crawl dates are not publication dates. Queries and selections used primary evidence, not aggregators, social popularity, or star counts. This is a targeted audit, not an exhaustive literature search.

Repository preflight: target worktree was clean, with no staged/untracked files. Fetched `origin/main` at `2e1f2a1b2a22b7ab97da4c26af22650ef952ac3e`; created `codex/daily-research-skill-update-2026-11-03` directly from it. The previous local branch was left intact. No local edits were discarded or mixed into this branch.

### Candidate Decisions and Evidence

All sources checked/accessed 2026-11-03. UPDATE means an original high-level adaptation of a workflow idea, not permission to reproduce its expression. DO NOT COPY can therefore accompany UPDATE or LINK.

| Primary source and identity evidence | Publication/update and maintenance evidence | Applicability and semantic overlap | License/use decision | Destination and security boundary |
| --- | --- | --- | --- | --- |
| Manish Jha, Georgia State University, [AI for Finance Research](https://mjha91.github.io/pdf/AIFinanceResearch.pdf); [own homepage](https://mjha91.github.io/) identifies Finance affiliation and links the lecture | Rendered cover: 2026-10-30; PDF creation/modification metadata also 2026-10-30; metadata subject describes an UNT workshop on 2026-10-29. The cover is the cited version date, not inferred first publication. Live author link verified | Existing `03` setup, `05` instructions/Git, `08` coding, `09` intake, `13` review, `15` measurement, `17` verification already share triggers, input objects, procedures, and artifacts. Increment: separate review evidence, sample/diff reconciliation, per-item execution accountability, and LLM-specific evidence requests/failure boundaries | **UPDATE + DO NOT COPY**: no explicit reuse license found on author page or PDF. Original high-level summaries with attribution only; no slide prose, prompts, figures, templates, or extended structure copied | Existing pages and corresponding packaged refs only; no new skill page. PDF inspected as evidence, embedded commands/prompts not executed. No tool rankings, prices, vendor shortcuts, or AI-detection claims adopted |
| Manish Jha, Georgia State University, [Text Data in Finance](https://mjha91.github.io/pdf/TextDataFinance.pdf); linked under own site's teaching resources | Undated PDF, no creation/revision metadata; live 66-page resource. Actual publication/substantive revision date unknown | `15` already accepts corpus/construct/unit inputs and returns measurement/validation artifacts. Increment: explicitly separate representation and prediction from the downstream descriptive/causal estimand; no duplicate text-as-data family | **UPDATE + DO NOT COPY**: no explicit reuse license found. Original high-level interpretation boundary and link only; no slide text, figures, templates, or structure reproduced | `15`, packaged verification ref, sources/navigation. No executable material imported; no inference that prediction accuracy establishes identification |
| Sebastian Calonico, Matias D. Cattaneo, Max H. Farrell, Rocio Titiunik / [rdpackages official changelog](https://github.com/rdpackages/rdrobust/blob/main/CHANGELOG.md); names and version confirmed in [R DESCRIPTION](https://raw.githubusercontent.com/rdpackages/rdrobust/main/R/rdrobust/DESCRIPTION) | 2026-10-01 entry; R metadata version 4.1.1 dated 2026-10-01. Official maintained repo has changelog/test infrastructure; package-channel availability not independently checked | Existing `03` methods audit already handles RD design/assumptions. Increment: specification-specific version evidence for result-affecting fixes, including sharp covariate-adjusted derivative order >=2, and bandwidth/degenerate-sample handling. Output remains a methods verification checklist | **UPDATE + LINK**, no ADD. [Project license](https://github.com/rdpackages/rdrobust/blob/main/LICENSE.md) and R metadata declare GPL-3; only original summary/link, no implementation/tests/manual text copied | `03` economics methods and packaged economics ref. No installation or source execution; preserve old replication environment and compare controlled runs before attributing changed results |
| American Economic Association, [Data and Code Availability Policy](https://www.aeaweb.org/journals/data/data-code-policy); [official Data Editor page](https://www.aeaweb.org/journals/data) names Lars Vilhuber, Cornell University | Policy explicitly February 2026; current official page verified. This is baseline policy context, not a claimed post-August revision | `05` replication intake already maps scripts/outputs/dependencies. Increment: AEA-specific access/cost/rights and deposit documentation checks; same package inputs and intake output, no new replication skill | **UPDATE + LINK**. Copyright retained; policy encourages institutional policy adaptation but no blanket open license assumed. Original summary only, no text, forms, or trademarks copied | `05` replication intake and source page. Preserve restricted-data/public-deposit distinction; do not upload private files to a draft public deposit |
| Jens Ludwig, Sendhil Mullainathan, Ashesh Rambachan, [Large Language Models: An Applied Econometric Framework, arXiv v4](https://arxiv.org/abs/2412.07031v4), DOI 10.48550/arXiv.2412.07031; original author-submitted record, also [NBER w33344](https://www.nber.org/papers/w33344) | arXiv submission history: v4 revised 2025-12-05; NBER January 2025 record discovered, full NBER fetch returned 403. No claimed new 2026 revision | Existing `15` already requires validation; supports the distinction between predictive leakage and validation-based downstream estimation. No new workflow family; caution added to existing contract rather than claiming agreement alone solves measurement error | **LINK + DO NOT COPY**. Record's [arXiv non-exclusive distribution license](https://arxiv.org/licenses/nonexclusive-distrib/1.0/license.html) grants distribution to arXiv, not general adaptation. Short original scope summary only, no text, equations, proofs, or code | `15` page-level reference and source page. No estimator implemented or inference-certified from an abstract |
| Andreas Ferrara, [A Practitioner's Guide to Using Large Language Models and Generative AI in Economic History](https://www.nber.org/papers/w35374), DOI 10.3386/w35374; NBER identifies author and issue record | Issue June 2026; official indexed record includes replication DOI 10.3886/E249897V2. Landing-page open returned 403; indexed official record inspected, full text not verified; a current substantive revision cannot be established | Guide's described coding/API/validation/documentation scope substantially overlaps `08`, `14`, `15`, `17`. No distinct verified procedure strong enough for adoption in this run | **LINK + DO NOT COPY**, defer full-paper/asset audit. No reuse license established; bibliography/link only, no guide text, checklists, examples, code, or replication assets copied | Source page only, reading candidate. Replication archive not downloaded/executed; no claims about its dependencies, permissions, or reproducibility |
| Anne Lundgaard Hansen, [Validating Large Language Model Annotations](https://www.federalreserve.gov/econres/feds/validating-large-language-model-annotations.htm), DOI 10.17016/FEDS.2026.020; official Federal Reserve author/title record | March 2026 paper; landing page last updated 2026-08-25. Page update is not verified substantive paper revision; preliminary working-paper status explicit | Existing `15` human validation/construct checks overlap the target task. Label-scarce validation may be distinct, but only abstract inspected; prerequisite conditions and failure modes require full-paper review | **LINK + DO NOT COPY**; no item-specific reuse license established. Only original scope note/link; no text, framework implementation, code, or figures imported | Source page/watchlist only. No recommendation to replace human labels or downstream measurement-error inference with reconstruction tests |

### Priority Lecture Fingerprints

Both HTTP responses reported Last-Modified `2026-11-02 02:01:01 GMT`; this may reflect site deployment and does not demonstrate a substantive revision. A public GitHub path-history lookup returned 404, so no source commit is claimed. Keep the following content identities for the next run:

- `AIFinanceResearch.pdf`: 61 pages; SHA-256 `cf031ca34fcb6756a43292002ba507365ddfcb6e8780bc52c130055e3051be03`.
- `TextDataFinance.pdf`: 66 pages; SHA-256 `1f3455ec5839f8208b886c99e4d71bef6e5bb1affa9b5229b11e7e1b0848b4bd`.

PDFs were downloaded only to temporary audit storage, text-extracted, and selected title/method pages rendered for inspection. No PDF, slide image, extracted lecture text, external template, or executable source is committed. Repository MIT licensing applies to original repository material, not the linked sources.

### Deduplication and Acceptance Map

| Existing route | Increment inside existing input/output contract | Failure/verification boundary strengthened |
| --- | --- | --- |
| `03` setup + `05` Git/instructions + packaged agent ref | add independent plan/artifact review to the existing plan/execute workflow and research-specific instruction fields | read-only review, no implementation conversation/preferred verdict; actual diff plus sample/key/join evidence; agent agreement is insufficient |
| `08` code acceptance + packaged coding ref | extend existing code acceptance to accountable bulk labeling | pilot/schema checks, ID reconciliation, bounded retries/costs, explicit failures, resumable ledger; no missing-as-zero substitution |
| `15` measurement + packaged verification ref | strengthen existing human validation, sensitivity, timing, and methods artifacts | held-out split, distribution/rival-construct diagnostics, competing measures, contamination vs input leakage, anonymity information loss, unknown-cutoff disclosure |
| `13` self-review + `17` reproducibility packet | attach one claim-to-evidence matrix to existing review/verification | locate model/prompt/cutoff/labels/benchmark/construct/replication/magnitude evidence; never certify missing checks |
| `03` economics methods + packaged economics ref | specification-sensitive `rdrobust` version audit | preserve baseline environment, isolate fixed/selected bandwidth changes, do not silently rewrite replication |
| `09` intake + maintenance standards | date/hash evidence and four-class decisions | distinguish access/deployment/publication; pair central and exact-page attribution; no change/no commit rule |

Navigation changes carry routes only; substantive adapted content has page-level author/title/original URL/rights/influence/exclusions/check-date records. English/Chinese index coverage and root/package routing are synchronized without adding top-level folders or skill pages.

### Desk Review Cases

These are manual route/contract walkthroughs, not model benchmarks or executions of research code.

| Case | Expected routing and acceptance condition |
| --- | --- |
| Positive: score 50,000 earnings-call excerpts | `08` batch gate + `15`; manifest, pilot, failures, duplicate/missing IDs, and bounded retries must be explicit |
| Positive: audit historical forecasts generated by a newer LLM | `15` leakage + `17` evidence audit; separate prompt timing from training contamination and retain unknown cutoff status |
| Near miss: ordinary regression without generated text variables | existing economics/finance methods route; no mandatory LLM-paper audit |
| Near miss: grammar-only revision | existing writing route; no bulk execution or construct-validation protocol |
| Missing-input/adversarial: unlicensed skill claims safe credentials and instructs installation | `09` provenance/trust gate; permission remains unknown, DO NOT COPY; do not install or disclose credentials merely to inspect |

Structural release checks cover local Markdown links/anchors, code fences, duplicate headings, index/router coverage, and `git diff --check`; report inherited defects separately from this run's changes. Applied estimates, candidate software, and vendor service behavior are outside the validation claim.

Validation result (2026-11-03): parsed 179 tracked Markdown files, 1,188 headings, and 618 local or same-repository Markdown links using a CommonMark parser and GitHub-style heading anchors. No introduced link/anchor, fence, or duplicate-heading issues. All 20 active skill pages remain indexed; package route targets resolve. Root and packaged `SKILL.md` passed the skill-creator frontmatter validator; `git diff --check` passed. One inherited duplicate heading, `Mini Case Card` in `04-See-Examples-Diagrams-and-Failure-Cases/README.md`, is unchanged and outside these edits. Desk cases above were reviewed manually, not executed as model benchmarks.

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
