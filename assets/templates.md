# 可复用模板

花括号是编写占位符，交付复制区前全部替换。导演说明中文；最终正文英文，台词保留原语言。

## 用户输入卡
剧情：{事件与情绪转折}
模式/平台：{已知内容}
素材：{角色图、场景图、首帧、尾帧及各自用途}
上一镜末态：{位置、左右手、朝向、道具、情绪}
目标片长/画幅：{期望值，等待平台核验}
对白：{角色：逐字原文；语言}
声音：{对白/背景人声/非语言声音/环境声/画外音乐，分别确定}
质感：{电影写实/自然手机/轻美颜/低照度/其他；不继承素材默认}
设备：{可选相机与镜头型号，仅在用户指定或有依据时填写}
光线：{相对方向、软硬、冷暖、主辅关系、背景亮度；只改照明时列出其他不变量}
构图：{主体数量、主次、前中后景、视线和遮挡、关键焦点、可用画幅}
成像目标：{具体的颗粒/高光/散景/眩光；设备名与效果说明分开}
运镜：{机位、主体运动、相机路径、起止构图、切镜或连续阶段}
素材参考：{匹配条目 ID、采用部分和必要改写}
必须保留/允许变化：{分别列明}

## 三段式导演草稿

先读取 references/h3-rules.md 所链官方基础指南。T2VA 直接从三段开始；首帧、首尾帧、尾帧模式必须先填入该模式官方图像对齐首行，空一行后再接下面正文。对齐首行中的图片顺序、实际尾镜编号和有效时长须一致。下文是正文模板，不是已填好的完整图生模式提示词。

integrated_multimodal_description:
[Shot 1] {Live-action style when needed. Starting state only as needed for the selected input mode.} {Character initiates action, follows a physical path, contacts the object, then settles.} {Camera type, amplitude and speed; framing outcome.} {Speaker} (S1) {delivery}, <d>[{Language}] {exact dialogue}</d>. {Reaction and mouth closure.}
[Shot 2] At {MM:SS.mmm}, {cut motivation, inherited state, next action, camera and final hold}.
overall_soundscape:
{Continuous ambience and physical sound texture; specific synchronized events also appear in the shot.}
non_diegetic_music:
{Instrumentation, tempo, dynamics, entry/exit; or N/A.}

只有一个镜头就删除 Shot 2，不能为了模板增加切镜。没有对白就删除说话人和对白标签。无输入首帧时补足场景与人物信息；有首帧时减少冗余静态复述。

## 全参考模式路由
读取 references/h3-rules.md 所链官方全参考指南，逐项生成六段，素材标签以实际输入为准。不要用本模板的三段式冒充全参考格式。主体、图片、视频、音频引用分别编号；明确每项素材用于身份、构图、动作、首尾帧、原片编辑或声音，未上传素材不得虚构标签。按官方指南检查保留关系与任务类型。

## 首尾帧路径句型
From the supplied first-frame pose, {subject} shifts weight onto {support}, moves {limb/object} along {path relative to fixed scenery}, makes contact with {target}, and finishes in {last-frame pose}. {Identity, costume and prop invariants}. The camera {movement}, settling into {ending composition}.

## 下一镜交接卡
角色 ID：
位置/朝向/视线：
左手/右手/道具状态：
服装/头发/光源：
情绪已完成的变化：
环境声延续：
计划末态：
检查过的实际末态：
下一镜需纠正的偏差：

## 素材模块组装
从 references/library-index.md 召回并筛选少量适用项。先写动作与摄影，再添加与景别适配的质感和声音，不把条目说明、来源标签或禁止清单整体粘进正文。

内部构图记录：{机位/视角} + {景别/焦点目标} + {主运镜} + {幅度和速度（有意义时）} + {人物动作路径} + {微动作（可选）} + {质感档位} + {声景范围} + {稳定末态}。这不是新增 H3 字段。

无对白时删掉 Speaker 设定、S 编号与 d 标签；明确保留的呼吸和环境音写入声音描述。无字幕、无 UI 或无标识仅在当前任务要求时应用。

## 灯光与设备的组装句型
照明：{main source position, softness and warmth}, with {fill and background relationship}, preserving {required facial and material detail}.
设备参考：Use {optional camera and lens reference} as an image-making reference, emphasizing {specific visible effects that fit the scene}.
群像：Place {primary subject} at {position and depth}, with {secondary subjects} at {distinct positions}, keeping {key face/action} readable through {foreground framing}.
这些句型写入所选模式的正文相应位置，不另创 lighting、camera_model、emotion 等 H3 API 字段。静帧案例转视频后必须补足动作、时间、声音和末态。
