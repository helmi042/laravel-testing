# Laravel Testing

Starter project Laravel 13 dengan Inertia.js, Vue 3, TypeScript, dan Laravel Fortify. Saat ini project masih berupa fondasi aplikasi dengan fitur autentikasi, halaman pengaturan akun, dan dashboard placeholder.

## Stack

- PHP 8.3+
- Laravel 13
- Laravel Fortify
- Inertia.js 2
- Vue 3 + TypeScript
- Vite
- Tailwind CSS 4
- Pest
- Laravel Boost

## Fitur Saat Ini

- Register, login, logout
- Reset password
- Email verification
- Two-factor authentication
- Profile settings
- Security settings
- Appearance settings
- Dashboard dasar

## Prasyarat

- PHP 8.3 atau lebih baru
- Composer
- Node.js dan npm
- SQLite
- Laravel Herd (opsional, untuk local web server)

## Instalasi

### Opsi cepat

```sh
composer setup
```

Script di atas akan:

- install dependency PHP
- membuat file `.env` jika belum ada
- generate app key
- menjalankan migrasi
- install dependency frontend
- build asset frontend

### Opsi manual

```sh
copy .env.example .env
composer install
npm install
php artisan key:generate
type nul > database\database.sqlite
php artisan migrate
npm run build
```

Catatan:

- Secara default project ini memakai SQLite.
- Session, cache, dan queue juga menggunakan database.

## Menjalankan Project

### Dengan script development Laravel

```sh
composer run dev
```

Script ini akan menjalankan:

- Laravel app server
- queue listener
- Vite dev server

### Dengan Laravel Herd

Jika Anda memakai Laravel Herd, project akan tersedia melalui domain `.test` sesuai nama folder project. Dalam mode ini biasanya cukup jalankan:

```sh
npm run dev
```

## Testing dan Quality Check

```sh
composer test
```

Perintah lain yang tersedia:

```sh
npm run lint:check
npm run format:check
npm run types:check
vendor/bin/pint --dirty
```

## Struktur Singkat

- `app/` - logic backend Laravel
- `resources/js/` - halaman dan komponen Inertia Vue
- `routes/` - route web dan settings
- `database/` - migration, factory, seeder
- `tests/` - test Pest

## Catatan

- Laravel Boost sudah dikonfigurasi untuk Codex dan Herd MCP.
- Project ini masih berada pada tahap starter kit, jadi landing page dan dashboard masih belum berisi fitur bisnis khusus.
