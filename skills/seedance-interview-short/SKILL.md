---
name: seedance-interview-short
description: '当用户需要快速生成 Seedance 2.0 创意简报、简短访谈、压缩式需求采集流程，或在撰写提示词前进行导演风格快速澄清时，应使用此技能。'
---

# seedance-interview-short

当速度优先于详尽创意挖掘时使用此技能。目标是通过不超过三个问题，将模糊想法转化为紧凑的导演简报，随后转入提示词撰写阶段。

## 流程

最多提出三个问题，且仅当答案会实质性影响提示词内容时才提问。优先级如下：

1. 主体在做什么？最终帧时发生了什么变化？
2. 期望呈现何种感受：产品润色、戏剧感、喜剧、写实、动画、动作或氛围？
3. 是否有图像、视频或音频参考素材？每项素材应控制哪些内容？

若用户已提供足够信息，则无需提问，立即生成简报。

## 精简简报模式

`Mode: [T2V/I2V/V2V/R2V]. Subject: [anchor]. Beat: [before -> action -> final state]. Camera: [one move]. Light/style: [physical source and safe descriptor]. Sound: [dialogue/ambience/SFX/music/silence]. Constraints: [identity, IP, safety, product, prompt budget].`

## 路由规则

若需完整制作级提示词，路由至 `skills/seedance-prompt/SKILL.md`；若需精简提示词，路由至 `skills/seedance-prompt-short/SKILL.md`；若涉及 IP/肖像风险，路由至 `skills/seedance-copyright/SKILL.md`；若用户从不良结果出发，路由至 `skills/seedance-troubleshoot/SKILL.md`。

## 输出约定

返回一份 150 字以内的精简简报、任何缺失的高影响力问题，以及推荐的路由技能。
