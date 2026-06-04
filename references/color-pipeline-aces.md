# 色彩管线与ACES注意事项

当Seedance输出需要进入专业剪辑、调色、HDR/SDR流程、代理商审核或交付工作流时，请使用此参考文档。

## 诚实边界

Seedance提示词可以描述色彩意图、布光动机、对比度、调色板、材质响应和氛围。但它们无法替代经过测量的色彩管理、校准监视、素材对位、调色、合法范围检查或交付转换。请保持提示词语言的创意性；将管线相关语言作为后期元数据保留。

## 提示词层级的色彩意图

使用：

- source light：钨丝灯实景光源、阴天自然光、钠灯街灯、霓虹招牌、冷调月光轮廓光；
- contrast：柔和低对比、硬朗黑色电影对比、干净产品对比、高调美颜；
- palette：克制冷暖分割、柔和冬季调色、高饱和音乐视频调色；
- material response：拉丝金属高光、皮肤过渡、光泽亚克力反射、湿润沥青镜面反射；
- transition：实景灯具为面部增添暖调、闪电瞬间强化剪影轮廓。

避免：

- 无法验证的声明，例如仅凭提示词声称完全符合ACES标准；
- 不可能的组合，例如在单一短镜头中同时要求HDR Dolby Vision、16mm胶片、霓虹、漂白跳过工艺和柔和商业风格；
- 将LUT名称当作魔法风格词使用，却不描述可见的视觉效果。

## 后期需跟踪的元数据

专业交接时，请记录：

| Field | Meaning |
|---|---|
| capture/source | 生成源、参考片段、静帧、源帧 |
| working color space | 项目工作色彩空间假设，通常为ACEScct/ACEScg或剪辑师管理的替代方案 |
| IDT/source transform | 源素材的解读方式（如适用） |
| show look | 创意外观描述，LUT/CDL/LMT备注 |
| output transform | SDR Rec.709、HDR PQ、影院/DCP、社交媒体平台转换 |
| trim pass | 独立的SDR/HDR/社交媒体审核备注 |
| QC notes | 裁切、非法电平、色带、肤色、产品颜色、标识颜色 |

## ACES友好型交接

当用户请求ACES时，请提供双层回答：

1. Prompt：Seedance可理解的可见色彩与布光指令。
2. Handoff：供剪辑师或调色师在Seedance之外验证的ACES/AMF/色彩备注。

示例：

`Prompt look: cool overcast daylight with a warm practical lamp reflected in the bottle, soft contrast, clean highlight rolloff, no crushed blacks. Post note: conform generated clip into the project color pipeline, verify source interpretation, preserve product color, create SDR Rec.709 and HDR trim review if required.`

`提示词外观：冷调阴天自然光，瓶身反射暖调实景灯具，柔和对比度，干净高光过渡，无死黑。后期备注：将生成片段对位至项目色彩管线，验证源素材解读，保留产品颜色，如需则创建SDR Rec.709和HDR修剪审核版本。`

## 色彩问题修复

| Symptom | Repair |
|---|---|
| Flat image | 添加有动机的主光源、轮廓光/分离光，以及一处材质高光 |
| Overprocessed color | 减少风格名称使用；指定自然对比度和中性肤色/产品颜色 |
| Inconsistent color across shots | 在每个镜头中重复光位方向、时间段、调色板和项目外观备注 |
| Product color wrong | 使用I2V产品参考、锁定机位，以及产品颜色保留约束 |
| HDR/social mismatch | 保持提示词中性；在后期规划独立的调色/导出版本 |