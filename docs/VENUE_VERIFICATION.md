# Venue Verification

Prevent wrong venue labeling. (Publication-type values and the discrepancy rule are also
defined in `AGENTS.md` §9–§10; this file adds concrete examples.)

## Rules

- **Never infer** the venue from a conference name.
- Always **copy the official venue exactly** from ACL Anthology when available.
- Distinguish clearly between these venue / publication types:

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

- Do **not** write `EMNLP 2025` unless the paper is actually in the EMNLP **main
  conference** proceedings.
- If it is a **workshop** paper, write the **exact workshop proceedings name**.

## Examples

| Verdict | Venue string |
|---------|--------------|
| ✅ Correct | `Proceedings of the Second Workshop on Bangla Language Processing (BLP-2025)` |
| ✅ Correct | `Findings of the Association for Computational Linguistics: EMNLP 2024` |
| ✅ Correct | `Proceedings of the 2025 Conference on Empirical Methods in Natural Language Processing` |
| ❌ Incorrect | `EMNLP 2025` (unless it is truly the EMNLP main conference) |

## Discrepancy Rule

If ACL Anthology metadata and the PDF venue text **disagree**, **report both** and mark
the field as a discrepancy. Never silently choose one.
