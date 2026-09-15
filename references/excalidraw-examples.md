# Excalidraw JSON Examples — Reference

Ready-to-use Excalidraw JSON snippets. Copy and paste into https://excalidraw.com or save as `.excalidraw` files.

---

## Example 1: Simple Pipeline Card

A single card with title, bullet points, and output section — the building block of pipeline boards.

```json
{
  "type": "excalidraw",
  "version": 2,
  "source": "whiteboard-diagram-skill",
  "elements": [
    {
      "id": "card-bg",
      "type": "rectangle",
      "x": 100,
      "y": 100,
      "width": 220,
      "height": 280,
      "angle": 0,
      "strokeColor": "#FDA4AF",
      "backgroundColor": "#FFE4E8",
      "fillStyle": "solid",
      "strokeWidth": 2,
      "strokeStyle": "solid",
      "roughness": 1,
      "opacity": 100,
      "groupIds": ["card-1"],
      "roundness": { "type": 3 },
      "seed": 42,
      "isDeleted": false,
      "boundElements": null,
      "locked": false
    },
    {
      "id": "card-number",
      "type": "text",
      "x": 110,
      "y": 110,
      "width": 30,
      "height": 30,
      "text": "①",
      "fontSize": 24,
      "fontFamily": 1,
      "textAlign": "left",
      "verticalAlign": "top",
      "groupIds": ["card-1"],
      "strokeColor": "#1E1E1E",
      "seed": 43,
      "isDeleted": false
    },
    {
      "id": "card-title",
      "type": "text",
      "x": 145,
      "y": 112,
      "width": 160,
      "height": 25,
      "text": "Research Phase",
      "fontSize": 18,
      "fontFamily": 1,
      "textAlign": "left",
      "verticalAlign": "top",
      "groupIds": ["card-1"],
      "strokeColor": "#1E1E1E",
      "seed": 44,
      "isDeleted": false
    },
    {
      "id": "card-body",
      "type": "text",
      "x": 115,
      "y": 155,
      "width": 190,
      "height": 120,
      "text": "• Scan data sources\n• Collect signals\n• Score opportunities\n• Build backlog",
      "fontSize": 14,
      "fontFamily": 1,
      "textAlign": "left",
      "verticalAlign": "top",
      "groupIds": ["card-1"],
      "strokeColor": "#343A40",
      "seed": 45,
      "isDeleted": false
    },
    {
      "id": "card-output-label",
      "type": "text",
      "x": 115,
      "y": 330,
      "width": 190,
      "height": 20,
      "text": "Output: scored topic list",
      "fontSize": 12,
      "fontFamily": 1,
      "textAlign": "left",
      "verticalAlign": "top",
      "groupIds": ["card-1"],
      "strokeColor": "#6C757D",
      "seed": 46,
      "isDeleted": false
    }
  ],
  "appState": {
    "viewBackgroundColor": "#FFFFFF",
    "gridSize": null
  },
  "files": {}
}
```

---

## Example 2: Arrow Connector

A hand-drawn arrow connecting two elements.

```json
{
  "id": "arrow-1",
  "type": "arrow",
  "x": 320,
  "y": 240,
  "width": 60,
  "height": 0,
  "angle": 0,
  "strokeColor": "#1E1E1E",
  "backgroundColor": "transparent",
  "fillStyle": "hachure",
  "strokeWidth": 2,
  "strokeStyle": "solid",
  "roughness": 1,
  "opacity": 100,
  "points": [[0, 0], [60, 0]],
  "startBinding": { "elementId": "card-1", "focus": 0, "gap": 8 },
  "endBinding": { "elementId": "card-2", "focus": 0, "gap": 8 },
  "startArrowhead": null,
  "endArrowhead": "arrow",
  "seed": 100,
  "isDeleted": false
}
```

---

## Example 3: Section Header Banner

A decorative header spanning the full width.

```json
[
  {
    "id": "header-bg",
    "type": "rectangle",
    "x": 50,
    "y": 20,
    "width": 1100,
    "height": 70,
    "strokeColor": "#7DD3FC",
    "backgroundColor": "#E0F2FE",
    "fillStyle": "solid",
    "strokeWidth": 2,
    "roughness": 1,
    "roundness": { "type": 3 },
    "seed": 200,
    "isDeleted": false
  },
  {
    "id": "header-title",
    "type": "text",
    "x": 400,
    "y": 35,
    "width": 400,
    "height": 40,
    "text": "System Architecture Overview",
    "fontSize": 28,
    "fontFamily": 1,
    "textAlign": "center",
    "strokeColor": "#1E1E1E",
    "seed": 201,
    "isDeleted": false
  }
]
```

---

## Key Element Properties Cheatsheet

| Property | Values | Description |
|----------|--------|-------------|
| `roughness` | `0` (clean), `1` (sketchy), `2` (very rough) | Hand-drawn intensity |
| `fillStyle` | `"solid"`, `"hachure"`, `"cross-hatch"` | Interior fill style |
| `strokeStyle` | `"solid"`, `"dashed"`, `"dotted"` | Border line style |
| `fontFamily` | `1` (Virgil/hand), `2` (Helvetica), `3` (Cascadia/code) | Font selection |
| `roundness` | `null` (sharp), `{type: 3}` (rounded) | Corner rounding |
| `strokeWidth` | `1`, `2`, `4` | Border thickness |

## Recommended Settings for Whiteboard Style
- `roughness: 1` — natural hand-drawn look without being too chaotic
- `fillStyle: "solid"` — clean pastel fills (use "hachure" for texture)
- `fontFamily: 1` — Virgil handwriting font
- `roundness: { type: 3 }` — soft rounded corners
- `strokeWidth: 2` — visible but not heavy borders
