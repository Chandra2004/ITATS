---

# **Alur Praktikum Teknik Sipil: Dari Manual ke Digital**  

## **Tech Stack**  

### **1. Backend**  
- **Bahasa Pemrograman**: PHP Native  
- **Database**: MySQL  
- **Authentication**: PHP Sessions & JWT  
- **File Upload & Storage**: Google Drive / Storage Lokal  

### **2. Frontend**  
- **Framework**: React.js  
- **CSS Framework**: Tailwind CSS  
- **State Management**: Redux  

### **3. Deployment**  
- **Hosting**: VPS dengan Apache atau Nginx  
- **Web Server**: Apache/Nginx  
- **CI/CD**: GitHub Actions (Opsional)  

### **4. Fitur Realtime (Chat & Meeting)**  
- **Chat Realtime**: WebSockets menggunakan PHP Ratchet  
- **Video Call**: WebRTC  

---

## **Tahapan Pengembangan**  

### **1. Perencanaan & Persiapan**  
- Menentukan cakupan utama aplikasi (fitur minimal yang harus tersedia).  
- Merancang database (ERD) berdasarkan alur yang telah dibuat.  
- Membuat wireframe UI untuk setiap peran pengguna.  

### **2. Setup Proyek**  
- Membuat repository Git (GitHub/GitLab/Bitbucket).  
- Mengatur PHP dan MySQL di lingkungan pengembangan lokal.  
- Mengonfigurasi autentikasi berbasis sesi atau JWT.  
- Mengatur frontend menggunakan React.js (jika menggunakan pendekatan SPA).  

### **3. Pengembangan Backend (PHP Native)**  
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

### **4. Pengembangan Frontend**  
- Mendesain antarmuka pengguna untuk setiap peran dengan Tailwind CSS.  
- Mengembangkan dashboard sesuai peran pengguna.  
- Mengintegrasikan frontend dengan backend melalui REST API berbasis PHP.  

### **5. Implementasi Fitur Realtime**  
- Menambahkan fitur chat realtime menggunakan WebSockets dengan PHP Ratchet.  
- Mengimplementasikan fitur video call menggunakan WebRTC.  

### **6. Pengujian & Debugging**  
- Melakukan uji coba terhadap fitur utama.  
- Melakukan debugging menggunakan error logging di PHP (error_log, Xdebug).  

### **7. Deployment & Maintenance**  
- Mendeploy backend ke VPS dengan Apache atau Nginx.  
- Mendeploy frontend ke Netlify/Vercel atau ke server yang sama.  
- Melakukan monitoring dengan tools seperti Monolog atau Sentry.  

---

## **Struktur Peran dalam Praktikum Teknik Sipil**  
1. **SuperAdmin** (Kepala Laboratorium – Kalab)  
   - Memiliki akses penuh ke seluruh sistem.  
   - Bertanggung jawab atas pengelolaan praktikum dan dosen pembimbing.  
2. **Pembimbing** (Dosen Pembimbing – Dospem)  
   - Bertanggung jawab terhadap mahasiswa yang melakukan praktikum.  
   - Memberikan penilaian dan asistensi kepada praktikan.  
3. **Asisten** (Asisten Laboratorium – Aslab)  
   - Mengatur jadwal, kelompok, serta membantu dalam pelaksanaan praktikum.  
4. **Praktikan**  
   - Peserta yang mengikuti praktikum sesuai dengan ketentuan yang telah ditetapkan.  

---

## **Alur Praktikum Teknik Sipil**  

1. **Registrasi**  
   - Praktikan melakukan registrasi dengan mengisi profil (foto, nama, NPM, telepon, email, password).  
   - SuperAdmin memiliki akses langsung tanpa perlu registrasi.  
   - Pendaftaran Asisten dilakukan melalui dashboard SuperAdmin.  

2. **Login**  
   - Semua peran dapat mengakses sistem melalui form login berbasis PHP Sessions atau JWT.  

3. **Verifikasi Pembayaran**  
   - Praktikan mengunggah bukti pembayaran dan mengisi formulir verifikasi.  
   - SuperAdmin atau Asisten akan melakukan validasi sebelum melanjutkan ke tahap berikutnya.  

4. **Pemilihan Modul Praktikum**  
   - Praktikan memilih modul praktikum yang diinginkan.  
   - Menunggu persetujuan dari SuperAdmin atau Asisten.  

5. **Pemilihan Dosen Pembimbing & Asisten**  
   - Praktikan dapat mengajukan preferensi pembimbing dan asisten.  
   - SuperAdmin memiliki kewenangan untuk menolak atau menggantikan pilihan tersebut.  

6. **Pembentukan Kelompok**  
   - Praktikan dapat memilih kelompok (3-5 orang) yang telah disediakan Asisten.  
   - Jika belum memiliki kelompok, Asisten dapat menetapkan kelompok bagi praktikan.  

7. **Distribusi Modul Praktikum**  
   - Asisten membagikan modul dalam bentuk buku fisik atau e-book.  

8. **Pengecekan Data Diri**  
   - Praktikan memastikan semua data telah terisi dengan benar sebelum pelaksanaan praktikum.  

9. **Penjadwalan Praktikum**  
   - SuperAdmin menetapkan jadwal praktikum sesuai dengan modul yang tersedia.  
   - Asisten membuat jadwal praktikum berdasarkan ketersediaan laboratorium.  

10. **Pelaksanaan Praktikum**  
    - Praktikan melakukan absensi sebelum mengikuti praktikum (bisa dengan bukti foto).  
    - Setelah praktikum, praktikan mengisi formulir laporan hasil pengujian.  

11. **Asistensi**  
    - Praktikan melakukan asistensi secara bertahap melalui Asisten → SuperAdmin → Pembimbing.  
    - Jika laporan belum disetujui, harus dilakukan revisi sebelum melanjutkan ke tahap berikutnya.  

12. **Penilaian Laporan**  
    - Penilaian berdasarkan bobot:  
      - **SuperAdmin**: 40%  
      - **Pembimbing**: 60%  
    - Jika laporan belum disetujui SuperAdmin, maka tidak dapat dinilai oleh Pembimbing.  

13. **Penyelesaian Praktikum**  
    - Setelah modul selesai, praktikan dapat mendaftar untuk modul lainnya.  
    - Mahasiswa dengan nilai di bawah standar diwajibkan mengulang praktikum sesuai semester yang diampu.  

---

## **Fitur Tambahan**  
- **Chat Realtime**: Komunikasi langsung antara peserta dan pembimbing dengan PHP WebSockets (Ratchet).  
- **Video Call (Meeting)**: Fitur WebRTC untuk diskusi online.  
- **Form Builder**: SuperAdmin dan Asisten dapat membuat dan membagikan formulir yang bisa diisi oleh praktikan.  

---

## **Daftar Praktikum Berdasarkan Semester**  

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
