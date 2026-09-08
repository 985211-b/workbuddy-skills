# workbuddy-skills

WorkBuddy 技能仓库：存放自定义 Agent Skill 与配套的 AI 概念结构化学习资料。

## 仓库用途

1. **沉淀可复用的 Skill**：把"某类任务该怎么做"的程序性知识固化为标准格式的技能包，跨会话复用；
2. **沉淀学习资料**：以结构化 HTML 笔记的形式积累 AI 领域核心概念的学习成果，并可随时回看、对比、检索。

## Skill 存放路径

```
workbuddy-skills/
├── .workbuddy/
│   └── skills/
│       ├── my-first-skill/                  # 占位示例技能
│       │   └── SKILL.md
│       └── ai-concept-structured-learning/  # 通用AI概念结构化学习生成技能
│           └── SKILL.md
├── learning-materials/                      # 结构化学习笔记（HTML）
│   ├── agent.html
│   ├── llm-context.html
│   ├── skill.html
│   ├── moe.html
│   └── concept-relationship.html
├── README.md
└── .gitignore
```

约定：每个 Skill 一个独立目录，目录名即技能名，目录内必须包含 `SKILL.md`（YAML frontmatter 元数据 + 指令正文 + 可选资源文件）。

## 如何在 WorkBuddy 中调用

1. **克隆本仓库到本地**：
   ```bash
   git clone https://github.com/985211-b/workbuddy-skills.git
   ```
2. **将 `.workbuddy/` 目录置于 WorkBuddy 工作区根目录下**（或把 `.workbuddy/skills/` 中的技能目录复制/链接到现有工作区的同名路径）。WorkBuddy 启动会话时会扫描 `.workbuddy/skills/` 下的技能索引。
3. **触发方式**：
   - **显式调用**：直接说"用 ai-concept-structured-learning 技能帮我学习 X"；
   - **自动触发**：当你的请求命中技能 description 中描述的场景（如"帮我学习某概念，生成结构化笔记"），技能会被自动加载，`SKILL.md` 指令注入上下文执行。
4. **典型用法**（以结构化学习技能为例）：
   ```
   目标概念：MoE，内容侧重偏落地应用
   ```
   技能会按五步流程（概念定位 → 资料调研 → 结构化生成 → 自检校验 → 交付）产出学习笔记，并可用"要"确认后入库到 `learning-materials/`。

## 已生成的学习资料

| 文件 | 主题 | 内容侧重 |
|------|------|----------|
| `agent.html` | Agent（智能体） | 兼顾原理与落地场景 |
| `llm-context.html` | 大模型上下文 | 兼顾原理与落地场景 |
| `skill.html` | Skill（技能） | 兼顾原理与落地 |
| `moe.html` | MoE（混合专家模型） | 偏落地应用 |
| `concept-relationship.html` | Context × Agent × Skill 三者关系 | 交叉梳理，含关系图与协同流程解剖 |

每份笔记遵循统一结构：概念速览 → 原理拆解 → 演进脉络 → 实践落地 → 对比辨析 → 常见误区 → 记忆锚点 → 延伸阅读（附可访问的权威来源链接）。

## 人工核查与修订记录

以上内容主要由 AI 辅助生成，生成后进行了以下人工核查与修改：

1. **逐份确认入库**：每份笔记生成后均经人工审阅确认（而非自动覆盖），确认无误后才替换原有占位文件并同步远端；
2. **技能定义以人工原文为准**：`ai-concept-structured-learning` 的技能定义由本人提供完整原文，AI 仅做 YAML frontmatter 格式规范化，未改动语义内容；
3. **参考来源可信度控制**：延伸阅读链接限定在可实际访问的权威域名（如 anthropic.com、ibm.com、arxiv.org、nvidia.cn、cloud.tencent.com 等），剔除了无法验证可达性的来源，避免"看起来有出处"的幻觉链接；
4. **同步完整性校验**：由于本地网络无法直连 github.com，文件经 API 通道同步；每次同步后均校验本地 commit SHA 与远端 HEAD 完全一致（当前 `131858e`），确保仓库内容无损；
5. **修订记录**：期间修复过一次本地 git 配置误写（`core.autocrlf` 被误赋值导致提交失败），已重设为 `autocrlf=false`、`eol=lf` 并复验通过。

> 说明：AI 生成的内容仍可能存在细节偏差，建议在用于生产决策前对关键数字与结论做二次核对；本仓库将持续以"生成 + 核查 + 修订"的方式迭代。
