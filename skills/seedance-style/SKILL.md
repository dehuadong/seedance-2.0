---
name: seedance-style
description: '当用户请求视觉风格、艺术指导、渲染感受、时期美学、纹理、动画风格、真实感级别，或工作室/系列参考的风格安全替代方案时，应使用此技能。'
user-invocable: true
---

# seedance-style

将风格请求转化为制作描述符。风格应描述媒介、纹理、调色板、镜头或渲染行为、时期线索及构图。当更安全的描述性风格能够保留用户意图时，请勿依赖工作室、系列、艺术家或在世创作者的名称。

## 风格安全规则

除非用户拥有明确授权的工作流程，否则请勿使用工作室、系列、艺术家或在世创作者的名称作为风格锚点。通过描述媒介、纹理、调色板、灯光、构图、时代、线条质感和运动节奏来保留预期的视觉功能。

| 用户意图         | 安全制作描述符                                                                                                                |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| 温馨手绘奇幻风格 | `hand-painted 2D animation, soft watercolor backgrounds, rounded character silhouettes, warm pastel palette, gentle parallax` |
| 犀利赛博朋克动作 | `neon noir city, wet pavement reflections, high-contrast magenta and cyan light, fast lateral tracking, angular silhouettes`  |
| 高端产品写实风格 | `clean commercial realism, controlled reflections, shallow depth of field, neutral background, polished material detail`      |
| 复古纪录片风格   | `1970s documentary texture, muted film grain, practical daylight, handheld observational framing`                             |
| 儿童动画风格     | `soft clay-like characters, simple expressive faces, bright primary palette, bouncy squash-and-stretch motion`                |

## 分层风格方法

将风格拆分为多个层次，而非使用单一宽泛标签：**媒介**（实拍、定格动画、2D、3D、微缩模型）、**表面**（纸张纹理、黏土、拉丝金属、玻璃、织物）、**调色板**（柔和粉彩、单色、钠灯橙）、**相机/渲染**（微距、浅景深、正交投影、手持拍摄）以及**运动节奏**（柔和、断奏、弹性、真实重量感）。

## 混合风格规则

若用户请求混合风格，请将每种风格分配至对应层次：`live-action product photography with illustrated UI overlays` 比混合多种命名影响更为清晰。确保角色设计、环境、灯光和视觉特效处于兼容的表现范畴内。

## 输出合约

返回一个安全的风格描述符、任何受保护名称的替代重写，以及一句整合后的提示语句。
