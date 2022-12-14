Responsive Web Design
Apa itu Responsive web design?
Responsive Web Design (RWD) adalah bertujuan membuat desain website kita dapat diakses dalam device apapun.
Device yang umumnya digunakan adalah laptop/PC, smartphone, dan tablet.
Setting up Chrome Dev Tools
Setiap developer website wajib menggunakan tools bawaan dari setiap browser yang memudahkan proses development website.
Pada browser chrome biasa disebut dengan Chrome Dev Tools
Akses Chrome Dev Tools
Jika sudah membuka browser Chrome, kita bisa menggunakan shortcut ini:
windows: ctrl + shift + j
Add Viewport in HTML
Meta Viewport required on mobile responsive
<meta name="viewport" content="width=device-width, initial-scale=1.0">
Use Max-width element
Panjang Image menjadi overflow karena mengikuti width real bawaan dari file image.
Add styling max-width
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Web Design</title>
</head>
<body>
  <img style="max-width: 100%;" src="images/nature.jpg" alt="image">
</body>
</html>
Media Query
Media Query digunakan untuk membuat beberapa styles tergantung pada jenis device.
Jenis media query
Media query untuk responsive web design umumnya hanya menggunakan 2 jenis media query.
Keduanya yaitu min-width dan max-width
Setting up media query
@media screen and (min-width: your pixel) {
  /* your tag element html and your css*/
}

@media screen and (max-width: your pixel) {
  /* your tag element html and your css*/
}
Ada 2 cara/pattern dalam menggunakan media query
Cara ke-1: Membuat file css berbeda untuk masing-masing device
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Web Design</title>

  <link rel="stylesheet" href="styles/main.css">

  <link rel="stylesheet" media="screen and (max-width: 500px)" href="styles/main.mobile.css">
</head>
<body>
  <h2>Responsive Web Design (RWD)</h2>
</body>
</html>
Cara ke-2: kita menggabungkan 1 file CSS untuk setting styling berbagai device
body {
  background-color: white;
}

@media screen and (max-width: 500px) {
  body {
    background-color: aquamarine;
  }
}
Breakpoint
Perubahan yang terjadi pada tampilan saat berganti device atau ukuran width disebut breakpoint.
Complex Breakpoint Media Query
Menggunakan range media query min and max
body {
  background-color: white;
}

@media screen and (min-width: 500px) and (max-width: 700px) {
  body {
    background-color: aquamarine;
  }
}
Important Notes
Tidak ada aturan baku besaran width dan berapa banyak breakpoint yang harus dilakukan.
Responsive web design dilakukan sesuai kebutuhan konten kita. jika konten yang ditampilkan sudah tidak bisa diakses atau sulit dilihat pada width tertentu. sudah saatnya menggunakan media query.
Bootstrap
Apa itu Bootstrap?
Bootstrap adalah framework web development berbasis HTML, CSS, dan JavaScript yang dirancang untuk mempercepat proses pengembangan web responsive dan mobile-first (memprioritaskan perangkat seluler).
Mengapa menggunakan Bootstrap
Tujuan dan fungsi Bootstrap adalah untuk membuat website responsive dan mobile-first. Jadi, semua elemen antarmuka website dipastikan bisa bekerja secara optimal di semua ukuran layar, baik desktop maupun perangkat seluler.
Kapan kita menggunakan bootstrap?
Boostrap digunakan ketika membuat website sederhana dan tidak memerlukan load lama
Layout pada Bootstrap
Breakpoint adalah ukuran lebar yang menentukan tampilan responsif terhadap ukuran viewport perangkat tertentu.
Dalam bootstrap terdapat beberapa breakpoint, yaitu:
sm
md
lg
xl
xxl
Container adalah elemen paling dasar dalam layout bootstrap.
Terdapat 3 macam container dalam bootstrap, yaitu:
Default Container: Class container memiliki sifat yang responsive dan fixed-width, yang berarti lebarnya akan berubah pada setiap breakpoint.
<div class="container">
  <!-- Content here -->
</div>
Fluid Container: Class container-fluid memiliki lebar yang sama dengan viewport
<div class="container-fluid">

  <!-- Content here -->
</div>
Responsive Container: Responsive container, diurutkan dari breakpoint terkecil, terdiri dari:
.container-sm
.container-md
.container-lg
.container-xl
.container-xxl
<div class="container-sm">100% wide until small breakpoint</div>
<div class="container-md">100% wide until medium breakpoint</div>
<div class="container-lg">100% wide until large breakpoint</div>
<div class="container-xl">100% wide until extra large breakpoint</div>
<div class="container-xxl">100% wide until extra extra large breakpoint</div>
Grid biasanya digunakan bersama dengan container.
Contoh kodenya sebagai berikut:
<div class="container">
  <div class="row">
    <div class="col">
      Column
    </div>
    <div class="col">
      Column
    </div>
    <div class="col">
      Column
    </div>
  </div>
</div>
Class row berfungsi untuk mengubah sifat dari div di dalamnya yang semula akan ditampilkan secara block, akan dapat ditampilkan secara inline.

Class col berfungsi untuk mengubah div tersebut menjadi responsif terhadap lebar viewport.

Gutters berfungsi untuk memberikan jarak antar item di dalamnya.

Contohnya sebagai berikut:

<div class="container">
  <div class="row g-2">
    <div class="col-6">
      <div class="p-3 border bg-light">Custom column padding</div>
    </div>
    <div class="col-6">
      <div class="p-3 border bg-light">Custom column padding</div>
    </div>
    <div class="col-6">
      <div class="p-3 border bg-light">Custom column padding</div>
    </div>
    <div class="col-6">
      <div class="p-3 border bg-light">Custom column padding</div>
    </div>
  </div>
</div>
Component pada Bootstrap
Ada banyak komponen yang disediakan oleh Bootstrap 5, seperti:
Breadcrumb
Card
Navbar
Modal
Collapse
Alerts
Pagination
Buttons
Carousel
Dropdowns
Badge