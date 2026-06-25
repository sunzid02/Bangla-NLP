# CLAUDE.md — Project Entry Point

**MSc Thesis — Bangla NLP Literature Review**

This is the **root entry point** for Claude Code. Read it first. It gives you the goal,
the repository layout, the core principles, and where to find everything else. It does
**not** repeat the portable rules (those live in `AGENTS.md`) or the reusable skills
(those live in `.claude/skills/*/SKILL.md`).

---

## Project Overview

A **systematic, verifiable literature review** of Bangla NLP research published between
**2024 and 2026**. The output is a literature review document and a paper matrix in
`artifacts/`, built up batch by batch.

**Guiding principle:** *Accuracy over speed.* Never guess. Never hallucinate.

## Main Research Question

> What problems have researchers worked on in Bangla NLP from 2024 to 2026?

---

## Repository Structure

| Path | Purpose |
|------|---------|
| `CLAUDE.md` | This entry point — orientation and high-level workflow. |
| `AGENTS.md` | **Portable project rules** — inclusion/exclusion, required fields, venue & publication-type rules, anti-hallucination, batch workflow. |
| `PROJECT_STATUS.md` | **Persistent project memory** — current phase, batch status, paper count, pending items, next action. |
| `WORKFLOW_RUN.md` | Defines the `RUN` command — what to read and do to continue from the latest state. |
| `README.md` | Human-facing project overview. |
| `.claude/skills/*/SKILL.md` | Reusable skills (Paper Finder, Extractor, Matrix Builder, Gap Finder, Bangla Explainer). |
| `docs/CHECKLIST.md` | Per-paper verification checklist — run **before** adding any paper. |
| `docs/SEARCH_STRATEGY.md` | Detailed search workflow. |
| `docs/INCLUSION_EXCLUSION.md` | Full inclusion/exclusion criteria. |
| `docs/VENUE_VERIFICATION.md` | Venue-naming rules and examples. |
| `papers/raw/` | Source PDFs. |
| `papers/notes/` | Per-paper extraction notes. |
| `artifacts/` | Final deliverables: literature review (`.md`) and paper matrix (`.csv`). |
| `batches/` | Working file per batch of 10 papers. |
| `logs/` | `search-log.md` (searches run) and `rejected-papers.md` (excluded papers + reason). |

---

## Which Files to Follow

- **For project rules** (what to include, required fields, venue/publication rules,
  anti-hallucination, batch workflow) → follow **`AGENTS.md`**.
- **For reusable task instructions** (finding, extracting, matrix, gaps, Bangla
  summaries) → follow **`.claude/skills/*/SKILL.md`**.
- **Before adding any paper** → run **`docs/CHECKLIST.md`**.
- For detailed procedures → `docs/SEARCH_STRATEGY.md`, `docs/INCLUSION_EXCLUSION.md`,
  `docs/VENUE_VERIFICATION.md`.

This entry point stays high-level; do not duplicate those files' content here.

---

## Source Priority (highest → lowest)

Always verify in this order:

1. **ACL Anthology** (official) — https://aclanthology.org/
2. Official conference proceedings
3. Official paper PDF
4. Google Scholar — https://scholar.google.com/
5. Semantic Scholar — https://www.semanticscholar.org/

**ACL Anthology always wins.** Never trust Google/Semantic Scholar over it for venue
information. If ACL Anthology and the PDF disagree, **report both and flag the
discrepancy** — never choose silently. Exact venue-naming and publication-type rules
live in `AGENTS.md` and `docs/VENUE_VERIFICATION.md`.

---

## High-Level Workflow

Work proceeds **in batches of 10 papers**. For each batch:

1. Search ACL Anthology first using both `Bangla` and `Bengali` for years 2024–2026, then cross-check with Google Scholar and Semantic Scholar if needed. *(See `docs/SEARCH_STRATEGY.md`.)*

2. Apply the inclusion and exclusion criteria. *(See `AGENTS.md` and `docs/INCLUSION_EXCLUSION.md`.)*

3. Ensure the official PDF for every batch paper exists in `papers/raw/`. If a PDF is missing, download it from ACL Anthology or the official publisher before completing the batch.

4. Extract the required fields for each paper. *(Fields are defined in `AGENTS.md`.)*

5. Run the verification checklist on every paper. *(See `docs/CHECKLIST.md`.)*

6. Perform the final self-review before marking the batch complete.

7. Present a summary table first, then concise per-paper notes with a beginner-friendly Bangla summary.

8. Log searches in `logs/search-log.md`; log excluded papers in `logs/rejected-papers.md`.

9. Stop and wait for user approval.

10. Update `artifacts/` only after approval.

---

## Strict Verification Principles

- **Never hallucinate** titles, authors, venues, datasets, metrics, results, or URLs.
- **Every paper needs an official source link.**
- If a field cannot be verified, write **`Not clearly stated`**.
- Verify against official sources in the priority order above.
- The detailed field-by-field checklist is `docs/CHECKLIST.md` — it is mandatory.

---

## Batch Approval Rule

**Never continue to the next batch, and never write to `artifacts/`, without explicit
user approval.** End each batch with:

> **"Batch [N] complete. Please review before I continue."**


## RUN Command

When the user says `RUN`, follow `WORKFLOW_RUN.md`.

Start by reading only:

1. `CLAUDE.md`
2. `WORKFLOW_RUN.md`
3. `PROJECT_STATUS.md`

Then open other files only if needed.

Do not spawn subagents unless explicitly requested.

At the end of every run, update `PROJECT_STATUS.md`.


## Token-Saving Rule

Keep this file as a short entry point. Do not duplicate detailed rules from `AGENTS.md`,
`docs/`, or `.claude/skills/`. For normal outputs, prefer concise tables and short notes.


## Official PDF Management

Every paper included in a verified batch must have its official PDF stored locally.

Rules:

- Check `papers/raw/` before downloading.
- If the PDF already exists, reuse it.
- If it does not exist, download the official PDF from ACL Anthology or the official publisher.
- Save it in `papers/raw/` using a clean and consistent filename.
- Do not keep temporary PDFs elsewhere.
- Every verified paper must have its corresponding official PDF inside `papers/raw/` before the batch is completed.

Local PDFs are for reproducibility only.

Official metadata must always be verified from ACL Anthology or another official publisher.


## Final Self-Review

Before completing any batch, perform a final self-review.

Verify that:

- No hallucinated values were introduced.
- Every factual claim is supported by the official paper or ACL Anthology.
- Future Work is explicitly stated in the paper. Otherwise write "Not clearly stated".
- Evaluation metrics match the official paper.
- Official Venue matches ACL Anthology exactly.
- Publication Type is correct.
- No duplicate papers exist.
- Every verified paper has its official PDF stored in `papers/raw/`.
- Every required field is completed.
- Every PDF in `papers/raw/` belongs to at least one paper in the current repository. Otherwise classify it as a future candidate or log it as rejected.

If any value cannot be verified, use:

Not clearly stated

Do not infer missing information.
