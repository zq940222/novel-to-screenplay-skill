---
name: novel-to-screenplay
description: >
  Adapt novels and stories into professional Hollywood-standard movie screenplays.
  Use when the user wants to: (1) Convert a novel/story into a screenplay,
  (2) Adapt fiction text into movie script format, (3) Transform narrative prose
  into cinematic scenes with proper formatting. Triggers include "adapt this novel",
  "convert to screenplay", "write a screenplay from this story", "turn this into
  a movie script", "novel to script", "改编剧本", "小说改编", "写剧本".
  Supports both full automatic adaptation and step-by-step guided workflow.
  Currently supports movie screenplays (90-120 min). Input: plain text, .txt files,
  or pasted novel content.
---

# Novel to Screenplay

Adapt novels into professional Hollywood-format movie screenplays.

## Workflow Overview

Two modes are available:

1. **Auto mode** — User provides novel text, receive complete screenplay
2. **Guided mode** — Step-by-step: analyze → outline → draft → polish

Determine which mode:
- User says "directly adapt" / "one step" / "直接改编" → **Auto mode**
- User says "step by step" / "guide me" / "分步骤" → **Guided mode**
- Unclear → Ask the user which mode they prefer

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

## Adaptation Techniques

For detailed guidance on converting novel elements to screen, see [adaptation-guide.md](references/adaptation-guide.md):
- **Show Don't Tell**: Converting internal narration to visual action
- **Compression**: 6:1 ratio strategies
- **Dialogue**: Removing exposition, adding subtext
- **Scene Conversion**: Distillation, visual substitution, scene fusion, externalization

## Format Reference

See [screenplay-format.md](references/screenplay-format.md) for complete Hollywood formatting:
- Scene headings, action, dialogue, transitions
- Special notations (V.O., O.S., MONTAGE, INTERCUT)
- Title page format, three-act page targets

## Output

Output the screenplay as plain text in standard screenplay format. Use [screenplay-template.fountain](assets/screenplay-template.fountain) as a starting point for the title page.

If the user requests a file, save as `.fountain` or `.txt`.
