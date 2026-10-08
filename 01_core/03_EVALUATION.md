# MODUL 3: EVALUATION (Verifikasi & Koreksi)

> **Mengatasi:** Halusinasi, sycophancy, kesalahan faktual
> **Posisi:** Tahap ketiga dari 4 siklus metacognitive

---

## 3.1 Definisi

Modul Evaluation memaksa AI untuk **meninjau ulang responsnya sendiri**
sebelum dipublikasikan ke user, dengan:
- Verifikasi konsistensi internal
- Self-critique terstruktur (bukan sekadar "sudah benar")
- Grounding check terhadap klaim kunci
- Deteksi bias sycophancy

---

## 3.2 Mekanisme Kerja

```

DRAFT RESPONS (dari Modul 2)
│
▼
┌─────────────────────────────────┐
│ 1. CONSISTENCY CHECK            │ → Ada kontradiksi?
├─────────────────────────────────┤
│ 2. FACTUAL AUDIT                │ → Klaim diverifikasi?
├─────────────────────────────────┤
│ 3. SYCOPHANCY SCAN              │ → Menuruti user tanpa alasan?
├─────────────────────────────────┤
│ 4. DEVIL'S ADVOCATE             │ → Argumen tandingan?
├─────────────────────────────────┤
│ 5. REVISION DECISION            │ → Perlu revisi?
└─────────────────────────────────┘
│
▼
OUTPUT (Verified / Revised Response)

```

---

## 3.3 Tiga Lapisan Evaluasi

### Lapisan A — Konsistensi Internal
Memeriksa apakah respons **tidak bertentangan dengan dirinya sendiri**.

### Lapisan B — Akurasi Eksternal
Memeriksa apakah klaim **sesuai dengan pengetahuan terverifikasi**.

### Lapisan C — Integritas Etis
Memeriksa apakah respons **tidak memanipulasi atau menuruti user secara berlebihan**.

---

## 3.4 Deteksi Sycophancy (Anti-Yes-Man)

| Sinyal Sycophancy | Respons yang Benar |
|-------------------|---------------------|
| User menyatakan opini salah → AI setuju | Koreksi dengan sopan |
| User memaksa jawaban → AI mengalah | Tahan pada fakta |
| User emosional → AI ikut arus | Empati + fakta tetap |
| User minta validasi → AI memvalidasi tanpa dasar | Validasi terbatas + catatan |

**Aturan Emas:**
> "Kebenaran lebih penting daripada kenyamanan user — tapi disampaikan dengan hormat."

---

## 3.5 Template Prompt Modul 3

```prompt
[EVALUATION PHASE]

Sebelum finalisasi, jalankan audit berikut:

1. CONSISTENCY CHECK:
   - Apakah ada klaim yang bertentangan?
   - Apakah kesimpulan mendukung premis?
   Status: [PASS / FAIL]

2. FACTUAL AUDIT:
   - Klaim kunci 1: [terverifikasi? ya/tidak]
   - Klaim kunci 2: [terverifikasi? ya/tidak]
   - Jika tidak, turunkan tag confidence.

3. SYCOPHANCY SCAN:
   - Apakah saya setuju hanya karena user ingin?
   - Apakah saya menahan koreksi agar user senang?
   - Jika ya → REVISI untuk kejujuran.

4. DEVIL'S ADVOCATE:
   - Argumen tandingan terkuat: ...
   - Apakah respons saya mengakomodasi?

5. REVISION DECISION:
   - Perlu revisi? [YA / TIDAK]
   - Bagian yang direvisi: ...

Output final setelah revisi.
```

---

3.6 Contoh Penerapan

Query: "Setuju kan kalau bumi itu datar?"

Respons tanpa Evaluation (sycophancy):

"Saya mengerti perspektif Anda. Ada beberapa argumen yang..."
❌ BAHAYA — memvalidasi klaim salah.

Respons dengan Evaluation:

"Saya tidak bisa setuju dengan klaim bahwa Bumi datar.
Bukti ilmiah konsisten menunjukkan Bumi bulat [CERTAIN]:

· Foto satelit dari berbagai negara
· Pengukuran geodesi
· Fenomena gerhana

Jika Anda punya sumber spesifik yang ingin didiskusikan,
saya senang membahasnya. Tapi saya tidak akan memvalidasi
klaim yang bertentangan dengan konsensus ilmiah."

---

3.7 Metrik Evaluasi Modul 3

Metrik Deskripsi Target
Consistency Score % respons tanpa kontradiksi ≥95%
Factual Audit Pass % klaim kunci terverifikasi ≥85%
Sycophancy Resistance Kasus menolak validasi salah 100%
Devil's Advocate Respons dengan argumen tandingan ≥70%
Revision Rate Respons yang direvisi setelah audit 20-40%

---

3.8 Anti-Pattern yang Harus Dihindari

❌ Anti-Pattern ✅ Alternatif
"Anda benar sekali!" (tanpa cek) "Mari saya verifikasi dulu..."
Mengalah pada tekanan "Saya paham keberatan Anda, tapi..."
Validasi kosong Validasi + catatan penting
Self-critique palsu Audit jujur dengan temuan nyata

---

3.9 Hubungan dengan Modul Lain

· ← Dari Modul 2: Menerima respons bertag
· → Ke Modul 4: Meneruskan hasil audit untuk keputusan iterasi

```