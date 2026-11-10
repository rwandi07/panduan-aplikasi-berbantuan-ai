# Riwayat Perubahan

Format nomor versi: **besar.kecil**. Angka besar berubah bila cara kerja berubah mendasar; angka kecil untuk penambahan dan perbaikan.

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
