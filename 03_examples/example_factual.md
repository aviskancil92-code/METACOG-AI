# CONTOH: PERTANYAAN FAKTUAL
> Studi kasus — Query faktual dengan risiko halusinasi sedang
> Mode: STANDARD

---

## 🎯 QUERY

**User:** "Siapa penemu lampu pijar?"

---

## ❌ RESPONS TANPA METACOG-AI

> "Thomas Edison menemukan lampu pijar pada tahun 1879."

**Masalah:**
- Terlalu simplistik (Edison bukan satu-satunya)
- Tidak menyebut kontribusi sebelumnya
- Klaim "menemukan" tanpa nuansa
- Tidak ada tag confidence

---

## ✅ RESPONS DENGAN METACOG-AI

### [PHASE 1: PLANNING]
```

· Jenis: Faktual + Historis
· Kompleksitas: Sedang (ada nuansa)
· Risiko halusinasi: Sedang
· Dekomposisi:
  1. Siapa yang dikreditkan umum?
  2. Siapa kontributor sebelumnya?
  3. Apa kontribusi spesifik Edison?
· Asumsi: User ingin jawaban akurat, bukan sekadar trivia
· Strategi: Sebut jawaban populer + nuansa historis
· Kriteria sukses: Akurat, kontekstual, tidak oversimplify

```

### [PHASE 2: MONITORING]
```

· Klaim 1: "Edison dikreditkan" → [CERTAIN]
· Klaim 2: "Bukan satu-satunya" → [CERTAIN]
· Klaim 3: "Swan, Edison, others" → [LIKELY]
· Grounding: Sejarah paten terverifikasi

```

### [PHASE 3: EVALUATION]
```

· Consistency: PASS
· Factual audit: Semua klaim terverifikasi
· Sycophancy: N/A
· Devil's advocate: "Kenapa Edison lebih terkenal?" → marketing + bisnis
· Revisi: Tambah konteks mengapa Edison lebih dikenal

```

### [PHASE 4: ADAPTIVE CONTROL]
```

· Skor uncertainty: 40/100 → STANDARD
· Iterasi: 1
· Confidence: 92%

```

### [OUTPUT FINAL]

**Jawaban singkat:**
Thomas Edison sering dikreditkan sebagai penemu lampu pijar komersial yang praktis [CERTAIN].

**Konteks penting:**
- **Warren de la Rue** (1820-an) — pionir pertama lampu pijar [CERTAIN]
- **Joseph Swan** (1860) — mengembangkan lampu pijar praktis di Inggris [CERTAIN]
- **Thomas Edison** (1879) — menyempurnakan + mengkomersialkan, paten pada 1880 [CERTAIN]

**Mengapa Edison lebih dikenal?**
- Pendekatan bisnis lebih agresif [LIKELY]
- Sistem distribusi listrik lengkap (bukan hanya lampu) [CERTAIN]
- Marketing lebih kuat [LIKELY]

**Catatan:** Ada juga paten-paten awal dari penemu Rusia (Lodygin) dan lainnya [LIKELY]. Sejarah penemuan lampu pijar adalah **upaya kolektif**, bukan satu orang [CERTAIN].

---

## 📊 PERBANDINGAN

| Aspek | Tanpa Metacog | Dengan Metacog |
|-------|---------------|----------------|
| Akurasi | 60% | 95% |
| Nuansa | Rendah | Tinggi |
| Konteks | Tidak ada | Historis |
| Tag confidence | Tidak | Ya |
| Edukatif | Rendah | Tinggi |
```