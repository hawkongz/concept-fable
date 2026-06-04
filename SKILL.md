---
name: concept-fable
description: Trigger when users say "explain with a story," "tell me a fable," "give me an analogy," "ELI5," or "help me understand intuitively" about a concept. Uses fables to illuminate abstract concepts — the story never mentions the term, only revealing it at the end.
---

# Concept Fable Explainer

## Overview

When a user wants to understand an abstract concept, don't throw a textbook definition at them. Instead, craft a carefully designed fable. The reader becomes immersed, only realizing near the end what it's about — then receives a clear explanation.

Core principle: **Let them *realize* through story, not *remember* through definition.**

## Workflow

Follow these 8 steps:

### Step 1 — Understand the Concept

1. If you fully grasp the concept, proceed directly to the next step.
2. If anything is unclear, search or consult authoritative sources.
3. Distill **2–3 core elements**: the central tension, the key mechanism, and why it matters.
4. Map out the concept's **causal chain** — a step-by-step breakdown of how the concept actually works: what triggers what, in what order, leading to what outcome. This is the plot-level blueprint: your story must reproduce this exact sequence, not just graze the theme.

> **Relationship between core elements and metaphor points**: Every core element must have a corresponding metaphor point that maps to it (this is the minimum). Additional metaphor points (3–5 total, including the ≥2 core mappings) enrich the story's details, but must not overshadow the core mapping. In short: **Core elements: ≥2 must be mapped. Total metaphor points: 3–5**.

### Step 2 — Confirm Scope & Scene (As Needed)

Check with the user when:
- The concept has multiple branches or schools of thought (e.g., "consistency" means different things in different contexts)
- The concept has different interpretations across domains
- The user's phrasing is vague and could mean several things

Confirm understanding: "So this concept is essentially about ______, and the key insight is ______ — is that right?"

**Confirm scene preference** — assess the concept first, then decide whether to ask:

- **Everyday scenes can precisely map the core process** → Don't interrupt; use everyday scenes directly.
- **The concept is abstract and far from daily experience** → Ask briefly: "This concept is fairly abstract — what kind of work do you do or what did you study? I'll pick a scene you're familiar with, which makes it easier to grasp."
- **The concept is familiar, but the user's profession could provide a sharper metaphor** → Same as above, ask briefly.

### Step 3 — Choose Story Type & Tone

**Story type** — Choose based on the concept's core characteristics:

- **Concept involves two-party standoff / conflict** → Classic parable or fable
- **Concept is a gradual, cumulative process** → Everyday life
- **Concept is systemic behavior / emergent phenomenon** → Natural phenomena or mechanical devices
- **Concept's core is a "surface vs. reality" contrast** → Dialogue-driven or instructional format
- **Concept exists to solve a problem** (tool/solution type, e.g., Node.js, caching, dependency injection) → Before-and-after contrast: first show the struggle without it, then show the change with it

Selection criteria:
- The story's "conflict" or "twist" must precisely map to the concept's core tension.
- 2–3 characters, one core plotline.

**Narrative tone** — Choose based on the concept's emotional flavor:

| Emotional Flavor | Recommended Tone | Example Scenario |
|------------------|------------------|-----------------|
| Cautionary / warning (e.g., technical debt, deadlock) | Measured, slightly rueful | Campfire storyteller style, unhurried |
| Revealing / counterintuitive (e.g., leaky abstraction, survivorship bias) | Light, with a twist | Like telling a "guess what happened" story |
| Trade-off / dilemma (e.g., CAP theorem) | Neutral, impartial | Plain narration; let the reader decide |
| Mechanism / principle (e.g., dependency injection) | Everyday, down-to-earth | Casual, conversational — like explaining over coffee |

> **Simple concept exemption**: For foundational concepts like "what is a variable" or "what is a loop," default to an everyday conversational tone — no need to match every row in the table above. The table is primarily for complex or abstract concepts that need emotional guidance.

### Step 4 — Validate Metaphor Mapping (Before Writing)

Before writing a single word, verify that the chosen story type's conflict structure can faithfully reproduce the concept's causal chain from Step 1:

1. **Draft planned metaphor points**: List the 3–5 planned metaphor points. For each, identify which specific link in the causal chain it maps to.
2. **Causal chain coverage**: Every essential link in the causal chain must have a corresponding metaphor point. If any link has no counterpart → the story's conflict structure doesn't fit this concept. Go back to Step 3.
3. **Mechanism vs. theme check**: Does the story's conflict map to the actual causal *mechanism*, or just the outcome *theme*? "Two parties stuck" is a theme; "each party holds something the other needs while refusing to release their own" is a mechanism. If you've only captured the theme → go back to Step 3.
4. If all checks pass → proceed to Step 5 (Write the Story).

### Step 5 — Write the Story

**Three-act structure:**

1. **Setup (60%–70%)**: Introduce characters and an everyday scene, seemingly unrelated to the concept. The plot unfolds naturally, quietly planting echoes of the concept. Let the reader sink into the story without sensing that it's a lesson.
2. **Conflict emerges (20%–30%)**: A twist, conflict, or dilemma appears that precisely maps to the core problem the concept addresses. Attentive readers may begin to catch on.
3. **Reveal (10%)**: Close with "This is the concept we're exploring today — **[concept name]**." One sentence to connect the dots, then stop.

**Writing principles:**
- Write in English; keep the story to 200–500 words.
- Do NOT hint at the concept name too early — suspense is the core appeal.
- Characters must behave naturally and credibly; never twist their actions just to serve the metaphor.
- Metaphor points: 3–5 total (≥2 must map to core elements). Don't map every detail.
- The story must be engaging *first*; the lesson seeps in naturally.
- **Tool/solution concepts must contrast**: Show both "life without it" and "life with it" in the story — let the value emerge through the difference rather than stating it directly.
- The story's causal chain must align with the concept's operating mechanism: it's not enough to merely touch on the "theme" — the plot's "cause → effect → dilemma" must replicate the concept's core process. After writing, ask yourself: if I translated the plot diagram back into technical terms, would it reconstruct the concept's key steps? If not → the mapping isn't tight enough.

**Metaphor Concreteness Principle (hard requirement):**

The metaphor vehicle must be something the reader can directly perceive in daily life. It must pass the **Grandma Test**:

> Can your grandma understand, in one sentence, what the metaphor vehicle is?
> Yes → use it. No → swap it out.

- ✅ Cooking, driving, moving house, waiting in line, picking up a package, fixing a leaky pipe, checking out at the grocery store, assembling IKEA furniture, untangling headphones...
- ❌ Magic runes, fantasy power-leveling systems, quantum entanglement, fourth-dimensional space, cyber-realms... (the reader has to decode the metaphor itself, defeating the purpose)
- The key test: the purpose of a metaphor is to *lower* the barrier to understanding. If the metaphor is harder to understand than the concept, you've defeated the purpose.

### Step 6 — Append Professional Explanation

```
---

## Explanation

### [Concept Name]

**One-sentence definition:** [Concise summary]

**Why this concept matters:** [1–2 sentences on practical significance]

**Key points:**
1. [What it is]
2. [Why it occurs / why it works this way]
3. [How to handle / apply it]

**Story-to-concept mapping:**
| Story Element | Concept Mapping |
|---------------|-----------------|
| [Character/Event] | [Concept element] |
| [Turning point] | [Core mechanism] |

**Prerequisite knowledge:** [If the explanation uses terms the reader might be unfamiliar with (e.g., using "bandwidth" to explain network latency, briefly explain bandwidth here in 1–2 sentences). Omit this line if not needed.]

**Food for thought:** [1–2 sentences to spark reflection]

**Story continuation (optional):** [If the concept has a naturally closely related concept (e.g., deadlock → deadlock prevention, npm → dependency hell), continue the story in 2–3 sentences to introduce the related concept. Give only a one-sentence definition, no full explanation template. End with "Want me to expand on this one?" Skip if no closely related concept exists.]
```

After completing the main explanation, **proactively check** whether a closely related concept exists (problem → solution, tool → common pitfall, phenomenon → adjacent phenomenon). If one does, don't skip the story continuation — it's one of the skill's most effective hooks.

Continuation constraints:
- Reuse the original story's characters and setting; you may introduce a new character to advance the plot, but don't elaborate on their background or motivations.
- Related concept gets only a one-sentence definition, no full explanation template.
- "Closely related" means: problem → solution, tool → common pitfall, phenomenon → adjacent phenomenon.
- If the user wants expansion → return to Step 1 and run the full workflow for the related concept separately.

### Step 7 — Self-Check

After writing the story, review the story against each item. **Rewrite at most 2 times.** If it still doesn't pass, output the current best version and honestly tell the user what you're not satisfied with:

1. **Character believability**: If you removed the concept, would the characters' actions still make sense within the story's logic? If a character does something implausible just to serve the metaphor → rewrite.
2. **Metaphor accuracy**: Does the story's core conflict map to the concept's **core tension** (not a peripheral feature)? Reconfirm: did the actual writing faithfully reproduce the mapping validated in Step 4, or did it drift during drafting? If a reader understands the story but not the concept → the metaphor missed.
3. **Story independence**: Setting the concept aside, is this story engaging and readable on its own? If it reads like "a textbook disguised as a story" → rewrite.
4. **Reveal timing**: Does the concept name only appear after the story's natural conclusion? If it shows up at the beginning or mid-story → too early.
5. **Conciseness**: Metaphor points 3–5? (≥2 must map to core elements.) Any redundant plot points you can cut?
6. **Concreteness**: Does the metaphor vehicle pass the Grandma Test? If the vehicle itself requires explanation (magic systems, fantasy world-building, sci-fi settings) → swap for everyday scenes.
7. **No unexplained jargon**: Does the explanation introduce new terms the reader might not know? If so → briefly explain them in 1–2 sentences at the end of the explanation.

### Step 8 — Output

- By default, output the story and explanation directly in the conversation.
- After output, ask briefly: "Did that make sense? If something's unclear, or you'd like a different scenario, let me know."
- If the user asks to save, write to `concept-fable-{concept-name}.md`.

---

## Post-Processing (Triggers After Output)

### Handling User Feedback

The following logic triggers after the user gives feedback on the output, not as part of the workflow steps:

1. **"The metaphor isn't quite right"** → Return to Step 1. Reconfirm whether the concept's core tension was understood correctly, then adjust the metaphor mapping.
2. **"This story doesn't work / try another"** → Return to Step 3. Switch to a different story type and tone, then rewrite.
3. **"Too subtle / too obvious"** → Adjust the reveal timing in the three-act structure, or increase/decrease the amount of setup.
4. **"Story too long / too short"** → Adjust the level of detail in the setup section without changing the core structure.

---

## Pre-Judgment (Triggers Before Writing)

### Handling Multi-Concept Requests

The following logic fires before writing begins, to decide the story strategy:

- **Concepts have a contrast/comparison relationship** → You can use one story to thread both concepts (e.g., two characters each embodying concept A and B, with different outcomes showing the contrast), but still reveal them separately at the end.
- **Concepts are unrelated** → Suggest two separate stories
- **Unsure** → Ask the user first: "Should I use one story to contrast these two concepts, or tell two separate stories?"

---

## Anti-Patterns: Avoid These

These are common failure modes. Actively avoid them while writing:

| Anti-Pattern | What It Looks Like | Why It Fails | The Fix |
|-------------|-------------------|-------------|---------|
| **Puppet characters** | Characters do things against their own nature to serve the metaphor | The reader feels the characters are "unreal," and the story collapses | First conceive the character's plausible motivation, then find the coincidental resemblance to the concept — not the reverse |
| **Over-metaphoring** | Every detail maps to the concept; the story reads like a cipher | Becomes a textbook in disguise, loses all charm | Only map the core elements; let the remaining details serve the story's vividness |
| **Premature reveal** | "This is like concept X" said at the beginning or mid-story | Kills the suspense; the reader stops "realizing" on their own | Hold back — let the story reach its natural conclusion. The reveal belongs only at the end. |
| **Hollow story** | The story has no conflict, no tension | The reader won't remember it — no emotion, no memory | Ensure there's a clear dilemma, choice, or twist. Make the reader care about the characters. |
| ⚠️ **Concept distortion** | Twisting the concept's core meaning to make a better story | The most serious error — the reader learns an incorrect understanding | After writing, self-check: if a reader only read the story and not the explanation, would their understanding be correct? |
| ⚠️ **Metaphor more abstract than concept** | Using magic runes to explain leaky abstractions, or fantasy power-leveling systems to explain design patterns | The reader has to decode the metaphor itself first — the barrier isn't lowered, it's raised | Use the Grandma Test: swap the vehicle for everyday scenes (a universal remote, a translation app glitch) — ensure the vehicle itself requires no explanation |

## Fallback Strategies

If a concept genuinely doesn't suit the fable format (too abstract, no concrete equivalent), don't force it:

1. First, try to find the **most concrete facet** of the concept and write a story around that.
2. If there's truly no good story angle, switch to a "scene analogy" (a short metaphor rather than a full story). For example:

   > To explain "recursion": "Imagine you're standing between two mirrors. You see a reflection within a reflection within a reflection — each layer identical to the last, just smaller. But there's always a 'smallest you' at the deepest point. When light reaches there, the reflections start coming back layer by layer. That's recursion."

3. If the concept is too broad (e.g., "object-oriented programming"), suggest the user narrow it down (e.g., "encapsulation," "polymorphism").
4. **If you can't find a scene the user is familiar with**, be honest rather than forcing it. For example: "I'm struggling to find a scene you'd be familiar with for this concept — would it be okay if I used a more everyday scenario instead?" The user would rather accept a slightly less precise but natural story than sit through a forced, awkward analogy.

---

## Quality Criteria

Each maps to a specific check in Step 7:

| Criterion | How to Verify |
|-----------|--------------|
| **Story before concept** | Self-check #3: Is the story readable on its own? |
| **Subtle but not obscure** | Self-check #2: Is the core tension precisely mapped? Does the causal chain align with the operating mechanism? |
| **Accurate but not rigid** | Self-check #1: Do the characters behave naturally? |
| **Respect the reader's intelligence** | Self-check #4: Is the reveal timed right? |
| **One story, one concept** | Self-check #5: Any redundant metaphors or plot points? |
| **Metaphor lowers the barrier** | Self-check #6: Does the metaphor vehicle pass the Grandma Test? |
| **Explanation creates no new confusion** | Self-check #7: Are all new terms briefly explained? |
