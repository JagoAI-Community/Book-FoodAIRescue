### 2.4.2 Analisis Kebutuhan Fungsional
Analisis kebutuhan fungsional menguraikan spesifikasi kapabilitas yang wajib dimiliki
oleh sistem guna menjawab permasalahan pengguna di lapangan. Merujuk pada
hasil observasi alur distribusi manual (As-Is) serta ekstraksi titik keluhan (pain
points) dari Empathy Map dan User Journey Map, platform yang dirancang harus
mampu menghadirkan solusi berupa otomatisasi verifikasi kelayakan pangan berbasis
Kecerdasan Buatan (AI), pencocokan donasi secara real-time, serta rekapitulasi pelaporan
dampak lingkungan (SROI) secara digital. Oleh karena itu, fungsionalitas yang akan
diimplementasikan pada ekosistem Food AI Rescue diklasifikasikan ke dalam enam
modul utama berikut

**1. Kebutuhan Modul Autentikasi dan Manajemen Akun**
*   Sistem harus mampu memfasilitasi proses pendaftaran (*register*) dan masuk (*login*) yang keamanannya terenkripsi menggunakan algoritma sandi berlapis *bcrypt*.
*   Sistem harus memiliki pendeteksi perutean berbasis peran (*Role-Based Router*) untuk mengarahkan pengguna secara spesifik ke antarmuka 6 (enam) grup akses yang berbeda (Donatur Individu, Donatur Korporat, Penerima, Relawan, Admin, dan SuperAdmin).
*   Sistem harus menyediakan fitur manajemen profil pengguna, yang mencakup utilitas pemotongan gambar (*crop image*) saat pengguna mengunggah foto avatar.

**2. Kebutuhan Modul Manajemen Donasi dan Inventori (Gudang Pangan)**
*   Sistem harus memfasilitasi pihak Donatur untuk membuat daftar donasi makanan baru beserta detail parameter minimum dan maksimum porsi yang tersedia.
*   Sistem harus dilengkapi dengan manajemen inventori otomatis yang mampu menyembunyikan status tayangan donasi dari publik apabila batas waktu konsumsi (kedaluwarsa) telah terlewati.
*   Sistem harus memfasilitasi donatur untuk melakukan validasi serah terima melalui fitur pemindaian Kode QR penerima secara nirkontak saat proses penyerahan berlangsung.

**3. Kebutuhan Modul Integrasi Kecerdasan Buatan (AI)**
*   Sistem wajib terintegrasi dengan layanan *Google Gemini Vision API* sebagai fitur "Polisi Pangan" untuk menjalankan verifikasi otomatis secara *real-time*. AI harus mampu mendeteksi wujud makanan, menilai kelayakan konsumsi, higienitas visual, serta mengevaluasi kehalalan sebelum donasi diterbitkan.
*   Sistem harus memfasilitasi fungsi bagi pengguna untuk memindai bahan sisa makanan guna mendapatkan rekomendasi resep masakan cerdas dari AI.
*   Khusus bagi grup Donatur Korporat (HORECA), sistem harus menyediakan fitur AI Generatif eksklusif berupa *Eco Packaging Editor* (didukung oleh Pollinations.ai) untuk merancang prototipe kemasan ramah lingkungan, serta asisten *CSR Copywriter* untuk otomatisasi pembuatan naskah kampanye sosial.

**4. Kebutuhan Modul Eksplorasi dan Klaim (Radar Penerima)**
*   Sistem harus menyediakan *Map Dashboard* interaktif (memanfaatkan pustaka geolokasi *Leaflet*) yang memungkinkan Mitra Penerima untuk melacak titik ketersediaan donasi pangan di sekitarnya.
*   Sistem harus memungkinkan Penerima melakukan klaim (*booking/checkout*) pesanan makanan untuk mencegah terjadinya insiden klaim ganda (*double-claim*) oleh pihak lain pada stok yang sama.
*   Sistem harus menyediakan *Forum Request* yang memungkinkan Penerima untuk memublikasikan kebutuhan spesifik panti/fasilitas sosial mereka.

**5. Kebutuhan Modul Operasional Logistik dan Gamifikasi (Relawan)**
*   Sistem harus menyediakan Papan Misi Penugasan (*Missions Board*) yang merincikan titik penjemputan donatur dan titik serah terima akhir bagi armada Relawan.
*   Sistem mewajibkan alur pemindaian silang (*mandatory scan*) Kode QR menggunakan kamera aplikasi sebagai prasyarat mutlak verifikasi validitas penyelesaian distribusi logistik.
*   Sistem harus dilengkapi mesin algoritma Gamifikasi (*Leaderboard Ranking Engine*) yang secara otomatis memproses ketepatan waktu misi menjadi poin pengalaman (XP), lalu mengonversinya menjadi kasta peringkat atau medali sosial.

**6. Kebutuhan Modul Pelacakan Dampak Sosial (SROI)**
*   Sistem harus memiliki Dasbor *Sustainability Impact* terpadu yang merekapitulasi rekam jejak aktivitas donasi pengguna.
*   Sistem harus memiliki kalkulator lingkungan yang mampu mengonversi kuantitas porsi makanan yang terselamatkan menjadi data analitik estimasi angka pengurangan emisi jejak karbon (kg CO₂) dan pelestarian air (liter).

**7. Kebutuhan Modul Konfigurasi Pusat (Admin dan SuperAdmin)**
*   Sistem harus menyediakan *Control Panel* operasional bagi Admin Pengelola untuk menindaklanjuti pendaftaran akun manual, membekukan akun yang melakukan pelanggaran, dan mengelola resolusi tiket keluhan pengguna melalui *Support Request Manager*.
*   Sistem harus menyediakan Dasbor Statistik Makro berupa peta panas (*heatmap*) penyebaran donasi pangan.
*   Sistem harus menyediakan instrumen khusus berupa panel *Prompt Engineering Injection*. Panel ini memungkinkan Admin memodifikasi atau menajamkan parameter instruksi batas toleransi AI secara waktu nyata (*real-time*) tanpa perlu mengubah kode sumber (*source code*) aplikasi.
*   Sistem harus memberi hak prerogatif (*Maintenance Mode Trigger*) kepada SuperAdmin untuk mengendalikan penguncian server saat terjadi pemeliharaan, serta memantau rekam log (*system logs*) seluruh aktivitas.