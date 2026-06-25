# CLAUDE.md — Operating Instructions for MSc Thesis Literature Review

## Project
**MSc Thesis — Bangla NLP Literature Review**

## Task
Review recent work in Bangla NLP from **2024 to 2026**.

## Main Research Question
> What problems have researchers worked on in Bangla NLP from 2024 to 2026?

---

## Target Venues
ACL, EMNLP, NAACL, COLING, EACL, AACL

## Main Sources
- **ACL Anthology**: https://aclanthology.org/
- **Google Scholar**: https://scholar.google.com/
- **Semantic Scholar**: https://www.semanticscholar.org/

---

## Rules

1. Work in small batches of **10 papers**.
2. Search **ACL Anthology first**.
3. Use Google Scholar and Semantic Scholar only to cross-check and discover missing papers.
4. **Do not hallucinate.** Never invent paper titles, authors, links, or results.
5. Every paper must have a **source link**.
6. If year, venue, dataset, metric, or result is unclear, write `Not clearly stated`.
7. **Avoid duplicate papers.**
8. Do not include a paper just because it casually mentions Bangla or Bengali.
9. Include only papers where **Bangla/Bengali is a meaningful part of the research**.
10. **Stop after each batch and ask me to review** before proceeding.
11. Keep output **concise** to save tokens.
12. Use **table format first**, then short paper notes.
13. Add one **beginner-friendly Bangla paragraph** at the end of each paper summary.

---

## Required Fields Per Paper

| Field | Notes |
|---|---|
| Title | Exact title |
| Authors | Full author list |
| Year | Publication year |
| Venue | Conference/journal name |
| Link | Direct URL (ACL Anthology preferred) |
| Problem | What problem does the paper address? |
| Task type | e.g., NER, MT, SA, QA, etc. |
| Dataset | Name and size if stated |
| Method/Model | Architecture or approach used |
| Evaluation Metric | e.g., F1, BLEU, Accuracy |
| Main Result | Key numbers or findings |
| Contribution | What is new or novel? |
| Limitation | Stated or obvious limitations |
| Beginner Bangla Summary | 3–5 sentences in simple Bangla |

---

## Artifact to Maintain

**Title:** `Recent Work in Bangla NLP (2024–2026): Literature Review`

### Artifact Sections
1. Search Strategy
2. Inclusion and Exclusion Criteria
3. Literature Matrix
4. Topic-wise Grouping
5. Year-wise Trend
6. Venue-wise Distribution
7. Research Problems Studied
8. Common Datasets
9. Common Models/Methods
10. Research Gaps
11. Possible Thesis Directions
12. Paper-by-paper Summaries

---

## Token-Saving Behavior

- Do not write long introductions.
- Do not repeat the same explanation.
- Use concise bullet points.
- Only expand when explicitly asked.
- Keep each paper summary **under 180 words** (plus Bangla summary).

---

## Workflow Per Batch

1. Search ACL Anthology for Bangla/Bengali NLP papers (2024–2026).
2. Collect 10 papers that pass inclusion criteria.
3. Present a **summary table** first.
4. Then write **short paper notes** (one per paper) with all required fields.
5. End with: **"Batch [N] complete. Please review before I continue."**
6. Update the artifact after approval.

---

## Inclusion Criteria
- Published 2024–2026
- Bangla/Bengali is a primary or major language in the study
- Published at a peer-reviewed venue (target venues preferred; others accepted if high quality)

## Exclusion Criteria
- Papers where Bangla is only mentioned in passing
- Preprints without any peer review (unless no venue alternative exists — flag these)
- Duplicate entries
- Papers with no verifiable source link
