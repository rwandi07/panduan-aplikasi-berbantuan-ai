# Kumpulan Prompt Siap Pakai

Salin, ganti bagian dalam `[kurung siku]`, lalu kirim ke AI. Urutannya mengikuti alur kerja. Penjelasan setiap tahap ada di [alur-kerja.md](alur-kerja.md).

---

## Memulai

### Percakapan pertama (lampirkan WORKFLOW_AI.md dan profilmu)

```text
Saya melampirkan WORKFLOW_AI.md sebagai aturan kerja kita, dan profil pengembang saya.
Pelajari keduanya. Jangan mulai mengerjakan apa pun dulu.

Setelah membaca, jawab singkat:
1. Apa yang kamu pahami dari aturan kerja ini (maksimal 5 poin).
2. Bagian mana yang bisa dan tidak bisa kamu lakukan dengan alat yang kamu punya sekarang,
   dan tingkat aksesmu ke GitHub (1: tanpa akses, 2: hanya membaca, 3: bisa menulis). Periksa, jangan menebak.
3. Konfirmasi bahwa audit, pembangunan, dan perbaikan adalah kegiatan terpisah,
   dan perbaikan hanya dilakukan setelah saya setujui.

Lalu tunggu instruksi saya tentang proyeknya.
```

### Melanjutkan proyek (agen coding dengan akses repo)

```text
Baca AGENTS.md, docs/KONTEKS_PROYEK.md, dan docs/PENGALAMAN.md di repo ini,
lalu jawab STATUS PROYEK. Jangan mengubah apa pun dulu.
```

### Melanjutkan proyek (chat tanpa akses repo, tingkat 1)

```text
Saya melampirkan WORKFLOW_AI.md dan isi docs/KONTEKS_PROYEK.md dari proyek saya.
Kamu tidak punya akses ke GitHub (tingkat 1); saya yang akan mengunggah.
Pelajari, lalu jawab STATUS PROYEK. Jangan mengerjakan apa pun dulu.
```

### Meminta perubahan siap unggah (tingkat 1 dan 2)

```text
Ini isi terbaru file yang akan diubah: [lampirkan atau tempel].
Setelah selesai, berikan: daftar file yang berubah (lokasi lengkap dan statusnya),
isi file utuh untuk setiap file, pesan commit siap tempel, dan pembaruan KONTEKS_PROYEK.
Jaga perubahannya kecil.
```

### Melaporkan bahwa sudah diunggah

```text
Sudah saya unggah. Kode commit-nya [7 karakter, misalnya 0529fbd].
```

### Menerapkan panduan ke aplikasi lama (Jalur Adopsi)

```text
Aplikasi ini dibuat sebelum saya memakai panduan. Terapkan Jalur Adopsi (WORKFLOW_AI.md Bagian 3.3):
tandai kondisi sekarang sebagai checkpoint titik awal (tanya saya dulu sebelum membuat tag), isi docs/KONTEKS_PROYEK.md hanya dari yang bisa kamu pastikan,
dan usulkan validator untuk fitur yang sekarang berjalan.
Jangan mengubah atau merapikan kode aplikasinya.
```

---

## Ide dan kebutuhan

### Merapikan ide

```text
MODE: DISKUSI. Saya ingin membuat aplikasi [jelaskan ide].
Bantu saya merapikan kebutuhannya: siapa penggunanya, fitur wajib, fitur tambahan, batasan,
dan kriteria berhasil dengan bahasa saya. Usulkan juga jalur Ringan atau Lengkap beserta alasannya.
```

### Diskusi Awal: meminta AI bertanya dulu

```text
Sebelum merancang apa pun, daftar dulu hal yang masih ambigu dan asumsi yang akan kamu pakai.
Beri pilihan jawaban bila bisa. Saya jawab dulu, baru kita lanjut.
```

---

## Discovery

### Mencari aplikasi pembanding

```text
MODE: DISCOVERY. Cari aplikasi atau proyek GitHub yang mirip dengan kebutuhan tadi.
Pastikan setiap tautan benar-benar ada. Bandingkan fiturnya, cek lisensinya,
lalu sarankan: pakai yang ada, kembangkan yang ada, atau bangun sendiri.
```

### Mencari referensi tampilan

```text
Carikan 3–5 referensi tampilan aplikasi sejenis dan pedoman desain resmi platformnya.
Lalu buat 2–3 mockup dengan gaya berbeda. Ikuti Kamus UI. Saya ingin tampilannya [rapi / simple / menarik].
```

---

## Rancangan

### Rancangan teknis

```text
Usulkan teknologi yang cocok untuk aplikasi ini dan untuk perangkat saya (lihat profil).
Jelaskan dengan bahasa awam kenapa memilih itu dan apa risikonya.
Buat roadmap bertahap, setiap tahap dengan kriteria selesai dan cara membuktikannya.
```

### Meminta Ringkasan Keputusan sebelum menyetujui

```text
Sebelum saya setujui, beri Ringkasan Keputusan: apa yang diputuskan, pilihan dan konsekuensinya,
rekomendasimu, bukti dan Tingkat Bukti-nya, apa yang bisa salah, dan cara membatalkannya.
```

### Menyetujui

```text
SETUJU RANCANGAN
```

---

## Membangun

### Mengerjakan satu tahap

```text
MODE: BANGUN. Kerjakan tahap [nomor] dari roadmap.
Setelah selesai, laporkan dengan Ringkasan Sederhana dan beri saya cara membuktikannya sendiri.
```

### Sebelum memasang sesuatu di komputer

```text
Apakah ini aman untuk perangkat saya (lihat profil)? Berapa ukurannya dan kebutuhan RAM-nya?
Kalau berat, apa alternatifnya, dan bagaimana membersihkannya nanti?
```

---

## Tes

### Membuat atau menambah validator

```text
Tambahkan pemeriksaan untuk fitur ini ke validator. Pemeriksaan lama tetap dijalankan.
Hasilnya harus BERHASIL/GAGAL dengan pesan bahasa awam, dan log tersimpan otomatis.
```

### Validator gagal

```text
Validator GAGAL. Ini log-nya: [lampirkan file log].
Jelaskan sederhana apa penyebabnya, lalu usulkan perbaikan. Jangan perbaiki sebelum saya setuju.
```

### Menanyakan kekuatan bukti

```text
Untuk setiap fitur yang kamu bilang sudah berfungsi, sebutkan Tingkat Bukti-nya (0–4)
dan apa yang masih belum terbukti.
```

### Tes yang tidak bisa saya lakukan

```text
SETUJU DENGAN CATATAN. Saya tidak bisa mengetes [jelaskan, misalnya: kirim file antar dua laptop]
karena [alasan]. Cari dulu bukti pengganti yang bisa saya jalankan, lalu susun Catatan Persetujuan.
```

### Checklist tes manual

```text
Buatkan checklist tes manual singkat untuk fitur ini: langkah, yang seharusnya terlihat, kolom hasil.
Hanya untuk hal yang tidak bisa dites otomatis.
```

---

## Menyimpan dan mengembalikan versi

### Menandai checkpoint

```text
Tes sudah BERHASIL. Commit, beri tag checkpoint, perbarui CHANGELOG dan KONTEKS_PROYEK.
```

### Memberi izin tetap untuk hal rutin

```text
Tambahkan ke bagian "Kewenangan versi dan rilis" di AGENTS.md:
AI boleh membuat tag checkpoint/* setelah validator BERHASIL.
Merge ke main dan rilis publik selalu tanya saya dulu.
```

### Kembali ke checkpoint sebelumnya

```text
Kembalikan aplikasi ke [checkpoint/v0.3.0] yang terakhir berhasil.
Jelaskan dulu apa yang akan terjadi sebelum melakukannya.
```

---

## Audit dan perbaikan

### Audit

```text
MODE: AUDIT. Periksa aplikasi ini: bug, kelemahan, risiko keamanan, dan tampilan.
Catat di register temuan. Jangan perbaiki apa pun.
```

### Audit dengan mata segar (AI lain atau percakapan baru)

```text
Kamu tidak ikut membangun aplikasi ini. Baca docs/WORKFLOW_AI.md dan docs/KONTEKS_PROYEK.md,
lalu lakukan MODE: AUDIT. Fokus pada hal yang mungkin terlewat oleh yang membangunnya.
Jangan perbaiki apa pun.
```

### Menyetujui perbaikan

```text
SETUJU PERBAIKAN: [ID temuan, misalnya BUG-002, UX-001]. Yang lain biarkan dulu.
```

### Memeriksa tampilan dari screenshot

```text
Periksa screenshot ini memakai Kamus UI. Sebutkan bagian yang belum rapi, belum simple,
atau kurang menarik. Usulkan perbaikan, jangan langsung ubah kodenya.
```

---

## Percakapan dan pengalaman

### Sebelum pindah ke percakapan baru

```text
HANDOFF PROYEK.
```

### Di percakapan baru

```text
Ini lanjutan proyek [nama]. Baca docs/KONTEKS_PROYEK.md dan docs/PENGALAMAN.md,
lalu jawab STATUS PROYEK. Kita fokus ke satu tugas: [tugas].
```

### Mencatat pengalaman

```text
CATAT PENGALAMAN. Masalah [jelaskan] tadi akhirnya selesai.
Tulis apa yang terjadi, penyebabnya, cara menghindarinya, dan apakah berlaku untuk proyek lain.
```

### Saat penjelasan AI membingungkan

```text
JELASKAN SEDERHANA.
```

---

## Rilis

### Menyiapkan Release Candidate

```text
MODE: RILIS. Siapkan Release Candidate untuk versi ini: file aplikasi, hasil tes yang sebenarnya,
checksum, dan catatan rilis singkat. Jangan terbitkan apa pun.
```

### Menerbitkan rilis publik

```text
RC [v0.3.0-rc.1] sudah saya periksa dan sesuai. Terbitkan sebagai rilis [v0.3.0].
```

---

## Aplikasi dengan fitur AI

```text
Buat set evaluasi 10–20 contoh untuk fitur AI ini: input dan ciri jawaban yang benar.
Simpan di repo dan tambahkan ke validator. Jalankan ulang setiap kali model atau prompt berubah.
```
