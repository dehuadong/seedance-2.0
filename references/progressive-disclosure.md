# 渐进式披露计划

根技能负责路由，子技能负责决策，参考资料承载密集表格与动态更新的事实。

| 内容 | 存放位置 | 加载条件 |
|---|---|---|
| 路由规则、高层级原则 | `SKILL.md` | 始终加载 |
| 提示词构建 | `skills/seedance-prompt/SKILL.md` | 执行提示词撰写任务时 |
| 平台/API 事实信息 | `references/api-status.md` | 执行平台或 API 相关任务时 |
| 词汇列表 | 语言技能 + 参考资料 | 执行翻译/压缩任务时 |
| 安全与知识产权 | `seedance-copyright` + `platform-constraints` | 涉及受保护身份或安全敏感任务时 |
| 长示例 | `seedance-examples-zh` 或未来的 `examples/` | 用户请求示例时 |

请勿将大型数据库移回活跃的子技能主体中。