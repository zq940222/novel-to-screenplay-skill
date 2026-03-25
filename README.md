# Novel to Screenplay Skill

[中文文档](README_CN.md)

A [Claude Code](https://docs.anthropic.com/en/docs/claude-code) skill that adapts novels into Hollywood screenplays and generates shot-by-shot AI video prompts for platforms like Seedance 2.0 (即梦 AI).

## Features

### Screenplay Adaptation
- **Two Adaptation Modes**
  - **Auto Mode** — One-step: provide novel text, receive a complete screenplay
  - **Guided Mode** — Step-by-step collaboration: story analysis → scene outline → draft → polish
- **Hollywood Standard Format** — Scene headings, action lines, dialogue, transitions, V.O., O.S., MONTAGE, INTERCUT
- **Three-Act Structure** — Automatic mapping of novel plot to cinematic three-act structure (~90 pages ≈ 90 minutes)
- **Smart Adaptation** — Character merging/cutting, 6:1 compression, internal monologue → visual action conversion

### AI Video Prompt Generation
- **Screenplay → Shot List** — Automatically decompose scenes into 5-10 second video shots
- **Character Cards** — Consistent visual descriptions reused across all shots for continuity
- **Camera Language** — Full cinematic vocabulary: shot sizes, angles, movements, transitions
- **Platform Ready** — Optimized for Seedance 2.0 (即梦 AI), Kling, Runway, and similar platforms
- **Multiple Output Formats** — Structured text, CSV/table for batch processing, or per-scene batches

### Content Safety & Moderation
- **Auto Safety Rewriting** — Detects and rewrites prompts that would fail platform moderation
- **7 Risk Categories** — Violence, weapons, sexual content, horror, drugs, political, minors
- **5 Substitution Principles** — Implication over depiction, emotion over action, shadow/silhouette, metaphor, sound cues
- **Platform-Specific Rules** — Tailored safety strategies for Chinese and Western AI video platforms

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

Once installed, the skill triggers automatically:

| Command | Workflow |
|---------|----------|
| "Adapt this novel into a screenplay" | Screenplay only |
| "Generate video prompts from this screenplay" | Video prompts only |
| "Novel to video, full pipeline" / "从小说到视频" | Full pipeline |
| "直接改编" / "一键改编" | Auto mode |
| "分步骤改编" / "step by step" | Guided mode |
| "生成视频提示词" / "分镜头提示词" | Video prompts |

### Full Pipeline Example

```
> Here's my novel: [paste or provide .txt file]
> Convert this to a 90-minute movie and generate video prompts for Seedance.
```

Claude will: analyze novel → write screenplay → create character cards → generate shot-by-shot video prompts → safety review all prompts.

### Video Prompt Output Example

```
SCENE 3 — SHOT 2
Shot type: MS | Camera: Static | Duration: 6s
Screenplay reference: Sarah enters the bar and scans the room
---
Prompt: "Medium shot of a 30-year-old woman with short black hair and sharp
cheekbones, wearing a worn brown leather jacket, stepping through a doorway
into a dimly lit jazz bar, neon blue light filtering through rain-streaked
windows behind her, she pauses and scans the room with focused intensity,
cinematic shallow depth of field, warm interior light on face, static camera,
film grain, 16:9 aspect ratio"
---
Safety notes: None — clean prompt
```

## Project Structure

```
novel-to-screenplay/
├── SKILL.md                              # Main skill: workflows + triggers
├── references/
│   ├── screenplay-format.md              # Hollywood formatting rules
│   ├── adaptation-guide.md               # Novel→screenplay techniques
│   ├── video-prompt-guide.md             # AI video prompt construction
│   └── content-safety-guide.md           # Platform moderation rules
└── assets/
    └── screenplay-template.fountain      # Fountain format template
```

## Output Formats

- **Screenplay**: Plain text in Hollywood format → `.fountain` or `.txt`
- **Video prompts**: Structured shot list → `.txt` or `.csv`

## Supported Input

- Plain text (pasted directly)
- `.txt` files
- Any prose fiction content
- Existing screenplay text (for video prompt generation)

## Roadmap

- [x] AI video prompt generation with content safety
- [ ] TV series screenplay support (multi-episode arc)
- [ ] Stage play format
- [ ] Chinese screenplay format (中文剧本格式)
- [ ] PDF/DOCX input support
- [ ] Image reference generation for character consistency

## License

MIT
