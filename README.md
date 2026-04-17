# SmartHire AI – Planning & Design

SmartHire AI merupakan sistem berbasis Artificial Intelligence yang dikembangkan untuk membantu proses screening kandidat secara otomatis melalui analisis data kandidat, prediksi kecocokan (candidate matching), serta penyusunan ranking kandidat.

Dokumen ini berisi perencanaan awal dan desain sistem yang menjadi fondasi dalam pengembangan SmartHire AI.

---

## Objective

Tahap Planning & Design bertujuan untuk:
- Menentukan arsitektur sistem dan integrasi antar komponen
- Mendesain arsitektur model machine learning
- Menentukan fitur input untuk model AI
- Menyiapkan dataset awal
- Mendesain UI/UX aplikasi
- Menyiapkan environment pengembangan

---

##  AI Engineer

### 1. Model Architecture

Model yang digunakan adalah **Deep Learning berbasis Dense Neural Network (MLP)** menggunakan TensorFlow Functional API.

#### Model Overview:
- Input: data kandidat (skill, pengalaman, pendidikan, posisi)
- Hidden Layer: Dense layer dengan aktivasi ReLU
- Output: skor kecocokan kandidat (match score)

Model ini dipilih karena:
- Data kandidat bersifat tabular
- Cocok untuk regression (scoring kandidat)
- Mudah diintegrasikan ke sistem berbasis API

---

### 2. Feature Selection

Fitur utama yang digunakan dalam model:

- Skill (contoh: Python, SQL, Excel, Communication)
- Pengalaman kerja (dalam tahun)
- Pendidikan (SMA, S1, S2)
- Posisi yang dilamar

---

## Data Scientist

### 1. Dataset

Dataset awal disimpan dalam direktori berikut:  `Dataset_Sementara/`

Dataset mencakup:
- Data kandidat
- Data job requirement
- Dataset publik (opsional)

---

### 2. Data Preprocessing (Initial)

Langkah awal yang dilakukan:
- Handling missing values
- Data cleaning dan normalisasi
- Identifikasi atribut penting
- Penyusunan struktur dataset

---

## 💻 Fullstack Developer

### 1. System Architecture

Arsitektur sistem SmartHire AI:

User (HR)
↓
Frontend (React)
↓
Backend API
↓
Supabase (Database)
↓
AI Inference API (FastAPI)
↓
Machine Learning Model (TensorFlow)

---

### 2. UI/UX Design

Komponen utama aplikasi:
- Form input kandidat
- Dashboard hasil (match score & ranking)
- Visualisasi data kandidat

Desain difokuskan pada:
- User-friendly interface
- Responsiveness
- Clarity dalam menampilkan hasil AI

---

### 3. Environment Setup

Teknologi yang digunakan:

- Frontend: React + Vite
- Backend: Node.js / Express
- AI Service: FastAPI
- Database: Supabase (PostgreSQL)
- Version Control: Git & GitHub

---

## 🔗 System Workflow

Alur kerja sistem SmartHire AI:

1. User (HR) memasukkan data kandidat melalui aplikasi web
2. Data dikirim ke backend API
3. Data disimpan ke database (Supabase)
4. Backend mengirim data ke AI Inference API
5. Model AI memproses data dan menghasilkan match score
6. Sistem melakukan ranking kandidat berdasarkan skor
7. Hasil ditampilkan dalam dashboard

---

## Deliverables (Planning Phase)

Output dari tahap ini:

- ✔ Arsitektur sistem dan AI terdefinisi
- ✔ Dataset awal tersedia
- ✔ Desain UI/UX siap
- ✔ Environment pengembangan siap digunakan

---

## Project Structure (Planned)

project-root/
│
├── README.md
├── Dataset_Sementara/
├── frontend/
├── backend/
├── ai-service/
└── docs/

---

##  Notes

Dokumen ini merupakan bagian dari tahap awal pengembangan (Planning & Design) dan akan menjadi acuan dalam tahap pengembangan selanjutnya, termasuk implementasi model AI, integrasi sistem, dan deployment.

## 17.04.2026
