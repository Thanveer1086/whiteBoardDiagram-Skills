# Whiteboard Diagram Generation

This repository contains a skill for generating professional hand-drawn whiteboard diagrams.

## When to Use
Activate when the user asks to create any: whiteboard, diagram, hand-drawn board, sketch, visual architecture, pipeline board, flowchart, mind map, kanban board, or comparison chart in a hand-drawn/sketchy style.

## How to Use
1. Read `SKILL.md` in the repository root for comprehensive generation instructions
2. Follow the output format decision tree:
   - **Mermaid** (default): Use `%%{init: {"look": "handDrawn"}}%%` — works in GitHub, docs, anywhere
   - **SVG**: Standalone hand-drawn SVG using filter displacement or Rough.js patterns
   - **Excalidraw JSON**: Importable `.excalidraw` files for editing
   - **HTML**: Self-contained interactive whiteboard
3. Apply hand-drawn aesthetics: sketchy borders, pastel fills, icons, clean typography
4. Use curated pastel palettes from SKILL.md
5. Check `references/` for extended examples

## Quick Mermaid Example
```
%%{init: {"look": "handDrawn", "theme": "neutral"}}%%
flowchart LR
    A["📊 Research"] --> B["✍️ Draft"]
    B --> C["🔍 Review"]
    C --> D["🚀 Publish"]
```
