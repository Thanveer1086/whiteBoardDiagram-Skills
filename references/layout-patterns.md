# Whiteboard Layout Patterns — Reference

Common layout patterns for whiteboard diagrams with ASCII previews, dimensions, and use cases.

---

## Pattern 1: Pipeline Grid (3×3 or 5×2)
Best for: Operational pipelines, process stages, workflow overviews

```
┌──────────────────────────────────────────────────┐
│                    TITLE HEADER                   │
├──────────┬──────────┬──────────┬──────────┬──────┤
│ ① Stage  │ ② Stage  │ ③ Stage  │ ④ Stage  │ ⑤   │
│  Name 1  │  Name 2  │  Name 3  │  Name 4  │     │
│ ──────── │ ──────── │ ──────── │ ──────── │     │
│ • Item 1 │ • Item 1 │ • Item 1 │ • Item 1 │     │
│ • Item 2 │ • Item 2 │ • Item 2 │ • Item 2 │     │
│ • Item 3 │ • Item 3 │ • Item 3 │ • Item 3 │     │
│ ──────── │ ──────── │ ──────── │ ──────── │     │
│ Output:  │ Output:  │ Output:  │ Output:  │     │
│ result   │ result   │ result   │ result   │     │
├──────────┼──────────┼──────────┼──────────┼──────┤
│ ⑥ Stage  │ ⑦ Stage  │ ⑧ Stage  │ ⑨ Stage  │     │
│  ...     │  ...     │  ...     │  ...     │     │
└──────────┴──────────┴──────────┴──────────┴──────┘
│           ARCHITECTURE / SUPPORT LAYER            │
├──────────┬──────────┬──────────┬──────────────────┤
│ Category │ Category │ Category │ Category         │
│ • item   │ • item   │ • item   │ • item           │
└──────────┴──────────┴──────────┴──────────────────┘
│  Flow: A → B → C → D → E → F                     │
└──────────────────────────────────────────────────┘
```

Card dimensions: ~180-220px wide × 200-280px tall
Gutter: 16-24px between cards
Total canvas: ~1200-1600px wide × 900-1200px tall

---

## Pattern 2: Horizontal Flow
Best for: Simple processes, data pipelines, decision trees

```
┌─────┐    ┌─────┐    ┌─────┐    ┌─────┐    ┌─────┐
│  A  │───→│  B  │───→│  C  │───→│  D  │───→│  E  │
└─────┘    └─────┘    └─────┘    └─────┘    └─────┘
```

---

## Pattern 3: Architecture Layers
Best for: Tech stack, system architecture, org structure

```
┌──────────────────────────────────────┐
│          PRESENTATION LAYER          │
│  ┌────────┐  ┌────────┐  ┌────────┐ │
│  │ Web UI │  │ Mobile │  │  API   │ │
│  └────────┘  └────────┘  └────────┘ │
├──────────────────────────────────────┤
│          BUSINESS LOGIC LAYER        │
│  ┌────────┐  ┌────────┐  ┌────────┐ │
│  │Auth Svc│  │Order Svc│ │Pay Svc │ │
│  └────────┘  └────────┘  └────────┘ │
├──────────────────────────────────────┤
│            DATA LAYER                │
│  ┌────────┐  ┌────────┐  ┌────────┐ │
│  │Postgres│  │ Redis  │  │  S3    │ │
│  └────────┘  └────────┘  └────────┘ │
└──────────────────────────────────────┘
```

---

## Pattern 4: Kanban Board
Best for: Task tracking, project status, sprint planning

```
┌─────────┬─────────┬─────────┬─────────┐
│ 📋 TODO │ 🔄 IN   │ 🔍 IN   │ ✅ DONE │
│         │ PROGRESS│ REVIEW  │         │
├─────────┼─────────┼─────────┼─────────┤
│ ┌─────┐ │ ┌─────┐ │ ┌─────┐ │ ┌─────┐ │
│ │Card │ │ │Card │ │ │Card │ │ │Card │ │
│ └─────┘ │ └─────┘ │ └─────┘ │ └─────┘ │
│ ┌─────┐ │ ┌─────┐ │         │ ┌─────┐ │
│ │Card │ │ │Card │ │         │ │Card │ │
│ └─────┘ │ └─────┘ │         │ └─────┘ │
│ ┌─────┐ │         │         │         │
│ │Card │ │         │         │         │
│ └─────┘ │         │         │         │
└─────────┴─────────┴─────────┴─────────┘
```

---

## Pattern 5: Mind Map / Radial
Best for: Brainstorming, concept exploration, topic breakdown

```
                    ┌─────────┐
            ┌──────→│ Topic A │
            │       └─────────┘
┌─────────┐ │       ┌─────────┐
│ CENTRAL │─┼──────→│ Topic B │
│  IDEA   │ │       └─────────┘
└─────────┘ │       ┌─────────┐
            ├──────→│ Topic C │
            │       └─────────┘
            │       ┌─────────┐
            └──────→│ Topic D │
                    └─────────┘
```

---

## Pattern 6: Comparison Matrix
Best for: Feature comparison, pros/cons, option evaluation

```
┌─────────────┬───────────┬───────────┬───────────┐
│             │ Option A  │ Option B  │ Option C  │
├─────────────┼───────────┼───────────┼───────────┤
│ Feature 1   │    ✅     │    ✅     │    ❌     │
│ Feature 2   │    ❌     │    ✅     │    ✅     │
│ Feature 3   │    ✅     │    ❌     │    ✅     │
│ Price       │   $$$     │    $$     │    $      │
│ Rating      │   ⭐⭐⭐  │   ⭐⭐⭐⭐ │   ⭐⭐    │
└─────────────┴───────────┴───────────┴───────────┘
```

---

## Pattern 7: Timeline
Best for: Roadmaps, project milestones, historical events

```
     Q1           Q2           Q3           Q4
──┬──────────┬──────────┬──────────┬──────────┬──
  │ 🎯       │ 🚀       │ 📊       │ 🏆       │
  │ Planning │ Launch   │ Scale    │ Optimize │
  │          │          │          │          │
  │ • Goal 1 │ • Goal 1 │ • Goal 1 │ • Goal 1 │
  │ • Goal 2 │ • Goal 2 │ • Goal 2 │ • Goal 2 │
──┴──────────┴──────────┴──────────┴──────────┴──
```

---

## Spacing & Dimension Guidelines

| Element | Recommended Size | Notes |
|---------|-----------------|-------|
| Card width | 180-220px | Consistent within a board |
| Card height | 200-300px | Varies by content |
| Gutter (between cards) | 16-24px | Consistent spacing |
| Header height | 60-80px | Bold, prominent |
| Footer/legend height | 40-60px | Subdued |
| Icon size | 24-32px | Consistent per board |
| Canvas width | 1200-1600px | Standard whiteboard |
| Canvas height | 900-1200px | 4:3 or 16:9 aspect |
| Border radius | 8-12px | Consistent roundness |
| Border width | 2px | Standard stroke |
| Font — title | 18-24px | Bold |
| Font — body | 12-14px | Regular |
| Font — label | 10-12px | Light/muted |
