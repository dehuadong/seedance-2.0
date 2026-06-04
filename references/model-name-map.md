# 模型名称映射

last_verified: 2026-05-30

当用户提及"Seedance Pro"、"Seedance V2"、"Seed2.0 Pro"或特定封装器的模型名称时，请使用此文件。

## 规范名称

| 名称 | 含义 | 使用指导 |
|---|---|---|
| Seedance 2.0 | 字节跳动 Seed 视频生成模型系列 | v2 视频模型系列的正确公开名称。请将其作为默认表述使用。 |
| Seedance 2.0 Fast | 官方/产品及封装器界面报告的更快版 Seedance 2.0 变体 | 当当前界面提供该变体时，用于草稿、迭代或低延迟场景的讨论。请重新核实具体的分辨率、时长和定价。 |
| Doubao Seedance 2.0 | 火山引擎/豆包风格的界面命名 | 视为产品/API 界面标签，而非不同的创作方法。 |
| `doubao-seedance-2-0-260128` | 5 月 29 日教程中观察到的火山引擎 Ark 模型 ID | 仅在重新核实当前控制台/文档后，才可用于实现示例。切勿将其视为通用的 BytePlus/全球可用性。 |
| `doubao-seedance-2-0-fast-260128` | 5 月 29 日教程中观察到的火山引擎 Ark Fast 模型 ID | 仅当当前界面提供 Fast 变体且已核实当前定价/限制时使用。 |
| `seedance2` | Runway API 模型 ID | 仅用于 Runway 的 API 界面。切勿替代火山引擎/豆包的模型 ID。 |
| Seedance V2 | 社区简写 | 除非用户明确指代特定封装器的模型，否则统一规范为 Seedance 2.0。 |
| Seedance 2.0 Pro | 含义模糊的社区简写 | 勿假设此为官方视频模型名称。请询问具体界面，或附带说明地规范为 Seedance 2.0 / Fast。 |
| Seed2.0 Pro | 在 Seedance 视频模型系列之外出现的独立 Seed/豆包命名 | 切勿与 Seedance 2.0 视频生成混淆。 |
| Seedance 1.5 Pro | 早期 Seedance 代系 | 仅适用于历史对比。切勿将其限制条件与 Seedance 2.0 混用。 |

## 回答模式

如果用户提及"Seedance 2.0 Pro"，请回答：

`除非您指的是特定封装器的 Pro 标签，否则我将此视为 Seedance 2.0。官方公开的视频模型表述为 Seedance 2.0，在某些界面上则为 Seedance 2.0 Fast。Seed2.0 Pro 属于不同的命名体系，未经来源确认，不应将其用作 Seedance 视频模型名称。`

## 封装器名称

第三方封装器可能提供诸如 `doubao-seedance-2.0`、`doubao-seedance-2.0-fast` 或带有提供商前缀的变体名称。这些名称可用于实现参考，但并非本仓库关于官方命名的权威来源。

除非相关数值已在当前官方页面或控制台中得到核实，否则切勿引用 JavaScript 渲染的定价页面中显示的当前 BytePlus Seedance 2.0 定价或模型 ID。引用火山引擎价格时，必须注明来源日期、模型、界面、币种，并附带重新核实的提醒。