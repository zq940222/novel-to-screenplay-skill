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

### 8. Real Persons & Likenesses (CRITICAL — Instant Rejection)
**Blocked**: ANY real person's name, celebrity reference, public figure, real person's photo/image as reference input. This is the #1 cause of prompt rejection on Chinese AI video platforms.

**What triggers rejection:**
- Real names in any language: "Tom Cruise", "刘德华", "Taylor Swift"
- Indirect references: "a famous Hollywood actor", "looks like [celebrity]"
- Character descriptions that clearly describe a specific real person
- Using real person photos as image-to-video reference input
- Historical figures by name: "Napoleon", "秦始皇" (context-dependent)
- Social media influencers, YouTubers, streamers by name

**Rewriting Strategies:**
| Original Intent | Safe Replacement |
|-----------------|------------------|
| "Looks like Brad Pitt" | "Ruggedly handsome man in his 40s with chiseled jawline and tousled blonde hair" |
| "A woman resembling Audrey Hepburn" | "Elegant woman with short dark hair, slender neck, refined features, classic beauty" |
| "Obama gives a speech" | "A distinguished authority figure in a dark suit addresses a crowd from a podium" |
| "Jackie Chan fighting" | "Athletic middle-aged man with agile movements performing martial arts" |
| "周杰伦 singing" | "Young man with stylish cap performing on a neon-lit stage, passionate expression" |
| Real person photo as input | Generate a fictional character portrait first, use THAT as reference |

**Mandatory Rules:**
1. **NEVER use real person names** in any prompt — not even in parenthetical notes
2. **NEVER reference celebrities** even indirectly ("that famous actor from...")
3. **Describe features generically** — age, build, hair, expression — never a specific identity
4. **Image inputs must be fictional** — AI-generated portraits, illustrations, or stock photos only
5. **Historical figures**: replace with role descriptions ("a military commander", "an emperor in ancient robes")

### 9. Copyright & Intellectual Property
**Blocked**: Copyrighted characters, brand logos, trademarked designs, recognizable IP elements

**What triggers rejection:**
- Character names from movies/anime/games: "Spider-Man", "孙悟空 (from specific adaptation)", "Mario"
- Brand logos: Nike swoosh, Apple logo, Coca-Cola
- Specific franchise elements: lightsabers (Star Wars), wands with specific designs (Harry Potter)
- Song lyrics or book quotes embedded in prompts
- Recognizable costume/outfit designs from specific IPs
- Architecture/locations that are trademarked (e.g., specific theme park castles)

**Rewriting Strategies:**
| Original Intent | Safe Replacement |
|-----------------|------------------|
| "Spider-Man swinging" | "A masked figure in a red and blue suit swinging between buildings on web-like ropes" |
| "Wearing Nike shoes" | "Wearing modern athletic sneakers" |
| "Hogwarts castle" | "A grand medieval castle with multiple towers on a misty hilltop" |
| "A character like Goku" | "A muscular warrior with spiky black hair in an orange martial arts uniform, energy aura" |
| "Starbucks coffee cup" | "A paper coffee cup with a green circular logo" → better: "a paper coffee cup" |
| "Driving a Ferrari" | "Driving a sleek red Italian sports car" |
| "Lightsaber duel" | "Two figures clashing with glowing energy swords in a dark corridor" |

**Mandatory Rules:**
1. **NEVER use copyrighted character names** — describe appearance generically
2. **NEVER include brand names** — describe the object without brand identity
3. **Remove all logos** — if a scene needs branded items, describe only the generic object
4. **Franchise elements**: abstract to generic fantasy/sci-fi equivalents
5. **Music/text**: never embed copyrighted lyrics or quotes in prompts
6. **When adapting a published novel**: the story itself is licensed, but visual prompts must not reference other copyrighted visual IPs

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
- [ ] **No real person names or likenesses** — no celebrities, politicians, historical figures, influencers
- [ ] **No real person photos as reference input** — only AI-generated or stock images
- [ ] **No copyrighted characters** — no Mickey Mouse, Spider-Man, Pikachu, 孙悟空 (specific adaptations), etc.
- [ ] **No brand names or logos** — no Nike, Apple, Coca-Cola, Ferrari, Starbucks, etc.
- [ ] **No franchise-specific props** — no lightsabers, Mjolnir, Death Note, dragon balls, etc.
- [ ] No visible weapons in active use
- [ ] No blood, gore, or graphic injury
- [ ] No nudity or overtly sexual content
- [ ] No real political figures or sensitive symbols
- [ ] No children in dangerous or distressing situations
- [ ] No drug use or paraphernalia shown
- [ ] No hate speech, slurs, or discriminatory content

## Platform-Specific Notes

### Seedance 2.0 (即梦 AI)

**Instant rejection triggers (zero tolerance):**
- **Real person names** — ANY real name in prompt text = instant rejection
- **Real person photos** — using a real person's photo as image reference input = instant rejection
- **Copyrighted characters** — Mickey Mouse (米老鼠), Doraemon (哆啦A梦), Pikachu (皮卡丘), Naruto (鸣人), etc. = instant rejection
- **Brand logos** — any recognizable trademark in prompt or reference image

**Other strict filters:**
- Violence and sexual content: stricter than Western platforms
- Political sensitivity: avoid any content related to Chinese politics, leaders, or sensitive historical events
- Religious content: keep abstract and respectful
- Smoking/alcohol: generally filtered; use the substitution strategies above
- Text/watermarks: avoid prompts that generate text on screen (often garbled)
- Chinese cultural sensitivity: respect traditional symbols, avoid stereotypes

**Recommended workflow for Seedance:**
1. Generate all character portraits using AI first (no real person reference)
2. Use these AI portraits as image-to-video reference for consistency
3. Run every prompt through the Pre-Submission Checklist above
4. Test one shot per scene before batch generating

### General Platform Tips
- When in doubt, make the prompt more abstract/artistic
- Test borderline prompts with a single shot before batching
- Keep a "safe version" and "director's cut version" of sensitive scenes
- Use post-production editing to combine safe AI outputs into a cohesive sequence
- **Golden rule**: if a prompt contains a proper noun (person name, brand, character name), replace it with a generic description
