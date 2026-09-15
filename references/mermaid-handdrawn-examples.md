# Mermaid Hand-Drawn Mode — Examples Reference

Ready-to-use Mermaid diagram code with `look: handDrawn`. Copy into any Markdown file, Mermaid Live Editor, or documentation system.

> **Requires**: Mermaid v11+ for `look: handDrawn` support.

---

## Example 1: Pipeline Flowchart

```mermaid
%%{init: {"look": "handDrawn", "theme": "neutral"}}%%
flowchart LR
    A["📊 Research\n& Intelligence"] --> B["✍️ Article\nDrafting"]
    B --> C["🌐 Web\nPublishing"]
    C --> D["📧 Newsletter\nDistribution"]
    D --> E["📈 Performance\nReporting"]
    E --> F["🎯 Demand\nGeneration"]
```

## Example 2: Architecture Layers

```mermaid
%%{init: {"look": "handDrawn", "theme": "neutral"}}%%
block-beta
    columns 3
    block:frontend["🖥️ Frontend"]
        A["React App"] B["Mobile App"] C["Admin Panel"]
    end
    block:backend["⚙️ Backend"]
        D["API Gateway"] E["Auth Service"] F["Core Logic"]
    end
    block:data["🗄️ Data Layer"]
        G["PostgreSQL"] H["Redis Cache"] I["S3 Storage"]
    end
```

## Example 3: Sequence Diagram

```mermaid
%%{init: {"look": "handDrawn", "theme": "neutral"}}%%
sequenceDiagram
    autonumber
    actor User
    participant API as 🌐 API Gateway
    participant Auth as 🔐 Auth Service
    participant DB as 🗄️ Database

    User->>API: POST /login
    API->>Auth: Validate credentials
    Auth->>DB: Query user record
    DB-->>Auth: User data
    Auth-->>API: JWT token
    API-->>User: 200 OK + token
```

## Example 4: Mind Map

```mermaid
%%{init: {"look": "handDrawn", "theme": "neutral"}}%%
mindmap
  root((🎯 Product\nStrategy))
    📊 Research
      Market Analysis
      Competitor Audit
      User Interviews
    ✍️ Design
      Wireframes
      Prototypes
      User Testing
    🚀 Build
      Frontend
      Backend
      Infrastructure
    📈 Growth
      Marketing
      Sales
      Partnerships
```

## Example 5: Gantt / Timeline

```mermaid
%%{init: {"look": "handDrawn", "theme": "neutral"}}%%
gantt
    title 🗓️ Project Roadmap 2026
    dateFormat YYYY-MM-DD
    section 📊 Research
        Market Analysis    :a1, 2026-01-01, 30d
        User Research      :a2, after a1, 20d
    section ✍️ Design
        Wireframes         :b1, after a2, 15d
        Prototyping        :b2, after b1, 20d
    section 🚀 Development
        Sprint 1           :c1, after b2, 14d
        Sprint 2           :c2, after c1, 14d
        Sprint 3           :c3, after c2, 14d
    section 📈 Launch
        Beta Release       :d1, after c3, 7d
        GA Release         :milestone, after d1, 0d
```

## Example 6: Decision Flowchart

```mermaid
%%{init: {"look": "handDrawn", "theme": "neutral"}}%%
flowchart TD
    Start(["🤔 What output\nformat?"]) --> Q1{"Needs to be\neditable?"}
    Q1 -->|Yes| Excalidraw["📐 Excalidraw JSON\n.excalidraw file"]
    Q1 -->|No| Q2{"Embedded in\ndocs/markdown?"}
    Q2 -->|Yes| Mermaid["📊 Mermaid\nhand-drawn mode"]
    Q2 -->|No| Q3{"Interactive\nneeded?"}
    Q3 -->|Yes| HTML["🌐 HTML\nself-contained"]
    Q3 -->|No| SVG["🖼️ SVG\nstandalone file"]

    style Excalidraw fill:#E0F2FE,stroke:#7DD3FC
    style Mermaid fill:#DCFCE7,stroke:#86EFAC
    style HTML fill:#F3E8FF,stroke:#D8B4FE
    style SVG fill:#FEF9C3,stroke:#FDE047
```

## Example 7: Entity Relationship (ER) Diagram

```mermaid
%%{init: {"look": "handDrawn", "theme": "neutral"}}%%
erDiagram
    USER ||--o{ ORDER : places
    USER {
        string name
        string email
        string role
    }
    ORDER ||--|{ LINE_ITEM : contains
    ORDER {
        int id
        date created
        string status
    }
    PRODUCT ||--o{ LINE_ITEM : "ordered in"
    PRODUCT {
        int id
        string name
        float price
    }
```

## Configuration Reference

### Minimal Hand-Drawn Config
```
%%{init: {"look": "handDrawn"}}%%
```

### Full Config with Seed (Deterministic)
```
%%{init: {"look": "handDrawn", "handDrawnSeed": 42, "theme": "neutral"}}%%
```

### Config via Frontmatter
```
---
config:
  look: handDrawn
  handDrawnSeed: 42
  theme: neutral
---
```

### Supported Diagram Types with Hand-Drawn
| Diagram Type | Supported | Notes |
|-------------|-----------|-------|
| Flowchart | ✅ | Best support |
| Sequence | ✅ | Full support |
| Class | ✅ | Full support |
| State | ✅ | Full support |
| ER Diagram | ✅ | Full support |
| Mindmap | ✅ | Great for brainstorming |
| Gantt | ✅ | Timeline views |
| Git Graph | ✅ | Repo visualization |
| Block | ✅ | Architecture diagrams |
| Pie | ✅ | Data visualization |
| Quadrant | ✅ | 2x2 matrices |
| Timeline | ✅ | Event sequences |
