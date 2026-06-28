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

# Laporan Praktikum Pemrograman Web 2

## Implementasi AJAX, REST API, dan VueJS pada Aplikasi Web Berbasis CodeIgniter 4

### Deskripsi

Proyek ini merupakan hasil praktikum Pemrograman Web 2 yang mencakup implementasi AJAX, REST API, VueJS, autentikasi, dan keamanan API menggunakan CodeIgniter 4 sebagai backend dan VueJS sebagai frontend.

---

## Praktikum yang Dikerjakan

### Praktikum 8 - AJAX CRUD

Fitur yang dibuat:

* Menampilkan data artikel
* Menambah artikel
* Mengubah artikel
* Menghapus artikel
* Semua proses menggunakan AJAX tanpa reload halaman

### Praktikum 9 - AJAX Pagination dan Search

Fitur yang dibuat:

* Pagination data artikel
* Pencarian artikel
* Filter kategori
* Sorting data
* Loading indicator

### Praktikum 10 - REST API

Membuat REST API menggunakan CodeIgniter 4 dengan endpoint:

* GET `/post`
* GET `/post/{id}`
* POST `/post`
* PUT `/post/{id}`
* DELETE `/post/{id}`

### Praktikum 11 - VueJS Dasar

Fitur yang dibuat:

* Menampilkan data artikel dari API
* Menambah data
* Mengubah data
* Menghapus data
* Integrasi Axios dengan REST API

### Praktikum 12 - VueJS SPA dan Routing

Fitur yang dibuat:

* Komponen VueJS
* Vue Router
* Navigasi tanpa reload halaman
* Halaman Home, Artikel, dan About

### Praktikum 13 - Autentikasi dan Navigation Guards

Fitur yang dibuat:

* Login
* Logout
* Penyimpanan token pada LocalStorage
* Proteksi halaman menggunakan Navigation Guards

### Praktikum 14 - Keamanan API dan Axios Interceptors

Fitur yang dibuat:

* Token Authentication
* API Filter pada CodeIgniter 4
* Axios Request Interceptor
* Axios Response Interceptor
* Penanganan error 401 secara otomatis

---

## Teknologi yang Digunakan

### Backend

* PHP 8.2
* CodeIgniter 4
* MySQL

### Frontend

* VueJS 3
* Vue Router
* Axios
* jQuery
* Bootstrap 5

### Tools

* XAMPP
* Visual Studio Code
* Postman
* Git

---

## Struktur Proyek

```text
ci4/
├── app/
├── public/
├── writable/
└── .env

lab8_vuejs/
├── index.html
├── assets/
│   ├── css/
│   └── js/
└── README.md
```

---

## Cara Menjalankan Aplikasi

### Backend

```bash
cd ci4
composer install
php spark serve
```

Akses:

```text
http://localhost:8080
```

### Frontend

Buka folder:

```text
lab8_vuejs
```

Kemudian jalankan menggunakan Live Server atau browser.

---

## Dokumentasi API

| Method | Endpoint   | Keterangan                 |
| ------ | ---------- | -------------------------- |
| GET    | /post      | Menampilkan semua artikel  |
| GET    | /post/{id} | Menampilkan detail artikel |
| POST   | /post      | Menambah artikel           |
| PUT    | /post/{id} | Mengubah artikel           |
| DELETE | /post/{id} | Menghapus artikel          |
| POST   | /api/login | Login pengguna             |



Repositori ini berisi kumpulan tugas praktikum mata kuliah **Pemrograman Web 2** di Universitas Pelita Bangsa.

##  Deskripsi Projek
Projek ini dibuat untuk memenuhi tugas praktikum mengenai pengembangan aplikasi web. Aplikasi ini dibangun menggunakan framework **CodeIgniter 4** untuk mengimplementasikan konsep MVC (Model-View-Controller) serta pengelolaan database menggunakan MySQL.

## Teknologi yang Digunakan
- **PHP** 8.x
- **Framework:** CodeIgniter 4
- **Database:** MySQL (via XAMPP)
- **Front-end:** HTML, CSS, Bootstrap

## Struktur Folder
```text
/
├── app/            # Source code utama (Controllers, Models, Views)
├── public/         # File publik (assets, css, js)
├── writable/       # Log dan cache
├── .env            # Konfigurasi environment
└── README.md       # Dokumentasi ini
```




## Kesimpulan

Melalui praktikum ini berhasil dibuat aplikasi web modern menggunakan CodeIgniter 4 dan VueJS yang menerapkan:

* AJAX untuk komunikasi data tanpa reload halaman
* REST API sebagai layanan backend
* VueJS untuk frontend interaktif
* SPA menggunakan Vue Router
* Autentikasi berbasis token
* Keamanan API menggunakan Filter dan Axios Interceptors



**Pemrograman Web 2**
**Universitas Pelita Bangsa**
**Tahun Akademik 2025/2026**
