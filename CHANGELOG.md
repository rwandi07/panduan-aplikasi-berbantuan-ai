# Riwayat Perubahan

Format nomor versi: **besar.kecil**. Angka besar berubah bila cara kerja berubah mendasar; angka kecil untuk penambahan dan perbaikan.

## v1.4 (10 November 2026)

**Ringkasan sederhana:** panduan kini menegaskan bahwa **tidak perlu langganan AI berbayar**. GitHub gratis; kalau AI tidak bisa membuka GitHub langsung, pengguna yang mengunggah file yang disiapkan AI, dan semua aturan tetap berlaku.

### Baru
- **Tingkat akses AI ke GitHub** (`WORKFLOW_AI.md` Bagian 8.2, `panduan/github-dasar.md`): 1 tanpa akses, 2 hanya membaca, 3 bisa menulis. Semua aturan berlaku sama; bedanya hanya siapa yang mengunggah.
- **Aturan untuk tingkat 1 dan 2:** minta versi file terbaru sebelum mengubah, berikan file utuh (bukan potongan), daftar file yang berubah, pesan commit siap tempel, perubahan kecil per unggahan, pembaruan buku catatan dalam unggahan yang sama, dan konfirmasi lewat kode commit.
- **Checkpoint tanpa tag:** dicatat sebagai kode commit; cara kembali ke checkpoint lewat unduhan ZIP dari situs GitHub; cara membuat tag lewat GitHub Desktop.
- **Langkah mengunggah lewat situs GitHub**: file baru, mengubah file, menghapus file.
- Prompt baru untuk tingkat 1: melanjutkan proyek, meminta perubahan siap unggah, melaporkan kode commit.

### Diubah
- Pesan pembuka meminta AI menyebut tingkat aksesnya ke GitHub, dengan memeriksa, bukan menebak.
- Profil Pengembang, `KONTEKS_PROYEK.md`, dan `AGENTS.md` mencatat tingkat akses AI.
- Glosarium ditambah: kode commit, tingkat akses AI ke GitHub.

## v1.3 (10 November 2026)

**Ringkasan sederhana:** panduan kini punya prinsip utama tentang kebebasan AI, kualitas bukti, dan keputusan yang dipahami manusia; batas tegas untuk pembayaran; cara menerapkan panduan pada aplikasi lama, kebiasaan mencatat pengalaman, aturan kapan memulai percakapan baru, kumpulan prompt siap salin, aturan tegas yang membedakan checkpoint dari rilis, dan subjudul "Human-Controlled AI Development Framework".

### Baru
- **Prinsip utama** (`WORKFLOW_AI.md` Bagian 1): AI bebas bertindak sebanding dengan seberapa mudah tindakannya dibatalkan; kepercayaan pada hasilnya sebanding dengan kualitas bukti; setiap keputusan untuk manusia disertai penjelasan, pilihan, dan konsekuensi yang bisa dipahami. Tujuannya mengurangi pekerjaan manusia tanpa mengurangi pemahaman dan kendalinya.
- **Ringkasan Keputusan** (Bagian 2.4): format wajib setiap kali AI meminta persetujuan, karena persetujuan tanpa pemahaman hanya formalitas.
- **Tingkat Bukti 0–4** (Bagian 10.4), dengan tingkat minimum untuk checkpoint, Release Candidate, dan rilis publik.
- **Persetujuan dengan Catatan** (Bagian 2.5) dan perintah `SETUJU DENGAN CATATAN`: pekerjaan tetap berjalan walau ada tes yang tidak bisa dilakukan pengguna; yang belum terbukti dicatat, tidak dianggap lulus, dan muncul di "Keterbatasan yang Diketahui" pada catatan rilis.
- **Batas tegas pembayaran** (`WORKFLOW_AI.md` Bagian 3.1, `panduan/batas-pembayaran.md`): fungsi yang memproses, memulai, atau menjadwalkan pembayaran berada di luar cakupan. AI wajib berhenti, menjelaskan risikonya dengan bahasa awam, dan menyarankan programmer profesional atau platform jadi. Batas ini tidak bisa dibuka oleh persetujuan atau aturan proyek.
- **Jalur Adopsi** untuk aplikasi yang sudah ada: tandai titik awal, isi buku catatan dari yang terverifikasi, buat validator untuk fitur yang berjalan, tanpa merombak kode.
- **Gerbang Diskusi Awal:** AI wajib mendaftar hal yang ambigu dan asumsinya, lalu menunggu jawaban, sebelum mengajukan rancangan.
- **Kapan memulai percakapan baru:** lima tanda konkret dan prinsip "satu tugas besar, satu percakapan".
- **Eksplorasi Pengalaman** (`docs/PENGALAMAN.md`, `template/PENGALAMAN.md`) dan perintah `CATAT PENGALAMAN`. Pengalaman lintas proyek dipindahkan ke Profil Pengembang.
- **Audit dengan mata segar** (opsional): audit oleh AI lain yang tidak ikut membangun, atau percakapan baru bila hanya punya satu AI.
- **Kumpulan prompt** siap salin untuk setiap tahap (`panduan/kumpulan-prompt.md`).
- **Judul dua tingkat:** "Panduan Pengembangan Aplikasi Berbantuan AI" sebagai nama utama, dengan subjudul "Human-Controlled AI Development Framework" yang menjelaskan pendekatannya. Nama repositori tidak berubah.
- **Manajemen versi, tag, dan rilis** (`WORKFLOW_AI.md` Bagian 8.1): empat kegiatan dibedakan tegas, yaitu commit pengembangan, tag checkpoint internal (`checkpoint/v0.3.0`), Release Candidate (`v0.3.0-rc.1`), dan rilis publik (`v0.3.0`). Tes PASS, tag internal, RC, dan build berhasil tidak otomatis berarti boleh merilis.
- **Kewenangan tertulis:** bagian "Kewenangan versi dan rilis" di template `AGENTS.md`. AI boleh membuat tag checkpoint, RC, merge, atau rilis tanpa bertanya hanya bila diizinkan di sana.

### Diubah
- Daftar izin (`WORKFLOW_AI.md` Bagian 2.3) dibagi dua: **A** selalu ditanyakan (tidak bisa didelegasikan) dan **B** ditanyakan kecuali kewenangannya sudah tertulis (tag, RC, merge, rilis).
- Istilah "tandai versi" diganti "tag checkpoint" di seluruh panduan; alur rilis kini dua tahap (RC, lalu rilis publik).
- `AGENTS.md`, `KONTEKS_PROYEK.md`, dan `PROFIL_PENGEMBANG.md` di folder template mengikuti aturan baru.
- Glosarium ditambah: autodebet, checksum, Eksplorasi Pengalaman, Gerbang Diskusi Awal, Jalur Adopsi, Keterbatasan yang Diketahui, konteks percakapan, payment gateway, Persetujuan dengan Catatan, Release Candidate, Ringkasan Keputusan, tag checkpoint, Tingkat Bukti.
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
