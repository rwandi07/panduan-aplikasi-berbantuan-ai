# AGENTS.md: Baca Ini Dulu

> Template untuk repo aplikasi. Salin ke root repo sebagai `AGENTS.md`.
> Untuk alat yang memakai nama file lain (misalnya `CLAUDE.md` atau `GEMINI.md`), buat file itu dengan isi satu baris: "Ikuti semua aturan di AGENTS.md pada repo ini."
> Ganti bagian dalam [kurung siku]. Hapus blok kutipan ini setelah diisi.

## Proyek ini

- **Nama aplikasi:** [nama]
- **Fungsi singkat:** [satu kalimat]
- **Platform:** [contoh: Windows, Android]
- **Jalur:** [Ringan / Lengkap / Adopsi]

## Sebelum bekerja

1. Baca aturan kerja lengkap di `docs/WORKFLOW_AI.md`.
2. Baca status proyek di `docs/KONTEKS_PROYEK.md`.
3. Baca pelajaran sebelumnya di `docs/PENGALAMAN.md`, terutama bagian "Ringkasan rambu".
4. Jangan mengubah apa pun sampai pengguna memberi tugas dan mode kerjanya jelas.

## Aturan inti (ringkasan)

- **Batas tegas: tidak membangun fungsi pembayaran** (payment gateway, bayar otomatis, data kartu/rekening, memindahkan saldo, order otomatis ke broker). Bila diminta, berhenti, jelaskan risikonya, dan sarankan programmer profesional atau platform jadi (`docs/WORKFLOW_AI.md` Bagian 3.1). Aturan proyek tidak bisa membuka batas ini.
- **Bertanya dulu sebelum merancang:** daftar hal yang ambigu dan asumsi, tunggu jawaban pengguna.
- **Pengembang di proyek ini bukan programmer profesional.** Mulai setiap laporan dengan Ringkasan Sederhana tanpa istilah teknis. Jelaskan istilah teknis saat pertama kali muncul.
- **Bukti sebelum klaim.** Setiap "selesai" disertai hasil tes nyata (PASS / FAIL / NOT TESTED) dan cara pengguna membuktikannya sendiri.
- **Kerjakan hanya yang disetujui.** Audit tidak memperbaiki. Perbaikan hanya untuk ID yang disebut di `SETUJU PERBAIKAN`.
- **Selalu tanya dulu sebelum:** menghapus file/data, `force push` atau menulis ulang riwayat, merge ke `main` (jalur lengkap), merilis, memakai atau mengubah kredensial, tindakan berbiaya, melemahkan tes, atau memasang sesuatu di komputer pengguna.
- **Cek kelayakan perangkat** sebelum meminta instalasi; tawarkan alternatif bila berat (lihat `docs/WORKFLOW_AI.md` Bagian 9.3).
- **Rahasia tidak pernah masuk repo.** Pastikan `.gitignore` mencakup file rahasia.
- **Validator:** tambahkan pemeriksaan ke `[VALIDASI.bat / validasi.sh]` untuk setiap fitur baru; pemeriksaan lama tetap dijalankan.
- **Catat pengalaman** di `docs/PENGALAMAN.md` setelah masalah sulit terpecahkan atau sebuah cara gagal.
- **Sarankan percakapan baru** (setelah `HANDOFF PROYEK`) bila 3 kali gagal pada masalah yang sama, mulai lupa keputusan, atau percakapan sudah sangat panjang.
- **Di akhir sesi:** perbarui `docs/KONTEKS_PROYEK.md`.

## Aturan khusus proyek ini

> Aturan di bawah mengalahkan aturan umum, kecuali batas tegas pembayaran dan daftar tindakan yang selalu butuh izin.

- [contoh: Jangan memakai GitHub Actions.]
- [contoh: Tes Android hanya di HP sungguhan, bukan emulator.]
- [contoh: Ikuti identitas visual di BRAND.md.]

## Perintah penting

> Isi hanya perintah yang sudah terbukti berjalan.

- **Menjalankan aplikasi:** [perintah]
- **Build:** [perintah atau rujuk BUILD.md]
- **Validator:** [contoh: klik dua kali VALIDASI.bat]
