### **Judul Artikel:**

**AIOS: LLM Agent Operating System**

### **Penulis:**

Qingqing Ai, Jiaqi Han, Zhaorun Chen, Penghao Wang, Jianing Chen, Yuxiang Chen, Zhen Wang, Yaliang Li, Bolin Ding, dan Jingren Zhou

### **Tahun Terbit:**

2025 – Conference on Language Modeling (COLM 2025)

---

## **1. Latar Belakang Penelitian**

Sekarang ini, model bahasa besar atau **LLM (Large Language Model)** seperti GPT, Llama, dan Mistral sudah makin canggih. Dari situ lahirlah banyak **AI agent**, yaitu program yang bisa berpikir dan bertindak otomatis — contohnya membantu menulis kode, menjawab pertanyaan, atau menjalankan tugas tertentu.

Masalahnya, makin banyak agen yang dibuat, makin besar juga beban sistemnya. Framework seperti **LangChain**, **AutoGen**, dan **MetaGPT** memang bisa jalan, tapi belum efisien kalau dijalankan dalam jumlah besar.
Beberapa masalah yang muncul:

* Penggunaan GPU dan memori yang boros,
* Sistem jadi lambat kalau banyak agen aktif,
* Tidak ada pengaturan sumber daya yang jelas,
* Kadang bisa crash karena agen saling rebutan akses.

Dari situ muncul ide: kalau komputer punya sistem operasi (kayak Windows atau Linux) yang bisa ngatur aplikasi dan hardware, kenapa agen AI tidak dibuatkan “sistem operasi” juga?
Nah, konsep itulah yang melahirkan penelitian **AIOS — LLM Agent Operating System.**

---

## **2. Rumusan Masalah**

Masalah utama yang dibahas penulis adalah:

1. Bagaimana cara mengatur sumber daya (GPU, memori, API, LLM) biar efisien saat banyak agen berjalan?
2. Bagaimana memastikan tiap agen bisa jalan bersamaan tanpa saling ganggu atau rebutan?
3. Bagaimana menjaga agar sistem tetap cepat, aman, dan stabil saat ribuan agen dijalankan?

---

## **3. Tujuan Penelitian**

Tujuan penelitian ini yaitu untuk:

1. Membuat **sistem operasi khusus** untuk agen-agen berbasis LLM agar bisa dikelola secara terpusat dan efisien.
2. Mengembangkan **kernel AIOS**, yaitu bagian utama sistem yang ngatur proses, memori, penyimpanan, dan keamanan antar agen.
3. Menyediakan **SDK (Software Development Kit)** supaya pengembang bisa bikin agen dengan lebih gampang tanpa harus ribet mikirin hardware.
4. Menguji seberapa cepat dan efisien sistem ini dibanding framework biasa.

---

## **4. Solusi yang Ditawarkan (Metodologi Penelitian)**

Penulis membuat arsitektur AIOS yang terdiri dari **tiga lapisan utama**:

### a. **Application Layer**

Ini bagian paling atas, tempat agen-agen AI dijalankan.
Agen di layer ini nggak berhubungan langsung dengan GPU atau LLM, tapi lewat **AIOS SDK**.
SDK ini berfungsi seperti jembatan antara agen dan sistem utama, serta mendukung framework populer seperti ReAct, Reflexion, Autogen, Open-Interpreter, dan MetaGPT.

### b. **Kernel Layer**

Ini inti dari AIOS — ibaratnya “otak” yang ngatur semua sumber daya.
Ada beberapa komponen penting:

1. **Scheduler:** ngatur giliran agen mana yang dijalankan duluan biar semua dapat waktu yang adil (pakai metode FIFO dan Round Robin).
2. **Context Manager:** bisa *pause* dan *resume* proses LLM tanpa kehilangan hasil, mirip kayak fitur “save progress”.
3. **Memory Manager:** ngatur memori biar nggak penuh dengan data lama, pakai sistem *LRU-K* untuk buang data yang jarang dipakai.
4. **Storage Manager:** menyimpan data penting ke penyimpanan permanen atau database vektor seperti ChromaDB.
5. **Tool Manager:** ngatur penggunaan alat atau API biar nggak tabrakan antar agen.
6. **Access Manager:** ngatur izin akses antar agen biar aman dan nggak saling ganggu.

Semua aktivitas agen diterjemahkan jadi *system call* seperti `LLM Syscall`, `Memory Syscall`, atau `Tool Syscall`, lalu diatur oleh kernel agar eksekusinya efisien dan aman.

### c. **Hardware Layer**

Bagian paling bawah, yaitu perangkat keras seperti CPU, GPU, RAM, dan storage.
AIOS nggak langsung ngatur hardware, tapi lewat OS utama seperti Linux.

---

## **5. Hasil Penelitian**

Penulis menguji AIOS pakai beberapa benchmark, yaitu:

* **HumanEval** → mengetes kemampuan menulis kode,
* **MINT** → tugas interaksi multi-tahap,
* **GAIA** → tugas yang melibatkan penggunaan alat,
* **SWE-Bench-Lite** → debugging dan pengujian software.

**Model yang dipakai:** GPT-4o-mini, Llama-3.1-8b, dan Mistral-7b
**Lingkungan uji:** GPU NVIDIA RTX A5000 (24GB)
**Jumlah agen:** hingga 2000 agen dijalankan bersamaan

### Hasil yang didapat:

1. **Performa meningkat:**
   AIOS mempertahankan bahkan meningkatkan *success rate* agen di semua benchmark, terutama GAIA.

2. **Efisiensi tinggi:**

   * Throughput meningkat sampai **2,1 kali lipat** dibanding framework biasa.
   * *Latency* (waktu respon) berkurang cukup besar.

3. **Skalabilitas bagus:**
   AIOS tetap stabil bahkan saat **2000 agen** aktif bersamaan, tanpa crash dan dengan penggunaan sumber daya yang lebih hemat.

4. **Manajemen sumber daya efisien:**
   AIOS berhasil mengatur penggunaan GPU dan memori dengan stabil, sehingga sistem bisa tetap cepat dan aman.

---

## **6. Kesimpulan**

Secara sederhana, AIOS adalah **“sistem operasi untuk agen AI”**.
Kalau Windows mengatur aplikasi komputer, maka AIOS mengatur agen-agen berbasis LLM.

Melalui arsitektur tiga lapisan dan kernel yang lengkap, AIOS:

* Membuat sistem multi-agen jadi lebih cepat dan efisien,
* Menghemat sumber daya GPU dan memori,
* Menjamin keamanan antar agen,
* Dan bisa menampung ribuan agen sekaligus tanpa penurunan performa.
