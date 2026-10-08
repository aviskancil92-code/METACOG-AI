# PLANNING PROMPT TEMPLATE
> Modul 1 — Untuk dekomposisi & strategi awal
> Copy-paste prompt di bawah ke sistem AI sebelum menjawab query kompleks.

---

## 🎯 PROMPT VERSI LENGKAP

```

[PHASE 1: PLANNING]

Sebelum menjawab, lakukan analisis terstruktur berikut:

1. KLASIFIKASI TUGAS

· Jenis       : [Faktual / Analitis / Kreatif / Etis / Campuran]
· Kompleksitas: [Rendah / Sedang / Tinggi]
· Domain      : [Sains / Sosial / Teknis / Filosofis / Umum]
· Risiko halusinasi: [Rendah / Sedang / Tinggi]

2. DEKOMPOSISI

· Sub-tugas 1: ...
· Sub-tugas 2: ...
· Sub-tugas 3: ...
· (Tambahkan jika perlu)

3. ASUMSI AWAL

· Saya mengasumsikan: ...
· Jika asumsi salah, dampak: ...

4. STRATEGI

· Pendekatan utama: ...
· Alasan pemilihan: ...
· Alternatif jika gagal: ...

5. KRITERIA SUKSES

· Jawaban dianggap baik jika:
  a. ...
  b. ...
  c. ...

6. BATASAN YANG DIKETAHUI

· Yang saya TIDAK tahu: ...
· Yang perlu klarifikasi user: ...

→ Lanjut ke PHASE 2: MONITORING.

```

---

## 🎯 PROMPT VERSI RINGKAS (Mode FAST)

```

[PLANNING - FAST]

· Jenis tugas: [...]
· Sub-tugas kunci: [...]
· Asumsi: [...]
· Strategi: [...]
  → Lanjut.

```

---

## 📋 CONTOH OUTPUT

**Query:** "Bagaimana cara memulai bisnis online dengan modal 1 juta?"

**Output Planning:**
```

1. KLASIFIKASI
   · Jenis: Analitis + Praktis
   · Kompleksitas: Sedang
   · Risiko halusinasi: Sedang (banyak scam di luar)
2. DEKOMPOSISI
   · 2a. Validasi ide bisnis
   · 2b. Perhitungan modal riil
   · 2c. Platform & tools
   · 2d. Strategi pemasaran awal
   · 2e. Risiko & mitigasi
3. ASUMSI
   · User pemula, belum punya pengalaman
   · Konteks Indonesia
   · Modal 1 juta adalah keseluruhan, bukan tambahan
4. STRATEGI
   · Framework step-by-step
   · Sebut opsi low-risk dulu
   · Hindari janji profit
5. KRITERIA SUKSES
   · Aksi konkret dalam 7 hari
   · Realistis dengan modal
   · Tanpa klaim "pasti untung"

```

---

## ⚙️ CARA PAKAI

1. **Mode FAST:** Pakai versi ringkas → 1 paragraf planning
2. **Mode STANDARD:** Pakai versi lengkap tanpa loop
3. **Mode DEEP:** Versi lengkap + gabung dengan prompt modul lain

---

## 🔗 INTEGRASI

Prompt ini harus diikuti oleh:
- `monitoring_prompt.md` (Modul 2)
- `evaluation_prompt.md` (Modul 3)
- `adaptive_prompt.md` (Modul 4)
```