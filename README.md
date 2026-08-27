# JIS Documentation

Dokumentasi resmi untuk [JIS](https://github.com/jegex/jis) — CMS & Toko Digital berbasis Laravel.

## Tentang

Repo ini berisi source code dokumentasi JIS yang dibangun dengan [Mintlify](https://mintlify.com). Dokumentasi mencakup:

- **Setup** — instalasi, konfigurasi, deployment
- **Admin Guide** — panduan menggunakan panel admin (Filament v5)
- **User Guide** — pandangan dari sisi pelanggan (checkout, download, profil)
- **Developer** — development workflow, testing, commands
- **Reference** — enums, environment variables, API, permissions

## Lokal Development

```bash
# Install Mintlify CLI
npm i -g mint

# Jalankan dev server
mint dev

# Buka http://localhost:3000
```

## Struktur Folder

```text
jis-docs/
├── docs.json              # Navigasi & konfigurasi site
├── index.mdx              # Homepage
├── quickstart.mdx         # Quick start guide
├── changelog.mdx          # Changelog
├── admin-panel/           # Panduan admin panel
│   ├── overview.mdx
│   ├── ecommerce/         # Products, orders, coupons
│   ├── content/           # Posts, categories, tags, pages
│   ├── users/             # User management
│   ├── mail/              # Email templates, logs, newsletter
│   ├── settings/          # Site settings, SEO
│   ├── projects.mdx
│   └── homepage-builder.mdx
├── user-portal/           # Panduan user/customer
│   ├── overview.mdx
│   ├── public/            # Homepage, catalog, blog
│   ├── auth/              # Login, register, 2FA, passkeys
│   ├── checkout/          # Checkout, payment result
│   └── customer/          # Dashboard, downloads, profile
├── configuration/         # Konfigurasi aplikasi
├── deployment/            # Deployment guides
├── development/           # Developer docs (testing, commands)
├── reference/             # Enums, env vars, API, permissions
└── seo/                   # Sitemap, meta tags
```

## Menambah Halaman Baru

1. Buat file `.mdx` di folder yang sesuai
2. Tambahkan entry ke `docs.json` di posisi navigasi yang tepat
3. Pastikan path di `docs.json` cocok dengan lokasi file (tanpa ekstensi `.mdx`)

## Validasi

Pastikan:
- Setiap entry di `docs.json` punya file `.mdx` yang valid
- Tidak ada duplicate navigation entry
- Internal links menggunakan path yang benar (contoh: `/features/payments`)

## Deploy

Dokumentasi otomatis ter-deploy ke production setelah push ke branch default melalui GitHub App Mintlify.

## Source Code Aplikasi

Source code JIS ada di repo terpisah: [jegex/jis](https://github.com/jegex/jis)
