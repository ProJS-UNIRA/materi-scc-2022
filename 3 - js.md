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

### 6.4 Arrow Function

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

## 9. DOM

DOM adalah singkatan dari Document Object Model. DOM adalah API yang digunakan untuk mengakses dan memanipulasi elemen HTML. DOM dapat digunakan untuk mengubah tampilan halaman web. DOM dapat digunakan untuk menambahkan event listener pada elemen HTML. DOM dapat digunakan untuk mengambil data dari elemen HTML.








