# Search Log

Record of searches and verification queries run during the review.

---

## Batch 1 — verification pass (June 2026)

Batch 1 papers were already collected in `artifacts/`. This pass **verified** them against
official sources (ACL Anthology metadata + official PDFs). Source priority per `AGENTS.md` §5.

### ACL Anthology metadata verification (per-paper pages)

| Paper | URL fetched | Verified |
|-------|-------------|----------|
| 1 BenLLM-Eval | https://aclanthology.org/2024.lrec-main.201/ | Title, authors, year, venue, abstract |
| 2 Bias & Context Length | https://aclanthology.org/2024.findings-acl.88/ | Title, authors, year, venue, abstract, DOI |
| 3 BanglaTLit | https://aclanthology.org/2024.findings-emnlp.859/ | Title, authors, year, venue, abstract, DOI |
| 4 BhasaBodh | https://aclanthology.org/2025.banglalp-1.9/ | Title, authors, year, venue, abstract, DOI |
| 5 BLUCK | https://aclanthology.org/2025.banglalp-1.14/ | Title, authors, year, venue, abstract, DOI |
| 6 BanHate | https://aclanthology.org/2025.banglalp-1.19/ | Title, authors, year, venue, abstract, DOI |
| 7 BanHateME | https://aclanthology.org/2025.banglalp-1.15/ | Title, authors, year, venue, abstract, DOI |
| 8 CheckSent-BN | https://aclanthology.org/2025.banglalp-1.10/ | Title, authors, year, venue, abstract, DOI |
| 9 BanglaTalk | https://aclanthology.org/2025.banglalp-1.4/ | Title, authors, year, venue, abstract, DOI |
| 10 Reveal-Bangla | https://aclanthology.org/2025.banglalp-1.3/ | Title, authors, year, venue, abstract, DOI |

### Volume / venue verification

| Query | URL | Finding |
|-------|-----|---------|
| BLP-2025 proceedings volume + co-location | https://aclanthology.org/volumes/2025.banglalp-1/ | "Proceedings of the Second Workshop on Bangla Language Processing (BLP-2025)", **associated with IJCNLP-AACL 2025** (Mumbai, India, December 2025) — NOT EMNLP 2025 |

### Full-text result verification (official PDFs read)

| Paper | PDF source | Items verified from full text |
|-------|-----------|-------------------------------|
| 1 BenLLM-Eval | local + aclanthology PDF | conclusion, future work, limitations |
| 2 Bias | local PDF | conclusion, future work, limitations |
| 3 BanglaTLit | https://aclanthology.org/2024.findings-emnlp.859.pdf | metrics (BLEU/ROUGE/METEOR/BERTScore), best results, limitations, future work |
| 4 BhasaBodh | https://aclanthology.org/2025.banglalp-1.9.pdf | dataset size (980/dialect), BLEU 87.44, limitations, future work |
| 5 BLUCK | https://aclanthology.org/2025.banglalp-1.14.pdf | conclusion, limitations, future work |
| 6 BanHate | https://aclanthology.org/2025.banglalp-1.19.pdf | metrics, best results (LLaMA-3.1-8B LoRA), limitations |
| 7 BanHateME | local PDF (BanHATEme.pdf) | full results tables (F1 74.08 best binary), metrics, limitations, future work |
| 8 CheckSent-BN | https://aclanthology.org/2025.banglalp-1.10.pdf | size (11,568), conclusion, limitations, future work |
| 9 BanglaTalk | https://aclanthology.org/2025.banglalp-1.4.pdf | WER/CER (74.1%/40.6%), MOS, limitations, future work |
| 10 Reveal-Bangla | https://aclanthology.org/2025.banglalp-1.3.pdf | dataset size (104 Qs), metric (Accuracy), limitations, future work |

### Search keywords (per `docs/SEARCH_STRATEGY.md`)
- Keywords: "Bangla", "Bengali" + task terms (hate speech, transliteration, MT, reasoning, ASR, bias, benchmark).
- Year filter: 2024–2026. Target venues first (ACL/EMNLP/NAACL/COLING/EACL/AACL), then workshops.

### Notes
- No new candidate searches for Batch 2 were run in this pass (verification-only).

---

## Batch 2 — search + verification pass (June 2026)

Goal: find 10 new papers (No. 11–20), distinct from Batch 1, with deliberate **venue diversification** beyond the BLP-2025 workshop. Source priority per `AGENTS.md` §5.

### Search queries run
| Source | Query | Keywords | Purpose |
|--------|-------|----------|---------|
| ACL Anthology (volume) | BLP-2025 volume listing | "Bangla", "Bengali" | Enumerate unused BLP-2025 research-track papers |
| Web (site:aclanthology.org) | "Bangla OR Bengali NLP ACL EMNLP NAACL COLING 2025 dataset" | "Bangla", "Bengali" | Surface main-conf / Findings candidates |
| Web (site:aclanthology.org) | "Bengali Bangla 2025 findings naacl coling main conference" | "Bangla", "Bengali" | Surface Findings/main candidates |

Year filter: 2024–2026. Target venues first (ACL/EMNLP/NAACL/COLING/EACL/AACL), then workshops.

### ACL Anthology metadata verification (per-paper pages)
| Paper | URL fetched | Verified |
|-------|-------------|----------|
| 11 Too Late to Train…? | https://aclanthology.org/2025.coling-main.79/ | Title, authors, year, venue, abstract |
| 12 BengFoS | https://aclanthology.org/2025.emnlp-main.941/ | Title, authors, year, venue, abstract |
| 13 BanglaByT5 | https://aclanthology.org/2025.findings-emnlp.297/ | Title, authors, year, venue, abstract |
| 14 BanNERD | https://aclanthology.org/2025.findings-naacl.380/ | Title, authors, year, venue, abstract |
| 15 Bengali ChartSumm | https://aclanthology.org/2025.chipsal-1.4/ | Title, authors, year, venue, abstract |
| 16 GRASP-ChoQ | https://aclanthology.org/2025.banglalp-1.2/ | Title, authors, year, venue (volume listing) |
| 17 BanglaBias | https://aclanthology.org/2025.banglalp-1.5/ | Title, authors, year, venue (volume listing) |
| 18 BiCap | https://aclanthology.org/2025.banglalp-1.6/ | Title, authors, year, venue (volume listing) |
| 19 P6Jiggasha | https://aclanthology.org/2025.banglalp-1.16/ | Title, authors, year, venue (volume listing) |
| 20 ChakmaBridge | https://aclanthology.org/2025.banglalp-1.21/ | Title, authors, year, venue (volume listing) |

### Volume / venue verification
| Query | URL | Finding |
|-------|-----|---------|
| CHiPSAL 2025 co-location | https://aclanthology.org/volumes/2025.chipsal-1/ | "Proceedings of the First Workshop on Challenges in Processing South Asian Languages (CHiPSAL 2025)", **co-located with COLING 2025** (Abu Dhabi, UAE, January 2025) |
| BLP-2025 volume | https://aclanthology.org/volumes/2025.banglalp-1/ | Confirms IDs/titles/authors for papers 16, 17, 18, 19, 20 |

### Full-text result verification (official PDFs read)
All 10 official PDFs downloaded to `papers/raw/` and text-extracted; verified dataset, metrics, main results, limitations, and future work from full text:
| Paper | PDF source | Items verified from full text |
|-------|-----------|-------------------------------|
| 11 Too Late to Train | aclanthology 2025.coling-main.79.pdf | tasks, datasets, metrics, per-task results, tokenization stat, limitations, future work |
| 12 BengFoS | aclanthology 2025.emnlp-main.941.pdf | dataset size/poets/labels, zero-shot + fine-tune + probing results, limitations, future work |
| 13 BanglaByT5 | aclanthology 2025.findings-emnlp.297.pdf | 14 GB corpus, params, downstream scores, baselines, limitations (future work absent) |
| 14 BanNERD | aclanthology 2025.findings-naacl.380.pdf | 85,175 sentences/29 domains/10 classes/IAA 0.88, 90.49% macro-F1, SOTA 5/6, limitations, future work |
| 15 Bengali ChartSumm | aclanthology 2025.chipsal-1.4.pdf | 4,100 charts, mT5/BanglaT5/Gemma scores, limitations, future work |
| 16 GRASP-ChoQ | aclanthology 2025.banglalp-1.2.pdf | BPDisC 2,847 (Bangla-English), F1 93.33, limitations (future work absent), Bangla-centrality |
| 17 BanglaBias | aclanthology 2025.banglalp-1.5.pdf | 200 articles/ternary labels, 28-LLM results, limitations, future work |
| 18 BiCap | aclanthology 2025.banglalp-1.6.pdf | Chitron 15,438 (existing), BLEU-4 32.73, human eval, limitations, future work |
| 19 P6Jiggasha | aclanthology 2025.banglalp-1.16.pdf | 1,500 MCQs, Acc@k results, cross-lingual analysis, limitations, future work |
| 20 ChakmaBridge | aclanthology 2025.banglalp-1.21.pdf | 807 sentences/5 forms, NLLB-200 BLEU 0.5228, limitations, future work, Bangla role |

### Candidates surfaced but NOT selected this batch (future-batch pool)
- bnContextQA (2025.banglalp-1.29), BOIGENRE (2025.banglalp-1.20), subjectivity detection (2025.banglalp-1.11), Gen-mABSA-T5 (2025.banglalp-1.12), summarization (2025.banglalp-1.13), depression detection code-mixed (2025.banglalp-1.8), several Sylheti/Chittagonian dialect MT papers (2025.banglalp-1.18/.22/.24/.26).
- MDC3 (multimodal commercial content classification, Findings) and Bengali figurative/literary candidates — to verify in a later batch.
- BanglaSTEM — appears to be an arXiv preprint; **not** selected (preprint without confirmed peer-reviewed venue).
