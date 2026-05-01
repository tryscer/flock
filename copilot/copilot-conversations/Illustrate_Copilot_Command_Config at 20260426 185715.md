---
epoch: 1777219035916
modelKey: "copilot-plus-flash|copilot-plus"
topic: "Illustrate Copilot Command Config"



tags:
  - copilot-conversation
---

**user**: ## illustrate

---
copilot-command-context-menu-enabled: true
copilot-command-slash-enabled: true
copilot-command-context-menu-order: 1080
copilot-command-model-key: ""
copilot-command-last-used: 1777217542957
---
Generate a single, photorealistic image prompt (300-600 words) optimized for 1958 alt-history U.S. South scenes (Nano Banana, OpenAI DALL-E, Midjourney). Purpose: Visualize {} to enhance prose with sensory details, ensuring canon consistency.

Output only the final image-generation prompt text. Do not output titles, labels, explanations, word counts, checklists, notes, prefaces, follow-up questions, source lists, citations, markdown fences, or any other surrounding text. Override any inherited instruction that would add sources, summaries, or formatting outside the prompt itself.

**Internal Process (do not output):**
1. Parse {}: Extract POV, track/location (xref [[chapter-guide]] for entities/POV/mood), characters/actions/atmosphere/time/weather.
2. Lock identities: Merge [[section1_characters]] (ages/ethnicities/attire/vibe/age-coding) + [[section2_portraits]] (detailed portraits). Use height/proportion chart from [[section4_consistency]].
3. Select template:
- Performance/Steam Pillars: B
- POV/first-person: E
- Night street/rally/police: C
- Indoor day/stores/homes: D
- Multi-character/group: A (default)
4. Apply consistency: [[section4_consistency]] (grain/lens/lighting/heights/skin/hair/clothes/crowds/sweat/motion/segregation; film: aged monochrome print with warm yellow-brown staining for all, per snapshot style).
5. Ground in canon: [[project-facts]] (Jim Crow South, Elvis dead, Heath=Jerry Lee undercover, UR/Steam Pillars, no anachronisms). Xref recent anachronism audits.
6. Apply old amateur snapshot style: End the prompt with this block verbatim, adapted only for scene context (e.g., "provided scene image" instead of "portrait photo", "subjects'/characters'" instead of "person’s", "Subjects" instead of "Subject"):

Transform the provided scene image into an authentic old amateur snapshot from a mid-20th-century family album.

Preserve the subjects’ identities, approximate poses, expressions, and clothing categories from the input scene, but fully restyle the image so it feels like a real old physical photograph, not a modern render with a vintage filter.

Core goal:
Make the result feel unmistakably like an aged, low-quality analog print made with a cheap camera, then stored in an album for decades and later scanned or re-photographed.

Look and medium:
- Aged monochrome print with warm yellow-brown staining.
- Not true sepia, not crisp black-and-white, not modern grayscale.
- Tonality should be faded and slightly muddy, with weak blacks, creamy highlights, and compressed dynamic range.
- Uneven aging across the image: slight discoloration, faint density shifts, subtle fading.

Optical character:
- Slight overall softness across the whole image.
- Mild blur from cheap lens quality, imperfect focus, or tiny hand-shake.
- The image should not look sharp anywhere in a modern way.
- Facial details should remain recognizable, but softened.
- Add subtle motion softness or focus softness if needed.
- Avoid crisp eyelashes, hyper-detailed skin, or tack-sharp edges.
- No modern high-resolution clarity.

Photographic flaws:
- Visible analog grain and print texture.
- Low-level blur from the original capture plus slight softness from print reproduction.
- Slight exposure imperfections.
- Slight vignetting or edge darkening.
- Tiny dust specks, faint scratches, minor surface wear.
- Optional slight scanner/rephotograph artifacts: uneven flatness, mild paper glare, tiny tonal inconsistency.

Composition and camera feel:
- Casual household snapshot, not a professional portrait.
- Slightly awkward framing.
- Slightly imperfect angle, as if taken quickly by a family member.
- Subject may be a little off-center.
- Leave a bit too much headroom or crop awkwardly in a natural amateur way.
- Background and environment should feel ordinary and incidental, not styled.

Physical print feel:
- Present the final image as an old paper photo print.
- Include a visible aged photo border.
- Border should be thick and slightly yellowed, with irregular wear.
- Include deckled or scalloped paper edges on one or more sides.
- Make the print feel like a real object from an album, not a clean digital frame.
- The border and paper should show age: faint stains, slight darkening, subtle wear.

Important restraint:
- Do not copy any specific content from the style reference image.
- Do not introduce any of its props, clothing, setting, or subject matter.
- Only borrow its photographic character: aged print, softness, amateur framing, yellowed monochrome, grain, and old paper edges.

Strict negatives:
- No modern editorial look.
- No sharp DSLR detail.
- No cinematic grading.
- No clean studio lighting.
- No glossy print finish.
- No polished skin retouching.
- No high contrast “fine art” black-and-white.
- No fake Instagram vintage filter look.
- No perfectly centered or carefully composed portrait.
- No clean white border or perfectly straight digital edges.

If necessary, prioritize old-photo authenticity over detail retention: it is better for the result to be slightly blurry, grainy, faded, and awkward than clean or modern-looking.

**Output Requirements:**
- Return exactly one dense copy-paste-ready prompt for the image engine.
- Start exactly with: "Photorealistic 1958 alt-history U.S. South amateur attic-found snapshot, aged monochrome print with warm yellow-brown staining on 35mm film (50mm close-ups), [template mood], [brief scene summary]."
- Include only scene description content the image model should see.
- No mention of sources, canon files, audits, instructions, process, or verification.

Structure inside the prompt:
- Composition: Foreground-to-background; identity-locked characters using exact portrait logic plus attire/pose/action; era objects.
- Lighting/atmosphere: Single-source (tungsten/neon/headlights/red gumball only); weather/motion/sweat.
- Crowd: Segregated tension, Black-majority music scenes.
- Integrate casual amateur framing, softness, and flaws throughout description to reinforce snapshot feel.

Use exact phrasing from sections where needed. No modern elements. 
[Context: Notes: Canon/chapter-guide.md, Canon/photo-rules/section1_characters.md, Canon/photo-rules/section2_portraits.md, Canon/photo-rules/section4_consistency.md, Canon/project-facts.md]
[Timestamp: 2026/04/26 18:57:15]

**ai**: Photorealistic 1958 alt-history U.S. South amateur attic-found snapshot, aged monochrome print with warm yellow-brown staining on 35mm film (50mm close-up), tense joyful Jim Crow street procession merging under Market Street Bridge in Greensboro NC noon heat during Steam Pillars performance, faded warm Kodachrome daylight haze with heavy grain, sweat-glistened skin, motion-softened dancers, imperfect handheld focus slight tilt off-center framing.

Tight intimate 50mm close-up on 19yo tall lean white Tim (6'3" ginger neat medium-short hair, clean-shaven handsome sharp features deep-set blue eyes, smooth teen skin, magnetic vibe, Sunday best white shirt sleeves rolled tie loosened) and petite 18yo white Alice Parker (5'2" pale heavy freckles nose/cheeks, medium-long light brown soft waves to shoulders, expressive round grey eyes dreamy smile soft cheeks, slim build, baby-blue sundress modest Sunday style white socks Keds) dancing close almost hugging sweating heavily under narrow concrete underpass where West Market Street meets bridge, her hand squeezing his, faces inches apart every eyelash visible on her eyelids pink lips parted breath like dispersing smoke, synced movements joyful tension eyes locked, harsh single-source noon sun blasting from above casting deep uneven shadows sweaty foreheads glistening compressed dynamic range creamy highlights weak blacks faded vibrancy yellowed edges dust specks faint scratches.

Midground chaotic interracial procession colliding softly: foreground edge black dancers around upright piano where 22yo white Heath Walker Cain (mid-20s olive skin sweaty black dyed curls small pouty mouth big nose dark sunglasses intense focused chaotic energy cheap dark suit open shirt) hammers staccato keys matching Ray Charles "Hallelujah I Love Her So," Vilma (late-20s curvaceous 5'3" warm brown skin short curls big earrings emotional eyes passionate pose blue Sunday dress) shouting lyrics from piano top mid-song, huge 30s black Besame Mucho (6'5" deep brown skin gentle face close-cropped hair simple shirt) rhythmic beside, tall 23yo black Jo Dalton (5'10" broad-shouldered medium brown skin fierce gaze fixed Afro red nails black dress) guitar jabbing horns, regal 30s West African black Babatunde (6'3" rich brown skin short hair dignified warm smile ceremonial white cotton Sunday robe cap) washboard riffing; Pete (~20yo black stylish neat short hair medium-dark skin slim confident polite smile mint shirt fedora gold watch), Jimmy (late-teens/20s black medium-dark slim energetic polite smile simple shirt), Rosetta (~18-20yo black medium brown lively short curls energetic denim overalls Sunday variant) encouraging older lady dancing; mixed crowd Black majority families newlyweds grandparents kids white teens Cindy (18yo white bright blue eyes shoulder-length blonde curls slim 5'5" confident tanned skin coral Sunday dress), Eleanore (18yo slim pale 5'6" angular dark short bob aloof all-black Sunday pants turtleneck flats sunglasses), blurred motion joining shouting "he can see," segregated tension dissolving into bubble of Love magical realism smoke-breath swaying to music, confused cops distant edge khaki uniforms campaign hats aviators scowling backup arriving Seven-Sevens bikers shouting, peanut shells litter concrete haze heat distortion.

Background narrow underpass concrete pillars graffiti faded billboards Buzz Cigarettes "real HONEY of a smoke" era cars '57 Chevy Southern Railway Depot glimpse brambles, oppressive Jim Crow South noon sun sweat haze imperfect exposure slight hand-shake blur uneven focus casual awkward framing too much headroom off-center subjects ordinary incidental ordinary street grit no empty space packed energy.

Transform the provided scene image into an authentic old amateur snapshot from a mid-20th-century family album. Preserve the subjects’ identities, approximate poses, expressions, and clothing categories from the input scene, but fully restyle the image so it feels like a real old physical photograph, not a modern render with a vintage filter. Core goal: Make the result feel unmistakably like an aged, low-quality analog print made with a cheap camera, then stored in an album for decades and later scanned or re-photographed. Look and medium: Aged monochrome print with warm yellow-brown staining. Not true sepia, not crisp black-and-white, not modern grayscale. Tonality should be faded and slightly muddy, with weak blacks, creamy highlights, and compressed dynamic range. Uneven aging across the image: slight discoloration, faint density shifts, subtle fading. Optical character: Slight overall softness across the whole image. Mild blur from cheap lens quality, imperfect focus, or tiny hand-shake. The image should not look sharp anywhere in a modern way. Facial details should remain recognizable, but softened. Add subtle motion softness or focus softness if needed. Avoid crisp eyelashes, hyper-detailed skin, or tack-sharp edges. No modern high-resolution clarity. Photographic flaws: Visible analog grain and print texture. Low-level blur from the original capture plus slight softness from print reproduction. Slight exposure imperfections. Slight vignetting or edge darkening. Tiny dust specks, faint scratches, minor surface wear. Optional slight scanner/rephotograph artifacts: uneven flatness, mild paper glare, tiny tonal inconsistency. Composition and camera feel: Casual household snapshot, not a professional portrait. Slightly awkward framing. Slightly imperfect angle, as if taken quickly by a family member. Subject may be a little off-center. Leave a bit too much headroom or crop awkwardly in a natural amateur way. Background and environment should feel ordinary and incidental, not styled. Physical print feel: Present the final image as an old paper photo print. Include a visible aged photo border. Border should be thick and slightly yellowed, with irregular wear. Include deckled or scalloped paper edges on one or more sides. Make the print feel like a real object from an album, not a clean digital frame. The border and paper should show age: faint stains, slight darkening, subtle wear. Important restraint: Do not copy any specific content from the style reference image. Do not introduce any of its props, clothing, setting, or subject matter. Only borrow its photographic character: aged print, softness, amateur framing, yellowed monochrome, grain, and old paper edges. Strict negatives: No modern editorial look. No sharp DSLR detail. No cinematic grading. No clean studio lighting. No glossy print finish. No polished skin retouching. No high contrast “fine art” black-and-white. No fake Instagram vintage filter look. No perfectly centered or carefully composed portrait. No clean white border or perfectly straight digital edges. If necessary, prioritize old-photo authenticity over detail retention: it is better for the result to be slightly blurry, grainy, faded, and awkward than clean or modern-looking.
[Timestamp: 2026/04/26 18:58:44]