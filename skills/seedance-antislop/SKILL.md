---
name: seedance-antislop
description: '当 Seedance 2.0 提示词包含通用 AI 填充词、空洞最高级、模糊电影语言、冗余形容词、弱动词，或需要更精准的制作导向措辞时，应使用此技能。'
---

# seedance-antislop

移除掩盖缺失视觉决策的填充内容。优秀的 Seedance 提示词使用可观察的名词、动词、摄像机运动、光源、音效提示及约束条件。弱提示词要求"卓越"却不说明卓越在视觉或听觉上具体呈现为何。

## 可见性测试

每个主要短语应能被摄像机捕捉、被测光表测量、在混音中可闻，或作为运动可观察。若短语无法通过该测试，则用制作语言替换。

| 填充词               | 追问其含义                       | 强替换模式                                                                                       |
| -------------------- | -------------------------------- | ------------------------------------------------------------------------------------------------ |
| cinematic（电影感）  | 什么摄像机和灯光使其具有电影感？ | `locked close-up, warm practical key, cool rim light`（锁定特写，暖色实景主光，冷色轮廓光）      |
| epic（史诗感）       | 规模或风险是什么？               | `wide low-angle shot, tiny figure against storm wall`（广角低角度镜头，微小人物对抗风暴墙）      |
| beautiful（美丽）    | 什么色彩、质感或光线行为？       | `pearl highlights on wet ceramic, soft window bounce`（湿润陶瓷上的珍珠高光，柔和窗户反射光）    |
| dynamic（动态）      | 什么在动、多快、终点在哪？       | `fast lateral track ending on the hero label`（快速横向跟拍，终点聚焦主打标签）                  |
| professional（专业） | 什么制作设置？                   | `clean commercial tabletop, controlled reflection, no clutter`（干净商业桌面，受控反射，无杂乱） |

## 重写流程

首先，标出所有最高级和模糊风格标签。其次，决定每个词应转化为摄像机、灯光、运动、材质、声音或约束语言。第三，减少重复项。第四，确保提示词在字符预算内并保留参考标签。

## 勿过度修正

当类型语言与具体指导配对时，勿移除有用的类型术语。`Noir hallway with hard venetian-blind shadows`（带有硬百叶窗阴影的黑色电影走廊）是有用的；`dramatic cinematic noir vibes`（戏剧性电影感黑色氛围）则无用。保留能传达媒介、时代、调色板或镜头行为的术语。

加载 `references/anti-slop-lexicon.md` 获取扩展替换词表。

## 输出约定

返回已移除词汇、按摄像机/灯光/运动/声音/约束分组的替换项，以及精简后的提示词。
