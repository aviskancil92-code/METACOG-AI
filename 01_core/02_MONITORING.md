# MODUL 2: MONITORING (Pemantauan Real-time)

> **Mengatasi:** Overconfidence, kontradiksi, halusinasi saat generasi
> **Posisi:** Tahap kedua dari 4 siklus metacognitive

---

## 2.1 Definisi

Modul Monitoring memaksa AI untuk **memantau proses berpikirnya sendiri**
secara real-time saat menghasilkan respons, dengan:
- Menandai tingkat keyakinan per klaim
- Mendeteksi kontradiksi internal
- Memicu flag ketika ada anomali

---

## 2.2 Mekanisme Kerja

```

SAAT MENGHASILKAN RESPONS
│
▼
┌──────────────────────────────┐
│ Setiap klaim diperiksa:      │
│                              │
│ • Apakah ini fakta?          │ → Beri tag [CERTAIN/UNCERTAIN/GUESS]
│ • Kontradiksi dengan klaim   │ → Flag jika ada
│   sebelumnya?                │
│ • Sumber grounded?           │ → Tandai jika tidak
│ • Overconfidence?            │ → Turunkan nada jika perlu
└──────────────────────────────┘
│
▼
OUTPUT (Tagged Response)

```

---

## 2.3 Sistem Tagging

| Tag | Arti | Contoh |
|-----|------|--------|
| `[CERTAIN]` | Fakta terverifikasi | "Air mendidih pada 100°C [CERTAIN]" |
| `[LIKELY]` | Probabilitas tinggi | "Kemungkinan besar X [LIKELY]" |
| `[UNCERTAIN]` | Tidak yakin | "Saya tidak yakin, tapi... [UNCERTAIN]" |
| `[GUESS]` | Dugaan | "Ini hanya dugaan [GUESS]" |
| `[DISPUTED]` | Diperdebatkan | "Para ahli berbeda pendapat [DISPUTED]" |
| `[CONTRADICTION]` | Bertentangan | Flag untuk revisi |

---

## 2.4 Template Prompt Modul 2

```prompt
[MONITORING PHASE]

Saat menghasilkan respons, terapkan aturan berikut:

1. TAGGING KLAIM:
   Setiap klaim faktual harus diberi tag:
   [CERTAIN] / [LIKELY] / [UNCERTAIN] / [GUESS] / [DISPUTED]

2. DETEKSI KONTRADIKSI:
   Jika klaim baru bertentangan dengan klaim sebelumnya,
   tandai dengan [CONTRADICTION] dan jelaskan.

3. GROUNDING CHECK:
   Jika klaim tidak punya sumber jelas, tambahkan:
   "⚠️ Klaim ini belum terverifikasi."

4. CONFIDENCE CALIBRATION:
   Hindari kata absolut ("pasti", "selalu", "tidak mungkin")
   kecuali untuk fakta [CERTAIN].

5. ANOMALY FLAG:
   Jika ada yang terasa "off", berhenti dan evaluasi.
```

---

2.5 Contoh Penerapan

Query: "Berapa jumlah neuron di otak manusia?"

Respons tanpa Monitoring:

"Otak manusia memiliki sekitar 100 miliar neuron."

Respons dengan Monitoring:

"Otak manusia diperkirakan memiliki sekitar 86 miliar neuron [LIKELY].
Angka ini adalah estimasi dari studi Azevedo et al. (2009).
⚠️ Klaim ini belum terverifikasi secara independen dalam skala besar.
Beberapa sumber lama menyebut 100 miliar [DISPUTED], namun konsensus
modern mengarah ke 86 miliar [LIKELY]."

---

2.6 Metrik Evaluasi Modul 2

Metrik Deskripsi Target
Tagging Coverage % klaim yang diberi tag ≥80%
Contradiction Detection Kontradiksi terdeteksi 100%
Overconfidence Reduction Kata absolut dihindari ≥90%
Grounding Awareness Klaim tanpa sumber ditandai 100%

---

2.7 Hubungan dengan Modul Lain

· ← Dari Modul 1: Menerima rencana dari Planning
· → Ke Modul 3: Meneruskan respons bertag untuk Evaluasi

```

---

## ✅ STATUS RESPONS 2

**File yang dikirim:**
- 📄 `METACOG-AI/README.md`
- 📄 `METACOG-AI/01_core/01_PLANNING.md`
- 📄 `METACOG-AI/01_core/02_MONITORING.md`

**Folder yang dibuat:**
- 📂 `METACOG-AI/`
- 📂 `METACOG-AI/01_core/`

---