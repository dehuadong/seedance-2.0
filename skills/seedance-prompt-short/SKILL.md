---
name: seedance-prompt-short
description: '当用户请求精简版 Seedance 2.0 提示词、简短中文提示词、提示词压缩、30-100 字输出，或移除不必要的提示词语言时，应使用此技能。'
---

# seedance-prompt-short

在不丢失制作信号的前提下压缩 Seedance 提示词。简短提示词仍需在有用时包含模式、主体、动作、摄像机、灯光、音效及约束条件。先删除填充词，再删除物理细节。

## 压缩优先级

按以下顺序保留内容：

1. 参考标签及其作用。
2. 主体或产品识别信息。
3. 动作动词及可见终点。
4. 一项摄像机运动。
5. 物理光源或氛围。
6. 音频提示或静音指令。
7. 安全、知识产权或连续性约束。

在删除保留约束之前，先删除通用形容词、重复风格标签、明显的背景细节、次要摄像机运动和次要动作。

对于双语或混合语言压缩，加载 `references/multilingual-community-examples.md`。仅保留能明确参考角色、对话、摄像机术语或安全制作约束的语言混合形式。

## 精简模板

| 需求 | 模板                                                                                                                                           |
| ---- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| T2V  | `[Subject] [action and endpoint] in [scene]. Camera: [one move]. Light/style: [physical source]. Sound: [cue]. Constraint: [risk/continuity].` |
| I2V  | `[Image1] preserved; only [motion/light/camera] changes. Camera: [one move]. Sound: [cue]. Constraint: [what must not change].`                |
| V2V  | `[Video1] controls [motion/camera/timing] only; new subject [anchor]. [Action]. Do not transfer [identity/scene/logo].`                        |
| 中文 | `[Image1]为参考，严格保持[主体]不变；仅加入[动作/光线/镜头]。声音：[提示]。`                                                                   |

## 输出约定

返回一个精简提示词，理想长度为 30-100 个英文单词；若用户要求中文或最大程度压缩，则提供等效中文提示词。仅当有重要内容被移除时，附加一行说明。
