# Monitor Fundamental IDX: Panduan Instal di Android

Aplikasi ini adalah Progressive Web App (PWA). Setelah dipasang, aplikasi muncul sebagai ikon di layar utama, terbuka layar penuh tanpa bilah browser, dan tetap bisa dibuka tanpa internet. Data di dalamnya adalah snapshot per 23 November 2026.

Isi folder:
- `index.html` adalah aplikasinya (data, grafik, dan pustaka d3 sudah ada di dalam file ini).
- `manifest.webmanifest` dan `sw.js` membuat aplikasi bisa dipasang dan berjalan offline.
- `icons/` berisi ikon aplikasi.

Syarat dari Android: aplikasi harus dibuka dari alamat **https://**. File yang dibuka langsung dari penyimpanan ponsel tidak bisa dipasang sebagai aplikasi. Karena itu langkah pertama adalah menaruh folder ini di hosting gratis.

---

## Cara A (disarankan): GitHub Pages, lalu pasang dari Chrome

### 1. Unggah ke GitHub (sekali saja, sekitar 10 menit, dari laptop)
1. Buat akun gratis di https://github.com (lewati jika sudah punya).
2. Klik **New repository**. Beri nama, misalnya `monitor-idx`, pilih **Public**, lalu klik **Create repository**.
3. Di halaman repositori, klik **uploading an existing file**.
4. Ekstrak file zip, lalu seret **seluruh isi folder** (`index.html`, `manifest.webmanifest`, `sw.js`, folder `icons`) ke halaman unggah. Klik **Commit changes**.
5. Buka **Settings → Pages**. Pada *Branch*, pilih `main`, folder `/ (root)`, lalu klik **Save**.
6. Tunggu 1–2 menit. Alamat aplikasi muncul di bagian atas halaman, misalnya `https://namaanda.github.io/monitor-idx/`.

### 2. Pasang di ponsel Android
1. Buka alamat tadi di **Google Chrome** di ponsel.
2. Ketuk menu **⋮** di kanan atas, lalu pilih **Instal aplikasi**. Di sebagian ponsel pilihannya bernama **Tambahkan ke layar utama**, lalu **Instal**.
3. Ikon **Monitor IDX** muncul di layar utama atau laci aplikasi. Buka sekali saat online. Setelah itu aplikasi bisa dibuka tanpa internet.

## Cara B: membuat file APK dari aplikasi yang sudah di-hosting

Gunakan cara ini jika Anda ingin file `.apk` yang bisa dipasang atau dibagikan seperti aplikasi biasa.

1. Selesaikan **Cara A langkah 1** dulu sampai Anda punya alamat `https://…github.io/…`.
2. Di laptop, buka https://www.pwabuilder.com, tempel alamat tersebut, lalu klik **Start**.
3. Klik **Package for stores → Android → Generate Package**, lalu unduh file zip-nya.
4. Di dalam zip, cari file **`.apk`** dan kirim ke ponsel (lewat kabel, Google Drive, atau Telegram ke diri sendiri).
5. Di ponsel, ketuk file `.apk`. Jika diminta, izinkan **Instal aplikasi tidak dikenal** untuk aplikasi yang Anda pakai membuka file (File Manager, Drive, dan sebagainya), lalu ketuk **Instal**.

Catatan: APK dari PWABuilder tetap mengambil tampilan dari alamat GitHub Pages Anda. Jadi alamat itu harus tetap aktif. Setelah dibuka sekali, aplikasinya tetap jalan offline.

---

## Memperbarui data
1. Minta Claude membuat paket baru.
2. Di repositori GitHub, unggah ulang `index.html` dan `sw.js` (timpa file lama).
3. Buka aplikasi di ponsel saat online. Versi baru akan dimuat otomatis, kadang perlu tutup lalu buka sekali lagi.

## Privasi
GitHub Pages bersifat publik: siapa pun yang tahu alamatnya bisa membukanya. Data emitennya sendiri berasal dari sumber publik, tetapi penanda "di portofolio" menunjukkan saham yang Anda pegang. Jika itu masalah, minta versi tanpa penanda portofolio sebelum mengunggah.
