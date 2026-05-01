---
epoch: 1777219927146
modelKey: "copilot-plus-flash|copilot-plus"
topic: "Creating a Leaner Prompt"



tags:
  - copilot-conversation
---

**user**: this prompt and the files that go with it -- this whole thing is bloated beyond proportions and the results suffer. Please create @composer 1 a new prompt in the active note, {activeNote} that leads to [[project-facts]] and to 2 new files you will create, one for the characters and one for the style. do stop and ask questions instead of taking decisions by yourself. 
target result:
the most consistent and token friendly novel scene illustrator for my book. 
[Context: Notes: Canon/project-facts.md, copilot/copilot-custom-prompts/illustrate.md]
[Timestamp: 2026/04/26 19:12:07]

**ai**: Agreed. The current [[illustrate]] prompt is trying to be prompt, canon router, style bible, consistency checklist, and post-processing recipe all at once. That’s exactly how you get token bloat and worse outputs.

Before I rewrite anything, I need these decisions from you:

- 1) Where should the two new support files live?
  - A. In `copilot/copilot-custom-prompts/`
  - B. In `Canon/photo-rules/`
  - C. Split: prompt in `copilot/...`, support files in `Canon/...`

- 2) Should the new illustrator reference only three notes:
  - `[[project-facts]]`
  - one new character file
  - one new style file  
  Or do you also want `[[chapter-guide]]` kept in the loop for scene parsing?
  
  My pushback: cutting [[chapter-guide]] saves tokens, but it also removes the cleanest way to resolve scene/location/POV when your input is shorthand like “Track 11 kiss” instead of a full scene brief.

- 3) What should the default visual mode be?
  - A. Amateur attic-found snapshot
  - B. Clean photorealistic period still
  - C. Neutral default, with optional style override when requested

  My recommendation for consistency + flexibility: C.

- 4) What belongs in the character file?
  - A. Only core recurring characters
  - B. Core cast + Steam Pillars + a few frequent secondary figures
  - C. Everyone currently used for image prompting

  My recommendation: B. C will bloat again.

- 5) When the user’s scene description is underspecified, what should the prompt do?
  - A. Ask 1–3 short questions before generating
  - B. Infer from canon silently
  - C. Infer from canon unless identity/composition is ambiguous, then ask

  My recommendation: C.

- 6) Do you want the new system to preserve the “output only the final image prompt text” behavior?
  - Yes
  - No, let it ask clarifying questions in normal chat first

  Important: this is the main design fork. If you want the illustrator itself to ask questions, the active note cannot be “final prompt only” in all cases.

- 7) Naming:
  - character file: what title/path do you want?
  - style file: what title/path do you want?

If you want, you can answer in a compact form like:

- 1C
- 2 = keep / remove [[chapter-guide]]
- 3C
- 4B
- 5C
- 6 = yes / no
- 7 = `[[...]]`, `[[...]]`

My strong recommendation for the leanest good version is:

- `illustrate.md` = tiny orchestrator
- one compact `characters` note = identity locks only
- one compact `style` note = visual grammar, negatives, era rules
- keep [[project-facts]] mandatory
- keep [[chapter-guide]] only if you often prompt by track shorthand

Once you answer those, I’ll make the files and keep the whole thing deliberately small.

## Sources
- `copilot/copilot-custom-prompts/illustrate.md`
- [[project-facts]]
[Timestamp: 2026/04/26 19:15:30]

**user**: @composer 1. C 2. add chapter guide 3. only a 4. alice, tim, barry, cindy, eleanore, eddie, all the steam pillars, mama, rosetta the cigarette girl, pete, jimmy, mo, shirley. 5. c 6. yes
one more addition: the bottom margin of the photo should have an image description written in ballpoint pen, e.g., me and alice at the county fair 
[Timestamp: 2026/04/26 19:21:09]

**ai**: Good. Two decisions still need your sign-off before I edit anything.

- 1) Color or monochrome?
  
  Pushback: the current prompt says both “aged monochrome print” and “kodachrome,” which fight each other. That contradiction is part of the bloat/problem.
  
  Pick one:
  - A. Faded color snapshot
  - B. Monochrome snapshot

  My recommendation: A. It is more specific to 1958 amateur photo vernacular and will usually produce better consistency than fake “vintage black-and-white.”

- 2) Approve these exact support-note paths/titles?
  - `Canon/photo-rules/illustrate-characters.md` → `[[illustrate-characters]]`
  - `Canon/photo-rules/illustrate-style.md` → `[[illustrate-style]]`

If yes, I’ll make:
- a much smaller `copilot/copilot-custom-prompts/illustrate.md`
- one compact character-lock file with exactly: Alice, Tim, Barry, Cindy, Eleanore, Eddie, all Steam Pillars, Mama, Rosetta the cigarette girl, Pete, Jimmy, Mo, Shirley
- one compact style file centered on attic-found amateur snapshot logic, including the handwritten ballpoint caption on the bottom margin

One last implementation detail bundled into that style file unless you object:
- if the scene gives enough context, the bottom caption will be generated as a casual period note like “Me and Alice at the county fair”
- if not, it will stay short and generic rather than invent specifics

Reply with:
- `1A` or `1B`
- `2 yes` or `2 change to: ...`

## Sources
- `copilot/copilot-custom-prompts/illustrate.md`
[Timestamp: 2026/04/26 19:24:11]

**user**: 1. a
2 yes 
[Timestamp: 2026/04/26 19:24:46]

**ai**: I rebuilt it as three lean files. The main change is structural: [[illustrate]] is now just an orchestrator; consistency lives in [[illustrate-characters]] and [[illustrate-style]].

Notable restraint: I kept Eddie, Jimmy, and Mo deliberately sparse because stronger visual canon was not surfaced here. That is a feature, not a gap; guessed portrait detail is how these systems bloat and drift.

`copilot/copilot-custom-prompts/illustrate.md`
```md
---
copilot-command-context-menu-enabled: true
copilot-command-slash-enabled: true
copilot-command-context-menu-order: 1080
copilot-command-model-key: ""
---
## illustrate

Generate one photorealistic image prompt for this novel scene:

"{}"

If the scene is clear enough, output only the final image-generation prompt text.
If who is in frame, where the scene is, or what the main action is remains materially ambiguous, ask up to 3 short questions instead.

Internal rules:
- Use [[project-facts]] for world rules, alt-history constraints, social reality, and anachronism guardrails.
- Use [[chapter-guide]] only if {} refers to a track, chapter, or shorthand scene reference that needs resolving.
- Use [[illustrate-characters]] to keep recurring characters visually consistent.
- Use [[illustrate-style]] for visual mode, framing, lighting, physical print look, and border caption behavior.
- Infer quietly when possible. Ask only when ambiguity would materially change the image.
- Keep the final prompt lean: concrete visible details over abstract mood language.

Output target:
- exactly one dense copy-paste-ready image prompt
- photorealistic 1958 alt-history U.S. South scene
- faded color amateur family snapshot, not cinematic or editorial
- clear foreground / midground / background
- diegetic lighting only
- no modern elements
- include the physical photo print with an aged border and a handwritten ballpoint caption on the bottom margin matching the scene

Start exactly with:
Photorealistic 1958 alt-history U.S. South amateur attic-found faded color snapshot,
```

`Canon/photo-rules/illustrate-characters.md`
```md
# illustrate-characters

Use only stable visible anchors. Do not invent extra traits unless the scene requires them.

- Alice Parker — 17, white, petite, gray eyes, light hair with pink-tinted ends when shown; intense, curious, easy to pick out in a crowd.
- Tim — 19, white, taller than Alice, red-haired, lean; earnest, observant.
- Barry MacAllister Jr. — 20, white, Cindy’s older brother; solid, confident.
- Cindy MacAllister — 17, white, Alice’s best friend, Barry’s sister; neat teenage presentation.
- Eleanore — 19, white, Cindy’s cousin; street-smart, bossy, slightly older and more urban in presence.
- Eddie — Italian émigré; use scene text for specific styling.
- Heath Walker Cain — Jerry Lee Lewis undercover; render as Heath, not as a celebrity cameo.
- Vilma — Black Steam Pillars member; stage-poised.
- Besame Mucho — Black Steam Pillars member; bassist.
- Babatunde — Black Steam Pillars member; physically striking, rhythmic presence.
- Jo Dalton — Black Steam Pillars member; drummer.
- Mama Bettye Davis (“Mama”) — older Black woman; organizer’s authority, forceful calm.
- Rosetta the cigarette girl — young woman associated with a cigarette tray when relevant.
- Pete — Black young man; activist/fan energy.
- Jimmy — recurring young man; use scene text for specifics.
- Mo — recurring young man; use scene text for specifics.
- Shirley — young Black woman; strong presence, direct gaze.

Relationship anchors:
- Alice and Cindy should read as close teenage friends.
- Barry and Cindy are siblings.
- Tim is Barry’s best friend and Alice’s love interest.
- Eleanore reads slightly older than Alice and Cindy.
- Steam Pillars should read as a coherent band unit, not random performers.
- If Heath appears with Steam Pillars, keep him integrated into the group rather than spotlighted as a star.
```

`Canon/photo-rules/illustrate-style.md`
```md
# illustrate-style

Default mode: faded color amateur family snapshot from summer 1958, later found in an attic album.

Core look:
- faded color print, not monochrome
- soft focus, mild blur, visible grain
- weak contrast, creamy highlights, slightly muddy shadows
- casual, slightly awkward framing
- never polished, symmetrical, or editorial
- physical paper photo visible with an aged border and light wear

Lighting:
- diegetic light only: sun, porch bulb, neon, projector, headlights, fairground lamps, stage spill
- no studio light, no cinematic rim light, no artificial “movie” polish

Scene construction:
- build the image from foreground to background
- keep one dominant visible action
- use a few decisive period objects instead of long prop lists
- sweat, dust, smoke, haze, and motion softness are useful
- if the setting involves interracial public space, Jim Crow tension should be legible in bodies, spacing, signage, policing, or crowd behavior when relevant

Negatives:
- no modern color grading
- no glossy magazine finish
- no tack-sharp digital detail
- no fashion-shoot posing
- no modern props, cars, signage, hair styling, or clothing
- no generic “nostalgia” filter language

Bottom margin:
- always show a handwritten ballpoint-pen caption on the lower photo border
- the caption should be short, casual, and scene-specific, for example: me and alice at the county fair
- use lowercase or loose everyday handwriting, not elegant script
- if the scene is ambiguous, keep the caption generic rather than inventing plot facts
```

This should produce much more stable results because the system now has:
- one world/canon source: [[project-facts]]
- one navigation source: [[chapter-guide]]
- one identity-lock source: [[illustrate-characters]]
- one visual grammar source: [[illustrate-style]]

If you want, next pass I’d do one more cleanup move: strip any now-obsolete notes from `Canon/photo-rules/` so the illustrator stops competing with older portrait rules.

## Sources
- `copilot/copilot-custom-prompts/illustrate.md`
- [[project-facts]]
[Timestamp: 2026/04/26 19:33:08]

**user**: @composer you are approved to create / change the files 
[Timestamp: 2026/04/26 19:38:14]

**ai**: Files created and illustrate.md updated successfully.

The new system is now:
- [[illustrate]] (orchestrator, ~250 tokens)
- [[illustrate-characters]] (identity locks, ~400 tokens)
- [[illustrate-style]] (visual rules, ~350 tokens)

Total overhead slashed. Prompts will parse {} against these + [[project-facts]] + [[chapter-guide]] (if needed), infer where safe, ask if ambiguous, output clean faded-color snapshot text starting with the exact phrase.

Test vector: Input “Alice and Tim kiss at Yadkin River overlook Track 11”—should generate without questions, locking heights/poses/Jim Crow dusk, caption like “me + alice by the river.”

Next step if desired: Archive/delete old `section1_characters.md` etc. to prevent prompt bleed.

## Sources
- `copilot/copilot-custom-prompts/illustrate.md`
- `Canon/photo-rules/illustrate-characters.md`
- `Canon/photo-rules/illustrate-style.md`
- [[project-facts]]
[Timestamp: 2026/04/26 19:38:43]

**user**: not good -- the new prompt doesn't lock in the characters (I got "3 men in their 20s") 
[Timestamp: 2026/04/26 19:42:41]

**ai**: I've reached the time limit for reasoning. Here's what I found so far based on the search results.
[Timestamp: 2026/04/26 19:54:38]

**user**: ## illustrate

Generate one photorealistic image prompt for this novel scene:

"{}"

If the scene is clear enough, output only the final image-generation prompt text.
If who is in frame, where the scene is, or what the main action is remains materially ambiguous, ask up to 3 short questions instead.

Internal rules:
- Use [[project-facts]] for world rules, alt-history constraints, social reality, racial dynamics, and anachronism guardrails.
- Use [[chapter-guide]] whenever {} uses a track/chapter/shorthand reference, or when canon is needed to resolve who is present, where the scene happens, POV, time of day, or mood.
- Use [[illustrate-characters]] to lock recurring characters. Translate every named or canon-resolved character into explicit visible traits in the final prompt.
- Use [[illustrate-style]] for image grammar, physical print look, lighting, framing, and border-caption behavior.
- Never collapse named or canon-resolved characters into generic placeholders like "three men," "a woman," "young people," or "band members." If a principal is in frame, specify that person individually.
- For each principal in frame, state visible identity anchors: apparent age band, race, hair, height/build, clothing when known, and exact placement/action in the frame.
- If Steam Pillars are in frame, name and visually distinguish each visible member rather than summarizing them as a generic band.
- Keep the final prompt lean, but spend tokens on identity lock before atmosphere or props.
- Infer quietly when possible. Ask only when ambiguity would materially change the image.

Output target:
- exactly one dense copy-paste-ready image prompt
- photorealistic 1958 alt-history U.S. South scene
- faded color amateur family snapshot, not cinematic or editorial
- clear foreground / midground / background
- principal characters individually described and spatially placed
- diegetic lighting only
- no modern elements
- include the physical paper photo print with an aged border and a handwritten ballpoint caption on the bottom margin matching the scene

Start exactly with:
Photorealistic 1958 alt-history U.S. South amateur attic-found faded color snapshot, 
[Context: Notes: Canon/chapter-guide.md, Canon/photo-rules/illustrate-characters.md, Canon/photo-rules/illustrate-style.md, Canon/project-facts.md]
[Timestamp: 2026/04/26 20:15:00]

**ai**: - Which beat do you want illustrated from this excerpt: 1) Tim driving with Barry beside him and Cindy/Eleanore flanking Heath in the back seat on US-360, 2) the bikers boxing in Barry’s Chevy, 3) the reunion with Alice cross-legged in the back of the Steam Pillars truck beside Babatunde, or 4) Mama, Rosetta, Jimmy, and Jo writing matchbooks in the parking deck?
- Which principals must be visible in frame?
- Do you want a tight interior snapshot, a medium roadside action shot, or a wider group composition?

## Sources
- [[Track 8 - I Saw It Too]]
- [[chapter-guide]]
- [[illustrate-characters]]
- [[illustrate-style]]
[Timestamp: 2026/04/26 20:22:28]

**user**: 1 
[Timestamp: 2026/04/26 20:22:50]

**ai**: Photorealistic 1958 alt-history U.S. South amateur attic-found faded color snapshot, interior of Barry's '57 Chevy Bel Air on blazing-sunlit US-360 highway, Tim (19 white lean red-haired driver, earnest profile at wheel in foreground left, hands on steering), Barry MacAllister Jr. (20 white solid confident brother in passenger seat foreground right, looking ahead), back seat midground with Eleanore (19 white street-smart bossy cousin flanking left of Heath, urban poise) and Cindy MacAllister (17 white neat teenage sister flanking right of Heath, best-friend closeness to Alice vibe), center Heath Walker Cain (Black Steam Pillars pianist undercover, jet-black hair dark sunglasses cheap dark suit sad face big nose small pouting mouth lips moving in prayer to radio song eyes shut behind shades, hands clasped in lap); empty road stretching ahead through windshield, sun glare on dashboard and vinyl seats, sweat on faces, Jim Crow South highway isolation no other cars visible; soft focus mild blur visible grain weak contrast creamy highlights muddy shadows casual awkward framing diegetic harsh sunlight only through car windows no cinematic polish; physical aged paper photo print with light wear border, bottom margin handwritten ballpoint caption in loose lowercase: me barry cindy eleanore heath on 360
[Timestamp: 2026/04/27 07:24:20]