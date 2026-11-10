# GitHub Dasar: Buku Catatan Pemrograman

> Bagaimana kamu bisa melanjutkan pekerjaan tanpa membuka catatan?

Programmer profesional tidak mengandalkan ingatan. Mereka mencatat semuanya: kode, keputusan, perubahan, dan masalah yang ditemukan. Untuk itulah **GitHub** dipakai. Dalam panduan ini, GitHub **wajib**, karena:

- AI tidak mengingat percakapan lama. Buku catatanmu yang mengingatnya.
- Kamu bisa kembali ke versi yang masih berjalan kapan saja.
- Kamu bisa berganti chat atau berganti AI tanpa mengulang penjelasan dari nol.

---

## GitHub sebagai buku catatan

| Istilah GitHub | Dalam buku catatan | Penjelasan singkat |
|---|---|---|
| **Repositori (repo)** | Satu buku untuk satu aplikasi | Tempat semua file aplikasi dan catatannya |
| **README.md** | Halaman sampul | Aplikasi ini apa, cara memakai, cara membangunnya |
| **Commit** | Satu entri bertanggal | "Hari ini mengubah apa, dan kenapa" |
| **Branch** | Kertas coretan | Tempat mencoba perubahan sebelum disalin ke buku utama |
| **main** | Buku utama | Versi yang dianggap resmi |
| **Merge** | Menyalin coretan ke buku utama | Dilakukan setelah perubahan terbukti berhasil |
| **Tag checkpoint** | Pembatas halaman | "Sampai sini tesnya lulus"; belum tentu siap dirilis |
| **Release** | Buku resmi diterbitkan | Versi yang resmi tersedia untuk pengguna |
| **Folder `docs/`** | Catatan keputusan | Konteks proyek, temuan, serah-terima, pengalaman |
| **AGENTS.md / CLAUDE.md** | Halaman "baca ini dulu" untuk AI | Aturan dan konteks yang dibaca AI sebelum bekerja |
| **.gitignore** | Daftar "jangan dicatat" | File rahasia atau sampah yang tidak boleh masuk buku |
| **Issues** | Kotak saran | Tempat mencatat masalah atau ide |

---

## Siapa melakukan apa

| Kamu | AI |
|---|---|
| Membuat akun dan repo | Mengetik perintah Git (commit, branch, tag) |
| Memberi AI akses ke repo | Menjelaskan arti setiap perintah dalam satu kalimat |
| Menyetujui merge, rilis, dan penghapusan | Menulis pesan commit yang jelas |
| Menjaga file rahasia di luar repo | Memastikan rahasia tercantum di `.gitignore` |

Kamu **tidak perlu menghafal perintah Git**. Yang perlu kamu pahami adalah *artinya*, seperti di tabel di atas.

---

## Langkah awal

1. **Buat akun** di [github.com](https://github.com) dan aktifkan verifikasi dua langkah (2FA) di pengaturan keamanan.
2. **Buat repositori** untuk setiap aplikasi:
   - pilih **Private** untuk aplikasi pribadi;
   - centang "Add a README file" bila kamu belum punya file apa pun.
3. **Ketahui tingkat akses AI-mu ke GitHub** (lihat bagian berikut), lalu tulis di Profil Pengembang.

---

## Tingkat akses AI ke GitHub

**GitHub gratis.** Yang sering butuh langganan berbayar adalah kemampuan AI untuk **masuk langsung** ke GitHub. Ketentuannya berbeda-beda per penyedia AI dan sering berubah. Kabar baiknya: **panduan ini tetap bisa dipakai sepenuhnya dengan AI gratis.**

| Tingkat | Kondisi | Siapa mengurus GitHub |
|---|---|---|
| **1. Tanpa akses** | Chat AI biasa, termasuk versi gratis | **Kamu** yang mengunggah. AI menyiapkan file utuh, daftar file, dan pesan commit. |
| **2. Hanya membaca** | Repo dilampirkan atau disambungkan hanya untuk dibaca | AI membaca langsung; **kamu** tetap yang mengunggah. |
| **3. Bisa menulis** | Agen coding yang tersambung ke repo | AI mengurus commit dan branch; kamu yang menyetujui merge dan rilis. |

Semua aturan panduan berlaku sama di ketiga tingkat. Bedanya hanya siapa yang mengetik ke GitHub. Di tingkat 1, kendalimu justru paling kuat: tidak ada perubahan yang masuk tanpa kamu unggah sendiri.

Alat untuk mengunggah di tingkat 1 dan 2:
- **Situs GitHub** lewat browser. Tidak perlu memasang apa pun; cocok untuk perubahan kecil.
- **GitHub Desktop**, aplikasi gratis untuk Windows dan macOS. Lebih nyaman untuk banyak file, dan bisa membuat tag checkpoint.

---

## Mengunggah perubahan lewat situs GitHub (tingkat 1 dan 2)

AI akan memberimu: **daftar file yang berubah**, **isi file utuh**, dan **pesan commit**.

**Sebelum AI mengubah sebuah file**, lampirkan atau tempelkan isi file itu dari repo, supaya AI bekerja dari versi terbaru dan tidak menimpa perubahan lain.

**File baru atau banyak file sekaligus:**
1. Buka repo, masuk ke folder tujuan.
2. Klik **Add file → Upload files**, lalu seret file ke halaman. File dengan nama yang sama akan diganti.
3. Tempel pesan commit dari AI.
4. Pilih **Commit directly to the main branch**, atau, untuk perubahan besar, **Create a new branch** supaya bisa diperiksa dulu lewat pull request.
5. Klik **Commit changes**.

**Mengubah satu file:**
1. Buka file-nya, klik ikon **pensil** (Edit this file).
2. Hapus semua isinya, tempel isi baru dari AI.
3. Klik **Commit changes**, tempel pesan commit, lalu konfirmasi.

**Menghapus file** (hanya setelah kamu setuju): buka file-nya, klik menu **⋯**, pilih **Delete file**, lalu commit.

**Setelah mengunggah**, beri tahu AI kode commit-nya: tujuh karakter pertama yang terlihat di riwayat **Commits**, misalnya `0529fbd`.

---

## Checkpoint dan kembali ke versi lama tanpa tag

Di situs GitHub, membuat tag checkpoint tidak semudah di GitHub Desktop atau lewat agen AI. Tidak masalah:
- **Catat checkpoint sebagai kode commit** di `docs/KONTEKS_PROYEK.md`, misalnya "checkpoint v0.3.0 = commit `0529fbd`".
- **Kalau pakai GitHub Desktop:** buka tab **History**, klik kanan commit yang berhasil, pilih **Create Tag**, beri nama `checkpoint/v0.3.0`, lalu **Push**.

**Kembali ke checkpoint lewat situs GitHub:**
1. Buka riwayat **Commits**, klik commit checkpoint-nya.
2. Klik **Browse files** untuk melihat isi repo persis pada saat itu.
3. Klik **Code → Download ZIP** untuk mengunduh semua file versi tersebut.
4. Minta AI membantu memulihkan file yang perlu dari ZIP itu, lalu unggah sebagai commit baru.

---

## Struktur minimum repo aplikasi

```text
README.md               ← halaman sampul
AGENTS.md               ← "baca ini dulu" untuk AI (salin dari template/AGENTS.md)
CHANGELOG.md            ← riwayat versi dengan bahasa awam
BUILD.md                ← resep membangun aplikasi (atau bagian di README)
.gitignore              ← daftar "jangan dicatat"
docs/
  WORKFLOW_AI.md        ← salinan aturan kerja untuk AI
  KONTEKS_PROYEK.md     ← status proyek dan serah-terima
  REGISTER_TEMUAN.md    ← temuan audit (jalur lengkap)
  PENGALAMAN.md         ← Eksplorasi Pengalaman: pelajaran agar tidak terulang
VALIDASI.bat / validasi.sh   ← tes yang bisa kamu jalankan sendiri
```

Kamu tidak perlu membuatnya sendiri. Minta AI:

> *"Siapkan struktur buku catatan sesuai panduan: README, AGENTS.md, CHANGELOG, BUILD, .gitignore, docs/WORKFLOW_AI.md, docs/KONTEKS_PROYEK.md, dan docs/PENGALAMAN.md."*

---

## Tiga kebiasaan profesional

### 1. Commit kecil dengan pesan yang jelas

Pesan commit yang baik menjawab *apa* dan *kenapa*:

- Kurang baik: `update`
- Baik: `Tambah pesan error saat HP tidak tersambung, supaya aplikasi tidak menutup sendiri`

*Kenapa:* bulan depan kamu (atau AI lain) bisa membaca riwayatnya dan mengerti apa yang terjadi.

### 2. Tandai checkpoint, lalu rilis secara terpisah

Ada empat kegiatan yang sering tertukar. Bedakan dengan jelas:

| Kegiatan | Dalam buku catatan | Contoh nama | Siapa yang memutuskan |
|---|---|---|---|
| **Commit** | Entri harian | (pesan commit) | AI, selama dalam lingkup yang kamu setujui |
| **Tag checkpoint** | Pembatas halaman: "sampai sini tesnya lulus" | `checkpoint/v0.3.0` | AI boleh, **kalau kamu sudah menuliskan izinnya** di `AGENTS.md`; kalau belum, AI bertanya dulu |
| **Release Candidate (RC)** | Draf terbitan untuk diperiksa terakhir | `v0.3.0-rc.1` | AI menyiapkan, kamu memeriksa |
| **Rilis publik** | Buku resmi diterbitkan | `v0.3.0` | **Kamu**, kecuali sudah kamu izinkan secara tertulis |

Setiap kali validator **BERHASIL**, tandai sebagai checkpoint.

*Kenapa:* kalau perubahan berikutnya merusak aplikasi, kamu bisa kembali ke checkpoint ini dalam satu langkah.

Yang perlu diingat:
- Tes lulus belum berarti siap dirilis.
- Checkpoint bukan rilis publik.
- Release Candidate belum berarti disetujui.
- Build berhasil bukan alasan untuk merge atau menerbitkan.

Cara membaca nomor versi `v1.4.2`:
- angka pertama (1): perubahan besar;
- angka kedua (4): fitur baru;
- angka ketiga (2): perbaikan kecil.

Supaya AI tidak perlu bertanya setiap kali untuk hal rutin, tulis izinmu di bagian "Kewenangan versi dan rilis" pada `AGENTS.md`. Contoh: *"AI boleh membuat tag checkpoint setelah validator BERHASIL. Merge ke main dan rilis publik selalu tanya saya."*

### 3. Coba dulu di branch (jalur lengkap)

Untuk perubahan besar, AI bekerja di branch (kertas coretan). Setelah tes berhasil dan kamu setuju, barulah di-merge ke `main`.

*Kenapa:* buku utama tetap bersih dan selalu berisi versi yang berjalan.

---

## Aturan keras: rahasia tidak pernah masuk repo

Jangan pernah menyimpan file berikut di repo, **termasuk repo private**:

- API key, token, password;
- file `.env` yang berisi rahasia;
- keystore Android (`.jks`, `.keystore`) dan sertifikat;
- file pribadi (KTP, data pelanggan, dan sejenisnya).

Pastikan semuanya tercantum di `.gitignore`. Simpan contoh tanpa isi rahasia, misalnya `.env.example`.

**Kalau rahasia terlanjur masuk repo:** menghapus filenya saja tidak cukup, karena riwayat commit masih menyimpannya. **Ganti rahasianya** (buat API key baru, ganti password), lalu minta AI membantu membersihkan riwayat.

### Cadangkan aset yang tidak tergantikan

Simpan cadangan di luar repo (flashdisk, penyimpanan cloud pribadi):
- **Keystore Android.** Tanpanya, update aplikasi tidak bisa dipasang di atas versi lama. Aplikasi harus di-uninstall dulu dan datanya ikut hilang.
- Password keystore dan sertifikat lain.

---

## Kalau bingung atau ada yang salah

- *"Apa yang terjadi kalau saya menjalankan perintah ini?"* Minta AI menjelaskan **sebelum** menjalankannya.
- *"Saya takut merusak sesuatu. Tunjukkan dulu apa yang akan berubah."*
- *"Kembalikan ke checkpoint terakhir yang berhasil."* Inilah gunanya tag checkpoint.

Selama perubahan sudah di-commit, hampir semua kesalahan bisa dibatalkan. Yang benar-benar berbahaya hanya hal-hal yang selalu memerlukan izinmu: menghapus, `force push`, dan menulis ulang riwayat.
