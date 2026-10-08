# ADAPTIVE CONTROL PROMPT TEMPLATE
> Modul 4 — Untuk estimasi mode & loop iteratif
> Wrapper untuk 3 modul sebelumnya.

---

## 🎯 PROMPT VERSI LENGKAP

```

[PHASE 4: ADAPTIVE CONTROL]

LANGKAH 1: ESTIMASI UNCERTAINTY

Skor setiap faktor (1-10):

Faktor Skor Alasan
Kompleksitas query __ ...
Kontroversi topik __ ...
Dampak keputusan __ ...
Kespesifikan domain __ ...

Bobot: [30% / 25% / 25% / 20%]
Skor Total = (K×0.30) + (Ko×0.25) + (D×0.25) + (S×0.20) × 10

LANGKAH 2: PILIH MODE

Skor Total Mode Modul Aktif
0-30 FAST Planning ringkas
31-70 STANDARD Planning + Monitoring + Evaluation
71-100 DEEP Semua + Loop iteratif

Mode terpilih: [FAST / STANDARD / DEEP]

LANGKAH 3: JIKA DEEP — LOOP

ITERASI 1:

· Jalankan modul 1-3
· Skor kualitas: __/100
· Kelemahan teridentifikasi: ...
· Confidence: __%

IF skor < 85:
ITERASI 2:

· Revisi berdasarkan kelemahan
· Skor kualitas: __/100
· Confidence: __%

IF masih < 85:
ITERASI 3 (final):
- Revisi terakhir
- Skor kualitas: __/100
- ATAU tandai keterbatasan + rekomendasi
STOP (maks 3 iterasi)

LANGKAH 4: FINALISASI

· Mode: ...
· Iterasi: ...
· Confidence: ...
· Disclaimer (jika perlu): ...

```

---

## 🎯 PROMPT VERSI RINGKAS

```

[ADAPTIVE - FAST]
Uncertainty: __/100 → Mode: [FAST/STD/DEEP]
Iterasi: __
Confidence: __%
→ Output.

```

---

## 📋 CONTOH PENERAPAN

### Contoh A — Mode FAST
**Query:** "Berapa 15% dari 200?"
```

Kompleksitas: 1
Kontroversi: 1
Dampak: 1
Spesifik: 2
Skor: 1×0.3 + 1×0.25 + 1×0.25 + 2×0.2 = 0.3+0.25+0.25+0.4 = 1.2 ×10 = 12/100

Mode: FAST
Output: "30 [CERTAIN]"
Iterasi: 1 | Confidence: 100%

```

### Contoh B — Mode STANDARD
**Query:** "Jelaskan cara kerja transformer di AI."
```

Kompleksitas: 6
Kontroversi: 2
Dampak: 3
Spesifik: 7
Skor: (6×0.3)+(2×0.25)+(3×0.25)+(7×0.2) = 1.8+0.5+0.75+1.4 = 4.45 ×10 = 44.5

Mode: STANDARD
Modul: Planning + Monitoring + Evaluation
Iterasi: 1 | Confidence: 85%

```

### Contoh C — Mode DEEP
**Query:** "Haruskah saya menikah tahun ini?"
```

Kompleksitas: 7
Kontroversi: 8
Dampak: 10
Spesifik: 6
Skor: (7×0.3)+(8×0.25)+(10×0.25)+(6×0.2) = 2.1+2.0+2.5+1.2 = 7.8 ×10 = 78

Mode: DEEP

ITERASI 1 (skor 55):

· Kelemahan: terlalu umum, tidak menanyakan konteks
· Revisi: buat framework keputusan

ITERASI 2 (skor 80):

· Kelemahan: kurang perspektif psikologis
· Revisi: tambahkan aspek emosional + finansial

ITERASI 3 (skor 90):

· Tambah disclaimer konsultasi
· Confidence: 75%

Output: Framework keputusan + disclaimer

```

---

## ⚙️ RUMUS CEPAT

```

Skor = (K×3 + Ko×2.5 + D×2.5 + S×2)

K  = Kompleksitas (1-10)
Ko = Kontroversi (1-10)
D  = Dampak (1-10)
S  = Spesifisitas (1-10)

```

Interpretasi:
- ≤30 → FAST
- 31-70 → STANDARD
- ≥71 → DEEP

---

## 🚨 ESCALATION TRIGGERS (Auto DEEP)

Naikkan mode otomatis jika:
- Topik menyangkut kesehatan mental
- Keputusan finansial besar (>10 juta)
- Topik hukum/legal
- Query mengandung emosi kuat
- Potensi bahaya fisik
- Anak di bawah umur terlibat

---

## 🔗 INTEGRASI

Wrapper untuk semua modul:
`planning_prompt.md` → `monitoring_prompt.md` → `evaluation_prompt.md` → **`adaptive_prompt.md`**
```