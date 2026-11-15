# Link Asli — Website Unshortener

## Menjalankan secara lokal
1. Install Node.js versi 20 atau lebih baru.
2. Clone atau unduh repository ini.
3. Jalankan `npm install`.
4. Jalankan `npm start`.
5. Buka http://localhost:3000.

## Deploy ke Vercel
1. Buka https://vercel.com/new.
2. Login dan hubungkan akun GitHub.
3. Import repository `makmanmemek/Pemecah-semua-link`.
4. Biarkan pengaturan framework/build default terdeteksi otomatis untuk Express.
5. Klik **Deploy**. Folder `public` disajikan sebagai aset statis oleh Vercel.

Setiap commit baru ke branch utama akan memicu deployment otomatis setelah repository terhubung.

## Fitur dan batasan
- Mengikuti redirect HTTP (301, 302, 303, 307, 308).
- Banyak link sekaligus (maksimal 30), salin hasil.
- Tidak menjalankan JavaScript halaman atau melewati CAPTCHA/login.
- Sebagian situs memakai proteksi sehingga tidak semua link bisa diurai otomatis.
- Resolver membatasi jumlah redirect dan waktu tunggu serta menolak alamat lokal/privat.
- Sebelum digunakan publik dengan trafik besar, lakukan audit keamanan SSRF/DNS rebinding dan tambahkan rate limiting.
