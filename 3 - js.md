# PERTEMUAN 3 - JAVASCRIPT

---

Materi __Sunday Code Camp 2022__ pertemuan III

## 1. Pengenalan Javascript

Javascript adalah bahasa pemrograman yang digunakan untuk membuat website dinamis. Javascript dapat berjalan di browser, server, dan perangkat mobile. Javascript dapat digunakan untuk membuat aplikasi web, aplikasi desktop, aplikasi mobile, dan aplikasi server. Versi terbaru adalah ES6. ES6 merupakan singkatan dari ECMAScript 6. ECMAScript adalah standar javascript. Versi ES6 merupakan versi javascript yang paling banyak digunakan saat ini. Versi ES6 memiliki banyak fitur baru yang mempermudah pembuatan aplikasi. Fitur-fitur tersebut antara lain:

  * Arrow Function (=>)
  * Class (extends, super)
  * Template Literals (``)
  * Destructuring (Array, Object)
  * Spread Operator (...)
  * Rest Parameter (...)
  * Default Parameter (a = 1)
  * Object Literal
  * Array Literal
  * Promise (then, catch, finally)
  * Async/Await (async, await)
  * Module (import, export)

Cara memasukkan javascript ke dalam halaman web adalah dengan menambahkan tag `<script>` di dalam tag `<head>` atau `<body>`. Tag `<script>` memiliki beberapa atribut, antara lain:

  * `src`: untuk menentukan lokasi file javascript
  * `type`: untuk menentukan tipe file javascript
  * `async`: untuk menentukan apakah file javascript dijalankan secara asynchronous atau tidak
  * `defer`: untuk menentukan apakah file javascript dijalankan setelah halaman web selesai di-load atau tidak

  Untuk memasukkan javascript dengan ES6, gunakan atribut `type="module"`.

  Contohnya:

  ```html
  <script src="script.js" type="text/javascript" async defer></script>

  <script src="script.js" type="module"></script>
  ```

## 2. Variabel

Untuk mendeklarasikan variabel dapat menggunakan kata kunci:

- ~~`var`~~: variabel yang dideklarasikan dengan kata kunci `var` dapat diakses di dalam fungsi atau di dalam blok kode. Variabel yang dideklarasikan dengan kata kunci `var` dapat diubah nilainya.

- `let`: variabel yang dideklarasikan dengan kata kunci `let` hanya dapat diakses di dalam blok kode. Variabel yang dideklarasikan dengan kata kunci `let` dapat diubah nilainya.

- `const`: variabel yang dideklarasikan dengan kata kunci `const` hanya dapat diakses di dalam blok kode. Variabel yang dideklarasikan dengan kata kunci `const` tidak dapat diubah nilainya.

  Contoh:

```javascript
// Deklarasi variabel dengan let
let a = 1;
let b = 2;

// Deklarasi variabel dengan const
const a = 1;
const b = 2;
b = 3; // Error
```

## 3. Debugging, Error Handling, dan Console

Debugging adalah proses mencari dan memperbaiki kesalahan dalam kode program. Untuk melakukan debugging, gunakan console.log() untuk mencetak nilai dari variabel. Nilai dari variabel dapat dilihat di console browser.

### 3.1 Error Handling

Error handling adalah proses menangani kesalahan yang terjadi pada kode program. Error handling dapat dilakukan dengan menggunakan try-catch-finally.

  * `try`: blok kode yang akan dieksekusi
  * `catch`: blok kode yang akan dieksekusi jika terjadi kesalahan pada blok kode try
  * `finally`: blok kode yang akan dieksekusi setelah blok kode try dan catch dieksekusi

  Contoh:

```javascript
try {
  // Blok kode yang akan dieksekusi
} catch (error) {
  // Blok kode yang akan dieksekusi jika terjadi kesalahan pada blok kode try
} finally {
  // Blok kode yang akan dieksekusi setelah blok kode try dan catch dieksekusi
}
```

### 3.2 Console

Console adalah tempat untuk mencetak nilai dari variabel. Console dapat diakses dengan menekan tombol F12 pada keyboard. Beberapa fungsi yang dapat digunakan di console antara lain:

  * `console.log()`: untuk mencetak nilai dari variabel
  * `console.error()`: untuk mencetak nilai dari variabel dengan warna merah
  * `console.warn()`: untuk mencetak nilai dari variabel dengan warna kuning
  * `console.table()`: untuk mencetak nilai dari variabel dalam bentuk tabel
  * `console.time()`: untuk mencetak waktu eksekusi kode
  * `console.timeEnd()`: untuk mencetak waktu eksekusi kode

  Contoh:

```javascript
// Mencetak nilai dari variabel
console.log("Hello World");

// Mencetak nilai dari variabel dengan warna merah
console.error("Hello World");

// Mencetak nilai dari variabel dengan warna kuning
console.warn("Hello World");

// Mencetak nilai dari variabel dalam bentuk tabel
console.table(["Hello", "World"]);
```


## 4. Tipe Data

Tipe data adalah jenis data yang digunakan untuk menyimpan nilai. Tipe data yang ada di javascript antara lain:

  * `number`: untuk menyimpan angka
  * `string`: untuk menyimpan teks
  * `boolean`: untuk menyimpan nilai true atau false
  * `null`: untuk menyimpan nilai kosong
  * `undefined`: untuk menyimpan nilai yang belum didefinisikan
  * `object`: untuk menyimpan objek
  * `array`: untuk menyimpan kumpulan nilai
  * `function`: untuk menyimpan fungsi

## 5. String

### 5.1 Template Literal

Template literal adalah string yang dapat menyimpan nilai dari variabel. Template literal ditulis di dalam tanda petik (`). Nilai dari variabel ditulis di dalam tanda kurung kurawal ({}). Selain variabel, template literal juga dapat menyimpan ekspresi.

  Contoh:

```javascript
// Deklarasi variabel
const name = "John Doe";
const age = 20;

// Deklarasi template literal
const str = `Nama saya ${name}, umur saya ${age + 1} tahun.`;

// Mencetak nilai dari variabel
console.log(`Str: ${str}`);
```

## 6. Array, Object, dan Function

Array, object, dan function merupakan tipe data yang kompleks,

### 6.1 Object Literal

Object literal adalah tipe data yang digunakan untuk menyimpan kumpulan nilai. Nilai yang disimpan dalam object literal terdiri dari pasangan key dan value. Key digunakan untuk mengakses value. Key dan value dipisahkan dengan titik dua (:). Pasangan key dan value dipisahkan dengan koma (,). Object literal ditulis di dalam kurung kurawal ({}) atau di dalam kurung siku ([]).

Contoh:

```javascript
// Deklarasi object literal
const obj = {
  name: "John Doe",
  age: 20,
  address: "Jl. ABC No. 123",
  hobbies: ["Membaca", "Menulis", "Menggambar"],
  isMarried: false,
  sayHello: function () {
    console.log("Hello World!");
  },
};

// Mengakses value dari object literal
console.log(obj.name); // John Do
obj.sayHello(); // Hello World!
obj.age = 21; // Mengubah value dari key age
obj.email = 'admin@domain.com'; // Menambahkan key dan value baru
```

### 6.2 Array

Array literal adalah tipe data yang digunakan untuk menyimpan kumpulan nilai. Array literal ditulis di dalam kurung siku ([]).

Contoh:

```javascript
// Deklarasi array literal
const arr = ["Membaca", "Menulis", "Menggambar"];

// Mengakses value dari array literal
console.log(arr[0]); // Membaca
console.log(arr[1]); // Menulis
console.log(arr[2]); // Menggambar
```

Operasi yang dapat dilakukan pada array antara lain:

  * `push`: untuk menambahkan nilai ke akhir array
  * `pop`: untuk menghapus nilai dari akhir array
  * `unshift`: untuk menambahkan nilai ke awal array
  * `shift`: untuk menghapus nilai dari awal array
  * `splice`: untuk menghapus nilai dari array
  * `slice`: untuk mengambil nilai dari array

### 6.3 Function

Function adalah blok kode yang digunakan untuk melakukan suatu tugas. Function dapat menerima parameter dan mengembalikan nilai. Function dapat dipanggil kembali di dalam function tersebut. Di javascript, function dapat disimpan dalam variabel, array, dan object.

Contoh:

```javascript
// Deklarasi function
function sayHello() {
  console.log("Hello World!");
}

const sayHello = function () {
  console.log("Hello World!");
};

// Memanggil function
sayHello();
```

### 6.4 Callback Function

Callback function adalah function yang diberikan sebagai parameter ke function lain. Callback function akan dipanggil kembali di dalam function lain. Pada umumnya callback function digunakan untuk menangani event. Contoh:

```javascript
setTimeout(function () {
  console.log("Hello World!");
}, 1000);
```

Pada contoh di atas, function yang diberikan sebagai parameter ke function `setTimeout` adalah callback function. Function `setTimeout` akan memanggil kembali callback function setelah 1 detik.

### 6.5 Arrow Function

Arrow function adalah function yang ditulis dengan sintaks yang lebih singkat. Arrow function tidak memiliki keyword `function` dan keyword `return`. Arrow function dapat ditulis dalam satu baris jika tidak memiliki parameter dan hanya memiliki satu baris kode.

Contoh:

```javascript
// Deklarasi arrow function
const sayHello = () => {
  console.log("Hello World!");
};

const sayHello = () => console.log("Hello World!");

// Memanggil arrow function
sayHello();

// Deklarasi arrow function dengan parameter
const sayHello = (name) => {
  console.log(`Hello ${name}!`);
};
```


## 7. Module

Module adalah file yang berisi kode javascript. Module dapat digunakan untuk memecah kode menjadi beberapa file. Module dapat diimpor ke dalam file lainnya. Module dapat diimpor dengan menggunakan keyword `import` dan `export`. Di browser, module dapat diimpor dengan menggunakan tag `<script>` dengan atribut `type="module"`.

Contoh:

```javascript
// File 1
export const name = "John Doe";
export const age = 20;

// atau bisa juga ditulis seperti ini
const name = "John Doe";
const age = 20;
export { name, age };

// File 2
import { name, age } from "./file1.js";

console.log(name); // John Doe
console.log(age); // 20
```

Jika ingin mengimpor semua nilai dari module, gunakan keyword `*` sebagai nama variabel.

```javascript
// File 1
export const name = "John Doe";
export const age = 20;

// File 2
import * as data from "./file1.js";

console.log(data.name); // John Doe
```

Jika ingin mengimpor nilai default dari module, gunakan keyword `default` di depan nama variabel.

```javascript
// File 1
const name = "John Doe";
export default name;

// File 2
import name from "./file1.js";

console.log(name); // John Doe
```

## 8. Promise dan Async/Await

![Promise](https://miro.medium.com/proxy/0*sdGZT038FoVSLwf4.jpg)

Promise dan async/await merupakan fitur baru yang ditambahkan pada ES6. Promise dan async/await digunakan untuk mengatasi masalah callback hell. Promise dan async/await digunakan untuk menangani proses asynchronous. Promise terdiri dari 3 state, yaitu:

  * `pending`: proses belum selesai
  * `fulfilled`: proses selesai
  * `rejected`: proses gagal

Contoh pembuatan promise adalah sebagai berikut:

```javascript
const promise = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve("Hello World!");
  }, 2000);
});

promise.then((result) => {
  console.log(result);
})
.catch((error) => {
  console.log(error);
});
```

Untuk membuat promise, gunakan keyword `new` untuk membuat object baru. Object promise memiliki method `then` dan `catch`. Method `then` digunakan untuk menangani state `fulfilled` dan method `catch` digunakan untuk menangani state `rejected`. Then dan catch menerima satu parameter berupa fungsi callback. Fungsi callback menerima satu parameter berupa nilai yang dikirimkan oleh fungsi `resolve` atau `reject`.

Async/await merupakan sintaks yang digunakan untuk menulis kode secara synchronous. Async/await dapat digunakan untuk menangani proses asynchronous. Async/await dapat digunakan untuk menangani promise. Async/await dapat digunakan untuk menangani function yang mengembalikan promise.

Contoh penggunaan async/await adalah sebagai berikut:

```javascript
const promise = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve("Hello World!");
  }, 2000);
});

const callPromise = async () => {
  const result = await promise;
  console.log(result);
};

callPromise();
```

Untuk membuat function async, gunakan keyword `async` di depan nama function. Untuk menunggu proses promise, gunakan keyword `await` di depan nama promise. Fungsi async akan menunggu hingga promise selesai. Fungsi async akan mengembalikan nilai yang dikirimkan oleh fungsi `resolve` atau `reject`.

Pada async function, jika terdapat error, maka async function akan langsung berhenti dan mengembalikan nilai yang dikirimkan oleh fungsi `reject`. Untuk menangani error, gunakan keyword `try` dan `catch`. Contoh penggunaan try dan catch adalah sebagai berikut:

```javascript
const promise = new Promise((resolve, reject) => {
  setTimeout(() => {
    reject("Error!");
  }, 2000);
});

const callPromise = async () => {
  try {
    const result = await promise;
    console.log(result);
  } catch (error) {
    console.log(error);
  }
};

callPromise();
```

## 9. DOM

DOM adalah singkatan dari Document Object Model. DOM adalah API yang digunakan untuk mengakses dan memanipulasi elemen HTML. DOM dapat digunakan untuk mengubah tampilan halaman web. DOM dapat juga digunakan untuk menambahkan event listener pada elemen HTML. 
### 9.1 Seleksi Elemen

Seleksi elemen adalah proses untuk memilih elemen HTML. Seleksi elemen dapat dilakukan dengan menggunakan method `document.querySelector` dan `document.querySelectorAll`. Method `document.querySelector` digunakan untuk memilih satu elemen HTML. Method `document.querySelectorAll` digunakan untuk memilih semua elemen HTML.

Contoh:

```javascript
// Seleksi satu elemen
const title = document.querySelector("#title");

// Seleksi semua elemen
const paragraphs = document.querySelectorAll("p");
```

Beberapa tipe data dalam DOM:

    * `Document`: merupakan tipe data yang merepresentasikan dokumen HTML
    * `Node`: merupakan tipe data yang merepresentasikan elemen HTML
    * `Element`: merupakan tipe data yang merepresentasikan elemen HTML
    * `NodeList`: merupakan tipe data yang merepresentasikan kumpulan elemen HTML
    * `Text`: merupakan tipe data yang merepresentasikan teks
    * `Comment`: merupakan tipe data yang merepresentasikan komentar

### 9.2 Manipulasi Elemen

Manipulasi elemen adalah proses untuk mengubah elemen HTML. Manipulasi elemen dapat dilakukan dengan menggunakan method `innerHTML`, `style`, `classList`, dan `setAttribute`.

  * `innerHTML`: digunakan untuk mengubah konten HTML
  * `style`: digunakan untuk mengubah style CSS
  * `classList`: digunakan untuk mengubah class CSS
  * `setAttribute`: digunakan untuk mengubah atribut HTML

Contoh:

```javascript
// Mengubah konten HTML
const title = document.querySelector("#title");
title.innerHTML = "Hello World!";

// Mengubah style CSS
title.style.color = "red";

// Mengubah class CSS
title.classList.add("active");
title.classList.remove("dark");

// Mengubah atribut HTML
title.setAttribute("id", "title");
```

### 9.3 Generate Elemen

Generate elemen adalah proses untuk membuat elemen HTML. Generate elemen dapat dilakukan dengan menggunakan method `createElement` dan `appendChild`.

  * `createElement`: digunakan untuk membuat elemen HTML
  * `appendChild`: digunakan untuk menambahkan elemen HTML
  * `removeChild`: digunakan untuk menghapus elemen HTML
  * `replaceChild`: digunakan untuk mengganti elemen HTML

Contoh:

```javascript
// Membuat elemen HTML
const title = document.createElement("h1");
title.innerHTML = "Hello World!";
title.style.color = "red";

// Menambahkan elemen HTML
const container = document.querySelector("#container");
container.appendChild(title);

// Menghapus elemen HTML
container.removeChild(title);

// Mengganti elemen HTML
const newTitle = document.createElement("h1");
newTitle.innerHTML = "Hello World!";
newTitle.style.color = "red";
container.replaceChild(newTitle, title);
```

### 9.4 Event Listener

Event Listener adalah proses untuk menambahkan event pada elemen HTML. Event Listener dapat digunakan untuk menangani event yang terjadi pada elemen HTML. Event Listener dapat digunakan untuk menangani event yang terjadi pada elemen HTML. Event Listener dapat digunakan untuk menangani event yang terjadi pada elemen HTML.

Secara umum terdapat dua cara untuk menambahkan event listener pada elemen HTML:

  * Menggunakan atribut HTML
  * Menggunakan method `addEventListener`

Contoh:

```html
<!-- Menggunakan atribut HTML -->
<button onclick="alert('Hello World!')">Click Me!</button>

<!-- Menggunakan method addEventListener -->
<button id="button">Click Me!</button>
<script>
  const button = document.querySelector("#button");
  button.addEventListener("click", () => {
    alert("Hello World!");
  });
</script>
```

Bentuk umum dari method `addEventListener` adalah sebagai berikut:

```javascript
element.addEventListener(event);
element.addEventListener(event, callback, options);
element.addEventListener(event, callback, useCapture);
```

  * `event`: nama event yang akan ditangani (daftar event dapat dilihat di [https://developer.mozilla.org/en-US/docs/Web/Events](https://developer.mozilla.org/en-US/docs/Web/Events))
  * `callback`: fungsi yang akan dipanggil ketika event terjadi
  * `options`: opsi tambahan (opsional)
  * `useCapture`: opsi tambahan (opsional)

`options` memiliki beberapa pilihan:

  * `capture`: jika bernilai `true`, maka event listener akan dipanggil ketika event terjadi pada fase capturing. Jika bernilai `false`, maka event listener akan dipanggil ketika event terjadi pada fase bubbling. Secara default, `capture` bernilai `false`.
  * `once`: jika bernilai `true`, maka event listener hanya akan dipanggil sekali. Secara default, `once` bernilai `false`.
  * `passive`: jika bernilai `true`, maka event listener tidak akan membatalkan event.

`useCapture` adalah alias dari `options.capture`.

Contoh:

```javascript
// Event listener pada fase capturing
element.addEventListener("click", () => {
  console.log("click");
}, true);

// Event listener pada fase bubbling
element.addEventListener("click", () => {
  console.log("click");
}, false);
```

Untuk menghapus event listener, dapat digunakan method `removeEventListener`.

```javascript
element.removeEventListener(event, callback, options);
element.removeEventListener(event, callback, useCapture);
```

### 9.5 Event Object

Event object adalah objek yang digunakan untuk menangani event. Event object dapat digunakan untuk mengakses informasi dari event yang terjadi. Contoh informasi yang dapat diakses melalui event object adalah:

  * `target`: elemen HTML yang menjadi target dari event
  * `preventDefault`: fungsi untuk membatalkan event
  * `stopPropagation`: fungsi untuk menghentikan event propagation

Contoh:
  
```javascript
element.addEventListener("click", (event) => {
  console.log(event.target);
});

element.addEventListener("click", (event) => {
  event.preventDefault();
});
```

## 10. Javascript API

### 10.1 Fetch API

Fetch API adalah API yang digunakan untuk mengambil data dari server. Fetch API dapat digunakan untuk mengambil data dari server dengan menggunakan method `fetch`.

```javascript
fetch(url);
fetch(url, options);
```

  * `url`: URL dari data yang akan diambil (contoh: `https://jsonplaceholder.typicode.com/posts/1`)
  * `options`: opsi tambahan (opsional)

`options` memiliki beberapa pilihan:

  * `method`: method HTTP yang digunakan untuk mengambil data (default: `GET`, daftar method HTTP dapat dilihat di [https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods)
  * `headers`: header HTTP yang digunakan untuk mengambil data (default: `{}`)
  * `body`: body HTTP yang digunakan untuk mengambil data (default: `null`)

Contoh:
  
```javascript
fetch("https://jsonplaceholder.typicode.com/posts/1")
  .then((response) => response.json())
  .then((data) => console.log(data));

// menggunakan async / await
const response = await fetch("https://jsonplaceholder.typicode.com/posts/1");
const data = await response.json();
console.log(data);

// menggunakan async / await (versi singkat)
const data = await (await fetch("https://jsonplaceholder.typicode.com/posts/1")).json();

// method POST dengan async / await
const response = await fetch("https://jsonplaceholder.typicode.com/posts", {
  method: "POST",
  headers: {
    "Content-Type": "application/json",
  },
  body: JSON.stringify({
    title: "Hello World!",
    body: "Lorem ipsum dolor sit amet",
    userId: 1,
  }),
});
const data = await response.json();
console.log(data);
```

### 10.2 Local dan Session Storage

Local storage dan session storage adalah API yang digunakan untuk menyimpan data pada browser. Data yang disimpan pada local storage dan session storage akan tersimpan pada browser, sehingga data tersebut dapat diakses kembali pada saat browser tersebut dibuka kembali.

Local storage dan session storage memiliki method yang sama, yaitu:

  * `setItem(key, value)`: menyimpan data dengan key dan value yang ditentukan
  * `getItem(key)`: mengambil data dengan key yang ditentukan
  * `removeItem(key)`: menghapus data dengan key yang ditentukan
  * `clear()`: menghapus semua data

Contoh:

```javascript
// menyimpan data
localStorage.setItem("name", "John Doe");
sessionStorage.setItem("name", "John Doe");

// mengambil data
const name = localStorage.getItem("name");
const name = sessionStorage.getItem("name");

// menghapus data
localStorage.removeItem("name");
sessionStorage.removeItem("name");

// menghapus semua data
localStorage.clear();
sessionStorage.clear();
```









