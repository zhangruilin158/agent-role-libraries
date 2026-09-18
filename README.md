# Agent 角色库合集（Agent Role Libraries）

收录 **4 个开源角色 / 人设库**的**角色定义内容**：**583 个角色** + **25 个工作流技能**。
用于多智能体团队搭建：为每个领域提供可复用的专家人设，便于按领域组建 ≥2 人的专家小组。

## 目录结构

```
agent-role-libraries/
├── general-role-library/      # 通用角色库（英文，280 个角色，按领域组织）
├── chinese-role-library/      # 中文角色库（278 个角色，中国本地化 + 公司/HR/法务/供应链等）
├── engineering-personas/      # 工程专家人设（21 个：架构/后端/安全/SRE/DevOps/根因分析/重构…）
├── review-personas/           # 评审专家人设（4 个：代码审查/安全审计/测试/Web 性能）
├── workflow-skills/           # 工作流技能（25 个：需求→计划→构建→验证→评审→发布 全流程）
└── LICENSES/                  # 各来源库的原始许可与版权声明（务必保留）
```

## 角色文件格式

每个角色是一个独立 Markdown 文件，含 YAML frontmatter + 人设正文：

```yaml
---
name: Code Reviewer
description: Expert code reviewer who provides constructive, actionable feedback ...
color: purple
emoji: 👁️
---
# Code Reviewer Agent
你是 **Code Reviewer**，一位提供深入、建设性代码审查的专家……
```

| 字段 | 用途 |
|------|------|
| `name` | 角色名称 |
| `description` | 核心能力（可直接作 Agent 的 goal） |
| 正文「角色 / 使命」段 | 职责与工作方式（可作 backstory） |

## 用法

1. **直接用**：把某个角色的 `.md` 作为 Agent 的 `role / goal / backstory` 喂给多智能体引擎或 AI 编码工具。
2. **组领域小组**：同一领域挑 ≥2 个角色，先组内讨论选出最佳方案，再全团队讨论如何落地。
3. **按需扩展**：库内没有的角色再自行新建，保持同一人设结构即可。

## 许可与署名（重要）

各来源库均为 **MIT / Apache-2.0** 许可。**原始许可与版权声明已完整保留在 `LICENSES/` 目录**，
使用与再分发时请一并保留。

| 子目录 | 许可文件 |
|--------|----------|
| `general-role-library/` | `LICENSES/general-role-library.LICENSE` |
| `chinese-role-library/` | `LICENSES/chinese-role-library.LICENSE` |
| `engineering-personas/` | `LICENSES/engineering-personas.LICENSE` |
| `review-personas/` | `LICENSES/review-personas.LICENSE` |
| `workflow-skills/` | `LICENSES/review-personas.LICENSE`（与 review-personas 同源） |

## 配套技能

本仓库是 **多智能体团队搭建（multi-agent-team）** 技能的角色资源库：
`https://github.com/zhangruilin158/multi-agent-team`

该技能用它来「按领域组建 ≥2 人的专家小组 → 小组讨论选方案 → 团队讨论定落地」。
技能的 `references/统一角色池.md`（去重组队视图，335 角色）与 `references/agent-全量清单.md`
（不去重讨论视图，608 条）即基于本仓库内容生成。

## 说明

- 仅收录**角色定义内容**；各来源库的项目脚手架（CI、脚本、评测、文档、示例）未收录。
- 目录名与内容中的来源标识已中性化处理；版权与许可信息按原样保留在 `LICENSES/`。
- 角色内容为第三方作者原创，本仓库仅做归集与目录整理。
