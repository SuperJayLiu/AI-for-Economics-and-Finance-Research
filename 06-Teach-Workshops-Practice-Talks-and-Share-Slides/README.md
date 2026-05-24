# Teach Workshops, Practice Talks, and Share Slides

This folder is for instructors, PIs, PhD organizers, and seminar leaders who want to teach the material.

> [!TIP]
> Treat every workshop as a live workflow-design session. Participants should leave with one usable project instruction, one skill, and one verification rule for their own research.

## Use This Folder For

| Goal | Use |
| --- | --- |
| teach a 90-minute introduction | Two-session workshop, Session 1 only |
| teach a half-day workshop | both sessions plus live skill-building |
| onboard RAs | RA onboarding checklist |
| prepare a seminar or job talk | presentation practice activity |
| make shareable material | slide-ready outline and HTML/Beamer skills |

## Two-Session Workshop

### Session 1: Foundations

Goal: help scholars understand what AI can and cannot do.

Agenda:
1. AI is not evidence.
2. LLMs, projects, skills, agents, MCPs.
3. Data safety and confidentiality.
4. Literature review without fake citations.
5. Empirical methods drafting and checking.
6. AI-use logs and disclosure.

Exercise:

```text
Take one research task you do repeatedly. Convert it into:
1. purpose
2. safe inputs
3. AI instruction
4. expected output
5. verification checklist
```

Live demo:

```text
Pick a harmless task such as summarizing a public abstract or rewriting a methods paragraph.
Ask AI to do it casually.
Then rerun the task with purpose, inputs, rules, output contract, and verification checklist.
Compare the two outputs.
```

### Session 2: Applied Workflows

Goal: help scholars build a safe workflow.

Agenda:
1. One paper, one repo, one AI project.
2. GitHub safety and `.gitignore`.
3. AGENTS.md and project instructions.
4. Replication-package agent workflow.
5. Presentation practice with AI.
6. Staying updated without hype.

Exercise:

```text
Create a safe AI project setup for one paper:
- project instructions
- folder structure
- data rules
- AI-use log
- first skill to create
- first verification check
```

Live demo:

```text
Take a messy mock research folder.
Ask AI to propose a Git-safe reorganization plan.
Reject any plan that changes raw data, deletes files, or skips verification.
Then show how a branch or worktree isolates the experiment.
```

## Slide-Ready Outline

```text
Title: AI for Economics and Finance Research

1. The promise and danger
2. Why AI output is not evidence
3. Research workflow maturity ladder
4. What AI can help with
5. What not to automate
6. Data safety matrix
7. Skills, projects, agents, MCPs
8. GitHub as research safety infrastructure
9. Copy-ready workflows
10. Failure cases
11. Building your own AI research system
12. Q&A and live workflow design
```

## Workshop Handout: One-Page Rules

```text
1. AI output is not evidence.
2. Never trust generated citations.
3. If AI can edit files, use Git.
4. If data is private, licensed, restricted, or confidential, do not upload it without permission.
5. Plan before execution.
6. Turn repeated tasks into skills.
7. Keep an AI-use log.
8. Check code, tables, equations, and citations against original sources.
9. Use dated tool claims.
10. Automate only when verification is stronger than automation.
```

## RA Onboarding Checklist

```text
Before an RA uses AI on a project:
- read project README
- read DATA.md
- read AGENTS.md
- confirm data privacy rules
- set up Git
- understand branch workflow
- know what files never to edit
- know how to log AI use
- run one small reproducibility check
- ask before uploading or sharing drafts
```

## RA First Assignment

```text
Create a safe project orientation note for this research project.

Use only the files and rules provided by the PI.

Include:
1. project purpose
2. folder map
3. data sensitivity rules
4. files never to edit
5. how to run the main code
6. how to record AI use
7. first reproducibility check
8. questions for the PI
```

## Presentation Practice Activity

Use the [presentation practice skill](../02-Copy-and-Use-AI-Research-Instructions-and-Templates/06-presentations-slides-websites-and-talk-practice-skills.md#skill-3-practice-my-presentation-with-ai).

Ask each participant to prepare:

- one-slide research question
- one-slide design/data
- one-slide main result
- one-slide limitation

Then have AI generate tough questions and require human answers.

## Slide-Building Exercise

Use both slide styles so participants see the tradeoff.

| Slide style | Exercise | Best for |
| --- | --- | --- |
| HTML interactive | create an animated mechanism, event timeline, or data-flow slide | teaching, online sharing, public explainers |
| LaTeX/Beamer | create a standard seminar deck with equations, tables, and limitations | conferences, job talks, academic seminars |

Prompt:

```text
Take this paper abstract and results summary.
Create two presentation plans:
1. an interactive HTML explainer deck;
2. a traditional LaTeX Beamer seminar deck.

For each, explain:
- target audience
- slide sequence
- what interaction or equation belongs where
- what claims must be verified
- where limitations should be shown
```
