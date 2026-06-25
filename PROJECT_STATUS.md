# PROJECT_STATUS.md — Persistent Project Memory

This file is the single source of truth for project progress. Future runs should read
this first (with `CLAUDE.md` and `WORKFLOW_RUN.md`) instead of reconstructing state from
old chats, logs, or PDFs.

---

## Current Project Phase
Systematic literature review of Bangla NLP (2024–2026), built batch by batch.

## Current Batch Status
- **Batch 2:** completed and verified.
- **Next batch:** Batch 3 — **not started** (start only after the user explicitly asks).

## Completed Batches
- **Batch 1:** completed and verified (papers 1–10).
- **Batch 2:** completed and verified (papers 11–20).

## Verified Paper Count
**20** (from the matrix CSV row count, minus header).

## Artifact Status
- `artifacts/Bangla_NLP_Paper_Matrix_2024_2026.csv` — up to date (20 papers).
- `artifacts/Bangla_NLP_Literature_Review_2024_2026.md` — up to date (Batches 1–2).

## PDF Status
All verified papers have official PDFs in `papers/raw/` (15 PDFs: 10 batch papers across
Batch 1 + 10 across Batch 2, plus pre-existing files). Every Batch 1–2 matrix paper has
its official PDF stored.

## Pending Manual Verification
- Paper 14 (BanNERD) metric scope — matrix leads with 90.49% on BanNERD + SOTA on 5/6; abstract 81.85% / §6.1 84.12% noted as different-scope averages.
- Papers 16 (GRASP-ChoQ) & 20 (ChakmaBridge) — kept with Bangla-centrality flags; revisit if a stricter inclusion view is preferred.
- Total BLP-2025 workshop paper count — not independently verified.
- `On Evaluation of Bangla Word Analogies.pdf` — year/venue/scope unverified; future-batch candidate.

## Known Issues
- `CLAUDE.md` and `batches/batch-01.md` may show as modified in git (pre-existing, not from recent batch work).
- Nothing committed yet — commits await user approval.

## Next Recommended Action
Wait for the user to explicitly request Batch 3. **Do not start Batch 3 automatically.**

## Last Updated
June 2026 — after Batch 2 completion and addition of the persistent-state system.
