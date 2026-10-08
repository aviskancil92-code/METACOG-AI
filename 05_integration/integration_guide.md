# PANDUAN INTEGRASI METACOG-AI

> Cara mengintegrasikan skill METACOG-AI ke berbagai platform AI

---

## 🎯 1. STRATEGI INTEGRASI

METACOG-AI dapat diintegrasikan melalui **4 jalur utama**:

```

┌────────────────────────────────────────────────┐
│              METACOG-AI                        │
├────────────────────────────────────────────────┤
│                                                │
│   A. System Prompt    → Paling mudah          │
│   B. API Wrapper      → Untuk production      │
│   C. Fine-Tuning      → Untuk model kustom    │
│   D. Middleware       → Untuk pipeline        │
│                                                │
└────────────────────────────────────────────────┘

```

---

## 🅰️ 2. JALUR A — SYSTEM PROMPT (MUDAH)

### Cocok untuk:
- ChatGPT Custom GPT
- Claude Projects
- Gemini Gems
- Chatbot internal sederhana

### Langkah-langkah:

**Step 1:** Copy `master_prompt.md` → Compact Version

**Step 2:** Paste ke system prompt / custom instructions

**Step 3:** Uji dengan 3-5 test case dasar

**Step 4:** Iterasi berdasarkan hasil

### Contoh Konfigurasi:

```

[Custom Instructions - ChatGPT]

Anda adalah asisten dengan skill METACOG-AI:

1. PLANNING: Klasifikasi → Dekomposisi → Asumsi → Strategi
2. MONITORING: Tag klaim [CERTAIN/LIKELY/UNCERTAIN] + cek kontradiksi
3. EVALUATION: Audit → Anti-sycophancy → Devil's advocate
4. ADAPTIVE: Estimasi mode (FAST/STD/DEEP) → Loop jika perlu

Aturan Emas:

· Jujur > nyaman
· Akui ketidakpastian
· Koreksi dengan hormat tapi tegas
· Escalate untuk: kesehatan, finansial besar, hukum, emosi kuat

```

---

## 🅱️ 3. JALUR B — API WRAPPER

### Cocok untuk:
- Aplikasi kustom
- Integrasi ke produk
- Kontrol penuh atas prompt

### Arsitektur:

```

User Query
│
▼
┌─────────────────────┐
│  WRAPPER (Python)   │
│  - Estimasi mode    │
│  - Inject prompt    │
│  - Parse response   │
└──────────┬──────────┘
│
▼
┌─────────────────────┐
│  LLM API (OpenAI,   │
│  Anthropic, etc)    │
└──────────┬──────────┘
│
▼
┌─────────────────────┐
│  POST-PROCESS       │
│  - Parse tags       │
│  - Log metrics      │
│  - Loop jika perlu  │
└──────────┬──────────┘
│
▼
Final Response

```

### Pseudocode Python:

```python
import openai
from pathlib import Path

class MetacogAI:
    def __init__(self, api_key, model="gpt-4"):
        self.client = openai.Client(api_key=api_key)
        self.model = model
        self.master_prompt = Path("METACOG-AI/02_prompts/master_prompt.md").read_text()
    
    def estimate_mode(self, query):
        """Estimasi FAST/STANDARD/DEEP"""
        scores = self._score_factors(query)
        total = scores['kompleksitas']*3 + scores['kontroversi']*2.5 \
              + scores['dampak']*2.5 + scores['spesifik']*2
        
        if total <= 30: return "FAST"
        elif total <= 70: return "STANDARD"
        else: return "DEEP"
    
    def process(self, query, mode=None):
        mode = mode or self.estimate_mode(query)
        prompt = self._build_prompt(query, mode)
        
        response = self.client.chat.completions.create(
            model=self.model,
            messages=[
                {"role": "system", "content": self.master_prompt},
                {"role": "user", "content": prompt}
            ]
        )
        
        if mode == "DEEP":
            response = self._loop_iterate(response, query)
        
        return self._parse_output(response)
    
    def _build_prompt(self, query, mode):
        return f"[MODE: {mode}]\n\n{query}"
    
    def _loop_iterate(self, response, query, max_iter=3):
        # Implementasi loop evaluasi-revisi
        for i in range(max_iter):
            score = self._quality_score(response)
            if score >= 85: break
            response = self._revise(response, score)
        return response
    
    def _parse_output(self, response):
        # Ekstrak tag [CERTAIN], [LIKELY], dll
        return response
```

---

🅲 4. JALUR C — FINE-TUNING

Cocok untuk:

· Model kustom (Llama, Mistral, etc)
· Perusahaan dengan kebutuhan spesifik
· Performa tinggi tanpa prompt panjang

Format Dataset (JSONL):

```jsonl
{"messages": [
  {"role": "system", "content": "Kamu adalah AI dengan skill METACOG-AI..."},
  {"role": "user", "content": "Apakah bumi datar?"},
  {"role": "assistant", "content": "Tidak. Bumi berbentuk bulat oblate [CERTAIN].\n\nBukti:\n- Foto satelit [CERTAIN]\n- Pengukuran geodesi [CERTAIN]\n- Fenomena gerhana [CERTAIN]\n\nKlaim 'bumi datar' adalah miskonsepsi modern [DISPUTED oleh komunitas flat earth, tapi konsensus ilmiah jelas]."}
]}
```

Sumber Data Training:

1. 03_examples/*.md → convert ke JSONL
2. Benchmark test cases
3. Skenario dari production logs

Platform Fine-Tuning:

Platform Cost Cocok Untuk
OpenAI Fine-tuning $$$ Produksi GPT
Anthropic Belum tersedia publik -
Together AI $$ Open source models
Local (LoRA) $ Kontrol penuh

---

🅳 5. JALUR D — MIDDLEWARE

Cocok untuk:

· Sistem multi-agent
· Microservice architecture
· Enterprise

Arsitektur Microservice:

```
┌─────────────┐
│ User Query  │
└──────┬──────┘
       │
       ▼
┌──────────────────────┐
│ Mode Router          │  → FAST/STD/DEEP
└──────┬───────────────┘
       │
   ┌───┴───┬─────────┐
   ▼       ▼         ▼
┌──────┐ ┌──────┐ ┌──────┐
│Plan  │ │Monit │ │Eval  │
│Agent │ │Agent │ │Agent │
└──┬───┘ └──┬───┘ └──┬───┘
   │        │        │
   └────────┼────────┘
            ▼
    ┌──────────────────┐
    │ Aggregator       │
    └──────┬───────────┘
           │
           ▼
    ┌──────────────┐
    │ Final Output │
    └──────────────┘
```

---

📊 6. PERBANDINGAN JALUR

Jalur Setup Cost Control Kualitas Cocok Untuk
A. System Prompt 5 menit Rendah Rendah Baik Personal
B. API Wrapper 1-2 hari Sedang Tinggi Sangat baik Startup
C. Fine-Tuning 1-2 minggu Tinggi Tinggi Terbaik Enterprise
D. Middleware 2-4 minggu Tinggi Sangat tinggi Terbaik Multi-agent

---

🔧 7. CHECKLIST INTEGRASI

Pre-Integration

☐ Baca 00_OVERVIEW.md
☐ Pahami 4 modul di 01_core/
☐ Test prompt di 02_prompts/
☐ Review contoh di 03_examples/

Integration

☐ Pilih jalur (A/B/C/D)
☐ Setup environment
☐ Implementasi sesuai panduan
☐ Setup logging

Post-Integration

☐ Jalankan benchmark (04_metrics/benchmark_template.md)
☐ Kumpulkan feedback user
☐ Monitor metrik
☐ Iterasi perbaikan

---

🎯 8. USE CASE SPESIFIK

Use Case A — Customer Service Bot

```
Integrasi: API Wrapper
Prioritas: Evaluation (anti-sycophancy)
Escalation: Selalu untuk komplain produk
```

Use Case B — Edukasi / Tutoring

```
Integrasi: System Prompt
Prioritas: Planning (dekomposisi)
Mode default: STANDARD
```

Use Case C — Asisten Medis

```
Integrasi: API Wrapper + Middleware
Prioritas: Evaluation + Adaptive Control
Escalation: WAJIB untuk topik apapun terkait diagnosis
Disclaimer: Selalu rekomendasi dokter
```

Use Case D — Konten Kreatif

```
Integrasi: System Prompt
Prioritas: Planning + Monitoring
Mode: FAST lebih sering
```

---

📌 9. PITFALLS & SOLUSI

Pitfall Solusi
Prompt terlalu panjang → token mahal Gunakan Compact Version
AI lambat karena loop Batasi iterasi ≤3, cache hasil
Over-engineering (semua DEEP) Tune threshold mode
AI tetap sycophant Perkuat fase Evaluation
Tag membingungkan user Sembunyikan tag di output final

---

🔗 10. FILE TERKAIT

· deployment.md — panduan deploy produksi
· config.yaml — konfigurasi sistem
· ../02_prompts/master_prompt.md — prompt utama
· ../04_metrics/evaluation_metrics.md — metrik

```