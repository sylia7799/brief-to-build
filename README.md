English | [中文](README.zh-CN.md)

# Brief to Build

> Turn “this should be pretty simple” into a project people can actually start, finish, and accept.

[![Agent Skill](https://img.shields.io/badge/Agent-Skill-6f42c1)](https://agentskills.io/)
[![Codex](https://img.shields.io/badge/Works%20with-Codex-111111)](https://github.com/openai/codex)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

`brief-to-build` is a requirements-analysis skill for Codex. It turns executive drive-bys, client messages, meeting notes, transcripts, attachments, and reference examples into a project baseline that is traceable, confirmable, executable, and testable.

It will not turn “build an intelligent platform” into 47 pages of imaginary architecture. It will not sprint into production while everyone is still politely disagreeing about the scope. First, it makes the work clear. Then it makes the work move—a surprisingly rebellious idea in project management.

## The problem it solves

You have probably met a requirement like this:

> “Take a look at the competitors, make it feel premium, and ideally ship by the end of the month.”

The usual workflow: everyone nods. Three weeks later, the team discovers that everyone nodded at a different project.

`brief-to-build` turns that sentence—and the material around it—into:

- explicit requirements, inferences, assumptions, recommendations, and risks that do not impersonate one another;
- in-scope and out-of-scope boundaries, deliverables, audiences, and authorization limits;
- a source, original strength, and acceptance condition for every formal requirement;
- dependency-ordered tasks, reusable prompts, validation methods, and evidence;
- a change record for the timeless classic: “That was always part of the request.”

## Three documents. No requirement archaeology.

The standard workflow maintains only three project documents:

| File | Purpose |
|---|---|
| `01_需求基线.md` | Define why the project exists, what is in and out, what will be delivered, and who accepts it |
| `02_执行计划与Prompt.md` | Map requirements to tasks, dependencies, reusable prompts, and verification methods |
| `03_验收与变更记录.md` | Record evidence, acceptance results, and the actual cost of “one tiny extra feature” |

Ordinary projects stay lightweight. Work involving production systems, sensitive data, paid calls, multiple teams, irreversible actions, or formal audits automatically upgrades to strict mode.

## Install

Use `skill-installer` in Codex:

```text
$skill-installer install https://github.com/sylia7799/brief-to-build/tree/main/skills/brief-to-build
```

Or copy the skill manually:

```text
skills/brief-to-build  →  ~/.codex/skills/brief-to-build
```

Restart Codex after installation so it reloads skill metadata.

## Use

Describe the task naturally, or invoke the skill explicitly:

```text
Use $brief-to-build to analyze these meeting notes and produce a confirmable requirements baseline, execution plan, and acceptance mechanism. Do not implement the project until I explicitly say “start.”
```

It also understands requests such as:

- “Turn this voice transcript from my manager into project requirements.”
- “Do not write code yet. Clarify scope, deliverables, and acceptance criteria first.”
- “The client changed their mind again. Show which tasks and deliverables are affected.”
- “This project touches production data. Build a strict traceability chain.”

## How it works

```text
Scattered source material
          ↓
Requirements / inferences / assumptions / risks
          ↓
Only the questions that can materially change the outcome
          ↓
Requirements baseline → execution plan & prompts → acceptance & change log
          ↓
Wait for an explicit “start” authorization
```

The core rule is simple: **do not call it confirmed when it is not; do not implement it when it is not authorized.**

## Repository layout

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

## Who it is for

- Product managers whose requirements arrive unexpectedly through chat windows;
- engineering teams that would like to collaborate without telepathy;
- project owners who need meeting notes to become tasks and acceptance criteria;
- anyone who wants Codex to understand first and act second.

## What it is not

- A reason to turn every small request into a United Nations summit;
- a machine for quietly making decisions on behalf of stakeholders;
- a ceremonial spreadsheet filled with impressive nouns and zero ownership;
- permission to conclude, “requirements analysis is done, therefore dropping production is probably fine.”

## License

[MIT](LICENSE). Take it, use it, and may your next project contain less “just start building—we will figure out the details later.”
