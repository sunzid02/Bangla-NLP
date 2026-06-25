# Batch 1 — Working Record

**Status:** Verified & committed to artifacts (June 2026)
**Papers:** 10 | **Verification:** ACL Anthology (metadata) + official PDFs (results)

---

## Papers in this batch

| No | Short name | Year | Official Venue | Type | ACL Anthology ID |
|----|-----------|------|----------------|------|------------------|
| 1 | BenLLM-Eval | 2024 | LREC-COLING 2024 | Main Conference | 2024.lrec-main.201 |
| 2 | Bias & Context Length for Bangla | 2024 | Findings of the ACL: ACL 2024 | Findings | 2024.findings-acl.88 |
| 3 | BanglaTLit | 2024 | Findings of the ACL: EMNLP 2024 | Findings | 2024.findings-emnlp.859 |
| 4 | BhasaBodh | 2025 | Second Workshop on Bangla Language Processing (BLP-2025) | Workshop | 2025.banglalp-1.9 |
| 5 | BLUCK | 2025 | Second Workshop on Bangla Language Processing (BLP-2025) | Workshop | 2025.banglalp-1.14 |
| 6 | BanHate | 2025 | Second Workshop on Bangla Language Processing (BLP-2025) | Workshop | 2025.banglalp-1.19 |
| 7 | BanHateME | 2025 | Second Workshop on Bangla Language Processing (BLP-2025) | Workshop | 2025.banglalp-1.15 |
| 8 | CheckSent-BN | 2025 | Second Workshop on Bangla Language Processing (BLP-2025) | Workshop | 2025.banglalp-1.10 |
| 9 | BanglaTalk | 2025 | Second Workshop on Bangla Language Processing (BLP-2025) | Workshop | 2025.banglalp-1.4 |
| 10 | Reveal-Bangla | 2025 | Second Workshop on Bangla Language Processing (BLP-2025) | Workshop | 2025.banglalp-1.3 |

All papers 4–10 are from the **BLP-2025** workshop, **associated with IJCNLP-AACL 2025** (Mumbai, India, December 2025) — *not* EMNLP 2025.

---

## Verification outcomes & corrections applied

1. **Venue strings.** Replaced the non-official "EMNLP 2025"/"(EMNLP 2025 Workshop)" suffix with the exact ACL Anthology proceedings string. Added `Publication Type` and `Associated Conference` fields. The BLP-2025 workshop is associated with **IJCNLP-AACL 2025**, not EMNLP 2025 (the earlier attribution was wrong).

2. **BanHateME title.** Canonical title now follows ACL Anthology metadata ("…Bangla Memes **thorough** Detection…"); the PDF heading's "**through**" is recorded as a discrepancy in the paper's Verification Status.

3. **Evaluation metrics** (were "Not clearly stated", now verified from PDFs):
   - Paper 3 BanglaTLit → BLEU, ROUGE, METEOR, BERTScore (+ Accuracy/F1 downstream).
   - Paper 6 BanHate → Precision, Recall, F1 (Micro/Macro), Subset Accuracy, Hamming.
   - Paper 7 BanHateME → Precision, Recall, F1, Accuracy.
   - Paper 10 Reveal-Bangla → Accuracy (via NLI verifier).

4. **Dataset sizes corrected:**
   - Paper 4 BhasaBodh → 980 sentences per dialect (was "not clearly stated").
   - Paper 10 Reveal-Bangla → 104 questions / 188 evidence / 355 steps (was "not clearly stated").
   - Paper 8 CheckSent-BN → 11,568 headlines (refined from "~11,500").

5. **Main results enriched** with concrete numbers (papers 3, 6, 7, 9) and nuance (BanHateME: concatenation best for binary; co-attention best for target groups).

6. **Future Work** added for all 10 papers (Paper 6 = "Not clearly stated").

7. **Verification Status** checklist added to every paper.

---

## Off-matrix PDFs in papers/raw/ (not part of Batch 1)

- `Distributed Representations of Words and Phrases.pdf` → out of scope (word2vec, 2013, not Bangla). Logged in rejected-papers.
- `On Evaluation of Bangla Word Analogies.pdf` → Bangla-related but not in matrix; year/venue unverified — candidate for a future batch.

---

## Next

Batch 1 complete. Awaiting approval before starting Batch 2.
