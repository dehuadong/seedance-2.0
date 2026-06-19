# 多镜头语法——一次生成中的真实剪辑

*Seedance 2.0 相较于 1.x 的决定性能力：一次 10–15 秒的调用可包含 2–3 个带有真正剪辑切点的镜头。标签：[official] = ByteDance/fal 文档 · [field] = 从业者报告。最后验证于 2026-06-09。*

## 语法 [official]
明确标注每个切点——使用 `Shot 1:` / `Shot 2:` / `Shot 3:` ——以纯文本形式呈现。这些标签为模型提供了切点依据；未标注的长提示倾向于渲染为单个连续镜头。每个镜头：**一个主要动作 + 一个摄像机运动**，以及对应的声音。每个镜头内部顺序：主体 + 动作 → 摄像机 → 声音。

## 预算 [official]
镜头以秒计。规划每个镜头约 4–6 秒：两个镜头需要约 10 秒，三个镜头需要 12–15 秒。要求在 5 秒内完成四个镜头，模型会压缩或跳过节拍。`duration: auto` 让模型根据提示复杂度决定片段时长——是多镜头的强大默认选项；仅在剪辑确实需要时才设置明确的时长。

## 要求 [official + field]
- **标准层级 [field]。** 官方 fal 文档显示快速端点具有相同的架构和多镜头支持，但现场报告称快速层级在首次尝试时不能可靠地支持多镜头（或慢动作、推轨运动）。
- **10–15 秒或 `auto` [official]。** 低于约 10 秒的多镜头会压缩节拍。

## 时间戳：西方界面为次要，中国界面为主要 [official + field]
优先使用 `Shot N:` 标签作为结构——清晰且可跨界面移植。fal 的参考转视频文档额外接受时间戳节奏短语（“At 5 seconds…”，“Cut scene to…”）；请谨慎使用它们作为*已标注镜头内的提示*，切勿使用 `[0-6s]` 这样的括号时间块来替代标签。

界面例外 [field]：在 Dreamina/即梦上，中文社区实践将较长的提示（约 8 秒以上）组织为以括号时间轴为主要骨架——`【时间轴】0-3s: … / 3-6s: … / 6-10s: …`——每个片段携带各自的 画面/镜头/音效。匹配当前界面的惯例；不要在单个提示中混合使用两种骨架。

## 对话与音频放置 [official + field]
对话行放在说话者出现在画面中的镜头内，以自然语言用引号书写；保持句子简短。为每个镜头命名具体声音——它们锚定音频通道。音频是按次调用生成的，而非跨调用生成：多段素材的统一配乐在后期添加。

## 单镜头替代方案 [official]
如需不间断的长镜头，请明确说明：“single continuous take, no cuts”——否则长动作描述可能会被切分。

## 示例结构
*三镜头商业广告（约 15 秒）：* Shot 1: extreme close-up of condensation sliding down a glass bottle, ice clinking. Shot 2: the bottle rises from crushed ice, camera tilting up into a backlit halo. Shot 3: a hand grabs it against a sunset rooftop, the city humming below. *（改述自官方示例结构。）*

*两镜头对话节拍（约 10 秒）：* Shot 1: close on the detective under a flickering platform light, rain on his shoulders — he says quietly, "You were never on that train." Shot 2: cut to the woman's face as the train doors close behind her, a half-smile; the departure chime swallows the silence.

## 失败修复 [field]
| 症状 | 修复 |
|---|---|
| 渲染为单个连续镜头 | 更清晰的 `Shot N:` 标签 · 减少为两个镜头 · 使用标准层级 |
| 某镜头的动作被跳过或压缩 | 减少镜头数 · 提高时长 / 使用 `auto` · 每个镜头一个动作 |
| 切点落在动作中途 | 在每个镜头句子的结尾处完成节拍；让下一个镜头开启新节拍 |
| 镜头间氛围断裂 | 为整个片段声明一次持续效果：“薄雾贯穿始终，每个镜头皆有”（全程薄雾） |