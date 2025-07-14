---
layout: post
title: "Bootstrap"
---
Penjelasan tentang Bootstrap

![Bootstrap](/assets/images/htmlgambar.png)
---
# 🎨 Panduan Dasar Bootstrap untuk Pemula

📅 *25 Juni 2025*

Bootstrap adalah framework CSS paling populer yang digunakan untuk membangun tampilan website modern dan responsif dengan cepat. Dikembangkan oleh tim Twitter, Bootstrap menyediakan komponen siap pakai seperti tombol, form, navbar, grid, dan masih banyak lagi.

---

## 🧰 Apa Kelebihan Bootstrap?

- ✅ Responsif di semua ukuran layar (mobile-first)
- ✅ Hemat waktu karena komponen sudah siap pakai
- ✅ Dokumentasi lengkap dan komunitas luas
- ✅ Mendukung customisasi dengan class bawaan

---

## 📦 Cara Menggunakan Bootstrap

### 🔗 1. CDN (langsung online)

Masukkan baris ini di `<head>` file HTML kamu:

```html
<!-- Bootstrap 5 CDN -->
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
````

### 💾 2. Unduh File

Kunjungi [getbootstrap.com](https://getbootstrap.com) → klik "Download" → lalu hubungkan ke file CSS dan JS yang diunduh.

---

## 🧱 Struktur Grid Sistem (Layout)

Bootstrap menggunakan sistem grid 12 kolom. Contoh:

```html
<div class="container">
  <div class="row">
    <div class="col-4">Kolom 1</div>
    <div class="col-4">Kolom 2</div>
    <div class="col-4">Kolom 3</div>
  </div>
</div>
```

📌 *Tips*: Gunakan `container` untuk pembungkus, dan `row` untuk baris sebelum `col`.

---

## 🧩 Komponen Dasar Bootstrap

### 1. 🔘 Tombol

```html
<button class="btn btn-primary">Tombol Biru</button>
<button class="btn btn-success">Tombol Hijau</button>
<button class="btn btn-danger">Hapus</button>
```

### 2. 📥 Formulir

```html
<form>
  <div class="mb-3">
    <label for="email" class="form-label">Email:</label>
    <input type="email" class="form-control" id="email">
  </div>
  <button type="submit" class="btn btn-primary">Kirim</button>
</form>
```

### 3. 📌 Alert

```html
<div class="alert alert-warning" role="alert">
  Ini adalah peringatan!
</div>
```

---

## 📱 Responsivitas

Gunakan class seperti:

* `d-none d-md-block`: elemen hanya muncul di layar medium ke atas
* `col-sm-6 col-md-4`: lebar kolom yang berubah tergantung ukuran layar

---

## 🎯 Tips Styling Cepat

| Class          | Fungsi                          |
| -------------- | ------------------------------- |
| `text-center`  | Teks rata tengah                |
| `mt-3`, `mb-2` | Margin top 3, margin bottom 2   |
| `bg-primary`   | Background biru                 |
| `text-white`   | Teks putih                      |
| `rounded`      | Membuat sudut elemen melengkung |

---

## 🔚 Kesimpulan

Dengan Bootstrap, kamu bisa membangun website yang tampil rapi dan profesional tanpa harus menulis CSS dari nol. Cukup pahami grid system, komponen dasar, dan class-class utility-nya — maka proses development akan jauh lebih cepat!

---