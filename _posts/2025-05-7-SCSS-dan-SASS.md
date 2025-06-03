---
layout: post
title: "Mengenal SCSS dan SASS"
---
Penjelasan tentang SCSS dan SASS

![scss dan sass](/assets/images/htmlgambar.png)

---

# 1. **Apa itu SASS dan SCSS?**

**SASS** (Syntactically Awesome Stylesheets) adalah ekstensi dari CSS yang memungkinkan penulisan stylesheet yang lebih modular, fleksibel, dan dinamis. SCSS adalah sintaks yang lebih modern dari SASS yang sepenuhnya kompatibel dengan CSS.

## 1.1. **Perbedaan SASS dan SCSS**

- **SASS** menggunakan indentasi untuk menentukan hierarki, tanpa menggunakan tanda kurung atau titik koma.
- **SCSS** menggunakan sintaks mirip CSS, yang berarti menggunakan kurung kurawal `{}` dan titik koma `;`.

---

# 2. **Keuntungan Menggunakan SASS/SCSS**

- **Variabel**: Menyimpan nilai seperti warna, ukuran font, dll, untuk digunakan di seluruh file CSS.
- **Nested Rules**: Menulis CSS yang terstruktur dengan lebih mudah menggunakan indentasi.
- **Partials**: Memecah kode menjadi file kecil agar lebih mudah dikelola.
- **Mixins**: Menyusun kode CSS yang dapat digunakan kembali di beberapa tempat.
- **Inheritance**: Menggunakan aturan pewarisan untuk menghindari pengulangan kode.

---

# 3. **Contoh Penggunaan SCSS**

## 3.1. **Penggunaan Variabel**

Dengan SCSS, kamu bisa mendeklarasikan variabel untuk nilai yang sering digunakan.

```scss
$primary-color: #3498db;
$font-size: 16px;

body {
  font-size: $font-size;
  color: $primary-color;
}
````

## 3.2. **Nested Rules (Aturan Bertingkat)**

SCSS memungkinkan penulisan aturan CSS yang lebih terstruktur dan lebih mudah dibaca.

```scss
nav {
  background-color: $primary-color;
  
  ul {
    list-style-type: none;
    
    li {
      display: inline;
      margin: 0 15px;
    }
  }
}
```

## 3.3. **Mixins**

Mixins memungkinkan kamu menulis ulang kode CSS yang dapat digunakan di beberapa tempat.

```scss
@mixin border-radius($radius) {
  -webkit-border-radius: $radius;
  -moz-border-radius: $radius;
  border-radius: $radius;
}

.button {
  @include border-radius(10px);
  padding: 10px 20px;
  background-color: $primary-color;
}
```

---

# 4. **Menggunakan Partials di SCSS**

SCSS mendukung partials, yaitu file kecil yang dapat diimpor ke dalam file utama untuk memecah kode menjadi bagian-bagian yang lebih kecil dan mudah dikelola.

### 4.1. **Contoh Struktur Partials**

1. **\_variables.scss** – Menyimpan semua variabel.
2. **\_base.scss** – Menyimpan aturan dasar seperti body, font, dll.
3. **\_buttons.scss** – Menyimpan aturan untuk tombol.

### 4.2. **Menggunakan Partials**

```scss
// _variables.scss
$primary-color: #3498db;
$font-size: 16px;

// _base.scss
body {
  font-size: $font-size;
  background-color: #f4f4f4;
}

// main.scss
@import 'variables';
@import 'base';

button {
  background-color: $primary-color;
  color: white;
}
```

---

# 5. **SASS vs SCSS: Mana yang Lebih Baik?**

* **SCSS** lebih sering digunakan karena sintaksnya yang lebih mirip dengan CSS, sehingga lebih mudah dipahami oleh banyak orang, terutama mereka yang sudah familiar dengan CSS.
* **SASS** menawarkan sintaks yang lebih ringkas dan minimalis, yang disukai oleh beberapa pengembang untuk kode yang lebih bersih dan lebih cepat ditulis.

---

# 6. **Cara Mengkompilasi SCSS ke CSS**

Untuk menggunakan SCSS atau SASS, kamu perlu mengkompilasi file `.scss` atau `.sass` ke dalam file `.css`. Ini bisa dilakukan dengan berbagai alat, seperti:

## 6.1. **Menggunakan Node.js dan npm**

1. Install package `sass` dengan npm:

```bash
npm install -g sass
```

2. Mengkompilasi file SCSS:

```bash
sass styles.scss styles.css
```

Atau untuk mengkompilasi secara otomatis setiap kali file SCSS diubah:

```bash
sass --watch styles.scss:styles.css
```

## 6.2. **Menggunakan Prepros**

Prepros adalah aplikasi desktop yang memudahkan kompilasi SCSS dan SASS. Kamu cukup memilih file SCSS yang ingin dikompilasi, dan Prepros akan menangani semuanya secara otomatis.

---

# 7. **Tips dan Best Practices**

* **Gunakan Partials**: Pecah kode SCSS menjadi file terpisah agar lebih mudah dikelola.
* **Jangan Berlebihan dengan Nesting**: Nesting terlalu dalam dapat memperumit kode dan menyebabkan masalah performa.
* **Manfaatkan Mixins dan Functions**: Untuk menghindari pengulangan kode dan meningkatkan maintainability.
* **Minimalkan File SCSS**: Gunakan kompresi untuk menghasilkan file CSS yang lebih kecil.

---

# 8. **Kesimpulan**

* **SASS** dan **SCSS** adalah alat yang kuat untuk mempercepat pengembangan dan menulis CSS yang lebih dinamis.
* **SCSS** lebih populer dan lebih mirip dengan CSS, sementara **SASS** menawarkan sintaks yang lebih ringkas.
* Dengan fitur seperti variabel, mixins, dan partials, SCSS membuat kode CSS lebih modular, mudah dibaca, dan dapat dipelihara.

Mulailah menggunakan SCSS atau SASS di proyekmu dan rasakan kemudahan serta fleksibilitas yang ditawarkannya!

```