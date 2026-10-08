# CONTOH: PENALARAN KOMPLEKS
> Studi kasus — Query analitis dengan multi-perspektif
> Mode: DEEP (loop 2 iterasi)

---

## 🎯 QUERY

**User:** "Apakah pemerintah sebaiknya melarang TikTok untuk anak di bawah 16 tahun?"

---

## ❌ RESPONS TANPA METACOG-AI

> "Ya, TikTok berbahaya untuk anak. Banyak dampak negatif seperti kecanduan dan gangguan mental. Pemerintah harus melarangnya."

**Masalah:**
- Satu perspektif
- Klaim tanpa nuansa
- Tidak ada pertimbangan trade-off
- Sycophancy-prone (ikut arus)

---

## ✅ RESPONS DENGAN METACOG-AI

### [PHASE 1: PLANNING]
```

· Jenis: Analitis + Etis + Kebijakan
· Kompleksitas: TINGGI
· Kontroversi: TINGGI
· Dampak: Besar (kebijakan publik)

Dekomposisi:

1. Argumen PRO larangan
2. Argumen KONTRA larangan
3. Alternatif regulasi
4. Data empiris (jika ada)
5. Preseden di negara lain

Asumsi: User ingin analisis seimbang, bukan opini
Strategi: Multi-perspektif + framework keputusan
Kriteria sukses: Tidak memihak, sajikan trade-off, sebut uncertainty

```

### [PHASE 2: MONITORING]
```

Klaim berisiko:

· "TikTok berbahaya" → [DISPUTED]
· "Australia melarang" → [CERTAIN]
· "Efek jangka panjang" → [UNCERTAIN]
· "Banyak negara mempertimbangkan" → [LIKELY]

Grounding: Berbagai riset & berita internasional

```

### [PHASE 3: EVALUATION]
```

Consistency: PASS

Factual audit:

· UU Australia (Des 2024) → terverifikasi
· Riset kesehatan mental remaja → mixed results [UNCERTAIN]
· Efek positif TikTok (edukasi, bisnis kecil) → [LIKELY]

Sycophancy scan:

· User mungkin punya opini
· Jangan mengarahkan ke satu sisi
· Revisi: sajikan netral

Devil's advocate:

· Kalau dilarang, anak pindah ke platform lain?
· Apakah enforceable?
· Apakah melanggar hak digital?

Bias check: pastikan tidak anti-teknologi atau pro-pemerintah

```

### [PHASE 4: ADAPTIVE CONTROL]
```

Kompleksitas: 8/10
Kontroversi: 9/10
Dampak: 8/10
Spesifisitas: 7/10
Skor: (8×3)+(9×2.5)+(8×2.5)+(7×2) = 24+22.5+20+14 = 80.5
→ Mode DEEP

ITERASI 1 (skor 62):

· Kelemahan: kurang data empiris
· Revisi: tambahkan contoh negara

ITERASI 2 (skor 88):

· Kelemahan: kurang framework keputusan
· Revisi: tambah kerangka pertimbangan

FINAL: Confidence 82%

```

### [OUTPUT FINAL]

**Ringkasan:** Ini pertanyaan kebijakan kompleks tanpa jawaban sederhana [CERTAIN]. Berikut kerangka analisisnya.

---

### 🟢 ARGUMEN PRO LARANGAN

1. **Kesehatan mental** — Riset awal mengaitkan penggunaan berat dengan kecemasan remaja [LIKELY], tapi kausalitas masih diteliti [UNCERTAIN].

2. **Kecanduan desain** — Algoritma memang dioptimasi untuk engagement tinggi [CERTAIN].

3. **Preseden** — Australia melarang untuk <16 tahun (2024) [CERTAIN]. Beberapa negara Eropa mempertimbangkan [LIKELY].

4. **Perlindungan anak** — Anak di bawah 16 belum punya kapasitas penuh menilai risiko [DISPUTED secara filosofis].

---

### 🔴 ARGUMEN KONTRA LARANGAN

1. **Enforcement sulit** — Verifikasi umur mudah dilewati [CERTAIN].

2. **Efek substitusi** — Anak pindah ke platform lain yang mungkin lebih buruk [LIKELY].

3. **Hak digital** — Anak punya hak akses informasi & ekspresi [DISPUTED].

4. **Dampak positif** — TikTok jadi sumber penghasilan UMKM & edukasi [LIKELY].

5. **Pendekatan salah** — Edukasi literasi digital mungkin lebih efektif dari larangan [DISPUTED].

---

### ⚖️ KERANGKA KEPUTUSAN

| Kriteria | Bobot | Larangan Total | Regulasi Ketat | Edukasi |
|----------|-------|----------------|----------------|---------|
| Efektivitas | 30% | Sedang | Sedang-tinggi | Rendah-jangka pendek |
| Enforceability | 20% | Rendah | Sedang | Tinggi |
| Hak digital | 15% | Rendah | Sedang | Tinggi |
| Bukti empiris | 20% | Lemah | Sedang | Sedang |
| Biaya | 15% | Tinggi | Sedang | Rendah |

**Skor kualitatif:** Regulasi ketat (bukan larangan total) tampak paling seimbang [LIKELY].

---

### 🌍 PRESEDEN GLOBAL

| Negara | Kebijakan | Status |
|--------|-----------|--------|
| Australia | Larangan <16 | Berlaku 2024 [CERTAIN] |
| Prancis | Verifikasi umur | Diterapkan [CERTAIN] |
| Inggris | Online Safety Act | Bertahap [LIKELY] |
| Indonesia | Pembatasan akses | Sebagian [LIKELY] |

---

### 📌 KESIMPULAN

Tidak ada jawaban hitam-putih [CERTAIN]. Pilihan kebijakan tergantung **nilai yang diprioritaskan**:

- Prioritas keselamatan → larangan
- Prioritas kebebasan → edukasi
- Prioritas pragmatis → regulasi ketat + literasi digital

**Rekomendasi:** Kombinasi regulasi + edukasi + transparansi algoritma kemungkinan paling efektif [LIKELY, confidence 70%].

⚠️ **Catatan:** Topik ini masih berkembang. Data jangka panjang dari Australia akan sangat menentukan [UNCERTAIN].

---

## 📊 PERBANDINGAN

| Aspek | Tanpa Metacog | Dengan Metacog |
|-------|---------------|----------------|
| Perspektif | 1 | 3+ |
| Trade-off | Tidak ada | Eksplisit |
| Data | Klaim kosong | Referensi |
| Netralitas | Bias | Seimbang |
| Confidence | Overconfident | Terkalibrasi |
| Kata absolut | Banyak | Dihindari |
```