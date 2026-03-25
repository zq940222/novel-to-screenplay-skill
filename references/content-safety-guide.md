# Content Safety & Platform Moderation Guide

AI video platforms enforce strict content moderation. Prompts that trigger filters will be rejected. This guide provides rewriting strategies to preserve narrative intent while passing moderation.

## High-Risk Categories

### 1. Violence & Gore
**Blocked**: Blood, wounds, weapons in use, death scenes, fighting, injury detail

**Rewriting Strategies:**
| Original Intent | Safe Replacement |
|-----------------|------------------|
| Character gets shot | Character stumbles backward, clutches chest, falls (no blood, no weapon visible) |
| Bloody wound | Character presses hand against side, grimaces in pain |
| Fistfight | Two figures grappling, intense physical confrontation, dynamic movement (no impact frames) |
| Dead body | Figure lying motionless on the ground, eyes closed, peaceful |
| Stabbing | Character gasps, reaches toward another character, drops to knees |
| Explosion with casualties | Bright flash of light, shockwave, dust and debris, characters thrown back |
| War battle | Large group of soldiers advancing through smoke and fog, tense atmosphere |

**Technique**: Show the BEFORE and AFTER of violence, skip the moment of impact. Use reaction shots instead of action shots.

### 2. Weapons & Military
**Blocked**: Visible guns, knives in threatening context, missiles, bombs

**Rewriting Strategies:**
| Original Intent | Safe Replacement |
|-----------------|------------------|
| Character holding gun | Character in tactical stance, hands raised in ready position, intense focus |
| Pointing weapon at someone | Two characters in tense standoff, facing each other, dramatic lighting |
| Military assault | Soldiers moving through fog, silhouettes against smoke, urgent movement |
| Sniper scene | Character lying prone on rooftop, looking through a scope-like device, one eye closed |

**Technique**: Focus on the character's body language and emotion rather than the weapon. Use silhouettes and shadows to imply threat.

### 3. Sexual & Suggestive Content
**Blocked**: Nudity, sexual acts, overly revealing clothing, suggestive poses, intimate physical contact

**Rewriting Strategies:**
| Original Intent | Safe Replacement |
|-----------------|------------------|
| Love scene | Two faces close together, foreheads touching, warm soft lighting, intimate whisper |
| Kiss | Faces inches apart, eyes closed, soft golden light, tender moment |
| Revealing outfit | Character in elegant/stylish attire, confident pose |
| Morning after | Character wrapped in blanket by window, morning light, contemplative expression |
| Physical attraction | Lingering eye contact across a room, slight smile, slow motion |

**Technique**: Use proximity, lighting, and eye contact to convey intimacy. Show emotional connection rather than physical.

### 4. Horror & Disturbing Imagery
**Blocked**: Gore, mutilation, extreme fear imagery, torture, graphic horror

**Rewriting Strategies:**
| Original Intent | Safe Replacement |
|-----------------|------------------|
| Monster/creature | Mysterious dark silhouette, partially obscured by fog/shadow |
| Jump scare | Character's face suddenly shifts to shock, quick camera push-in, dramatic lighting change |
| Haunted scene | Eerie atmosphere, cold breath visible, flickering lights, long shadows |
| Torture | Character bound to chair in dark room, single overhead light, distressed expression |

**Technique**: Atmosphere over explicit imagery. Shadows, sound design cues (in text), and reaction shots create horror effectively.

### 5. Drugs & Substance Abuse
**Blocked**: Drug use, drug paraphernalia, intoxication depiction, smoking (on some platforms)

**Rewriting Strategies:**
| Original Intent | Safe Replacement |
|-----------------|------------------|
| Character drinking heavily | Character sitting alone at a bar, rows of empty glasses, weary expression |
| Drug use | Character in altered state, hazy/distorted visual style, unfocused eyes |
| Smoking | Character standing outside, breath visible in cold air, contemplative |
| Overdose | Character slumped in chair, unresponsive, another character rushing to help |

### 6. Political & Sensitive Topics
**Blocked**: Political figures, national symbols in negative context, religious offense, hate symbols

**Rewriting Strategies:**
- Replace specific political references with fictional equivalents
- Use generic "authority figure" instead of specific political roles
- Avoid national flags, emblems, or uniforms that identify real countries
- Replace religious symbols with abstract/fictional spiritual imagery

### 7. Minors in Danger
**Blocked**: Children in any violent, dangerous, or distressing situation

**Rewriting Strategy**: If the scene involves a child in peril, split into:
- Shot A: The child in a safe context (before danger)
- Shot B: Adult character's reaction of fear/urgency (no child visible)
- Shot C: Resolution with child safe (after danger)
Never show a child in the dangerous moment itself.

## Universal Safety Rewriting Rules

### The 5 Substitution Principles

1. **Implication over depiction** — Show the cause and the aftermath, skip the act itself
2. **Emotion over action** — A terrified face is more powerful (and safer) than showing what causes the terror
3. **Shadow and silhouette** — Dark outlines convey threat without explicit content
4. **Metaphor and symbol** — A wilting flower, a cracking mirror, rain on a window
5. **Sound cues in description** — "the sound of shattering glass" in scene notes (for editing, not for AI prompt)

### Safety Prompt Suffixes
Add these to any borderline prompt to reduce rejection risk:
- "tasteful and artistic composition"
- "cinematic and non-graphic"
- "suggestive but not explicit"
- "dramatic shadows obscuring detail"
- "PG-13 appropriate"
- "artistic and atmospheric"

### Pre-Submission Checklist
Before finalizing any prompt, verify:
- [ ] No visible weapons in active use
- [ ] No blood, gore, or graphic injury
- [ ] No nudity or overtly sexual content
- [ ] No real political figures or sensitive symbols
- [ ] No children in dangerous or distressing situations
- [ ] No drug use or paraphernalia shown
- [ ] No hate speech, slurs, or discriminatory content
- [ ] No real brand logos or copyrighted characters
- [ ] No celebrity faces or likenesses referenced by name

## Platform-Specific Notes

### Seedance 2.0 (即梦 AI)
- Stricter on violence and sexual content than Western platforms
- Political sensitivity: avoid any content related to Chinese politics, leaders, or sensitive historical events
- Religious content: keep abstract and respectful
- Smoking/alcohol: generally filtered; use the substitution strategies above
- Text/watermarks: avoid prompts that generate text on screen (often garbled)
- Chinese cultural sensitivity: respect traditional symbols, avoid stereotypes

### General Platform Tips
- When in doubt, make the prompt more abstract/artistic
- Test borderline prompts with a single shot before batching
- Keep a "safe version" and "director's cut version" of sensitive scenes
- Use post-production editing to combine safe AI outputs into a cohesive sequence
