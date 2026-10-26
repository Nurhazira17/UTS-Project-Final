# Nusa Stationery — Sistem Inventaris dan Penjualan

Aplikasi web berbasis Laravel untuk membantu operasional toko alat tulis, mulai dari pengelolaan produk hingga pencatatan transaksi.

## Fitur Utama

- Dashboard ringkasan inventaris dan penjualan.
- Pengelolaan produk dan kategori.
- Pengelolaan data pemasok.
- Pencatatan stok masuk dan penjualan.
- Ringkasan serta laporan transaksi.
- Portal pelanggan untuk melihat produk dan membuat pesanan.
- Riwayat pesanan pelanggan dan tampilan struk yang dapat dicetak melalui browser.
- Tiga role aplikasi: **Admin**, **Staff**, dan **Pelanggan**.

## Teknologi

- PHP
- Laravel
- SQLite
- Composer
- Blade / HTML / CSS

## Persyaratan

Pastikan PHP, Composer, dan ekstensi PHP yang dibutuhkan Laravel/SQLite telah tersedia. Periksa instalasi dengan:

```powershell
php --version
composer --version
```

## Cara Instalasi di Windows

1. Ekstrak folder proyek.
2. Buka terminal di folder proyek yang memiliki file `artisan` dan `composer.json`.
3. Instal dependency:

   ```powershell
   composer install
   ```

4. Buat file konfigurasi lokal jika belum ada:

   ```powershell
   Copy-Item .env.example .env
   ```

   Jika `.env` sudah ada, jangan menimpanya.

5. Buat application key:

   ```powershell
   php artisan key:generate
   ```

6. Pastikan konfigurasi `.env` menggunakan SQLite. Umumnya:

   ```dotenv
   DB_CONNECTION=sqlite
   DB_DATABASE=database/database.sqlite
   ```

   Jika `database/database.sqlite` belum ada, buat file kosong:

   ```powershell
   New-Item database/database.sqlite -ItemType File
   ```

7. Jalankan migrasi dan data demo:

   ```powershell
   php artisan migrate --seed
   ```

8. Jalankan server lokal:

   ```powershell
   php artisan serve
   ```

9. Buka `http://127.0.0.1:8000` di browser.

## Role Pengguna

- **Admin** — akses administrasi dan pengelolaan data utama sesuai implementasi aplikasi.
- **Staff** — operasional inventaris dan transaksi sesuai implementasi aplikasi.
- **Pelanggan** — melihat katalog, membuat pesanan, serta melihat riwayat/struk sesuai implementasi aplikasi.

## Akun Demo

Jika seeder proyek menyediakan akun demo, gunakan kredensial yang tercantum pada halaman login atau file panduan instalasi. Jangan gunakan kredensial demo sebagai password produksi.

## Catatan

- Fitur yang memerlukan integrasi eksternal, seperti pembayaran online, tidak dianggap aktif kecuali telah dikonfigurasi dan diuji.
- Uji login setiap role, perubahan stok, transaksi, laporan, dan pencetakan struk sebelum demonstrasi atau pengumpulan.
- Sesuaikan dokumentasi ini apabila nama database, route, atau fitur aktual pada kode berbeda.

## Pengembangan

Proyek ini dibuat untuk pembelajaran/pengembangan tugas akademik. Jelaskan sumber kode atau template pihak ketiga yang digunakan sesuai ketentuan lisensinya dan aturan dosen.
