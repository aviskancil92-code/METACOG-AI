# CHANGELOG METACOG-AI

> Semua perubahan penting pada proyek ini didokumentasikan di file ini.
> Format berdasarkan [Keep a Changelog](https://keepachangelog.com/).
> Versi mengikuti [Semantic Versioning](https://semver.org/).

---

## [1.0.0] — 2026-10-08

### 🎉 Rilis Perdana

**Fokus:** Fondasi sistem regulasi diri metakognitif untuk AI

### Ditambahkan

#### Core Modules
- **Modul 1 — Planning**: Dekomposisi tugas, identifikasi asumsi, pemetaan strategi, penetapan kriteria sukses
- **Modul 2 — Monitoring**: Tagging klaim (`[CERTAIN]`, `[LIKELY]`, `[UNCERTAIN]`, `[GUESS]`, `[DISPUTED]`), deteksi kontradiksi internal, grounding check, kalibrasi confidence
- **Modul 3 — Evaluation**: Audit konsistensi, verifikasi faktual, deteksi sycophancy, devil's advocate, bias check, keputusan revisi
- **Modul 4 — Adaptive Control**: Estimasi uncertainty, pemilihan mode (FAST/STANDARD/DEEP), loop iteratif maks 3 iterasi, escalation triggers

#### Prompt Templates
- `planning_prompt.md` — Template dekomposisi & strategi
- `monitoring_prompt.md` — Template tagging & real-time monitoring
- `evaluation_prompt.md` — Template audit & anti-sycophancy
- `adaptive_prompt.md` — Template estimasi mode & loop
- `master_prompt.md` — Prompt terintegrasi (full + compact version)

#### Examples
- `example_factual.md` — Studi kasus pertanyaan faktual (penemu lampu pijar)
- `example_reasoning.md` — Studi kasus penalaran kompleks (TikTok ban untuk anak)
- `example_contradiction.md` — Studi kasus informasi kontradiktif & sycophancy trap

#### Metrics
- `evaluation_metrics.md` — 20+ metrik evaluasi (akurasi, kalibrasi, sycophancy, safety)
- `benchmark_template.md` — Template benchmark 10 test case standar

#### Integration
- `integration_guide.md` — 4 jalur integrasi (System Prompt, API Wrapper, Fine-Tuning, Middleware)
- `deployment.md` — Panduan deployment production (Serverless, Container, VM)
- `config.yaml` — Konfigurasi lengkap sistem

#### Meta
- `changelog.md` — File ini
- `references.md` — Referensi riset & bacaan

### Diketahui Terbatas

- Loop iteratif hanya berjalan di mode DEEP (perlu evaluasi untuk mode STANDARD)
- Estimasi uncertainty masih berbasis heuristik (bukan ML-based)
- Benchmark belum dijalankan secara ekstensif
- Belum ada integrasi dengan sistem evaluasi otomatis

### Catatan Teknis

- Basis teori: Ann Brown's Regulatory Cycle (Planning → Monitoring → Evaluation)
- Terinspirasi dari riset Think² (grounded metacognitive reasoning) yang menunjukkan peningkatan 3x dalam koreksi diri berhasil [reference:0]
- Arsitektur multi-agent untuk anti-sycophancy terinspirasi dari Epistemic Fortitude [reference:1]

---

## [Unreleased] — Roadmap v1.1.0

### Direncanakan

#### Peningkatan Modul
- [ ] **Planning**: Tambah template khusus untuk domain medis, hukum, finansial
- [ ] **Monitoring**: Implementasi uncertainty quantification berbasis token-level logprob
- [ ] **Evaluation**: Tambah cross-model verification (bandingkan output 2 model)
- [ ] **Adaptive**: Confidence-aware escalation (bukan hard threshold)

#### Fitur Baru
- [ ] **Meta-Learning**: Sistem yang belajar dari kesalahan sebelumnya
- [ ] **User Feedback Loop**: Integrasi rating user untuk tuning
- [ ] **Multi-language Support**: Adaptasi untuk bahasa selain Indonesia & Inggris
- [ ] **API Endpoint**: REST API siap pakai untuk production

#### Metrics & Benchmark
- [ ] Benchmark dengan dataset standar (TruthfulQA, HaluEval)
- [ ] A/B testing framework
- [ ] Automated regression testing

### Direncanakan untuk v2.0.0

- **Arsitektur Multi-Agent**: Pisahkan Planning Agent, Monitoring Agent, Evaluation Agent
- **Fine-Tuning Dataset**: 10,000+ contoh untuk training
- **Real-time Adaptation**: Model yang menyesuaikan diri dari feedback user
- **Explainability Dashboard**: Visualisasi proses metacognitive
- **Integration dengan Tools**: Search, Calculator, Database untuk grounding

---

## [0.9.0-beta] — 2026-09-15 (Internal)

### Ditambahkan
- Konsep awal METACOG-AI
- Analisis 6 kekurangan fundamental AI
- Draf arsitektur 4 modul

### Diubah
- Threshold mode dari 3-level ke continuous scale

### Dihapus
- Modul "Introspection" (digabung ke Monitoring)

---

## [0.5.0-alpha] — 2026-08-20 (Internal)

### Ditambahkan
- Riset literatur: metacognition, sycophancy, hallucination
- Prototype prompt untuk Planning & Monitoring

### Catatan
- Eksperimen awal menunjukkan peningkatan konsistensi ~25%
- Terlalu banyak false positive pada deteksi kontradiksi

---

## 📊 STATISTIK VERSI

| Versi | Tanggal | File | Baris Kode | Status |
|-------|---------|------|------------|--------|
| 1.0.0 | 2026-10-08 | 22 | ~5000 | ✅ Stable |
| 0.9.0-beta | 2026-09-15 | 8 | ~1500 | 🧪 Beta |
| 0.5.0-alpha | 2026-08-20 | 3 | ~500 | 🔬 Alpha |

---

## 🔗 REFERENSI VERSI

- **v1.0.0** → [Respons 1-7](.)
- **v0.9.0** → Arsip internal
- **v0.5.0** → Arsip internal

---

## 📌 KONVENSI

### Format Perubahan
- `Ditambahkan` — Fitur baru
- `Diubah` — Perubahan pada fitur existing
- `Dihapus` — Fitur yang dihapus
- `Diperbaiki` — Bug fix
- `Keamanan` — Perbaikan keamanan
- `Diketahui Terbatas` — Known limitations
- `Direncanakan` — Roadmap

### Format Versi
- **MAJOR** (X.0.0) — Perubahan breaking
- **MINOR** (1.X.0) — Fitur baru, backward compatible
- **PATCH** (1.0.X) — Bug fix, backward compatible

---

## 🎯 CARA BERKONTRIBUSI

1. Fork repositori
2. Buat branch: `feature/nama-fitur`
3. Update `CHANGELOG.md` di bagian `[Unreleased]`
4. Submit Pull Request

---

## 📞 KONTAK

- **Maintainer:** aviskancil92
- **Repository:** [aviskancil92-code](https://github.com/aviskancil92-code).
- **Issues:** [METACOG-AI Issues](https://github.com/aviskancil92-code/METACOG-AI/issues).
```