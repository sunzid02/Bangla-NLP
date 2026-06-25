# Batch 2 — Working Record

**Status:** Verified & committed to artifacts (June 2026)
**Papers:** 10 (No. 11–20) | **Verification:** ACL Anthology (metadata) + official PDFs (results)

---

## Papers in this batch

| No | Short name | Year | Official Venue | Type | Assoc. Conf. | ACL Anthology ID |
|----|-----------|------|----------------|------|--------------|------------------|
| 11 | Too Late to Train…? | 2025 | 31st Int'l Conf. on Computational Linguistics (COLING 2025) | Main Conference | COLING 2025 | 2025.coling-main.79 |
| 12 | BengFoS (Literary Companions) | 2025 | 2025 Conf. on EMNLP | Main Conference | EMNLP 2025 | 2025.emnlp-main.941 |
| 13 | BanglaByT5 | 2025 | Findings of the ACL: EMNLP 2025 | Findings | EMNLP 2025 | 2025.findings-emnlp.297 |
| 14 | BanNERD | 2025 | Findings of the ACL: NAACL 2025 | Findings | NAACL 2025 | 2025.findings-naacl.380 |
| 15 | Bengali ChartSumm | 2025 | First Workshop on CHiPSAL (CHiPSAL 2025) | Workshop | COLING 2025 | 2025.chipsal-1.4 |
| 16 | GRASP-ChoQ ⚠ | 2025 | Second Workshop on Bangla Language Processing (BLP-2025) | Workshop | IJCNLP-AACL 2025 | 2025.banglalp-1.2 |
| 17 | Read Between the Lines (BanglaBias) | 2025 | Second Workshop on BLP (BLP-2025) | Workshop | IJCNLP-AACL 2025 | 2025.banglalp-1.5 |
| 18 | BiCap | 2025 | Second Workshop on BLP (BLP-2025) | Workshop | IJCNLP-AACL 2025 | 2025.banglalp-1.6 |
| 19 | P6Jiggasha | 2025 | Second Workshop on BLP (BLP-2025) | Workshop | IJCNLP-AACL 2025 | 2025.banglalp-1.16 |
| 20 | ChakmaBridge ⚠ | 2025 | Second Workshop on BLP (BLP-2025) | Workshop | IJCNLP-AACL 2025 | 2025.banglalp-1.21 |

**Venue diversity:** Unlike Batch 1 (concentrated in BLP-2025), Batch 2 adds COLING 2025 main, EMNLP 2025 main, Findings-EMNLP 2025, Findings-NAACL 2025, and CHiPSAL 2025. Five papers are from the BLP-2025 research track (distinct from Batch 1's BLP papers — no overlap).

- CHiPSAL 2025 co-located with COLING 2025 (Abu Dhabi, UAE, January 2025) — verified from the volume page.
- BLP-2025 associated with IJCNLP-AACL 2025 (Mumbai, India, December 2025).

---

## Verification outcomes & notes

1. **All 10 verified** against ACL Anthology metadata (title/authors/year/exact venue) and against the official PDF for dataset sizes, metrics, results, limitations, and future work.

2. **Publication types** assigned by anthology section, never by conference name: Main Conference (11, 12), Findings (13, 14), Workshop (15–20).

3. **Future Work = "Not clearly stated"** for Papers 13 (BanglaByT5) and 16 (GRASP-ChoQ) — no explicit future-work statement in those PDFs.

4. **Bangla-centrality flags (⚠):**
   - **16 GRASP-ChoQ** — BPDisC is code-mixed Bangla-English; reasoning runs in English after GPT-4o translation; 6/7 eval datasets are non-Bangla. Has Bangla-specific results (F1 93.33 on BPDisC) and is in the Bangla workshop → meets "Bangla is a major part," retained with note.
   - **20 ChakmaBridge** — target language is endangered Chakma; Bangla is a major source/pivot (3 of 5 parallel forms). Meets "Bangla is a major part," retained with note.

5. **Metric-scope note (14 BanNERD):** abstract "81.85% avg macro-F1 across 10 classes" vs §6.1 "84.12% highest average" vs "90.49% on BanNERD" — all reported for different scopes; matrix leads with 90.49% (on BanNERD) + SOTA on 5/6 prior datasets.

6. **Existing-dataset note (18 BiCap):** uses the existing Chitron dataset (Sazzed 2020); the contribution is the captioning method, not the dataset.

---

## Official PDFs added to papers/raw/

All 10 official PDFs downloaded from ACL Anthology:
- Too Late to Train Too Early to Use - Low-Resource Bengali LLMs.pdf
- Can LLMs be Literary Companions - Bengali Figures of Speech (BengFoS).pdf
- BanglaByT5 - Byte-Level Modelling for Bangla.pdf
- BanNERD - Bangla Named Entity Recognition Dataset.pdf
- Bengali ChartSumm - Chart to Text Summarization.pdf
- GRASP-ChoQ - Stance Detection in Political Texts.pdf
- Read Between the Lines - Political Bias in Bangla News.pdf
- BiCap - Bangla Image Captioning.pdf
- P6Jiggasha - Bangla Physics Question Answering.pdf
- ChakmaBridge - Five-Way Parallel Corpus.pdf

---

## Next

Batch 2 complete. Awaiting approval before starting Batch 3.
