---
layout: post
title: "Menambahkan Video ke dalam HTML"
---
penjelasan tentang cara menambahkan file video ke halaman HTML

![HTML Video](/assets/images/htmlgambar.png)

---

# 1. **HTML Video**

HTML menyediakan tag `<video>` untuk menampilkan dan memutar file video langsung dalam halaman web. Elemen ini memungkinkan Anda menyisipkan video tanpa memerlukan plugin tambahan.

## 1.1. **Struktur Dasar Tag Video**

Berikut adalah struktur dasar penggunaan tag `<video>`:

```html
<video controls>
  <source src="video-file.mp4" type="video/mp4">
  Browser Anda tidak mendukung pemutar video.
</video>
````

* **`<video>`**: Elemen utama untuk menyisipkan video.
* **`controls`**: Menampilkan kontrol pemutaran seperti play, pause, volume.
* **`<source>`**: Menentukan file video yang akan diputar dan jenis formatnya.
* **Fallback Text**: Ditampilkan jika browser tidak mendukung elemen video.

## 1.2. **Format Video yang Didukung**

HTML5 mendukung beberapa format video populer:

* MP4: `type="video/mp4"` — paling banyak didukung.
* WebM: `type="video/webm"`
* Ogg: `type="video/ogg"`

### Contoh Multi Format:

```html
<video controls>
  <source src="video.webm" type="video/webm">
  <source src="video.mp4" type="video/mp4">
  Browser Anda tidak mendukung video HTML5.
</video>
```

**Penjelasan**:

* Browser akan memilih format yang didukung.
* Memberikan fallback memastikan kompatibilitas lintas browser.

## 1.3. **Atribut Tambahan pada Tag Video**

* **`autoplay`**: Video diputar otomatis saat halaman dimuat.
* **`loop`**: Video diputar berulang secara terus-menerus.
* **`muted`**: Video diputar dalam keadaan tanpa suara.
* **`poster`**: Gambar thumbnail yang ditampilkan sebelum video diputar.
* **`width` & `height`**: Menentukan ukuran tampilan video.

### Contoh:

```html
<video width="640" height="360" controls autoplay muted loop poster="thumbnail.jpg">
  <source src="clip.mp4" type="video/mp4">
</video>
```

**Penjelasan**:

* Video diputar otomatis tanpa suara, terus-menerus, dan menampilkan gambar thumbnail sebelum diputar.

---

# 2. **Fallback dan Teks Alternatif**

Tambahkan teks alternatif agar pengguna dengan browser lama tetap mendapat informasi:

```html
<video controls>
  <source src="video.ogg" type="video/ogg">
  Maaf, browser Anda tidak mendukung elemen video HTML5.
</video>
```

---

# 3. **Kesimpulan**

* Gunakan tag `<video>` untuk menampilkan video langsung di halaman web.
* Tambahkan atribut seperti `controls`, `autoplay`, `loop`, dan `poster` untuk menyesuaikan tampilan dan perilaku video.
* Gunakan beberapa format video agar kompatibel dengan berbagai browser.
* Selalu sertakan fallback text untuk pengguna yang tidak mendukung HTML5.

Video adalah media visual yang sangat efektif untuk meningkatkan pengalaman pengguna dalam berbagai konteks web, mulai dari edukasi hingga promosi.

```