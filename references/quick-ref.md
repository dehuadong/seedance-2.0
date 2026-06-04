# 快速参考

## 默认路由

- 模糊想法：`seedance-interview`。
- 清晰想法：`seedance-prompt`。
- 简短提示：`seedance-prompt-short`。
- 效果不佳：`seedance-troubleshoot`。
- IP 或真人风险：`seedance-copyright`。
- 被拦截的提示：`seedance-filter`。
- 摄像机、灯光、运动、风格、视觉特效、音频或角色专项工作：加载匹配的专业子技能。

## 提示词检查清单

| 检查项 | 通过条件 |
|---|---|
| 模式 | T2V、I2V、V2V 或 R2V 明确指定。 |
| 参考素材 | 除非刻意分层，否则每个素材仅有一个主要作用。 |
| 主体 | 主体出现在首句，必要时附带稳定标签。 |
| 动作 | 一个可见节拍具有可观察的终点。 |
| 摄像机 | 一个主要运镜包含起点、速度、与主体关系及终点。 |
| 灯光 | 光源、方向、色彩、氛围或过渡符合物理规律。 |
| 音频 | 对话、环境音、音效、音乐或静音均为有意设计。 |
| 安全 | 受保护身份、IP 及不安全措辞需重写或经授权审核。 |
| 反空洞 | 空洞的强化词替换为可观察的制作术语。 |
| 预算 | 最终提示词控制在 2000 字符以内。 |

## 快速修复短语

| 问题 | 添加或替换为 |
|---|---|
| I2V 漂移 | `preserve [Image1] subject/product exactly; only motion, light, and camera change` |
| 效果泛化 | `physical light source + material behavior + specific camera endpoint` |
| 运镜混乱 | `one controlled [move] from [start frame] to [end frame]` |
| 动作乏力 | `actor + verb + timing + consequence + final state` |
| 口型不同步 | `locked medium close-up, short quoted line, no head turn during dialogue` |
| 特效杂乱 | `source + material + path + interaction + dissipation endpoint` |
| 风格/IP 风险 | `medium + texture + palette + composition + motion rhythm` |