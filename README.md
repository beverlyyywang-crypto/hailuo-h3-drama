# Hailuo H3 通用视频提示词导演

A reusable, instruction-only skill for MiniMax Hailuo H3 video prompt writing.

输入想拍的场景，技能先查看参考资料、补问关键缺项，再结合素材库设计动作、运镜、声音与连续性，输出对应 H3 模式的提示词。

这是独立创作的自定义技能，与 MiniMax 官方无隶属关系。

## 能做什么
- 通用场景创作：校园、街头、室内、人物互动等，示例不会限制题材。
- 按需补问：人物、情绪、动作、镜头、时长、声音等，只问影响结果的缺项。
- 48 项摄影方法：推拉、摇镜、跟拍、升降、环绕、POV、焦点转移及风格化效果。
- 自然人物细节：按景别选择皮肤肌理、微动作、重心、材质和光线关系。
- 连续剧情：记录角色、道具握持、视线、站位及片段末态。
- 可扩充素材库：关键词检索、适用条件、来源和证据等级。
- H3 格式路由：保留官方基础/全参考模式的区别，不将内部记录当作 API 字段。

## 快速开始
参见 [安装说明](INSTALL.md)，将完整文件夹放到 Codex 的技能目录。

调用示例：

> 使用 $hailuo-h3-drama。我想拍一个人在校园林荫大道边喝奶茶边看手机。请先问我需要补齐的要素，再输出提示词。

素材扩充示例：

> 使用 $hailuo-h3-drama。把下面的运镜素材整理进素材库，只保留通用摄影方法，人物妆容和服饰由每次任务自定义。

每次使用以当前用户的剧情、参考图和明确要求为准；不会默认继承任何示例造型、地点或配乐设置。

## 文件导航
| 文件/目录 | 用途 |
|---|---|
| [SKILL.md](SKILL.md) | 技能入口与工作路由 |
| [INSTALL.md](INSTALL.md) | 下载后的安装、调用与更新 |
| [references/intake.md](references/intake.md) | 需求补齐流程 |
| [references/h3-rules.md](references/h3-rules.md) | 官方模式规则入口 |
| [references/evidence.md](references/evidence.md) | 官方来源、经验与边界 |
| [references/workflow.md](references/workflow.md) | 内部结构与验证清单 |
| [references/library-index.md](references/library-index.md) | 素材关键词索引 |
| references/library/ | 运镜、真人质感、自拍和微动作素材 |
| [assets/templates.md](assets/templates.md) | 可编辑提示词模板 |
| [PUBLISH.md](PUBLISH.md) | 仓库发布与许可证选择说明 |

## 格式与来源
H3 对应模式的格式要求与用户经验分别记录，新增素材不能覆盖官方格式。本包链接官方指南，不附模型权重、LoRA 或完整官方手册。生成效果仍需结合所用模型、平台和实际视频检查，未提供身份、嘴型或尾帧必达保证。

## 下载与更新
仓库地址：https://github.com/beverlyyywang-crypto/hailuo-h3-drama。可通过仓库 Code 菜单的 Download ZIP 下载，也可使用仓库克隆方式更新。具体操作见 [GitHub 下载说明](https://docs.github.com/en/repositories/working-with-files/using-files/downloading-source-code-archives)。

## 许可与第三方来源
本仓库尚未指定开源许可证。维护者可选择许可范围并添加 LICENSE 文件；第三方资料、原始案例和链接仍按各自条款处理。官方文档与经验素材的归属见 references/evidence.md。参见 [GitHub 许可证说明](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository)。
