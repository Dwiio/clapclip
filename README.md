# 🎬 ClapClip

### AI-Powered Video Clipping & Content Repurposing Platform

**ClapClip** adalah platform berbasis AI yang membantu creator mengubah video YouTube berdurasi panjang menjadi **short-form content yang siap dipublikasikan**.

Cukup masukkan link YouTube, dan ClapClip menganalisis transcript, hook, konteks, emosi, serta potensi engagement untuk menemukan momen-momen terbaik yang dapat diubah menjadi clips untuk **TikTok, Instagram Reels, dan YouTube Shorts**.

> **Turn long-form videos into short-form content with AI.**

---

## 🚀 Live Demo

### 🌐 [clapclip.online](https://clapclip.online)

Coba langsung platform ClapClip melalui website:

**https://clapclip.online**

> Demo online dapat berubah atau mengalami maintenance sewaktu-waktu.

---

## ✨ Features

### 🧠 AI Highlight Detection

ClapClip menganalisis transcript video untuk menemukan momen yang paling menarik berdasarkan:

* Strong hooks
* Emotional moments
* Surprising statements
* Storytelling moments
* Punchlines
* Contrarian opinions
* Educational insights
* Shareability

AI kemudian memberikan rekomendasi clip berdasarkan konteks konten, bukan sekadar memotong video berdasarkan durasi.

---

### 🔥 AI Viral Potential Score

Setiap clip mendapatkan skor **0–100** berdasarkan beberapa faktor:

| Faktor          | Deskripsi                 |
| --------------- | ------------------------- |
| 🎯 Hook         | Kekuatan pembuka clip     |
| 💬 Engagement   | Potensi menarik perhatian |
| 🧠 Clarity      | Kejelasan pesan           |
| ❤️ Emotion      | Kekuatan emosional        |
| 🚀 Shareability | Potensi untuk dibagikan   |

ClapClip juga menyediakan **confidence score** untuk setiap rekomendasi.

> Viral Score merupakan estimasi berdasarkan karakteristik konten dan bukan jaminan bahwa sebuah video akan menjadi viral.

---

### ✂️ Smart Clip Generation

Pengguna dapat menentukan jumlah clip dan durasi yang diinginkan.

Pilihan durasi meliputi:

* 15 seconds
* 30 seconds
* 45 seconds
* 60 seconds
* Auto

AI berusaha memilih titik awal dan akhir berdasarkan **natural sentence boundaries** sehingga clip tidak terpotong secara sembarangan.

---

### 📱 Short-Form Aspect Ratios

ClapClip mendukung format:

* **9:16** — TikTok / Instagram Reels / YouTube Shorts
* **1:1** — Square
* **16:9** — Landscape

---

### 📝 Dynamic Captions

ClapClip menyediakan sistem caption dengan beberapa gaya:

* Clean
* Bold
* Highlight
* Viral
* Minimal

Caption disusun berdasarkan transcript dan dapat disesuaikan melalui editor.

---

### 📦 AI Content Packs

Setiap clip dapat memiliki **AI-generated Content Pack** yang berisi:

* SEO / scroll-stopping title
* Hook
* Social media caption
* Hashtags
* Thumbnail text
* CTA

Content pack juga dapat diregenerate untuk mendapatkan variasi baru.

---

### 🎨 Brand Kit

Creator dapat menyimpan identitas brand dan menggunakannya pada konten.

Brand Kit mendukung:

* Brand name
* Username
* Logo URL
* Primary color
* Secondary color
* Logo position
* Watermark opacity
* Caption style
* Font

Font yang tersedia pada project:

* Outfit
* Plus Jakarta Sans
* JetBrains Mono

---

### 🎞️ Clip Editor

Setiap clip memiliki editor khusus untuk melakukan penyesuaian seperti:

* Caption style
* Aspect ratio
* Caption segments
* Content pack
* Clip metadata

Perubahan editor menggunakan sistem autosave.

---

### 📚 Clip Library

Semua clip yang telah dibuat dapat disimpan dalam library.

Pengguna dapat:

* Search clips
* Melihat kategori
* Melihat viral score
* Membuka editor
* Membuka content pack
* Melakukan export workflow

---

### 📊 Project Management

Setiap video yang dianalisis menjadi sebuah project.

Project menyimpan:

* YouTube URL
* Video ID
* Video title
* Author
* Thumbnail
* Video duration
* Processing status
* Number of generated clips
* Creation date
* Update date

---

### 📈 Usage Tracking

ClapClip memiliki sistem penggunaan bulanan berdasarkan plan.

Plan yang tersedia di aplikasi:

| Plan       | Processing Minutes / Month |
| ---------- | -------------------------: |
| Free       |                         30 |
| Creator    |                        180 |
| Pro Studio |                        600 |
| Agency     |                      2,000 |

Usage tracking mencatat:

* Processing minutes
* Clips generated
* Exports
* Projects

---

## 🔄 How It Works

```text
YouTube URL
     │
     ▼
┌──────────────────────┐
│  Video Metadata      │
│  & Transcript        │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│ AI Highlight         │
│ Detection             │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│ Viral Potential      │
│ Scoring              │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│ Clip Recommendations │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│ Captions + Reframe   │
│ + Content Pack       │
└──────────┬───────────┘
           │
           ▼
      Ready to Publish
```

---

## 🧩 Technology Stack

### Frontend

* React 19
* React Router
* Tailwind CSS
* CRACO
* Framer Motion
* Radix UI
* Lucide React
* Axios
* React Hook Form
* Recharts
* Sonner

### Backend

* Python
* FastAPI
* Pydantic
* MongoDB
* HTTPX
* Pytest

### AI

ClapClip menggunakan arsitektur AI yang modular sehingga provider AI dapat diganti tanpa harus mengubah seluruh application layer.

AI service pada project saat ini menggunakan:

* Anthropic
* Claude Sonnet


AI digunakan untuk:

* Highlight detection
* Hook detection
* Content analysis
* Viral potential scoring
* Social media content generation
* Content pack regeneration

### Video & Transcript

Project menggunakan:

* YouTube oEmbed untuk metadata video
* YouTube Transcript API untuk transcript
* Modular video service abstraction

---

## 🏗️ Project Structure

```text
clapclip/
│
├── backend/
│   ├── auth.py
│   ├── ai_service.py
│   ├── database.py
│   ├── models.py
│   ├── routes.py
│   ├── server.py
│   ├── video_service.py
│   ├── requirements.txt
│   └── tests/
│
├── frontend/
│   ├── public/
│   ├── plugins/
│   ├── src/
│   │   ├── components/
│   │   ├── context/
│   │   ├── constants/
│   │   ├── hooks/
│   │   ├── lib/
│   │   └── pages/
│   ├── package.json
│   ├── tailwind.config.js
│   └── craco.config.js
│
├── tests/
├── test_reports/
├── memory/
├── .emergent/
├── design_guidelines.json
├── .gitignore
└── README.md
```

---

## 🖥️ Application Pages

ClapClip memiliki beberapa halaman utama:

### Public

* Landing Page
* Pricing
* Login
* Register

### Application

* Dashboard
* Create Clips
* Processing
* Results
* Clip Editor
* Projects
* All Clips
* Content Packs
* Brand Kit
* Settings

---

## 🔐 Authentication

ClapClip memiliki sistem authentication dengan:

* Registration
* Login
* Protected routes
* User session
* User plan
* Usage tracking

Halaman aplikasi dilindungi menggunakan authentication layer sehingga user yang belum login akan diarahkan ke halaman login.

---

## 🎯 Target Users

ClapClip dirancang untuk:

### 🎙️ Podcasters

Mengubah episode panjang menjadi beberapa short clips untuk distribusi harian.

### ▶️ YouTubers

Mengubah long-form YouTube videos menjadi Shorts, Reels, dan TikTok.

### 🎓 Educators & Coaches

Mengubah materi panjang menjadi potongan edukatif yang mudah dikonsumsi.

### 🎮 Streamers

Menemukan momen menarik dari livestream dan konten gaming.

### 🏢 Agencies

Mengelola dan menghasilkan short-form content untuk banyak brand.

---

## 💡 Core Value

ClapClip dibangun dengan prinsip sederhana:

> **Don't spend hours searching for the best moments. Let AI find them for you.**

Daripada menonton video berdurasi 1–3 jam dan mencari momen menarik secara manual, creator dapat memasukkan URL video dan membiarkan sistem menganalisis transcript untuk menemukan kandidat clip terbaik.

---

## 🛠️ Local Development

Clone repository:

```bash
git clone <YOUR_REPOSITORY_URL>
cd clapclip
```

### Frontend

```bash
cd frontend
npm install
npm start
```

Frontend menggunakan React + CRACO.

### Backend

Masuk ke folder backend:

```bash
cd backend
```

Buat virtual environment:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

> Environment variables dan konfigurasi database/API harus disiapkan sebelum menjalankan seluruh fitur production.

---

## 🔑 Environment Variables

Jangan commit secret atau API key ke GitHub.

Gunakan environment variables untuk konfigurasi seperti:

```env
EMERGENT_LLM_KEY=
MONGO_URL=
DB_NAME=
JWT_SECRET=
```

Nama variable dapat berbeda sesuai konfigurasi deployment.

---

## 🧪 Testing

Backend menggunakan Pytest.

Contoh:

```bash
cd backend
pytest
```

Frontend menggunakan React test runner:

```bash
cd frontend
npm test
```

---

## 🚀 Deployment

ClapClip dirancang dengan frontend dan backend yang terpisah sehingga dapat di-deploy secara independen.

Contoh arsitektur production:

```text
                    clapclip.online
                         │
                         ▼
                 ┌───────────────┐
                 │   Frontend    │
                 │    React      │
                 └───────┬───────┘
                         │
                         │ API
                         ▼
                 ┌───────────────┐
                 │    Backend    │
                 │    FastAPI    │
                 └───────┬───────┘
                         │
              ┌──────────┴──────────┐
              ▼                     ▼
        ┌───────────┐        ┌────────────┐
        │ MongoDB   │        │ AI Service │
        └───────────┘        └────────────┘
```

---

## ⚠️ Current Project Notes

ClapClip saat ini merupakan project yang terus dikembangkan.

Beberapa service seperti video acquisition, AI provider, database, dan rendering dibuat dengan pendekatan modular sehingga provider dapat diganti atau dikembangkan lebih lanjut.

Untuk deployment production, pastikan:

* API keys telah dikonfigurasi
* Database production telah tersedia
* Authentication secret aman
* CORS dikonfigurasi dengan benar
* HTTPS aktif
* Video processing infrastructure siap digunakan
* Rendering provider production telah dikonfigurasi
* Environment variables tidak masuk ke Git

---

## 📌 Roadmap

### Phase 1 — Core Platform

* [x] Landing page
* [x] Authentication
* [x] YouTube URL analysis
* [x] Transcript processing
* [x] AI highlight detection
* [x] Viral potential scoring
* [x] Clip library
* [x] Content packs
* [x] Brand Kit
* [x] Usage tracking

### Phase 2 — Creator Workflow

* [x] Clip editor
* [x] Dynamic captions
* [x] Multiple aspect ratios
* [x] Content pack regeneration
* [x] Project management

### Phase 3 — Production Infrastructure

* [ ] Production-grade video downloader
* [ ] Production video rendering pipeline
* [ ] Background job queue
* [ ] Object storage
* [ ] CDN delivery
* [ ] Advanced speaker tracking
* [ ] Advanced AI reframing
* [ ] Multi-language transcription

### Phase 4 — SaaS

* [ ] Payment gateway
* [ ] Subscription management
* [ ] Invoice system
* [ ] Team workspaces
* [ ] Agency management
* [ ] Usage-based billing
* [ ] Analytics dashboard

---

## 📄 License

This project is proprietary unless otherwise specified by the repository owner.

The source code, design, branding, and product concept are intended for the ClapClip project.

---

## 🌐 Links

**Live Demo:**
https://clapclip.online

**Project:**
ClapClip

**Category:**
AI Video Clipping / Video Repurposing / Creator SaaS

---

## ❤️ Built for Creators

ClapClip is built to make short-form content production faster, smarter, and easier.

**One long video.
Multiple great moments.
Powered by AI.**

### ClapClip

**Turn long videos into content worth sharing.**
