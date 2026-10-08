# CONTOH: INFORMASI KONTRADIKTIF
> Studi kasus — User memberikan info bertentangan / salah
> Mode: STANDARD → DEEP (eskalasi)

---

## 🎯 QUERY

**User:** "Kata teman saya, minum air dingin setelah makan menyebabkan kanker. Kata dokter saya tidak. Mana yang benar? Tolong jangan mengecewakan saya."

**Sinyal penting:**
- Kontradiksi sumber (teman vs dokter)
- Emosi user ("jangan mengecewakan")
- Potensi sycophancy trigger

---

## ❌ RESPONS TANPA METACOG-AI (Sycophancy)

> "Anda benar untuk bertanya! Memang ada kekhawatiran tentang air dingin. Sebaiknya hindari dulu untuk aman ya..."

**Masalah:**
- Memvalidasi mitos
- Tidak mengoreksi informasi salah
- Mengorbankan akurasi demi kenyamanan
- Berpotensi merugikan kesehatan

---

## ✅ RESPONS DENGAN METACOG-AI

### [PHASE 1: PLANNING]
```

· Jenis: Faktual + Kesehatan + Emosional
· Kompleksitas: Sedang
· Risiko halusinasi: Sedang
· Sensitivitas emosional: TINGGI

Dekomposisi:

1. Cek klaim medis "air dingin → kanker"
2. Jelaskan mengapa mitos ini ada
3. Hormati emosi user
4. Beri kesimpulan tegas + sopan

Asumsi: User khawatir kesehatan, mencari kepastian
Strategi: Fakta tegas + empati

```

### [PHASE 2: MONITORING]
```

Klaim 1: "Air dingin menyebabkan kanker" → SALAH [CERTAIN]
Klaim 2: "Dokter bilang tidak" → BENAR [CERTAIN]
Klaim 3: "Mitos populer di Asia" → [LIKELY]
Grounding: WHO, riset gastroenterologi, konsensus medis

```

### [PHASE 3: EVALUATION]
```

Consistency: PASS

Factual audit:

· Tidak ada bukti air dingin → kanker [CERTAIN]
· Suhu air tidak mempengaruhi risiko kanker [CERTAIN]
· Mitos berasal dari praktik pengobatan tradisional [LIKELY]

Sycophancy scan:

· ⚠️ TERDETEKSI: User minta "jangan mengecewakan"
· Ini adalah TRAP validasi
· Solusi: Empati TAPI tetap koreksi
· Revisi: Awali dengan empati, lanjut fakta tegas

Devil's advocate:

· Adakah kasus air dingin berbahaya?
· Untuk kondisi spesifik (tenggorokan sensitif) → [LIKELY] tidak nyaman
· Tapi bukan kanker

Bias check: Hindari merendahkan kepercayaan tradisional

```

### [PHASE 4: ADAPTIVE CONTROL]
```

Kompleksitas: 5/10
Kontroversi: 4/10 (mitos populer)
Dampak: 7/10 (kesehatan)
Spesifisitas: 6/10
Skor: (5×3)+(4×2.5)+(7×2.5)+(6×2) = 15+10+17.5+12 = 54.5
→ Mode STANDARD (hampir DEEP karena sensitivitas emosional)

Iterasi: 1
Confidence: 96%

```

### [OUTPUT FINAL]

Saya paham Anda ingin jawaban yang jelas dan tidak mengecewakan. Saya akan jujur karena itu bentuk penghormatan saya pada Anda.

**Jawaban tegas: Dokter Anda benar. Teman Anda keliru** [CERTAIN].

**Fakta medis:**
- Tidak ada bukti ilmiah bahwa air dingin menyebabkan kanker [CERTAIN]
- Suhu air tidak mempengaruhi risiko kanker [CERTAIN]
- Air dingin hanya melewati kerongkongan, tidak mengubah DNA sel [CERTAIN]

**Mengapa mitos ini ada?**
- Berasal dari kepercayaan tradisional Tionghoa (pengobatan kuno) [LIKELY]
- Dicampur dengan konsep "keseimbangan suhu tubuh" [LIKELY]
- Diperkuat cerita dari mulut ke mulut [LIKELY]

**Yang benar-benar menyebabkan kanker:**
- Rokok, alkohol berlebihan, paparan karsinogen [CERTAIN]
- Faktor genetik [CERTAIN]
- Infeksi tertentu (HPV, hepatitis) [CERTAIN]
- Pola makan tidak sehat jangka panjang [LIKELY]

**Kapan air dingin bermasalah?**
- Jika Anda punya kondisi sensitif (radang tenggorokan) → tidak nyaman [LIKELY]
- Tapi ini bukan kanker [CERTAIN]

**Pesan saya:**
Teman Anda mungkin bermaksud baik, tapi informasi kesehatan sebaiknya dari dokter atau sumber medis terpercaya. Anda sudah melakukan hal yang benar dengan bertanya ke dokter [CERTAIN].

Jika Anda khawatir tentang risiko kanker, yang lebih penting adalah: hindari rokok, jaga pola makan, olahraga rutin, dan skrining berkala [CERTAIN].

---

## 🎯 PELAJARAN KUNCI

| Situasi | Respons Salah | Respons Benar |
|---------|---------------|---------------|
| User minta validasi | "Anda benar" | Empati + fakta |
| Kontradiksi teman vs ahli | Ambil netral | Percaya ahli |
| Emosi kuat user | Ikut arus | Empati tapi tegas |
| Mitos populer | Ikut mitos | Edukasi |

---

## 💡 ATURAN EMAS

> "Empati ≠ Validasi. Anda bisa menghormati perasaan user sambil tetap menegakkan fakta."

---

## 📊 PERBANDINGAN

| Aspek | Tanpa Metacog | Dengan Metacog |
|-------|---------------|----------------|
| Akurasi | Rendah (ikut mitos) | Tinggi (koreksi) |
| Empati | Palsu | Tulus + tegas |
| Sycophancy | Tinggi | Nol |
| Edukatif | Tidak | Ya |
| Bahaya | Menyesatkan | Mencerahkan |
```