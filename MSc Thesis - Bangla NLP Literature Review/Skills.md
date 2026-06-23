# Skills.md — Reusable Skills for MSc Thesis Workflow

---

## Skill 1: Paper Finder

**Purpose:** Find relevant Bangla NLP papers from 2024 to 2026.

**When to use:** When searching ACL Anthology, Google Scholar, or Semantic Scholar.

**Instructions:**
- Search using both "Bangla" and "Bengali" as keywords.
- Prioritize papers from ACL, EMNLP, NAACL, COLING, EACL, AACL.
- Keep only papers where Bangla/Bengali is a primary or major part of the research.
- Avoid duplicates across batches.
- Return only the fields in the output format below.

**Output format:**

| No | Title | Year | Venue | Link | Why Included |
|----|-------|------|-------|------|--------------|

---

## Skill 2: Paper Extractor

**Purpose:** Extract structured information from one paper.

**When to use:** When a paper link, PDF, title, abstract, or metadata is available.

**Instructions — extract the following fields:**

| Field | Notes |
|---|---|
| Title | Exact title |
| Authors | Full author list |
| Year | Publication year |
| Venue | Conference/journal name |
| Link | Direct URL |
| Problem | What problem does the paper address? |
| Task type | e.g., NER, MT, SA, QA |
| Dataset | Name and size if stated |
| Method/Model | Architecture or approach |
| Metric | e.g., F1, BLEU, Accuracy |
| Result | Key numbers or findings |
| Contribution | What is new or novel? |
| Limitation | Stated or obvious limitations |
| Future Work | Directions suggested by authors |
| Beginner Bangla Summary | 3–5 sentences in simple Bangla (max 120 words) |

**Rules:**
- Do not hallucinate. Never invent fields.
- If any field is missing or unclear, write `Not clearly stated`.
- Keep the summary concise (under 180 words, excluding Bangla summary).

---

## Skill 3: Literature Matrix Builder

**Purpose:** Maintain a compact comparison table of all reviewed papers.

**When to use:** After each batch is approved, add new papers to the matrix.

**Output format:**

| No | Title | Year | Venue | Problem | Task | Dataset | Method | Result | Limitation |
|----|-------|------|-------|---------|------|---------|--------|--------|------------|

**Rules:**
- One row per paper.
- Keep each cell brief (1–2 lines max).
- Sort by year, then venue.

---

## Skill 4: Research Gap Finder

**Purpose:** Analyze reviewed papers and identify research gaps.

**When to use:** After a batch or set of batches to synthesize findings.

**Instructions — group gaps under these categories:**

| Gap Type | Description |
|---|---|
| Dataset Gap | Missing or insufficient Bangla datasets for a task |
| Benchmark Gap | No standard benchmark for evaluation |
| Model Gap | No strong baseline or state-of-the-art model for a task |
| Evaluation Gap | Inconsistent or missing evaluation protocols |
| Low-Resource Issue | Lack of labeled data, especially for dialects or domains |
| Domain Gap | Underrepresented domains (medical, legal, social media, etc.) |
| Practical Deployment Gap | No real-world application or system built from the research |

**Output format:** For each gap type, list:
- Which papers revealed this gap
- A short explanation of the gap
- Possible directions to address it

---

## Skill 5: Beginner Bangla Explainer

**Purpose:** Explain each paper in easy, accessible Bangla.

**When to use:** At the end of every paper note (Paper Extractor output).

**Instructions — write one short Bangla paragraph answering:**
1. এই পেপারটা কোন সমস্যা নিয়ে কাজ করেছে?
2. কী method বা model ব্যবহার করেছে?
3. কী result পেয়েছে?
4. Limitation কী ছিল?
5. আমার thesis-এর জন্য কেন useful হতে পারে?

**Rules:**
- Maximum **120 Bangla words**.
- Use simple, everyday language — avoid jargon.
- Write in first person if it helps clarity ("এই গবেষণায়...").
- Do not translate the paper title literally; describe it naturally.
