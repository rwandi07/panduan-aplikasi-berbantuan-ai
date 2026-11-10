# Eksplorasi Pengalaman: [Nama Aplikasi]

> Letakkan di `docs/PENGALAMAN.md` di repo aplikasi.
> AI membacanya di awal sesi dan menambah entri bila: masalah sulit terpecahkan, sebuah cara gagal atau dibatalkan, ada kejutan dari alat/perangkat, atau kamu meminta `CATAT PENGALAMAN`.
> Entri terbaru di paling atas. Tulis dengan bahasa awam.
> Pengalaman yang berlaku untuk semua proyek, pindahkan juga ke Profil Pengembang-mu.

## Ringkasan rambu

> Daftar pendek pelajaran terpenting dari entri-entri di bawah. Ini yang paling sering dibaca AI.

- [contoh: Jangan pakai library X untuk membaca PDF hasil scan; hasilnya kosong. Pakai OCR.]
- [contoh: Tes kirim file selalu di Wi-Fi yang sama; jaringan kantor memblokir koneksi antarperangkat.]

---

## Entri

### P-002: [judul singkat] ([tanggal])

- **Apa yang terjadi:**
- **Penyebab:**
- **Yang sudah dicoba dan gagal:** (bila ada)
- **Yang akhirnya berhasil:**
- **Cara menghindarinya ke depan:**
- **Berlaku untuk proyek lain?** Ya / Tidak (bila ya, pindahkan ke Profil Pengembang)
- **Terkait:** (temuan BUG-xxx, commit, atau tag bila ada)

### P-001: [judul singkat] ([tanggal])

- **Apa yang terjadi:**
- **Penyebab:**
- **Yang sudah dicoba dan gagal:**
- **Yang akhirnya berhasil:**
- **Cara menghindarinya ke depan:**
- **Berlaku untuk proyek lain?**
- **Terkait:**

---

### Contoh entri yang baik

### P-000: Aplikasi menutup sendiri saat memilih file besar (3 Nov 2026)

- **Apa yang terjadi:** memilih video 2 GB membuat aplikasi langsung tertutup tanpa pesan.
- **Penyebab:** seluruh file dibaca ke memori sekaligus; RAM laptop tidak cukup.
- **Yang sudah dicoba dan gagal:** menambah batas memori aplikasi. Hanya menunda masalah.
- **Yang akhirnya berhasil:** file dikirim sedikit demi sedikit (per potongan), bukan sekaligus.
- **Cara menghindarinya ke depan:** setiap fitur yang membaca file harus dites dengan file besar (> 1 GB). Pemeriksaan ini sudah ditambahkan ke validator.
- **Berlaku untuk proyek lain?** Ya, untuk semua aplikasi yang membaca file.
- **Terkait:** BUG-004, tag v0.4.1
