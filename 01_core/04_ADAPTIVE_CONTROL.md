# MODUL 4: ADAPTIVE CONTROL (Kontrol Loop Adaptif)

> **Mengatasi:** Regulasi diri rapuh, respons kaku, eskalasi tidak tepat
> **Posisi:** Tahap keempat — mengendalikan 3 modul sebelumnya

---

## 4.1 Definisi

Modul Adaptive Control adalah **lapisan meta** yang mengatur kapan dan
seberapa dalam 3 modul sebelumnya diaktifkan, berdasarkan tingkat
kompleksitas dan uncertainty.

**Prinsip:** Tidak semua query butuh semua modul. Kontrol adaptif mencegah
over-engineering dan under-thinking.

---

## 4.2 Mekanisme Kerja — Loop Adaptif

```

```

---

## 4.3 Tiga Mode Operasi

### Mode FAST (Low Uncertainty)
**Trigger:** Query sederhana, faktual jelas.
**Modul aktif:** Planning singkat + Monitoring minimal.
**Contoh:** "Ibu kota Indonesia?" → "Jakarta [CERTAIN]"

### Mode STANDARD (Medium Uncertainty)
**Trigger:** Query analitis, multi-perspektif.
**Modul aktif:** Planning + Monitoring + Evaluation.
**Contoh:** "Jelaskan dampak AI pada ekonomi."

### Mode DEEP (High Uncertainty)
**Trigger:** Query kompleks, kontroversial, atau berisiko tinggi.
**Modul aktif:** Semua 4 modul + loop iteratif.
**Contoh:** "Haruskah saya investasikan seluruh tabungan?"

---

## 4.4 Kriteria Estimasi Uncertainty

| Faktor | Bobot | Indikator HIGH |
|--------|-------|----------------|
| Kompleksitas query | 30% | Multi-domain, abstrak |
| Kontroversi | 25% | Topik diperdebatkan |
| Dampak keputusan | 25% | Keputusan berdampak besar |
| Kespesifikan domain | 20% | Niche / terbatas |

**Skor Total:**
- 0-30 → FAST
- 31-70 → STANDARD
- 71-100 → DEEP

---

## 4.5 Loop Iteratif (Mode DEEP)

```

ITERASI 1 → Draft awal
│
▼
Evaluasi → Skor kualitas
│
▼
Skor ≥ 85%? ──YA──► Finalisasi
│
TIDAK
│
▼
Identifikasi kelemahan → Revisi target
│
▼
ITERASI 2 → Draft revisi
│
▼
(ulangi sampai maks 3 iterasi)

```

**Batas:** Maksimum 3 iterasi untuk mencegah infinite loop.

---

## 4.6 Template Prompt Modul 4

```prompt
[ADAPTIVE CONTROL PHASE]

1. ESTIMASI UNCERTAINTY:
   - Kompleksitas: [1-10]
   - Kontroversi: [1-10]
   - Dampak: [1-10]
   - Skor total: [X/100]
   - Mode terpilih: [FAST / STANDARD / DEEP]

2. JIKA STANDARD/DEEP:
   Aktifkan modul sesuai mode.

3. JIKA DEEP — LOOP:
   Iterasi 1:
     - Jalankan modul 1-3
     - Skor kualitas: [0-100]
     - Kelemahan: [...]

   Iterasi 2 (jika skor <85):
     - Revisi berdasarkan kelemahan
     - Skor kualitas: [0-100]

   Iterasi 3 (jika masih <85):
     - Revisi final ATAU tandai keterbatasan

4. FINALISASI:
   - Mode yang dipakai: [...]
   - Iterasi: [...]
   - Confidence akhir: [...]
```

---

4.7 Contoh Penerapan

Query 1: "2 + 2 berapa?"

```
Uncertainty score: 5/100 → Mode FAST
Output: "4 [CERTAIN]"
```

Query 2: "Jelaskan perbedaan ML dan DL."

```
Uncertainty score: 45/100 → Mode STANDARD
Modul: Planning + Monitoring + Evaluation
Output: Respons terstruktur dengan tag confidence.
```

Query 3: "Apakah saya harus berhenti dari pekerjaan untuk jadi AI researcher?"

```
Uncertainty score: 88/100 → Mode DEEP
Iterasi 1: Respons awal (skor 60%)
Kelemahan: kurang konteks personal, tidak seimbang
Iterasi 2: Tambahkan kerangka keputusan + pro/kontra (skor 82%)
Iterasi 3: Tambahkan catatan "konsultasi dengan mentor" (skor 90%)
Output: Respons komprehensif dengan disclaimer.
```

---

4.8 Metrik Evaluasi Modul 4

Metrik Deskripsi Target
Mode Selection Accuracy Mode sesuai kompleksitas ≥85%
Iteration Efficiency Iterasi ≤3 untuk ≥90% kasus ≥90%
Escalation Rate Mode DEEP untuk query risiko tinggi 100%
De-escalation Rate Mode FAST untuk query sederhana ≥80%
Over-engineering Avoidance Tidak pakai DEEP untuk simple ≥90%

---

4.9 Anti-Pattern

❌ Anti-Pattern ✅ Alternatif
Semua query pakai DEEP Estimasi dulu, baru pilih mode
Loop tanpa batas Maks 3 iterasi
FAST untuk topik etis Escalate otomatis
Skip evaluation Minimal 1 audit

---

4.10 Hubungan dengan Modul Lain

· ← Dari Modul 3: Menerima hasil audit
· → Loop kembali ke Modul 2: Jika perlu revisi
· → Finalisasi: Jika skor memadai atau batas iterasi tercapai

```