# 📚 Praktikum Pemrograman Web 2 (CodeIgniter 4)

## 👨‍🎓 Identitas

* Nama: Dira Rohmaeni
* NIM: 312410465
* Kelas: I241E

---

## 📌 Deskripsi

Repository ini berisi hasil praktikum **Pemrograman Web 2** menggunakan framework **CodeIgniter 4** yang meliputi:

* CRUD Artikel
* View Layout & View Cell
* Sistem Login (Authentication)
* Filter (Proteksi Halaman Admin)

---

# 🧪 Praktikum 1 — Pengenalan CodeIgniter 4

## 🎯 Tujuan

Memahami struktur dasar framework CodeIgniter 4 dan cara menjalankan aplikasi.

## ✅ Hasil

* Menjalankan server dengan `php spark serve`
* Menampilkan halaman awal CodeIgniter

📸 Screenshot:

* Halaman welcome CodeIgniter

---

# 🧪 Praktikum 2 — CRUD Artikel

## 🎯 Tujuan

Membuat fitur CRUD (Create, Read, Update, Delete)

## ✅ Fitur

* Menampilkan daftar artikel
* Menambahkan artikel
* Mengedit artikel
* Menghapus artikel

## 🛠️ Komponen

* Model: `ArtikelModel.php`
* Controller: `Artikel.php`
* View: `artikel/index.php`, `form_add.php`, `form_edit.php`

📸 Screenshot:

* Halaman daftar artikel
* Tambah artikel
* Edit artikel
* Hapus artikel

---

# 🧪 Praktikum 3 — View Layout & View Cell

## 🎯 Tujuan

Menggunakan template layout dan komponen dinamis

## ✅ Hasil

* Menggunakan layout utama (`layout/main.php`)
* Menggunakan `extend()` dan `section()`
* Menampilkan sidebar dinamis (Artikel Terbaru)

## 🧠 Konsep

* **View Layout**: Template utama untuk tampilan
* **View Cell**: Komponen reusable untuk menampilkan data dinamis

📸 Screenshot:

* Layout utama
* Sidebar artikel terbaru

---

# 🧪 Praktikum 4 — Login & Authentication

## 🎯 Tujuan

Membuat sistem login dan proteksi halaman admin

## ✅ Fitur

* Login user
* Logout
* Session login
* Proteksi halaman admin menggunakan filter

## 🛠️ Komponen

* Model: `UserModel.php`
* Controller: `User.php`
* View: `user/login.php`
* Filter: `Auth.php`

## 🔐 Alur Login

1. User menginput email & password
2. Sistem mencocokkan data di database
3. Jika valid → login berhasil
4. Redirect ke halaman admin

## 🧠 Auth Filter

* Digunakan untuk membatasi akses halaman admin
* Jika belum login → redirect ke login

📸 Screenshot:

* Halaman login
* Login berhasil
* Database user
* Filter redirect ke login

---

# ⚙️ Konfigurasi

## 🔗 Database

Edit file `.env`:

```
database.default.hostname = localhost
database.default.database = lab_ci4
database.default.username = root
database.default.password =
database.default.DBDriver = MySQLi
```

---

# 🚀 Cara Menjalankan

1. Clone repository:

```
git clone https://github.com/username/repository.git
```

2. Masuk ke folder project:

```
cd project-folder
```

3. Jalankan server:

```
php spark serve
```

4. Buka browser:

```
http://localhost:8080
```

---

# 🎯 Kesimpulan

Dengan menggunakan CodeIgniter 4:

* Pengembangan aplikasi menjadi lebih terstruktur
* Kode lebih rapi dan reusable
* Memiliki sistem keamanan (login & filter)

---

# 🙌 Penutup

Demikian hasil praktikum ini dibuat sebagai bentuk pemahaman terhadap materi Pemrograman Web 2.

Terima kasih.
