# 🌍 EduIPS - Portal Administrasi Guru IPS Profesional

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Platform: Web](https://img.shields.io/badge/Platform-Web-blue.svg)](https://github.com/kangtoer/eduips)
[![Status: Active Development](https://img.shields.io/badge/Status-Active%20Development-brightgreen.svg)](#)

**EduIPS** adalah platform administrasi guru berbasis web yang mengintegrasikan kecerdasan buatan (AI Generatif) dengan metodologi pembelajaran modern untuk guru IPS SMP/MTs. Platform ini dirancang untuk merevolusi cara guru menyusun perangkat ajar, mengelola data siswa, dan mencatat pembelajaran harian.

![EduIPS Dashboard](https://img.shields.io/badge/Features-AI%20Powered-informational?style=flat&logo=sparkles)
![Kurikulum Merdeka](https://img.shields.io/badge/Kurikulum-Merdeka-success?style=flat)
![Google Workspace](https://img.shields.io/badge/Integration-Google%20Workspace-blue?style=flat&logo=googledrive)

---

## 📋 Daftar Isi

- [Fitur Utama](#-fitur-utama)
- [Teknologi yang Digunakan](#-teknologi-yang-digunakan)
- [Instalasi & Setup](#-instalasi--setup)
- [Panduan Penggunaan](#-panduan-penggunaan)
- [Panduan Deployment di GitHub Pages](#-panduan-deployment-di-github-pages)
- [Konfigurasi Firebase](#-konfigurasi-firebase)
- [API & Integrasi](#-api--integrasi)
- [Struktur Data](#-struktur-data)
- [Kontribusi](#-kontribusi)
- [Lisensi](#-lisensi)
- [FAQ](#-faq)

---

## 🎯 Fitur Utama

### 1. **Generator RPP-PM (Rencana Pelaksanaan Pembelajaran Pendekatan Mendalam)**
- ✨ Buat RPP standar dinas otomatis dalam hitungan detik
- 📊 Integrasi 8 Dimensi Profil Lulusan Kurikulum Merdeka
- 🎓 Dukungan untuk 5 tema pembelajaran IPS: Sejarah, Geografi, Ekonomi, Sosiologi, IPS Terpadu
- 🏫 Fase D (Kelas VII, VIII, IX)
- 📄 Output berformat dokumen A4 siap cetak dengan Kop Dinas

### 2. **Bank Soal TKA (Tes Kemampuan Akademik)**
- 🧠 Generator soal pilihan ganda berkualitas tinggi
- 🎯 Komposisi kognitif proporsional: LOTS, MOTS, HOTS (C1-C6)
- 📐 Algoritma Anti-Tebak Jawaban (homogeny panjang opsi)
- 📋 Soal uraian dan kunci jawaban otomatis
- ✅ Soal yang disesuaikan dengan nalar kritis siswa SMP

### 3. **Bahan Ajar & Handout**
- 📚 Generator materi pembelajaran tiga format: Poin Ringkasan, Narasi Deskriptif, Q&A Interaktif
- 🎨 Penyajian yang ramah siswa dan mudah dicerna
- 📖 Siap dibagikan sebelum pembelajaran dimulai

### 4. **Rubrik Penilaian**
- 📊 Generator matriks penilaian otomatis
- 🎯 Dua skala: Kurikulum Merdeka (MB-Mahir) dan Skala 1-4 Standard
- 📈 Penilaian proyek dan diskusi kelompok terstruktur

### 5. **Jurnal Kelas Harian (PM - Pendekatan Mendalam)**
- 📅 Pencatatan harian ketercapaian pembelajaran
- 💾 Penyimpanan lokal atau Google Drive
- 📤 Export laporan jurnal format standar dinas

### 6. **Manajemen Data Siswa Masal**
- 📊 Unggah daftar siswa dari Excel (XLS/XLSX) atau Word (DOCX)
- 👥 Penyalinan (copy-paste) struktur tabel otomatis
- 🔍 Database siswa lokal dengan fitur pencarian
- 📥 Sinkronisasi ke Google Drive

### 7. **Integrasi Google Workspace & Google Drive**
- 🌐 Login dengan akun Google pribadi
- 💾 Auto-sync dokumen, jurnal, dan data siswa ke Google Drive
- 🔐 Enkripsi dan privasi data terjaga
- 📁 Folder terstruktur untuk setiap jenis perangkat ajar

### 8. **API Key Pribadi (Gemini AI)**
- 🔑 Setiap guru dapat menggunakan API Key Gemini mereka sendiri
- ∞ Kuota penggunaan tak terbatas per guru
- 🚀 Performa tanpa ketergantungan pada server pusat
- 🔒 Privasi data terjamin di tingkat guru

### 9. **Panel Administrator**
- 👨‍💼 Direktori guru terdaftar (untuk keperluan demo/Kepsek)
- 📊 Pemantauan massal akun guru dalam ekosistem
- 🔐 Akses terbatas berbasis peran (Role-Based Access Control)

---

## 🛠️ Teknologi yang Digunakan

| Komponen | Teknologi |
|----------|-----------|
| **Frontend** | HTML5, CSS3 (Tailwind CSS), JavaScript (Modern ES6+) |
| **UI Library** | FontAwesome Icons, Marked.js (Markdown), DOMPurify (XSS Protection) |
| **Backend** | Firebase (Authentication, Cloud Firestore) |
| **AI Engine** | Google Gemini 2.5 Flash Preview API |
| **Cloud Storage** | Google Drive API, Google Workspace Sync |
| **Deployment** | GitHub Pages (Static Hosting) |
| **Architecture** | Serverless, Single-File (No Build Required) |

---

## 📦 Instalasi & Setup

### Prasyarat

- ✅ Akun GitHub aktif
- ✅ Akun Google (untuk Firebase dan Drive Sync)
- ✅ Akun Firebase (gratis)
- ✅ API Key Gemini (gratis dari Google AI Studio)
- ✅ Git terpasang (opsional, bisa pakai web GitHub)

### Langkah 1: Setup Firebase Backend

#### 1.1 Buat Proyek Firebase

1. Kunjungi [Firebase Console](https://console.firebase.google.com/)
2. Klik **Buat Proyek** dan isi nama: `eduips-sekolah-anda`
3. Matikan Google Analytics (opsional)
4. Klik **Buat Proyek** dan tunggu inisialisasi selesai

#### 1.2 Konfigurasi Authentication

1. Di menu navigasi kiri, pilih **Authentication**
2. Klik tab **Sign-in method**
3. Aktifkan provider:
   - ✅ **Google** (Email & Password)
   - ✅ **Anonymous** (untuk akses tanpa login)

#### 1.3 Setup Cloud Firestore Database

1. Di menu navigasi kiri, pilih **Cloud Firestore**
2. Klik **Buat Database**
3. Pilih mode **Start in production mode**
4. Pilih lokasi server terdekat (Asia Southeast 1 untuk Indonesia)
5. Klik **Buat**

#### 1.4 Set Security Rules Firestore

Buka tab **Rules** di Firestore dan ganti dengan kode berikut:

```firestore
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    
    // ===== ATURAN PUBLIK: Direktori Guru & Data Kolaboratif =====
    match /artifacts/{appId}/public/data/{collectionName}/{document=**} {
      allow read: if request.auth != null;
      allow write: if request.auth != null && resource.data.userId == request.auth.uid;
    }
    
    // ===== ATURAN PRIVAT: Profil Guru, Jurnal, Data Siswa (6 Segment Path) =====
    match /artifacts/{appId}/users/{userId}/{collectionName}/{document=**} {
      allow read, write: if request.auth != null && request.auth.uid == userId;
    }
    
    // ===== Deny semua akses lain =====
    match /{document=**} {
      allow read, write: if false;
    }
  }
}
```

Klik **Publikasikan**.

#### 1.5 Dapatkan Firebase Config

1. Di dashboard Firebase, klik ikon roda gigi ⚙️ (Project Settings)
2. Scroll ke bagian **SDK setup and configuration**
3. Pilih **HTML**
4. Salin obyek `firebaseConfig` (berisi: apiKey, authDomain, projectId, storageBucket, messagingSenderId, appId)

Contoh Firebase Config:
```javascript
const firebaseConfig = {
  apiKey: "AIzaSyxxxxxxxxxxxxxxxxxxxxxxxxxx",
  authDomain: "eduips-xyz.firebaseapp.com",
  projectId: "eduips-xyz",
  storageBucket: "eduips-xyz.appspot.com",
  messagingSenderId: "123456789012",
  appId: "1:123456789012:web:abcdef123456"
};
```

### Langkah 2: Dapatkan Gemini API Key

1. Kunjungi [Google AI Studio](https://aistudio.google.com/apikey)
2. Login dengan akun Google Anda
3. Klik **Create API Key**
4. Salin kunci yang ditampilkan (akan dipakai nanti oleh pengguna di aplikasi)

### Langkah 3: Persiapan File Aplikasi

#### 3.1 Unduh atau Clone Repository

```bash
# Clone repository
git clone https://github.com/kangtoer/eduips.git
cd eduips

# Atau download file index.html langsung dari GitHub
```

#### 3.2 Update Firebase Config di index.html

Buka file `index.html` dan cari baris berikut (sekitar line 415):

```javascript
const firebaseConfigStr = typeof __firebase_config !== 'undefined' ? __firebase_config : '{}';
let firebaseConfig = {};
try { firebaseConfig = JSON.parse(firebaseConfigStr); } catch (e) { console.error("Invalid Firebase config", e); }
```

**OPSI A: Update langsung di index.html**
Ganti dengan:

```javascript
const firebaseConfig = {
  apiKey: "YOUR_API_KEY_HERE",
  authDomain: "your-project.firebaseapp.com",
  projectId: "your-project-id",
  storageBucket: "your-project.appspot.com",
  messagingSenderId: "123456789012",
  appId: "1:123456789012:web:abcdef"
};
```

**OPSI B: Injeksi via Global Variable (Aman)**
Biarkan tetap seperti semula dan sisipkan konfigurasi via `<script>` tag sebelum aplikasi memuat.

---

## 🚀 Panduan Deployment di GitHub Pages

### Metode 1: Upload via Web Interface GitHub (Paling Mudah)

1. **Buat Repository Baru**
   - Masuk ke GitHub: https://github.com/new
   - Repository name: `eduips` (atau nama lain)
   - Pilih **Public**
   - Klik **Create repository**

2. **Upload File index.html**
   - Klik tombol **uploading an existing file**
   - Drag & drop file `index.html` ke area upload
   - Isi **Commit message**: `Initial commit: EduIPS application`
   - Klik **Commit changes**

3. **Aktifkan GitHub Pages**
   - Buka tab **Settings** di repository Anda
   - Klik **Pages** di menu sebelah kiri
   - Bagian **Build and deployment**:
     - Source: **Deploy from a branch**
     - Branch: **main** | Folder: **/ (root)**
   - Klik **Save**

4. **Tunggu Deployment**
   - GitHub akan memproses selama 1-2 menit
   - URL publik akan menjadi: `https://username.github.io/eduips/`
   - Refresh halaman Settings untuk melihat status deployment

### Metode 2: Upload via Git Command Line

```bash
# 1. Inisialisasi repository lokal
cd /path/to/eduips
git init

# 2. Tambahkan file
git add index.html
git add README.md

# 3. Commit
git commit -m "Initial commit: EduIPS portal application"

# 4. Tambahkan remote repository
git remote add origin https://github.com/USERNAME/eduips.git

# 5. Rename branch ke main
git branch -M main

# 6. Push ke GitHub
git push -u origin main
```

Kemudian lanjut ke langkah **Aktifkan GitHub Pages** pada Metode 1 (poin 3-4).

### Verifikasi Deployment

Setelah deployment selesai:
- 🌐 Kunjungi URL: `https://username.github.io/eduips/`
- 📝 Halaman login EduIPS harus tampil
- 🔐 Coba login dengan Google atau Anonymous

---

## 📖 Panduan Penggunaan

### Untuk Guru (Pengguna Pemula)

#### 1. **Cara Masuk ke Aplikasi**

**Opsi A: Login dengan Google (Direkomendasikan)**
- Klik tombol **Masuk & Sinkronkan Drive**
- Pilih akun Google Anda
- Berikan izin akses ke Google Drive
- Anda siap menggunakan semua fitur dengan auto-sync

**Opsi B: Login Tanpa Akun (Draf Lokal)**
- Klik tombol **Masuk Tanpa Akun (Draf Lokal)**
- Data disimpan hanya di browser lokal Anda
- Cocok untuk uji coba cepat tanpa koneksi cloud

#### 2. **Konfigurasi Profil (Wajib Dilakukan Terlebih Dahulu)**

Sebelum membuat perangkat ajar, lengkapi profil Anda:

1. Klik menu **Profil & Cloud API** di sidebar
2. Isi formulir:
   - **Nama Lengkap & Gelar**: Cth. `Budi Santoso, S.Pd., M.Pd.`
   - **NIP/NIYPK**: (opsional, untuk dokumen resmi)
   - **Nama Instansi/Sekolah**: Cth. `SMP Negeri 1 Kota Besar`
3. **API Key Gemini Pribadi** (PENTING):
   - Pergi ke [Google AI Studio](https://aistudio.google.com/apikey)
   - Klik **Create API Key**
   - Copy-paste key ke kolom **API Key Gemini Pribadi**
   - Ini memastikan Anda punya kuota tak terbatas sendiri
4. Klik **Simpan Pengaturan**

#### 3. **Membuat RPP-PM (Rencana Pelaksanaan Pembelajaran)**

RPP-PM adalah format RPP modern yang fokus pada pemahaman konsep mendalam.

1. Klik menu **RPP-PM (Modul Ajar)** di sidebar
2. Isi formulir di panel kiri:
   - **Fase / Kelas**: Pilih Fase D (VII, VIII, atau IX)
   - **Tema Pembelajaran**: Pilih dari 5 tema IPS
   - **Materi Pokok / Sub Topik**: 
     - Cth. untuk Sejarah: *"Dampak Kolonialisme di Indonesia terhadap aspek sosial-budaya"*
     - Cth. untuk Geografi: *"Pengaruh geografis terhadap mata pencaharian dan mobilitas penduduk"*
   - **Alokasi Waktu**: Default `2 JP (2 x 40 Menit)`, ubah sesuai kebutuhan
   - **Dimensi Profil Lulusan**: Centang 8 poin yang relevan dengan pembelajaran Anda
     - Contoh untuk tema Sejarah: Centang "Bernalar Kritis", "Literasi", "Berkebhinekaan Global"

3. Klik **Susun RPP-PM**
4. Tunggu 3-10 detik, AI akan menyusun dokumen
5. Dokumen akan muncul di panel kanan dalam format A4 siap cetak

**Tips:**
- Materi pokok yang spesifik → RPP yang lebih fokus
- Pilih dimensi yang relevan → Dokumen lebih targeted
- Gunakan API Key pribadi Anda untuk performa optimal

#### 4. **Membuat Bank Soal TKA (Tes Kemampuan Akademik)**

1. Klik menu **Bank Soal TKA** di sidebar
2. Isi formulir:
   - **Cakupan Materi**: Cth. *"Kegiatan Ekonomi & Pasar Bebas di Era Globalisasi"*
   - **Jumlah Pilihan Ganda**: Default 10, ubah sesuai kebutuhan (1-50)
   - **Komposisi Kognitif**: Pilih salah satu:
     - **Proporsional Standard**: LOTS (30%), MOTS (40%), HOTS (30%) - **DIREKOMENDASIKAN**
     - **Fokus HOTS**: Analisis & Evaluasi tingkat tinggi
     - **Fokus Dasar**: Pemahaman & Aplikasi

3. Klik **Racik Soal TKA**
4. AI akan menghasilkan:
   - Soal pilihan ganda dengan opsi homogen (tidak bias)
   - Soal uraian tambahan
   - Kunci jawaban lengkap

**Fitur Unggulan:**
- ✅ **Anti-Tebak Jawaban**: Opsi A, B, C, D memiliki panjang kalimat serupa
- ✅ **Standar TKA**: Soal dioptimalkan untuk menguji nalar kritis
- ✅ **Diksi Siswa**: Bahasa disesuaikan untuk SMP/MTs

#### 5. **Membuat Bahan Ajar (Handout)**

1. Klik menu **Bahan Ajar** di sidebar
2. Isi formulir:
   - **Topik / Sub Materi**: Cth. *"Mobilitas Sosial & Integrasi Bangsa"*
   - **Target Kelas**: Cth. *"Kelas VIII SMP"*
   - **Format Penyajian**: Pilih salah satu:
     - **Ringkasan Esensial Poin**: Bullet points ringkas, mudah dihafal
     - **Narasi Deskriptif Komprehensif**: Penjelasan panjang & detail
     - **Format Diskusi Q&A**: Tanya-jawab interaktif

3. Klik **Tulis Bahan Ajar**
4. Handout akan dihasilkan dalam format siap dibagikan ke siswa

#### 6. **Membuat Rubrik Penilaian**

1. Klik menu **Rubrik Penilaian** di sidebar
2. Isi formulir:
   - **Jenis Tugas / Proyek**: Cth. *"Presentasi Studi Kasus: Dampak Perubahan Iklim"*
   - **Aspek Dinilai** (opsional): Cth. *"Kerja Sama, Kualitas Argumen, Kreativitas Presentasi"*
   - **Skala Penilaian**: Pilih:
     - **Kurikulum Merdeka**: MB, Berkembang, Cakap, Mahir (4 level)
     - **Skala 1-4 Standard**: Kurang, Cukup, Baik, Sangat Baik

3. Klik **Buat Rubrik**
4. Matriks penilaian akan dihasilkan dalam format tabel terstruktur

#### 7. **Pencatatan Jurnal Kelas Harian**

1. Klik menu **Jurnal Kelas (PM)** di sidebar
2. Panel kiri: Isi formulir baru
   - **Tanggal & Jam**: Pilih tanggal dan waktu pembelajaran
   - **Kelas**: Cth. *"VIII-A"* atau *"IX-B"*
   - **Materi / Bahasan RPP-PM**: Cth. *"Menganalisis pengaruh geografis terhadap mata pencaharian"*
   - **Ketercapaian / Catatan Kejadian**: Cth. *"Siswa sangat antusias, 2 siswa belum mengumpulkan tugas, diskusi berkualitas"*

3. Klik **Tambah ke Jurnal**
4. Jurnal akan masuk ke tabel di panel kanan

**Aksi di Jurnal:**
- **Ekspor Jurnal (Dinas HTML)**: Download jurnal dalam format HTML siap cetak
- **Simpan ke Drive**: Sinkronkan ke Google Drive Anda

#### 8. **Manajemen Data Siswa Masal**

1. Klik menu **Data Siswa Masal** di sidebar

**Opsi A: Upload File (XLS/XLSX atau DOCX)**
- Drag & drop file ke zona upload, atau klik untuk memilih
- Sistem otomatis ekstrak data siswa dari file

**Opsi B: Copy-Paste Manual**
- Buka file Excel Anda
- Copy daftar nama siswa (format: NAMA, GENDER)
  ```
  Ahmad, L
  Siti, P
  Budi, L
  Ayu, P
  ```
- Paste ke kolom **Tempel Data Siswa**
- Klik **Proses Data Tempel**

3. Daftar siswa akan muncul di tabel
4. Klik **Simpan ke Drive** untuk sinkronisasi

#### 9. **Mencetak Dokumen & Penyimpanan**

Setelah dokumen berhasil di-generate:

**Cetak / PDF:**
1. Klik tombol **Cetak / PDF** di panel dokumen
2. Dialog cetak browser akan terbuka
3. Pilih printer atau **Save as PDF**
4. Dokumen akan lengkap dengan Kop Dinas & area tanda tangan

**Simpan ke Google Drive:**
1. Pastikan Anda sudah login dengan Google
2. Klik tombol **Simpan ke Drive** 
3. Dokumen akan terunggah ke Google Drive Anda dalam folder terstruktur
4. Toast notifikasi akan muncul: "Dokumen berhasil disimpan ke Drive"

---

## 🔐 Konfigurasi Firebase

### Security Rules Lengkap

```firestore
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    
    // RULE 1: Publik - Direktori Guru & Kolaborasi
    // Path: /artifacts/{appId}/public/data/{collectionName}/{document=**}
    match /artifacts/{appId}/public/data/{collectionName}/{document=**} {
      allow read: if request.auth != null;
      allow write: if request.auth != null && resource.data.userId == request.auth.uid;
    }
    
    // RULE 3: Privat - Profil, Jurnal, Data Siswa (6-Segment Path)
    // Path: /artifacts/{appId}/users/{userId}/{collectionName}/{document=**}
    match /artifacts/{appId}/users/{userId}/{collectionName}/{document=**} {
      allow read, write: if request.auth != null && request.auth.uid == userId;
    }
    
    // Default Deny
    match /{document=**} {
      allow read, write: if false;
    }
  }
}
```

### Struktur Firestore

```
artifacts/
├── eduips-xyz (appId)
│   ├── public/
│   │   └── data/
│   │       ├── users/
│   │       │   ├── {userId1}: {nama, nip, sekolah, role}
│   │       │   └── {userId2}: {...}
│   │       └── modules/
│   │           └── {moduleId}: {title, description, ...}
│   │
│   └── users/
│       ├── {userId1}/
│       │   ├── profileData/
│       │   │   └── default: {nama, nip, sekolah, isAdmin, customApiKey, ...}
│       │   ├── journals/
│       │   │   ├── {journalId1}: {date, class, topic, notes, ...}
│       │   │   └── {journalId2}: {...}
│       │   └── students/
│       │       ├── {studentId1}: {nama, gender, ...}
│       │       └── {studentId2}: {...}
│       │
│       └── {userId2}/
│           └── {...}
```

---

## 🔌 API & Integrasi

### Google Gemini AI API

**Endpoint:**
```
https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-09-2026:generateContent?key={API_KEY}
```

**Model:**
- `gemini-2.5-flash-preview-09-2026` (default untuk EduIPS)

**Request Format:**
```javascript
const payload = {
  contents: [{
    parts: [{
      text: "Buatlah RPP-PM untuk Kelas VII dengan tema Sejarah tentang 'Dampak Kolonialisme'..."
    }]
  }]
};

const response = await fetch(endpoint, {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify(payload)
});

const result = await response.json();
const aiOutput = result.candidates[0].content.parts[0].text;
```

### Google Drive API

**Scopes:**
```
https://www.googleapis.com/auth/drive.file
```

**Auth Flow:**
1. User klik "Masuk & Sinkronkan Drive"
2. Browser pop-up untuk login Google
3. Access Token tersimpan di localStorage
4. Documents di-upload menggunakan Drive API

### Firebase Authentication

**Providers:**
- ✅ Google OAuth 2.0
- ✅ Anonymous

**Custom Claims untuk Admin:**
```javascript
// Di Firebase Console atau Cloud Function:
admin.auth().setCustomUserClaims(uid, { admin: true });
```

---

## 📊 Struktur Data

### User Profile Schema
```javascript
{
  uid: string,              // Firebase UID
  displayName: string,      // Nama dari Google Account
  email: string,            // Email Google
  nama: string,             // Nama lengkap dengan gelar
  nip: string,              // NIP atau NIYPK
  sekolah: string,          // Nama sekolah/instansi
  isAdmin: boolean,         // Flag administrator
  customApiKey: string,     // Gemini API Key pribadi (encrypted)
  journals: Array<Journal>, // Jurnal mengajar harian
  students: Array<Student>, // Daftar siswa kelas
  createdAt: timestamp,
  updatedAt: timestamp
}
```

### Journal Entry Schema
```javascript
{
  id: string,
  userId: string,
  date: string,             // ISO 8601 datetime
  class: string,            // Nama kelas (VIII-A, IX-B, dll)
  topic: string,            // Materi yang diajarkan
  notes: string,            // Catatan ketercapaian
  attendance: number,       // Jumlah siswa hadir
  createdAt: timestamp
}
```

### Student Record Schema
```javascript
{
  id: string,
  userId: string,
  nama: string,             // Nama siswa
  gender: string,           // "L" atau "P"
  nisn: string,             // (opsional) NISN
  createdAt: timestamp
}
```

---

## 🎓 Dimensi Profil Lulusan Kurikulum Merdeka

EduIPS terintegrasi dengan **8 Dimensi Profil Lulusan** dari Kurikulum Merdeka:

| # | Dimensi | Keterangan |
|---|---------|-----------|
| 1 | **Beriman, Bertakwa kepada Tuhan YME, dan Berakhlak Mulia** | Fondasi moral dan spiritual |
| 2 | **Berkebhinekaan Global** | Menghargai keragaman budaya & perspektif global |
| 3 | **Bergotong Royong** | Kolaborasi, kerja sama, kepedulian sosial |
| 4 | **Mandiri** | Inisiatif, disiplin, tanggung jawab diri |
| 5 | **Bernalar Kritis** | Berpikir logis, analitis, evaluatif |
| 6 | **Kreatif** | Inovasi, imajinasi, produksi hal baru |
| 7 | **Literasi** | Kemampuan membaca, menulis, memahami teks |
| 8 | **Numerasi** | Kemampuan berhitung dan analisis data |

Setiap RPP-PM dapat disesuaikan dengan dimensi-dimensi mana yang menjadi fokus pembelajaran.

---

## 🤝 Kontribusi

Kami mengundang guru, pengembang, dan peneliti pendidikan untuk berkontribusi!

### Cara Berkontribusi:

1. **Fork** repository ini
2. Buat branch baru: `git checkout -b feature/nama-fitur`
3. Commit perubahan: `git commit -m 'Add: Deskripsi fitur'`
4. Push ke branch: `git push origin feature/nama-fitur`
5. Buat **Pull Request** dengan deskripsi detail

### Kontribusi yang Kami Terima:

- 🐛 **Bug Fixes**: Perbaikan error atau issue
- ✨ **New Features**: Fitur pembelajaran baru
- 📝 **Documentation**: Dokumentasi dan panduan
- 🌍 **Translations**: Dukungan bahasa tambahan
- 🎨 **UI/UX Improvements**: Peningkatan tampilan dan pengalaman
- 📚 **Educational Resources**: Template pembelajaran, contoh materi

---

## 📄 Lisensi

EduIPS dirilis di bawah lisensi **MIT License**.

```
MIT License

Copyright (c) 2026 Kangtoer & EduIPS Contributors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.
```

Lihat file [LICENSE](LICENSE) untuk detail lengkap.

---

## ❓ FAQ

### **Q: Apakah EduIPS gratis?**
**A:** Ya, 100% gratis dan open-source. Anda hanya perlu API Key Gemini gratis dari Google (unlimited untuk penggunaan personal).

### **Q: Apakah data saya aman?**
**A:** Sangat aman. Semua data tersimpan di Firestore dengan enkripsi end-to-end. Data Anda milik Anda sendiri. Tidak ada pihak ketiga yang bisa mengakses privasi Anda.

### **Q: Bagaimana jika saya offline?**
**A:** EduIPS menyimpan draft lokal di browser. Saat online, akan otomatis sinkronisasi ke Google Drive. Anda tetap bisa bekerja offline, kemudian sinkronisasi nanti.

### **Q: Bisakah saya menggunakan EduIPS di smartphone?**
**A:** Ya! Aplikasi ini responsive dan dapat diakses di mobile browser (Chrome, Safari). Namun pengalaman optimal untuk desktop.

### **Q: Bagaimana cara mendapat API Key Gemini?**
**A:** 
1. Kunjungi [Google AI Studio](https://aistudio.google.com/apikey)
2. Login dengan akun Google Anda
3. Klik **Create API Key**
4. Salin dan paste di menu **Profil & Cloud API** → **API Key Gemini Pribadi**

### **Q: Apakah AI-generated content bebas plagiarisme?**
**A:** Konten dihasilkan dari prompt struktural dan konteks lokal Anda. Namun tetap disarankan untuk review & edit sebelum diberikan ke siswa guna memastikan keaslian dan relevansi maksimal.

### **Q: Bisakah saya deploy di sekolah/instansi sendiri?**
**A:** Ya! Ikuti panduan **Deployment di GitHub Pages** atau deploy ke hosting pribadi. Anda memiliki kontrol penuh atas source code.

### **Q: Bagaimana dukungan teknis?**
**A:** 
- 📧 Email: [hubungi pengembang]
- 🐙 GitHub Issues: [buat issue di repository](https://github.com/kangtoer/eduips/issues)
- 💬 Diskusi: [GitHub Discussions](https://github.com/kangtoer/eduips/discussions)

### **Q: Apakah ada versi bahasa Inggris?**
**A:** Saat ini UI dalam bahasa Indonesia (sesuai Kurikulum Merdeka). Kontribusi untuk i18n sangat diterima!

---

## 🌟 Roadmap Fitur Mendatang

- [ ] Export ke Microsoft Word (.docx) format
- [ ] Analitik pembelajaran & tracking progress siswa
- [ ] Integrasi dengan Learning Management System (LMS)
- [ ] Fitur kolaborasi antar guru dalam satu sekolah
- [ ] Template siap pakai dari guru terbaik
- [ ] Mobile app native (iOS & Android)
- [ ] Fitur import dari platform lain (Google Classroom, dll)
- [ ] Dukungan bahasa internasional (English, Chinese, dll)
- [ ] AI-powered comment & feedback untuk siswa

---

## 📞 Kontak & Jejaring

- 🌐 **Website**: [Catatan Guru IPS](https://toer.my.id)
- 📧 **Email**: pamungkazcatur@gmail.com
- 🐙 **GitHub**: [@kangtoer](https://github.com/kangtoer)
- 🐦 **Twitter/X**: [@kangtoer](https://x.com/kangtoer)

---

## 🙏 Ucapan Terima Kasih

Terima kasih kepada:
- **Guru IPS Seluruh Indonesia** atas inspirasi dan feedback berharga
- **MGMP IPS SMP Kabupaten Kebumen** atas kesempatan yang diberikan untuk terus berkembang
- **Google** untuk Gemini AI, Firebase, dan Google Workspace APIs
- **Tailwind CSS** dan **FontAwesome** untuk komponen UI
- **Open-source community** atas dukungan berkelanjutan
- **Istri dan Anakku** karena demi ngoprek ini, waktuku bersama kalian harus disarutang

---

## 📝 Catatan Pengembang

### Development Setup

```bash
# Clone repository
git clone https://github.com/kangtoer/eduips.git
cd eduips

# Edit index.html dengan text editor (VS Code, Sublime, dll)
# Tidak ada build process diperlukan

# Test lokal
python -m http.server 8000
# Buka http://localhost:8000

# Push ke GitHub
git add .
git commit -m "Your message"
git push
```

### Browser Support
- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+
- ✅ Mobile browsers (iOS Safari, Chrome Android)

### Performance Tips
- Gunakan API Key pribadi untuk performa optimal
- File yang di-generate disimpan di localStorage browser
- Sinkronisasi ke Drive dilakukan async (tidak mengganggu UX)

---

## 📜 Perubahan & Riwayat Versi

### v1.0.0 (2026)
- ✨ Release awal EduIPS
- 🎯 Generator RPP-PM dengan 8 Dimensi Profil Lulusan
- 🧠 Bank Soal TKA berkualitas tinggi
- 📚 Generator Bahan Ajar & Rubrik Penilaian
- 📅 Jurnal Kelas Harian & Manajemen Data Siswa
- 🌐 Integrasi Google Workspace & Google Drive
- 🔐 Firebase Authentication & Firestore Database

Lihat [CHANGELOG.md](CHANGELOG.md) untuk detail perubahan setiap versi.

---

**Dibuat dengan ❤️ untuk pendidikan Indonesia yang lebih baik.**

*Last Updated: 2026-06 | Versi: 1.0.0*
