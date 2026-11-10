# Alur Kerja: dari Ide sampai Aplikasi Jadi

Halaman ini menuntunmu melewati satu proyek dari awal sampai akhir. Di setiap langkah ada **contoh kalimat** yang bisa kamu tiru saat bicara dengan AI.

Aturan lengkap untuk AI-nya ada di [WORKFLOW_AI.md](../WORKFLOW_AI.md). Kamu tidak perlu menghafalnya; cukup lampirkan ke AI.

---

## Gambaran besar

```text
1. Ide & kebutuhan
2. Cari aplikasi pembanding (Discovery)
3. Rancang tampilan (mockup) dan teknis
4. Bangun
5. Tes dan buktikan
6. Tandai versi yang berhasil
7. Rilis / pakai
   ... lalu ulangi dari langkah 3 untuk fitur berikutnya
```

Setiap langkah punya **gerbang**: kamu baru lanjut kalau langkah sebelumnya sudah terbukti berhasil. Ini kebiasaan profesional yang mencegah masalah kecil menumpuk.

---

## Sebelum mulai: jalur Ringan atau Lengkap?

Tidak semua aplikasi butuh proses penuh.

- **Jalur Ringan:** aplikasi kecil untuk dirimu sendiri, sedikit fitur, satu platform. Contoh: auto-clicker, pengubah nama file massal.
- **Jalur Lengkap:** banyak fitur atau layar, ada AI di dalam aplikasi, menyimpan data penting, dipakai orang lain, atau berjalan di beberapa platform.

> *"Ini ide aplikasinya: [jelaskan]. Menurutmu jalur Ringan atau Lengkap? Jelaskan alasannya."*

---

## Langkah 1 — Ide dan kebutuhan

Ceritakan idemu dengan bahasamu sendiri. Bagian paling penting adalah **kriteria berhasil**: kalimat yang menjelaskan apa yang terjadi kalau aplikasinya bekerja dengan benar.

Contoh kriteria berhasil yang baik:
- "Saat saya memilih file di laptop lalu menekan Kirim, file muncul di folder Download HP dalam waktu kurang dari 10 detik."
- "Kalau HP tidak tersambung, aplikasi menampilkan pesan, bukan menutup sendiri."

> *"MODE: DISKUSI. Saya ingin membuat aplikasi [ide]. Bantu saya merapikan kebutuhannya: siapa penggunanya, fitur wajib, fitur tambahan, batasan, dan kriteria berhasil dengan bahasa saya."*

**Gerbang:** kamu setuju dengan ringkasan kebutuhan dan kriteria berhasilnya.

---

## Langkah 2 — Cari pembanding (Discovery)

Sebelum membangun, cari tahu apakah aplikasi seperti itu sudah ada. Bisa jadi kamu cukup memakainya, atau mengembangkan yang sudah ada.

> *"MODE: DISCOVERY. Cari aplikasi atau proyek GitHub yang mirip dengan kebutuhan tadi. Pastikan setiap tautan benar-benar ada. Bandingkan fiturnya, cek lisensinya, lalu sarankan: pakai yang ada, kembangkan yang ada, atau bangun sendiri."*

Hati-hati: AI kadang menyebut repositori yang tidak ada. Klik tautannya sendiri untuk memastikan.

**Gerbang:** kamu memutuskan jalur (pakai / kembangkan / bangun sendiri).

---

## Langkah 3 — Rancang tampilan dan teknis

### Tampilan

Kamu tidak perlu menjelaskan "menarik" itu seperti apa. **Pilih saja.**

> *"Carikan 3–5 referensi tampilan aplikasi sejenis, lalu buat 2–3 mockup dengan gaya berbeda. Ikuti Kamus UI. Saya ingin tampilannya rapi dan simple."*

Lalu tanggapi: *"Saya suka warna yang nomor 2, tapi tata letak yang nomor 1."* Lihat [kamus-ui.md](kamus-ui.md).

### Teknis

> *"Usulkan teknologi yang cocok untuk aplikasi ini dan untuk laptop saya (lihat profil). Jelaskan dengan bahasa awam kenapa memilih itu, dan apa risikonya. Buat roadmap bertahap, setiap tahap dengan kriteria selesai dan cara membuktikannya."*

**Gerbang:** kamu mengetik `SETUJU RANCANGAN`.

---

## Langkah 4 — Bangun

AI mengerjakan kode sesuai rancangan. Kamu tidak perlu menyetujui setiap perubahan kecil, tetapi AI tetap harus bertanya sebelum melakukan hal berisiko (menghapus file, memasang sesuatu di laptopmu, memakai API berbayar, dan sejenisnya).

> *"MODE: BANGUN. Kerjakan tahap 1 dari roadmap. Setelah selesai, laporkan dengan Ringkasan Sederhana dan beri saya cara membuktikannya sendiri."*

Kalau AI memintamu memasang sesuatu dan kamu ragu laptopmu kuat:

> *"Apakah ini aman untuk laptop saya? Kalau berat, apa alternatifnya?"*

---

## Langkah 5 — Tes dan buktikan

Jangan terima "sudah selesai" begitu saja. Minta bukti yang bisa kamu jalankan sendiri.

> *"Tambahkan pemeriksaan untuk fitur ini ke validator. Saya akan menjalankannya dan mengirim log-nya."*

Lalu jalankan validatornya, misalnya klik dua kali `VALIDASI.bat`. Kalau hasilnya **GAGAL**, kirim file log-nya ke AI. Lihat [tes-sendiri.md](tes-sendiri.md).

**Gerbang:** validator **BERHASIL** dan checklist manual sudah kamu centang.

---

## Langkah 6 — Tandai versi yang berhasil

Begitu tahap ini terbukti berhasil, tandai versinya. Ibarat menempel pembatas di buku catatan: "sampai halaman ini, semuanya berjalan."

> *"Tes sudah BERHASIL. Commit, beri tag versi, perbarui CHANGELOG dan KONTEKS_PROYEK."*

Kalau suatu saat perubahan berikutnya merusak aplikasi:

> *"Kembalikan aplikasi ke versi v0.3.0 yang terakhir berhasil. Jelaskan dulu apa yang akan terjadi sebelum melakukannya."*

---

## Langkah 7 — Rilis atau pakai

> *"MODE: RILIS. Siapkan file aplikasi (APK/EXE/lainnya) untuk versi ini, beserta catatan rilis singkat. Jangan unggah ke mana pun sebelum saya setujui."*

---

## Kalau ingin mencari masalah: Audit

Sesekali, terutama pada jalur lengkap, minta AI memeriksa aplikasi tanpa memperbaikinya.

> *"MODE: AUDIT. Periksa aplikasi ini: bug, kelemahan, risiko keamanan, dan tampilan. Catat di register temuan. Jangan perbaiki apa pun."*

Setelah membaca hasilnya, kamu yang memilih:

> *"SETUJU PERBAIKAN: BUG-002, UX-001. Yang lain biarkan dulu."*

Ingat: tidak semua temuan harus diperbaiki. Ada kelemahan yang wajar diterima.

---

## Pindah chat atau pindah AI

Percakapan AI punya batas panjang, dan kamu mungkin ingin berganti AI. Sebelum pindah:

> *"HANDOFF PROYEK."*

AI akan memperbarui `docs/KONTEKS_PROYEK.md`. Di chat baru, cukup minta AI membaca file itu. Karena semuanya tercatat di GitHub, kamu tidak perlu menjelaskan ulang dari nol.

---

## Kalau penjelasan AI membingungkan

Itu bukan salahmu. Ketik:

> *"JELASKAN SEDERHANA."*

Atau tanyakan langsung: *"Apa arti [istilah]? Kenapa itu perlu?"* Istilah yang sering muncul juga ada di [glosarium.md](glosarium.md).
