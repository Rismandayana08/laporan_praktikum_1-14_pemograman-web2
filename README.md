# laporan_praktikum_1-14
# Nama : Aldi Rismandayana
# Kelas : I241A
# Nim : 312410015

## Halaman Login
<img width="2861" height="1700" alt="image" src="https://github.com/user-attachments/assets/cf703271-207a-4edb-9f88-3d49fffc244e" />

## Halaman Admin
<img width="2880" height="1800" alt="image" src="https://github.com/user-attachments/assets/ffb5c001-9aa2-4d99-a905-dd0ac3d893cc" />

## Tampilan Kelola Artikel ada fitur hapus dan ubah
<img width="2861" height="1093" alt="image" src="https://github.com/user-attachments/assets/c014aa57-1bc4-49dd-bb8f-97ccd5ecb5ba" />
<img width="997" height="1098" alt="image" src="https://github.com/user-attachments/assets/38051484-3d78-40de-bac4-c0ba118802e0" />
<img width="2880" height="1800" alt="image" src="https://github.com/user-attachments/assets/784996ac-6af2-472e-a270-9fc27c230079" />

## Tambah Artikel
<img width="1143" height="1222" alt="image" src="https://github.com/user-attachments/assets/a1cd97f8-2add-450e-a712-b6c1d38a0572" />
<img width="2880" height="1800" alt="image" src="https://github.com/user-attachments/assets/97402e14-cb1a-40cf-9221-a12a878a5831" />

## Tampilan Layout Sederhana
<img width="2860" height="1524" alt="image" src="https://github.com/user-attachments/assets/0259e42b-b7c0-48da-94cc-7f6d5da21610" />

## Tampilan Artikel
<img width="2880" height="1800" alt="image" src="https://github.com/user-attachments/assets/07948fc9-7bca-4ad6-933c-501a7d4b9809" />

## Tampilan About
<img width="2880" height="1800" alt="image" src="https://github.com/user-attachments/assets/1d1a7ae5-0ce2-43b1-89bd-9a534236ecf8" />

## Tampilan Kontak
<img width="2880" height="1800" alt="image" src="https://github.com/user-attachments/assets/deb4163a-1a9d-4be0-a0f7-e890890b8339" />

## Logout
<img width="374" height="234" alt="image" src="https://github.com/user-attachments/assets/961e40d8-c8c5-4404-9f18-2c4c5e5b9b41" />

 saya mendokumentasikan langkah demi langkah perjalanan saya membangun platform web secara *End-to-End*, mulai dari konfigurasi dasar framework CodeIgniter 4, perancangan RESTful API, hingga integrasi *Frontend* modern sebagai *Single Page Application* (SPA) menggunakan VueJS.

Berikut adalah detail teknis pengerjaan dari setiap modul praktikum yang telah saya selesaikan:

---

### 🚀 Bagian 1: Fondasi Backend & Pengembangan Framework (CodeIgniter 4)

*   **Praktikum 1: Pengenalan PHP Framework (CodeIgniter 4) & Konsep MVC**
    *   Melakukan konfigurasi *environment* pengembangan dengan mengaktifkan ekstensi krusial pada `php.ini` di XAMPP, seperti `php-intl`, `php-json`, dan `php-mysqlnd`[span_0](start_span)[span_0](end_span).
    *   Mengaktifkan mode *debugging* dengan mengubah nilai `CI_ENVIRONMENT` menjadi `development` pada file `.env` untuk mempermudah pelacakan *error*[span_1](start_span)[span_1](end_span).
    *   Memahami struktur direktori CodeIgniter 4 dan mengimplementasikan arsitektur MVC (Model-View-Controller) dengan mengatur *Routing* dasar dan menggunakan Spark CLI (`php spark routes`)[span_2](start_span)[span_2](end_span).
    *   Membuat sistem *templating* dengan memecah komponen antarmuka menjadi *header*, *content*, dan *footer*[span_3](start_span)[span_3](end_span).

*   **Praktikum 2: Framework Lanjutan (CRUD)**
    *   Merancang database `lab_ci4` dan membuat tabel `artikel` yang berisi *field* `id`, `judul`, `isi`, `gambar`, `status`, dan `slug`[span_4](start_span)[span_4](end_span).
    *   Menghubungkan database menggunakan file `.env` dan membuat `ArtikelModel` dengan mendefinisikan properti `$allowedFields`[span_5](start_span)[span_5](end_span).
    *   Membangun fungsi CRUD (Create, Read, Update, Delete) di dalam *Controller* `Artikel.php`, lengkap dengan validasi form menggunakan `\Config\Services::validation()` untuk memastikan *field* judul wajib diisi (*required*)[span_6](start_span)[span_6](end_span).

*   **Praktikum 3: View Layout dan View Cell**
    *   Membersihkan kode antarmuka menggunakan *View Layout* dengan fungsi `$this->extend()` dan `$this->section()` yang merujuk pada template utama `layout/main.php`[span_7](start_span)[span_7](end_span).
    *   Mengimplementasikan *View Cell* (`App\Cells\ArtikelTerkini`) untuk merender komponen UI secara dinamis dan terisolasi[span_8](start_span)[span_8](end_span).
    *   Komponen ini menarik data artikel terbaru dari database menggunakan klausa `orderBy('created_at', 'DESC')` dan menampilkannya sebagai *widget sidebar*[span_9](start_span)[span_9](end_span).

*   **Praktikum 4: Framework Lanjutan (Modul Login)**
    *   Membangun sistem autentikasi dengan menambahkan tabel `user` (*username*, *useremail*, *userpassword*) dan men- *generate* data *dummy* menggunakan *Database Seeder* (`UserSeeder`) lengkap dengan enkripsi `password_hash()`[span_10](start_span)[span_10](end_span).
    *   Membuat proses *login* di *Controller* menggunakan fungsi verifikasi `password_verify()` dan mengelola *Session* login pengguna[span_11](start_span)[span_11](end_span).
    *   Mengamankan rute *platform web* dengan membuat kelas *Filter* (`app/Filters/Auth.php`) yang memeriksa *session*. Filter ini disematkan pada konfigurasi `Routes.php` menggunakan fitur *Route Grouping* untuk memproteksi direktori `/admin`[span_12](start_span)[span_12](end_span).

---

### ⚡ Bagian 2: Interaktivitas Data (AJAX)

*   **Praktikum 8: Dasar AJAX**
    *   Mengadopsi library jQuery (`jquery-3.6.0.min.js`) untuk melakukan *HTTP request* asinkron sehingga pembaruan data terjadi di latar belakang tanpa memuat ulang ( *reload*) halaman web[span_13](start_span)[span_13](end_span).
    *   Membuat `AjaxController.php` yang mengembalikan respon data dari Model dalam format JSON menggunakan `$this->response->setJSON()`[span_14](start_span)[span_14](end_span).
    *   Menambahkan fungsi JavaScript khusus untuk memunculkan pesan indikator "*Loading data...*" saat proses pengambilan *fetch* data sedang berlangsung[span_15](start_span)[span_15](end_span).

*   **Praktikum 9: AJAX Pagination dan Search**
    *   Memperbarui method *backend* untuk menerima parameter pencarian (`?q=`) dan kategori (`?kategori_id=`) yang dieksekusi menggunakan *Query Builder* `like` dan `where`[span_16](start_span)[span_16](end_span).
    *   Mengimplementasikan fungsi `$builder->paginate()` untuk memecah data per halaman[span_17](start_span)[span_17](end_span).
    *   Di sisi *frontend*, memanfaatkan `$.ajax` untuk menangkap objek JSON yang berisi `data.artikel` dan `data.pager`, lalu melakukan manipulasi *Document Object Model* (DOM) secara dinamis untuk merender isi tabel dan tombol navigasi *pagination*[span_18](start_span)[span_18](end_span).

---

### 🌐 Bagian 3: Web Services & Frontend Modern (VueJS)

*   **Praktikum 10: Implementasi RESTful API**
    *   Mentransformasi fungsi CodeIgniter menjadi RESTful API menggunakan class `ResourceController` dan `ResponseTrait`[span_19](start_span)[span_19](end_span).
    *   Membangun *endpoint* khusus (`/post`) yang menyediakan fungsi `index` (GET), `show` (GET detail), `create` (POST), `update` (PUT), dan `delete` (DELETE)[span_20](start_span)[span_20](end_span).
    *   Setiap proses modifikasi database dikonfigurasi untuk mengembalikan respon JSON standar dengan *HTTP Status Codes* (misal: 200 OK, 201 Created) dan telah diuji secara menyeluruh menggunakan metode `x-www-form-urlencoded` pada aplikasi Postman[span_21](start_span)[span_21](end_span).

*   **Praktikum 11: Pengenalan VueJS dan API Integration**
    *   Mengembangkan *Frontend* menggunakan Framework VueJS 3 dan *library* `Axios` (keduanya dimuat via CDN) untuk mengonsumsi REST API *backend*[span_22](start_span)[span_22](end_span).
    *   Menerapkan *Data Binding* reaktif dari VueJS; menggunakan direktif `v-for` untuk me-*looping* data JSON ke dalam tabel, dan `v-model` untuk sinkronisasi input pada *form modal* Tambah/Ubah Data[span_23](start_span)[span_23](end_span).
    *   Mengontrol *state* antarmuka UI dengan `@click` dan `v-if` untuk membuka atau menyembunyikan *modal popup* tanpa memerlukan manipulasi DOM manual[span_24](start_span)[span_24](end_span).

*   **Praktikum 12: VueJS Komponen dan Routing (Single Page Application)**
    *   Meningkatkan struktur *Frontend* menjadi *Single Page Application* (SPA) sejati dengan mengintegrasikan library Vue Router (`vue-router.global.js`)[span_25](start_span)[span_25](end_span).
    *   Memecah logika JavaScript ke dalam file komponen yang terisolasi secara modular, yakni `Home.js` dan `Artikel.js`[span_26](start_span)[span_26](end_span).
    *   Melakukan pemetaan rute (`createRouter` dan `createWebHashHistory`) serta memodifikasi struktur HTML utama dengan tag `<router-link>` dan `<router-view>` untuk perpindahan antar halaman yang kilat tanpa *hard-reload* pada *browser*[span_27](start_span)[span_27](end_span).

*   **Praktikum 13: VueJS Autentikasi dan Navigation Guards**
    *   Membangun mekanisme *Client-Side Security* dengan menyiapkan API Endpoint `/api/login` di *backend* CI4 yang akan merespon dengan mengembalikan kode *Token* berbasis `base64_encode` apabila kredensial *user* valid[span_28](start_span)[span_28](end_span).
    *   Merancang komponen `Login.js` di *Frontend* yang menangkap *token* tersebut dan menyimpannya secara aman di `localStorage` (*browser*) dengan *flag* `isLoggedIn`[span_29](start_span)[span_29](end_span).
    *   Mengamankan komponen *Vue* menggunakan fitur *Navigation Guards* (`router.beforeEach`). Rute yang dilindungi tanda `meta: { requiresAuth: true }` akan secara otomatis menolak akses dan melempar *user* kembali ke halaman *login* jika tidak terautentikasi[span_30](start_span)[span_30](end_span).

*   **Praktikum 14: Keamanan API, Autentikasi Token, dan Axios Interceptors**
    *   Menyempurnakan proteksi secara *End-to-End* dengan metode *Server-Side Security* berbasis Token[span_31](start_span)[span_31](end_span).
    *   Pada *backend* CodeIgniter, saya membuat `ApiAuthFilter` (di dalam `app/Filters/`) yang bertugas mengekstrak dan memvalidasi `Authorization: Bearer <token>` dari *HTTP Header*. Filter ini diterapkan ke rute POST, PUT, dan DELETE agar database terlindungi dari tembakan API ilegal (misalnya dari Postman), dan akan merespon dengan error `401 Unauthorized` jika *token* kosong atau salah[span_32](start_span)[span_32](end_span).
    *   Pada *Frontend* VueJS, saya mengonfigurasi fitur tingkat lanjut *Axios Interceptors* (`axios.interceptors.request.use`). Fitur ini secara otomatis menyuntikkan *token* dari `localStorage` ke dalam setiap *Header HTTP request* yang keluar, sehingga proses interaksi data antar *platform web* berjalan aman dan tanpa hambatan di latar belakang[span_33](start_span)[span_33](end_span).

---
