---
copilot-command-context-menu-enabled: true
copilot-command-slash-enabled: true
copilot-command-context-menu-order: 1080
copilot-command-model-key: ""
copilot-command-last-used: 1777223699994
---
## illustrate

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