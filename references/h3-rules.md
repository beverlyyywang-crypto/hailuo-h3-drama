# H3 官方格式入口：素材库不能覆盖

核验：2026-11-06。这是精简导航，提交时读取选定模式的官方指南获取全部细则和精确首行；离线无法核验精确语法时标记导演草稿。原截图经验继续保存在 [evidence.md](evidence.md)，不升级为官方规则。

## 基础模式
[Official base guide: T2VA / I2VA / FL2VA / L2VA](https://huggingface.co/MiniMaxAI/MiniMax-H3/raw/main/docs/VIDEO_PROMPT_WRITING_GUIDE_base_en.md)

Verified summary (not an API schema):

T2VA starts with integrated_multimodal_description, overall_soundscape, non_diegetic_music. Image-anchored modes require the guide's mode-specific alignment instruction first, then a blank line. I2VA anchors the opening; FL2VA connects both frames, normally in one shot unless multiple shots are requested; L2VA converges on the ending. Final-frame instructions use the actual last shot and duration with two decimals.

Establish style and composition in Shot 1 without a timestamp. Later cuts carry increasing MM:SS.mmm timestamps within the duration. Write camera actions naturally, adding meaningful amplitude and speed. Keep speaker IDs stable across shots; do not number silent characters. Preserve dialogue verbatim inside language-tagged d blocks. Voiceover uses the prescribed phrase and closed-lip instruction. Cross-cut speech uses scenetrans; terminal truncation uses cutoff. Quote visible text without translating it.

Soundscape covers ambience, physical and nonverbal sounds in 1–4 sentences; N/A means complete silence. Audience-only music uses 1–3 concrete sentences; N/A means no score. Dialogue, singing and diegetic music belong in the timeline.

## 全参考模式
[Official full-reference guide](https://huggingface.co/MiniMaxAI/MiniMax-H3/raw/main/docs/VIDEO_PROMPT_WRITING_GUIDE_ref_en.md)

Verified summary (not an API schema):

Keep six sections in order: subject_definitions, summary, retention_analysis, detailed_description, overall_soundscape, non_diegetic_music. Write English except original-language dialogue, lyrics and visible text. Define Subject, Picture, Video and Audio labels by their actual roles, retaining meanings throughout. Asset labels and vocal IDs are distinct. Bind an audio reference to the existing speaker ID rather than renumbering it.

Choose summary task types from actual relationships; use the guide's exact prefixes. Retention markers differ for visual and audio material; consult the guide rather than inventing values. Introduce style before Shot 1. Describe referenced features, composition, actions, camera and sound where they apply. Generation descriptions normally use 350–500 English words, adjusted for spoken timing; editing descriptions scale with complexity. Shared shot, dialogue and audio conventions follow the base guide. Preserve reference audio's copy/reference relationship in the appropriate audible layer.

## 本技能执行边界
- 原有三段/六段、英文正文、原语对白、人物一致性、首尾路径、声音分层、编号和时间戳规则继续生效。
- 官方首帧锚点与截图少重复首帧可以兼容：简要写清必需锚点和不变量，再把篇幅用于后续变化。
- 没有对白、没有任何人类声音、全静音分别处理，不能互相替代；具体配置见 [adaptation.md](library/adaptation.md)。
- 模式标题和内部字段不是新接口参数。模型可用模式、时长、分辨率及平台限制另行核验。
