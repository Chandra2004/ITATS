# 🎓 Alur Praktikum Teknik Sipil: Dari Manual ke Digital

## 🔥 Struktur Peran dalam Praktikum Teknik Sipil

| Peran          | Deskripsi                                           |
| -------------- | --------------------------------------------------- |
| **SuperAdmin** | Kepala Lab (Kalab) dengan akses penuh ke sistem     |
| **Pembimbing** | Dosen Pembimbing (Dospem) yang menilai praktikan    |
| **Asisten**    | Asisten Lab (Aslab) yang mengatur jadwal & kelompok |
| **Praktikan**  | Peserta yang mengikuti praktikum                    |

---

## 🏆 Alur Praktikum Teknik Sipil

1️⃣ **Registrasi**

- Praktikan mengisi profil (foto, nama, NPM, telepon, email, password).
- SuperAdmin tidak perlu registrasi.
- Asisten didaftarkan oleh SuperAdmin.

2️⃣ **Verifikasi Pembayaran**

- Praktikan mengunggah **bukti pembayaran** dan menunggu validasi dari SuperAdmin/Asisten.

3️⃣ **Pemilihan Modul Praktikum**

- Praktikan memilih modul praktikum dan menunggu persetujuan SuperAdmin/Asisten.

4️⃣ **Pemilihan Pembimbing & Asisten**

- Praktikan dapat mengajukan preferensi pembimbing dan asisten.
- SuperAdmin memiliki wewenang untuk menolak atau mengganti pilihan.

5️⃣ **Pembentukan Kelompok**

- Praktikan memilih kelompok (3-5 orang) atau ditempatkan oleh Asisten.

6️⃣ **Distribusi Modul Praktikum**

- Asisten membagikan modul dalam bentuk **buku fisik atau e-book**.

7️⃣ **Pengecekan Data Diri**

- Praktikan memastikan semua data sudah benar sebelum pelaksanaan praktikum.

8️⃣ **Penjadwalan Praktikum**

- SuperAdmin dan Asisten menetapkan jadwal praktikum.

9️⃣ **Pelaksanaan Praktikum**

- Praktikan **absen** sebelum memulai praktikum.
- Setelah selesai, praktikan mengisi **form laporan hasil pengujian**.

🔠 **Asistensi**

- Asistensi harus dilakukan secara bertahap: **Asisten → SuperAdmin → Pembimbing**.
- Jika laporan belum disetujui, harus direvisi sebelum lanjut ke tahap berikutnya.

1️1️⃣ **Penilaian Laporan**

- **SuperAdmin**: 40%
- **Pembimbing**: 60%
- Jika laporan tidak disetujui SuperAdmin, maka tidak bisa dinilai oleh Pembimbing.

1️2️⃣ **Penyelesaian Praktikum**

- Setelah modul selesai, praktikan dapat mendaftar untuk modul lain.
- Mahasiswa dengan nilai di bawah standar wajib mengulang praktikum.

---

## 📌 Fitur Tambahan

👉 **Chat Realtime**: Komunikasi langsung antara peserta dan pembimbing.\
👉 **Video Call (Meeting)**: Fitur WebRTC untuk diskusi online.\
👉 **Form Builder**: SuperAdmin dan Asisten dapat membuat formulir digital.

---

## 🏢 Daftar Praktikum Berdasarkan Semester

| No | Praktikum         | Semester | Jenis Pengujian            |
| -- | ----------------- | -------- | -------------------------- |
| 1  | Ilmu Ukur Tanah   | 1        | Praktik, Tertulis, Laporan |
| 2  | Teknologi Beton   | 1        | Praktik, Tertulis, Laporan |
| 3  | Kimia I           | 1        | Praktik, Tertulis, Laporan |
| 4  | Kimia II          | 2        | Praktik, Tertulis, Laporan |
| 5  | Mekanika Tanah I  | 3        | Praktik, Tertulis, Laporan |
| 6  | Fisika            | 3        | Praktik, Tertulis, Laporan |
| 7  | Mekanika Tanah II | 4        | Praktik, Tertulis, Laporan |
| 8  | Hidrolika         | 5        | Praktik, Tertulis, Laporan |
| 9  | Bahan Jalan       | 6        | Praktik, Tertulis, Laporan |

---

## 🔢 Skema Database

```sql
// Use DBML to define your database structure
// Docs: https://dbml.dbdiagram.io/docs


// Enum
Enum user_role {
  SuperAdmin
  Pembimbing
  Asisten
  Praktikan
}

Enum user_gender {
  Male
  Female
}

Enum semester_praktikum {
  "1"
  "2"
  "3"
  "4"
  "5"
  "6"
}

Enum payment_status {
  Pending
  Approved
  Rejected
}

Enum asisten_status {
  Pending
  Approved
  Revised
}

Enum superadmin_status {
  Pending
  Approved
  Revised
}

Enum pembimbing_status {
  Pending
  Approved
  Revised
}

Enum report_status {
  Pending
  Approved
  Revised
}

// Table
Table users {
  id integer [primary key]
  id_user integer [primary key, not null, unique]

  full_name varchar(255) [not null]
  npm varchar(255) [not null]
  email varchar(255) [not null]
  phone varchar(255) [not null]
  password varchar(255) [not null]
  gender user_gender [not null]
  role user_role
  profile_picture blob

  created_at timestamp [default: `now()`]
  updated_at timestamp
}

Table praktikums {
  id integer [primary key]
  id_praktikum integer [primary key, not null, unique]
  
  name_praktikum varchar(255) [not null]
  semester semester_praktikum [not null]

  created_at timestamp [default: `now()`]
  updated_at timestamp
}

Table payments {
  id integer [primary key]
  id_payment integer [primary key, not null, unique]
  
  user_id integer [not null]
  praktikum_id integer [not null]
  payment_proof bloob [not null]
  status payment_status
  verified_by varchar(255)

  created_at timestamp [default: `now()`]
  updated_at timestamp
}

Table module_praktikums {
  id integer [primary key]
  id_module_praktikum integer [primary key, not null, unique]

  praktikum_id integer
  name varchar(255) [not null]
  description text [not null]
  file_path varchar(255)

  created_at timestamp [default: `now()`]
  updated_at timestamp
}

Table teams {
  id integer [primary key]
  id_team integer [primary key, not null, unique]

  praktikum_id integer
  name varchar(255) [not null]
  max_members integer

  created_at timestamp [default: `now()`]
  updated_at timestamp
}

Table team_members {
  id integer [primary key]

  team_id integer
  user_id integer
}

Table praktikum_schedules {
  id integer [primary key]
  id_schedule integer [primary key, not null, unique]

  praktikum_id integer
  asisten_id integer
  pembimbing_id integer
  user_id integer
  date_schedule date
  time_start_schedule time
  time_end_schedule time
  
  created_at timestamp [default: `now()`]
  updated_at timestamp
}

Table asistensi {
  id integer [primary key]
  id_asistensi integer [primary key, not null, unique]

  praktikum_id integer
  praktikan_id integer

  asisten asisten_status
  superadmin superadmin_status
  pembimbing pembimbing_status
  
  created_at timestamp [default: `now()`]
  updated_at timestamp
}

Table report_praktikums {
  id integer [primary key]
  id_report integer [primary key, not null, unique]

  praktikum_id integer
  praktikan_id integer
  file_path varchar
  report report_status
  
  created_at timestamp [default: `now()`]
  updated_at timestamp
}


Table scores {
  id integer [primary key]
  id_score integer [primary key, not null, unique]

  praktikum_id integer
  praktikan_id integer
  score_superadmin float // 40%
  score_pembimbing float // 60%
  score_total float // rata-rata
  score_predicate varchar // konversi ke huruf
  
  created_at timestamp [default: `now()`]
  updated_at timestamp
}

Table chats {
  id integer [primary key]
  id_chat integer [primary key, not null, unique]

  sender_id integer [not null]
  receiver_id integer [not null]
  message text [not null]
  attachment varchar(255)
  is_read boolean [default: false]

  created_at timestamp [default: `now()`]
  updated_at timestamp
}

Table video_calls {
  id integer [primary key]
  id_video_call integer [primary key, not null, unique]

  caller_id integer [not null]
  receiver_id integer [not null]
  status enum('ongoing', 'ended', 'missed') [default: 'ongoing']
  call_duration integer [default: 0] // Durasi dalam detik

  created_at timestamp [default: `now()`]
  updated_at timestamp
}

Table forms {
  id integer [primary key]
  id_form integer [primary key, not null, unique]

  created_by integer [not null] // SuperAdmin atau Asisten
  title varchar(255) [not null]
  description text
  created_at timestamp [default: `now()`]
  updated_at timestamp
}

Table form_fields {
  id integer [primary key]
  id_field integer [primary key, not null, unique]

  form_id integer [not null]
  label varchar(255) [not null]
  type enum('text', 'number', 'date', 'file', 'radio', 'checkbox', 'textarea', 'select') [not null]
  options text // JSON atau CSV untuk pilihan (jika radio/checkbox/select)
  is_required boolean [default: true]

  created_at timestamp [default: `now()`]
  updated_at timestamp
}

Table form_responses {
  id integer [primary key]
  id_response integer [primary key, not null, unique]

  form_id integer [not null]
  user_id integer [not null] // User yang mengisi form
  created_at timestamp [default: `now()`]
  updated_at timestamp
}

Table form_answers {
  id integer [primary key]
  id_answer integer [primary key, not null, unique]

  response_id integer [not null]
  field_id integer [not null]
  answer text [not null] // Bisa teks atau path file jika upload

  created_at timestamp [default: `now()`]
  updated_at timestamp
}

Ref: "payments"."user_id" < "users"."id_user"
Ref: "payments"."verified_by" < "users"."id_user"
Ref: "payments"."praktikum_id" < "praktikums"."id_praktikum"

Ref: "module_praktikums"."praktikum_id" < "praktikums"."id_praktikum"

Ref: "teams"."praktikum_id" < "praktikums"."id_praktikum"

Ref: "team_members"."team_id" < "teams"."id_team"
Ref: "team_members"."user_id" < "users"."id_user"

Ref: "praktikum_schedules"."praktikum_id" < "praktikums"."id_praktikum"
Ref: "praktikum_schedules"."user_id" < "users"."id_user"
Ref: "praktikum_schedules"."pembimbing_id" < "users"."id_user"

Ref: "asistensi"."praktikum_id" < "praktikums"."id_praktikum"
Ref: "asistensi"."praktikan_id" < "users"."id_user"

Ref: "report_praktikums"."praktikum_id" < "praktikums"."id_praktikum"
Ref: "report_praktikums"."praktikan_id" < "users"."id_user"

Ref: "scores"."praktikum_id" < "praktikums"."id_praktikum"
Ref: "scores"."praktikan_id" < "users"."id_user"

Ref: "chats"."sender_id" < "users"."id_user"
Ref: "chats"."receiver_id" < "users"."id_user"

Ref: "video_calls"."caller_id" < "users"."id_user"
Ref: "video_calls"."receiver_id" < "users"."id_user"

Ref: "forms"."created_by" < "users"."id_user"

Ref: "form_fields"."form_id" < "forms"."id_form"

Ref: "form_responses"."form_id" < "forms"."id_form"
Ref: "form_responses"."user_id" < "users"."id_user"

Ref: "form_answers"."response_id" < "form_responses"."id_response"
Ref: "form_answers"."field_id" < "form_fields"."id_field"
```

```
```
