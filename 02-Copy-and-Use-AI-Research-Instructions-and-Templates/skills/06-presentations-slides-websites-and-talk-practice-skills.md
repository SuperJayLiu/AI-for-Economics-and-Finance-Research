> Copyright (c) 2026 SuperJayLiu (Chaojie Liu). Licensed under the repository MIT License.

# Presentations, Slides, Websites, and Talk Practice Skills

These skills are for turning research into usable communication artifacts: interactive HTML slides, traditional LaTeX/Beamer slides, talk practice, and simple academic websites.

> [!TIP]
> Slides are not a decoration task. A good slide workflow converts a paper into a clear sequence of claims, evidence, limits, and audience questions.

> [!NOTE]
> Import/use-as-skill protocol for any block on this page: `Start by collecting only the missing inputs needed for the task. Ask up to five clarifying questions when required inputs, data rules, method details, permissions, audience, or output format are unclear. For long outputs, file-producing tasks, slides, code, methods sections, literature reviews, referee responses, or agentic workflows, first return "Proposed structure and assumptions" and ask the user to confirm before producing the full output. Before finalizing, double-check for unsupported claims, invented citations or results, privacy risks, and mismatch with the requested format. End with "What I produced", "What I did not change", "What you must verify", and "Questions for you".`

## Choose a Skill

| Need | Use |
| --- | --- |
| full paper or full materials, but slide structure is not confirmed yet | Skill 0 |
| web-native interactive slides after structure is confirmed | Skill 1 |
| traditional academic slides after structure is confirmed | Skill 2 |
| practice Q&A | Skill 3 |
| academic website | Skill 4 |
| convert a paper into a talk plan before making slides | Skill 5 |

## Skill 0: Full-Materials Presentation Intake and Structure Confirmation

Use this before creating any full slide deck from a paper, draft, replication package, figures, tables, or mixed materials. The goal is to confirm the presentation type, structure, and evidence before asking AI to produce HTML or Beamer slides.

```text
Use this as an imported presentation-intake skill for an economics/finance research project.

Task:
I will provide full paper materials, partial materials, or supporting files. Do not create the final slide deck yet. First inspect the materials and return "Proposed structure and assumptions" for my confirmation.

Materials I am providing:
- Full paper or draft: If I have not provided it, ask me to specify: paste/upload/link/none
- Abstract and introduction: If I have not provided it, ask me to specify: paste/upload/link/none
- Methods/model section: If I have not provided it, ask me to specify: paste/upload/link/none
- Results, tables, figures, or appendix: If I have not provided it, ask me to specify: paste/upload/link/none
- Existing slides or notes: If I have not provided it, ask me to specify: paste/upload/link/none
- Target talk date/event: If I have not provided it, ask me to specify: event
- Confidentiality status: If I have not provided it, ask me to specify: public / coauthor draft / unpublished / restricted / unknown

Presentation type to consider:
- academic seminar
- job talk
- conference talk
- PhD workshop or brown-bag
- professional/policy audience
- teaching session
- public-facing research summary
- internal coauthor/RA update

Possible output format:
- interactive single-file HTML slides
- LaTeX Beamer slides
- PowerPoint outline only
- talk plan only, no slides yet
- not sure; recommend format

Before producing a deck, ask up to five clarifying questions if any of these are unclear:
1. audience and expected technical level;
2. talk length and number of slides;
3. required format, template, or institutional style;
4. which claims, tables, figures, or results are verified;
5. which materials are confidential or should not be shown.

Return only this pre-slide plan:
1. Material inventory: what I provided and what is missing.
2. Recommended presentation type and format, with reason.
3. Proposed deck structure with section titles and approximate timing.
4. Core research narrative in one paragraph.
5. Must-use figures/tables and why.
6. Figures/tables to simplify, move to backup, or omit.
7. Claims that need evidence before appearing on slides.
8. Privacy, coauthor, data-license, or disclosure issues.
9. Backup-slide plan.
10. Questions for you.

Stop after the pre-slide plan and wait for my confirmation. Do not generate HTML, Beamer, or final slide text until I confirm the structure and format.
```

## Skill 1: Interactive HTML Research Slides

Use for shareable, interactive, web-native slides.

```text
Create an interactive single-file HTML slide deck for an economics/finance research presentation after the presentation structure has been confirmed.

Inputs:
- Confirmed deck structure: If I have not provided it, ask me to specify: paste the approved structure from Skill 0, or say "not confirmed"
- Paper title: If I have not provided it, ask me to specify: title
- Audience: If I have not provided it, ask me to specify: seminar/conference/class/public
- Talk length: If I have not provided it, ask me to specify: minutes
- Research question: If I have not provided it, ask me to specify: question
- Setting/data: If I have not provided it, ask me to specify: setting and data
- Method/design/model: If I have not provided it, ask me to specify: method
- Main results: If I have not provided it, ask me to specify: verified results
- Figures/tables to include: If I have not provided it, ask me to specify: list
- Tone: If I have not provided it, ask me to specify: academic/public/teaching
- Visual style: If I have not provided it, ask me to specify: clean academic / interactive mechanism / finance dashboard / teaching explainer
- Interaction style: If I have not provided it, ask me to specify: timeline / mechanism diagram / data explorer / animated equation / policy dashboard / no interaction

If the deck structure or format has not been confirmed, do not write the final HTML yet. First return "Proposed structure and assumptions" and ask me to confirm.

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
11. Use interactive elements to teach the economics/finance logic: mechanism, timeline, treatment timing, portfolio construction, event window, model intuition, data pipeline, or robustness comparison.
12. Keep animations purposeful and slow enough for a seminar room.

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
1. Proposed structure and assumptions, if not already confirmed.
2. Slide-by-slide plan.
3. Visual style choices.
4. Full HTML file content.
5. Manual verification checklist.
6. What I produced.
7. What I did not change.
8. What you must verify.
9. Questions for you.

Before finalizing, double-check that every claim is traceable to the paper, table, figure, model, or supplied note; that no confidential material is exposed; and that the deck format matches the confirmed presentation type.
```

## Skill 2: Traditional LaTeX/Beamer Research Slides

Use for standard academic seminars and conferences.

```text
Create a LaTeX Beamer slide deck for an economics/finance research talk after the presentation structure has been confirmed.

Inputs:
- Confirmed deck structure: If I have not provided it, ask me to specify: paste the approved structure from Skill 0, or say "not confirmed"
- Paper title: If I have not provided it, ask me to specify: title
- Authors: If I have not provided it, ask me to specify: authors
- Event/audience: If I have not provided it, ask me to specify: event
- Talk length: If I have not provided it, ask me to specify: minutes
- Research question: If I have not provided it, ask me to specify: question
- Motivation: If I have not provided it, ask me to specify: motivation
- Data: If I have not provided it, ask me to specify: data
- Empirical strategy/model: If I have not provided it, ask me to specify: method
- Main results: If I have not provided it, ask me to specify: verified results
- Figures/tables: If I have not provided it, ask me to specify: files or descriptions
- Style preference: If I have not provided it, ask me to specify: plain professional / journal seminar / teaching
- Beamer theme preference: If I have not provided it, ask me to specify: default/simple/custom institution theme

If the deck structure or format has not been confirmed, do not write the final Beamer file yet. First return "Proposed structure and assumptions" and ask me to confirm.

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
4. Figure-needed markers with clear filenames.
5. A backup slide plan for robustness, data details, and extra results.
6. A claim-to-evidence checklist for the main slides.
7. A short "What you must verify" list.

Rules:
- Do not fabricate results.
- Use concise slide text.
- Preserve mathematical notation.
- Make limitations visible.
- Use comments for speaker notes and verification reminders.
- Preserve the confirmed presentation type: academic seminar, job talk, conference talk, professional/policy talk, teaching, public summary, or internal update.
- For equations and tables, prefer clarity over completeness; move dense derivations and robustness tables to backup slides.

Suggested LaTeX packages only if needed:
- `amsmath`
- `booktabs`
- `graphicx`
- `appendixnumberbeamer`

Before finalizing, double-check that every claim is traceable to the paper, table, figure, model, or supplied note; that notation is consistent; that no confidential material is exposed; and that the deck format matches the confirmed presentation type.

End with:
1. What I produced.
2. What I did not change.
3. What you must verify.
4. Questions for you.
```

## Skill 3: Practice My Presentation With AI

```text
Act as a tough but fair seminar audience for my economics/finance talk.

Inputs:
- Talk title: If I have not provided it, ask me to specify: title
- Abstract: If I have not provided it, ask me to specify: abstract
- Slide outline or slides: If I have not provided it, ask me to specify: paste/upload
- Audience: If I have not provided it, ask me to specify: field seminar/conference/job talk/PhD workshop
- Main claim: If I have not provided it, ask me to specify: claim
- Weakest part: If I have not provided it, ask me to specify: what worries me

Run a presentation practice session:
0. If audience, time, main claim, or slide materials are missing, ask clarifying questions before beginning.
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
- End with "What I produced", "What I did not change", "What you must verify", and "Questions for you".
```

## Skill 4: Personal Academic Website From GitHub or Google Sites

```text
Help me create a simple academic website.

Inputs:
- Name: If I have not provided it, ask me to specify: name
- Position: If I have not provided it, ask me to specify: position
- Fields: If I have not provided it, ask me to specify: fields
- Email/contact: If I have not provided it, ask me to specify: contact
- Google Scholar/SSRN/ORCID/GitHub: If I have not provided it, ask me to specify: links
- Working papers: If I have not provided it, ask me to specify: titles, abstracts, links
- Publications: If I have not provided it, ask me to specify: citations, links
- Teaching: If I have not provided it, ask me to specify: courses
- CV: If I have not provided it, ask me to specify: link or file
- Preferred platform: If I have not provided it, ask me to specify: GitHub Pages / Google Sites

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
- If the platform, audience, or public/private status is unclear, ask clarifying questions before drafting final text.
- End with "What I produced", "What I did not change", "What you must verify", and "Questions for you".
```

## Skill 5: Paper-to-Talk Converter

Use this before making slides.

```text
Turn this economics/finance paper into a talk plan before creating slides.

Inputs:
- Paper title: If I have not provided it, ask me to specify: title
- Abstract: If I have not provided it, ask me to specify: abstract
- Introduction or summary: If I have not provided it, ask me to specify: paste
- Methods/model: If I have not provided it, ask me to specify: paste
- Main results: If I have not provided it, ask me to specify: paste
- Audience: If I have not provided it, ask me to specify: job talk / field seminar / conference / PhD workshop / public policy / teaching
- Talk length: If I have not provided it, ask me to specify: minutes
- My main concern: If I have not provided it, ask me to specify: concern

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
- If the talk format, audience, length, or verified results are unclear, first return "Proposed structure and assumptions" and ask me to confirm.
- Before finalizing, double-check that every slide claim can be traced to supplied materials.
- End with "What I produced", "What I did not change", "What you must verify", and "Questions for you".
```

Sources and workflow influences: Zara Zhang's frontend slide work, SlideCraft-style workflow ideas, and academic presentation practices. Adapted here for economics and finance research communication.
