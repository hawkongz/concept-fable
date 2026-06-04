<div align="center">
  <h1>📖 Concept Fable</h1>
  <p>Understand any abstract concept through a carefully crafted fable — not by memorizing textbook definitions.</p>

  [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
  [![Platform](https://img.shields.io/badge/Platform-Claude%20Code-blue)](https://code.claude.com)
  [![Stars](https://img.shields.io/github/stars/hawkongz/concept-fable)](https://github.com/hawkongz/concept-fable)

  <p><strong>Language:</strong> <a href="README.md">English</a> | <a href="zh-CN/README.md">简体中文</a></p>
</div>

---

## 📋 Table of Contents

- [Background: Inspired by Amanda Askell](#background-inspired-by-amanda-askell)
- [What This Skill Does](#what-this-skill-does)
- [Features](#features)
- [Quick Start](#quick-start)
- [Usage Example](#usage-example)
- [Design Philosophy](#design-philosophy)
- [Topics](#topics)
- [Contributing](#contributing)
- [License](#license)

---

## Background: Inspired by Amanda Askell

**Amanda Askell** is Anthropic's in-house philosopher and head of the Character Alignment team. With a Ph.D. in philosophy from NYU, she is the principal author of Claude's Constitution — the 30,000-word document that shapes Claude's personality and moral compass.

In April 2026, during a podcast interview, Askell shared a small technique that quickly spread through the AI community:

> **"Ask Claude to write a fable that explains a concept — but never mention the concept's name."**

Her core insight is simple yet profound:

> *"Stories are the most fundamental learning vehicle for humans. Traditional learning tackles definitions head-on. Fables take the opposite path — you get immersed in an engaging story, and only at the very end do you realize what it was about. By then, you've already intuitively grasped the concept's essence."*

Askell herself uses this daily: *"When I'm bored, I ask Claude to tell me fables. Now I have all these little stories in my head, each one corresponding to a concept from some discipline. Sometimes I can't remember the concept's formal name anymore — but I still remember the story."*

**This skill takes her idea and expands it from a simple prompt into a complete, structured, reusable methodology.**

---

## What This Skill Does

Askell's original idea is a brilliant starting point, but in practice, raw prompts hit several walls:

- AI falls into formulaic narratives (traveler seeks wisdom, village epiphany, wise-mentor dialogues)
- The same tired imagery keeps appearing (rivers, clocks, mirrors, mountains, stars — over and over)
- Characters become puppets of the metaphor, sacrificing natural behavior for conceptual mapping
- Metaphors sometimes end up more abstract than the concept itself (explaining design patterns through elaborate fantasy world-building)

**Concept Fable** systematizes Askell's core idea into an **8-step workflow** with extensive anti-pattern detection and quality guardrails:

| Askell's Original Idea | This Skill's Systematic Expansion |
|:---|:---|
| Never mention the concept name | Step 5: Three-act structure with precise reveal-timing control |
| Let the story carry the meaning | Step 4: Causal-chain alignment check — verify metaphor points map to every link of the causal chain before writing; Step 5: the plot's "cause → effect → dilemma" must replicate the concept's operating mechanism |
| — | Step 3: Automatically matches story type to concept characteristics (rivalry → ancient fable / gradual → daily life / emergence → nature / surface vs. reality → dialogue / tool/solution → before-and-after contrast) |
| — | Step 3: Narrative tone matched to the concept's emotional flavor (cautionary / counterintuitive / trade-off / mechanistic) |
| — | Step 7: 7-point self-check — character believability, metaphor accuracy, story independence, reveal timing, conciseness, concreteness, no unexplained jargon |
| — | Anti-pattern table: 6 common failure modes with specific fixes |
| — | "Grandma Test" for metaphor concreteness: the vehicle must be something perceptible in daily life |
| — | Fallback strategies: 4 alternatives when a concept genuinely doesn't fit the fable format |

---

## Features

- **📚 8-Step Structured Workflow**: Understand concept → Confirm scope → Choose story type & tone → Validate metaphor mapping → Write fable → Append explanation → Self-check → Output
- **🎭 Automatic Story-Type Matching**: Selects the best fable genre based on the concept's core nature (rivalry, gradual emergence, surface-vs-reality contrast, tool/solution)
- **🎯 Causal-Chain Alignment**: Goes beyond thematic similarity — the plot's cause-and-effect must mirror the concept's actual mechanism
- **🔀 Before-and-After Contrast**: For concepts that exist to solve a problem (e.g., Node.js, caching), the story shows both "life without it" and "life with it," letting the value emerge through the difference
- **🧹 Anti-Pattern Guardrails**: Built-in avoidance of 6 failure modes: puppet characters, over-metaphoring, premature reveals, hollow stories, distorted concepts, and metaphors more abstract than the concept itself
- **👵 The Grandma Test**: A hard requirement that every metaphor vehicle must use everyday, tangible experiences (cooking, driving, queuing) — no abstract fantasy settings that themselves need decoding
- **✅ 7 Quality Self-Checks**: Systematic review after every story; maximum 2 rewrites; honestly report shortcomings if still not satisfied
- **🔄 Feedback Handling Loop**: Inaccurate metaphor? Wrong story type? Too subtle or too obvious? Too long or too short? — each feedback type maps to a specific adjustment strategy
- **📖 Standardized Explanation Template**: Unified output format with definition, story-to-concept mapping table, prerequisite knowledge notes, and further thinking prompts

---

## Quick Start

> **What you need:** Claude Code installed and running.

**Step 1 — Install the skill**

This skill requires only a single `SKILL.md` file to run (English version).

macOS / Linux:

```bash
mkdir -p ~/.claude/skills/concept-fable
curl -o ~/.claude/skills/concept-fable/SKILL.md https://raw.githubusercontent.com/hawkongz/concept-fable/main/SKILL.md
```

Windows (PowerShell):

```powershell
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.claude\skills\concept-fable"
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/hawkongz/concept-fable/main/SKILL.md" -OutFile "$env:USERPROFILE\.claude\skills\concept-fable\SKILL.md"
```

> **中文用户**：请下载中文版 —— 把上面 URL 中的 `main/SKILL.md` 换成 `main/zh-CN/SKILL.md`。

**Step 2 — Done.**

Restart Claude Code and the skill activates automatically. Try saying:

- "Explain deadlock with a story"
- "Tell me a fable about CAP theorem"
- "Help me understand dependency injection using an everyday scenario"

> To update: re-run the commands from Step 1.

---

## Usage Example

**Input:** "Explain what deadlock is with a story"

**Claude will:**
1. Confirm conceptual understanding (the four necessary conditions of deadlock, the core dilemma)
2. Select a story type (two-party standoff → ancient fable style)
3. Craft a fable that never mentions "deadlock"
4. Reveal the concept only at the story's natural conclusion
5. Append a professional explanation with a story-to-concept mapping table
6. Run the 7-point self-check, then output

The story might be: two wagons confronting each other on a narrow bridge, neither willing to yield, both stuck until nightfall — while there was clearly enough room for one to pass first.

---

## Design Philosophy

### Core Principle: Let them *realize* through story, not *remember* through definition

Traditional teaching follows the path: definition → explanation → example. The reader is a passive recipient.

The fable method reverses this: story → immersion → epiphany → reveal. The reader understands the core of the concept before they even know what they're "learning." The moment of revelation — "oh, *that's* what this was about" — creates an emotional anchor that makes the understanding far more durable than passive reception.

### Why It Works

1. **Narrative memory advantage**: Human brains retain stories far better than abstract definitions. Stories provide context, emotion, and causal chains.
2. **Understand first, name later**: The reader is already grasping the concept through the story; they just don't know its formal name yet. The "aha" moment at reveal is far stronger than being told upfront.
3. **Lowered cognitive barrier**: Everyday scenarios map to abstract concepts — the reader doesn't need to finish a textbook before understanding.

---

## Topics

[`claude-code`](https://github.com/topics/claude-code) [`skill`](https://github.com/topics/skill) [`prompt-engineering`](https://github.com/topics/prompt-engineering) [`fable`](https://github.com/topics/fable) [`storytelling`](https://github.com/topics/storytelling) [`education`](https://github.com/topics/education) [`learning`](https://github.com/topics/learning) [`concept-explanation`](https://github.com/topics/concept-explanation)

---

## Contributing

Contributions are welcome! If you have ideas for better story types, discover new anti-patterns, or have particularly successful fable examples, please submit an Issue or PR.

---

## License

MIT © [hawkongz](https://github.com/hawkongz)

---

> *"Sometimes I can't remember the concept's formal name anymore — but I still remember the story."* — Amanda Askell
