---
name: novel-to-screenplay
description: >
  Adapt novels into Hollywood screenplays AND generate AI video prompts for
  platforms like Seedance 2.0 (即梦AI). Full pipeline: novel → screenplay →
  shot-by-shot video prompts with content safety filtering.
  Use when: (1) Convert novel/story to screenplay, (2) Generate video prompts
  from screenplay/novel, (3) Create AI video shot lists for Seedance/即梦/Runway/Kling.
  Triggers: "adapt this novel", "convert to screenplay", "novel to script",
  "改编剧本", "小说改编", "写剧本", "generate video prompts", "生成视频提示词",
  "分镜头提示词", "AI视频", "screenplay to video".
  Supports auto/guided modes, content moderation safety rewriting.
  Input: plain text, .txt files, or pasted content.
---

# Novel to Screenplay + AI Video Prompts

Full pipeline: Novel → Screenplay → AI Video Prompts (Seedance 2.0 / 即梦 AI compatible).

## Workflow Overview

Three capabilities:

1. **Screenplay Mode** — Novel → Hollywood-format screenplay (Auto or Guided)
2. **Video Prompt Mode** — Screenplay → Shot-by-shot AI video prompts
3. **Full Pipeline** — Novel → Screenplay → Video prompts (end-to-end)

Determine which workflow:
- "改编剧本" / "adapt to screenplay" → **Screenplay only**
- "生成视频提示词" / "generate video prompts" / "分镜头" → **Video Prompt only** (from existing screenplay)
- "从小说到视频" / "novel to video" / "full pipeline" → **Full Pipeline**
- "直接改编" / "one step" → **Auto mode**
- "分步骤" / "step by step" / "guide me" → **Guided mode**
- Unclear → Ask the user which workflow they need

---

## Auto Mode

Execute all steps sequentially, output the final screenplay.

### Step 1: Read and Analyze
Read the full novel text. Extract:
- Protagonist, antagonist, key supporting characters (limit to 5-8)
- Central conflict and stakes
- Theme
- Key plot events mapped to three-act structure

### Step 2: Build Scene Outline
Create a scene-by-scene outline (~40-55 scenes for 90 min). Each entry:
```
Scene #: INT/EXT. LOCATION - TIME
Characters: [list]
Beat: [what happens — one sentence]
Purpose: [setup / conflict / revelation / climax / resolution]
Page estimate: [X-Y]
```

### Step 3: Draft the Screenplay
Write the full screenplay following Hollywood format. See [screenplay-format.md](references/screenplay-format.md) for formatting rules.

Key rules:
- FADE IN: at the start, FADE OUT. at the end
- Scene headings: `INT./EXT. LOCATION - TIME` in ALL CAPS
- First character appearance: NAME in ALL CAPS with (age, brief description)
- Action lines: present tense, only what camera sees/hears, 3-4 lines max per paragraph
- Dialogue: character name centered in ALL CAPS, dialogue below
- Target ~90 pages (1 page ≈ 1 minute)

### Step 4: Self-Review
Check the draft against these criteria:
- [ ] Three-act structure is clear with proper turning points
- [ ] No internal monologue left unconverted (must be visual/behavioral)
- [ ] Each scene has a clear purpose — cut any that don't advance plot or character
- [ ] Dialogue has subtext, not on-the-nose exposition
- [ ] Character voices are distinct
- [ ] Page count is within 85-95 pages
- [ ] Format follows Hollywood standard

Fix any issues, then output the final screenplay.

---

## Guided Mode

### Phase 1: Story Analysis Report
Read the novel and present a structured analysis:

**Story Spine:**
- Protagonist: [name, goal, flaw]
- Antagonist/Opposition: [name/force, goal]
- Central conflict: [one sentence]
- Stakes: [what's at risk]
- Theme: [one sentence]

**Character Decisions:**
| Character | Role | Decision | Reason |
|-----------|------|----------|--------|
| Name | Protagonist | Keep | Drives main plot |
| Name | Supporting | Merge with X | Similar function |
| Name | Minor | Cut | Subplot only |

**Three-Act Mapping:**
- Act 1 (pages 1-22): [key events]
- Act 2A (pages 23-45): [key events]
- Act 2B (pages 46-67): [key events]
- Act 3 (pages 68-90): [key events]

**Adaptation Challenges:**
- [list challenges, e.g., "heavy internal monologue in chapters 3-5"]
- [proposed solutions for each]

Wait for user feedback before proceeding.

### Phase 2: Scene Outline
Present the scene-by-scene outline (same format as Auto Step 2).
Wait for user approval/edits.

### Phase 3: Draft Screenplay
Write the screenplay based on the approved outline. Output in sections (Act 1, Act 2A, Act 2B, Act 3) for incremental feedback.

### Phase 4: Polish
Apply user feedback. Run the self-review checklist from Auto Step 4.

---

---

## Video Prompt Mode (Screenplay → AI Video Shots)

Convert a screenplay (or novel, if using Full Pipeline) into shot-by-shot AI video generation prompts. Compatible with Seedance 2.0 (即梦 AI), Kling, Runway, and similar platforms.

### Step V1: Character Cards
Before generating shots, create a **Character Card** for each main character. This card is reused verbatim across ALL shots featuring that character to maintain visual consistency.

```
CHARACTER CARD: [Character Name]
Visual: [age] [gender] [ethnicity/skin tone] [hair] [distinctive features]
Default outfit: [primary clothing description]
Expression baseline: [neutral demeanor]
```

Example:
```
CHARACTER CARD: Sarah
Visual: 30-year-old woman, East Asian, short black hair with sharp cheekbones
Default outfit: worn brown leather jacket over dark shirt, black jeans
Expression baseline: focused, intense gaze
```

### Step V2: Scene-to-Shot Breakdown
For each screenplay scene, decompose into individual video shots. See [video-prompt-guide.md](references/video-prompt-guide.md) for camera language and shot types.

**Segmentation rules:**
- One action per shot (5-10 seconds each)
- Start each scene with an establishing wide shot
- One speaker per dialogue shot
- Use reaction shots between dialogue exchanges
- Group shots by visual continuity (same location/lighting)

Output format per shot:
```
SCENE [#] — SHOT [#]
Shot type: [EWS/WS/MS/MCU/CU/ECU] | Camera: [movement] | Duration: [Xs]
Screenplay reference: [which action/dialogue line this covers]
---
Prompt: "[complete AI video prompt — see structure below]"
---
Safety notes: [any content flags and rewrites applied]
```

### Step V3: Prompt Construction
Each prompt follows this structure (order = AI weight priority):

```
[Subject & Action], [Environment/Setting], [Lighting & Atmosphere], [Camera Movement], [Style/Mood]
```

**Rules:**
- Lead with the character card description (copy verbatim for consistency)
- 80-120 words per prompt (sweet spot for most platforms)
- English prompts for best cinematic results
- Specify camera movement explicitly — AI defaults to minimal/random motion
- End with style keywords: "cinematic, photorealistic, shallow depth of field, film grain"
- Add "16:9 aspect ratio" for widescreen film look

### Step V4: Content Safety Review (CRITICAL)
**Every prompt MUST pass the safety check before output.** See [content-safety-guide.md](references/content-safety-guide.md) for complete rules.

Apply the **5 Substitution Principles** for any flagged content:
1. **Implication over depiction** — show before/after, skip the act
2. **Emotion over action** — terrified face > what causes terror
3. **Shadow and silhouette** — outlines convey threat without explicit content
4. **Metaphor and symbol** — wilting flower, cracking mirror, rain on window
5. **Sound cues in notes** — "the sound of shattering glass" (for editing, not for AI prompt)

**ZERO TOLERANCE rules** (instant rejection — rewrite ALWAYS):
- **Real person names** → replace with generic physical descriptions (age, build, hair, features)
- **Real person photos as input** → generate AI character portrait first, use that as reference
- **Copyrighted characters** (Mickey Mouse, Spider-Man, Pikachu, Doraemon, etc.) → describe appearance generically without naming the character or franchise
- **Brand names/logos** (Nike, Apple, Ferrari, Starbucks, etc.) → describe the generic object only
- **Franchise-specific props** (lightsabers, dragon balls, Death Note, etc.) → abstract to generic equivalents

**Other auto-rewrite triggers** (rewrite before outputting):
- Violence/weapons → reaction shots, aftermath, silhouettes
- Sexual/intimate → proximity, eye contact, soft lighting
- Gore/horror → atmosphere, shadows, character reactions
- Drugs/smoking → empty glasses, hazy atmosphere, altered-state styling
- Political/religious → fictionalized/abstract equivalents
- Minors in danger → split into before/reaction/after shots

**Safety suffix** — append to any borderline prompt:
> "cinematic and non-graphic, artistic composition, PG-13 appropriate"

### Step V5: Shot List Assembly
Output the complete shot list organized by scene, with:
1. **Character Cards** section at the top
2. **Shots grouped by scene** with sequential numbering
3. **Continuity notes** between scenes (lighting shifts, costume changes, time jumps)
4. **Total shot count** and **estimated total video duration**

For a 90-minute screenplay, expect approximately:
- 40-55 scenes → 150-300 individual shots
- At 5-8 seconds per shot → 12-40 minutes of raw AI video
- Post-production editing assembles the final cut

### Output Format Options
Ask the user which format they prefer:
- **Structured text** — formatted shot list as shown above
- **CSV/table** — for batch processing (columns: scene, shot, type, camera, duration, prompt, safety_flag)
- **Per-scene batches** — output one scene at a time for iterative workflow

---

## Reference Files

### Screenplay
- [screenplay-format.md](references/screenplay-format.md) — Hollywood formatting rules, scene headings, dialogue, transitions, three-act structure
- [adaptation-guide.md](references/adaptation-guide.md) — Novel-to-screen techniques: show don't tell, compression, dialogue, scene conversion

### Video Prompts
- [video-prompt-guide.md](references/video-prompt-guide.md) — Prompt structure, camera language, shot types, platform parameters, continuity, examples
- [content-safety-guide.md](references/content-safety-guide.md) — Content moderation rules, rewriting strategies for violence/sex/drugs/politics, platform-specific notes

### Assets
- [screenplay-template.fountain](assets/screenplay-template.fountain) — Fountain format title page template

## Output

**Screenplay output**: plain text in Hollywood format. Save as `.fountain` or `.txt`.

**Video prompt output**: structured shot list with prompts. Save as `.txt` or `.csv`.
