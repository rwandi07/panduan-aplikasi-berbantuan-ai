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
| **Tag / Release** | Pembatas halaman | "Versi ini sudah dites dan berhasil" |
| **Folder `docs/`** | Catatan keputusan | Konteks proyek, temuan, serah-terima |
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
3. **Pilih cara bekerja dengan repo:**
   - **AI yang bisa mengakses GitHub langsung** (agen coding): beri akses ke repo, AI yang mengurus commit dan push.
   - **GitHub Desktop** (aplikasi gratis untuk Windows dan macOS): untuk menyimpan perubahan dengan klik, tanpa mengetik perintah.
   - **Situs GitHub:** untuk mengunggah file lewat browser ("Add file → Upload files"). Cocok untuk perubahan kecil.

Kalau AI-mu hanya chat biasa tanpa akses GitHub, minta: *"Berikan file lengkapnya dan langkah mengunggahnya ke GitHub."*

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
VALIDASI.bat / validasi.sh   ← tes yang bisa kamu jalankan sendiri
```

Kamu tidak perlu membuatnya sendiri. Minta AI:

> *"Siapkan struktur buku catatan sesuai panduan: README, AGENTS.md, CHANGELOG, BUILD, .gitignore, docs/WORKFLOW_AI.md, dan docs/KONTEKS_PROYEK.md."*

---

## Tiga kebiasaan profesional

### 1. Commit kecil dengan pesan yang jelas

Pesan commit yang baik menjawab *apa* dan *kenapa*:

- Kurang baik: `update`
- Baik: `Tambah pesan error saat HP tidak tersambung, supaya aplikasi tidak menutup sendiri`

*Kenapa:* bulan depan kamu (atau AI lain) bisa membaca riwayatnya dan mengerti apa yang terjadi.

### 2. Tandai versi yang berhasil

Setiap kali validator **BERHASIL**, beri tag, misalnya `v0.3.0`.

*Kenapa:* kalau perubahan berikutnya merusak aplikasi, kamu bisa kembali ke versi ini dalam satu langkah.

Cara membaca nomor versi `v1.4.2`:
- angka pertama (1): perubahan besar;
- angka kedua (4): fitur baru;
- angka ketiga (2): perbaikan kecil.

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
- *"Kembalikan ke versi terakhir yang berhasil."* Inilah gunanya tag.

Selama perubahan sudah di-commit, hampir semua kesalahan bisa dibatalkan. Yang benar-benar berbahaya hanya hal-hal yang selalu memerlukan izinmu: menghapus, `force push`, dan menulis ulang riwayat.
