# Concept Index And Glossary

Use this page when a term appears in the handbook and you need the research meaning, not a marketing definition.

> [!NOTE]
> Many AI terms sound technical but matter for ordinary research decisions. If you know the difference between a prompt, a project, a skill, an agent, and an MCP, you can avoid many bad setups.

## Core AI Concepts

| Concept | Research meaning | Read next |
| --- | --- | --- |
| LLM | A language model that predicts and generates text, code, and structured output; not a database | [What LLMs Are and Are Not](what-scholars-must-know/01-what-llms-are-and-are-not.md) |
| Hallucination | Plausible but false or unsupported output | [Hallucination and Fake Citations](what-scholars-must-know/02-hallucination-and-fake-citations.md) |
| Context window | The information available to the model in a session or task | [Context Windows and Files](what-scholars-must-know/03-context-windows-and-files.md) |
| RAG | Retrieval-augmented generation: model output grounded in retrieved source material | [RAG and Source-Grounded AI](what-scholars-must-know/05-rag-and-source-grounded-ai.md) |
| Agent | An AI system that can plan, use tools, and execute multi-step tasks | [Agents and Automation](what-scholars-must-know/06-agents-and-automation.md) |
| Local model | A model run on local or institution-controlled infrastructure | [Local vs Cloud Models](what-scholars-must-know/07-local-vs-cloud-models.md) |

## Workflow Concepts

| Concept | Research meaning | Read next |
| --- | --- | --- |
| Prompt | One-time instruction | [Prompts, Projects, Skills, Agents, MCPs](tools-and-features/01-prompts-projects-skills-agents-mcps.md) |
| Project | Persistent AI workspace for a paper, dataset, talk, or recurring task | [Skills, Projects, Agents, and MCPs](../../../01-Start-Here-to-Learn-AI-for-Econ-Finance-Research/README.md#13-skills-projects-agents-and-mcps) |
| Skill | Reusable procedure for a repeated task | [Build For One Workflows](ai-skills-management/08-build-for-one-research-workflows.md) |
| MCP | Connector standard that lets AI applications connect to external tools and data sources | [Knowledge Links](00-knowledge-links.md) |
| AGENTS.md | Project instruction file for coding agents | [Git, Data, Replication, and Research Safety Templates](../../../02-Copy-and-Use-AI-Research-Instructions-and-Templates/05-git-data-replication-and-research-safety-templates.md) |
| AI-use log | Record of AI-assisted tasks, accepted output, checks, and remaining uncertainty | [Verification, Reproducibility, and Disclosure Skills](../../../02-Copy-and-Use-AI-Research-Instructions-and-Templates/17-verification-reproducibility-and-disclosure-skills.md) |

## Economics And Finance Concepts AI Often Mishandles

| Concept | Why AI may fail |
| --- | --- |
| Identification | AI may describe a design fluently without understanding threats to validity |
| Endogeneity | AI may list generic concerns instead of project-specific mechanisms |
| Event study | AI may confuse event timing, treatment windows, and pre-trends |
| Panel data | AI may miss fixed-effect, clustering, and dependence issues |
| Robustness | AI may invent checks that were not run |
| Economic magnitude | AI may report significance without interpreting size |
| Factor mining | AI may generate plausible finance stories after the fact |
| Equilibrium | AI may skip existence, uniqueness, or boundary cases |

## Fast Diagnosis

| If the AI output... | The likely concept problem is... | What to do |
| --- | --- | --- |
| sounds polished but has no sources | hallucination or unsupported synthesis | ask for source-grounded claims and verify manually |
| summarizes papers that may not exist | fake citations | check Crossref, Google Scholar, journal sites, or the original PDF |
| rewrites your causal claim too strongly | identification and overclaiming | restore precise language and verify design assumptions |
| edits many files at once | agent/tool permission risk | use Git, inspect diffs, and record the AI-use log |
| gives a generic "best tool" answer | undated tool claim | require date, task, tool version, plan, and uncertainty |

## Sources and Workflow Influences

Draws on economics and finance research methodology, official AI tool documentation, and AI agents for economic research.

Last checked: 2026-05-24
