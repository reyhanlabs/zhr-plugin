# 📖 Panduan Lengkap Aplikasi Registrasi Plugin Transaksi v3.0 Enhanced

## 📋 Daftar Isi
1. [Getting Started](#getting-started)
2. [Dashboard](#dashboard)
3. [Data Registrasi](#data-registrasi)
4. [Tambah/Edit Data](#tambahédit-data)
5. [Laporan & Export](#laporan--export)
6. [Pengaturan](#pengaturan)
7. [Keyboard Shortcuts](#keyboard-shortcuts)
8. [FAQ](#faq)
9. [Tips & Trik](#tips--trik)
10. [Troubleshooting](#troubleshooting)

---

## Getting Started

### 1️⃣ Login ke Aplikasi
- Klik tombol **"Login dengan Google"**
- Pilih akun Google Anda
- Tunggu sampai dashboard muncul
- Sistem akan menyimpan preferensi Anda (dark mode, sidebar state, dll)

### 2️⃣ Memahami Layout
```
┌─────────────────────────────────────────────┐
│  🎯 SIDEBAR          │ TOPBAR             │
│  Navigation Menu     │ Title + Theme      │
│                      │                    │
│                      ├─────────────────────┤
│                      │                    │
│                      │ CONTENT AREA       │
│                      │ (Dashboard/Data)   │
│                      │                    │
└─────────────────────────────────────────────┘
```

### 3️⃣ Interface Utama
- **Sidebar (Kiri)**: Menu navigasi dengan collapsible
- **Top Bar**: Title halaman dan theme toggle
- **Content Area**: Area utama untuk menampilkan data
- **Toast Notifications**: Pesan di kanan bawah

---

## Dashboard

### 📊 Fitur-Fitur Dashboard

#### A. Quick Actions
Empat tombol pintas untuk navigasi cepat:

```
┌─────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐
│  ➕     │  │    👤   │  │   📥    │  │   📤    │
│ Tambah  │  │  Kelola  │  │ Export  │  │ Import  │
│   Data  │  │   User   │  │   CSV   │  │  Excel  │
└─────────┘  └──────────┘  └──────────┘  └──────────┘
```

**Cara Menggunakan:**
- **Tambah Registrasi**: Buka form input untuk data baru
- **Kelola User**: Kelola akses dan role (admin saja)
- **Export CSV**: Download semua data dalam CSV
- **Import Excel**: Upload data dari file (admin saja)

#### B. Highlight Cards (Statistik)
Tiga kartu statistik penting:

1. **📊 Total Registrasi**
   - Menampilkan jumlah semua registrasi dalam sistem
   - Update real-time saat ada tambah/hapus data

2. **✅ Status Aktif**
   - Menampilkan registrasi yang masih berlaku
   - Registrasi dengan tanggal expired > hari ini

3. **⏰ Akan Expired**
   - Menampilkan registrasi yang akan kadaluarsa
   - Dalam range 30 hari ke depan dari hari ini

#### C. Distribusi Paket Plugin
Card yang menampilkan breakdown paket:

```
Starter          : [5 registrasi]    █░░░░░░░░
Professional     : [12 registrasi]   ███████░░░
Enterprise       : [8 registrasi]    █████░░░░░
```

- Otomatis update saat ada perubahan data
- Membantu tracking penggunaan paket

#### D. Upcoming Expiry Alerts
Fitur smart alert untuk registrasi yang akan expired:

```
🔔 REGISTRASI AKAN EXPIRED (Next 30 Days)

┌─────────────────────────────────────┐
│ PT. ABC Indonesia                   │
│ Expired: 2025-06-20                 │
│ Sisa: 15 hari                       │
└─────────────────────────────────────┘

┌─────────────────────────────────────┐
│ PT. XYZ Corp                        │
│ Expired: 2025-06-25                 │
│ Sisa: 20 hari                       │
└─────────────────────────────────────┘
```

**Fitur:**
- ✅ Maksimal 5 registrasi paling urgent
- ✅ Otomatis sorting by expiry date (terdekat dulu)
- ✅ Menampilkan countdown hari
- ✅ Klik untuk edit langsung

---

## Data Registrasi

### 🔍 Pencarian & Filtering

#### Search Box
- Ketik nama perusahaan, nomor invoice, atau nama paket
- Pencarian real-time saat Anda mengetik
- Case-insensitive (tidak peduli besar/kecil huruf)

**Contoh Search:**
```
✓ "PT Telkom" → cari nama perusahaan
✓ "INV-2025-001" → cari nomor invoice
✓ "Professional" → cari nama paket
✓ "trial" → cari tipe registrasi (lowercase)
```

#### Status Filter
Pilih filter dari dropdown:
- **Semua Status**: Tampilkan semua data
- **Aktif**: Hanya registrasi dengan status aktif
- **Kadaluarsa**: Hanya registrasi yang sudah expired

### 🏷️ Status Badges

Setiap registrasi memiliki badge status dengan warna berbeda:

```
✅ AKTIF (Hijau)
   └─ Registrasi masih berlaku, tidak ada masalah

⏰ AKAN EXPIRED (Orange)
   └─ Registrasi akan kadaluarsa dalam 30 hari

❌ KADALUARSA (Merah)
   └─ Registrasi sudah melewati tanggal expired
```

### 📋 Kolom-Kolom Tabel

| Kolom | Penjelasan |
|-------|-----------|
| No | Nomor urut (auto) |
| Perusahaan | Nama perusahaan customer |
| Invoice | Nomor invoice referensi |
| Paket | Tipe paket (Starter/Professional/Enterprise) |
| Tgl Aktif | Tanggal registrasi dimulai |
| Tgl Expired | Tanggal registrasi berakhir |
| Status | Badge status (Aktif/Akan Expired/Kadaluarsa) |
| Aksi | Tombol Edit & Hapus |

### ⚙️ Action Buttons

Setiap baris memiliki 2 tombol:

1. **✏️ Edit**
   - Buka form untuk mengedit data
   - Semua field akan terisi dengan data sebelumnya
   - Klik "Simpan Data" untuk update

2. **🗑️ Hapus**
   - Hapus data registrasi
   - Sistem akan minta konfirmasi terlebih dahulu
   - Tidak bisa di-undo, hati-hati!

---

## Tambah/Edit Data

### 📝 Form Input

Form terdiri dari 7 field yang harus/boleh diisi:

#### Field-Field Wajib (ditandai * berwarna merah):

1. **Nama Perusahaan***
   - Masukkan nama lengkap perusahaan customer
   - Contoh: "PT. Telkom Indonesia", "CV. Maju Jaya"
   - Maksimal 100 karakter

2. **Invoice***
   - Nomor invoice atau reference number
   - Contoh: "INV-2025-001", "ATL-001234"
   - Unik per registrasi (hindari duplikasi)

3. **Paket Plugin***
   - Pilih salah satu dari dropdown:
     - **Starter**: Paket dasar
     - **Professional**: Paket menengah
     - **Enterprise**: Paket premium

4. **Tipe Registrasi***
   - Pilih salah satu dari dropdown:
     - **Komersial**: Registrasi berbayar/komersial
     - **Internal**: Registrasi untuk internal/testing
     - **Trial**: Registrasi trial/gratis

5. **Tgl Registrasi***
   - Tanggal saat registrasi dilakukan
   - Format: YYYY-MM-DD (picker otomatis)
   - Biasanya sama dengan hari ini

6. **Tgl Aktif Hingga***
   - Tanggal registrasi akan berakhir
   - Format: YYYY-MM-DD
   - Otomatis system menghitung sisa hari

#### Field Optional:

7. **Catatan**
   - Keterangan tambahan atau notes penting
   - Bisa berisi info khusus, kontak, dll
   - Tidak wajib diisi

### 💡 Tips Menggunakan Form

#### A. Focus Effects
```
┌─────────────────────────────┐
│ Nama Perusahaan             │  ← Normal state
└─────────────────────────────┘

┌─────────────────────────────┐
│ Nama Perusahaan             │  ← Fokus: ada shadow biru
└─────────────────────────────┘
```

#### B. Validasi Input
- Field dengan * harus diisi sebelum bisa save
- Jika ada yang kosong, sistem akan warn
- Error message akan tampil jelas

#### C. Saran Input Data
```
✓ BENAR:
  Nama: "PT. Telkom Indonesia"
  Invoice: "TEL-2025-001"
  Tgl: 2025-06-01 s/d 2025-12-31

✗ SALAH:
  Nama: "telkom" (terlalu singkat)
  Invoice: "" (kosong)
  Tgl: 2025-01-01 s/d 2024-12-31 (tanggal balik)
```

### 🔄 Edit Data Existing

Untuk mengedit data:
1. Di halaman Data Registrasi, klik tombol **✏️ Edit** pada baris
2. Form akan terbuka dengan data terisi
3. Ubah field yang perlu diubah
4. Klik **Simpan Data** untuk update
5. Sistem akan show toast notification "Data berhasil diperbarui"

### 🗑️ Menghapus Data

Untuk menghapus data:
1. Di halaman Data Registrasi, klik tombol **🗑️ Hapus** pada baris
2. Dialog konfirmasi akan muncul
3. Klik **OK** untuk konfirmasi atau **Cancel** untuk batal
4. Data akan dihapus permanent (tidak bisa di-undo)

---

## Laporan & Export

### 💰 Rekap Komisi

Halaman ini menampilkan ringkasan komisi dari semua registrasi:

**Informasi yang Ditampilkan:**
- No urut
- Tanggal registrasi
- Nomor invoice
- Nama perusahaan
- Tipe paket
- Keterangan/catatan

**Cara Menggunakan:**
1. Klik menu **"Rekap Komisi"** di sidebar
2. Tabel akan menampilkan semua data
3. Klik tombol **🖨️ Cetak** untuk print/PDF

**Print Tips:**
```
✓ Browser akan terbuka window baru
✓ Preview menampilkan laporan siap cetak
✓ Pilih printer atau "Save as PDF"
✓ Format otomatis landscape untuk tabel lebar
```

### ⏱️ Riwayat Update

Menampilkan log semua perubahan data:

**Informasi:**
- Waktu perubahan
- User yang melakukan perubahan
- Data sebelum & sesudah
- Jenis action (create/update/delete)

**Berguna Untuk:**
- Audit trail & compliance
- Tracking siapa yang ubah apa
- Recovery info jika ada kesalahan

### 📥 Export CSV

Export semua data ke format CSV (Excel-compatible):

**Cara Export:**
1. Klik **"Export CSV"** di Quick Actions
2. File akan otomatis di-download
3. Nama file: `registrasi_YYYY-MM-DD.csv`

**File Format:**
```
No,Nama Perusahaan,Invoice,Paket,Tgl Registrasi,Tgl Aktif,Status
1,"PT. ABC Indonesia","INV-001","Professional","2025-06-01","2025-12-31","Aktif"
2,"CV. XYZ","INV-002","Starter","2025-06-05","2025-09-30","Akan Expired"
```

**Kegunaan:**
- ✓ Backup data
- ✓ Share data ke orang lain
- ✓ Import ke aplikasi lain
- ✓ Analisis data dengan Excel

### 📤 Import Excel

Import data dari file Excel/CSV (Admin saja):

**Syarat File:**
```
Format: .xlsx, .xls, atau .csv
Header: No,Perusahaan,Invoice,Paket,Tgl Reg,Tgl Aktif,...
Encoding: UTF-8
```

**Cara Import:**
1. Siapkan file Excel dengan format yang benar
2. Klik **"Import Excel"** di Quick Actions
3. Pilih file dari komputer
4. Tunggu proses import selesai
5. Toast notification akan muncul

**Template Excel:**
```
| No | Nama Perusahaan | Invoice | Paket | Tgl Registrasi | Tgl Aktif |
|----|-----------------|---------|-------|----------------|-----------|
| 1  | PT. ABC         | INV-001 | Prof  | 2025-06-01     | 2025-12-31|
| 2  | CV. XYZ         | INV-002 | Start | 2025-06-05     | 2025-09-30|
```

---

## Pengaturan

### 🌙 Dark Mode

Toggle antara light dan dark theme:

**Cara:**
1. Klik tombol **moon/sun icon** di top-right topbar
2. Tema akan berubah instantly
3. Preference disimpan otomatis di browser
4. Akan apply otomatis saat buka lagi

**Dark Mode Benefits:**
- ✓ Lebih nyaman di mata saat malam
- ✓ Hemat baterai di device OLED
- ✓ Professional appearance
- ✓ Reduce eye strain

### 🔐 User Role

Ada 2 tipe role dalam sistem:

#### 1. Admin (👨‍💼)
- Akses penuh ke semua fitur
- Bisa import data dari Excel
- Bisa kelola user
- Bisa hapus data

#### 2. User (👤)
- Akses terbatas
- Hanya bisa view & add data
- Tidak bisa import
- Tidak bisa hapus data

**Cek Role Anda:**
- Buka **"Informasi Sistem"** menu
- Lihat badge di sebelah "Role"

### 📊 Informasi Sistem

Menampilkan info teknis tentang sistem:

**Informasi yang Ditampilkan:**
- Project ID: `plugin-transaksi`
- User Login: [Nama Anda]
- Email: [Email Anda]
- Role: Admin/User
- Total Data: [Jumlah registrasi]
- Versi App: 3.0 Enhanced

**Kegunaan:**
- Verifikasi login
- Check role untuk akses
- Lihat total data
- Support info

---

## Keyboard Shortcuts

Gunakan keyboard shortcut untuk navigasi lebih cepat:

| Shortcut | Fungsi |
|----------|--------|
| **ESC** | Tutup modal/dialog yang terbuka |
| **Tab** | Navigasi ke field berikutnya di form |
| **Shift+Tab** | Navigasi ke field sebelumnya di form |
| **Enter** | Submit form atau konfirmasi action |
| **Ctrl+S** | Save data (jika di form) |

### Contoh Penggunaan:
```
1. Buka form dengan klik "Tambah Registrasi"
2. Ketik data di field pertama
3. Tekan Tab untuk pindah ke field berikutnya
4. Setelah semua field terisi, tekan Enter untuk save
5. Tekan ESC jika ingin batal
```

---

## FAQ

### Q: Bagaimana cara membuat registrasi baru?
**A:** 
1. Klik **"Tambah Registrasi"** di dashboard atau sidebar
2. Isi semua field yang ditandai * (wajib)
3. Klik **"Simpan Data"**
4. Data akan tersimpan dan tampil di tabel

### Q: Bagaimana cara menghapus data?
**A:**
1. Buka halaman **"Data Registrasi"**
2. Cari data yang ingin dihapus
3. Klik tombol **🗑️ Hapus** di baris tersebut
4. Konfirmasi saat dialog muncul
5. ⚠️ Perhatian: Data tidak bisa di-restore!

### Q: Bagaimana cara edit data yang sudah ada?
**A:**
1. Buka halaman **"Data Registrasi"**
2. Klik tombol **✏️ Edit** pada baris yang ingin diedit
3. Ubah field yang diperlukan
4. Klik **"Simpan Data"**
5. Data akan terupdate

### Q: Bagaimana cara export data?
**A:**
- **Quick**: Klik **"Export CSV"** di quick actions dashboard
- **Detail**: Buka menu **"Informasi Sistem"** → klik **"Export ke CSV"**
- File akan otomatis di-download

### Q: Siapa yang bisa import data?
**A:** Hanya **Admin** yang memiliki hak untuk import data dari Excel/CSV. User biasa tidak bisa.

### Q: Bagaimana format tanggal yang benar?
**A:** Format: **YYYY-MM-DD** (ISO format)
```
✓ Benar: 2025-06-15, 2025-12-31
✗ Salah: 15-06-2025, 06/15/2025, 15 Juni 2025
```

### Q: Bagaimana jika lupa password?
**A:** Sistem menggunakan Google Authentication. Gunakan "Forgot Password" di Google atau hubungi admin.

### Q: Berapa lama data disimpan?
**A:** Data disimpan di Firebase cloud secara permanent sampai dihapus manual. Tidak ada auto-delete.

### Q: Bisa backup data?
**A:** Ya, gunakan fitur **"Export CSV"** untuk membuat backup data secara berkala.

### Q: Berapa banyak data yang bisa disimpan?
**A:** Tidak ada batasan jumlah data. Sistem dapat menangani ribuan registrasi tanpa masalah.

### Q: Bagaimana jika ada error/bug?
**A:** Hubungi support di `datazahir@gmail.com` dengan detail:
- Deskripsi error
- Screenshot
- Langkah-langkah repeat bug
- Browser & versi yang digunakan

---

## Tips & Trik

### 💡 Tip 1: Gunakan Search untuk Quick Find
Daripada scroll tabel panjang, gunakan search box:
```
Cari "Jakarta" untuk filter semua customer di Jakarta
Cari "Professional" untuk lihat semua paket Professional
```

### 💡 Tip 2: Filter Status untuk fokus
```
Filter "Aktif" → fokus pada registrasi yang berjalan
Filter "Kadaluarsa" → lihat mana yang perlu renewal
```

### 💡 Tip 3: Monitor Upcoming Expiry
Dashboard otomatis menampilkan 5 registrasi yang akan expired. Pantau ini regular untuk proactive renewal.

### 💡 Tip 4: Export Regular untuk Backup
Setiap minggu atau bulan, export data ke CSV sebagai backup. Simpan di multiple lokasi.

### 💡 Tip 5: Gunakan Catatan untuk Informasi Penting
```
Contoh catatan:
"PIC: Budi Santoso (081234567890)"
"Payment: Lunas per invoice XXX"
"Special discount 10% applied"
```

### 💡 Tip 6: Dark Mode untuk Penggunaan Malam
Kalau kerja malam, aktifkan dark mode untuk less eye strain. Klik moon icon di top-right.

### 💡 Tip 7: Check Info Sistem Berkala
Buka "Informasi Sistem" untuk lihat total data dan verifikasi login.

### 💡 Tip 8: Gunakan Keyboard Shortcut
Lebih cepat pake shortcut daripada mouse:
- **Tab** untuk pindah field
- **Enter** untuk save
- **ESC** untuk batal

---

## Troubleshooting

### ❌ Problem: Tidak bisa login

**Solusi:**
1. Pastikan koneksi internet stabil
2. Refresh halaman (Ctrl+F5)
3. Clear browser cache
4. Coba browser lain
5. Pastikan akun Google aktif

### ❌ Problem: Data tidak muncul di tabel

**Solusi:**
1. Refresh halaman (F5)
2. Check apakah ada filter yang aktif
3. Cek search box (kemungkinan typo)
4. Logout dan login ulang

### ❌ Problem: Tidak bisa save data

**Solusi:**
1. Pastikan semua field * (wajib) sudah diisi
2. Check format tanggal (harus YYYY-MM-DD)
3. Pastikan koneksi internet aktif
4. Lihat error message yang muncul
5. Hubungi support jika tetap error

### ❌ Problem: Import Excel error

**Solusi:**
1. Check format file (harus .xlsx/.xls/.csv)
2. Pastikan header sesuai dengan template
3. Pastikan encoding UTF-8
4. Cek apakah ada data invalid (missing field, format salah)
5. Hubungi support dengan file sample

### ❌ Problem: Lambat/lag saat buka

**Solusi:**
1. Refresh halaman
2. Clear browser cache
3. Close tab lain yang berat
4. Gunakan browser terbaru
5. Check koneksi internet speed

### ❌ Problem: Dark mode tidak tersimpan

**Solusi:**
1. Clear browser cookies
2. Check localStorage di developer tools
3. Coba mode private/incognito
4. Refresh dan coba lagi

### ❌ Problem: Lupa data sudah pernah di-delete

**Catatan:** 
- ⚠️ Sistem tidak memiliki fitur undo
- Data yang didelete permanent hilang
- Untuk recovery, harus dari backup CSV yang ada
- Hati-hati saat klik tombol Delete!

---

## 📞 Contact & Support

### Email Support
**📧 datazahir@gmail.com**

### Informasi yang Sertakan:
1. Deskripsi detail masalah
2. Screenshot (jika ada)
3. Langkah-langkah untuk reproduce
4. Browser & versi yang digunakan
5. Waktu kejadian error

### Response Time
Biasanya dijawab dalam 24 jam kerja.

---

## 📚 Informasi Teknis

### Browser Support
✅ Chrome/Chromium (Latest)
✅ Firefox (Latest)
✅ Safari (Latest)
✅ Edge (Latest)
✅ Mobile Browsers

### Data Storage
- Cloud: Firebase Firestore
- Region: asia-southeast1
- Encryption: SSL/TLS
- Backup: Automatic by Firebase

### Versi Aplikasi
- Current: **3.0 Enhanced**
- Last Updated: 2025
- Status: Production Ready

---

## 📝 Changelog

### v3.0 Enhanced (2025)
- ✅ UI/UX refresh dengan gradient colors
- ✅ Smooth animations & transitions
- ✅ Enhanced dashboard dengan quick actions
- ✅ Upcoming expiry alerts
- ✅ Better search & filter
- ✅ Dark mode support
- ✅ Responsive design improvement
- ✅ Better notifications (toast)
- ✅ Comprehensive help/guide

### v2.5 (Previous)
- Firebase integration
- Role-based access
- Export/Import CSV
- Print laporan komisi

---

**Selamat menggunakan! 🎉**

*Jika ada pertanyaan atau saran, jangan ragu untuk menghubungi support.*
