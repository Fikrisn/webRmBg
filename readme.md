# 🎨 Background Remover Web

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)](https://html.spec.whatwg.org/)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)](https://www.w3.org/Style/CSS/)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)](https://www.ecma-international.org/publications-and-standards/standards/ecma-262/)

Aplikasi web sederhana dan cepat untuk menghapus background gambar secara otomatis langsung di browser Anda. Tidak perlu upload ke server, semua proses berjalan secara lokal untuk menjaga privasi dan keamanan data Anda.

## ✨ Fitur Utama

- 🚀 **Proses Cepat**: Penghapusan background dalam hitungan detik
- 📁 **Upload Fleksibel**: Mendukung drag & drop atau klik untuk memilih file
- 🖼️ **Pratinjau Real-time**: Lihat gambar asli dan hasil side-by-side
- 🎯 **Akurat**: Algoritma deteksi warna dominan untuk hasil optimal
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

## 🚀 Instalasi & Penggunaan

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

3. **Mulai Menggunakan**
   - Klik area upload atau drag & drop gambar
   - Tunggu gambar diproses
   - Klik "Hapus Background"
   - Download hasil sebagai PNG transparan

### Format File yang Didukung
- **JPG/JPEG**: Format gambar kompresi
- **PNG**: Format dengan transparansi
- **WEBP**: Format modern dengan kompresi tinggi
- **Ukuran Maksimal**: 10MB per file

## 🔧 Cara Kerja Algoritma

Aplikasi ini menggunakan algoritma sederhana namun efektif:

1. **Deteksi Background**: Mengambil sampel warna dari sudut dan tepi gambar
2. **Analisis Warna**: Menghitung rata-rata warna background dominan
3. **Penghapusan**: Membandingkan setiap piksel dengan warna background
4. **Feathering**: Menerapkan efek halus pada tepi untuk hasil natural
5. **Transparansi**: Mengubah piksel background menjadi transparan

### Parameter Algoritma
- **Tolerance**: 50 (sensitivitas deteksi warna)
- **Sample Points**: 8 titik (sudut dan tengah tepi)
- **Feathering**: Distance-based alpha blending

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

## 🛠️ Troubleshooting

### Masalah Umum dan Solusi

**❌ Gambar tidak terdeteksi sebagai background**
- Pastikan background memiliki warna yang konsisten
- Coba gambar dengan kontras yang lebih tinggi
- Gunakan gambar dengan resolusi yang lebih baik

**❌ Hasil download tidak transparan**
- Pastikan browser mendukung Canvas API
- Coba refresh halaman dan ulangi proses
- Gunakan browser terbaru

**❌ Aplikasi lambat atau crash**
- Kurangi ukuran gambar (maksimal 10MB)
- Tutup tab browser lain
- Restart browser

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
- **Canvas API**: Untuk manipulasi gambar
- **Blob API**: Untuk membuat file download
- **URL API**: Untuk generate download link

## 🤝 Kontribusi

Kontribusi sangat diterima! Silakan ikuti langkah berikut:

1. Fork repository ini
2. Buat branch fitur baru (`git checkout -b feature/AmazingFeature`)
3. Commit perubahan (`git commit -m 'Add some AmazingFeature'`)
4. Push ke branch (`git push origin feature/AmazingFeature`)
5. Buat Pull Request

### Area yang Bisa Dikembangkan
- [ ] Algoritma penghapusan background yang lebih canggih
- [ ] Dukungan untuk format gambar tambahan
- [ ] Batch processing untuk multiple images
- [ ] Integration dengan WebAssembly untuk performa lebih baik
- [ ] UI/UX improvements
- [ ] PWA (Progressive Web App) features

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