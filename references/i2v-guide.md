# 图像转视频指南

## 核心规则

仅提示图像无法呈现的内容。静态图像已包含主体身份、产品形态、服饰搭配、色彩基调、构图布局与背景环境。重复描述这些静态细节往往会导致画面漂移。请补充运动、镜头、时序、形变、光影变化、音频及保真约束。

## 极简模板

`[Image1] 为参考；精确保留 [身份/产品/场景]。仅 [运动] 发生变化。镜头：[单一运镜]。光影：[光源或过渡]。音效：[提示音]。约束：[禁止变更的内容]。`

## 保真表述

对易失锚点使用精准锁定：`preserve face identity`（保留面部身份）、`preserve logo and label`（保留标识与标签）、`preserve bottle shape and cap geometry`（保留瓶身形状与瓶盖几何结构）、`preserve outfit and hairstyle`（保留服饰与发型）、`preserve room layout`（保留房间布局）。若场景需要自然动态，无需锁定全部元素，仅锁定必须保持稳定的部分。

## 优质 I2V 补充项

| 补充项 | 示例 |
|---|---|
| 微表情 | `subject blinks once and lowers their eyes`（主体眨眼一次并垂下目光） |
| 产品光影 | `thin highlight travels across the label`（一道纤细高光掠过标签表面） |
| 天气效果 | `rain streaks behind the subject; droplets bead on the surface`（主体身后雨丝斜落；水珠在表面凝结成滴） |
| 镜头运动 | `slow dolly-in from current composition to tighter detail`（从当前构图缓慢推近至更紧凑的细节特写） |
| 氛围渲染 | `dust catches the doorway beam and settles`（尘埃捕捉门框光束并缓缓沉降） |
| 音频提示 | `soft room tone, one key click at the endpoint`（柔和环境底噪，终点处一声按键轻响） |

## 失败修复方案

- 若身份漂移：减少新增视觉描述，强化保真约束。
- 若镜头跳跃：使用单一运镜，明确起点与终点。
- 若产品形变：声明"保留、静态身份、无形状变化、无产品形变"。
- 若输出静止：添加一个物理动作 + 一个时间提示。
- 若背景变化：保留环境布局，仅让光影、天气或氛围产生动态。
- 若手部变形：简化手部动作，或让手部避开主要动作区域。