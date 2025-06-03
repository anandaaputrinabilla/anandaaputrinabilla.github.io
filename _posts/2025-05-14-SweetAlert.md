---
layout: post
title: "SweetAlert"
---
Penjelasan tentang SweetAlert

![SweetAlert](/assets/images/htmlgambar.png)
---

# 1. **Apa itu SweetAlert?**

SweetAlert adalah pustaka JavaScript yang digunakan untuk menampilkan popup atau alert dengan tampilan yang lebih menarik dan interaktif dibandingkan alert bawaan browser.

## 1.1. **Fungsi Utama SweetAlert**

- Menampilkan pesan konfirmasi atau notifikasi dengan desain yang bagus.
- Mendukung berbagai jenis ikon: success, error, warning, info, question.
- Bisa dikustomisasi dengan tombol, animasi, dan input.

---

# 2. **Cara Menggunakan SweetAlert**

## 2.1. **Menambahkan SweetAlert ke Proyek**

Tambahkan script berikut di bagian `<head>` atau sebelum `</body>`:

```html
<script src="https://cdn.jsdelivr.net/npm/sweetalert2@11"></script>
````

## 2.2. **Contoh Penggunaan Dasar**

```html
<script>
  Swal.fire('Hello World!');
</script>
```

## 2.3. **Dengan Judul, Teks, dan Ikon**

```html
<script>
  Swal.fire({
    title: 'Berhasil!',
    text: 'Data telah disimpan.',
    icon: 'success',
    confirmButtonText: 'Oke'
  });
</script>
```

---

# 3. **Contoh Konfirmasi Aksi**

Misalnya ingin konfirmasi sebelum menghapus data:

```html
<script>
  function hapusData() {
    Swal.fire({
      title: 'Yakin ingin menghapus?',
      text: 'Data yang sudah dihapus tidak bisa dikembalikan!',
      icon: 'warning',
      showCancelButton: true,
      confirmButtonColor: '#3085d6',
      cancelButtonColor: '#d33',
      confirmButtonText: 'Ya, hapus!'
    }).then((result) => {
      if (result.isConfirmed) {
        Swal.fire(
          'Terhapus!',
          'Data telah berhasil dihapus.',
          'success'
        );
      }
    });
  }
</script>
```

---

# 4. **Kustomisasi Lanjutan**

SweetAlert bisa dikustomisasi:

* **Timer otomatis tertutup:**

```js
Swal.fire({
  title: 'Auto close!',
  text: 'Akan tertutup dalam 2 detik.',
  timer: 2000,
  showConfirmButton: false
});
```

* **Dengan input form:**

```js
Swal.fire({
  title: 'Masukkan nama',
  input: 'text',
  showCancelButton: true,
  inputPlaceholder: 'Nama kamu'
});
```

---

# 5. **Kesimpulan**

* SweetAlert adalah alternatif modern dari `alert()`.
* Memberikan tampilan yang lebih interaktif dan profesional.
* Mudah digunakan hanya dengan beberapa baris JavaScript.
* Cocok digunakan untuk notifikasi, konfirmasi, hingga input pengguna.

Dengan menggunakan SweetAlert, pengalaman pengguna di web akan menjadi jauh lebih baik dan menarik.

```