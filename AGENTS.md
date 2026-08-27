# Documentation project instructions

## About this project

- Documentation site for [JIS](https://github.com/jegex/jis) — Laravel-based digital product CMS & shop
- Built on [Mintlify](https://mintlify.com) — pages are MDX files with YAML frontmatter
- Configuration lives in `docs.json`
- Source code repo: [jegex/jis](https://github.com/jegex/jis)

## Language Policy

| Context | Language |
| --- | --- |
| **Navigation & UI labels** | English (Getting Started, Admin Guide, User Guide, Developer, Reference) |
| **Page titles** | English |
| **Content body** | Bahasa Indonesia |
| **Code blocks & commands** | English (as-is) |
| **Technical terms** | Keep English if no established Indonesian equivalent (e.g., "queue", "middleware", "slug", "checkout") |

This is a deliberate editorial decision, not an oversight. The navigation uses English for consistency with the tech ecosystem; the content uses Bahasa Indonesia for the target audience.

## Terminology

| Term | Usage |
| --- | --- |
| JIS | Nama produk, bukan singkatan lain |
| Admin Panel | Panel administrasi Filament, bukan "dashboard admin" |
| User Portal | Area pelanggan yang login, bukan "customer panel" |
| Checkout | Proses pembelian, bukan "pembayaran" (payment adalah bagian dari checkout) |
| Order | Transaksi/pesanan, konsisten pakai "order" bukan "pesanan" |
| Digital Product | Produk digital, bukan "produk unduhan" |
| Newsletter | Email massal ke subscriber, bukan "email blast" |

## Style Preferences

- Gunakan active voice dan second person ("kamu", "user")
- Kalimat singkat — satu ide per kalimat
- Sentence case untuk headings
- Bold untuk UI elements: Klik **Settings**
- Code formatting untuk file names, commands, paths, dan code references
- Screenshot hanya jika ada perubahan visual signifikan yang sulit dijelaskan teks
- Gunakan komponen Mintlify (`<Steps>`, `<Warning>`, `<Tip>`, `<Info>`) untuk struktur

## Content Boundaries

**Didokumentasikan:**
- Setup & konfigurasi aplikasi
- Fitur admin panel (Filament resources)
- User-facing features (checkout, download, profil)
- Development workflow
- Deployment guides
- API reference & environment variables

**Tidak didokumentasikan:**
- Internal implementation details yang tidak relevan untuk user/developer
- Code architecture detail (itu untuk source code, bukan docs)
- Perubahan minor/cosmetic

## Adding Pages

1. Buat file `.mdx` di folder yang sesuai
2. Tambahkan entry ke `docs.json` — pastikan path cocok dengan lokasi file
3. Validasi tidak ada duplicate navigation entry
4. Gunakan frontmatter yang konsisten:
   ```yaml
   ---
   title: "Judul Halaman"
   description: "Deskripsi singkat untuk SEO"
   ---
   ```

## Validation Rules

Sebelum push, pastikan:
- [ ] Setiap entry di `docs.json` punya file `.mdx` yang valid
- [ ] Tidak ada duplicate navigation entry
- [ ] Internal links (`/path/to/page`)指向 halaman yang ada
- [ ] Environment variables yang didokumentasi sesuai `.env.example` source code
- [ ] Route yang didokumentasi sesuai `route:list` source code
