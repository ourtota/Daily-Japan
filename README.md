# Daily Japan — Versi Publik

Aplikasi web belajar Bahasa Jepang harian (satu file HTML, GitHub Pages) untuk pengguna umum Daily Japan, terpisah dari versi keluarga.

## Cara kerja

- **Aktivasi:** pengguna memasukkan *kode akses* unik dari admin + nama. Kode, nama, dan ID perangkat tersimpan hanya di perangkat (localStorage `djp.*`).
- **Server pusat:** satu Apps Script Web App melayani semua pengguna & level (N5–N1): mengambil materi, mencatat hasil quiz dan progres, serta menghitung streak.
- **Level terkunci:** N2 terbuka setelah lulus 7 hari berturut-turut (≥9/10) di N3; N1 setelah lulus 7 hari berturut-turut di N2. Hanya percobaan quiz *pertama* setiap hari yang dicap **Resmi** oleh server; sisanya **Latihan**.
- **Offline:** materi ter-cache di perangkat; hasil quiz/progres yang gagal terkirim masuk antrean dan dikirim ulang saat app dibuka lagi.
- **Data contoh:** `seed.json` berisi 3 hari contoh per level (tanggal dipetakan dinamis ke hari ini/kemarin/lusa menurut Asia/Tokyo) — dipakai hanya sebelum data server tersedia.
- **Hiragana & Katakana:** modul tetap 10 bab; konten diambil dari server (`action=kana`) dengan cadangan `seed-kana.json`.

## Berkas

| Berkas | Isi |
|---|---|
| `index.html` | Aplikasi lengkap (UI + logika) |
| `seed.json` | 3 hari contoh × 5 level |
| `seed-kana.json` | Cadangan konten modul Hiragana & Katakana |
| `hasian.gif` | Avatar di header |
| `index-base-keluarga.html` | Berkas acuan versi keluarga (tidak dipakai app) |
