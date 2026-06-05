# 🔧 Troubleshooting Login & Firebase Setup

## ⚠️ Login Problem - Solusi Cepat

Jika aplikasi tidak bisa login, coba solusi ini:

### ✅ Solusi Cepat (Gunakan Demo Version)
```
Gunakan file: index-enhanced-DEMO.html
Klik "Login sebagai User" atau "Login sebagai Admin"
Tidak perlu Firebase setup!
```

---

## 🔴 Masalah Login pada index-enhanced.html

### Error #1: "pop-up blocked"
```
❌ Pop-up blocked. Pastikan allow pop-ups di browser settings.
```

**Solusi:**
1. Check browser pop-up blocker settings
2. Allow pop-ups untuk domain aplikasi
3. Coba di browser lain
4. Gunakan mode incognito/private

### Error #2: "Network error"
```
❌ Network error. Check internet connection.
```

**Solusi:**
1. Check internet connection
2. Restart router/modem
3. Coba WiFi atau mobile data
4. Refresh halaman (Ctrl+F5)

### Error #3: "Firebase tidak bisa initialized"
```
❌ Firebase tidak bisa initialized. Check console for details.
```

**Solusi:**
1. Open browser console (F12 → Console tab)
2. Lihat error message yang muncul
3. Copy error message dan search di Google
4. Mungkin Firebase SDK tidak load dengan baik

### Error #4: "Permission Denied"
```
❌ Akses denied. Check Firestore rules atau login lagi.
```

**Solusi:**
1. Logout dan login ulang
2. Clear browser cache & cookies
3. Check Firestore security rules di Firebase console
4. Pastikan user sudah disetup di Firestore

---

## 🔧 Setup Firebase yang Benar

Jika ingin setup Firebase sendiri, ikuti langkah ini:

### Step 1: Create Firebase Project
1. Buka https://console.firebase.google.com
2. Klik "Add Project"
3. Masukkan nama project (contoh: "registrasi-plugin")
4. Pilih region (pilih yang dekat, contoh: asia-southeast1)
5. Create project

### Step 2: Enable Authentication
1. Di sidebar, klik "Authentication"
2. Klik "Get Started"
3. Pilih "Google" sign-in method
4. Enable toggle
5. Tambahkan email support
6. Save

### Step 3: Create Firestore Database
1. Di sidebar, klik "Firestore Database"
2. Klik "Create Database"
3. Pilih region (sama dengan project): asia-southeast1
4. Start in test mode (untuk development)
5. Create

### Step 4: Get Config
1. Di sidebar, klik "Project Settings" (gear icon)
2. Pilih tab "General"
3. Scroll ke bawah, cari "Firebase SDK snippet"
4. Copy config object

### Step 5: Update HTML File
1. Buka file `index-enhanced.html` dengan text editor
2. Find bagian Firebase config:
```javascript
const firebaseConfig={
  apiKey:"AIzaSyCKFMyRhFVTIyYL_l-Cxn4LaVLq2fMyJMk",
  authDomain:"plugin-transaksi-c0da0.firebaseapp.com",
  projectId:"plugin-transaksi-c0da0",
  storageBucket:"plugin-transaksi-c0da0.appspot.com",
  messagingSenderId:"1010706549843",
  appId:"1:1010706549843:web:0c8b047f2f5cf2be0e3f57"
};
```

3. Replace dengan config dari Step 4
4. Save file

### Step 6: Setup Firestore Security Rules
1. Di Firebase console, buka Firestore Database
2. Klik "Rules" tab
3. Ganti rules dengan:
```
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    // Allow authenticated users
    match /registrasi/{document=**} {
      allow read, write: if request.auth != null;
    }
    match /users/{document=**} {
      allow read, write: if request.auth != null;
    }
  }
}
```

4. Click "Publish"

### Step 7: Add Authorized Domains
1. Di Firebase console, buka "Authentication"
2. Klik "Settings" tab
3. Scroll ke "Authorized domains"
4. Add domain Anda:
   - Localhost: `localhost`
   - Production: `yourdomain.com`
   - Hosting: `yourproject.firebaseapp.com`

### Step 8: Test Login
1. Buka HTML file di browser
2. Klik "Login dengan Google"
3. Login dengan Google account
4. Seharusnya bisa masuk

---

## 📋 Checklist Firebase Setup

- [ ] Firebase project created
- [ ] Authentication enabled (Google)
- [ ] Firestore database created
- [ ] Security rules updated
- [ ] Config copied ke HTML
- [ ] Authorized domains added
- [ ] Test login berhasil

---

## 🎯 Alternatives: Jika Masih Error

### Option 1: Gunakan Demo Version
Pakai file `index-enhanced-DEMO.html` tanpa Firebase:
```
✓ No setup needed
✓ Works immediately
✓ Perfect for testing
✗ Data tidak permanent
```

### Option 2: Gunakan Firebase Hosting
Deploy ke Firebase Hosting supaya lebih mudah:
```
npm install -g firebase-tools
firebase login
firebase init hosting
firebase deploy
```

### Option 3: Gunakan Supabase (Alternative)
Supabase adalah alternative PostgreSQL-based:
```
1. Create account di supabase.com
2. Create new project
3. Setup authentication & database
4. Update HTML dengan Supabase SDK
```

### Option 4: Setup Balik ke Original
Gunakan file original yang sudah working sebelumnya.

---

## 🛠️ Debug Tips

### Check Browser Console (F12)
1. Open DevTools (F12)
2. Klik "Console" tab
3. Lihat error messages
4. Copy error dan search di Google

### Check Network Tab
1. Open DevTools (F12)
2. Klik "Network" tab
3. Lakukan login
4. Lihat request ke `accounts.google.com`
5. Check response status (200 = ok, 400+ = error)

### Check Firestore
1. Firebase console → Firestore Database
2. Lihat collections yang ada
3. Check apakah ada data
4. Check rules untuk permission

### Enable Debug Logging
Tambah ke HTML sebelum Firebase init:
```javascript
firebase.firestore.setLoggingEnabled(true);
```

---

## 🚀 Quick Solutions by Error Type

### Error: "apiKey invalid"
- ✅ Re-copy config dari Firebase console
- ✅ Make sure tidak ada typo
- ✅ Check apiKey format

### Error: "projectId not found"
- ✅ Check projectId di config
- ✅ Make sure project masih active di Firebase
- ✅ Coba create project baru

### Error: "auth/operation-not-supported"
- ✅ Make sure Google sign-in enabled
- ✅ Check authorized domains
- ✅ Try different browser

### Error: "auth/invalid-origin"
- ✅ Add localhost ke authorized domains
- ✅ Add your domain ke authorized domains
- ✅ Use exact domain (with or without www)

### Error: "permission-denied"
- ✅ Check Firestore rules
- ✅ Make sure rules allow authenticated users
- ✅ Login dulu sebelum access database

---

## 📞 Masih Bermasalah?

Jika masih ada masalah:

### 1. Cek di Sini
- [ ] Internet connection ok?
- [ ] Browser updated?
- [ ] Pop-ups allowed?
- [ ] Firebase project created?
- [ ] Config copied dengan benar?

### 2. Kirim Email Support
Email: **datazahir@gmail.com**

Sertakan:
- Error message (screenshot)
- Firebase project ID
- Browser & versi
- Langkah-langkah reproduce
- Firebase config yang digunakan (hide API key!)

### 3. Gunakan Demo Version
Sambil tunggu support:
```
Gunakan: index-enhanced-DEMO.html
Test fitur tanpa login Firebase
Prepare data di demo version
```

---

## 🎓 Recommended Path

### Untuk Testing/Development:
```
1. Gunakan index-enhanced-DEMO.html
2. Test semua fitur
3. Prepare data
4. Setup Firebase saat siap production
```

### Untuk Production:
```
1. Setup Firebase dengan benar
2. Update config di HTML
3. Setup security rules
4. Deploy ke hosting
5. Test dari production domain
```

---

**Last Updated: 2025**

**Good Luck! 🚀**
