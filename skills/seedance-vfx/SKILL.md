---
name: seedance-vfx
description: '当用户在 Seedance 2.0 中请求 VFX、粒子、能量、破坏、变形、天气效果、魔法效果、爆炸、烟雾、火焰、水流或物理可信效果时，应使用此技能。'
user-invocable: true
---

# seedance-vfx

VFX 提示词需要包含材质行为、来源、时序和结果。将每个效果视为物理过程：它始于某处，与光线和物体交互，随时间变化，并最终呈现为可见状态。避免使用"魔法的"、"爆炸性的"或"电影感的"等泛泛词汇，除非它们能具体转化为粒子、流体、烟雾、光线、碎片、形变或能量行为的描述。

## 效果契约

需明确说明：效果来源、材质、运动路径、与光线的交互、与物体的交互、消散方式及终点状态。

| 效果类型 | 可直接用于提示词的短语                                                                           | 稳定性注意事项                     |
| -------- | ------------------------------------------------------------------------------------------------ | ---------------------------------- |
| 产品粒子 | `gold dust particles spiral from behind the logo, catch the backlight, then settle on the table` | 保持 Logo 和瓶身刚性不变。         |
| 能量效果 | `thin blue electrical arcs crawl along the cable, briefly illuminating fingerprints on the plug` | 保持电弧附着于来源物体。           |
| 烟雾效果 | `cold white vapor rolls over the rim, sinks down the glass, and thins near the tabletop`         | 描述密度与流动方向。               |
| 变形效果 | `paper edge chars inward from the corner, flakes curl and fall, final logo remains untouched`    | 保护身份锚点（核心标识）不受影响。 |
| 天气效果 | `wind pushes rain diagonally across the frame, puddles ripple outward from each step`            | 将天气效果与表面材质关联。         |

## VFX 集成规则

每个镜头仅使用一个主效果。将效果来源锚定到明确的物体或身体部位。确保效果遵循重力、风力、碰撞、反射和遮挡关系。当 VFX 靠近面部、手部、Logo 或文字时，保持核心标识稳定，将效果布置在其周围而非穿透其中。

## 时序与消散

效果必须有终点：沉降、淡出、蒸发、凝固、坍缩、辉光消退或留下残留物。若效果较复杂，请使用三阶段时序短语：`forms -> travels -> dissipates`（形成 → 移动 → 消散）。避免无结果、无消耗的永续效果，因为它们常会退化为嘈杂的叠加层。

## 输出契约

返回 VFX 契约内容、稳定性约束条件，以及一句紧凑的、可直接用于提示词的短语。
