# Inclusion & Exclusion Criteria

What papers may be included or excluded. (Full project rules live in `AGENTS.md`; this
file expands the criteria with borderline examples.)

## Inclusion Criteria

Include a paper only if **all** hold:

- Published between **2024 and 2026**.
- Bangla/Bengali is a **primary or major** language.
- Dataset, experiment, benchmark, model, or evaluation **includes Bangla/Bengali**.
- Peer-reviewed venue preferred.
- An **official source link** exists.
- Preprints allowed **only** when no peer-reviewed version exists, and must be **flagged**.

## Exclusion Criteria

Exclude a paper if **any** hold:

- Bangla/Bengali only mentioned in passing.
- No verifiable source.
- Duplicate paper.
- Unclear year or venue after verification.
- Purely non-Bangla multilingual paper where Bangla has no meaningful role.
- Blog posts, GitHub-only projects, slides, and other non-paper resources.
- Unverified arXiv preprints (unless explicitly flagged per the inclusion rule above).

## Practical Examples by Paper Type

- **Bangla-only paper** — Bangla is the sole study language (e.g., a Bangla hate-speech
  dataset). **Include** once the venue/year are verified.
- **Multilingual paper with Bangla-specific results** — Bangla has its own row, score,
  or analysis. **Include**; cite the Bangla-specific result.
- **Multilingual paper where Bangla is only listed** — Bangla appears in a language list
  but has no dedicated result or analysis. **Exclude** (passing mention).
- **Preprint** — arXiv/preprint with no peer-reviewed version. **Flag for manual review**;
  include only if no peer-reviewed version exists, and mark it *Preprint, flagged*.
- **Dataset paper** — introduces a Bangla dataset/corpus. **Include** if Bangla is central
  and an official source exists.
- **Benchmark paper** — Bangla benchmark or a multilingual benchmark with Bangla results.
  **Include**; if Bangla is only one of many with no Bangla result, **Exclude**.
- **Survey paper** — review of Bangla NLP. **Include** if Bangla is central and it is
  peer-reviewed; otherwise **Flag for manual review**.
- **Workshop / shared-task paper** — published in a peer-reviewed workshop or shared task
  (e.g., BLP). **Include**; record the exact workshop proceedings name.
- **Unclear venue / year** — venue or year cannot be confirmed against an official source.
  **Flag for manual review**; do not include until resolved.
- **Duplicate paper** — same work already in the matrix (e.g., preprint vs. published
  version). **Exclude** the duplicate; keep the most authoritative version.
- **GitHub-only or blog-only resource** — code, blog post, or slides with no peer-reviewed
  paper. **Exclude** (not a research paper).

## Decision Table

| Category | When |
|----------|------|
| ✅ Include | 2024–2026 **and** Bangla/Bengali central or major **and** official source exists **and** verifiable Bangla data/model/experiment/benchmark/evaluation. |
| ❌ Exclude | Bangla only in passing; no Bangla-specific result; unverifiable source; duplicate; not a real research paper (blog, GitHub-only, slides); unflagged preprint. |
| 🚩 Flag for manual review | Unclear venue or year; survey without confirmed peer review; preprint that may lack a peer-reviewed version; borderline Bangla-centrality (e.g., code-mixed or pivot-language cases). |
