# Background Remover Web

Aplikasi web sederhana untuk menghapus background gambar secara otomatis langsung di browser, tanpa perlu upload ke server. Dibangun dengan HTML, CSS, dan JavaScript.

## Fitur
- **Upload gambar** (JPG, PNG, WEBP, max 10MB)
- **Drag & drop** atau klik untuk memilih file
- **Pratinjau gambar asli dan hasil**
- **Penghapusan background otomatis** menggunakan deteksi warna dominan di tepi gambar
- **Download hasil** dengan background transparan (PNG)
- **UI modern** dan responsif
- Semua proses **langsung di browser** (client-side, tanpa backend)

## Cara Menggunakan
1. Buka `index.html` di browser modern (Chrome, Edge, Firefox, dsb)
2. Klik area upload atau drag & drop gambar ke area tersebut
3. Setelah gambar tampil, klik **Hapus Background**
4. Setelah proses selesai, klik **Download Hasil** untuk menyimpan gambar tanpa background

## Teknologi
- HTML5, CSS3 (custom style, responsive)
- JavaScript (tanpa library eksternal)
- Algoritma penghapusan background: deteksi warna dominan di tepi gambar, lalu transparansikan piksel serupa

## Catatan
- Hasil terbaik untuk gambar dengan background polos/warna solid
- Tidak cocok untuk background kompleks atau multiwarna
- Semua proses berjalan lokal, aman untuk privasi

## Lisensi
Proyek ini bebas digunakan untuk keperluan pribadi/non-komersial.

---

**Dibuat untuk latihan/magang.**
