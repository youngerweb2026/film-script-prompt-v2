# 影视脚本提示词2.0

将影视剧本、分镜、镜头想法、参考素材和返修反馈，整理为适合 Seedance 2.5 的完整中文视频提示词。

作者：[不二何](https://github.com/youngerweb2026)。Skill 标识：`film-script-prompt-v2`。基于 SD2.5 提示词助手调整，作为独立 Skill 使用，无需另行安装旧版。

## 复制这段指令给 Agent 安装

把下方整段文字粘贴给支持自定义 Skills、能够联网并操作本地文件的 Agent，让它实际完成安装。

```text
请帮我实际安装 GitHub 上的「影视脚本提示词2.0」（film-script-prompt-v2）Skill。

仓库：https://github.com/youngerweb2026/film-script-prompt-v2
Skill 目录：skills/film-script-prompt-v2
直达：https://github.com/youngerweb2026/film-script-prompt-v2/tree/main/skills/film-script-prompt-v2

请先读取仓库说明和技能内容，识别当前操作系统与本 Agent 实际支持的用户级 Skills 安装目录，优先使用原生 Skill 安装器。如果你是 Codex，使用 Skill Installer，仓库参数为 youngerweb2026/film-script-prompt-v2，路径参数为 skills/film-script-prompt-v2。如果原生安装器不可用或缺少 Python，请根据当前环境自动改用 Git、macOS/Linux 的 curl/unzip 或 Windows PowerShell 下载，不要仅因缺少 Python 就停止。

完整安装 skills/film-script-prompt-v2 目录及其全部文件，技能文件夹名保持 film-script-prompt-v2；保留 SKILL.md、agents/openai.yaml 和 references/ 下的 model-notes.md、task-patterns.md、examples.md，不要只复制 SKILL.md。

如果已有同名 Skill，先比较：内容相同则保留，内容不同则备份后更新，只改动这个 Skill，不影响其他技能。安装后核对来源、文件完整性及相对引用，并检查本 Agent 是否能识别。告诉我实际安装位置、调用方法及何时生效、是否需要重新加载；如果当前环境不支持自定义 Skills 或不能实际安装，请如实说明，不要把阅读技能当作安装完成。

只执行安装，不启动剧本创作、提示词编写、素材上传或视频生成。调用方法：使用 $film-script-prompt-v2，按四段结构整理我的影视脚本提示词。
```

## 使用示例

```text
使用 $film-script-prompt-v2，将下面的影视脚本整理为 Seedance 2.5 中文视频提示词。
沿用已经确认的人物、环境和视觉风格，合理划分单次生成段，每段给出完整四段提示词。只编写提示词，不生成视频。

（在这里粘贴剧本、分镜或镜头想法，并说明参考素材用途。）
```

## 核心规则

每个可独立提交的生成段，依次包含四部分：

1. **【素材绑定】**：明确素材锁定谁、什么环境或产品，以及外观、动作、运镜、音色等职责与作用范围。无外部素材时保留此段并说明。
2. **【视觉风格锁定】**：沿用上下文已确认的色彩、影调、光线、材质、画面质感与情绪，统一各镜头。
3. **【画面描述】**：按情境描述叙事、景别、机位、动作、运镜、持续时间及衔接，不要求每镜机械逐项填写。声音也写在此段内。
4. **【负面提示词】**：仅写本镜头或本段需要避免的内容，与正向要求一致。

用户未明确要求时，默认不添加背景音乐；可按画面需要配置环境声与动作音效，配乐留待后期剪辑统一处理。编辑原片时保留未要求改变的已有声音。

按 Seedance 2.5 单次4—30秒规划，常规优先低于25秒；确有连续动作、特殊衔接或较高连接要求时，可使用25—30秒，最长30秒。这里指**一次生成的视频总长**，一个生成段可以包含多个更短的镜头，不要求每个镜头接近20秒。实际执行时以对应平台当前支持情况为准。

## 资料与能力边界

基础资料为截至2026-10-23的 Seedance 2.5 手册整理快照，本版结构、声音默认值与时长规划来自后续用户要求。详见 [model-notes.md](skills/film-script-prompt-v2/references/model-notes.md)。仓库只发布提示词助手及必要提炼，不附原手册全文。

这是提示词工作 Skill；默认中文，不需要 API Key，不自动上传素材、创建画布或消耗视频生成额度。实际生成需要用户明确授权及相应平台工具。资料快照和写作建议不等于当前所有入口的能力保证，结构校验也不等于视频生成效果实测。

## 文件结构

```text
skills/film-script-prompt-v2/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── model-notes.md
    ├── task-patterns.md
    └── examples.md
```

入口：[SKILL.md](skills/film-script-prompt-v2/SKILL.md)。任务写法与完整示例按需读取。其他 Agent 的显式调用方式及安装生效时机，以该 Agent 的实际支持为准。
