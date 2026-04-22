---
copilot-command-context-menu-enabled: true
copilot-command-slash-enabled: true
copilot-command-context-menu-order: 1080
copilot-command-model-key: ""
copilot-command-last-used: 1776695988706
---
You are generating YAML frontmatter metadata for a chapter in a fiction manuscript.

Read the chapter text: {} and output **only** a YAML block.

The YAML must contain exactly three top-level keys:
- POV
- changes
- entities

Do not output any prose, explanation, or commentary outside the YAML block.

## POV
`POV` identifies who narrates or focalizes the chapter.

Rules:
- use the character’s name if the chapter has a clear narrator or focal character
- use a concise value
- if the chapter is clearly split between two narrators or focalizers, use a short list
- if no valid chapter text is provided, return `POV: unknown`

Good:
- POV: Alice
- POV: Tim
- POV:
  - Alice
  - Tim

## changes
`changes` is a short list of 1-7 major story-state changes introduced by the chapter.

These should capture the most important central developments that alter:
- relationships
- group direction
- stakes
- membership
- reader knowledge
- character knowledge
- social status
- physical status
- plans
- who is traveling with whom
- who belongs where
- if a named character is first introduced in this chapter

A change should be something that would matter in a chapter recap, continuity check, beat-matching task, or “what changed here?” query.

Each item must:
- be written as a concise factual statement
- describe a meaningful before/after shift
- be specific and retrievable
- avoid interpretation

Prefer:
- Alice and Tim sleep together
- The group decides to keep following the Steam Pillars
- Cindy dies
- The caravan grows dramatically
- Tim becomes useful to the band backstage
- Alice spreads palm-pressing as a shared mourning gesture
- Police pressure forces the show to end
- Eddie joins the travelers
- The crowd becomes a flock

Avoid:
- The chapter raises the stakes
- Their bond deepens
- Music changes everything
- Tension intensifies
- A sense of belonging emerges

Do not use `changes` for minor beats or scene texture. Only include major shifts. If there are more than 3, choose the most consequential.
## entities
`entities` is a lean index of concrete retrieval anchors appearing in the chapter.

Always include these four categories:
- characters
- locations
- groups
- ideas

Include only items that your predict will improve retrieval, continuity checking, or chapter matching.

### characters
Named people who appear in person and matter to retrieval.

### locations
Specific named place or places where the plot of the chapter takes place. Include venues, buildings, towns, roads, stages, homes, and vehicles used as active settings. Do not include referenced locations that the plot doesn't take place in. 

Include:
- Larry's Juke Joint
- US-360
- Barry's Chevy Bel Air
- Alice's parents' home

Do not include unnamed generic places such as:
- a wooden bridge
- a picnic table
- the woods


### groups
Named bands, institutions, companies, agencies, fan organizations, flocks, or other social bodies with retrieval value.

### ideas
Concrete in-world social technologies, rituals, repeatable gestures, contagious behaviors, shared scripts, active concepts, crowd effects, or named/repeated interpersonal formulas that characters use, perform, transmit, or recognize.

Include only ideas with clear in-world function and retrieval value.

Good:
- hand-pressing gesture
- palm-pressing after Elvis's death
- Love (capital-L concept)
- automatic dancing
- "morning, gorgeous"
- "maybe we'll dance again later"
- fan clubs becoming flocks

Bad:
- freedom
- racism
- longing
- youth rebellion
- music as transcendence

Do not include themes, motifs, moods, symbols, ideology, or abstract interpretation anywhere in the output.

Keep the metadata lean. Prefer precision over completeness. If an item is unlikely to help answer a future retrieval question, omit it.

## Output
Return a YAML frontmatter block. If no valid chapter text is provided, return:

```yaml
---
POV: unknown
changes: []
plot_points: []
entities:
  characters: []
  locations: []
  groups: []
  ideas: []
---
```
