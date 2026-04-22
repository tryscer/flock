---
copilot-command-context-menu-enabled: true
copilot-command-slash-enabled: true
copilot-command-context-menu-order: 1080
copilot-command-model-key: ""
copilot-command-last-used: 1776687734733
---
Create a file called `chapter-guide.md` that serves as a first-pass retrieval layer for the manuscript in {Flock Music}.

The client of this file is an LLM. Its job is to answer questions about the manuscript without loading chapter prose unless necessary, and when prose is needed, to identify the smallest relevant set of chapters to load.

Use [[index]] to determine the exact chapter order.  
For each chapter linked from [[index]], read the full chapter prose and write a compact synopsis that preserves the facts most useful for retrieval, continuity tracking, and chapter identification.

Each chapter entry must use this exact format:

```md
[[Chapter Title]]

[60–150 word synopsis paragraph]
```
Use the exact chapter title from [[index]] and preserve the wiki-link syntax exactly.
Objective
Each synopsis must preserve enough factual information to allow an LLM to determine:
what happens in the chapter
what changes by the end of the chapter
what facts uniquely identify the chapter
whether the chapter prose needs to be loaded to answer a future query
The synopsis must be compact, accurate, and retrieval-oriented.
Workflow
For each chapter:
read the full chapter prose
identify the retrieval-critical facts established in that chapter
rank those facts by retrieval value
compress the chapter into one dense paragraph of 60–150 words
preserve the facts needed for retrieval and continuity
remove details that do not materially improve retrieval precision
This is not a prose summary.
It is a retrieval artifact.
Retrieval-Critical Facts
Prioritize facts that improve one or more of the following:
chapter identification
continuity tracking
semantic retrieval
Highest priority:
events that change the story state
revelations or newly known information
decisions, commitments, or plan changes
relationship changes
new risks, conflicts, or objectives
facts explicitly referenced later
facts recorded in the chapter YAML frontmatter
chapter-specific anchors that uniquely identify the chapter
Lowest priority:
atmosphere
jokes
scenic movement
repetitive beats
dialogue flavor
descriptive detail with no later consequence
incidental action that does not alter the story state
Only include low-priority details if removing them would make the chapter harder to distinguish from nearby chapters.
Each synopsis must preserve at least one unique retrieval anchor that distinguishes the chapter from adjacent chapters.

Accuracy Rules
Remain strictly faithful to the chapter prose.
Only record what the chapter explicitly establishes.

Do not infer:

motives
thematic meaning
implied significance
emotional interpretation
unstated causality
Do not describe one event as causing another unless the causal relationship is explicit or unambiguous in the prose.
If causality is uncertain, report the sequence without asserting cause.

Prefer:

Alice confronts Barry after finding the letter. Police arrive during the confrontation.
Not:
Alice’s confrontation causes the police to arrive.
Preserve:
the concrete events that occur
the explicit outcomes of those events
the factual state changes true by the end of the chapter
State changes must be concrete and verifiable:
a secret is revealed
a decision is made
a relationship changes
an alliance forms or breaks
an objective changes
a new threat appears
a location is gained or lost
If later chapters explicitly depend on a fact, preserve that fact.
Do not preserve details merely because they recur later.
Compression Rules
Use dense factual compression.
Compress by:

combining related events
removing redundant setup
removing beat-level narration
preserving outcomes instead of incidental sequencing
Do not compress by abstraction.
Good:

Cindy reveals she plans to run away, and Barry agrees to keep pursuing the band instead of taking the group home.
Bad:
The group becomes more committed to the journey.
The bad example loses retrieval value because it replaces concrete developments with abstraction.
Maintain:

concrete names
concrete actions
concrete outcomes
concrete state changes
Use:
present tense
neutral factual prose
plain declarative statements
maximum information density
Avoid:
thematic framing
dramatic commentary
evaluative language
editorial phrasing
Never include phrases like:
“this chapter reveals”
“the stakes rise”
“the tension deepens”
“this marks a turning point”
“the consequences are irreversible”
Do not explain why the chapter matters.
Do not summarize thematic significance.
Only record what happens and what becomes true.
Word Budget Rules
Each synopsis must be 60–150 words.
If the chapter exceeds the word budget, remove information in this order:

descriptive detail
incidental beats
secondary identifiers
non-essential supporting facts
Never remove:
state changes
decisions
revelations
chapter-unique retrieval anchors
facts needed for continuity
Compression must preserve retrieval value, not merely reduce word count.
Output Rules
Preserve the order from [[index]] exactly.
Output only the completed chapter-guide.md content.

Do not output:

explanations
headings
labels
commentary
markdown fences
metadata
Output only repeated chapter entries in this format:
> 
> [[Chapter Title]]
> [Synopsis paragraph]