# Two-Hour Presentation: AI for Economics and Finance Research

This is the readable teaching script for a two-hour presentation based on the handbook. It is designed for economics and finance scholars who may be new to AI, GitHub, coding agents, or formal AI-use logs.

Use it with the live HTML deck: [two-hour-ai-econ-finance-slides.html](two-hour-ai-econ-finance-slides.html).

This deck follows the repo's own slide guidance:

- [Interactive HTML Research Slides](../02-Copy-and-Use-AI-Research-Instructions-and-Templates/06-presentations-slides-websites-and-talk-practice-skills.md#skill-1-interactive-html-research-slides)
- [Paper-to-Talk Converter](../02-Copy-and-Use-AI-Research-Instructions-and-Templates/06-presentations-slides-websites-and-talk-practice-skills.md#skill-5-paper-to-talk-converter)
- [Practice My Presentation With AI](../02-Copy-and-Use-AI-Research-Instructions-and-Templates/06-presentations-slides-websites-and-talk-practice-skills.md#skill-3-practice-my-presentation-with-ai)

> [!IMPORTANT]
> Do not demo with private data, unpublished coauthor material, referee reports, student records, licensed database extracts, or confidential work. Use public abstracts, synthetic examples, screenshots, or toy data.

## Audience

Use this for:

- PhD students and RAs;
- junior faculty and applied researchers;
- finance/economics seminar groups;
- methods workshops;
- research teams setting shared AI-use rules.

## Learning Goals

By the end, participants should be able to:

1. explain what AI/LLMs are useful for in research and where they are dangerous;
2. distinguish prompts, projects, skills, agents, and MCP/connectors;
3. choose a safe AI workflow for literature, coding, empirical methods, writing, and presentations;
4. set up a minimal Git/GitHub/AI-use-log safety system;
5. verify AI outputs with source, data, code, equation, or presentation checks;
6. leave with one copy-ready instruction they can use on a non-confidential task.

## Materials To Prepare

| Item | Required? | Notes |
| --- | --- | --- |
| This repo open in browser | yes | preload root README and folders 01, 02, 03, 04, 06 |
| HTML deck | yes | open locally or through GitHub Pages if later enabled |
| One harmless public abstract | yes | use a public paper abstract, not a private draft |
| One toy data example | optional | useful for showing verification by known answer |
| Institutional AI policy link | recommended | remind participants local rules come first |
| Screenshots | optional | placeholders are included in the HTML deck |

## Two-Hour Run Of Show

| Time | Segment | Goal | Interaction |
| --- | --- | --- | --- |
| 0-5 | Opening | explain the promise and the warning | ask who uses AI weekly |
| 5-15 | Mental model | AI output is labor, not evidence | audience gives one research task |
| 15-25 | Tool glossary | define LLM, Project, Skill, Agent, MCP, GitHub | quick tool-choice poll |
| 25-38 | What AI can help with | literature, code, writing, slides, logs | map tasks to workflows |
| 38-50 | What AI should not decide | identification, causality, final claims, confidential data | upload-or-not exercise |
| 50-65 | Live demo 1 | casual prompt vs controlled workflow | compare outputs |
| 65-75 | Break or buffer | handle questions | optional |
| 75-90 | Git/GitHub safety | one paper, one repo, one AI-use log | show repo structure |
| 90-105 | Agentic workflow | plan, approve, edit, check, log | show approval gate |
| 105-115 | Failure cases | fake citation, wrong code, overclaiming | identify verification method |
| 115-120 | Next steps | one task, one skill, one verification check | participants choose next action |

If you only have 90 minutes, skip the agent demo and keep the Git/GitHub section conceptual.

## Slide-By-Slide Storyboard

| Slide | Title | Purpose | Speaker note | Interaction |
| --- | --- | --- | --- | --- |
| 1 | AI for Economics and Finance Research | frame the talk | this is a workflow talk, not a prompt collection | none |
| 2 | The Promise And The Trap | motivate | AI reduces labor but not responsibility | ask for one AI use case |
| 3 | The Core Rule | anchor principle | AI output is not evidence | audience repeats examples of evidence |
| 4 | What AI Can Help With | positive map | show useful tasks before warnings | ask which task costs the most time |
| 5 | What AI Should Not Decide | boundary | separate assistance from judgment | ask what should never be automated |
| 6 | Tool Map | define terms | LLM, Project, Skill, Agent, MCP, GitHub | quick poll |
| 7 | Prompt To Project To Skill To Agent | progression | move from chat to systems | ask where audience is now |
| 8 | Data Safety Traffic Light | risk | public vs licensed vs restricted vs confidential | upload-or-not |
| 9 | Live Demo 1 Setup | setup | harmless public abstract or methods paragraph | choose demo text |
| 10 | Casual Prompt vs Controlled Workflow | show difference | vague prompts invite vague outputs | compare side-by-side |
| 11 | Verification Is The Skill | teach method | match output to check | classify checks |
| 12 | GitHub As Safety Infrastructure | versioning | if AI edits files, use Git | show branch/diff/commit idea |
| 13 | Minimal Research Repo | practical setup | README, DATA, AGENTS, AI-USE-LOG | screenshot placeholder |
| 14 | Agentic Workflow | agent safety | plan, approve, edit, check, log | approval gate |
| 15 | Collaboration Workflow | team safety | coauthors and RAs need shared rules | ask who approves PRs |
| 16 | Failure Case: Fake Citation | concrete risk | source grounding matters | ask how to catch |
| 17 | Failure Case: Wrong Code That Runs | concrete risk | toy tests matter | ask what toy test would show |
| 18 | Failure Case: Overclaiming | communication risk | slide titles can change meaning | rewrite slide title |
| 19 | Copy-Ready Skills | direct use | show skill folder and fast paths | pick one skill |
| 20 | Two Ways To Use Slides | HTML vs Beamer | format follows audience | ask use case |
| 21 | Personal Next Step | action | one task, one skill, one check | write plan |
| 22 | Q&A | close | invite questions and suggestions | email and repo link |

## Live Demo 1: Casual Prompt vs Controlled Workflow

Use a public abstract, public methods paragraph, or synthetic paragraph.

Bad prompt:

```text
Summarize this paper and tell me the contribution.
```

Controlled prompt:

```text
Using only the text I provide, create a structured research note for an economics/finance audience.

Return:
1. research question;
2. data or setting;
3. method/design/model;
4. main claim stated cautiously;
5. what cannot be verified from the supplied text;
6. what citations or facts I must check manually;
7. three seminar questions.

Do not invent citations, results, datasets, robustness checks, or institutional details.
If anything is unclear, ask up to five clarifying questions.
```

Debrief:

- The second prompt is longer because it defines inputs, output, rules, and verification.
- The output is still not evidence.
- The researcher must still verify the source.

## Live Demo 2: Agentic Setup Without Risky Data

Use a blank or toy folder. Do not use real data.

```text
Inspect this research folder and do not edit files yet.

Report:
1. folder structure;
2. whether README.md, DATA.md, AGENTS.md, AI-USE-LOG.md, and .gitignore exist;
3. what files should never be edited by an agent;
4. first safe task;
5. questions before any edits.
```

Then show the approval gate:

```text
Before editing, give me an approval table:

| Proposed action | Files affected | Why needed | Risk | Verification check | Needs approval? |
| --- | --- | --- | --- | --- | --- |

Wait for approval before editing, running commands, installing packages, or pushing to GitHub.
```

## Audience Exercise: Upload Or Not?

Ask participants to classify each item:

| Material | Usually safe? | Rule |
| --- | --- | --- |
| public paper abstract | usually yes | still cite and verify |
| coauthor draft | only with consent | ask before upload |
| WRDS/CRSP/Compustat extract | usually no for public tools | check license |
| referee report | no unless policy allows | journal rules first |
| toy synthetic data | yes | label as synthetic |
| error message with no private data | often yes | remove paths/secrets |

## Audience Exercise: Match Output To Verification

| AI output | Verification method |
| --- | --- |
| citation claim | DOI/journal/source check |
| merge code | toy data with known answer |
| coefficient interpretation | units and magnitude check |
| event-study paragraph | timing, leads/lags, pre-trends, estimator check |
| proof step | assumptions, limiting cases, notation |
| slide title | compare to actual table/figure and causal design |

## Screenshot Guidance For The HTML Deck

The HTML deck already labels the screenshot slots. Replace them only with public or synthetic screenshots: no private repo names, data paths, paper drafts, coauthor comments, student data, licensed extracts, referee material, or credentials.

## Participant Takeaway Sheet

```text
After this session, do one small thing:

1. Pick one non-confidential research task.
2. Choose one skill from the repo.
3. Define safe inputs.
4. Ask AI for a plan before output.
5. Verify with source, data, code, equation, or slide check.
6. Record what you accepted in an AI-use log.
7. Do not upload restricted, licensed, private, or confidential material without permission.
```

## Q&A Bank

| Question | Short answer |
| --- | --- |
| Can AI write my paper? | It can draft and revise text, but humans own claims, evidence, citations, and responsibility. |
| Can I use AI on referee reports? | Only if journal/conference policy permits it. |
| Can I upload coauthor drafts? | Only with coauthor consent and policy compliance. |
| Do I need GitHub? | If AI edits files, version control is strongly recommended. Private GitHub repos are often the practical starting point. |
| Which tool is best? | It depends on task, date, privacy settings, cost, and verification. Do not make timeless tool rankings. |
| Can AI choose identification? | It can critique and explain designs, but it should not decide causal credibility for you. |
| How should I disclose AI use? | Check journal, university, funder, and coauthor rules; keep an AI-use log so disclosure is possible. |

## Generate A Customized Two-Hour Deck

Copy this if another instructor wants to adapt the deck.

```text
Using this repository as source material, create a two-hour presentation for:
[audience: PhD students / RAs / faculty / finance researchers / applied economists / mixed audience]

Constraints:
- no private or confidential examples;
- no unsupported tool rankings;
- explain technical terms for non-CS scholars;
- include live exercises and verification checks;
- include Git/GitHub safety;
- include one agentic workflow example;
- include data safety and institutional policy warnings.

Return:
1. timed agenda;
2. slide-by-slide outline;
3. speaker notes;
4. live demos;
5. audience exercises;
6. screenshot placeholders;
7. repo links for each major segment;
8. what the presenter must verify before teaching.

If anything is unclear, ask up to five clarifying questions first.
```

## Maintenance Notes

- Update tool-specific claims only with dated checks.
- Keep live demos harmless and reproducible.
- Prefer public examples, synthetic data, screenshots, or toy folders.
- When the handbook changes substantially, update both this Markdown script and the HTML deck.
