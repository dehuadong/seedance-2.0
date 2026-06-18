# 中文词汇表

将此参考用于中文Seedance提示词措辞、角色绑定和紧凑提示词压缩。保持参考标签不变：`[Image1]`、`[Video1]`和`[Audio1]`保留原样。

| 功能 | 中文 | English meaning |
|---|---|---|
| 角色 | `@图1 为首帧` | Image 1 is the first frame |
| 角色 | `@图2 为尾帧` | Image 2 is the last frame |
| 角色 | `@图1 锁定主体身份` | Image 1 locks subject identity |
| 角色 | `@图2 参考场景氛围` | Image 2 provides scene mood only |
| 角色 | `@视频1 仅参考运镜` | Video 1 provides camera movement only |
| 角色 | `@视频1 参考动作节奏` | Video 1 provides action rhythm |
| 角色 | `@音频1 参考节奏和氛围` | Audio 1 provides tempo and mood |
| 首帧/末帧 | `首帧保持不变` | keep first frame unchanged |
| 首帧/末帧 | `自然过渡到尾帧` | transition naturally to final frame |
| 首帧/末帧 | `中间动作连续，不跳切` | continuous in-between motion, no jump cut |
| 首帧/末帧 | `以尾帧为最终画面目标` | use final frame as the target image |
| 摄影 | `缓慢推镜` | slow push-in |
| 摄影 | `后退揭示镜头` | pull back to reveal the space |
| 摄影 | `横向稳定跟拍` | stable lateral tracking |
| 摄影 | `轨道平移` | slider / dolly lateral move |
| 摄影 | `固定中景` | locked medium shot |
| 摄影 | `微距特写` | macro close-up |
| 摄影 | `低角度仰拍` | low-angle shot |
| 摄影 | `高角度俯拍` | high-angle shot |
| 摄影 | `过肩镜头` | over-the-shoulder shot |
| 摄影 | `弧形绕摄` | arc orbit shot |
| 摄影 | `手持镜头，轻微呼吸晃动` | handheld shot with slight breathing sway |
| 景别 | `中近景` | medium close-up |
| 景别 | `宽幅远景` | wide establishing shot |
| 景别 | `三分之二侧脸` | three-quarter profile |
| 镜头 | `长焦压缩空间` | telephoto compression |
| 镜头 | `广角空间感` | wide-angle spatial feel |
| 镜头 | `焦点从模糊过渡到清晰` | focus resolves from blur to sharpness |
| 灯光 | `柔和侧逆光` | soft side backlight |
| 灯光 | `暖色实用灯` | warm practical light |
| 灯光 | `左侧暖色实用灯` | warm practical light from left |
| 灯光 | `冷色月光轮廓光` | cool moon rim light |
| 灯光 | `体积光穿过薄雾` | volumetric light through mist |
| 灯光 | `湿地反射霓虹` | wet ground reflects neon |
| 动作 | `脚步带动薄雾扩散` | footsteps disturb fog |
| 动作 | `水珠聚合后沿表面下滑` | droplets merge and slide down |
| 动作 | `缓慢转头并停住` | slow head turn and stop |
| 动作 | `衣料随动作自然摆动` | fabric moves naturally with action |
| 视觉特效 | `金色粒子升起后消散` | gold particles rise and dissipate |
| 视觉特效 | `蓝色电弧沿边缘游走` | blue arcs crawl along the edge |
| 视觉特效 | `光线扫过材质表面` | light sweep travels across material |
| 音频 | `一句短而清晰的对白` | one short clear spoken line |
| 音频 | `无配乐，仅低环境声` | no music, low ambience only |
| 音频 | `对白期间镜头固定` | locked camera during dialogue |
| 音频 | `脚步声卡点` | footsteps hit the beat |
| 文字 | `不要新增字幕、水印或无关文字` | no new subtitles, watermark, or unrelated text |
| 剪辑 | `接着拍` | continue the shot |
| 剪辑 | `延长 5 秒` | extend by five seconds |
| 剪辑 | `只替换失败片段` | replace only the failed segment |
| 约束 | `严格保持logo、标签、形状和颜色不变` | preserve logo, label, shape, and color |
| 约束 | `仅改变动作、光线和镜头` | change only action, light, and camera |
| 约束 | `不复制人物、场景或品牌` | do not copy person, scene, or brand |
| 安全 | `改为原创角色` | change to an original character |
| 安全 | `仅使用已授权参考` | use only authorized references |
| 安全 | `保留创意功能，不保留受保护身份` | preserve creative function, not protected identity |

## 紧凑模板

`[Image1]为参考，严格保持[主体/产品/脸部/标志]不变；仅加入[动作/光线/镜头变化]。镜头：[一个动作]。声音：[音效或环境声]。`

## 时间轴模板

社区常用的长提示词骨架（即梦/Dreamina 表面，约 8 秒以上时使用；field-observed）。保持 `[Image1]` 等引用标签不变：

```
【风格】[媒介、质感、色调，一句话]
【时间轴】0-3s：[画面+镜头+音效]；3-6s：[画面+镜头+音效]；6-10s：[画面+镜头+音效]
【声音】[对白/环境声/音效/无配乐]
【参考】[Image1] 锁定主体身份；[Video1] 仅参考运镜；[Audio1] 仅参考节奏
```

## 废话陷阱

社区共识：抽象的"感觉词"会让模型无法判断该强调哪个元素。把感觉词拆解成制造这种感觉的物理元素——材质、光线、色彩、空气——画面立即变稳。

| 套话 | 改写为 |
|---|---|
| `电影感` | 写出景别、运镜、光源和调色：`宽幅远景，缓慢推镜，低角度暖阳，低饱和青橙调` |
| `氛围感` | 写出制造氛围的物理元素：`薄雾、逆光轮廓、湿地反光、低环境声` |
| `高级感` | 写出光线与材质行为：`柔和侧光、受控反光、干净背景、金属拉丝纹理` |
| `大片感` | 写出物理规模：人群数量、镜头距离、建筑高度 |
| `质感`（单独使用） | 指明哪种质感：`磨砂玻璃、丝绒吸光、纸张纤维` |
| `震撼` | 写出造成震撼的那一个画面对比或揭示 |
| `唯美` | 写出色彩、构图与光的具体行为 |
| `史诗级` | 删除，或换成具体的空间尺度与人数 |
| `超高清 / 8K / 4K` | 删除；分辨率是参数，不是描述 |
| `杰作 / 顶级品质` | 删除；质量不是请求出来的 |
| `绝美` | 写出最重要的那一个视觉细节 |
| `酷炫转场` | 写出转场名称：`匹配剪辑、硬切、甩镜` |