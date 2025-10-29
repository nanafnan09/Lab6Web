# Lab6Web

Nama: Afnan Dika Ramadhan 

NIM : 312410518

Kelas: TI24.A5

# STEP BY STEP LAB6WEB

1.  Buatlah file baru yang bernama `index.html`

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Praktikum 6 Bootstrap</title>

    <!-- Bootstrap CSS CDN -->
    <link
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"
      rel="stylesheet"
      integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH"
      crossorigin="anonymous"
    />
  </head>
  <body>
    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark mb-4">
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
            <li class="nav-item"><a class="nav-link" href="#">Artikel</a></li>
            <li class="nav-item">
              <a class="nav-link" href="form.html">Form</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="portofolio.html">Portfolio</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <!-- Container -->
    <div class="container">
      <h1 class="mb-3">Halo, Bootstrap!</h1>
      <button class="btn btn-primary mb-4">Ini Tombol Bootstrap</button>

      <!-- Grid System -->
      <div class="row mb-4">
        <div class="col-4 bg-light p-3 border">Kolom 1</div>
        <div class="col-4 bg-light p-3 border">Kolom 2</div>
        <div class="col-4 bg-light p-3 border">Kolom 3</div>
      </div>

      <div class="row mb-4">
        <div class="col-md-8 bg-secondary text-white p-3">
          Main Content (8 Kolom)
        </div>
        <div class="col-md-4 bg-dark text-white p-3">Sidebar (4 Kolom)</div>
      </div>

      <!-- Card -->
      <div class="row">
        <div class="col-md-4">
          <div class="card">
            <img
              src="https://via.placeholder.com/300x200"
              class="card-img-top"
              alt="..."
            />
            <div class="card-body">
              <h5 class="card-title">Judul Card 1</h5>
              <p class="card-text">Deskripsi singkat card pertama.</p>
              <a href="#" class="btn btn-primary">Lihat Detail</a>
            </div>
          </div>
        </div>

        <div class="col-md-4">
          <div class="card">
            <img
              src="https://via.placeholder.com/300x200"
              class="card-img-top"
              alt="..."
            />
            <div class="card-body">
              <h5 class="card-title">Judul Card 2</h5>
              <p class="card-text">Deskripsi singkat card kedua.</p>
              <a href="#" class="btn btn-success">Lihat Detail</a>
            </div>
          </div>
        </div>

        <div class="col-md-4">
          <div class="card">
            <img
              src="https://via.placeholder.com/300x200"
              class="card-img-top"
              alt="..."
            />
            <div class="card-body">
              <h5 class="card-title">Judul Card 3</h5>
              <p class="card-text">Deskripsi singkat card ketiga.</p>
              <a href="#" class="btn btn-danger">Lihat Detail</a>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Bootstrap JS -->
    <script
      src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"
      integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz"
      crossorigin="anonymous"
    ></script>
  </body>
</html>

```

![foto](https://github.com/nanafnan09/Lab6Web/blob/41157ad6e6ac4c4adc4521b9ac429025cec8937e/LAB6%20image/Tampilan%201.png)

`index.html` adalah halaman beranda utama. Fungsinya adalah menampilkan contoh dasar penggunaan Bootstrap 5, seperti grid system, tombol, dan komponen Card, untuk menunjukkan tata letak dan styling halaman web menggunakan framework tersebut.


2. Buatlah file baru yang bernama `form.html`
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Refactor Form - Praktikum 6 Bootstrap</title>
    <link
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"
      rel="stylesheet"
      crossorigin="anonymous"
    />

    <script>
      function validateForm() {
        var nama = document.forms["myForm"]["nama"].value; //
        var usia = document.forms["myForm"]["usia"].value; //

        if (nama == "") {
          //
          alert("Nama harus diisi.");
          document.forms["myForm"]["nama"].focus();
          return false;
        }

        if (usia == "") {
          //
          alert("Usia harus diisi.");
          document.forms["myForm"]["usia"].focus();
          return false;
        }

        if (isNaN(usia)) {
          //
          alert("Usia harus berupa angka.");
          document.forms["myForm"]["usia"].focus();
          return false;
        }

        alert("Form berhasil divalidasi dan siap untuk disubmit!");
        return true;
      }
    </script>
  </head>
  <body>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
      <div class="container">
        <a class="navbar-brand" href="#">Layout Sederhana</a>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarNav"
          aria-controls="navbarNav"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav">
            <li class="nav-item">
              <a class="nav-link" href="index.html">Home</a>
            </li>
            <li class="nav-item"><a class="nav-link" href="#">Artikel</a></li>
            <li class="nav-item">
              <a class="nav-link" href="portofolio.html">About</a>
            </li>
            <li class="nav-item">
              <a class="nav-link active" aria-current="page" href="form.html"
                >Kontak</a
              >
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <div class="container py-5">
      <div class="row justify-content-center">
        <div class="col-md-6">
          <h2 class="mb-4">Form Pendaftaran (Refactored dengan Bootstrap)</h2>

          <form
            name="myForm"
            action="/submit-data"
            onsubmit="return validateForm()"
            method="post"
          >
            <div class="mb-3">
              <label for="nama" class="form-label">Nama:</label>
              <input
                type="text"
                id="nama"
                name="nama"
                class="form-control"
                required
              />
            </div>

            <div class="mb-3">
              <label for="usia" class="form-label">Usia:</label>
              <input
                type="text"
                id="usia"
                name="usia"
                class="form-control"
                required
              />
            </div>

            <button type="submit" class="btn btn-primary">Submit</button>
          </form>
        </div>
      </div>
    </div>

    <footer class="bg-dark text-white text-center py-3 mt-5">
      <div class="container">
        <p class="mb-0">&copy; 2021 - Universitas Pelita Bangsa</p>
      </div>
    </footer>

    <script
      src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"
      crossorigin="anonymous"
    ></script>
  </body>
</html>
```
![foto](https://github.com/nanafnan09/Lab6Web/blob/41157ad6e6ac4c4adc4521b9ac429025cec8937e/LAB6%20image/Tampilan%202.png)

`form.html` berfungsi sebagai halaman Kontak atau Pendaftaran. Halaman ini menampilkan sebuah form sederhana dengan kolom Nama dan Usia yang telah di-styling menggunakan Bootstrap. Selain itu, file ini juga menyertakan script JavaScript untuk melakukan validasi sisi klien dasar pada input form tersebut sebelum data dikirim (submit).

3. Buatlah file baru yang bernama `portofolio.html`

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Tugas Portfolio Sederhana</title>
    <link
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"
      rel="stylesheet"
      crossorigin="anonymous"
    />
    <style>
      .img-circle {
        border-radius: 50%;
        object-fit: cover;
        width: 400px;
        height: 400px;
      }
    </style>
  </head>
  <body>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark shadow-sm">
      <div class="container">
        <a class="navbar-brand" href="#">Portofolio Saya</a>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarNav"
          aria-controls="navbarNav"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav ms-auto">
            <li class="nav-item">
              <a class="nav-link" href="index.html">Home</a>
            </li>
            <li class="nav-item"><a class="nav-link" href="#">Artikel</a></li>
            <li class="nav-item">
              <a class="nav-link active" aria-current="page" href="#about"
                >About</a
              >
            </li>
            <li class="nav-item">
              <a class="nav-link" href="form.html">Kontak</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <section id="about" class="py-5">
      <div class="container">
        <h2 class="text-center mb-5">Tentang Saya</h2>
        <div class="row align-items-center">
          <div class="col-md-4 text-center mb-4 mb-md-0">
            <img
              src="img/orang sangar.jpg"
              alt="Foto Saya"
              class="img-fluid img-circle shadow-lg"
            />
          </div>

          <div class="col-md-8">
            <h3>Afnan Dika Ramadhan</h3>
            <p class="lead text-muted">
              Mahasiswa Universitas Pelita Bangsa | IT Support | Web Dev
            </p>
            <p>
              Saya adalah seorang mahasiswa yang sedang bersemangat mempelajari
              IT Support. Saat ini, saya aktif membangun pemahaman tentang
              manajemen sistem, dasar-dasar jaringan, dan prosedur resolusi
              masalah teknis. Saya bersemangat untuk mengaplikasikan ilmu yang
              diperoleh dan siap menghadapi tantangan awal di lapangan.Contohnya
              ialah setting Mikrotik,Crimping Kabel,Cisco
            </p>
          </div>
        </div>
      </div>
    </section>

    <hr class="my-5" />

    <section id="portofolio" class="py-5 bg-light">
      <div class="container">
        <h2 class="text-center mb-5">Portofolio Proyek Saya</h2>

        <div class="row">
          <div class="col-md-4 mb-4">
            <div class="card h-100 shadow">
              <img src="img/Projek 1.png" class="card-img-top" alt="Proyek 1" />
              <div class="card-body">
                <h5 class="card-title">UI Lunakin</h5>
                <p class="card-text">
                  Pada projek ini saya baru memulai pada perancangan UI nya
                  untuk menyusun letak pada projek ini saya menambahkan
                  splash,logo,menu,opsi payment dan selanjutnya akan melakukan
                  implementasi ke "Android Studio"
                </p>
                <a href="#" class="btn btn-outline-primary">Lihat Proyek</a>
              </div>
            </div>
          </div>

          <div class="col-md-4 mb-4">
            <div class="card h-100 shadow">
              <img src="img/Projek 2.png" class="card-img-top" alt="Proyek 2" />
              <div class="card-body">
                <h5 class="card-title">Sistem Informasi Akademik</h5>
                <p class="card-text">
                  Pada projek ini saya membuat input dan melihat tabel mahasiswa
                  dan dosen menggunakan Xampp projek tersebut bernama sistem
                  informasi akademik
                </p>
                <a href="#" class="btn btn-outline-primary">Lihat Proyek</a>
              </div>
            </div>
          </div>

          <div class="col-md-4 mb-4">
            <div class="card h-100 shadow">
              <img
                src="img/Cuplikan layar 2025-10-29 102315.png"
                class="card-img-top"
                alt="Proyek 3"
              />
              <div class="card-body">
                <h5 class="card-title">HTML and CSS</h5>
                <p class="card-text">
                  Di projek ini saya mengerjakan tugas Pratikum yang dimana
                  disini mendapat banyak pelajaran dan pengetahuan terkait HTML
                  dan CSS
                </p>
                <a href="#" class="btn btn-outline-primary">Lihat Proyek</a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <footer class="bg-dark text-white text-center py-3 mt-5">
      <div class="container">
        <p class="mb-0">&copy; 2021 - Universitas Pelita Bangsa</p>
      </div>
    </footer>

    <script
      src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"
      crossorigin="anonymous"
    ></script>
  </body>
</html>

```

![foto](https://github.com/nanafnan09/Lab6Web/blob/41157ad6e6ac4c4adc4521b9ac429025cec8937e/LAB6%20image/Tampilan3.png)

`portofolio.html` adalah halaman Portofolio atau About (Tentang). Tujuan utamanya adalah menampilkan informasi pribadi (Tentang Saya) dan contoh-contoh proyek (Portofolio Proyek Saya). Halaman ini menggunakan komponen navigasi, tata letak responsif, dan komponen Card dari Bootstrap untuk menyajikan informasi dengan rapi dan profesional.



