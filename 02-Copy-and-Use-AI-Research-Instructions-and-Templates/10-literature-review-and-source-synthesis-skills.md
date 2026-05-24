> Copyright (c) 2026 SuperJayLiu (Chaojie Liu). Licensed under the repository MIT License.

# Literature Review and Source Synthesis Skills

Use these skills when the task is more serious than "summarize this paper." The goal is to build a source-grounded literature map, identify real gaps, synthesize arguments, and avoid fake citations.

> [!IMPORTANT]
> AI is not a literature database. Use these skills only with supplied papers, notes, BibTeX, Zotero exports, or verified search results. Never trust AI-generated citations without checking original sources.

Questions or suggestions for this part: email [jay.liu@bristol.ac.uk](mailto:jay.liu@bristol.ac.uk) with subject `[AI Econ Finance Literature Review] Suggestion`.

> [!NOTE]
> Default add-on for any block on this page: `If any required input, term, method detail, data rule, or output format is unclear, ask me up to five clarifying questions before giving the final output. Define unfamiliar technical terms in plain language and end with "Questions for you" if anything remains uncertain.`

## Grounding Rule

Use the right source mode for the task.

| Task | Acceptable grounding | Not acceptable |
| --- | --- | --- |
| summarize a paper | supplied PDF, notes, abstract, or verified excerpt | model memory |
| build a literature map | supplied papers, BibTeX, Zotero export, or verified search results | "find papers from memory" |
| write a contribution paragraph | closest papers already read and verified | invented "gap" claims |
| check citation support | original source, DOI, page/section, or verified notes | title similarity |
| discover missing literatures | search-grounded exploration labeled as hypothesis | uncited AI suggestions treated as facts |

The safest workflow is:

```text
search or collect sources -> verify source exists -> read/source-note -> AI synthesis -> claim-to-source check -> human rewrite
```

## Choose a Skill

| Need | Use |
| --- | --- |
| build a full literature review from real sources | Skill 1 |
| create a paper matrix | Skill 2 |
| read one paper deeply | Skill 3 |
| compare two or more papers | Skill 4 |
| find fake novelty risk | Skill 5 |
| create a source support bank | Skill 6 |
| build a worked literature-review spine | Skill 7 |

## Skill 1: Source-Grounded Literature Review Builder

```text
Build a source-grounded literature review for an economics/finance research project.

Research project:
- Field/subfield: [field]
- Research question: [question]
- Intended contribution: [contribution]
- Target audience: [PhD field paper / seminar / journal / proposal]

Sources I provide:
- Papers/BibTeX/notes: [paste or upload]
- Sources already read carefully: [list]
- Sources only skimmed: [list]

Tasks:
1. Group the supplied literature by mechanism, method, setting, and data.
2. Identify the closest papers and explain why they are close.
3. Separate what the literature has established from what remains uncertain.
4. Explain what my project may add, using cautious language.
5. Flag fake novelty risk, missing literature risk, and citation risk.
6. Draft a literature review outline.
7. Draft one source-grounded synthesis paragraph.

Rules:
- Use only supplied or explicitly verified sources.
- Never invent author names, titles, journals, years, results, or citations.
- Do not write "little is known" unless the supplied evidence supports that claim.
- Distinguish direct evidence from interpretation.
- Mark any claim needing citation as [CITE NEEDED].

Return:
1. literature map
2. closest-paper table
3. synthesis outline
4. draft paragraph
5. claims to verify manually
```

## Skill 2: Literature Matrix for Econ/Finance

```text
Create a literature matrix from the papers I provide.

For each paper, extract:
- citation key or short name
- research question
- setting
- data
- method or model
- identification strategy or theoretical mechanism
- main result
- limitation
- relation to my project
- citation risk or verification needed

Then create cross-paper columns for:
- shared mechanism
- differences in design/model
- differences in data or sample
- what each paper can and cannot show
- how my project could be positioned

Rules:
- Do not summarize papers not supplied.
- If a paper is missing key information, write "not available from supplied material."
- Keep the matrix factual. Put interpretation in a separate section.
```

## Skill 3: Deep Paper Reading Card

```text
Create a deep reading card for this economics/finance paper.

Paper:
[paste abstract, notes, or paper text]

Extract:
1. research question
2. motivation
3. contribution claim
4. data and sample
5. method/model/design
6. main result
7. identification assumption or theoretical mechanism
8. limitations
9. what I should verify in the original paper
10. how this paper relates to my project

Also answer:
- What is the strongest version of the paper?
- What is the weakest link?
- What would a skeptical seminar participant ask?

Rules:
- Do not add outside facts.
- Separate author claims from your interpretation.
```

## Skill 4: Compare Papers Without Listing Them

```text
Compare these papers as a synthesized literature review, not as a sequence of summaries.

Papers/notes:
[paste]

Comparison dimensions:
- question
- mechanism
- data
- identification or model
- result
- limitation
- relation to my project

Write:
1. a synthesis table;
2. three thematic paragraphs;
3. one paragraph explaining the unresolved gap;
4. one paragraph explaining why my project may address the gap.

Rules:
- Do not write one paragraph per paper.
- Do not claim novelty unless supported by the supplied sources.
- Flag any unsupported gap claim.
```

## Skill 5: Fake Novelty and Missing Literature Risk Check

```text
Audit my literature positioning for fake novelty risk.

My claim:
[paste contribution/literature paragraph]

Known related papers:
[paste sources]

Check:
1. Does the claim sound broader than the evidence?
2. Are there nearby literatures not considered?
3. Are similar mechanisms, data, methods, or settings already present?
4. Is the gap framed as "nobody studied X" when the real issue is measurement, data, variation, theory, or external validity?
5. What must I search or read before making this claim?

Return:
- high-risk sentences
- safer replacement language
- missing-source search plan
- closest-paper questions to answer
```

## Skill 6: Claim-to-Source Support Bank

```text
Build a source support bank for my literature review.

Claims:
[paste claims]

Supplied sources:
[paste notes/BibTeX/PDF summaries]

For each claim, return:
- claim
- source that directly supports it
- source that indirectly supports it
- whether the support is strong, partial, weak, or absent
- exact page/section if supplied
- safer wording if support is weak
- what I must verify manually

Rules:
- If no supplied source supports a claim, say so.
- Do not create references.
- Do not use a famous paper as support unless it actually supports the sentence.
```

## Skill 7: Literature Review Spine With Worked Output

Use this when you have a messy collection of notes and need a readable related-work section.

```text
Create a literature review spine for my economics/finance paper.

Project:
- Research question: [question]
- Proposed contribution: [contribution]
- Empirical design or model: [design/model]
- Setting/data: [setting/data]
- Target audience: [seminar/journal/proposal]

Verified sources:
[paste citation keys and short notes]

Build:
1. the closest-paper table;
2. theme groups;
3. what each theme establishes;
4. what remains unresolved;
5. how my project fits without overclaiming novelty;
6. a paragraph-level outline;
7. one sample synthesis paragraph.

For the sample paragraph, label every sentence as:
- [SOURCE-GROUNDED]
- [INTERPRETATION]
- [NEEDS VERIFICATION]

Return:
- literature review spine;
- sample paragraph;
- unsupported claims list;
- reading/search tasks before writing the final version.

Rules:
- Do not write one paragraph per paper.
- Do not invent missing literatures.
- Do not claim novelty from absence of supplied sources.
```

### Mini Worked Example

```text
Input facts:
- My paper studies whether bank branch closures reduce small-firm credit.
- Supplied papers: one on branch closures and local credit, one on relationship lending, one on fintech substitution.

Good AI output should say:
- The literature groups around physical bank access, relationship lending, and digital substitution.
- The closest papers are close because of mechanism and setting, not only because they mention "banks."
- A possible contribution is about the margin where digital substitution fails, if the data support that.
- The author must verify whether existing papers already study the same closure shock, geography, and firm outcomes.

Bad AI output would say:
- "No prior work studies this question" without verified search.
- "This proves branch closures cause employment losses" before design evidence.
```

Sources and workflow influences: Paper-review and literature-synthesis skill patterns, Paul Goldsmith-Pinkham's LLM-friendly paper orientation idea, PaperSpine-style audit trails, and source-grounded academic writing practices.
