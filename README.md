---

# 🌐 Praktikum 6: Twitter Bootstrap

---

**Mata Kuliah:** Pemrograman Web1

**Dosen Pengampu:** Agung Nugroho, S.Kom., M.Kom.

**Nama:** Zaenal Maulana Rizki

**NIM:** 312410332

**Kelas:** TI.2A.A.4
---

## 💻 **1. File: `index.html`**

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Praktikum 6 Bootstrap</title>

  <!-- Bootstrap CSS -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" 
        rel="stylesheet" 
        crossorigin="anonymous">
</head>
<body>

  <!-- NAVBAR -->
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">Praktikum 6</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item"><a class="nav-link active" href="#">Home</a></li>
          <li class="nav-item"><a class="nav-link" href="#">Artikel</a></li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- CONTAINER -->
  <div class="container mt-4">
    <h1 class="text-center mb-4">Halo, Bootstrap!</h1>
    <button class="btn btn-primary mb-3">Ini Tombol Bootstrap</button>
  </div>

  <!-- GRID SYSTEM -->
  <div class="container">
    <div class="row text-white">
      <div class="col bg-primary p-3">Kolom 1</div>
      <div class="col bg-success p-3">Kolom 2</div>
      <div class="col bg-danger p-3">Kolom 3</div>
    </div>

    <div class="row mt-3">
      <div class="col-md-8 bg-light p-3 border">Main Content (8 kolom)</div>
      <div class="col-md-4 bg-secondary p-3 text-white border">Sidebar (4 kolom)</div>
    </div>
  </div>

  <!-- CARD -->
  <div class="container mt-5">
    <div class="row">
      <div class="col-md-4">
        <div class="card">
          <img src="https://via.placeholder.com/300x200" class="card-img-top" alt="...">
          <div class="card-body">
            <h5 class="card-title">Judul Card 1</h5>
            <p class="card-text">Deskripsi singkat card pertama.</p>
            <a href="#" class="btn btn-primary">Lihat Detail</a>
          </div>
        </div>
      </div>

      <div class="col-md-4">
        <div class="card">
          <img src="https://via.placeholder.com/300x200" class="card-img-top" alt="...">
          <div class="card-body">
            <h5 class="card-title">Judul Card 2</h5>
            <p class="card-text">Deskripsi singkat card kedua.</p>
            <a href="#" class="btn btn-success">Lihat Detail</a>
          </div>
        </div>
      </div>

      <div class="col-md-4">
        <div class="card">
          <img src="https://via.placeholder.com/300x200" class="card-img-top" alt="...">
          <div class="card-body">
            <h5 class="card-title">Judul Card 3</h5>
            <p class="card-text">Deskripsi singkat card ketiga.</p>
            <a href="#" class="btn btn-danger">Lihat Detail</a>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- FORM -->
  <div class="container mt-5 mb-5">
    <h3>Formulir Kontak</h3>
    <div class="mb-3">
      <label for="emailInput" class="form-label">Alamat Email</label>
      <input type="email" class="form-control" id="emailInput" placeholder="nama@contoh.com">
    </div>
    <div class="mb-3">
      <label for="pesanText" class="form-label">Pesan</label>
      <textarea class="form-control" id="pesanText" rows="3"></textarea>
    </div>
    <button type="submit" class="btn btn-primary">Kirim</button>
  </div>

  <!-- Bootstrap JS -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" crossorigin="anonymous"></script>
</body>
</html>
```

---

## 🧾 **2. Penjelasan untuk README.md GitHub**

Gunakan penjelasan berikut untuk file **README.md** di repository `Lab6Web`:

---

# **Praktikum 6: Twitter Bootstrap**

## 🎯 Tujuan

1. Memahami konsep **CSS Framework** dan apa itu **Bootstrap**.
2. Mampu menggunakan **Bootstrap Grid System** untuk layout responsif.
3. Dapat menerapkan **komponen Bootstrap** seperti Navbar, Button, Card, dan Form.

---

## ⚙️ Langkah-Langkah Praktikum

### 1. Setup Bootstrap

Menambahkan library **Bootstrap 5.3.3** melalui **CDN** agar bisa langsung digunakan tanpa instalasi manual.

```html
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
```

---

### 2. Container

Container berfungsi untuk membungkus konten agar memiliki padding dan batas lebar otomatis.

* `.container` → lebar tetap
* `.container-fluid` → lebar penuh (100%)

---

### 3. Grid System

Bootstrap memiliki sistem grid berbasis **12 kolom** untuk membuat layout responsif.
Contoh:

```html
<div class="row">
  <div class="col-md-8">Main Content</div>
  <div class="col-md-4">Sidebar</div>
</div>
```

Hasilnya akan menampilkan layout 8 kolom dan 4 kolom di layar besar, namun otomatis menumpuk di layar kecil.

---

### 4. Komponen: Button

Bootstrap menyediakan berbagai gaya tombol yang bisa digunakan dengan mudah:

```html
<button class="btn btn-primary">Primary</button>
<button class="btn btn-success">Success</button>
<button class="btn btn-danger">Danger</button>
```

---

### 5. Komponen: Navbar

Menambahkan navigasi responsif dengan class `.navbar`:

```html
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <a class="navbar-brand" href="#">Praktikum 6</a>
</nav>
```

---

### 6. Komponen: Card

Card digunakan untuk menampilkan konten seperti gambar dan teks dalam satu blok:

```html
<div class="card">
  <img src="https://via.placeholder.com/300x200" class="card-img-top">
  <div class="card-body">
    <h5 class="card-title">Judul Card</h5>
    <p class="card-text">Deskripsi singkat.</p>
  </div>
</div>
```

---

### 7. Komponen: Form

Membuat form yang rapi dengan class `.form-control` dan `.form-label`:

```html
<div class="mb-3">
  <label for="emailInput" class="form-label">Alamat Email</label>
  <input type="email" class="form-control" id="emailInput" placeholder="nama@contoh.com">
</div>
```

---

## 📸 Screenshot Hasil

> Tambahkan hasil screenshot dari tampilan setiap bagian:

* Setup & Container
* Grid System
* Navbar
* Card
* Form

---

## 🧠 Kesimpulan

Dengan menggunakan **Bootstrap**, proses pembuatan layout web menjadi **lebih cepat, konsisten, dan responsif** tanpa perlu menulis banyak kode CSS manual.

---

Apakah kamu ingin saya lanjutkan juga membuat **`portfolio.html`** (untuk tugas bagian 3: Halaman Portfolio Sederhana) agar sekalian lengkap dengan README-nya?
