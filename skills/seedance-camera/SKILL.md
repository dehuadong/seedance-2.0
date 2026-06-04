---
name: seedance-camera
description: '当用户请求 Seedance 2.0 的摄像机运动、景别、镜头感、构图、一镜到底指导、推轨、摇摄、俯仰、推进、手持、航拍、微距或摄像机迁移指导时，应使用此技能。'
---

# seedance-camera

除非用户请求多镜头序列，否则每个短视频片段仅使用一个清晰的摄像机构思。最佳的摄像机指导应包含起始帧、运动方式、速度、与主体的关系及终点。避免堆叠相互冲突的运动，例如在同一五秒镜头内同时使用无人机上升、推轨、手持晃动及环绕。

加载 `references/quick-ref.md` 获取提示词组装指南，加载 `references/cinematography-shot-language.md` 获取专业镜头约定，当摄像机措辞需多语言支持时加载 `references/vocab/zh.md` 或 `references/vocab/ru.md`。

## 摄像机约定

声明：景别、角度、运动、速度、主体关系及终点。提示词就绪的摄像机短语应物理可行并与主体动作关联。

| 需求     | 强表述                                                                                                                                                | 避免                                                      |
| -------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------- |
| 情感领悟 | `slow dolly-in from medium close-up to tight close-up as Character A lowers the envelope`（角色 A 放下信封时，从中近景缓慢推进至特写）                | `dramatic cinematic zoom`（戏剧性电影感变焦）             |
| 产品展示 | `controlled slider move from silhouette to front three-quarter hero angle, ending on the label`（可控滑轨从剪影移至前四分之三主打角度，终点聚焦标签） | `dynamic product camera`（动态产品摄像机）                |
| 规模感   | `low-angle crane up from boots to skyline, ending behind the character's shoulder`（低角度摇臂从靴子升至天际线，终点停在角色肩后）                    | `epic wide moving shot`（史诗级广角运动镜头）             |
| 不稳定感 | `subtle handheld shoulder camera, small breathing sway, subject kept centered`（细微手持肩扛摄像机，轻微呼吸式晃动，主体保持居中）                    | `shaky chaotic camera everywhere`（各处晃动混乱的摄像机） |
| 精度细节 | `locked macro shot, focus stays on the watch gears while the second hand clicks once`（锁定微距镜头，焦点保持在手表齿轮上，秒针咔哒一次）             | `cool close-up details`（酷炫特写细节）                   |

## 镜头与构图锚点

仅当镜头锚点能提升指导效果时使用：`24mm wide lens for spatial energy`（24mm 广角镜头营造空间张力）、`35mm natural street perspective`（35mm 自然街头透视）、`50mm portrait compression`（50mm 人像压缩感）、`85mm shallow close-up`（85mm 浅景深特写）或 `macro lens for material detail`（微距镜头呈现材质细节）。将镜头术语与主体距离及运动配对；勿堆叠镜头数值作为装饰。

## 运动选择

**固定机位**适用于口型同步、产品识别及精细视觉特效。**推轨推进**适用于发现或领悟时刻。**跟拍**适用于旅行、追逐及产品运动。**环绕**仅当主体可从各角度清晰呈现时使用。**摇臂或无人机**适用于规模感、抵达或揭示。**手持**仅当真实感优先于精度时使用。

## 连续性规则

多角色场景中，将摄像机锚定到命名标签：`camera holds Character A in foreground while Character B crosses behind`（摄像机保持角色 A 在前景，同时角色 B 从后方穿过）。对于 I2V，除非用户明确要求重新构图，否则保留图像构图。对于参考视频，声明 `[Video1]` 是迁移摄像机运动、动作节奏还是场面调度；勿让其迁移身份（除非已获授权）。

对于复杂摄像机运动，视频参考通常优于冗长的文字堆叠。使用 `[Video1] controls camera rhythm only; do not transfer performer, room, logo, or identity`（`[Video1]` 仅控制摄像机节奏；不迁移表演者、房间、徽标或身份）。

## 冲突规则

若用户提供多个不兼容的运动，选择一个主体摄像机运动，将其余放入可选变体。若镜头需要多个节拍，建议拆分为独立片段或使用时间分段提示词。

## 输出约定

返回选定的摄像机短语、适配理由、已移除的冲突项、脆弱锚点、终点，以及一句提示词就绪的整合句式。
