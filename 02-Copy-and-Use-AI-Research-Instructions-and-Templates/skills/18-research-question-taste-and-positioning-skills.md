> Copyright (c) 2026 SuperJayLiu (Chaojie Liu). Licensed under the repository MIT License.

# Research Question, Taste, and Positioning Skills

Use these skills before execution. AI makes coding, drafting, tables, and slides cheaper. That makes question choice, taste, data quality, identification, institutional knowledge, and contribution more important.

> [!IMPORTANT]
> These skills do not let AI decide what is worth studying. They help you make your own judgment more explicit, testable, and discussable with advisors, coauthors, and seminar audiences.

Questions or suggestions for this part: email [jay.liu@bristol.ac.uk](mailto:jay.liu@bristol.ac.uk) with subject `[AI Econ Finance Taste Skill] Suggestion`.

> [!NOTE]
> Import/use-as-skill protocol for any block on this page: `Start by collecting only the missing inputs needed for the task. Ask up to five clarifying questions when required inputs, data rules, method details, permissions, audience, or output format are unclear. For long outputs, file-producing tasks, slides, code, methods sections, literature reviews, referee responses, or agentic workflows, first return "Proposed structure and assumptions" and ask the user to confirm before producing the full output. Before finalizing, double-check for unsupported claims, invented citations or results, privacy risks, and mismatch with the requested format. End with "What I produced", "What I did not change", "What you must verify", and "Questions for you".`

## Choose a Skill

| Need | Use |
| --- | --- |
| turn a broad topic into a sharp question | Skill 1 |
| identify competing mechanisms | Skill 2 |
| position against closest papers by design/model | Skill 3 |
| ask the "so what?" question rigorously | Skill 4 |
| decide whether AI is worth using for a task | Skill 5 |

## Skill 1: Topic-to-Tension Research Question Builder

```text
Act as a skeptical economics/finance research advisor.

Broad topic:
[topic]

Current idea:
[one paragraph]

Possible setting/data:
[setting/data]

Target audience:
[field seminar/top field journal/PhD proposal/policy audience/etc.]

Turn this topic into sharper research questions by identifying:
1. a real economic or financial tension;
2. two or more mechanisms that make different predictions;
3. the unit of analysis and variation needed;
4. what data would make the question answerable;
5. what result would surprise a knowledgeable reader;
6. why the question matters beyond this setting.

Return:
- five candidate research questions;
- for each, the mechanism, data need, identification challenge, and "so what";
- one recommended narrow version;
- one ambitious version;
- what I must read or verify before proceeding.

Rules:
- Do not claim novelty.
- Do not flatter the idea.
- Do not choose a question because data is easy if the economic stakes are weak.
- Mark speculative claims as speculative.
```

## Skill 2: Two-Mechanism Competition Builder

```text
Help me sharpen this paper around competing mechanisms.

Current question:
[question]

Setting:
[setting]

Observed pattern or proposed result:
[pattern/result]

Candidate mechanisms:
[list or say unknown]

Produce:
1. at least two mechanisms that could explain the pattern;
2. what each mechanism predicts;
3. empirical moments or tests that distinguish them;
4. variables or institutional facts needed;
5. theory or model implication if relevant;
6. what result would be hard for each mechanism to explain.

Return:
- mechanism comparison table;
- proposed figure/table that would distinguish mechanisms;
- paragraph framing the research tension;
- risk that this is only a descriptive pattern.

Rules:
- Do not make up evidence.
- Do not assume the author's preferred mechanism is correct.
- Do not turn mechanism discussion into causal proof.
```

## Skill 3: Closest-Paper Positioning by Design, Not Topic

```text
Audit my contribution claim against the closest papers.

My project:
- Question: [question]
- Setting/data: [setting/data]
- Design/model: [design/model]
- Main intended contribution: [claim]

Closest papers I know:
[paste citations/notes]

Compare my project to the closest papers by:
1. research question;
2. identification strategy or model;
3. data and measurement;
4. mechanism;
5. external validity;
6. result or prediction;
7. limitation.

Return:
- closest-paper table;
- contribution claims that are too broad;
- sharper contribution claims;
- missing papers or literatures to search;
- one paragraph I could use in an introduction after verification.

Rules:
- Do not say "no one has studied" unless the supplied sources prove it.
- Treat papers as close if they share design/model/variation, not only if they share topic words.
- Mark every unsupported claim as [VERIFY].
```

## Skill 4: The "So What?" Test

```text
Apply a strict "so what?" test to this economics/finance project.

Project summary:
[summary]

Intended audience:
[audience]

Main result or expected result:
[result]

Evaluate:
1. Why should economists or finance scholars care?
2. What belief, model, policy, or empirical practice would change?
3. Is the effect economically large enough to matter?
4. Is the setting important or just convenient?
5. Does the result generalize, or is the value in the case itself?
6. What would a skeptical seminar participant say is missing?
7. What is the strongest honest version of the contribution?

Return:
- one-sentence "so what";
- three possible contribution frames;
- weakest part of each frame;
- evidence needed to make the frame credible;
- sentences to avoid.
```

## Skill 5: AI Cost-Benefit Decision Rule for a Research Task

```text
Decide whether I should use AI for this research task.

Task:
[task]

Context:
- Stakes: [notes/draft/submission/public output]
- Confidentiality: [public/private/licensed/restricted]
- Can I verify the output? [yes/no/how]
- Estimated time to do manually: [time]
- Estimated time to prompt/check: [time]
- Risk if wrong: [low/medium/high]
- Reuse potential: [one-off/repeated]

Evaluate:
1. labor saved;
2. setup cost;
3. verification cost;
4. privacy/security risk;
5. maintenance cost;
6. reuse potential.

Return:
- decision: use AI / do manually / use AI only on toy or synthetic example / use only approved local tool;
- reasoning;
- safe prompt if AI is appropriate;
- verification checklist;
- what not to automate.

Decision rule:
Use AI only if labor saved is greater than setup cost plus verification cost plus privacy risk plus future maintenance cost.
```

## Sources and Workflow Influences

This page adapts research-advisor, top-journal-introduction, proposal-building, and theory-discussant workflows into direct-use prompts for research taste and positioning.

Last checked: 2026-05-24
