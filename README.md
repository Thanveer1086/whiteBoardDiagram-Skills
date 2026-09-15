# 🎨 Whiteboard Diagram Skill

> **A universal AI skill that teaches coding agents to generate professional hand-drawn whiteboard diagrams.**

Turn any idea into a beautiful, sketchy, hand-drawn whiteboard — like someone drew it with markers on a real whiteboard. Works with **Claude Code**, **Antigravity**, **Cursor**, **Windsurf**, **GitHub Copilot**, and any AI coding agent.

---

## ✨ What It Does

This skill instructs AI coding agents to generate **hand-drawn style diagrams** with:

- 🖊️ **Sketchy, imperfect borders** — organic, hand-drawn feel (not machine-perfect)
- 🎨 **Pastel color palettes** — 6 curated palettes with fill + border variants
- 🔢 **Numbered badges** — ① ② ③ for sequential stages
- 🎯 **Icons & emojis** — visual anchors for every section
- 📐 **7 layout patterns** — Pipeline Grid, Flow, Architecture Layers, Kanban, Mind Map, Comparison, Timeline
- ✍️ **Hand-drawn fonts** — Virgil, Comic Neue, Architect's Daughter
- 📤 **4 output formats** — Mermaid, SVG, Excalidraw JSON, HTML

---

## 🚀 Quick Start

### Just Tell Your Agent

After installing, simply ask your AI agent:

```
"Create a hand-drawn whiteboard showing our 5-stage content pipeline"
```

```
"Draw a sketchy architecture diagram of our microservice system"
```

```
"Make a whiteboard-style comparison chart of React vs Vue vs Svelte"
```

The agent will read the skill and generate a professional hand-drawn diagram.

---

## 📦 Installation

### Antigravity (Google)

Copy the skill folder to your global skills directory:

```bash
# Global (all projects)
cp -r whiteBoardDiagram-Skills/ ~/.gemini/config/skills/whiteboard-diagram/

# Project-level (this project only)
cp -r whiteBoardDiagram-Skills/ .agents/skills/whiteboard-diagram/
```

### Claude Code (Anthropic)

Copy to your Claude Code skills directory:

```bash
# Project-level
mkdir -p .claude/skills/whiteboard-diagram
cp SKILL.md .claude/skills/whiteboard-diagram/
cp CLAUDE.md ./CLAUDE.md  # or append to existing

# Global
mkdir -p ~/.claude/skills/whiteboard-diagram
cp SKILL.md ~/.claude/skills/whiteboard-diagram/
```

### Cursor

Copy the `.cursorrules` file to your project root:

```bash
cp .cursorrules /path/to/your/project/.cursorrules
# Or for modern Cursor Rules 2.0:
mkdir -p /path/to/your/project/.cursor/rules
cp SKILL.md /path/to/your/project/.cursor/rules/whiteboard-diagram.mdc
```

### Windsurf / Codeium

Copy the `.windsurfrules` file to your project root:

```bash
cp .windsurfrules /path/to/your/project/.windsurfrules
# Or for modern Windsurf rules:
mkdir -p /path/to/your/project/.windsurf/rules
cp SKILL.md /path/to/your/project/.windsurf/rules/whiteboard-diagram.md
```

### GitHub Copilot

Copy the instructions file to your `.github/` directory:

```bash
mkdir -p /path/to/your/project/.github
cp .github/copilot-instructions.md /path/to/your/project/.github/copilot-instructions.md
```

### Any Other Agent

Copy the content of `SKILL.md` into your agent's system prompt or instruction file. The skill is written in plain Markdown — it works anywhere.

---

## 🎯 Output Formats

| Format | Best For | Works In |
|--------|----------|----------|
| **Mermaid** (default) | Docs, README, quick diagrams | GitHub, VS Code, any markdown renderer |
| **SVG** | Standalone images, print | Any browser, image editors |
| **Excalidraw JSON** | Editable, collaborative boards | [excalidraw.com](https://excalidraw.com), VS Code extension |
| **HTML** | Interactive, animated boards | Any web browser |

### Output Decision Tree

```
Need a diagram → For docs/markdown?
                  ├─ YES → Mermaid (hand-drawn mode)  ← DEFAULT
                  └─ NO → Editable?
                           ├─ YES → Excalidraw JSON
                           └─ NO → Interactive?
                                    ├─ YES → HTML
                                    └─ NO → SVG
```

---

## 🎨 Color Palettes

The skill includes 6 curated pastel palettes. Default is **Pastel Rainbow**:

| | Pink | Blue | Yellow | Green | Purple | Orange |
|---|---|---|---|---|---|---|
| **Fill** | `#FFE4E8` | `#E0F2FE` | `#FEF9C3` | `#DCFCE7` | `#F3E8FF` | `#FFEDD5` |
| **Border** | `#FDA4AF` | `#7DD3FC` | `#FDE047` | `#86EFAC` | `#D8B4FE` | `#FDBA74` |

Additional palettes: Ocean Breeze, Sunset Warm, Forest Natural, Corporate Clean, Neon Pop — see `references/color-palettes.md`.

---

## 📐 Layout Patterns

| Pattern | Best For | Example |
|---------|----------|---------|
| **Pipeline Grid** | Operational stages, workflows | 5-column grid with numbered cards |
| **Horizontal Flow** | Simple processes | A → B → C → D |
| **Architecture Layers** | Tech stack, system design | Stacked horizontal layers |
| **Kanban Board** | Task tracking, sprints | TODO → In Progress → Done |
| **Mind Map** | Brainstorming, topic breakdown | Central idea with branches |
| **Comparison Matrix** | Feature comparison, pros/cons | Table with ✅/❌ marks |
| **Timeline** | Roadmaps, milestones | Q1 → Q2 → Q3 → Q4 |

Detailed examples with ASCII previews in `references/layout-patterns.md`.

---

## 📂 Project Structure

```
whiteBoardDiagram-Skills/
├── SKILL.md                            ★ The skill — everything in one file
├── README.md                           This file
├── LICENSE                             MIT License
├── CLAUDE.md                           Claude Code integration
├── .cursorrules                        Cursor integration
├── .windsurfrules                      Windsurf integration
├── .github/
│   └── copilot-instructions.md         GitHub Copilot integration
└── references/
    ├── color-palettes.md               Extended color palettes (6 palettes)
    ├── layout-patterns.md              Layout patterns with ASCII previews
    ├── excalidraw-examples.md          Ready-to-import Excalidraw JSON
    └── mermaid-handdrawn-examples.md   Copy-paste Mermaid diagrams
```

---

## 🔌 Agent Integration Summary

| Agent | Config File | Install Complexity |
|-------|------------|-------------------|
| **Antigravity** | `SKILL.md` | Copy 1 folder |
| **Claude Code** | `SKILL.md` + `CLAUDE.md` | Copy 2 files |
| **Cursor** | `.cursorrules` | Copy 1 file |
| **Windsurf** | `.windsurfrules` | Copy 1 file |
| **GitHub Copilot** | `.github/copilot-instructions.md` | Copy 1 file |
| **Any Agent** | `SKILL.md` content | Paste into system prompt |

---

## 🛠️ Technologies Used

This skill leverages these tools/formats for hand-drawn rendering:

| Technology | Role | Link |
|-----------|------|------|
| **Mermaid.js** | Text-to-diagram with `look: handDrawn` | [mermaid.js.org](https://mermaid.js.org) |
| **Excalidraw** | Editable whiteboard canvas | [excalidraw.com](https://excalidraw.com) |
| **Rough.js** | Sketchy shape rendering library | [roughjs.com](https://roughjs.com) |
| **SVG Filters** | `<feTurbulence>` displacement for wobble | [MDN SVG Filters](https://developer.mozilla.org/en-US/docs/Web/SVG/Element/filter) |

---

## 💡 Example Prompts

Here are prompts you can try after installing the skill:

| Prompt | What You Get |
|--------|-------------|
| "Create a whiteboard of our CI/CD pipeline" | Pipeline grid with numbered stages |
| "Draw a hand-drawn system architecture" | Layered architecture diagram |
| "Make a sketchy comparison of AWS vs GCP vs Azure" | Comparison matrix board |
| "Whiteboard our sprint kanban" | Kanban board with task cards |
| "Draw a mind map of our product strategy" | Radial mind map |
| "Create a roadmap timeline for 2026" | Timeline with milestones |
| "Make it look like a real whiteboard photo" | Full board with all elements |

---

## 🤝 Contributing

Contributions welcome! To improve the skill:

1. Fork this repository
2. Make your changes to `SKILL.md` or `references/`
3. Test with at least 2 different AI agents
4. Submit a pull request

### What to Contribute
- New color palettes in `references/color-palettes.md`
- New layout patterns in `references/layout-patterns.md`
- New Mermaid examples in `references/mermaid-handdrawn-examples.md`
- New Excalidraw JSON templates in `references/excalidraw-examples.md`
- Bug fixes or clarity improvements to `SKILL.md`

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.

---

## ⭐ Star This Repo

If this skill helps you create better diagrams, give it a ⭐ on GitHub!

---

*Made with ✍️ for the AI coding agent community*
