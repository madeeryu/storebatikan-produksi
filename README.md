# Store Batik AN — Monitoring Produksi

Aplikasi PWA (satu file) untuk monitoring produksi batik cap **Batik AN** (Indramayu).
Menggantikan papan tulis monitoring: pelacakan kodi per tahap (WIP), input hasil harian
pekerja, deteksi hasil mengendap, beban antrian pengobat, stok bahan, dan HPP per kodi/warna.

Satu database & autentikasi dengan app Grosir (Firebase project `store-batik-an`).
Batch yang selesai otomatis bisa dikirim menjadi stok barang jadi di app Grosir.

## Deploy
File tunggal `index.html` — bisa langsung dihost di:
- **GitHub Pages**: Settings → Pages → Branch `main` / root.
- **Vercel / Netlify**: import repo, tanpa build command (output = root).

## Penggunaan singkat
1. Login dengan akun owner (sama dengan app Grosir).
2. Menu **Master Data → Isi Data Awal** (sekali di awal): mengisi golongan, tipe, warna,
   alur tahapan (Poman cabang A/B, Trusmian, Lebar), pekerja, bahan, dan konfigurasi HPP.
3. **Batch & WIP**: buat batch + rincian kodi per warna.
4. **Papan Tulis**: catat hasil harian pekerja — WIP otomatis pindah ke tahap berikutnya.

## Teknologi
HTML + JS modular, Firebase (Firestore + Auth), tanpa build step.
