<p align="center">
  <img src="https://img.shields.io/badge/EduIPS%20v2026-Portal%20Administrasi%20Guru%20IPS-1e40af?style=for-the-badge&logo=education&logoColor=white" alt="EduIPS Header Banner" width="100%" />
</p>

<h1 align="center">🌍 EduIPS (Portal Administrasi Guru IPS Profesional)</h1>

<p align="center">
  <a href="https://tailwindcss.com/"><img src="https://img.shields.io/badge/UI_Framework-Tailwind_CSS_v3.x-38bdf8?style=flat-square&logo=tailwind-css&logoColor=white" alt="Tailwind CSS" /></a>
  <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript"><img src="https://img.shields.io/badge/Language-Vanilla_JS_ES6+-f7df1e?style=flat-square&logo=javascript&logoColor=black" alt="JavaScript" /></a>
  <a href="https://developers.google.com/drive"><img src="https://img.shields.io/badge/Cloud_Integration-Google_Drive_API-34a853?style=flat-square&logo=google-drive&logoColor=white" alt="Google Drive API" /></a>
  <a href="https://github.com/cure53/DOMPurify"><img src="https://img.shields.io/badge/Security-DOMPurify_Protected-ea4335?style=flat-square&logo=securityscorecard&logoColor=white" alt="DOMPurify" /></a>
  <a href="https://github.com/markedjs/marked"><img src="https://img.shields.io/badge/Parser-Marked.js-bb86fc?style=flat-square&logo=markdown&logoColor=white" alt="Marked.js" /></a>
</p>

<br />

<p align="center">
  <strong>EduIPS</strong> ialah sebuah platform portal pentadbiran digital tulen dari sisi klien (<i>pure client-side portal</i>) yang direka khas untuk memenuhi keperluan tugasan pengurusan dokumentasi Guru Ilmu Pengetahuan Sosial (IPS) peringkat SMP/MTs (Fase D). Aplikasi ini mengautomasikan penyusunan dokumen rancangan pengajaran berstandard kualiti <b>RPP-PM (Rencana Pelaksanaan Pembelajaran - Pendalaman Materi) v2026</b> serta instrumen penilaian berfikir aras tinggi secara instan terus ke storan awan (cloud storage) peribadi anda.
</p>

<p align="center">
  Aplikasi ini dibangunkan dalam seni bina <i>Single Page Application (SPA)</i> berasaskan fail tunggal yang sangat ringan, responsif dan sedia cetak mengikut piawaian rasmi.
</p>

---

## 🛠️ Seni Bina & Spesifikasi Teknikal

Platform ini menggunakan pendekatan **Zero-Build Stack**, yang bermaksud ia memberikan kelajuan pelaksanaan maksimum tanpa memerlukan sebarang proses kompilasi web yang berat atau pemasangan perisian pelayan (runtime server) luaran:

<table width="100%">
  <thead>
    <tr>
      <th width="30%" align="left">Komponen Utama</th>
      <th width="70%" align="left">Teknologi & Pustaka (Libraries)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><b>Reka Bentuk Antaramuka (UI)</b></td>
      <td>Tailwind CSS (v3.x) melalui talian sistem CDN dengan konfigurasi tema warna korporat institusi yang tersuai (Primary, Secondary, Accent, Success, Danger).</td>
    </tr>
    <tr>
      <td><b>Ikonografi</b></td>
      <td>FontAwesome v6.4.0 untuk menyediakan penanda visual yang lengkap dan jelas pada menu navigasi utama.</td>
    </tr>
    <tr>
      <td><b>Enjin Dokumen</b></td>
      <td>Marked.js sebagai komponen penukar (Markdown parser) terpantas untuk menukarkan draf teks berstruktur kepada format HTML sedia cetak.</td>
    </tr>
    <tr>
      <td><b>Sistem Keselamatan DOM</b></td>
      <td>DOMPurify v3.0.6 bertindak menapis dan membersihkan sebarang elemen HTML berbahaya hasil parsing, memberikan perlindungan mutlak daripada ancaman Cross-Site Scripting (XSS).</td>
    </tr>
    <tr>
      <td><b>Logika Aplikasi</b></td>
      <td>Vanilla JavaScript (ES6+) tulen digunakan untuk menguruskan pertukaran halaman (SPA Switching melalui dataset target), interaksi komponen, penyegerakan storan lokal (local storage), serta integrasi API awan.</td>
    </tr>
  </tbody>
</table>

---

## 🚀 Ciri-Ciri Utama & Pembagian Modul

Sistem pentadbiran di dalam EduIPS dibahagikan kepada 4 pilar utama yang dikemas rapi di dalam sistem navigasi menu sisi (sidebar) yang responsif:

### 1. Pentadbiran Perancangan (Perangkat Ajar)
<details>
<summary><b>📐 Klik untuk lihat butiran Modul Perancangan</b></summary>
<br>
<ul>
  <li><b>Modul Ajar (RPP-PM):</b> Penjana dokumen perancangan automatik berdasarkan tetapan parameter dinamik:
    <ul>
      <li>Pilihan Fase & Kelas (Fase D - Kelas VII, VIII, IX).</li>
      <li>Pembahagian Tema Pembelajaran IPS Terpiawai (Geografi, Sejarah, Ekonomi, Sosiologi, atau IPS Terpadu merentasi tema).</li>
      <li>Input tersuai bagi Materi Pokok / Sub Topik serta peruntukan Alokasi Waktu.</li>
      <li>Pilihan pelbagai bagi 8 Dimensi Profil Lulusan (Beriman & Bertakwa, Berkebhinekaan Global, Bergotong Royong, Mandiri, Bernalar Kritis, Kreatif, Literasi, Numerasi).</li>
    </ul>
  </li>
  <li><b>Prota & Prosem (Program Tahunan & Semester):</b> Menyusun pembahagian peruntukan Jam Pelajaran (JP) tahunan (secara lalai ditetapkan sebanyak 144 JP) mengikut fokus bab perbincangan secara automatik.</li>
</ul>
</details>

### 2. Pentadbiran Pelaksanaan Kelas
<details>
<summary><b>📝 Klik untuk lihat butiran Modul Pelaksanaan</b></summary>
<br>
<ul>
  <li><b>Jurnal Agenda Guru:</b> Merekodkan log aktiviti harian bagi sesi pengajaran di dalam kelas, tahap pencapaian topik penting, serta nota mengenai kekangan yang dihadapi di lapangan.</li>
  <li><b>Presensi & Bimbingan (BK):</b> Menguruskan rekod kehadiran harian murid di samping menyediakan log bimbingan kaunseling ringkas untuk tindakan pantas bagi menyelesaikan masalah pembelajaran murid.</li>
</ul>
</details>

### 3. Pentadbiran Evaluasi & Asesmen
<details>
<summary><b>📊 Klik untuk lihat butiran Modul Evaluasi</b></summary>
<br>
<ul>
  <li><b>Kisi-kisi & Soal TKA (Tes Kemampuan Akademik):</b> Menyusun instrumen penilaian kognitif berasaskan kemahiran berfikir aras tinggi (HOTS) yang dikonfigurasikan agar bebas daripada corak teks yang terlalu panjang.</li>
  <li><b>Nilai & Analisis Remedial:</b> Modul kemasukan markah hasil pembelajaran yang dilengkapi dengan fungsi analisis automatik untuk mengenal pasti murid yang memerlukan program pemulihan (remedial) atau pengayaan.</li>
  <li><b>Bahan Ajar & Rubrik:</b> Menyediakan pengkalan data bahan bantu mengajar serta helaian kriteria rubrik penilaian prestasi murid.</li>
</ul>
</details>

### 4. Pentadbiran Sokongan Wali Kelas
<details>
<summary><b>🪑 Klik untuk lihat butiran Modul Sokongan</b></summary>
<br>
<ul>
  <li><b>Denah Kelas Pintar:</b> Ciri visual interaktif bagi susun atur kedudukan tempat duduk murid untuk mengoptimumkan kawalan suasana bilik darjah.</li>
  <li><b>Buku Mutasi & Log Siswa:</b> Pengurusan pangkalan data profil murid yang lengkap dengan keupayaan memuat naik atau mengimport data secara pukal daripada format spreadsheet luaran.</li>
</ul>
</details>

---

## 🔐 Mod Akses & Pengurusan Sesi

Aplikasi menyediakan dua pilihan gerbang masuk (*Login Gate*) untuk fleksibiliti tugasan harian guru:
1. **Masuk & Sinkronkan Drive (Google Workspace):** Menggunakan perkhidmatan *Google Identity Services* untuk proses log masuk pengguna yang selamat, memaparkan penunjuk status *Workspace Active*, dan mengaktifkan integrasi Google Drive API secara langsung untuk tujuan sandaran fail automatik.
2. **Masuk Tanpa Akun (Sesi Lokal):** Menggunakan sistem enkapsulasi storan lokal pelayar web (*Local Storage*) pada peranti anda. Mod awanama (anonim) ini dijamin selamat sepenuhnya kerana data tidak akan dihantar ke mana-mana pelayan luaran.

---

## 🖨️ Piawaian Cetakan Rasmi (Paper Preview Setup)

Helaian output dokumen pratonton direka bentuk dengan visualisasi **Paper Preview Layout** yang mengikut nisbah dimensi tepat kertas rasmi **A4** (Lebar: `210mm`, Tinggi Minimum: `297mm`). Tetapan tipografi bawaan menggunakan fon rasmi *Times New Roman* dengan saiz kandungan teks `11pt`, susunan teks rata kiri-kanan (*justify*), serta garisan sempadan jadual yang jelas (`#111827`).

### 💡 Panduan Eksport ke PDF / Cetakan Fizikal:
1. Klik butang **Cetak / PDF** yang terdapat pada bahagian menu pratonton dokumen.
2. Pada tetingkap sistem cetakan (print dialog) pelayar web anda:
   * Tetapkan **Destinasi / Destination** kepada **Simpan sebagai PDF (Save as PDF)** atau pilih mesin pencetak fizikal anda.
   * Pastikan pilihan **Ukuran Kertas (Paper Size)** ditetapkan kepada **A4**.
   * Laraskan bahagian **Margin** kepada pilihan **None** atau **Default**.
   * **Wajib** menandakan (tick) pada pilihan **Grafik Latar Belakang (Background Graphics)** supaya kesan warna pada bahagian atas jadual (`#f3f4f6`) dan warna tema dokumen dapat dicetak dengan sempurna.

---

## 🚀 Panduan Pemasangan Lokal

Disebabkan platform ini beroperasi sepenuhnya pada sisi klien (client-side), proses pemasangan adalah sangat mudah:

### Langkah 1: Klon Repositori
```bash
git clone [https://github.com/USERNAME_ANDA/EduIPS.git](https://github.com/USERNAME_ANDA/EduIPS.git)
cd EduIPS

Langkah 2: Jalankan Fail Utama
Pilihan A (Penggunaan Pantas): Klik dua kali pada fail index.html secara terus melalui pengurus fail komputer anda untuk membukanya di pelayar web pilihan anda.

Pilihan B (Syor Pembangun): Jalankan sambungan (extension) Live Server di dalam VS Code untuk membolehkan pemantauan kod secara masa nyata dengan alamat host tempatan lalai http://127.0.0.1:5500.

Langkah 3: Konfigurasi OAuth Google Cloud (Opsional)
Untuk mengaktifkan fungsi sandaran automatik ke Google Drive pada tab Profil & Cloud API:

Log masuk ke talian Google Cloud Console.

Bina sebuah projek baharu dan aktifkan fungsi Google Drive API di dalam perpustakaan API (API Library).

Konfigurasikan paparan kebenaran OAuth (OAuth Consent Screen) dan bina maklumat kelayakan bagi jenis OAuth Client ID serta API Key.

Salin rentetan maklumat kelayakan tersebut ke dalam borang konfigurasi Profil & Cloud API di dalam papan pemuka EduIPS anda.

📂 Struktur Fail Repositori
EduIPS/
├── index.html          # Fail utama tunggal mengandungi kod HTML, CSS Kustom, Reka Letak SPA dan logik JavaScript
├── README.md           # Fail dokumentasi teknikal platform (fail ini)
└── LICENSE             # Maklumat lesen hak cipta projek

🤝 Sumbangan (Contribution)
Sumbangan untuk pembangunan komponen templat RPP-PM baharu, pengoptimuman fungsi penjana penilaian, atau pembaikan pepijat (bug) pada manipulasi DOM amat dialu-alukan:

Fork Repositori ini.

Bina branch ciri baharu (git checkout -b ciri/KomponenPentadbiranBaharu).

Lakukan commit terhadap perubahan kod anda (git commit -m 'Menambah Ciri Analisis Kriteria Baharu').

Muat naik branch tersebut ke repositori anda (git push origin ciri/KomponenPentadbiranBaharu).

Ajukan permohonan Pull Request ke repositori utama.

📄 Lesensi
Projek ini dilesenkan di bawah syarat MIT License - Anda dibenarkan untuk mengguna, mengubah ubah, dan mengedarkan semula kod ini demi kemajuan dunia pendidikan.

🛠️ Cara Memasukkannya ke GitHub:
Buka repositori projek EduIPS di laman GitHub anda.

Klik butang Add file -> Pilih Create new file.

Letakkan nama fail sebagai README.md (pastikan guna huruf besar sepenuhnya).

Paste (tampal) keseluruhan kandungan teks di dalam kotak kod di atas.

Skrol ke bawah halaman, masukkan mesej commit anda, dan klik butang Commit changes.... Fail anda kini sedia dipaparkan dengan susunan HTML yang sangat cantik!
