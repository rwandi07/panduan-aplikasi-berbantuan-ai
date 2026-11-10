# Tes Sendiri: Membuktikan Hasil Kerja AI

Kalau kamu tidak membaca detail kode, bagaimana kamu tahu AI benar? Jawabannya: **jangan percaya klaim, percaya bukti.** Bukti terbaik adalah tes yang bisa kamu jalankan sendiri dan hasilnya mudah dibaca.

---

## 1. Kamu yang menentukan arti "berhasil"

Kalau AI menulis kode sekaligus tesnya, ada celah: tes bisa lulus padahal yang dicek bukan hal yang kamu pedulikan. Misalnya tes hanya mengecek "aplikasi bisa dibuka", bukan "file benar-benar terkirim".

Karena itu, sebelum AI membangun, tulis **kriteria berhasil** dengan bahasamu sendiri:

> "Saat saya memilih 3 foto lalu menekan Kirim, ketiga foto muncul di folder Download HP."

Tes harus membuktikan kalimat itu.

---

## 2. Validator: satu file untuk mengecek semuanya

Setiap proyek punya **satu validator** yang terus ditambah, bukan banyak file tes sekali pakai (`test1.bat`, `test2.bat`, ...) yang menumpuk dan membingungkan.

Contoh tampilan validator yang baik:

```text
=== VALIDASI APLIKASI v0.3.0 ===
Cek 1/5: Python tersedia ............... BERHASIL
Cek 2/5: Aplikasi bisa dijalankan ...... BERHASIL
Cek 3/5: Koneksi ke HP ................. GAGAL
         HP tidak ditemukan di jaringan. Pastikan HP dan laptop di Wi-Fi yang sama.
Cek 4/5: Kirim file contoh ............. DILEWATI (butuh Cek 3)
Cek 5/5: Fitur lama: daftar riwayat .... BERHASIL

HASIL: GAGAL (1 gagal, 1 dilewati)
Log tersimpan di: logs/validasi-2026-11-10-0715.txt
```

Ciri validator yang baik:
- **Satu langkah menjalankan:** klik dua kali `VALIDASI.bat` (Windows) atau satu perintah.
- **Setiap pemeriksaan bernomor**, dengan pesan bahasa awam bila gagal.
- **Ringkasan akhir yang jelas:** BERHASIL atau GAGAL.
- **Log tersimpan otomatis.** Kamu cukup mengirim file log-nya ke AI, tanpa menyalin layar.
- **Fitur lama ikut dicek ulang** setiap kali (disebut *regresi*), supaya perbaikan baru tidak diam-diam merusak yang lama.
- **Aman dijalankan berkali-kali** dan tidak menghapus data.

Minta ke AI:

> *"Buat validator untuk proyek ini sesuai panduan tes-sendiri. Setiap fitur baru menambah pemeriksaan baru."*

---

## 3. Kalau validator GAGAL

1. Jangan panik. Itu tujuan validator: menemukan masalah sebelum kamu memakainya.
2. Baca pesan di baris yang GAGAL. Kadang penyebabnya sederhana (Wi-Fi beda, aplikasi lain masih terbuka).
3. Kirim file log ke AI:

> *"Validator GAGAL. Ini log-nya. Jelaskan sederhana apa penyebabnya, lalu usulkan perbaikan. Jangan perbaiki sebelum saya setuju."*

---

## 4. Checklist manual

Beberapa hal tidak bisa dites otomatis: tampil di HP sungguhan, kenyamanan tampilan, jaringan nyata. Untuk itu pakai checklist singkat ([template/CHECKLIST_TES.md](../template/CHECKLIST_TES.md)):

| No | Langkah | Yang seharusnya terlihat | Hasil |
|---|---|---|---|
| 1 | Buka aplikasi di HP | Layar utama muncul < 3 detik | ☐ Sesuai ☐ Tidak |
| 2 | Tekan tombol Kirim tanpa memilih file | Muncul pesan "Pilih file dulu" | ☐ Sesuai ☐ Tidak |

AI seharusnya meminta tes manual **hanya bila memang perlu**, bukan untuk setiap hal kecil.

---

## 5. Kalau tes butuh memasang sesuatu

Kadang tes memerlukan library Python, alat build, atau model AI. Sebelum memasang apa pun, AI wajib memberi tahu:

- apa yang dipasang dan ukurannya;
- kebutuhan RAM dan apakah butuh kartu grafis tertentu;
- apakah cocok untuk komputermu (berdasarkan profilmu).

Kalau terlalu berat, AI harus menawarkan alternatif dan memastikan alternatif itu bisa kamu jalankan:

1. **AI menjalankan tesnya sendiri** di lingkungannya, bila AI-mu punya fasilitas itu. Kamu hanya menjalankan tes yang benar-benar butuh komputer atau HP-mu.
2. **Versi yang lebih ringan:** library versi CPU, model yang lebih kecil, alat yang lebih sederhana.
3. **Pasang terisolasi di folder proyek:** kalau mau bersih, cukup hapus foldernya.
4. **Layanan cloud** gratis atau murah, dengan penjelasan batas dan biayanya.
5. **Kalau tetap tidak bisa:** ditandai *NOT TESTED* dengan alasannya, tidak dipaksakan dan tidak dianggap lulus.

Setiap instalasi sebaiknya disertai cara membersihkannya, misalnya file `BERSIHKAN.bat`.

Tips umum:
- **Aplikasi Android:** tes langsung di HP sungguhan. Emulator Android berat untuk laptop dengan RAM 8 GB atau kurang.
- **Model AI lokal:** pilih ukuran kecil yang sesuai RAM komputermu.

> *"Apakah ini aman untuk laptop saya? Kalau berat, apa alternatifnya, dan bagaimana membersihkannya nanti?"*

---

## 6. Membaca laporan tes dari AI

| Label | Artinya |
|---|---|
| **PASS / BERHASIL** | Tes benar-benar dijalankan dan lulus |
| **FAIL / GAGAL** | Tes dijalankan dan gagal |
| **NOT TESTED / DILEWATI** | Tes belum atau tidak bisa dijalankan |

Waspadai kalimat seperti *"seharusnya sudah berfungsi"* atau *"build berhasil, jadi aplikasinya sudah jalan"*. Itu dugaan, bukan bukti. Tanyakan: *"Tes apa yang benar-benar sudah dijalankan? Bagaimana saya membuktikannya sendiri?"*

### Tingkat Bukti

Tidak semua bukti sama kuatnya. AI yang mengikuti panduan ini menyebut **Tingkat Bukti** untuk setiap klaimnya:

| Tingkat | Artinya | Seberapa bisa dipercaya |
|---|---|---|
| **0** | Baru klaim: "seharusnya sudah bisa" | Belum bisa dipercaya |
| **1** | Build berhasil atau kode sudah dibaca ulang | Lemah |
| **2** | Tes dijalankan AI di komputernya sendiri | Cukup, untuk checkpoint |
| **3** | Validator kamu jalankan di perangkatmu | Kuat, untuk Release Candidate |
| **4** | Sudah dipakai sungguhan atau checklist manual lulus | Paling kuat, untuk rilis |

Ingat: kalau AI menulis kode **dan** tesnya sendiri, keduanya bisa salah dengan cara yang sama. Karena itu kriteria berhasil yang kamu tulis sendiri penting.

---

## 7. Kalau kamu tidak bisa melakukan tes tertentu

Kadang sebuah tes memang tidak mungkin kamu lakukan. Misalnya fitur kirim file antar dua laptop, padahal kamu hanya punya satu laptop. Pekerjaan tidak harus berhenti. Ketik:

> *"SETUJU DENGAN CATATAN."*

AI akan mencari bukti pengganti dulu (misalnya tes laptop ke HP), lalu menyusun **Catatan Persetujuan**:

| Isi | Contoh |
|---|---|
| Yang belum dites | Transfer file antar dua laptop |
| Alasan | Hanya punya satu laptop |
| Bukti pengganti | Laptop ke HP berhasil (Tingkat 3) |
| Risiko bila gagal | Dua laptop mungkin tidak saling menemukan |
| Kapan dites ulang | Saat ada laptop kedua, atau sebelum rilis |

Yang perlu kamu tahu:
- Catatan **tidak membuat** bagian itu dianggap sudah terbukti. Statusnya tetap "belum dites", hanya saja kamu sadar dan setuju melanjutkan.
- Catatan **tidak hilang.** Semuanya dicatat di `docs/KONTEKS_PROYEK.md` dan akan muncul lagi di catatan rilis sebagai "Keterbatasan yang Diketahui".
- Kalau yang belum terbukti adalah **fitur utama**, AI akan mengatakannya terus terang. Kamu tetap boleh melanjutkan, tapi dengan mata terbuka.
