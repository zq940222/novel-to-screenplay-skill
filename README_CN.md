# 小说改编剧本 Skill

一个 [Claude Code](https://docs.anthropic.com/en/docs/claude-code) 技能插件，将小说和故事改编为专业的好莱坞标准电影剧本。

## 功能特性

- **双模式改编**
  - **自动模式** — 一键改编：提供小说文本，直接输出完整剧本
  - **引导模式** — 分步协作：故事分析 → 场景大纲 → 分幕写作 → 润色定稿
- **好莱坞标准格式** — 场景标题、动作描写、对白、转场、画外音 (V.O.)、画外音效 (O.S.)、蒙太奇、交叉剪辑
- **三幕结构** — 自动将小说情节映射为电影三幕结构（约90页 ≈ 90分钟）
- **智能改编** — 角色合并/删减、6:1 压缩比、内心独白转化为视觉动作、对白潜台词化
- **中英双语触发** — 支持中文和英文指令

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

| 指令 | 模式 |
|------|------|
| "把这个小说改编成剧本" | 自动（询问模式） |
| "直接改编" / "一键改编" | 自动模式 |
| "分步骤改编" / "一步一步来" | 引导模式 |
| "adapt this novel" / "convert to screenplay" | 自动（询问模式） |

### 自动模式示例

```
> 这是我的小说内容：[粘贴文本或提供 .txt 文件]
> 把它改编成90分钟的电影剧本。
```

Claude 会自动执行：分析 → 大纲 → 写作 → 自检 → 输出完整剧本。

### 引导模式示例

```
> 这是我的小说：[粘贴文本或提供 .txt 文件]
> 帮我分步骤改编成剧本。
```

Claude 会分 4 个阶段引导你，每个阶段都可以给出反馈：

1. **故事分析** — 角色取舍决策、三幕结构映射、改编难点分析
2. **场景大纲** — 40-55 个场景分解，包含节拍和页码估算
3. **分幕写作** — 按幕输出剧本，支持逐步审阅
4. **润色定稿** — 应用反馈意见，执行质量自检清单

## 项目结构

```
novel-to-screenplay/
├── SKILL.md                              # 主入口：工作流程 + 触发规则
├── references/
│   ├── screenplay-format.md              # 好莱坞剧本格式规范
│   └── adaptation-guide.md               # 小说→剧本改编技巧
└── assets/
    └── screenplay-template.fountain      # Fountain 格式剧本模板
```

## 输出格式

剧本以纯文本形式输出，遵循好莱坞标准格式，兼容 [Fountain](https://fountain.io/) 标记语言。可保存为 `.fountain` 或 `.txt` 文件。

## 支持的输入格式

- 纯文本（直接粘贴到对话中）
- `.txt` 文件
- 任何散文体小说内容

## 未来规划

- [ ] 电视剧剧本支持（多集连续剧弧线）
- [ ] 舞台剧格式
- [ ] 中文剧本格式
- [ ] PDF / DOCX 输入支持

## 许可证

MIT
