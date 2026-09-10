# Website Permintaan Maaf

Website "surat permintaan maaf" interaktif: amplop yang dibuka dengan diklik/diketuk,
surat, galeri foto polaroid, dan bubble wrap yang bisa dipencet dengan pesan-pesan kecil.

## Cara mengganti isi
Semua teks (nama, tanggal, isi surat, foto, pesan bubble) ada di satu tempat:
buka `index.html`, cari bagian **KONFIGURASI** di dalam tag `<script>` menjelang akhir file,
lalu ubah sesuai kebutuhanmu.

Untuk pakai foto asli, ganti isi `foto` di KONFIGURASI, lalu di bagian JavaScript
polaroid ganti `style="background:..."` menjadi `<img src="nama-file.jpg">`
(taruh file foto di folder yang sama, lalu deploy ulang).

## Cara upload ke GitHub Pages
1. Buat repo baru di GitHub, misalnya `surat-maaf`.
2. Upload file `index.html` ini ke repo tersebut (lewat "Add file → Upload files").
3. Buka **Settings → Pages** di repo, pilih branch `main` dan folder `/ (root)`, lalu Save.
4. Tunggu 1-2 menit, situsmu akan aktif di `https://username.github.io/surat-maaf/`.
