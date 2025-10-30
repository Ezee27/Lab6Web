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

---

## Setup Bootstrap (Menggunakan CDN)

Kita akan menggunakan **Bootstrap** melalui **CDN (Content Delivery Network)**.
Ini mirip dengan cara kita menyertakan file JavaScript eksternal.
Kita perlu menyertakan file **CSS** di bagian `<head>` dan file **JavaScript** di akhir `<body>`.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Praktikum 6 Bootstrap</title>

    <!-- Bootstrap CSS -->
    <link 
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"
      rel="stylesheet"
      integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH"
      crossorigin="anonymous"
    >
  </head>

  <body>
    <div class="container mt-5 text-center">
      <h1>Halo, Bootstrap!</h1>
      <button class="btn btn-primary mt-3">Ini Tombol Bootstrap</button>
    </div>

    <!-- Bootstrap JS Bundle -->
    <script 
      src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"
      integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz"
      crossorigin="anonymous">
    </script>
  </body>
</html>
```

---

## Materi Praktikum

### 1. Container

Bootstrap mengharuskan konten dibungkus di dalam container untuk mengatur lebar dan perataan.

* **.container**: Memberikan lebar maksimum yang tetap (*fixed-width*) yang berubah pada ukuran layar tertentu.
* **.container-fluid**: Memberikan lebar penuh (*full-width*) 100%.

```html
<div class="container">
</div>

<div class="container-fluid">
</div>
```

---

### 2. Grid System (Sistem Grid)

Ini adalah fitur inti Bootstrap yang menggantikan *float* manual. Sistem grid Bootstrap menggunakan 12 kolom.

* **.row**: Pembungkus untuk kolom. Ini menggantikan kebutuhan akan *clearfix*.
* **.col**: Menandakan sebuah kolom. Jika hanya `.col`, lebarnya akan dibagi rata.
* **.col-{angka}**: Menentukan lebar kolom dari 1 sampai 12. Contoh: `.col-4` berarti lebar 4/12 (sepertiga).
* **.col-{breakpoint}-{angka}**: Menentukan lebar kolom pada ukuran layar tertentu (misal: `md` untuk *medium*).

**Contoh Grid:**
Membuat 3 kolom sama lebar yang di layout Praktikum 4 harus menggunakan `float: left`.
Di Bootstrap, caranya:

```html
<div class="container">
  <div class="row">
    <div class="col-4"></div>
    <div class="col-4"></div>
    <div class="col-4"></div>
  </div>

  <div class="row">
    <div class="col-md-8"></div>
    <div class="col-md-4"></div>
  </div>
</div>
```

> 📝 **Catatan:**
> `col-md-8` berarti di layar *medium* ke atas, lebarnya 8 kolom.
> Di layar kecil, lebarnya otomatis jadi 100% dan menumpuk ke bawah.

---

### 3. Komponen: Button (Tombol)

Bootstrap menyediakan berbagai style tombol.

```html
<button class="btn btn-primary">Primary</button>
<button class="btn btn-secondary">Secondary</button>
<button class="btn btn-success">Success</button>
<button class="btn btn-danger">Danger</button>
```

---

### 4. Komponen: Navbar (Navigasi)

Membuat navigasi *responsive* yang bisa *collapse* (menjadi menu hamburger di mobile) sangat mudah.

```html
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Praktikum 6</a>

    <button 
      class="navbar-toggler" 
      type="button" 
      data-bs-toggle="collapse" 
      data-bs-target="#navbarNav"
    >
      <span class="navbar-toggler-icon"></span>
    </button>

    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item">
          <a class="nav-link active" href="#">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Artikel</a>
        </li>
      </ul>
    </div>
  </div>
</nav>
```

---

### 5. Komponen: Card (Kartu)

Card adalah *container* konten yang fleksibel, menggantikan *widget box* atau *box* dari Praktikum 4.

```html
<div class="card" style="width: 18rem;">
  <img src="..." class="card-img-top" alt="...">
  <div class="card-body">
    <h5 class="card-title">Judul Card</h5>
    <p class="card-text">Ini adalah deskripsi singkat di dalam card.</p>
    <a href="#" class="btn btn-primary">Lihat Detail</a>
  </div>
</div>
```

---

### 6. Komponen: Form (Formulir)

Bootstrap men-*styling* elemen form agar terlihat rapi dan konsisten.
Ini jauh lebih mudah daripada men-*style* form manual seperti di Praktikum 5.

```html
<div class="mb-3">
  <label for="emailInput" class="form-label">Alamat Email</label>
  <input 
    type="email" 
    class="form-control" 
    id="emailInput" 
    placeholder="nama@contoh.com"
  >
</div>

<div class="mb-3">
  <label for="pesanText" class="form-label">Pesan</label>
  <textarea 
    class="form-control" 
    id="pesanText" 
    rows="3"
  ></textarea>
</div>

<button type="submit" class="btn btn-primary">Kirim</button>
```

**Penjelasan Class:**

* `.form-label` → Memberi styling pada `<label>`.
* `.form-control` → Memberi styling pada `<input>`, `<textarea>`, `<select>`.
* `.mb-3` → Memberi *margin-bottom: 3* (spasi).

---

Apakah kamu mau saya bantu tambahkan bagian **preview hasil tampilan** (misalnya screenshot atau contoh hasil render HTML) biar README-nya lebih menarik saat diunggah ke GitHub?
