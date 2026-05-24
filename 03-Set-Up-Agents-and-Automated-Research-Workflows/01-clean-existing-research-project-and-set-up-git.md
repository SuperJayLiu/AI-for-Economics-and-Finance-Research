# Clean Existing Research Project and Set Up Git

Use this when a research folder has scattered files, unclear data lineage, manual copies, and no safe version control.

> [!NOTE]
> Default add-on for this workflow: `If any required input, file permission, data rule, Git term, agent permission, or output format is unclear, ask me up to five clarifying questions before acting. Define unfamiliar technical terms in plain language and end with "Questions for you" if anything remains uncertain.`

## Copy-Paste Agent Instruction

```text
I want your help cleaning up this research project and setting up a Git repo safely.

Project folder: [path]
Research topic: [topic]
Software used: [Stata/R/Python/Matlab/LaTeX/etc.]
Data sensitivity: [public/licensed/restricted/private/unknown]
Remote repo preference: [private GitHub repo / local only / not sure]

Phase 1: Inspect only.
- List files and folders.
- Identify likely raw data, derived data, scripts, outputs, paper files, slides, and temporary files.
- Identify privacy/license risks.
- Suggest a `.gitignore`.
- Suggest a clean folder structure.
- Suggest what should be backed up.
- Do not move, edit, delete, or commit anything yet.

Phase 2: After I approve.
- Create a backup copy.
- Initialize Git if needed.
- Add README.md, DATA.md, AGENTS.md, and AI-USE-LOG.md.
- Commit the original state.
- Create a restructuring branch.
- Move files into approved folders.
- Update paths only where necessary.
- Run modified scripts and compare outputs.
- Commit the restructured state.

Rules:
- Never edit raw data.
- Never commit private, restricted, or licensed data.
- Never push to a public repo.
- Ask before installing packages.
- Ask up to five clarifying questions before acting if the project folder, data sensitivity, remote repo choice, or software environment is unclear.
- Define technical terms such as `.gitignore`, branch, commit, diff, and raw data in plain language when they first appear.
- Report commands run and checks performed.
```

## Recommended Folder Structure

```text
project/
  README.md
  AGENTS.md
  DATA.md
  AI-USE-LOG.md
  data/
    raw/
    derived/
  code/
  output/
    tables/
    figures/
  paper/
  slides/
```

## Success Criteria

- raw data is untouched
- private data is ignored
- code paths still work
- tables/figures can be rebuilt
- Git history shows original state and restructuring
- AI-use log records what changed

Sources and workflow influences: Paul Goldsmith-Pinkham's Claude Code research workflow discussions and Git-centered AI coding advice; official Git/GitHub documentation.
