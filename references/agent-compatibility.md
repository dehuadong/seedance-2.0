# Agent 兼容性

last_verified: 2026-05-30

在审查此仓库是否正确构建为 Agent Skill 软件包时，请使用本文件。此处关注的是软件包封装与 Agent 行为，而非 Seedance 模型能力。

## 当前 Agent-Skill 结构

Codex 当前的 Agent Skills 文档将技能描述为一个包含必需 `SKILL.md` 文件，以及可选 `scripts/`、`references/`、`assets/` 和 `agents/` 文件夹的目录。它还描述了渐进式披露机制：Agent 首先仅看到名称、描述和路径，仅当技能与任务匹配时才加载完整的 `SKILL.md`。

本仓库遵循该模式：

| Agent-skill 期望项 | 仓库位置 | 状态 |
|---|---|---|
| 根技能元数据与路由 | `SKILL.md` | 已存在 |
| 任务特定子技能 | `skills/*/SKILL.md` | 已存在 |
| 密集参考材料 | `references/*.md` | 已存在 |
| 验证与维护脚本 | `scripts/*.py` | 已存在 |
| README 面向的视觉资源 | `assets/*` | 已存在 |
| Codex UI 元数据 | `agents/openai.yaml` | 已存在 |
| 行为评估 | `evals/evals.json` | 已存在 |
| CI 验证 | `.github/workflows/validate-skills.yml` | 已存在 |
| 本地 Codex 安装器 | `scripts/install_codex_skill.py` | 已存在 |

## 兼容性规则

- 保持每个活跃 `description` 使用第三人称激活措辞，以便工具能从精简技能列表中匹配。
- 保持根 `SKILL.md` 精简。路由至子技能和参考文件，而非将长表格复制到根目录。
- 将易变事实存放在带日期的参考文件中，例如 `api-status.md` 和 `source-registry.md`。
- 若位图图像被 README 引用，请将其保留在 `assets/` 内。
- 保持 `agents/openai.yaml` 与根技能名称对齐，并确保默认提示词调用 `$seedance-20`。
- 使用 `scripts/install_codex_skill.py --force` 安装或刷新本地用户级 Codex 副本至 `$CODEX_HOME/skills/seedance-20` 或 `~/.codex/skills/seedance-20`。
- 保持脚本确定性与本地化。它们应验证结构、模式、设计与源元数据，而无需私有凭证。
- 切勿在技能包中存储 API 密钥、账户 Cookie 或私有提示词语料库。

## 跨客户端说明

不同 Agent 客户端扫描不同的本地路径。Codex 文档指出，Codex 会从当前目录向上扫描 `.agents/skills` 位置，以及用户/管理员/系统技能位置。具有 `SKILL.md` 的仓库根目录具备正确的技能文件夹结构，但除非安装在被扫描的技能目录下，或通过相关插件/分发路径打包，否则不会自动被识别为仓库技能。其他 Agent 客户端可能使用 `.claude/skills`、`.gemini/skills`、`.github/skills`、`.cursor/skills` 或 `.windsurf/skills`。请将这些视为安装目标，而非独立的源代码树。

Runway MCP 是独立的 Agent 连接器表面。它可通过 Runway 在 MCP 兼容的 Agent 中暴露 Seedance 2.0，但不会使本仓库成为 Runway 插件，也不会改变 Codex 技能安装规则。

## 来源信号

- OpenAI Codex Agent Skills 文档：https://developers.openai.com/codex/skills
- OpenAI Codex Plugins 文档：https://developers.openai.com/codex/plugins
- OpenAI Academy 插件与技能说明：https://openai.com/academy/codex-plugins-and-skills/
- OpenAI 技能目录：https://github.com/openai/skills
- Agent Skills 开放标准概览：https://agentskills.io/
- Runway MCP 公告：https://runwayml.com/news/mcp

## 禁止声明

- 切勿声明每个 Agent 客户端都能直接从本仓库 URL 安装。
- 切勿声明每个客户端都认可 `name` 和 `description` 之外的相同元数据字段。
- 切勿声明本仓库提供实时的 Seedance API 封装。它是一个 Agent 技能工作流与参考软件包。