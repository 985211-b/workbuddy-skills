# workbuddy-skills

WorkBuddy 技能仓库，用于存放自定义 Agent Skill 与学习资料。

## 仓库结构

```
workbuddy-skills/
├── .workbuddy/
│   └── skills/
│       └── my-first-skill/
│           └── SKILL.md
├── learning-materials/
│   ├── agent.html
│   ├── llm-context.html
│   ├── skill.html
│   └── concept-relationship.html
├── README.md
└── .gitignore
```

## 目录说明

- `.workbuddy/skills/<skill-name>/SKILL.md`：Skill 元信息与使用说明
- `learning-materials/`：HTML 格式的学习材料，涵盖 Agent、LLM Context、Skill 和概念关系
- `.gitignore`：忽略本地临时文件、凭据等

## 使用方式

将本仓库克隆到本地后，可在 `.workbuddy/skills/` 下新增 Skill 目录，并保证每个 Skill 目录下包含 `SKILL.md`。
