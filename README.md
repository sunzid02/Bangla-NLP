# Bangla NLP Literature Review 2024–2026

An MSc thesis literature review project.

**Main research question:**

> What problems have researchers worked on in Bangla NLP from 2024 to 2026?

## Purpose

This repository stores everything for the review:

- collected papers
- paper notes
- batch reviews
- verification docs
- the final literature review artifact
- the paper matrix CSV

## Folder Structure

| Path | Purpose |
|------|---------|
| `CLAUDE.md` | Claude Code entry point. |
| `AGENTS.md` | Portable project rules for any AI agent. |
| `.claude/skills/` | Reusable skills (paper finder, extractor, matrix builder, gap finder, Bangla explainer). |
| `docs/` | Verification docs (checklist, search strategy, inclusion/exclusion, venue verification). |
| `papers/raw/` | Source PDFs. |
| `papers/notes/` | Per-paper notes. |
| `batches/` | Working file per batch of 10 papers. |
| `logs/` | Search log and rejected-papers log. |
| `artifacts/` | Final deliverables: literature review and paper matrix. |

## Workflow

- Search **ACL Anthology first**.
- Use both **`Bangla`** and **`Bengali`** keywords.
- Work in **batches of 10 papers**.
- Verify venue, publication type, dataset, metric, and result.
- **Stop after each batch** for review.
- Update artifacts **only after approval**.

## Verification Principle

- **Accuracy over speed.**
- **Never hallucinate.**
- If something is unclear, write **`Not clearly stated`**.
- **Official source links required.**

## Active Instruction Files

- **`CLAUDE.md`** — Claude Code entry point.
- **`AGENTS.md`** — portable project rules.
- **`.claude/skills/*/SKILL.md`** — active reusable skills.

The old combined `Skills.md` file was removed. Active reusable skills live in `.claude/skills/*/SKILL.md`.

## Final Artifacts

- `artifacts/Bangla_NLP_Literature_Review_2024_2026.md`
- `artifacts/Bangla_NLP_Paper_Matrix_2024_2026.csv`
