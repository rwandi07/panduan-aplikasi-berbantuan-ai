# Kamus UI: Rapi, Simple, dan Menarik

Hampir semua orang kesulitan menjelaskan "tampilan yang menarik" dengan kata-kata, termasuk desainer profesional. Karena itu panduan ini memakai dua cara:

1. **Kamu memilih, bukan menjelaskan.** AI menunjukkan pilihan, kamu menunjuk yang disukai.
2. **Kata-katamu punya arti yang sudah disepakati.** Saat kamu bilang "rapi", AI mana pun menafsirkannya dengan cara yang sama, berdasarkan kamus di bawah.

---

## 1. Alur memilih tampilan (UI Discovery)

1. **Referensi.** AI mengumpulkan 3–5 contoh tampilan dari aplikasi sejenis dan pedoman desain resmi platform.
2. **Pilih.** Kamu menunjuk yang disukai, boleh campuran: *"warna nomor 2, tata letak nomor 4"*.
3. **Mockup.** AI membuat 1–3 gambar rancangan sebelum menulis kode. Mengubah gambar jauh lebih murah daripada mengubah aplikasi jadi.
4. **Tanggapi.** Kamu boleh bilang *"terlalu ramai"*, *"terlalu polos"*, *"tombolnya kurang kelihatan"*. Itu sudah cukup.
5. **Bangun.** Setelah kamu puas dengan mockup, baru dibuat kodenya.

> *"Carikan referensi tampilan untuk aplikasi seperti ini, lalu buatkan 2–3 mockup dengan gaya berbeda: satu minimalis, satu berwarna, satu mode gelap."*

---

## 2. Kamus

### Rapi
- Jarak antar elemen konsisten (memakai kelipatan yang sama, misalnya 8 piksel).
- Semua elemen sejajar pada garis yang sama; tidak ada yang "melenceng".
- Maksimal 2 jenis huruf; ukuran huruf hanya beberapa tingkat (judul, subjudul, isi, keterangan).
- Tombol sejenis punya ukuran dan bentuk yang sama.
- Tidak ada teks yang terpotong atau bertumpuk, di layar kecil maupun besar.

### Simple
- Satu aksi utama per layar, ditampilkan paling menonjol.
- Opsi lanjutan disembunyikan di menu "Pengaturan" atau "Lainnya".
- Label memakai kata sehari-hari, bukan istilah teknis.
- Langkah sesedikit mungkin untuk tugas yang paling sering dilakukan.
- Tidak ada elemen hiasan yang tidak punya fungsi.

### Menarik
- Satu warna aksen untuk hal penting (tombol utama, status aktif); sisanya warna netral.
- Kontras teks dan latar jelas, mudah dibaca.
- Ikon dari satu set yang sama gayanya.
- Sudut membulat dan bayangan dipakai secara konsisten.
- Animasi halus dan singkat saat berpindah layar atau menekan tombol, tidak berlebihan.
- Ada tampilan ramah saat kosong ("Belum ada file, tekan + untuk menambah") dan saat gagal.

### Modern
- Mengikuti pedoman desain terbaru platformnya (lihat bagian 3).
- Mendukung mode gelap bila platformnya mendukung.
- Banyak ruang kosong; tidak padat.

### Profesional
- Konsisten di semua layar: warna, huruf, ikon, dan istilah yang sama.
- Pesan error sopan, menjelaskan apa yang terjadi dan apa yang bisa dilakukan.
- Ada halaman "Tentang" dengan nama aplikasi, versi, dan pembuat.

---

## 3. Ikuti pedoman resmi platform

Cara paling mudah mendapat tampilan "seperti aplikasi profesional" adalah mengikuti pedoman desain resmi:

| Platform | Pedoman |
|---|---|
| Android | Material Design (Google) |
| Windows | Fluent Design (Microsoft) |
| iOS / macOS | Human Interface Guidelines (Apple) |
| Web | Pilih satu sistem desain yang umum dan konsisten |

> *"Ikuti pedoman desain resmi platform ini, kecuali bila bertentangan dengan identitas visual saya."*

---

## 4. Identitas visual (opsional)

Kalau kamu membuat beberapa aplikasi, pertimbangkan **satu identitas visual** supaya semua terlihat seperti satu keluarga. Kamu cukup memutuskan selera sekali; setelah itu tiap proyek tinggal memakainya.

Simpan di file `BRAND.md` (formatnya di [template/BRAND.md](../template/BRAND.md)): logo, warna, huruf, gaya ikon, dan aturan penulisan nama aplikasi.

Tips logo dan ikon aplikasi:
- **Buat logo induk dalam format vektor (SVG)** supaya tetap tajam di ukuran apa pun.
- **Ikon di layar HP sangat kecil (±1 cm).** Tulisan di dalam ikon tidak terbaca, padahal sistem sudah menampilkan nama aplikasi di bawah ikon. Siapkan dua versi:
  - **ikon tanpa tulisan** untuk layar utama HP atau taskbar;
  - **logo dengan nama aplikasi** untuk splash screen dan halaman "Tentang".
- **Nama aplikasi di bawah logo** memakai satu jenis huruf, satu gaya penulisan (misalnya Huruf Kapital Di Awal Kata), dan posisi yang sama di semua aplikasi.
- **Latar ikon seragam**, misalnya semua memakai kotak putih bersudut bulat.

---

## 5. Memeriksa tampilan yang sudah jadi

Kirim screenshot ke AI:

> *"Periksa screenshot ini memakai Kamus UI. Sebutkan bagian yang belum rapi, belum simple, atau kurang menarik. Usulkan perbaikan, jangan langsung ubah kodenya."*
