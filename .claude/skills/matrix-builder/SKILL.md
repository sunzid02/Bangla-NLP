---
name: matrix-builder
description: Maintain a compact comparison matrix of reviewed Bangla NLP papers. Use only after the user approves a batch; never modify artifacts without explicit approval.
---

# Matrix Builder

**Purpose:** Maintain a compact comparison matrix of all reviewed papers.

**When to use:** **After the user approves a batch**, add the approved papers to the
matrix.

## Output Format

| No | Title | Year | Official Venue | Publication Type | Problem | Task | Dataset | Method | Result | Limitation |
|----|-------|------|----------------|------------------|---------|------|---------|--------|--------|------------|

## Rules

- **One row per paper.**
- Keep each cell brief (1–2 lines max).
- **Sort by year, then by venue.**
- **Update the matrix only after user approval.**
- **Do not modify artifacts without explicit approval.**
- No duplicate rows; if a field is unknown, write `Not clearly stated`.
