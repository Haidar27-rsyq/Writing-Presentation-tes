# Writing and Presentation Test
## 1.Command Line Interface

- Shell merupakan program yang digunakan untuk berkomunikasi atau memerintah sistem
- Command Line Interface (CLI) ialah Command Line Interface, jenis shell yang berbasis teks
- Terminal Emulator yaitu aplikasi untuk mengakses CLI

  ## A. FileSystem
  - Sebuah filesystem mengatur bagaimana data disimpan di dalam sebuah system
  - Sistem operasi Windows & Unix-like menyusun file dan direktori menggunakan struktur yang bentuknya mirip tree

  ## B. Command Untuk Navigasi
  - Pwd (Print working directory) Command untuk melihat current working directory.
  - Is (lists) Command untuk melihat isi file yang ada di sebuah direktori.
  - cd <direktori> (change directory) Command untuk berpindah direktori.

  ## C. Membuat Files & Direktori
  - touch Command untuk membuat sebuah file
  - mkdir Command untuk membuat sebuah direktori

  ## D. Melihat isi files
  - head Command untuk melihat beberapa line awal dari sebuah file text
  - tail Command untuk melihat beberapa line awal dari sebuah file text
  - cat Command untuk melihat isi sebuah file

  ## E. Menyalin, memindahkan, dan menghapus files & directory
  - cp (cp) Command untuk mengcopy files atau directory
  - mv (move) Command untuk memindahkan files atau directory. Bisa digunakan untuk rename.
  - rm (remove) Command untuk menghapus file atau directory

## 2. Git & GitHub Dasar
- Git adalah Tools untuk Programer
- Git sebagai Version Control System
 Tugasnya adalah mencatat setiap perubahan pada File (termasuk code yang kita buat) pada suatu proyek baik dikerjakan secara individu maupun tim.
- Git adalah aplikasi yang dapat melacak setiap perubahan yang terjadi pada suatu folder atau file.
- Git biasanya digunakan oleh para programmer sebagai tempat penyimpanan file pemrograman mereka, karena lebih efektif.
File -file yg disimpan menggunakan git akan terlacak seluruh perubahannya, termasuk siapa yang mengubah.

## A. Instalasi Git
    #Setup Awal
    git config --global user.name "Radar Tegal"
    git config --global user.email berita@radartegal.com
    git config --list
## B. Repository GIT
Repository adalah direktori proyek yang kita buat.
1 Repo =  1 Proyek = 1 Direktori

    #Membuat Repository
    git init proyek-01

Command line tadi akan membuat sebuah direktori baru
Bagaimana jika folder sudah ada sebelumnya?

Calm down, kamu bisa gunakan  ini:

    #git init .

- Git Status digunakan untuk mengetahui sebuah status dari repository lokal.
- Git add digunakan untuk menambahkan file baru di repository yang dipilih.
- Git commit -m "commit pertama "digunakan untuk menyimpan perubahan yang sudah dilakukan, namun tidak ada perubahan yang terjadi pada remote repository.
-Git branch -m [nama branch] digunakan untuk menambahkan fitur baru atau memperbaiki bug.
-Git remote digunakan untuk petunjuk ke versi repositori yang biasanya disimpan di server lain.
-Git push -u origin main digunakan untuk mengirimkan perubahan file yang dilakukan setelah di commit ke remote repository.
-Git clone digunakan untuk membuat salinan repository lokal.

## 3. HTML
- HTML atau Hyoertext Markup Language digunakan untuk menampilkan konten pada browser.
- Tools yang dibutuhkan untuk membuat HTML yaitu Browser dan Code Editor.
- Visual Studio Code adalah code editor yang dikembangkan oleh tim Engineer Microsoft.
- Keunggulan Visual Studio Code dapat digunakan di Windows, Mac, dan juga Linux.
- HTML Structure

      # <!DOCTYPE html>
        <html lang="en"
        <head>
           <meta charset="UTF-8">
           <meta name="viewport" content="width=device-width, initial-scale=1.0">
           <title>Document</title>
        </title>
        <body>
          This is my very first page writing with HTML
        </body>
        </html>

     # Tag Wajib
       <!DOCTYPE html> yaitu tag untuk deklarasi type dokumen.
       <html> yaitu tag utama dalam HTML.
       <head> yaitu tag untuk bagian kepala dari dokumen.
       <title> yaitu tag untuk judul web
       <body> yaitu tag bagian body dari dokumen.

     # HTML Element terdiri opening tag dan closing tag
      opening tag: <p>
      content: Hello World
      closing tag: </p>

## 4. CSS
- CSS atau Cascading Style Sheet adalah bahasa yang digunakan untuk mendesain halaman website.
- Struktur CSS

      .elementHTML {
      property : value
      }
- CSS Comment yaitu memberikan keterangan maksud dari line code yang dikerjakan /* */.
- Ada 3 cara menyisipkan CSS ke dalam HTML.
 Inline styles adalah kita menambahkan CSS pada attribute element HTML

       <p style="color: coral; font-size: 36px;">This is paragraph using inline styles</p>

   Internal CSS adalah kode CSS yang ditulis dalam tag<style> dan kode HTML yang ditulis di bagian header file HTML.

      <style></style>

- Sintaks CSS terdiri dari tiga bagian: pemilih atau selektor (selector), sifat atau properti (property), dan nilai (value).
- Contoh sintaks dasar dari CSS:

      h1 {
      color: red;
      }
- Ada beberapa cara yang bisa digunakan sesuai kebutuhan untuk mendesain element HTML di CSS.
- Tag Name: Selektor ini akan memilih elemen berdasarkan nama tag.

      p {
       color: blue;
      }

- Tag Class: selektor yang memilih elemen berdasarkan nama class yang diberikan.

      .pink {
       color: white;
       background: pink;
       padding: 5px;
      }

- Tag ID: Selektor ID hampir sama dengan class. Bedanya, ID bersifat unik. Hanya boleh digunakan oleh satu elemen saja.

      #header {
         background: teal;
         color: white;
         height: 100px;
         padding: 50px;
      }

- !important CSS: jika pada styling CSS menggunakan !important, maka styling sebelumnya baik itu ID Name atau Class Name akan di override.

      h1.title {
         color: green;
      }

## 5. Algorithms and Data Structures
- Algoritma adalah deskripsi berupa step-step yang dibutuhkan untuk menyelesaikan suatu masalah.

- Struktur data adalah cara penyimpanan , pengorganisasian , dan pengaturan data di dalam media penyimpanan komputer sehingga data tersebut dapat digunakan secara efisien. Algoritma adalah sederetan langkah-langkah logis yang disusun secara sistematis untuk memecahkan suatu masalah.

  # Ciri-ciri Algoritma

  - Input: memiliki 0 atau lebih inputan.
  - Ouput: memiliki min 1 buah output
  - Definiteness: Instruksi jelas tidak ambigu
  - Finitess: Memiliki titik berhenti (stop)
  - Effectiveness: Sebisa mungkin tepat sasaran dan efisien

   # Penyajian Algoritma

  - Deskriptif
  - Flowchart
  - Pseudocode

  # Jenis flowchart

- Flowchart dokumen: untuk menelusuri alur form dari satu bagian ke bagian yang lain, termasuk bagaimana laporan diproses, dicatat, dan disimpan.
- Flowchart program: menggambarkan secara rinci prosedur dari proses program.
- Flowchart proses: cara penggambaran rekayasa industrial dengan cara merinci dan menganalisis langkah-langkah selanjutnya dalam suatu prosedur atau sistem.
- Flowchart sistem: flowchart yang menampilkan tahapan atau proses kerja yang sedang berlangsung di dalam sistem secara menyeluruh.
- Flowchart skematik: menampilkan alur prosedur suatu sistem, hampir sama dengan flowchart sistem.

  # Jenis-jenis Pseudocode
  - Procedural: cara berpikir secara runtun
  - Conditional: digunakan saat dibutuhkan percabangan kasus.
  - Looping: dapat melakukan sebuah proses yang sama berulang-ulang.
  - Recursive: pola pikir dalam algoritma yang memanggil method/function didalam sebuah function.

## 6. Java Scripts
- JavaScript adalah bahasa pemrograman yang sangat powerful yang digunakan untuk logic pada sebuah website.
- Cara menjalankan JavaScript yaitu melalui browser pada device setiap user.
- Pada JavaScript dikenal dengan istilah Syntax dan Statement.

  > Syntax adalah seperangkat aturan yang menentukan program JavaScript yang terstruktur dengan benar.
  > Statement adalah sebuah intruksi untuk dieksekusi oleh web browser.

  # Tipe Data (Data Types)
  - Tipe Data adalah jenis-jenis data yang bisa disimpan di dalam variabel.
  - Ada 6 Tipe data pada JavaScript:
  > -number: tipe data yang mengandung semua angka termasuk angka desimal.
    -string: grup karakter yang ada pada keyboard laptop/PC kita yaitu letters (huruf), number (angka), spaces (spasi), symbol, dan lainnya.
    -boolean: tipe data yang hanya mempunyai 2 buah nilai.
    -null: tipe data yang diartikan bahwa sebuah variable/data tidak memiliki nilai.
    -undefined: tipe data yang merepresentasikan varibel/data yang tidak memiliki nilai.
    -object: koleksi data yang saling berhubungan (related). Tipe data pbject dapat menyimpan data dengan tipe data apapun (number, string, boolean, dan lainnya).

  # Looping
 - Looping adalah statement yang mengulang sebuah instruksi hingga kondisi terpenuhi atau jika kondisi stop/berhenti tercapai.
 - Ada 4 macam looping yaitu:
   - Foor Loop
   - While Loop
   - Do While
   - Nested Loop
- For Loop merupakan instruksi pengulangan yang dapat kita berikan pada program yang kita kembangkan.
- Contoh Foor Loop

      let angka = 1;
      for (angka; angka <= 10; angka++) {
        console.log(angka);
      }

- While Loop akan menjalankan instruksi pengulangan kondisi bernilai TRUE.
- Contoh While Loop

      let angka = 1;
      while (angka <= 10) {
         console.log(angka);
         angka++;
      }
- Do While

      do {
         console.log("Nyalakan mesin!");
         bensin--;
     } while(bensin > 0)

- Nested Loop digunakan untuk membuat looping didalam looping.
- Contoh Nested Loop

      for (let i = 1; i <= 10; i++) {
      for (let j = 1; j <= i; j++) {
         document.write('<br />')
         document.write('Baris', +i);
         document.write('<br />')
         document.write('Kolom', +j);
        }
      }






