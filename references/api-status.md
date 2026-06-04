# Seedance 2.0 API 与平台状态

last_verified: 2026-05-30
confidence: 截至验证日期的公开来源快照；不保证在所有平台上对访问权限、定价、模型 ID、上传限制、授权行为或区域可用性的承诺

## 来自公开来源的确认信息

- 字节跳动官方 Seedance 2.0 页面描述了一个统一的多模态音视频架构，支持文本、图像、音频和视频输入。
- 字节跳动的发布文章指出，Seedance 2.0 最多可使用 9 张图片、3 段视频片段、3 段音频片段，以及自然语言指令。
- 官方材料说明参考素材可指导视觉构图、镜头语言、运动节奏、视觉效果及声音特征。
- 官方材料描述了视频扩展与编辑作为支持的创意工作流程。
- 官方材料描述了 15 秒多镜头音视频输出及双声道音频。
- arXiv 模型卡片有助于了解模型系列背景，包括 4-15 秒音视频生成、论文中原生的 480p/720p 帧率，以及 Fast 变体。
- Volcengine/Ark 文档发布了 Seedance 2.0 教程和视频生成 API 导航，包括创建/查询/列表/取消 - 删除任务流程，但具体的模式、价格、模型 ID、区域和限制需实时重新核查。
- Volcengine 的模型列表页面观察到于 2026-05-29 更新。
- Volcengine 的 Seedance 2.0 教程观察到于 2026-05-29 更新，仍列出 `doubao-seedance-2-0-260128` 和 `doubao-seedance-2-0-fast-260128`。
- Volcengine 的通用视频生成教程观察到于 2026-05-29 更新，是当前重新核查任务生命周期、首/末帧角色、返回末帧、网络搜索工具及文件/参考素材组合的首选官方渠道。
- Volcengine 的提示词指南观察到于 2026-05-15 更新，并强化了多模态参考提示。
- Volcengine 的定价页面观察到于 2026-05-28 更新。引用 Volcengine 价格时，必须注明平台、日期、货币、模型/分辨率/时长背景，并附上重新核查警告。对于未经实时验证的 JavaScript 渲染 BytePlus 页面，请保留更强的"不报价"免责声明。
- 一篇 Volcengine 开发者社区文章称 Seedance 2.0 API 服务已上线，并提及肖像/版权安全标准、人脸验证、肖像授权、虚拟肖像资产及 BytePlus 海外 API 服务。请将此视为官方生态/新闻证据，而非 API 合约。
- 公开的 BytePlus 页面在静态抓取时可能为 JavaScript 渲染。未经实时官方验证，切勿引用此类页面中的 Seedance 2.0 BytePlus 定价或模型 ID。
- Runway 官方 Seedance 2 API 指南记录了模型 `seedance2`、5-15 秒时长、图像/视频/音频参考素材、通过 `runway://` 的上传处理、音频组合规则，以及 `referenceAudio` 的 SDK 类型延迟。
- 如 ComfyUI 等合作伙伴工作流文档暴露了 T2V、R2V 和 FLF2V 工作流术语，但这些文档具有平台特异性。
- 近期的音视频生成基准论文，包括 AVBench 和 VABench，有助于理解音视频一致性等评估术语，但它们并非 Seedance 平台访问来源。

## 操作措辞建议

除非有更新的原始来源说明，否则请使用以下措辞：

> 截至 2026-05-30，字节跳动公开来源将 Seedance 2.0 描述为支持文本、图像、音频和视频输入的统一多模态音视频生成模型。官方发布和模型卡片材料指出，参考素材最多可包含 9 张图片、3 段视频片段和 3 段音频片段。Volcengine/Ark 和 Runway 发布了当前的 Seedance 2 文档，但访问权限、模型 ID、定价、文件限制、区域可用性、分辨率、音频组合规则及肖像授权均具有平台特异性，生产使用前必须重新核查。

## 模型命名规则

- 使用 `Seedance 2.0` 指代官方视频模型系列。
- 仅当活跃平台明确展示 Fast 变体时，才使用 `Seedance 2.0 Fast`。
- 仅针对 Runway 的 API 平台使用 `seedance2`。
- 未经当前来源支持，勿将 `Seedance 2.0 Pro` 称为官方视频模型名称。请将其视为模糊的封装层或社区用语。
- 勿将 `Seed2.0 Pro` 或 Doubao/Seed 通用模型名称与 Seedance 视频生成混淆。

参见 [`model-name-map.md`](model-name-map.md)。

## 声明边界

- 说明 API 可用性、定价、模型 ID、上传限制、权限规则、速率限制及区域可用性必须对照当前原始来源进行核查。
- 除非当前原始来源明确说明，否则避免声称某 API 在全球范围内可用或不可用。
- 除非当前原始来源明确说明，否则避免声称人脸或肖像上传普遍支持或普遍禁止。
- 区分模型能力与产品平台行为。Dreamina/Jimeng、Doubao、Volcengine/Ark、BytePlus/ModelArk、ComfyUI 及第三方封装层可能存在差异。
- 将第三方封装层的价格和模型别名视为封装层特定信息，而非官方信息。

## 已知限制类别

官方/提供方材料及实地观察指出以下方面较为脆弱：

- 细节稳定性，
- 超写实效果，
- 动态活力，
- 多主体一致性，
- 文本渲染，
- 复杂编辑，
- 音频失真，
- 多说话人口型同步，
- 产品/标识保留，
- 真人授权及平台门控。

## 真人、肖像与语音规则

真人人脸、肖像和语音工作流需要授权、法律/伦理合规性以及平台特定支持。切勿从已上传素材推断获得许可。在未获得明确授权且符合适用规则及用户同意要求的工作流情况下，切勿协助模仿公众人物、私人个体、名人或声音。

## 需重新核查的原始来源

- https://seed.bytedance.com/en/seedance2_0
- https://seed.bytedance.com/en/blog/seedance-2-0-official-launch
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
- https://docs.dev.runwayml.com/guides/seedance/
- https://help.runwayml.com/hc/en-us/articles/50488490233363-Creating-with-Seedance-2-0
- https://docs.comfy.org/zh/tutorials/partner-nodes/bytedance/seedance-2-0
- https://arxiv.org/abs/2605.24652
- https://openaccess.thecvf.com/content/CVPR2026/papers/Hua_VABench_A_Comprehensive_Benchmark_for_Audio-Video_Generation_CVPR_2026_paper.pdf