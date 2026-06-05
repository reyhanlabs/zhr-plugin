# 🎯 Quick Reference Guide - Registrasi Plugin v3.0 Enhanced

## 📱 Interface Quick Map

```
┌─────────────────────────────────────────────────────────────┐
│                         APLIKASI DASHBOARD                  │
├────────────────────────┬──────────────────────────────────────┤
│                        │  🌙 Theme Toggle                     │
│  🎯 SIDEBAR           │━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━  │
│  ┌─────────────────┐  │ [Quick Actions Grid]                 │
│  │ 📊 Dashboard ✓  │  │ ┌───────┬───────┬───────┬────────┐ │
│  │ 📋 Data Reg     │  │ │ ➕   │  👤  │ 📥   │  📤   │ │
│  │ ➕ Tambah Data  │  │ └───────┴───────┴───────┴────────┘ │
│  │ 💰 Rekap Komisi │  │                                      │
│  │ ⏱️ Riwayat      │  │ [Highlight Stats Cards]              │
│  │ ℹ️ Info Sistem  │  │ ┌──────┬──────┬──────┐             │
│  │ 📖 Panduan      │  │ │Total │Active│Expiring             │
│  │          [👤] │  │ └──────┴──────┴──────┘             │
│  └─────────────────┘  │                                      │
│  [Toggle ◀/▶]         │ [Data Table / Content Area]          │
│                        │                                      │
└────────────────────────┴──────────────────────────────────────┘
```

---

## 🚀 Navigasi Cepat

### Menu Sidebar
```
MENU UTAMA:
  ✓ Dashboard      → Statistik & overview
  📋 Data Reg      → Lihat semua registrasi
  ➕ Tambah Data   → Input data baru
  
LAPORAN:
  💰 Rekap Komisi  → Laporan komisi
  ⏱️ Riwayat       → Log perubahan data
  
INFO:
  ℹ️ Info Sistem   → Info teknis & export
  📖 Panduan       → Bantuan & tutorial
```

### Topbar Controls
```
LEFT:
  📄 Title        → Judul halaman aktif
  📝 Subtitle     → Deskripsi halaman

RIGHT:
  🌙/☀️ Theme     → Toggle dark/light mode
```

---

## 📊 Dashboard Features

### Quick Actions (4 Tombol)
```
┌─────────────────┬─────────────────┬─────────────────┬─────────────────┐
│       ➕        │        👤       │       📥        │       📤        │
│   Tambah Data   │   Kelola User   │   Export CSV    │  Import Excel   │
│  (→ Form input) │  (→ Modal user) │  (→ Download)   │  (→ File pick)  │
└─────────────────┴─────────────────┴─────────────────┴─────────────────┘
```

### Highlight Cards (3 Stat)
```
┌──────────────────────┐
│  📊 TOTAL REGISTRASI │
│        150           │
│  Semua data terdaftar│
└──────────────────────┘

┌──────────────────────┐
│  ✅ STATUS AKTIF     │
│        128           │
│  Masih berlaku       │
└──────────────────────┘

┌──────────────────────┐
│  ⏰ AKAN EXPIRED     │
│         12           │
│  30 hari ke depan    │
└──────────────────────┘
```

### Distribusi Paket
```
Starter      : ▓▓▓▓░░░░░░  (40 registrasi)
Professional : ▓▓▓▓▓▓▓░░░  (75 registrasi)
Enterprise   : ▓▓▓░░░░░░░  (35 registrasi)
```

### Upcoming Expiry (5 Most Urgent)
```
1. PT. ABC - Expire: 2025-06-15 (10 hari) 🔴
2. CV. XYZ - Expire: 2025-06-20 (15 hari) 🟠
3. PT. Maju - Expire: 2025-06-25 (20 hari) 🟡
4. PT. Telkom - Expire: 2025-06-28 (23 hari) 🟡
5. PT. Indo - Expire: 2025-07-02 (27 hari) 🟡
```

---

## 📋 Data Registrasi Page

### Search & Filter Bar
```
┌─────────────────────────┬──────────────────────┐
│  🔍 Cari...            │ Status: [Semua ▼]    │
│  (Real-time search)    │ [Aktif] [Kadaluarsa] │
└─────────────────────────┴──────────────────────┘
```

### Table Structure
```
┌────┬──────────────┬──────────┬────────────┬───────┬──────────┬────────┬─────────┐
│ No │ Perusahaan   │ Invoice  │ Paket      │ Aktif │ Expired  │ Status │  Aksi   │
├────┼──────────────┼──────────┼────────────┼───────┼──────────┼────────┼─────────┤
│ 1  │ PT. ABC Inc  │ INV-001  │ Starter    │ 2025- │ 2025-09- │ ✅ Aktif│ ✏️ 🗑️  │
│    │              │          │            │ 06-01 │ 30       │        │         │
│ 2  │ CV. XYZ      │ INV-002  │ Professional│ 2025-│ 2025-06-│ ⏰ Will │ ✏️ 🗑️  │
│    │              │          │            │ 05-15 │ 20      │ Expire │         │
└────┴──────────────┴──────────┴────────────┴───────┴──────────┴────────┴─────────┘

Status Badges:
  ✅ AKTIF (Green)        - Registrasi masih berlaku
  ⏰ AKAN EXPIRED (Orange)  - Akan kadaluarsa dalam 30 hari
  ❌ KADALUARSA (Red)     - Sudah melewati tanggal expired
```

---

## 📝 Form Input Fields

### Field Wajib (Required) - ditandai *
```
┌──────────────────────────────────────────────┐
│ Nama Perusahaan *                            │ ← Text input
│ (Contoh: PT. Telkom Indonesia)               │
└──────────────────────────────────────────────┘

┌──────────────────────────────────────────────┐
│ Invoice *                                    │ ← Text input
│ (Contoh: INV-2025-001)                       │
└──────────────────────────────────────────────┘

┌──────────────────────────────────────────────┐
│ Paket Plugin *                    [Pilih ▼]  │ ← Dropdown
│ • Starter      • Professional    • Enterprise│
└──────────────────────────────────────────────┘

┌──────────────────────────────────────────────┐
│ Tipe Registrasi *                [Pilih ▼]  │ ← Dropdown
│ • Komersial   • Internal         • Trial     │
└──────────────────────────────────────────────┘

┌──────────────────────────────────────────────┐
│ Tgl Registrasi *                             │ ← Date picker
│ 📅 2025-06-01                                │
└──────────────────────────────────────────────┘

┌──────────────────────────────────────────────┐
│ Tgl Aktif Hingga *                           │ ← Date picker
│ 📅 2025-12-31                                │
└──────────────────────────────────────────────┘

┌──────────────────────────────────────────────┐
│ Catatan (Optional)                           │ ← Textarea
│                                              │
│ (Keterangan, notes, kontak, dll)             │
└──────────────────────────────────────────────┘

┌──────────────────────────────────────────────┐
│ [✅ Simpan Data]  [↻ Reset]                  │
└──────────────────────────────────────────────┘
```

---

## 🎨 Color & Status Reference

### Status Colors
```
✅ AKTIF         Green (#00d084)       Registrasi berlaku
⏰ AKAN EXPIRED   Orange (#fbbf24)     30 hari ke depan
❌ KADALUARSA    Red (#ff6b6b)         Sudah kadaluarsa
```

### UI Colors (Gradients)
```
Primary:  Purple → Dark Purple      (#667eea → #764ba2)
Success:  Green → Bright Green      (#00d084 → #0cce6b)
Warning:  Red → Darker Red          (#ff6b6b → #ee5a6f)
Info:     Cyan → Bright Cyan        (#4facfe → #00f2fe)
```

---

## ⌨️ Keyboard Shortcuts

```
┌──────────────┬─────────────────────────────────┐
│ ESC          │ Tutup modal/dialog              │
│ Tab          │ Pindah ke field berikutnya      │
│ Shift+Tab    │ Pindah ke field sebelumnya      │
│ Enter        │ Submit form / Confirm action    │
│ Ctrl+S       │ Save data (jika di form)        │
└──────────────┴─────────────────────────────────┘
```

---

## 🔐 Role & Permissions

### Admin
```
✓ View all data
✓ Create registrasi
✓ Edit registrasi
✓ Delete registrasi
✓ Import Excel/CSV
✓ Manage users
✓ View all reports
✓ Access all menus
```

### User
```
✓ View registrasi
✓ Create registrasi
✓ Edit own registrasi
✗ Delete registrasi (blocked)
✗ Import Excel/CSV (blocked)
✗ Manage users (blocked)
✓ View limited reports
```

---

## 📊 Export/Import Reference

### Export CSV Format
```
No,Nama Perusahaan,Invoice,Paket,Tgl Registrasi,Tgl Aktif,Status
1,"PT. ABC Indonesia","INV-001","Professional","2025-06-01","2025-12-31","Aktif"
2,"CV. XYZ Corp","INV-002","Starter","2025-06-05","2025-09-30","Akan Expired"
3,"PT. Telkom","INV-003","Enterprise","2025-05-15","2025-05-31","Kadaluarsa"
```

### Import Excel Template
```
| No | Nama Perusahaan | Invoice  | Paket       | Tgl Registrasi | Tgl Aktif  |
|----|-----------------:|----------|-------------|:-------------:|:----------:|
| 1  | PT. ABC         | INV-001  | Starter     | 2025-06-01   | 2025-12-31 |
| 2  | CV. XYZ         | INV-002  | Professional| 2025-06-05   | 2025-09-30 |
| 3  | PT. Maju        | INV-003  | Enterprise  | 2025-05-01   | 2025-11-30 |
```

**Important:**
- Format: .xlsx, .xls, atau .csv
- Encoding: UTF-8
- Header harus match dengan template
- Date format: YYYY-MM-DD
- All required fields must be filled

---

## 🔔 Toast Notifications

```
┌─────────────────────────────────────┐
│ ✅ Data berhasil disimpan           │  (Success - Green)
└─────────────────────────────────────┘

┌─────────────────────────────────────┐
│ ❌ Error: Field tidak boleh kosong  │  (Danger - Red)
└─────────────────────────────────────┘

┌─────────────────────────────────────┐
│ ⚠️ Warning: Data sudah expired       │  (Warning - Orange)
└─────────────────────────────────────┘

┌─────────────────────────────────────┐
│ ℹ️ CSV berhasil diekspor            │  (Info - Blue)
└─────────────────────────────────────┘

Auto-dismiss: 3 detik
Location: Bottom-right
```

---

## 🌙 Dark Mode

### Toggle Location
```
Top-right corner of topbar
┌─────────────────────────────────────┐
│ ... [🌙 or ☀️ button] ...            │
└─────────────────────────────────────┘
```

### Color Scheme Switch
```
LIGHT MODE:
  Background: White (#ffffff)
  Text: Dark (#1f2937)
  Accents: Bright colors

DARK MODE:
  Background: Dark (#0f172a)
  Text: Light (#f1f5f9)
  Accents: Muted colors

Auto-saved in browser localStorage
```

---

## 📱 Responsive Breakpoints

```
Desktop (1200px+)
  │
  └─ Full layout
     │ 4-column grid for charts
     │ Full sidebar visible
     │ Large table with all columns

Tablet (768px - 1199px)
  │
  └─ Adjusted layout
     │ 2-column grid for charts
     │ Sidebar remains visible
     │ Table scrollable

Mobile (<768px)
  │
  └─ Stack layout
     │ 1-column grid for charts
     │ Sidebar collapses automatically
     │ Touch-friendly buttons
     │ Single column table
```

---

## 🛠️ Troubleshooting Quick Fixes

```
❌ Problem               │ ✅ Quick Fix
────────────────────────┼──────────────────────────────────
Tidak bisa login         │ Refresh (Ctrl+F5), clear cache
Data tidak muncul        │ Check filter & search box
Tidak bisa save          │ Verify all * fields filled
Form butuh reload        │ ESC to close, reopen
Lag/slow                 │ Clear cache, refresh
Dark mode tidak saved    │ Clear localStorage
Konfirmasi dialog stuck  │ Press ESC key
```

---

## 📞 Quick Contact

### Email Support
```
📧 datazahir@gmail.com
Subject: [BUG REPORT] or [FEATURE REQUEST] or [QUESTION]
Include:
  - Error message
  - Screenshot
  - Steps to reproduce
  - Browser & version
```

### Response Time
```
Weekday: ~4-8 jam
Weekend: ~24 jam
Holiday: +1 hari
```

---

## 📋 Common Tasks Checklist

### Daily Tasks
- [ ] Check Dashboard for upcoming expirations
- [ ] Monitor inbox for new registrations
- [ ] Check alerts for system issues

### Weekly Tasks
- [ ] Review registrations status
- [ ] Export data for backup
- [ ] Check admin logs

### Monthly Tasks
- [ ] Export full data to archive
- [ ] Review all registrations
- [ ] Plan renewals for expiring registrations
- [ ] Update customer records as needed

### Quarterly Tasks
- [ ] Full data audit
- [ ] Performance review
- [ ] System optimization
- [ ] Backup verification

---

## 💡 Pro Tips

```
🔥 SUPER TIPS:
1. Use search instead of scroll untuk data besar
2. Filter status untuk fokus pada urgent items
3. Export CSV setiap minggu untuk backup
4. Monitor upcoming expiry di dashboard
5. Gunakan catatan field untuk info penting
6. Set reminder untuk renewal 7 hari sebelum expired
7. Gunakan dark mode saat kerja malam
8. Keyboard shortcut Tab+Enter lebih cepat dari mouse
```

---

## 📊 System Info

```
Application: Registrasi Plugin Transaksi
Version: 3.0 Enhanced
Status: Production Ready
Last Updated: 2025
License: Internal Use Only

Backend: Firebase Firestore
Authentication: Google OAuth
Region: asia-southeast1
Encryption: SSL/TLS
Backup: Automatic Daily

Browser Support:
  ✓ Chrome/Edge (Latest)
  ✓ Firefox (Latest)
  ✓ Safari (Latest)
  ✓ Mobile Browsers
```

---

**Print this guide for quick reference! 📖**

Last Updated: 2025
Version: 3.0 Enhanced
