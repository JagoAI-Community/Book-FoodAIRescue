***

### 2.5 Analisis Kinerja Sistem
Kinerja sistem merepresentasikan standar minimum dan tolok ukur (benchmark) yang
diterapkan guna memastikan seluruh ekosistem aplikasi Food AI Rescue, khususnya pada
Modul Konfigurasi Pusat (Admin) dan Dasbor Dampak Sosial (SROI), mampu beroperasi
selaras dengan spesifikasi dan perancangan fungsionalnya. Proses evaluasi kinerja dalam
pengembangan platform ini dititikberatkan pada empat parameter fundamental, meliputi:
fungsionalitas antarmuka perangkat lunak, keandalan serta stabilitas jalur komunikasi
data (terutama integrasi Google Gemini API), tingkat responsivitas keamanan sistem,
dan metrik kecepatan muat halaman (page load). Ruang lingkup pengukuran kinerja
ini tidak melibatkan pengujian ketahanan perangkat keras fisik (hardware) di lapangan,
melainkan dibatasi secara ketat pada domain rekayasa perangkat lunak dengan rincian
standar pengujian sebagai berikut:

**1. Kinerja Waktu Respons dan Pemrosesan Media (*Response Time & Media Processing*)**
*   **Optimalisasi *Payload* AI**: Mengingat sistem harus mengirimkan data visual ke server *Google Gemini Vision API*, kinerja waktu respons (*latency*) dijaga agar tetap rendah dengan menggunakan pustaka `sharp` pada sisi *backend*. Sebelum foto makanan dikirimkan ke jaringan AI, gambar akan dikompresi dan dimanipulasi secara otomatis untuk mengurangi beban *bandwith* tanpa menghilangkan fitur visual penting.
*   **Kecepatan Antarmuka (*Frontend*)**: Penggunaan *build tool* Vite pada lingkungan React.js (v19) memastikan waktu muat (*loading time*) halaman yang sangat cepat. Transformasi aplikasi menjadi *Progressive Web App* (PWA) juga memungkinkan *caching* data statis di sisi peramban (*browser*) pengguna, sehingga transisi antar-menu dengan gaya *Glassmorphism* berjalan mulus tanpa hambatan.

**2. Kinerja Akurasi dan Keandalan AI (*AI Accuracy & Reliability*)**
*   **Mitigasi Bias Deteksi (Anti-*Clever Hans Effect*)**: Kinerja "Polisi Pangan" (Gemini AI) sangat bergantung pada akurasi klasifikasi. Sistem dirancang secara tangguh untuk menghindari jalan pintas pembelajaran (*shortcut learning* atau *Clever Hans effect*), di mana AI dapat keliru menilai kelayakan makanan hanya berdasarkan korelasi palsu pada latar belakang gambar, bukan pada objek makanannya. 
*   **Ketahanan terhadap Manipulasi Visual**: Arsitektur *prompt* pada modul AI FAR dimitigasi secara presisi melalui dasbor *Prompt Engineering* Admin agar tidak mudah dikecoh oleh *adversarial patches* (manipulasi visual kecil yang disengaja untuk mengelabui deteksi objek).

**3. Kinerja Konkurensi dan Basis Data (*Database Concurrency*)**
*   **Pencegahan Klaim Ganda (*Double-Claim Prevention*)**: Kinerja basis data MySQL2 diuji pada kondisi di mana beberapa Penerima (fasilitas sosial) mungkin mencoba melakukan klaim ( *booking* ) pada stok makanan yang sama di waktu yang bersamaan. Sistem dikonfigurasi untuk menangani *race-condition* ini secara *real-time*, sehingga status *inventory* langsung berubah menjadi *Reserved* atau *Claimed* dalam hitungan milidetik setelah permintaan pertama divalidasi.

**4. Kinerja Keamanan dan Validasi Lapangan (*Security & Validation*)**
*   **Kriptografi Akses**: Kinerja keamanan data pengguna dijamin melalui proses enkripsi kata sandi berlapis menggunakan algoritma `bcryptjs` sebelum disimpan ke dalam pangkalan data. 
*   **Validasi Nirkontak**: Untuk memastikan efisiensi dan keamanan serah terima makanan di lapangan, kinerja validasi tidak mengandalkan konfirmasi manual, melainkan menggunakan sistem *mandatory scan* (wajib pindai) Kode QR menggunakan kamera *smartphone*. Sistem harus merespon pemindaian ini secara instan untuk memperbarui status pengantaran kurir (Relawan) menjadi *Completed*.

**5. Kinerja Komputasi Analitik dan Gamifikasi (*Analytical Efficiency*)**
*   **Pemrosesan SROI *Real-Time***: Sistem dituntut untuk memiliki kinerja kalkulasi dinamis pada modul Dasbor Dampak Sosial (SROI). Setiap kali transaksi donasi berhasil diselesaikan, algoritma di *backend* harus segera menghitung konversi porsi makanan menjadi angka pengurangan emisi jejak karbon (CO₂) dan penghematan air (liter) tanpa membebani *thread* transaksi utama.
*   **Algoritma Poin XP**: Mesin *Leaderboard Ranking* bekerja secara efisien di latar belakang untuk mendistribusikan poin pengalaman (XP) kepada relawan berdasarkan ketepatan waktu misi, untuk memastikan klasemen peringkat sosial selalu terbarui secara *real-time*.

***