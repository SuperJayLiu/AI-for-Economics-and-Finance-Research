# Repository Reference and Maintenance

Open this folder only when you need repository-level reference files. This README explains what is stored here; the detailed maintenance files live inside [`reference-files/`](reference-files/) so ordinary readers can ignore them and use the handbook, skills, workflows, examples, sources, and teaching material first.

## What Moved Here

| Need | File |
| --- | --- |
| Cite this repository | [How To Cite](reference-files/HOW-TO-CITE.md) |
| Contribute corrections or additions | [Contributing](reference-files/CONTRIBUTING.md) |
| Review quality standards | [Review Standards](reference-files/REVIEW-STANDARDS.md) |
| See release and editing history | [Changelog](reference-files/CHANGELOG.md) |
| See planned structure | [Roadmap](reference-files/ROADMAP.md) |
| Older English quick-start page | [Start Here English](reference-files/START-HERE.en.md) |
| Older Chinese quick-start page | [Start Here Chinese](reference-files/START-HERE.zh.md) |
| Older English learning paths page | [Learning Paths English](reference-files/LEARNING-PATHS.en.md) |
| Older Chinese learning paths page | [Learning Paths Chinese](reference-files/LEARNING-PATHS.zh.md) |
| Old short scaffold pages | [Archived Old Pages](reference-files/archived-old-pages/) |

## Why This Folder Exists

The main repository page should leave readers with only the README and the main action folders. Maintenance files are still available, but they should not distract new readers from the usable content.

## Editing Rule

When adding new repository-level files, put them here unless ordinary readers must open them before using the handbook or templates.

## Reader-Facing Quality Checklist

Use this before each public release or major content pass.

```text
[ ] Root README roadmaps and card tables are readable in GitHub preview.
[ ] Main folder READMEs start with what is inside the folder and how to use it.
[ ] Detailed files are nested under one subfolder when a top folder has many pages.
[ ] Reader pages avoid maintainer-facing implementation notes.
[ ] Copy-ready skills state required inputs, expected output, verification, and clarification behavior.
[ ] Copy-ready skills ask clarifying questions when inputs, terms, data rules, permissions, or output format are unclear.
[ ] Copy-ready skills ask AI to state what changed, what did not change, and what the scholar must verify.
[ ] Tool claims have a date or are phrased as task-specific examples rather than timeless rankings.
[ ] Dataset advice mentions access type, confidentiality, license or provider rules, and safer AI inputs.
[ ] Source links are grouped by reader task, not only by author name.
[ ] Chinese pages include Chinese explanations, with technical English terms kept where useful.
[ ] Teaching materials use public or synthetic examples only.
```

## Manual Release Checklist

```text
Before tagging a release:
1. Run `git status`.
2. Run `git diff --check`.
3. Search for visible reader-language problems: maintainer notes, draft markers, and unsupported "best tool" claims without a date.
4. Count skill/template/role headings and confirm the toolbox index still matches.
5. Open the root README, 01, 02, 03, 05, and 06 in GitHub preview.
6. Check that no restricted, licensed, private, or confidential example data is included.
7. Update the changelog and release notes.
```
