# Novel to Screenplay Skill

[中文文档](README_CN.md)

A [Claude Code](https://docs.anthropic.com/en/docs/claude-code) skill that adapts novels and stories into professional Hollywood-standard movie screenplays.

## Features

- **Two Adaptation Modes**
  - **Auto Mode** — One-step: provide novel text, receive a complete screenplay
  - **Guided Mode** — Step-by-step collaboration: story analysis → scene outline → draft → polish
- **Hollywood Standard Format** — Scene headings, action lines, dialogue, transitions, V.O., O.S., MONTAGE, INTERCUT
- **Three-Act Structure** — Automatic mapping of novel plot to cinematic three-act structure (~90 pages ≈ 90 minutes)
- **Smart Adaptation** — Character merging/cutting, 6:1 compression, internal monologue → visual action conversion
- **Bilingual Triggers** — Supports both English and Chinese commands

## Installation

### Option 1: Install from `.skill` file

```bash
claude install-skill /path/to/novel-to-screenplay.skill
```

### Option 2: Install from GitHub

```bash
claude install-skill https://github.com/zq940222/novel-to-screenplay-skill
```

### Option 3: Manual installation

Copy the `novel-to-screenplay` folder into your Claude Code skills directory:

```
~/.claude/skills/novel-to-screenplay/
# or
<project>/.claude/skills/novel-to-screenplay/
```

## Usage

Once installed, the skill triggers automatically when you say things like:

| Command | Mode |
|---------|------|
| "Adapt this novel into a screenplay" | Auto (ask) |
| "Convert to screenplay, one step" / "直接改编" | Auto |
| "Turn this into a movie script, step by step" / "分步骤改编" | Guided |
| "改编剧本" / "小说改编" / "写剧本" | Auto (ask) |

### Auto Mode Example

```
> Here's my novel text: [paste or provide .txt file]
> Convert this to a 90-minute movie screenplay.
```

Claude will analyze → outline → draft → self-review → output the complete screenplay.

### Guided Mode Example

```
> Here's my novel: [paste or provide .txt file]
> Help me adapt this step by step.
```

Claude will walk you through 4 phases with feedback opportunities at each stage:

1. **Story Analysis** — Character decisions, three-act mapping, adaptation challenges
2. **Scene Outline** — 40-55 scene breakdown with beats and page estimates
3. **Draft** — Full screenplay output by act for incremental review
4. **Polish** — Apply feedback and run quality checklist

## Project Structure

```
novel-to-screenplay/
├── SKILL.md                              # Main skill entry point
├── references/
│   ├── screenplay-format.md              # Hollywood formatting rules
│   └── adaptation-guide.md               # Novel→screenplay techniques
└── assets/
    └── screenplay-template.fountain      # Fountain format template
```

## Output Format

Screenplays are output in plain text following Hollywood standard formatting, compatible with [Fountain](https://fountain.io/) markup. Can be saved as `.fountain` or `.txt`.

## Supported Input

- Plain text (pasted directly)
- `.txt` files
- Any prose fiction content

## Roadmap

- [ ] TV series screenplay support (multi-episode arc)
- [ ] Stage play format
- [ ] Chinese screenplay format (中文剧本格式)
- [ ] PDF/DOCX input support

## License

MIT
