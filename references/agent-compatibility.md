# 智能体兼容性

最后验证时间：2026-06-12

在审查此代码库是否以正确的智能体技能包形态组织时，请使用此文件。此处涉及的是打包方式和智能体行为，而非 Seedance 模型能力。

## 当前智能体技能形态

Codex 当前的智能体技能文档将技能描述为一个目录，其中包含必需的 `SKILL.md` 文件，以及可选的 `scripts/`、`references/`、`assets/` 和 `agents/` 文件夹。同时还描述了渐进式披露机制：智能体首先看到名称、描述和路径，仅当技能与任务匹配时才加载完整的 `SKILL.md`。

此代码库遵循该模式：

| 智能体技能预期 | 代码库位置 | 状态 |
|---|---|---|
| 根技能元数据和路由 | `SKILL.md` | 存在 |
| 任务特定子技能 | `skills/*/SKILL.md` | 存在 |
| 密集参考资料 | `references/*.md` | 存在 |
| 验证和维护脚本 | `scripts/*.py` | 存在 |
| README 中使用的视觉资源 | `assets/*` | 存在 |
| Codex UI 元数据 | `agents/openai.yaml` | 存在 |
| 行为评估 | `evals/evals.json` | 存在 |
| CI 验证 | `.github/workflows/validate-skills.yml` | 存在 |
| 本地 Codex 安装程序 | `scripts/install_codex_skill.py` | 存在 |

## 兼容性规则

- 保持每个活跃的 `description` 使用第三人称激活措辞，以便工具能从简短的技能列表中匹配到它。
- 保持根目录 `SKILL.md` 简短。路由到子技能和参考资料，而不是将长表格复制到根目录中。
- 将易变的事实信息放在带日期的参考资料中，如 `api-status.md` 和 `source-registry.md`。
- 如果 README 中引用了生成的位图图像，请将其保存在 `assets/` 内。
- 保持 `agents/openai.yaml` 与根技能名称一致，并使默认提示调用 `$seedance-20`。
- 使用 `scripts/install_codex_skill.py --force` 在用户级 Codex 副本中安装或刷新，路径为 `$CODEX_HOME/skills/seedance-20` 或 `~/.codex/skills/seedance-20`。
- 保持脚本具有确定性和本地性。它们应能验证结构、模式、设计和来源元数据，而无需私有凭证。
- 不要在技能包中存储 API 密钥、账户 Cookie 或私有提示语料库。

## 跨智能体矩阵

于 2026-06-12 根据各智能体的公开文档验证；安装路径可能变化——在承诺行为之前请重新检查当前客户端。将此代码库安装为单个根技能（`seedance-20`）；子技能和参考资料通过相对于根目录的路径加载。

| 智能体 | 技能位置 | 安装方式 | 备注 |
|---|---|---|---|
| Claude Code / claude.ai | `.claude/skills/`（工作区），托管技能 | 复制或通过市场安装 | SKILL.md 形态的发源平台。 |
| Codex | `.agents/skills/` 向上扫描 + 用户/系统目录 | `scripts/install_codex_skill.py --force` | `agents/openai.yaml` 提供 UI 元数据。 |
| Google Antigravity | `.agents/skills/`（工作区），`~/.gemini/antigravity-cli/skills/`（全局） | 复制文件夹，重启会话 | 与 Codex 工作区使用相同的目录约定；SKILL.md + scripts/references/assets 形态与此代码库匹配。 |
| OpenClaw | 工作区 `skills/`，`~/.openclaw/skills/`（全局） | `openclaw skills install`（git/本地安装期望 `SKILL.md` 位于源码根目录——此代码库符合要求） | ClawHub 是公共注册表（使用 `clawhub` CLI 发布）。此处的每个技能都已携带 `openclaw:` 元数据。 |
| Hermes Agent（Nous Research） | 项目 `skills/`，`~/.hermes/skills/` | `hermes skills install`（会运行安全扫描） | 根据 frontmatter 中的 `description` 激活——此代码库的第三人称激活措辞正是它所匹配的。 |
| Gemini CLI / Cursor / Windsurf / Copilot | `.gemini/`、`.cursor/`、`.windsurf/`、`.github/` + `skills/` | 复制文件夹 | 将其视为安装目标，而非独立的源码树。 |

## 跨客户端说明

不同的智能体客户端扫描不同的本地路径。Codex 文档说明 Codex 从当前目录向上扫描 `.agents/skills` 位置，外加用户/管理员/系统技能位置。包含 `SKILL.md` 的代码库根目录具有正确的技能文件夹形态，但除非安装在已扫描的技能目录下，或通过相关插件/分发路径打包，否则不会自动被识别为仓库技能。其他智能体客户端可能使用 `.claude/skills`、`.gemini/skills`、`.github/skills`、`.cursor/skills` 或 `.windsurf/skills`。将这些视为安装目标，而非独立的源码树。

Runway MCP 是一个独立的智能体连接表面。它可以通过 MCP 兼容智能体内的 Runway 暴露 Seedance 2.0，但这不会使此代码库成为 Runway 插件，也不会改变 Codex 技能安装规则。

## 来源参考

- OpenAI Codex 智能体技能文档：https://developers.openai.com/codex/skills
- OpenAI Codex 插件文档：https://developers.openai.com/codex/plugins
- OpenAI Academy 插件和技能说明：https://openai.com/academy/codex-plugins-and-skills/
- OpenAI 技能目录：https://github.com/openai/skills
- 智能体技能开放标准概述：https://agentskills.io/
- Google Antigravity 技能文档：https://antigravity.google/docs/cli-plugins 和 https://codelabs.developers.google.com/getting-started-with-antigravity-skills
- OpenClaw 技能文档：https://docs.openclaw.ai/tools/skills
- Hermes Agent 技能文档：https://hermes-agent.nousresearch.com/docs/user-guide/features/skills
- Runway MCP 公告：https://runwayml.com/news/mcp

## 不得声称的事项

- 不得声称每个智能体客户端都能从此代码库 URL 直接安装。
- 不得声称 ClawHub 或任何注册表已收录此技能，除非实际已发布到该处。
- 不得声称每个客户端都支持除 `name` 和 `description` 之外的相同元数据字段。
- 不得声称此代码库提供实时的 Seedance API 封装。它是一个智能体技能工作流和参考包。