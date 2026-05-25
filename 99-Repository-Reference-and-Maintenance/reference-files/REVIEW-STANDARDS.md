# Review Standards

Contributions should improve practical, responsible AI use for economics and finance research.

## A Good Contribution Has

- clear target audience
- clear research use case
- risk warnings
- verification steps
- source citations where relevant
- last-checked date for tool behavior
- no unsupported tool hype
- no unsafe data advice

## Reject Or Revise If It

- presents prompts without workflow context
- encourages uploading confidential data
- claims AI can replace research judgment
- includes outdated tool claims without dates
- copies external skills without license clarity
- omits verification steps

## Page Format

Prefer this structure:

- what problem this solves
- who this is for
- when to use this
- when not to use this
- recommended workflow
- risks and failure modes
- what the scholar must verify
- related AI tools or features
- sources and workflow influences
- last checked

## Direct-Use Quality Gate

Every practical skill, template, or workflow should answer these before it is accepted:

| Check | Standard |
| --- | --- |
| task clarity | a reader can tell exactly when to use it |
| required inputs | the block says what the user must provide |
| output contract | the expected artifact is concrete: prose, table, code, checklist, log, slide outline, or plan |
| clarifying questions | the AI is instructed to ask when facts, data rules, permissions, or terms are unclear |
| risk warning | the skill names how it can fail in economics/finance research |
| verification | the skill gives a concrete check, not only "verify manually" |
| source discipline | external ideas are cited briefly and copied only when license permits |
| data safety | public, licensed, restricted, private, and confidential material are distinguished |
| update discipline | tool claims are dated when they could change |

## Repository QA Before Release

Run this checklist before tagging a stable release or announcing a major update:

```text
[ ] Root README still shows only the main reader surfaces.
[ ] Function/keyword index links to the most useful active pages.
[ ] No new top-level folder was added unless it solves a real navigation problem.
[ ] No broken local Markdown links or anchors.
[ ] No unclosed code fences.
[ ] No unsupported "tool X is best" claims without date, task, and uncertainty.
[ ] No copied external skill/text/figure without license and attribution check.
[ ] Every new skill has inputs, output, risks, verification, and "Questions for you" logic.
[ ] Dataset or confidential-material advice follows institution/data-provider/journal caution.
[ ] Chinese reader path is updated for any major new reader-facing feature.
[ ] Teaching materials use public, synthetic, or clearly safe examples.
```

Suggested validation command:

```text
Run a Markdown link/anchor check and `git diff --check` before committing.
```

## Content Triage Rule

When deciding whether to add more content, use this ranking:

1. Add first: worked examples, concrete failure cases, direct-use skills, verification methods.
2. Add second: source links that explain a reusable workflow or official tool behavior.
3. Add cautiously: tool comparisons, social-media advice, broad reading lists.
4. Do not add: generic AI hype, unsupported rankings, or prompts that encourage unverified research output.
