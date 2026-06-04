---
name: seedance-lighting
description: '当用户请求 Seedance 2.0 中的灯光设计、氛围、时段、色温、阴影、反射、天气光效、实景光源或情绪过渡时，应使用此技能。'
---

# seedance-lighting

灯光描述应聚焦物理光源与过渡变化，而非抽象美感。有效的灯光提示词需告知模型：光源位置、色温、阴影行为、光线与氛围的交互方式，以及光线在片段中是否发生变化。

当用户提及 ACES、HDR/SDR、项目外观、调色、LUT、CDL、产品色彩或专业色彩交接时，加载 `references/color-pipeline-aces.md`。

## 灯光约定

声明：主光源、方向、色温、氛围、阴影行为、反射行为及任何过渡变化。

| 情绪或任务 | 提示词就绪灯光描述                                                                            | 有效原因           |
| ---------- | --------------------------------------------------------------------------------------------- | ------------------ |
| 产品奢华感 | `narrow warm strip light sweeps across brushed metal, black acrylic reflection remains clean` | 材质与反射受控。   |
| 夜间戏剧感 | `warm practical lamp from frame left, blue moonlight rim on shoulders, soft hallway shadows`  | 使用有动机的光源。 |
| 发现时刻   | `door crack opens and a thin white beam widens across dust in the air`                        | 光线随动作变化。   |
| 美食真实感 | `large soft window light from the right, gentle bounce on the plate, no harsh specular glare` | 保持纹理可读性。   |
| 风暴氛围   | `cool overcast daylight, intermittent lightning flashes briefly sharpen the silhouette`       | 天气影响对比度。   |

## 光源选择

**实景灯具**适用于室内、亲密场景及可见动机光源。**窗户光**适用于自然主义、美食或生活场景。**轮廓光**用于主体分离需求。**硬光**适用于黑色电影、强烈日光或图形化阴影。**柔光**适用于美妆、肤色、产品润饰及儿童/家庭场景。**动态光源**用于需要可见变化的场景。

## 色彩与氛围

仅当必要时标注色温：暖色钨丝灯、冷色月光、绿色荧光灯、钠蒸汽街灯、中性阴天日光。谨慎添加氛围元素：雾气、尘埃、雨丝、烟雾或冷凝水应与光线及主体产生交互，而非仅装饰画面。

## 故障修复

若输出画面平淡，添加有动机的主光源、轮廓分离及一项材质特异性高光。若画面过度处理，移除宽泛风格声明并指定更柔和的对比度。若出现闪烁或灯光跳跃，使光源稳定并移除竞争性过渡。

## 输出约定

返回精简灯光模块、必要时附过渡说明，以及一句提示词就绪的整合句式。
