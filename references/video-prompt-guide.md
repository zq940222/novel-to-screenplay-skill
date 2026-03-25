# AI Video Prompt Generation Guide

## Table of Contents
1. [Prompt Structure](#prompt-structure)
2. [Shot Segmentation Strategy](#shot-segmentation-strategy)
3. [Camera Language](#camera-language)
4. [Visual Description Techniques](#visual-description-techniques)
5. [Platform Parameters](#platform-parameters)
6. [Shot Continuity](#shot-continuity)
7. [Example Prompts](#example-prompts)

## Prompt Structure

Each video prompt follows this structure (order matters for AI weight):

```
[Subject & Action], [Environment/Setting], [Lighting & Atmosphere], [Camera Movement], [Style/Mood], [Technical Parameters]
```

### Key Principles
- Lead with the most important visual element (subject first)
- Use concrete, observable descriptions — no abstract emotions
- Each prompt = one continuous shot (5-10 seconds)
- English prompts generally produce better results than Chinese on most platforms
- Keep prompts under 200 words; 80-120 words is the sweet spot

## Shot Segmentation Strategy

### Screenplay Scene → Video Shots

One screenplay scene typically breaks into 3-8 video shots:

| Screenplay Element | Video Shot Type | Duration |
|-------------------|----------------|----------|
| Scene heading (establishing) | Wide/establishing shot | 5-8s |
| Action description | Medium/full shot | 5-8s |
| Dialogue line | Close-up / medium close-up | 5-8s |
| Reaction beat | Close-up reaction | 3-5s |
| Transition | Movement shot or cutaway | 3-5s |

### Segmentation Rules
1. **One action per shot** — "She walks in and sits down" = 2 shots
2. **One speaker per dialogue shot** — alternate between speakers
3. **Establish before detail** — wide shot first, then close-ups
4. **Group by visual continuity** — same location/lighting = batch
5. **Target 5-10 seconds per clip** — matches AI video generation limits

### Shot Sequence Pattern (per scene)
```
Shot 1: Establishing wide — set the location and time
Shot 2: Medium — introduce character(s) in context
Shot 3-N: Medium/close alternating — action and dialogue
Shot N+1: Reaction or cutaway — emotional beat
Shot N+2: Transition — bridge to next scene
```

## Camera Language

### Camera Movements (use in prompts)

| Movement | Prompt Keyword | Use For |
|----------|---------------|---------|
| Static | "static shot", "locked camera" | Dialogue, tension |
| Pan left/right | "camera pans left/right" | Reveal, follow action |
| Tilt up/down | "camera tilts up/down" | Reveal height, power |
| Dolly in/out | "camera slowly moves in/out" | Intimacy, isolation |
| Tracking | "camera tracks alongside" | Following movement |
| Crane up/down | "camera rises/descends" | Establishing, drama |
| Handheld | "handheld camera, slight shake" | Urgency, realism |
| Steadicam | "smooth following shot" | Elegant movement |
| Push in | "slow push in on face" | Realization, focus |
| Pull back | "camera pulls back to reveal" | Surprise, context |
| Orbit | "camera orbits around subject" | Hero moment, 360 view |
| Zoom | "slow zoom into" | Focus, dramatic |

### Shot Sizes

| Size | Prompt Description | Use For |
|------|-------------------|---------|
| Extreme wide | "extreme wide shot, vast landscape" | Establishing, scale |
| Wide | "wide shot showing full scene" | Context, geography |
| Full | "full body shot of character" | Movement, costume |
| Medium | "medium shot from waist up" | Dialogue, interaction |
| Medium close | "medium close-up, chest and above" | Emotion + context |
| Close-up | "close-up on face" | Emotion, detail |
| Extreme close-up | "extreme close-up on eyes/hands" | Tension, detail |
| Over-shoulder | "over the shoulder shot" | Dialogue coverage |
| POV | "point of view shot, first person" | Immersion |

### Angles

| Angle | Prompt Description | Psychological Effect |
|-------|-------------------|---------------------|
| Eye level | "eye level angle" | Neutral, relatable |
| Low angle | "low angle looking up" | Power, dominance |
| High angle | "high angle looking down" | Vulnerability, overview |
| Dutch angle | "tilted angle" | Unease, disorientation |
| Bird's eye | "overhead bird's eye view" | God view, pattern |
| Worm's eye | "ground level looking up" | Dramatic scale |

## Visual Description Techniques

### Character Description Formula
```
[age range] [gender] [ethnicity/skin tone] [distinctive feature], wearing [outfit], [expression/emotion through action]
```

Example: "A 30-year-old woman with sharp cheekbones and short black hair, wearing a worn leather jacket, staring intensely ahead"

**DO NOT** use: celebrity names, copyrighted character names, or real person references

### Environment Description Formula
```
[interior/exterior] [specific location type] [time of day], [weather/atmosphere], [key props/details], [lighting quality]
```

Example: "Interior of a dimly lit jazz bar at night, blue neon light filtering through rain-streaked windows, empty glasses on the counter, smoky atmosphere"

### Lighting Keywords
- Golden hour, warm sunlight, soft diffused light
- Harsh overhead fluorescent, cold blue light
- Rim lighting, backlit silhouette
- Candlelight, firelight warmth
- Neon glow, city lights reflection
- Dramatic chiaroscuro, high contrast shadows
- Overcast soft light, flat lighting

### Mood/Style Keywords
- Cinematic, film grain, anamorphic lens
- Photorealistic, hyperrealistic
- Moody, atmospheric, ethereal
- Gritty, raw, documentary style
- Dreamy, soft focus, romantic
- Dark, noir, high contrast
- Epic, grand, sweeping

## Platform Parameters

### Seedance 2.0 (即梦 AI)
- **Video length**: 5s or 10s per clip
- **Resolution**: 720p / 1080p
- **Aspect ratios**: 16:9 (landscape), 9:16 (portrait), 1:1 (square)
- **Input modes**: Text-to-video, Image-to-video, Video-to-video
- **Best practice**: Use reference image + text prompt for character consistency
- **Prompt language**: Chinese or English both supported; English often yields more cinematic results
- **Motion intensity**: Specify camera movement explicitly; default is minimal motion

### General AI Video Platform Tips
- Keep subject centered and clearly described
- Avoid complex multi-character interactions in a single shot
- Specify camera movement explicitly — AI defaults to minimal/random motion
- Use consistent character descriptions across shots for continuity
- Generate at highest resolution available, downscale if needed
- Batch similar shots (same location/lighting) together

## Shot Continuity

### Maintaining Visual Consistency Across Shots

**Character Consistency:**
- Use identical character descriptions across all shots of the same character
- Create a "character card" at the top of the shot list with fixed descriptions
- If platform supports reference images: generate one hero portrait first, use as reference for all subsequent shots

**Environment Consistency:**
- Describe the same location identically across shots within a scene
- Lock lighting description per scene (don't change unless time passes)
- Use "same scene as previous" style cues in notes

**Color/Mood Consistency:**
- Define a color palette per act or sequence
- Keep style keywords consistent within a scene
- Note any intentional shifts (e.g., "lighting shifts from warm to cold")

### Continuity Checklist Per Scene
- [ ] Same character appearance description across all shots
- [ ] Consistent environment/location description
- [ ] Matching lighting and time of day
- [ ] Logical camera progression (wide → medium → close)
- [ ] Props/costume unchanged within scene

## Example Prompts

### Establishing Shot
```
Prompt: "Extreme wide shot of a rain-soaked city street at night, neon signs reflecting in puddles, steam rising from manhole covers, a lone figure walking with an umbrella in the distance, cinematic atmosphere, blue and orange color palette, camera slowly dollies forward, 16:9 aspect ratio, photorealistic"

Duration: 8s | Shot: EWS | Camera: Dolly forward
```

### Character Introduction
```
Prompt: "Medium shot of a 30-year-old woman with short black hair and sharp features, wearing a worn brown leather jacket over a dark shirt, standing in a dimly lit doorway, rain dripping behind her, warm interior light on her face, cold blue light behind, she looks up slowly with determined expression, cinematic shallow depth of field, camera static"

Duration: 6s | Shot: MS | Camera: Static
```

### Dialogue Close-up
```
Prompt: "Close-up of a 30-year-old woman with short black hair, warm golden light from a table lamp on her face, soft shadows, slight frown as she speaks with intensity, shallow depth of field blurred background of a cozy apartment interior, static camera, cinematic film grain"

Duration: 5s | Shot: CU | Camera: Static
```

### Action Sequence
```
Prompt: "Medium tracking shot following a woman in a leather jacket sprinting through a narrow rain-soaked alley at night, neon signs blurring past, puddles splashing underfoot, handheld camera movement, urgent pace, dark atmospheric cinematography, motion blur on background"

Duration: 6s | Shot: Tracking MS | Camera: Handheld tracking
```

### Emotional Moment
```
Prompt: "Slow push-in close-up on a woman's face, tears welling in her eyes, warm golden hour sunlight streaming through a window, dust particles floating in the light, she closes her eyes and takes a deep breath, cinematic shallow depth of field, gentle lens flare, emotional intimate moment"

Duration: 8s | Shot: CU push-in | Camera: Slow push in
```

### Transition / Cutaway
```
Prompt: "Extreme close-up of a coffee cup on a wooden table, steam rising in slow motion, warm morning light, a hand reaches in and lifts the cup, camera tilts up to reveal a bright kitchen window, soft natural lighting, peaceful atmosphere"

Duration: 5s | Shot: ECU to reveal | Camera: Tilt up
```
