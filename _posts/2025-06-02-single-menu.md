---
layout: post
title: "Single Menu"
---
Penjelasan tentang Single Menu

![Single Menu](/assets/images/htmlgambar.png)
---

## 📌 Apa Itu Single Menu?

**Single Menu** adalah jenis antarmuka interaktif yang hanya memperbolehkan pengguna memilih satu aksi atau satu opsi dari beberapa pilihan yang tersedia. Menu ini umum digunakan dalam aplikasi web, desktop, maupun mobile—terutama saat pengguna perlu membuat pilihan yang eksklusif.

---

## 🧩 Jenis-Jenis Komponen Single Menu

### 1. 🎯 **Radio Button**

Radio Button digunakan ketika hanya satu opsi yang boleh dipilih dari sekumpulan opsi.

**Kapan digunakan?**
- Pemilihan jenis kelamin
- Memilih metode pengiriman

**Contoh HTML:**

```html
<p>Jenis Kelamin:</p>
<input type="radio" name="gender" value="pria" id="pria">
<label for="pria">Pria</label>
<input type="radio" name="gender" value="wanita" id="wanita">
<label for="wanita">Wanita</label>
````

---

### 2. 🟢 **Toggle Button**

Toggle Button adalah tombol yang dapat mengubah status antara aktif dan tidak aktif (on/off).

**Fungsi:**

* Mengaktifkan atau menonaktifkan fitur
* Memberi pengalaman visual seperti saklar

**Contoh HTML:**

```html
<button onclick="this.classList.toggle('aktif')">Toggle Fitur</button>
```

---

### 3. ☑️ **Checkbox**

Checkbox memungkinkan pengguna memilih **lebih dari satu opsi** secara bersamaan.

**Penggunaan Umum:**

* Memilih hobi
* Memilih layanan tambahan

**Contoh HTML:**

```html
<p>Hobi:</p>
<input type="checkbox" id="membaca" name="hobi" value="Membaca">
<label for="membaca">Membaca</label>
<input type="checkbox" id="musik" name="hobi" value="Musik">
<label for="musik">Musik</label>
```

---

### 4. 📋 **Dropdown (Select Menu)**

Dropdown menyajikan opsi dalam bentuk daftar tarik-turun (combo box) yang hemat ruang.

**Keunggulan:**

* Cocok untuk daftar panjang (misalnya daftar kota)
* Menjaga antarmuka tetap rapi

**Contoh HTML:**

```html
<label for="kota">Pilih Kota:</label>
<select name="kota" id="kota">
  <option value="medan">Medan</option>
  <option value="makassar">Makassar</option>
  <option value="bali">Bali</option>
</select>
```

---

## 📊 Tabel Perbandingan Komponen

| Komponen      | Pilihan Tunggal | Pilihan Ganda      | Bentuk Visual |
| ------------- | --------------- | ------------------ | ------------- |
| Radio Button  | ✅               | ❌                  | Bulat         |
| Checkbox      | ❌               | ✅                  | Kotak         |
| Dropdown      | ✅               | ❌                  | Daftar        |
| Toggle Button | ✅ / Ganda       | Bergantung Konteks | Tombol        |

---

## 🔚 Kesimpulan

Setiap komponen Single Menu memiliki fungsinya masing-masing tergantung konteks aplikasi.

* **Radio Button** untuk pilihan tunggal
* **Toggle Button** untuk fitur aktif/nonaktif
* **Checkbox** untuk pilihan ganda
* **Dropdown** untuk pilihan tunggal dalam format ringkas