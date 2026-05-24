# Data Sensitivity Matrix

## What Problem This Solves

Economics and finance researchers work with very different data types. AI upload decisions should depend on data sensitivity, licenses, and institutional policy.

| Data or material | AI use risk | Rule |
| --- | ---: | --- |
| Public macro data | Low | Usually okay; cite sources and document transformations |
| Public paper PDFs | Low-medium | Check copyright and tool policy |
| WRDS, Compustat, CRSP extracts | Medium-high | Check license before upload |
| Bank transaction data | High | Do not upload to public tools |
| Administrative microdata | High | Restricted environment only |
| Unpublished coauthor draft | Medium-high | Get coauthor consent |
| Referee report or manuscript | High | Only if journal policy allows |
| Student data | High | Avoid public AI tools |
| Proprietary firm data | High | Do not upload without explicit approval |

## Safer Alternatives

- use synthetic data
- upload data dictionaries only
- summarize structure without values
- use local or institution-approved tools
- keep sensitive files out of Git and public AI systems

## Sources and Workflow Influences

Draws on academic data-use norms, commercial database license concerns, and responsible AI guidance.

Last checked: 2026-05-24
