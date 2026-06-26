# 🌍 EduIPS - Portal Administrasi Guru IPS Profesional & RPP-PM

[![Framework - TailwindCSS](https://img.shields.io/badge/UI--Framework-Tailwind--CSS-blue.svg)](https://tailwindcss.com/)
[![Language - JavaScript](https://img.shields.io/badge/Language-Vanilla--JavaScript-yellow.svg)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Integration - Google Drive](https://img.shields.io/badge/Integration-Google--Drive--API-emerald.svg)](https://developers.google.com/drive)
[![Security - DOMPurify](https://img.shields.io/badge/Security-DOMPurify--Protected-red.svg)](https://github.com/cure53/DOMPurify)

**EduIPS** adalah platform portal administrasi digital terintegrasi yang dirancang khusus untuk memfasilitasi kebutuhan administratif Guru Ilmu Pengetahuan Sosial (IPS) tingkat SMP/MTs (Fase D). Aplikasi ini mengotomatisasi penyusunan dokumen perangkat ajar berstandar mutu **RPP-PM (Rencana Pelaksanaan Pembelajaran - Pendalaman Materi) v2026** serta instrumen penilaian nalar tinggi secara instan ke penyimpanan cloud pribadi Anda.

---

## ✨ Fitur Utama Aplikasi

Sistem administrasi di dalam EduIPS dibagi menjadi 4 pilar utama yang dapat diakses langsung melalui Sidebar Navigasi yang responsif:

### 1. Perencanaan Pembelajaran (RPP-PM)
* **Generator Modul Ajar (RPP-PM):** Menyusun Modul Ajar secara otomatis berbasis parameter spesifik: Fase/Kelas (VII, VIII, IX), Tema IPS (Sejarah, Geografi, Ekonomi, Sosiologi, atau IPS Terpadu), materi pokok, alokasi waktu, serta pemilihan 8 Dimensi Profil Lulusan.
* **Penyusun Prota & Prosem:** Otomatisasi pembagian alokasi Jam Pelajaran (JP) tahunan (default: 144 JP) ke dalam Bab Pembahasan program tahunan dan semesteran secara rapi.

### 2. Pelaksanaan Kelas (Manajemen Harian)
* **Jurnal Agenda Guru:** Mencatat aktivitas harian, ketercapaian materi, dan hambatan pembelajaran di kelas secara real-time.
* **Presensi & Bimbingan (BK):** Mengelola daftar kehadiran siswa sekaligus log bimbingan konseling ringkas untuk siswa yang membutuhkan penanganan khusus.

### 3. Evaluasi & Asesmen Pintar
* **Kisi-kisi & Soal TKA (Tes Kemampuan Akademik):** Menghasilkan instrumen soal evaluasi berbasis nalar/HOTS secara acak dan bebas pola panjang untuk mengukur kedalaman berpikir siswa.
* **Nilai & Analisis Remedial:** Menginput nilai hasil belajar sekaligus melakukan analisis otomatis untuk menentukan siswa yang memerlukan program remedial atau pengayaan.
* **Bahan Ajar & Rubrik:** Menyediakan bank data bahan ajar pendukung beserta rubrik penilaian performa siswa yang terstandardisasi.

### 4. Pendukung Wali Kelas
* **Denah Kelas Pintar:** Fitur visual tata letak tempat duduk siswa di kelas yang interaktif untuk membantu manajemen kondusivitas ruang belajar.
* **Buku Mutasi & Log Siswa:** Manajemen database profil siswa lengkap dengan fitur impor data massal dari format XLS/Docx.

### 5. Integrasi Cloud & Keamanan Kode
* **Sinkronisasi Google Workspace:** Mendukung login menggunakan Google Account untuk otomatisasi pencadangan dan sinkronisasi berkas administrasi langsung ke Google Drive Workspace Anda.
* **Mode Sesi Lokal (Anonim):** Akses penuh tanpa login akun untuk pengerjaan cepat menggunakan penyimpanan lokal (*local storage*) perangkat.
* **Secure Document Rendering:** Menggunakan pustaka *Marked.js* untuk pratinjau dokumen berbasis Markdown dan diproteksi oleh *DOMPurify* untuk mencegah celah keamanan Cross-Site Scripting (XSS).
* **Fitur Pratinjau Standar Dinas:** Tampilan editor menggunakan *Paper Preview Layout* berbasis skala ukuran kertas A4 siap cetak atau ekspor langsung ke format PDF.

---

## 🛠️ Spesifikasi Teknologi (Tech Stack)

Aplikasi ini dibangun menggunakan arsitektur modern berbasis *Single Page Application (SPA)* murni tanpa memerlukan kompilasi berat (*Zero-Build Stack*):

* **HTML5 & CSS3:** Struktur dokumen semantik berkemampuan cetak (*print-friendly rules*).
* **Tailwind CSS (v3.x):** Framework CSS utilitas untuk tata letak antarmuka yang modern, dinamis, dan responsif (Mobile & Desktop).
* **Vanilla JavaScript (ES6+):** Logika manipulasi DOM, state management lokal, dan integrasi API cloud tanpa ketergantungan framework berat.
* **FontAwesome v6.4.0:** Pustaka ikonografi premium untuk penanda visual menu dan tombol aksi.
* **Marked.js:** Engine parser pengubah format teks terstruktur AI menjadi HTML siap tayang.
* **DOMPurify v3.0.6:** Sanitasi elemen HTML dinamis untuk menjaga keamanan injeksi skrip.

---

## 🚀 Panduan Instalasi & Penggunaan

Karena aplikasi ini bersifat *client-side murni*, Anda tidak perlu menginstal server lokal (seperti Node.js/PHP). Cukup ikuti langkah mudah berikut:

### Langkah 1: Kloning Repositori
Kloning proyek ini ke komputer lokal Anda menggunakan Git:
```bash
git clone [https://github.com/USERNAME_ANDA/EduIPS.git](https://github.com/USERNAME_ANDA/EduIPS.git)
cd EduIPS
