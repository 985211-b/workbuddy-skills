# my-first-skill

## 概述

我的第一个 WorkBuddy Agent Skill，用于演示标准 Skill 目录结构与元信息写法。

## 触发条件

当用户提到以下关键词时，可以加载本 Skill：

- 我的第一个技能
- my-first-skill
- 演示 skill 结构
- 仓库结构示例

## 能力范围

1. 解释仓库结构：说明 `.workbuddy/skills/` 与 `learning-materials/` 的用途
2. 生成模板：根据要求生成新的 `SKILL.md` 或 HTML 学习资料模板
3. 检查规范：检查新 Skill 是否包含必须的 `SKILL.md` 文件

## 使用方式

直接在对话中触发关键词，Agent 会调用本 Skill 的模板能力。

## 目录结构要求

每个 Skill 目录下必须包含：

- `SKILL.md`：技能说明、触发词、使用方式、示例

可选文件：

- `references/`：参考资料
- `templates/`：模板文件
- `examples/`：示例对话或代码

## 示例

**用户**：我想新建一个 skill，应该怎么写 SKILL.md？

**Agent**：根据 `my-first-skill/SKILL.md` 的格式，新建目录并包含以下内容：概述、触发条件、能力范围、使用方式、目录结构要求、示例。
