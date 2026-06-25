---
name: paper-extractor
description: Extract structured metadata from one verified Bangla NLP paper. Use when a paper link, PDF, or ACL Anthology page is available and full per-paper fields are needed.
---

# Paper Extractor

**Purpose:** Extract structured information from a single verified paper.

**When to use:** When a paper's link, PDF, abstract, or ACL Anthology metadata is
available and you need the full set of fields for the literature review.

## Fields to Extract

| Field | Notes |
|-------|-------|
| Title | Exact paper title |
| Authors | Full author list |
| Year | Publication year |
| Official Venue | Exact venue from ACL Anthology |
| Publication Type | Main Conference / Findings / Workshop / Journal / Demo / Industry Track / Shared Task / Student Research Workshop / Preprint, flagged / Not clearly stated |
| Link | Direct official URL (ACL Anthology preferred) |
| Problem | Research problem addressed |
| Task Type | e.g., NER, MT, SA, QA, Hate Speech, ASR |
| Dataset | Name and size if stated |
| Method / Model | Architecture or approach |
| Evaluation Metric | e.g., F1, BLEU, Accuracy, ROUGE |
| Main Result | Key quantitative result or finding |
| Contribution | What is new or novel |
| Limitation | Stated or obvious limitations |
| Future Work | Directions suggested by the authors |
| Beginner Bangla Summary | 3–5 simple Bangla sentences (see `bangla-explainer`) |
| Verification Status | The per-paper verification checklist |

## Rules

- **Do not hallucinate.** Never invent any field.
- If any field is missing or unclear, write `Not clearly stated`.
- **Use ACL Anthology first** as the source of truth.
- **Copy the official venue exactly** — do not infer or shorten it.
- Do **not** write "EMNLP 2025" unless the paper is truly in the EMNLP **main
  conference** proceedings; for workshops, use the exact workshop proceedings name.
- If ACL Anthology and the PDF disagree, report both and mark the field as a discrepancy.
- Keep the note **under 180 words**, excluding the Beginner Bangla Summary.
