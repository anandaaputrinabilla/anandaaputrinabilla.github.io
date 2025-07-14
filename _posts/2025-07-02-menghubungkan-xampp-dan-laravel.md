---
layout: post
title: "XAMPP dan Laravel"
---

Penjelasan tentang Menghubungkan XAMPP dan Laravel

![Single Menu](/assets/images/htmlgambar.png)

---

# 🌐 Koneksi Laravel ke Database XAMPP untuk Form Pendaftaran

Tutorial ini menjelaskan cara menghubungkan Laravel dengan database MySQL yang berjalan di XAMPP, khususnya untuk aplikasi **form pendaftaran siswa**.

---

## 🔧 Langkah 1: Pastikan XAMPP Aktif

1. Buka **XAMPP Control Panel**
2. Aktifkan modul:
   - ✅ **Apache**
   - ✅ **MySQL**
3. Buka browser → akses `http://localhost/phpmyadmin`

---

## 🛢️ Langkah 2: Buat Database di phpMyAdmin

1. Masuk ke `http://localhost/phpmyadmin`
2. Klik menu **Database**
3. Buat database baru, misalnya: `db_siswa`

---

## ⚙️ Langkah 3: Konfigurasi File `.env` Laravel

Buka file `.env` di root folder project Laravel kamu (`latihvel/.env`) dan ubah bagian berikut:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=db_siswa
DB_USERNAME=root
DB_PASSWORD=
Keterangan:

Key	Keterangan
DB_CONNECTION	Tipe database, default mysql
DB_HOST	Alamat server DB, default 127.0.0.1
DB_PORT	Port MySQL, default 3306
DB_DATABASE	Nama database yang tadi kamu buat
DB_USERNAME	Username database, default root
DB_PASSWORD	Password MySQL, biasanya kosong (default)

📌 Pastikan database db_siswa sudah dibuat sebelum lanjut.

🛠️ Langkah 4: Migrasi Struktur Tabel ke Database
Laravel menggunakan fitur migration untuk membuat tabel secara otomatis dari file.

Jalankan perintah:

bash
Copy
Edit
php artisan migrate
🧠 Apa yang terjadi?

Laravel membaca semua file migrasi di database/migrations

Menjalankan perintah CREATE TABLE ke database db_siswa

Tabel-tabel berikut akan dibuat secara otomatis:

users

password_resets

personal_access_tokens

dan lainnya jika kamu punya migrasi tambahan

📥 Langkah 5: Isi Data Form ke Database
Misalnya kamu memiliki form pendaftaran di file:

bash
Copy
Edit
resources/views/siswa/create.blade.php
Dan sudah membuat model serta controller dengan perintah:

bash
Copy
Edit
php artisan make:model Siswa -mcr
Kode untuk menyimpan data ke database (SiswaController.php):

php
Copy
Edit
public function store(Request $request)
{
    Siswa::create([
        'nama' => $request->nama,
        'alamat' => $request->alamat,
        'agama' => $request->agama,
        'sekolah_asal' => $request->sekolah_asal,
        'jenis_kelamin' => $request->jenis_kelamin,
    ]);
    return redirect()->route('siswa.index');
}
Form HTML pada create.blade.php:

blade
Copy
Edit
<form action="{{ route('siswa.store') }}" method="POST">
  @csrf
  <input name="nama" placeholder="Nama"><br>
  <input name="alamat" placeholder="Alamat"><br>
  <input name="agama" placeholder="Agama"><br>
  <input name="sekolah_asal" placeholder="Sekolah Asal"><br>
  <select name="jenis_kelamin">
    <option value="Laki-laki">Laki-laki</option>
    <option value="Perempuan">Perempuan</option>
  </select><br>
  <button type="submit">Simpan</button>
</form>
✅ Selesai! Coba Jalankan Aplikasi
Jalankan Laravel:

bash
Copy
Edit
php artisan serve
Buka browser dan akses:

arduino
Copy
Edit
http://127.0.0.1:8000/siswa/create
Isi form → klik simpan → data akan tersimpan di database db_siswa

🧠 Tips Tambahan
Jalankan php artisan migrate:fresh untuk reset dan migrasi ulang

Lihat data langsung via phpMyAdmin → tabel siswas

Tambahkan validasi input di controller agar lebih aman

Gunakan @csrf di setiap form untuk perlindungan CSRF

📌 Struktur Folder View (Contoh)
pgsql
Copy
Edit
resources/views/
├── siswa/
│   ├── create.blade.php
│   ├── edit.blade.php
│   ├── index.blade.php
│   └── dashboard.blade.php