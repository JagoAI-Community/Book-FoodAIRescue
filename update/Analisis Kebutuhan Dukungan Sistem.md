**2.4.3 Analisis Kebutuhan Dukungan Sistem**. 

Konten ini telah disusun berdasarkan dokumen spesifikasi teknis dan lingkungan pengembangan dari proyek FoodAI Rescue yang ada pada referensi Anda. 

***

### 2.4.3 Analisis Kebutuhan Dukungan Sistem
Analisa kebutuhan dukungan sistem mendefinisikan seluruh infrastruktur teknis, baik dari segi perangkat lunak (*software*), perangkat keras (*hardware*), maupun konfigurasi lingkungan (*environment*) yang disyaratkan agar platform FoodAI Rescue (FAR) dapat beroperasi secara stabil. Mengingat platform ini dirancang menggunakan arsitektur *Client-Server* yang terpisah antara *Frontend* dan *Backend*, maka spesifikasi dukungan sistemnya diuraikan ke dalam tiga kategori berikut:

**1. Kebutuhan Perangkat Lunak (*Software*)**
Untuk membangun dan menjalankan antarmuka (*User Interface*) serta logika peladen (*Server-Side*), sistem disyaratkan menggunakan tumpukan teknologi (*tech stack*) terkini:
*   **Sisi Klien (*Frontend*)**: Aplikasi antarmuka dibangun menggunakan *framework* React.js (v19) yang dikombinasikan dengan TypeScript dan *build tool* Vite agar dapat dieksekusi secara mulus pada *web browser* (melalui antarmuka *localhost:5173*). Tampilan visual mengusung gaya *Glassmorphism* interaktif, yang didukung oleh berbagai pustaka (*library*) khusus seperti `react-leaflet` untuk pemetaan geolokasi, `react-easy-crop` untuk penyesuaian (*cropping*) foto profil dan makanan, serta `lucide-react` untuk ikonografi.
*   **Sisi Server (*Backend*)**: Logika sistem dan manajemen pangkalan data beroperasi dalam lingkungan (*environment*) Node.js menggunakan *framework* API Express.js (v5.x) pada antarmuka *localhost:5000*. Sistem basis data relasional dikelola menggunakan MySQL2 dengan skema *database* utama `foodairescue`.
*   **Pustaka Modul Pendukung (*Library*)**: Pada sisi *backend*, sistem membutuhkan pustaka `bcryptjs` untuk perlindungan enkripsi kata sandi berlapis, `nodemailer` untuk layanan *Simple Mail Transfer Protocol* (SMTP) notifikasi, serta `sharp` sebagai modul kompresi dan manipulasi gambar sebelum foto makanan dikirim ke jaringan AI.
*   **Layanan Pihak Ketiga (API AI)**: Sistem sangat bergantung pada *Application Programming Interface* (API) eksternal, khususnya *Google Gemini API* (`@google/genai` dan `@google/generative-ai`) sebagai inti intelijensi "Polisi Pangan", serta integrasi layanan *pollinations.ai* untuk mendukung fitur *Eco Packaging Generator*.

**2. Kebutuhan Perangkat Keras (*Hardware*)**
Karena pengembangan aplikasi FoodAI Rescue pada fase iterasi awal (v1) ditujukan untuk pengujian lokal, maka dibutuhkan spesifikasi perangkat keras sebagai berikut:
*   **Perangkat Pengembang (*Development*)**: Membutuhkan komputer personal (PC) atau laptop yang sepenuhnya mendukung *Cross-Platform* (Windows, Mac OS, maupun Linux). Mesin pengembang harus mampu menjalankan *local server* (seperti Apache dan MySQL melalui XAMPP/Laragon) serta mengeksekusi minimal dua terminal  Command Node.js secara serentak (untuk *Frontend* dan *Backend*).
*   **Perangkat Pengguna (Klien)**: Pengguna membutuhkan perangkat seluler pintar (*smartphone*) atau komputer yang dilengkapi dengan koneksi internet yang stabil dan *browser* modern. Khusus untuk Donatur, Penerima, dan Relawan, perangkat fisik **wajib dilengkapi dengan fitur kamera yang berfungsi secara normal** guna memfasilitasi pengambilan foto makanan donasi dan pemindaian wajib (*mandatory scan*) Kode QR saat proses validasi serah terima.

**3. Kebutuhan Konfigurasi Lingkungan (*Environment Variables*)**
*   **Sistem Kredensial `.env`**: Agar sistem dapat berjalan secara utuh, arsitektur FAR membutuhkan pengaturan rahasia berbasis `.env` pada *root path* direktori proyek. Konfigurasi ini diwajibkan memuat parameter seperti *port database*, URL pangkalan data, sandi akses *localhost*, dan yang paling krusial adalah kunci rahasia eksekutif berupa `VITE_GEMINI_API_KEY`. Tanpa adanya variabel kunci API ini terkonfigurasi dengan benar, sistem validasi cerdas dan keseluruhan pintu masuk aplikasi tidak akan merespon perintah.