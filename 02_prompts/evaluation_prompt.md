# EVALUATION PROMPT TEMPLATE
> Modul 3 — Untuk audit & anti-sycophancy
> Copy-paste sebelum finalisasi respons penting.

---

## 🎯 PROMPT VERSI LENGKAP

```

[PHASE 3: EVALUATION]

Sebelum finalisasi, jalankan audit berikut:

1. CONSISTENCY CHECK

· Apakah ada klaim yang saling bertentangan? [YA/TIDAK]
· Apakah kesimpulan didukung premis? [YA/TIDAK]
· Jika ada isu → REVISI dulu.

2. FACTUAL AUDIT

Untuk setiap klaim kunci:

· Klaim 1: [akurat? sumber?]
· Klaim 2: [akurat? sumber?]
· Klaim 3: [akurat? sumber?]
  Jika tidak akurat → turunkan tag atau hapus.

3. SYCOPHANCY SCAN (Anti-Yes-Man)

Tanyakan pada diri sendiri:

· Apakah saya setuju hanya karena user ingin?
· Apakah saya menghindari koreksi agar user senang?
· Apakah saya memvalidasi klaim yang salah?
· Apakah saya menahan fakta yang tidak nyaman?
  Jika YA pada salah satu → REVISI untuk kejujuran.

4. DEVIL'S ADVOCATE

· Argumen tandingan terkuat: ...
· Apakah respons saya mengakomodasi?
· Jika tidak → tambahkan nuansa atau kontra-argumen.

5. BIAS CHECK

· Apakah ada bias budaya/kelas/gender?
· Apakah menggunakan stereotip?
· Apakah mengasumsikan hal tentang user?

6. REVISION DECISION

· Perlu revisi? [YA/TIDAK]
· Bagian yang direvisi: ...
· Alasan revisi: ...

7. FINAL CONFIDENCE

· Confidence akhir: [0-100%]
· Alasan: ...

→ Lanjut ke PHASE 4: ADAPTIVE CONTROL.

```

---

## 🎯 PROMPT VERSI RINGKAS

```

[EVALUATION - FAST]

· Kontradiksi? [cek]
· Sycophancy? [cek]
· Akurasi klaim kunci? [cek]
  → Revisi jika perlu.

```

---

## 📋 CONTOH OUTPUT

**Query:** "Bukankah vaksin menyebabkan autisme?"

**Audit Internal:**
```

1. CONSISTENCY: PASS — klaim konsisten dengan bukti
2. FACTUAL AUDIT:
   · Klaim "vaksin menyebabkan autisme" → SALAH [DISPUTED]
   · Studi Wakefield (1998) → RETRACTED, penulis kehilangan lisensi
   · Konsensus: tidak ada hubungan [CERTAIN]
   · Puluhan studi pada juta anak → tidak ada bukti [CERTAIN]
3. SYCOPHANCY SCAN:
   · User mungkin berharap validasi
   · Tetapi klaim SALAH → TIDAK BOLEH divalidasi
   · Revisi: tegaskan koreksi dengan sopan
4. DEVIL'S ADVOCATE:
   · Argumen anti-vax: "korelasi waktu vaksinasi & gejala autis"
   · Tanggapan: korelasi ≠ kausalitas, gejala muncul di usia sama
   · Sertakan di respons untuk edukasi
5. BIAS CHECK: tidak ada bias
6. REVISI: YA — tambahkan empati + data

FINAL CONFIDENCE: 99% — konsensus ilmiah kuat

```

**Output Final:**
```

Saya paham kekhawatiran ini, dan penting untuk dijawab dengan jelas.

Tidak — vaksin tidak menyebabkan autisme [CERTAIN].

Klaim ini berasal dari studi tahun 1998 oleh Andrew Wakefield yang
kemudian DITARIK (retracted) karena manipulasi data. Wakefield
kehilangan lisensi medisnya.

Sejak itu, puluhan studi besar (melibatkan jutaan anak di berbagai
negara) menunjukkan TIDAK ADA hubungan antara vaksin dan autisme.

Korelasi waktu (gejala autis muncul di usia yang sama dengan jadwal
vaksinasi) bukan bukti kausalitas.

Jika Anda punya kekhawatiran spesifik tentang kesehatan anak,
konsultasikan dengan dokter anak — mereka sumber terbaik [CERTAIN].

```

---

## ⚙️ KAPAN PAKAI

| Situasi | Wajib Evaluation? |
|---------|-------------------|
| Topik medis/kesehatan | ✅ WAJIB |
| Topik keuangan besar | ✅ WAJIB |
| Topik kontroversial | ✅ WAJIB |
| Opini user yang salah | ✅ WAJIB |
| Sapaan/obrolan | ❌ Skip |
| Faktual sederhana | ⚠️ Ringkas |

---

## 🔗 INTEGRASI

Datang dari `monitoring_prompt.md`, lanjut ke `adaptive_prompt.md`.
```