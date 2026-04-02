# 🎨 Background Remover Web cuy

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)](https://html.spec.whatwg.org/)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)](https://www.w3.org/Style/CSS/)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)](https://www.ecma-international.org/publications-and-standards/standards/ecma-262/)

Aplikasi web sederhana dan cepat untuk menghapus background gambar secara otomatis langsung di browser Anda. Tidak perlu upload ke server, semua proses berjalan secara lokal untuk menjaga privasi dan keamanan data Anda.

## ✨ Fitur Utama

- 🚀 **Proses Cepat**: Penghapusan background dalam hitungan detik
- 📁 **Upload Fleksibel**: Mendukung drag & drop atau klik untuk memilih file
- 🖼️ **Pratinjau Real-time**: Lihat gambar asli dan hasil side-by-side
- 🎯 **Akurat & Presisi**: Algoritma deteksi warna dominan dengan morphological operations
- ✏️ **Editing Manual**: Tools pen dan eraser untuk fine-tuning hasil
- 🎨 **Kontrol Brush**: Sesuaikan ukuran brush dan sensitivitas
- ↩️ **Undo/Redo**: Kembalikan perubahan dengan mudah
- 💾 **Download Mudah**: Simpan hasil sebagai PNG transparan
- 📱 **Responsif**: UI modern yang bekerja di desktop dan mobile
- 🔒 **Privasi Aman**: Semua proses berjalan di browser, data tidak dikirim ke server
- 🎨 **UI Modern**: Desain yang menarik dengan animasi halus

## 📋 Persyaratan Sistem

### Browser yang Didukung
- ✅ Chrome 70+
- ✅ Firefox 65+
- ✅ Safari 12+
- ✅ Edge 79+
- ✅ Opera 57+

### Spesifikasi Minimum
- **RAM**: 512MB
- **Storage**: 50MB untuk file aplikasi
- **Resolusi**: 1024x768 atau lebih tinggi

## 🚀 Instalasi & Penggunaan....

### Cara Menjalankan

1. **Download atau Clone Repository**
   ```bash
   git clone https://github.com/Fikrisn/webRmBg.git
   cd webRmBg
   ```

2. **Buka di Browser**
   - Buka file `index.html` langsung di browser modern Anda
   - Atau gunakan server lokal untuk pengalaman terbaik:
     ```bash
     # Menggunakan Python
     python -m http.server 8000

     # Atau menggunakan Node.js
     npx http-server
     ```

3. **Proses Gambar**
   - Klik area upload atau drag & drop gambar
   - Tunggu gambar diproses otomatis
   - Klik "Manual" untuk editing lebih lanjut

4. **Editing Manual (Opsional)**
   - **Pen Tool**: Klik untuk menghapus area yang tidak terdeteksi
   - **Eraser Tool**: Klik untuk memulihkan area yang terhapus salah
   - **Brush Size**: Sesuaikan ukuran kuas untuk presisi
   - **Tolerance**: Atur sensitivitas deteksi warna
   - **Undo/Redo**: Kembalikan perubahan jika diperlukan

5. **Download Hasil**
   - Klik "Download Hasil" untuk menyimpan sebagai PNG transparan
   - File akan tersimpan dengan background transparan

### Format File yang Didukung
- **JPG/JPEG**: Format gambar kompresi
- **PNG**: Format dengan transparansi
- **WEBP**: Format modern dengan kompresi tinggi
- **Ukuran Maksimal**: 10MB per file

## 🔧 Cara Kerja Algoritma

Aplikasi ini menggunakan algoritma canggih untuk hasil yang lebih presisi:

1. **Deteksi Background Enhanced**: Mengambil sampel warna dari sudut, tepi, dan titik strategis lainnya
2. **Analisis Warna Weighted**: Menghitung rata-rata warna background dengan bobot yang berbeda
3. **Pembuatan Mask**: Membuat mask biner dengan kontrol tolerance yang dapat disesuaikan
4. **Morphological Operations**: Menerapkan dilate dan erode untuk membersihkan mask
5. **Feathering**: Menerapkan smoothing pada tepi untuk hasil natural
6. **Editing Manual**: Tools pen dan eraser untuk fine-tuning hasil

### Parameter Algoritma
- **Tolerance**: 10-100 (sensitivitas deteksi warna)
- **Brush Size**: 5-50px (untuk editing manual)
- **Sample Points**: 13 titik strategis untuk deteksi background
- **Morphological Kernel**: 3x3 untuk operasi dilate/erode
- **History Limit**: 20 state untuk undo/redo

### Tools Editing Manual
- **Pen Tool**: Menghapus area yang dipilih (membuat transparan)
- **Eraser Tool**: Memulihkan area yang terhapus (membuat opaque)
- **Brush Size Control**: Mengatur ukuran kuas untuk presisi
- **Tolerance Slider**: Mengatur sensitivitas deteksi warna

## 📖 Contoh Penggunaan

### Skenario 1: Foto Produk
```
Input: foto-produk.jpg (background putih)
Output: produk-transparan.png
Hasil: Produk siap digunakan untuk e-commerce
```

### Skenario 2: Foto Profil
```
Input: selfie.jpg (background kompleks)
Output: profil-transparent.png
Hasil: Foto profil dengan background transparan
```

## 🛠️ Troubleshooting....

### Masalah Umum dan Solusi

**❌ Gambar tidak terdeteksi sebagai background**
- Pastikan background memiliki warna yang konsisten
- Coba gambar dengan kontras yang lebih tinggi
- Gunakan gambar dengan resolusi yang lebih baik
- Sesuaikan tolerance slider ke nilai yang lebih rendah

**❌ Hasil download tidak transparan**
- Pastikan browser mendukung Canvas API
- Coba refresh halaman dan ulangi proses
- Gunakan browser terbaru
- Pastikan tidak ada masalah dengan editing manual

**❌ Tools editing tidak berfungsi**
- Pastikan mode "Manual" sudah aktif
- Coba refresh halaman jika ada masalah JavaScript
- Pastikan browser mendukung event listeners
- Gunakan mouse atau touch yang kompatibel

**❌ Undo/Redo tidak berfungsi**
- Pastikan sudah melakukan editing manual terlebih dahulu
- History terbatas pada 20 langkah terakhir
- Jika history penuh, langkah tertua akan dihapus

**❌ Aplikasi lambat atau crash**
- Kurangi ukuran gambar (maksimal 10MB)
- Tutup tab browser lain
- Restart browser
- Kurangi brush size untuk performa lebih baik

**❌ Pen tool menghapus area yang salah**
- Kurangi tolerance untuk sensitivitas yang lebih rendah
- Gunakan brush size yang lebih kecil
- Gunakan eraser tool untuk memperbaiki kesalahan

**❌ Drag & drop tidak berfungsi**
- Gunakan tombol "Pilih Gambar" sebagai alternatif
- Pastikan file gambar valid

### Tips untuk Hasil Terbaik
- Gunakan gambar dengan background polos
- Pastikan subjek memiliki kontras yang cukup dengan background
- Hindari gambar dengan bayangan atau pencahayaan kompleks
- Gunakan resolusi gambar yang tidak terlalu tinggi

## 🏗️ Teknologi & Arsitektur

### Frontend Stack
- **HTML5**: Struktur dan semantic markup
- **CSS3**: Custom styling dengan animasi dan responsivitas
- **Vanilla JavaScript**: Logika aplikasi tanpa framework

### Algoritma Utama
```javascript
// Deteksi warna background
const avgBg = calculateAverageBackground(data, samplePoints);

// Penghapusan background dengan tolerance
for (let i = 0; i < data.length; i += 4) {
    const distance = calculateColorDistance(pixel, avgBg);
    if (distance < tolerance) {
        data[i + 3] = 0; // Set alpha to transparent
    }
}
```

### Browser APIs yang Digunakan
- **File API**: Untuk membaca file gambar
- **Canvas API**: Untuk manipulasi gambar dan drawing manual
- **Blob API**: Untuk membuat file download
- **URL API**: Untuk generate download link
- **Pointer Events**: Untuk interaksi mouse dan touch
- **ImageData API**: Untuk pemrosesan piksel tingkat rendah

## 🤝 Kontribusi

Kontribusi sangat diterima! Silakan ikuti langkah berikut:

1. Fork repository ini
2. Buat branch fitur baru (`git checkout -b feature/AmazingFeature`)
3. Commit perubahan (`git commit -m 'Add some AmazingFeature'`)
4. Push ke branch (`git push origin feature/AmazingFeature`)
5. Buat Pull Request

### Area yang Bisa Dikembangkan
- [x] **Manual Editing Tools**: Pen dan eraser untuk fine-tuning
- [x] **Enhanced Algorithm**: Morphological operations dan feathering
- [x] **Undo/Redo System**: History management untuk editing
- [x] **Brush Size Control**: Kontrol ukuran kuas yang dapat disesuaikan
- [x] **Tolerance Slider**: Kontrol sensitivitas deteksi warna
- [ ] **Batch Processing**: Proses multiple images sekaligus
- [ ] **AI-Powered Detection**: Menggunakan machine learning untuk deteksi yang lebih baik
- [ ] **Shape Tools**: Rectangle, circle, dan lasso selection
- [ ] **Layer System**: Multiple layers untuk editing kompleks
- [ ] **Filter Effects**: Blur, sharpen, dan efek lainnya
- [ ] **Export Options**: Format JPG, WebP, dan SVG
- [ ] **Cloud Integration**: Upload ke cloud storage
- [ ] **PWA Features**: Install sebagai aplikasi native

## 📄 Lisensi

Distributed under the MIT License. See `LICENSE` for more information.

```
MIT License

Copyright (c) 2025 Fikrisn

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.
```

## 📞 Kontak & Dukungan

- **Author**: Fikrisn
- **GitHub**: [@Fikrisn](https://github.com/Fikrisn)
- **Email**: fikrisn@example.com
- **Project Link**: [https://github.com/Fikrisn/webRmBg](https://github.com/Fikrisn/webRmBg)

## 🙏 Acknowledgments

- Terima kasih kepada komunitas open source
- Inspirasi dari berbagai tools penghapus background online
- Dokumentasi MDN Web Docs untuk referensi API browser

---

**⭐ Jika proyek ini bermanfaat, berikan star di GitHub!**
