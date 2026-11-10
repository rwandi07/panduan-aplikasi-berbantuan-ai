# Batas Tegas: Pembayaran

Panduan ini **tidak dipakai untuk membangun fungsi pembayaran**, dan kami sangat tidak menyarankan memakai AI untuk mengembangkan aplikasi yang berkaitan langsung dengan pembayaran. Halaman ini menjelaskan alasannya dengan bahasa sederhana, supaya kamu paham, bukan sekadar patuh.

---

## Kenapa pembayaran berbeda

Untuk aplikasi biasa, kalau ada bug, akibatnya aplikasi error atau hasilnya salah. Kamu perbaiki, lalu jalan lagi.

Untuk pembayaran, akibat bug adalah **uang orang hilang atau tertagih salah.** Itu tidak bisa sekadar "diperbaiki lalu jalan lagi".

Selain itu:
- **Celahnya halus.** Kode pembayaran buatan AI bisa terlihat benar dan lulus tes, tapi tetap punya celah yang hanya ditemukan ahli keamanan. Celah seperti inilah yang dicari penipu.
- **Kamu tidak bisa memeriksanya.** Panduan ini dibuat untuk pengembang yang tidak membaca detail kode. Untuk aplikasi biasa, validator dan checklist sudah cukup. Untuk pembayaran tidak cukup.
- **Ada aturan dan tanggung jawab hukum.** Layanan pembayaran diatur ketat oleh regulator. Kesalahan bisa berujung tanggung jawab hukum, bukan sekadar bug.

---

## Cara kerja pembayaran, secara sederhana

### Pembayaran biasa lewat payment gateway

1. Aplikasi membuat "tagihan".
2. Pengguna diarahkan ke halaman atau aplikasi pembayaran resmi.
3. Pengguna mengonfirmasi dengan PIN atau OTP.
4. Penyedia pembayaran memberi tahu aplikasi: "tagihan ini sudah lunas".

Setiap pembayaran dikonfirmasi pengguna. Tapi aplikasi tetap harus menyimpan **kunci rahasia** penyedia pembayaran dan memeriksa pesan "lunas" dengan benar. Kalau salah, misalnya aplikasi percaya pada pesan "lunas" palsu, barang atau layanan bisa diberikan tanpa dibayar.

### Bayar otomatis: di sinilah celah terbesar

Bayar otomatis mencakup simpan kartu, autodebet, langganan otomatis, dan "sekali hubungkan, bayar tanpa PIN". Pengguna memberi izin **sekali**. Setelah itu aplikasi bisa menagih **tanpa konfirmasi lagi**.

Artinya seluruh keamanan pindah ke kode aplikasi:
- **Bug kecil bisa menguras saldo.** Contohnya perintah tagih yang terulang, atau satu pembayaran tertagih dua kali.
- **Kunci rahasia yang bocor bisa dipakai orang lain** untuk menagih atas nama aplikasimu.
- **Pengamannya hanya bisa diperiksa orang yang membaca kode.** Programmer profesional memasang beberapa lapis pengaman: batas nominal, pencegah tagihan ganda, verifikasi pesan dari penyedia, dan notifikasi setiap transaksi.

---

## Garis batasnya

| Status | Contoh |
|---|---|
| ❌ **Dilarang** | Kode aplikasi yang **memproses, memulai, atau menjadwalkan** pembayaran: menyambung ke API payment gateway, bayar otomatis, autodebet, langganan otomatis, menyimpan data kartu/rekening/dompet digital, memindahkan saldo, mengirim order jual-beli otomatis ke broker atau bursa |
| ✅ **Boleh** | Aplikasi yang hanya **mencatat atau menganalisis** uang tanpa memindahkannya: pencatat pengeluaran, kalkulator cicilan, alat analisis yang keputusan akhirnya tetap di tanganmu |
| ✅ **Boleh** | Aplikasi yang hanya **menampilkan tautan atau QR pembayaran** yang kamu buat sendiri secara manual di dashboard resmi penyedia. Seluruh proses pembayaran terjadi di aplikasi resmi, bukan di aplikasimu. |

Batas ini tidak bisa dibuka dengan persetujuan apa pun dalam panduan ini, termasuk `SETUJU RANCANGAN`.

---

## Kalau aplikasimu memang butuh pembayaran

AI yang mengikuti panduan ini akan **berhenti**, menjelaskan risikonya, lalu menyarankan salah satu jalan berikut:

1. **Libatkan programmer profesional** untuk bagian pembayaran, idealnya yang berpengalaman dengan keamanan pembayaran.
2. **Pakai platform jadi** yang menangani pembayaran sepenuhnya, misalnya toko online, marketplace, atau layanan penjualan yang sudah resmi. Aplikasimu cukup mengarahkan pembeli ke sana.
3. **Pakai pola yang masih boleh:** tampilkan tautan atau QR pembayaran buatan manual, lalu konfirmasi pembayaran dilakukan oleh manusia.

Bagian lain aplikasimu yang tidak menyentuh pembayaran tetap bisa dikembangkan seperti biasa.
