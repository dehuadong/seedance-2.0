# 模型名称映射表

last_verified: 2026-06-14

当用户提到“Seedance Pro”、“Seedance V2”、“Seed2.0 Pro”或特定包装器的模型名称时，请使用此文件。

## 标准名称

| 名称 | 含义 | 指导 |
|---|---|---|
| Seedance 2.0 | 字节跳动 Seed 视频生成模型系列 | v2 视频模型系列的正确公开名称。将其作为默认用语。 |
| Seedance 2.0 Fast | 官方/产品和包装器界面报告的更快 Seedance 2.0 变体 | 用于草稿、迭代或低延迟讨论（当活动界面暴露该变体时）。重新确认确切分辨率、时长和定价。 |
| Doubao Seedance 2.0 | 火山引擎/豆包风格的界面命名 | 视为产品/API 界面标签，而非不同的创作方法。 |
| `doubao-seedance-2-0-260128` | 在 5 月 29 日教程中观察到的火山引擎 Ark 模型 ID | 仅在重新检查当前控制台/文档后，用于实现示例。不要视为通用 BytePlus/全球可用性。 |
| `doubao-seedance-2-0-fast-260128` | 在 5 月 29 日教程中观察到的火山引擎 Ark Fast 模型 ID | 仅在活动界面暴露 Fast 变体且已检查当前定价/限制时使用。 |
| `doubao-seedance-2-0-pro-260215` | 火山引擎 Ark Pro 模型 ID（报告于 2026-06-14，此处未经验证控制台） | 仅在重新检查实时 Ark 控制台后使用。不要与 `doubao-seed-2-0-pro-*` LLM 混淆（见非 Seedance 部分）。 |
| `dreamina-seedance-2-0-260128` / `-fast-260128` | BytePlus ModelArk 模型 ID——火山引擎 `doubao-` ID 的国际对应版本（报告于 2026-06-14） | BytePlus 使用 `dreamina-` 前缀，而火山引擎使用 `doubao-`。同一模型系列，不同界面；引用前重新检查实时 ModelArk 文档。 |
| `seedance2` | Runway API 模型 ID | 仅用于 Runway 的 API 界面。不要替代火山引擎/豆包模型 ID。 |
| fal Seedance 2.0 端点 | fal 托管的 Seedance 2.0 界面：`text-to-video`、`image-to-video`、`reference-to-video`，各有 `/fast` 层级 | 仅对 fal 界面使用 fal 端点命名（验证于 2026-06-09）。引用前重新确认端点 ID、分辨率层级和每秒定价。不要替代火山引擎、豆包或 Runway 模型 ID。 |
| Seedance V2 | 社区简称 | 标准化为 Seedance 2.0，除非用户明确指向特定包装器模型。 |
| Seedance 2.0 Pro | 含义模糊的社区简称 | 不要假设这是官方视频模型名称。询问具体界面，或标准化为 Seedance 2.0 / Fast 并加以说明。 |
| Seed2.0 Pro | 在 Seedance 视频模型系列之外看到的独立 Seed/Doubao 命名 | 不要与 Seedance 2.0 视频生成混淆。 |
| Seedance 1.5 Pro | 较早的 Seedance 生成版本 | 仅用于历史比较。不要将其限制与 Seedance 2.0 混合。 |

## 回答模式

如果用户说“Seedance 2.0 Pro”，回答：

`我将视为 Seedance 2.0，除非您指特定包装器的 Pro 标签。官方公开视频模型用语是 Seedance 2.0，在某些界面上还有 Seedance 2.0 Fast。Seed2.0 Pro 是另一套命名体系，在没有来源确认的情况下不应作为 Seedance 视频模型名称使用。`

## 非 Seedance 模型（请勿混淆）

这些 NOT 不是 Seedance，不应触发 Seedance 特定的语法、规格或界面。版本验证于 2026-06-14；引用前重新确认。

| 名称 | 实际是什么 | 注意 |
|---|---|---|
| Seedream（如 Seedream 4.5） | 字节跳动的**图像**生成模型 | 同一供应商，名称几乎相同（Seedr**ea**m 与 Seed**a**nce）。混淆风险最高。非视频。 |
| Doubao-Seed-2.0（`doubao-seed-2-0-pro-*`） | 字节跳动在火山引擎上的 **LLM** | 共享 Ark 界面和“Seed”系列，但是语言模型，而非 Seedance 视频。 |
| Sora 2（OpenAI） | 竞品视频模型 | 注意：OpenAI 宣布 Sora 停用——应用程序约 2026 年 4 月关闭，API 约 2026 年 9 月结束。非 Seedance。 |
| Veo 3.1（Google） | 竞品视频模型（系列：3.1 / Fast / Lite） | “Veo 3”为前代。非 Seedance。 |
| Kling 3.0（快手） | 竞品视频模型（“Omni”为其多模态变体） | 非 Seedance。 |
| Runway Gen-4.5 | Runway 自有的视频模型系列 | 区别于 Runway 通过其 API *托管* Seedance 2.0。非 Seedance。 |
| Hailuo / Vidu / Luma Ray3 / Pika / Wan | 其他竞品视频模型 | 非 Seedance。 |

对于这些模型，仅提供通用电影制作技巧——绝不提供 Seedance 参考标签、镜头语法或界面特定设置。

## 包装器名称

第三方包装器可能暴露诸如 `doubao-seedance-2.0`、`doubao-seedance-2.0-fast` 或供应商前缀变体等名称。这些对实现有参考价值，但并非本仓库官方命名的依据。

除非值已在当前官方页面或控制台中验证，否则不要引用由 JavaScript 渲染的定价页面中的当前 BytePlus Seedance 2.0 定价或模型 ID。火山引擎价格仅在附有来源日期、模型、界面、货币和重新检查警告的情况下方可引用。