# PERTEMUAN 1 - HTML & CSS

---

Materi ___Sunday Code Camp 2022___ pertemuan I

## HTML

![html](https://www.w3.org/html/logo/downloads/HTML5_Logo_512.png)

### Struktur Dasar HTML

Kita tidak akan membahas HTML secara detail, karena nanti akan dibahas secara mendalam di Pemrograman Web. Kita hanya akan membahas struktur dasar HTML. HTML adalah singkatan dari Hyper Text Markup Language. HTML merupakan bahasa markup yang terdiri dari tag-tag yang digunakan untuk menandai bagian-bagian dari isi sebuah halaman web.

Bagian utama dari elemen HTML adalah:
  * Tag pembuka: Terdiri dari tanda `<`, nama elemen, dan tanda `>`. Ini menunjukkan awal dari elemen.
  * Tag penutup: Terdiri dari tanda `<`, tanda `/`, nama elemen, dan tanda `>`. Ini menunjukkan akhir dari elemen.
  * Konten: Ini adalah konten dari elemen, seperti teks, gambar, video, dll.
  * Atribut: Ini adalah tambahan informasi tentang elemen. Atribut terdiri dari nama dan nilai dengan bentuk `nama="nilai"`.

Beberapa elemen HTML tidak memiliki konten dan hanya memiliki tag pembuka dan penutup. Contohnya adalah `<br>` dan `<img>`. Contohnya: `<img src="image.jpg" alt="My Image">`.

Secara umum dokumen HTML terdiri dari 3 bagian, yaitu:

  * `<!DOCTYPE html>` - Ini adalah deklarasi bahwa dokumen ini adalah dokumen HTML
  * `<html>` - Ini adalah tag pembuka dan penutup dokumen HTML
  * `<head>` - Ini adalah bagian dari dokumen HTML yang berisi informasi tentang dokumen HTML
  * `<body>` - Ini adalah bagian dari dokumen HTML yang berisi konten yang akan ditampilkan di browser

__`<!DOCTYPE html>`__

  <!DOCTYPE html> adalah deklarasi bahwa dokumen ini adalah dokumen HTML. Ini harus ditulis di baris pertama dari dokumen HTML.

__`<html>`__
  
  Tag <html> adalah tag pembuka dan penutup dokumen HTML. Semua elemen HTML harus ditulis di dalam tag <html>. Tag ini adalah induk dari semua elemen HTML.

__`<head>`__

  Tag <head> adalah bagian dari dokumen HTML yang berisi informasi tentang dokumen HTML yang bukan konten dan tidak akan ditampilkan di browser. Tag `<head>` berisi elemen `<title>`, `<meta>`, `<link>`, `<style>` dan `<script>`. Tag `<title>` adalah elemen yang paling penting di dalam tag `<head>`. Tag `<title>` berisi judul dari dokumen HTML. Tag `<meta>` berisi informasi tentang dokumen HTML. Tag `<link>` digunakan untuk menghubungkan dokumen HTML dengan file CSS. Tag `<style`> digunakan untuk menulis kode CSS langsung di dalam dokumen HTML. Tag `<script>` digunakan untuk menulis kode JavaScript langsung di dalam dokumen HTML.

__`<body>`__
  
    Tag `<body>` adalah bagian dari dokumen HTML yang berisi konten yang akan ditampilkan di browser.

### Semantic Tags

Semantic adalah makna atau arti dari sesuatu. Dalam HTML, contohnya `<h1>` adalah tag yang memiliki makna sebagai judul utama. Dengan tag ini, browser akan mengetahui bahwa tag tersebut adalah judul utama. Secara default, browser akan menampilkan tag tersebut dengan ukuran font yang lebih besar daripada tag lainnya (meskipun kita dapat mengubahnya dengan CSS). Dengan menggunakan tag yang semantik, kita dapat membuat HTML kita lebih mudah dibaca oleh mesin dan manusia.

HTML seharusnya ditulis untuk menyajikan __data__ yang akan ditampilkan dan bukan pada __tampilan__ nya di browser. Tampilan hanya ditentukan oleh CSS. Dengan demikian, kita dapat mengubah tampilan HTML tanpa harus mengubah struktur HTML nya. Beberapa keuntungan menggunakan tag semantik:

  * Mesin pencari dapat memahami struktur HTML kita sehingga dapat menampilkan hasil pencarian yang lebih baik (SEO)
  * Screen reader dapat membaca HTML kita dengan lebih baik sehingga dapat membantu orang dengan disabilitas visual
  * HTML kita akan lebih mudah dibaca oleh manusia karena struktur HTML nya lebih jelas dibandingkan dengan menggunakan tag non-semantik seperti `<div>` dan `<span>`

Ketika kita menuliskan tag mana yang sesuai, tanyakan pada diri kita terlebih dahulu __"Tag apa yang paling sesuai untuk menunjukkan makna dari data ini?"__. Contohnya, apakah dia daftar / _list_ dari data; apakah urutan penting? apakah dia sebuah article? apakah dia sebuah header? apakah dia sebuah navigasi?; dan sebagainya.

Terdapat sekitar 100 semantic tag yang tersedia, beberapa yang sering digunakan adalah:

  * `<header>`: Header dari sebuah halaman
  * `<nav>`: Navigasi
  * `<main>`: Bagian utama dari sebuah halaman
  * `<article>`: Artikel
  * `<section>`: Bagian dari sebuah halaman
  * `<aside>`: Bagian dari sebuah halaman yang tidak terkait dengan konten utama
  * `<footer>`: Footer dari sebuah halaman
  * `<figure>`: Gambar, video, atau audio
  * `<figcaption>`: Caption dari sebuah gambar, video, atau audio
  * `<details>`: Detail dari sebuah halaman
  * `<summary>`: Ringkasan dari sebuah halaman
  * `<time>`: Waktu
  
Elemen seperti `<header>`, `<nav>`, `<section>`, `<article>`, `<aside>`, dan `<footer>` memiliki bentuk yang sama seperti elemen `<div>`. Namun meskipun `<div>` bisa berisi bermacam jenis informasi, akan lebih mudah mengidentifikasi jenis data atau informasi dibagian tersebut jika menggunakan semantic tag seperti `<header>` misalnya.

Kode berikut adalah kode HTML yang menggunakan tag semantik:

```html
<header></header>
<section>
	<article>
		<figure>
			<img>
			<figcaption></figcaption>
		</figure>
	</article>
</section>
<footer></footer>
```

Kode berikut adalah kode HTML yang menggunakan tag non-semantik:

```html
<div id="header"></div>
<div class="section">
	<div class="article">
		<div class="figure">
			<img>
			<div class="figcaption"></div>
		</div>
	</div>
</div>
<div id="footer"></div>
```

Beberapa penjelasan mengenai tag semantik:

- `<section>` dan `<article>`

  `<section>` digunakan untuk membagi konten menjadi bagian-bagian yang berbeda. `<article>` digunakan untuk membagi konten menjadi artikel-artikel yang berbeda. `<section>` dan `<article>` dapat digunakan bersamaan. `<section>` biasanya digunakan untuk mengelompokkan konten menjadi bagian-bagian yang berbeda berdasarkan konteks, seperti bagian header, bagian konten, bagian navigasi, dan bagian footer. `<article>` biasanya digunakan untuk membagi konten menjadi artikel-artikel yang berbeda dan dapat didistribusikan atau dipublikasikan secara terpisah.

- `<header>`

  `<header>` digunakan untuk menunjukkan bagian header dari sebuah halaman. `<header>` dapat berisi judul, logo, navigasi, pencarian dan lain-lain. `<header>` dapat digunakan bersamaan dengan `<nav>` untuk menunjukkan bagian header dari sebuah halaman yang berisi

- `<aside>`

  `<aside>` digunakan untuk membagi konten menjadi bagian-bagian yang berbeda yang tidak terkait dengan konten utama. `<aside>` pada umumnya digunakan sebagai bagian sidebar dari sebuah halaman.

- `<footer>`

  `<footer>` digunakan untuk menunjukkan bagian footer dari sebuah halaman. `<footer>` dapat berisi informasi kontak, navigasi, dan lain-lain. Biasanya bagian ini berada di bagian bawah halaman.

- `<figure>` dan `<figcaption>`

  `<figure>` digunakan untuk menunjukkan gambar, video, atau audio. `<figcaption>` digunakan untuk menunjukkan caption dari sebuah gambar, video, atau audio.

- `<time>`

  `<time>` digunakan untuk menunjukkan waktu. Kenapa harus menggunakan tag `<time>`? Meskipun manusia dapat membaca tanggal dan waktu dengan mudah, mesin pencari tidak dapat membaca tanggal dan waktu dengan mudah. Tag `<time>` dapat membantu mesin pencari untuk mengidentifikasi tanggal dan waktu.

```html
<time datetime="2017-10-31T11:21:00+02:00">Januari 2019</time>
<details>
  <summary>Detail</summary>
  <p>Ini adalah detail dari sebuah halaman.</p>
</details>
```

### Emmet

Emmet adalah sebuah plugin yang dapat membantu kita untuk menuliskan kode HTML dengan cepat. Emmet dapat digunakan pada berbagai editor seperti Sublime Text, Atom, Visual Studio Code, dan lain-lain. Untuk menggunakan Emmet, kita harus menginstall plugin tersebut terlebih dahulu.

Emmet adalah toolkit untuk pengembang web yang wajib dimiliki. Kita cukup mengetikkan beberapa karakter dan kemudian tekan tombol `Tab` atau `Ctrl + E`, maka Emmet akan mengubahnya menjadi kode HTML yang lebih panjang. Emmet menggunakan sintaks mirip _CSS selector_. 

Kita dapat mencoba beberapa contoh berikut:

  * `!`
  * `header>h1.logo+nav>ul>li*5>a`
  * `div#header>h1.logo>a{nama situs}`
  * `div#header>h1.logo>a{nama situs}+nav>ul>li*5>a{item $}`
  * `header#site-header^div.container#main>.primary+aside#sidebar^footer#site-footer`
  * `(header#site-header>h1.logo>a[href=#]{site name})^div.container#main>(.primary>h1.post-title{post title here}+img.featured-img+p{post text here})+(aside#sidebar>#widget>h2.widget-title+p{widget text})^footer.#site-footer>.col-4.widget*3>h2.widget-title+p.widget-text`

Berikut ini adalah beberapa operator yang dapat digunakan pada Emmet:

  * `>`: Indentasi
  * `+`: Sibling
  * `*`: Multiplication
  * `{}`: Text
  * `$`: Numbering

__Element__

Untuk membuat sebuah elemen, cukup ketikkan nama elemen tersebut. Contoh: `div`, `p`, `h1`, `img`, `a`, `ul`, `li`, dan lain-lain.

__ID__

Untuk menambahkan ID pada sebuah elemen, cukup ketikkan `#` diikuti dengan nama ID. Contoh: `#header`, `#footer`, `#logo`, `#content`, dan lain-lain.

__Class__

Untuk menambahkan class pada sebuah elemen, cukup ketikkan `.` diikuti dengan nama class. Contoh: `.header`, `.footer`, `.logo`, `.content`, dan lain-lain.

__Child__

Untuk membuat child element, cukup ketikkan `>` diikuti dengan nama elemen. Contoh: `div>h1`, `div>p`, `div>img`, `div>a`, `div>ul`, `div>li`, dan lain-lain.

__Sibling__

Untuk membuat sibling element, cukup ketikkan `+` diikuti dengan nama elemen. Contoh: `div+p`, `div+img`, `div+a`, `div+ul`, `div+li`, dan lain-lain.

__Multiplication__

Untuk membuat beberapa sibling element, cukup ketikkan `*` diikuti dengan jumlah sibling element. Contoh: `div*5`, `div*10`, `div*20`, dan lain-lain.

__Numbering__

Untuk menambahkan numbering pada sebuah elemen, cukup ketikkan `$` diikuti dengan angka. Contoh: `div$*5`, `div$*10`, `div$*20`, dan lain-lain.

__Text__

Untuk menambahkan text pada sebuah elemen, cukup ketikkan `{}` diikuti dengan text. Contoh: `div{ini adalah text}`, `div{ini adalah text}+p{ini adalah text}`, `div{ini adalah text}+p{ini adalah text}+img{ini adalah text}`, dan lain-lain.

__Grouping__

Untuk membuat grouping, cukup ketikkan `()` diikuti dengan elemen. Contoh: `div>(h1+p)+img`, `div>(h1+p)+img+ul>li*5`, `div>(h1+p)+img+ul>li*5>a`, dan lain-lain.

__Climb-up__

Untuk membuat climb-up, cukup ketikkan `^` diikuti dengan elemen. Contoh: `div>ul>li*5>a^p`, `div>ul>li*5>a^p^div`, `div>ul>li*5>a^p^div>img`, dan lain-lain.

---

## CSS

![CSS](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d5/CSS3_logo_and_wordmark.svg/1200px-CSS3_logo_and_wordmark.svg.png)

### Penempatan CSS

### CSS Selector

### Animasi