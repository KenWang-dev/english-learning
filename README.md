# Scene-Based English Learning Skill

> 场景英语学习系统 — 双向路由 · 帕累托聚焦 · 六维框架

A Claude Code skill that teaches English through **real-life scenes**, not textbooks. Every interaction produces a complete, usable dialogue set in a concrete situation — learn it, use it immediately.

## Core Idea

```
Traditional:  Word → Grammar → Sentence → ??? → Real usage (inefficient, broken chain)
This skill:   Scene → Sentence → Phrase → Word naturally acquired (efficient, closed loop)
```

### Four Priorities

| Higher Priority | Over |
|----------------|------|
| Scene | Isolated words |
| High-frequency | Low-frequency |
| Usable | Merely recognizable |
| Natural/idiomatic | Grammatically correct but stiff |

## How It Works

### Dual-Routing System

No matter what you input — a scene, a sentence, a phrase, or a single word — the skill routes you to the same destination: a **complete scene-based learning loop**.

**Top-Down (scene input):**
```
"Going to the movies" → MECE breakdown → 2-3 high-freq sentences per step → dialogue → archive
```

**Bottom-Up (word/phrase input):**
```
"splash" → top phrase: "a splash of" → top sentence → top scene: "coffee shop" → full dialogue → archive
```

Low-frequency inputs get intercepted with a brief definition and a redirect to high-frequency content.

### 6-Dimension Pipeline

| Dimension | Purpose |
|-----------|---------|
| D0 Archive Lookup | Check if scene already learned (save tokens) |
| D1 Input Parsing | Identify type, intent, user context |
| D2 Frequency Routing | Pareto filter + path decision |
| D3 Scene Modeling | MVP closed-loop + MECE breakdown |
| D4 Expression Extraction | High-freq sentences + key phrases |
| D5 Content Presentation | Genre, register, length control |
| D6 Iteration | Difficulty switch, synonyms, scene expansion |

### Three Difficulty Levels

| Level | Target |
|-------|--------|
| L1 Daily Basics | Survive daily life — simple sentences, common words |
| L2 Work Fluent | Function at work — professional vocab, compound sentences |
| L3 Native-Level | Impress native speakers — idioms, slang, flexible structures |

## Scene Archive System

Every learning output is saved to `learned-scenes/` as a reusable asset:

- **Token saving**: Hit an archived scene → load instantly, no regeneration
- **Spaced review**: Revisit archived scenes anytime
- **Iterative deepening**: Upgrade difficulty, swap expressions, extend scenes — all versions preserved
- **Personal textbook**: Accumulate enough scenes and you have your own curated English course

## Project Structure

```
english-learning/
├── skills/scene-english/
│   ├── SKILL.md                          # Skill instructions
│   └── references/
│       └── scene-english-framework.md    # Full 6D×3I framework (theory)
├── learned-scenes/                       # Your archived scenes (grows over time)
│   └── movie-night-at-the-cinema.md
├── SceneEnglish-Framework-v2.0.md        # Original framework document
└── README.md
```

## Installation

Copy the skill to your Claude Code project:

```bash
# Clone the repo
git clone https://github.com/KenWang-dev/english-learning.git

# Copy skill to your project's .claude/skills/
cp -r english-learning/skills/scene-english your-project/.claude/skills/
```

Or install globally:

```bash
cp -r english-learning/skills/scene-english ~/.claude/skills/
```

## Usage Examples

Just talk to Claude naturally:

| Input | Route | Result |
|-------|-------|--------|
| `在星巴克点咖啡` | Top-Down | Full coffee shop dialogue |
| `splash` | Bottom-Up | Traces to "a splash of" → coffee shop scene |
| `checkmate` | Low-freq intercept | Brief definition + redirect to high-freq content |
| `看电影` | Archive hit | Load saved scene, offer review/iterate/regenerate |

## Framework

This skill is built on the **Scene-Based English Learning Framework v2.0** — a structured methodology using:

- **First Principles** → full landscape mapping
- **MECE** → no-overlap, no-gap decomposition
- **Pareto** → focus on the 20% that covers 80% of real usage

See `SceneEnglish-Framework-v2.0.md` for the complete theory.

## License

MIT
