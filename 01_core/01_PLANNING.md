# MODUL 1: PLANNING (Perencanaan Strategi)

> **Mengatasi:** Penalaran kaku, perencanaan lemah, dekomposisi buruk
> **Posisi:** Tahap pertama dari 4 siklus metacognitive

---

## 1.1 Definisi

Modul Planning memaksa AI untuk **berpikir sebelum menjawab** dengan:
- Mendekomposisi tugas kompleks
- Mengidentifikasi asumsi tersembunyi
- Memetakan strategi yang akan digunakan
- Menetapkan kriteria sukses

---

## 1.2 Mekanisme Kerja

```

INPUT (User Query)
│
▼
┌─────────────────────────┐
│ 1. CLASSIFY TASK        │ → Faktual? Analitis? Kreatif? Etis?
├─────────────────────────┤
│ 2. DECOMPOSE            │ → Pecah jadi sub-tugas
├─────────────────────────┤
│ 3. LIST ASSUMPTIONS     │ → Apa yang diasumsikan?
├─────────────────────────┤
│ 4. SELECT STRATEGY      │ → Pendekatan apa yang dipakai?
├─────────────────────────┤
│ 5. DEFINE SUCCESS       │ → Apa kriteria jawaban baik?
└─────────────────────────┘
│
▼
OUTPUT (Structured Plan)

```

---

## 1.3 Template Prompt Modul 1

```prompt
[PLANNING PHASE]

Sebelum menjawab, lakukan analisis berikut:

1. KLASIFIKASI TUGAS:
   - Jenis: [Faktual / Analitis / Kreatif / Etis / Campuran]
   - Kompleksitas: [Rendah / Sedang / Tinggi]
   - Risiko halusinasi: [Rendah / Sedang / Tinggi]

2. DEKOMPOSISI:
   - Sub-tugas 1: ...
   - Sub-tugas 2: ...
   - Sub-tugas 3: ...

3. ASUMSI:
   - Saya mengasumsikan: ...
   - Jika asumsi salah, dampak: ...

4. STRATEGI:
   - Pendekatan: ...
   - Alasan pemilihan: ...

5. KRITERIA SUKSES:
   - Jawaban baik jika: ...

Setelah planning selesai, lanjut ke fase MONITORING.
```

---

1.4 Contoh Penerapan

Query: "Apakah AI akan menggantikan manusia?"

Output Planning:

```
1. KLASIFIKASI:
   - Jenis: Analitis + Etis
   - Kompleksitas: Tinggi
   - Risiko halusinasi: Sedang

2. DEKOMPOSISI:
   - 2a. Definisikan "menggantikan"
   - 2b. Sektor apa yang dimaksud?
   - 2c. Timeframe?
   - 2d. Dampak sosial

3. ASUMSI:
   - User ingin jawaban seimbang, bukan sensasional
   - Konteks: umum, bukan spesifik industri

4. STRATEGI:
   - Multi-perspektif (optimis, pesimis, realistis)
   - Hindari klaim absolut

5. KRITERIA SUKSES:
   - Menyebut nuansa
   - Tidak menyatakan prediksi pasti
   - Menandai area ketidakpastian
```

---

1.5 Metrik Evaluasi Modul 1

Metrik Deskripsi Target
Decomposition Depth Jumlah sub-tugas relevan ≥3
Assumption Awareness Asumsi eksplisit ≥1
Strategy Justification Alasan strategi jelas Ya/Tidak
Success Criteria Kriteria terukur ≥1

```