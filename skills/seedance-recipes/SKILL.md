---
name: seedance-recipes
description: '当用户请求 Seedance 2.0 模板、类型配方、产品广告、生活视频、戏剧场景、音乐视频、风景镜头、商业广告、动画场景或可复用的制作模式时，应使用此技能。'
---

# seedance-recipes

将配方作为起始模式使用，而非僵化的提示词模板。选择与用户目标匹配的配方，然后自定义主体、动作、摄像机、灯光、音频及约束条件。配方应保持短视频的"单节拍"原则。

当需要类型模式时加载 `references/genre-guides.md`，当用户需要可直接复制的示例时加载 `references/examples-by-mode.md`，当涉及专业多镜头序列或商业广告时加载 `references/shot-list-continuity.md`，当配方需体现中文/俄语/日语/韩语/西班牙语社区风格结构时加载 `references/multilingual-community-examples.md`。

## 配方家族

| 家族     | 最佳用途                                              | 核心模式                                                                            |
| -------- | ----------------------------------------------------- | ----------------------------------------------------------------------------------- |
| 产品     | 广告、电商、主打镜头、材质展示                        | `product anchor + one material change + controlled camera + logo preservation`      |
| 生活     | 人物使用、美食、旅行、社交短片                        | `simple action + lived environment + handheld or natural light + ambient sound`     |
| 戏剧     | 情感、对话、简短叙事节拍                              | `character tag + gesture + motivated camera + silence or sparse sound`              |
| 音乐视频 | 节拍同步、舞蹈、风格化剪辑                            | `rhythm reference + visible beat changes + light pulses + clear character blocking` |
| 风景     | 建立镜头、自然、氛围                                  | `slow camera + weather motion + layered depth + natural sound`                      |
| 商业广告 | 品牌安全润色与功能展示                                | `problem/use/result beat + precise product constraint + clean light`                |
| 动画     | 原创角色与风格化动作                                  | `medium + shape language + palette + elastic or weighted motion`                    |
| 视觉特效 | 变形、粒子、天气、能量效果                            | `source + material behavior + interaction + dissipation endpoint`                   |
| 首/尾帧  | 中间过渡、产品状态变化、角色姿态目标                  | `first frame + last frame + continuous transition + identity locks`                 |
| 商业活动 | 6/10/15/30 秒变体、竖屏/社交精简版、无文字/本地化母版 | `hook + product proof + end state + cutdown matrix + delivery notes`                |

## 提示词骨架

**产品 I2V：** `[Image1] 为产品参考；精确保留徽标、标签、形状及材质。[一项材质或灯光变化]。摄像机：[单一运动]。灯光：[物理光源]。音效：[环境音/音效]。`

**戏剧 T2V：** `角色 A 在 [具体场景] 中执行 [可见的情感动作]。摄像机：[有动机的构图]。灯光：[有动机的光源]。音效：[环境音或简短对话]。结束状态：[表情/动作变化]。`

**参考动作：** `[Video1] 仅提供 [摄像机/动作/时机] 参考；不迁移身份、服装、徽标或环境。新主体：[授权/原创主体]。[动作与终点]。`

**首/尾帧：** `[Image1] 为起始帧。[Image2] 为结束帧。保留 [身份/产品/场景锚点]。生成从 [起始状态] 到 [结束状态] 的连续过渡。摄像机：[锁定或单一可控运动]。音效：[环境音/音效]。`

**动画：** `原创 [角色原型] 在 [环境] 中执行 [动作]。风格：[媒介、线条质感、纹理、调色板]。动作：[节奏]。摄像机与音效：[简洁辅助]。`

## 选择规则

若用户提出多个目标，选择能保护最脆弱需求的配方。产品识别度优于摄像机炫技；口型同步优于大幅头部动作；角色一致性优于复杂编舞；首/尾帧目标精度优于额外风格变化；安全与授权优于风格模仿。

## 输出约定

返回一项选定的配方、适配理由、自定义提示词骨架、精简最终提示词，以及在相关时附上活动/交付说明。
