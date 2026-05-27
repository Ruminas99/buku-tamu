# Buku Tamu Pengunjung

Sistem informasi buku tamu berbasis Laravel untuk pencatatan pengunjung di Pengadilan Tata Usaha Negara Medan. Aplikasi ini dirancang untuk memudahkan registrasi tamu, pemantauan kehadiran, serta pembuatan laporan harian dan bulanan secara lebih rapi dan terstruktur.

## Ringkasan

Aplikasi ini berfokus pada pencatatan kunjungan berdasarkan kategori tamu, seperti tamu sidang, layanan PTSP, tamu dinas, dan tamu mahasiswa. Selain form input pengunjung, tersedia juga dashboard ringkas, daftar kehadiran berdasarkan nomor perkara, serta ekspor laporan ke Excel.

## Fitur Utama

- Dashboard utama dengan navigasi kategori kunjungan yang cepat.
- Form registrasi untuk:
  - Tamu Sidang
  - Layanan PTSP
  - Tamu Dinas
  - Tamu Mahasiswa
- Halaman kehadiran untuk melihat status tamu berdasarkan nomor perkara.
- Laporan harian yang menampilkan total tamu dan rincian kunjungan hari ini.
- Laporan bulanan untuk rekap kunjungan per periode.
- Export laporan ke Excel.
- Tampilan UI modern, responsif, dan lebih nyaman digunakan di desktop maupun perangkat mobile.

## Tumpukan Teknologi

- Laravel 10
- PHP 8.1+
- Blade Template
- Vite
- Maatwebsite Excel
- Laravel Sanctum

## Struktur Halaman

- `/dashboard` - Halaman utama navigasi kunjungan.
- `/pihak` - Form tamu sidang.
- `/ptsp` - Form layanan PTSP.
- `/dinas` - Form tamu dinas.
- `/mahasiswa` - Form tamu mahasiswa.
- `/kehadiran` - Daftar kehadiran berdasarkan nomor perkara.
- `/laporan` - Laporan harian.
- `/bulanan` - Laporan bulanan.

## Prasyarat

- PHP 8.1 atau lebih baru
- Composer
- Node.js dan npm
- Database MySQL atau MariaDB

## Instalasi

1. Clone repository ini.
2. Jalankan instalasi dependency backend dan frontend:

```bash
composer install
npm install
```

3. Salin file environment dan atur konfigurasi aplikasi:

```bash
Copy-Item .env.example .env
php artisan key:generate
```

4. Sesuaikan pengaturan database di file `.env`.
5. Jalankan migrasi database jika diperlukan:

```bash
php artisan migrate
```

6. Jalankan aplikasi pada dua terminal berbeda:

```bash
php artisan serve
npm run dev
```

## Cara Menggunakan

1. Buka halaman utama aplikasi.
2. Pilih kategori tamu sesuai kebutuhan kunjungan.
3. Isi form data pengunjung.
4. Lihat ringkasan data pada dashboard laporan.
5. Gunakan menu laporan harian atau bulanan untuk rekap dan ekspor data.

## Tangkapan Layar

Bagian ini menampilkan screenshot hasil website yang disimpan di folder `public/docs/screenshots/`.

### Dashboard

![Dashboard utama](public/docs/screenshots/dashboard.png)

### Form Kunjungan

![Form tamu sidang](public/docs/screenshots/form-pihak.png)

### Laporan Harian

![Laporan harian](public/docs/screenshots/laporan-harian.png)

### Kehadiran

![Halaman kehadiran](public/docs/screenshots/kehadiran.png)

## Catatan Pengembangan

- Aplikasi memakai Blade untuk render halaman.
- Export laporan menggunakan library Excel.
- Struktur route sudah dipisah berdasarkan kebutuhan kunjungan dan laporan.

## Lisensi

Proyek ini menggunakan lisensi MIT.
