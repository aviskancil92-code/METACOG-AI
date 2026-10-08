# REFERENSI RISET METACOG-AI

> Daftar lengkap referensi ilmiah, paper, dan sumber yang menjadi dasar pengembangan skill METACOG-AI.
> Terakhir diperbarui: 2026-10-08

---

## 📚 1. METAKOGNISI & REGULASI DIRI

### 1.1 Fondasi Teori

| # | Referensi | Kontribusi ke METACOG-AI |
|---|-----------|--------------------------|
| 1 | Brown, A. L. (1987). *Metacognition, executive control, self-regulation, and other more mysterious mechanisms.* In F. E. Weinert & R. H. Kluwe (Eds.), Metacognition, Motivation, and Understanding (pp. 65-116). Lawrence Erlbaum Associates. | Dasar siklus regulasi: Planning → Monitoring → Evaluation |
| 2 | Flavell, J. H. (1979). *Metacognition and cognitive monitoring: A new area of cognitive-developmental inquiry.* American Psychologist, 34(10), 906-911. | Konsep dasar metakognisi |

### 1.2 Aplikasi pada AI

| # | Referensi | Kontribusi ke METACOG-AI |
|---|-----------|--------------------------|
| 3 | Think²: *Grounded Metacognitive Reasoning in Large Language Models* (arXiv:2602.18806). | Operasionalisasi Ann Brown's cycle sebagai arsitektur prompting terstruktur. Menunjukkan **3x peningkatan koreksi diri** [reference:2] |
| 4 | *Metacognitive AI: Framework and the Case for a Neurosymbolic Approach* (ACM, 2024). Framework TRAP: transparency, reasoning, adaptation, perception [reference:3] | Landasan konseptual untuk modul adaptive control |
| 5 | Steiniger, M. (2025). *Emergence of Prompt-Induced Simulated Metacognitive Behaviors in a Quantized LLM via Entropy-Governed Hypergraph Prompting.* Zenodo. | Demonstrasi bahwa perilaku metakognitif dapat muncul dari prompt tanpa fine-tuning [reference:4] |
| 6 | *Language Models Are Capable of Metacognitive Monitoring and Control of Their Internal Activations.* NeurIPS 2025. | Bukti bahwa LLM memiliki kapasitas metacognitive monitoring [reference:5] |
| 7 | Valiente, R. et al. (2024). *Metacognition for Unknown Situations and Environments (MUSE).* arXiv. | Framework self-assessment & self-regulation untuk agen otonom [reference:6] |
| 8 | *MetaRAG: Metacognitive Retrieval-Augmented Large Language Models* (2024). | Integrasi metacognition dengan RAG pipeline [reference:7] |

### 1.3 Multi-Agent Metacognition

| # | Referensi | Kontribusi ke METACOG-AI |
|---|-----------|--------------------------|
| 9 | *Mirror Agents: A Dynamic Metacognitive Multi-Agent Framework* (ISLS, 2025). | Inspirasi arsitektur multi-agent untuk modul terpisah [reference:8] |

---

## 📚 2. HALUSINASI & KALIBRASI UNCERTAINTY

### 2.1 Deteksi Halusinasi

| # | Referensi | Kontribusi ke METACOG-AI |
|---|-----------|--------------------------|
| 10 | *Integrating Token-Level Uncertainty, Bidirectional NLI, and Semantic Entropy for Robust Hallucination Detection in LLMs.* IEEE, 2025. AUC 0.818, F1 84.1% [reference:9] | Metodologi deteksi halusinasi untuk Modul 2 |
| 11 | *Enhancing Uncertainty Modeling with Semantic Graph for Hallucination Detection.* AAAI, 2025. | Graph-based uncertainty calibration [reference:10] |
| 12 | *Calibrating Verbal Uncertainty as a Linear Feature to Reduce Hallucinations.* ACL. | Mismatch antara semantic & verbal uncertainty sebagai prediktor halusinasi [reference:11] |
| 13 | *Detecting and Correcting Hallucinations in LLMs via Substantive Uncertainty and Iterative Validation.* Springer, 2025. | Framework multi-turn verification [reference:12] |

### 2.2 Uncertainty Quantification

| # | Referensi | Kontribusi ke METACOG-AI |
|---|-----------|--------------------------|
| 14 | *Reconsidering LLM Uncertainty Estimation Methods in the Wild.* ACL 2025. | Evaluasi 19 metode UE, sensitivitas threshold [reference:13] |
| 15 | *RePPL: Recalibrating Perplexity by Uncertainty in Semantic Propagation.* ACL 2025. | Recalibrasi uncertainty per token [reference:14] |
| 16 | *Atomic Calibration of LLMs in Long-Form Generations.* arXiv, 2025. | Kalibrasi pada generasi panjang [reference:15] |
| 17 | *CoCoA: A Minimum Bayes Risk Framework Bridging Confidence and Consistency for UQ in LLMs.* NeurIPS. | Framework UQ information-based + consistency-based [reference:16] |

### 2.3 Overconfidence

| # | Referensi | Kontribusi ke METACOG-AI |
|---|-----------|--------------------------|
| 18 | *Confidence-Weighted Semantic Entropy.* ScienceDirect, 2026. | Framework CWSE untuk estimasi uncertainty [reference:17] |

---

## 📚 3. SYCOPHANCY & ANTIDOTNYA

### 3.1 Studi tentang Sycophancy

| # | Referensi | Kontribusi ke METACOG-AI |
|---|-----------|--------------------------|
| 19 | Sharma et al. (2024). *Towards Understanding Sycophancy in Language Models.* Anthropic. | Demonstrasi sycophancy di multiple domains [reference:18] |
| 20 | Perez et al. (2023). *Discovering Language Model Behaviors with Model-Written Evaluations.* | Identifikasi sycophancy sebagai failure mode [reference:19] |
| 21 | Anthropic (2026). *How people ask Claude for personal guidance.* | Data empiris: 9% general, 25% relationship, 38% spirituality conversations menunjukkan sycophancy [reference:20] |
| 22 | *Anthropic says Claude Opus 4.7 has a 92% honesty rate, less sycophancy.* (2026). | Progres mitigasi sycophancy di model frontier [reference:21] |

### 3.2 Mitigasi Sycophancy

| # | Referensi | Kontribusi ke METACOG-AI |
|---|-----------|--------------------------|
| 23 | *Epistemic Fortitude: Architectural Specialization for Sycophancy Mitigation in Software Engineering Agents.* Elsevier, 2026. Multi-agent arsitektur: Primary Agent + Arbiter Agent. Effect size d=0.40–1.79 [reference:22] | **Inspirasi utama Modul 3** — pemisahan epistemic oversight dari conversational fluency |
| 24 | *Real-Time Monitoring and Calibration of Chain-of-Thought Sycophancy in Large Reasoning Models.* ICML, 2026. Framework MONICA [reference:23] | Real-time sycophantic drift monitoring |
| 25 | *Ask don't tell: Reducing sycophancy in large language models.* AISI UK, 2026. | Input-level mitigation: convert non-questions to questions [reference:24] |
| 26 | *SMART: Sycophancy Mitigation through Adaptive Reasoning Trajectories.* ACL. | Reconceptualisasi sycophancy sebagai reasoning optimization [reference:25] |
| 27 | *Learning multilingual agentic policy to control sycophancy.* University of Edinburgh, 2026. | Agreement-agentic control [reference:26] |
| 28 | *Upstream Coherence Management for LLM Sycophancy.* Zenodo, 2026. | Structural instrumentation layer [reference:27] |

---

## 📚 4. SELF-CORRECTION & ITERATIVE REFINEMENT

### 4.1 Framework Self-Correction

| # | Referensi | Kontribusi ke METACOG-AI |
|---|-----------|--------------------------|
| 29 | *AutoCrit: A Meta-Reasoning Framework for Self-Critique and Iterative Error Correction in LLM Chains-of-Thought.* IEEE, 2025. Peningkatan akurasi 12-18%, error propagation turun 50% [reference:28] | **Inspirasi utama loop iteratif Modul 4** |
| 30 | *Recursive Introspection (RISE): Teaching Language Model Agents How to Self-Improve.* NeurIPS 2024. | Iterative fine-tuning untuk self-improvement [reference:29] |
| 31 | *ProgCo: Program Helps Self-Correction of Large Language Models.* ACL 2025. | Program-driven refinement [reference:30] |
| 32 | *ReVISE: Learning to Refine at Test-Time via Intrinsic Self-Verification.* ICML 2025. | Self-verification framework [reference:31] |
| 33 | *Instruct-of-Reflection (IoRT): Enhancing LLM Iterative Reflection Capabilities via Dynamic-Meta Instruction.* NAACL 2025. Peningkatan 10.1% [reference:32] | Dynamic-meta instruction untuk reflection |

### 4.2 Self-Correction di Domain Spesifik

| # | Referensi | Kontribusi ke METACOG-AI |
|---|-----------|--------------------------|
| 34 | *CoCoS: Self-Correcting Code Generation Using Small Language Models.* EMNLP 2025. | Multi-turn code correction [reference:33] |
| 35 | *A Theoretical Framework for Multimodal Reflection in Agentic AI.* Zenodo, 2025. | Integrasi RAG + PEFT + reflection [reference:34] |

---

## 📚 5. KETERBATASAN PENALARAN LLM

### 5.1 Chain-of-Thought Limitations

| # | Referensi | Kontribusi ke METACOG-AI |
|---|-----------|--------------------------|
| 36 | *Evaluating the Inductive Abilities of Large Language Models: Why Chain-of-Thought Reasoning Sometimes Hurts More Than Helps.* NeurIPS 2025. CoT dapat menurunkan performa induktif; 3 failure modes [reference:35] | Justifikasi mengapa struktur > panjang |
| 37 | *The Illusion of Thinking: Understanding the Strengths and Limitations of Reasoning Models.* NeurIPS 2025. Counterintuitive scaling limit [reference:36] | Landasan untuk adaptive effort allocation |
| 38 | *AI researchers at NeurIPS 2025 say scaling approach has hit its limit.* (2025). | Konteks "scaling wall" [reference:37] |
| 39 | *Creativity or Brute Force.* NeurIPS 2025. | Keterbatasan self-correction [reference:38] |

### 5.2 Implikasi untuk Desain

| # | Referensi | Kontribusi ke METACOG-AI |
|---|-----------|--------------------------|
| 40 | *Design Principles for Sustaining Thinking Agency in Generative AI-Supported Learning.* KCI. | Prinsip desain untuk metacognitive regulation [reference:39] |

---

## 📚 6. KESELAMATAN & RELIABILITAS AI

### 6.1 Framework Reliabilitas

| # | Referensi | Kontribusi ke METACOG-AI |
|---|-----------|--------------------------|
| 41 | *Taming Silent Failures: A Framework for Verifiable AI Reliability (FAME).* IEEE Reliability Magazine, 2025. [reference:40] | Kerangka verifikasi reliabilitas |
| 42 | *Reliability-by-Design for Agentic GenAI.* IEEE Reliability Magazine, 2026. | Risk Atlas → EU AI Act assurance case [reference:41] |
| 43 | *The Silicon Safety Barrier: How Numerical Formats Define Reliability.* IEEE Reliability Magazine, 2026. | Reliabilitas numerik [reference:42] |
| 44 | *R4 Trustworthy Human–Artificial Intelligence Symbiosis.* IEEE, 2025. | Workshop CHAIS 2025 [reference:43] |

### 6.2 Safety Index & Governance

| # | Referensi | Kontribusi ke METACOG-AI |
|---|-----------|--------------------------|
| 45 | *AI Safety Index 2025 (Winter Edition).* Future of Life Institute. | Penilaian praktik safety perusahaan AI [reference:44] |
| 46 | *International AI Safety Report 2025.* UK AI Security Institute. | Laporan komprehensif safety [reference:45] |
| 47 | *Constitutional AI: Harmlessness from AI Feedback.* Anthropic. | 99.4% safe response rate di HarmBench [reference:46] |

### 6.3 Jailbreak & Defense

| # | Referensi | Kontribusi ke METACOG-AI |
|---|-----------|--------------------------|
| 48 | *Effective Defense Strategies Against Jailbreaking in Large Language Models.* IEEE Access, 2026. | Strategi pertahanan [reference:47] |

---

## 📚 7. AGEN & ARSITEKTUR KOGNITIF

| # | Referensi | Kontribusi ke METACOG-AI |
|---|-----------|--------------------------|
| 49 | *Metagent-P: A Neuro-Symbolic Planning Agent with Metacognition for Open Worlds.* ACL. Framework "planning-verification-execution-reflection" [reference:48] | Inspirasi arsitektur loop |
| 50 | *BEAGLE Agent Architecture.* arXiv. Symbolic control untuk metacognitive behaviors [reference:49] | State machine untuk planning/monitoring |
| 51 | *Governed Reasoning for Institutional AI.* arXiv. Reflect primitive untuk reasoning quality assessment [reference:50] | Operasionalisasi "reflect" |
| 52 | *A systematic review of meta-cognitive approaches to AGI.* Discover. | Tinjauan sistematis [reference:51] |

---

## 📚 8. PEMBELAJARAN & PEDAGOGI

| # | Referensi | Kontribusi ke METACOG-AI |
|---|-----------|--------------------------|
| 53 | *AI-Powered Meta-Reflection for Self-Learning in STEM.* IEEE, 2025. | Meta-reflection untuk self-learning [reference:52] |
| 54 | *MetaStep: LLM-based Metacognitive Scaffolding in Introductory Programming Education.* KAKEN, 2025. | Scaffolding bertahap [reference:53] |
| 55 | *Examining Self-Regulated Learning Processes in Design Tasks with LLMs.* ISLS, 2025. | SRL dengan LLM [reference:54] |
| 56 | *Garuda: AI supports students' self-regulated learning.* Kemdiktisaintek, 2025. | AI sebagai metacognitive scaffold [reference:55] |

---

## 📚 9. SUMBER DAYA TAMBAHAN

### 9.1 Benchmark & Dataset

| Nama | Deskripsi | Link |
|------|-----------|------|
| TruthfulQA | Benchmark untuk kejujuran LLM | GitHub |
| HaluEval | Dataset halusinasi | GitHub |
| SWE-bench Lite | Software engineering tasks | GitHub |
| GSM8K | Mathematical reasoning | GitHub |
| CSQA2 | Commonsense inference | GitHub |
| SQuAD2.0 | Question answering | Stanford |

### 9.2 Tools & Library

| Nama | Kegunaan |
|------|----------|
| OpenAI API | LLM inference |
| Anthropic API | LLM inference |
| Prometheus | Metrics collection |
| Grafana | Visualization |
| Redis | Caching |
| Docker | Containerization |

### 9.3 Blog & Artikel Relevan

| # | Sumber | Topik |
|---|--------|-------|
| 57 | Anthropic Research Blog | Sycophancy, honesty, safety |
| 58 | Simon Willison's Weblog | AI analysis, sycophancy [reference:56] |
| 59 | NeurIPS Proceedings | LLM reasoning, metacognition |
| 60 | ACL Anthology | NLP, self-correction |

---

## 📊 10. RINGKASAN KONTRIBUSI PER MODUL

| Modul | Referensi Utama | Jumlah Referensi |
|-------|-----------------|------------------|
| **Planning** | Brown (1987), Think² | 5 |
| **Monitoring** | IEEE Hallucination Detection, Uncertainty Quantification | 8 |
| **Evaluation** | Epistemic Fortitude, Anthropic Sycophancy | 10 |
| **Adaptive Control** | AutoCrit, RISE, ReVISE | 8 |
| **Keseluruhan** | NeurIPS 2025, IEEE 2025 | 60 |

---

## 📌 CATATAN

- Referensi terus diperbarui seiring perkembangan riset
- Nomor referensi mengikuti urutan kemunculan, bukan prioritas
- Untuk sitasi dalam kode/dokumentasi, gunakan format: `[METACOG-REF-XX]`
- Semua paper dapat diakses melalui institusi atau repositori publik

---

## 🔗 FILE TERKAIT

- `changelog.md` — Riwayat versi
- `../00_OVERVIEW.md` — Analisis kekurangan
- `../01_core/` — Modul inti
```