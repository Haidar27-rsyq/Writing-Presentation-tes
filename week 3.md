## JavaScript Object
Apa itu Object
Dalam kehidupan nyata, kita sebenarnya sudah sering menjumpai object. Entah itu benda mati atau benda hidup. Semuanya adalah object. Properti adalah data lengkap dari sebuah object. Method adalah action dari sebuah object. Apa saja yang dapat dilakukan dari suatu object.
Tipe data yang sudah kita pelajari:

- number
- string
- boolean
- null
- undefined
- array
- object

> Membuat sebuah object
Sama seperti tipe data sebelumnya. Object dapat diassign kedalam sebuah variabel. Sama seperti array, didalam object kita dapat menyimpan properti dengan tipe data apapun.

Mengakses Object dan Property Object
- Bracket Notation
Kita juga bisa menggunakan bracket notation saat memanggil properti dari sebuah object.

Update Object
Kita dapat melakukan update pada variabel dengan tipe data Object.
>Do’s
- Object dapat mengupdate value dari key yang sudah tersedia
- Object dapat menambahkan key dan value baru
>Dont’s
- Jika menggunakan constant pada variable object. Kita tidak bisa mengganti seluruh data object dengan object yang baru.

Delete Object Property
Kita dapat menghapus properti dari object menggunakan delete operator.
> Method
Jika value yang kita masukkan pada property berupa function.
Maka itu disebut method.
Kamu pasti terbiasa menggunakan console.log() bukan?
Atau menggunakan Math.floor() ?
Nah console adalah global javascript object.
log() adalah property yang berupa function dari object console.
Sehingga kita memanggila dengan cara console.log().
Kita bisa membuat method custom untuk kita gunakan pada aplikasi kita loh.
Kita akan membuat method untuk greeting pada aplikasi ecommerce misalnya.

Nested Object
Pada real application nanti kalian pasti menemukan data object yang kompleks.
Object yang berasal dari turunan object lainnya.

Pass by reference
Kita bisa mengubah data yang ada pada object melalui sebuah function dan memasukkan object sebagai parameter function.
Ini biasa disebut passed by reference.

Looping Object
Jika kita ingin menampilkan seluruh object properti. Kita bisa menggunakan looping.
Jadi tidak perlu mengakses secara manual memanggil setiap propertinya.

Array of Object
Apakah object hanya menyimpan 1 data?
Tidak. 
Object sama seperti Array yang bisa menyimpan banyak data.
Kita dapat menggunakan array of object untuk data yang lebih dari satu.

## Javascript - Recursive
Recursive adalah function yang memanggil dirinya sendiri sampai kondisi tertentu. Recursive kebanyakan digunakan untuk case matematika, fisika, kimia, dan yang berhubungan dengan calculation.

A New Paradigm:

- procedural
- conditional
- looping
- modular (function)
- recursive

Ciri dari rekursif:

- Fungsi rekursif selalu memiliki kondisi yang menyatakan kapan fungsi tersebut berhenti. Kondisi ini harus dapat dibuktikan akan tercapai, karena jika tidak tercapai maka kita tidak dapat membuktikan bahwa fungsi akan berhenti, yang berarti algoritma kita tidak benar.
- Fungsi rekursif selalu memanggil dirinya sendiri sambil mengurangi atau memecahkan data masukan setiap panggilannya. Hal ini penting diingat, karena tujuan utama dari rekursif ialah memecahkan masalah dengan mengurangi masalah tersebut menjadi masalah-masalah kecil.

## Javascript - Asynchronous
Javascript adalah bahasa pemrograman single-thread yang artinya hanya dapat mengeksekusi satu task pada satu waktu atau biasa disebut synchronous.
Pada konsep pemrograman (web development pada case kita) dikenal istilah Asynchronous. Asynchronous mengizinkan komputer memproses task yang lain sambil menunggu proses yang masih berlangsung.
Kita bisa membuat asynchronous secara simulasi artinya tidak murni asynchronous dengan beberapa cara:

1. Callback
2. Promises
3. Async/Await

Callback
Callback function adalah function yang kita letakan di dalam argumen/parameter pada function, dan function tersebut akan dieksekusi setelah function pertama menyelesaikan tugasnya.
Proses asynchronous identik dengan delay, dimana hasil dari proses tersebut membutuhkan selang waktu tertentu untuk menghasilkan output. 
Kita akan menemukan proses asynchronous pada proses Ajax, komunikasi HTTP, Operasi file, timer, dsb
setTimeout digunakan untuk simulasi asynchronous. Karena sebenarnya kita tidak bisa membuat proses asynchronous murni.

Promises
a Promise is an object that may produce a single value some time in the future: either a reloved value, or a reason that it's not resolved. -Eric Elliot.
Promise adalah salah satu fitur baru di ES6, biasa digunakan untuk melakukan http request/fetch data dari API.
Dalam pengambilan data, promise memiliki 3 kemungkinan state.
1. Pending(sedang dalam proses)
2. Fulfilled (berhasil)
3. Rejected (gagal)

Async-Await
Async - await adalah salah satu fitur baru dari javascript yang digunakan untuk menangani hasil dari sebuah Promise. Sedangkan await berfungsi untuk menunda sebuah kode dijalankan sampai proses asynchronous berhasil.

HTTP Request fetch()
Fetch adalah native web API untuk melakukan HTTP calls dari external network.


