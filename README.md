# 🌍 EduIPS - Portal Administrasi Guru IPS Profesional & RPP-PM v2026

[![Framework - TailwindCSS](https://img.shields.io/badge/UI--Framework-Tailwind--CSS-blue.svg)](https://tailwindcss.com/)
[![Language - JavaScript](https://img.shields.io/badge/Language-Vanilla--JavaScript-yellow.svg)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Integration - Google Drive](https://img.shields.io/badge/Integration-Google--Drive--API-emerald.svg)](https://developers.google.com/drive)
[![Security - DOMPurify](https://img.shields.io/badge/Security-DOMPurify--Protected-red.svg)](https://github.com/cure53/DOMPurify)
[![Markdown - Marked.js](https://img.shields.io/badge/Parser-Marked.js-blueviolet.svg)](https://github.com/markedjs/marked)

**EduIPS** adalah platform portal administrasi digital murni sisi-klien (*pure client-side portal*) yang dirancang khusus untuk memfasilitasi kebutuhan kerja administratif Guru Ilmu Pengetahuan Sosial (IPS) tingkat SMP/MTs (Fase D). Aplikasi ini mengotomatisasi penyusunan dokumen perangkat ajar berstandar mutu **RPP-PM (Rencana Pelaksanaan Pembelajaran - Pendalaman Materi) v2026** serta instrumen penilaian nalar tinggi secara instan langsung ke penyimpanan cloud pribadi Anda.

Aplikasi dikemas dalam arsitektur *Single Page Application (SPA)* berbasis berkas tunggal yang ringan, responsif, dan siap cetak sesuai standar kedinasan.

---

## 🚀 Fitur Utama & Pembagian Modul

Sistem administrasi di dalam EduIPS dibagi menjadi 4 pilar utama yang dapat diakses langsung melalui Sidebar Navigasi yang responsif:

### 1. Administrasi Perencanaan (Perangkat Ajar)
* **Modul Ajar (RPP-PM):** Generator dokumen perencanaan otomatis berbasis parameter dinamis:
  * Pemilihan Fase & Kelas (Fase D - Kelas VII, VIII, IX).
  * Pembagian Tema Pembelajaran IPS Terstandardisasi (Sejarah, Geografi, Ekonomi, Sosiologi, atau IPS Terpadu lintas tema).
  * Custom input Materi Pokok / Sub Topik serta Alokasi Waktu.
  * Pemilihan multi-opsi 8 Dimensi Profil Lulusan (Beriman & Bertakwa, Berkebhinekaan Global, Bergotong Royong, Mandiri, Bernalar Kritis, Kreatif, Literasi, Numerasi).
* **Prota & Prosem (Program Tahunan & Semester):** Menyusun pembagian alokasi Jam Pelajaran (JP) tahunan (secara default diset ke 144 JP) berdasarkan fokus bab pembahasan secara otomatis.

### 2. Administrasi Pelaksanaan Kelas
* **Jurnal Agenda Guru:** Mencatat log harian aktivitas mengajar kelas, ketercapaian materi esensial, serta catatan hambatan di lapangan.
* **Presensi & Bimbingan (BK):** Mengelola absensi harian siswa sekaligus log bimbingan konseling ringkas untuk penanganan cepat kendala belajar siswa.

### 3. Administrasi Evaluasi & Asesmen
* **Kisi-kisi & Soal TKA (Tes Kemampuan Akademik):** Penyusun instrumen evaluasi kognitif berbasis nalar tinggi (HOTS) yang dikonfigurasi agar bebas pola panjang.
* **Nilai & Analisis Remedial:** Modul input nilai hasil belajar yang dilengkapi dengan mesin analisis otomatis untuk mendeteksi siswa yang membutuhkan program remedial atau pengayaan.
* **Bahan Ajar & Rubrik:** Menyediakan pangkalan data materi pendukung pembelajaran serta lembar kriteria rubrik penilaian performa siswa.

### 4. Administrasi Pendukung Wali Kelas
* **Denah Kelas Pintar:** Fitur visual interaktif penataan posisi tempat duduk siswa untuk mengoptimalkan kondusivitas ruang kelas.
* **Buku Mutasi & Log Siswa:** Manajemen database profil murid lengkap dengan kapabilitas pengunggahan/impor data massal dari format eksternal spreadsheet.

---

## 🛠️ Spesifikasi Teknologi (Tech Stack)

EduIPS mengadopsi pendekatan *Zero-Build Stack*, artinya aplikasi dapat berjalan langsung di peramban tanpa memerlukan tahapan kompilasi web atau instalasi runtime server eksternal:

* **Antarmuka (UI):** [Tailwind CSS (v3.x)](https://tailwindcss.com/) via CDN dengan konfigurasi tema warna institusional (`primary: #1e40af`, `secondary: #3b82f6`, `accent: #f59e0b`, `success: #10b981`, `danger: #ef4444`).
* **Ikonografi:** [FontAwesome v6.4.0](https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css) untuk penanda visual menu navigasi yang komprehensif.
* **Mesin Dokumen:** [Marked.js](https://cdn.jsdelivr.net/npm/marked/marked.min.js) sebagai Markdown parser tercepat untuk mengubah draf dokumen teks terstruktur menjadi markup HTML siap cetak.
* **Keamanan DOM:** [DOMPurify v3.0.6](https://cdnjs.cloudflare.com/ajax/libs/dompurify/3.0.6/purify.min.js) untuk menyaring elemen HTML ilegal hasil parsing, memberikan proteksi mutlak dari celah keamanan Cross-Site Scripting (XSS).
* **Logika Aplikasi:** Vanilla JavaScript (ES6+) murni untuk mengelola state view (*SPA Switching via dataset target*), interaksi komponen, sinkronisasi local storage, serta jembatan API.

---

## 🔐 Mode Akses & Manajemen Sesi

Aplikasi menyediakan dua jalur gerbang masuk (*Login Gate*) untuk fleksibilitas kerja guru:
1. **Masuk & Sinkronkan Drive (Google Workspace):** Memanfaatkan *Google Identity Services* untuk otentikasi aman pengguna, memunculkan indikator status *Workspace Active*, dan mengaktifkan integrasi Google Drive API secara langsung.
2. **Masuk Tanpa Akun (Sesi Lokal):** Menggunakan enkapsulasi penyimpanan lokal peramban (*Local Storage*) perangkat Anda. Mode anonim ini sepenuhnya aman karena data tidak dikirim ke server luar manapun.

---

## 🖨️ Standar Cetak Kedinasan (Paper Preview Setup)

Lembar keluaran dokumen pratinjau (`#ai-output-container` & `#prota-output-container`) dirancang menggunakan visualisasi **Paper Preview Layout** dengan rasio dimensi presisi kertas dinas **A4** (Lebar: `210mm`, Tinggi Minimum: `297mm`). Aturan tipografi bawaan menggunakan font resmi *Times New Roman* dengan ukuran font isi `11pt`, teks rata kanan-kiri (*justify*), serta border tabel bergaris tegas (`#111827`).

### Panduan Ekspor ke PDF / Cetak Fisik:
1. Klik tombol **Cetak / PDF** pada bilah menu pratinjau dokumen.
2. Pada dialog cetak bawaan sistem operasi / peramban:
   * Atur **Tujuan / Destination** ke **Simpan sebagai PDF (Save as PDF)** atau pilih mesin pencetak fisik Anda.
   * Pastikan **Ukuran Kertas (Paper Size)** diatur ke opsi **A4**.
   * Setel **Margin** ke **None** atau **Default**.
   * Wajib mencentang opsi **Grafik Latar Belakang (Background Graphics)** agar warna shading header tabel (`#f3f4f6`) dan aksen warna cetak tetap terekam sempurna.

---

## 🚀 Panduan Instalasi Lokal

Karena platform ini berjalan di sisi klien secara penuh, proses instalasi sangat sederhana:

### Langkah 1: Kloning Repositori
```bash
git clone [https://github.com/USERNAME_ANDA/EduIPS.git](https://github.com/USERNAME_ANDA/EduIPS.git)
cd EduIPS
Langkah 2: Jalankan Berkas Utama
Opsi A (Penggunaan Cepat): Klik ganda berkas index.html langsung dari file manager komputer Anda untuk membukanya di peramban web pilihan Anda.

Opsi B (Rekomendasi Pengembang): Jalankan ekstensi Live Server di VS Code untuk mengaktifkan pemantauan kode berkala dengan alamat host lokal default http://127.0.0.1:5500.

Langkah 3: Konfigurasi OAuth Google Cloud (Opsional)
Untuk mengaktifkan pencadangan otomatis Google Drive secara penuh pada tab Profil & Cloud API:

Masuk ke Google Cloud Console.

Buat project baru dan aktifkan Google Drive API di dalam library API.

Konfigurasikan layar persetujuan OAuth (OAuth Consent Screen) dan buat kredensial jenis OAuth Client ID serta API Key.

Salin string kredensial tersebut ke form konfigurasi Profil & Cloud API di dalam dasbor EduIPS Anda.
📂 Struktur Berkas Repositori
EduIPS/
├── index.html          # File tunggal utama berisi arsitektur HTML, CSS Custom, Layout SPA, dan core JavaScript logic
├── README.md           # Berkas dokumentasi teknis platform (berkas ini)
└── LICENSE             # Informasi lisensi hak cipta proyek

🤝 Kontribusi
Kontribusi untuk pengembangan komponen templat RPP-PM baru, optimalisasi generator evaluasi, atau perbaikan bug manipulasi DOM sangat terbuka lebar:

Fork Repositori ini.

Buat branch fitur baru (git checkout -b fitur/KomponenAdministrasiBaru).

Lakukan commit terhadap perubahan Anda (git commit -m 'Menambahkan Fitur Analisis Kriteria Baru').

Unggah branch ke repositori Anda (git push origin fitur/KomponenAdministrasiBaru).

Ajukan sebuah Pull Request ke repositori utama.

📄 Lisensi
Proyek ini dilisensikan di bawah MIT License - Silakan gunakan, modifikasi, dan distribusikan kembali untuk kemajuan dunia pendidikan Indonesia.

with open("README.md", "w", encoding="utf-8") as f:
f.write(readme_content)

print("File README.md successfully created with rich GitHub HTML structures.")

Langkah 2: Jalankan Berkas Utama
Opsi A (Penggunaan Cepat): Klik ganda berkas index.html langsung dari file manager komputer Anda untuk membukanya di peramban web pilihan Anda.

Opsi B (Rekomendasi Pengembang): Jalankan ekstensi Live Server di VS Code untuk mengaktifkan pemantauan kode berkala dengan alamat host lokal default http://127.0.0.1:5500
Langkah 3: Konfigurasi OAuth Google Cloud (Opsional)
Untuk mengaktifkan pencadangan otomatis Google Drive secara penuh pada tab Profil & Cloud API:

Masuk ke Google Cloud Console.

Buat project baru dan aktifkan Google Drive API di dalam library API.

Konfigurasikan layar persetujuan OAuth (OAuth Consent Screen) dan buat kredensial jenis OAuth Client ID serta API Key.

Salin string kredensial tersebut ke form konfigurasi Profil & Cloud API di dalam dasbor EduIPS Anda.

📂 Struktur Berkas Repositori
EduIPS/
├── index.html          # File tunggal utama berisi arsitektur HTML, CSS Custom, Layout SPA, dan core JavaScript logic
├── README.md           # Berkas dokumentasi teknis platform (berkas ini)
└── LICENSE             # Informasi lisensi hak cipta proyek
🤝 Kontribusi
Kontribusi untuk pengembangan komponen templat RPP-PM baru, optimalisasi generator evaluasi, atau perbaikan bug manipulasi DOM sangat terbuka lebar:

Fork Repositori ini.

Buat branch fitur baru (git checkout -b fitur/KomponenAdministrasiBaru).

Lakukan commit terhadap perubahan Anda (git commit -m 'Menambahkan Fitur Analisis Kriteria Baru').

Unggah branch ke repositori Anda (git push origin fitur/KomponenAdministrasiBaru).

Ajukan sebuah Pull Request ke repositori utama.

📄 Lisensi
Proyek ini dilisensikan di bawah MIT License - Silakan gunakan, modifikasi, dan distribusikan kembali untuk kemajuan dunia pendidikan Indonesia.




