---
name: seedance-audio
description: '当用户请求 Seedance 2.0 音频、对话、口型同步、音乐、音效、环境音、节拍同步、音频参考映射、不同步故障排查或声音驱动视觉时机时，应使用此技能。'
---

# seedance-audio

本技能用于对话、口型同步、声音层次、音乐、环境音、节拍同步、音频参考映射、不同步故障排查或声音驱动视觉时机。音频应支持可见节拍，而非成为第二个相互竞争的提示词。

加载 `references/audio-guide.md` 获取详细约束、节拍同步、不同步修复、音频参考冲突及多角色变通方案。当用户需要分轨、M&E、配音、响度、同步、混音或交付指导时，加载 `references/audio-post-delivery.md`。

## 核心规则

保持对话简短，引用具体台词，并将每句台词分配给命名说话人。口型同步时优先使用锁定或稳定构图。当口型精度关键时，移除转头、大幅面部运动、极端摄像机运动或复杂手部手势。除非当前平台文档明确说明精确播放行为，否则将 `[Audio1]` 视为节奏、节拍、情绪、音色或环境音参考。

## 声音层次模式

使用紧凑层次：`Dialogue: ... Sound: ... SFX: ... Music: ... Silence: ...`。仅包含必要的层次。当静默能强化戏剧性或避免口型同步混淆时，静默是有效选项。

| 需求     | 稳定音频指导                                                                                                                                              |
| -------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 口型同步 | `Character A, locked medium close-up, says "I found it." Clear dry dialogue, no head turn.`（角色 A，锁定中近景，说"我找到了。"清晰干声对话，无转头。）   |
| 产品广告 | `Sound: low room tone. SFX: magnetic click on lid open, soft glass chime at final frame.`（音效：低环境底噪。音效：开盖时磁性咔哒声，终帧时柔和玻璃音。） |
| 节拍同步 | `[Audio1] provides tempo only; light pulses and foot taps match the downbeat.`（`[Audio1]` 仅提供节奏；灯光脉冲与脚步轻踏匹配强拍。）                     |
| 戏剧感   | `Distant rain and refrigerator hum; no music during the line.`（远处雨声与冰箱嗡鸣；台词期间无配乐。）                                                    |
| 动作     | `Breathing grows louder, shoe squeak at landing, metal door buzzer at endpoint.`（呼吸声渐强，落地时鞋面摩擦声，终点时金属门蜂鸣音。）                    |

## 多角色对话

当可靠性关键时，每个短视频片段仅使用一位说话人。若必须有两位角色对话，分开轮次并保持摄像机稳定：`Character A says... pause. Character B answers...`（角色 A 说...停顿。角色 B 回答...）。对于复杂对话交换，建议生成受控的单说话人片段并在后期合成。

## 故障修复

若对话不同步，缩短台词、锁定摄像机、移除转头动作、清理音频角色并减少竞争性音效。若错误说话人发声，分配标签并按说话人拆分台词。若音频被忽略，移除额外音乐/音效指令并明确参考角色。

若音频与视频参考相互冲突，上传前尽可能静音参考视频，或明确优先级：`[Video1] controls camera only; [Audio1] controls tempo and energy`（`[Video1]` 仅控制摄像机；`[Audio1]` 控制节奏与能量）。

## 输出约定

返回说话人映射、引用台词、声音层次、音频参考角色、口型同步约束、必要时附后期/交付说明，以及一句紧凑的提示词就绪音频模块。
