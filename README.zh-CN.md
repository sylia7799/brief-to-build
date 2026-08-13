[English](README.md) | 中文

# Brief to Build

> 把“这个应该不复杂吧”翻译成真正能开工、能验收、也能说清楚为什么延期的项目基线。

[![Agent Skill](https://img.shields.io/badge/Agent-Skill-6f42c1)](https://agentskills.io/)
[![Codex](https://img.shields.io/badge/Works%20with-Codex-111111)](https://github.com/openai/codex)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

`brief-to-build` 是一个面向 Codex 的需求分析 Skill。它负责把领导口述、客户消息、会议纪要、录音转写和散落附件，整理成一套可追溯、可确认、可执行、可验收的项目启动包。

它不会把一句“做个智能平台”脑补成 47 页架构设计，也不会在你还没确认范围时，兴奋地冲进生产环境。它先把话说明白，再让事情动起来——一种在项目管理里略显叛逆的做法。

## 它解决什么问题

你可能见过这样的需求：

> “参考一下竞品，做得高级一点，月底能上线最好。”

普通流程：大家点头，三周后一起发现每个人点的是不同的头。

`brief-to-build` 会把它整理为：

- 明确要求、推断、假设、建议和风险，互不冒充；
- 范围内、范围外、交付物、受众与授权边界；
- 每条正式需求的来源、强度和验收条件；
- 按依赖拆分的任务、可复制 Prompt 与验证证据；
- 基线后的变更记录，避免“我一直都是这么说的”。

## 三份文档，结束需求考古

默认只维护三份项目文档：

| 文件 | 用途 |
|---|---|
| `01_需求基线.md` | 说清楚为什么做、做什么、不做什么，以及谁来验收 |
| `02_执行计划与Prompt.md` | 把需求映射为任务、依赖、验证方法和可复制 Prompt |
| `03_验收与变更记录.md` | 记录证据、验收结果和“顺手再加一个功能”的真实代价 |

低风险项目走简洁流程；涉及生产、敏感数据、付费调用、多团队协作或正式审计时，自动升级严格模式。

## 安装

在 Codex 中使用 `skill-installer`：

```text
$skill-installer install https://github.com/sylia7799/brief-to-build/tree/main/skills/brief-to-build
```

也可以手动复制：

```text
skills/brief-to-build  →  ~/.codex/skills/brief-to-build
```

安装后重启 Codex，让它重新加载 Skill 元数据。

## 使用

自然描述任务即可触发，或显式点名：

```text
Use $brief-to-build 分析这份会议纪要，把需求整理成可确认的基线、执行计划和验收机制。在我明确说“正式开始”之前，不要实施项目。
```

你也可以直接说：

- “把老板这段语音转写整理成项目需求。”
- “先别写代码，帮我确认范围、交付物和验收标准。”
- “客户又改口了，分析这次变更会影响哪些任务。”
- “这个项目涉及生产数据，请用严格模式建立追溯链。”

## 工作方式

```text
零散材料
   ↓
提取明确要求 / 推断 / 假设 / 风险
   ↓
集中澄清真正会改变结果的问题
   ↓
需求基线 → 执行计划与 Prompt → 验收与变更记录
   ↓
等待你明确说“正式开始”
```

核心原则只有一句：**没确认的，不装作确认；没授权的，不顺手实施。**

## 仓库结构

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

## 适合谁

- 需求总从聊天窗口里突然出现的产品经理；
- 想开工，但不想靠心灵感应协作的研发团队；
- 需要把会议纪要变成任务与验收标准的项目负责人；
- 希望 Codex 先问清楚、再行动的任何人。

## 不是什么

- 不是让每个小需求都开一次联合国大会；
- 不是替决策者偷偷做决定；
- 不是一张写满术语、但没人敢签字的表格；
- 更不是“需求分析完成，所以现在可以删库了”的许可证。

## License

[MIT](LICENSE)。拿去用，愿天下少一点“你先做着，细节后面再说”。
