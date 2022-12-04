# WRITING WEEK 2
## Javascript - Scope
Scope adalah konsep dalam flow data variabel. 
Menentukan suatu variabel bisa diakses pada scope tertentu atau tidak.

- Blocks
Blocks adalah code yang berada didalam curly braces {}.
Conditional, function, dan  looping menggunakan blocks.
- Global Scope
Global scope berarti variabel yang kita buat dapat diakses dimanapun dalam suatu file.
Agar menjadi Global Scope, suatu variabel harus dideklarasikan diluar Blocks
- Local Scope
Local scope berarti kita mendeklarasikan variabel didalam blocks seperti function, conditional, dan looping.
Maka variabel hanya bisa diakses didalam blocks saja. Tidak bisa diakses diluar blocks.

## JAVASCRIPT - FUNCTION
Apa itu Function?
Function adalah sebuah blok kode dalam sebuah grup untuk menyelesaikan 1 task/1 fitur.
Saat kita membutuhkan fitur tersebut nantinya, kita bisa kembali menggunakannya.
- Membuat Function
- Memanggil Function
- Parameter dan Argumen
Parameter Function
-- Dengan parameter, function dapat menerima sebuah inputan data dan menggunakannya untuk melakukan task/tugas.
-- Saat membuat function/fitur, kita harus tahu data-data yang dibutuhkan. Misalnya saat membuat function penambahan 2 buah nilai. Data yang dibutuhkan adalah 2 buah nilai tersebut.
Argumen Function
-- Argumen adalah nilai yang digunakan saat memanggil function.
-- Jumlah argumen harus sama dengan jumlah parameternya
-- Jadi jika di function penambahan ada 2 parameter nilai saat membuat    function. Saat memanggil function kita gunakan 2 buah nilai argumen.
- Default Parameters
Default paramaters digunakan untuk memberikan nilai awal/default pada parameter function.
Default parameters bisa digunakan jika kita ingin menjaga function agar tidak error saat dipanggil tanpa argumen
- Function Helper
Kita bisa menggunakan function yang sudah dibuat pada function lain.
- Arrow Function
Arrow function adalah cara lain menuliskan function. Ini adalah fitur terbaru yang ada pada ES6 (Javascript Version)
- Short Syntax Function
- Exercise
Waktunya latihan dan mengerjakan project sederhana
- Exercise - Question
Question - Answer in markdown file (.md)
-- Kapan harus menggunakan function?
-- Apa bedanya parameter dan argumen?
-- Apa itu arrow function?
-- Apakah wajib menggunakan return pada function? Jelaskan alasannya
- Exercise - Project

## DATA TYPE BUILT IN PROTOTYPE
Built in adalah sebuah properti method yang digunakan menyelesaikan sebuah nilai

let hewan = 'HaRimau';
console.log( typeof hewan);
console.log(hewan.length);
console.log(hewan.toLocaleUpperCase);
console.log(hewan.charAt(2));


let nomor = 1234;
console.log(isNaN(nomor));
console.log(nomor.toString());

console.log(Math.PI);

let pi = 3.1445654
console.log(pi.toFixed(2))

## JavaScript dan HTML DOM
Proses rendering di balik layar
- HTML -> Parsing -> Tokens -> DOM
- CSS -> Parsing -> Tokens -> CSSOM
- DOM + CSSOM = Render Tree
- Layouting

Isu terkait proses rendering
-- Jika saat proses parsing HTML, ditemukan tag <script>, secara default proses parsing akan dihentikan sampai script tersebut selesai diunduh dan dijalankan

Solusi dari isu terkait proses rendering
- Taruh tag <script> eksternal sebelum tag penutup </body> - ini solusi paling umum agar dia mulai diproses setelah parsing HTML selesai.
- Taruh tag <script> sedini mungkin dan gunakan atribut async - atribut async akan membuat script tersebut diunduh tanpa menghentikan proses parsing dan dieksekusi seselesainya ia diunduh.
- Untuk script yang bergantung pada DOM, taruh tag <script> sedini mungkin, dan gunakan atribut defer - atribut defer akan membuat script tersebut diunduh tanpa menghentikan proses parsing dan dieksekusi seselesainya proses parsing selesai.

Memanipulasi Element HTML
Kalian kan mempelajari caranya
1. Mencari Element HTML
2. Mengubah Konten Element
3. Mengubah Atribut Element
4. Membuat Element

Mengubah Konten Element
- Element.textContent
- Element.innerHTML

Menangkap Interaksi User
- Element.addEventListener(“event”)
- Element.onevent

EventListener
- Dengan cara Element.addEventListener(“event”)
  - Bisa dihilangkan
  - Bisa ada beberapa event listener yang sama untuk 1 element
  - Memiliki argument tambahan { options }

EventListener - Click
Misalkan kita mempunyai element <input id=”user-input” />  dan <button id=”alert-button”>show</button>. 
Kita ingin menampilkan pop up box yang berisi teks di dalam input tadi.

    // cari dulu kedua element tersebut berdasarkan id-nya
    const input = document.getElementById(“user-input”)
    const button = document.getElementById(“alert-button”)
    // baru tambahkan event listener
    button.addEventListener(“click”, function() {
	alert(input.value)
    })
    // atau
    button.onclick = function() { alert(input.value) }

EventListener - Blur
“Blur”, lawan dari “focus”, adalah event di mana sebuah element kehilangan fokus dari user (misal user klk mouse di luar element tersebut atau user klik tab untuk berpindah element)
Misalkan kita ingin memvalidasi isi dari <input id=”username” /> agar panjangnya minimal 6 karakter..

    // cari dulu element tersebut berdasarkan id-nya
    const input = document.getElementById(“username”)
    // tambahkan event listener
    input.addEventListener(“blur”, () => {
	if(input.value.length < 6) alert(“Panjang username minimal 6”)
    })

EventListener - Form Submission
Misalkan kita mempunyai element beberapa input dalam sebuah form <input name=”email /> dan <input type=”password” name=”password” />. Bagaimana caranya  kita mendapatkan isi dari kedua input tersebut saat submit form?
Ada 2 cara:
- Pasang event listener di kedua input dan tombol submit, lalu saat tombol diklik, baca value dari kedua input tersebut. 
- Pasang event listener di form, lalu gunakan FormData untuk mengambil data dari masing-masing input

Pasang event listener di form, lalu gunakan FormData untuk mengambil data dari masing-masing input

    const form = document.getElementById(“form”)
    form.addEventListener(“submit”, function(event) {
	 // cegah page refresh
	event.preventDefault()
	const formData = new FormData(form)
	const values = Object.fromEntries(formData) // { email: ... }
    })

## JavaScript - Array
Apa itu Array?
Array adalah tipe data list order yang dapat menyimpan tipe data apapun di dalamnya.
Array dapat menyimpan tipe data String, Number, Boolean, dan lainnya.

Membuat Array
Array didefinisikan menggunakan square brackets

Mengakses/Memanggil Array
Array pada javascript dihitung dari index data ke-0.
Data pertama adalah index ke-0.

Update Array
Seperti tipe data dan variabel pada umumnya, kita dapat mengupdate data pada Array

Const in Array
- Jika menggunakan let, kita dapat mengubah array  dengan array baru dan konten nilai yang ada di dalam array dengan nilai lain
- Const tidak bisa melakukan update data. Namun pada Array kita dapat melakukan update konten nilai di dalam array (mutable).
- Yang tidak bisa adalah mengubah array dengan array yang baru jika menggunakan const

Array Properties
Array memiliki 5 properti yang sering digunakan yaitu constructor, length, index, input, dan prototype.
Kita hanya membahas length. Untuk yang lainnya kamu bisa cek di link ini [array properties and method][df1]
Properties adalah fitur yang sudah disediakan oleh Javascript untuk memudahkan developer.

Array Method
Array memiliki method atau biasa disebut built-in methods.
Artinya Javascript sudah memudahkan kita dengan menyediakan function/method umum yang bisa kita gunakan.
Kita tidak perlu membuat function lagi jika method yang kita butuhkan sudah tersedia.
Sama halnya dengan Array properti. Kita bisa cek dokumentasi untuk melihat method yang sudah tersedia pada link ini [built-in methods][df1] atau [MDN documentation][df1]





[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Dillinger is a cloud-enabled, mobile-ready, offline-storage compatible,
AngularJS-powered HTML5 Markdown editor.

- Type some Markdown on the left
- See HTML in the right
- ✨Magic ✨

## Features

- Import a HTML file and watch it magically convert to Markdown
- Drag and drop images (requires your Dropbox account be linked)
- Import and save files from GitHub, Dropbox, Google Drive and One Drive
- Drag and drop markdown and HTML files into Dillinger
- Export documents as Markdown, HTML and PDF

Markdown is a lightweight markup language based on the formatting conventions
that people naturally use in email.
As [John Gruber] writes on the [Markdown site][df1]

> The overriding design goal for Markdown's
> formatting syntax is to make it as readable
> as possible. The idea is that a
> Markdown-formatted document should be
> publishable as-is, as plain text, without
> looking like it's been marked up with tags
> or formatting instructions.

This text you see here is *actually- written in Markdown! To get a feel
for Markdown's syntax, type some text into the left window and
watch the results in the right.

## Tech

Dillinger uses a number of open source projects to work properly:

- [AngularJS] - HTML enhanced for web apps!
- [Ace Editor] - awesome web-based text editor
- [markdown-it] - Markdown parser done right. Fast and easy to extend.
- [Twitter Bootstrap] - great UI boilerplate for modern web apps
- [node.js] - evented I/O for the backend
- [Express] - fast node.js network app framework [@tjholowaychuk]
- [Gulp] - the streaming build system
- [Breakdance](https://breakdance.github.io/breakdance/) - HTML
to Markdown converter
- [jQuery] - duh

And of course Dillinger itself is open source with a [public repository][dill]
 on GitHub.

## Installation

Dillinger requires [Node.js](https://nodejs.org/) v10+ to run.

Install the dependencies and devDependencies and start the server.

```sh
cd dillinger
npm i
node app
```

For production environments...

```sh
npm install --production
NODE_ENV=production node app
```

## Plugins

Dillinger is currently extended with the following plugins.
Instructions on how to use them in your own application are linked below.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |

## Development

Want to contribute? Great!

Dillinger uses Gulp + Webpack for fast developing.
Make a change in your file and instantaneously see your updates!

Open your favorite Terminal and run these commands.

First Tab:

```sh
node app
```

Second Tab:

```sh
gulp watch
```

(optional) Third:

```sh
karma test
```

#### Building for source

For production release:

```sh
gulp build --prod
```

Generating pre-built zip archives for distribution:

```sh
gulp build dist --prod
```

## Docker

Dillinger is very easy to install and deploy in a Docker container.

By default, the Docker will expose port 8080, so change this within the
Dockerfile if necessary. When ready, simply use the Dockerfile to
build the image.

```sh
cd dillinger
docker build -t <youruser>/dillinger:${package.json.version} .
```

This will create the dillinger image and pull in the necessary dependencies.
Be sure to swap out `${package.json.version}` with the actual
version of Dillinger.

Once done, run the Docker image and map the port to whatever you wish on
your host. In this example, we simply map port 8000 of the host to
port 8080 of the Docker (or whatever port was exposed in the Dockerfile):

```sh
docker run -d -p 8000:8080 --restart=always --cap-add=SYS_ADMIN --name=dillinger <youruser>/dillinger:${package.json.version}
```

> Note: `--capt-add=SYS-ADMIN` is required for PDF rendering.

Verify the deployment by navigating to your server address in
your preferred browser.

```sh
127.0.0.1:8000
```

## License

MIT

**Free Software, Hell Yeah!**

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [dill]: <https://github.com/joemccann/dillinger>
   [git-repo-url]: <https://github.com/joemccann/dillinger.git>
   [john gruber]: <http://daringfireball.net>
   [df1]: <http://daringfireball.net/projects/markdown/>
   [markdown-it]: <https://github.com/markdown-it/markdown-it>
   [Ace Editor]: <http://ace.ajax.org>
   [node.js]: <http://nodejs.org>
   [Twitter Bootstrap]: <http://twitter.github.com/bootstrap/>
   [jQuery]: <http://jquery.com>
   [@tjholowaychuk]: <http://twitter.com/tjholowaychuk>
   [express]: <http://expressjs.com>
   [AngularJS]: <http://angularjs.org>
   [Gulp]: <http://gulpjs.com>

   [PlDb]: <https://github.com/joemccann/dillinger/tree/master/plugins/dropbox/README.md>
   [PlGh]: <https://github.com/joemccann/dillinger/tree/master/plugins/github/README.md>
   [PlGd]: <https://github.com/joemccann/dillinger/tree/master/plugins/googledrive/README.md>
   [PlOd]: <https://github.com/joemccann/dillinger/tree/master/plugins/onedrive/README.md>
   [PlMe]: <https://github.com/joemccann/dillinger/tree/master/plugins/medium/README.md>
   [PlGa]: <https://github.com/RahulHP/dillinger/blob/master/plugins/googleanalytics/README.md>
