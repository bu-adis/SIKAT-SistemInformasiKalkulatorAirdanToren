# 💧 Sistem Informasi Kalkulator Air dan Toren

Aplikasi web interaktif untuk menghitung kebutuhan air bersih dan menentukan kapasitas toren (tandon) sesuai **SNI 03-7065-2005**.

Dibuat sebagai bahan ajar mata pelajaran Utilitas Bangunan, program keahlian **Desain Pemodelan dan Informasi Bangunan (DPIB)**, SMK Negeri 8 Pontianak.

🔗 **Repositori:** https://github.com/bu-adis/SIKAT-SistemInformasiKalkulatorAirdanToren

---

## ✨ Fitur

- **Pilihan jenis bangunan** lengkap dengan standar pemakaian air per hari menurut SNI (rumah tinggal, rumah susun, asrama, sekolah, kantor, rumah sakit, hotel, tempat ibadah, dan lainnya).
- **Input jumlah pengguna** (penghuni, siswa, pegawai, atau tempat tidur, menyesuaikan jenis bangunan).
- **Cadangan air yang bisa diatur** (0–50%, bawaan 20%).
- **Dua pilihan sistem:**
  - toren tunggal di atas (sistem langsung), atau
  - tandon bawah + toren atas (sistem dual), dengan porsi toren atas yang bisa diatur (10–50% dari kebutuhan harian, bawaan 20%).
- **Rekomendasi ukuran toren komersial** yang umum dijual di pasaran (250 L – 30.000 L), dibulatkan ke ukuran terdekat di atas kebutuhan.
- **Visualisasi tingkat isi toren** dalam bentuk gambar SVG.
- **Lampiran acuan SNI** di dalam aplikasi: dasar perhitungan, Tabel 1 pemakaian air dingin minimum, ketentuan umum tangki, dan panduan memilih sistem toren.
- Tampilan **responsif**, nyaman dibuka di HP maupun komputer.

## 🧮 Cara Perhitungan

```
Kebutuhan dasar (L/hari) = jumlah pengguna × standar pemakaian air (L/orang/hari)
Kebutuhan total (L/hari) = kebutuhan dasar × (1 + cadangan%)
```

**Sistem toren tunggal:** kapasitas toren = kebutuhan total, lalu dipilih ukuran komersial terdekat di atasnya.

**Sistem tandon bawah + toren atas:**

```
Tandon bawah = kebutuhan total (100% kebutuhan harian)
Toren atas   = kebutuhan total × porsi toren atas (%)
```

Keduanya dipilih ke ukuran komersial terdekat di atas hasil hitung.

### Contoh

Rumah tinggal dengan 5 penghuni, cadangan 20%:

```
Kebutuhan dasar = 5 × 120       = 600 L/hari
Kebutuhan total = 600 × 1,20    = 720 L/hari
```

Toren yang disarankan: ukuran komersial terdekat di atas 720 L, yaitu **1.000 L**.

## 🚀 Cara Menggunakan

1. Pilih **jenis bangunan**.
2. Isi **jumlah pengguna**.
3. Atur **cadangan air** dengan penggeser.
4. Pilih **sistem toren** (tunggal atau tandon bawah + toren atas).
5. Baca **hasil rekomendasi** di panel hasil.
6. Buka **Lampiran** untuk melihat aturan dan tabel acuan SNI.

## 🛠️ Menjalankan Secara Lokal

Aplikasi ini berupa satu file HTML, tidak perlu instalasi.

1. Unduh file `kalkulator-toren-air.html` (atau `index.html` jika sudah diganti namanya).
2. Buka file tersebut di browser (Chrome, Edge, Firefox, Safari).

> **Catatan untuk pengguna HP:** jika file terbuka sebagai teks di aplikasi lain (misalnya WPS), pilih "Buka di browser" (Chrome atau Safari).

Font ditampilkan dari Google Fonts, jadi tampilan terbaik didapat saat terhubung internet. Tanpa internet, perhitungan tetap berjalan dengan font bawaan perangkat.

## 📚 Acuan

- SNI 03-7065-2005, *Tata Cara Perencanaan Sistem Plambing*, Badan Standardisasi Nasional.

## ⚠️ Catatan Penggunaan

Ukuran toren komersial dalam aplikasi ini adalah daftar kapasitas yang umum dijual di pasaran. Untuk proyek nyata, periksa kembali katalog produsen toren setempat karena ukuran yang tersedia bisa berbeda antar merek. Aplikasi ini ditujukan untuk **keperluan pembelajaran**.

## 👩‍🏫 Pembuat

**Adisthya Mellisa Rukmana, ST.**
Guru DPIB, SMK Negeri 8 Pontianak

## 📄 Lisensi

Proyek ini dilisensikan di bawah [Lisensi MIT](LICENSE).

Kamu bebas menggunakan, menyalin, mengubah, dan membagikan proyek ini, dengan syarat tetap mencantumkan pemberitahuan hak cipta dan teks lisensi dari pembuat (Adisthya Mellisa Rukmana, ST.).
