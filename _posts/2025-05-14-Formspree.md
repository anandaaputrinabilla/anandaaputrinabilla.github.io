---
layout: post
title: "Formspree"
---
Penjelasan tentang Formspree

![Formspree](/assets/images/htmlgambar.png)
---

# 1. **Apa itu Formspree?**

Formspree adalah layanan backend gratis (hingga batas tertentu) yang memungkinkan kamu mengirim data form HTML ke email tanpa perlu membuat server sendiri.

## 1.1. **Fungsi Utama Formspree**

- Mengirimkan data form ke email.
- Mudah diintegrasikan dengan HTML statis.
- Tidak perlu PHP, Node.js, atau backend lainnya.
- Mendukung AJAX dan integrasi dengan Zapier.

---

# 2. **Cara Menggunakan Formspree**

## 2.1. **Langkah Dasar**

1. Buka [https://formspree.io](https://formspree.io) dan daftar/login.
2. Buat form baru dan salin endpoint URL yang diberikan (biasanya seperti `https://formspree.io/f/{form_id}`).
3. Tempel ke tag `<form>` HTML-mu.

---

## 2.2. **Contoh Form HTML**

```html
<form action="https://formspree.io/f/yourFormID" method="POST">
  <label>
    Nama:
    <input type="text" name="nama">
  </label>
  <label>
    Email:
    <input type="email" name="email">
  </label>
  <label>
    Pesan:
    <textarea name="pesan"></textarea>
  </label>
  <button type="submit">Kirim</button>
</form>
````

> Ganti `yourFormID` dengan ID form kamu di Formspree.

---

# 3. **Fitur Tambahan**

## 3.1. **Redirect Setelah Submit**

Tambahkan atribut `data` untuk redirect:

```html
<form action="https://formspree.io/f/yourFormID" method="POST">
  <input type="hidden" name="_redirect" value="https://example.com/thanks.html">
  ...
</form>
```

## 3.2. **Tampilan AJAX Tanpa Reload**

```html
<script>
  const form = document.querySelector("form");
  form.addEventListener("submit", async (e) => {
    e.preventDefault();
    const data = new FormData(form);
    const response = await fetch(form.action, {
      method: form.method,
      body: data,
      headers: {
        'Accept': 'application/json'
      }
    });
    if (response.ok) {
      alert("Terima kasih, pesanmu sudah dikirim!");
      form.reset();
    } else {
      alert("Terjadi kesalahan. Coba lagi.");
    }
  });
</script>
```

---

# 4. **Keamanan dan Validasi**

* Gunakan `required` untuk validasi dasar.
* Gunakan CAPTCHA (reCAPTCHA) jika tersedia di akun Formspree Premium.
* Batasi form hanya dari domain tertentu lewat dashboard Formspree.

---

# 5. **Kesimpulan**

* Formspree sangat cocok untuk form kontak di web statis.
* Tidak perlu backend untuk mengirimkan data ke email.
* Mudah diintegrasikan dan bisa digunakan gratis dengan batas tertentu.
* Mendukung AJAX, validasi, dan integrasi lanjutan.

Dengan Formspree, kamu bisa membangun form profesional tanpa perlu server atau database sendiri.

```