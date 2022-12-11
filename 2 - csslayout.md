# PERTEMUAN 2 - CSS LAYOUT (FLEXBOX & GRID)

---

Materi ___Sunday Code Camp 2022___ pertemuan II

Sebelum membahas tentang CSS Layout, kita akan membahas terlebih dahulu tentang CSS Box Model dan CSS Position.

### Inline dan Block

Secara default, elemen HTML memiliki 2 jenis, yaitu inline dan block. Elemen HTML juga memiliki box model yang terdiri dari margin, border, padding, dan content.

#### __Inline__

Inline element adalah elemen yang tidak memiliki lebar dan tinggi dan  hanya memiliki panjang sesuai dengan panjang teksnya. Inline element tidak bisa diatur lebarnya, hanya bisa diatur tingginya. Contoh inline element adalah `a`, `span`, `img`, `input`, `button`, `label`, dan lain-lain.

#### __Block__

Block element adalah elemen yang memiliki lebar dan tinggi yang bisa diatur. Secara default, block element akan mengambil lebar 100% dari parent elementnya dan berposisi di bawah element sebelumnya. Contoh block element adalah `div`, `p`, `h1`, `h2`, `h3`, `h4`, `h5`, `h6`, `ul`, `ol`, `li`, dan lain-lain.

### Box Model

![Box Model](https://media.gcflearnfree.org/content/5ef2084faaf0ac46dc9c10be_06_23_2020/box_model.png)

Box model adalah model yang digunakan untuk mengatur tampilan elemen HTML. Box model terdiri dari 4 bagian, yaitu:

#### __Margin__

Margin adalah jarak antara elemen dengan elemen lainnya yang disebelahnya. Margin bisa diatur dengan property `margin` dan `margin-*` (misalnya `margin-top`, `margin-bottom`, `margin-left`, `margin-right`).

#### __Border__

Border adalah garis yang mengelilingi elemen. Border bisa diatur dengan property `border` dan `border-*` (misalnya `border-top`, `border-bottom`, `border-left`, `border-right`). Property `border` bisa diatur dengan 3 cara, yaitu:

1. `border: 1px solid black;` (lebar, jenis, dan warna border)
2. `border: 1px solid;` (lebar dan jenis border)
3. `border: 1px;` (lebar border)

#### __Padding__

Padding adalah jarak antara border dan isi elemen. Padding bisa diatur dengan property `padding` dan `padding-*` (misalnya `padding-top`, `padding-bottom`, `padding-left`, `padding-right`).

#### __Content__

Content adalah isi dari elemen. Content bisa diatur dengan property `width` dan `height`. Property `width` dan `height` bisa diatur dengan 3 cara, yaitu:

1. `width: 100px;` (lebar elemen)
2. `width: 100%;` (lebar elemen 100% dari parent element)
3. `width: auto;` (lebar elemen sesuai dengan isi elemen)

### Position

Position adalah property yang digunakan untuk mengatur posisi elemen HTML. 

#### Relative

Position relative adalah posisi dimana elemen akan berada di posisi normalnya, tetapi bisa diatur posisinya. Elemen dengan posisi relative bisa diatur posisinya dengan property `top`, `bottom`, `left`, dan `right`.

#### Absolute

Position absolute adalah posisi relatif terhadap parent elementnya (jika parent elementnya tidak memiliki posisi absolute, maka posisi absolute akan berada relatif terhadap body). Posisi juga bisa diatur dengan property `top`, `bottom`, `left`, dan `right`.

#### Fixed

Elemen dengan posisi fixed akan berada relatif terhadap viewport browser yang berarti akan tetap berada di posisi yang sama meskipun kita scroll. Elemen dengan posisi fixed bisa diatur posisinya dengan property `top`, `bottom`, `left`, dan `right`. Elemen dengan posisi fixed akan berada di luar parent elementnya.

#### Sticky

Elemen dengan posisi sticky diposisikan berdasarkan posisi scroll. Elemen sticky akan berada di posisi normalnya, tetapi jika kita scroll, maka elemen sticky akan berada di posisi fixed.

### Display

Berdasarkan property `display`, elemen HTML bisa diatur menjadi 4 jenis, yaitu:

1. __Block__
2. __Inline__
3. __Inline-block__ (inline yang bisa diatur lebarnya)
4. __None__ (elemen tidak akan ditampilkan)

---

## Flexbox

![Flexbox](https://img.devrant.com/devrant/rant/r_71175_yi7sg.jpg)

Flexbox bertujuan untuk menyediakan cara yang lebih efisien untuk mengatur, meratakan dan menyebarkan ruang di antara item-item dalam sebuah container, bahkan ketika ukurannya tidak diketahui dan/atau dinamis (dengan kata lain, “flex”). Ide utamanya adalah memberikan container kemampuan untuk mengubah lebar/tinggi item (dan urutan) untuk mengisi ruang yang tersedia.

Flex adalah satu paket / modul, sehingga terdiri dari beberapa property yang saling berhubungan satu sama lain. Beberapa property diset pada container (`flex container`), dan beberapa property diset pada item (`flex item`).

### Flex Container

Untuk membuat flex container, kita bisa menggunakan property `display: flex;` atau `display: inline-flex;`. Flex container adalah elemen yang akan menampung flex item. Flexbox memiliki 2 sumbu, yaitu sumbu utama dan sumbu silang. Sumbu utama adalah sumbu yang sesuai dengan arah flex item, sedangkan sumbu silang adalah sumbu yang tegak lurus dengan sumbu utama.

```css
.container {
  display: flex;
}
```

Kemudian, kita bisa mengatur flex container dengan property-property berikut:

#### __Flex Direction__

Property `flex-direction` digunakan untuk mengatur arah flex item sesuai sumbu utama. Property `flex-direction` memiliki 4 nilai, yaitu:

- `row` (default) - flex item akan berada di sumbu utama dari kiri ke kanan
- `row-reverse` - flex item akan berada di sumbu utama dari kanan ke kiri
- `column` - flex item akan berada di sumbu utama dari atas ke bawah
- `column-reverse` - flex item akan berada di sumbu utama dari bawah ke atas

#### __Flex Wrap__

Secara default semua flex item akan berada di satu baris. Property `flex-wrap` digunakan untuk mengatur flex item jika ukuran flex container tidak cukup untuk menampung semua flex item. Property `flex-wrap` memiliki 3 nilai, yaitu:

- `nowrap` (default) - semua flex item akan berada di satu baris
- `wrap` - flex item akan berada di baris baru jika ukuran flex container tidak cukup untuk menampung semua flex item
- `wrap-reverse` - flex item akan berada di baris baru jika ukuran flex container tidak cukup untuk menampung semua flex item, tetapi baris pertama akan berada di bawah baris terakhir

#### __Flex Flow__

Property `flex-flow` adalah gabungan dari `flex-direction` dan `flex-wrap`. Property `flex-flow` memiliki 2 nilai, yaitu:

- `flex-flow: row nowrap;` (default)
- `flex-flow: column wrap;`

#### __Justify Content__

Property `justify-content` digunakan untuk mengatur posisi flex item di sumbu utama. Property `justify-content` memiliki 6 nilai, yaitu:

- `flex-start` (default) - flex item akan berada di ujung awal sumbu utama
- `flex-end` - flex item akan berada di ujung akhir sumbu utama
- `center` - flex item akan berada di tengah sumbu utama
- `space-between` - flex item akan berada di antara ujung awal dan ujung akhir sumbu utama, dengan jarak yang sama di antara flex item
- `space-around` - flex item akan berada di antara ujung awal dan ujung akhir sumbu utama, dengan jarak yang sama di antara flex item dan ujung awal/akhir sumbu utama
- `space-evenly` - flex item akan berada di antara ujung awal dan ujung akhir sumbu utama, dengan jarak yang sama di antara flex item dan ujung awal/akhir sumbu utama

![justify-content](https://samanthaming.gumlet.io/flexbox30/14-space-around-vs-space-evenly.jpg.gz?format=auto)

#### __Align Items__

Property `align-items` digunakan untuk mengatur posisi flex item di sumbu silang. Property `align-items` memiliki 6 nilai, yaitu:

- `stretch` (default) - flex item akan memperluas ukuran sesuai dengan ukuran flex container
- `flex-start` - flex item akan berada di ujung awal sumbu silang
- `flex-end` - flex item akan berada di ujung akhir sumbu silang
- `center` - flex item akan berada di tengah sumbu silang
- `baseline` - flex item akan berada di baseline sumbu silang

#### __Align Content__

Property `align-content` digunakan untuk mengatur posisi flex item di sumbu silang jika flex item __lebih dari satu baris__. Property `align-content` memiliki 6 nilai, yaitu:

- `normal` (default) - flex item akan berada di ujung awal sumbu silang
- `flex-start` - flex item akan berada di ujung awal sumbu silang
- `flex-end` - flex item akan berada di ujung akhir sumbu silang
- `center` - flex item akan berada di tengah sumbu silang
- `space-between` - flex item akan berada di antara ujung awal dan ujung akhir sumbu silang, dengan jarak yang sama di antara flex item
- `space-around` - flex item akan berada di antara ujung awal dan ujung akhir sumbu silang, dengan jarak yang sama di antara flex item dan ujung awal/akhir sumbu silang
- `space-evenly` - flex item akan berada di antara ujung awal dan ujung akhir sumbu silang, dengan jarak yang sama di antara flex item dan ujung awal/akhir sumbu silang
- `stretch` - flex item akan memperluas ukuran sesuai dengan ukuran flex container

#### __Gap__, __Row Gap__, __Column Gap__

Property `gap`, `row-gap`, dan `column-gap` digunakan untuk mengatur jarak antar flex item (__hanya jarak antar item bukan jarak item dengan sisi luar__). Property `gap` memiliki 3 nilai, yaitu:

### Flex Item

Flex item ada property yang diletakkan pada anak dari flex container. Property-property tersebut adalah:

#### __Order__

Property `order` digunakan untuk mengatur urutan flex item. Property `order` memiliki nilai angka, dimana angka tersebut menunjukkan urutan flex item. Angka yang lebih besar akan berada di belakang angka yang lebih kecil. Angka defaultnya adalah 0. Dengan menggunakan property `order` kita bisa mengatur urutan flex item tanpa harus mengubah urutan HTML.

#### __Flex Grow__

Property `flex-grow` digunakan untuk mengatur ukuran flex item. Property `flex-grow` memiliki nilai angka, dimana angka tersebut menunjukkan ukuran flex item. Angka yang lebih besar akan memperluas ukuran flex item lebih besar daripada angka yang lebih kecil. Angka defaultnya adalah 0. Jika semua item diberi nilai 1, maka ruangan akan dibagi rata untuk semua item. Jika satu item diberi nilai 2, maka item tersebut akan memperluas ukuran 2 kali lipat dari item lainnya.

#### __Flex Shrink__

Property `flex-shrink` digunakan untuk mengatur ukuran flex item. Property `flex-shrink` memiliki nilai angka, dimana angka tersebut menunjukkan ukuran flex item. Angka yang lebih besar akan memperkecil ukuran flex item lebih besar daripada angka yang lebih kecil.

#### __Flex Basis__

Property `flex-basis` digunakan untuk menentukan ukuran default sebuah elemen sebelum ukuran tersebut diatur oleh `flex-grow` dan `flex-shrink`. 

#### __Flex__

Property `flex` merupakan gabungan dari `flex-grow`, `flex-shrink`, dan `flex-basis`. Property `flex` memiliki 3 nilai, yaitu:

- `flex-grow` - nilai defaultnya adalah 0
- `flex-shrink` - nilai defaultnya adalah 1
- `flex-basis` - nilai defaultnya adalah `auto`

```css
.item {
  flex: 1 1 200px;
}
```

#### __Align Self__

Property `align-self` digunakan untuk mengatur posisi flex item di sumbu silang yang diset oleh `align-items`.

--- 

## Grid

Grid adalah sistem layout 2 dimensi yang terdiri dari baris dan kolom. Grid sangat berguna untuk membuat layout yang kompleks. Flexbox hanya bisa membuat layout 1 dimensi (satu arah) untuk kasus yang berbeda. Flexbox dan grid bisa digunakan bersamaan untuk membuat layout yang kompleks. Grid memiliki 2 komponen, yaitu:

- Grid Container - elemen yang berisi grid
- Grid Item - elemen yang berada di dalam grid container

### Grid Container

Grid container ada property yang diletakkan pada elemen yang akan menjadi grid. Property-property tersebut adalah:

#### __Display__

Property `display` digunakan untuk mengatur elemen menjadi grid. Property `display` memiliki 2 nilai, yaitu:

- `grid` - elemen akan menjadi grid container
- `inline-grid` - elemen akan menjadi grid container inline

#### __Row Gap__, __Column Gap__ dan __Grid Gap__

Gap adalah jarak antar grid item. Property `row-gap`, `column-gap`, dan `grid-gap` digunakan untuk mengatur jarak antar grid item. Property `grid-gap` memiliki 3 nilai, yaitu:

- `row-gap` - jarak antar grid item di sumbu baris (contoh: `row-gap: 20px`)
- `column-gap` - jarak antar grid item di sumbu kolom (contoh: `column-gap: 20px`)
- `grid-gap` - jarak antar grid item di sumbu baris dan kolom (contoh: `grid-gap: 20px 10px`)

#### __Grid Template Columns__, __Grid Template Rows__

Property `grid-template-columns` dan `grid-template-rows`  digunakan untuk mengatur ukuran kolom dan baris grid. Property ini memiliki beberapa nilai, yaitu:

- `repeat()` - mengulang kolom grid sebanyak jumlah yang ditentukan
  Contoh: `repeat(3, 1fr)` akan menghasilkan 3 kolom dengan ukuran yang sama. `repeat()` memiliki 2 parameter, yaitu:
  * `jumlah` - jumlah kolom yang akan diulang
  * `ukuran` - ukuran kolom yang akan diulang
  
Untuk `jumlah`, kita bisa menggunakan `auto-fill` atau `auto-fit`.Contoh: `repeat(auto-fill, minmax(100px, 1fr))` akan menghasilkan kolom grid sebanyak yang bisa ditampilkan di layar, dengan ukuran minimal 100px dan maksimal 1fr. `auto-fill` akan mengulang kolom grid sebanyak yang bisa ditampilkan di layar. Sedangkan `auto-fit` akan mengulang kolom grid sebanyak mungkin hingga ukuran kolom grid mencapai ukuran maksimal.

- `fr` - mengatur ukuran kolom grid berdasarkan pembagian ruang yang tersisa (contoh: `1fr 1fr 1fr`)
- `minmax()` - mengatur ukuran kolom grid dengan batasan minimal dan maksimal (contoh: `minmax(100px, 1fr)`)
- `min-content` - minimal ukuran kolom grid sesuai dengan isi. contoh: `min-content() 1fr 1fr`
- `max-content` - maksimal ukuran kolom grid sesuai dengan isi
- `fit-content` - mengatur ukuran kolom grid sesuai dengan isi
- `auto` - mengatur ukuran kolom grid sesuai dengan isi

```css
.container {
  grid-template-columns: repeat(3, 1fr);
  /*
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-columns: minmax(100px, 1fr) 1fr 1fr;
  grid-template-columns: 50px auto 100px 1fr;
}
```

![Grid Template Columns](https://css-tricks.com/wp-content/uploads/2018/11/template-columns-rows-01.svg)

#### __Grid Template Areas__

Property `grid-template-areas` digunakan untuk mengatur nama-nama area grid. Property ini memiliki 3 nilai, yaitu:

- `.` - area kosong
- `nama-area` - area dengan nama tertentu
- `nama-area nama-area` - area dengan nama tertentu yang berada di baris berikutnya (nama yang sama akan menggabungkan area)

```css
.container {
  grid-template-areas:
    "header header header"
    "main main sidebar"
    "footer footer footer";

  grid-template-row: 100px 1fr 100px;
  grid-template-columns: 1fr 200px 1fr;
}
```

#### __Place Items__

Property `place-items` merupakan gabungan dari `align-items` dan `justify-items`. Property ini memiliki 2 nilai, yaitu:

- `justify-items` - mengatur posisi grid item di sumbu baris
- `align-items` - mengatur posisi grid item di sumbu kolom

```css
.container {
  place-items: center;
}
```

Nilai yang bisa digunakan untuk `justify-items` dan `align-items` adalah:

- `start` - posisi grid item di ujung awal
- `end` - posisi grid item di ujung akhir
- `center` - posisi grid item di tengah
- `stretch` - posisi grid item di ujung awal dan akhir
- `baseline` - posisi grid item di baris pertama

#### __Place Content__

Property `place-content` merupakan gabungan dari `align-content` dan `justify-content`. Property ini memiliki 2 nilai, yaitu:

- `justify-content` - mengatur posisi grid item di sumbu baris
- `align-content` - mengatur posisi grid item di sumbu kolom

```css
.container {
  place-content: center;
}
```
Nilai yang bisa digunakan sama dengan `place-items`.

#### __Grid Auto Rows__, __Grid Auto Columns__

Property `grid-auto-rows` dan `grid-auto-columns` digunakan untuk mengatur ukuran kolom dan baris grid secara otomatis. Property ini biasanya digunakan untuk mengatur ukuran kolom dan baris grid yang tidak ditentukan.

```css
.container {
  grid-auto-rows: 100px;
  grid-auto-columns: 100px;
}
```

#### __Grid Auto Flow__

Jika kita tidak menentukan posisi grid item, maka grid item akan ditampilkan secara otomatis. Property `grid-auto-flow` digunakan untuk mengatur cara grid item ditampilkan secara otomatis. Property ini memiliki 2 nilai, yaitu:

- `row` - grid item ditampilkan secara horizontal
- `column` - grid item ditampilkan secara vertikal
- `dense` - grid item ditampilkan secara otomatis dengan mengisi ruang kosong

```css
.container {
  grid-auto-flow: row;
}
```

---

#### __Grid Row__, __Grid Column__

![Grid Row dan Grid Column](https://css-tricks.com/wp-content/uploads/2018/11/grid-column-row-start-end-02.svg)

Grid_row dan grid_column digunakan untuk mengatur posisi grid item. Property ini merupakan gabungan dari `grid-row-start`, `grid-row-end`, `grid-column-start`, dan `grid-column-end`. Dengan property ini, kita bisa melakukan hal-hal seperti menggabungkan beberapa grid item menjadi satu, mengatur posisi grid item, dan lain-lain.

```css
.item {
  grid-row: 1 / 3;
  grid-column: 1 / 3;
}
```

Jika kita tidak tahu posisi grid item, kita bisa menggunakan `span` untuk mengatur posisi grid item. `span` digunakan untuk mengatur posisi grid item berdasarkan jumlah kolom atau baris yang akan diambil. Contoh: `grid-row: 1 / span 2`, `grid-column: span 2 / auto`.

#### __Grid Area__

Kita bisa memberikan item grid sebuah nama sehingga dapat di referensikan oleh template yang dibuat dengan property `grid-template-areas`. Property `grid-area` memiliki 3 nilai, yaitu:

- `nama-area` - memberikan item grid sebuah nama
- `nama-area / nama-area` - memberikan item grid sebuah nama dan mengatur posisi item grid
- `nama-area / nama-area / nama-area / nama-area` - memberikan item grid sebuah nama dan mengatur posisi item grid

```css
.item {
  grid-area: header;
}
```

#### __Place Self__

Property `place-self` merupakan gabungan dari `align-self` dan `justify-self`. Property ini memiliki 2 nilai, yaitu:

- `justify-self` - mengatur posisi grid item di sumbu baris
- `align-self` - mengatur posisi grid item di sumbu kolom

```css
.item {
  place-self: center;
}
```

Nilai yang bisa digunakan sama dengan `place-items`.

Lihat referensi lengkapnya di [https://css-tricks.com/snippets/css/complete-guide-grid/](https://css-tricks.com/snippets/css/complete-guide-grid/).

## Latihan

[https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Grid_skills](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Grid_skills)
















