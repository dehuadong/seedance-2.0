---
name: seedance-20
description: '当指导 Seedance 2.0 T2V、I2V、V2V、R2V、音频、安全或 API 相关工作时，应使用此技能。'
user-invocable: true
---

# seedance-20

Seedance 2.0 面向智能体导向视频工作的操作循环。使用此根技能进行路由、事实核查、参考保护，并在加载专业子技能前保持提示词简洁。

## 操作循环

1. 需求接入：明确用户目标、制作阶段、目标平台、模式、时长、宽高比、参考素材、音频需求、交付物及安全/知识产权风险。
2. 来源把关：在提出平台相关声明前，加载 `references/api-status.md` 和 `references/source-registry.md`。若涉及 Runway 或 Volcengine 的具体内容，还需加载 `references/platform-surface-matrix.md`。
3. 专业把关：若用户提出电影、广告、营销活动、客户项目、交付、本地化、调色、声音、字幕、后期、质检或多镜头制作需求，起草前需加载 `references/pro-filmmaking-standards.md`。
4. 模式把关：在撰写正文前，先确定采用 T2V、I2V、V2V、R2V、FLF2V、编辑、扩展或故障排查模式。
5. 参考映射：为每个素材分配一个主要角色：身份、首帧、末帧、产品、环境、运动、摄像机、时序、音频或风格。明确说明哪些内容不得迁移。
6. 多语言把关：若提示词使用中文、俄语、日语、韩语、西班牙语或混合语言表述，加载 `references/multilingual-community-examples.md` 并精确保留参考标签。
7. 安全把关：将涉及知识产权、肖像、声音、品牌、真人、图形内容或规避性表述的内容，通过 `skills/seedance-copyright/SKILL.md` 或 `skills/seedance-filter/SKILL.md` 进行路由处理。
8. 提示词构建：路由至 `skills/seedance-interview/SKILL.md`、`skills/seedance-prompt/SKILL.md`、`skills/seedance-prompt-short/SKILL.md`，或针对摄像机、运动、音频、角色、视觉特效、风格、配方或流程的领域技能。
9. 质量检查：执行反低质内容检测，检查一个可见节奏点、一个主摄像机运动、物理光照、声音意图、连续性锚点、约束条件、交付注意事项及来源日期注意事项。
10. 修复循环：若输出失败，先诊断根本原因再添加修饰词；使用 `skills/seedance-troubleshoot/SKILL.md`。

## 加载映射

| 情境                                              | 加载内容                                                                                                                                                                             |
| ------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 想法模糊或缺乏简报                                | `skills/seedance-interview/SKILL.md` 或 `skills/seedance-interview-short/SKILL.md`                                                                                                   |
| 制作提示词                                        | `skills/seedance-prompt/SKILL.md`、`references/quick-ref.md`、`references/prompt-examples.md`                                                                                        |
| 专业电影、商业广告、营销活动或交付工作流          | `references/pro-filmmaking-standards.md`、`references/shot-list-continuity.md`、`references/delivery-qc.md`                                                                          |
| 简洁提示词或中文压缩                              | `skills/seedance-prompt-short/SKILL.md`、语言词汇参考                                                                                                                                |
| 摄像机、镜头、场面调度、镜头合约                  | `skills/seedance-camera/SKILL.md`、`references/cinematography-shot-language.md`                                                                                                      |
| 图像参考/首帧                                     | `references/i2v-guide.md`、`references/reference-workflow.md`                                                                                                                        |
| 首帧与末帧                                        | `references/first-last-frame-guide.md`                                                                                                                                               |
| API、Runway、Volcengine、工作流、定价、模型 ID    | `skills/seedance-pipeline/SKILL.md`、`references/api-workflow.md`、`references/model-name-map.md`                                                                                    |
| 调色、ACES、HDR/SDR、宽高比、字幕、音频后期或质检 | `references/color-pipeline-aces.md`、`references/aspect-ratio-delivery.md`、`references/subtitles-localization.md`、`references/audio-post-delivery.md`、`references/delivery-qc.md` |
| 类型模板或示例                                    | `skills/seedance-recipes/SKILL.md`、`references/examples-by-mode.md`、`references/genre-guides.md`                                                                                   |
| 中文/俄语/日语/韩语/西班牙语或混合语言示例        | `references/multilingual-community-examples.md`、语言词汇参考                                                                                                                        |
| 效果不佳                                          | `skills/seedance-troubleshoot/SKILL.md`                                                                                                                                              |

精确保留参考标签，保持提示词简短，切勿将实地观察到的社区技巧转化为官方平台保证。针对专业电影制作人的需求，交付该角色所需的工作流对象：镜头列表、镜头合约、连续性记录、提示词、后期交接文档、本地化方案或质检清单。
