---
copilot-command-context-menu-enabled: true
copilot-command-slash-enabled: true
copilot-command-context-menu-order: 1060
copilot-command-model-key: ""
copilot-command-last-used: 1776017599941
---
Your job is to tell me the next unwritten beat I should write in [[Flock Music|the manuscript]] by aligning the manuscript to its beatmap. 

Process:
1. Identify the exact last written line or sentence in [[Flock Music]] even if it is partial or out of order.
2. Each Track (chapter) has its own beatmap file in the directory {Beatmaps}. For example, the track 6 beatmap is in [[Chapter 6 Beatmap]]. Determine which Track I'm writing and open the corresponding beatmap file. 
3. Find the closest exact or near-exact beatmap line that matches the manuscript’s last written line.
4. Determine the first beat immediately after that matched line. If the manuscript has drifted, use the best matching beatmap anchor and still resume from the next unwritten beat in that same section.
5. If the last written line matches a beat inside a titled subsection such as "tact 2", output the first unwritten bullet point(s) immediately after that title, not a higher-level inferred beat.

Rules:
- The beatmap overrides narrative inference. 
- Do not hallucinate characters, actions, motives, or transitions.
- Do not summarize the scene.
- Do not skip ahead to a later beat because it feels more natural.
- Do not give reasoning or alternatives.
- Return only the next beat or beats that have not yet been reached.
- Rephrase them for clarity and momentum, but keep them tightly faithful to the beatmap.
- If the matched point is inside a subsection, begin with the first unread bullet after that subsection title.

OUTPUT FORMAT
You're on Track 6. The last beat written is "Ruminating Tim says this is the moment the pillars exploded, mentioning Atlanta. ״there was no stopping after that.""
The next beat is: 
on the road, later, they discover the vigilanties follow them. 