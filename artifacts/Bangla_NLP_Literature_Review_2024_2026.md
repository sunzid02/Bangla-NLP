# Recent Work in Bangla NLP (2024–2026): Literature Review

**MSc Thesis — Bangla NLP Literature Review**
**Author:** Sarker Sunzid Mahmud | TU Dortmund
**Last updated:** June 2026 | Batches 1–2 — 20 papers (verified against ACL Anthology + official PDFs)

---

## 1. Search Strategy

- **Primary source:** ACL Anthology (aclanthology.org) — keywords: "Bangla", "Bengali", "NLP", "language model", "low-resource". Year filter: 2024–2026.
- **Secondary:** Google Scholar and Semantic Scholar for cross-checking and gap-filling.
- **Target venues:** ACL, EMNLP, NAACL, COLING, EACL, AACL. Workshop papers accepted if at a target-venue workshop (e.g., BLP-2025, associated with IJCNLP-AACL 2025).
- **Batch size:** 10 papers per batch. Review required after each batch before proceeding.

---

## 2. Inclusion and Exclusion Criteria

**Include:**
- Published 2024–2026
- Bangla/Bengali is primary or major language in the study
- Peer-reviewed venue (target venues preferred; others accepted if high quality)
- Verifiable source link (ACL Anthology preferred)

**Exclude:**
- Papers where Bangla is only mentioned in passing
- Preprints without peer review (flagged if included as exception)
- Duplicate entries
- Papers with no verifiable source link

---

## 3. Literature Matrix — Batch 1

| No | Title | Year | Venue | Type | Problem | Task | Dataset | Method | Main Result | Limitation |
|----|-------|------|-------|------|---------|------|---------|--------|-------------|------------|
| 1 | BenLLM-Eval | 2024 | LREC-COLING | Main Conf. | LLMs not benchmarked on Bengali | Multi-task eval | Custom (6 tasks) | ChatGPT, LLaMA-2, Claude-2 (zero-shot) | LLMs underperform fine-tuned models on most tasks; LLaMA-2 worst | Zero-shot only; 3 LLMs tested |
| 2 | Bias & Context Length for Bangla | 2024 | Findings-ACL | Findings | Social bias in Bangla LMs unstudied | Bias measurement | New Bangla gender bias dataset | Adapted WEAT/SEAT metrics | Bias metrics depend on context length | Gender bias only; intrinsic measures only |
| 3 | BanglaTLit | 2024 | Findings-EMNLP | Findings | Romanized Bangla untapped; no back-transliteration benchmark | Transliteration | BanglaTLit 42.7k; BanglaTLit-PT 245.7k | TB-encoders + dual encoder-decoder (T5) | Best BLEU 36.07 / ROUGE-1 78.92; SOTA on romanized classification | Single-domain source (TrickBd); noisy text |
| 4 | BhasaBodh | 2025 | BLP-2025 | Workshop | Bangla dialects (Chittagong/Sylhet) underserved in MT | Machine Translation | 980 sentences/dialect, multi-way parallel | Fine-tuned NLLB-200, mBART-50 | BLEU 87.44 on Romanized→Standard; mBART-50 best | Modest scale; synthetic romanized data; 2 dialects |
| 5 | BLUCK | 2025 | BLP-2025 | Workshop | No LLM benchmark for Bengali cultural/linguistic knowledge | MCQ Benchmark / QA | BLUCK 2,366 MCQs (23 categories) | GPT-4o, Claude-3.5, Gemini, LLaMA, DeepSeek | LLMs weak in Bengali phonetics; below English | Text-only MCQ; no open-ended evaluation |
| 6 | BanHate | 2025 | BLP-2025 | Workshop | Outdated, narrow Bangla hate speech resources | Hate Speech Detection | BanHate 19,203 YouTube comments | Prompting + LoRA fine-tuning on LLMs | LoRA best; LLaMA-3.1-8B F1 ~84–86; implicit hate hard | YouTube only; single LoRA epoch |
| 7 | BanHateME | 2025 | BLP-2025 | Workshop | No multimodal Bangla hate meme dataset | Multimodal Hate Detection | BanHateME 3,819 memes (3-level annotations) | LM+vision fusion (sum/concat/co-attention) + hierarchical loss | BanglaBERT+Swin concat best binary (F1 74.08); co-attention best for targets | Modest dataset; cultural cues hard |
| 8 | CheckSent-BN | 2025 | BLP-2025 | Workshop | No Bengali dataset for claim checkworthiness + sentiment | Fact-check + Sentiment (MTL) | CheckSent-BN 11,568 news headlines | IndicBERTv2, BanglaBERT, mDeBERTa (STL/MTL) | IndicBERTv2 best in MTL setting | LLM-annotated; West-Bengal only; class imbalance |
| 9 | BanglaTalk | 2025 | BLP-2025 | Workshop | No real-time Bengali dialect speech assistant | ASR / Speech System | RegSpeech12 (12 regions; 10 trained) | BRDialect: IndicWav2Vec + RTP + VITS TTS | WER ↓ 12.41–33.98% (abs WER 74.1%); 4.9s delay at 24 kbps | 4.9s latency; only 10/12 regions trained |
| 10 | Reveal-Bangla | 2025 | BLP-2025 | Workshop | Multi-step reasoning in Bangla unevaluated | Multi-step Reasoning / QA | Reveal-Bangla: 104 Qs, 188 evidence, 355 steps | Eval of ~1B SLMs (EngLlama, BenLlama) | Models underuse Bangla reasoning steps; context helps non-binary Qs | Small set; only small models; single-annotator translation |

---

## 3b. Literature Matrix — Batch 2

| No | Title | Year | Venue | Type | Problem | Task | Dataset | Method | Main Result | Limitation |
|----|-------|------|-------|------|---------|------|---------|--------|-------------|------------|
| 11 | Too Late to Train…? | 2025 | COLING 2025 | Main Conf. | Is a dedicated Bengali LLM still needed? | Multi-task LLM eval | Existing Bengali test sets (8 tasks) | Zero-shot LLMs vs fine-tuned BanglaT5/BanglaBERT; QLoRA LLaMA-3-8B | LLMs win QA/reasoning; BanglaT5 wins paraphrase (BLEU 32.80)/summ; Bengali tokenization inefficient | No human eval; FT limited to LLaMA-3-8B |
| 12 | BengFoS (Literary Companions) | 2025 | EMNLP 2025 | Main Conf. | Bengali figures-of-speech identification unexplored | Multi-label FoS classification | BengFoS 3,148 sentences, 6 poets, 13 labels | Zero-shot + fine-tuned Llama-3/DeepSeek-R1; probing | Best DeepSeek-R1-7B (16-bit) weighted-F1 0.64; gains modest | 6-poet skew; class imbalance |
| 13 | BanglaByT5 | 2025 | Findings-EMNLP | Findings | Subword tokenizers fragment morphologically rich Bangla | Byte-level LM (gen + classification) | 14 GB corpus (VACASPATI + IndicCorp-bn) | BanglaByT5 (~300M, byte-level ByT5) | Beats IndicBART/BanglaT5/BLOOM-1.1B; within ~5% of GPT2-XL at ~5x smaller | Limited 14 GB data; small variant |
| 14 | BanNERD | 2025 | Findings-NAACL | Findings | Bangla NER lacks large quality datasets | Named Entity Recognition | BanNERD 85,175 sentences, 29 domains, 10 classes, IAA 0.88 | BanNERCEM (per-context ensemble) + PLM-CRF | 90.49% macro-F1 on BanNERD; SOTA on 5/6 prior datasets | Per-context passing slow; CW labels weak |
| 15 | Bengali ChartSumm | 2025 | CHiPSAL 2025 | Workshop | No Bengali chart-to-text summarization benchmark | Chart-to-text summarization | Bengali ChartSumm 4,100 chart images + metadata + summaries | mT5, BanglaT5, Gemma-2b fine-tuned | mT5 best BLEU 0.2779/lowest error; BanglaT5 best ROUGE-1 0.0678 | Only bar/line charts; limited compute |
| 16 | GRASP-ChoQ ⚠ | 2025 | BLP-2025 | Workshop | Political stance detection in Bangladesh context unstudied | Political stance detection | BPDisC 2,847 Bangla-English tweets (+6 non-Bangla sets) | KG retrieval (Neo4j) + Chain-of-Questions over LLMs | DeepSeek-R1+GRASP-ChoQ F1 93.33 (+40.6 vs zero-shot) | Text-only; no FT; reasoning done in English |
| 17 | Read Between the Lines (BanglaBias) | 2025 | BLP-2025 | Workshop | Bangla political-bias datasets scarce | Political bias (ternary stance) | BanglaBias 200 articles, 46 events, 54 sources | Eval of 28 LLMs (zero/few-shot, reasoning prompt) | Best Qwen3-235B weighted-F1 0.74; "Neutral" hardest (F1↓0.00) | Small corpus; contamination risk; text-only |
| 18 | BiCap | 2025 | BLP-2025 | Workshop | Bangla image captioning limited; no VL models | Image captioning | Chitron (existing) 15,438 image-caption pairs | ResNet-50 + Bahdanau attention + LSTM | BLEU-4 32.73 (+10 over strongest baseline); best human scores | Local-only features; sequential LSTM |
| 19 | P6Jiggasha | 2025 | BLP-2025 | Workshop | LLMs on Bangla physics QA + cross-lingual consistency unmeasured | Physics QA (MCQ) / benchmark | P6Jiggasha 1,500 Bangla physics MCQs (+English) | GPT-4.1, Gemini-2.5-Pro, DeepSeek-R1; zero-shot/CoT | GPT-4.1 best Bangla Acc@1 86.67%; near-identical Bangla vs English | MCQ-only; no diagrams; physics-only |
| 20 | ChakmaBridge ⚠ | 2025 | BLP-2025 | Workshop | Endangered Chakma lacks parallel corpora (Bangla as pivot) | Parallel corpus + MT | ChakmaBridge 807 sentences, 5 parallel forms | mBART-50, NLLB-200 fine-tuned; Gemini romanization | (Eng+Bangla)→Chakma NLLB-200 BLEU 0.5228 (+124% over next-best) | 807 sentences; clean LLM romanization; 20-sentence validation |

⚠ Bangla-centrality flag — 16 (BPDisC is code-mixed Bangla-English; reasoning runs in English after translation; 6/7 eval datasets non-Bangla) and 20 (target language is endangered **Chakma**; Bangla is a major source/pivot, 3 of 5 parallel forms). Both retain Bangla-specific datasets/results and are published in the Bangla workshop, so both meet "Bangla is a major part," flagged here for transparency.

---

## 4. Topic-wise Grouping

| Topic | Papers |
|-------|--------|
| Safety & Content Moderation | 6 (BanHate), 7 (BanHateME), 8 (CheckSent-BN) |
| LLM Evaluation & Benchmarks | 1 (BenLLM-Eval), 5 (BLUCK), 11 (Too Late to Train), 19 (P6Jiggasha) |
| Machine Translation (Dialectal / Endangered) | 4 (BhasaBodh), 20 (ChakmaBridge) |
| Transliteration | 3 (BanglaTLit) |
| Bias & Fairness | 2 (Bias & Context Length), 17 (BanglaBias) |
| Speech Recognition | 9 (BanglaTalk) |
| Reasoning / QA | 10 (Reveal-Bangla), 19 (P6Jiggasha) |
| Named Entity Recognition | 14 (BanNERD) |
| Language Models / Pretraining | 13 (BanglaByT5) |
| Summarization | 15 (Bengali ChartSumm) |
| Stance / Political NLP | 16 (GRASP-ChoQ), 17 (BanglaBias) |
| Figurative & Literary NLP | 12 (BengFoS) |
| Multimodal / Vision-Language | 7 (BanHateME), 18 (BiCap) |

---

## 5. Year-wise Trend

| Year | Papers | Key Themes |
|------|--------|------------|
| 2024 | 3 | LLM evaluation, bias measurement, transliteration |
| 2025 | 17 | Safety/hate speech, LLM benchmarks, dialectal & endangered NLP, speech, reasoning, NER, byte-level LM, summarization, stance/bias, figurative & multimodal NLP |
| 2026 | 0 (Batches 1–2) | — |

2025 dominates, driven both by the BLP-2025 workshop (associated with IJCNLP-AACL 2025) and by 2025 main-conference / Findings tracks (COLING, EMNLP, NAACL). Safety, LLM benchmarking, and dialectal/low-resource NLP are recurring themes. *(The total BLP-2025 paper count is not yet independently verified — see remaining-verification notes.)*

---

## 6. Venue-wise Distribution

| Official Venue | Publication Type | Year | Papers |
|----------------|------------------|------|--------|
| LREC-COLING 2024 | Main Conference | 2024 | 1 |
| Findings of the ACL: ACL 2024 | Findings | 2024 | 1 |
| Findings of the ACL: EMNLP 2024 | Findings | 2024 | 1 |
| 31st Int'l Conf. on Computational Linguistics (COLING 2025) | Main Conference | 2025 | 1 |
| 2025 Conf. on Empirical Methods in NLP (EMNLP 2025) | Main Conference | 2025 | 1 |
| Findings of the ACL: EMNLP 2025 | Findings | 2025 | 1 |
| Findings of the ACL: NAACL 2025 | Findings | 2025 | 1 |
| First Workshop on Challenges in Processing South Asian Languages (CHiPSAL 2025) | Workshop | 2025 | 1 |
| Second Workshop on Bangla Language Processing (BLP-2025) | Workshop | 2025 | 12 |

*The BLP-2025 workshop is associated with IJCNLP-AACL 2025 (Mumbai, India, December 2025). CHiPSAL 2025 is co-located with COLING 2025 (Abu Dhabi, UAE, January 2025). "EMNLP 2025" used as a BLP venue in earlier drafts was incorrect and has been removed.*

---

## 7. Research Problems Studied

1. LLM capability evaluation on Bangla NLP tasks (multi-task zero-shot benchmarking)
2. Social/gender bias measurement in Bangla pretrained language models
3. Back-transliteration of romanized Bangla to standard script
4. Dialectal machine translation (Chittagong/Sylhet ↔ Standard Bangla / English)
5. Cultural and linguistic knowledge benchmarking for LLMs in Bengali
6. Text-based hate speech detection (binary + fine-grained + target identification)
7. Multimodal hate detection in Bangla memes (text + image)
8. Joint claim checkworthiness detection + sentiment analysis in Bengali news
9. Real-time dialect-aware automatic speech recognition for Bengali
10. Cross-lingual multi-step reasoning evaluation in Bangla
11. Necessity/viability of a dedicated Bengali LLM vs English-centric LLMs (7-task evaluation)
12. Figures-of-speech (figurative language) identification in Bengali literature
13. Byte-level language modelling for morphologically rich Bangla
14. Large-scale, validated Bangla Named Entity Recognition and context-driven NER
15. Bengali chart-to-text summarization
16. Political stance detection in Bangladeshi political discourse
17. Political bias detection in Bangla news (ternary stance)
18. Bangla image captioning (multimodal generation)
19. LLM benchmarking on Bangla physics QA with cross-lingual consistency
20. Parallel-corpus construction and MT for the endangered Chakma language (Bangla as pivot)

---

## 8. Common Datasets (Introduced / Used)

**Batch 1**

| Dataset | Paper | Size | Task |
|---------|-------|------|------|
| BanglaTLit | Paper 3 | 42.7k pairs (38.7k/1.5k/2.5k) | Transliteration |
| BanglaTLit-PT | Paper 3 | 245.7k | Pre-training corpus |
| Bangla gender bias dataset | Paper 2 | Not clearly stated | Bias measurement |
| BhasaBodh corpus | Paper 4 | 980 sentences/dialect (multi-way parallel) | Dialectal MT |
| BLUCK | Paper 5 | 2,366 MCQs, 23 categories | Cultural/linguistic QA |
| BanHate | Paper 6 | 19,203 YouTube comments | Hate speech detection |
| BanHateME | Paper 7 | 3,819 memes (2,673/381/765) | Multimodal hate detection |
| CheckSent-BN | Paper 8 | 11,568 news headlines | Fact-check + sentiment |
| RegSpeech12 | Paper 9 | 12 regions (10 used for training) | Dialect ASR |
| Reveal-Bangla | Paper 10 | 104 questions, 188 evidence, 355 steps | Multi-step reasoning |

**Batch 2** *(new datasets introduced; † = existing dataset reused)*

| Dataset | Paper | Size | Task |
|---------|-------|------|------|
| BengFoS | Paper 12 | 3,148 annotated sentences (6 poets, 13 labels) | Figures-of-speech classification |
| BanglaByT5 corpus | Paper 13 | 14 GB (VACASPATI + IndicCorp-bn) | Byte-level LM pre-training |
| BanNERD | Paper 14 | 85,175 sentences, 29 domains, 10 classes | Named Entity Recognition |
| Bengali ChartSumm | Paper 15 | 4,100 chart images + metadata + summaries | Chart-to-text summarization |
| BPDisC | Paper 16 | 2,847 Bangla-English tweets | Political stance detection |
| BanglaBias | Paper 17 | 200 news articles (46 events, 54 sources) | Political bias (ternary stance) |
| Chitron † | Paper 18 | 15,438 image-caption pairs | Image captioning |
| P6Jiggasha | Paper 19 | 1,500 physics MCQs (+English) | Physics QA |
| ChakmaBridge | Paper 20 | 807 sentences, 5 parallel forms | Endangered-language MT |

---

## 9. Common Models and Methods

**Encoder models:** BanglaBERT, IndicBERTv2, MuRIL, mDeBERTa, BanglishBERT, XLM-RoBERTa, BERT-CRF (NER)

**Generative LLMs:** ChatGPT (GPT-3.5), LLaMA-2, Claude-2, GPT-4 / GPT-4o / GPT-4.1, Claude-3.5-Sonnet / Claude-Sonnet-4, Gemini-1.5-Pro / Gemini-2.5-Pro / Gemini-2.5-Flash, LLaMA-3-8B/70B, LLaMA-3.1-8B, LLaMA-3.3-70B, Qwen-2/2.5/3 (up to 235B), Gemma-2b/3-12B, Phi-4-14B, Mistral-7B/Large, DeepSeekV3, DeepSeek-R1 (& Distill-Llama-70B), Aya-23, GLM, TigerLLM

**Seq2Seq / byte-level / MT models:** mBART-50, NLLB-200, mT5, BanglaT5, ByT5 / **BanglaByT5**, IndicBART, BLOOM, GPT-2, Paramanu

**Speech models:** IndicWav2Vec (fine-tuned → BRDialect), VITS-Bengali (TTS)

**Vision / multimodal:** ViT, Swin Transformer, ResNet-50 (+ Bahdanau attention + LSTM)

**Adaptation / inference methods:** LoRA / QLoRA fine-tuning, zero-shot & few-shot prompting, Chain-of-Thought / Chain-of-Questions reasoning, multi-task learning (MTL), further pre-training, hierarchical loss, knowledge-graph retrieval augmentation (Neo4j), context-ensemble + entity-aware voting (BanNERCEM), layer-wise linear probing

**Bias methods:** Adapted WEAT/SEAT intrinsic bias metrics for Bangla

---

## 10. Research Gaps

| Gap Type | Description | Relevant Papers |
|----------|-------------|-----------------|
| Dataset Gap | NER now addressed by BanNERD (Batch 2); coreference, dialogue, and math reasoning still lack large-scale data; dialectal data remains scarce | 4, 10, 14 |
| Benchmark Gap | No unified multi-task Bangla benchmark comparable to GLUE/SuperGLUE; task-specific benchmarks proliferating (cultural, physics, chart, stance, NER) but not unified | 1, 5, 11, 15, 17, 19 |
| Model Gap | Still no dedicated Bangla instruction-tuned LLM; Paper 11 argues a Bengali-oriented LLM is needed; BanglaByT5 (13) is a byte-level step but small | 1, 5, 11, 13 |
| Tokenization Gap | English-centric subword tokenizers are inefficient/fragmenting for Bangla script (a cross-cutting bottleneck) | 11, 13 |
| Evaluation Gap | Inconsistent metrics across papers; no standard Bangla eval protocol; bias lacks extrinsic evaluation; cross-lingual answer inconsistency | 2, 6, 7, 10, 19 |
| Low-Resource / Dialect / Endangered Gap | Only Chittagong/Sylhet covered for dialects; endangered Chakma only just addressed; diaspora Bangla ignored | 4, 9, 20 |
| Domain Gap | Scientific (physics) QA now started (P6Jiggasha); medical, legal, financial domains still absent | 11, 19 |
| Multimodal Gap | Multimodal Bangla still thin — only hateful memes (7) and image captioning (18); no Bangla VLM, VQA, or chart-image (vs metadata) understanding | 7, 15, 18 |
| Practical Deployment Gap | Only BanglaTalk is a deployed system; most papers produce datasets/models without real-world deployment | 9 |

---

## 11. Possible Thesis Directions

1. **Unified Bangla Benchmark:** Build a multi-task evaluation suite (NLU, generation, reasoning, cultural knowledge) — fill the GLUE-equivalent gap for Bangla.
2. **Instruction-Tuned Bangla LLM:** Fine-tune an open-source LLM (LLaMA/Mistral) on Bangla instruction data; evaluate on BenLLM-Eval and BLUCK.
3. **Dialectal NLP Expansion:** Extend BhasaBodh to more dialects; build cross-dialect NLU or MT pipeline beyond Chittagong/Sylhet.
4. **Bias Mitigation:** Build on the Findings-ACL 2024 bias paper to study intersectional bias (gender × religion × dialect) and propose debiasing strategies.
5. **Domain-Specific NLP:** First Bangla NLP corpus and models for medical or legal domains — a clear, unoccupied research gap.
6. **Multimodal Bangla NLP:** Extend BanHateME approach to other multimodal tasks (visual QA, image captioning) using low-resource multimodal data.

---

## 12. Paper-by-Paper Summaries

---

### Paper 1 — BenLLM-Eval

| Field | Details |
|-------|---------|
| **Title** | BenLLM-Eval: A Comprehensive Evaluation into the Potentials and Pitfalls of Large Language Models on Bengali NLP |
| **Authors** | Mohsinul Kabir, Mohammed Saidul Islam, Md Tahmid Rahman Laskar, Mir Tafseer Nayeem, M Saiful Bari, Enamul Hoque |
| **Year** | 2024 |
| **Official Venue** | Proceedings of the 2024 Joint International Conference on Computational Linguistics, Language Resources and Evaluation (LREC-COLING 2024) |
| **Publication Type** | Main Conference |
| **Link** | https://aclanthology.org/2024.lrec-main.201/ |
| **Problem** | LLMs evaluated mostly in English; no systematic Bangla NLP benchmark existed. |
| **Task Type** | Multi-task evaluation: summarization, QA, paraphrasing, NLI, text classification, sentiment analysis |
| **Dataset** | Custom evaluation set across 6 Bengali NLP tasks (specific dataset names not clearly stated) |
| **Method / Model** | Zero-shot evaluation of ChatGPT (GPT-3.5), LLaMA-2-13b-chat, Claude-2 |
| **Evaluation Metric** | Task-specific: ROUGE, F1, Accuracy, BLEU |
| **Main Result** | Zero-shot LLMs match/exceed SOTA on a few tasks (e.g., sentiment) but underperform fine-tuned models on most; LLaMA-2 worst overall |
| **Contribution** | First comprehensive zero-shot LLM benchmark for Bengali NLP across 6 diverse tasks; includes task-contamination analysis |
| **Limitation** | Zero-shot only; only 3 LLMs; no instruction-tuned/fine-tuned LLM comparison; undisclosed LLM training data limits contamination check |
| **Future Work** | Expand experiments to additional low/modest-resource languages, tasks, datasets, and settings |

**Verification Status:** Title ✓ · Authors ✓ · Year ✓ · Official venue ✓ · Publication type ✓ · ACL URL ✓ · PDF checked ✓ · Dataset ✓ · Metrics ✓ · Results ✓ · Limitation ✓

**বিগিনার বাংলায় সারসংক্ষেপ:**
এই গবেষণায় দেখা হয়েছে যে ChatGPT, LLaMA-2 এবং Claude-2 এর মতো বড় ভাষা মডেলগুলো বাংলায় কতটা ভালো কাজ করতে পারে। গবেষকরা ছয়টি কাজের (যেমন: সারাংশ লেখা, প্রশ্নোত্তর, sentiment বিশ্লেষণ) উপর zero-shot পরীক্ষা করেছেন — অর্থাৎ মডেলকে কোনো উদাহরণ না দিয়ে সরাসরি প্রশ্ন করা হয়েছে। ফলাফলে দেখা গেছে যে বেশিরভাগ কাজে এই মডেলগুলো বর্তমান সেরা পদ্ধতির চেয়ে অনেক পিছিয়ে, বিশেষত LLaMA-2 সবচেয়ে দুর্বল। এই পেপারটি আমার thesis-এর জন্য গুরুত্বপূর্ণ কারণ এটি বাংলায় LLM-এর দুর্বলতাগুলো স্পষ্টভাবে চিহ্নিত করে এবং আরো গবেষণার প্রয়োজনীয়তা দেখায়।

---

### Paper 2 — Bias & Context Length for Bangla

| Field | Details |
|-------|---------|
| **Title** | An Empirical Study on the Characteristics of Bias upon Context Length Variation for Bangla |
| **Authors** | Jayanta Sadhu, Ayan Khan, Abhik Bhattacharjee, Rifat Shahriyar |
| **Year** | 2024 |
| **Official Venue** | Findings of the Association for Computational Linguistics: ACL 2024 |
| **Publication Type** | Findings |
| **Link** | https://aclanthology.org/2024.findings-acl.88/ |
| **Problem** | Social bias in Bangla pretrained LMs unstudied; impact of context length on bias measurement unexplored. |
| **Task Type** | Bias measurement / Fairness |
| **Dataset** | New Bangla intrinsic gender bias dataset (created in this work; size not clearly stated) |
| **Method / Model** | Adapted WEAT/SEAT intrinsic bias metrics for Bangla; context length variation experiments |
| **Evaluation Metric** | Intrinsic bias metrics (WEAT/SEAT effect sizes) |
| **Main Result** | Bias metrics show clear dependency on context length — a factor overlooked in prior work |
| **Contribution** | First Bangla gender bias dataset; novel finding that context length affects bias measurement |
| **Limitation** | Only gender bias; only intrinsic measures; datasets adapted/synthetic; no extrinsic downstream evaluation |
| **Future Work** | Study bias in downstream applications; develop language-specific debiasing; extend to generative models and to other bias types (social, religious, political) |

**Verification Status:** Title ✓ · Authors ✓ · Year ✓ · Official venue ✓ · Publication type ✓ · ACL URL ✓ · PDF checked ✓ · Dataset ✓ · Metrics ✓ · Results ✓ · Limitation ✓

**বিগিনার বাংলায় সারসংক্ষেপ:**
এই পেপারে গবেষকরা বাংলা ভাষার language model-এ লিঙ্গভিত্তিক পক্ষপাত (gender bias) কতটুকু আছে তা পরিমাপ করেছেন। তারা প্রথমবার বাংলার জন্য একটি gender bias dataset তৈরি করেছেন এবং WEAT/SEAT পদ্ধতিকে বাংলার উপযোগী করেছেন। সবচেয়ে গুরুত্বপূর্ণ আবিষ্কার হলো: context-এর দৈর্ঘ্য বদলালে bias পরিমাপের ফলাফলও বদলে যায় — আগের কোনো গবেষণায় এটি দেখা যায়নি। আমার thesis-এর জন্য এটি দরকারী কারণ এটি বাংলায় fairness গবেষণার ভিত্তি স্থাপন করেছে।

---

### Paper 3 — BanglaTLit

| Field | Details |
|-------|---------|
| **Title** | BanglaTLit: A Benchmark Dataset for Back-Transliteration of Romanized Bangla |
| **Authors** | Md Fahim, Fariha Tanjim Shifat, Fabiha Haider, Deeparghya Dutta Barua, MD Sakib Ul Rahman Sourove, Md Farhan Ishmam, Md Farhad Alam Bhuiyan |
| **Year** | 2024 |
| **Official Venue** | Findings of the Association for Computational Linguistics: EMNLP 2024 |
| **Publication Type** | Findings |
| **Link** | https://aclanthology.org/2024.findings-emnlp.859/ |
| **Problem** | Romanized Bangla is abundant on the internet but untapped; no large-scale back-transliteration benchmark existed. |
| **Task Type** | Transliteration / Back-transliteration |
| **Dataset** | BanglaTLit: 42.7k samples (38.7k/1.5k/2.5k train/val/test); BanglaTLit-PT pre-training corpus: 245.7k samples |
| **Method / Model** | TB-Encoders (encoders further pre-trained on BanglaTLit-PT) + dual encoder-decoder (TB-encoder-aggregated T5) |
| **Evaluation Metric** | BLEU, ROUGE, METEOR, BERTScore (back-transliteration); Accuracy/F1 (downstream romanized classification) |
| **Main Result** | Best model TB-XLM_R + BanglaT5_NMT: BLEU 36.07, ROUGE-1 78.92, METEOR 78.14, BERTScore 98.82; TB-encoders reach SOTA on romanized Bangla classification |
| **Contribution** | Largest Bangla transliteration dataset; SOTA romanized Bangla encoders; novel dual encoder-decoder; open code and data |
| **Limitation** | Source data (TrickBd) is single-domain (tech-support); informal romanized text is noisy |
| **Future Work** | Expand dataset for training larger models / fine-tuning LLMs; transliteration of Bangla regional dialects; parameter-efficient fine-tuning of LLMs |

**Verification Status:** Title ✓ · Authors ✓ · Year ✓ · Official venue ✓ · Publication type ✓ · ACL URL ✓ · PDF checked ✓ · Dataset ✓ · Metrics ✓ · Results ✓ · Limitation ✓ — *Note: the earlier "evaluation metric not clearly stated" was incorrect; the paper reports BLEU/ROUGE/METEOR/BERTScore.*

**বিগিনার বাংলায় সারসংক্ষেপ:**
ইন্টারনেটে অনেক মানুষ বাংলা ভাষা রোমান হরফে লেখেন (যেমন: "ami bhalo achi")। এই পেপারে গবেষকরা এই রোমান বাংলাকে আবার বাংলা script-এ রূপান্তর করার জন্য BanglaTLit নামে ৪২,৭০০টি sample-এর একটি বড় dataset তৈরি করেছেন। তারা একটি encoder-decoder model তৈরি করেছেন যা এই কাজে state-of-the-art ফলাফল দিয়েছে। এই গবেষণাটি আমার thesis-এর জন্য গুরুত্বপূর্ণ কারণ রোমান বাংলার data ব্যবহার করে বাংলা NLP-এর data scarcity সমস্যা কমানো যেতে পারে।

---

### Paper 4 — BhasaBodh

| Field | Details |
|-------|---------|
| **Title** | BhasaBodh: Bridging Bangla Dialects and Romanized Forms through Machine Translation |
| **Authors** | Md. Tofael Ahmed Bhuiyan, Md. Abdur Rahman, Abdul Kadar Muhammad Masum |
| **Year** | 2025 |
| **Official Venue** | Proceedings of the Second Workshop on Bangla Language Processing (BLP-2025) |
| **Publication Type** | Workshop |
| **Associated Conference** | IJCNLP-AACL 2025 (Mumbai, India, December 2025) |
| **Link** | https://aclanthology.org/2025.banglalp-1.9/ |
| **Problem** | Bangla dialects (Chittagong, Sylhet) and romanized forms severely underserved in MT; no sentence-level benchmark existed. |
| **Task Type** | Machine Translation (dialectal + romanized) |
| **Dataset** | Multi-way sentence-level parallel corpus: 980 sentences per dialect (Chittagong, Sylhet) aligned with Standard Bangla and English, plus romanized versions |
| **Method / Model** | Fine-tuned NLLB-200 and mBART-50 on 7 translation tasks |
| **Evaluation Metric** | BLEU |
| **Main Result** | mBART-50 outperforms NLLB-200 on most tasks; best BLEU 87.44 on Romanized-to-Standard Bangla normalization (authors note synthetic uniformity inflates this score) |
| **Contribution** | First MT benchmark for Bangla dialects + romanized forms; novel multi-way parallel dataset; comprehensive baselines |
| **Limitation** | Modest scale (980 sentences/dialect); synthetic romanized data; small non-expert manual validation without inter-annotator agreement; only 2 models; automatic metrics only; only 2 dialects |
| **Future Work** | Human evaluation; benchmark larger models (7B–13B) in few-shot + fine-tuning; expand with authentic romanized text; multi-dialect transfer learning; dialect-aware pretraining |

**Verification Status:** Title ✓ · Authors ✓ · Year ✓ · Official venue ✓ · Publication type ✓ · ACL URL ✓ · PDF checked ✓ · Dataset ✓ · Metrics ✓ · Results ✓ · Limitation ✓ — *Note: dataset size IS stated (980 sentences/dialect); earlier "size not clearly stated" was incorrect.*

**বিগিনার বাংলায় সারসংক্ষেপ:**
বাংলাদেশে চট্টগ্রাম ও সিলেটের মানুষ আলাদা উপভাষায় কথা বলেন, কিন্তু এই উপভাষাগুলোর জন্য machine translation প্রায় নেই। এই পেপারে BhasaBodh নামে একটি benchmark তৈরি করা হয়েছে যেখানে চট্টগ্রামি ও সিলেটি উপভাষা থেকে স্ট্যান্ডার্ড বাংলা ও ইংরেজিতে অনুবাদের জন্য parallel data আছে। NLLB-200 ও mBART-50 মডেল ব্যবহার করে ৭টি translation task-এ পরীক্ষা করা হয়েছে, যেখানে mBART-50 সেরা ফলাফল দিয়েছে। এই গবেষণা আমার thesis-এ dialectal NLP gap-এর প্রমাণ হিসেবে ব্যবহার করা যাবে।

---

### Paper 5 — BLUCK

| Field | Details |
|-------|---------|
| **Title** | BLUCK: A Benchmark Dataset for Bengali Linguistic Understanding and Cultural Knowledge |
| **Authors** | Daeen Kabir, Minhajur Rahman Chowdhury Mahim, Sheikh Shafayat, Adnan Sadik, Arian Ahmed, Eunsu Kim, Alice Oh |
| **Year** | 2025 |
| **Official Venue** | Proceedings of the Second Workshop on Bangla Language Processing (BLP-2025) |
| **Publication Type** | Workshop |
| **Associated Conference** | IJCNLP-AACL 2025 (Mumbai, India, December 2025) |
| **Link** | https://aclanthology.org/2025.banglalp-1.14/ |
| **Problem** | No benchmark to test LLM knowledge of Bengali culture, history, and linguistics. |
| **Task Type** | MCQ Benchmark / Cultural QA / LLM Evaluation |
| **Dataset** | BLUCK: 2,366 MCQs across 23 subcategories / 4 domains (Bangladesh culture, history, Bengali linguistics) |
| **Method / Model** | Evaluation of 9 LLMs (6 proprietary + 3 open-source): GPT-4o, Claude-3.5-Sonnet, Gemini-1.5-Pro, LLaMA-3.3-70B-Instruct, DeepSeekV3, others |
| **Evaluation Metric** | Accuracy (MCQ) |
| **Main Result** | Models reasonably good overall but weak in Bengali phonetics / linguistic nuances; all below English; Bengali positioned as a mid-resource language |
| **Contribution** | First MCQ benchmark centered on native Bengali culture, history, and linguistics |
| **Limitation** | Text-only MCQ format (cannot inspect reasoning); 23 categories may not cover all domains; small vs M-MMLU/Global-MMLU; no open-ended evaluation |
| **Future Work** | Expand BLUCK; improve LLMs' understanding of Bengali linguistic and cultural nuances |

**Verification Status:** Title ✓ · Authors ✓ · Year ✓ · Official venue ✓ · Publication type ✓ · ACL URL ✓ · PDF checked ✓ · Dataset ✓ · Metrics ✓ · Results ✓ · Limitation ✓

**বিগিনার বাংলায় সারসংক্ষেপ:**
এই পেপারে BLUCK নামে একটি MCQ benchmark তৈরি করা হয়েছে যেখানে বাংলাদেশের ইতিহাস, সংস্কৃতি এবং বাংলা ভাষাতত্ত্ব নিয়ে ২,৩৬৬টি প্রশ্ন আছে। GPT-4o, Claude-3.5, Gemini সহ ৯টি বড় LLM এই benchmark-এ পরীক্ষা করা হয়েছে। ফলাফলে দেখা গেছে বেশিরভাগ মডেল বাংলা phonetics-এ দুর্বল। এটি আমার thesis-এর জন্য গুরুত্বপূর্ণ কারণ এটি প্রমাণ করে বাংলার সাংস্কৃতিক জ্ঞান LLM-এ এখনও অনেক কম এবং এখানে গবেষণার সুযোগ আছে।

---

### Paper 6 — BanHate

| Field | Details |
|-------|---------|
| **Title** | BanHate: An Up-to-Date and Fine-Grained Bangla Hate Speech Dataset |
| **Authors** | Faisal Hossain Raquib, Akm Moshiur Rahman Mazumder, Md Tahmid Hasan Fuad, Md Farhan Ishmam, Md Fahim |
| **Year** | 2025 |
| **Official Venue** | Proceedings of the Second Workshop on Bangla Language Processing (BLP-2025) |
| **Publication Type** | Workshop |
| **Associated Conference** | IJCNLP-AACL 2025 (Mumbai, India, December 2025) |
| **Link** | https://aclanthology.org/2025.banglalp-1.19/ |
| **Problem** | Existing Bangla hate speech resources are outdated, binary-labeled, and miss evolving implicit hate. |
| **Task Type** | Hate Speech Detection (binary + fine-grained categories + target group identification) |
| **Dataset** | BanHate: 19,203 YouTube comments (April 2024 – June 2025); binary hate, 7 categories, 7 target groups |
| **Method / Model** | Prompting (zero-shot, CoT) + LoRA fine-tuning on 5 open-source (Qwen-2.5-7B, Gemma-3-12B, Llama-3.1-8B, Phi-4-14B, Mistral-7B) and 2 closed (GPT-4o, Gemini-2.5-Flash) LLMs |
| **Evaluation Metric** | Precision, Recall, F1 (Micro/Macro), Subset Accuracy, Hamming loss |
| **Main Result** | LoRA fine-tuning gives most consistent gains; LLaMA-3.1-8B (LoRA) best (Non-Hate F1 85.96 / Hate F1 83.83); GPT-4o/Gemini strong on binary but weak on implicit/fine-grained hate |
| **Contribution** | Largest up-to-date Bangla hate speech dataset; 3-level fine-grained annotations; public on HuggingFace |
| **Limitation** | Data limited to YouTube top-level comments (single platform); single LoRA epoch, greedy decoding, no held-out dev set or multi-seed runs |
| **Future Work** | Not clearly stated (the paper positions BanHate as a general foundation for future hate-speech research) |

**Verification Status:** Title ✓ · Authors ✓ · Year ✓ · Official venue ✓ · Publication type ✓ · ACL URL ✓ · PDF checked ✓ · Dataset ✓ · Metrics ✓ · Results ✓ · Limitation ✓ — *Note: the earlier "evaluation metric not clearly stated" was incorrect; the paper reports P/R/F1, Micro/Macro F1, Subset Accuracy, and Hamming loss.*

**বিগিনার বাংলায় সারসংক্ষেপ:**
এই পেপারে BanHate নামে বাংলার সবচেয়ে বড় hate speech dataset তৈরি করা হয়েছে — YouTube থেকে সংগ্রহ করা ১৯,২০৩টি মন্তব্য, যেগুলো ২০২৪-২০২৫ সালের। প্রতিটি মন্তব্যে তিন স্তরে label দেওয়া আছে: hate আছে কি না, কোন ধরনের hate, এবং কাকে টার্গেট করা হয়েছে। LoRA দিয়ে fine-tune করলে open-source মডেলগুলো অনেক ভালো করে, কিন্তু সূক্ষ্ম hate detect করা এখনও কঠিন। আমার thesis-এর জন্য এটি content moderation বা hate speech detection নিয়ে কাজ করার একটি ভালো resource।

---

### Paper 7 — BanHateME

| Field | Details |
|-------|---------|
| **Title** | BanHateME: Understanding Hate in Bangla Memes thorough Detection, Categorization, and Target Profiling |
| **Authors** | Md Ayon Mia, Md Fahim |
| **Year** | 2025 |
| **Official Venue** | Proceedings of the Second Workshop on Bangla Language Processing (BLP-2025) |
| **Publication Type** | Workshop |
| **Associated Conference** | IJCNLP-AACL 2025 (Mumbai, India, December 2025) |
| **Link** | https://aclanthology.org/2025.banglalp-1.15/ |
| **Problem** | No Bangla multimodal hate meme dataset; prior resources only binary-labeled; cultural visual cues understudied. |
| **Task Type** | Multimodal Hate Speech Detection (text + image, meme analysis) |
| **Dataset** | BanHateME: 3,819 Bangla memes (Facebook 2,517 + Instagram 1,302; train/val/test 2,673/381/765) with 3-level hierarchical annotations (binary, 5 hate categories, 4 target groups) |
| **Method / Model** | Pretrained language + vision encoders (BanglaBERT/XLM-RoBERTa × ViT/Swin); fusion: summation, concatenation, co-attention; hierarchical loss function |
| **Evaluation Metric** | Precision, Recall, F1, Accuracy |
| **Main Result** | BanglaBERT+Swin with concatenation best on binary detection (F1 74.08 / Acc 74.51); co-attention gives clearest gains for target-group recognition; hierarchical loss (α=β=0.5) most balanced |
| **Contribution** | First hierarchically annotated Bangla hateful meme dataset; novel hierarchical loss; systematic multimodal fusion study |
| **Limitation** | Modest dataset size; pretrained encoders not Bangla-optimized; subtle cultural cues remain hard for models |
| **Future Work** | Expand dataset with more efficient annotation; explore culturally-adapted multimodal architectures; experiment with LVLMs and prompting techniques |

**Verification Status:** Title ✓ (see discrepancy) · Authors ✓ · Year ✓ · Official venue ✓ · Publication type ✓ (Workshop — **not** EMNLP main) · ACL URL ✓ · PDF checked ✓ · Dataset ✓ · Metrics ✓ · Results ✓ · Limitation ✓
**Discrepancy:** The canonical title above follows the official ACL Anthology metadata, which records "Bangla Memes **thorough** Detection…". The official PDF heading instead reads "Bangla Memes **through** Detection…". The ACL Anthology metadata is used as canonical per project rule; the PDF wording is noted here.

**বিগিনার বাংলায় সারসংক্ষেপ:**
মিম (meme) হলো ছবি ও লেখার মিশ্রণ — এগুলোতে অনেক সময় ঘৃণাসূচক বার্তা থাকে, বিশেষত বাংলাদেশের সামাজিক মাধ্যমে। এই পেপারে BanHateME নামে ৩,৮১৯টি বাংলা মিমের একটি dataset তৈরি হয়েছে, যেখানে তিন স্তরে annotation আছে। ছবি ও টেক্সট একসাথে বিশ্লেষণ করার জন্য co-attention fusion পদ্ধতি সবচেয়ে ভালো কাজ করেছে। এই পেপারটি আমার thesis-এ multimodal NLP gap দেখানোর জন্য ব্যবহার করা যাবে।

---

### Paper 8 — CheckSent-BN

| Field | Details |
|-------|---------|
| **Title** | CheckSent-BN: A Bengali Multi-Task Dataset for Claim Checkworthiness and Sentiment Classification from News Headlines |
| **Authors** | Pritam Pal, Dipankar Das |
| **Year** | 2025 |
| **Official Venue** | Proceedings of the Second Workshop on Bangla Language Processing (BLP-2025) |
| **Publication Type** | Workshop |
| **Associated Conference** | IJCNLP-AACL 2025 (Mumbai, India, December 2025) |
| **Link** | https://aclanthology.org/2025.banglalp-1.10/ |
| **Problem** | No Bengali annotated dataset for claim checkworthiness; no joint checkworthiness + sentiment benchmark. |
| **Task Type** | Multi-task: Claim Checkworthiness Detection + Sentiment Classification |
| **Dataset** | CheckSent-BN: 11,568 Bengali news headlines (West Bengal, India sources); checkworthy 9,254 / non-checkworthy 2,314; annotated by LLMs (GPT-4o-mini, GPT-4.1-mini + 1) with manual verification |
| **Method / Model** | 8 multilingual transformer models in single-task (STL) and multi-task (MTL) frameworks; IndicBERTv2, BanglaBERT, mDeBERTa strongest |
| **Evaluation Metric** | Accuracy, F1 |
| **Main Result** | IndicBERTv2-based MTL framework best overall; STL better at identifying positive sentiment |
| **Contribution** | First Bengali joint claim checkworthiness + sentiment dataset; cost-effective LLM annotation pipeline |
| **Limitation** | LLM-annotated labels may be noisy; "mini" GPT variants used; class imbalance; headlines from West Bengal only (excludes Bangladesh/Tripura/Assam); single domain (headlines) |
| **Future Work** | Expand sample size; compare LLM vs human annotation; add labels such as clickbait/sarcasm; hire professional annotators; balance dataset; incorporate Tripura/Assam/Bangladesh headlines |

**Verification Status:** Title ✓ · Authors ✓ · Year ✓ · Official venue ✓ · Publication type ✓ · ACL URL ✓ · PDF checked ✓ · Dataset ✓ (size refined to 11,568) · Metrics ✓ · Results ✓ · Limitation ✓

**বিগিনার বাংলায় সারসংক্ষেপ:**
এই পেপারে CheckSent-BN নামে বাংলা সংবাদ শিরোনামের একটি dataset তৈরি করা হয়েছে, যেখানে প্রায় ১১,৫০০টি headline আছে। প্রতিটি headline-এর জন্য দুটি label দেওয়া আছে: এটি fact-check করার যোগ্য কিনা, এবং এর sentiment কী। LLM দিয়ে annotation করে manually যাচাই করা হয়েছে। IndicBERTv2 মডেল multi-task learning-এ সেরা ফলাফল দিয়েছে। এই গবেষণা আমার thesis-এ misinformation detection এবং sentiment analysis গবেষণার gap দেখাতে কাজে লাগবে।

---

### Paper 9 — BanglaTalk

| Field | Details |
|-------|---------|
| **Title** | BanglaTalk: Towards Real-Time Speech Assistance for Bengali Regional Dialects |
| **Authors** | Jakir Hasan, Shubhashis Roy Dipta |
| **Year** | 2025 |
| **Official Venue** | Proceedings of the Second Workshop on Bangla Language Processing (BLP-2025) |
| **Publication Type** | Workshop |
| **Associated Conference** | IJCNLP-AACL 2025 (Mumbai, India, December 2025) |
| **Link** | https://aclanthology.org/2025.banglalp-1.4/ |
| **Problem** | No real-time speech assistant for Bengali regional dialects; existing systems support standard Bengali only. |
| **Task Type** | Automatic Speech Recognition (ASR) / Real-time Speech System (with TTS) |
| **Dataset** | RegSpeech12 (spans 12 Bangladeshi regions; BRDialect trained on 10 dialects); TTS evaluated on a BanSpeech subset |
| **Method / Model** | BRDialect: IndicWav2Vec fine-tuned on 10 Bengali dialects; client-server RTP architecture; VITS-Bengali TTS |
| **Evaluation Metric** | WER, CER (ASR); MOS (TTS) |
| **Main Result** | BRDialect beats baseline ASR by 12.41–33.98% on RegSpeech12 (absolute WER 74.1% / CER 40.6%); TTS MOS 4.49; average end-to-end delay 4.9s at 24 kbps |
| **Contribution** | First real-time dialect-aware Bengali speech assistant; first dialect ASR model (BRDialect) for 10 dialects |
| **Limitation** | 4.9s delay limits conversational use; only 10 of 12 regions used for training; no user-interruption handling |
| **Future Work** | Add user-interruption handling; incorporate speech data from the remaining regions of Bangladesh |

**Verification Status:** Title ✓ · Authors ✓ · Year ✓ · Official venue ✓ · Publication type ✓ · ACL URL ✓ · PDF checked ✓ · Dataset ✓ · Metrics ✓ · Results ✓ · Limitation ✓ — *Note: the 12.41–33.98% figure is the relative improvement over baselines; absolute WER is 74.1%.*

**বিগিনার বাংলায় সারসংক্ষেপ:**
এই পেপারে BanglaTalk নামে বাংলার আঞ্চলিক উপভাষার জন্য প্রথম real-time speech assistant তৈরি করা হয়েছে। BRDialect মডেলটি ১০টি আঞ্চলিক উপভাষায় কথা বোঝার জন্য IndicWav2Vec-কে fine-tune করে তৈরি। এটি baseline-এর তুলনায় ওয়ার্ড এরর ১২–৩৪% কমিয়েছে এবং মাত্র ২৪ kbps-এ কাজ করে। আমার thesis-এর জন্য এটি dialectal speech এবং low-resource language technology-র একটি গুরুত্বপূর্ণ উদাহরণ।

---

### Paper 10 — Reveal-Bangla

| Field | Details |
|-------|---------|
| **Title** | Reveal-Bangla: A Dataset for Cross-Lingual Multi-Step Reasoning Evaluation |
| **Authors** | Khondoker Ittehadul Islam, Gabriele Sarti |
| **Year** | 2025 |
| **Official Venue** | Proceedings of the Second Workshop on Bangla Language Processing (BLP-2025) |
| **Publication Type** | Workshop |
| **Associated Conference** | IJCNLP-AACL 2025 (Mumbai, India, December 2025) |
| **Link** | https://aclanthology.org/2025.banglalp-1.3/ |
| **Problem** | Multi-step reasoning in Bangla completely unevaluated; unclear whether models can exploit Bangla reasoning chains. |
| **Task Type** | Multi-step Reasoning / QA / Cross-lingual Evaluation |
| **Dataset** | Reveal-Bangla: manually translated subset of the English Reveal dataset — 104 unique questions, 188 evidence paragraphs, 355 reasoning steps (751 translated texts; ~70% binary questions) |
| **Method / Model** | Controlled evaluation of Llama-3.2-1B-Instruct (EngLlama) and BanglaLLama-3.2-1b (BenLlama); answers verified with the mDeBERTa-v3 NLI model |
| **Evaluation Metric** | Accuracy (answer correctness via NLI verifier) |
| **Main Result** | Reasoning context benefits more challenging non-binary questions; models struggle to use Bangla reasoning steps (CoT gains larger in English than Bangla) |
| **Contribution** | First Bangla multi-step reasoning dataset; controlled cross-lingual evaluation revealing Bangla reasoning-chain underuse |
| **Limitation** | Small (104 questions); ~70% binary skew; only ~1B small models; single-annotator translation; NLI-verifier limitations; no large (GPT-4-class) model |
| **Future Work** | Test whether trends hold with larger model sizes; explore model interpretability in low-resource languages |

**Verification Status:** Title ✓ · Authors ✓ · Year ✓ · Official venue ✓ · Publication type ✓ · ACL URL ✓ · PDF checked ✓ · Dataset ✓ · Metrics ✓ · Results ✓ · Limitation ✓ — *Note: dataset size and metric (Accuracy) ARE stated; earlier "not clearly stated" entries were incorrect.*

**বিগিনার বাংলায় সারসংক্ষেপ:**
এই পেপারে Reveal-Bangla নামে একটি dataset তৈরি করা হয়েছে যেখানে বাংলায় multi-step reasoning মূল্যায়ন করা হয়েছে — অর্থাৎ একটি প্রশ্নের উত্তর দেওয়ার জন্য কয়েক ধাপে চিন্তা করার দক্ষতা। ইংরেজি Reveal dataset থেকে অনুবাদ করে binary ও non-binary প্রশ্ন তৈরি করা হয়েছে। ফলাফলে দেখা গেছে মডেলগুলো বাংলা reasoning step ঠিকভাবে ব্যবহার করতে পারে না। এই গবেষণা আমার thesis-এ বাংলায় reasoning-এর gap দেখানোর জন্য গুরুত্বপূর্ণ।

---

### Paper 11 — Too Late to Train, Too Early To Use?

| Field | Details |
|-------|---------|
| **Title** | Too Late to Train, Too Early To Use? A Study on Necessity and Viability of Low-Resource Bengali LLMs |
| **Authors** | Tamzeed Mahfuz, Satak Kumar Dey, Ruwad Naswan, Hasnaen Adil, Khondker Salman Sayeed, Haz Sameen Shahgir |
| **Year** | 2025 |
| **Official Venue** | Proceedings of the 31st International Conference on Computational Linguistics (COLING 2025) |
| **Publication Type** | Main Conference |
| **Associated Conference** | COLING 2025 |
| **Link** | https://aclanthology.org/2025.coling-main.79/ |
| **Problem** | Given improving cross-lingual transfer in English-centric LLMs, is a dedicated Bengali-oriented LLM still necessary? |
| **Task Type** | Multi-task LLM evaluation (translation, mono/cross-lingual summarization, paraphrase, QA, NLI, reward modeling) |
| **Dataset** | Existing Bengali test sets: BanglaNMT, XLSum, CrossSum, BanglaParaphrase, SQuAD-bn, BanglaRQA, BEnQA, XNLI-bn |
| **Method / Model** | Zero-shot LLaMA-3-8B/70B, Mistral-7B, Aya-23, Qwen-2-72B, GPT-3.5/4/4o, Gemini-1.5-Pro, NLLB vs fine-tuned BanglaT5-248M / BanglaBERT-111M; plus a QLoRA-fine-tuned LLaMA-3-8B |
| **Evaluation Metric** | BLEU, ROUGE-2, F1, Exact Match, Accuracy |
| **Main Result** | LLMs lead on QA/reasoning (LLaMA-3-70B SQuAD-bn F1 81.9; GPT-4 BEnQA 75.1) but fine-tuned BanglaT5 still wins paraphrase (BLEU 32.80) and monolingual summarization (ROUGE-2 13.7); Bengali tokenization highly inefficient (~0.85 char/token vs ~4.5 English) |
| **Contribution** | Comprehensive evaluation across 7 Bengali NLU/NLG tasks; analysis of tokenization inefficiency and machine-translation dataset bias; a new reward-modeling task |
| **Limitation** | No human evaluation; fine-tuning limited mainly to LLaMA-3-8B; findings may become outdated |
| **Future Work** | Efficient tokenization for non-Latin scripts; high-quality Bengali datasets; cross-lingual transfer |

**Verification Status:** Title ✓ · Authors ✓ · Year ✓ · Official venue ✓ · Publication type ✓ (Main) · ACL URL ✓ · PDF checked ✓ · Dataset ✓ · Metrics ✓ · Results ✓ · Limitation ✓ · Future work ✓ · Bangla-central ✓

**বিগিনার বাংলায় সারসংক্ষেপ:**
এই গবেষণা প্রশ্ন তোলে—বাংলার জন্য আলাদা LLM কি দরকার? লেখকরা ৭টি বাংলা কাজে বড় LLM ও ফাইন-টিউন করা ছোট মডেল তুলনা করেছেন। দেখা যায় বড় LLM প্রশ্নোত্তর ও যুক্তিতে ভালো, কিন্তু প্যারাফ্রেজ ও সারাংশে BanglaT5 এগিয়ে। বাংলা লেখা ভাঙতে LLM-এর টোকেনাইজার অদক্ষ, খরচ বাড়ায়। তাই বাংলা-কেন্দ্রিক LLM ও ভালো ডেটাসেট দরকার।

---

### Paper 12 — BengFoS (Can LLMs be Literary Companions?)

| Field | Details |
|-------|---------|
| **Title** | Can LLMs be Literary Companions?: Analysing LLMs on Bengali Figures of Speech Identification |
| **Authors** | Sourav Das, Kripabandhu Ghosh |
| **Year** | 2025 |
| **Official Venue** | Proceedings of the 2025 Conference on Empirical Methods in Natural Language Processing (EMNLP 2025) |
| **Publication Type** | Main Conference |
| **Associated Conference** | EMNLP 2025 |
| **Link** | https://aclanthology.org/2025.emnlp-main.941/ |
| **Problem** | Identifying figures of speech (FoS) in Bengali literary text is underexplored; computational FoS approaches for Bengali are virtually nonexistent. |
| **Task Type** | Multi-label figures-of-speech classification (13 labels) |
| **Dataset** | BengFoS: 3,148 expert-annotated literary sentences (from 10,198 collected) across 6 Bengali poets; 13 FoS labels; Cohen's κ 0.78 |
| **Method / Model** | Zero-shot then fine-tuned Llama-3-8B and DeepSeek-R1-Distill-7B (full/LoRA, 8/16-bit); SVM & Naive Bayes baselines; layer-wise linear probing |
| **Evaluation Metric** | Accuracy, Precision, Recall, micro/macro/weighted F1 (5-fold CV) |
| **Main Result** | Zero-shot weak (Llama-3 F1 0.42); best deployed fine-tuned DeepSeek-R1-7B (16-bit) weighted-F1 0.64 (Llama-3 0.40); probing peaks Llama-3 micro-F1 0.624, DeepSeek 0.575; gains remain modest |
| **Contribution** | First gold-standard Bengali FoS corpus; large-scale LLM evaluation (zero-shot → fine-tune → deploy); first layer-wise probing for Bengali literary analysis |
| **Limitation** | Only 6 poets (authorial skew); class imbalance (near-zero recall on rare FoS); prose lacks FoS; length sensitivity |
| **Future Work** | Synthetic discourse contexts / span-level augmentation to improve underrepresented labels |

**Verification Status:** Title ✓ · Authors ✓ · Year ✓ · Official venue ✓ · Publication type ✓ (Main) · ACL URL ✓ · PDF checked ✓ · Dataset ✓ · Metrics ✓ · Results ✓ · Limitation ✓ · Future work ✓ · Bangla-central ✓

**বিগিনার বাংলায় সারসংক্ষেপ:**
এই কাজটি বাংলা সাহিত্যে অলংকার (উপমা, রূপক ইত্যাদি) চেনার প্রথম ডেটাসেট BengFoS তৈরি করেছে—৬ জন কবির ৩,১৪৮টি বাক্য। বড় LLM প্রথমে দুর্বল ছিল; ফাইন-টিউন করার পর DeepSeek-R1 সবচেয়ে ভালো (weighted-F1 ০.৬৪)। তবু ফল মাঝারি, কারণ কিছু অলংকার খুব কম পাওয়া যায়। লেখকরা বলছেন আরও ডেটা ও কৌশল দরকার।

---

### Paper 13 — BanglaByT5

| Field | Details |
|-------|---------|
| **Title** | BanglaByT5: Byte-Level Modelling for Bangla |
| **Authors** | Pramit Bhattacharyya, Arnab Bhattacharya |
| **Year** | 2025 |
| **Official Venue** | Findings of the Association for Computational Linguistics: EMNLP 2025 |
| **Publication Type** | Findings |
| **Associated Conference** | EMNLP 2025 |
| **Link** | https://aclanthology.org/2025.findings-emnlp.297/ |
| **Problem** | Subword tokenizers (BPE/SentencePiece) fragment morphologically rich Bangla; no byte-level Bangla model existed. |
| **Task Type** | Byte-level language modelling; generative + classification tasks |
| **Dataset** | 14 GB pre-training corpus (VĀCASPATI literature + IndicCorp-Bangla news); downstream: sentiment, NER (Naamapadam-bn), MT, paraphrase, GEC (VAIYAKARANA) |
| **Method / Model** | BanglaByT5 (~300M params, ByT5-small variant, byte-level span-corruption pre-training) vs mT5, ByT5, GPT-2, BLOOM, IndicBART, BanglaT5, Paramanu |
| **Evaluation Metric** | macro-F1, sacreBLEU, GLEU, BERTScore, BLEU, METEOR, LLM-as-judge |
| **Main Result** | Outperforms similar-size IndicBART/BanglaT5 and larger BLOOM-1.1B; within ~5% of GPT2-XL despite being ~5× smaller; sentiment 68.30, NER 33.60, MT 24.36, paraphrase 35.78, GEC 66.27 |
| **Contribution** | First monolingual byte-level encoder-decoder for Bangla; extensive cross-task/cross-setting evaluation |
| **Limitation** | Limited (14 GB) data forced a small variant; possible hallucination; memorization inherent (here minimal, EM 0.00) |
| **Future Work** | Not clearly stated (Limitations note a larger variant on a larger corpus would help) |

**Verification Status:** Title ✓ · Authors ✓ · Year ✓ · Official venue ✓ · Publication type ✓ (Findings) · ACL URL ✓ · PDF checked ✓ · Dataset ✓ · Metrics ✓ · Results ✓ · Limitation ✓ · Future work = Not clearly stated · Bangla-central ✓

**বিগিনার বাংলায় সারসংক্ষেপ:**
বাংলা শব্দ গঠনে জটিল, তাই সাধারণ টোকেনাইজার ভালো কাজ করে না। লেখকরা বাইট-লেভেলে কাজ করা প্রথম বাংলা মডেল BanglaByT5 (~৩০ কোটি প্যারামিটার) তৈরি করেছেন, ১৪ জিবি ডেটায় প্রশিক্ষিত। এটি সমান বা বড় অনেক মডেলকে হারায়। সীমাবদ্ধতা হলো ডেটা কম, তাই বড় সংস্করণ আরও ভালো হতে পারে।

---

### Paper 14 — BanNERD

| Field | Details |
|-------|---------|
| **Title** | BanNERD: A Benchmark Dataset and Context-Driven Approach for Bangla Named Entity Recognition |
| **Authors** | Md. Motahar Mahtab, Faisal Ahamed Khan, Md. Ekramul Islam, Md. Shahad Mahmud Chowdhury, Labib Imam Chowdhury, Sadia Afrin, Hazrat Ali, Mohammad Mamun Or Rashid, Nabeel Mohammed, Mohammad Ruhul Amin |
| **Year** | 2025 |
| **Official Venue** | Findings of the Association for Computational Linguistics: NAACL 2025 |
| **Publication Type** | Findings |
| **Associated Conference** | NAACL 2025 |
| **Link** | https://aclanthology.org/2025.findings-naacl.380/ |
| **Problem** | Bangla NER lacks large quality datasets; existing resources are noisy; context-concatenation approaches truncate external context. |
| **Task Type** | Named Entity Recognition (NER) |
| **Dataset** | BanNERD: 85,175 sentences, 29 domains, 10 NER classes, IAA 0.88; 51 annotators + 5 validators |
| **Method / Model** | BanNERCEM (context-ensemble: each retrieved Wikipedia context passed separately + hierarchical entity-aware majority voting); PLM (BanglaBERT/XLM-R) + CRF |
| **Evaluation Metric** | Entity-wise macro F1 |
| **Main Result** | 90.49% macro-F1 on BanNERD; new SOTA on 5 of 6 prior Bangla NER datasets (~5.67% higher avg macro-F1 than second-best cross-dataset); English MultiCoNER I 90.34% |
| **Contribution** | Largest validated Bangla NER dataset; a lightweight context-ensemble method with better context utilization and best cross-dataset performance |
| **Limitation** | Per-context passing increases training/inference time; "Creative Work" labels weakest on MultiCoNER |
| **Future Work** | Incorporate more knowledge bases; explore more efficient context utilization |

**Verification Status:** Title ✓ · Authors ✓ · Year ✓ · Official venue ✓ · Publication type ✓ (Findings) · ACL URL ✓ · PDF checked ✓ · Dataset ✓ · Metrics ✓ · Results ✓ (+ figure note) · Limitation ✓ · Future work ✓ · Bangla-central ✓
**Note:** The abstract states a "highest average macro F1 of 81.85% across 10 NER classes," while §6.1 reports 84.12% as the highest **average** performance and 90.49% **on the BanNERD dataset** itself. All three are reported in the paper for different scopes; the matrix leads with 90.49% (on BanNERD) and SOTA-on-5/6.

**বিগিনার বাংলায় সারসংক্ষেপ:**
বাংলায় ভালো নামসত্তা শনাক্তকরণ (NER) ডেটার অভাব। লেখকরা এ পর্যন্ত সবচেয়ে বড় হাতে-লেবেল করা বাংলা NER ডেটাসেট BanNERD (৮৫ হাজারের বেশি বাক্য, ১০টি শ্রেণি) তৈরি করেছেন। তাঁদের পদ্ধতি BanNERCEM প্রতিটি প্রসঙ্গ আলাদাভাবে দেখে, ফলে BanNERD-এ ৯০.৪৯% ম্যাক্রো-F1 পায় এবং আগের ৬টির মধ্যে ৫টি ডেটাসেটে সেরা হয়। সীমাবদ্ধতা—সময় বেশি লাগে।

---

### Paper 15 — Bengali ChartSumm

| Field | Details |
|-------|---------|
| **Title** | Bengali ChartSumm: A Benchmark Dataset and study on feasibility of Large Language Models on Bengali Chart to Text Summarization |
| **Authors** | Nahida Akter Tanjila, Afrin Sultana Poushi, Sazid Abdullah Farhan, Abu Raihan Mostofa Kamal, Md. Azam Hossain, Md. Hamjajul Ashmafee |
| **Year** | 2025 |
| **Official Venue** | Proceedings of the First Workshop on Challenges in Processing South Asian Languages (CHiPSAL 2025) |
| **Publication Type** | Workshop |
| **Associated Conference** | COLING 2025 (Abu Dhabi, UAE, January 2025) |
| **Link** | https://aclanthology.org/2025.chipsal-1.4/ |
| **Problem** | No Bengali chart-to-text summarization benchmark; LLMs not yet applied to Bengali chart summarization. |
| **Task Type** | Chart-to-text summarization |
| **Dataset** | Bengali ChartSumm: 4,100 Bengali chart images + metadata + summaries (bar/line charts; machine-translated from English then human-annotated; 70/10.5/19.5 split) |
| **Method / Model** | mT5-small, BanglaT5, Gemma-2b fine-tuned on title+metadata → caption |
| **Evaluation Metric** | BLEU, ROUGE-1/2/L, CER, WER |
| **Main Result** | mT5 best BLEU 0.2779 and lowest errors (CER 0.5295 / WER 0.7189); BanglaT5 best ROUGE-1 0.0678 (+63% over mT5); all ROUGE-2/L scores low |
| **Contribution** | First Bengali chart-to-text summarization benchmark; baseline study of three models |
| **Limitation** | Only bar/line charts; limited compute; small homogeneous annotator pool (five students) |
| **Future Work** | Bengali OCR; more chart types; SOTA LLMs (LLaMA/Mistral); cross-lingual comparisons; interactive tools |

**Verification Status:** Title ✓ · Authors ✓ · Year ✓ · Official venue ✓ · Publication type ✓ (Workshop) · ACL URL ✓ · PDF checked ✓ · Dataset ✓ · Metrics ✓ · Results ✓ · Limitation ✓ · Future work ✓ · Bangla-central ✓

**বিগিনার বাংলায় সারসংক্ষেপ:**
চার্ট থেকে বাংলায় সারাংশ লেখার কোনো বেঞ্চমার্ক ছিল না। লেখকরা ৪,১০০টি বাংলা চার্ট-ছবি, তথ্য ও সারাংশ নিয়ে Bengali ChartSumm তৈরি করেছেন। mT5, BanglaT5 ও Gemma পরীক্ষা করা হয়েছে; mT5 BLEU-তে সেরা, BanglaT5 ROUGE-1-এ সেরা। কাজটি কঠিন—স্কোর কম। ভবিষ্যতে বাংলা OCR ও বড় মডেল যোগ করার পরিকল্পনা।

---

### Paper 16 — GRASP-ChoQ ⚠

| Field | Details |
|-------|---------|
| **Title** | GRASP-ChoQ: Knowledge Graph-Based Retrieval Augmentation for Stance Detection in Political Texts with Chain-of-Questions Reasoning |
| **Authors** | Rasel Mahmud, Md. Abdur Rakib Mollah, Aninda Kumar Sharma, Omar Faruq Osama |
| **Year** | 2025 |
| **Official Venue** | Proceedings of the Second Workshop on Bangla Language Processing (BLP-2025) |
| **Publication Type** | Workshop |
| **Associated Conference** | IJCNLP-AACL 2025 (Mumbai, India, December 2025) |
| **Link** | https://aclanthology.org/2025.banglalp-1.2/ |
| **Problem** | Political stance detection in the low-resource Bangladesh context is unstudied; LLMs struggle with dynamic political contexts and indirect entity relations. |
| **Task Type** | Political stance detection (FAVOR/AGAINST) |
| **Dataset** | BPDisC: 2,847 Bangladesh-politics tweets (1,512 favor / 1,335 against), language tagged Bangla-English; + 6 non-Bangla benchmark datasets |
| **Method / Model** | GRASP-ChoQ: Neo4j knowledge-graph retrieval augmentation + Chain-of-Questions reasoning over GPT-4/4o, Gemini-1.5-Pro, Mistral-Large, DeepSeek-R1 (non-English translated to English via GPT-4o) |
| **Evaluation Metric** | Accuracy, Precision, Recall, F1 |
| **Main Result** | DeepSeek-R1 + GRASP-ChoQ best on BPDisC: F1 93.33 (+40.6 over zero-shot); consistent gains across all 7 datasets |
| **Contribution** | First to integrate multi-hop KG traversal with question-guided reasoning for political stance detection; new Bangladesh political-discourse dataset (BPDisC) |
| **Limitation** | Text-only (no multimodal); no fine-tuning; limited knowledge base; political sarcasm hard; small inter-annotator samples |
| **Future Work** | Not clearly stated |

**Verification Status:** Title ✓ · Authors ✓ · Year ✓ · Official venue ✓ · Publication type ✓ (Workshop) · ACL URL ✓ · PDF checked ✓ · Dataset ✓ · Metrics ✓ · Results ✓ · Limitation ✓ · Future work = Not clearly stated · **Bangla-central = ⚠ flagged**
**⚠ Flag:** BPDisC is code-mixed **Bangla-English** and all reasoning runs in English after GPT-4o translation; 6 of 7 evaluation datasets are non-Bangla. It does have Bangla-specific results (F1 93.33 on the Bangla-context dataset) and appears in the Bangla workshop, so it meets "Bangla is a major part," retained with this transparency note.

**বিগিনার বাংলায় সারসংক্ষেপ:**
এই গবেষণা রাজনৈতিক অবস্থান (পক্ষে/বিপক্ষে) শনাক্ত করে, বিশেষত বাংলাদেশের ২০২৪ আন্দোলন নিয়ে টুইট দিয়ে তৈরি BPDisC ডেটাসেটে। পদ্ধতি GRASP-ChoQ নলেজ-গ্রাফ ও ধাপে ধাপে প্রশ্ন ব্যবহার করে। DeepSeek-R1 দিয়ে সর্বোচ্চ F1 ৯৩.৩৩ পাওয়া গেছে। তবে লেখা ইংরেজিতে অনুবাদ করে কাজ করা হয়, এটি একটি সীমাবদ্ধতা।

---

### Paper 17 — Read Between the Lines (BanglaBias)

| Field | Details |
|-------|---------|
| **Title** | Read Between the Lines: A Benchmark for Uncovering Political Bias in Bangla News Articles |
| **Authors** | Nusrat Jahan Lia, Shubhashis Roy Dipta, Abdullah Khan Zehady, Naymul Islam, Madhusodan Chakraborty, Abdullah Al Wasif |
| **Year** | 2025 |
| **Official Venue** | Proceedings of the Second Workshop on Bangla Language Processing (BLP-2025) |
| **Publication Type** | Workshop |
| **Associated Conference** | IJCNLP-AACL 2025 (Mumbai, India, December 2025) |
| **Link** | https://aclanthology.org/2025.banglalp-1.5/ |
| **Problem** | Annotated datasets for Bangla political bias are scarce; detecting government-affiliation bias in Bangla news is challenging. |
| **Task Type** | Political bias / stance detection (ternary: Government Leaning / Critique / Neutral) |
| **Dataset** | BanglaBias: 200 annotated Bangla news articles; 46 events, 54 sources; 3 annotators (Cohen's κ 0.574) |
| **Method / Model** | Evaluation of 28 LLMs (Qwen, LLaMA, GLM, DeepSeek, GPT, Claude, Gemini, TigerLLM) in reasoning-then-decision prompting; zero-shot vs few-shot; no training |
| **Evaluation Metric** | Accuracy, Precision, Recall, weighted F1 |
| **Main Result** | Best weighted-F1 Qwen3-235B 0.74, LLaMA-3.3-70B 0.73; Government-Critique easiest (F1 up to 0.83), Neutral hardest (down to 0.00); models over-predict government-leaning; few-shot lagged zero-shot for large models |
| **Contribution** | First Bangla political-stance benchmark with rich metadata and a leaderboard; systematic analysis across LLM sizes and their biases |
| **Limitation** | Small/possibly non-representative corpus; data-contamination risk; text-only; limited few-shot compute |
| **Future Work** | More diverse sources; contamination checks; multimodal stance detection; fine-tuning; extend to other low-resource languages |

**Verification Status:** Title ✓ · Authors ✓ · Year ✓ · Official venue ✓ · Publication type ✓ (Workshop) · ACL URL ✓ · PDF checked ✓ · Dataset ✓ · Metrics ✓ · Results ✓ · Limitation ✓ · Future work ✓ · Bangla-central ✓

**বিগিনার বাংলায় সারসংক্ষেপ:**
বাংলা সংবাদে রাজনৈতিক পক্ষপাত মাপার জন্য BanglaBias নামে প্রথম বেঞ্চমার্ক (২০০টি নিবন্ধ, ৩টি শ্রেণি) তৈরি হয়েছে। ২৮টি LLM পরীক্ষা করা হয়; সেরা Qwen3-235B (weighted-F1 ০.৭৪)। মডেলগুলো "সরকার-সমালোচনা" ভালো চেনে কিন্তু "নিরপেক্ষ" শ্রেণি চিনতে পারে না। ডেটাসেট ছোট হওয়া বড় সীমাবদ্ধতা।

---

### Paper 18 — BiCap

| Field | Details |
|-------|---------|
| **Title** | BiCap: Bangla Image Captioning Using Attention-based Encoder-Decoder Architecture |
| **Authors** | Md Aminul Kader Bulbul |
| **Year** | 2025 |
| **Official Venue** | Proceedings of the Second Workshop on Bangla Language Processing (BLP-2025) |
| **Publication Type** | Workshop |
| **Associated Conference** | IJCNLP-AACL 2025 (Mumbai, India, December 2025) |
| **Link** | https://aclanthology.org/2025.banglalp-1.6/ |
| **Problem** | Bangla image captioning is limited; no large multimodal corpora / pretrained vision-language models; prior captions suffer repetition and semantic incompleteness. |
| **Task Type** | Image captioning |
| **Dataset** | Chitron (existing, Sazzed 2020): 15,438 image-caption pairs (12,350/1,544/1,544) — dataset reused, not a contribution |
| **Method / Model** | Attention-based encoder-decoder: ResNet-50 encoder + Bahdanau attention + LSTM decoder |
| **Evaluation Metric** | BLEU-1..4, METEOR, ROUGE, CIDEr; human evaluation (83 raters) |
| **Main Result** | BLEU-4 32.73 (+10 over strongest baseline Masud et al. 2025), METEOR 0.37, ROUGE 0.42, CIDEr 0.29; best human scores (fluency 4.3 / adequacy 4.4 / relevance 4.6) |
| **Contribution** | Attention-based Bangla captioning framework outperforming prior baselines on the largest Bangla captioning dataset, with human evaluation |
| **Limitation** | ResNet-50 captures local not global features; sequential LSTM decoder; generalization to unseen domains unverified |
| **Future Work** | CNN-ViT hybrids; transformer decoders; more datasets; subword/morphological tokenization |

**Verification Status:** Title ✓ · Authors ✓ · Year ✓ · Official venue ✓ · Publication type ✓ (Workshop) · ACL URL ✓ · PDF checked ✓ · Dataset ✓ (existing — Chitron) · Metrics ✓ · Results ✓ · Limitation ✓ · Future work ✓ · Bangla-central ✓

**বিগিনার বাংলায় সারসংক্ষেপ:**
ছবি দেখে বাংলায় বর্ণনা লেখা (image captioning) কম-সম্পদ ভাষায় কঠিন। লেখক ResNet-50, অ্যাটেনশন ও LSTM দিয়ে BiCap মডেল বানিয়েছেন এবং Chitron ডেটাসেটে পরীক্ষা করেছেন। BLEU-4 ৩২.৭৩ পেয়ে আগের সব মডেলকে হারিয়েছে। সীমাবদ্ধতা—মডেল পুরো দৃশ্য ভালো বোঝে না এবং নতুন ক্ষেত্রে পরীক্ষা হয়নি।

---

### Paper 19 — P6Jiggasha

| Field | Details |
|-------|---------|
| **Title** | P6Jiggasha: Benchmarking Large Language Models on Bangla Physics Question Answering with Cross-lingual Evaluation |
| **Authors** | S.M. Shahriar, Md Tahmid Hasan Fuad, Md Fahim, Md. Azad Hossain |
| **Year** | 2025 |
| **Official Venue** | Proceedings of the Second Workshop on Bangla Language Processing (BLP-2025) |
| **Publication Type** | Workshop |
| **Associated Conference** | IJCNLP-AACL 2025 (Mumbai, India, December 2025) |
| **Link** | https://aclanthology.org/2025.banglalp-1.16/ |
| **Problem** | LLM performance on Bangla scientific (physics) QA and cross-lingual answer consistency is unmeasured. |
| **Task Type** | Physics question answering (MCQ) / LLM benchmarking (cross-lingual) |
| **Dataset** | P6Jiggasha: 1,500 Bangla physics MCQs (HSC textbooks/guides/question banks; 4 options; 6 topics, 6 question types; 500 test) + English translations |
| **Method / Model** | GPT-4.1, Gemini-2.5-Pro, DeepSeek-R1-Distill-Llama-70B; zero-shot vs CoT; Bangla vs English |
| **Evaluation Metric** | Cumulative Accuracy@k (k=1..4) |
| **Main Result** | GPT-4.1 best Bangla Acc@1 86.67% (Gemini 71.24, DeepSeek 48.00); Gemini reaches 89.52% at Acc@4; GPT-4.1 near-identical Bangla vs English (86.67 vs 84.57); question-type complexity drives gaps more than language |
| **Contribution** | First large-scale Bangla physics MCQ dataset with English translations; multi-model cross-lingual evaluation; the Cumulative Accuracy@k metric |
| **Limitation** | MCQ-only; no diagrams; physics-only; cross-lingual inconsistencies; translation may introduce subtle shifts |
| **Future Work** | Open-ended formats; multimodal (diagrams); other STEM domains and low-resource languages |

**Verification Status:** Title ✓ · Authors ✓ · Year ✓ · Official venue ✓ · Publication type ✓ (Workshop) · ACL URL ✓ · PDF checked ✓ · Dataset ✓ · Metrics ✓ · Results ✓ · Limitation ✓ · Future work ✓ · Bangla-central ✓

**বিগিনার বাংলায় সারসংক্ষেপ:**
বাংলায় পদার্থবিজ্ঞানের প্রশ্নে LLM কেমন করে তা মাপতে P6Jiggasha নামে ১,৫০০টি MCQ ডেটাসেট তৈরি হয়েছে। GPT-4.1, Gemini-2.5-Pro ও DeepSeek-R1 পরীক্ষা করা হয়। GPT-4.1 সবচেয়ে ভালো (বাংলায় ৮৬.৬৭%)। বাংলা ও ইংরেজিতে ফল প্রায় সমান—মূল পার্থক্য প্রশ্নের কঠিনতায়। সীমাবদ্ধতা—শুধু MCQ ও ছবি/চিত্র নেই।

---

### Paper 20 — ChakmaBridge ⚠

| Field | Details |
|-------|---------|
| **Title** | ChakmaBridge: A Five-Way Parallel Corpus for Navigating the Script Divide in an Endangered Language |
| **Authors** | Md. Abdur Rahman, Md. Tofael Ahmed Bhuiyan, Abdul Kadar Muhammad Masum |
| **Year** | 2025 |
| **Official Venue** | Proceedings of the Second Workshop on Bangla Language Processing (BLP-2025) |
| **Publication Type** | Workshop |
| **Associated Conference** | IJCNLP-AACL 2025 (Mumbai, India, December 2025) |
| **Link** | https://aclanthology.org/2025.banglalp-1.21/ |
| **Problem** | The endangered Chakma language lacks standardized parallel corpora linking romanized and native-script forms; MT for Chakma is nascent. |
| **Task Type** | Parallel-corpus construction + machine translation (endangered language) |
| **Dataset** | ChakmaBridge: 807 sentences in 5 forms (English, Standard Bangla, Bengali-script Chakma, Romanized Bangla, Romanized Chakma); 564/81/162 split |
| **Method / Model** | Gemini-2.5-Pro generated romanizations (human-validated); mBART-50 and NLLB-200 fine-tuned across 6 translation tasks |
| **Evaluation Metric** | BLEU, METEOR, BERTScore-F1 |
| **Main Result** | Best (English+Standard Bangla)→Chakma with NLLB-200: BLEU 0.5228, METEOR 0.6486, BERTScore-F1 0.9136 (+124% BLEU over next-best task); Bangla as source beats English; NLLB-200 generally beats mBART-50 |
| **Contribution** | First five-way parallel corpus for Chakma; MT baselines across six language/script modalities |
| **Limitation** | Only 807 sentences; LLM-romanization cleaner than real-world usage; validation on only 20 sentences; no native Chakma (Ajhā Pāṭh) script |
| **Future Work** | Expand data; back-translation; native Chakma script support; constrained decoding |

**Verification Status:** Title ✓ · Authors ✓ · Year ✓ · Official venue ✓ · Publication type ✓ (Workshop) · ACL URL ✓ · PDF checked ✓ · Dataset ✓ · Metrics ✓ · Results ✓ · Limitation ✓ · Future work ✓ · **Bangla = major (Chakma-primary) — flagged**
**⚠ Flag:** The target/endangered language is **Chakma**; Bangla is a major source/pivot (3 of 5 parallel forms involve Bangla/Bengali script, and Bangla-as-source drives the best results). Meets "Bangla is a major part," retained with this transparency note.

**বিগিনার বাংলায় সারসংক্ষেপ:**
বিপন্ন চাকমা ভাষার জন্য কোনো ভালো অনুবাদ ডেটা ছিল না। লেখকরা ChakmaBridge তৈরি করেছেন—৮০৭টি বাক্য পাঁচ রূপে (ইংরেজি, প্রমিত বাংলা, বাংলা-হরফে চাকমা, রোমান বাংলা, রোমান চাকমা)। NLLB-200 দিয়ে ইংরেজি+বাংলা থেকে চাকমায় সেরা ফল (BLEU ০.৫২২৮)। বাংলা উৎস হিসেবে ইংরেজির চেয়ে ভালো কাজ করে। সীমাবদ্ধতা—ডেটা খুব ছোট।

---

*Batches 1–2 complete — 20 papers. All metadata verified via ACL Anthology; results verified against official PDFs (June 2026). Two Bangla-centrality flags (Papers 16, 20) retained transparently. Awaiting review before Batch 3.*
