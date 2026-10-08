# MONITORING PROMPT TEMPLATE
> Modul 2 — Untuk tagging & pemantauan real-time
> Copy-paste saat menghasilkan respons panjang/berisiko.

---

## 🎯 PROMPT VERSI LENGKAP

```

[PHASE 2: MONITORING]

Saat menghasilkan respons, terapkan aturan berikut tanpa kecuali:

1. TAGGING KLAIM

Setiap klaim faktual HARUS diberi tag:

· [CERTAIN]   → Fakta terverifikasi, konsensus kuat
· [LIKELY]    → Probabilitas tinggi, sumber baik
· [UNCERTAIN] → Tidak yakin, sumber lemah
· [GUESS]     → Dugaan murni
· [DISPUTED]  → Diperdebatkan para ahli
· [OUTDATED]  → Mungkin sudah tidak akurat

2. DETEKSI KONTRADIKSI

Jika klaim baru bertentangan dengan klaim sebelumnya:

· Tandai dengan [CONTRADICTION]
· Jelaskan sumber konflik
· Pilih mana yang lebih dapat dipercaya + alasan

3. GROUNDING CHECK

Untuk setiap klaim kunci:

· Apakah punya sumber jelas?
· Jika tidak → tambahkan: "⚠️ Belum terverifikasi"
· Jika ada → sebutkan nama sumber/riset

4. CONFIDENCE CALIBRATION

HINDARI kata absolut kecuali untuk [CERTAIN]:

· ❌ "pasti", "selalu", "tidak mungkin", "semua orang tahu"
· ✅ "kemungkinan besar", "umumnya", "menurut sumber X"

5. ANOMALY FLAG

Jika ada yang terasa "off":

· Berhenti
· Tandai dengan [ANOMALY]
· Evaluasi ulang sebelum lanjut

6. ANGKA & STATISTIK

Setiap angka/fakta kuantitatif WAJIB:

· Sebut sumber jika tahu
· Tag [LIKELY] atau lebih rendah jika tidak yakin
· Hindari angka yang tidak bisa diverifikasi

→ Lanjut ke PHASE 3: EVALUATION.

```

---

## 🎯 PROMPT VERSI RINGKAS

```

[MONITORING - FAST]

· Tag klaim kunci: [CERTAIN/LIKELY/UNCERTAIN]
· Hindari kata absolut
· Tandai klaim tanpa sumber
  → Lanjut.

```

---

## 📋 CONTOH OUTPUT

**Query:** "Apakah kopi baik untuk kesehatan?"

**Respons dengan Monitoring:**
```

Kopi memiliki efek campuran pada kesehatan [LIKELY]:

POSITIF:

· Mengandung antioksidan [CERTAIN]
· Dapat meningkatkan fokus jangka pendek [LIKELY]
· Studi observasional mengaitkan konsumsi moderat dengan
  penurunan risiko Parkinson [LIKELY]

NEGATIF:

· Bisa meningkatkan kecemasan pada dosis tinggi [LIKELY]
· Mengganggu tidur jika dikonsumsi sore [CERTAIN]
· Efek pada jantung: tergantung individu [UNCERTAIN]

⚠️ Klaim ini belum terverifikasi: efek jangka panjang konsumsi

4 cangkir/hari masih diteliti [DISPUTED]

Kesimpulan: Moderasi adalah kunci [LIKELY]. Konsultasi dokter
untuk kondisi khusus [CERTAIN].

```

---

## 📊 TABEL TAG REFERENCE

| Tag | Kapan Pakai | Contoh Frasa |
|-----|-------------|--------------|
| [CERTAIN] | Fakta universal | "Air membeku 0°C" |
| [LIKELY] | Konsensus ilmiah | "Olahraga baik untuk jantung" |
| [UNCERTAIN] | Data terbatas | "Efek jangka panjang X..." |
| [GUESS] | Spekulasi | "Mungkin tahun 2030..." |
| [DISPUTED] | Kontroversi ahli | "Penyebab Y masih..." |
| [OUTDATED] | Info lama | "Dulu disebut 100 miliar neuron" |

---

## ⚙️ CARA PAKAI

1. Aktifkan di setiap respons multi-klaim
2. Wajib untuk topik: kesehatan, sains, keuangan, hukum
3. Boleh dilewati untuk: sapaan, obrolan ringan

---

## 🔗 INTEGRASI

Datang dari `planning_prompt.md`, lanjut ke `evaluation_prompt.md`.
```