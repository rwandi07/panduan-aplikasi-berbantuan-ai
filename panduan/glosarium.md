# Glosarium

Istilah yang sering muncul saat bekerja dengan AI, dijelaskan dalam satu atau dua kalimat. Diurutkan menurut abjad.

| Istilah | Arti |
|---|---|
| **API** | Pintu bagi satu program untuk meminta layanan dari program lain. Contoh: aplikasimu meminta terjemahan ke layanan AI lewat API-nya. |
| **API key** | "Kunci" rahasia untuk memakai API. Siapa pun yang memegangnya bisa memakai (dan menghabiskan kuota) akunmu. Jangan pernah masuk repo. |
| **APK** | File pemasang aplikasi Android. |
| **Artefak** | Hasil akhir build yang bisa dipasang atau dibagikan, misalnya file APK atau EXE. |
| **Audit** | Pemeriksaan untuk mencari bug, kelemahan, dan risiko, **tanpa** memperbaikinya. |
| **Autodebet / bayar otomatis** | Izin sekali kepada aplikasi untuk menagih berulang tanpa konfirmasi lagi. Di luar cakupan panduan ini; lihat [batas-pembayaran.md](batas-pembayaran.md). |
| **Backend** | Bagian aplikasi yang bekerja "di belakang layar", misalnya server yang menyimpan data. |
| **Branch** | "Kertas coretan" di repo. Tempat mencoba perubahan tanpa mengganggu versi utama. |
| **Bug** | Kesalahan yang membuat aplikasi berperilaku tidak sesuai harapan. |
| **Build** | Proses mengubah kode menjadi aplikasi yang bisa dijalankan (misalnya APK atau EXE). Build berhasil **belum tentu** aplikasinya bekerja benar. |
| **Checksum** | "Sidik jari" sebuah file berupa deretan huruf dan angka. Kalau isi file berubah sedikit saja, checksum-nya ikut berubah; berguna untuk memastikan file aplikasi yang dibagikan masih asli. |
| **CHANGELOG** | Catatan riwayat perubahan per versi, ditulis supaya mudah dibaca manusia. |
| **CI (Continuous Integration)** | Layanan yang otomatis menjalankan build dan tes setiap ada perubahan di repo, misalnya GitHub Actions. |
| **Commit** | Satu entri bertanggal di buku catatan (repo): perubahan apa dan kenapa. |
| **Dependensi** | Program atau library lain yang dibutuhkan aplikasimu untuk berjalan. |
| **Discovery** | Tahap mencari dan mempelajari aplikasi atau proyek yang sudah ada sebelum membangun sendiri. |
| **Eksplorasi Pengalaman** | Catatan di `docs/PENGALAMAN.md` tentang masalah yang pernah terjadi, penyebabnya, dan cara menghindarinya, agar tidak terulang. |
| **Emulator** | Program yang meniru HP di komputer. Praktis, tapi berat untuk komputer dengan RAM kecil. |
| **.env** | File berisi pengaturan dan rahasia (misalnya API key). Tidak boleh masuk repo. |
| **EXE** | File program Windows. |
| **Fork** | Membuat salinan repo milik orang lain ke akunmu sendiri untuk dikembangkan. Perhatikan lisensinya. |
| **Framework** | Kerangka siap pakai untuk membangun aplikasi, supaya tidak mulai dari nol. |
| **Gerbang tahap** | Titik pemeriksaan: tahap berikutnya baru dimulai bila tahap ini terbukti berhasil. |
| **Gerbang Diskusi Awal** | Aturan bahwa AI harus bertanya dan mendaftar asumsinya dulu sebelum mengajukan rancangan. |
| **Git** | Program pencatat perubahan file. GitHub adalah situs tempat menyimpan catatan Git secara online. |
| **.gitignore** | Daftar file yang sengaja tidak dicatat di repo, misalnya file rahasia dan file hasil build. |
| **GPU / kartu grafis** | Komponen komputer yang mempercepat pekerjaan grafis dan AI. Banyak alat AI berjalan lambat tanpa GPU yang sesuai. |
| **Handoff** | Catatan serah-terima supaya pekerjaan bisa dilanjutkan di chat atau AI lain. |
| **Jalur Adopsi** | Cara menerapkan panduan ini secara sebagian dan bertahap pada aplikasi yang sudah ada, tanpa merombak kodenya. |
| **Keterbatasan yang Diketahui** | Bagian di catatan rilis yang mendaftar hal yang belum terbukti atau belum berfungsi sempurna, termasuk Catatan Persetujuan yang masih terbuka. |
| **Keystore** | File kunci untuk menandatangani aplikasi Android. Kalau hilang, update aplikasi tidak bisa dipasang di atas versi lama. Wajib dicadangkan. |
| **Konteks (percakapan AI)** | Semua yang "diingat" AI dalam satu percakapan. Kalau terlalu panjang, AI mulai lupa dan keliru; saatnya mulai percakapan baru. |
| **Library** | Kumpulan kode siap pakai yang dipasang untuk menambah kemampuan, misalnya library Python untuk membaca PDF. |
| **Lisensi** | Aturan tentang boleh tidaknya sebuah kode, model, atau dokumen dipakai, diubah, dan dibagikan. |
| **Log** | Catatan otomatis tentang apa yang terjadi saat program berjalan. Berguna untuk mencari penyebab masalah. |
| **main** | Cabang utama di repo; berisi versi resmi. |
| **Merge** | Menggabungkan perubahan dari branch ke cabang utama. |
| **Mockup** | Gambar rancangan tampilan sebelum aplikasinya dibuat. |
| **Model (AI)** | "Otak" AI yang dilatih untuk tugas tertentu. Ada yang berjalan di perangkat (lokal) dan ada yang lewat internet (online). |
| **NOT TESTED** | Label untuk tes yang belum atau tidak bisa dijalankan. Bukan berarti lulus. |
| **Payment gateway** | Layanan perantara yang memproses pembayaran antara aplikasi dan bank atau dompet digital. Menyambungkan aplikasi ke sini berada di luar cakupan panduan ini. |
| **Persetujuan dengan Catatan** | Persetujuan untuk melanjutkan walau ada tes yang belum bisa dilakukan. Yang belum terbukti dicatat (Catatan Persetujuan) dan tidak dianggap lulus. |
| **Prompt** | Instruksi atau pertanyaan yang diberikan ke AI. |
| **Push** | Mengirim commit dari komputer (atau dari AI) ke GitHub. |
| **README** | Halaman sampul repo: aplikasi ini apa dan cara memakainya. |
| **Refactor** | Merapikan susunan kode tanpa mengubah fungsinya. |
| **Register temuan** | Daftar hasil audit beserta bukti, tingkat keparahan, dan keputusanmu. |
| **Regresi** | Fitur lama yang tadinya bekerja menjadi rusak karena perubahan baru. Dicegah dengan menjalankan ulang tes lama. |
| **Release / rilis publik** | Versi aplikasi yang resmi diterbitkan untuk pengguna, misalnya `v0.3.0`, biasanya disertai file aplikasi dan catatan rilis. Butuh persetujuanmu. |
| **Release Candidate (RC)** | Versi kandidat untuk pemeriksaan terakhir sebelum rilis publik, misalnya `v0.3.0-rc.1`. Belum berarti disetujui. |
| **Repositori (repo)** | Buku catatan proyek di GitHub: semua file dan riwayat perubahan satu aplikasi. |
| **Ringkasan Keputusan** | Penjelasan yang wajib diberikan AI sebelum meminta persetujuanmu: apa yang diputuskan, pilihan dan konsekuensinya, rekomendasi, bukti, dan cara membatalkan. |
| **Rollback** | Kembali ke versi sebelumnya yang masih berjalan. |
| **Severity / Priority** | Severity: seberapa parah suatu masalah. Priority: seberapa penting segera ditangani. Keduanya dinilai terpisah. |
| **Set evaluasi** | Kumpulan contoh input tetap untuk menguji fitur AI setiap kali model atau prompt berubah. |
| **Tag** | Penanda pada satu commit di repo. Dalam panduan ini ada dua jenis: tag checkpoint (`checkpoint/v0.3.0`) dan tag rilis (`v0.3.0`). |
| **Tag checkpoint** | Penanda internal bahwa kriteria tes tertentu lulus pada commit itu, misalnya `checkpoint/v0.3.0`. Bukan rilis, dan bukan bukti aplikasi bebas masalah. |
| **Tingkat Bukti** | Ukuran kekuatan bukti dari 0 (baru klaim) sampai 4 (sudah dipakai sungguhan). Kepercayaan pada hasil kerja AI sebanding dengan tingkat ini. |
| **UAT (User Acceptance Test)** | Tes oleh pemakai untuk memastikan aplikasi sesuai kebutuhan. Dalam panduan ini: checklist manual. |
| **UI / UX** | UI: tampilan aplikasi. UX: pengalaman memakainya (mudah, nyaman, tidak membingungkan). |
| **Validator** | Satu file tes yang bisa kamu jalankan sendiri dan menghasilkan BERHASIL atau GAGAL. |
| **Virtual environment (venv)** | Folder terisolasi tempat library Python dipasang khusus untuk satu proyek. Hapus foldernya untuk membersihkan. |
