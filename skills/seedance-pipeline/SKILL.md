---
name: seedance-pipeline
description: '当用户询问 Seedance 2.0 工作流操作、API 规划、BytePlus ModelArk、Dreamina/Jimeng 界面、ComfyUI、后期制作、拼接、批量工作流或集成规划时，应使用此技能。'
---

# seedance-pipeline

本技能用于操作工作流、API、网页界面、后期制作及集成规划。

## 状态规则

始终加载 `references/api-status.md` 获取当前 API 与平台声明。当用户提及 Pro、Fast、V2 或封装模型 ID 时，加载 `references/model-name-map.md`。勿依赖过时的发布状态记忆。
加载 `references/api-workflow.md` 获取实施规划、任务生命周期、Runway/Volcengine 字段差异、定价注意事项、上传处理及生产就绪性信息。
加载 `references/pro-filmmaking-standards.md` 获取专业影视、商业广告、代理机构、本地化、后期及交付工作流标准。在声明素材可交付前，加载 `references/delivery-qc.md`。

## 工作流拆分

1. 网页工作流：Dreamina/Jimeng 界面、参考素材、提示词、输出审核。
2. API 工作流：Volcengine、BytePlus 或 Runway 文档、模型 ID、认证、文件处理、任务创建、轮询/查询、取消/删除、任务台账及检索。
3. 专业制作工作流：方案、镜头列表、连续性台账、参考素材权限映射、审核循环、后期交接及交付/QC。
4. 后期工作流：剪辑、套底、拼接、稳定、音频清理、字幕/多语言字幕、调色、本地化、版本管理、无文字版及交付。
5. 首/尾帧工作流：映射起始帧、结束帧、过渡动作、身份锁定及终点目标。
6. Runway 工作流：模型 `seedance2`、`runway://` 上传、音频参考组合规则、区域/计划注意事项及 SDK 类型延迟为 Runway 特有内容。
7. 社区工作流：ComfyUI 或非官方节点除非有明确来源，否则必须标注为社区/未验证。
8. 语料挖掘工作流：复用前先分类来源；提取结构与词汇，而非不安全的原始提示词。

## 输出约定

返回工作流路径、来源状态、所需输入、制作阶段、验证步骤、交付假设及风险。对于专业项目，需包含下一步需创建的产物：简报、镜头列表、连续性台账、提示词批次、审核包、本地化矩阵或 QC 预检清单。
