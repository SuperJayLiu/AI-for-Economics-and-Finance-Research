> Copyright (c) 2026 SuperJayLiu (Chaojie Liu). Licensed under the repository MIT License.

# Presentations, Slides, Websites, and Talk Practice Skills

These skills are for turning research into usable communication artifacts: interactive HTML slides, traditional LaTeX/Beamer slides, talk practice, and simple academic websites.

> [!TIP]
> Slides are not a decoration task. A good slide workflow converts a paper into a clear sequence of claims, evidence, limits, and audience questions.

> [!NOTE]
> Default add-on for any block on this page: `If any required input, term, method detail, data rule, or output format is unclear, ask me up to five clarifying questions before giving the final output. Define unfamiliar technical terms in plain language and end with "Questions for you" if anything remains uncertain.`

## Choose a Skill

| Need | Use |
| --- | --- |
| web-native interactive slides | Skill 1 |
| traditional academic slides | Skill 2 |
| practice Q&A | Skill 3 |
| academic website | Skill 4 |
| convert a paper into a talk plan before making slides | Skill 5 |

## Skill 1: Interactive HTML Research Slides

Use for shareable, interactive, web-native slides.

```text
Create an interactive single-file HTML slide deck for an economics/finance research presentation.

Inputs:
- Paper title: [title]
- Audience: [seminar/conference/class/public]
- Talk length: [minutes]
- Research question: [question]
- Setting/data: [setting and data]
- Method/design/model: [method]
- Main results: [verified results]
- Figures/tables to include: [list]
- Tone: [academic/public/teaching]
- Visual style: [clean academic / interactive mechanism / finance dashboard / teaching explainer]
- Interaction style: [timeline / mechanism diagram / data explorer / animated equation / policy dashboard / no interaction]

Requirements:
1. Use one self-contained HTML file unless external assets are necessary.
2. Include keyboard navigation.
3. Use interactive elements only when they clarify mechanism, identification, data, or results.
4. Avoid generic AI aesthetics.
5. Keep text readable on projector and laptop.
6. Include speaker notes as HTML comments or hidden notes.
7. Include a final "limitations and Q&A" section.
8. Include a visual preview plan before writing final HTML.
9. Prevent text overflow; split dense slides rather than shrinking everything.
10. Make any simulated visual clearly labeled as illustrative.

Recommended deck structure:
1. title and one-sentence question
2. motivation and why the audience should care
3. setting, institution, or model
4. data or mechanism visual
5. empirical design or theoretical logic
6. main result
7. robustness or alternative explanations
8. limits
9. takeaway and Q&A

Do not:
- invent figures or results
- change chart labels, units, or legends
- overstate causal interpretation
- deploy unpublished work publicly without approval

Return:
- slide-by-slide plan
- visual style choices
- HTML file content
- manual verification checklist
```

## Skill 2: Traditional LaTeX/Beamer Research Slides

Use for standard academic seminars and conferences.

```text
Create a LaTeX Beamer slide deck for an economics/finance research talk.

Inputs:
- Paper title: [title]
- Authors: [authors]
- Event/audience: [event]
- Talk length: [minutes]
- Research question: [question]
- Motivation: [motivation]
- Data: [data]
- Empirical strategy/model: [method]
- Main results: [verified results]
- Figures/tables: [files or descriptions]
- Style preference: [plain professional / journal seminar / teaching]
- Beamer theme preference: [default/simple/custom institution theme]

Output:
1. A complete `main.tex` Beamer file.
2. Slide outline:
   - title
   - motivation
   - question
   - setting/data
   - method/design/model
   - main results
   - robustness/limitations
   - contribution
   - conclusion/Q&A
3. Speaker-note bullets below each slide as comments.
4. Figure placeholders with clear filenames.
5. A backup slide plan for robustness, data details, and extra results.

Rules:
- Do not fabricate results.
- Use concise slide text.
- Preserve mathematical notation.
- Make limitations visible.
- Use comments for speaker notes and verification reminders.

Suggested LaTeX packages only if needed:
- `amsmath`
- `booktabs`
- `graphicx`
- `appendixnumberbeamer`
```

## Skill 3: Practice My Presentation With AI

```text
Act as a tough but fair seminar audience for my economics/finance talk.

Inputs:
- Talk title: [title]
- Abstract: [abstract]
- Slide outline or slides: [paste/upload]
- Audience: [field seminar/conference/job talk/PhD workshop]
- Main claim: [claim]
- Weakest part: [what worries me]

Run a presentation practice session:
1. Ask 10 likely audience questions.
2. Ask 5 hostile-but-fair questions.
3. Ask 5 clarification questions.
4. Identify where the talk overclaims.
5. Identify missing institutional, data, or identification details.
6. Draft concise answers.
7. Suggest slide changes.

Rules:
- Do not flatter.
- Do not invent answers.
- If an answer requires evidence, say what evidence is needed.
- Separate "answer now" from "need to check before seminar".
```

## Skill 4: Personal Academic Website From GitHub or Google Sites

```text
Help me create a simple academic website.

Inputs:
- Name: [name]
- Position: [position]
- Fields: [fields]
- Email/contact: [contact]
- Google Scholar/SSRN/ORCID/GitHub: [links]
- Working papers: [titles, abstracts, links]
- Publications: [citations, links]
- Teaching: [courses]
- CV: [link or file]
- Preferred platform: [GitHub Pages / Google Sites]

Produce:
1. Site structure.
2. Homepage text.
3. Research page text.
4. Teaching page text.
5. Contact section.
6. GitHub Pages README or Google Sites build checklist.
7. Maintenance checklist.

Rules:
- Professional academic tone.
- No marketing fluff.
- Do not invent publications or affiliations.
```

## Skill 5: Paper-to-Talk Converter

Use this before making slides.

```text
Turn this economics/finance paper into a talk plan before creating slides.

Inputs:
- Paper title: [title]
- Abstract: [abstract]
- Introduction or summary: [paste]
- Methods/model: [paste]
- Main results: [paste]
- Audience: [job talk / field seminar / conference / PhD workshop / public policy / teaching]
- Talk length: [minutes]
- My main concern: [concern]

Create:
1. one-sentence talk thesis;
2. audience-specific hook;
3. slide sequence with minutes per section;
4. what to show visually on each slide;
5. which tables/figures should be simplified;
6. where to state limitations;
7. likely questions and where to answer them in the deck;
8. what should go to backup slides.

Rules:
- Do not rewrite results.
- Do not invent visuals.
- Do not hide limitations.
- Keep the talk centered on the research question, design/model, and evidence.
```

Sources and workflow influences: Zara Zhang's frontend slide work, SlideCraft-style workflow ideas, and academic presentation practices. Adapted here for economics and finance research communication.
