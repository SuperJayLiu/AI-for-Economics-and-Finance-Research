> Copyright (c) 2026 SuperJayLiu (Chaojie Liu). Licensed under the repository MIT License.

# Paper Drafting, Revision, and Citation Skills

These are for writing with guardrails. They should improve structure and clarity without inventing substance.

> [!TIP]
> Diagnose before rewriting. A polished paragraph with a vague research question, weak evidence, or unsupported contribution is still weak.

> [!NOTE]
> Import/use-as-skill protocol for any block on this page: `Start by collecting only the missing inputs needed for the task. Ask up to five clarifying questions when required inputs, data rules, method details, permissions, audience, or output format are unclear. For long outputs, file-producing tasks, slides, code, methods sections, literature reviews, referee responses, or agentic workflows, first return "Proposed structure and assumptions" and ask the user to confirm before producing the full output. Before finalizing, double-check for unsupported claims, invented citations or results, privacy risks, and mismatch with the requested format. End with "What I produced", "What I did not change", "What you must verify", and "Questions for you".`

## Skill 1: Introduction Spine Builder

```text
Act as a top-field economics/finance paper editor. Build the spine of my introduction without writing final prose yet.

Inputs:
- Field: If I have not provided it, ask me to specify: economics/finance subfield
- Research question: If I have not provided it, ask me to specify: question
- Setting: If I have not provided it, ask me to specify: setting
- Data: If I have not provided it, ask me to specify: data
- Identification/model: If I have not provided it, ask me to specify: design or model
- Main results: If I have not provided it, ask me to specify: verified results only
- Contribution claim: If I have not provided it, ask me to specify: current claim
- Target audience/journal: If I have not provided it, ask me to specify: audience

Produce:
1. Motivation: why a serious scholar should care.
2. Puzzle or friction: what is not understood.
3. Research question in one sentence.
4. What the paper does.
5. Identification/model credibility paragraph.
6. Main findings, with economic magnitude.
7. Contribution to each relevant literature.
8. Limitations and scope.
9. A paragraph-by-paragraph introduction outline.

Rules:
- Do not invent citations.
- Do not strengthen causal claims.
- Do not hide limitations.
- Mark every sentence that needs a citation.
```

## Skill 2: Evidence-Preserving Revision

```text
Revise the following academic prose for clarity, precision, and flow while preserving meaning.

Text:
If I have not provided this, ask me to provide: paste text

Context:
- Field: If I have not provided it, ask me to specify: field
- Section: If I have not provided it, ask me to specify: intro/literature/methods/results/discussion
- Target audience: If I have not provided it, ask me to specify: journal/seminar/policy

Rules:
1. Preserve all citations, numbers, notation, hypotheses, and hedging.
2. Do not add new claims.
3. Do not remove limitations.
4. Improve sentence structure and paragraph logic.
5. If a claim is unclear or unsupported, flag it instead of fixing it silently.

Return:
- Revised text.
- Change log explaining substantive risks.
- Claims I must verify.
```

## Skill 3: Citation Support Bank

```text
Create a citation support bank for the claims below using only sources I provide.

Claims:
If I have not provided this, ask me to provide: paste claims

Sources:
If I have not provided this, ask me to provide: paste BibTeX, notes, PDFs, or source list

For each claim, produce a table:
- claim
- candidate source
- exact reason the source supports the claim
- whether support is direct, indirect, or weak
- sentence that still needs verification
- citation risk

Rules:
- Do not invent sources.
- Do not use a source unless it actually supports the claim.
- If no source supports a claim, say "no supplied source supports this claim."
```

## Skill 4: Referee Response Planner

```text
Help me plan a response to referee/editor comments.

Inputs:
- Paper summary: If I have not provided it, ask me to specify: summary
- Decision letter: If I have not provided it, ask me to specify: paste
- Referee comments: If I have not provided it, ask me to specify: paste
- Constraints: If I have not provided it, ask me to specify: time/data/code limits

Produce:
1. Comment taxonomy: fatal, major, minor, misunderstanding, optional.
2. Repeated themes across referees.
3. Revision plan by section/table/figure.
4. New analyses needed, with feasibility.
5. Response-letter outline.
6. Places where we should concede.
7. Places where we can respectfully disagree.
8. Risks if we do not address a comment.

Rules:
- Do not draft fake results.
- Do not promise analyses unless data/code can support them.
- Keep tone professional, not defensive.
```

## Skill 5: Top-Journal Introduction Diagnostic

```text
Diagnose this economics/finance paper introduction before rewriting it.

Introduction:
If I have not provided this, ask me to provide: paste

Project facts:
- Field: If I have not provided it, ask me to specify: field
- Research question: If I have not provided it, ask me to specify: question
- Setting/data/model: If I have not provided it, ask me to specify: setting/data/model
- Identification or mechanism: If I have not provided it, ask me to specify: design/mechanism
- Main result: If I have not provided it, ask me to specify: verified result
- Target audience/journal: If I have not provided it, ask me to specify: target

Check the introduction funnel:
1. broad stakes
2. object of study
3. specific unanswered question
4. why prior work could not answer
5. ideal evidence or model needed
6. why this setting/data/design works
7. strategy
8. findings
9. contribution

Return:
- funnel status: intact / partly broken / broken
- first failure point
- main issue
- why it matters
- surgical fix
- optional rewrite of only the weakest paragraph

Rules:
- Do not invent results, citations, data, or mechanisms.
- Do not turn the introduction into a literature review.
- When information is missing, write plain labels such as MAIN ESTIMATE or CLOSEST PAPER and list them under "Questions for you" instead of inventing details.
```

## Skill 6: Finance Journal Prose Revision

```text
Revise this finance manuscript prose for a serious journal audience while preserving meaning.

Text:
If I have not provided this, ask me to provide: paste

Context:
- Section: If I have not provided it, ask me to specify: introduction/results/discussion/literature/etc.
- Design/evidence: If I have not provided it, ask me to specify: brief
- Target journal/audience: If I have not provided it, ask me to specify: target

Rules:
1. Preserve all citations, numbers, notation, variables, sample definitions, and hedging.
2. Do not add claims, mechanisms, results, or robustness checks.
3. Keep causal language disciplined.
4. Emphasize economic magnitude where supplied.
5. Avoid generic academic filler and chatbot-style phrasing.
6. Do not use LaTeX emphasis commands unless functionally necessary.

Return:
- revised prose
- change log
- claims requiring verification
- sentences where meaning may have changed
```

Sources and workflow influences: PaperSpine's writing rationale matrix and citation support bank; Paul Goldsmith-Pinkham's warnings about AI writing and cognitive offloading; the repository author's top-journal introduction, paper-writer, and paper-review coaching skills.
