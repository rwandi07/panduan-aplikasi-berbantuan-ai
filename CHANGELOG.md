# Riwayat Perubahan

Format nomor versi: **besar.kecil**. Angka besar berubah bila cara kerja berubah mendasar; angka kecil untuk penambahan dan perbaikan.

## v1.3 (10 November 2026)

**Ringkasan sederhana:** panduan kini punya batas tegas untuk pembayaran, cara menerapkan panduan pada aplikasi lama, kebiasaan mencatat pengalaman, aturan kapan memulai percakapan baru, dan kumpulan prompt siap salin.

### Baru
- **Batas tegas pembayaran** (`WORKFLOW_AI.md` Bagian 3.1, `panduan/batas-pembayaran.md`): fungsi yang memproses, memulai, atau menjadwalkan pembayaran berada di luar cakupan. AI wajib berhenti, menjelaskan risikonya dengan bahasa awam, dan menyarankan programmer profesional atau platform jadi. Batas ini tidak bisa dibuka oleh persetujuan atau aturan proyek.
- **Jalur Adopsi** untuk aplikasi yang sudah ada: tandai titik awal, isi buku catatan dari yang terverifikasi, buat validator untuk fitur yang berjalan, tanpa merombak kode.
- **Gerbang klarifikasi:** AI wajib mendaftar hal yang ambigu dan asumsinya, lalu menunggu jawaban, sebelum mengajukan rancangan.
- **Kapan memulai percakapan baru:** lima tanda konkret dan prinsip "satu tugas besar, satu percakapan".
- **Eksplorasi Pengalaman** (`docs/PENGALAMAN.md`, `template/PENGALAMAN.md`) dan perintah `CATAT PENGALAMAN`. Pengalaman lintas proyek dipindahkan ke Profil Pengembang.
- **Audit dengan mata segar** (opsional): audit oleh AI lain yang tidak ikut membangun, atau percakapan baru bila hanya punya satu AI.
- **Kumpulan prompt** siap salin untuk setiap tahap (`panduan/kumpulan-prompt.md`).

### Diubah
- `AGENTS.md`, `KONTEKS_PROYEK.md`, dan `PROFIL_PENGEMBANG.md` di folder template mengikuti aturan baru.
- Glosarium ditambah: autodebet, Eksplorasi Pengalaman, Jalur Adopsi, konteks percakapan, payment gateway.
- Aturan proyek tetap mengalahkan aturan umum, kecuali batas pembayaran dan daftar tindakan yang selalu butuh izin.

## v1.2 (10 November 2026)

**Ringkasan sederhana:** panduan diubah dari "aturan untuk AI" menjadi paket lengkap untuk pengembang tingkat menengah yang bukan programmer profesional: ada panduan untuk manusia, aturan untuk AI, dan template siap pakai.

### Baru
- **Dua lapisan dokumen:** panduan untuk manusia (`README.md`, folder `panduan/`) dan aturan untuk AI (`WORKFLOW_AI.md`).
- **Pesan pembuka** yang lebih singkat menggantikan teks pengantar v1.1.
- **Profil Pengembang:** tingkat keahlian, perangkat, dan preferensi; AI menyesuaikan bahasa dan saran.
- **Jalur Ringan dan Jalur Lengkap**, supaya aplikasi kecil tidak harus melewati proses penuh.
- **Gerbang tahap:** setiap tahap punya kriteria selesai dan cara membuktikannya.
- **Kosakata perintah:** `MODE:`, `SETUJU RANCANGAN`, `SETUJU PERBAIKAN:`, `STATUS PROYEK`, `HANDOFF PROYEK`, `JELASKAN SEDERHANA`, `STOP`.
- **Daftar tindakan yang selalu butuh izin** (menghapus, force push, rilis, kredensial, biaya, instalasi, dan lainnya).
- **GitHub sebagai buku catatan:** GitHub wajib; struktur minimum repo; `AGENTS.md` sebagai halaman "baca ini dulu" untuk AI.
- **Tes sendiri:** satu validator per proyek dengan hasil BERHASIL/GAGAL, log otomatis, dan pemeriksaan regresi.
- **Cek kelayakan perangkat** sebelum instalasi, beserta urutan alternatif bila perangkat tidak sanggup.
- **UI Discovery dan Kamus UI:** pengguna memilih dari referensi dan mockup; arti "rapi", "simple", "menarik" disepakati.
- **Aplikasi dengan fitur AI:** set evaluasi, prompt seperti kode, pemilihan model, rencana gagal, privasi, biaya.
- **Keamanan:** rahasia tidak masuk repo; cadangan keystore dan sertifikat.
- **Skala severity dan priority** yang terdefinisi, plus skala tiga label untuk jalur ringan.
- **Format laporan** selalu diawali Ringkasan Sederhana.
- **Glosarium**, **panduan alat AI** (terpisah agar mudah diperbarui), dan **template**: profil, konteks proyek, checklist tes, register temuan, AGENTS.md, identitas visual.
- **Lisensi** CC BY 4.0.

### Diubah
- Lembar konteks proyek (v1.1 bagian 13) dan handoff (v1.1 bagian 11) digabung menjadi satu template `KONTEKS_PROYEK.md`.
- GitHub Discovery: tautan wajib diverifikasi, jumlah kandidat dibatasi sesuai jalur, lisensi model AI ikut diperiksa.
- Nama alat AI dipindahkan dari aturan inti ke `panduan/alat-ai.md`.
- Penamaan diseragamkan menjadi "Pengembangan Aplikasi Berbantuan AI".

## v1.1 (22 Oktober 2026)

Versi awal yang dipublikasikan di repo ini. Disimpan apa adanya di [arsip/v1.1](arsip/v1.1/).
