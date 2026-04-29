Berikut adalah penjelasan untuk masing-masing *Customer Journey Map* (CJM) dalam format Markdown, berdasarkan konten file yang diberikan.

> **Catatan:** Tiga file pertama (DonaturKorporat, Penerima, Relawan) memiliki konten tabel yang identik. Penjelasan di bawah tetap ditulis sesuai judul file masing-masing, meskipun secara naratif tabel tersebut lebih menggambarkan alur **Relawan**. Hal ini mungkin terjadi karena kesamaan template atau kebutuhan analisis yang berbeda.

---

## 1. CJM – Donatur Korporat (Hendra)

*Fase perjalanan: Inisiatif & Niat Baik → Pemilihan Misi → Penjemputan & Pengantaran → Serah Terima & Apresiasi*

| Fase | Aksi | Titik Sentuh | Emosi & Pikiran | Pain Points | Peluang Solusi (FAR) |
|------|------|--------------|------------------|-------------|----------------------|
| **Inisiatif & Niat Baik** | Mencari kegiatan sosial (crowdsourcing) untuk mengisi waktu luang. | Kampus, Media Sosial | Antusias: "Ingin bantu distribusi donasi tapi butuh sistem yang jelas." | Niat baik tidak tersalurkan karena ketiadaan platform terpusat. | Login peran khusus (RBAC) dengan lingkungan tugas mandiri. |
| **Pemilihan Misi** | Membuka aplikasi FAR, memilih misi pengantaran berdasarkan rute terdekat. | Aplikasi FAR (Missions Board) | Termotivasi: "Misi ini searah jalan pulang, poin XP-nya juga lumayan!" | Repot mencari alamat; alokasi tugas sering tumpang tindih manual. | Missions Board interaktif menampilkan daftar penugasan logistik harian. |
| **Penjemputan & Pengantaran** | Menjemput ke lokasi donatur, mengantar dengan navigasi GPS, melakukan pemindaian. | Aplikasi FAR (Navigasi Peta & Pemindai Kamera) | Fokus: "Harus memastikan makanan diserahkan ke alamat dan orang yang tepat." | Takut salah sasaran; rentan dituduh jika tidak ada bukti penyelesaian. | Wajib Pindai (Mandatory Scan) QR Code nirkontak sebagai validasi transaksi mutlak. |
| **Serah Terima & Apresiasi** | Memindai QR Code penerima; memantau kenaikan pangkat di sistem gamifikasi. | Aplikasi FAR (Leaderboard Ranking) | Bangga: "XP saya naik, sedikit lagi mencapai gelar Sultan Relawan!" | Kurang motivasi jangka panjang karena ketiadaan pencatatan apresiasi. | Sistem Gamifikasi Dinamis: poin XP dan kasta peringkat (Trainee → Sultan). |

---

## 2. CJM – Penerima Donasi (Bu Ani)

*Fase perjalanan: Inisiatif & Niat Baik → Pemilihan Misi → Penjemputan & Pengantaran → Serah Terima & Apresiasi*  
*(Tabel yang diberikan identik dengan CJM Relawan, namun berikut penjelasan sesuai konteks peran Penerima)*

| Fase | Aksi | Titik Sentuh | Emosi & Pikiran | Pain Points | Peluang Solusi (FAR) |
|------|------|--------------|------------------|-------------|----------------------|
| **Inisiatif & Niat Baik** | Mencari kegiatan sosial (crowdsourcing) – misalnya mengajukan permintaan donasi atau menunggu ketersediaan. | Kampus, Media Sosial (atau panti asuhan) | Antusias: "Ingin mendapatkan donasi tapi butuh sistem yang jelas." | Niat baik (mendapat bantuan) tidak terwujud karena tidak ada platform terpusat. | Login peran khusus (RBAC) sebagai penerima, dengan akses melihat donasi tersedia. |
| **Pemilihan Misi** | Membuka aplikasi FAR, memilih misi pengantaran (atau klaim donasi) berdasarkan rute terdekat. | Aplikasi FAR (Missions Board) | Termotivasi: "Donasi ini dekat panti, bisa segera diklaim!" | Repot mengetahui alamat donatur; klaim tumpang tindih secara manual. | Missions Board interaktif untuk melihat daftar donasi yang bisa diklaim oleh penerima. |
| **Penjemputan & Pengantaran** | Menjemput ke lokasi donatur, mengantar dengan navigasi GPS, melakukan pemindaian (jika penerima menjemput sendiri). | Aplikasi FAR (Navigasi Peta & Pemindai Kamera) | Fokus: "Harus memastikan makanan diserahkan ke orang yang tepat." | Takut makanan bukan untuk dirinya; tidak ada bukti serah terima. | Wajib Pindai QR Code nirkontak sebagai validasi bahwa donasi sampai ke penerima yang benar. |
| **Serah Terima & Apresiasi** | Memindai QR Code penerima (atau menunjukkan kode); memantau kenaikan pangkat – dalam konteks penerima bisa berupa reputasi atau poin kepercayaan. | Aplikasi FAR (Leaderboard Ranking) | Bangga: "Sistem mencatat saya sebagai penerima terverifikasi, aman dari double-claim." | Tidak ada apresiasi atau catatan kontribusi sebagai penerima (misalnya tingkat kepercayaan). | Sistem Gamifikasi Dinamis memberikan poin kepercayaan atau badge bagi penerima yang aktif dan terverifikasi. |

---

## 3. CJM – Relawan (Rizky)

*Fase perjalanan: Inisiatif & Niat Baik → Pemilihan Misi → Penjemputan & Pengantaran → Serah Terima & Apresiasi*

| Fase | Aksi | Titik Sentuh | Emosi & Pikiran | Pain Points | Peluang Solusi (FAR) |
|------|------|--------------|------------------|-------------|----------------------|
| **Inisiatif & Niat Baik** | Mencari kegiatan sosial (crowdsourcing) untuk mengisi waktu luang. | Kampus, Media Sosial | Antusias: "Ingin bantu distribusi donasi tapi butuh sistem yang jelas." | Niat baik tidak tersalurkan karena ketiadaan platform terpusat. | Login peran khusus (RBAC) sebagai relawan dengan lingkungan tugas mandiri. |
| **Pemilihan Misi** | Membuka aplikasi FAR, memilih misi pengantaran berdasarkan rute terdekat. | Aplikasi FAR (Missions Board) | Termotivasi: "Misi ini searah jalan pulang, poin XP-nya juga lumayan!" | Repot mencari alamat; alokasi tugas sering tumpang tindih manual. | Missions Board interaktif menampilkan daftar penugasan logistik harian. |
| **Penjemputan & Pengantaran** | Menjemput ke lokasi donatur, mengantar dengan navigasi GPS, melakukan pemindaian. | Aplikasi FAR (Navigasi Peta & Pemindai Kamera) | Fokus: "Harus memastikan makanan diserahkan ke alamat dan orang yang tepat." | Takut salah sasaran; rentan dituduh jika tidak ada bukti penyelesaian. | Wajib Pindai (Mandatory Scan) QR Code nirkontak sebagai validasi transaksi mutlak. |
| **Serah Terima & Apresiasi** | Memindai QR Code penerima; memantau kenaikan pangkat di sistem gamifikasi. | Aplikasi FAR (Leaderboard Ranking) | Bangga: "XP saya naik, sedikit lagi mencapai gelar Sultan Relawan!" | Kurang motivasi jangka panjang karena ketiadaan pencatatan apresiasi. | Sistem Gamifikasi Dinamis: poin XP dan kasta peringkat (Trainee → Sultan). |

---

## 4. CJM – Donatur Individu (Siti)

*Fase perjalanan: Kesadaran → Pencarian Penerima → Pelaksanaan Donasi → Pasca-Donasi & Pelaporan*

| Fase | Aksi | Titik Sentuh | Emosi & Pikiran | Pain Points | Peluang Solusi (FAR) |
|------|------|--------------|------------------|-------------|----------------------|
| **Kesadaran** | Melihat makanan berlebih di kulkas/dapur yang masih sangat layak konsumsi. | Kulkas, meja makan rumah | Bersalah: "Sayang jika dibuang, tapi apakah ini masih aman dimakan orang lain?" | Ketidaktahuan standar keamanan pangan sisa skala rumah tangga. | Rekomendasi resep masakan dari bahan sisa menggunakan AI. |
| **Pencarian Penerima** | Mencari secara manual kontak pihak/kurir yang membutuhkan makanan. | Grup WhatsApp, Internet | Repot: "Mencari panti asuhan satu per satu sangat menghabiskan waktu." | Blind spot informasi penerima; tidak ada akses logistik penjemputan. | Integrasi ke peta Radar Penerima dan akses Relawan Kurir secara instan. |
| **Pelaksanaan Donasi** | Memotret makanan melalui aplikasi FAR, menunggu penjemputan, validasi QR. | Aplikasi FAR (Kamera "Polisi Pangan") | Lega: "Prosesnya mudah, makanan dijemput langsung ke rumah." | Ragu apakah makanan bisa cepat disalurkan sebelum basi di jalan. | Verifikasi AI Quality Verification mencegah makanan beracun lolos sistem. |
| **Pasca-Donasi & Pelaporan** | Melihat kontribusi pribadi terhadap pelestarian bumi. | Dasbor SROI Personal di Aplikasi FAR | Termotivasi: "Ternyata donasi kecil saya membantu menghemat literan air!" | Tidak pernah tahu dampak lingkungan riil dari tindakan donasinya. | Dasbor SROI Pribadi menampilkan total porsi terselamatkan dan emisi yang dicegah. |

---

Semua penjelasan di atas disusun berdasarkan tabel yang tersedia dalam file gambar masing-masing, tanpa mengubah isi aslinya.