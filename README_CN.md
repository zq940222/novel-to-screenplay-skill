# 小说改编剧本 Skill

[English](README.md)

一个 [Claude Code](https://docs.anthropic.com/en/docs/claude-code) 技能插件，将小说改编为好莱坞标准电影剧本，并生成逐镜头 AI 视频提示词，适配即梦 AI (Seedance 2.0) 等平台。

## 功能特性

### 剧本改编
- **双模式改编**
  - **自动模式** — 一键改编：提供小说文本，直接输出完整剧本
  - **引导模式** — 分步协作：故事分析 → 场景大纲 → 分幕写作 → 润色定稿
- **好莱坞标准格式** — 场景标题、动作描写、对白、转场、画外音 (V.O.)、画外音效 (O.S.)、蒙太奇、交叉剪辑
- **三幕结构** — 自动将小说情节映射为电影三幕结构（约90页 ≈ 90分钟）
- **智能改编** — 角色合并/删减、6:1 压缩比、内心独白转化为视觉动作、对白潜台词化

### AI 视频提示词生成
- **剧本→分镜头** — 自动将场景拆分为 5-10 秒的独立视频镜头
- **角色卡片** — 固定视觉描述跨镜头复用，确保角色一致性
- **电影镜头语言** — 完整的景别、角度、运镜、转场词汇表
- **平台适配** — 针对即梦 AI (Seedance 2.0)、Kling、Runway 等平台优化
- **多种输出格式** — 结构化文本、CSV 表格（批量处理）、按场景分批输出

### 内容安全审核
- **自动安全改写** — 检测并重写可能触发平台审核的提示词
- **7大风险类别** — 暴力、武器、色情、恐怖、毒品、政治敏感、未成年人
- **5大替换原则** — 暗示>描绘、情感>动作、剪影>实拍、隐喻>直叙、音效提示
- **平台差异化** — 针对国内外不同 AI 视频平台的审核策略

## 安装方式

### 方式一：从 `.skill` 文件安装

```bash
claude install-skill /path/to/novel-to-screenplay.skill
```

### 方式二：从 GitHub 安装

```bash
claude install-skill https://github.com/zq940222/novel-to-screenplay-skill
```

### 方式三：手动安装

将 `novel-to-screenplay` 文件夹复制到 Claude Code 的 skills 目录：

```
~/.claude/skills/novel-to-screenplay/
# 或
<项目目录>/.claude/skills/novel-to-screenplay/
```

## 使用方法

安装后，输入以下指令即可自动触发：

| 指令 | 工作流 |
|------|--------|
| "把这个小说改编成剧本" | 仅剧本 |
| "生成视频提示词" / "分镜头提示词" | 仅视频提示词 |
| "从小说到视频" / "全链路" | 完整流程 |
| "直接改编" / "一键改编" | 自动模式 |
| "分步骤改编" / "一步一步来" | 引导模式 |
| "AI视频" / "screenplay to video" | 视频提示词 |

### 全链路示例

```
> 这是我的小说内容：[粘贴文本或提供 .txt 文件]
> 改编成90分钟电影，并生成即梦AI的视频提示词。
```

Claude 会自动执行：分析小说 → 写剧本 → 创建角色卡片 → 生成逐镜头视频提示词 → 安全审核所有提示词。

### 视频提示词输出示例

```
场景 3 — 镜头 2
景别: 中景 | 运镜: 固定 | 时长: 6秒
剧本参考: Sarah 走进酒吧，环顾四周
---
Prompt: "Medium shot of a 30-year-old woman with short black hair and sharp
cheekbones, wearing a worn brown leather jacket, stepping through a doorway
into a dimly lit jazz bar, neon blue light filtering through rain-streaked
windows behind her, she pauses and scans the room with focused intensity,
cinematic shallow depth of field, warm interior light on face, static camera,
film grain, 16:9 aspect ratio"
---
安全审核: 通过 — 无风险内容
```

## 项目结构

```
novel-to-screenplay/
├── SKILL.md                              # 主入口：工作流程 + 触发规则
├── references/
│   ├── screenplay-format.md              # 好莱坞剧本格式规范
│   ├── adaptation-guide.md               # 小说→剧本改编技巧
│   ├── video-prompt-guide.md             # AI视频提示词构建指南
│   └── content-safety-guide.md           # 平台审核规避策略
└── assets/
    └── screenplay-template.fountain      # Fountain 格式剧本模板
```

## 输出格式

- **剧本**: 好莱坞标准纯文本 → `.fountain` 或 `.txt`
- **视频提示词**: 结构化分镜头列表 → `.txt` 或 `.csv`

## 支持的输入格式

- 纯文本（直接粘贴到对话中）
- `.txt` 文件
- 任何散文体小说内容
- 已有剧本文本（用于生成视频提示词）

## 未来规划

- [x] AI 视频提示词生成 + 内容安全审核
- [ ] 电视剧剧本支持（多集连续剧弧线）
- [ ] 舞台剧格式
- [ ] 中文剧本格式
- [ ] PDF / DOCX 输入支持
- [ ] 角色参考图生成（提升跨镜头一致性）

## 许可证

MIT
