# 📺 Sistem Antrian TV & Kontroler Web (Vercel Ready)

Aplikasi Display Antrian TV dengan tema **Clean Dark Blue**, pembatas tab hitam tegas, siaran YouTube anti-Error 153, dan kontroler web interaktif.

---

## 🎯 Fitur Utama

1. **Clean Dark Blue UI**: Desain futuristik dengan warna dasar biru gelap (#040814), aksen cyann glowing, dan border pemisah warna **Hitam Tegas (Pure Black)**.
2. **YouTube Video / Playlist Integrasi (Error 153 Fix)**: Menggunakan Official YouTube JS iFrame API yang kompatibel dengan browser TV Android seperti **BrowserHere by TCL**, menghindari pembatasan error 153.
3. **Panggil Suara (Text-to-Speech)**: Fitur panggil suara otomatis dalam Bahasa Indonesia (`"Nomor antrian 001, silakan menuju loket 1"`).
4. **Kontrol Penuh dari HP / Tablet**: Kontroler web responsif yang mudah diakses dari browser smartphone.
5. **Real-time Sync**: Menggunakan **Firebase Realtime Database** gratis untuk sinkronisasi seketika tanpa delay.

---

## 📁 Struktur File

- [`display.html`](file:///d:/ANTIGRAVITY/antrian-tv/display.html) : Halaman Utama Tampilan Layar TV.
- [`index.html`](file:///d:/ANTIGRAVITY/antrian-tv/index.html) : Halaman Pengontrol (Controller) dari Smartphone/Tablet.
- [`firebase-config.js`](file:///d:/ANTIGRAVITY/antrian-tv/firebase-config.js) : File konfigurasi kredensial Firebase Database.
- [`vercel.json`](file:///d:/ANTIGRAVITY/antrian-tv/vercel.json) : Konfigurasi routing otomatis untuk Vercel.

---

## 🚀 Langkah Deploy Cepat ke Vercel

### 1. Buat Firebase Realtime Database (Gratis)
1. Buka [Firebase Console](https://console.firebase.google.com/) dan buat project baru.
2. Ke menu **Build → Realtime Database** → Klik **Create Database**.
3. Pilih lokasi server (singapore/asia) dan pilih mode **Start in test mode** (agar dapat dibaca/ditulis tanpa login).
4. Masuk ke **Rules** pada Realtime Database, pastikan isinya:
   ```json
   {
     "rules": {
       ".read": true,
       ".write": true
     }
   }
   ```
5. Buka **Project Settings** (ikon gerigi) → Scroll ke bawah ke bagian **Your apps** → Tambahkan Web App `</>`.
6. Salin objek `firebaseConfig` dan tempelkan ke file [`firebase-config.js`](file:///d:/ANTIGRAVITY/antrian-tv/firebase-config.js).

---

### 2. Deploy ke Vercel (Gratis)

**Cara A: Lewat Vercel CLI / Terminal**
1. Jalankan perintah di folder project:
   ```bash
   npx vercel
   ```
2. Ikuti petunjuk di terminal sampai selesai.

**Cara B: Upload ke GitHub & Import ke Vercel**
1. Upload semua file project ini ke repositori GitHub.
2. Buka [Vercel Dashboard](https://vercel.com/dashboard) → Klik **Add New Project**.
3. Import repositori GitHub tersebut dan klik **Deploy**.

---

## 📱 Cara Penggunaan

1. **Di TV Android / TCL (BrowserHere)**:
   - Buka alamat Vercel kamu ditambahkan `/display` (Contoh: `https://antrian-tv.vercel.app/display`).
   - Masukkan ke mode Fullscreen.

2. **Di HP / Tablet Pengontrol**:
   - Buka alamat utama Vercel kamu (Contoh: `https://antrian-tv.vercel.app`).
   - Gunakan tombol **PANGGIL NEXT**, **RECALL**, atau ganti Video YouTube ID & Running Text secara langsung!
