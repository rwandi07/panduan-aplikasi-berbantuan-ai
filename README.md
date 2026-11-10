# Panduan Pengembangan Aplikasi Berbantuan AI

### Human-Controlled AI Development Framework

> **AI mengerjakan, manusia mengendalikan.** AI menulis kode, menjalankan tes, dan mencatat. Keputusan produk, persetujuan perubahan, dan rilis tetap di tanganmu.
>
> Prinsip utamanya: AI boleh bekerja sebebas mungkin selama tindakannya bisa dibatalkan, hasilnya dipercaya sebatas buktinya, dan setiap keputusan yang diminta darimu disajikan dengan penjelasan, pilihan, dan konsekuensi yang bisa kamu pahami. Tujuannya mengurangi pekerjaanmu **tanpa** mengurangi pemahaman dan kendalimu.

Panduan ini untuk kamu yang **membuat aplikasi dengan bantuan AI** (ChatGPT, Claude, Gemini, Codex, dan sejenisnya), tetapi **bukan programmer profesional**.

Mungkin kamu paham alur aplikasimu, tapi tidak selalu paham detail kode yang ditulis AI. Itu wajar. Panduan ini membantu kamu bekerja **hampir setara profesional**: proyek tercatat rapi, hasil kerja AI bisa kamu buktikan sendiri, dan pekerjaan bisa dilanjutkan kapan saja, di chat mana pun, dengan AI mana pun.

**Versi:** 1.4 (10 November 2026). Lihat [CHANGELOG.md](CHANGELOG.md).

> **Batas tegas:** panduan ini tidak dipakai untuk membangun fungsi pembayaran (payment gateway, bayar otomatis, menyimpan data kartu, memindahkan saldo). Alasannya ada di [panduan/batas-pembayaran.md](panduan/batas-pembayaran.md).

---

## Isi panduan

| Bagian | Untuk siapa | Isi |
|---|---|---|
| [WORKFLOW_AI.md](WORKFLOW_AI.md) | **AI** | Aturan kerja yang kamu berikan ke AI di awal setiap proyek |
| [panduan/alur-kerja.md](panduan/alur-kerja.md) | Kamu | Langkah demi langkah membuat aplikasi, termasuk untuk aplikasi lama (Jalur Adopsi) |
| [panduan/kumpulan-prompt.md](panduan/kumpulan-prompt.md) | Kamu | Kalimat perintah siap salin untuk setiap tahap |
| [panduan/batas-pembayaran.md](panduan/batas-pembayaran.md) | Kamu dan AI | Kenapa fungsi pembayaran berada di luar cakupan panduan ini |
| [panduan/github-dasar.md](panduan/github-dasar.md) | Kamu | GitHub sebagai buku catatan pemrograman |
| [panduan/tes-sendiri.md](panduan/tes-sendiri.md) | Kamu | Cara membuktikan sendiri bahwa hasil kerja AI benar |
| [panduan/kamus-ui.md](panduan/kamus-ui.md) | Kamu dan AI | Arti "rapi", "simple", dan "menarik" untuk tampilan aplikasi |
| [panduan/aplikasi-dengan-fitur-ai.md](panduan/aplikasi-dengan-fitur-ai.md) | Kamu dan AI | Hal khusus bila aplikasimu sendiri memakai AI di dalamnya |
| [panduan/alat-ai.md](panduan/alat-ai.md) | Kamu | Alat AI mana untuk pekerjaan apa |
| [panduan/glosarium.md](panduan/glosarium.md) | Kamu | Arti istilah teknis dalam satu kalimat |
| [template/](template/) | Kamu dan AI | Formulir siap pakai: profil, konteks proyek, checklist tes, dan lainnya |
| [arsip/](arsip/) | Referensi | Versi lama panduan |

---

## Mulai cepat

> **Tidak perlu langganan AI berbayar.** GitHub gratis. Kalau AI-mu tidak bisa membuka GitHub langsung, kamu yang mengunggah file yang disiapkan AI, dan semua aturan panduan tetap berlaku. Lihat [tingkat akses AI ke GitHub](panduan/github-dasar.md#tingkat-akses-ai-ke-github).

1. **Isi profilmu sekali saja.** Salin [template/PROFIL_PENGEMBANG.md](template/PROFIL_PENGEMBANG.md), isi tingkat keahlian, spesifikasi komputer dan HP-mu, serta tingkat akses AI-mu ke GitHub. Simpan di tempat pribadi (jangan di repo publik).
2. **Buat satu repositori GitHub untuk setiap aplikasi.** Kalau belum pernah, baca [panduan/github-dasar.md](panduan/github-dasar.md) dulu.
3. **Mulai percakapan dengan AI** memakai pesan pembuka di bawah, lampirkan `WORKFLOW_AI.md` dan profilmu.
4. **Ikuti alurnya:** ide → cari aplikasi pembanding → pilih rancangan → bangun → tes → tandai checkpoint → rilis. Detailnya di [panduan/alur-kerja.md](panduan/alur-kerja.md).
5. **Jangan terima "sudah selesai" tanpa bukti** yang bisa kamu jalankan sendiri. Lihat [panduan/tes-sendiri.md](panduan/tes-sendiri.md).

Aplikasimu sudah ada sebelum memakai panduan ini? Pakai **Jalur Adopsi** di [panduan/alur-kerja.md](panduan/alur-kerja.md#aplikasi-lama-jalur-adopsi).

### Pesan pembuka untuk AI

Salin dan tempel di awal percakapan baru:

```text
Saya melampirkan WORKFLOW_AI.md sebagai aturan kerja kita, dan profil pengembang saya.
Pelajari keduanya. Jangan mulai mengerjakan apa pun dulu.

Setelah membaca, jawab singkat:
1. Apa yang kamu pahami dari aturan kerja ini (maksimal 5 poin).
2. Bagian mana yang bisa dan tidak bisa kamu lakukan dengan alat yang kamu punya sekarang
   (misalnya menjalankan kode, membuat gambar mockup), dan tingkat aksesmu ke GitHub
   (1: tanpa akses, 2: hanya membaca, 3: bisa menulis). Periksa, jangan menebak.
3. Konfirmasi bahwa audit, pembangunan, dan perbaikan adalah kegiatan terpisah,
   dan perbaikan hanya dilakukan setelah saya setujui.

Lalu tunggu instruksi saya tentang proyeknya.
```

Kalau AI-mu bisa membuka repositori langsung (agen coding), cukup:

```text
Baca AGENTS.md, docs/KONTEKS_PROYEK.md, dan docs/PENGALAMAN.md di repo ini,
lalu jawab STATUS PROYEK. Jangan mengubah apa pun dulu.
```

Prompt untuk tahap-tahap lain ada di [panduan/kumpulan-prompt.md](panduan/kumpulan-prompt.md).

---

## Perintah singkat yang bisa kamu pakai

| Ketik | Artinya |
|---|---|
| `MODE: DISKUSI` | Ngobrol dan berpikir dulu, jangan ubah apa pun |
| `MODE: AUDIT` | Cari masalah, tapi jangan perbaiki |
| `SETUJU RANCANGAN` | Rancangan terakhir boleh dibangun |
| `SETUJU PERBAIKAN: BUG-001` | Hanya temuan itu yang boleh diperbaiki |
| `SETUJU DENGAN CATATAN` | Lanjutkan walau ada tes yang belum bisa kamu lakukan; AI mencatat apa yang belum terbukti |
| `STATUS PROYEK` | Minta laporan posisi proyek |
| `HANDOFF PROYEK` | Minta catatan serah-terima sebelum pindah chat atau AI |
| `JELASKAN SEDERHANA` | Minta penjelasan ulang dengan bahasa awam |
| `CATAT PENGALAMAN` | Simpan pelajaran dari masalah yang baru terjadi, agar tidak terulang |
| `STOP` | Hentikan yang sedang dikerjakan |

Daftar lengkap ada di [WORKFLOW_AI.md, Bagian 2](WORKFLOW_AI.md#2-mode-kerja-izin-dan-kosakata-perintah).

---

## Memakai dan menyesuaikan panduan ini

Panduan ini boleh dipakai, dibagikan, dan diubah sesuai kebutuhanmu dengan menyebut sumbernya. Lihat [LICENSE](LICENSE).

Punya saran atau menemukan bagian yang membingungkan? Buka tab **Issues** di repositori ini dan tulis masukanmu.
