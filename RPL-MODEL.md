# **Materi Presentasi: Model Pengembangan Perangkat Lunak & Studi Kasus Spiral**

## **1. Pendahuluan**
### **Apa itu Model Pengembangan Perangkat Lunak?**
Model pengembangan perangkat lunak adalah metode atau pendekatan sistematis yang digunakan untuk merancang, membangun, menguji, dan mengelola perangkat lunak agar efisien dan sesuai dengan kebutuhan pengguna. Model ini membantu pengembang dan pemangku kepentingan dalam memastikan perangkat lunak yang dibuat memiliki struktur yang jelas dan terorganisir.

### **Mengapa Model Pengembangan Perangkat Lunak Penting?**
- **Meningkatkan Efisiensi** – Mempermudah perencanaan dan pelaksanaan pengembangan perangkat lunak.
- **Mengurangi Risiko Kegagalan** – Setiap tahapan memiliki proses evaluasi yang dapat mendeteksi potensi masalah lebih awal.
- **Memastikan Kualitas Perangkat Lunak** – Dengan proses yang terstruktur, kualitas perangkat lunak lebih terjaga.
- **Fleksibilitas dalam Pengembangan** – Beberapa model memungkinkan perubahan kebutuhan dalam proses pengembangan.

## **2. Model Pengembangan Perangkat Lunak**
Berikut adalah beberapa model pengembangan perangkat lunak yang sering digunakan:

### **a. Waterfall Model**
#### **Pengertian**
Model Waterfall adalah pendekatan pengembangan perangkat lunak yang berurutan, di mana setiap tahap harus selesai sebelum tahap berikutnya dimulai.

#### **Tahapan**
1. **Analisis Kebutuhan** – Mengumpulkan semua kebutuhan pengguna sebelum mulai pengembangan.
2. **Desain Sistem** – Merancang arsitektur perangkat lunak berdasarkan kebutuhan yang dikumpulkan.
3. **Implementasi** – Pengkodean dilakukan berdasarkan desain yang telah dibuat.
4. **Pengujian** – Memastikan perangkat lunak berjalan sesuai spesifikasi dan tidak ada bug.
5. **Pemeliharaan** – Menyelesaikan masalah atau menyesuaikan perangkat lunak setelah rilis.

#### **Kelebihan**
✅ Mudah diterapkan untuk proyek kecil dan stabil.  
✅ Dokumentasi lengkap, memudahkan pemeliharaan.  
✅ Struktur kerja yang jelas dan mudah dikelola.  

#### **Kekurangan**
❌ Tidak fleksibel, sulit menangani perubahan setelah tahap awal selesai.  
❌ Jika ada kesalahan di tahap awal, biaya perbaikannya sangat tinggi.  

---

![17429555189973511364834407520621](https://github.com/user-attachments/assets/c0c2d40e-342c-484d-8eb0-fd506170794c)


### **3. Model Spiral (Pilihan untuk Studi Kasus)**
#### **Pengertian**
Model Spiral adalah pendekatan pengembangan perangkat lunak yang menggabungkan elemen dari model Waterfall dan Prototyping dengan fokus utama pada manajemen risiko dan iterasi bertahap. Model ini dirancang untuk menangani proyek yang kompleks dan dinamis, di mana kebutuhan sering berubah dan risiko harus dikelola dengan baik.

#### **Metode Model Spiral**
Model Spiral beroperasi dalam **siklus iteratif** yang terdiri dari empat fase utama. Setiap iterasi akan menghasilkan perangkat lunak yang lebih matang dan stabil.

1. **Tahap Perencanaan**
   - Mengidentifikasi kebutuhan sistem dan tujuan pengembangan.
   - Menyusun strategi dan menetapkan anggaran serta jadwal proyek.
   - Menentukan teknologi yang akan digunakan dan persyaratan fungsional serta non-fungsional.

2. **Tahap Identifikasi Risiko**
   - Menilai risiko teknis, operasional, dan bisnis dalam pengembangan perangkat lunak.
   - Mengembangkan strategi mitigasi risiko untuk mengurangi potensi kegagalan proyek.
   - Jika risiko tinggi terdeteksi, iterasi dapat diulang atau proyek diarahkan ulang.

3. **Tahap Pengembangan dan Pengujian**
   - Implementasi fitur atau modul secara bertahap.
   - Pengujian dilakukan setelah setiap iterasi untuk memastikan sistem stabil dan bebas bug.
   - Setiap iterasi menghasilkan peningkatan dari versi sebelumnya.

4. **Tahap Evaluasi dan Validasi**
   - Stakeholder (SuperAdmin, Asisten, Pembimbing, Praktikan) melakukan evaluasi terhadap hasil iterasi.
   - Jika ada perubahan atau masukan, sistem kembali ke tahap perencanaan sebelum iterasi baru dimulai.
   - Setelah beberapa iterasi, sistem akan lebih stabil dan siap untuk diterapkan secara penuh.

#### **Kelebihan Model Spiral**
✅ **Fleksibel dan Adaptif** – Cocok untuk proyek yang berkembang dengan perubahan kebutuhan secara dinamis.  
✅ **Manajemen Risiko yang Kuat** – Risiko dievaluasi di setiap tahap sehingga dapat diminimalkan sebelum proyek berkembang lebih jauh.  
✅ **Peningkatan Bertahap** – Setiap iterasi menghasilkan sistem yang lebih matang dan stabil.  
✅ **Keterlibatan Stakeholder** – Stakeholder dapat memberikan umpan balik di setiap tahap, memastikan sistem sesuai dengan kebutuhan pengguna.  
✅ **Cocok untuk Proyek Besar dan Kompleks** – Dapat menangani banyak fitur dan pemangku kepentingan secara efisien.  

#### **Kekurangan Model Spiral**
❌ **Biaya Lebih Tinggi** – Dibandingkan dengan model lain, Spiral membutuhkan lebih banyak sumber daya karena adanya evaluasi dan revisi terus-menerus.  
❌ **Memakan Waktu Lebih Lama** – Proses iteratif yang berulang membuat proyek berjalan lebih lama dibandingkan model linear seperti Waterfall.  
❌ **Membutuhkan Keahlian Tinggi** – Tim pengembang harus memiliki keterampilan dalam manajemen risiko dan pengambilan keputusan strategis.  

---

## **4. Studi Kasus Digitalisasi Praktikum Teknik Sipil dengan Model Spiral**
Sistem digitalisasi Praktikum Teknik Sipil membutuhkan model yang dapat menangani banyak stakeholder serta fitur yang terus berkembang. Model Spiral dipilih karena kemampuannya dalam **mengakomodasi perubahan, mengelola risiko, dan menghasilkan sistem yang lebih stabil melalui evaluasi berulang**.

### **Implementasi Model Spiral dalam Studi Kasus**
1. **Tahap Perencanaan**
   - Menganalisis kebutuhan praktikan, asisten, pembimbing, dan SuperAdmin.
   - Menentukan fitur utama: registrasi, verifikasi pembayaran, penjadwalan, asistensi, chat, video call, laporan nilai.
   - Menyusun roadmap pengembangan fitur secara bertahap.

2. **Tahap Identifikasi Risiko**
   - **Skalabilitas Sistem** → Apakah server bisa menangani banyak pengguna?
   - **Keamanan Data** → Bagaimana mencegah kebocoran data akademik?
   - **Stabilitas Fitur Real-time** → Apakah chat dan video call berjalan lancar?
   - **Integrasi Modul** → Bagaimana memastikan semua fitur berjalan tanpa konflik?

3. **Tahap Pengembangan dan Pengujian**
   - **Iterasi 1**: Pengembangan fitur inti (registrasi, login, dashboard admin).
   - **Iterasi 2**: Implementasi jadwal dan verifikasi pembayaran.
   - **Iterasi 3**: Pengujian chat & video call real-time.
   - **Iterasi 4**: Pengolahan laporan nilai dan finalisasi sistem.

4. **Tahap Evaluasi dan Validasi**
   - Setiap iterasi diuji oleh stakeholder untuk mendapatkan umpan balik.
   - Jika ada revisi atau tambahan fitur, sistem kembali ke tahap perencanaan.
   - Setelah beberapa iterasi, sistem siap diluncurkan secara penuh.

## **5. Kesimpulan**
Model Spiral adalah pilihan terbaik untuk digitalisasi praktikum Teknik Sipil karena mampu:
- **Menyesuaikan dengan kebutuhan yang terus berkembang**.
- **Mengidentifikasi dan mengurangi risiko sebelum proyek berkembang lebih jauh**.
- **Menghasilkan sistem yang lebih matang dan stabil melalui evaluasi bertahap**.

## **6. Referensi**
- Google Scholar: https://scholar.google.com/scholar?q=spiral+model+software+development
- Jurnal: https://jurnal.polgan.ac.id/index.php/remik/article/view/11523/995

