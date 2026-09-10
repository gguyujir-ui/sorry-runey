# Website Permintaan Maaf

Website "surat permintaan maaf" interaktif: amplop yang dibuka dengan diklik/diketuk,
surat, galeri foto polaroid, bubble wrap yang bisa dipencet, dan lagu yang otomatis
main saat amplop dibuka.

## Cara mengganti isi
Semua teks (nama, tanggal, isi surat, foto, pesan bubble, musik) ada di satu tempat:
buka `index.html`, cari bagian **KONFIGURASI** di dalam tag `<script>` menjelang akhir file,
lalu ubah sesuai kebutuhanmu.

Untuk pakai foto asli, ganti isi `foto` di KONFIGURASI, lalu di bagian JavaScript
polaroid ganti `style="background:..."` menjadi `<img src="nama-file.jpg">`
(taruh file foto di folder yang sama, lalu deploy ulang).

## Cara menambahkan lagu
1. Siapkan file musik (format `.mp3`), pastikan kamu punya izin untuk memakainya.
2. Taruh file tersebut di folder yang sama dengan `index.html`, misalnya beri nama `lagu.mp3`.
3. Di bagian KONFIGURASI, ubah:
   ```js
   musik: {
     file: "lagu.mp3",   // sesuaikan dengan nama file musikmu
     judul: "With Love"  // teks yang tampil di pill pemutar musik
   }
   ```
4. Lagu akan otomatis coba diputar begitu amplop diketuk. Kalau browser
   memblokir autoplay, orang yang buka situs tinggal tap pill musik di atas.

## Cara upload ke GitHub Pages
1. Buat repo baru di GitHub, misalnya `surat-maaf`.
2. Upload `index.html` (dan file musik/foto kalau ada) ke repo tersebut lewat "Add file → Upload files".
3. Buka **Settings → Pages** di repo, pilih branch `main` dan folder `/ (root)`, lalu Save.
4. Tunggu 1-2 menit, situsmu akan aktif di `https://username.github.io/surat-maaf/`.
