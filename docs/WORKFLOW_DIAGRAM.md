# Workflow Diagram — Bangla NLP Thesis Review

How the project continues from its saved state when the user says `RUN`.

```mermaid
flowchart TD
    A([User says RUN]) --> B[Read CLAUDE.md + WORKFLOW_RUN.md + PROJECT_STATUS.md]
    B --> C[Identify next pending action]

    C --> D{Need more context?}
    D -->|project rules| E[Open AGENTS.md]
    D -->|detailed verification rules| F[Open docs/]
    D -->|task helper| G[Open .claude/skills/]
    D -->|no| H[Execute next safe step]
    E --> H
    F --> H
    G --> H

    H --> I[Search ACL Anthology]
    I --> J[Apply inclusion / exclusion]
    J --> K[Verify metadata]
    K --> L[Download missing official PDFs to papers/raw/]
    L --> M[Extract required fields]
    M --> N[Run checklist]
    N --> O[Final self-review]
    O --> P[Prepare report]
    P --> Q{User approval?}
    Q -->|no| P
    Q -->|yes| R[Update artifacts/ + batches/ + logs/]
    R --> S[Update PROJECT_STATUS.md]
    S --> T([End with next recommended action])
```

## What each file is for

- **`CLAUDE.md`** — project entry point.
- **`WORKFLOW_RUN.md`** — defines the `RUN` command behavior.
- **`PROJECT_STATUS.md`** — persistent memory / current state.
- **`AGENTS.md`** — portable project rules (opened lazily).
- **`docs/`** — detailed verification references (opened lazily).
- **`.claude/skills/`** — optional task helpers (opened lazily).
- **`logs/`** — research history (searches, rejected papers).
- **`artifacts/`** — final thesis outputs (matrix + literature review).
