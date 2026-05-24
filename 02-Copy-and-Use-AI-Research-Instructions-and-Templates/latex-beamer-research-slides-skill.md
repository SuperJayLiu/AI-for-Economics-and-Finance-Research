> Copyright (c) 2026 SuperJayLiu (Chaojie Liu). Licensed under the repository MIT License.
> This instruction/workflow is original to this repository unless otherwise noted. External inspirations are cited in “Sources and workflow influences.”

# Skill: Traditional LaTeX Beamer Research Slides

## Purpose

Create a traditional LaTeX/Beamer slide deck for economics or finance seminars, job talks, conference presentations, and theory or empirical research talks.

This skill prioritizes academic clarity, equations, tables, citations, and reproducible PDF output.

## Best For

- economics seminars
- finance seminars
- job market talks
- theory presentations
- empirical results presentations
- conference talks requiring PDF
- slides that should live in the paper repository

## Not Suitable For

- highly interactive web presentations
- public-facing visual explainers
- slide decks that must be edited in PowerPoint
- talks requiring complex live animation

## Required Inputs

Provide:

- paper title
- author names and affiliations
- talk type: seminar, conference, job talk, lecture, internal update
- talk length
- target audience
- abstract or paper summary
- core research question
- contribution statement
- model, data, or empirical design summary
- main results
- figures and tables, with file paths if available
- bibliography file or citation style
- preferred Beamer theme constraints, if any

## Optional Inputs

- paper `.tex` source
- existing slide deck
- appendix/backup slide list
- theorem/proposition statements
- table notes
- journal or conference branding requirements

## Workflow

1. Create a talk outline before writing Beamer code.
2. Separate main slides from backup slides.
3. Keep one main idea per slide.
4. Preserve notation, table notes, figure labels, and citation keys.
5. Use concise slide text and speaker notes where needed.
6. Put dense proofs, extra tables, and robustness checks in backup slides.
7. Compile and fix LaTeX errors.
8. Verify claims, citations, equations, and figures against the source paper.

## Output Requirements

- compilable `.tex` Beamer source
- PDF output target
- clear main/backup split
- citations compatible with the project bibliography
- figures/tables referenced by path rather than pasted as unexplained images
- no invented results, citations, or robustness checks

## Verification Checklist

- Does the deck compile?
- Are all equations correct?
- Are all citation keys real?
- Are all figure/table files available?
- Are all results stated consistently with the paper?
- Are causal claims appropriately hedged?
- Are backup slides sufficient for likely questions?

## Sources And Workflow Influences

Draws on academic LaTeX/Beamer presentation practice and AI-assisted research presentation workflows. It is paired with the HTML slide skill for users who need a more interactive and shareable format.

Last checked: 2026-05-24
