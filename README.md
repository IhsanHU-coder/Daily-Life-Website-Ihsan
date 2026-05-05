# 🗓 Daily Life Ihsan

Website produktivitas harian pribadi yang bisa diakses dari semua device.

## 🚀 Cara Deploy ke GitHub Pages (GRATIS & Online)

### Langkah 1 — Persiapan
1. Buat akun di [github.com](https://github.com) kalau belum punya
2. Buat repository baru, namanya misalnya `daily-ihsan`
3. Centang **"Add a README file"**

### Langkah 2 — Upload File
1. Di halaman repository, klik **"Add file" → "Upload files"**
2. Upload file `index.html` dari folder ini
3. Klik **"Commit changes"**

### Langkah 3 — Aktifkan GitHub Pages
1. Klik **"Settings"** di repository kamu
2. Di sidebar kiri, klik **"Pages"**
3. Di bagian "Source", pilih **"Deploy from a branch"**
4. Pilih branch: **main**, folder: **/ (root)**
5. Klik **Save**

### Langkah 4 — Akses Website
- Setelah 1-2 menit, website kamu live di:
  `https://USERNAME.github.io/daily-ihsan/`
- Ganti `USERNAME` dengan username GitHub kamu

---

## ⚙️ Setup Google Sheets (Simpan Data Harian)

### Langkah 1 — Buat Google Sheet
1. Buka [sheets.google.com](https://sheets.google.com) → buat spreadsheet baru
2. Rename sheet pertama menjadi: `Data Harian`
3. Di baris pertama, buat header (Row 1):
   ```
   A: Tanggal
   B: Nama
   C: Email
   D: Prioritas 1
   E: Selesai 1
   F: Prioritas 2
   G: Selesai 2
   H: Prioritas 3
   I: Selesai 3
   J: Checklist
   K: Habits
   L: Mood
   M: Notes
   N: Produktivitas
   ```

### Langkah 2 — Buat Google Apps Script
1. Di Google Sheet, klik **Extensions → Apps Script**
2. Hapus semua kode yang ada, ganti dengan ini:

```javascript
function doPost(e) {
  var sheet = SpreadsheetApp.getActiveSpreadsheet().getSheetByName('Data Harian');
  var data = JSON.parse(e.postData.contents);
  
  sheet.appendRow([
    data.tanggal,
    data.nama,
    data.email,
    data.prioritas1,
    data.selesai1,
    data.prioritas2,
    data.selesai2,
    data.prioritas3,
    data.selesai3,
    data.checklist,
    data.habits,
    data.mood,
    data.notes,
    data.produktivitas,
    new Date()
  ]);
  
  return ContentService
    .createTextOutput(JSON.stringify({status: 'ok'}))
    .setMimeType(ContentService.MimeType.JSON);
}
```

3. Klik **Save** (ikon disket), beri nama project misalnya "Daily Ihsan"
4. Klik **Deploy → New deployment**
5. Pilih type: **Web app**
6. Isi deskripsi, pilih:
   - **Execute as: Me**
   - **Who has access: Anyone**
7. Klik **Deploy** → **Authorize access** → pilih akun Google kamu
8. **Copy URL** yang muncul (bentuknya seperti `https://script.google.com/macros/s/ABC123.../exec`)

### Langkah 3 — Masukkan URL ke Aplikasi
1. Login ke website dengan akun **Admin**
2. Klik tab **Admin** (ikon ⚙)
3. Di bagian "Pengaturan Google Sheets", paste URL tadi
4. Klik **Simpan URL**
5. Sekarang tombol "Simpan ke Google Sheets" sudah terhubung!

---

## 👤 Pengaturan Akun

### Akun Admin
- Email admin **sudah dikonfigurasi** di dalam `index.html`
- Cari baris: `const ADMIN_EMAIL = 'ihsanpunya@gmail.com';`
- **Ganti** dengan email kamu sendiri sebelum deploy

### Menambah Pengguna
1. Login sebagai admin
2. Pergi ke tab **Admin**
3. Masukkan email yang ingin diizinkan, pilih role (User/Admin)
4. Klik **Tambah**
5. Pengguna tersebut sekarang bisa mendaftar akun dengan email itu

### Keamanan
- Data akun dan sesi tersimpan di **localStorage** browser
- Cocok untuk penggunaan pribadi & tim kecil
- Password di-encode dengan Base64 (tambahkan enkripsi lebih kuat jika perlu)

---

## 📱 Fitur

| Fitur | Keterangan |
|-------|-----------|
| ✅ Responsif | Optimal di HP, tablet, laptop |
| ✅ Multi-device | Bisa dibuka dari device manapun |
| ✅ Auth | Login dengan verifikasi email |
| ✅ Admin Panel | Kelola siapa yang bisa akses |
| ✅ Daily Checklist | Interaktif, bisa tambah/hapus |
| ✅ Time Blocking | Jadwal per jam |
| ✅ Habit Tracker | Toggle on/off |
| ✅ Mood Tracker | 5 level mood |
| ✅ Progress Bar | Auto-hitung produktivitas |
| ✅ Weekly Chart | Grafik 7 hari |
| ✅ Notes | Brain dump bebas |
| ✅ Google Sheets | Simpan data ke spreadsheet |
| ✅ Offline | Data tersimpan lokal dulu |

---

## 🔧 Kustomisasi

Edit `index.html` untuk mengubah:
- **Nama app**: cari `Daily Life Ihsan`
- **Email admin**: cari `ADMIN_EMAIL`
- **Checklist default**: cari `defaultChecks`
- **Habit default**: cari `defaultHabits`
- **Warna**: ubah variabel CSS di bagian `:root { }`

---

*Dibuat dengan ❤️ untuk disiplin dan produktivitas harian*
