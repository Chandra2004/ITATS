# 🎓 Alur Praktikum Teknik Sipil: Dari Manual ke Digital

## 🛠 Tech Stack

### 1️⃣ Backend
- **Bahasa Pemrograman**: PHP Native  
- **Database**: MySQL  
- **Authentication**: PHP Sessions & JWT  
- **File Upload & Storage**: Google Drive / Storage Lokal  

### 2️⃣ Frontend
- **Framework**: React.js  
- **CSS Framework**: Tailwind CSS  
- **State Management**: Redux  

### 3️⃣ Deployment
- **Hosting**: VPS dengan Apache atau Nginx  
- **Web Server**: Apache/Nginx  
- **CI/CD**: GitHub Actions (Opsional)  

### 4️⃣ Fitur Realtime (Chat & Meeting)
- **Chat Realtime**: WebSockets menggunakan PHP Ratchet  
- **Video Call**: WebRTC  

---

## 📌 Tahapan Pengembangan

### 📝 1. Perencanaan & Persiapan
- Menentukan cakupan utama aplikasi (fitur minimal yang harus tersedia).
- Merancang database (ERD) berdasarkan alur yang telah dibuat.
- Membuat wireframe UI untuk setiap peran pengguna.

### 🚀 2. Setup Proyek
- Membuat repository Git (GitHub/GitLab/Bitbucket).
- Mengatur PHP dan MySQL di lingkungan pengembangan lokal.
- Mengonfigurasi autentikasi berbasis sesi atau JWT.
- Mengatur frontend menggunakan React.js.

### 🏗 3. Pengembangan Backend (PHP Native)
Membuat modul untuk:
- **User Management** (SuperAdmin, Pembimbing, Asisten, Praktikan).
- **Praktikum Management** (Ilmu Ukur Tanah, Teknologi Beton, dll.).
- **Kelompok Praktikum**.
- **Penjadwalan**.
- **Pembayaran**.
- **Laporan & Penilaian**.
- **Asistensi**.

Mengimplementasikan fitur utama:
- **Registrasi & Login (PHP Sessions/JWT)**.
- **Role-Based Access Control (RBAC)**.
- **Verifikasi Pembayaran**.
- **Penjadwalan & Pembagian Kelompok**.
- **Sistem Asistensi Bertahap**.
- **Pengumpulan Laporan & Penilaian**.

### 🎨 4. Pengembangan Frontend
- Mendesain UI dengan Tailwind CSS.
- Mengembangkan dashboard untuk setiap peran.
- Menghubungkan frontend ke backend melalui REST API.

### 🔄 5. Implementasi Fitur Realtime
- Menambahkan **chat realtime** menggunakan WebSockets dengan PHP Ratchet.
- Menggunakan **WebRTC** untuk fitur video call.

### 🛠 6. Pengujian & Debugging
- Uji coba fitur utama.
- Debugging menggunakan error logging di PHP (error_log, Xdebug).

### 🚀 7. Deployment & Maintenance
- Deploy backend ke VPS dengan **Apache/Nginx**.
- Deploy frontend ke **Netlify/Vercel** atau ke server yang sama.
- Monitoring menggunakan **Monolog** atau **Sentry**.

---

## 🔥 Struktur Peran dalam Praktikum Teknik Sipil

| Peran       | Deskripsi |
|-------------|-------------------------------------------------|
| **SuperAdmin** | Kepala Lab (Kalab) dengan akses penuh ke sistem |
| **Pembimbing** | Dosen Pembimbing (Dospem) yang menilai praktikan |
| **Asisten** | Asisten Lab (Aslab) yang mengatur jadwal & kelompok |
| **Praktikan** | Peserta yang mengikuti praktikum |

---

## 🏆 Alur Praktikum Teknik Sipil

1️⃣ **Registrasi**  
   - Praktikan mengisi profil (foto, nama, NPM, telepon, email, password).  
   - SuperAdmin tidak perlu registrasi.  
   - Asisten didaftarkan oleh SuperAdmin.  

2️⃣ **Login**  
   - Semua peran masuk menggunakan form login berbasis **PHP Sessions/JWT**.  

3️⃣ **Verifikasi Pembayaran**  
   - Praktikan mengunggah **bukti pembayaran** dan menunggu validasi dari SuperAdmin/Asisten.  

4️⃣ **Pemilihan Modul Praktikum**  
   - Praktikan memilih modul praktikum dan menunggu persetujuan SuperAdmin/Asisten.  

5️⃣ **Pemilihan Pembimbing & Asisten**  
   - Praktikan dapat mengajukan preferensi pembimbing dan asisten.  
   - SuperAdmin memiliki wewenang untuk menolak atau mengganti pilihan.  

6️⃣ **Pembentukan Kelompok**  
   - Praktikan memilih kelompok (3-5 orang) atau ditempatkan oleh Asisten.  

7️⃣ **Distribusi Modul Praktikum**  
   - Asisten membagikan modul dalam bentuk **buku fisik atau e-book**.  

8️⃣ **Pengecekan Data Diri**  
   - Praktikan memastikan semua data sudah benar sebelum pelaksanaan praktikum.  

9️⃣ **Penjadwalan Praktikum**  
   - SuperAdmin dan Asisten menetapkan jadwal praktikum.  

🔟 **Pelaksanaan Praktikum**  
   - Praktikan **absen** sebelum memulai praktikum.  
   - Setelah selesai, praktikan mengisi **form laporan hasil pengujian**.  

1️⃣1️⃣ **Asistensi**  
   - Asistensi harus dilakukan secara bertahap: **Asisten → SuperAdmin → Pembimbing**.  
   - Jika laporan belum disetujui, harus direvisi sebelum lanjut ke tahap berikutnya.  

1️⃣2️⃣ **Penilaian Laporan**  
   - **SuperAdmin**: 40%  
   - **Pembimbing**: 60%  
   - Jika laporan tidak disetujui SuperAdmin, maka tidak bisa dinilai oleh Pembimbing.  

1️⃣3️⃣ **Penyelesaian Praktikum**  
   - Setelah modul selesai, praktikan dapat mendaftar untuk modul lain.  
   - Mahasiswa dengan nilai di bawah standar wajib mengulang praktikum.  

---

## 📌 Fitur Tambahan
✅ **Chat Realtime**: Komunikasi langsung antara peserta dan pembimbing.  
✅ **Video Call (Meeting)**: Fitur WebRTC untuk diskusi online.  
✅ **Form Builder**: SuperAdmin dan Asisten dapat membuat formulir digital.  

---

## 🏫 Daftar Praktikum Berdasarkan Semester

| No | Praktikum               | Semester | Jenis Pengujian |
|----|-------------------------|----------|----------------|
| 1  | Ilmu Ukur Tanah         | 1        | Praktik, Tertulis, Laporan |
| 2  | Teknologi Beton         | 1        | Praktik, Tertulis, Laporan |
| 3  | Kimia I                 | 1        | Praktik, Tertulis, Laporan |
| 4  | Kimia II                | 2        | Praktik, Tertulis, Laporan |
| 5  | Mekanika Tanah I        | 3        | Praktik, Tertulis, Laporan |
| 6  | Fisika                  | 3        | Praktik, Tertulis, Laporan |
| 7  | Mekanika Tanah II       | 4        | Praktik, Tertulis, Laporan |
| 8  | Hidrolika               | 5        | Praktik, Tertulis, Laporan |
| 9  | Bahan Jalan             | 6        | Praktik, Tertulis, Laporan |

---  
