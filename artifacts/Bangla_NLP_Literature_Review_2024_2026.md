# Recent Work in Bangla NLP (2024–2026): Literature Review

**MSc Thesis — Bangla NLP Literature Review**
**Author:** Sarker Sunzid Mahmud | TU Darmstadt
**Last updated:** June 2026 | Batch 1 — 10 papers

---

## 1. Search Strategy

- **Primary source:** ACL Anthology (aclanthology.org) — keywords: "Bangla", "Bengali", "NLP", "language model", "low-resource". Year filter: 2024–2026.
- **Secondary:** Google Scholar and Semantic Scholar for cross-checking and gap-filling.
- **Target venues:** ACL, EMNLP, NAACL, COLING, EACL, AACL. Workshop papers accepted if at a target-venue workshop (e.g., BLP-2025 @ EMNLP 2025).
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

| No | Title | Year | Venue | Problem | Task | Dataset | Method | Main Result | Limitation |
|----|-------|------|-------|---------|------|---------|--------|-------------|------------|
| 1 | BenLLM-Eval | 2024 | LREC-COLING | LLMs not benchmarked on Bengali | Multi-task eval | Custom (6 tasks) | ChatGPT, LLaMA-2, Claude-2 (zero-shot) | LLMs underperform SOTA on most tasks; LLaMA-2 worst | Zero-shot only; 3 LLMs tested |
| 2 | Bias & Context Length for Bangla | 2024 | Findings-ACL | Social bias in Bangla LMs unstudied | Bias measurement | New Bangla gender bias dataset | Adapted WEAT/SEAT metrics | Bias metrics depend on context length | Gender bias only; intrinsic measures only |
| 3 | BanglaTLit | 2024 | Findings-EMNLP | Romanized Bangla untapped; no back-transliteration benchmark | Transliteration | BanglaTLit 42.7k; BanglaTLit-PT 245.7k | Encoder-decoder + further pre-training | SOTA on romanized Bangla classification | Noisy informal text; evaluation metric not clearly stated |
| 4 | BhasaBodh | 2025 | BLP-2025 | Bangla dialects (Chittagong/Sylhet) underserved in MT | Machine Translation | New parallel corpus (dialect + romanized) | Fine-tuned NLLB-200, mBART-50 | BLEU 87.44 on Romanized→Standard; mBART-50 best | Small dataset; complex cross-script MT hard |
| 5 | BLUCK | 2025 | BLP-2025 | No LLM benchmark for Bengali cultural/linguistic knowledge | MCQ Benchmark / QA | BLUCK 2,366 MCQs (23 categories) | GPT-4o, Claude-3.5-Sonnet, Gemini, LLaMA, DeepSeek | LLMs struggle with Bengali phonetics; below English performance | MCQ only; no open-ended evaluation |
| 6 | BanHate | 2025 | BLP-2025 | Outdated, narrow Bangla hate speech resources | Hate Speech Detection | BanHate 19,203 YouTube comments | LoRA fine-tuning + prompting on LLMs | LoRA boosts open-source models; implicit hate detection hard | YouTube only; implicit hate remains challenging |
| 7 | BanHateME | 2025 | BLP-2025 | No multimodal Bangla hate meme dataset | Multimodal Hate Detection | BanHateME 3,819 memes (3-level annotations) | Multimodal fusion (co-attention) + hierarchical loss | Co-attention + hierarchical loss most effective | Small dataset; cultural cues hard for models |
| 8 | CheckSent-BN | 2025 | BLP-2025 | No Bengali dataset for claim checkworthiness + sentiment | Fact-check + Sentiment (MTL) | CheckSent-BN ~11,500 news headlines | IndicBERTv2, BanglaBERT, mDeBERTa (MTL) | IndicBERTv2 best in MTL setting | LLM-annotated labels may have noise |
| 9 | BanglaTalk | 2025 | BLP-2025 | No real-time Bengali dialect speech assistant | ASR / Speech System | RegSpeech12 (10 dialects) | BRDialect: IndicWav2Vec fine-tuned on 10 dialects | WER ↓ 12.41–33.98% vs baseline; 4.9s delay at 24 kbps | 4.9s latency; tested on single dataset only |
| 10 | Reveal-Bangla | 2025 | BLP-2025 | Multi-step reasoning in Bangla unevaluated | Multi-step Reasoning / QA | Reveal-Bangla (translated from English Reveal) | Evaluation of multilingual SLMs | Models struggle with Bangla reasoning steps; context helps non-binary Qs | Manually translated; only small models evaluated |

---

## 4. Topic-wise Grouping

| Topic | Papers |
|-------|--------|
| Safety & Content Moderation | 6 (BanHate), 7 (BanHateME), 8 (CheckSent-BN) |
| LLM Evaluation & Benchmarks | 1 (BenLLM-Eval), 5 (BLUCK) |
| Machine Translation (Dialectal) | 4 (BhasaBodh) |
| Transliteration | 3 (BanglaTLit) |
| Bias & Fairness | 2 (Bias & Context Length) |
| Speech Recognition | 9 (BanglaTalk) |
| Reasoning / QA | 10 (Reveal-Bangla) |

---

## 5. Year-wise Trend

| Year | Papers | Key Themes |
|------|--------|------------|
| 2024 | 3 | LLM evaluation, bias measurement, transliteration |
| 2025 | 7 | Safety/hate speech, LLM benchmarks, dialectal NLP, speech, reasoning |
| 2026 | 0 (Batch 1) | — |

Growth driven by BLP-2025 workshop (69 papers). Safety and LLM benchmarking are dominant 2025 themes.

---

## 6. Venue-wise Distribution

| Venue | Year | Papers |
|-------|------|--------|
| LREC-COLING | 2024 | 1 |
| Findings of ACL | 2024 | 1 |
| Findings of EMNLP | 2024 | 1 |
| BLP-2025 (EMNLP 2025 Workshop) | 2025 | 7 |

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

---

## 8. Common Datasets (Introduced in Batch 1)

| Dataset | Paper | Size | Task |
|---------|-------|------|------|
| BanglaTLit | Paper 3 | 42.7k pairs | Transliteration |
| BanglaTLit-PT | Paper 3 | 245.7k | Pre-training corpus |
| Bangla gender bias dataset | Paper 2 | Not clearly stated | Bias measurement |
| BhasaBodh corpus | Paper 4 | Not clearly stated | Dialectal MT |
| BLUCK | Paper 5 | 2,366 MCQs, 23 categories | Cultural/linguistic QA |
| BanHate | Paper 6 | 19,203 YouTube comments | Hate speech detection |
| BanHateME | Paper 7 | 3,819 memes | Multimodal hate detection |
| CheckSent-BN | Paper 8 | ~11,500 news headlines | Fact-check + sentiment |
| RegSpeech12 | Paper 9 | 10 Bengali dialects | Dialect ASR |
| Reveal-Bangla | Paper 10 | Not clearly stated | Multi-step reasoning |

---

## 9. Common Models and Methods

**Encoder models:** BanglaBERT, IndicBERTv2, MuRIL, mDeBERTa, BanglishBERT

**Generative LLMs:** ChatGPT, LLaMA-2, Claude-2, GPT-4o, Claude-3.5-Sonnet, Gemini-1.5-Pro, LLaMA-3.3-70B, DeepSeekV3

**Seq2Seq / MT models:** mBART-50, NLLB-200, mT5

**Speech models:** IndicWav2Vec (fine-tuned on Bengali dialects)

**Adaptation methods:** LoRA fine-tuning, zero-shot prompting, few-shot prompting, multi-task learning (MTL), further pre-training

**Bias methods:** Adapted WEAT/SEAT intrinsic bias metrics for Bangla

---

## 10. Research Gaps

| Gap Type | Description | Relevant Papers |
|----------|-------------|-----------------|
| Dataset Gap | No large-scale annotated data for NER, coreference, dialogue, math reasoning; dialectal data extremely scarce | 4, 10 |
| Benchmark Gap | No unified multi-task Bangla benchmark comparable to GLUE/SuperGLUE | 1, 5 |
| Model Gap | No dedicated Bangla instruction-tuned LLM; all work uses English-centric multilingual models | 1, 5 |
| Evaluation Gap | Inconsistent metrics across papers; no standard Bangla eval protocol; bias lacks extrinsic evaluation | 2, 6, 7, 10 |
| Low-Resource / Dialect Gap | Only Chittagong/Sylhet covered; no other dialects; diaspora Bangla ignored | 4, 9 |
| Domain Gap | No Bangla NLP research in medical, legal, financial, or scientific domains in Batch 1 | all |
| Practical Deployment Gap | Only BanglaTalk is a deployed system; all other papers produce datasets/models without real-world deployment | 9 |

---

## 11. Possible Thesis Directions

1. **Unified Bangla Benchmark:** Build a multi-task evaluation suite (NLU, generation, reasoning, cultural knowledge) — fill the GLUE-equivalent gap for Bangla.
2. **Instruction-Tuned Bangla LLM:** Fine-tune an open-source LLM (LLaMA/Mistral) on Bangla instruction data; evaluate on BenLLM-Eval and BLUCK.
3. **Dialectal NLP Expansion:** Extend BhasaBodh to more dialects; build cross-dialect NLU or MT pipeline beyond Chittagong/Sylhet.
4. **Bias Mitigation:** Build on the ACL 2024 bias paper to study intersectional bias (gender × religion × dialect) and propose debiasing strategies.
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
| **Venue** | LREC-COLING 2024 |
| **Link** | https://aclanthology.org/2024.lrec-main.201/ |
| **Problem** | LLMs evaluated mostly in English; no systematic Bangla NLP benchmark existed. |
| **Task Type** | Multi-task evaluation: summarization, QA, paraphrasing, NLI, text classification, sentiment analysis |
| **Dataset** | Custom evaluation set across 6 Bengali NLP tasks (specific dataset names not clearly stated) |
| **Method / Model** | Zero-shot evaluation of ChatGPT, LLaMA-2, Claude-2 |
| **Evaluation Metric** | Task-specific: ROUGE, F1, Accuracy, BLEU |
| **Main Result** | Zero-shot LLMs match SOTA on a few tasks; significantly underperform on most; LLaMA-2 worst overall |
| **Contribution** | First comprehensive zero-shot LLM benchmark for Bengali NLP across 6 diverse tasks |
| **Limitation** | Zero-shot only; only 3 LLMs evaluated; no instruction-tuned or fine-tuned LLM comparison |

**বিগিনার বাংলায় সারসংক্ষেপ:**
এই গবেষণায় দেখা হয়েছে যে ChatGPT, LLaMA-2 এবং Claude-2 এর মতো বড় ভাষা মডেলগুলো বাংলায় কতটা ভালো কাজ করতে পারে। গবেষকরা ছয়টি কাজের (যেমন: সারাংশ লেখা, প্রশ্নোত্তর, sentiment বিশ্লেষণ) উপর zero-shot পরীক্ষা করেছেন — অর্থাৎ মডেলকে কোনো উদাহরণ না দিয়ে সরাসরি প্রশ্ন করা হয়েছে। ফলাফলে দেখা গেছে যে বেশিরভাগ কাজে এই মডেলগুলো বর্তমান সেরা পদ্ধতির চেয়ে অনেক পিছিয়ে, বিশেষত LLaMA-2 সবচেয়ে দুর্বল। এই পেপারটি আমার thesis-এর জন্য গুরুত্বপূর্ণ কারণ এটি বাংলায় LLM-এর দুর্বলতাগুলো স্পষ্টভাবে চিহ্নিত করে এবং আরো গবেষণার প্রয়োজনীয়তা দেখায়।

---

### Paper 2 — Bias & Context Length for Bangla

| Field | Details |
|-------|---------|
| **Title** | An Empirical Study on the Characteristics of Bias upon Context Length Variation for Bangla |
| **Authors** | Jayanta Sadhu, Ayan Khan, Abhik Bhattacharjee, Rifat Shahriyar |
| **Year** | 2024 |
| **Venue** | Findings of the Association for Computational Linguistics: ACL 2024 |
| **Link** | https://aclanthology.org/2024.findings-acl.88/ |
| **Problem** | Social bias in Bangla pretrained LMs unstudied; impact of context length on bias measurement unexplored. |
| **Task Type** | Bias measurement / Fairness |
| **Dataset** | New Bangla gender bias dataset (created in this work; size not clearly stated) |
| **Method / Model** | Adapted WEAT/SEAT intrinsic bias metrics for Bangla; context length variation experiments |
| **Evaluation Metric** | Intrinsic bias metrics (WEAT/SEAT effect sizes) |
| **Main Result** | Bias metrics show clear dependency on context length — a factor overlooked in prior work |
| **Contribution** | First Bangla gender bias dataset; novel finding that context length affects bias measurement |
| **Limitation** | Only gender bias; only intrinsic measures; no extrinsic downstream evaluation |

**বিগিনার বাংলায় সারসংক্ষেপ:**
এই পেপারে গবেষকরা বাংলা ভাষার language model-এ লিঙ্গভিত্তিক পক্ষপাত (gender bias) কতটুকু আছে তা পরিমাপ করেছেন। তারা প্রথমবার বাংলার জন্য একটি gender bias dataset তৈরি করেছেন এবং WEAT/SEAT পদ্ধতিকে বাংলার উপযোগী করেছেন। সবচেয়ে গুরুত্বপূর্ণ আবিষ্কার হলো: context-এর দৈর্ঘ্য বদলালে bias পরিমাপের ফলাফলও বদলে যায় — আগের কোনো গবেষণায় এটি দেখা যায়নি। আমার thesis-এর জন্য এটি দরকারী কারণ এটি বাংলায় fairness গবেষণার ভিত্তি স্থাপন করেছে।

---

### Paper 3 — BanglaTLit

| Field | Details |
|-------|---------|
| **Title** | BanglaTLit: A Benchmark Dataset for Back-Transliteration of Romanized Bangla |
| **Authors** | Md Fahim, Fariha Tanjim Shifat, Fabiha Haider, Deeparghya Dutta Barua, MD Sakib Ul Rahman Sourove, Md Farhan Ishmam, Md Farhad Alam Bhuiyan |
| **Year** | 2024 |
| **Venue** | Findings of the Association for Computational Linguistics: EMNLP 2024 |
| **Link** | https://aclanthology.org/2024.findings-emnlp.859/ |
| **Problem** | Romanized Bangla is abundant on the internet but untapped; no large-scale back-transliteration benchmark existed. |
| **Task Type** | Transliteration / Back-transliteration |
| **Dataset** | BanglaTLit: 42.7k samples; BanglaTLit-PT pre-training corpus: 245.7k samples |
| **Method / Model** | Encoder-decoder with further pre-trained encoders on BanglaTLit-PT; multiple baseline methods |
| **Evaluation Metric** | Not clearly stated (accuracy on downstream romanized Bangla classification tasks reported) |
| **Main Result** | Further pre-trained encoders achieve SOTA on romanized Bangla classification; back-transliteration feasibility demonstrated |
| **Contribution** | Largest Bangla transliteration dataset; SOTA romanized Bangla encoder; open code and data |
| **Limitation** | Informal romanized text is noisy; evaluation metric not clearly specified |

**বিগিনার বাংলায় সারসংক্ষেপ:**
ইন্টারনেটে অনেক মানুষ বাংলা ভাষা রোমান হরফে লেখেন (যেমন: "ami bhalo achi")। এই পেপারে গবেষকরা এই রোমান বাংলাকে আবার বাংলা script-এ রূপান্তর করার জন্য BanglaTLit নামে ৪২,৭০০টি sample-এর একটি বড় dataset তৈরি করেছেন। তারা একটি encoder-decoder model তৈরি করেছেন যা এই কাজে state-of-the-art ফলাফল দিয়েছে। এই গবেষণাটি আমার thesis-এর জন্য গুরুত্বপূর্ণ কারণ রোমান বাংলার data ব্যবহার করে বাংলা NLP-এর data scarcity সমস্যা কমানো যেতে পারে।

---

### Paper 4 — BhasaBodh

| Field | Details |
|-------|---------|
| **Title** | BhasaBodh: Bridging Bangla Dialects and Romanized Forms through Machine Translation |
| **Authors** | Md. Tofael Ahmed Bhuiyan, Md. Abdur Rahman, Abdul Kadar Muhammad Masum |
| **Year** | 2025 |
| **Venue** | Proceedings of the Second Workshop on Bangla Language Processing (BLP-2025), EMNLP 2025 |
| **Link** | https://aclanthology.org/2025.banglalp-1.9/ |
| **Problem** | Bangla dialects (Chittagong, Sylhet) and romanized forms severely underserved in MT; no evaluation benchmark existed. |
| **Task Type** | Machine Translation (dialectal + romanized) |
| **Dataset** | New sentence-level parallel corpus for Chittagong and Sylhet dialects + romanized versions (size not clearly stated) |
| **Method / Model** | Fine-tuned NLLB-200 and mBART-50 on 7 translation tasks |
| **Evaluation Metric** | BLEU |
| **Main Result** | mBART-50 outperforms NLLB-200; best BLEU 87.44 on Romanized-to-Standard Bangla normalization task |
| **Contribution** | First MT benchmark for Bangla dialects + romanized forms; novel parallel dataset; comprehensive baselines |
| **Limitation** | Dataset size not clearly stated; complex cross-lingual/cross-script translation remains hard; no other dialects covered |

**বিগিনার বাংলায় সারসংক্ষেপ:**
বাংলাদেশে চট্টগ্রাম ও সিলেটের মানুষ আলাদা উপভাষায় কথা বলেন, কিন্তু এই উপভাষাগুলোর জন্য machine translation প্রায় নেই। এই পেপারে BhasaBodh নামে একটি benchmark তৈরি করা হয়েছে যেখানে চট্টগ্রামি ও সিলেটি উপভাষা থেকে স্ট্যান্ডার্ড বাংলা ও ইংরেজিতে অনুবাদের জন্য parallel data আছে। NLLB-200 ও mBART-50 মডেল ব্যবহার করে ৭টি translation task-এ পরীক্ষা করা হয়েছে, যেখানে mBART-50 সেরা ফলাফল দিয়েছে। এই গবেষণা আমার thesis-এ dialectal NLP gap-এর প্রমাণ হিসেবে ব্যবহার করা যাবে।

---

### Paper 5 — BLUCK

| Field | Details |
|-------|---------|
| **Title** | BLUCK: A Benchmark Dataset for Bengali Linguistic Understanding and Cultural Knowledge |
| **Authors** | Daeen Kabir, Minhajur Rahman Chowdhury Mahim, Sheikh Shafayat, Adnan Sadik, Arian Ahmed, Eunsu Kim, Alice Oh |
| **Year** | 2025 |
| **Venue** | Proceedings of the Second Workshop on Bangla Language Processing (BLP-2025), EMNLP 2025 |
| **Link** | https://aclanthology.org/2025.banglalp-1.14/ |
| **Problem** | No benchmark to test LLM knowledge of Bengali culture, history, and linguistics. |
| **Task Type** | MCQ Benchmark / Cultural QA / LLM Evaluation |
| **Dataset** | BLUCK: 2,366 MCQs across 23 categories (Bangladesh culture, history, Bengali linguistics) |
| **Method / Model** | Evaluation of 9 LLMs: GPT-4o, Claude-3.5-Sonnet, Gemini-1.5-Pro, LLaMA-3.3-70B-Instruct, DeepSeekV3 |
| **Evaluation Metric** | Accuracy (MCQ) |
| **Main Result** | LLMs struggle with Bengali phonetics; Bengali positioned as mid-resource language; all models perform below English |
| **Contribution** | First MCQ benchmark centered on native Bengali culture, history, and linguistics |
| **Limitation** | MCQ format only; 23 categories may not cover all cultural domains; no open-ended evaluation |

**বিগিনার বাংলায় সারসংক্ষেপ:**
এই পেপারে BLUCK নামে একটি MCQ benchmark তৈরি করা হয়েছে যেখানে বাংলাদেশের ইতিহাস, সংস্কৃতি এবং বাংলা ভাষাতত্ত্ব নিয়ে ২,৩৬৬টি প্রশ্ন আছে। GPT-4o, Claude-3.5, Gemini সহ ৯টি বড় LLM এই benchmark-এ পরীক্ষা করা হয়েছে। ফলাফলে দেখা গেছে বেশিরভাগ মডেল বাংলা phonetics-এ দুর্বল। এটি আমার thesis-এর জন্য গুরুত্বপূর্ণ কারণ এটি প্রমাণ করে বাংলার সাংস্কৃতিক জ্ঞান LLM-এ এখনও অনেক কম এবং এখানে গবেষণার সুযোগ আছে।

---

### Paper 6 — BanHate

| Field | Details |
|-------|---------|
| **Title** | BanHate: An Up-to-Date and Fine-Grained Bangla Hate Speech Dataset |
| **Authors** | Faisal Hossain Raquib, Akm Moshiur Rahman Mazumder, Md Tahmid Hasan Fuad, Md Farhan Ishmam, Md Fahim |
| **Year** | 2025 |
| **Venue** | Proceedings of the Second Workshop on Bangla Language Processing (BLP-2025), EMNLP 2025 |
| **Link** | https://aclanthology.org/2025.banglalp-1.19/ |
| **Problem** | Existing Bangla hate speech resources are outdated, binary-labeled, and miss evolving implicit hate. |
| **Task Type** | Hate Speech Detection (binary + fine-grained categories + target group identification) |
| **Dataset** | BanHate: 19,203 YouTube comments (April 2024 – June 2025); binary hate, 7 categories, 7 target groups |
| **Method / Model** | LoRA fine-tuning and prompting on open/closed LLMs (GPT-4o, Gemini, and others) |
| **Evaluation Metric** | Not clearly stated |
| **Main Result** | LoRA substantially improves open-source models; GPT-4o/Gemini strong on binary but weak on implicit/fine-grained hate |
| **Contribution** | Largest up-to-date Bangla hate speech dataset; 3-level fine-grained annotations; public on HuggingFace |
| **Limitation** | Data limited to YouTube; implicit hate detection remains difficult; 14-month collection window |

**বিগিনার বাংলায় সারসংক্ষেপ:**
এই পেপারে BanHate নামে বাংলার সবচেয়ে বড় hate speech dataset তৈরি করা হয়েছে — YouTube থেকে সংগ্রহ করা ১৯,২০৩টি মন্তব্য, যেগুলো ২০২৪-২০২৫ সালের। প্রতিটি মন্তব্যে তিন স্তরে label দেওয়া আছে: hate আছে কি না, কোন ধরনের hate, এবং কাকে টার্গেট করা হয়েছে। LoRA দিয়ে fine-tune করলে open-source মডেলগুলো অনেক ভালো করে, কিন্তু সূক্ষ্ম hate detect করা এখনও কঠিন। আমার thesis-এর জন্য এটি content moderation বা hate speech detection নিয়ে কাজ করার একটি ভালো resource।

---

### Paper 7 — BanHateME

| Field | Details |
|-------|---------|
| **Title** | BanHateME: Understanding Hate in Bangla Memes through Detection, Categorization, and Target Profiling |
| **Authors** | Md Ayon Mia, Md Fahim |
| **Year** | 2025 |
| **Venue** | Proceedings of the Second Workshop on Bangla Language Processing (BLP-2025), EMNLP 2025 |
| **Link** | https://aclanthology.org/2025.banglalp-1.15/ |
| **Problem** | No Bangla multimodal hate meme dataset; prior resources only binary-labeled; cultural visual cues understudied. |
| **Task Type** | Multimodal Hate Speech Detection (text + image, meme analysis) |
| **Dataset** | BanHateME: 3,819 Bangla memes with 3-level hierarchical annotations (binary, category, target group) |
| **Method / Model** | Multimodal fusion (summation, concatenation, co-attention) of pretrained language + vision models; hierarchical loss function |
| **Evaluation Metric** | Not clearly stated |
| **Main Result** | Co-attention fusion with hierarchical loss most effective; cross-modal alignment improves fine-grained classification |
| **Contribution** | First hierarchically annotated Bangla hateful meme dataset; novel hierarchical loss; multimodal fusion study |
| **Limitation** | Small dataset (3,819 memes); cultural cue interpretation remains hard for models |

**বিগিনার বাংলায় সারসংক্ষেপ:**
মিম (meme) হলো ছবি ও লেখার মিশ্রণ — এগুলোতে অনেক সময় ঘৃণাসূচক বার্তা থাকে, বিশেষত বাংলাদেশের সামাজিক মাধ্যমে। এই পেপারে BanHateME নামে ৩,৮১৯টি বাংলা মিমের একটি dataset তৈরি হয়েছে, যেখানে তিন স্তরে annotation আছে। ছবি ও টেক্সট একসাথে বিশ্লেষণ করার জন্য co-attention fusion পদ্ধতি সবচেয়ে ভালো কাজ করেছে। এই পেপারটি আমার thesis-এ multimodal NLP gap দেখানোর জন্য ব্যবহার করা যাবে।

---

### Paper 8 — CheckSent-BN

| Field | Details |
|-------|---------|
| **Title** | CheckSent-BN: A Bengali Multi-Task Dataset for Claim Checkworthiness and Sentiment Classification from News Headlines |
| **Authors** | Pritam Pal, Dipankar Das |
| **Year** | 2025 |
| **Venue** | Proceedings of the Second Workshop on Bangla Language Processing (BLP-2025), EMNLP 2025 |
| **Link** | https://aclanthology.org/2025.banglalp-1.10/ |
| **Problem** | No Bengali annotated dataset for claim checkworthiness; no joint checkworthiness + sentiment benchmark. |
| **Task Type** | Multi-task: Claim Checkworthiness Detection + Sentiment Classification |
| **Dataset** | CheckSent-BN: ~11,500 Bengali news headlines; annotated by LLMs + manual verification |
| **Method / Model** | IndicBERTv2, BanglaBERT, mDeBERTa in single-task and MTL frameworks |
| **Evaluation Metric** | F1 / Accuracy (MTL setting) |
| **Main Result** | IndicBERTv2 achieves best overall MTL performance; BanglaBERT and mDeBERTa competitive |
| **Contribution** | First Bengali joint claim checkworthiness + sentiment dataset; cost-effective LLM annotation pipeline |
| **Limitation** | LLM-annotated labels may have noise; headlines only; single domain |

**বিগিনার বাংলায় সারসংক্ষেপ:**
এই পেপারে CheckSent-BN নামে বাংলা সংবাদ শিরোনামের একটি dataset তৈরি করা হয়েছে, যেখানে প্রায় ১১,৫০০টি headline আছে। প্রতিটি headline-এর জন্য দুটি label দেওয়া আছে: এটি fact-check করার যোগ্য কিনা, এবং এর sentiment কী। LLM দিয়ে annotation করে manually যাচাই করা হয়েছে। IndicBERTv2 মডেল multi-task learning-এ সেরা ফলাফল দিয়েছে। এই গবেষণা আমার thesis-এ misinformation detection এবং sentiment analysis গবেষণার gap দেখাতে কাজে লাগবে।

---

### Paper 9 — BanglaTalk

| Field | Details |
|-------|---------|
| **Title** | BanglaTalk: Towards Real-Time Speech Assistance for Bengali Regional Dialects |
| **Authors** | Jakir Hasan, Shubhashis Roy Dipta |
| **Year** | 2025 |
| **Venue** | Proceedings of the Second Workshop on Bangla Language Processing (BLP-2025), EMNLP 2025 |
| **Link** | https://aclanthology.org/2025.banglalp-1.4/ |
| **Problem** | No real-time speech assistant for Bengali regional dialects; existing systems support standard Bengali only. |
| **Task Type** | Automatic Speech Recognition (ASR) / Real-time Speech System |
| **Dataset** | RegSpeech12 (10 Bengali regional dialects) |
| **Method / Model** | BRDialect: IndicWav2Vec fine-tuned on 10 Bengali dialects; client-server RTP architecture |
| **Evaluation Metric** | WER (Word Error Rate) |
| **Main Result** | WER reduced by 12.41–33.98% vs baseline; average end-to-end delay 4.9s at 24 kbps |
| **Contribution** | First real-time dialect-aware Bengali speech assistant; first dialect ASR model (BRDialect) for 10 dialects |
| **Limitation** | 4.9s delay limits conversational use; evaluation on RegSpeech12 only |

**বিগিনার বাংলায় সারসংক্ষেপ:**
এই পেপারে BanglaTalk নামে বাংলার আঞ্চলিক উপভাষার জন্য প্রথম real-time speech assistant তৈরি করা হয়েছে। BRDialect মডেলটি ১০টি আঞ্চলিক উপভাষায় কথা বোঝার জন্য IndicWav2Vec-কে fine-tune করে তৈরি। এটি baseline-এর তুলনায় ওয়ার্ড এরর ১২–৩৪% কমিয়েছে এবং মাত্র ২৪ kbps-এ কাজ করে। আমার thesis-এর জন্য এটি dialectal speech এবং low-resource language technology-র একটি গুরুত্বপূর্ণ উদাহরণ।

---

### Paper 10 — Reveal-Bangla

| Field | Details |
|-------|---------|
| **Title** | Reveal-Bangla: A Dataset for Cross-Lingual Multi-Step Reasoning Evaluation |
| **Authors** | Khondoker Ittehadul Islam, Gabriele Sarti |
| **Year** | 2025 |
| **Venue** | Proceedings of the Second Workshop on Bangla Language Processing (BLP-2025), EMNLP 2025 |
| **Link** | https://aclanthology.org/2025.banglalp-1.3/ |
| **Problem** | Multi-step reasoning in Bangla completely unevaluated; unclear whether models can exploit Bangla reasoning chains. |
| **Task Type** | Multi-step Reasoning / QA / Cross-lingual Evaluation |
| **Dataset** | Reveal-Bangla: manually translated from English Reveal dataset; binary + non-binary question types (size not clearly stated) |
| **Method / Model** | Controlled evaluation of English-centric and Bangla-centric multilingual small language models (SLMs) |
| **Evaluation Metric** | Not clearly stated |
| **Main Result** | Models struggle to use Bangla reasoning steps; reasoning context benefits non-binary questions; cross-lingual gap exposed |
| **Contribution** | First Bangla multi-step reasoning dataset; controlled cross-lingual evaluation revealing Bangla reasoning chain underuse |
| **Limitation** | Manually translated; only small language models evaluated; no large model (GPT-4 class) comparison |

**বিগিনার বাংলায় সারসংক্ষেপ:**
এই পেপারে Reveal-Bangla নামে একটি dataset তৈরি করা হয়েছে যেখানে বাংলায় multi-step reasoning মূল্যায়ন করা হয়েছে — অর্থাৎ একটি প্রশ্নের উত্তর দেওয়ার জন্য কয়েক ধাপে চিন্তা করার দক্ষতা। ইংরেজি Reveal dataset থেকে অনুবাদ করে binary ও non-binary প্রশ্ন তৈরি করা হয়েছে। ফলাফলে দেখা গেছে মডেলগুলো বাংলা reasoning step ঠিকভাবে ব্যবহার করতে পারে না। এই গবেষণা আমার thesis-এ বাংলায় reasoning-এর gap দেখানোর জন্য গুরুত্বপূর্ণ।

---

*Batch 1 complete — 10 papers. All links verified via ACL Anthology. Awaiting review before Batch 2.*
