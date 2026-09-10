# Website Permintaan Maaf — "Maaf, Bestie..."

Website satu-halaman (semua di `index.html`), nada santai buat sahabat (bukan romantis):

1. **Landing** — judul "Maaf, Bestie..." + tombol Mulai
2. **Amplop** — diketuk untuk buka, lalu pilih **Baca** atau **Aku butuh waktu lagi**
3. **Surat** — lagu otomatis coba diputar begitu layar ini kebuka + isi surat
4. **Minta maaf** — pertanyaan "Kamu mau maafin aku, nggak?" dengan pilihan Ya / butuh waktu lagi
5. **Game interaktif "Sambung Lagi"** — pencet tos 🤝 yang muncul buat menyambungkan jembatan pertemanan, nggak pakai tema hati-hati romantis
6. **Penutup** — janji + ucapan santai buat bestie

## Musik otomatis diputar
Begitu layar **surat** terbuka, situs otomatis mencoba memutar file musik yang kamu atur di KONFIGURASI.
Kalau browser memblokir autoplay (kebijakan sebagian browser), tombol ▶ di kartu lagu tetap bisa dipencet manual.

## Cara mengganti isi
Semua teks, isi surat, dan pengaturan game ada di satu tempat: buka `index.html`,
cari bagian **KONFIGURASI** di dalam tag `<script>`, lalu ubah sesuai kebutuhanmu:

- `paragrafSurat` — isi surat (array paragraf)
- `musik` — nama file lagu, judul, dan artis
- `jumlahHatiJembatan` — jumlah tos yang perlu dipencet untuk menyelesaikan game

Judul dan teks tiap layar bisa diedit langsung di bagian HTML masing-masing
`<section class="screen" data-screen="...">`.

## Cara menambahkan lagu
1. Siapkan file musik format `.mp3` yang kamu punya izin untuk memakainya.
2. Taruh file itu di folder yang sama dengan `index.html`, misal `lagu.mp3`.
3. Di KONFIGURASI, sesuaikan:
   ```js
   musik: {
     file: "lagu.mp3",
     judul: "Judul Lagu",
     artis: "Nama Artis"
   }
   ```

## Cara upload ke GitHub Pages
1. Buat repo baru di GitHub, misalnya `maaf-bestie`.
2. Upload `index.html` (dan file musik kalau ada) lewat "Add file → Upload files".
3. Buka **Settings → Pages**, pilih branch `main` dan folder `/ (root)`, lalu Save.
4. Situsmu aktif di `https://username.github.io/maaf-bestie/` setelah 1-2 menit.
