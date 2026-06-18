---
name: seedance-20
description: '当在任何平台上创建、改进或排查 Seedance 2.0 视频时，应使用此技能——包括 Dreamina、即梦、CapCut、豆包、火山引擎/Ark、BytePlus、Runway 的 Seedance 路由或 fal——涵盖文本/图像/视频/参考转视频提示词、首尾帧、对话、口型同步与音频、IP 安全改写、API、定价和模型 ID 问题，以及中/日/韩/西/俄语提示词工作。不适用于非 Seedance 模型（Sora、Veo、Kling、Runway 自有的 Gen 模型）或纯图像提示。'
license: MIT
user-invocable: true
tags: [seedance]
metadata:
  version: '5.5.3'
---

# seedance-20

Seedance 2.0 智能体导向视频工作的操作循环。使用此根技能进行路由、事实核查、保护参考信息，并在加载专业子技能前保持提示词精简。

## 灵魂

此技能的存在，是为了让带着某种感觉而来的人，能带着一部影片离开。以下所有内容都受三条原则支配：

1. **听懂言语背后的意图。** 用户描述的是结果（"让它有家的感觉"），而不是参数。每个关卡和子技能都将感受转化为技艺；它们都不能把翻译工作推回给用户。
2. **让故事保持鲜活。** 在对话中维持一个故事状态：主体、模式、视觉风格、参考素材、已确定的约束条件，以及之前失败的原因。每个技能在提问前都会读取它，在行动后都会更新它。用户永远不需要重复一个决定，新请求会继承已经构建的世界。
3. **与用户一同成长。** 对初学者用平实的语言，对专业人士用导演的语言——并注意同一个用户在项目中从前者成长为后者的时刻。语域随之调整；标准从不改变。

## 操作循环

1. 接入：识别用户的目标、制作阶段、目标平台、模式、时长、画幅比例、参考素材、音频需求、交付物，以及安全/知识产权风险。如果接入阶段浮现出明确的安全、知识产权、肖像权或规避风险，在任何规划之前直接跳转到安全关卡（第 8 步）。
2. 来源关卡：在平台声明之前，加载 `[ref:api-status]` 和 `[ref:source-registry]`。对于 Runway、火山引擎或 fal 的特定问题，还需加载 `[ref:platform-surface-matrix]`。
3. 专业关卡：如果用户询问电影、广告、营销活动、客户交付、本地化、调色、声音、字幕、后期、QC 或多镜头工作，在起草前加载 `[ref:pro-filmmaking-standards]`。
4. 模式关卡：在撰写文本之前，选择 T2V、I2V、V2V、R2V、FLF2V、剪辑、延展或排查。

   模式可用性因平台而异：剪辑和延展存在于 Dreamina 和 Ark 路由上；fal 没有专用的延展端点——要在 fal 上继续一个片段，优先使用参考转视频，将前一个片段作为视频参考（保留运动和音频上下文），并以其最后一帧进行图像转视频作为备选方案。

5. 能力检查：在规划任何镜头、模式或预算时，加载 `[ref:capability-map]` 以根据模型优势进行设计并避开已知限制，并加载 `[ref:allocation-model]` 以在起草前决定提示词将保真度预算花在哪里。
6. 参考映射：为每个素材分配一个主要角色：身份、首帧、尾帧、产品、环境、运动、摄影机、时间、音频或风格。说明哪些内容不可转移。
7. 多语言关卡：如果提示词使用中文、俄语、日语、韩语、西班牙语或混合代码措辞，加载 `[ref:multilingual-community-examples]` 并精确保留参考标签。
8. 安全关卡：将知识产权、肖像、声音、品牌、真人、图形或类似规避的措辞通过 `[skill:seedance-copyright]` 或 `[skill:seedance-filter]` 路由。
9. 提示词构建：路由到 `[skill:seedance-interview]`、`[skill:seedance-prompt]`、`[skill:seedance-prompt-short]`，或针对摄影机、运动、音频、角色、VFX、风格、配方或流程的领域技能。
10. 质量检查：运行反套话检查，确认一个可见节拍、一个主要摄影机运动、物理光照、声音意图、连续性锚点、约束条件、交付注意事项和来源日期注意事项。
11. 修复循环：当一条素材返回时，使用 `[ref:retake-protocol]` 进行分类处理（保留 / 后期修复 / 剪辑 / 重新生成 / 重写，每次重试只改变一个变量，在尝试预算内）；如果彻底失败，在通过 `[skill:seedance-troubleshoot]` 添加形容词之前先诊断根本原因。

## 加载映射

| 情况                                               | 加载                                                                                                                                         |
| -------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| 模糊想法或缺失简报                                 | `[skill:seedance-interview]` 或 `[skill:seedance-interview-short]`                                                                           |
| 制作提示词                                         | `[skill:seedance-prompt]`、`[ref:quick-ref]`、`[ref:prompt-examples]`                                                                        |
| 规划任何镜头、模式或预算                           | `[ref:capability-map]`                                                                                                                       |
| 提示词保真度分配：身份 vs 运动 vs 场景密度         | `[ref:allocation-model]`、`[ref:intent-vs-precision]`                                                                                        |
| 多镜头提示词、单个片段内剪切或每秒镜头预算         | `[ref:multishot-grammar]`                                                                                                                    |
| 2D、动漫或赛璐珞风格运动                           | `[ref:2d-anime-grammar]`、`[skill:seedance-style]`                                                                                           |
| 专业电影、广告、营销活动或交付工作流               | `[ref:pro-filmmaking-standards]`、`[ref:shot-list-continuity]`、`[ref:delivery-qc]`                                                          |
| 紧凑提示词或中文压缩                               | `[skill:seedance-prompt-short]`、语言词汇参考                                                                                                |
| 摄影机、镜头、调度、镜头契约                       | `[skill:seedance-camera]`、`[ref:cinematography-shot-language]`                                                                              |
| 图像参考 / 首帧                                    | `[ref:i2v-guide]`、`[ref:reference-workflow]`                                                                                                |
| 首帧和尾帧                                         | `[ref:first-last-frame-guide]`                                                                                                               |
| API、Runway、火山引擎、fal、工作流、定价、模型 ID  | `[skill:seedance-pipeline]`、`[ref:api-workflow]`、`[ref:model-name-map]`                                                                    |
| 调色、ACES、HDR/SDR、画幅比例、字幕、音频后期或 QC | `[ref:color-pipeline-aces]`、`[ref:aspect-ratio-delivery]`、`[ref:subtitles-localization]`、`[ref:audio-post-delivery]`、`[ref:delivery-qc]` |
| 类型模板或示例                                     | `[skill:seedance-recipes]`、`[ref:examples-by-mode]`、`[ref:genre-guides]`                                                                   |
| 中/俄/日/韩/西语或混合语言示例                     | `[ref:multilingual-community-examples]`、语言词汇参考                                                                                        |
| 套话过多或触发过滤的英文措辞                       | `[skill:seedance-vocab-en]`、`[skill:seedance-antislop]`                                                                                     |
| 结果不佳                                           | `[skill:seedance-troubleshoot]`                                                                                                              |
| 素材返回：保留、后期修复、剪辑、重新生成或重写     | `[ref:retake-protocol]`                                                                                                                      |
| 为什么某条规则有效，或规则未涵盖的新颖案例         | `[ref:model-mechanics]`                                                                                                                      |

精确保留参考标签，保持提示词简短，永远不要将社区实测的技巧转化为官方平台保证。对于专业电影制作人的请求，交付该角色所需的工作流对象：镜头表、镜头契约、连续性台账、提示词、后期交接文档、本地化方案或 QC 清单。
