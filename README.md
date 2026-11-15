# Link Asli — Website Unshortener

## Menjalankan
1. Install Node.js versi 18 atau lebih baru.
2. Ekstrak ZIP ini.
3. Jalankan `npm install`
4. Jalankan `npm start`
5. Buka http://localhost:3000

## Deploy
Deploy sebagai aplikasi Node.js/Express di hosting yang mendukung Node.js. Start command: `npm start`.

## Fitur dan batasan
- Mengikuti redirect HTTP (301, 302, 303, 307, 308).
- Banyak link sekaligus (maksimal 30), hapus duplikat, salin hasil.
- Tidak menjalankan JavaScript halaman atau melewati CAPTCHA/login.
- Sebagian situs memakai proteksi sehingga tidak semua link bisa diurai otomatis.
- Resolver membatasi redirect, waktu tunggu, dan menolak alamat lokal/privat. Sebelum dipublikasikan luas, lakukan audit keamanan SSRF/DNS rebinding dan tambahkan rate limiting.
