# Whiteboard Diagram Generation

When the user asks to create a whiteboard, diagram, hand-drawn board, sketch, visual architecture, pipeline board, or any hand-drawn style visualization:

1. Read `SKILL.md` in this project root for comprehensive instructions
2. Follow the output format decision tree (Mermaid → SVG → Excalidraw → HTML)
3. Always apply hand-drawn aesthetics: sketchy borders, pastel fills, icons, clean typography hierarchy
4. Use the color palettes and layout patterns defined in the skill
5. Reference `references/` directory for extended examples and templates

## Quick Reference
- **Mermaid hand-drawn**: Use `%%{init: {"look": "handDrawn", "theme": "neutral"}}%%`
- **Excalidraw**: Set `roughness: 1`, `fillStyle: "hachure"`, `fontFamily: 1` (Virgil)
- **SVG**: Use `<feTurbulence>` + `<feDisplacementMap>` filters or Rough.js patterns
