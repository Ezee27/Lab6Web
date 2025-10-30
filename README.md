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
Hasil di browsernya:
---
<img width="1130" height="231" alt="image" src="https://github.com/user-attachments/assets/3a62cfec-97e5-4b21-92c2-a28bf7d567d1" />

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
Hasil di browsernya:
---
<img width="1919" height="270" alt="image" src="https://github.com/user-attachments/assets/0c7ab131-3248-468d-bba2-cce891972ff9" />

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
Hasil di browsernya:
---
<img width="1919" height="319" alt="image" src="https://github.com/user-attachments/assets/6e5b6e4c-2b79-4628-ad62-924df62bb6d5" />

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
Hasil di browsernya:
---
+<img width="1919" height="492" alt="image" src="https://github.com/user-attachments/assets/04602841-b122-407f-8612-68af2afa8de2" />

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
Hasil di browsernya:
---
<img width="1919" height="743" alt="image" src="https://github.com/user-attachments/assets/bf85ea14-f7e4-418c-9e86-f8669aac077b" />

---


**Penjelasan Class:**

* `.form-label` → Memberi styling pada `<label>`.
* `.form-control` → Memberi styling pada `<input>`, `<textarea>`, `<select>`.
* `.mb-3` → Memberi *margin-bottom: 3* (spasi).

---
## Pertanyaan dan Tugas:
---
<img width="778" height="662" alt="image" src="https://github.com/user-attachments/assets/e12e2d14-6c09-4bfb-8984-2e4e58c91315" />

---
## Code Program nya:

---
html
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Layout Sederhana</title>

    <!-- Bootstrap CSS (CDN) -->
    <link
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"
      rel="stylesheet"
      integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH"
      crossorigin="anonymous"
    />

    <!-- Custom CSS -->
    <link rel="stylesheet" href="style.css" />
  </head>

  <body class="bg-page">
    <!-- Header -->
    <header class="brandbar py-3">
      <div class="container">
        <h1 class="brandtitle fw-bold text-secondary">Layout Sederhana</h1>
      </div>
    </header>

    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-primary shadow-sm">
      <div class="container">
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#mainNav"
        >
          <span class="navbar-toggler-icon"></span>
        </button>

        <div id="mainNav" class="collapse navbar-collapse">
          <ul class="navbar-nav me-auto">
            <li class="nav-item">
              <a href="home.html" class="nav-link active">Home</a>
            </li>
            <li class="nav-item">
              <a href="artikel.html" class="nav-link">Artikel</a>
            </li>
            <li class="nav-item">
              <a href="about.html" class="nav-link">About</a>
            </li>
            <li class="nav-item">
              <a href="kontak.html" class="nav-link">Kontak</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <!-- Hero Section -->
    <section class="container mt-3">
      <div class="p-4 bg-light rounded shadow-sm">
        <h2 class="fw-bold mb-2">Hello World!</h2>
        <p class="lead text-secondary mb-3">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum
          lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin
          in leo fringilla, vestibulum mi porta, faucibus felis. Integer
          pharetra est nunc, nec pretium nunc pretium ac.
        </p>
        <a class="btn btn-primary btn-lg" href="#">Learn more »</a>
      </div>
    </section>

    <!-- Main Content -->
    <main class="container my-4">
      <div class="row gx-4 gy-4">
        <!-- Main Column -->
        <div class="col-lg-8">
          <!-- 3 Circles -->
          <div class="row text-center g-4 mt-2">
            <div class="col-md-4">
              <div>
                <div
                  class="circle bg-warning text-white mx-auto d-flex align-items-center justify-content-center"
                >
                  120 × 120
                </div>
                <h5 class="mt-3 fw-semibold">Heading</h5>
                <p class="small text-secondary">
                  Donec sed odio dui. Etiam porta sem malesuada magna mollis
                  euismod.
                </p>
                <a class="btn btn-light btn-sm" href="#">View detail</a>
              </div>
            </div>

            <div class="col-md-4">
              <div>
                <div
                  class="circle bg-primary text-white mx-auto d-flex align-items-center justify-content-center"
                >
                  120 × 120
                </div>
                <h5 class="mt-3 fw-semibold">Heading</h5>
                <p class="small text-secondary">
                  Donec sed odio dui. Etiam porta sem malesuada magna mollis
                  euismod.
                </p>
                <a class="btn btn-light btn-sm" href="#">View detail</a>
              </div>
            </div>

            <div class="col-md-4">
              <div>
                <div
                  class="circle bg-info text-white mx-auto d-flex align-items-center justify-content-center"
                >
                  120 × 120
                </div>
                <h5 class="mt-3 fw-semibold">Heading</h5>
                <p class="small text-secondary">
                  Donec sed odio dui. Etiam porta sem malesuada magna mollis
                  euismod.
                </p>
                <a class="btn btn-light btn-sm" href="#">View detail</a>
              </div>
            </div>
          </div>

          <hr class="my-4" />

          <!-- Featurette 1 -->
          <article class="row align-items-start gy-3">
            <div class="col-4 col-sm-3">
              <div
                class="bg-secondary bg-opacity-50 text-center py-5 rounded"
              >
                150 × 150
              </div>
            </div>
            <div class="col">
              <h3 class="h4 fw-bold text-dark mb-2">
                First featurette heading.
              </h3>
              <p class="mb-0 text-secondary">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                Vestibulum lorem elit, iaculis in nisl volutpat, malesuada
                tincidunt arcu. Proin in leo fringilla, vestibulum mi porta,
                faucibus felis. Integer pharetra est nunc, nec pretium nunc
                pretium ac.
              </p>
            </div>
          </article>

          <hr class="my-4" />

          <!-- Featurette 2 -->
          <article class="row align-items-start gy-3">
            <div class="col">
              <h3 class="h4 fw-bold text-dark mb-2">
                First featurette heading.
              </h3>
              <p class="mb-0 text-secondary">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                Vestibulum lorem elit, iaculis in nisl volutpat, malesuada
                tincidunt arcu. Proin in leo fringilla, vestibulum mi porta,
                faucibus felis. Integer pharetra est nunc, nec pretium nunc
                pretium ac.
              </p>
            </div>
            <div class="col-4 col-sm-3">
              <div
                class="bg-secondary bg-opacity-50 text-center py-5 rounded"
              >
                150 × 150
              </div>
            </div>
          </article>
        </div>

        <!-- Sidebar -->
        <aside class="col-lg-4">
          <div class="card mb-4">
            <div class="card-header bg-primary text-white fw-bold">
              Widget Header
            </div>
            <ul class="list-group list-group-flush">
              <li class="list-group-item"><a href="#">Widget Link</a></li>
              <li class="list-group-item"><a href="#">Widget Link</a></li>
              <li class="list-group-item"><a href="#">Widget Link</a></li>
              <li class="list-group-item"><a href="#">Widget Link</a></li>
              <li class="list-group-item"><a href="#">Widget Link</a></li>
            </ul>
          </div>

          <div class="card">
            <div class="card-header bg-primary text-white fw-bold">
              Widget Text
            </div>
            <div class="card-body text-secondary">
              Vestibulum lorem elit, iaculis in nisl volutpat, malesuada
              tincidunt arcu. Proin in leo fringilla, vestibulum mi porta,
              faucibus felis. Integer pharetra est nunc, nec pretium nunc
              pretium ac.
            </div>
          </div>
        </aside>
      </div>
    </main>

    <!-- Footer -->
    <footer class="bg-dark text-white py-3">
      <div class="container small">
        © 2025 - Universitas Pelita Bangsa
      </div>
    </footer>

    <!-- Bootstrap JS -->
    <script
      src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"
      integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz"
      crossorigin="anonymous"
    ></script>
  </body>
</html>
```
---

## Hasil di browsernya:
---
<img width="1920" height="1117" alt="screencapture-127-0-0-1-5500-tugas-html-2025-10-30-14_55_01" src="https://github.com/user-attachments/assets/2e9a5164-5d2c-4fd2-8cb6-1479864a8c68" />

---
