# Seedance 2.0 API 与平台状态

最后验证时间：2026-06-13
置信度：截至验证日期的公开来源快照；各章节适用日期已注明（海外 API 状态和 Replicate 记录于 2026-06-13，fal 部分重新验证于 2026-06-11，早期表面信息验证于 2026-05-30）；不保证各表面上的访问权限、定价、模型 ID、上传限制、授权行为或区域可用性。

## 已从公开来源确认的信息

- ByteDance 官方 Seedance 2.0 页面将其描述为支持文本、图像、音频和视频输入的统一多模态音视频架构。
- ByteDance 发布文章称 Seedance 2.0 可使用最多 9 张图像、3 个视频片段、3 个音频片段，外加自然语言指令。
- 官方材料称参考内容可引导视觉构图、镜头语言、运动节奏、视觉效果和声音特征。
- 官方材料将视频扩展和编辑描述为支持的创意工作流。
- 官方材料描述为 15 秒多镜头音视频输出，支持双声道音频。
- arXiv 模型卡对了解模型系列背景有帮助，包括论文中提到的 4-15 秒音视频生成、原生 480p/720p 画幅，以及 Fast 变体。
- Volcengine/Ark 文档发布了 Seedance 2.0 教程和视频生成 API 导航，包含创建/查询/列表/取消删除任务流程，但具体模式、价格、模型 ID、区域和限制需实时重新确认。
- Volcengine 模型列表页面于 2026-05-29 观察到更新。
- Volcengine 的 Seedance 2.0 教程于 2026-05-29 观察到更新，仍列出 `doubao-seedance-2-0-260128` 和 `doubao-seedance-2-0-fast-260128`。
- Volcengine 通用视频生成教程于 2026-05-29 观察到更新，是目前重新确认任务生命周期、首帧/尾帧角色、返回尾帧、联网搜索工具以及文件/参考组合的第一方官方位置。
- Volcengine 提示词指南于 2026-05-15 观察到更新，强化了多模态参考提示。
- Volcengine 定价页面于 2026-05-28 观察到更新。引用 Volcengine 价格时须附带表面、日期、货币、模型/分辨率/时长上下文以及重新确认警告。对于未经实时验证的 JavaScript 渲染 BytePlus 页面，保留更严格的不引用价格声明。
- 一篇 Volcengine 开发者社区文章称 Seedance 2.0 API 服务已上线，并提及肖像/版权安全标准、人脸验证、肖像授权、虚拟肖像资产以及 BytePlus 海外 API 服务。将此视为官方生态系统/新闻证据，而非 API 合同。
- 公开的 BytePlus 页面可能在静态获取时采用 JavaScript 渲染。未经官方实时验证，不要从这类页面引用 Seedance 2.0 BytePlus 定价或模型 ID。
- Runway 官方 Seedance 2 API 指南记录了模型 `seedance2`，5-15 秒时长，图像/视频/音频参考，通过 `runway://` 处理上传，音频组合规则，以及 `referenceAudio` 的 SDK 类型延迟。
- ComfyUI 等合作伙伴工作流文档暴露了 T2V、R2V 和 FLF2V 工作流词汇，但这些文档是针对特定表面的。
- 最近的音视频生成基准论文，包括 AVBench 和 VABench，对围绕音视频一致性的评估词汇有帮助，但它们不是 Seedance 平台访问来源。

## 海外 API 状态 — 版权暂停 *(记录于 2026-06-13)*

权威报道（Variety 和 CNBC，2026 年 2-3 月）记载，在 Seedance 2.0 于 2026-02-12 在中国上线后，迪士尼、华纳兄弟、派拉蒙、Netflix 和美国电影协会向 ByteDance 发送了停止侵权函，指控其侵犯知识产权，ByteDance **暂停了原计划的海外 API 推出（约 2026-03-15）**，等待问题解决并增加了保护措施。这对指导意味着：

- 将海外/全球 Seedance 2.0 API 访问视为**有争议且不稳定的**，而非保证可用。在依赖任何表面之前，请验证实时访问权限、区域和权利状态。
- 第三方表面（fal、Atlas Cloud、Replicate 等）在不同日期显示过实时的 Seedance 2.0 端点；这并不代表已建立稳定的官方全球可用性——访问权限已经变化并可能再次变化。生产使用前请立即重新确认。
- 该争议使本仓库的固定规则具有操作性，而非假设：切勿复制受保护的角色、场景或真人肖像——正是这种行为触发了暂停。

## 平台保护措施 — 现已上线 *(记录于 2026-06-14)*

权威报道（SCMP、CNBC、The Next Web，2026 年 2-4 月）记录了 ByteDance 为应对争议而向 Seedance 2.0 增加的保护措施。这些不再是假设——将其视为官方表面上的当前平台行为，并设计提示词以*配合*这些措施工作：

- **真人面部输入拦截：** 包含真人面部的图像或视频生成受到限制（反深度伪造）。不要假定真人参考会被接受；将肖像类工作通过 `[skill:seedance-copyright]` 路由。
- **受版权保护角色拦截：** 生成可识别的受保护角色（如史莱克、海绵宝宝、达斯·维达）被阻止。这是强制执行，而不仅仅是政策——`[skill:seedance-filter]` 的原创角色改写是可行的路径。
- 输出上带有**可见水印 + C2PA 内容凭证**，以及**不可见水印**配合主动 IP 监控（ByteDance 声明其能够识别并针对模型输出采取行动，即使在被分享或修改后）。

对本技能的影响：误报修复和 IP 安全改写不是可选的润色——而是提示词通过实时防护栏的方式。特定表面的行为仍然不同；请在活动表面上进行验证。

## 分辨率 — 模型与表面的差异 *(记录于 2026-06-14)*

一手来源（arXiv 模型卡和 ByteDance Seed 页面）指出 Seedance 2.0 的**原生输出分辨率为 480p/720p**。更高分辨率是**特定于表面的，非模型原生保证**，即使同一表面的文档也可能不一致：Volcengine/Ark (Pro)、BytePlus、Atlas Cloud、Runway 和 WaveSpeed 显示 **1080p**；fal 的文字指南称 480p/720p，而其模型和定价页面列出 1080p（参见下方 fal 部分）。将 480p/720p 视为基线能力，任何 1080p/"2K" 声明视为调用时需按端点验证的特定表面功能——而非通用模型规格。

## fal — 授权提供商，全球 *(添加于 2026-06-10；字段、分辨率和定价于 2026-06-11 重新验证)*

**端点：** `text-to-video`、`image-to-video`（起始图像 + 可选的 `end_image_url` 用于 A→B）、`reference-to-video`——每个都有 `/fast` 层级。
**时长：** 4-15 秒或 `auto`（模型根据提示词复杂度调整；多镜头 → 更长）。**宽高比：** 21:9 / 16:9 / 4:3 / 1:1 / 3:4 / 9:16 / auto。
**参数（t2v）：** `prompt`、`resolution`、`duration`、`aspect_ratio`、`generate_audio`（默认开启；**音频包含在内，不额外计费**）、`seed`（**可复现性辅助，非硬锁定** — 即使使用相同种子，输出也可能不同）。
**参数（i2v）：** t2v 字段加上 `image_url`（起始帧）和可选的 `end_image_url`（A→B）。不要将图像字段发送到 t2v 端点。
**参数（r2v）：** 参考素材放入数组字段 `image_urls`、`video_urls`、`audio_urls`（于 2026-06-11 验证）——不要将 i2v 的 `image_url`/`end_image_url` 字段复用于参考；实施前请重新确认实时模式。
**参考（r2v）：** @Image×9、@Video×3、@Audio×3，≤12 个文件。图像 JPEG/PNG/WebP ≤30 MB；视频 480–720p，合计 ≤15 秒，总大小 <50 MB；音频 MP3/WAV 每个 ≤15 MB，合计 ≤15 秒；**音频需要至少 1 张图像或 1 个视频。**
**分辨率（于 2026-06-11 验证）：** 标准端点列出 480p/720p/**1080p（约 $0.682/秒）**；fast 层级上限为 720p。文字指南曾落后于模式——请在调用时按端点验证。
**定价（引用前请实时验证）：** 720p 标准约 $0.30/秒 · fast 约 $0.24/秒 · 视频参考 ×0.6 · 1080p 约 $0.682/秒。
**提示方式：** 散文式指导；`Shot 1:/Shot 2:` 标签用于多镜头；r2v 文档也接受时间节奏短语作为次要提示。**Fast 层级：** fal 官方文档为 fast 端点提供相同的模式和多镜头支持；实地报告仍偏向标准层级用于多镜头、慢动作和轨道车运动——将其视为实地指导，而非提供商文档。
**无专用扩展端点** — 扩展是 Dreamina 应用功能。要在 fal 上继续片段，首选使用前一片段作为视频参考进行 reference-to-video（保留运动和音频上下文）；从前一片段最后一帧链式调用 image-to-video 是备选方案。

## 操作用语

除非更新的主要来源另有说明，否则使用此用语：

> 截至 2026-05-30，公开的 ByteDance 来源将 Seedance 2.0 描述为具有文本、图像、音频和视频输入的统一多模态音视频生成模型。官方发布和模型卡材料称参考内容可包括最多 9 张图像、3 个视频片段和 3 个音频片段。Volcengine/Ark 和 Runway 发布当前的 Seedance 2 文档，但访问权限、模型 ID、定价、文件限制、区域可用性、分辨率、音频组合规则和肖像授权仍取决于具体表面，在生产使用前必须重新确认。

## 模型命名规则

- 使用 `Seedance 2.0` 指代官方视频模型系列。
- 仅当活动表面暴露 Fast 变体时使用 `Seedance 2.0 Fast`。
- 仅对 Runway 的 API 表面使用 `seedance2`。
- 在没有当前来源的情况下，不要将 `Seedance 2.0 Pro` 称为官方视频模型名称。将其视为含义模糊的封装器或社区用语。
- 不要将 `Seed2.0 Pro` 或 Doubao/Seed 通用模型名称与 Seedance 视频生成混淆。

参见 [`model-name-map.md`](model-name-map.md)。

## 声明边界

- 说明 API 可用性、定价、模型 ID、上传限制、授权规则、速率限制和区域可用性必须对照当前一手来源进行核实。
- 除非当前一手来源明确说明，否则避免声称 API 在全球可用或不可用。
- 除非当前一手来源明确说明，否则避免声称面部或肖像上传普遍支持或普遍被阻止。
- 将模型能力与产品表面行为分开。Dreamina/即梦、Doubao、Volcengine/Ark、BytePlus/ModelArk、ComfyUI、fal 和第三方封装器可能存在差异。
- 将第三方封装器的价格和模型别名视为封装器特定的，而非官方。

## 已知限制类别

官方/提供商材料和实地观察指出以下领域较为脆弱：

- 细节稳定性，
- 超写实效果，
- 动态活力，
- 多主体一致性，
- 文字渲染，
- 复杂编辑，
- 音频失真，
- 多说话人口型同步，
- 产品/标识保留，
- 真人授权和表面门槛。

## 真人、肖像和声音规则

真人面部、肖像和声音工作流需要授权、法律/道德合规以及平台特定支持。不要从上传的素材推断许可。未经明确授权且符合适用规则和用户同意要求的工作流，不要帮助模仿公众人物、私人个体、名人或声音。

## 需要重新确认的一手来源

- https://seed.bytedance.com/en/seedance2_0
- https://seed.bytedance.com/en/blog/seedance-2-0-official-launch
- https://replicate.com/bytedance/seedance-2.0
- https://variety.com/2026/film/news/paramount-disney-bytedance-cease-and-desist-seedance-ai-infringement-ip-1236663663/
- https://www.cnbc.com/2026/02/16/bytedance-safegaurds-seedance-ai-copyright-disney-mpa-netflix-paramount-sony-universal.html
- https://arxiv.org/abs/2604.14148
- https://www.volcengine.com/docs/82379/1330310?redirect=1&lang=zh
- https://www.volcengine.com/docs/82379/1520757?lang=zh
- https://www.volcengine.com/docs/82379/2291680?lang=zh
- https://www.volcengine.com/docs/82379/2298881?lang=zh
- https://www.volcengine.com/docs/82379/2222480?lang=zh
- https://www.volcengine.com/docs/82379/1544106?lang=zh
- https://developer.volcengine.com/articles/7628567056649125942
- https://docs.byteplus.com/en/docs/ModelArk/2291680
- https://docs.byteplus.com/en/docs/ModelArk/1099320
- https://fal.ai/models/bytedance/seedance-2.0/text-to-video
- https://fal.ai/models/bytedance/seedance-2.0/image-to-video
- https://fal.ai/models/bytedance/seedance-2.0/reference-to-video
- https://docs.dev.runwayml.com/guides/seedance/
- https://help.runwayml.com/hc/en-us/articles/50488490233363-Creating-with-Seedance-2-0
- https://docs.comfy.org/zh/tutorials/partner-nodes/bytedance/seedance-2-0
- https://arxiv.org/abs/2605.24652
- https://openaccess.thecvf.com/content/CVPR2026/papers/Hua_VABench_A_Comprehensive_Benchmark_for_Audio-Video_Generation_CVPR_2026_paper.pdf