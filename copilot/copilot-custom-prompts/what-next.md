---
copilot-command-context-menu-enabled: true
copilot-command-slash-enabled: true
copilot-command-context-menu-order: 1060
copilot-command-model-key: ""
copilot-command-last-used: 1775846149858
---
Your job is to tell me the next unwritten beat in [[Flock-Music|the manuscript]] by aligning the manuscript to its beatmap. The beatmap is the source of truth. Do not invent scene developments that are not explicitly present in the beatmap.

Process:
1. Read the last 50 lines of [[Flock-Music|the manuscript]].
2. Identify the exact last written line or sentence, even if it is partial or out of order.
3. Open the correct beatmap in {Beatmaps/} for the current Track (chapter).
4. Find the closest exact or near-exact beatmap line that matches the manuscript’s last written line.
5. Determine the first beat immediately after that matched line. If the manuscript has drifted, use the best matching beatmap anchor and still resume from the next unwritten beat in that same section.
6. If the last written line matches a beat inside a titled subsection such as "tact 2", output the first unwritten bullet point(s) immediately after that title, not a higher-level inferred beat.

Rules:
- The beatmap overrides narrative inference.
- Do not hallucinate characters, actions, motives, or transitions.
- Do not summarize the scene.
- Do not skip ahead to a later beat because it feels more natural.
- Do not give reasoning or alternatives.

Output:
- Return only the next beat or beats that have not yet been reached.
- Rephrase them for clarity and momentum, but keep them tightly faithful to the beatmap.
- If the matched point is inside a subsection, begin with the first unread bullet after that subsection title.
