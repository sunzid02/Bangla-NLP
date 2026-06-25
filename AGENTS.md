# AGENTS.md — Portable Project Rules

Tool-independent rules for any AI agent working on this project. These rules define the
research workflow and verification standards and do not depend on any specific tool or
assistant. (For repository orientation, see `CLAUDE.md`; for reusable task instructions,
see `.claude/skills/*/SKILL.md`.)

> **Responsibility split:** `AGENTS.md` contains portable project rules. The `docs/`
> folder contains detailed procedures, examples, and edge-case guidance. If a rule is
> summarized here and expanded in `docs/`, use the relevant docs file for detailed
> execution.

---

## 1. Project

**MSc Thesis — Bangla NLP Literature Review**

A systematic, verifiable review of Bangla NLP research. The guiding principle is
**accuracy over speed**: never guess, never hallucinate.

## 2. Main Research Question

> What problems have researchers worked on in Bangla NLP from 2024 to 2026?

## 3. Scope

- Papers published between **2024 and 2026**.
- Bangla/Bengali must be a **primary or major** part of the research.
- Peer-reviewed work preferred; preprints only when no peer-reviewed version exists
  (and they must be flagged).

## 4. Target Venues

ACL, EMNLP, NAACL, COLING, EACL, AACL. Other peer-reviewed venues may be included if
they contain significant Bangla NLP research.

---

## 5. Source Priority (highest → lowest)

Verify every paper in this order:

1. **ACL Anthology**
2. Official conference proceedings
3. Official paper PDF
4. Google Scholar
5. Semantic Scholar

**If sources conflict:**

- **ACL Anthology wins** for venue metadata.
- If ACL Anthology and the PDF disagree, **report both** and mark the field as a
  **discrepancy** — never choose one silently.

---

## 6. Inclusion Criteria

Include a paper only if it is from **2024–2026**, Bangla/Bengali is **central or major**,
an **official source** exists, and it has verifiable Bangla-related data, model,
experiment, benchmark, or evaluation.

For detailed examples and borderline cases, see `docs/INCLUSION_EXCLUSION.md`.

## 7. Exclusion Criteria

Exclude a paper if Bangla/Bengali is only mentioned in passing, the source is
unverifiable, the paper is a duplicate, the year/venue cannot be verified, or it is not a
real research paper.

For detailed examples and borderline cases, see `docs/INCLUSION_EXCLUSION.md`.

---

## 8. Required Fields Per Paper

| Field | Description |
|-------|-------------|
| Title | Exact paper title |
| Authors | Full author list |
| Year | Publication year |
| Official Venue | Exact venue from ACL Anthology |
| Publication Type | One of the allowed values (see §10) |
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
| Beginner Bangla Summary | 3–5 simple Bangla sentences (see §16) |
| Verification Status | The checklist in §15 |

If any field is missing or unclear, write **`Not clearly stated`**.

---

## 9. Venue Verification Rules

- **Never infer** the venue from a conference name.
- Always **copy the official venue exactly** from ACL Anthology when available.
- Clearly distinguish between:
  - Main Conference
  - Findings
  - Workshop
  - Journal
  - Demo
  - Industry Track
  - Shared Task
  - Student Research Workshop
  - Preprint (flagged)
- Do **not** write “EMNLP 2025” unless the paper is actually published in the EMNLP
  **main conference** proceedings.
- If a paper is in a workshop, write the **exact workshop proceedings name** (e.g.,
  *Proceedings of the Second Workshop on Bangla Language Processing (BLP-2025)*).

## 10. Publication Type Rules

Every paper must specify exactly one of these allowed values:

- Main Conference
- Findings
- Workshop
- Journal
- Demo
- Industry Track
- Shared Task
- Student Research Workshop
- Preprint, flagged
- Not clearly stated

Never guess the publication type. If it cannot be verified, use **`Not clearly stated`**.

---

## 11. Anti-Hallucination Rules

- **Never invent** titles, authors, venues, datasets, metrics, results, or URLs.
- Every paper must have an **official source link**.
- Every claim must be traceable to an official source or the paper PDF.
- If something cannot be verified, write **`Not clearly stated`** — do not approximate.
- No duplicate papers.

---

## 12. Batch Workflow

- Work in **batches of 10 papers**.
- Search **ACL Anthology first**.
- Search using **both “Bangla” and “Bengali”**.
- Cross-check with Google Scholar and Semantic Scholar **only after** ACL Anthology.
- **Stop after every batch** and ask the user to review before continuing.
- **Do not update the final artifacts** until the user approves the batch.

---

## 13. Output Format

- **Summary table first**, then concise per-paper notes.
- Keep each paper note **under 180 words**, excluding the Beginner Bangla Summary.
- Use bullets and tables; avoid long introductions and repetition.
- End each batch with: **“Batch [N] complete. Please review before I continue.”**

## 14. Artifact Update Rule

Update the deliverables (the literature review and the paper matrix) **only after the
user approves the batch**. Never write to the artifacts mid-batch or without approval.

---

## 15. Verification Status Checklist

Every paper must pass the mandatory verification checklist before being added to a batch
or artifact. The checklist must verify title, authors, year, venue, publication type,
official URL, PDF, dataset, method, metrics, results, contribution, limitation, future
work, duplicate status, and Bangla/Bengali centrality.

For the full checklist, see `docs/CHECKLIST.md`.

## 16. Beginner-Friendly Bangla Summary Rule

For every paper, include a short Bangla summary:

- **3 to 5 simple Bangla sentences.**
- Clear, beginner-friendly language; avoid jargon.
- Briefly cover: the problem, the method/model, the result, and the limitation.

## Token-Saving Behavior

- Keep responses concise.
- Use tables first, then short notes.
- Avoid long introductions.
- Avoid repeating rules already defined in other files.
- Do not paste full paper text unless explicitly asked.
- Do not repeat the full verification checklist explanation every time.
- For each paper, keep the note under 180 words, excluding the Beginner Bangla Summary.
- Beginner Bangla Summary must be maximum 120 Bangla words.
- When updating artifacts, only add or change the necessary sections.
- If a file already contains a rule, reference that file instead of repeating the full rule.