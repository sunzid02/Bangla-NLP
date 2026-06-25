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

1. Search ACL Anthology first (`Bangla` + `Bengali`, 2024–2026), then cross-check
   Google Scholar and Semantic Scholar. *(See `docs/SEARCH_STRATEGY.md`.)*
2. Apply inclusion/exclusion criteria. *(See `AGENTS.md`.)*
3. Extract the required fields for each paper. *(Fields defined in `AGENTS.md`.)*
4. Run the verification checklist on every paper. *(See `docs/CHECKLIST.md`.)*
5. Present a summary table first, then concise per-paper notes with a beginner Bangla
   summary.
6. Log searches in `logs/search-log.md`; log exclusions in `logs/rejected-papers.md`.
7. **Stop and wait for approval. Update `artifacts/` only after approval.**

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


## Token-Saving Rule

Keep this file as a short entry point. Do not duplicate detailed rules from `AGENTS.md`,
`docs/`, or `.claude/skills/`. For normal outputs, prefer concise tables and short notes.