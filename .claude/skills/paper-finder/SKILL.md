---
name: paper-finder
description: Find candidate Bangla NLP papers (2024–2026) by searching ACL Anthology first, then cross-checking. Use when discovering papers for a batch; returns candidates only, not full details.
---

# Paper Finder

**Purpose:** Find relevant Bangla NLP papers published from 2024 to 2026.

**When to use:** At the start of a batch, to discover candidate papers before extraction.

## Instructions

- **Search ACL Anthology first.**
- Search using **both "Bangla" and "Bengali"** as keywords.
- Prioritize papers from **ACL, EMNLP, NAACL, COLING, EACL, AACL**. Other peer-reviewed
  venues are allowed if they contain significant Bangla NLP work.
- Filter to publication years **2024, 2025, 2026**.
- Keep only papers where **Bangla/Bengali is a primary or major** part of the research.
- **Avoid duplicates** across batches.
- Return **candidate papers only** — do **not** extract full paper details in this skill
  (that is the job of `paper-extractor`).

## Output Format

| No | Title | Year | Official Venue | Publication Type | Link | Why Included |
|----|-------|------|----------------|------------------|------|--------------|

## Rules

- Do not hallucinate titles, venues, or links.
- Every candidate must have an official source link.
- If a field is unclear at this stage, write `Not clearly stated`.
