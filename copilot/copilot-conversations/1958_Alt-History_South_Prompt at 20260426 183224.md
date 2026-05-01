---
epoch: 1777217544104
modelKey: "copilot-plus-flash|copilot-plus"
topic: "1958 Alt-History South Prompt"



tags:
  - copilot-conversation
---

**user**: Generate a single, photorealistic image prompt (300-600 words) optimized for 1958 alt-history U.S. South scenes (Nano Banana, OpenAI DALL-E, Midjourney). Purpose: Visualize {} to enhance prose with sensory details, ensuring canon consistency.

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
4. Apply consistency: [[section4_consistency]] (grain/lens/lighting/heights/skin/hair/clothes/crowds/sweat/motion/segregation; film: Kodachrome=day, Ektachrome=night/performance).
5. Ground in canon: [[project-facts]] (Jim Crow South, Elvis dead, Heath=Jerry Lee undercover, UR/Steam Pillars, no anachronisms). Xref recent anachronism audits.

**Output Requirements:**
- Return exactly one dense copy-paste-ready prompt for the image engine.
- Start exactly with: "Photorealistic 1958 alt-history U.S. South scene on [film stock] 35mm (50mm close-ups), [template mood], [brief scene summary]."
- Include only scene description content the image model should see.
- No mention of sources, canon files, audits, instructions, process, or verification.

Structure inside the prompt:
- Composition: Foreground-to-background; identity-locked characters using exact portrait logic plus attire/pose/action; era objects.
- Lighting/atmosphere: Single-source (tungsten/neon/headlights/red gumball only); weather/motion/sweat.
- Crowd: Segregated tension, Black-majority music scenes.

Use exact phrasing from sections where needed. No modern elements. 
[Context: Notes: Canon/chapter-guide.md, Canon/photo-rules/section1_characters.md, Canon/photo-rules/section2_portraits.md, Canon/photo-rules/section4_consistency.md, Canon/project-facts.md]
[Timestamp: 2026/04/26 18:32:24]

**ai**: Photorealistic 1958 alt-history U.S. South scene on aged Ektachrome 35mm (50mm close-ups), somber grief-stricken night drive-in infiltration, Tim's POV peering through Barry's '57 Chevy Bel Air window at crying Elvis fans during Hitching Post Drive-In screening of Jailhouse Rock, post-death radio news shock rippling through parked cars.

Inside dimly lit '57 Chevy Bel Air gliding silently between rows of parked '50s sedans and coupes facing enormous outdoor screen, headlights off, warm summer night air heavy with humidity and distant crickets; foreground Tim (19yo tall athletic 6'3" lean white man, ginger neat medium-short hair, clean-shaven handsome sharp features deep-set blue eyes, tight white T-shirt with sunglasses hooked on collar, tense worried expression) sandwiched in back seat, flanked left by Alice Parker (18yo petite slim 5'2" pale white girl heavy freckles nose/cheeks, medium-long light brown soft waves to shoulders, expressive round grey eyes soft youthful cheeks dreamy gaze, baby-blue sleeveless cotton sundress white socks white Keds) hugging his left arm tightly eyes wide peering out, right by Cindy MacAllister (18yo slim athletic 5'5" white girl bright blue eyes shoulder-length blonde curled hair tanned youthful skin warm sad smile, stunning coral dress); front seat Eleanore ("Poppy") (slim pale 5'6" 18-19yo white girl sharp angular high cheekbones dark short bob hair aloof tense expression gripping dashboard like captain) in all-black cigarette pants turtleneck sunglasses flats, Barry MacAllister Jr. ("Bear") (20yo slight soft 5'8" bulky white man short blonde/light-brown hair boyish clean-shaven earnest sweaty forehead) driving disheveled oversized brown suit tie loosened hands light on wheel whispering "Play innocent."

Through open passenger-side windows, nearest cars reveal grieving fans: teenage white boy red-nosed wiping eyes, girl sobbing into handkerchief; next back seat three hugging teen girls; older lone white man blowing nose; consoling couple "Maybe it's a hoax"; all illuminated silvery blue-white glow from massive screen dominating background showing gigantic brooding young Elvis Presley (black-and-white Jailhouse Rock, hairline cropped by Chevy roof, in jail cell dreaming freedom, thumbs in pockets fancy suit); speaker posts with stretched wires to car windows tinny audio faint, cars facing screen haphazardly parked immense lot perimeter mounds, subtle Jim Crow tension in mixed caravan fringes Black figures distant hugging.

Uneven diegetic lighting: harsh silvery screen spill casting long shadows inside Chevy on faces/sundresses/suit, faint dashboard glow warm yellow, deep indigo night sky hazy stars no moon, headlights off stealthy; heavy Ektachrome grain desaturated reds/blues faded vibrancy yellowed edges dust specks scratches attic-found snapshot imperfections motion blur handheld tilt off-center framing candid unstaged realism sweat-glistened skin imperfect focus foreground figures slightly sharper background blurred crowds.

Era details: '50s Chevys Fords Plymouths chrome bumpers tailfins, no modern cars, Buzz Cigarette packs visible dashboards, Moon Pie wrappers seats, segregated undertone white teens central Black caravan members peripheral hugging, oppressive summer heat haze breath visible, emotional grief raw whispering "God are they all crying" innocent tension play, Elvis looming ghostly kingly tragic post-death aura, single-source screen light uneven pools deep shadows obscured edges no fill.

Amateur 35mm snapshot style: vignette curvature grain prominent low-light intensified slight shake varied poses natural orientations Tim turning peering Alice hugging Cindy leaning Eleanore forward Barry glancing mirror, relationships via spacing hugs tension, no posed perfection bokeh distortion LED bloom.
[Timestamp: 2026/04/26 18:32:46]

**user**: combine this prompt and the following prompt:
Transform the provided portrait photo into an authentic old amateur snapshot from a mid-20th-century family album.

Preserve the person’s identity, approximate pose, expression, and clothing category from the input image, but fully restyle the image so it feels like a real old physical photograph, not a modern portrait with a vintage filter.

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
[Timestamp: 2026/04/26 18:45:53]

**ai**: Photorealistic 1958 alt-history U.S. South scene on aged Ektachrome 35mm print transformed into authentic old amateur snapshot from mid-20th-century family album (warm yellow-brown monochrome staining, faded muddy tonality weak blacks creamy highlights compressed dynamic range, uneven discoloration faint density shifts subtle fading), somber grief-stricken night drive-in infiltration as casual household snapshot not professional portrait, Tim's POV peering through Barry's '57 Chevy Bel Air window at crying Elvis fans during Hitching Post Drive-In screening of Jailhouse Rock post-death radio news shock rippling through parked cars, imperfect focus slight hand-shake blur cheap lens softness overall no sharp modern details facial features recognizable but softened no crisp eyelashes hyper-detailed skin tack-sharp edges.

Inside dimly lit '57 Chevy Bel Air gliding silently between rows of parked '50s sedans coupes facing enormous outdoor screen headlights off warm summer night air heavy humidity distant crickets; foreground Tim (19yo tall athletic 6'3" lean white man ginger neat medium-short hair clean-shaven handsome sharp features deep-set blue eyes tight white T-shirt sunglasses hooked collar tense worried expression) sandwiched back seat flanked left Alice Parker (18yo petite slim 5'2" pale white girl heavy freckles nose/cheeks medium-long light brown soft waves shoulders expressive round grey eyes soft youthful cheeks dreamy gaze baby-blue sleeveless cotton sundress white socks white Keds) hugging left arm tightly eyes wide peering out right Cindy MacAllister (18yo slim athletic 5'5" white girl bright blue eyes shoulder-length blonde curled hair tanned youthful skin warm sad smile stunning coral dress); front seat Eleanore (slim pale 5'6" 18-19yo white girl sharp angular high cheekbones dark short bob hair aloof tense expression gripping dashboard like captain) all-black cigarette pants turtleneck sunglasses flats Barry MacAllister Jr. (20yo slight soft 5'8" bulky white man short blonde/light-brown hair boyish clean-shaven earnest sweaty forehead) driving disheveled oversized brown suit tie loosened hands light wheel whispering "Play innocent" slightly off-center awkward framing too much headroom incidental ordinary background.

Through open passenger-side windows nearest cars reveal grieving fans: teenage white boy red-nosed wiping eyes girl sobbing handkerchief next back seat three hugging teen girls older lone white man blowing nose consoling couple "Maybe hoax" all silvery blue-white glow massive screen background gigantic brooding young Elvis Presley (black-white Jailhouse Rock hairline cropped Chevy roof jail cell dreaming freedom thumbs pockets fancy suit) speaker posts stretched wires car windows tinny audio faint cars facing screen haphazard immense lot perimeter mounds subtle Jim Crow tension mixed caravan fringes Black figures distant hugging; visible analog grain print texture low-level blur exposure imperfections slight vignetting edge darkening tiny dust specks faint scratches minor surface wear optional scanner artifacts uneven flatness mild paper glare tonal inconsistency.

Uneven diegetic lighting harsh silvery screen spill long shadows inside Chevy faces/sundresses/suit faint dashboard glow warm yellow deep indigo night sky hazy stars no moon headlights off stealthy heavy grain desaturated faded vibrancy yellowed edges dust specks scratches attic-found snapshot imperfections motion blur handheld tilt candid unstaged realism sweat-glistened skin softened; era details '50s Chevys Fords Plymouths chrome bumpers tailfins no modern cars Buzz Cigarette packs dashboards Moon Pie wrappers seats segregated undertone white teens central Black peripheral hugging oppressive summer heat haze breath visible emotional grief raw whispering "God are they all crying" innocent tension Elvis looming ghostly kingly tragic post-death aura single-source screen light uneven pools deep shadows obscured edges no fill modern editorial cinematic grading clean studio lighting glossy finish polished retouching high contrast.

Amateur snapshot style thick aged photo border yellowed irregular wear deckled scalloped paper edges one+ sides print real object album not clean digital frame vignette curvature grain prominent low-light intensified slight shake varied poses natural orientations Tim turning peering Alice hugging Cindy leaning Eleanore forward Barry glancing mirror relationships spacing hugs tension no posed perfection bokeh distortion LED bloom perfectly centered carefully composed crisp DSLR detail fake Instagram vintage filter clean white border straight digital edges high-resolution clarity.
[Timestamp: 2026/04/26 18:46:24]