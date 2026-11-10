# Glosarium

Istilah yang sering muncul saat bekerja dengan AI, dijelaskan dalam satu atau dua kalimat. Diurutkan menurut abjad.

| Istilah | Arti |
|---|---|
| **API** | Pintu bagi satu program untuk meminta layanan dari program lain. Contoh: aplikasimu meminta terjemahan ke layanan AI lewat API-nya. |
| **API key** | "Kunci" rahasia untuk memakai API. Siapa pun yang memegangnya bisa memakai (dan menghabiskan kuota) akunmu. Jangan pernah masuk repo. |
| **APK** | File pemasang aplikasi Android. |
| **Artefak** | Hasil akhir build yang bisa dipasang atau dibagikan, misalnya file APK atau EXE. |
| **Audit** | Pemeriksaan untuk mencari bug, kelemahan, dan risiko, **tanpa** memperbaikinya. |
| **Backend** | Bagian aplikasi yang bekerja "di belakang layar", misalnya server yang menyimpan data. |
| **Branch** | "Kertas coretan" di repo. Tempat mencoba perubahan tanpa mengganggu versi utama. |
| **Bug** | Kesalahan yang membuat aplikasi berperilaku tidak sesuai harapan. |
| **Build** | Proses mengubah kode menjadi aplikasi yang bisa dijalankan (misalnya APK atau EXE). Build berhasil **belum tentu** aplikasinya bekerja benar. |
| **CHANGELOG** | Catatan riwayat perubahan per versi, ditulis supaya mudah dibaca manusia. |
| **CI (Continuous Integration)** | Layanan yang otomatis menjalankan build dan tes setiap ada perubahan di repo, misalnya GitHub Actions. |
| **Commit** | Satu entri bertanggal di buku catatan (repo): perubahan apa dan kenapa. |
| **Dependensi** | Program atau library lain yang dibutuhkan aplikasimu untuk berjalan. |
| **Discovery** | Tahap mencari dan mempelajari aplikasi atau proyek yang sudah ada sebelum membangun sendiri. |
| **Emulator** | Program yang meniru HP di komputer. Praktis, tapi berat untuk komputer dengan RAM kecil. |
| **.env** | File berisi pengaturan dan rahasia (misalnya API key). Tidak boleh masuk repo. |
| **EXE** | File program Windows. |
| **Fork** | Membuat salinan repo milik orang lain ke akunmu sendiri untuk dikembangkan. Perhatikan lisensinya. |
| **Framework** | Kerangka siap pakai untuk membangun aplikasi, supaya tidak mulai dari nol. |
| **Gerbang tahap** | Titik pemeriksaan: tahap berikutnya baru dimulai bila tahap ini terbukti berhasil. |
| **Git** | Program pencatat perubahan file. GitHub adalah situs tempat menyimpan catatan Git secara online. |
| **.gitignore** | Daftar file yang sengaja tidak dicatat di repo, misalnya file rahasia dan file hasil build. |
| **GPU / kartu grafis** | Komponen komputer yang mempercepat pekerjaan grafis dan AI. Banyak alat AI berjalan lambat tanpa GPU yang sesuai. |
| **Handoff** | Catatan serah-terima supaya pekerjaan bisa dilanjutkan di chat atau AI lain. |
| **Keystore** | File kunci untuk menandatangani aplikasi Android. Kalau hilang, update aplikasi tidak bisa dipasang di atas versi lama. Wajib dicadangkan. |
| **Library** | Kumpulan kode siap pakai yang dipasang untuk menambah kemampuan, misalnya library Python untuk membaca PDF. |
| **Lisensi** | Aturan tentang boleh tidaknya sebuah kode, model, atau dokumen dipakai, diubah, dan dibagikan. |
| **Log** | Catatan otomatis tentang apa yang terjadi saat program berjalan. Berguna untuk mencari penyebab masalah. |
| **main** | Cabang utama di repo; berisi versi resmi. |
| **Merge** | Menggabungkan perubahan dari branch ke cabang utama. |
| **Mockup** | Gambar rancangan tampilan sebelum aplikasinya dibuat. |
| **Model (AI)** | "Otak" AI yang dilatih untuk tugas tertentu. Ada yang berjalan di perangkat (lokal) dan ada yang lewat internet (online). |
| **NOT TESTED** | Label untuk tes yang belum atau tidak bisa dijalankan. Bukan berarti lulus. |
| **Prompt** | Instruksi atau pertanyaan yang diberikan ke AI. |
| **Push** | Mengirim commit dari komputer (atau dari AI) ke GitHub. |
| **README** | Halaman sampul repo: aplikasi ini apa dan cara memakainya. |
| **Refactor** | Merapikan susunan kode tanpa mengubah fungsinya. |
| **Register temuan** | Daftar hasil audit beserta bukti, tingkat keparahan, dan keputusanmu. |
| **Regresi** | Fitur lama yang tadinya bekerja menjadi rusak karena perubahan baru. Dicegah dengan menjalankan ulang tes lama. |
| **Release** | Versi aplikasi yang diterbitkan, biasanya disertai file aplikasi dan catatan rilis. |
| **Repositori (repo)** | Buku catatan proyek di GitHub: semua file dan riwayat perubahan satu aplikasi. |
| **Rollback** | Kembali ke versi sebelumnya yang masih berjalan. |
| **Severity / Priority** | Severity: seberapa parah suatu masalah. Priority: seberapa penting segera ditangani. Keduanya dinilai terpisah. |
| **Set evaluasi** | Kumpulan contoh input tetap untuk menguji fitur AI setiap kali model atau prompt berubah. |
| **Tag** | Penanda versi di repo, misalnya `v1.2.0`: "versi ini sudah dites dan berhasil". |
| **UAT (User Acceptance Test)** | Tes oleh pemakai untuk memastikan aplikasi sesuai kebutuhan. Dalam panduan ini: checklist manual. |
| **UI / UX** | UI: tampilan aplikasi. UX: pengalaman memakainya (mudah, nyaman, tidak membingungkan). |
| **Validator** | Satu file tes yang bisa kamu jalankan sendiri dan menghasilkan BERHASIL atau GAGAL. |
| **Virtual environment (venv)** | Folder terisolasi tempat library Python dipasang khusus untuk satu proyek. Hapus foldernya untuk membersihkan. |
