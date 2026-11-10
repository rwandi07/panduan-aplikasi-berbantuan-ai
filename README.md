# Panduan Pengembangan Aplikasi Berbantuan AI

Panduan ini untuk kamu yang **membuat aplikasi dengan bantuan AI** (ChatGPT, Claude, Gemini, Codex, dan sejenisnya), tetapi **bukan programmer profesional**.

Mungkin kamu paham alur aplikasimu, tapi tidak selalu paham detail kode yang ditulis AI. Itu wajar. Panduan ini membantu kamu bekerja **hampir setara profesional**: proyek tercatat rapi, hasil kerja AI bisa kamu buktikan sendiri, dan pekerjaan bisa dilanjutkan kapan saja, di chat mana pun, dengan AI mana pun.

**Versi:** 1.2 (10 November 2026). Lihat [CHANGELOG.md](CHANGELOG.md).

---

## Isi panduan

| Bagian | Untuk siapa | Isi |
|---|---|---|
| [WORKFLOW_AI.md](WORKFLOW_AI.md) | **AI** | Aturan kerja yang kamu berikan ke AI di awal setiap proyek |
| [panduan/alur-kerja.md](panduan/alur-kerja.md) | Kamu | Langkah demi langkah membuat aplikasi, dengan contoh kalimat perintah |
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

1. **Isi profilmu sekali saja.** Salin [template/PROFIL_PENGEMBANG.md](template/PROFIL_PENGEMBANG.md), isi tingkat keahlian, spesifikasi komputer, dan HP-mu. Simpan di tempat pribadi (jangan di repo publik).
2. **Buat satu repositori GitHub untuk setiap aplikasi.** Kalau belum pernah, baca [panduan/github-dasar.md](panduan/github-dasar.md) dulu.
3. **Mulai percakapan dengan AI** memakai pesan pembuka di bawah, lampirkan `WORKFLOW_AI.md` dan profilmu.
4. **Ikuti alurnya:** ide → cari aplikasi pembanding → pilih rancangan → bangun → tes → tandai versi. Detailnya di [panduan/alur-kerja.md](panduan/alur-kerja.md).
5. **Jangan terima "sudah selesai" tanpa bukti** yang bisa kamu jalankan sendiri. Lihat [panduan/tes-sendiri.md](panduan/tes-sendiri.md).

### Pesan pembuka untuk AI

Salin dan tempel di awal percakapan baru:

```text
Saya melampirkan WORKFLOW_AI.md sebagai aturan kerja kita, dan profil pengembang saya.
Pelajari keduanya. Jangan mulai mengerjakan apa pun dulu.

Setelah membaca, jawab singkat:
1. Apa yang kamu pahami dari aturan kerja ini (maksimal 5 poin).
2. Bagian mana yang bisa dan tidak bisa kamu lakukan dengan alat yang kamu punya sekarang
   (misalnya akses GitHub, menjalankan kode, membuat gambar mockup).
3. Konfirmasi bahwa audit, pembangunan, dan perbaikan adalah kegiatan terpisah,
   dan perbaikan hanya dilakukan setelah saya setujui.

Lalu tunggu instruksi saya tentang proyeknya.
```

Kalau AI-mu bisa membuka repositori langsung (agen coding), cukup:

```text
Baca AGENTS.md dan docs/KONTEKS_PROYEK.md di repo ini, lalu jawab STATUS PROYEK.
Jangan mengubah apa pun dulu.
```

---

## Perintah singkat yang bisa kamu pakai

| Ketik | Artinya |
|---|---|
| `MODE: DISKUSI` | Ngobrol dan berpikir dulu, jangan ubah apa pun |
| `MODE: AUDIT` | Cari masalah, tapi jangan perbaiki |
| `SETUJU RANCANGAN` | Rancangan terakhir boleh dibangun |
| `SETUJU PERBAIKAN: BUG-001` | Hanya temuan itu yang boleh diperbaiki |
| `STATUS PROYEK` | Minta laporan posisi proyek |
| `HANDOFF PROYEK` | Minta catatan serah-terima sebelum pindah chat atau AI |
| `JELASKAN SEDERHANA` | Minta penjelasan ulang dengan bahasa awam |
| `STOP` | Hentikan yang sedang dikerjakan |

Daftar lengkap ada di [WORKFLOW_AI.md, Bagian 2](WORKFLOW_AI.md#2-mode-kerja-izin-dan-kosakata-perintah).

---

## Memakai dan menyesuaikan panduan ini

Panduan ini boleh dipakai, dibagikan, dan diubah sesuai kebutuhanmu dengan menyebut sumbernya. Lihat [LICENSE](LICENSE).

Punya saran atau menemukan bagian yang membingungkan? Buka tab **Issues** di repositori ini dan tulis masukanmu.
