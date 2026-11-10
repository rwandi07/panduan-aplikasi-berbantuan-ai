# Aplikasi dengan Fitur AI di Dalamnya

Halaman ini berlaku kalau **aplikasimu sendiri memakai AI**: misalnya merangkum teks, menerjemahkan, mengenali tulisan di gambar, atau menjawab pertanyaan. Ini berbeda dari "dibuat dengan bantuan AI".

Aplikasi seperti ini otomatis memakai **Jalur Lengkap**.

---

## Kenapa fitur AI perlu perlakuan khusus

Kode biasa selalu memberi hasil yang sama untuk input yang sama. **AI tidak.** Jawabannya bisa sedikit berbeda setiap kali, bisa salah dengan yakin, dan bisa berubah total ketika model atau prompt-nya diganti.

Akibatnya, tes biasa ("apakah output-nya persis X?") tidak cukup. Kamu butuh cara lain untuk membuktikan bahwa fitur AI-mu tetap bekerja.

---

## 1. Set evaluasi

**Set evaluasi** adalah kumpulan contoh input tetap beserta ciri jawaban yang diharapkan. Bukan jawaban persisnya, tapi ciri-cirinya.

Contoh untuk fitur terjemahan:

| No | Input | Ciri jawaban yang benar |
|---|---|---|
| 1 | "Selamat pagi, apa kabar?" | Bahasa Inggris; mengandung "good morning" |
| 2 | Teks kosong | Pesan "teks kosong", bukan error |
| 3 | Paragraf 500 kata | Selesai < 30 detik; tidak terpotong |
| 4 | Teks campuran Indonesia–Inggris | Bagian Inggris tidak rusak |

Jalankan set evaluasi **setiap kali** model, prompt, atau pengaturan diubah. Masukkan ke validator.

> *"Buat set evaluasi 10–20 contoh untuk fitur AI ini, simpan di repo, dan tambahkan ke validator."*

*Kenapa:* tanpa set evaluasi, kamu tidak bisa membuktikan bahwa mengganti model membuat aplikasi lebih baik, bukan lebih buruk.

---

## 2. Prompt diperlakukan seperti kode

Prompt (instruksi yang dikirim aplikasi ke model AI) sangat memengaruhi hasil. Perlakukan seperti kode:

- Simpan di file tersendiri di repo, misalnya folder `prompts/`, bukan tersebar di dalam kode.
- Setiap perubahan prompt di-commit dengan alasan.
- Setelah prompt berubah, jalankan set evaluasi.

---

## 3. Memilih model

| Pertanyaan | Kenapa penting |
|---|---|
| Lokal (di perangkat) atau online (lewat internet)? | Lokal: gratis, privat, bisa offline, tapi terbatas oleh perangkat. Online: lebih pintar, tapi butuh internet, bisa berbiaya, dan data keluar dari perangkat. |
| Berapa ukuran model? | Model lokal butuh RAM kira-kira sedikit di atas ukuran file modelnya. Pastikan muat di perangkat target bersama aplikasi lain yang berjalan. |
| Butuh kartu grafis tertentu? | Banyak alat AI berjalan jauh lebih cepat dengan kartu grafis NVIDIA. Tanpa itu, pilih versi CPU dan model kecil. |
| Apa lisensinya? | Lisensi model terpisah dari lisensi kode. Ada model yang melarang pemakaian tertentu. |
| Seberapa cepat? | Ukur waktu jawaban di perangkat yang sebenarnya, bukan perkiraan. |

Catat pilihan model (nama, versi, ukuran, lisensi) di `docs/KONTEKS_PROYEK.md`.

---

## 4. Rencana kalau AI gagal

Model bisa lambat, mati, kehabisan kuota, atau memberi jawaban kacau. Aplikasi harus tetap sopan:

- Ada batas waktu tunggu, lalu pesan yang jelas ("AI sedang tidak tersedia, coba lagi").
- Aplikasi tidak menutup sendiri dan tidak kehilangan data yang sedang dikerjakan.
- Bila ada, beralih ke cara cadangan (model lain, atau fitur tanpa AI).
- Bila AI diminta menghasilkan format tertentu (misalnya daftar atau tabel), aplikasi memeriksa formatnya sebelum memakainya.

---

## 5. Privasi

- Jelaskan data apa yang dikirim ke layanan AI online.
- **Bawaan:** jangan mengirim data pribadi (nama, nomor telepon, dokumen pribadi) ke layanan online tanpa persetujuan pemakai.
- Kalau aplikasimu dipakai orang lain, beri tahu mereka bahwa ada fitur yang memakai AI online.

---

## 6. Biaya

Kalau memakai API AI berbayar:

- Minta AI menghitung perkiraan biaya per pemakaian dan per bulan.
- Pasang batas pemakaian atau batas anggaran di akun penyedia API.
- Simpan API key sebagai rahasia (lihat [github-dasar.md](github-dasar.md)), jangan di dalam kode.

---

## Checklist singkat

- [ ] Set evaluasi tersedia dan masuk validator
- [ ] Prompt tersimpan di repo dan diberi versi
- [ ] Model tercatat: nama, ukuran, lisensi, kebutuhan RAM
- [ ] Sudah diukur kecepatannya di perangkat sebenarnya
- [ ] Ada perilaku yang jelas saat AI gagal atau lambat
- [ ] Jelas data apa yang dikirim keluar perangkat
- [ ] Bila berbayar: perkiraan biaya dan batas pemakaian sudah dipasang
