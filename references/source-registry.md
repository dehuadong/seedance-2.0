# 来源登记表

last_verified: 2026-06-11

在对 Seedance 2.0 平台行为进行事实性陈述之前，请使用本登记表。优先使用主要的公开来源，附上核实日期，并将易变动的声明标记为需要重新核查。本文件是一个声明边界图，并非对每个产品界面或地区访问权限的保证。

## 证据标签

| 标签 | 含义 | 必需措辞 |
|---|---|---|
| `confirmed` | 在核实日期可直接在主要公开来源中看到。 | `公开来源表明……截至[日期]。` |
| `volatile` | 可能因界面、账户、地区、定价页面或模型更新而发生变化。 | `在给出数字或承诺前请重新核查。` |
| `field-observed` | 反复出现的创作者/从业者模式，但并非官方平台事实。 | `现场观察，非保证的平台行为。` |
| `unverified` | 看似合理但未经主要来源确认。 | `需要测试或所有者确认。` |
| `internal` | 来源于本技能包的仓库指导。 | `用作工作流指导，而非外部事实。` |

## 主要来源层级

| 主题 | 首选来源 | 证据标签 | 核实说明 | 声明边界 |
|---|---|---|---|---|
| 核心模型能力 | 字节跳动 Seedance 2.0 官方页面：https://seed.bytedance.com/en/seedance2_0 | confirmed | 在发布说明、API 声明或营销文案前重新核查。 | 仅用于广泛的公共能力框架描述。 |
| 发布功能和已知限制 | 字节跳动 Seedance 2.0 官方发布文章：https://seed.bytedance.com/en/blog/seedance-2-0-official-launch | confirmed | 在讨论多模态参考、编辑、音频和平台示例时重新核查。 | 不要将发布示例转化为每个界面上的保证行为。 |
| 模型卡和论文 | arXiv 模型卡：https://arxiv.org/abs/2604.14148 | confirmed | 适用于模型家族背景和基准测试注意事项。 | 提供商撰写的论文；不要用作当前商业访问证明。 |
| API 教程和平台文档 | BytePlus ModelArk 和火山引擎 Ark 文档：https://docs.byteplus.com/en/docs/ModelArk/2291680、https://www.volcengine.com/docs/82379/1520757?lang=zh 和 https://www.volcengine.com/docs/82379/2291680?lang=zh | volatile | 在程序性 API 指导前重新核查端点、请求字段、模型 ID、任务流程和定价。 | API 形态可能因地区、账户或发布渠道而异。 |
| 视频生成任务生命周期 | 火山引擎视频生成教程：https://www.volcengine.com/docs/82379/2298881?lang=zh | volatile | 在实现前重新核查创建/查询/列表/取消删除流程、首帧/尾帧角色、返回尾帧、工具和文件引用规则。 | 官方界面，但字段和账户支持可能发生变化。 |
| 模型 ID 和定价 | 火山引擎模型列表/定价和 BytePlus 定价页面 | volatile | 在引用数字或 ID 前务必立即重新核查。 | 火山引擎价格仅可在注明日期、货币、模型、界面和警告的情况下引用；切勿从不完整的 JS 渲染页面推断 BytePlus 定价。 |
| API 服务生态系统新闻 | 火山引擎开发者文章：https://developer.volcengine.com/articles/7628567056649125942 | volatile | 用作 API 服务推出、安全标准、肖像授权、虚拟肖像和 BytePlus 海外服务声明的官方生态系统/新闻证据。实现细节请重新核查文档/控制台。 | 不是 API 合同、价格表或权利保证。 |
| BytePlus 定价页面 | BytePlus ModelArk 定价文档：https://docs.byteplus.com/en/docs/ModelArk/1099320 | volatile | 在引用 Seedance 2.0 定价、配额或模型 ID 前，重新核查实时官方页面或控制台。 | 部分页面在静态抓取时由 JavaScript 渲染；不要从不完整的静态内容推断当前 Seedance 2.0 定价。 |
| 提示词指南 | 火山引擎 Seedance 2.0 提示词指南：https://www.volcengine.com/docs/82379/2222480?lang=zh | confirmed | 在添加多模态参考措辞或提示词示例时重新核查。 | 提示词建议是官方指导，并非保证每个界面都暴露每个控制项。 |
| 首帧/尾帧工作流 | 火山引擎教程和 ComfyUI 合作伙伴文档：https://www.volcengine.com/docs/82379/2298881?lang=zh 和 https://docs.comfy.org/zh/tutorials/partner-nodes/bytedance/seedance-2-0 | volatile | 火山引擎记录了首帧/尾帧角色；ComfyUI 使用 FLF2V 工作流词汇。在使用确切字段前重新核查活跃界面。 | `FLF2V` 标签是界面特定的，但首帧/尾帧能力已在火山引擎上记录。 |
| 面部、肖像和声音行为 | 活跃产品界面、官方政策和用户授权 | volatile | 重新核查当前界面行为和授权上下文。 | 不要从文件上传推断同意。 |
| Runway Seedance 2 界面 | Runway API 和帮助文档：https://docs.dev.runwayml.com/guides/seedance/ 和 https://help.runwayml.com/hc/en-us/articles/50488490233363-Creating-with-Seedance-2-0 | volatile | 在用于生产前重新核查时长、宽高比、音频/参考组合规则、地区可用性、套餐要求和 SDK 支持。 | 官方 Runway 界面，不是字节跳动/火山引擎 API 合同。 |
| fal Seedance 2.0 界面 | fal 模型/API 页面：https://fal.ai/models/bytedance/seedance-2.0/text-to-video、https://fal.ai/models/bytedance/seedance-2.0/image-to-video 和 https://fal.ai/models/bytedance/seedance-2.0/reference-to-video | volatile | 在引用数字或编写 API 调用前重新核查端点、请求字段、分辨率层级、时长和每秒定价。 | 官方 fal 界面行为，非火山引擎、BytePlus 或 Runway 行为。快速端点共享记录的模式；快速层级上的多镜头可靠性降级是现场观察结果，非官方行为。 |
| 智能体技能结构 | OpenAI Codex Agent Skills 文档：https://developers.openai.com/codex/skills、OpenAI Academy 插件/技能说明：https://openai.com/academy/codex-plugins-and-skills/、OpenAI Codex Plugins 文档和 Agent Skills 开放标准：https://agentskills.io/ | confirmed | 在更改安装指导或根技能布局前重新核查。 | 打包指导，非 Seedance 平台能力。 |
| Runway MCP 智能体界面 | Runway MCP 公告：https://runwayml.com/news/mcp | confirmed | 仅用于智能体界面可用性。 | 不改变 Seedance 模型能力；套餐和连接器访问是 Runway 特定的。 |
| 音视频评估词汇 | AVBench 和 VABench 论文：https://arxiv.org/abs/2605.24652 和 https://openaccess.thecvf.com/content/CVPR2026/papers/Hua_VABench_A_Comprehensive_Benchmark_for_Audio-Video_Generation_CVPR_2026_paper.pdf | field-observed | 用于评估维度，如音视频同步和跨模态一致性。 | 基准框架，非产品访问或官方 Seedance 性能证明。 |
| 专业镜头语言 | ASC 摄影机运动教育和制作镜头列表实践：https://theasc.com/article/shot-craft-camera-movement/ 和 https://www.studiobinder.com/blog/shot-list-template-free-download/ | field-observed | 用于镜头合约、摄影机运动和镜头列表字段。 | 行业工作流指导，非 Seedance 能力证明。 |
| 连续性实践 | ScreenSkills 剧本监督角色：https://www.screenskills.com/job-profiles/browse/film-and-tv-drama/technical/script-supervisor-film-and-tv-drama/ | field-observed | 用于连续性锚点，如服装、道具、视线、画面方向和备注。 | 角色指导，非平台行为。 |
| 色彩管理和 ACES | ACES 文档和 AMF 规范：https://docs.acescentral.com/background/overview/ 和 https://docs.acescentral.com/amf/specification/ | confirmed | 用于色彩流程词汇和交接元数据。 | 提示词可以描述一种风格；但无法认证 ACES 合规性。 |
| 宽高比和交付容器 | DCI、ISDCF 和买家/平台规范：https://www.dcimovies.com/dci-specification/ 和 https://registry-page.isdcf.com/ | field-observed | 用于宽高比/容器分离和命名注意事项。 | 始终遵循合同约定的交付规范。 |
| 字幕和隐藏字幕 | Netflix 时序文本、WebVTT 和无障碍规则：https://partnerhelp.netflixstudios.com/hc/en-us/articles/215758617-Timed-Text-Style-Guide-General-Requirements、https://w3c.github.io/webvtt/ 和 https://www.law.cornell.edu/cfr/text/47/79.1 | volatile | 用于字幕/SDH/强制叙事规划和字幕安全框。重新核查买家、语言、地区和平台要求。 | 交付要求因买家、语言、地区和平台而异。 |
| 音频响度和后期 | ITU BS.1770、EBU R128、ATSC A/85 和买家声音规范：https://www.itu.int/rec/R-REC-BS.1770、https://tech.ebu.ch/fr/publications/r128、https://www.atsc.org/atsc-documents/a85-techniques-for-establishing-and-maintaining-audio-loudness-for-digital-television/ 和 https://partnerhelp.netflixstudios.com/hc/en-us/articles/360001794307-Netflix-Sound-Mix-Specifications-Best-Practices-v1-6 | volatile | 用于音轨主干、M&E、同步、响度和混音交接语言。重新核查目标买家或平台规范。 | 提示词音频不是经过认证的最终混音。 |
| 交付和质量控制 | SMPTE IMF、DPP 规范、Netflix 交付规范和 MovieLabs OMC：https://www.smpte.org/standards/st2067、https://www.thedpp.com/specs/、https://partnerhelp.netflixstudios.com/hc/en-us/sections/10066414335891-Delivery-Specifications 和 https://movielabs.com/ontology-for-media-creation/ | volatile | 用于交付预检和元数据/版本控制指导。在最终交付前重新核查合同约定的平台规范。 | 合同约定的平台规范优先于通用指导。 |
| 社区实践 | 抖音、Bilibili、CSDN、Reddit、Habr、创作者笔记、工作流截图 | field-observed | 仅用作从业者指导。 | 标记为非官方；不要声明为模型保证。 |
| 本地化和混合语言提示词 | 日语、韩语、西班牙语、俄语和多语言社区指南及论坛观察 | field-observed | 在发布前重新核查公开页面；仅用于词汇和示例结构。 | 语码混合可以澄清安全提示词，但切勿将其视为官方过滤行为或安全规避手段。 |
| 社区提示词语料库 | YouMind/OpenLab、公开提示词画廊、论坛合集 | field-observed | 仅在进行安全分类后挖掘结构、时序、词汇和失败模式。 | 不要将不安全的、涉及知识产权的或真实人物的提示词复制到活跃示例中。 |
| 仓库指导 | README、SKILL.md、参考文档、评估 | internal | 保持与来源登记表和 API 状态一致。 | 工作流指导，非平台事实的外部来源。 |

## 必需的声明模式

在回答平台状态问题时，请说：`截至 2026-06-11，公开官方来源将 Seedance 2.0 描述为支持文本、图像、音频和视频输入，包括用于构图、镜头语言、运动节奏、视觉效果和声音的多模态参考。火山引擎记录了首帧/尾帧角色，Runway 记录了一个 Seedance 2 界面，fal 记录了文生视频、图生视频和参考生视频端点，但访问、定价、模型 ID、上传限制、地区、分辨率、音频组合规则和授权行为仍因界面而异，应重新核查。`

在回答定价、配额、上传限制、模型 ID 或地区可用性问题时，不要猜测。说明这些数值是易变动的，需要查看当前官方界面。

在回答相似度、肖像和声音问题时，区分三件事：技术界面支持、权利/授权和提示词安全性。不要从文件上传推断同意。

在使用社区来源时，请说：`现场观察，非保证的平台行为。`