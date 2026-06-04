# 音频后期与交付

当 Seedance 工作涉及对白、声音设计、音乐、分轨、M&E（音乐与效果轨）、配音、同步或最终交付检查时，请使用此参考文档。

## 提示词层级音频

使用提示词音频来指导故事节奏和情绪：

- dialogue（对白）：简短、带引号、指定给单一说话人；
- ambience（环境音）：房间底噪、交通声、雨声、人群背景音、机器嗡鸣；
- SFX（音效）：一到两个与故事相关、并与可见动作绑定的声音；
- music（音乐）：大致速度、能量感、乐器配置，或静音；
- sync cue（同步提示）：终点处的关门声、最终帧的产品点击声、强拍上的灯光脉冲。

除非版权和平台支持明确，否则避免声称精确还原受保护歌曲、真实人声或授权表演。

## 后期层级音频交付物

| 交付物 | 用途 |
|---|---|
| Full mix | 最终立体声/5.1/Atmos 或平台要求的混音格式 |
| Dialogue stem | 用于剪辑、配音和清理的语音对白 |
| Music stem | 仅含音乐的音轨层 |
| Effects stem | 音效与设计声音 |
| M&E | 不含原始对白、用于本地化的音乐与效果轨 |
| Printmaster | 经批准的最终母版混音 |
| Dubbing guide | 说话人时序、语气、发音、停顿参考 |
| Loudness report | 交付目标合规性证明 |

## 音频规划模板

`Dialogue: [说话人/台词/语言]. Ambience: [背景音床]. SFX: [可见同步提示]. Music: [速度/情绪或无]. Reference: [Audio1 角色]. Post: [分轨/M&E/响度/同步备注].`

## 同步与响度检查

专业交付时，请检查：

- 口型与最终画面同步；
- 帧率转换后音乐/音效的同步；
- 对白未被音乐或效果音掩盖；
- R2V（视频重制）工作流中无意外残留的源视频音频；
- 响度目标与真峰值符合买方/平台规格；
- 如需本地化，确保存在 M&E 轨或分轨。

## 常见问题修复

| 问题 | 修复方案 |
|---|---|
| dialogue desync（对白不同步） | shorter line（缩短台词）, locked framing（锁定构图）, less head motion（减少头部运动）, one speaker（单一说话人） |
| wrong speaker（说话人错误） | tag the speaker and split turns（标注说话人并拆分轮次） |
| music overwhelms line（音乐盖过台词） | remove music during dialogue, keep room tone（对白期间移除音乐，保留房间底噪） |
| audio reference ignored（音频参考被忽略） | map `[Audio1]` to tempo or mood and bind a visible event to it（将 `[Audio1]` 映射到速度或情绪，并将可见事件与其绑定） |
| video and audio refs conflict（视频与音频参考冲突） | mute video reference or assign video to camera only（静音视频参考或将视频仅分配给摄像机） |
| localization impossible（无法本地化） | plan M&E/stems and textless picture before final edit（在最终剪辑前规划 M&E/分轨及无文字画面） |