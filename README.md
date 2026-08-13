English | [中文](README.zh-CN.md)

# Brief to Build

> **From a spoken request to an executable project plan.**

[![Agent Skill](https://img.shields.io/badge/Agent-Skill-6f42c1)](https://agentskills.io/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

`brief-to-build` turns leadership recordings, meeting transcripts, chat messages, attachments, and rough requests into a project package that people and Agents can actually execute.

Give it the original material. It extracts what was really requested, asks only the questions that can change the outcome, and generates:

- a traceable requirements baseline;
- a step-by-step execution plan;
- task-specific prompts ready for other Agents;
- acceptance criteria and a change log.

The journey is simple:

```text
One spoken request → clear requirements → executable steps → Agent prompts → verifiable delivery
```

## From a spoken request to an executable project plan

A leader might say:

> “Use the meeting recording and the material I sent to research AI-native databases. Compare the major products and recent papers, explain the technical approaches, identify commercial opportunities, and prepare something I can use in next Friday’s review.”

The intent is clear, but the project is not:

- Which products count as major?
- How recent must the papers be?
- Is the deliverable a report, a presentation, or both?
- How deep should the technical analysis go?
- What evidence is required?
- Which tasks may an Agent execute independently?
- What does “ready for review” mean?

`brief-to-build` converts the source material into confirmed scope, deliverables, dependencies, acceptance criteria, execution steps, and reusable Agent prompts.

No telepathy required.

## What it generates

Running the Skill produces three connected documents:

| File | What you get |
|---|---|
| `01_requirements_baseline.md` | Confirmed requirements, sources, goals, scope, deliverables, constraints, authorization boundaries, and acceptance criteria |
| `02_execution_plan_and_prompts.md` | Ordered tasks, dependencies, outputs, validation methods, and a reusable Agent prompt for every execution stage |
| `03_acceptance_and_change_log.md` | Requirement-to-deliverable mapping, validation evidence, acceptance results, and the impact of later changes |

Together, they answer three questions:

1. **What exactly are we expected to deliver?**
2. **How should people and Agents execute the work?**
3. **How will we prove the result is complete and acceptable?**

## How it works

```text
Leadership recording, transcript, notes, messages, or attachments
                              ↓
       Extract requirements, assumptions, risks, and information gaps
                              ↓
          Clarify only questions that materially affect delivery
                              ↓
                Generate the requirements baseline
                              ↓
         Generate execution steps and task-specific Agent prompts
                              ↓
            Generate acceptance and change-control records
                              ↓
                Wait for explicit execution authorization
```

The Skill keeps confirmed requirements, inferences, assumptions, recommendations, risks, and unresolved questions separate. An assumption never quietly becomes a requirement, and a suggestion never disguises itself as a decision.

## Example prompt

```text
Use $brief-to-build to analyze the attached leadership recording,
meeting transcript, and reference files.

Generate:
1. a requirements baseline with traceable sources;
2. an execution plan with ordered tasks and dependencies;
3. a reusable Agent prompt for every execution stage;
4. acceptance criteria and a change log.

Do not begin research, coding, deployment, data modification,
or external system changes until I explicitly authorize execution.
```

## Works with real project input

- Leadership recordings and transcripts
- Customer calls and interview notes
- Meeting minutes
- Chat and email threads
- Project briefs and informal requests
- Reference documents and examples
- Existing requirements that need review
- New requests that change an approved baseline

Use it for research, software delivery, reports, presentations, data work, product design, internal tools, and multi-Agent workflows.

## Lightweight by default, strict when needed

Ordinary projects use the focused three-document workflow. Stricter checks activate when work involves sensitive or production data, paid services, irreversible operations, multiple teams, conflicting sources, formal audits, or complete source-to-evidence traceability.

The goal is enough structure to prevent expensive misunderstandings—not enough paperwork to qualify as office furniture.

## Safety and execution boundaries

Generating a plan does not authorize implementation. Before execution, the Skill confirms the goal, scope, deliverables, audience, acceptance criteria, dependencies, and authority for external or irreversible actions.

If a later request changes the goal, scope, technical direction, cost, data, external systems, or acceptance criteria, affected work pauses until the change is recorded and confirmed.

## Installation

Install this directory using the standard Skill installation method supported by your Agent:

```text
https://github.com/sylia7799/brief-to-build/tree/main/skills/brief-to-build
```

## Repository structure

```text
brief-to-build/
├── README.md
├── README.zh-CN.md
├── LICENSE
└── skills/
    └── brief-to-build/
        ├── SKILL.md
        ├── agents/
        │   └── openai.yaml
        └── references/
            ├── standard-templates.md
            └── strict-checks.md
```

## License

[MIT](LICENSE)

Turn the next spoken request into a plan people can execute—not another message everyone interprets differently.
