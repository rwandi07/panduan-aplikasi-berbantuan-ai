# Alur Kerja: dari Ide sampai Aplikasi Jadi

Halaman ini menuntunmu melewati satu proyek dari awal sampai akhir. Di setiap langkah ada **contoh kalimat** yang bisa kamu tiru saat bicara dengan AI.

Aturan lengkap untuk AI-nya ada di [WORKFLOW_AI.md](../WORKFLOW_AI.md). Kamu tidak perlu menghafalnya; cukup lampirkan ke AI. Semua contoh kalimat di halaman ini juga dikumpulkan di [kumpulan-prompt.md](kumpulan-prompt.md).

---

## Gambaran besar

```text
1. Ide & kebutuhan
2. Cari aplikasi pembanding (Discovery)
3. Rancang tampilan (mockup) dan teknis
4. Bangun
5. Tes dan buktikan
6. Tandai checkpoint
7. Release Candidate, lalu rilis
   ... lalu ulangi dari langkah 3 untuk fitur berikutnya
```

Setiap langkah punya **gerbang**: kamu baru lanjut kalau langkah sebelumnya sudah terbukti berhasil. Ini kebiasaan profesional yang mencegah masalah kecil menumpuk.

---

## Sebelum mulai: jalur Ringan atau Lengkap?

Tidak semua aplikasi butuh proses penuh.

- **Jalur Ringan:** aplikasi kecil untuk dirimu sendiri, sedikit fitur, satu platform. Contoh: auto-clicker, pengubah nama file massal.
- **Jalur Lengkap:** banyak fitur atau layar, ada AI di dalam aplikasi, menyimpan data penting, dipakai orang lain, atau berjalan di beberapa platform.

> *"Ini ide aplikasinya: [jelaskan]. Menurutmu jalur Ringan atau Lengkap? Jelaskan alasannya."*

### Aplikasi lama: Jalur Adopsi

Kalau aplikasinya sudah ada sebelum kamu memakai panduan ini, jangan perlakukan seperti proyek baru. Memaksa kode lama mengikuti panduan justru berisiko merusak yang sudah berjalan. Terapkan sebagian saja:

1. Tandai kondisi sekarang sebagai checkpoint titik awal.
2. AI mengisi `docs/KONTEKS_PROYEK.md` dari hal yang bisa ia pastikan; sisanya "belum diketahui".
3. Buat validator untuk fitur yang sekarang berjalan, sebagai patokan.
4. Pekerjaan **baru** setelah itu mengikuti panduan.

Langkah Discovery dan rancangan awal dilewati, karena aplikasinya sudah ada. Prompt-nya ada di [kumpulan-prompt.md](kumpulan-prompt.md).

### Satu hal yang tidak dikerjakan: pembayaran

Panduan ini tidak dipakai untuk membangun fungsi pembayaran: payment gateway, bayar otomatis, menyimpan data kartu, memindahkan saldo, atau order otomatis ke broker. AI akan berhenti dan menjelaskan alasannya. Baca [batas-pembayaran.md](batas-pembayaran.md).

---

## Langkah 1 — Ide dan kebutuhan

Ceritakan idemu dengan bahasamu sendiri. Bagian paling penting adalah **kriteria berhasil**: kalimat yang menjelaskan apa yang terjadi kalau aplikasinya bekerja dengan benar.

Contoh kriteria berhasil yang baik:
- "Saat saya memilih file di laptop lalu menekan Kirim, file muncul di folder Download HP dalam waktu kurang dari 10 detik."
- "Kalau HP tidak tersambung, aplikasi menampilkan pesan, bukan menutup sendiri."

> *"MODE: DISKUSI. Saya ingin membuat aplikasi [ide]. Bantu saya merapikan kebutuhannya: siapa penggunanya, fitur wajib, fitur tambahan, batasan, dan kriteria berhasil dengan bahasa saya."*

Ini disebut **Diskusi Awal**. AI seharusnya **bertanya dulu** sebelum merancang: apa saja yang masih belum jelas, dan asumsi apa yang akan dipakai kalau kamu tidak menjawab. Jawab pertanyaannya. Kesalahpahaman di awal adalah penyebab kerja ulang yang paling mahal.

**Gerbang:** kamu setuju dengan ringkasan kebutuhan dan kriteria berhasilnya, dan pertanyaan AI sudah terjawab.

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

Sebelum kamu menyetujui, AI wajib memberi **Ringkasan Keputusan**: apa yang diputuskan, pilihan dan konsekuensinya, rekomendasinya, bukti yang ada, dan cara membatalkan kalau keliru. Kalau ada yang tidak kamu pahami, jangan setujui dulu. Tanyakan, atau ketik `JELASKAN SEDERHANA`. Persetujuan tanpa pemahaman hanya formalitas.

**Gerbang:** kamu memahami Ringkasan Keputusan-nya, lalu mengetik `SETUJU RANCANGAN`.

---

## Langkah 4 — Bangun

AI mengerjakan kode sesuai rancangan. Kamu tidak perlu menyetujui setiap perubahan kecil, tetapi AI tetap harus bertanya sebelum melakukan hal berisiko (menghapus file, memasang sesuatu di laptopmu, memakai API berbayar, dan sejenisnya).

> *"MODE: BANGUN. Kerjakan tahap 1 dari roadmap. Setelah selesai, laporkan dengan Ringkasan Sederhana dan beri saya cara membuktikannya sendiri."*

Kalau AI memintamu memasang sesuatu dan kamu ragu laptopmu kuat:

> *"Apakah ini aman untuk laptop saya? Kalau berat, apa alternatifnya?"*

---

## Langkah 5 — Tes dan buktikan

Jangan terima "sudah selesai" begitu saja. Minta bukti yang bisa kamu jalankan sendiri, dan perhatikan **Tingkat Bukti** yang disebut AI (0 sampai 4). Kalau ada tes yang tidak bisa kamu lakukan, misalnya butuh perangkat yang tidak kamu punya, gunakan `SETUJU DENGAN CATATAN`. Penjelasannya di [tes-sendiri.md](tes-sendiri.md).

> *"Tambahkan pemeriksaan untuk fitur ini ke validator. Saya akan menjalankannya dan mengirim log-nya."*

Lalu jalankan validatornya, misalnya klik dua kali `VALIDASI.bat`. Kalau hasilnya **GAGAL**, kirim file log-nya ke AI. Lihat [tes-sendiri.md](tes-sendiri.md).

**Gerbang:** validator **BERHASIL** dan checklist manual sudah kamu centang.

---

## Langkah 6 — Tandai checkpoint

Begitu tahap ini terbukti berhasil, tandai sebagai **checkpoint**. Ibarat menempel pembatas di buku catatan: "sampai halaman ini, tesnya lulus."

> *"Tes sudah BERHASIL. Commit, beri tag checkpoint, perbarui CHANGELOG dan KONTEKS_PROYEK."*

Kalau AI-mu tidak bisa membuka GitHub dan kamu mengunggah lewat situs GitHub, cukup catat **kode commit**-nya sebagai checkpoint di `docs/KONTEKS_PROYEK.md` (lihat [github-dasar.md](github-dasar.md#checkpoint-dan-kembali-ke-versi-lama-tanpa-tag)).

Checkpoint **bukan** rilis. Tes yang lulus belum berarti aplikasinya siap dibagikan. Kalau kamu ingin AI membuat checkpoint tanpa bertanya setiap kali, tulis izinnya di bagian "Kewenangan versi dan rilis" pada `AGENTS.md`.

Kalau suatu saat perubahan berikutnya merusak aplikasi:

> *"Kembalikan aplikasi ke checkpoint/v0.3.0 yang terakhir berhasil. Jelaskan dulu apa yang akan terjadi sebelum melakukannya."*

---

## Langkah 7 — Release Candidate, lalu rilis

Rilis dilakukan dua tahap, supaya ada pemeriksaan terakhir sebelum aplikasi dipakai atau dibagikan.

**a. Release Candidate (RC):** AI menyiapkan versi kandidat, misalnya `v0.3.0-rc.1`, beserta file aplikasi, hasil tes, checksum (sidik jari file untuk memastikan tidak berubah), dan catatan rilis.

> *"MODE: RILIS. Siapkan Release Candidate untuk versi ini: file aplikasi (APK/EXE/lainnya), hasil tes, checksum, dan catatan rilis singkat. Jangan terbitkan apa pun."*

Coba RC-nya sendiri. Jalankan checklist tes manual.

**b. Rilis publik:** setelah kamu puas, baru diterbitkan sebagai versi resmi, misalnya `v0.3.0`.

> *"RC sudah saya periksa dan sesuai. Terbitkan sebagai rilis v0.3.0."*

Merge ke `main`, membuat GitHub Release, dan mengunggah ke toko aplikasi selalu menunggu persetujuanmu, kecuali kamu sudah mengizinkannya secara tertulis.

---

## Kalau ingin mencari masalah: Audit

Sesekali, terutama pada jalur lengkap, minta AI memeriksa aplikasi tanpa memperbaikinya.

> *"MODE: AUDIT. Periksa aplikasi ini: bug, kelemahan, risiko keamanan, dan tampilan. Catat di register temuan. Jangan perbaiki apa pun."*

Setelah membaca hasilnya, kamu yang memilih:

> *"SETUJU PERBAIKAN: BUG-002, UX-001. Yang lain biarkan dulu."*

Ingat: tidak semua temuan harus diperbaiki. Ada kelemahan yang wajar diterima.

### Audit dengan mata segar (opsional)

AI yang ikut membangun cenderung tidak melihat kesalahannya sendiri. Kalau kamu punya lebih dari satu jenis AI (misalnya membangun dengan satu AI, berlangganan AI lain juga), minta AI yang **tidak ikut membangun** untuk mengaudit di antara tahap besar. Kalau hanya punya satu AI, buka percakapan baru tanpa riwayat pembangunan. Hasilnya tidak sebaik AI yang berbeda, tapi tetap memberi sudut pandang baru. Prompt-nya ada di [kumpulan-prompt.md](kumpulan-prompt.md).

---

## Kapan mulai percakapan baru

Percakapan yang terlalu panjang membuat AI mudah lupa dan keliru. Pegang prinsip ini: **satu tugas besar, satu percakapan.**

Mulai percakapan baru kalau kamu melihat salah satu tanda ini:
1. AI sudah **3 kali gagal** memperbaiki masalah yang sama.
2. AI **lupa atau bertentangan** dengan keputusan yang sudah disepakati.
3. AI **salah menyebut nama file**, atau mengulang kesalahan yang sudah diperbaiki.
4. Percakapan sudah **sangat panjang** atau balasan terasa melambat.
5. Kamu **pindah ke tugas yang berbeda**.

AI yang mengikuti panduan ini juga akan menyarankannya sendiri. Caranya:

1. Di percakapan lama: *"HANDOFF PROYEK."* AI memperbarui `docs/KONTEKS_PROYEK.md`.
2. Di percakapan baru: minta AI membaca `docs/KONTEKS_PROYEK.md` dan `docs/PENGALAMAN.md`, lalu jawab `STATUS PROYEK`.

Karena semuanya tercatat di GitHub, kamu tidak perlu menjelaskan ulang dari nol. Cara yang sama berlaku kalau kamu ingin **berganti AI**.

---

## Eksplorasi Pengalaman

Programmer berpengalaman bukan orang yang tidak pernah salah, tapi orang yang tidak mengulang kesalahan yang sama. Setiap proyek punya file `docs/PENGALAMAN.md` untuk mencatat:
- masalah sulit yang akhirnya terpecahkan;
- cara yang dicoba tapi gagal;
- kejutan, misalnya alat atau perangkat yang tidak berperilaku seperti perkiraan.

Setiap catatan berisi: apa yang terjadi, penyebabnya, cara menghindarinya, dan apakah berlaku untuk proyek lain.

> *"CATAT PENGALAMAN. Masalah [jelaskan] tadi akhirnya selesai."*

Pengalaman yang berlaku untuk semua proyek, misalnya "di laptop saya, emulator Android selalu terlalu berat", pindahkan ke **Profil Pengembang**-mu supaya ikut dibaca AI di proyek berikutnya.

---

## Kalau penjelasan AI membingungkan

Itu bukan salahmu. Ketik:

> *"JELASKAN SEDERHANA."*

Atau tanyakan langsung: *"Apa arti [istilah]? Kenapa itu perlu?"* Istilah yang sering muncul juga ada di [glosarium.md](glosarium.md).
