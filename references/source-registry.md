# 源注册表

last_verified: 2026-05-30

在对 Seedance 2.0 平台行为做出事实性声明之前，请先使用此注册表。优先采用主要公开来源，附上验证日期，并将易变声明标记为"需重新核查"。本文件是一份声明边界映射，而非对每个产品界面或区域访问权限的保证。

## 证据标签

| 标签 | 含义 | 必需措辞 |
|---|---|---|
| `confirmed` | 在验证日期时，主要公开来源中可直接查看到。 | `公开来源声明……截至 [日期]。` |
| `volatile` | 可能因界面、账户、区域、定价页面或模型更新而变化。 | `在提供数字或承诺前请重新核查。` |
| `field-observed` | 创作者/从业者反复观察到的模式，但非官方平台事实。 | `实地观察，非保证的平台行为。` |
| `unverified` | 合理但未获主要来源确认。 | `需要测试或所有者确认。` |
| `internal` | 源自本技能包的仓库指导。 | `用作工作流指导，非外部事实。` |

## 主要来源层级

| 主题 | 首选来源 | 证据标签 | 验证说明 | 声明边界 |
|---|---|---|---|---|
| 核心模型能力 | 字节跳动 Seedance 2.0 官方页面：https://seed.bytedance.com/en/seedance2_0 | confirmed | 在发布说明、API 声明或营销文案前请重新核查。 | 仅用于广泛的公开能力框架描述。 |
| 发布能力与已知限制 | 字节跳动 Seedance 2.0 官方发布博文：https://seed.bytedance.com/en/blog/seedance-2-0-official-launch | confirmed | 在讨论多模态参考、编辑、音频及平台示例时请重新核查。 | 切勿将发布示例转化为每个界面上的保证行为。 |
| 模型卡片与论文 | arXiv 模型卡片：https://arxiv.org/abs/2604.14148 | confirmed | 有助于理解模型家族背景与基准测试注意事项。 | 由提供方撰写的论文；勿用作当前商业访问权限的证明。 |
| API 教程与平台文档 | BytePlus ModelArk 与 Volcengine Ark 文档：https://docs.byteplus.com/en/docs/ModelArk/2291680, https://www.volcengine.com/docs/82379/1520757?lang=zh, 以及 https://www.volcengine.com/docs/82379/2291680?lang=zh | volatile | 在提供程序化 API 指导前，请重新核查端点、请求字段、模型 ID、任务流及定价。 | API 形态可能因区域、账户或发布渠道而异。 |
| 视频生成任务生命周期 | Volcengine 视频生成教程：https://www.volcengine.com/docs/82379/2298881?lang=zh | volatile | 在实现前，请重新核查创建/查询/列表/取消 - 删除流程、首帧/末帧角色、返回末帧、工具及文件引用规则。 | 官方界面，但字段与账户支持可能变更。 |
| 模型 ID 与定价 | Volcengine 模型列表/定价页及 BytePlus 定价页 | volatile | 在引用数字或 ID 前务必立即重新核查。 | Volcengine 价格仅在注明日期、货币、模型、界面及注意事项后方可引用；切勿从不完整的 JS 渲染页面推断 BytePlus 定价。 |
| API 服务生态新闻 | Volcengine 开发者文章：https://developer.volcengine.com/articles/7628567056649125942 | volatile | 用作 API 服务 rollout、安全标准、肖像授权、虚拟人像及 BytePlus 海外服务声明的官方生态/新闻证据。实施前请重新核查文档/控制台。 | 非 API 合约、价格表或权益保证。 |
| BytePlus 定价页面 | BytePlus ModelArk 定价文档：https://docs.byteplus.com/en/docs/ModelArk/1099320 | volatile | 在引用 Seedance 2.0 定价、配额或模型 ID 前，请重新核查实时官方页面或控制台。 | 部分页面在静态抓取时为 JavaScript 渲染；切勿从不完整的静态内容推断当前 Seedance 2.0 定价。 |
| 提示词指南 | Volcengine Seedance 2.0 提示词指南：https://www.volcengine.com/docs/82379/2222480?lang=zh | confirmed | 在添加多模态参考措辞或提示词示例时请重新核查。 | 提示词建议为官方指导，不保证每个界面都开放每项控制。 |
| 首帧/末帧工作流 | Volcengine 教程与 ComfyUI 合作伙伴文档：https://www.volcengine.com/docs/82379/2298881?lang=zh 及 https://docs.comfy.org/zh/tutorials/partner-nodes/bytedance/seedance-2-0 | volatile | Volcengine 文档说明首帧/末帧角色；ComfyUI 使用 FLF2V 工作流术语。在使用确切字段前，请重新核查当前界面。 | `FLF2V` 标签为界面特定，但首帧/末帧能力已在 Volcengine 文档中说明。 |
| 人脸、肖像与语音行为 | 活跃产品界面、官方政策及用户授权 | volatile | 请重新核查当前界面行为与授权上下文。 | 切勿从文件上传推断同意授权。 |
| Runway Seedance 2 界面 | Runway API 与帮助文档：https://docs.dev.runwayml.com/guides/seedance/ 及 https://help.runwayml.com/hc/en-us/articles/50488490233363-Creating-with-Seedance-2-0 | volatile | 在生产环境使用前，请重新核查时长、比例、音频/参考组合规则、区域可用性、套餐要求及 SDK 支持。 | 官方 Runway 界面，非字节跳动/Volcengine API 合约。 |
| Agent Skills 结构 | OpenAI Codex Agent Skills 文档：https://developers.openai.com/codex/skills，OpenAI Academy 插件/skills 说明：https://openai.com/academy/codex-plugins-and-skills/，OpenAI Codex Plugins 文档，及 Agent Skills 开放标准：https://agentskills.io/ | confirmed | 在更改安装指导或根技能布局前请重新核查。 | 打包指导，非 Seedance 平台能力。 |
| Runway MCP 代理界面 | Runway MCP 公告：https://runwayml.com/news/mcp | confirmed | 仅用于代理界面可用性说明。 | 不改变 Seedance 模型能力；套餐与连接器访问权限为 Runway 特定。 |
| 音视频评估术语 | AVBench 与 VABench 论文：https://arxiv.org/abs/2605.24652 及 https://openaccess.thecvf.com/content/CVPR2026/papers/Hua_VABench_A_Comprehensive_Benchmark_for_Audio-Video_Generation_CVPR_2026_paper.pdf | field-observed | 用于音视频同步、跨模态一致性等评估维度。 | 基准测试框架，非产品访问权限或官方 Seedance 性能证明。 |
| 专业镜头语言 | ASC 摄像机运动教育及制作镜头列表实践：https://theasc.com/article/shot-craft-camera-movement/ 及 https://www.studiobinder.com/blog/shot-list-template-free-download/ | field-observed | 用于镜头合约、摄像机运动及镜头列表字段。 | 行业工作流指导，非 Seedance 能力证明。 |
| 连续性实践 | ScreenSkills 剧本监督角色：https://www.screenskills.com/job-profiles/browse/film-and-tv-drama/technical/script-supervisor-film-and-tv-drama/ | field-observed | 用于服装、道具、视线、屏幕方向及笔记等连续性锚点。 | 角色指导，非平台行为。 |
| 色彩管理与 ACES | ACES 文档与 AMF 规范：https://docs.acescentral.com/background/overview/ 及 https://docs.acescentral.com/amf/specification/ | confirmed | 用于色彩流程术语与交接元数据。 | 提示词可描述外观；但无法认证 ACES 合规性。 |
| 画幅比与交付容器 | DCI、ISDCF 及买方/平台规范：https://www.dcimovies.com/dci-specification/ 及 https://registry-page.isdcf.com/ | field-observed | 用于画幅比/容器分离及命名注意事项。 | 始终遵循合同约定的交付规范。 |
| 字幕与隐藏式字幕 | Netflix 定时文本、WebVTT 及无障碍规则：https://partnerhelp.netflixstudios.com/hc/en-us/articles/215758617-Timed-Text-Style-Guide-General-Requirements, https://w3c.github.io/webvtt/, 及 https://www.law.cornell.edu/cfr/text/47/79.1 | volatile | 用于字幕/SDH/强制叙事规划及字幕安全框架。请重新核查买方、语言、区域及平台要求。 | 交付要求因买方、语言、区域及平台而异。 |
| 音频响度与后期 | ITU BS.1770、EBU R128、ATSC A/85 及买方音频规范：https://www.itu.int/rec/R-REC-BS.1770, https://tech.ebu.ch/fr/publications/r128, https://www.atsc.org/atsc-documents/a85-techniques-for-establishing-and-maintaining-audio-loudness-for-digital-television/, 及 https://partnerhelp.netflixstudios.com/hc/en-us/articles/360001794307-Netflix-Sound-Mix-Specifications-Best-Practices-v1-6 | volatile | 用于分轨、M&E、同步、响度及混音交接术语。请重新核查目标买方或平台规范。 | 提示词音频非认证的最终混音。 |
| 交付与质检 | SMPTE IMF、DPP 规范、Netflix 交付规范及 MovieLabs OMC：https://www.smpte.org/standards/st2067, https://www.thedpp.com/specs/, https://partnerhelp.netflixstudios.com/hc/en-us/sections/10066414335891-Delivery-Specifications, 及 https://movielabs.com/ontology-for-media-creation/ | volatile | 用于交付预检及元数据/版本管理指导。在最终交付前请重新核查合同约定的平台规范。 | 合同约定的平台规范优先于通用指导。 |
| 社区实践 | 抖音、哔哩哔哩、CSDN、Reddit、Habr、创作者笔记、工作流截图 | field-observed | 仅用作从业者指导。 | 标记为非官方；勿声明为模型保证。 |
| 本地化与混合语言提示词 | 日语、韩语、西班牙语、俄语及多语言社区指南与论坛观察 | field-observed | 发布前请重新核查公开页面；仅用于词汇与示例结构。 | 代码混合可澄清安全提示词，但切勿将其视为官方过滤行为或安全规避手段。 |
| 社区提示词语料库 | YouMind/OpenLab、公开提示词画廊、论坛合集 | field-observed | 仅在进行安全分类后，挖掘结构、时序、词汇及失败模式。 | 切勿将不安全、涉知识产权或真人提示词复制到活跃示例中。 |
| 仓库指导 | README、SKILL.md、references、evals | internal | 与源注册表及 API 状态保持一致。 | 工作流指导，非平台事实的外部来源。 |

## 必需声明模式

回答平台状态问题时，请表述：`截至 2026-05-30，公开官方来源描述 Seedance 2.0 支持文本、图像、音频及视频输入，包括用于构图、镜头语言、运动节奏、视觉效果及声音的多模态参考。Volcengine 文档说明了首帧/末帧角色，Runway 文档描述了 Seedance 2 界面，但访问权限、定价、模型 ID、上传限制、区域、分辨率、音频组合规则及授权行为仍为界面特定，应重新核查。`

回答定价、配额、上传限制、模型 ID 或区域可用性问题时，切勿猜测。请声明这些值为易变项，需核查当前官方界面。

回答肖像、人像及语音问题时，请区分三件事：技术界面支持、权利/授权及提示词安全。切勿从文件上传推断同意授权。

使用社区来源时，请表述：`实地观察，非保证的平台行为。`