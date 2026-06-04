![Seedance 2.0 Skill OS 电影化命令中心主图：简报、参考、提示词、后期、质检、字幕、音频波形及镜头卡片](assets/hero-command-center.png)

# Seedance 2.0 Skill OS

**以意图为先的 Seedance 2.0 AI 电影制作工具。**

文本生成视频 · 图像生成视频 · 视频生成视频 · 参考生成视频 · 音频感知提示 · 版权安全改写 · 智能体技能

[![版本](https://img.shields.io/badge/version-5.4.5-111827?labelColor=0f172a)](#changelog)
[![技能](https://img.shields.io/badge/sub--skills-23-0ea5e9?labelColor=0f172a)](#skill-map)
[![参考](https://img.shields.io/badge/references-40-8b5cf6?labelColor=0f172a)](#reference-library)
[![评测](https://img.shields.io/badge/evals-52-22c55e?labelColor=0f172a)](#validation)
[![许可证](https://img.shields.io/badge/license-MIT-f59e0b?labelColor=0f172a)](LICENSE)

作者：[Iamemily2050 (@iamemily2050)](https://github.com/Emily2040) · [Instagram](https://instagram.com/iamemily2050) · [X](https://x.com/iamemily2050) · [网站](https://iamemily2050.com)

平台上下文：[字节跳动 Seedance 2.0](https://seed.bytedance.com/en/seedance2_0) · Dreamina · 即梦 · 豆包 · [火山引擎方舟](https://www.volcengine.com/docs/82379/2291680?lang=zh) · [BytePlus ModelArk](https://docs.byteplus.com/en/docs/ModelArk/2291680) · [Runway Seedance 2](https://docs.dev.runwayml.com/guides/seedance/)

更新时间：**2026-05-30** · **v5.4.5 视觉压力测试图库及专业信息图扩展**

---

## 本仓库存在的原因

Seedance 2.0 Skill OS 是一个用于指导 Seedance 2.0 视频生成的模块化智能体技能包。它围绕一个简单原则构建：**指导模型，而非微观管理每一帧**。

本仓库为 AI 助手提供了一套公开、可审计的 Seedance 工作操作系统。它定义了何时进行访谈、何时编写简洁提示词、何时加载技术参考、何时改写不安全的知识产权内容，以及何时排查生成失败的问题。

## 本技能包的功能

此技能包将 Seedance 2.0 工作转化为可重复的助手工作流：

- 将模糊想法引导至简短创意访谈，而非过早进行提示词堆砌。
- 为 T2V、I2V、V2V、R2V、FLF2V、编辑、扩展、音频感知及首/末帧工作流编写完整或压缩的提示词。
- 按角色分离每个参考素材：身份、环境、动作、镜头节奏、音频节拍、风格或端点。
- 保持模型和平台声明的来源日期标注，确保 API、定价、区域、配额及模型 ID 等细节不被猜测。
- 提供更深入的多语言电影词汇（中文、日文、韩文、西班牙文及俄文），包括角色绑定、首/末帧表述、编辑/扩展措辞、安全措辞及音频提示。
- 新增原创社区启发示例，涵盖中英、俄英、日英、韩英及西英提示词结构。
- 新增专业电影制作工作流，包括方案转镜头列表规划、镜头合约、连续性日志、ACES/色彩交接、音频后期、字幕/本地化、宽高比变体、活动精简版、交付/质检及客户审阅包。
- 通过澄清良性制作上下文（而非隐藏不安全意图）处理安全的误报修复。
- 将涉及名人、受保护知识产权、私人、品牌、标识、歌曲或语音的不安全请求改写为更安全的创意等价内容。
- 通过具体修复杠杆诊断失败输出：镜头、灯光、动作、参考角色、时长、构图、音频或安全措辞。
- 提供验证脚本、评测用例、源数据及设计检查，使维护者可在发布前审查变更。

## 专业电影制作范围

本包专为工作中的电影及商业团队设计，不仅限于休闲提示词编写。它可帮助智能体生成角色实际所需的产出物：

| 角色 | 技能应生成的内容 |
|---|---|
| 导演 | 方案、场景节拍、表演意图、覆盖范围、镜头端点、审阅意见 |
| 摄影指导/摄影师 | 镜头合约、镜头景别、镜头感、镜头支撑、运动、走位、灯光连续性 |
| 制片人/代理公司 | 客户简报、权利图谱、审批节点、活动变体、风险日志、审阅包 |
| 剪辑师 | 精选计划、编辑/扩展决策、连续性交接、素材句柄、无文本需求、合成备注 |
| 调色师 | 色彩意图、ACES 感知交接、成片外观备注、HDR/SDR 注意事项、产品色彩检查 |
| 声音团队 | 对白图谱、环境音/音效/音乐分层、同步提示、分轨、M&E、配音及响度备注 |
| 本地化团队 | 字幕、SDH 字幕、强制叙事、配音指南、市场文案、无文本底板 |
| 交付/质检 | 帧率、宽高比、裁剪、色彩、响度、字幕、元数据、命名、人工质检清单 |

针对此类请求，技能不应止步于单个提示词。它应首先生成制作对象，然后返回符合该计划的 Seedance 提示词或提示词批次。

## 从这里开始

| 用户情境 | 优先加载 | 输出 |
|---|---|---|
| "我有个模糊的想法。" | [`seedance-interview`](skills/seedance-interview/SKILL.md) | 聚焦的创意简报及下一步提示词路径。 |
| "我知道想要的场景。" | [`seedance-prompt`](skills/seedance-prompt/SKILL.md) | 生产就绪的 Seedance 提示词。 |
| "让它简短有力。" | [`seedance-prompt-short`](skills/seedance-prompt-short/SKILL.md) | 压缩的 30–100 字提示词。 |
| "我有图像/视频/音频参考。" | [`reference-workflow`](references/reference-workflow.md) | 每个参考素材的角色映射。 |
| "用这个作首帧，那个作末帧。" | [`first-last-frame-guide`](references/first-last-frame-guide.md) | 带端点锁定的连续过渡。 |
| "生成失败或效果不佳。" | [`seedance-troubleshoot`](skills/seedance-troubleshoot/SKILL.md) | 根本原因诊断及修复后的提示词。 |
| "这涉及角色、品牌、名人或真人。" | [`seedance-copyright`](skills/seedance-copyright/SKILL.md) | 保留创意功能的更安全改写。 |
| "我需要用于电影、客户、活动或交付。" | [`pro-filmmaking-standards`](references/pro-filmmaking-standards.md) | 专业工作流计划、角色特定产出物及提示词路径。 |
| "将此方案转为镜头列表。" | [`shot-list-continuity`](references/shot-list-continuity.md) | 镜头列表、连续性日志及提示词批次结构。 |
| "这需要字幕、配音、色彩、声音或质检。" | [`delivery-qc`](references/delivery-qc.md) | 后期、本地化、音频、色彩及交付检查。 |
| "我需要 API、Runway、定价、模型 ID 或制作工作流指导。" | [`api-workflow`](references/api-workflow.md) | 来源门控的操作清单。 |
| "这是 Seedance Pro/Fast/V2 吗？" | [`model-name-map`](references/model-name-map.md) | 来源日期标注的命名及表面注意事项。 |
| "我需要中文/俄文/日文/韩文/西班牙文或混合语言提示词示例。" | [`multilingual-community-examples`](references/multilingual-community-examples.md) | 安全的社区启发结构及误报修复模式。 |
| "我作为智能体技能安装或审阅此包。" | [`agent-compatibility`](references/agent-compatibility.md) | Codex/智能体技能结构及分发说明。 |

## 当前状态规则

Seedance 平台行为变化迅速。在对 API 可用性、人脸或肖像授权、上传限制、定价、区域可用性或模型名称做出事实性声明前，请加载 [`references/api-status.md`](references/api-status.md) 并检查其 `last_verified` 日期。

截至 2026-05-30，公开官方来源描述 Seedance 2.0 支持文本、图像、音频及视频输入。官方发布及模型卡片材料指出参考素材最多可包含 9 张图像、3 个视频片段及 3 个音频片段。

火山引擎 5 月 29 日文档仍将 `doubao-seedance-2-0-260128` 和 `doubao-seedance-2-0-fast-260128` 显示为当前方舟模型 ID，并记录了该表面上首/末帧角色用法。Runway 文档描述 `seedance2` 支持 5-15 秒时长及可选图像、视频和音频参考。

访问权限、定价、上传限制、区域、分辨率、音频组合规则及授权要求仍因表面而异。

## 研究快照

v5.4 发布线添加了带日期的研究层，以实现更安全的数据挖掘及平台声明：

- [`research-2026-05-30.md`](references/research-2026-05-30.md) 记录官方及实地观察信号。
- [`platform-surface-matrix.md`](references/platform-surface-matrix.md) 区分模型能力与 Dreamina/即梦、火山引擎/方舟、BytePlus、ComfyUI 及封装行为。
- [`model-name-map.md`](references/model-name-map.md) 防止 `Seedance 2.0`、`Seedance 2.0 Fast`、`Seedance V2` 及模糊的 Pro 标签混用。
- [`community-source-methodology.md`](references/community-source-methodology.md) 解释如何挖掘公开提示词语料库而不复制不安全示例。
- [`multilingual-community-examples.md`](references/multilingual-community-examples.md) 从社区模式挖掘中捕获安全的混合语言及本地化提示词结构。
- [`pro-filmmaking-standards.md`](references/pro-filmmaking-standards.md) 为镜头列表、连续性、色彩、音频、本地化及交付添加行业工作流边界。

## 操作系统一览

![Seedance 2.0 Skill OS 信息图：来源注册表、提示词路由器、多模态参考、安全门及评测循环](assets/skill-os-infographic.png)

操作系统映射保持简洁以确保 GitHub 可读性；下方视觉图库添加了文字丰富的专业信息图。二者共同代表本包保持分离的六条通道：

- 研究来源：带日期的官方、学术、平台及社区证据。
- 制作主干：简报、镜头列表、连续性、后期交接、本地化及交付/质检。
- 提示词路由器：访谈、提示词编写、压缩、配方及故障排查。
- 多模态参考：图像、视频、音频、首帧、末帧及角色绑定素材。
- 安全门：知识产权、肖像、语音、品牌、真人、过滤及平台政策检查。
- 质量评测：模式检查、来源新鲜度、词汇完整性、设计审计及行为用例。

## 视觉图库

自述文件现在包含提交的视觉集，而非单一通用主图。这些生成的位图素材与可搜索的 Markdown 配对，使图像具有电影感的同时仓库仍可审计。

### 主图

![Seedance 2.0 命令中心主图，展示简报、参考、提示词、后期、质检、字幕、音频波形及镜头卡片](assets/hero-command-center.png)

![全球电影人模式主图，展示导演、摄影指导、剪辑师、调色师、混音师、本地化负责人及质检负责人在电影制作舞台上](assets/hero-global-filmmaker-mode.png)

### 文字丰富信息图

![本技能功能信息图：简报、参考、提示词、生成、后期、交付](assets/infographic-skill-capabilities.png)

![CDN 视频交付地图信息图：创作者、源站、CDN 边缘、全球审阅、交付、快速播放、区域缓存、版本控制及发布前质检](assets/infographic-cdn-delivery-map.png)

![参考角色映射信息图：图像=身份，视频=动作，音频=时序](assets/infographic-reference-role-map.png)

![制作到交付信息图：简报、镜头列表、生成、编辑、本地化、质检](assets/infographic-production-delivery.png)

![专业质检堆栈信息图：画面、色彩、音频、文本、权利、元数据](assets/infographic-professional-qc-stack.png)

## 技能映射

![Seedance 2.0 电影化技能映射：围绕 AI 电影制作导演控制台的模块化技能集群](assets/skill-map-cinematic.png)

### 核心管线

| 技能 | 适用场景 |
|---|---|
| [`seedance-interview`](skills/seedance-interview/SKILL.md) | 想法模糊、未发展或需要创意指导时。 |
| [`seedance-interview-short`](skills/seedance-interview-short/SKILL.md) | 用户需要快速简报，而非长访谈时。 |
| [`seedance-prompt`](skills/seedance-prompt/SKILL.md) | 用户需要从清晰概念生成完整提示词时。 |
| [`seedance-prompt-short`](skills/seedance-prompt-short/SKILL.md) | 提示词需压缩以获得更强 Seedance 性能时。 |
| [`seedance-camera`](skills/seedance-camera/SKILL.md) | 需指定镜头行为、镜头感、景别或运动时。 |
| [`seedance-motion`](skills/seedance-motion/SKILL.md) | 身体动作、物体运动、编排或物理动作重要时。 |
| [`seedance-lighting`](skills/seedance-lighting/SKILL.md) | 情绪、时段、氛围或光线过渡驱动镜头时。 |
| [`seedance-characters`](skills/seedance-characters/SKILL.md) | 角色身份、多角色走位或一致性重要时。 |
| [`seedance-style`](skills/seedance-style/SKILL.md) | 用户需要视觉风格而不涉及不安全工作室/特许经营借用时。 |
| [`seedance-vfx`](skills/seedance-vfx/SKILL.md) | 粒子、破坏、能量、天气、魔法或变换效果重要时。 |
| [`seedance-audio`](skills/seedance-audio/SKILL.md) | 对白、口型同步、音乐、环境音或音频参考行为重要时。 |
| [`seedance-pipeline`](skills/seedance-pipeline/SKILL.md) | 用户询问 API、网页工作流、ComfyUI、后期制作或集成时。 |
| [`seedance-recipes`](skills/seedance-recipes/SKILL.md) | 用户需要类型模板或可重复制作配方时。 |
| [`seedance-troubleshoot`](skills/seedance-troubleshoot/SKILL.md) | 输出质量差、不稳定、模糊、偏离提示词或被阻止时。 |

### 治理与质量

| 技能 | 适用场景 |
|---|---|
| [`seedance-copyright`](skills/seedance-copyright/SKILL.md) | 涉及受保护知识产权、公众人物、真人、品牌、标识、歌曲或确切场景时。 |
| [`seedance-antislop`](skills/seedance-antislop/SKILL.md) | 提示词语言通用、臃肿或充满空泛质量增强词时。 |
| [`seedance-filter`](skills/seedance-filter/SKILL.md) | 提示词被阻止、降级或可能触发内容过滤时。 |

### 多语言词汇

| 技能 | 适用场景 |
|---|---|
| [`seedance-vocab-zh`](skills/seedance-vocab-zh/SKILL.md) | 需要中文提示词压缩或普通话电影词汇时。 |
| [`seedance-vocab-ja`](skills/seedance-vocab-ja/SKILL.md) | 需要日文电影词汇时。 |
| [`seedance-vocab-ko`](skills/seedance-vocab-ko/SKILL.md) | 需要韩文电影词汇时。 |
| [`seedance-vocab-es`](skills/seedance-vocab-es/SKILL.md) | 需要西班牙文电影词汇时。 |
| [`seedance-vocab-ru`](skills/seedance-vocab-ru/SKILL.md) | 需要俄文电影词汇时。 |
| [`seedance-examples-zh`](skills/seedance-examples-zh/SKILL.md) | 需要中文工作示例或示例安全改写时。 |

## 参考库

| 参考文档 | 用途 |
|---|---|
| [`api-status.md`](references/api-status.md) | 当前带日期的平台及 API 状态。 |
| [`source-registry.md`](references/source-registry.md) | 来源层级及证据标签。 |
| [`research-2026-05-30.md`](references/research-2026-05-30.md) | 带日期的来源及实地观察快照。 |
| [`agent-compatibility.md`](references/agent-compatibility.md) | 智能体技能结构、Codex 兼容性及打包说明。 |
| [`api-workflow.md`](references/api-workflow.md) | 火山引擎、BytePlus、Runway、异步任务、参考文件、定价及制作工作流清单。 |
| [`pro-filmmaking-standards.md`](references/pro-filmmaking-standards.md) | 专业制作主干及电影、商业、后期、本地化及交付工作的来源边界。 |
| [`cinematography-shot-language.md`](references/cinematography-shot-language.md) | 镜头合约、景别、镜头感、镜头支撑、运动、走位及覆盖语言。 |
| [`shot-list-continuity.md`](references/shot-list-continuity.md) | 方案转镜头列表工作流、连续性日志及专业交接字段。 |
| [`color-pipeline-aces.md`](references/color-pipeline-aces.md) | ACES 感知色彩意图、成片外观备注、HDR/SDR 交接及色彩质检边界。 |
| [`aspect-ratio-delivery.md`](references/aspect-ratio-delivery.md) | 创意构图、交付容器、社交精简版、安全区域及无文本/版本规划。 |
| [`subtitles-localization.md`](references/subtitles-localization.md) | 字幕、SDH、强制叙事、配音、无文本及文化本地化规划。 |
| [`audio-post-delivery.md`](references/audio-post-delivery.md) | 对白、音效、音乐、分轨、M&E、响度、配音及同步交接指导。 |
| [`delivery-qc.md`](references/delivery-qc.md) | 画面、色彩、音频、字幕、权利、元数据、版本及人工质检的专业预检。 |
| [`examples-by-mode.md`](references/examples-by-mode.md) | T2V、I2V、V2V、R2V、FLF2V、编辑、扩展及故障排查的模式特定提示词示例。 |
| [`multilingual-community-examples.md`](references/multilingual-community-examples.md) | 来自安全社区模式挖掘的原创中文、俄文、日文、韩文、西班牙文及混合语言提示词结构。 |
| [`platform-surface-matrix.md`](references/platform-surface-matrix.md) | 模型与表面声明边界。 |
| [`model-name-map.md`](references/model-name-map.md) | Seedance 命名、Fast 变体及 Pro 标签注意事项。 |
| [`first-last-frame-guide.md`](references/first-last-frame-guide.md) | FLF2V、首帧及末帧提示词编写。 |
| [`field-observed-tips.md`](references/field-observed-tips.md) | 安全从业者工作流模式。 |
| [`community-source-methodology.md`](references/community-source-methodology.md) | 安全公开语料库挖掘及标签规则。 |
| [`platform-constraints.md`](references/platform-constraints.md) | 稳定平台风险规则。 |
| [`quick-ref.md`](references/quick-ref.md) | 紧凑路由及提示词清单。 |
| [`reference-workflow.md`](references/reference-workflow.md) | 如何映射图像、视频、音频及故事板参考。 |
| [`i2v-guide.md`](references/i2v-guide.md) | 图像生成视频最佳实践。 |
| [`prompt-examples.md`](references/prompt-examples.md) | 安全可复制粘贴的提示词示例。 |
| [`genre-guides.md`](references/genre-guides.md) | 类型特定提示词模式。 |
| [`storytelling-framework.md`](references/storytelling-framework.md) | 叙事设计及视觉分层。 |
| [`intent-vs-precision.md`](references/intent-vs-precision.md) | 意图优先理念。 |
| [`audio-guide.md`](references/audio-guide.md) | 音频、对白、节拍同步及口型同步指导。 |
| [`anti-slop-lexicon.md`](references/anti-slop-lexicon.md) | 弱短语替换表。 |
| [`filter-vocab.md`](references/filter-vocab.md) | 被阻止/降级提示词的更安全措辞。 |
| [`frontend-design-system.md`](references/frontend-design-system.md) | 自述文件及 SVG 设计标准。 |
| [`json-schema.md`](references/json-schema.md) | 用于管线的结构化提示词封装器。 |
| [`eval-rubric.md`](references/eval-rubric.md) | 如何评判评测输出。 |
| [`progressive-disclosure.md`](references/progressive-disclosure.md) | 根技能、子技能及参考边界。 |
| [`vocab/zh.md`](references/vocab/zh.md) | 用于紧凑提示词的中文电影词汇。 |
| [`vocab/ja.md`](references/vocab/ja.md) | 用于紧凑提示词的日文电影词汇。 |
| [`vocab/ko.md`](references/vocab/ko.md) | 用于紧凑提示词的韩文电影词汇。 |
| [`vocab/es.md`](references/vocab/es.md) | 用于紧凑提示词的西班牙文电影词汇。 |
| [`vocab/ru.md`](references/vocab/ru.md) | 用于紧凑提示词的俄文电影词汇。 |

## 安装

智能体技能的客户端支持仍因工具而异。Codex 将技能记录为包含必需 `SKILL.md`、可选 `scripts/`、`references/`、`assets/` 及可选 `agents/` 元数据的目录。

Codex 从工作目录向上扫描 `.agents/skills` 位置，以及用户/管理员/系统技能位置。具有 `SKILL.md` 的仓库根目录形似技能文件夹，但仍需安装/复制到扫描的技能目录下，或作为插件分发以实现自动发现。

本仓库现在包含 `agents/openai.yaml` 及本地 Codex 安装程序。要为此 Windows 工作站或任何本地 Codex 配置文件安装，请运行：

```bash
python scripts/install_codex_skill.py --force
```

安装程序在设置 `CODEX_HOME` 时将仓库复制到 `$CODEX_HOME/skills/seedance-20`，否则复制到 `~/.codex/skills/seedance-20`。安装后重启 Codex，使 `$seedance-20` 出现在可用技能列表中。

本仓库将密集事实保留在参考文档中，以保持活动技能小巧。

如果您的客户端支持直接从 GitHub 仓库安装技能，请使用此仓库 URL：

```text
https://github.com/Emily2040/seedance-2.0
```

对于手动安装，请将此仓库复制到智能体客户端使用的技能目录中。目录名称应与根技能名称 `seedance-20` 匹配。将下表视为常见本地目标以在您自己的客户端中验证，而非通用支持保证。

| 平台 | 典型工作区路径 |
|---|---|
| Claude Code / OpenClaw | `.claude/skills/seedance-20/` |
| Codex 风格智能体工作区 | `.agents/skills/seedance-20/` |
| Gemini CLI 风格工作区 | `.gemini/skills/seedance-20/` |
| GitHub Copilot 工作区 | `.github/skills/seedance-20/` |
| Cursor 工作区 | `.cursor/skills/seedance-20/` |
| Windsurf 工作区 | `.windsurf/skills/seedance-20/` |

## 验证

每次发布前运行这些检查：

```bash
python scripts/validate_skills.py --strict
python scripts/content_audit.py --strict
python scripts/eval_schema_check.py --strict
python scripts/design_audit.py --strict
python scripts/source_registry_check.py --strict
python scripts/vocab_schema_check.py --strict
```

CI 工作流在推送及拉取请求时运行相同检查。

## 设计标准

v5.4.5 首页使用多个生成的电影化位图主图、文字丰富信息图、生成的操作系统信息图、生成的电影化技能映射信息图，以及清理后的 v5.2 信息架构。自述文件应在 GitHub 移动端、深色模式及窄宽度下保持可读。SVG 素材必须包含 `<title>` 及 `<desc>` 元素、仅使用内部 CSS，并避免外部字体或脚本。参见 [`docs/frontend-redesign.md`](docs/frontend-redesign.md)。

## 更新日志

参见 [`CHANGELOG.md`](CHANGELOG.md)。当前版本：**v5.4.5**。

## 许可证

MIT © 2026 Iamemily2050 (@iamemily2050)