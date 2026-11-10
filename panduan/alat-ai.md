# Alat AI: Mana untuk Pekerjaan Apa

Nama dan fitur alat AI berubah cepat. Halaman ini sengaja dipisah dari aturan inti supaya mudah diperbarui. **Diperbarui terakhir: November 2026.** Selalu cek dokumentasi resmi alatnya.

---

## Tiga jenis alat AI

| Jenis | Contoh | Bisa apa | Batasannya |
|---|---|---|---|
| **Chat AI** | ChatGPT, Claude, Gemini (versi chat) | Diskusi, merancang, menulis kode, menjelaskan, membuat mockup | Biasanya tidak bisa langsung mengubah repo atau menjalankan aplikasimu |
| **Agen coding** | Codex, Claude Code, agen di dalam editor kode | Membaca dan mengubah banyak file di repo, menjalankan tes, commit | Perlu akses repo; perlu batas izin yang jelas |
| **Kamu sendiri** | Laptop dan HP-mu | Tes di perangkat sungguhan, menilai kenyamanan tampilan, menyetujui | Waktumu terbatas, jadi pakai hanya bila perlu |

Banyak chat AI sekarang juga punya mode agen (bisa menjalankan kode atau mengakses GitHub). Tanyakan langsung ke AI-nya apa yang bisa dilakukan, memakai pesan pembuka di [README](../README.md).

---

## Pekerjaan dan alat yang cocok

| Pekerjaan | Paling cocok |
|---|---|
| Ide, kebutuhan, memilih prioritas fitur | Chat AI + kamu |
| Discovery (mencari aplikasi pembanding) | Chat AI yang bisa mencari di internet |
| Mockup tampilan | Chat AI yang bisa membuat gambar atau halaman pratinjau |
| Bug kecil, perubahan satu-dua file | Chat AI atau agen coding |
| Fitur baru lintas banyak file, build, menjalankan tes | Agen coding |
| Audit menyeluruh | Agen coding dengan mode penalaran tinggi |
| Tes di HP atau laptop sungguhan | Kamu, dengan validator dan checklist dari AI |
| Keputusan produk, persetujuan, rilis | **Selalu kamu** |

Untuk pekerjaan sulit (arsitektur, bug yang membingungkan, audit), pilih mode AI dengan penalaran lebih tinggi bila tersedia, walau lebih lambat.

---

## File "baca ini dulu" untuk agen coding

Agen coding membaca file instruksi di repo secara otomatis. Nama filenya berbeda per alat:

| Alat | File yang dibaca |
|---|---|
| Codex dan banyak agen lain | `AGENTS.md` |
| Claude Code | `CLAUDE.md` |
| Gemini CLI | `GEMINI.md` |
| GitHub Copilot | `.github/copilot-instructions.md` |

Saran: tulis isi lengkapnya di `AGENTS.md` (template: [template/AGENTS.md](../template/AGENTS.md)). Untuk alat lain, buat file sesuai namanya yang isinya cukup:

```text
Ikuti semua aturan di AGENTS.md pada repo ini.
```

Dengan begitu kamu hanya memelihara satu file.

---

## Kalau AI tidak punya akses repo

Tidak masalah. Minta:

> *"Berikan file lengkap yang berubah, dan langkah mengunggahnya ke GitHub."*

Lalu unggah lewat GitHub Desktop atau situs GitHub (lihat [github-dasar.md](github-dasar.md)). Setelah itu, beri tahu AI bahwa perubahan sudah tersimpan.

---

## Berpindah antar AI

Karena semua tercatat di repo, kamu bebas berpindah: misalnya merancang di satu chat AI, membangun dengan agen coding, lalu meminta audit dari AI lain. Kuncinya:

1. Sebelum pindah: `HANDOFF PROYEK`.
2. Di AI baru: lampirkan `WORKFLOW_AI.md`, lalu minta AI membaca `docs/KONTEKS_PROYEK.md`.
