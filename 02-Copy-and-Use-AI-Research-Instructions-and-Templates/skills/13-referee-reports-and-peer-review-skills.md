> Copyright (c) 2026 SuperJayLiu (Chaojie Liu). Licensed under the repository MIT License.

# Referee Reports and Peer Review Skills

Use these skills for self-review, journal referee reports, response letters, and GitHub-style feedback handling.

> [!IMPORTANT]
> Do not upload confidential manuscripts, referee reports, editorial letters, or private comments to AI tools unless the journal, conference, institution, and tool privacy rules allow it.

Questions or suggestions for this part: email [jay.liu@bristol.ac.uk](mailto:jay.liu@bristol.ac.uk) with subject `[AI Econ Finance Peer Review Skill] Suggestion`.

> [!NOTE]
> Import/use-as-skill protocol for any block on this page: `Start by collecting only the missing inputs needed for the task. Ask up to five clarifying questions when required inputs, data rules, method details, permissions, audience, or output format are unclear. For long outputs, file-producing tasks, slides, code, methods sections, literature reviews, referee responses, or agentic workflows, first return "Proposed structure and assumptions" and ask the user to confirm before producing the full output. Before finalizing, double-check for unsupported claims, invented citations or results, privacy risks, and mismatch with the requested format. End with "What I produced", "What I did not change", "What you must verify", and "Questions for you".`

## Choose a Skill

| Need | Use |
| --- | --- |
| review your own paper before submission | Skill 1 |
| plan a response to referees | Skill 2 |
| draft a referee report when policy allows AI use | Skill 3 |
| triage PR/GitHub-style comments | Skill 4 |

## Skill 1: Staged Self-Review Before Submission

```text
Review this economics/finance paper draft in stages.

Draft:
[paste or summarize]

Context:
- Field: [field]
- Target: [journal/seminar/dissertation/etc.]
- Stage: [early draft / submission draft / revision]
- Main concern: [concern]

Review order:
1. research question and contribution;
2. identification/model credibility;
3. evidence and interpretation;
4. structure and flow;
5. literature positioning;
6. writing clarity;
7. grammar and mechanics last.

Return:
- paper understanding check
- what is working
- top 3-5 revision priorities
- passage-specific comments
- next-step revision plan

Rules:
- Do not rewrite the whole paper.
- Do not verify citations unless sources are supplied.
- Do not smooth weak reasoning with prettier prose.
```

## Skill 2: Journal Referee Response Planner

```text
Help me plan a journal revision response.

Inputs:
- Paper summary: [summary]
- Editor letter: [paste]
- Referee reports: [paste]
- Constraints: [data/code/time/coauthor constraints]
- New results already available: [if any]

Tasks:
1. Cluster comments by theme.
2. Separate fatal, major, minor, misunderstanding, and optional comments.
3. Identify repeated concerns across referees.
4. Create a revision plan by section/table/figure.
5. Identify analyses that are feasible, infeasible, or risky.
6. Draft response-letter structure.
7. Identify where to concede and where to respectfully disagree.
8. Identify claims that must be softened.

Rules:
- Do not promise analyses not yet run.
- Do not invent new results.
- Keep tone professional and precise.
```

## Skill 3: Referee Report Drafting Aid

```text
Help me structure a referee report for an economics/finance paper, only if AI use is allowed by the relevant policy.

Paper:
[paste summary or allowed excerpts]

Review focus:
[identification/theory/data/writing/contribution/etc.]

Create:
1. short summary of the paper's question and contribution;
2. major comments ranked by importance;
3. minor comments;
4. specific questions for authors;
5. recommendation logic without making the final decision for me.

Rules:
- Do not upload or process confidential material unless allowed.
- Do not invent facts about the paper.
- Be constructive but not soft.
- Separate fatal problems from repairable weaknesses.
```

## Skill 4: GitHub-Style Review Comment Triage

Use for research repos, replication packages, and collaborative writing tracked through GitHub.

```text
Triage these review comments on a research repo or paper PR.

Comments:
[paste comments]

Project context:
[context]

Tasks:
1. Group comments by file, behavior area, or paper section.
2. Separate actionable requests from informational comments, duplicates, and already-resolved issues.
3. Identify conflicts between comments.
4. Propose an implementation order.
5. For each actionable comment, say whether it needs code, text, data, documentation, or reply-only action.
6. Draft concise replies for ambiguous comments.

Rules:
- Do not mark anything resolved unless I ask.
- Do not push or reply publicly without approval.
- Keep every change traceable to a comment cluster.
```

Sources and workflow influences: the repository author's paper-review and GitHub comment-handling skills, journal revision practice, and GitHub PR review safety workflows.
