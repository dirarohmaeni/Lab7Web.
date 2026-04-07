# 📚 Praktikum Pemrograman Web 2 — CodeIgniter 4

## 👨‍🎓 Identitas Mahasiswa

* Nama  : Dira Rohmaeni
* NIM   : 312410465
* Kelas : I241E

---

# 📌 Deskripsi Project

Project ini merupakan hasil praktikum mata kuliah **Pemrograman Web 2** menggunakan framework **CodeIgniter 4**.

Aplikasi yang dibuat adalah **Portal Berita sederhana** yang memiliki fitur:

* CRUD Artikel
* Layout Template
* Sidebar dinamis (View Cell)
* Sistem Login (Authentication)
* Proteksi halaman admin (Filter)

---

# ⚙️ Teknologi yang Digunakan

* PHP 8
* CodeIgniter 4
* MySQL (XAMPP)
* HTML, CSS

---

# 📁 Struktur Project

```bash
app/
 ├── Controllers/
 │   ├── Artikel.php
 │   └── User.php
 ├── Models/
 │   ├── ArtikelModel.php
 │   └── UserModel.php
 ├── Views/
 │   ├── artikel/
 │   ├── user/
 │   ├── layout/
 │   └── components/
 ├── Filters/
 │   └── Auth.php
```

---

# 🧪 Praktikum 1 — Instalasi & Routing

## 🎯 Tujuan

Memahami dasar CodeIgniter 4 dan routing.

## 🧠 Hasil

* Menjalankan server dengan `php spark serve`
* Mengakses route:

  * `/`
  * `/about`
  * `/contact`

## 📸 Halaman Welcome
![FOTO](https://github.com/dirarohmaeni/Lab7Web./blob/e355dcdcebec95046142d5d53b7b3b382be30e65/LAB11_CI/PRAKTIKUM1/Screenshot%202026-04-02%20101715.png)

---

# 🧪 Praktikum 2 — CRUD Artikel

## 🎯 Tujuan

Membuat fitur CRUD menggunakan MVC.

## ✅ Fitur

* Menampilkan artikel
* Menambahkan artikel
* Mengedit artikel
* Menghapus artikel

## 🧠 Penjelasan

* Model digunakan untuk mengakses database
* Controller sebagai penghubung logic
* View untuk tampilan

## 📸 Halaman List Artikel
![foto](https://github.com/dirarohmaeni/Lab7Web./blob/e355dcdcebec95046142d5d53b7b3b382be30e65/LAB11_CI/PRAKTIKUM2/list.png)

## 📸 Halaman Tambah Artikel
![foto](https://github.com/dirarohmaeni/Lab7Web./blob/e355dcdcebec95046142d5d53b7b3b382be30e65/LAB11_CI/PRAKTIKUM2/tambah.png)

## 📸 Halaman Edit Artikel
![foto](https://github.com/dirarohmaeni/Lab7Web./blob/e355dcdcebec95046142d5d53b7b3b382be30e65/LAB11_CI/PRAKTIKUM2/edit.png)

## 📸 Halaman Hapus Artikel
![foto](https://github.com/dirarohmaeni/Lab7Web./blob/e355dcdcebec95046142d5d53b7b3b382be30e65/LAB11_CI/PRAKTIKUM2/hapus.png)

---

# 🧪 Praktikum 3 — View Layout & View Cell

## 🎯 Tujuan

Menggunakan template dan komponen reusable.

## ✅ Implementasi

### 🔹 View Layout

Menggunakan:

```php
<?= $this->extend('layout/main') ?>
```

Manfaat:

* Tampilan lebih rapi
* Tidak perlu copy-paste header/footer

---

### 🔹 View Cell

Digunakan untuk sidebar artikel terbaru.

```php
<?= view_cell('App\\Cells\\ArtikelTerbaru::render') ?>
```

Manfaat:

* Komponen dinamis
* Bisa digunakan ulang

---

## 📸 Halaman Layout Utama
![foto](https://github.com/dirarohmaeni/Lab7Web./blob/e355dcdcebec95046142d5d53b7b3b382be30e65/LAB11_CI/PRAKTIKUM3/utama.png)

## 📸 Halaman Sidebar Artikel Baru
![foto](https://github.com/dirarohmaeni/Lab7Web./blob/e355dcdcebec95046142d5d53b7b3b382be30e65/LAB11_CI/PRAKTIKUM2/Screenshot%202026-04-03%20195035.png)

---

# 🧪 Praktikum 4 — Login & Authentication

## 🎯 Tujuan

Membuat sistem login dan keamanan halaman.

---

## 🔐 Sistem Login

### Alur:

1. User memasukkan email & password
2. Sistem memverifikasi data di database
3. Password dicek menggunakan `password_verify`
4. Jika valid → login berhasil

---

## 🔐 Session

Digunakan untuk menyimpan status login:

```php
session()->set([
 'logged_in' => true
]);
```

---

## 🔐 Auth Filter

Digunakan untuk membatasi akses halaman admin.

```php
if (!session()->get('logged_in')) {
    return redirect()->to('/user/login');
}
```

---

## 🔐 Logout

```php
session()->destroy();
```

---

## 📸 Database User
![foto](https://github.com/dirarohmaeni/Lab7Web./blob/e355dcdcebec95046142d5d53b7b3b382be30e65/LAB11_CI/PRAKTIKUM5/database_user.png)

## 📸 Halaman Login
![foto](https://github.com/dirarohmaeni/Lab7Web./blob/e355dcdcebec95046142d5d53b7b3b382be30e65/LAB11_CI/PRAKTIKUM5/login.png)

## 📸 Filter Redirect
![foto](https://github.com/dirarohmaeni/Lab7Web./blob/e355dcdcebec95046142d5d53b7b3b382be30e65/LAB11_CI/PRAKTIKUM5/filter_redirect.png)

---

# ⚙️ Konfigurasi Database

Edit file `.env`:

```ini
database.default.hostname = localhost
database.default.database = lab_ci4
database.default.username = root
database.default.password =
database.default.DBDriver = MySQLi
```

---

# 🚀 Cara Menjalankan Project

1. Jalankan XAMPP (Apache & MySQL)
2. Masuk folder project
3. Jalankan:

```bash
php.exe spark serve
```

4. Buka:

```bash
http://localhost:8080
```

---

# 🎯 Kesimpulan

Dari praktikum ini dapat disimpulkan bahwa:

* CodeIgniter 4 mempermudah pengembangan web
* Konsep MVC membuat kode lebih terstruktur
* View Layout dan View Cell meningkatkan efisiensi
* Sistem login dan filter meningkatkan keamanan aplikasi

---

# 🙌 Penutup

Project ini dibuat sebagai bentuk pemahaman terhadap materi Pemrograman Web 2.

Terima kasih.
